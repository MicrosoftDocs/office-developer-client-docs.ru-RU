---
title: Адресной книги кнопок команд
TOCTitle: Address Book command buttons
ms:assetid: bcea6f53-3e36-b067-03c2-b157ed02d41d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249908(v=office.15)
ms:contentKeyID: 48547422
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f586b92f309ffd330230bf732d0e477acf0a8ba9
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946932"
---
# <a name="address-book-command-buttons"></a><span data-ttu-id="5a3ab-102">Адресной книги кнопок команд</span><span class="sxs-lookup"><span data-stu-id="5a3ab-102">Address Book command buttons</span></span>


<span data-ttu-id="5a3ab-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5a3ab-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="5a3ab-104">Адресная книга приложения включает в себя следующие командные кнопки:</span><span class="sxs-lookup"><span data-stu-id="5a3ab-104">The Address Book application includes the following command buttons:</span></span>

- <span data-ttu-id="5a3ab-105">**Найдите** кнопку для отправки запросов к базе данных.</span><span class="sxs-lookup"><span data-stu-id="5a3ab-105">A **Find** button to submit a query to the database.</span></span>

- <span data-ttu-id="5a3ab-106">**Снимите флажок** , чтобы снимите текстовых полей, чтобы приступить к работе новый поиск.</span><span class="sxs-lookup"><span data-stu-id="5a3ab-106">A **Clear** button to clear the text boxes before starting a new search.</span></span>

- <span data-ttu-id="5a3ab-107">Кнопка **Обновить профиль** для сохранения изменений в запись сотрудника.</span><span class="sxs-lookup"><span data-stu-id="5a3ab-107">An **Update Profile** button to save changes to an employee record.</span></span>

- <span data-ttu-id="5a3ab-108">**Отмена изменений** , чтобы отменить изменения.</span><span class="sxs-lookup"><span data-stu-id="5a3ab-108">A **Cancel Changes** button to discard changes.</span></span>

## <a name="find-button"></a><span data-ttu-id="5a3ab-109">Найдите кнопку</span><span class="sxs-lookup"><span data-stu-id="5a3ab-109">Find Button</span></span>

<span data-ttu-id="5a3ab-110">Нажмите кнопку **Найти** активирует поиска VBScript\_процедуры OnClick Sub, которая создает и отправляет запрос SQL.</span><span class="sxs-lookup"><span data-stu-id="5a3ab-110">Clicking the **Find** button activates the VBScript Find\_OnClick Sub procedure, which builds and sends the SQL query.</span></span> <span data-ttu-id="5a3ab-111">При нажатии этой кнопки заполняет таблицу данных.</span><span class="sxs-lookup"><span data-stu-id="5a3ab-111">Clicking this button populates the data grid.</span></span>

## <a name="building-the-sql-query"></a><span data-ttu-id="5a3ab-112">Построение запросов SQL</span><span class="sxs-lookup"><span data-stu-id="5a3ab-112">Building the SQL Query</span></span>

<span data-ttu-id="5a3ab-113">Первая часть Find\_процедуры OnClick Sub создает запрос SQL, одной фразе одновременно, путем добавления строк текста для глобального инструкции SQL SELECT.</span><span class="sxs-lookup"><span data-stu-id="5a3ab-113">The first part of the Find\_OnClick Sub procedure builds the SQL query, one phrase at a time, by appending text strings to a global SQL SELECT statement.</span></span> <span data-ttu-id="5a3ab-114">Начинается путем установки переменной инструкции SQL SELECT, для которого запрашивается всех строк данных из таблицы источника данных.</span><span class="sxs-lookup"><span data-stu-id="5a3ab-114">It begins by setting the variable to a SQL SELECT statement that requests all rows of data from the data source table.</span></span> <span data-ttu-id="5a3ab-115">Далее процедуры Sub сканирование каждого из четырех поля ввода на странице.</span><span class="sxs-lookup"><span data-stu-id="5a3ab-115">Next, the Sub procedure scans each of the four input boxes on the page.</span></span>

<span data-ttu-id="5a3ab-116">Так как программа использует word в создание инструкций SQL, запросы, поиск подстрок, а не точного совпадения.</span><span class="sxs-lookup"><span data-stu-id="5a3ab-116">Because the program uses the word in building the SQL statements, the queries are substring searches rather than exact matches.</span></span>

<span data-ttu-id="5a3ab-117">К примеру Если поле **Last Name** содержится запись «Berge» и в поле **Название** содержится запись «Руководитель программы», будет чтение инструкции SQL (значение):</span><span class="sxs-lookup"><span data-stu-id="5a3ab-117">For example, if the **Last Name** box contained the entry "Berge" and the **Title** box contained the entry "Program Manager", the SQL statement (value of ) would read:</span></span>

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

<span data-ttu-id="5a3ab-118">Если запрос прошла успешно, все лиц с фамилией, содержащая текст «Berge» (например, Berge и Бергер) и с заголовком, содержащие слова «Руководитель программы» (например, руководитель программы, дополнительные технологиях) отображаются в сетке данных HTML.</span><span class="sxs-lookup"><span data-stu-id="5a3ab-118">If the query was successful, all persons with a last name containing the text "Berge" (such as Berge and Berger) and with a title containing the words "Program Manager" (for example, Program Manager, Advanced Technologies) are displayed in the HTML data grid.</span></span>

## <a name="preparing-and-sending-the-query"></a><span data-ttu-id="5a3ab-119">Подготовка и отправка запроса</span><span class="sxs-lookup"><span data-stu-id="5a3ab-119">Preparing and Sending the Query</span></span>

<span data-ttu-id="5a3ab-120">Последнюю часть Find\_процедуры OnClick Sub состоит из двух операторов.</span><span class="sxs-lookup"><span data-stu-id="5a3ab-120">The last part of the Find\_OnClick Sub procedure consists of two statements.</span></span> <span data-ttu-id="5a3ab-121">Первый оператор присваивает свойству SQL RDS. Объект DataControl равно динамически построенного запроса SQL.</span><span class="sxs-lookup"><span data-stu-id="5a3ab-121">The first statement assigns the SQL property of the RDS.DataControl object equal to the dynamically built SQL query.</span></span> <span data-ttu-id="5a3ab-122">Второй оператор вызывает **RDS. DataControl** объекта () в базе данных и отображения новой результаты запроса в сетке.</span><span class="sxs-lookup"><span data-stu-id="5a3ab-122">The second statement causes the **RDS.DataControl** object () to query the database, and then display the new results of the query in the grid.</span></span>

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a><span data-ttu-id="5a3ab-123">Обновление профиля кнопки</span><span class="sxs-lookup"><span data-stu-id="5a3ab-123">Update Profile Button</span></span>

<span data-ttu-id="5a3ab-124">Нажмите кнопку **Обновить профиль** активирует обновление VBScript\_процедуры OnClick Sub, которая выполняет RDS. Методы SubmitChanges и обновление () DataControl объекта.</span><span class="sxs-lookup"><span data-stu-id="5a3ab-124">Clicking the **Update Profile** button activates the VBScript Update\_OnClick Sub procedure, which executes the RDS.DataControl object's () SubmitChanges and Refresh methods.</span></span>

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

<span data-ttu-id="5a3ab-125">Когда DC1. Выполняет SubmitChanges, удаленной службы данных пакеты всех пакетов обновления и отправляет его на сервер по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="5a3ab-125">When DC1.SubmitChanges executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</span></span> <span data-ttu-id="5a3ab-126">Обновление отдельных; Если часть обновления завершается неудачно, изменения внесены и возвращается сообщение о состоянии.</span><span class="sxs-lookup"><span data-stu-id="5a3ab-126">The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</span></span> <span data-ttu-id="5a3ab-127">выполняет, удаленной службы данных пакеты всех пакетов обновления и отправляет его на сервер по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="5a3ab-127">executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</span></span> <span data-ttu-id="5a3ab-128">Обновление отдельных; Если часть обновления завершается неудачно, изменения внесены и возвращается сообщение о состоянии.</span><span class="sxs-lookup"><span data-stu-id="5a3ab-128">The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</span></span> <span data-ttu-id="5a3ab-129">DC1. Обновление не обязательно после **SubmitChanges** с удаленной службы данных, но обеспечивает новые данные.</span><span class="sxs-lookup"><span data-stu-id="5a3ab-129">DC1.Refresh isn't necessary after **SubmitChanges** with Remote Data Service, but it ensures fresh data.</span></span>

## <a name="cancel-changes-button"></a><span data-ttu-id="5a3ab-130">Кнопка "Отмена"</span><span class="sxs-lookup"><span data-stu-id="5a3ab-130">Cancel Changes Button</span></span>

<span data-ttu-id="5a3ab-131">Нажав кнопку **Отмена изменений** активирует Отмена VBScript\_процедуры OnClick Sub, которая выполняет RDS. DataControl объекта (метод CancelUpdate.</span><span class="sxs-lookup"><span data-stu-id="5a3ab-131">Clicking **Cancel Changes** activates the VBScript Cancel\_OnClick Sub procedure, which executes the RDS.DataControl object's ( CancelUpdate method.</span></span>

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

<span data-ttu-id="5a3ab-132">При выполнении отменяет все изменения, внесенные пользователем с записью сотрудника в таблице данных с момента последнего запроса или обновления.</span><span class="sxs-lookup"><span data-stu-id="5a3ab-132">When executes, it discards any edits that a user has made to an employee record on the data grid since the last query or update.</span></span> <span data-ttu-id="5a3ab-133">Он восстанавливает исходные значения.</span><span class="sxs-lookup"><span data-stu-id="5a3ab-133">It restores the original values.</span></span>

