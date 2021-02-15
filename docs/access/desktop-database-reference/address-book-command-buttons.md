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
# <a name="address-book-command-buttons"></a><span data-ttu-id="3acfe-102">Кнопки адресной книги</span><span class="sxs-lookup"><span data-stu-id="3acfe-102">Address Book command buttons</span></span>


<span data-ttu-id="3acfe-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3acfe-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="3acfe-104">Приложение адресной книги включает следующие кнопки команд:</span><span class="sxs-lookup"><span data-stu-id="3acfe-104">The Address Book application includes the following command buttons:</span></span>

- <span data-ttu-id="3acfe-105">**Кнопка** "Найти" для отправки запроса в базу данных.</span><span class="sxs-lookup"><span data-stu-id="3acfe-105">A **Find** button to submit a query to the database.</span></span>

- <span data-ttu-id="3acfe-106">Кнопка **"Очистить"** для очистки текстовых полей перед началом нового поиска.</span><span class="sxs-lookup"><span data-stu-id="3acfe-106">A **Clear** button to clear the text boxes before starting a new search.</span></span>

- <span data-ttu-id="3acfe-107">Кнопка **"Обновить профиль"** для сохранения изменений в записи сотрудника.</span><span class="sxs-lookup"><span data-stu-id="3acfe-107">An **Update Profile** button to save changes to an employee record.</span></span>

- <span data-ttu-id="3acfe-108">Кнопка **отмены изменений** для отмены изменений.</span><span class="sxs-lookup"><span data-stu-id="3acfe-108">A **Cancel Changes** button to discard changes.</span></span>

## <a name="find-button"></a><span data-ttu-id="3acfe-109">Кнопка "Найти"</span><span class="sxs-lookup"><span data-stu-id="3acfe-109">Find Button</span></span>

<span data-ttu-id="3acfe-110">**Нажатие** кнопки "Найти" активирует процедуру VBScript Find OnClick Sub, которая создает и отправляет SQL \_ запроса.</span><span class="sxs-lookup"><span data-stu-id="3acfe-110">Clicking the **Find** button activates the VBScript Find\_OnClick Sub procedure, which builds and sends the SQL query.</span></span> <span data-ttu-id="3acfe-111">Нажатие этой кнопки заполняет сетку данных.</span><span class="sxs-lookup"><span data-stu-id="3acfe-111">Clicking this button populates the data grid.</span></span>

## <a name="building-the-sql-query"></a><span data-ttu-id="3acfe-112">Создание SQL запроса</span><span class="sxs-lookup"><span data-stu-id="3acfe-112">Building the SQL Query</span></span>

<span data-ttu-id="3acfe-113">Первая часть процедуры Find OnClick Sub создает запрос SQL по одной фразе за раз, привнося текстовые строки в глобальный SQL \_ SELECT.</span><span class="sxs-lookup"><span data-stu-id="3acfe-113">The first part of the Find\_OnClick Sub procedure builds the SQL query, one phrase at a time, by appending text strings to a global SQL SELECT statement.</span></span> <span data-ttu-id="3acfe-114">Она начинается с установки переменной SQL SELECT, которая запрашивает все строки данных из таблицы источника данных.</span><span class="sxs-lookup"><span data-stu-id="3acfe-114">It begins by setting the variable to a SQL SELECT statement that requests all rows of data from the data source table.</span></span> <span data-ttu-id="3acfe-115">Затем процедура Sub сканирует каждое из четырех полей ввода на странице.</span><span class="sxs-lookup"><span data-stu-id="3acfe-115">Next, the Sub procedure scans each of the four input boxes on the page.</span></span>

<span data-ttu-id="3acfe-116">Поскольку программа использует слово при создании SQL, запросы — это поиск подстроки, а не точные совпадения.</span><span class="sxs-lookup"><span data-stu-id="3acfe-116">Because the program uses the word in building the SQL statements, the queries are substring searches rather than exact matches.</span></span>

<span data-ttu-id="3acfe-117">Например, если  поле "Фамилия" содержало запись "Berge", а поле "Заголовок" содержало запись "Program Manager", SQL (значение) будет читать: </span><span class="sxs-lookup"><span data-stu-id="3acfe-117">For example, if the **Last Name** box contained the entry "Berge" and the **Title** box contained the entry "Program Manager", the SQL statement (value of ) would read:</span></span>

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

<span data-ttu-id="3acfe-118">В случае успешного выполнения запроса все люди с фамилией, содержащей текст "Berge" (например, Berge и Berger) и заголовком, содержащим слова "Program Manager" (например, Program Manager, Advanced Technologies), отображаются в сетке данных HTML.</span><span class="sxs-lookup"><span data-stu-id="3acfe-118">If the query was successful, all persons with a last name containing the text "Berge" (such as Berge and Berger) and with a title containing the words "Program Manager" (for example, Program Manager, Advanced Technologies) are displayed in the HTML data grid.</span></span>

## <a name="preparing-and-sending-the-query"></a><span data-ttu-id="3acfe-119">Подготовка и отправка запроса</span><span class="sxs-lookup"><span data-stu-id="3acfe-119">Preparing and Sending the Query</span></span>

<span data-ttu-id="3acfe-120">Последняя часть процедуры Find \_ OnClick Sub состоит из двух заявлений.</span><span class="sxs-lookup"><span data-stu-id="3acfe-120">The last part of the Find\_OnClick Sub procedure consists of two statements.</span></span> <span data-ttu-id="3acfe-121">Первый выписка назначает SQL RDS. Объект DataControl, равный динамически SQL запросу.</span><span class="sxs-lookup"><span data-stu-id="3acfe-121">The first statement assigns the SQL property of the RDS.DataControl object equal to the dynamically built SQL query.</span></span> <span data-ttu-id="3acfe-122">Вторая выписка вызывает **RDS. Объект DataControl** () для запроса базы данных и отображения новых результатов запроса в сетке.</span><span class="sxs-lookup"><span data-stu-id="3acfe-122">The second statement causes the **RDS.DataControl** object () to query the database, and then display the new results of the query in the grid.</span></span>

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a><span data-ttu-id="3acfe-123">Кнопка обновления профиля</span><span class="sxs-lookup"><span data-stu-id="3acfe-123">Update Profile Button</span></span>

<span data-ttu-id="3acfe-124">Нажатие **кнопки "Обновить профиль"** активирует процедуру ВУП обновления VBScript OnClick, которая выполняет \_ RDS. Методы SubmitChanges и Refresh объекта DataControl.</span><span class="sxs-lookup"><span data-stu-id="3acfe-124">Clicking the **Update Profile** button activates the VBScript Update\_OnClick Sub procedure, which executes the RDS.DataControl object's () SubmitChanges and Refresh methods.</span></span>

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

<span data-ttu-id="3acfe-125">Когда DC1. SubmitChanges выполняется, удаленная служба данных упаковывает все сведения об обновлении и отправляет их на сервер по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="3acfe-125">When DC1.SubmitChanges executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</span></span> <span data-ttu-id="3acfe-126">Обновление является "все или ничего"; Если часть обновления не выполнена, никакие изменения не вносяся, и возвращается сообщение о состоянии.</span><span class="sxs-lookup"><span data-stu-id="3acfe-126">The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</span></span> <span data-ttu-id="3acfe-127">выполняется, удаленная служба данных упаковывает все сведения об обновлении и отправляет их на сервер по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="3acfe-127">executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</span></span> <span data-ttu-id="3acfe-128">Обновление является "все или ничего"; Если часть обновления не выполнена, никакие изменения не вносяся, и возвращается сообщение о состоянии.</span><span class="sxs-lookup"><span data-stu-id="3acfe-128">The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</span></span> <span data-ttu-id="3acfe-129">DC1. Обновление не требуется после **submitChanges** с удаленной службой данных, но обеспечивает новые данные.</span><span class="sxs-lookup"><span data-stu-id="3acfe-129">DC1.Refresh isn't necessary after **SubmitChanges** with Remote Data Service, but it ensures fresh data.</span></span>

## <a name="cancel-changes-button"></a><span data-ttu-id="3acfe-130">Кнопка отмены изменений</span><span class="sxs-lookup"><span data-stu-id="3acfe-130">Cancel Changes Button</span></span>

<span data-ttu-id="3acfe-131">**Нажатие кнопки "Отмена** изменений" активирует процедуру VBScript Cancel \_ OnClick Sub, которая выполняет RDS. Объект DataControl ( Метод CancelUpdate.</span><span class="sxs-lookup"><span data-stu-id="3acfe-131">Clicking **Cancel Changes** activates the VBScript Cancel\_OnClick Sub procedure, which executes the RDS.DataControl object's ( CancelUpdate method.</span></span>

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

<span data-ttu-id="3acfe-132">При выполнении он удаляет все изменения, которые пользователь внес в запись сотрудника в сетке данных с момента последнего запроса или обновления.</span><span class="sxs-lookup"><span data-stu-id="3acfe-132">When executes, it discards any edits that a user has made to an employee record on the data grid since the last query or update.</span></span> <span data-ttu-id="3acfe-133">Он восстанавливает исходные значения.</span><span class="sxs-lookup"><span data-stu-id="3acfe-133">It restores the original values.</span></span>

