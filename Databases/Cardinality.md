# ERD to Relation Schema
## M:N
Many-to-many. Requires a new relation to show the connection:
1. A(<u>a1</u>, a2)
2. R(<u>a1</u>, <u>b1</u>)
3. B(<u>b1</u>, b2)
## 1:N
One-to-many. Requires a modification to the second relation:
1. A(<u>a1</u>, a2)
2. BR(a1, <u>b1</u>, b2) — a1 is a [[foreign key]]
## N:1
Many-to-one. Requires a modification to the first relation:
1. AR(<u>a1</u>, a2, b2) — b2 is a [[foreign key]]
2. B(<u>b1</u>, b2)
## 1:1
One-to-one. Can be shown as N:1 or as 1:N