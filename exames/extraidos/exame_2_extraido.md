# OutSystems Exame 2 Reactive — Extração e Correção

## Resumo
- **Total de perguntas:** 50
- **Respostas corretas:** 42
- **Respostas erradas:** 8
- **Percentagem:** 84%
- **Perguntas erradas:** 3, 6, 11, 12, 26, 42, 46, 50

---

### Pergunta 1
**Enunciado:** Considering the following Entities, what is required to create a many-to-many relationship between them?
*(Imagem/Diagrama: Duas entidades sem relação entre si — `Order` com atributos `Id`, `Description`, `DueDate`, `CreatedOn`, `ShippedOn`, `Priority`, `AssignedTo`, `ReviewedBy`, `Status`, `RequestedBy`; e `Product` com atributos `Id`, `Name`, `VAT`, `Price`.)*
- **A)** Create a third Entity that contains two attributes of types Order Identifier and Product Identifier.
- **B)** Create a third Entity with a primary key of type Order Identifier and an attribute of type Product Identifier.
- **C)** Create an attribute of type Order Identifier in the Product Entity and an attribute of type Product Identifier in the Order Entity.
- **D)** Create an attribute of type Product Identifier in the Order Entity.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 2
**Enunciado:** In OutSystems, an Entity Identifier ...
- **A)** ... must have its Data Type set to Long Integer.
- **B)** ... must be set to Auto Number.
- **C)** ... can only be a single attribute.
- **D)** ... is created automatically and cannot be modified.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 3
**Enunciado:** Considering the following Aggregate, what will be the attributes of the GetOrdersShippingState.List.Current record?
*(Imagem/Diagrama: Referenciada no enunciado, não presente no PDF exportado — Aggregate com Group By em `ShippingState` e agregação `Count`.)*
- **A)** The two aggregation attributes: ShippingState and Count.
- **B)** The two aggregation attributes (ShippingState and Count) plus all the attributes of the Source Entity.
- **C)** Six attributes corresponding to the six visible columns in the Aggregate: ShippingState, Count, Description, DueDate, CreatedOn and Priority.
- **D)** The two aggregation attributes (ShippingState and Count) plus the columns used to calculate these aggregations.

- **Resposta correta:** A
- **Tua resposta:** B (❌ Errada)

---

### Pergunta 4
**Enunciado:** Considering the following Aggregate, where the Orders are fetched with their reviewers (Employees), which of the following options is correct?
*(Imagem/Diagrama: Referenciada no enunciado, não presente no PDF exportado.)*
- **A)** The Aggregate only returns Orders with Priority, Status and Employee.
- **B)** The Aggregate returns Orders without Employee and without Status.
- **C)** The Aggregate returns Orders with Status and at least one Employee.
- **D)** The Aggregate returns Orders with Priority and with zero or more Employees.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 5
**Enunciado:** How would you change the following Aggregate to return the number of orders per priority?
*(Imagem/Diagrama: Referenciada no enunciado, não presente no PDF exportado.)*
- **A)** Change the Join between the Order and the Priority to Only With and create a Count over the Priority.Id attribute.
- **B)** Create a Group By over the Priority.Id attribute and a Count over the Order.Id attribute.
- **C)** Create a GroupBy over the Order.Id attribute and a Count over the Priority.Id attribute.
- **D)** Remove the Join between the Order and the OrderStatus and create a Count over the Priority.Id attribute.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 6
**Enunciado:** Considering the On Initialize lifecycle event, which of the following options is true?
- **A)** The On Initialize event is triggered before the Screen or Block is rendered and before fetching any data.
- **B)** The On Initialize event is triggered after the Screen or Block has been rendered, so you can use it to manipulate its structure.
- **C)** The On Initialize event is triggered after an Aggregate finishes fetching data and can be used to act upon the retrieved data before it’s used in the Screen.
- **D)** The On Initialize event is triggered after the input parameter of a Block changes.

- **Resposta correta:** A
- **Tua resposta:** B (❌ Errada)

---

### Pergunta 7
**Enunciado:** The following Screen has two Dropdowns, one to select a Country and one to select a City. The GetCountries and GetCities Aggregates provide the countries and the cities to be displayed in the respective dropdowns and are both set to be fetched At Start. Which of the following options is **not a valid step** if we want to just fetch the cities for the country selected in the respective dropdown?
*(Imagem/Diagrama: Referenciada no enunciado, não presente no PDF exportado.)*
- **A)** Set the Fetch property of the GetCities Aggregate to Only On Demand.
- **B)** Refresh the GetCities Aggregate in the OnChange Action of the Country Dropdown.
- **C)** Filter the GetCities Aggregate by the selected country.
- **D)** Call the GetCities Aggregate in the GetCountries’ On After Fetch Event handler.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 8
**Enunciado:** Regarding Blocks in OutSystems reactive apps, which of the following options is correct?
- **A)** Blocks can only be instantiated on Screens.
- **B)** Blocks can be instantiated on Screens and other Blocks.
- **C)** Blocks can be instantiated on Client Actions on the Screen.
- **D)** Blocks can be instantiated on Screens and external HTML pages, using a special HTML tag.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 9
**Enunciado:** Which of the following options is a valid usage of the Trigger Event node?
- **A)** The Trigger Event allows a Block to notify its parent (Screen or Block) that something relevant occurred in the scope of the Block.
- **B)** The Trigger Event allows a Screen to notify its children (Blocks) that something relevant occurred in the scope of the Screen.
- **C)** The Trigger Event allows a Block to notify its children (other Blocks) that something relevant occurred in the scope of the Block.
- **D)** The Trigger Event allows a Screen to notify its parent (Screen or Block) that something relevant occurred in the scope of the Screen.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 10
**Enunciado:** Consider a Form with a Save button with the Built-in Validations property set to **Yes**. When a user clicks on the Save button, some validations over the data submitted to the Form are automatically performed by OutSystems by default. Which validations are those?
- **A)** Check if the mandatory fields are filled in.
- **B)** Check if the mandatory fields are filled in and if the non-mandatory fields, that are later used in the logic, are also filled in.
- **C)** Check if the mandatory fields are filled in and if the data submitted by the user matches the data type expected in the input fields.
- **D)** Check if the mandatory fields are filled in and if the data submitted by the user matches the data type of the Form’s data source.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 11
**Enunciado:** In the following scenario, we are implementing the ColorsDropdown widget which will allow a user to select a color. What should be set in the **Options Text** property to make sure that the names of the colors appear in the dropdown?
*(Imagem/Diagrama: Referenciada no enunciado, não presente no PDF exportado.)*
- **A)** Color.Id
- **B)** GetColors.Color.Label
- **C)** Color
- **D)** Color.Label

- **Resposta correta:** D
- **Tua resposta:** B (❌ Errada)

---

### Pergunta 12
**Enunciado:** Considering a Button in a Screen, which of the following options **cannot** be set as its On Click Destination?
- **A)** Screen.
- **B)** Client Action.
- **C)** Block.
- **D)** External Site.

- **Resposta correta:** B *(⚠️ Nota: O gabarito do exame indica B, mas em OutSystems Reactive a resposta tecnicamente correta é **C — Block**, pois um Button pode ter como destino um Screen, uma Screen Action [Client Action do Screen] ou um External Site, mas nunca um Block.)*
- **Tua resposta:** D (❌ Errada)

---

### Pergunta 13
**Enunciado:** Consider the Action called *Absolute* which returns an absolute value (abs) of a number *N* passed as Input Parameter. When does the Action return 0?
*(Imagem/Diagrama: Referenciada no enunciado, não presente no PDF exportado.)*
- **A)** Never.
- **B)** When the input parameter (N) is less than zero.
- **C)** When the input parameter (N) is zero.
- **D)** When the input parameter (N) is greater than zero.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 14
**Enunciado:** Consider the following Server Action. What happens if the *GetEmployeeById* Aggregate does not return any record?
*(Imagem/Diagrama: Referenciada no enunciado, não presente no PDF exportado.)*
- **A)** The DatabaseException flow is executed.
- **B)** The RecordNotFound flow is executed.
- **C)** No exception flow is executed.
- **D)** The module’s global exception handler is executed.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 15
**Enunciado:** Considering the Function property in Client Actions, which of the following options is correct?
- **A)** Setting the Function property to Yes restricts the Action to have only one Output Parameter.
- **B)** Setting the Function property to No ensures the Action can only be used in the module where it is defined.
- **C)** Setting the Function property to Yes is not possible, if the Action is exposed to other modules as Public.
- **D)** Setting the Function property to No ensures the Action can only be used in Screen Expressions.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 16
**Enunciado:** In an application with three roles of Anonymous, Registered and OrdersAdmin, considering that Michael is a user of the Orders application, with only the *OrdersAdmin* Role assigned to him, which of the following options is **correct**?
- **A)** Michael has access to Screens with the Registered Role checked.
- **B)** Michael does not have access to Screens with the Anonymous Role checked.
- **C)** Michael has access to Screens that have the OrdersAdmin Role checked, but not to Screens with the Registered Role checked.
- **D)** Michael has only access to Screens that have the OrdersAdmin Role checked.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 17
**Enunciado:** Which of the following options should **not** be a use case of client variables?
- **A)** Username.
- **B)** Password.
- **C)** Search filter keyword.
- **D)** ID of a user session.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 18
**Enunciado:** Consider the following Action, that calculates the square root (sqrt) of a positive decimal number (N). Knowing that the function was called with N = 0, and the debugger is stopped at the Start node, what will happen when the developer selects the **Continue (F9)** option highlighted in the picture?
*(Imagem/Diagrama: Referenciada no enunciado, não presente no PDF exportado.)*
- **A)** The Action will end, with sqrt = 0.
- **B)** The Action will throw an exception and sqrt will have no value.
- **C)** The debugger will stop in the N < 0 If node.
- **D)** The debugger will stop at the breakpoint in the End node.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 19
**Enunciado:** Consider the following Pagination that is associated with an already implemented Table on a Screen. There are no errors in Service Studio, but when the user selects a new page (in the pagination widget) the results do not change on the Table. What is the reason for that behavior?
*(Imagem/Diagrama: Referenciada no enunciado, não presente no PDF exportado.)*
- **A)** The GetMovies Aggregate is not being refreshed in the OnNavigate Action.
- **B)** The Max. Records of the Aggregate should be equal to the total number of movies in the database.
- **C)** The Table is not being refreshed on the OnNavigate Action.
- **D)** The Max Records property of the Pagination should be set to GetMovies.Count and the TotalCount to RecordsPerPage.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 20
**Enunciado:** Consider a Screen that contains a Form to collect Customer data. The Form has a Save Button with the On Click Destination set to a SaveOnClick Action, which sends the data to the server to store it in the database. What is the best way to make sure that we do not send the data to the server when the mandatory Customer data fields have not been filled in?
- **A)** Just set the Built-in validations of the Save button to Yes.
- **B)** Perform custom validations for all inputs. If one fails, set the Valid property of the Form to False.
- **C)** Set the Built-in validations of the Save button to Yes and check if the Form’s Valid property is True.
- **D)** Set the Built-in validations of the Save button to Yes and add an Exception Handler flow to handle invalid inputs.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 21
**Enunciado:** Which of the following is not a Development Environment?
- **A)** Service Studio.
- **B)** Integration Studio.
- **C)** Service Center.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 22
**Enunciado:** One of the following Tools allows you to manage the application's lifecycle across an infrastructure. Which one?
- **A)** Service Center.
- **B)** LifeTime.
- **C)** Service Studio.
- **D)** Integration Studio.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 23
**Enunciado:** During the 1-Click Publish, your application data model, code, and interface is compiled and generates .NET code, HTML, JavaScript and CSS. True or False?
- **A)** True.
- **B)** False.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 24
**Enunciado:** In which Service Studio layer can Screens and Blocks be found?
- **A)** Processes.
- **B)** Interface.
- **C)** Logic.
- **D)** Data.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 25
**Enunciado:** In which Service Studio layer can Entities be found?
- **A)** Processes.
- **B)** Interface.
- **C)** Logic.
- **D)** Data.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 26
**Enunciado:** Regarding Reactive Web Apps in OutSystems, which of the following options is false?
- **A)** A Reactive Web app is a cross-device app.
- **B)** Data requests are executed synchronously.
- **C)** The code generated by OutSystems results in a single-page application.
- **D)** A developer builds the Reactive Web App in Service Studio.

- **Resposta correta:** B
- **Tua resposta:** C (❌ Errada)

---

### Pergunta 27
**Enunciado:** Regarding Mobile (Phone or Tablet) Apps in OutSystems, which of the following options is false?
- **A)** Mobile Apps can run natively on iOS and Android.
- **B)** Mobile Apps can be distributed as a PWA.
- **C)** Mobile Apps do not have offline capabilities.
- **D)** The programming model of Mobile Apps is similar to Reactive Web Apps.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 28
**Enunciado:** What happens when a developer publishes a module?
- **A)** The OutSystems platform compiles it and generates the HTML, CSS, and JavaScript.
- **B)** The browser opens.
- **C)** Nothing.
- **D)** The code is uploaded but only compiled when a user accesses the application.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 29
**Enunciado:** Which of the following options is false regarding Modules and Applications?
- **A)** An application is composed of a set of modules.
- **B)** Modules can be of different types such as Reactive Web App, Blank or Extension.
- **C)** Elements can be exposed and reused, but only within the same application.
- **D)** A module that reuses an element from another module is called a Consumer.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 30
**Enunciado:** Business concepts that need to be stored and accessed in our applications should be modeled as...
- **A)** Entities.
- **B)** Entity diagrams.
- **C)** Entity relationships.
- **D)** Database tables.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 31
**Enunciado:** Which of the following mappings between OutSystems and the Database is NOT correct?
- **A)** Entities - Tables.
- **B)** Attributes - Column.
- **C)** Reference attribute - Primary Key.
- **D)** Index - Index.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 32
**Enunciado:** Which of the following statements about Entities is false?
- **A)** Entities have attributes.
- **B)** Entities do not require an identifier.
- **C)** Entities are only stored in memory.
- **D)** Entities can be created, updated, and deleted.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 33
**Enunciado:** If an Entity Attribute named HouseNumber is created, what needs to be done about its Data Type?
- **A)** It should be set to Integer.
- **B)** It should be set to Decimal.
- **C)** Nothing, it will automatically be set to Identifier.
- **D)** Nothing, it will automatically be set to Integer.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 34
**Enunciado:** Which of the following is not an Entity Action of the Customer Entity?
- **A)** CreateCustomer.
- **B)** RetrieveCustomer.
- **C)** UpdateCustomer.
- **D)** DeleteCustomer.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 35
**Enunciado:** Which of the following is a characteristic of a Static Entity?
- **A)** It can’t be changed after the first publish.
- **B)** It contains a set of Records.
- **C)** It has two Entity Actions.
- **D)** It can’t be extended with any new attributes.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 36
**Enunciado:** Regarding the Records of a Static Entity, which of the following options is false?
- **A)** The values for all 4 default attributes must be defined.
- **B)** Records can only be added and removed during development.
- **C)** The record identifier is the identifier of Static Entity.
- **D)** The Identifier attribute is required for all Static Entities.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 37
**Enunciado:** Static Entities are most similar to which other programming concept?
- **A)** Linked lists.
- **B)** Enumeration.
- **C)** Hash Maps.
- **D)** Static variables.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 38
**Enunciado:** Screens can be composed of a combination of several elements called Widgets.
- **A)** True.
- **B)** False.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 39
**Enunciado:** What type of variables can be created inside a Screen?
- **A)** Local Variables only.
- **B)** Input Parameters only.
- **C)** Input Parameters and Local Variables.
- **D)** Input Parameters, Output Parameters, and Local Variables.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 40
**Enunciado:** Which of the following options is false?
- **A)** Input Parameters allow passing data between Screens when navigating between them.
- **B)** Local Variables from a Screen may be directly accessed from another Screen.
- **C)** Local Variables allow temporarily storing relevant information inside a Screen.
- **D)** When the value of a Local Variable changes the user interface reacts immediately.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 41
**Enunciado:** The Expression widget...
- **A)** … displays only static text.
- **B)** … displays text calculated at runtime.
- **C)** … displays only the result of mathematical expressions.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 42
**Enunciado:** Which of the following behaviors is true for Links and Buttons?
- **A)** Links can only navigate to Screens.
- **B)** Buttons can only have a Screen Action as an On Click Destination.
- **C)** Links and Buttons can either Navigate to screens or trigger Screen Actions.
- **D)** Only Links can navigate to external URLs.

- **Resposta correta:** C
- **Tua resposta:** B (❌ Errada)

---

### Pergunta 43
**Enunciado:** Regarding the If Widget, which of the following options is false?
- **A)** Functions can be used inside the Condition of an If.
- **B)** More branches may be added to an If Widget.
- **C)** Only one of the branches is shown at runtime.
- **D)** Multiple widgets may be added inside each branch.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 44
**Enunciado:** Regarding the Container widget, which of the following options is false?
- **A)** Containers allow grouping several widgets.
- **B)** By default, containers can span from 1 column up to 12 columns.
- **C)** Containers can be placed inside other containers.
- **D)** All containers must have at least one widget inside.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 45
**Enunciado:** Which of the following options is correct?
- **A)** Screen Actions can call other Screen Actions from a different screen.
- **B)** Client Actions can call Screen Actions.
- **C)** Server Actions can call Client Actions.
- **D)** Client Actions can call Server Actions.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 46
**Enunciado:** Client Actions and Server Actions can have the following variables:
- **A)** Input and Output Parameters, but no Local variables.
- **B)** Input Parameters and Local Variables, but no Output Parameters.
- **C)** Input and Output Parameters, as well as Local Variables.
- **D)** Output Parameters and Local Variables, but no Input Parameters.

- **Resposta correta:** C
- **Tua resposta:** A (❌ Errada)

---

### Pergunta 47
**Enunciado:** The flow of an action can have...
- **A)** … multiple Start and End nodes.
- **B)** … one or more Start nodes but only one End node.
- **C)** … only one Start node but multiple End nodes.
- **D)** … only one Start node and one End node.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 48
**Enunciado:** Regarding the If statement, which of the following options is false?
- **A)** Both True and False branches are mandatory.
- **B)** Only one of the branches is executed, depending on the If condition’s outcome.
- **C)** If statements can also be used to implement ad-hoc loops.
- **D)** More branches may be added if needed.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 49
**Enunciado:** Regarding the Switch statement, which of the following options is false?
- **A)** The first branch that the condition evaluates to True is executed.
- **B)** Every branch that evaluates to True is executed.
- **C)** If no branch evaluates to True, the Otherwise branch is executed.
- **D)** The Otherwise branch must exist.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 50
**Enunciado:** Inside an Action flow…
- **A)** … only one Exception Handler may exist.
- **B)** … it’s mandatory to have at least one Exception Handler.
- **C)** … the Exception Handler flow can’t intersect other flows.

- **Resposta correta:** C
- **Tua resposta:** B (❌ Errada)
