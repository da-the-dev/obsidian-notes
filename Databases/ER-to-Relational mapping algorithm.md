---
tags:
  - TODO
---
# Step 1. Mapping strong entity types
- For each [[Entity types#Strong entity|strong entity]] type $\textcolor{red}{E}$ in the entity relation schema, create a [[Relational model#Relation|relation]] $\textcolor{lightgreen}{R}$ that includes all the simple attributes of $\textcolor{red}{E}$.
- Choose one of the key attributes of $\textcolor{red}{E}$ as the [[Keys#Primary key|primary key]] for $\textcolor{lightgreen}{R}$.
- If the chosen key of $\textcolor{red}{E}$ is composite, the set of simple attributes that form it will together form the [[Keys#Primary key|primary key]] of $\textcolor{lightgreen}{R}$
# Step 2. Mapping weak entity types
- For each [[Entity types#Weak entity|weak entity]] type $\textcolor{aqua}{W}$ in the entity relation schema with owner entity type $\textcolor{red}{E}$, create a [[Relational model#Relation|relation]] $\textcolor{lightgreen}{R}$ and include attributes of $\textcolor{aqua}{W}$ as attributes of $\textcolor{lightgreen}{R}$.
- Include the [[Keys#Primary key|primary key]] attributes of the relation that correspond to the owner entity types as [[Keys#Foreign key|foreignf key]] attributes of $\textcolor{lightgreen}{R}$.
- The primary key of $\textcolor{lightgreen}{R}$ is the combination of the [[Keys#Primary key|primary key]] of the owner and the [[Keys#Partial key|partial key]] of the [[Entity types#Weak entity|weak entity]] type $\textcolor{aqua}{W}$.
# Step 3. Mapping of 1:1 relationships
For each binary 1:1 relationship type $\textcolor{lightgreen}{R}$ in the entity relation schema, identify the relations $\textcolor{orange}{S}$ and $\textcolor{orange}{T}$ that correspond to the entity types participating in $\textcolor{lightgreen}{R}$.

There are three possible approaches:
1. **[[Keys#Foreign key|Foreign key]] approach**: Choose one of the relations — say $\textcolor{orange}{S}$ — and include the [[Keys#Primary key|primary key]] of $\textcolor{orange}{T}$ as a [[Keys#Foreign key|foreign key]] in $\textcolor{orange}{S}$. It is better to choose an entity type with [[Participation#Total participation|total participation]] in $\textcolor{lightgreen}{R}$ in the role of $\textcolor{orange}{S}$.
	- Example: relation MANAGES is mapped by choosing the participating entity type DEPARTMENT to serve in the role of S, because its participation in the MANAGES relationship type is total.
2. **Merged relation**: Merge the two entity types and the relationship into a single relation. This may be appropriate when both participation are [[Participation|total]].
3. **Cross-reference or relationship relation**: Set up a third relation $\textcolor{lightgreen}{R}$ for the purpose of cross-referencing the [[Keys#Primary key|primary keys]] of the two relations $\textcolor{orange}{S}$ and $\textcolor{orange}{T}$ representing the entity types
# Step 4. Mapping of 1:N Relationship types
- For each regular binary 1:N relationship type $\textcolor{lightgreen}{R}$, identify the relation $\textcolor{orange}{S}$ that represent the participating entity type at the N-side of the relationship type.
- Include the [[Keys#Primary key|primary key]] of the relation $\textcolor{orange}{T}$ that represent the other entity type participating in $\textcolor{lightgreen}{R}$ as [[Keys#Foreign key|foreign key]] in $\textcolor{orange}{S}$ .
- Include any simple attributes of the 1:N relation type as attributes of $\textcolor{orange}{S}$
In simpler terms:
![[Cardinality#1 N]]
# Step 5. Mapping of Binary M:N Relationship types
- For each regular binary M:N relationship type $\textcolor{lightgreen}{R}$, create a new relation $\textcolor{orange}{S}$ to represent $\textcolor{lightgreen}{R}$.
- Include the [[Keys#Primary key|primary keys]] of the relations that represent the participating entity types as [[Keys#Foreign key|foreign key]] attributes in $\textcolor{orange}{S}$; their combination will form the primary key of $\textcolor{orange}{S}$.
- Also include any simple attributes of the M:N relationship type as attributes of $\textcolor{orange}{S}$
In simpler terms:
![[Cardinality#M N]]
# Step 6. Mapping of Multivalued attributes
- For each multivalued attribute $\textcolor{gold}{A}$, create a new relation $\textcolor{lightgreen}{R}$
- This relation $\textcolor{lightgreen}{R}$ will include an attribute corresponding to $\textcolor{gold}{A}$, plus the primary key attribute $\textcolor{violet}{K}$ — as a foreign key in $\textcolor{lightgreen}{R}$ — of the relation that represents the entity type of relationship type that has $\textcolor{gold}{A}$ as an attribute.
- The primary key of R is the combination of A and K. If the multivalued attribute is composite, Yeahwe include its simple components.