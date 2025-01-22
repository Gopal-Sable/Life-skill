# Technical Paper: Spring MVC Framework

The Spring MVC Framework follows the Model-View-Controller architectural design pattern which works around the Front Controller i.e. the Dispatcher Servlet. The Dispatcher Servlet handles and dispatches all the incoming HTTP requests to the appropriate controller. It uses @Controller and @RequestMapping as default request handlers. The @Controller annotation defines that a particular class is a controller. @RequestMapping annotation maps web requests to Spring Controller methods.
## Key Components of Spring MVC

1. **Model**: The model represents the data of the application and the business logic. In Spring MVC, it can be any Java object that holds application data.
2. **View**: The view is responsible for rendering the model’s data to the user. Common view technologies used in Spring MVC include JSP (JavaServer Pages), Thymeleaf, and others.
3. **Controller**: The controller manages user input and works as an intermediary between the Model and the View. It processes user requests and returns the appropriate view for display.

## Spring MVC Architecture

Here’s a basic diagram showing the flow of data in a Spring MVC application:

![Spring MVC Architecture](https://media.geeksforgeeks.org/wp-content/uploads/20231106150237/Spring-MVC-Framework-Control-flow-Diagram.png)

## Workflow of a Spring MVC Application

1. **DispatcherServlet** intercepts HTTP requests and routes them to the appropriate controller.
2. The **Controller** processes the request, interacts with the **Model**, and returns a **View**.
3. The **View** displays the processed data to the user.

## Advantages of Spring MVC Framework

1. The container is used for the development and deployment of applications and uses a lightweight servlet.
2. It enables rapid and parallel development.
3. Development of the application becomes fast.
4. Easy for multiple developers to work together.
5. Easier to Update the application.
6. It is Easier to Debug because we have multiple levels in the application.

## Disadvantages of Spring MVC Framework

1. It has high complexity to develop the applications using this pattern.
2. It is not suitable for small applications which affect the application’s performance and design.


## Examples
### Spring MVC Controller

```java
@@Controller  
public class HelloGeek {  
@RequestMapping("/")  
    public String display()  
    {  
        return "hello";  
    }     
}  
```
### Spring MVC JSP View
```jsp
<!-- hello.jsp -->
<!DOCTYPE html>
<html>
<head>
    <title>Spring MVC Example</title>
</head>
<body>
    <h1>${message}</h1>
</body>
</html>
```
### Spring Configuration (XML-based)
```xml
<!-- spring-servlet.xml -->
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
                           http://www.springframework.org/schema/beans/spring-beans.xsd">

    <bean name="/hello" class="com.example.HelloController" />

</beans>
```
## References 
- [https://docs.spring.io/spring-framework/docs/3.2.x/spring-framework-reference/html/mvc.html](https://docs.spring.io/spring-framework/docs/3.2.x/spring-framework-reference/html/mvc.html)
- [GFG-https://www.geeksforgeeks.org/spring-mvc-framework/](https://www.geeksforgeeks.org/spring-mvc-framework/)
