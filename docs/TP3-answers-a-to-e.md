# TP 3 – Answers to questions (a)–(e)

## (a) Direction and association arrow
`left to right direction` changes the orientation of the automatically generated diagram: PlantUML arranges its elements from left to right instead of using its default layout direction.

In `Customer --> Withdraw`, the arrow indicates a directed relationship in the drawing. It changes the visual notation; it does not mean that the customer sends a message or that the use case is executed in a particular order. The reference notation used in Chapter 3 is an ordinary actor–use-case association, represented as `Customer -- Withdraw`, without an arrowhead.

## (b) Reversed `extend` relationship
PlantUML can render the reversed relationship, but it does not reliably determine that the UML `extend` direction is semantically wrong. A modeling tool can check syntax, recognized notation, and some structural constraints. It cannot determine by itself whether the model accurately represents the real requirements or whether the business meaning and conditions are correct. Those require human review and domain knowledge.

## (c) Two advantages and two drawbacks of PlantUML automatic layout
**Advantages**
1. It saves time because the diagram is arranged automatically without manually positioning every element.
2. The layout can be regenerated after source changes, and the text source is easy to edit.

**Drawbacks**
1. The automatic arrangement may not match the reference layout; lines can cross or elements may be far apart.
2. The user has less precise control over element positions than in a graphical editor, so direction hints and declaration order may be needed.

## (d) PlantUML compared with a graphical tool such as Modelio
- **Editing:** PlantUML is edited as text, which is quick for users comfortable with code and makes changes easy to review. Modelio uses a graphical palette and direct manipulation, which may be easier for beginners.
- **Layout:** PlantUML generates layout automatically and supports direction hints. A graphical tool usually gives more direct control over element placement.
- **Version control:** PlantUML text files work well with Git because changes appear as readable line-by-line diffs. A graphical model may be stored in a format that is harder to compare.
- **Consistency:** PlantUML source files can be kept together and reviewed, but consistency still depends on the author. A graphical modeling tool may provide model-level features and shared elements that help maintain consistency.

## (e) Why keep models in the same repository as the code?
Keeping models in the same repository links the design to the implementation. Developers can review diagrams and code together, track changes in the same Git history, identify which design version belongs to a code version, collaborate through commits and pull requests, and update documentation when the implementation changes. This reduces the risk that diagrams become outdated or separated from the software they describe.
