---
aliases:
  - Generalization
---
A superset of [[ER diagram]]
### Generalization
- **Definition:** Generalization is the process of combining lower-level entities to form a higher-level entity that contains the properties of all the generalized entities.
- **Approach:** It follows a bottom-up approach where two lower-level entities are combined.
- **Relation to Specialization:** Generalization is the reverse process of [[#specialization]], defining a general entity type from a set of specialized entity types.
- **Purpose:** It minimizes differences between entities by identifying common features.
![[Pasted image 20240305174335.png]]
### Specialization
- **Definition:** Specialization is a process that divides a group of entities into subgroups based on their characteristics.
- **Approach:** It follows a top-down approach, where one higher-level entity is broken down into two or more lower-level entities.
- **Purpose:** Specialization maximizes the difference between members of an entity by identifying unique characteristics or attributes.
- **Relationships:** It establishes superclass/subclass relationships by defining one or more subclasses for the superclass.
![[Pasted image 20240305174546.png]]
### Category (Union)
- **Definition:** Category represents a single superclass or subclass relationship with more than one superclass.
- **Participation:** It can involve total or partial [[participation]]. For instance, in car booking, the car owner can be a person, a bank (which holds a lien on a car), or a company.
- **Example:** In the context of car ownership, "Owner" is a subclass that is a subset of the union of three superclasses: Company, Bank, and Person. A category member must exist in at least one of its superclasses.
![[Pasted image 20240305182255.png]]
### Aggregation
- **Definition:** Aggregation represents a relationship between a whole object and its component parts.
- **Abstraction:** It abstracts a relationship between objects by viewing the relationship as an object itself.
- **Treatment:** It occurs when two entities are treated as a single entity, emphasizing the collective nature of their relationship.
![[Pasted image 20240305183016.png]]
### Specialization
**1. Disjointness Constraint:**
- Specifies that subclasses of the specialization must be disjoint.
- An entity can belong to at most one subclass of the specialization.
- Shown as "d" in EER diagrams.
- If not disjoint, specialization is overlapping, allowing entities to belong to more than one subclass.
- Overlapping is specified by "o" in EER diagrams.

**2. Completeness Constraint:**
- **Total**: Every entity in the superclass must belong to some subclass in the specialization.
  - Shown as a double line in EER diagrams.
- **Partial**: Allows entities not to belong to any subclass.
  - Represented by a single line in EER diagrams.

### Types of Specialization/Generalization

Hence, there are four types of specialization/generalization:
- Disjoint, total
- Disjoint, partial
- Overlapping, total
- Overlapping, partial