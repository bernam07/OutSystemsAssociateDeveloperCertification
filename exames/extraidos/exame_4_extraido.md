# OutSystems Exame 4 Reactive — Extração e Correção

## Resumo
- **Total de perguntas:** 50
- **Respostas corretas:** 46
- **Respostas erradas:** 4
- **Percentagem:** 92% (46/50)
- **Perguntas erradas:** 4, 14, 23, 30
- **Nota sobre o gabarito:** A **Pergunta 21** foi dada como correta com a opção **B** pelo gabarito do exame, mas tecnicamente em OutSystems a resposta correta é a **D** (ver nota na Pergunta 21).

---

### Pergunta 1
**Enunciado:** Consider the data model below containing the Use, Asset and Category Entities. What needs to be changed in the data model to have Assets assigned to one specific Category?
*(Imagem/Diagrama: Diagrama de entidades com `User` (Id, Name, Username, Password, Email, MobilePhone, External_Id, Creation_Date, Last_Login, Is_Active), `Asset` (Id, Name, BelongsTo -> relação N:1 com User) e `Category` (Id, Name) sem relação com Asset.)*
- **A)** Create a new attribute, AssetId, in the Category Entity, with Data Type set to Long Integer.
- **B)** Create a new attribute, CategoryId, in the Asset Entity, with Data Type set to Category Identifier.
- **C)** Create a new attribute, AssetId, in the Category Entity, with Data Type set to Asset Identifier.
- **D)** Create a new attribute, CategoryId, in the Asset Entity, with Data Type set to Long Integer.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 2
**Enunciado:** Consider the following Entity Diagram. What is the data type of the Id attribute of the ShippingDetail Entity?
*(Imagem/Diagrama: Diagrama não incluído na exportação PDF; refere-se à entidade de extensão 1:1 `ShippingDetail` associada a `Order`.)*
- **A)** Order Identifier.
- **B)** ShippingDetail Identifier.
- **C)** Integer.
- **D)** Long Integer.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 3
**Enunciado:** Considering Static Entities, which of the following operations can be done at runtime?
- **A)** Expose the Entity as Public.
- **B)** Fetch data. Creating and editing records must be done in design time.
- **C)** Fetch, create and update records.
- **D)** Change the Is_Active attribute of the records to True/False.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 4
**Enunciado:** Consider the Excel file and Entity in the picture, where the Entity attributes have the following data types:
-Id: Long Integer, Auto-Number;
-Name: Text;
-Email: Email;
-PhoneNumber: Phone Number;
-Address: Text.
What will happen when we create an action to Bootstrap data from this Excel file to the Contact Entity?
*(Imagem/Diagrama: Imagem do ficheiro Excel e da Entidade não incluída na exportação PDF.)*
- **A)** The PhoneNumber attribute will not be populated with data, because the values in the respective Excel column do not match the expected data type.
- **B)** The matching attributes of the Entity will be populated with the values in the respective Excel columns.
- **C)** The Id attribute will not be populated with data, since there is no matching column in the Excel file.
- **D)** The Email attribute will not be populated with data, because the values in the respective Excel column do not match the expected data type.

- **Resposta correta:** B
- **Tua resposta:** A (❌ Errada)

---

### Pergunta 5
**Enunciado:** The Delete<Entity>Entity Action...
- **A)** ... returns the deleted record in its Output Parameter.
- **B)** ... requires that the record to be deleted exists in the database, otherwise an exception is thrown.
- **C)** ... expects the Entity record to be deleted, as Input Parameter.
- **D)** ... expects the Id of the record to be deleted, as Input Parameter.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 6
**Enunciado:** Consider that you need to change the database of your application, with the respective Data Model in the following image, to include the types of Products. A Product can **only** have one type and those types can be: Books, Music, Movies and Electronics. You have been told by the project manager that the Product types have not changed since last year. Which of the following is the **best** way to implement this change?
*(Imagem/Diagrama: Imagem do Data Model não incluída na exportação PDF.)*
- **A)** Add a Text attribute, Product Type, to Product and set its values to Books", "Music", "Movies and Electronics.
- **B)** Add a new Static Entity, Product Type, with 4 records, one for each type of product. In addition, add an attribute to the Static Entity of type Product Identifier.
- **C)** Add an Integer attribute, ProductType, to the Product Entity and set i for Books, 2 for Music, 3 for Movies, e for Electronics.
- **D)** Add a new Static Entity, ProductType, with 4 records, one for each type of product. In addition, add an attribute to the Product Entity of type Product Type Identifier.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 7
**Enunciado:** Considering the following Aggregate, what would be the **correct** way of obtaining the total price (including VAT) per Order?
*(Imagem/Diagrama: Imagem do Aggregate não incluída na exportação PDF.)*
- **A)** Create a Sum aggregation function over the OrderProduct.Quantity, Porduct.VAT and Product.WholesalePrice, then add a calculated attribute ProductTotalWithVAT with the expression: SumQuantity * SumWholesalePrice * (1 +SumVAT/100).
- **B)** Create a Server Action that calculates the total price with VAT for an Order, based on the OrderId Input Parameter. Then, add a calculated attribute ProductTotalWithVAT to the Aggregate, using the output of the Action.
- **C)** Create a calculated attribute ProductTotalWithVAT with the expression: Product.WholesalePrice * (1 + Product.VAT/100) * OrderProduct.Quantity. Then, use a Sum aggregation function over that attribute.
- **D)** This is not possible to do with an Aggregate. A SQL Query is required to determine the total price per Order.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 8
**Enunciado:** Considering calculated attributes in Aggregates, which of the following options is **correct**?
- **A)** Calculated attributes need to defined using SQL syntax.
- **B)** Calculated attributes are calculated in the memory by OutSystems before executing the final SQL.
- **C)** Calculated attributes allow using your own functions over existing attribute values.
- **D)** Calculated attributes allow adding new attributes based on the values of existing attributes.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 9
**Enunciado:** Consider the following Aggregate that shows all existing data from the Movie and MovieGenre Entities in the Preview area. Which of the following options is **correct**?
*(Imagem/Diagrama: Imagem do Aggregate não incluída na exportação PDF.)*
- **A)** Changing the Join to Only With won't display any data in the Preview.
- **B)** Changing the Join to Only With, and swapping the Entities order in the Join, will yield the same result in the Preview.
- **C)** Changing the Join to With or Without will yield the same result in the Preview.
- **D)** Changing the Join to With or Without, and swapping the Entities order in the Join, won't display any data in the Preview.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 10
**Enunciado:** In the following Aggregate, which of the following options is the **best** way to ignore the Orders that have been Canceled?
*(Imagem/Diagrama: Imagem do Aggregate não incluída na exportação PDF.)*
- **A)** Add a Filter with: OrderStatus <> "Canceled".
- **B)** Group By OrderStatus.Label and the Add a Group Filter with: OrderStatus.Label <> "Canceled".
- **C)** Add a Filter with: Order.OrderStatusId <> NullIdentifier().
- **D)** Add a Filter with: Order.OrderStatusId <> Entites.OrderStatus.Canceled.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 11
**Enunciado:** Considering a Screen with a Data Action that was created using the Fetching Data from Other Sources option, which of the following sentences is **False**?
- **A)** A Data Action can run Aggregates.
- **B)** A Data Action can execute server-side logic.
- **C)** A Data Action can run Advanced SQL Queries.
- **D)** A Data Action can execute client-side logic.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 12
**Enunciado:** Consider the Sorting criteria in the given Aggregate. If there are at least two movies with the same title and different years in the database, which of the following options is true?
*(Imagem/Diagrama: Imagem do Aggregate não incluída na exportação PDF.)*
- **A)** Deleting the Movie.Title sort will not change the query output.
- **B)** Changing the Movie.Year direction to Descending will sort the results by Title first and then by Year, changing the query output.
- **C)** Deleting the Movie.Year sort will require a new sorting criteria to replace it.
- **D)** Changing the Movie.Year direction to Descending will sort the results by Year first and the by Title, changing the query output.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 13
**Enunciado:** In the context of a Screen, when is the On After Fetch lifecycle event triggered?
- **A)** When an Input Parameter of the Screen changes.
- **B)** When an Aggregate or Data Action finishes fetching data.
- **C)** When a call to a Server Action terminates.
- **D)** When all the data in a Screen is fetched.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 14
**Enunciado:** Considering the On Ready lifecycle event, which of the following options is **true**?
- **A)** The On Ready Event is triggered right after the On Render event handler of the Screen or Block.
- **B)** The On Ready Event is triggered in a Block anytime the parent changes one of its Input Parameters.
- **C)** The On Ready Event is triggered after the Screen or Block structure is ready and before it is rendered.
- **D)** The On Ready Event is triggered before navigating to the Screen and the application starts fetching data.

- **Resposta correta:** C
- **Tua resposta:** B (❌ Errada)

---

### Pergunta 15
**Enunciado:** Consider a Screen with two Aggregates with the Fetch Property set to At Start. For both Aggregates, when is the data fetched?
- **A)** Concurrently after the On Initialize Event.
- **B)** Sequentially after the On Render Event.
- **C)** Sequentially after the On Ready Event.
- **D)** Concurrently after the On Ready Event.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 16
**Enunciado:** Considering the Screen Lifesycle and its Events, what happens when the user transitions from Screen A to Screen B?
- **A)** The Aggregates of Screen B run after the On Destroy Event of Screen A is triggered.
- **B)** The Aggregates of Screen B run when the Screen is rendered.
- **C)** The OnDestroy event of Screen A is triggered when Screen B is being initialized.
- **D)** The OnDestroy event of the Screen A is triggered after Screen B is rendered.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 17
**Enunciado:** If the Aggregate's Fetch property is set to Only On Demand, when will the query be triggered?
- **A)** When a Refresh Data node is used on the Aggregate.
- **B)** Automatically, when the data is needed on the screen.
- **C)** After the OnRender Event is triggered.
- **D)** After the Aggregates set to be fetched At Start.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 18
**Enunciado:** What needs to be changed in the following Aggregate to obtain the number of comments per Movie, for movies with one or more comments?
*(Imagem/Diagrama: Imagem do Aggregate não incluída na exportação PDF. Nota: o PDF contém apenas 3 opções nesta pergunta.)*
- **A)** Change the existing Join to With or Without and create a Count over the UserMovieComment Id attribute.
- **B)** Change the existing Join to With or Without, create a Group By over the Movie.Id attribute, and a Count over the UserMovieComment.Id attribute.
- **C)** Create a Group By over the Movie.Id attribute and a Count over the UserMovieComment.Id attribute.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 19
**Enunciado:** What will happen once the following Block is dropped on the area represented in the picture?
*(Imagem/Diagrama: Imagem não incluída na exportação PDF.)*
- **A)** The Block content will be displayed since it is possible to nest Blocks.
- **B)** The Block content will be displayed, but only if it is inside a Container.
- **C)** We will get an error since we cannot place a Block inside itself.
- **D)** We will get and error since we cannot nest a Block inside another Block.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 20
**Enunciado:** The Countdown Block has an OnClick Action that triggers the Start Event. What is expected when this Block is added to a Screen?
- **A)** Is is always necessary to specify an Event handler on the Screen for the Start Event.
- **B)** It is necessary to specify an Event handler on the Screen if the Start Event is mandatory.
- **C)** It is not necessary to specify and Event handler on the Screen because the Start Event does not have Input Parameters.
- **D)** It is necessary to specify an Event handler on the Screen because the Block will be added to a Screen.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 21
**Enunciado:** Which of the following options is correct regarding Event parameters?
- **A)** An Event needs to have an Output Parameter if it is mandatory.
- **B)** An Input Parameter of an Event is only available in the scope of the Block.
- **C)** An Output Parameter of an Event can send information to the parent.
- **D)** An Event Input Parameter can be used in Event handler Actions.

- **Resposta correta:** B *(⚠️ Gabarito do exame questionável — tecnicamente em OutSystems a resposta correta é **D**, pois os Input Parameters de um Event existem precisamente para passar dados do Block para o Event Handler no elemento pai, e não ficam restritos ao scope do Block.)*
- **Tua resposta:** B (✅ Correta segundo o gabarito do exame)

---

### Pergunta 22
**Enunciado:** Which of the following elements cannot be created in a Block?
- **A)** Server Actions.
- **B)** Aggregates.
- **C)** Events.
- **D)** Input Parameters.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 23
**Enunciado:** Consider the following List Widget, with the GetEmployees Aggregate as Source, and where the Input_Search is being used to search by employee name. However, when the user inserts a search keyword, the List of Employees is not being updated. What is missing in this application to make the search work?
*(Imagem/Diagrama: Imagem do widget/Aggregate não incluída na exportação PDF.)*
- **A)** Assign the SearchKeyword with the user inserted value.
- **B)** Trigger the OnRender event.
- **C)** Explicitly refresh the List Widget.
- **D)** Add a filter using the SearchKeyword to the Aggregate.

- **Resposta correta:** D
- **Tua resposta:** A (❌ Errada)

---

### Pergunta 24
**Enunciado:** Consider a Screen with the Form with multiple input fields inside it. When the end-user is filling the input fields with data, where is that data being stored?
- **A)** In the Entity attributes associated with each input field.
- **B)** In the Variables associated with each input field.
- **C)** In the Variable associated with the Form.
- **D)** In a Local Variable that is automatically created for the Form.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 25
**Enunciado:** Just Considering Built-in validations, which of the following scenarios would make a Form not valid?
- **A)** The user inserts a text on the field expect an Integer.
- **B)** The user inserts a number on a field expects a Text.
- **C)** The user inserts a negative number on a field that expects an Integer.
- **D)** The user inserts a date on a field that expect a Text.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 26
**Enunciado:** Consider the next image and assume that we have a ButtonGroup with three ButtonGroupItems with the following values: Entities.Priority.Low, Entities.Priority.High. What should be the data type of the element selected for the ButtonGroup's Variable property?
*(Imagem/Diagrama: Imagem não incluída na exportação PDF.)*
- **A)** Long Integer.
- **B)** Text.
- **C)** Priority Identifier.
- **D)** Priority.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 27
**Enunciado:** Considering the following example, what should be the option selected in the Options Value property of the Dropdown 1?
*(Imagem/Diagrama: Imagem não incluída na exportação PDF.)*
- **A)** User.Name.
- **B)** User.
- **C)** GetUsers.List.Current.
- **D)** User.Id.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 28
**Enunciado:** Consider that we have mandatory Input widget and we add a Label text next to it on the Screen. What is the necessary to do to automatically create a visual cue to end-user, indicating that the Input is mandatory?
- **A)** Select the corresponding Label in the properties of the Input widget.
- **B)** Select the corresponding Input widget in the properties of the Label.
- **C)** Drag the Input widget and drop it inside the Label.
- **D)** Enclose the Label and the Input widgets in a Container.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 29
**Enunciado:** Consider the following image, where we have the ContactList widget with the GetContacts Aggregate as Source. Which of the following options should we use to properly display the Name of all the contacts in the ContactList?
*(Imagem/Diagrama: Imagem não incluída na exportação PDF.)*
- **A)** ContactList.Contacts.Name.
- **B)** Home.GetContacts.Contacts.Name.
- **C)** Contacts.Name.
- **D)** GetContacts.List.Current.Contacts.Name.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 30
**Enunciado:** Considering the we want to display all the records of an Entity in a List widget, which of the following statements is true?
- **A)** An Expression in a List widget can combine the values of more than on attribute of a record.
- **B)** Only Expression widgets can be used to display the values of the Entity attributes.
- **C)** A List Item widget must be used to display the values of each record in the List widget.
- **D)** The Entity must be set as the Source property of the List widget.

- **Resposta correta:** A
- **Tua resposta:** D (❌ Errada)

---

### Pergunta 31
**Enunciado:** Considering a Link in a Block, which of the following options cannot be set as the Link's OnClick Destination?
- **A)** Event.
- **B)** Screen.
- **C)** Client Action.
- **D)** Server Action.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 32
**Enunciado:** Consider the following two final implementations of the Loop Action (A and B), where the Assign statement is detailed on the right. The goal is to repeat the RunActionWithNumber multiple times based on the value of the Number input Parameter (e.g. 10). Based on this scenario, select the correct option.
*(Imagem/Diagrama: Imagem dos fluxos A e B não incluída na exportação PDF.)*
- **A)** Only Alternative A is possible, since a For Each always requires a list to iterate.
- **B)** Both alternatives are possible, as long as the if and For Each conditions are set to Number >= 0.
- **C)** Only Alternative B is possible, since the For Each is the logic statement used to implement generic loops.
- **D)** Only Alternative A is possible, as long as the condition is Number < 0.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 33
**Enunciado:** Consider the following Client Action containing a Switch, where its conditions are detailed on the connectors. The assignments are also detailed on the respective Assign labels. Which of the following options is correct?
*(Imagem/Diagrama: Imagem do fluxo com Switch não incluída na exportação PDF.)*
- **A)** If the value of the Priority is "d", the Color output will be "grey".
- **B)** The Color output value will always be "red", "yellow" or "green".
- **C)** The Color output value will always be "grey".
- **D)** The Color output value will be influenced by the order of the conditions.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 34
**Enunciado:** Before iterating a non-empty List, the List.Current element contains...
- **A)** ... the last record of the list.
- **B)** ... null.
- **C)** ... an empty record.
- **D)** ... the first record of the List.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 35
**Enunciado:** Consider the following Client Action, where the Employee_Create Action has no exception handling and just creates a new record in the database, using the CreateEmployee Entity Action. What happens if an exception is thrown during the execution of the Employee_Create Action?
*(Imagem/Diagrama: Imagem do fluxo da Client Action não incluída na exportação PDF.)*
- **A)** No exception flow is executed and an information message is shown.
- **B)** The AllExceptions flow is executed and an error message is shown.
- **C)** The DatabaseException flow is executed and and error message is shown.
- **D)** Both DatabaseException and AllExceptions flows are executed and an error message is shown.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 36
**Enunciado:** Setting the Function property of a Client Action to Yes...
- **A)** ... allows it to be used in other modules.
- **B)** ... allows it to be used in Screen Expressions and other Client Actions.
- **C)** ... restricts it to be exclusively used in other Client Actions.
- **D)** ... restricts it to be exclusively used in an Expression on a Screen.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 37
**Enunciado:** Regarding Client and Server Actions, which of the following options is correct?
- **A)** Server Actions can be set as the Destination of a Button / Link.
- **B)** Server Actions can execute Client Actions.
- **C)** Client Actions can execute Public Server Actions, defined on the modules.
- **D)** Client Actions from a Screen can execute Client Actions from other Screens.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 38
**Enunciado:** Consider the following Action flow, where some custom validations are performed over data submitted from the Form named ProductForm. Which of the following conditions should be set for the highlighted if statement?
*(Imagem/Diagrama: Imagem do fluxo de validação não incluída na exportação PDF.)*
- **A)** ProductForm.Valid = True.
- **B)** ProductForm.Price <= 0 and ProductForm.QuantityInStock < 0.
- **C)** ProductForm.Price > 0 and ProductForm.QuantityInStock >= 0.
- **D)** ProductForm.Valid = False.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 39
**Enunciado:** Consider the following Server Action. When the if statement is evaluated to False. What is the expected behavior?
*(Imagem/Diagrama: Imagem do fluxo da Server Action não incluída na exportação PDF.)*
- **A)** The DatabaseException flow of the Action will be executed.
- **B)** The Exception will not be handled.
- **C)** The AllExceptions flow of the Action will be executed.
- **D)** The Exception will be handled by the module Global Exception Handler.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 40
**Enunciado:** Which of the following options is correct, regarding Site Properties in OutSystems?
- **A)** Site Properties can be changed programatically.
- **B)** Site Properties can only be changed in Service Center.
- **C)** Site Properties can have the List Data Type.
- **D)** Site Properties can only be changed in Service Studio.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 41
**Enunciado:** Consider the following Roles properties from the CinemaDetail Screen. What are the minimum required Roles for a user to access this Screen?
*(Imagem/Diagrama: Imagem das propriedades de Roles não incluída na exportação PDF.)*
- **A)** Either OSMDbAdmin or OSMDbUser.
- **B)** Registered and either the OSMDbAdmin or OSMDbUser.
- **C)** Registered and OSMDbAdmin and OSMDbUser.
- **D)** Registered.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

---

### Pergunta 42
**Enunciado:** Não temos a questão. *(Pergunta original omissa no PDF; refere-se a verificar a role `Manager` através de `CheckManagerRole` para usar numa condição `If` num Screen Reactive.)*
- **A)** Create a Client Action that uses the CheckManagerRole, set it as a Function and set its output to the result of the CheckRole Action. Then, use the output in the if condition.
- **B)** Create a Data Action that uses the CheckManagerRole and set its output to the result of the CheckRole Action. Then, use the output in the if condition.
- **C)** Just use the CheckManagerRole Action directly in the if condition.
- **D)** Use the CheckManagerRole action directly in the if condition and have just the Manager Role selected in this Screen roles.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 43
**Enunciado:** Setting the Expose Read Only property of a Entity to Yes will...
- **A)** ... require other modules to use SQL Queries to modify the Entity's data.
- **B)** ... allow other modules to use all of its Entity Actions.
- **C)** ... only expose the Get<Entity>Entity Action to other modules.
- **D)** ... prevent other modules from accessing the Entity records.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 44
**Enunciado:** Não temos a questão. Mas temos a mesma imagem no exame 1 com a seguinte pergunta: After opening the OSMDb module, the following appears on the Manage Dependencies dialog. Considering this scenario, select the **correct** option.
*(Imagem/Diagrama: Imagem do diálogo Manage Dependencies não incluída na exportação PDF.)*
- **A)** An element from the OSMDb_Core module referenced in the OSMDb module had a breaking change.
- **B)** Publishing the OSMDb module will refresh all the dependencies.
- **C)** Clicking the Apply button will refresh all the dependencies.
- **D)** One element from the OSMDb_Core module was modified, but the module was not published yet.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

---

### Pergunta 45
**Enunciado:** When are Client Variables reset to their default values?
- **A)** Client Variables are never reset.
- **B)** Whenever the user logs in.
- **C)** Whenever the user logs out.
- **D)** Whenever the user closes browser.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 46
**Enunciado:** Consider the following Action that calculates the square root (sqrt) of a positive decimal number (N). Knowing that the function was called with N = 4, and the debugger is stopped at the Start node, what will happen when the developer selects the Continue (F9) option highlighted in the picture?
*(Imagem/Diagrama: Imagem do fluxo no debugger não incluída na exportação PDF.)*
- **A)** The Action will end, with sqrt = 0, and an error message will appear on the Screen.
- **B)** The debugger will stop at the sqrt = N Assign node.
- **C)** The Action will end, with sqrt = Sqrt(N).
- **D)** The debugger will stop at the N < 0 if node.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 47
**Enunciado:** In OutSystems, how can application error logs be analysed?
- **A)** In Service Studio, under the Logic tab.
- **B)** In Service Center, under the Monitoring tab.
- **C)** Must be queried directly from the database.
- **D)** The errors can only be analysed at runtime.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 48
**Enunciado:** Consider that we want to add the pagination functionality to a List widget that displays employees fetched using the GetEmployees Aggregate. What should be the value of the TotalCount property of the Pagination widget?
- **A)** The number of elements displayed per page.
- **B)** The Count output of the Aggregate.
- **C)** The number of elements in the Aggregate output list.
- **D)** The total number of pages available to navigate to.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

---

### Pergunta 49
**Enunciado:** Complete the following sentence: "The Form's Valid property...
- **A)** ... is set to True only if the user fills all of the Form's mandatory input fields."
- **B)** ... must be explicitly set to True or False using an Assign."
- **C)** ... is set to False when one of the Form's input fields is not valid."
- **D)** ... is set to False when a Database Exception is triggered when saving the Form data."

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

---

### Pergunta 50
**Enunciado:** Consider the following List widget that has the GetEmployees Aggregate as Source, and the Button Group that allows end-users to dynamically sort the List when one of the items is clicked. The dynamic sorting is working properly, but now there is a new requirement: allow the end-user to also sort by Email. What is necessary to do in the application to support the new requirement?
*(Imagem/Diagrama: Imagem do List widget e Button Group não incluída na exportação PDF.)*
- **A)** Add a new Local Variable to hold the new sorting by Email.
- **B)** Add a new ButtonGroupItem and set its value to {Employee}.[Email].
- **C)** Change the logic of the Sort Action to include the new sorting by Email.
- **D)** Add a new Sort criteria by Employee.Email to the Aggregate.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)
