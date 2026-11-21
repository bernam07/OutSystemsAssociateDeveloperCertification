# OutSystems Exame 3 Reactive — Extração Completa

## Resumo
- **Total de perguntas:** 50
- **Respostas corretas:** 40
- **Respostas erradas:** 10
- **Percentagem:** 80% (40/50)
- **Perguntas erradas:** 3, 6, 10, 16, 19, 21, 23, 24, 30, 49

---

### Pergunta 1
**Enunciado:** If we have multiple Exception Handlers in an Action flow and an Exception is raised...
- **A)** … the execution is always moved to the Global Exception Handler.
- **B)** … the execution is moved to the Exception Handler that is most specific to the Exception.
- **C)** … the execution is moved to all Exception Handlers of the Action.
- **D)** … a Switch statement is needed to select which Exception Handler will continue the execution.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

### Pergunta 2
**Enunciado:** In an Aggregate, the Sources section is used for...
- **A)** Defining values for testing the Aggregate’s output records.
- **B)** Defining the Entities we want to retrieve records from.
- **C)** Defining conditions to get specific subsets of records.
- **D)** Defining the order of the Aggregate’s output records.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

### Pergunta 3
**Enunciado:** Considering that we can add several filters to an Aggregate, which of the following options is false?
- **A)** A record is included in the output if it matches at least one of the filters.
- **B)** Filters are concatenated with the AND operator.
- **C)** All filters are translated to SQL and included in the WHERE clause.
- **D)** Logical operators and some built-in functions can be used inside filters.

- **Resposta correta:** A
- **Tua resposta:** B (❌ Errada)

### Pergunta 4
**Enunciado:** Regarding Sorting in Aggregates, which of the following options is correct?
- **A)** Aggregates only support one sorting criterion.
- **B)** If more than one sorting criterion is defined, all of them must have the same direction (ascending or descending).
- **C)** It is mandatory to set the direction for all sorting criteria (ascending or descending).
- **D)** It is only possible to set multiple sorting criteria if duplicate records exist in the entity.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

### Pergunta 5
**Enunciado:** In an Aggregate, the purpose of the Test Values section is…
- **A)** To define values for testing the preview of the Aggregate’s output.
- **B)** To set the conditions to get specific records, not all the records.
- **C)** To define the order of its output records.
- **D)** To define the Entities we want to get records from.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

### Pergunta 6
**Enunciado:** Regarding Screen Aggregates, which of the following options is false?
- **A)** Screen Aggregates run asynchronously and in parallel.
- **B)** Screen Aggregates only exist within the scope of the Screen where they were defined.
- **C)** Screen Aggregates can only be executed when explicitly called.
- **D)** Screen Aggregates can only fetch data from the database.

- **Resposta correta:** C
- **Tua resposta:** D (❌ Errada)

### Pergunta 7
**Enunciado:** How is the data fetched by an Aggregate bound to a Table or a List widget?
- **A)** By setting the Source property of the widget to the output of the Aggregate.
- **B)** The binding is done automatically since the Aggregate is in the scope of the Screen.
- **C)** By adding an Expression inside the widget that refers to an attribute of the data fetched by the Aggregate.
- **D)** By creating a Screen Action that programmatically assigns the widget to the data fetched by the Aggregate.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

### Pergunta 8
**Enunciado:** Considering ListItem and List Actions, which of the following options is false?
- **A)** List Actions can only be used inside List Items.
- **B)** List Items can be used outside of Lists.
- **C)** When List Items have the full swiping option activated, the List Action is not necessary.
- **D)** The List Action triggers a Screen Action that will have the logic to be executed on swipe.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

### Pergunta 9
**Enunciado:** Regarding data relationships, which of the following options is correct?
- **A)** An Entity must have an identifier to allow relationships.
- **B)** A reference attribute needs to be mandatory.
- **C)** An Entity can only have one reference attribute.
- **D)** The Entity identifier must be an integer.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

### Pergunta 10
**Enunciado:** Which of the following steps is necessary to create a 1-to-1 relationship between Entity A and Entity B?
- **A)** Set the data type of the identifier attribute of Entity B to Entity A Identifier.
- **B)** Add a new Entity C, with two reference attributes of type Entity A Identifier and Entity B Identifier.
- **C)** Add a new reference attribute of type Entity B Identifier to Entity A.
- **D)** Add a new Entity C, with the identifier attribute being a composition of types Entity A Identifier and Entity B Identifier.

- **Resposta correta:** A
- **Tua resposta:** C (❌ Errada)

### Pergunta 11
**Enunciado:** Which of the following steps is necessary to create a 1-to-many relationship between a Master Entity A and a Detail Entity B?
- **A)** Set the data type of the identifier attribute of Entity B to Entity A Identifier.
- **B)** Add a new Entity C, with two reference attributes of type Entity A Identifier and Entity B Identifier.
- **C)** Entity A must have a reference attribute of type Entity B Identifier.
- **D)** Entity B must have a reference attribute of type Entity A Identifier.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

### Pergunta 12
**Enunciado:** Which of the following steps is necessary to create a many-to-many relationship between Entity A and Entity B?
- **A)** Set the data type of the identifier attribute of Entity B to Entity A Identifier.
- **B)** Add a new reference attribute of type Entity B Identifier to Entity A.
- **C)** Add a new Entity C, with two reference attributes of type Entity A Identifier and Entity B Identifier.
- **D)** Add a new reference attribute of type Entity B Identifier to Entity A and a new reference attribute of type Entity A Identifier to Entity B.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

### Pergunta 13
**Enunciado:** Regarding Indexes, which of the following options is correct?
- **A)** Custom indexes cannot be added to an Entity.
- **B)** Indexes speed up data retrieval without any kind of impact.
- **C)** Unique indexes help prevent data duplication.
- **D)** Indexes over referenced attributes cannot be deleted.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

### Pergunta 14
**Enunciado:** Regarding the Delete Rule property, which of the following options does not guarantee referential integrity?
- **A)** Protect.
- **B)** Delete.
- **C)** Ignore.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

### Pergunta 15
**Enunciado:** Which of the following behaviors does not apply to Forms?
- **A)** A Form groups input widgets and allows displaying and editing data.
- **B)** A Form has a Source property that will hold the values submitted by the user.
- **C)** Besides input widgets, a Form can hold other widgets such as Links and Buttons.
- **D)** A Form is useful to validate data submitted by the user.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

### Pergunta 16
**Enunciado:** Considering the Dropdown and the Button Group, which of the following options is false?
- **A)** A Button Group needs a Button Group Item to represent each option that the user will have available to choose from.
- **B)** The List property of the Dropdown defines the data that will appear as options to a user on a Screen.
- **C)** Each Button Group Item within a Button Group has a Variable property to save the option chosen by the user.
- **D)** The Variable property of the Dropdown will hold the value selected by the user. That value is defined in the Options Value property.

- **Resposta correta:** C
- **Tua resposta:** D (❌ Errada)

### Pergunta 17
**Enunciado:** The Checkbox or Switch Widgets are bound to a variable of which type?
- **A)** Text.
- **B)** Integer.
- **C)** Boolean.
- **D)** Date.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

### Pergunta 18
**Enunciado:** Considering Inputs and Labels, which of the following options is correct?
- **A)** Every input must have a Label associated with.
- **B)** An input widget can only be used for the Text data type.
- **C)** To access the value submitted in an Input widget, we can simply use InputName.Value.
- **D)** Labels associated with mandatory fields will display a visual cue on the Screen.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

### Pergunta 19
**Enunciado:** What is the Screen behavior when a widget is not valid (Valid property set to False)?
- **A)** The Screen displays the widget grayed out, and displays the validation error message on the input.
- **B)** The widget does not appear on the Screen and the validation message appears in its place.
- **C)** Displays the regular widget and displays the validation error message when we hover the mouse.
- **D)** Displays the regular widget, applies a specific styling (e.g. red border), and displays the validation error message.

- **Resposta correta:** D
- **Tua resposta:** A (❌ Errada)

### Pergunta 20
**Enunciado:** Which of the following options is not a built-in validation in OutSystems?
- **A)** Mandatory Fields.
- **B)** Maximum length of text fields.
- **C)** Data types of input fields.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

### Pergunta 21
**Enunciado:** Which of the following options is correct regarding the Valid property of the Form?
- **A)** The Valid property of the Form should be checked after the last custom validation.
- **B)** The Valid property of the Form is automatically changed to False when all the input fields of the Form are not valid.
- **C)** The Valid property of the Form should be explicitly set to False (e.g. with an Assign) when an input field is not valid.
- **D)** When built-in validations are enabled, the Valid property of the Form is automatically checked before executing the client action logic.

- **Resposta correta:** A
- **Tua resposta:** D (❌ Errada)

### Pergunta 22
**Enunciado:** Considering Users and Roles in OutSystems, which of the following options is correct?
- **A)** By default, end-users are managed in the built-in Users application.
- **B)** End-users can only be created programmatically, using Actions from the Users application.
- **C)** There are three built-in roles in OutSystems: Anonymous, AppUser and Registered.
- **D)** All users, with or without a login, have automatically the Registered Role.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

### Pergunta 23
**Enunciado:** In OutSystems, how do we restrict access to a Screen?
- **A)** Go to the Users application and associate the Screen to a specific role.
- **B)** In the Screen Properties, untick roles to restrict their access.
- **C)** Use the CheckRole Action.
- **D)** We don’t. Only users with a username and password can access.

- **Resposta correta:** B
- **Tua resposta:** A (❌ Errada)

### Pergunta 24
**Enunciado:** Considering the built-in Role Actions, which of the following options is false?
- **A)** The CheckRole Action checks if a user has that particular Role.
- **B)** The GrantRole Action allows to grant a Role to a user programmatically.
- **C)** The RevokeRole Action allows to remove a Role from a user programmatically.
- **D)** The CreateUserWithRole Action creates an end-user and assigns it the Role.

- **Resposta correta:** D
- **Tua resposta:** C (❌ Errada)

### Pergunta 25
**Enunciado:** In OutSystems, where can we place breakpoints?
- **A)** In Actions only (Client-side and Server-Side).
- **B)** Server-side logic only.
- **C)** Client-side logic only.
- **D)** In Actions and Variables.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

### Pergunta 26
**Enunciado:** In OutSystems, it is possible to inspect the values of variables while debugging.
- **A)** True.
- **B)** False.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

### Pergunta 27
**Enunciado:** Which of the following commands is not available in the OutSystems debugger?
- **A)** Stop Debugging.
- **B)** Continue Request.
- **C)** Step Over.
- **D)** Restart Debugging.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

### Pergunta 28
**Enunciado:** When debugging a consumer module, how do we guarantee that the execution stops on breakpoints defined in the producer module?
- **A)** We just need to set breakpoints in the producer module. The execution will stop on its breakpoints automatically.
- **B)** We need to also start the debugger on the producer module.
- **C)** Nothing, just leave Service Studio open.
- **D)** In the producer, set the Entry Module property to the consumer module.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

### Pergunta 29
**Enunciado:** Consider an Aggregate with a "With or Without" join between two entities. What is the expected output of the Aggregate?
- **A)** All records from both Entities (FULL OUTER JOIN).
- **B)** Only records where there is a match between the two Entities (INNER JOIN).
- **C)** All records from the left entity even if there is no match in the right entity (LEFT JOIN).
- **D)** All records from the right entity even if there is no match in the left entity (RIGHT JOIN).

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

### Pergunta 30
**Enunciado:** Considering that Aggregates can have hidden columns, which of the following options is correct?
- **A)** Hiding columns in the Aggregate only affects the preview of the output.
- **B)** Columns that are empty in the database are automatically hidden.
- **C)** The hidden columns help optimizing the Aggregate.
- **D)** The hidden columns are not part of the output.

- **Resposta correta:** A
- **Tua resposta:** D (❌ Errada)

### Pergunta 31
**Enunciado:** Which of the following elements can’t be used to create calculated attributes in an Aggregate?
- **A)** Value of the attributes of the Source Entities.
- **B)** Built-in Functions that can be translated to SQL (e.g. Length(), Power()).
- **C)** Variables.
- **D)** Server Actions using Entity Attributes.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

### Pergunta 32
**Enunciado:** Consider that we want to apply aggregation functions in an Aggregate. Which of the following options is false?
- **A)** We can apply multiple aggregation functions inside an Aggregate.
- **B)** The output of the Aggregate will contain all attributes from the Source Entities plus the aggregation columns.
- **C)** We can apply the following functions on attributes of integer data type: sum, max, min, count and average.
- **D)** The output of the Aggregate will not include the columns at grey.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

### Pergunta 33
**Enunciado:** In OutSystems, a Block is a reusable UI component. Which of the following is NOT correct?
- **A)** Block promotes reusability, i.e. develop once, reuse many times.
- **B)** A Block encapsulates its own logic.
- **C)** A Block improves maintainability, i.e., change the design or functionality, affect all usages.
- **D)** A Block can only be reused once.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

### Pergunta 34
**Enunciado:** A Block can be used...
- **A)** Only inside other Screens.
- **B)** Inside Screens and Blocks, including itself.
- **C)** Inside Screens and Blocks, except on itself.
- **D)** Only inside other Blocks.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

### Pergunta 35
**Enunciado:** Regarding Placeholders, which of the following options is correct?
- **A)** A Placeholder reserves space in the interface to be allocated when the block is instantiated.
- **B)** When a Block with Placeholders is instantiated, it is mandatory to place at least one widget inside the placeholders.
- **C)** Placeholders can be added to Screens and Blocks.
- **D)** Only one placeholder may be added per Block.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

### Pergunta 36
**Enunciado:** Regarding Block Events, which of the following options is false?
- **A)** Events can be defined at the Block or Screen level.
- **B)** Events allow to pass information from the Block’s scope to the parent scope.
- **C)** Events are triggered by a Block and handled by its parent.
- **D)** Two instances of a Block may use the same handler for the same event.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

### Pergunta 37
**Enunciado:** In which of the following situations is it necessary to define a handler for a Block Event?
- **A)** When the event has Input Parameters.
- **B)** When the Block has Placeholders.
- **C)** When the event Input Parameters are all mandatory.
- **D)** When the Event is set to mandatory.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

### Pergunta 38
**Enunciado:** In which of the following situations is the On Parameters Changed Event triggered?
- **A)** If the value of a Block Input Parameters changes inside a Client Action of the Block.
- **B)** The On Parameters Changed must be explicitly triggered by the parent of the Block.
- **C)** When the parent of the Block changes the value of at least one of the Block Input Parameters.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

### Pergunta 39
**Enunciado:** Which of the following events is not available in Screens or Blocks?
- **A)** Initialize.
- **B)** Ready.
- **C)** After Fetch.
- **D)** Render.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

### Pergunta 40
**Enunciado:** Considering the Initialize event of a Screen, which of the following would be the best use case for that event?
- **A)** Retrieve data from the server database.
- **B)** Act on data returned by a Data Action.
- **C)** Manipulate the DOM.
- **D)** Set the default value of a Local Variable.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

### Pergunta 41
**Enunciado:** Which of the following is the correct order of occurrence of events in a Screen?
- **A)** Initialize, Ready, Render, Destroy.
- **B)** Initialize, Destroy, Ready, Render.
- **C)** Ready, Initialize, Render, Destroy.
- **D)** Initialize, Render, Ready, Destroy.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

### Pergunta 42
**Enunciado:** Which of the following options is false regarding Screen Aggregates?
- **A)** The Render Event on the Screen is triggered when an Aggregate with the Fetch property set to "only on demand" finishes its execution.
- **B)** A Screen Aggregate can be triggered when a screen is initializing or only On Demand.
- **C)** All Aggregates, by default, have the Fetch property set to On Demand.
- **D)** The On After Fetch Event is triggered for every Aggregate, regardless of its Fetch property.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

### Pergunta 43
**Enunciado:** Consider an Aggregate with the Fetch property set to Only On Demand. When does that Aggregate run?
- **A)** Automatically, when the Screen is initializing.
- **B)** Programmatically, using a Refresh Data node in a Screen Action.
- **C)** Automatically, when the Aggregates set to run "At Start" finish.
- **D)** Programmatically, using a Server Action.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

### Pergunta 44
**Enunciado:** Which of the following options is correct regarding Client Variables?
- **A)** The value of a Client Variable is shared among all logged-in users.
- **B)** Lists or Binary Data can also be stored on Client Variables.
- **C)** Client Variables should be used to store confidential information.
- **D)** Client Variables are useful to cache frequently accessed information.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

### Pergunta 45
**Enunciado:** Which of the following would be a good use case for a Client Variable?
- **A)** Credit Card Number.
- **B)** Profile Picture.
- **C)** User Identifier.
- **D)** User Name.

- **Resposta correta:** D
- **Tua resposta:** D (✅ Correta)

### Pergunta 46
**Enunciado:** The value of a Site Property can be modified in Service Center to change the application behavior at runtime.
- **A)** True.
- **B)** False.

- **Resposta correta:** A
- **Tua resposta:** A (✅ Correta)

### Pergunta 47
**Enunciado:** Which of the following is a good use case for a Site Property?
- **A)** Current user ID.
- **B)** Total Stock Quantity of Products.
- **C)** REST Web Service API Key.
- **D)** Search Keyword.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)

### Pergunta 48
**Enunciado:** Which of the following options is correct, when implementing pagination with Tables or Lists?
- **A)** The Start Index property of the Pagination holds the current page number.
- **B)** The Max Records property of the Pagination holds the number of records to show per page.
- **C)** The Total Count input of the Pagination pattern should be set to the number of records per page.

- **Resposta correta:** B
- **Tua resposta:** B (✅ Correta)

### Pergunta 49
**Enunciado:** Regarding sorting in a Table, which of the following options is correct?
- **A)** All header cells need to have the Sort Attribute property defined.
- **B)** Only the Sort Attribute of the header cells needs to be defined. Data is refreshed automatically.
- **C)** The On Sort event has an input parameter containing the clicked column.

- **Resposta correta:** C
- **Tua resposta:** B (❌ Errada)

### Pergunta 50
**Enunciado:** Regarding sorting Lists, which of the following options is correct?
- **A)** Lists have a built-in On Sort event.
- **B)** Sort clauses cannot be changed dynamically at runtime when using Lists.
- **C)** Other Widgets should be used to allow the end-user to define the sort criteria.

- **Resposta correta:** C
- **Tua resposta:** C (✅ Correta)
