Here are the sorted questions and answers:

1.  If you want to delete user details using JDBC API, which of the following is correct?
    1.  Answer: D. PreparedStatement with executeUpdate()
2.  How to deploy a web application listener within a web application?
    1.  Answer: D. A or C
3.  How many ServletConfig & ServletContext objects will be created by the web container?
    1.  Answer: B. One per servlet & one per web application
4.  Consider the following 2 servlets.

```
@WebServlet(value="/s1", loadOnStartup=1) 
public class FirstServlet extends HttpServlet {...} 

@WebServlet(value="/s2") 
public class SecondServlet extends HttpServlet {...}
```

1.  Which of the following is true?

    Answer: C. Web container invokes the init method of the first servlet at web app startup.

2.  Which of the following attributes are inherently thread-unsafe?
    1.  Answer: D. Application scoped attributes
3.  What will be the output if the client sends the following request to test1.jsp?

```
http://host:port/test_web/test1.jsp?pid=101&type=electronic&name=tv
```

1.  Answer: D. Name: tv Type:
2.  To execute a stored procedure or a stored function in JDBC, what will you use?
    1.  Answer: C. CallableStatement with execute
3.  Default type of ResultSet is
    1.  Answer: D. scrollable & read only
4.  While using request chaining scenario in page navigation, what should be the minimum scope of server-side attributes?
    1.  Answer: B. request scope
5.  Which of the following is not accessible via EL syntax?
    1.  Answer: D. session
6.  Which of the following is the default behavior of Spring Security?
    1.  Answer: D. All of the above
7.  If you want to achieve complete DB normalization as per the Object world, which JPA inheritance strategy will you choose?
    1.  Answer: C. Joined Table inheritance
8.  If you want to skip a field or a property during serialization but add it during deserialization in a RESTful web service, what will you use?
    1.  Answer: A. @JsonProperty(access=ACCESS.WRITE_ONLY)
9.  In Hibernate, many-to-many association, which of the following is true?
    1.  Answer: D. The default fetch type of this type of association is lazy.
10. Which of the following is true regarding the Spring container?
    1.  Answer: B. In a standalone application, you can't launch a Spring container
11. Spring supports
    1.  Answer: D. All of the above
12. In Front Controller based MVC, what is the role of the front controller?
    1.  Answer: C. Centralized dispatcher
13. What will happen in the following Hibernate code, if the user id is annotated with @Id & @GeneratedValue?
    1.  Answer: B. Throws PersistentObjectException
14. In a bidirectional one-to-many association, what will happen if the mappedBy attribute is not specified?
    1.  Answer: C. Hibernate will create an additional table, having PKs of both the tables.
15. What will happen for the following code, when you bootstrap Hibernate?
    1.  Answer: C. Table will be created with id, code & stockDesc columns
16. In a many-to-many relationship between Book & Author, what will happen if you access System.out.println(a1.getBooks()) after executing a JPQL query?
    1.  Answer: B. Hibernate throws LazyInitializationException
17. Which of the following is true?
    1.  Answer: C. L1 cache is implicitly enabled in Hibernate.
18. What can be said regarding the saveOrUpdate method of Hibernate?
    1.  Answer: C. A & B
19. What will happen in the following Hibernate code sample if the account a with id=100 exists in DB, with balance=5000?
    1.  Answer: B. Balance will be 7000
20. Which default fetching policy does JPA use for one-to-one & one-to-many?
    1.  Answer: A. Eager & Lazy
21. In Spring Hibernate based web application, what can you say regarding Session's load method?
    1.  Answer: A. Returns a proxy by default
22. In a many-to-many mapping, how will you specify the name of the association table, containing a composite primary key?
    1.  Answer: C. @JoinTable
23. In a Spring application class, which of the following is not a part of @SpringBootApplication?
    1.  Answer: C. @EnableWebMvc
24. How will you create a composite primary key class in JPA or Hibernate?
    1.  Answer: A. @Embeddable
25. Which of the following is true regarding servlet filters?
    1.  Answer: D. Typical use case of filters is to write cross-cutting concern.
26. What will you propose to avoid SQL injection attack?
    1.  Answer: A. Use PreparedStatement API to set IN parameters.
27. Which of the following is true regarding Spring Security?
    1.  Answer: D. If a hacker tampers with JWT, the Restful web service will detect an invalid JWT signature.
