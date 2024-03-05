1. Analyze -> [[ER diagram]]
2. Design -> TODO
3. Build
![[Pasted image 20240305165952.png]]
# Simplified overview of the database design process
1. **Requirements collection and analysis**
   Ask the client what the project is about. This gives an overview of what kind of functionality is required
2. **Conceptual design**
   Define the database structure. This is the time when [[ER diagram|ER diagrams]] & [[Relational model|relational diagrams]] are born. 
3. **Implementation of the database using a (commercial) DBMS**
   Now we use some DMBS system to implement the design into life
4. **Physical design phase**
   This is when we think how to optimize the database, so that it is always available. We might think about sharding to increase throughput for example, instancing to increase reliability, etc.
   
   