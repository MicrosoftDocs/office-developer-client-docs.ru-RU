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
localization_priority: Normal
ms.openlocfilehash: 5ed20555726d0a6f63f0e48fb154cedb411ef8cd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711492"
---
# <a name="transfersqldatabase-macro-action"></a><span data-ttu-id="90f2c-102">Макрокоманда TransferSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="90f2c-102">TransferSQLDatabase macro action</span></span>

<span data-ttu-id="90f2c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="90f2c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="90f2c-104">В проекте Microsoft Access **«ПереносБазыДанныхSQL»** можно использовать для передачи Microsoft SQL Server 7.0 или более поздняя версия базы данных на другой SQL Server 7.0 или более поздняя версия базы данных.</span><span class="sxs-lookup"><span data-stu-id="90f2c-104">In an Access project, you can use the **TransferSQLDatabase** action to transfer a Microsoft SQL Server 7.0 or later database to another SQL Server 7.0 or later database.</span></span> <span data-ttu-id="90f2c-105">Дополнительные сведения о переносе базы данных SQL Server см.</span><span class="sxs-lookup"><span data-stu-id="90f2c-105">For more information about transferring a database, see the SQL Server documentation.</span></span>

> [!NOTE]
> <span data-ttu-id="90f2c-106">Это действие не разрешено, если база данных не является доверенной.</span><span class="sxs-lookup"><span data-stu-id="90f2c-106">This action will not be allowed if the database is not trusted.</span></span>

## <a name="setting"></a><span data-ttu-id="90f2c-107">Setting</span><span class="sxs-lookup"><span data-stu-id="90f2c-107">Setting</span></span>

<span data-ttu-id="90f2c-108">**«ПереносБазыДанныхSQL»** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="90f2c-108">The **TransferSQLDatabase** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="90f2c-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="90f2c-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="90f2c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="90f2c-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90f2c-111"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="90f2c-111"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="90f2c-112">Имя SQL Server 7.0 или более поздняя версия сервера базы данных выполняется копирование.</span><span class="sxs-lookup"><span data-stu-id="90f2c-112">The name of the SQL Server 7.0 or later database server you are copying to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90f2c-113"><strong>База данных</strong></span><span class="sxs-lookup"><span data-stu-id="90f2c-113"><strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="90f2c-114">Имя новой базы данных, которая будет создана на целевом сервере.</span><span class="sxs-lookup"><span data-stu-id="90f2c-114">The name of the new database that will be created on the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90f2c-115"><strong>Доверительное соединение</strong></span><span class="sxs-lookup"><span data-stu-id="90f2c-115"><strong>Use Trusted Connection</strong></span></span></p></td>
<td><p><span data-ttu-id="90f2c-116">Указывает ли представляет доверительное соединение к серверу SQL Server.</span><span class="sxs-lookup"><span data-stu-id="90f2c-116">Specifes whether or not there is a trusted connection to the SQL Server.</span></span> <span data-ttu-id="90f2c-117">Если задано значение <strong>Да</strong>, то есть доверительное соединение и параметры <strong>входа в систему</strong> и <strong>пароль</strong> не являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="90f2c-117">If set to <strong>Yes</strong>, then there is a trusted connection and the <strong>Login</strong> and <strong>Password</strong> arguments are not required.</span></span> <span data-ttu-id="90f2c-118">Если задано значение <strong>No</strong>, <strong>имя пользователя</strong> и <strong>пароль</strong> аргументов не требуется.</span><span class="sxs-lookup"><span data-stu-id="90f2c-118">If set to <strong>No</strong>, the <strong>Login</strong> and <strong>Password</strong> arguments are required.</span></span> <span data-ttu-id="90f2c-119">По умолчанию используется значение <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="90f2c-119">The default is <strong>Yes</strong>.</span></span> <span data-ttu-id="90f2c-120">При использовании доверительное соединение безопасности SQL Server интегрируется с безопасности операционной системы Windows для обеспечения единого входа сеть и базы данных.</span><span class="sxs-lookup"><span data-stu-id="90f2c-120">When you use a trusted connection, SQL Server security integrates with the Windows operating system security to provide a single log on to the network and the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90f2c-121"><strong>Учетные данные</strong></span><span class="sxs-lookup"><span data-stu-id="90f2c-121"><strong>Login</strong></span></span></p></td>
<td><p><span data-ttu-id="90f2c-122">Имя для входа на целевой сервер.</span><span class="sxs-lookup"><span data-stu-id="90f2c-122">The name of the Login to the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90f2c-123"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="90f2c-123"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="90f2c-124">Пароль для <strong>входа</strong> на конечный сервер.</span><span class="sxs-lookup"><span data-stu-id="90f2c-124">The password for the <strong>Login</strong> argument.</span></span> <span data-ttu-id="90f2c-125">Этот пароль хранится в виде текста в проект Microsoft Access, но скрыт во время операции переноса базы данных.</span><span class="sxs-lookup"><span data-stu-id="90f2c-125">This password is stored as text in the Access project, but is hidden during the transfer database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90f2c-126"><strong>Копирование данных</strong></span><span class="sxs-lookup"><span data-stu-id="90f2c-126"><strong>Transfer Copy Data</strong></span></span></p></td>
<td><p><span data-ttu-id="90f2c-127">Указывает, следует ли включать данные в операции переноса базы данных.</span><span class="sxs-lookup"><span data-stu-id="90f2c-127">Specifies whether or not to include data in the transfer database operation.</span></span> <span data-ttu-id="90f2c-128">Если установлено значение " <strong>Да"</strong>, все данные для всех таблиц, а также все структуры данных, расширенные свойства и объекты базы данных.</span><span class="sxs-lookup"><span data-stu-id="90f2c-128">When set to <strong>Yes</strong>, all data is included for all the tables, along with all data structures, extended properties, and database objects.</span></span> <span data-ttu-id="90f2c-129">Если задано значение <strong>No</strong>, данные не включен из таблиц.</span><span class="sxs-lookup"><span data-stu-id="90f2c-129">When set to <strong>No</strong>, no data is included from the tables.</span></span> <span data-ttu-id="90f2c-130">Структура таблицы и расширенные свойства создаются на целевом сервере, а также все объекты базы данных (за исключением схемы базы данных).</span><span class="sxs-lookup"><span data-stu-id="90f2c-130">Only the table structure and extended properties are created on the destination server, along with all other database objects (except database diagrams).</span></span> <span data-ttu-id="90f2c-131">По умолчанию используется значение <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="90f2c-131">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="90f2c-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="90f2c-132">Remarks</span></span>

<span data-ttu-id="90f2c-133">Нельзя выполнять другие операции во время передачи базы данных.</span><span class="sxs-lookup"><span data-stu-id="90f2c-133">You cannot perform other operations while the database is being transferred.</span></span>

<span data-ttu-id="90f2c-134">**«ПереносБазыДанныхSQL»,** по умолчанию, копирование данных, определений данных, объектов базы данных и расширенные свойства, такие как значения по умолчанию, текстовые ограничения и значений подстановки.</span><span class="sxs-lookup"><span data-stu-id="90f2c-134">The **TransferSQLDatabase** action, by default, copies data, data definitions, database objects, and extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="90f2c-135">Существует требования для переноса базы данных.</span><span class="sxs-lookup"><span data-stu-id="90f2c-135">There are requirements for transferring a database:</span></span>

- <span data-ttu-id="90f2c-136">Необходимо быть членом роли sysadmin на конечном сервере (нет специальных роль необходима на исходном сервере).</span><span class="sxs-lookup"><span data-stu-id="90f2c-136">You must be a member of the sysadmin role on the destination server (No special role is required on the source server).</span></span>

- <span data-ttu-id="90f2c-137">Текущий сервер SQL, подключенный к проекту доступа и на целевой сервер, на которого переключается базы данных должен быть SQL Server версии 7.0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="90f2c-137">The current SQL server connected to the Access project and the destination server you are transferring the database to must be SQL Server version 7.0 or later.</span></span>

  > [!NOTE]
  > <span data-ttu-id="90f2c-138">Связанные серверы не переносятся во время операции переноса базы данных.</span><span class="sxs-lookup"><span data-stu-id="90f2c-138">Linked servers are not transferred during a database transfer operation.</span></span>

<span data-ttu-id="90f2c-139">Чтобы запустить **«ПереносБазыДанныхSQL»** в Visual Basic для приложений (VBA) модуль, используйте метод **TransferSQLDatabase** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="90f2c-139">To run the **TransferSQLDatabase** action in a Visual Basic for Applications (VBA) module, use the **TransferSQLDatabase** method of the **DoCmd** object.</span></span>

