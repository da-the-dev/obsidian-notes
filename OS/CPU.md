Does math and logic. Stores values in [[Registers|registers]].
# Basic cycles
- **Fetch Instruction** - read next expected instruction into buffer
- **Decode Instruction** - determine opcode operand specifiers
- **Calculate Operands** - calculate the effective address of each source operand
- **Fetch Operands** - fetch each operand from memory. Operands in registers need not be fetched
- **Execute Instruction** - perform the indicated operation and store the result
## Pipelines
### Three-stage pipeline
```mermaid
flowchart LR
	id1("Fetch unit")
	id2("Decode unit")
	id3("Execute unit")
	
	id1 ==> id2
	id2 ==> id3
```
### Superscalar CPU
```mermaid
flowchart LR
	f1("Fetch unit")
	f2("Fetch unit")
	d1("Decode unit")
	d2("Decode unit")
	e1("Execute unit")
	e2("Execute unit")
	h((("Holding buffer")))
	
	f1 ==> d1
	f2 ==> d2
	d1 ==> h
	d2 ==> h
	h ==> e1
	h ==> e2
```

