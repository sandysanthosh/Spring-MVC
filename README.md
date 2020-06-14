### Spring-MVC

      1.add dependecies
      2.bean class
      3.create controller - BO
      4.empDAO - JDBC template
      5.web.xml-dispatcher servlet
      6.spring-servlet:prefix,suffix,user,pass,url,driver.datasource,template

#### JSP/servlet:

          @Autowired -search in <context:component-scan> - create a instance of service
          @Service
          @Controller
          @RequestMapping
          @ModelAttribute
          @PathVariable
          
####  Form tag:

    <%@ taglib prefix="form" uri="http://www.springframework.org/tags/form" %>  
    <%@ taglib uri="http://java.sun.com/jsp/jstl/core" prefix="c"%> 


#### Form:form:

        <form:form method="post" commandName="todo">

        <form : input type="text" name="desc" class =" form control" required="requirted">

        </form:form>


#### TodoController:

          @RequestMapping( Value ="/add-todo", method = "RequestMethod.POST")
          public String addToDo(ModelMap Model, Todo todo){
          service.addTodo("in28Minutes",todo.desc(), new Date(), model.clear());
          return "redirect:/list-todos";
          }

#### Jars:

            spring mvc
            tomcat-jasper
            servlet-api
            jstl
            mysql-connector-java
            spring-jdbc

#### Form tag:

      <form: form method="post" commandName="todo">
      <form:input path="name"/>

####  In controller:

      @RequestMapping( Value ="/add-todo", method="post")

      addToDo()

##### Form Tag:

              form:form
              form:input
              form:radiobutton
              form:checkbox
              form:password
              form:select
              form:textarea
              form:hidden

              <form:input path="name"/>
              <td>${emp.id}</td>

#### Spring JAXB:

####  Jars:

        spring Core Jar
        spring Web Jar

##### Employee.java:

          @XmlRootElements
          @XmlAttribute
          @XmlElement

##### applicaiton context.xml:

        <oxm:jaxb2-marshaller id="jaxbMarshallerBean">  
        <oxm:class-to-be-bound name="com.javatpoint.Employee"/>  
        </oxm:jaxb2-marshaller>

##### clientMain.java:

          ApplicationContext context = new ClassPathXmlApplicationContext("applicationContext.xml");
          Marshaller marshall = (Marshaller) context.getBean(jaxbMarshallerBean);


