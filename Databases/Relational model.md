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
# Operations
Four main operation in a database:
- **<u><b>C</b></u>REATE** (INSERT in SQL)
- **<u><b>R</b></u>ETRIEVE** (SELECT in SQL)
- **<u><b>U</b></u>PDATE** (same in SQL)
- **<u><b>D</b></u>ELETE** (DROP in SQL)
These are the <u>CRUD</u> operations
Any model constraints must be preserved when these operations occur
## Operation constraints
### INSERT
- **Domain Constraint Violation**: some attribute value is not of correct domain
- **Entity Integrity Violation**: some attribute within a key of the new tuple has "value" null
- **Key Constraint Violation**: key of new tuple is same as key of already-existing tuple
- **Referential Integrity Violation**: foreign key of new tuple refers to non-existent tuple
**Solution:**
- Reject the insert request!
### DELETE
- **Referential integrity violation**: a tuple referring to the deleted one exists
**Solution:**
1. **Reject the Deletion:** Prevent the deletion if it would violate referential integrity.
2. **Cascade (or Propagate) Deletion:** Attempt to delete referencing tuples, along with those referencing them, recursively.
3. **Modify Foreign Key Attributes:** Update foreign key attribute values in referencing tuples to null or to valid values referencing different tuples.
### UPDATE
- **Key Constraint Violation:** Occurs when the primary key is changed to become the same as another tuple.
- **Referential Integrity Violation:**
    - Foreign key is changed, and the new value refers to a nonexistent tuple.
    - Primary key is changed, causing other tuples referring to it to violate the constraint.
**Solution:**
1. **Reject the Update:** Prevent the update if it would violate key or referential integrity.
2. **Modify Foreign Key Attributes:** Update foreign key attribute values in referencing tuples to null or valid values referencing different tuples.
## Transactions
Transactions allow us to "experiment" with the query. We can call whatever queries in whatever way we want, but the changes are applied **only** if transaction is **committed** as **is valid**.

- **Definition:** A transaction is an executing program comprising various database operations, including reading from the database and applying insertions, deletions, or updates.
- **Maintaining Valid State:**
  - At the end of the transaction, the database must be in a valid or consistent state that satisfies all constraints specified on the database schema.
- **Atomic Unit of Work:**
  - Transactions consist of retrievals and updates that form an atomic unit of work against the database.
## Relational algebra
[[Relational algebra|Best read in a separate note]]