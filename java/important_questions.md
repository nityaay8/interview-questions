## JAVA Class loader
https://www.digitalocean.com/community/tutorials/java-classloader

**Bootstrap Class Loader** – It loads JDK internal classes. It loads rt.jar and other core classes for example java.lang.* package classes.  

**Extensions Class Loader** – It loads classes from the JDK extensions directory, usually $JAVA_HOME/lib/ext directory.  

**System Class Loader** – This classloader loads classes from the current classpath. We can set classpath while invoking a program using -cp or -classpath command line option.  

## SOLID PRINCIPLES
https://stackify.com/interface-segregation-principle/

## immutability
https://www.linkedin.com/pulse/20140528113353-16837833-6-benefits-of-programming-with-immutable-objects-in-java/

  * Immutable objects are thread-safe so you will not have any synchronization issues.
  * Immutable objects are good Map keys and Set elements, since these typically do not change once created.
  * Immutability makes it easier to write, use and reason about the code (class invariant is established once and then unchanged)
  * Immutability makes it easier to parallelize your program as there are no conflicts among objects.
  * The internal state of your program will be consistent even if you have exceptions.
  * References to immutable objects can be cached as they are not going to change.

## inheriteance vs composistion

https://stackoverflow.com/questions/2399544/difference-between-inheritance-and-composition

https://www.digitalocean.com/community/tutorials/composition-vs-inheritance
