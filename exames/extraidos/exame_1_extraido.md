# OutSystems Exame 1 Reactive — Extração Completa

## Resumo do Resultado
- **Total de perguntas:** 50
- **Corretas:** 39 (78%)
- **Erradas:** 11 (22%)
- **Perguntas erradas:** 12, 14, 21, 22, 23, 28, 33, 34, 35, 41, 49

---

### Pergunta 1
**Enunciado:** Consider the following two Entities: Contact and Group. Contacts are grouped together in groups (e. g. "Work Contacts", "Family Contacts") using these two Entities, and each contact only belongs to a single group at a time. What do we need to do to create the missing one-to-many relationship these two entities?
*(Imagem/Diagrama: Entidade `Contact` com Id, Name, Email, PhoneNumber, Address; Entidade `Group` com Id, Name.)*
- **A)** Create a new attribute in Contact of data type Group.
- **B)** Create a new Entity with attributes, one with data type Contact Identifier and the other with data type Group Identifier.
- **C)** Create a new attribute in Contact of data type Group Identifier.
- **D)** Create a new attribute in Group of data type Contact Identifier.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 2
**Enunciado:** Entities and Attributes created in OutSystems are mapped to...
- **A)** ...Classes and Attributes
- **B)** ...Database Tables and Columns
- **C)** ...Structures and Enumerates
- **D)** ...Lists and Records

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 3
**Enunciado:** Regarding Static Entities and its attributes, which of the following options is correct?
- **A)** It is possible to change the value of a Static Entity's attribute in runtime, by using the Update `<StaticEntity>` Entity Action.
- **B)** It is possible to add new mandatory attributes to the Static Entity, but their values need to be specified at design time.
- **C)** It is not possible to change the Entity's automatically created attributes.
- **D)** It is not possible to use the Static Entity Identifier (ID attribute) in another Entity, to create a relationship.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 4
**Enunciado:** Consider the following Entity and the following Excel file. What will happen when we create an action to Bootstrap data from this Excel file to the Contact Entity?
*(Imagem/Diagrama: Entidade `Contact` com atributos `Id`, `Name`, `Email`, `Phone`. Ficheiro Excel com colunas `Name`, `Email`, `PhoneNumber`, `Address`.)*
- **A)** The Name, Email and PhoneNumber columns in the Excel file will match with the Name, Email and Phone attributes in the Contact Entity. The Address columns will be ignored.
- **B)** The Name, Email and PhoneNumber columns in the Excel file will match with the Name, Email and Phone attributes in the Contact Entity. The Address columns will be created by the platform.
- **C)** The Name and Email columns in the Excel file will match with the Name and Email attributes in the Contact Entity. The PhoneNumber and the Address columns will be ignored.
- **D)** No data will be bootstrapped, because at the Entity attributes must match all the columns in the Excel file.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 5
**Enunciado:** The `CreateOrUpdate<Entity>` Entity Action...
- **A)** ... will fail with an exception if the record already exists.
- **B)** ... will update an existing record if the Id of the input record is NullIdentifier()
- **C)** ... return the Id of the created or updated Record.
- **D)** ... returns the Record that was created or updated.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 6
**Enunciado:** Consider the following data model with the Status Entity, and the Customer, Order, ShippingDetail, OrderProduct and Product Entities. Why is this model wrong?
*(Imagem/Diagrama: Modelo com `Customer`, `Order` (CustomerId, StatusId), `ShippingDetail` (Id como FK para Order), `OrderProduct` (OrderId, ProductId, Quantity), `Product`, e Static Entity `Status` com atributos Id, Label, Order, Is_Active e um atributo de referência `OrderId`.)*
- **A)** The OrderId attribute cannot be in the Status Entity since a Static Entity can only have a reference attribute to other Static Entities.
- **B)** The Id attribute of the ShippingDetail cannot be reference the Order Entity, since Id attribute cannot be of type Entity Identifier.
- **C)** The StatusId attribute cannot be in the Order Entity, since the Order Entity already has another reference attribute (CustomerId).
- **D)** The Quantity attribute cannot be in the OrderProduct Entity, since it is an Entity supporting the relationship between Order and Product.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 7
**Enunciado:** Which attributes are returned in the output of the following Aggregate?
*(Imagem/Diagrama: Aggregate com source `Product` (Name, VAT, Price) onde o utilizador aplica a função `Average` na coluna `Price`.)*
- **A)** Only the list of products.
- **B)** The Average of the attribute price and the list of products.
- **C)** The list of products, with the average of the attribute Price in each record.
- **D)** Only the Average of the attribute Price.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 8
**Enunciado:** Which attributes are returned in the output of the following Aggregate?
*(Imagem/Diagrama: Aggregate `GetProductsWithOrderProducts` com sources `Product` Only With `OrderProduct` e um atributo calculado `PriceWithoutVAT = Quantity * WholesalePrice`.)*
- **A)** Not yet defined. You need to add an Output Structure / Entity to the Aggregate.
- **B)** Only the Product and OrderProduct Entity and Attributes.
- **C)** The Product and OrderProduct Entity attributes, plus a PriceWithoutVAT attribute.
- **D)** Only the PriceWithoutVAT attribute.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 9
**Enunciado:** In the image below, the UserMovieRating Entity is being dragged into an Aggregate that already has a Movie Entity. Considering this scenario, which of the following statements is correct?
*(Imagem/Diagrama: Aggregate `GetMovies` com `Movie`, a arrastar `UserMovieRating` para as Sources.)*
- **A)** A With type of Join will be created between the Movie and UserMovieRating Entities, if the UserMovieRating MovieId attribute is non mandatory.
- **B)** A With type of Join will be created between the Movie and UserMovieRating Entities, if the UserMovieRating MovieId attribute is mandatory.
- **C)** A Only With type of Join will be created between the Movie and UserMovieRating Entities, if the UserMovieRating MovieId attribute is non mandatory.
- **D)** A With or Without type of Join will be created between the Movie and UserMovieRating Entities, if the UserMovieRating MovieId attribute is non mandatory.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 10
**Enunciado:** In the following Aggregate, we want to filter the results to only return contacts that have 'John' anywhere in their name. What is the correct expression to put in the Filter of the Aggregate to achieve the desired result?
*(Imagem/Diagrama: Aggregate `GetContacts` com `Contact.Name`, `JobTitle`, `Phone`, `Email`.)*
- **A)** `Contact.Name like "John"`
- **B)** `Contact.Name like "%John%"`
- **C)** `Contact.Name = "John"`
- **D)** `Contact.Name = "%John%"`

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 11
**Enunciado:** Which of the following option is **not** possible to use to fetch data the screen is initializing?
- **A)** REST API methods within a Data Action flow.
- **B)** Advanced SQL Queries defined at the Screen level.
- **C)** Aggregates defined at the Screen level.
- **D)** Aggregates within a Data Action flow.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 12
**Enunciado:** Considering the following Aggregate, what will happen if a developer selects the Add Sort option and then chooses the `Customer.Name` attribute?
*(Imagem/Diagrama: Aggregate `GetOrders` com Sorting já definido em `#1 Order.Date Ascending`.)*
- **A)** A second sorting criteria will be added to the Aggregate and the records with the same `Order.Date` will appear sort by `Customer.Name`.
- **B)** The change will lead to an error in the application, because there is a sorting criteria defined that is based on an attribute of a different Entity.
- **C)** A second sorting criteria will be added to the Aggregate and the records with the same `Customer.Name` will appear sort by `Order.Date`.
- **D)** The sorting criteria by `Order.Date` will be replaced by the new `Customer.Name` sorting criteria.

- **Resposta correta:** A
- **Tua resposta:** C (❌ Errada)

---

### Pergunta 13
**Enunciado:** Considering the `On Parameters Changed` lifecycle event, which of the following options is **true**?
- **A)** The On Parameters Changed event is triggered when a variable used in a filter of an Aggregate, or an input parameter of a Data Action, changes.
- **B)** The On Parameters Changed event are bound to Screen Widget and are triggered when new data comes from Screen Aggregates / Data Action.
- **C)** The On Parameters Changed event is available for both Blocks and Screens.
- **D)** The On Parameters Changed event is triggered anytime the parent of a Block changes one of Block's Input Parameters.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 14
**Enunciado:** Considering the `On Render` lifecycle event, which of the following options is **true**?
- **A)** The On Render Event is the First event triggered when accessing a Screen for the first time.
- **B)** The On Render Event is triggered before the Screen or Block are ready.
- **C)** The On Render Event is triggered every time the underlying data of a Screen or Block changes.
- **D)** The On Render Event is only triggered when the application is transitioning from one Screen to another.

- **Resposta correta:** C
- **Tua resposta:** D (❌ Errada)

---

### Pergunta 15
**Enunciado:** By default, how is data fetched on a Screen?
- **A)** The Aggregates run first, then the Data Actions.
- **B)** The Aggregates and Data Action do not run in any particular order.
- **C)** The Aggregates and Data Actions run following their order on the Screen (from top to bottom).
- **D)** The Aggregates and Data Actions run only when they are explicitly called.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 16
**Enunciado:** When transitioning from the Employees Screen to the EmployeeDetail Screen, when does the application require accessing the server?
*(Imagem/Diagrama: `MainFlow` com `EmployeeDetail` (Input `EmployeeId`, Aggregate `GetEmployeeById`, Action `SaveOnClick`) e `Employees` (Aggregate `GetEmployees`).)*
- **A)** For destroying the Employee Screen.
- **B)** For destroying the EmployeeDetail Screen.
- **C)** For triggering Screen Events.
- **D)** For Querying the database.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 17
**Enunciado:** Considering the scenario in the picture, which of the following option is an important step to guarantee that the cities will only be fetched when a user selects a country?
*(Imagem/Diagrama: Ecrã `EmployeeDetail` com dropdown `Country` e dropdown `City`, e Aggregates `GetCities`, `GetCountries`, `GetEmployeeById`.)*
- **A)** Set the Fetch property of the GetCities Aggregates to Only On Demand.
- **B)** Call the GetCities Aggregate in the OnAfterFetch event of the GetCountries Aggregates.
- **C)** Call the GetCities Aggregate when the On Render event is triggered.
- **D)** Call the GetCities following by the GetCities Aggregate in a Data Action.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 18
**Enunciado:** What needs to be changed in the following Aggregate to obtain the number of *comments per Movie*, for all the movies in the database?
*(Imagem/Diagrama: Aggregate com `Movie` Only With `UserMovieComment` onde `UserMovieComment.MovieId = Movie.Id`.)*
- **A)** Create a Group By over the Movie Id attribute and a Count over the UserMovieComment Id attribute.
- **B)** Change the existing Join to With or Without and create Count over the UserMovieComment Id attribute.
- **C)** Remove the Join between Movie and UserMovieComment Entities and create a Count over UserMovieComment Id attribute.
- **D)** Change the existing Join to With or Without, create a Group By over the Movie Id attribute, and a Count over the UserMovieComment Id attribute.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 19
**Enunciado:** Modifying the content of a Block...
- **A)** ...requires every instance of the Block to throw an Event to the parent, to apply the changes.
- **B)** ...applies the changes to all the existing instances of that Block.
- **C)** ...only applies the changes to new instances of the Block. The existing instances remain unchanged.
- **D)** ...is not possible after it has been instantiated in another Block or Screen.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 20
**Enunciado:** Consider the following Countdown Block with an `OnClickAction` Action that triggers the `Start` Event. Which of the following option is **correct**?
*(Imagem/Diagrama: Block `Countdown` com Event `Start` tendo a propriedade `Is Mandatory = Yes`.)*
- **A)** An Event handler for the Start Event must be defined on the parent when instantiating the Countdown Block.
- **B)** If no Event handler is defined for the Start Event, the trigger Event statement will throw an error at runtime.
- **C)** The Event handler for the Start Event must be defined in the scope of the Countdown Block.
- **D)** It is not necessary to create an Event handler for the Start Event, as the OnClickAction will handle the Event.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 21
**Enunciado:** Given a reusable Block that allows the user to set a rating between 1 and 5 stars, how can the rating selected by the user be sent to the parent of the Block?
- **A)** Create a Local Variable in the Block for the selected rating, that can be read from the outside if you make it Public.
- **B)** Create a Local Variable in the parent for selected rating, that can be updated by the Block.
- **C)** Create an event in the Block, contain the selected rating as Input Parameter, that is triggered by the Block when the rating is selected.
- **D)** Create an event in the parent to receive the selected rating as Input Parameter, that is triggered by the Block when the rating is selected.

- **Resposta correta:** C
- **Tua resposta:** A (❌ Errada)

---

### Pergunta 22
**Enunciado:** Regarding Blocks, which of the following options is **correct**?
- **A)** A Block can have its own Output Parameters.
- **B)** A Block can have Client Action defined in its scope.
- **C)** A Block can be nested inside itself.
- **D)** A Block can only be instantiated inside Screens.

- **Resposta correta:** B
- **Tua resposta:** A (❌ Errada)

---

### Pergunta 23
**Enunciado:** What is needed to ensure the list is updated by InputSearch criteria?
- **A)** Refresh the GetEmployees Aggregate.
- **B)** Explicitly refresh the List Widget.
- **C)** Create a new query to filter Employees.
- **D)** Assign the SearchKeyword with the user inserted value.

- **Resposta correta:** A
- **Tua resposta:** B (❌ Errada)

---

### Pergunta 24
**Enunciado:** What is the main advantage of using the Form Widget?
- **A)** It's the only way to edit a record from an Entity.
- **B)** Easily validate the input widgets that are inside the Form.
- **C)** Apply a common style to all the input widgets inside the Form.
- **D)** Save in the database all the attribute of a record at once.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 25
**Enunciado:** Just considering Built-in validations, which of the following scenarios would keep a Form **Valid**?
- **A)** The user inserts a text on a field that expects an Integer.
- **B)** The user does not fill a non mandatory field that is used in the logic.
- **C)** The user inserts a date on a field that expects an Integer.
- **D)** The user does not fill in a mandatory field.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 26
**Enunciado:** Consider the next picture with a ButtonGroup widget and the Priority Entity. The ButtonGroup Variable property is set with the `PriorityId` Local Variable of type Priority Identifier. What should be set in the **Value** property of the leftmost Button Group item?
*(Imagem não incluída no PDF; cenário clássico com Static Entity `Priority` tendo Low / Medium / High.)*
- **A)** `Entities.Priority.Id`
- **B)** `Entities.Priority.Label`
- **C)** `Entities.Priority`
- **D)** `Entities.Priority.Low`

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 27
**Enunciado:** Considering the following scenario, what should be the data type of the option selected in the Variable property of the dropdown?
*(Imagem não incluída no PDF; Dropdown com List `GetUsers.List` e Option Value `User.Id`.)*
- **A)** User
- **B)** User Identifier
- **C)** Text
- **D)** GetUsers.List

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 28
**Enunciado:** Complete the following sentence: "By setting the Valid property of the Name input field to False..."
- **A)** ... the Valid property of the EmployeeForm will automatically be set to False.
- **B)** ... it is mandatory to programmatically set the Valid property of the EmployeeForm to false.
- **C)** ... the valid properties of the other input fields will also be set to False.
- **D)** ... it is mandatory to set a message in the ValidationMessage property of the Input.

- **Resposta correta:** A
- **Tua resposta:** D (❌ Errada)

---

### Pergunta 29
**Enunciado:** Which of the following options **cannot** be used **directly** in an Expression?
- **A)** The result of a mathematical expression.
- **B)** The output of a Server Action.
- **C)** Static text.
- **D)** A numeric calculated attribute in the output of an Aggregate.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 30
**Enunciado:** Which of the following steps would remove the error in the List widget represented in the picture?
*(Imagem não incluída no PDF; List widget com Source em falta.)*
- **A)** Specify a list in the Source property.
- **B)** Specify a record in the Source property.
- **C)** Specify a Structure in the Source property.
- **D)** Specify an Entity in the Source property.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 31
**Enunciado:** Considering the **On Click Destination** of Links and Buttons, what is the main difference between widgets?
- **A)** Links can have the On Click Destination set to a Screen, while Buttons cannot.
- **B)** Links can have the On Click Destination set to an Event inside Blocks, while Buttons cannot.
- **C)** There is no difference between the two widgets in terms of their On Click Destination.
- **D)** Button can have the On Click Destination set to an Action, while links cannot.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 32
**Enunciado:** Considering the following Server Action, which of the following option is **correct**?
*(Imagem não incluída no PDF; Server Action com If sobre `IntegerInput` e Assign ao Output.)*
- **A)** The Output value will always be equal to 2.
- **B)** The Output value will either be its default value or equal to the value of IntegerInput.
- **C)** The Output value will always be equal to the IntegerInput value.
- **D)** If the IntegerInput has value 2, then the Output value will be equal to 2.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 33
**Enunciado:** Consider the following Server Action containing a Switch, where its conditions are detailed on the connectors. The assignments are also detailed on the respective Assign tables. Which of the following options is **correct**?
*(Imagem não incluída no PDF; cenário clássico de Switch com condições mal ordenadas onde a primeira condição verdadeira é executada primeiro.)*
- **A)** If the value of the Integer Input Parameter is exactly 1000, the Text Output Parameter will be "> 1k".
- **B)** At runtime, the Otherwise path will never be executed.
- **C)** If the value of the Integer Input Parameter is higher than 1000, the Text Output Parameter will be "> 1k".
- **D)** If the value of the Integer Input Parameter is 2000, the Text Output Parameter will be "< 1k".

- **Resposta correta:** D
- **Tua resposta:** C (❌ Errada)

---

### Pergunta 34
**Enunciado:** Which of the following options is a use case for a For Each?
- **A)** To create conditional branches.
- **B)** To iterate over a variable of type List.
- **C)** To bulk insert data in a Static Entity.
- **D)** To define generic loops.

- **Resposta correta:** B
- **Tua resposta:** D (❌ Errada)

---

### Pergunta 35
**Enunciado:** Consider the Save Client Action (on the left), where the `Employee_Create` Action (on the right) is called in the logic flow. What happens if an exception is thrown during the execution of the `CreateEmployee` Entity Action?
*(Imagem não incluída no PDF; `Employee_Create` tem um handler `AllExceptions` no seu fluxo, enquanto `Save` tem `DatabaseException` e `AllExceptions`.)*
- **A)** The DatabaseException flow in the Save action is executed.
- **B)** The AllException flow in the Save action is executed.
- **C)** The AllException flow in the Employee_Create action is executed.
- **D)** The Exception is not handled.

- **Resposta correta:** C
- **Tua resposta:** A (❌ Errada)

---

### Pergunta 36
**Enunciado:** Considering the `ChangeStatus` Action in the screenshot, which of the following option is **correct**?
*(Imagem não incluída no PDF; Client Action não pública com Function = No.)*
- **A)** The ChangeStatus Action can be called from another module.
- **B)** The ChangeStatus Action can be called from a Screen action.
- **C)** The ChangeStatus Action can be called from a Server action.
- **D)** The ChangeStatus Action can be used in an Expression on a Screen.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 37
**Enunciado:** Consider the following Action, which is set as Destination of a Save button within a Form to edit information about Employees. What will happen when the user inserts an employee with 17 years old?
*(Imagem não incluída no PDF; validação customizada de idade >= 18 que marca o input BirthDate como Valid = False e ValidationMessage antes do check `Form.Valid`.)*
- **A)** The Employee_CreateOrUpdate Action will not run and no message will appear on the Screen.
- **B)** The Employee_CreateOrUpdate Action will run and Success Message will appear on the Screen.
- **C)** The Employee_CreateOrUpdate Action will run and a Database Exception will be thrown.
- **D)** The Employee_CreateOrUpdate Action will not run and a message will appear next to the Birth Date input.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 38
**Enunciado:** Consider the following Server action. In which scenario will the execution move from the main logic flow to the `DatabaseException` flow?
*(Imagem não incluída no PDF; Server Action com `CheckPermissions`, `CreateOrUpdate`, handler `DatabaseException` e handler `AllExceptions`.)*
- **A)** Never, since the DatabaseException is not being triggered in the logic flow.
- **B)** Whenever the CheckPermissions if conditions is evaluated to False.
- **C)** Whenever the CreateOrUpdate Action triggers a DatabaseException.
- **D)** Never, since the AllExceptions handler takes precedence over the DatabaseException handler.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 39
**Enunciado:** Regarding **Site Properties**, which of the following statements is **true**?
- **A)** Site Properties cannot be changed inside a Server Action.
- **B)** Site Properties cannot have a Record Data type.
- **C)** Site Properties cannot be changed outside Service Studio.
- **D)** Site Properties cannot be assigned programmatically.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 40
**Enunciado:** Consider the following Roles selection of the `CinemaDetail` Screen. Which users can access this Screen?
*(Imagem não incluída no PDF; Role `Anonymous` marcada.)*
- **A)** Only authenticated users.
- **B)** Only users with both OSMDbAdmin and OSMDbUser Roles.
- **C)** All users, regardless of authentication.
- **D)** All users, as long as they have an application specific Role.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 41
**Enunciado:** Considering the `CheckRegisteredRole` Action, which of the following option is **True**?
- **A)** I can use the Action in an if condition inside a Client Action.
- **B)** I can use the Action on a Screen Data Action flow.
- **C)** I can use the Action to hide a widget on a Screen.
- **D)** I can use the Action on a Screen Expression.

- **Resposta correta:** B
- **Tua resposta:** C (❌ Errada)

---

### Pergunta 42
**Enunciado:** After opening the OSMDb module, the following appears on the Manage Dependencies dialog. Considering this scenario, select the **correct** option.
*(Imagem/Diagrama: Manage Dependencies com ícone azul de refresh ao lado do producer `OSMDb_Core`.)*
- **A)** A referenced element has been changed in the OSMDb_Core module.
- **B)** Clicking the Apply button will refresh all dependencies.
- **C)** The OSMDb_Core module has one or more references to elements in the OSMDb module.
- **D)** The OSMDb_Core module has been deleted from the Server.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 43
**Enunciado:** Consider the following Action, that calculates the square root (sqrt) of a positive decimal number (N). Knowing that the function was called with `N = -1`, and the debugger is stopped at the Start node, what will happen when the developer selects the **Continue (F9)** option highlighted in the picture?
*(Imagem/Diagrama: Client Action `SquareRoot` com breakpoint no `Start`, `If N < 0` -> Raise `InvalidNumber` -> Handler `InvalidNumber` faz `sqrt = 0` -> `ErrorMessage` -> `End`.)*
- **A)** The debugger will stop at the InvalidNumber Exception Handler flow.
- **B)** The debugger will stop at the N < 0 if node.
- **C)** The Action will end, with sqrt = 0, and an error message will appear on the Screen.
- **D)** The Action will end with sqrt = -1.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 44
**Enunciado:** Consider the following scenario where the developer is debugging a Client Action, defined in the scope of a Screen, and the execution is stopped at the Start node. Which of the following statements is **False**?
- **A)** It is possible to inspect and see the value of the Input Parameters of this Action.
- **B)** It is possible to inspect and see the value of the GetAge Action output.
- **C)** It is possible to inspect and see the value of the Screen widgets.
- **D)** It is possible to inspect and see the value of the Screen's Local Variable.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 45
**Enunciado:** Consider that the following Pagination widget will be used to implement the pagination functionality in a List of Employees. What should be the value of its **MaxRecords** property?
- **A)** The number of pages available to navigate to.
- **B)** The total number of Employees.
- **C)** The number of elements to be displayed per page.
- **D)** The total number of attributes used in the List.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 46
**Enunciado:** Consider a Form with a Button with the Built-in validations property set to **Yes**, and the On Click Destination set to a `SaveOnClick` Action. The `SaveOnClick` Action sends the Form data to the server, to store it in the database. How should we prevent the Form data from being sent to the server, if any of the fields contain data with an unexpected / invalid data type?
- **A)** Query the database, before storing the data.
- **B)** Nothing needs to be done. Having the built-in validation is sufficient.
- **C)** Check if the Form's Valid property is set to True, before storing the data.
- **D)** Set the Form Valid property to False, before storing the data.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 47
**Enunciado:** Consider the scenario in the picture with a List widget that has the output of the `GetEmployees` Aggregate as Source, and a ButtonGroup widget with three items. This ButtonGroup allows the end-user to sort the employees in the List, when one of its item is clicked. However, when a user clicks on a Button Group item, the List is not changing. What is the problem with this implementation?
- **A)** The developer forgot to add a Dynamic Sort to the Aggregate based on the ListSort Local Variable.
- **B)** The developer forgot to trigger an Event on the Sort Action to execute the sort on the List.
- **C)** The developer forgot to explicitly refresh the List widget in the Sort Action.
- **D)** The developer forgot to assign the ListSort Local Variable to the respective option chosen in the Sort Action.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 48
**Enunciado:** In which of the following situation, do you need to refresh the dependency of a consumer module?
- **A)** When the producer module does not exist in the OutSystems environment that you are connected to.
- **B)** In all these situations you need to check the Management Dependencies.
- **C)** When the element is no longer set as Public on the producer module.
- **D)** When the element was deleted from the producer module.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 49
**Enunciado:** In which of the following situation is it necessary to define a handler for a Block event?
- **A)** When the event has input parameters.
- **B)** When the Block has Placeholders.
- **C)** When the event's input parameters are all mandatory.
- **D)** When the event is defined as mandatory.

- **Resposta correta:** D
- **Tua resposta:** A (❌ Errada)

---

### Pergunta 50
**Enunciado:** The `After Fetch` event:
- **A)** Always happens after a new screen is requested.
- **B)** Only happens after a Data action finishes data.
- **C)** Is triggered after an Aggregate finishes fetching data.
- **D)** Happens after fetching new data through synchronization.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)
