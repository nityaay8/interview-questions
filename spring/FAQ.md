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
   
### Difference between BeanFactory and Application Context.

|Bean Factory|Application Context|
|------------|-------------------|
|it supports lazy initialization, bean object will be created when get bean mehod inoked.|it supports eager initialization, bean objets will be created at the time of initilization |
|it is suitalble for stand alone appliaions.|it is suialble to all appliaions (sandalong , web and enepise application|
|it supports singleton and protoype scopes|it supports all sopes (singleon,protoype,request,session, global session)|
|it supports basic features and less memory|it supports all features (i18n,security and transactions)|
|it does not support autowiring though to annotaions|it supports annotation based on configuration|


### What is circular dependency
    A circular dependency occurs when a bean A depends on another bean B, and the bean B depends on bean A as well:

    Bean A → Bean B → Bean A
    
    If we try to run this test, we will get this exception:
    
        BeanCurrentlyInCreationException: Error creating bean with name 'circularDependencyA':
        Requested bean is currently in creation: Is there an unresolvable circular reference?
        
   * The Workarounds
     * Redesign the components
        When we have a circular dependency, it’s likely we have a design problem and that the responsibilities are not well separated
     * Use @Lazy
     A simple way to break the cycle is by telling Spring to initialize one of the beans lazily. So, instead of fully initializing the bean, 
     it will create a proxy to inject it into the other bean. The injected bean will only be fully created when it’s first needed.
     
    code:
    
            @Component
        public class CircularDependencyA {

            private CircularDependencyB circB;

            @Autowired
            public CircularDependencyA(@Lazy CircularDependencyB circB) {
                this.circB = circB;
            }
        }

### How do you create object using factroy patteren in sping
    * Spring treats a bean container as a factory that produces beans.
    * Each of the getBean methods is considered a factory method
    
  * Factory method hides the complex creation logic of object (with in a single method call)
  * https://www.baeldung.com/spring-beans-factory-methods
  
  * using annotation
      * https://stackoverflow.com/questions/33993063/annotation-based-servicelocatorfactorybean
      * https://github.com/nityaay8/interview-questions/blob/1b45574208e1ddc92619c32ec3848a6c3b68ff42/spring/spring_boot_factory_patteren.png



### Spring bean life cycle

  ![image](https://user-images.githubusercontent.com/20619643/192310428-1f87dded-fcb0-4acc-88c0-72c1624cf2ca.png)


### What is AOP.
    *Spring AOP is used to implementing the cross cutting concerns
    *Example Cross cutting concerns are Security,Logging and Transaction Management.
    
    *AOP Concepts
        * Join point
        * Advice
        * Pointcut
        * Introduction
        * Target Object
        * Aspect
        * Interceptor
        * AOP Proxy
        * Weaving
    
    https://www.javatpoint.com/spring-aop-tutorial
    

