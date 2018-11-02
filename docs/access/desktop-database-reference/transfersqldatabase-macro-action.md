---
title: Макрокоманда TransferSQLDatabase
TOCTitle: TransferSQLDatabase macro action
ms:assetid: 8cb95e22-f1f0-6c70-7dcb-3a3e9aafdc57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197344(v=office.15)
ms:contentKeyID: 48546244
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm111536
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ae05da3d07cc17f54584d11282721ac83f23ccd8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926544"
---
# <a name="transfersqldatabase-macro-action"></a><span data-ttu-id="78ff7-102">Макрокоманда TransferSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="78ff7-102">TransferSQLDatabase macro action</span></span>


<span data-ttu-id="78ff7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="78ff7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="78ff7-104">В проекте Microsoft Access **«ПереносБазыДанныхSQL»** можно использовать для передачи Microsoft SQL Server 7.0 или более поздняя версия базы данных на другой SQL Server 7.0 или более поздняя версия базы данных.</span><span class="sxs-lookup"><span data-stu-id="78ff7-104">In an Access project, you can use the **TransferSQLDatabase** action to transfer a Microsoft SQL Server 7.0 or later database to another SQL Server 7.0 or later database.</span></span> <span data-ttu-id="78ff7-105">Дополнительные сведения о переносе базы данных SQL Server см.</span><span class="sxs-lookup"><span data-stu-id="78ff7-105">For more information about transferring a database, see the SQL Server documentation.</span></span>


> [!NOTE]
> <span data-ttu-id="78ff7-p102">
		Эта действие не разрешено, если база данных не является доверенной. Дополнительные сведения о включении макросов см. по ссылкам в разделе See Also этой статьи.
</span><span class="sxs-lookup"><span data-stu-id="78ff7-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span>



## <a name="setting"></a><span data-ttu-id="78ff7-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="78ff7-108">Setting</span></span>

<span data-ttu-id="78ff7-109">**«ПереносБазыДанныхSQL»** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="78ff7-109">The **TransferSQLDatabase** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="78ff7-110">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="78ff7-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="78ff7-111">Описание</span><span class="sxs-lookup"><span data-stu-id="78ff7-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78ff7-112"><strong>Сервер</strong></span><span class="sxs-lookup"><span data-stu-id="78ff7-112"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="78ff7-113">Имя SQL Server 7.0 или более поздняя версия сервера базы данных выполняется копирование.</span><span class="sxs-lookup"><span data-stu-id="78ff7-113">The name of the SQL Server 7.0 or later database server you are copying to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78ff7-114"><strong>База данных</strong></span><span class="sxs-lookup"><span data-stu-id="78ff7-114"><strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="78ff7-115">Имя новой базы данных, которая будет создана на целевом сервере.</span><span class="sxs-lookup"><span data-stu-id="78ff7-115">The name of the new database that will be created on the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78ff7-116"><strong>Доверительное соединение</strong></span><span class="sxs-lookup"><span data-stu-id="78ff7-116"><strong>Use Trusted Connection</strong></span></span></p></td>
<td><p><span data-ttu-id="78ff7-117">Указывает ли представляет доверительное соединение к серверу SQL Server.</span><span class="sxs-lookup"><span data-stu-id="78ff7-117">Specifes whether or not there is a trusted connection to the SQL Server.</span></span> <span data-ttu-id="78ff7-118">Если задано значение <strong>Да</strong>, то есть доверительное соединение и параметры <strong>входа в систему</strong> и <strong>пароль</strong> не являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="78ff7-118">If set to <strong>Yes</strong>, then there is a trusted connection and the <strong>Login</strong> and <strong>Password</strong> arguments are not required.</span></span> <span data-ttu-id="78ff7-119">Если задано значение <strong>No</strong>, <strong>имя пользователя</strong> и <strong>пароль</strong> аргументов не требуется.</span><span class="sxs-lookup"><span data-stu-id="78ff7-119">If set to <strong>No</strong>, the <strong>Login</strong> and <strong>Password</strong> arguments are required.</span></span> <span data-ttu-id="78ff7-120">По умолчанию используется значение <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="78ff7-120">The default is <strong>Yes</strong>.</span></span> <span data-ttu-id="78ff7-121">При использовании доверительное соединение безопасности SQL Server интегрируется с безопасности операционной системы Windows для обеспечения единого входа сеть и базы данных.</span><span class="sxs-lookup"><span data-stu-id="78ff7-121">When you use a trusted connection, SQL Server security integrates with the Windows operating system security to provide a single log on to the network and the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78ff7-122"><strong>Учетные данные</strong></span><span class="sxs-lookup"><span data-stu-id="78ff7-122"><strong>Login</strong></span></span></p></td>
<td><p><span data-ttu-id="78ff7-123">Имя для входа на целевой сервер.</span><span class="sxs-lookup"><span data-stu-id="78ff7-123">The name of the Login to the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78ff7-124"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="78ff7-124"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="78ff7-125">Пароль для <strong>входа</strong> на конечный сервер.</span><span class="sxs-lookup"><span data-stu-id="78ff7-125">The password for the <strong>Login</strong> argument.</span></span> <span data-ttu-id="78ff7-126">Этот пароль хранится в виде текста в проект Microsoft Access, но скрыт во время операции переноса базы данных.</span><span class="sxs-lookup"><span data-stu-id="78ff7-126">This password is stored as text in the Access project, but is hidden during the transfer database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78ff7-127"><strong>Копирование данных</strong></span><span class="sxs-lookup"><span data-stu-id="78ff7-127"><strong>Transfer Copy Data</strong></span></span></p></td>
<td><p><span data-ttu-id="78ff7-128">Указывает, следует ли включать данные в операции переноса базы данных.</span><span class="sxs-lookup"><span data-stu-id="78ff7-128">Specifies whether or not to include data in the transfer database operation.</span></span> <span data-ttu-id="78ff7-129">Если установлено значение " <strong>Да"</strong>, все данные для всех таблиц, а также все структуры данных, расширенные свойства и объекты базы данных.</span><span class="sxs-lookup"><span data-stu-id="78ff7-129">When set to <strong>Yes</strong>, all data is included for all the tables, along with all data structures, extended properties, and database objects.</span></span> <span data-ttu-id="78ff7-130">Если задано значение <strong>No</strong>, данные не включен из таблиц.</span><span class="sxs-lookup"><span data-stu-id="78ff7-130">When set to <strong>No</strong>, no data is included from the tables.</span></span> <span data-ttu-id="78ff7-131">Структура таблицы и расширенные свойства создаются на целевом сервере, а также все объекты базы данных (за исключением схемы базы данных).</span><span class="sxs-lookup"><span data-stu-id="78ff7-131">Only the table structure and extended properties are created on the destination server, along with all other database objects (except database diagrams).</span></span> <span data-ttu-id="78ff7-132">По умолчанию используется значение <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="78ff7-132">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="78ff7-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="78ff7-133">Remarks</span></span>

<span data-ttu-id="78ff7-134">Нельзя выполнять другие операции во время передачи базы данных.</span><span class="sxs-lookup"><span data-stu-id="78ff7-134">You cannot perform other operations while the database is being transferred.</span></span>

<span data-ttu-id="78ff7-135">**«ПереносБазыДанныхSQL»,** по умолчанию, копирование данных, определений данных, объектов базы данных и расширенные свойства, такие как значения по умолчанию, текстовые ограничения и значений подстановки.</span><span class="sxs-lookup"><span data-stu-id="78ff7-135">The **TransferSQLDatabase** action, by default, copies data, data definitions, database objects, and extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="78ff7-136">Существует требования для переноса базы данных.</span><span class="sxs-lookup"><span data-stu-id="78ff7-136">There are requirements for transferring a database:</span></span>

  - <span data-ttu-id="78ff7-137">Необходимо быть членом роли sysadmin на конечном сервере (нет специальных роль необходима на исходном сервере).</span><span class="sxs-lookup"><span data-stu-id="78ff7-137">You must be a member of the sysadmin role on the destination server (No special role is required on the source server).</span></span>

<!-- end list -->

  - <span data-ttu-id="78ff7-138">Текущий сервер SQL, подключенный к проекту доступа и на целевой сервер, на которого переключается базы данных должен быть SQL Server версии 7.0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="78ff7-138">The current SQL server connected to the Access project and the destination server you are transferring the database to must be SQL Server version 7.0 or later.</span></span>


> [!NOTE]
> <P><span data-ttu-id="78ff7-139">Связанные серверы не переносятся во время операции переноса базы данных.</span><span class="sxs-lookup"><span data-stu-id="78ff7-139">Linked servers are not transferred during a database transfer operation.</span></span></P>



<span data-ttu-id="78ff7-140">Чтобы запустить **«ПереносБазыДанныхSQL»** в Visual Basic для приложений (VBA) модуль, используйте метод **TransferSQLDatabase** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="78ff7-140">To run the **TransferSQLDatabase** action in a Visual Basic for Applications (VBA) module, use the **TransferSQLDatabase** method of the **DoCmd** object.</span></span>

