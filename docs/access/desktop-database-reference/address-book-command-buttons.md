---
title: Кнопки адресной книги
TOCTitle: Address Book command buttons
ms:assetid: bcea6f53-3e36-b067-03c2-b157ed02d41d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249908(v=office.15)
ms:contentKeyID: 48547422
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 09f2513a3c541c76352e773f7f2a8f0c24f78850
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282480"
---
# <a name="address-book-command-buttons"></a><span data-ttu-id="6803d-102">Кнопки адресной книги</span><span class="sxs-lookup"><span data-stu-id="6803d-102">Address Book command buttons</span></span>


<span data-ttu-id="6803d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6803d-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="6803d-104">Приложение адресной книги содержит следующие командные кнопки:</span><span class="sxs-lookup"><span data-stu-id="6803d-104">The Address Book application includes the following command buttons:</span></span>

- <span data-ttu-id="6803d-105">Кнопка " **найти** " для отправки запроса в базу данных.</span><span class="sxs-lookup"><span data-stu-id="6803d-105">A **Find** button to submit a query to the database.</span></span>

- <span data-ttu-id="6803d-106">Кнопка **clear** , позволяющая очистить текстовые поля перед началом нового поиска.</span><span class="sxs-lookup"><span data-stu-id="6803d-106">A **Clear** button to clear the text boxes before starting a new search.</span></span>

- <span data-ttu-id="6803d-107">Кнопка **обновления профиля** для сохранения изменений в записи сотрудника.</span><span class="sxs-lookup"><span data-stu-id="6803d-107">An **Update Profile** button to save changes to an employee record.</span></span>

- <span data-ttu-id="6803d-108">Кнопка **отменить изменения** , чтобы отменить изменения.</span><span class="sxs-lookup"><span data-stu-id="6803d-108">A **Cancel Changes** button to discard changes.</span></span>

## <a name="find-button"></a><span data-ttu-id="6803d-109">Кнопка "найти"</span><span class="sxs-lookup"><span data-stu-id="6803d-109">Find Button</span></span>

<span data-ttu-id="6803d-110">При нажатии кнопки **найти** активируется процедура поиска\_OnClick для VBScript, которая создает и отправляет запрос SQL.</span><span class="sxs-lookup"><span data-stu-id="6803d-110">Clicking the **Find** button activates the VBScript Find\_OnClick Sub procedure, which builds and sends the SQL query.</span></span> <span data-ttu-id="6803d-111">Нажатие этой кнопки заполняет сетку данных.</span><span class="sxs-lookup"><span data-stu-id="6803d-111">Clicking this button populates the data grid.</span></span>

## <a name="building-the-sql-query"></a><span data-ttu-id="6803d-112">Создание SQL запроса</span><span class="sxs-lookup"><span data-stu-id="6803d-112">Building the SQL Query</span></span>

<span data-ttu-id="6803d-113">В первой части процедуры поиска\_OnClick подписывается запрос SQL, по одной фразе с добавлением текстовых строк в глобальную инструкцию SQL SELECT.</span><span class="sxs-lookup"><span data-stu-id="6803d-113">The first part of the Find\_OnClick Sub procedure builds the SQL query, one phrase at a time, by appending text strings to a global SQL SELECT statement.</span></span> <span data-ttu-id="6803d-114">Она начинается с присвоения переменной инструкции SQL SELECT, которая запрашивает все строки данных из таблицы источника данных.</span><span class="sxs-lookup"><span data-stu-id="6803d-114">It begins by setting the variable to a SQL SELECT statement that requests all rows of data from the data source table.</span></span> <span data-ttu-id="6803d-115">Затем процедура Sub проверяет каждое из четырех полей ввода на странице.</span><span class="sxs-lookup"><span data-stu-id="6803d-115">Next, the Sub procedure scans each of the four input boxes on the page.</span></span>

<span data-ttu-id="6803d-116">Так как программа использует Word при создании инструкций SQL, запросы представляют собой поиск подстрок, а не точные совпадения.</span><span class="sxs-lookup"><span data-stu-id="6803d-116">Because the program uses the word in building the SQL statements, the queries are substring searches rather than exact matches.</span></span>

<span data-ttu-id="6803d-117">Например, если поле **Last Name** содержит запись "Берже", а поле **Title** содержит запись "Диспетчер программ", инструкция SQL (значение) будет считаться следующим:</span><span class="sxs-lookup"><span data-stu-id="6803d-117">For example, if the **Last Name** box contained the entry "Berge" and the **Title** box contained the entry "Program Manager", the SQL statement (value of ) would read:</span></span>

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

<span data-ttu-id="6803d-118">Если запрос выполнен успешно, все лица с последним именем "Берже" (например, Берже и Бержер) и с заголовком, содержащим слова "Диспетчер программ" (например, диспетчер программ, дополнительные технологии), отображаются в сетке данных HTML.</span><span class="sxs-lookup"><span data-stu-id="6803d-118">If the query was successful, all persons with a last name containing the text "Berge" (such as Berge and Berger) and with a title containing the words "Program Manager" (for example, Program Manager, Advanced Technologies) are displayed in the HTML data grid.</span></span>

## <a name="preparing-and-sending-the-query"></a><span data-ttu-id="6803d-119">Подготовка и отправка запроса</span><span class="sxs-lookup"><span data-stu-id="6803d-119">Preparing and Sending the Query</span></span>

<span data-ttu-id="6803d-120">Последняя часть процедуры поиска\_OnClick состоит из двух операторов.</span><span class="sxs-lookup"><span data-stu-id="6803d-120">The last part of the Find\_OnClick Sub procedure consists of two statements.</span></span> <span data-ttu-id="6803d-121">Первый оператор присваивает свойство SQL объекта RDS. Объект управления объектом, равный динамически созданному SQL запросу.</span><span class="sxs-lookup"><span data-stu-id="6803d-121">The first statement assigns the SQL property of the RDS.DataControl object equal to the dynamically built SQL query.</span></span> <span data-ttu-id="6803d-122">Второй оператор вызывает \*\*RDS. \*\*Объект DataObject () для запроса к базе данных и отображения новых результатов запроса в сетке.</span><span class="sxs-lookup"><span data-stu-id="6803d-122">The second statement causes the **RDS.DataControl** object () to query the database, and then display the new results of the query in the grid.</span></span>

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a><span data-ttu-id="6803d-123">Кнопка "Обновить профиль"</span><span class="sxs-lookup"><span data-stu-id="6803d-123">Update Profile Button</span></span>

<span data-ttu-id="6803d-124">При нажатии кнопки **Обновить профиль** активируется процедура OnClick обновления\_VBScript, в которой выполняется RDS. Методы SubmitChanges и Refresh объекта DataObject ().</span><span class="sxs-lookup"><span data-stu-id="6803d-124">Clicking the **Update Profile** button activates the VBScript Update\_OnClick Sub procedure, which executes the RDS.DataControl object's () SubmitChanges and Refresh methods.</span></span>

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

<span data-ttu-id="6803d-125">Когда DC1. SubmitChanges выполняет, удаленная служба данных упаковывает все сведения об обновлении и отправляет их на сервер через HTTP.</span><span class="sxs-lookup"><span data-stu-id="6803d-125">When DC1.SubmitChanges executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</span></span> <span data-ttu-id="6803d-126">Обновление все-или-нет; Если часть обновления завершается неудачно, никакие изменения не вносятся и возвращается сообщение о состоянии.</span><span class="sxs-lookup"><span data-stu-id="6803d-126">The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</span></span> <span data-ttu-id="6803d-127">выполняется, удаленная служба данных упаковывает все сведения об обновлении и отправляет их на сервер через HTTP.</span><span class="sxs-lookup"><span data-stu-id="6803d-127">executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</span></span> <span data-ttu-id="6803d-128">Обновление все-или-нет; Если часть обновления завершается неудачно, никакие изменения не вносятся и возвращается сообщение о состоянии.</span><span class="sxs-lookup"><span data-stu-id="6803d-128">The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</span></span> <span data-ttu-id="6803d-129">DC1. Обновление не требуется после **SubmitChanges** с удаленной службой данных, но гарантирует актуальность данных.</span><span class="sxs-lookup"><span data-stu-id="6803d-129">DC1.Refresh isn't necessary after **SubmitChanges** with Remote Data Service, but it ensures fresh data.</span></span>

## <a name="cancel-changes-button"></a><span data-ttu-id="6803d-130">Кнопка отмены изменений</span><span class="sxs-lookup"><span data-stu-id="6803d-130">Cancel Changes Button</span></span>

<span data-ttu-id="6803d-131">При нажатии кнопки **Отмена изменений** активируется\_процедура отмены OnClick для VBScript, в которой выполняется RDS. Метод CancelUpdate объекта DataObject.</span><span class="sxs-lookup"><span data-stu-id="6803d-131">Clicking **Cancel Changes** activates the VBScript Cancel\_OnClick Sub procedure, which executes the RDS.DataControl object's ( CancelUpdate method.</span></span>

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

<span data-ttu-id="6803d-132">При выполнении он отменяет любые изменения, внесенные пользователем в запись сотрудника в сетке данных с момента последнего запроса или обновления.</span><span class="sxs-lookup"><span data-stu-id="6803d-132">When executes, it discards any edits that a user has made to an employee record on the data grid since the last query or update.</span></span> <span data-ttu-id="6803d-133">Он восстанавливает исходные значения.</span><span class="sxs-lookup"><span data-stu-id="6803d-133">It restores the original values.</span></span>

