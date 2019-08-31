##chapter1
    spring bean的创建和依赖注入
        构造方法创建
        工厂方式创建
        setter 方法注入
        构造方法注入
##chapter03a
    1 servlet 转发器使用org.springframework.web.servlet.DispatcherServlet 在web.xml 中配置 
    2 controller 在 spring.xml 中的配置
        name 使用path ;  class 使用 xxxcontroller
    3 使用 org.springframework.web.servlet.ModelAndView;
      org.springframework.web.servlet.mvc.Controller;    完成mvc 的功能
    4 controller 中只有一个 handleRequest 的action 方法 只能处理单一一个请求动作，而基于注解的controller可以同时处理多个请求动作  
    5 controller 的 handleRequest  通过以path形式指定view[name]  如 /WEB-INF/jsp/ProductDetails.jsp;
    
    注： spring 如何初始化
        1 tomcat 容器转发到org.springframework.web.servlet.DispatcherServlet ，
        2 spring 在DispatcherServlet 完成初始化
##chapter03b
    1 对chapter03a 改进
    2 controller 的 handleRequest  通过以name形式指定 view[name] 如 ProductForm, 
    ProductForm 是通过 ViewResolver 来进行解析
        <bean id="viewResolver" class="org.springframework.web.servlet.view.InternalResourceViewResolver">
            <property name="prefix" value="/WEB-INF/jsp/"/>
            <property name="suffix" value=".jsp"/>
        </bean>
