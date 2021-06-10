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
# <a name="address-book-command-buttons"></a><span data-ttu-id="85982-102">Кнопки адресной книги</span><span class="sxs-lookup"><span data-stu-id="85982-102">Address Book command buttons</span></span>


<span data-ttu-id="85982-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="85982-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="85982-104">Приложение Адресная книга содержит следующие кнопки команд:</span><span class="sxs-lookup"><span data-stu-id="85982-104">The Address Book application includes the following command buttons:</span></span>

- <span data-ttu-id="85982-105">Кнопка **Найти** для отправки запроса в базу данных.</span><span class="sxs-lookup"><span data-stu-id="85982-105">A **Find** button to submit a query to the database.</span></span>

- <span data-ttu-id="85982-106">Кнопка **Clear** для очистки текстовых полей перед началом нового поиска.</span><span class="sxs-lookup"><span data-stu-id="85982-106">A **Clear** button to clear the text boxes before starting a new search.</span></span>

- <span data-ttu-id="85982-107">Кнопка **Update Profile** для сохранения изменений в записи сотрудников.</span><span class="sxs-lookup"><span data-stu-id="85982-107">An **Update Profile** button to save changes to an employee record.</span></span>

- <span data-ttu-id="85982-108">Кнопка **Отмена изменений,** чтобы отменить изменения.</span><span class="sxs-lookup"><span data-stu-id="85982-108">A **Cancel Changes** button to discard changes.</span></span>

## <a name="find-button"></a><span data-ttu-id="85982-109">Найдите кнопку</span><span class="sxs-lookup"><span data-stu-id="85982-109">Find Button</span></span>

<span data-ttu-id="85982-110">Нажав **кнопку Найти,** активирует процедуру VBScript Find OnClick Sub, которая создает и отправляет \_ SQL запрос.</span><span class="sxs-lookup"><span data-stu-id="85982-110">Clicking the **Find** button activates the VBScript Find\_OnClick Sub procedure, which builds and sends the SQL query.</span></span> <span data-ttu-id="85982-111">Нажатие этой кнопки заполняет сетку данных.</span><span class="sxs-lookup"><span data-stu-id="85982-111">Clicking this button populates the data grid.</span></span>

## <a name="building-the-sql-query"></a><span data-ttu-id="85982-112">Создание SQL запроса</span><span class="sxs-lookup"><span data-stu-id="85982-112">Building the SQL Query</span></span>

<span data-ttu-id="85982-113">В первой части процедуры Найти onClick Sub создается запрос SQL, одна фраза за раз, путем примещения текстовых строк к общему заявлению \_ SQL SELECT.</span><span class="sxs-lookup"><span data-stu-id="85982-113">The first part of the Find\_OnClick Sub procedure builds the SQL query, one phrase at a time, by appending text strings to a global SQL SELECT statement.</span></span> <span data-ttu-id="85982-114">Она начинается с настройки переменной в SQL SELECT, запрашивает все строки данных из таблицы источников данных.</span><span class="sxs-lookup"><span data-stu-id="85982-114">It begins by setting the variable to a SQL SELECT statement that requests all rows of data from the data source table.</span></span> <span data-ttu-id="85982-115">Далее процедура Sub сканирует каждый из четырех входных полей на странице.</span><span class="sxs-lookup"><span data-stu-id="85982-115">Next, the Sub procedure scans each of the four input boxes on the page.</span></span>

<span data-ttu-id="85982-116">Так как программа использует слово при создании SQL, запросы являются подстройки поиска, а не точные совпадения.</span><span class="sxs-lookup"><span data-stu-id="85982-116">Because the program uses the word in building the SQL statements, the queries are substring searches rather than exact matches.</span></span>

<span data-ttu-id="85982-117">Например, если  в поле Фамилия содержится запись "Berge", а в поле **Title** содержится запись "Менеджер программы", в SQL (значение ) будет прочитано:</span><span class="sxs-lookup"><span data-stu-id="85982-117">For example, if the **Last Name** box contained the entry "Berge" and the **Title** box contained the entry "Program Manager", the SQL statement (value of ) would read:</span></span>

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

<span data-ttu-id="85982-118">Если запрос был успешным, все лица с фамилией, содержащей текст "Berge" (например, Berge и Berger) и с заголовком, содержащим слова "Менеджер программы" (например, Менеджер программы, Расширенные технологии) отображаются в htmL-сетке данных.</span><span class="sxs-lookup"><span data-stu-id="85982-118">If the query was successful, all persons with a last name containing the text "Berge" (such as Berge and Berger) and with a title containing the words "Program Manager" (for example, Program Manager, Advanced Technologies) are displayed in the HTML data grid.</span></span>

## <a name="preparing-and-sending-the-query"></a><span data-ttu-id="85982-119">Подготовка и отправка запроса</span><span class="sxs-lookup"><span data-stu-id="85982-119">Preparing and Sending the Query</span></span>

<span data-ttu-id="85982-120">Последняя часть процедуры Find \_ OnClick Sub состоит из двух заявлений.</span><span class="sxs-lookup"><span data-stu-id="85982-120">The last part of the Find\_OnClick Sub procedure consists of two statements.</span></span> <span data-ttu-id="85982-121">Первое утверждение назначает SQL свойства RDS. Объект DataControl равен динамически построенной SQL запросу.</span><span class="sxs-lookup"><span data-stu-id="85982-121">The first statement assigns the SQL property of the RDS.DataControl object equal to the dynamically built SQL query.</span></span> <span data-ttu-id="85982-122">Второе утверждение вызывает **RDS. Объект DataControl** () для запроса базы данных и отображения новых результатов запроса в сетке.</span><span class="sxs-lookup"><span data-stu-id="85982-122">The second statement causes the **RDS.DataControl** object () to query the database, and then display the new results of the query in the grid.</span></span>

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a><span data-ttu-id="85982-123">Кнопка обновления профиля</span><span class="sxs-lookup"><span data-stu-id="85982-123">Update Profile Button</span></span>

<span data-ttu-id="85982-124">Нажав **кнопку "Профиль** обновления", активирует процедуру обновления VBScript OnClick Sub, которая выполняет \_ RDS. Методы отправки и обновления объекта DataControl.</span><span class="sxs-lookup"><span data-stu-id="85982-124">Clicking the **Update Profile** button activates the VBScript Update\_OnClick Sub procedure, which executes the RDS.DataControl object's () SubmitChanges and Refresh methods.</span></span>

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

<span data-ttu-id="85982-125">Когда DC1. SubmitChanges выполняется, служба удаленных данных упаковывает всю информацию об обновлении и отправляет ее на сервер через HTTP.</span><span class="sxs-lookup"><span data-stu-id="85982-125">When DC1.SubmitChanges executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</span></span> <span data-ttu-id="85982-126">Обновление является все или ничего; если часть обновления не выполнена, ни одно из изменений не выполнено, и сообщение о состоянии возвращается.</span><span class="sxs-lookup"><span data-stu-id="85982-126">The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</span></span> <span data-ttu-id="85982-127">выполняется, служба удаленных данных упаковывает всю информацию об обновлении и отправляет ее на сервер через HTTP.</span><span class="sxs-lookup"><span data-stu-id="85982-127">executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</span></span> <span data-ttu-id="85982-128">Обновление является все или ничего; если часть обновления не выполнена, ни одно из изменений не выполнено, и сообщение о состоянии возвращается.</span><span class="sxs-lookup"><span data-stu-id="85982-128">The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</span></span> <span data-ttu-id="85982-129">DC1. Обновление не требуется после **SubmitChanges** с удаленной службой данных, но оно обеспечивает свежие данные.</span><span class="sxs-lookup"><span data-stu-id="85982-129">DC1.Refresh isn't necessary after **SubmitChanges** with Remote Data Service, but it ensures fresh data.</span></span>

## <a name="cancel-changes-button"></a><span data-ttu-id="85982-130">Кнопка Отмена изменений</span><span class="sxs-lookup"><span data-stu-id="85982-130">Cancel Changes Button</span></span>

<span data-ttu-id="85982-131">**Щелкнув кнопку Отмена** изменений, активирует процедуру отмены onClick Sub VBScript, которая \_ выполняет RDS. Объект DataControl (Метод CancelUpdate.</span><span class="sxs-lookup"><span data-stu-id="85982-131">Clicking **Cancel Changes** activates the VBScript Cancel\_OnClick Sub procedure, which executes the RDS.DataControl object's ( CancelUpdate method.</span></span>

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

<span data-ttu-id="85982-132">При выполнении он удаляет все изменения, которые пользователь внес в запись сотрудника в сетке данных после последнего запроса или обновления.</span><span class="sxs-lookup"><span data-stu-id="85982-132">When executes, it discards any edits that a user has made to an employee record on the data grid since the last query or update.</span></span> <span data-ttu-id="85982-133">Восстанавливает исходные значения.</span><span class="sxs-lookup"><span data-stu-id="85982-133">It restores the original values.</span></span>

