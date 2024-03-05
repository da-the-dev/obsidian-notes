# Fundamentals
Relation is a made up of:
- Attributes (columns)
- Tuples (rows with data)
# Relational diagram
A diagram that represents the model
![[Pasted image 20240305212554.png|600]]
# Constraints
**1. Inherent Model-Based Constraints (Implicit Constraints)**
Constraints inherent in the definition/assumptions of a particular data model:
- Apply to every database using that data model.
- Example: In the relational model, a relation cannot have duplicate tuples.

**2. Schema-Based Constraints (Explicit Constraints)**
Constraints expressed in the schemas of the data model:
- Defined explicitly during database design.
- Examples include primary key constraints, foreign key constraints, and check constraints.

**3. Application-Based Constraints (Business Rules)**
Constraints enforced by the application programs:
- Reflect specific requirements and business rules.
- Typically implemented through application logic.
- Example: Validating user input against predefined business rules before data insertion.

**4. Semantic Integrity Constraints**
Application-specific restrictions unlikely to be expressible in Data Definition Language (DDL):
- Mechanisms like triggers and assertions in SQL can specify some of these constraints.
- Often verified within application programs.

**5. State vs. Transition Constraints**
- **State Constraints:** Define the constraints a valid state of the database must satisfy.
- **Transition Constraints:** Deal with state changes in the database.