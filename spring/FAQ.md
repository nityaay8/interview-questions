### How do you initialize Application context or Bean Factory context in Spring

    <beans>   
      <bean id="department" class="com.Department"></bean>   
    </beans>  

   ApplicationContext ctx = new ClassPathXmlApplicationContext( "beans.xml");
   
   BeanFactory
   
    Resource res = new FileSystemResource("beans.xml");
    XmlBeanFactory factory = new XmlBeanFactory(res);
    or

    ClassPathResource res = new ClassPathResource("beans.xml");
    XmlBeanFactory factory = new XmlBeanFactory(res);
   
   https://docs.spring.io/spring-framework/docs/1.2.x/reference/beans.html
   
### difference between BeanFactory and Application Context.

|Bean Factory|Application Context|
|------------|-------------------|
|it supports lazy initialization, bean object will be created when get bean mehod inoked.|it supports eager initialization, bean objets will be created at the time of initilization |
|it is suitalble for stand alone appliaions.|it is suialble to all appliaions (sandalong , web and enepise application|
|it supports singleton and protoype scopes|it supports all sopes (singleon,protoype,request,session, global session)|
|it supports basic features and less memory|it supports all features (i18n,security and transactions)|
|it does not support autowiring though to annotaions|it supports annotation based on configuration|


### how do you create object using factroy patteren in sping


### sping bean life cycle

  ![image](https://user-images.githubusercontent.com/20619643/192209460-31018af7-81ab-4085-91e9-247501487912.png)


### what is AOP.

