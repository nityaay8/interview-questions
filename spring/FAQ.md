## How do you initialize Application context or Bean Factory context in Spring

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
   
## difference between BeanFactory and Application Context.

|Bean Factory|Application Context|
|---------------------------------|

## how do you create object using factroy patteren in sping


## sping bean life cycle

  ![image](https://user-images.githubusercontent.com/20619643/192209460-31018af7-81ab-4085-91e9-247501487912.png)


## what is AOP.

