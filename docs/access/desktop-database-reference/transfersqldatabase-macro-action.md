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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306848"
---
# <a name="transfersqldatabase-macro-action"></a><span data-ttu-id="6c1d1-102">Макрокоманда TransferSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="6c1d1-102">TransferSQLDatabase macro action</span></span>

<span data-ttu-id="6c1d1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c1d1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6c1d1-104">В проекте Access действие **TransferSQLDatabase** можно использовать для передачи базы данных Microsoft SQL Server 7.0 или более поздней в другую базу данных SQL Server 7.0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="6c1d1-104">In an Access project, you can use the **TransferSQLDatabase** action to transfer a Microsoft SQL Server 7.0 or later database to another SQL Server 7.0 or later database.</span></span> <span data-ttu-id="6c1d1-105">Дополнительные сведения о передаче базы данных см. в SQL Server документации.</span><span class="sxs-lookup"><span data-stu-id="6c1d1-105">For more information about transferring a database, see the SQL Server documentation.</span></span>

> [!NOTE]
> <span data-ttu-id="6c1d1-106">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="6c1d1-106">This action will not be allowed if the database is not trusted.</span></span>

## <a name="setting"></a><span data-ttu-id="6c1d1-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="6c1d1-107">Setting</span></span>

<span data-ttu-id="6c1d1-108">Действие **TransferSQLDatabase** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="6c1d1-108">The **TransferSQLDatabase** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c1d1-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="6c1d1-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="6c1d1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6c1d1-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c1d1-111"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="6c1d1-111"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6c1d1-112">Имя сервера базы данных SQL Server 7.0 или более поздней копии.</span><span class="sxs-lookup"><span data-stu-id="6c1d1-112">The name of the SQL Server 7.0 or later database server you are copying to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1d1-113"><strong>База данных</strong></span><span class="sxs-lookup"><span data-stu-id="6c1d1-113"><strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="6c1d1-114">Имя новой базы данных, которая будет создана на сервере назначения.</span><span class="sxs-lookup"><span data-stu-id="6c1d1-114">The name of the new database that will be created on the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c1d1-115"><strong>Использование доверенного подключения</strong></span><span class="sxs-lookup"><span data-stu-id="6c1d1-115"><strong>Use Trusted Connection</strong></span></span></p></td>
<td><p><span data-ttu-id="6c1d1-116">Сообщает, существует ли надежное подключение к SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6c1d1-116">Specifes whether or not there is a trusted connection to the SQL Server.</span></span> <span data-ttu-id="6c1d1-117">Если за <strong>установлено "Да",</strong>то существует <strong></strong> надежное подключение, а аргументы <strong>входа</strong> и пароля не требуются.</span><span class="sxs-lookup"><span data-stu-id="6c1d1-117">If set to <strong>Yes</strong>, then there is a trusted connection and the <strong>Login</strong> and <strong>Password</strong> arguments are not required.</span></span> <span data-ttu-id="6c1d1-118">Если за <strong>установлено "Нет",</strong>необходимы аргументы <strong>входа</strong> и пароля. <strong></strong></span><span class="sxs-lookup"><span data-stu-id="6c1d1-118">If set to <strong>No</strong>, the <strong>Login</strong> and <strong>Password</strong> arguments are required.</span></span> <span data-ttu-id="6c1d1-119">Значение по умолчанию <strong>— Да.</strong></span><span class="sxs-lookup"><span data-stu-id="6c1d1-119">The default is <strong>Yes</strong>.</span></span> <span data-ttu-id="6c1d1-120">При использовании доверенного подключения система SQL Server с безопасностью операционной системы Windows, обеспечивая единый вход в сеть и базу данных.</span><span class="sxs-lookup"><span data-stu-id="6c1d1-120">When you use a trusted connection, SQL Server security integrates with the Windows operating system security to provide a single log on to the network and the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1d1-121"><strong>Вход</strong></span><span class="sxs-lookup"><span data-stu-id="6c1d1-121"><strong>Login</strong></span></span></p></td>
<td><p><span data-ttu-id="6c1d1-122">Имя входа на сервер назначения.</span><span class="sxs-lookup"><span data-stu-id="6c1d1-122">The name of the Login to the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c1d1-123"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="6c1d1-123"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="6c1d1-124">Пароль для <strong>аргумента Login.</strong></span><span class="sxs-lookup"><span data-stu-id="6c1d1-124">The password for the <strong>Login</strong> argument.</span></span> <span data-ttu-id="6c1d1-125">Этот пароль хранится в проекте Access в виде текста, но скрыт во время операции переноса базы данных.</span><span class="sxs-lookup"><span data-stu-id="6c1d1-125">This password is stored as text in the Access project, but is hidden during the transfer database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c1d1-126"><strong>Передача данных копии</strong></span><span class="sxs-lookup"><span data-stu-id="6c1d1-126"><strong>Transfer Copy Data</strong></span></span></p></td>
<td><p><span data-ttu-id="6c1d1-127">Указывает, следует ли включать данные в операцию передачи базы данных.</span><span class="sxs-lookup"><span data-stu-id="6c1d1-127">Specifies whether or not to include data in the transfer database operation.</span></span> <span data-ttu-id="6c1d1-128">Если за <strong>установлено "Да",</strong>все данные включаются во все таблицы, а также все структуры данных, расширенные свойства и объекты баз данных.</span><span class="sxs-lookup"><span data-stu-id="6c1d1-128">When set to <strong>Yes</strong>, all data is included for all the tables, along with all data structures, extended properties, and database objects.</span></span> <span data-ttu-id="6c1d1-129">Если за <strong>установлено "Нет",</strong>данные из таблиц не включаются.</span><span class="sxs-lookup"><span data-stu-id="6c1d1-129">When set to <strong>No</strong>, no data is included from the tables.</span></span> <span data-ttu-id="6c1d1-130">На конечном сервере создаются только структура таблицы и расширенные свойства, а также все остальные объекты базы данных (кроме схем базы данных).</span><span class="sxs-lookup"><span data-stu-id="6c1d1-130">Only the table structure and extended properties are created on the destination server, along with all other database objects (except database diagrams).</span></span> <span data-ttu-id="6c1d1-131">Значение по умолчанию <strong>— Да.</strong></span><span class="sxs-lookup"><span data-stu-id="6c1d1-131">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6c1d1-132">Заметки</span><span class="sxs-lookup"><span data-stu-id="6c1d1-132">Remarks</span></span>

<span data-ttu-id="6c1d1-133">Нельзя выполнять другие операции во время переноса базы данных.</span><span class="sxs-lookup"><span data-stu-id="6c1d1-133">You cannot perform other operations while the database is being transferred.</span></span>

<span data-ttu-id="6c1d1-134">Действие **TransferSQLDatabase** по умолчанию копирует данные, определения данных, объекты базы данных и расширенные свойства, такие как значения по умолчанию, текстовые ограничения и значения поиска.</span><span class="sxs-lookup"><span data-stu-id="6c1d1-134">The **TransferSQLDatabase** action, by default, copies data, data definitions, database objects, and extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="6c1d1-135">Существуют требования для передачи базы данных:</span><span class="sxs-lookup"><span data-stu-id="6c1d1-135">There are requirements for transferring a database:</span></span>

- <span data-ttu-id="6c1d1-136">Необходимо быть участником роли sysadmin на сервере назначения (на сервере-источнике не требуется специальная роль).</span><span class="sxs-lookup"><span data-stu-id="6c1d1-136">You must be a member of the sysadmin role on the destination server (No special role is required on the source server).</span></span>

- <span data-ttu-id="6c1d1-137">Текущий SQL к проекту Access и сервер назначения, на который вы переносите базу данных, должен быть SQL Server версии 7.0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="6c1d1-137">The current SQL server connected to the Access project and the destination server you are transferring the database to must be SQL Server version 7.0 or later.</span></span>

  > [!NOTE]
  > <span data-ttu-id="6c1d1-138">Связанные серверы не переносятся во время операции передачи базы данных.</span><span class="sxs-lookup"><span data-stu-id="6c1d1-138">Linked servers are not transferred during a database transfer operation.</span></span>

<span data-ttu-id="6c1d1-139">Чтобы запустить **действие TransferSQLDatabase** в модуле Visual Basic для приложений (VBA), используйте метод **TransferSQLDatabase** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="6c1d1-139">To run the **TransferSQLDatabase** action in a Visual Basic for Applications (VBA) module, use the **TransferSQLDatabase** method of the **DoCmd** object.</span></span>

