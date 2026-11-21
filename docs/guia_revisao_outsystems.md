# Guia de Revisão — OutSystems Associate Reactive Developer

> **Resumo dos teus 4 simulados:** Estás muito bem preparado! A nota mínima no exame oficial é **70%** e a tua média global é **83,5%** com tendência crescente até aos **92%** no Exame 4.

## 1. Resumo de Pontuações

| Exame | Corretas | Erradas | Nota | Ficheiro Extraído |
| :--- | :---: | :---: | :---: | :--- |
| **Exame 1** | 39 / 50 | 11 | **78%** | `exame_1_extraido.md` |
| **Exame 2** | 42 / 50 | 8 | **84%** | `exame_2_extraido.md` |
| **Exame 3** | 40 / 50 | 10 | **80%** | `exame_3_extraido.md` |
| **Exame 4** | 46 / 50 | 4 | **92%** | `exame_4_extraido.md` |
| **TOTAL** | **167 / 200** | **33** | **83,5%** | — |

---

## 2. ⚠️ Atenção: 2 Possíveis Erros nos Gabaritos dos Simulados

Antes de reveres os teus erros, tem atenção a estas 2 perguntas onde o gabarito do formulário Microsoft parece ter um erro técnico face à documentação oficial da OutSystems:

1. **Exame 4 — Pergunta 21 (Event Parameters):**
   - *Enunciado:* "Which of the following options is correct regarding Event parameters?"
   - *Gabarito do simulado:* **B** ("An Input Parameter of an Event is only available in the scope of the Block.")
   - *Verdade oficial OutSystems:* **D** ("An Event Input Parameter can be used in Event handler Actions.")
   - *Porquê:* Os Events só têm **Input Parameters** (nunca Output Parameters), e o objetivo desses Input Parameters é exatamente enviar dados do Block para o **Event Handler** no pai (Screen ou Block pai).

2. **Exame 2 — Pergunta 12 (Button On Click Destination):**
   - *Enunciado:* "Considering a Button in a Screen, which of the following options **cannot** be set as its On Click Destination?"
   - *Gabarito do simulado:* **B** ("Client Action")
   - *Verdade oficial OutSystems:* **C** ("Block") — um Button pode navegar para um **Screen**, um **External Site** ou executar uma **Client Action (Screen Action)**, mas **nunca** pode ter um **Block** como destino. *(Na tua tentativa puseste D - External Site, que também é permitido.)*

---

## 3. Revisão Completa dos Teus 33 Erros (Agrupados por Tema)

### Tema A: Ciclo de Vida de Screens e Blocks (3 erros — SAI SEMPRE NO EXAME!)

Memoriza esta ordem exata:
1. **`On Initialize`**: Antes de renderizar o Screen/Block e **antes** de os Aggregates/Data Actions arrancarem. (Sem acesso ao DOM).
2. **`On Ready`**: Assim que a estrutura (DOM) do Screen/Block está pronta, **antes** do primeiro render visual.
3. **`On Render`**: Depois do `On Ready` e **sempre que os dados subjacentes do Screen ou Block mudam** (re-render).
4. **`On Parameters Changed`** *(só existe em Blocks!)*: Sempre que o **pai altera um Input Parameter** do Block.
5. **`On Destroy`**: Antes de o Screen ou Block ser destruído/removido da memória.

*Os teus erros neste tema:*
- **Exame 1, P14 (`On Render`):** Escolheste D ("só ao transitar de ecrã"). **Correta: C** — é disparado sempre que os dados do Screen ou Block mudam.
- **Exame 2, P6 (`On Initialize`):** Escolheste B ("depois de renderizado"). **Correta: A** — é disparado antes de renderizar e antes de ir buscar dados.
- **Exame 4, P14 (`On Ready`):** Escolheste B ("quando o pai muda um Input Parameter"). **Correta: C** — quando o DOM/estrutura está pronto, antes de renderizar. (Mudança de Input Parameter = `On Parameters Changed`).

---

### Tema B: Aggregates, Filters, Sorting, Group By e Refresh (7 erros)

- **Exame 1, P12 (Add Sort):** Já havia `#1 Order.Date Ascending` e adicionou-se `Customer.Name`. Escolheste C. **Correta: A** — o 2.º critério serve de desempate: registos com a **mesma `Order.Date`** ficam ordenados por `Customer.Name`.
- **Exame 1, P23 (Atualizar List com InputSearch):** Escolheste B ("Explicitly refresh the List Widget"). **Correta: A** — **Refresh Data no Aggregate (`GetEmployees`)**. Em Reactive Web **nunca** fazes refresh a widgets; atualizas os dados e a UI reage automaticamente!
- **Exame 4, P23 (Pesquisa não atualiza List):** Escolheste A ("Assign SearchKeyword"). **Correta: D** — o Input tem *two-way binding* automático para a variável `SearchKeyword`, não precisas de `Assign`. O que faltava era adicionar um **Filter** com `SearchKeyword` ao Aggregate.
- **Exame 2, P3 (Group By / Aggregations Output):** Escolheste B ("agregações + todos os atributos da Entity"). **Correta: A** — assim que usas **Group By** ou funções de agregação (`Count`, `Sum`, `Average`, `Min`, `Max`), o output do Aggregate devolve **APENAS** os atributos agrupados e agregados!
- **Exame 3, P3 (Múltiplos Filters — pergunta de "FALSE"):** Escolheste B. **Correta: A** — vários Filters num Aggregate são combinados com **`AND`** (têm de cumprir *todos* os filtros), logo dizer "basta cumprir pelo menos um" é **falso**.
- **Exame 3, P6 (Screen Aggregates — pergunta de "FALSE"):** Escolheste D. **Correta: C** — por defeito têm `Fetch = At Start` (correm automaticamente ao iniciar o ecrã, assíncronos e em paralelo), portanto dizer que "só correm quando chamados explicitamente" é **falso**. *(Só precisam de chamada explícita se estiverem como `Only on demand`.)*
- **Exame 3, P30 (Hidden Columns num Aggregate):** Escolheste D ("não fazem parte do output"). **Correta: A** — esconder colunas num Aggregate **só afeta a pré-visualização (preview)** no Service Studio; continuam a existir no output e não afetam otimização (a plataforma otimiza automaticamente consoante o uso).

---

### Tema C: Blocks e Events (3 erros)

- **Exame 1, P21 (Enviar dados do Block para o Pai):** Escolheste A ("Local Variable Public"). **Correta: C** — cria-se um **Event no Block** com o valor como **Input Parameter** e dispara-se esse Event quando o utilizador escolhe a classificação. *(Local Variables de Blocks nunca são públicas.)*
- **Exame 1, P22 (Características dos Blocks):** Escolheste A ("Block pode ter Output Parameters"). **Correta: B** — um Block **pode ter Client Actions no seu scope**. **Nunca** tem Output Parameters, nunca pode ser instanciado dentro de si próprio (recursão) e pode ser instanciado tanto em Screens como noutros Blocks.
- **Exame 1, P49 (Quando é obrigatório definir Handler para um Event):** Escolheste A ("quando tem input parameters"). **Correta: D** — apenas quando o Event tem a propriedade **`Is Mandatory = Yes`**.

---

### Tema D: Forms e Validações (3 erros)

- **Exame 1, P28 (`Input.Valid = False`):** Escolheste D ("é obrigatório pôr `ValidationMessage`"). **Correta: A** — ao definir `Input.Valid = False`, a propriedade **`Form.Valid` passa automaticamente a `False`**. (`ValidationMessage` é opcional, embora boa prática).
- **Exame 3, P19 (Aspeto visual de widget inválido):** Escolheste A ("grayed out"). **Correta: D** — o widget continua normal/editável, recebe estilo de erro (borda vermelha) e mostra a mensagem de validação por baixo.
- **Exame 3, P21 (`Form.Valid` na Action):** Escolheste D ("se Built-in validations estiver ativo, o `Form.Valid` é verificado automaticamente antes da Action"). **Correta: A** — as validações built-in correm antes da Client Action e atualizam `Input.Valid` e `Form.Valid`, **mas a Action executa na mesma!** Tens sempre de colocar um `If (Form.Valid)` **depois** da última validação customizada antes de gravar na BD.

---

### Tema E: UI Widgets — Dropdown, Button Group, Links/Buttons, List e Table (6 erros)

- **Exame 2, P11 (Dropdown `Options Text`):** Escolheste B (`GetColors.Color.Label`). **Correta: D (`Color.Label`)** — `Options Text` e `Options Value` referenciam diretamente o atributo do registo da `List` associada, sem o nome do Aggregate.
- **Exame 2, P12 e P42 (Links vs Buttons):** Em P42 escolheste B ("Buttons só podem chamar Screen Actions"). **Correta: C** — **Links e Buttons têm exatamente as mesmas opções de `On Click`**: navegar para um Screen, navegar para um External URL, ou disparar uma Screen/Client Action.
- **Exame 3, P16 (Dropdown vs Button Group — pergunta de "FALSE"):** Escolheste D. **Correta: C** — quem tem a propriedade **`Variable`** é o **`Button Group`** (o contentor); cada **`Button Group Item`** tem apenas a propriedade **`Value`**.
- **Exame 3, P49 (Table Sorting):** Escolheste B ("basta definir `Sort Attribute` e os dados refrescam sozinhos"). **Correta: C** — clicar num cabeçalho dispara o evento **`On Sort`**, que recebe um Input Parameter (`SortBy`) com a coluna clicada; no handler tens de atualizar a variável de ordenação e fazer **Refresh Data** ao Aggregate.
- **Exame 4, P30 (List Widget):** Escolheste D ("A Entity deve ser posta na propriedade Source"). **Correta: A** — a `Source` de uma List tem de ser uma **List** (ex: `GetEntities.List`), nunca a Entity diretamente. Dentro da List, uma `Expression` pode combinar vários atributos do registo atual (e `List Item` não é obrigatório).

---

### Tema F: Lógica, Variáveis, Switch, For Each e Exception Handling (5 erros)

- **Exame 1, P33 (`Switch`):** Escolheste C. **Correta: D** — o `Switch` avalia os ramos **pela ordem em que estão definidos** e executa **apenas o primeiro** cuja condição seja `True`. Cuidado com condições sobrepostas nos exames (ex: `N > 100` antes de `N > 1000` apanha o `2000` no primeiro ramo!).
- **Exame 1, P34 (`For Each`):** Escolheste D ("definir loops genéricos"). **Correta: B** — em OutSystems, o `For Each` serve especificamente para **iterar sobre uma variável do tipo List**. (Loops genéricos fazem-se com um `If` + `Assign` contador).
- **Exame 1, P35 (Propagação de Exceções):** `Save` (Client) chama `Employee_Create` (Server), que chama `CreateEmployee` e tem um handler `AllExceptions`. Escolheste A (`DatabaseException` na `Save`). **Correta: C (`AllExceptions` na `Employee_Create`)** — uma exceção é sempre apanhada no **primeiro handler compatível dentro da própria Action** onde ocorreu (ou na mais próxima na call stack). Como `Employee_Create` tem `AllExceptions`, a exceção morre lá e nunca sobe para a `Save`!
- **Exame 2, P46 (Variáveis em Actions):** Escolheste A ("sem Local Variables"). **Correta: C** — tanto **Client Actions** como **Server Actions** podem ter **Input Parameters, Output Parameters e Local Variables**. *(Quem NÃO tem Output Parameters são Screens e Blocks!)*
- **Exame 2, P50 (Fluxos de Exception Handler):** Escolheste B ("obrigatório ter pelo menos um"). **Correta: C** — Exception Handlers são **opcionais**, podem existir vários na mesma Action, e **o seu fluxo nunca pode cruzar/intersetar** o fluxo principal nem outros fluxos de exceção.

---

### Tema G: Segurança e Roles (3 erros)

- **Exame 1, P41 (`CheckRegisteredRole`):** Escolheste C ("usar para esconder um widget no Screen"). **Correta: B** — pode ser usado num **Screen Data Action flow**. *(Regra de ouro: `Check<Role>Role` é uma Server Action — não pode ser usada diretamente numa expressão/propriedade `Visible` do Screen nem numa Client Action sem passar por JS/Data Action. Em Reactive, para UI usa-se um Data Action ou `$public.Security.checkIfCurrentUserHasRole` em JS, e validação real faz-se sempre no Server!)*
- **Exame 3, P23 (Restringir acesso a Screens):** Escolheste A ("na app Users"). **Correta: B** — a restrição de acesso a Screens faz-se **nas propriedades do Screen no Service Studio** (marcando/desmarcando as Roles). A app *Users* serve para gerir utilizadores, grupos e atribuir roles a utilizadores.
- **Exame 3, P24 (Built-in Role Actions — pergunta de "FALSE"):** Escolheste C. **Correta: D** — cada Role gera exatamente **3 ações built-in**: `Check<Role>Role`, `Grant<Role>Role` e `Revoke<Role>Role`. `CreateUserWithRole` não existe!

---

### Tema H: Data Modeling, Bootstrap e Arquitetura Reactive (3 erros)

- **Exame 2, P26 (Arquitetura Reactive Web — pergunta de "FALSE"):** Escolheste C. **Correta: B** — Reactive Web Apps geram **Single-Page Applications (SPA)** e os pedidos de dados são **assíncronos** (em paralelo). Logo, dizer que são síncronos é **falso**.
- **Exame 3, P10 (Relação 1-para-1):** Escolheste C ("adicionar um novo atributo de referência"). **Correta: A** — numa relação **1-para-1** (extensão), muda-se o tipo de dados do **próprio `Id` da Entidade B** para `Entity A Identifier` (PK = FK). Adicionar um novo atributo separado cria uma relação **1-para-N**!
- **Exame 4, P4 (Bootstrap de Excel):** Escolheste A. **Correta: B** — `Email` e `Phone Number` são armazenados como texto na base de dados; o Bootstrap mapeia por **nome exato da coluna** (colunas sem correspondência exata como `PhoneNumber` vs `Phone` são ignoradas), popula todas as colunas correspondentes, e o `Id` Auto-Number é gerado automaticamente.

---

## 4. Folha de Revisão Rápida (Cheat Sheet para Amanhã)

### 1. Data Modeling
- **Entities → Database Tables**, **Attributes → Columns**.
- **1-para-N:** Atributo de referência (FK) na entidade do lado **N** (ex: `Contact` tem `GroupId`).
- **1-para-1:** O **`Id` (PK)** da Entidade B tem data type `Entity A Identifier`.
- **N-para-N:** Entidade intermédia (Junction Entity) com 2 atributos de referência (`EntityAId`, `EntityBId`).
- **Static Entities:** Registos definidos em *design time*; **só têm ação `Get<StaticEntity>`** (não têm Create/Update/Delete em runtime); só podem ter atributos de referência para **outras Static Entities**; novos atributos obrigatórios têm de ter valor em design time.
- **`CreateOrUpdate<Entity>`:** Se `Id = NullIdentifier()`, cria registo; caso contrário atualiza. Devolve sempre o **Id** do registo.

### 2. Aggregates & Joins
- **Join automático ao arrastar Entity:**
  - FK **obrigatória** (`Is Mandatory = Yes`) → **Only With** (Inner Join)
  - FK **não obrigatória** (`Is Mandatory = No`) → **With or Without** (Left Join)
- **Contar tudo incluindo zeros** (ex: todos os Movies mesmo com 0 comentários): Join **`With or Without`** + `Group By` no `Movie.Id` + `Count` no `Comment.Id`.
- **Group By / Aggregations:** O output devolve **apenas** as colunas agrupadas e agregadas.
- **Calculated Attributes:** Devolvem as colunas das Entities **+ o atributo calculado**.
- **Filters:** Múltiplos filtros são ligados com **`AND`**. Pesquisa parcial: `Attribute like "%texto%"`.
- **Sorting:** Vários critérios aplicam-se por ordem (o 2.º desempata empates do 1.º).
- **Hidden Columns:** Só escondem na preview do Service Studio; continuam no output.

### 3. Screen Data Fetching & Lifecycle
- **O que corre num Screen:** **Screen Aggregates** (só BD) e **Data Actions** (REST, SQL avançado, lógica server, múltiplos outputs). **SQL Queries diretas no Screen NÃO existem** (só dentro de Data Actions / Server Actions).
- **Execução por defeito:** `At Start`, **assíncronos e em paralelo** (sem ordem garantida).
- **Dependent dropdowns (ex: País → Cidade):** `GetCities` com `Fetch = Only on demand`, e chamar `Refresh Data` no `OnChange` do País.
- **`On After Fetch`:** Dispara quando um Aggregate ou Data Action termina de ir buscar dados.
- **Ordem do Lifecycle:** `On Initialize` → `On Ready` → `On Render` *(repete quando dados mudam)* → `On Destroy`. *(Em Blocks também existe `On Parameters Changed` quando o pai altera um Input Parameter.)*

### 4. Blocks & Events
- Alterar um Block atualiza **todas** as instâncias existentes.
- Blocks têm **Input Parameters, Local Variables, Client Actions, Aggregates, Data Actions, Placeholders e Events** — **NUNCA Output Parameters**.
- **Pai → Filho:** Input Parameters (dispara `On Parameters Changed`).
- **Filho → Pai:** **Event** definido no Block (com Input Parameters se quiser enviar dados) + **Handler** definido no Pai.
- Handler só é **obrigatório** quando `Event.Is Mandatory = Yes`.

### 5. UI, Forms & Validations
- **List Widget:** `Source` tem de ser uma **List** (nunca uma Entity).
- **Pagination Widget:** `MaxRecords` = número de elementos por página.
- **Button Group:** `Variable` está no **Button Group**; `Value` está em cada **Button Group Item**.
- **Dropdown:** `List` = lista de dados; `Options Value` e `Options Text` são atributos relativos à lista (sem nome do Aggregate); `Variable` tem o mesmo tipo do `Options Value`.
- **Links & Buttons:** Mesmas opções de `On Click` (Screen, Screen Action, External URL; nunca Block).
- **Expressions:** Podem usar texto, contas, atributos, Client Functions — **NUNCA Server Actions diretamente**.
- **Form Validation:**
  1. Built-in validations correm antes da Action (verificam mandatory e data types).
  2. Pôr qualquer `Input.Valid = False` torna `Form.Valid = False` automaticamente.
  3. Verificar `If (Form.Valid)` **depois** da última validação customizada antes de chamar o Server.

### 6. Logic, Exceptions, Security & Dependencies
- **Variables:** Client/Server Actions têm Input, Output e Local. Screens/Blocks só Input e Local.
- **Site Properties:** Guardam configurações globais no servidor; alteráveis no Service Center; **não podem ser Record/List** (só tipos básicos / Entity Identifiers).
- **Switch:** Executa apenas o **1.º ramo verdadeiro** (ordem importa!).
- **Exception Handling:** Apanhada pelo handler mais específico na **própria Action**; se não existir, sobe para o caller. Fluxos de exceção nunca se cruzam com outros fluxos.
- **Roles:** Acesso a Screens configurado nas **Properties do Screen**. `Anonymous` = todos (autenticados ou não). `Registered` = qualquer autenticado. 3 ações built-in: `Check`, `Grant`, `Revoke`.
- **Manage Dependencies:** Ícone de refresh azul = elemento referenciado mudou no producer.
- **Debugger:** `Continue (F9)` corre até ao próximo breakpoint ou até ao fim da Action. Num breakpoint no `Start`, ainda não vês outputs de Actions que ainda não executaram.

Boa sorte para o exame amanhã! 🚀
