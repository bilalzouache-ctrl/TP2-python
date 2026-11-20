# TP 3 – Use Case Diagrams with a UML Tool

Software Engineering – University of Bordj Bou Arreridj – 2026–2027

This package contains the PlantUML source files, UC-07 fully dressed description, and answers (a)–(e).

## Structure
- `docs/uml/atm.puml`
- `docs/uml/use-cases.puml`
- `docs/uml/register-loan-activity.puml`
- `docs/uml/register-return.md`
- `docs/uml/register-return-activity.puml`
- `docs/uml/TP3-answers-a-to-e.md`

## Export diagrams
Open each `.puml` file in VS Code with the PlantUML extension and choose **PlantUML: Export Current Diagram**. Export PNG files into `docs/uml/` before submission. Alternatively, with Java and PlantUML installed:
```bash
java -jar plantuml.jar docs/uml/atm.puml -tpng
java -jar plantuml.jar docs/uml/use-cases.puml -tpng
java -jar plantuml.jar docs/uml/register-loan-activity.puml -tpng
java -jar plantuml.jar docs/uml/register-return-activity.puml -tpng
```

## Source limitation
The provided TP3 PDF does not include the full text of Chapter 3, Tables 3.4 and 3.5. The scenarios here follow all requirements in the TP sheet and the teacher's correction message; details not stated in those sources are kept generic.

## GitHub
Copy `docs/uml` into the TP2 repository, then run:
```bash
git add docs/uml
git commit -m "Add corrected TP3 UML diagrams and answers"
git push origin main
```
