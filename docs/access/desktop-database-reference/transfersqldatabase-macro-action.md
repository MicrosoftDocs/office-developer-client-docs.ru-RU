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
# <a name="transfersqldatabase-macro-action"></a><span data-ttu-id="b40b7-102">Макрокоманда TransferSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="b40b7-102">TransferSQLDatabase macro action</span></span>

<span data-ttu-id="b40b7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b40b7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b40b7-104">В проекте Access вы можете использовать действие **TransferSQLDatabase** для передачи базы данных Microsoft SQL Server 7.0 или более поздней базы данных в другую SQL Server 7.0 или более поздней базе данных.</span><span class="sxs-lookup"><span data-stu-id="b40b7-104">In an Access project, you can use the **TransferSQLDatabase** action to transfer a Microsoft SQL Server 7.0 or later database to another SQL Server 7.0 or later database.</span></span> <span data-ttu-id="b40b7-105">Дополнительные сведения о передаче базы данных см. в SQL Server документации.</span><span class="sxs-lookup"><span data-stu-id="b40b7-105">For more information about transferring a database, see the SQL Server documentation.</span></span>

> [!NOTE]
> <span data-ttu-id="b40b7-106">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="b40b7-106">This action will not be allowed if the database is not trusted.</span></span>

## <a name="setting"></a><span data-ttu-id="b40b7-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="b40b7-107">Setting</span></span>

<span data-ttu-id="b40b7-108">Действие **TransferSQLDatabase** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="b40b7-108">The **TransferSQLDatabase** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b40b7-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="b40b7-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b40b7-110">Описание</span><span class="sxs-lookup"><span data-stu-id="b40b7-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b40b7-111"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b40b7-111"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b40b7-112">Имя сервера SQL Server 7.0 или более поздней базы данных, на который вы копируете.</span><span class="sxs-lookup"><span data-stu-id="b40b7-112">The name of the SQL Server 7.0 or later database server you are copying to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b40b7-113"><strong>База данных</strong></span><span class="sxs-lookup"><span data-stu-id="b40b7-113"><strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="b40b7-114">Имя новой базы данных, которая будет создана на сервере назначения.</span><span class="sxs-lookup"><span data-stu-id="b40b7-114">The name of the new database that will be created on the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b40b7-115"><strong>Использование надежного подключения</strong></span><span class="sxs-lookup"><span data-stu-id="b40b7-115"><strong>Use Trusted Connection</strong></span></span></p></td>
<td><p><span data-ttu-id="b40b7-116">Засвидекторирует, есть ли надежное подключение к SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b40b7-116">Specifes whether or not there is a trusted connection to the SQL Server.</span></span> <span data-ttu-id="b40b7-117">Если <strong>установлено да,</strong>то есть доверяемая <strong></strong> связь, и аргументы <strong>входа</strong> и пароля не требуются.</span><span class="sxs-lookup"><span data-stu-id="b40b7-117">If set to <strong>Yes</strong>, then there is a trusted connection and the <strong>Login</strong> and <strong>Password</strong> arguments are not required.</span></span> <span data-ttu-id="b40b7-118">Если <strong>установлено нет,</strong>необходимо использовать аргументы <strong>Login</strong> и <strong>Password.</strong></span><span class="sxs-lookup"><span data-stu-id="b40b7-118">If set to <strong>No</strong>, the <strong>Login</strong> and <strong>Password</strong> arguments are required.</span></span> <span data-ttu-id="b40b7-119">По умолчанию — <strong>Да.</strong></span><span class="sxs-lookup"><span data-stu-id="b40b7-119">The default is <strong>Yes</strong>.</span></span> <span data-ttu-id="b40b7-120">При использовании надежного подключения SQL Server безопасности интегрируется с безопасностью Windows операционной системы для обеспечения единого входа в сеть и базу данных.</span><span class="sxs-lookup"><span data-stu-id="b40b7-120">When you use a trusted connection, SQL Server security integrates with the Windows operating system security to provide a single log on to the network and the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b40b7-121"><strong>Вход</strong></span><span class="sxs-lookup"><span data-stu-id="b40b7-121"><strong>Login</strong></span></span></p></td>
<td><p><span data-ttu-id="b40b7-122">Имя входа на сервер назначения.</span><span class="sxs-lookup"><span data-stu-id="b40b7-122">The name of the Login to the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b40b7-123"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="b40b7-123"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="b40b7-124">Пароль для <strong>аргумента Login.</strong></span><span class="sxs-lookup"><span data-stu-id="b40b7-124">The password for the <strong>Login</strong> argument.</span></span> <span data-ttu-id="b40b7-125">Этот пароль хранится в виде текста в проекте Access, но скрыт во время операции базы данных передачи.</span><span class="sxs-lookup"><span data-stu-id="b40b7-125">This password is stored as text in the Access project, but is hidden during the transfer database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b40b7-126"><strong>Передача данных копирования</strong></span><span class="sxs-lookup"><span data-stu-id="b40b7-126"><strong>Transfer Copy Data</strong></span></span></p></td>
<td><p><span data-ttu-id="b40b7-127">Указывает, следует ли включать данные в операцию базы данных передачи.</span><span class="sxs-lookup"><span data-stu-id="b40b7-127">Specifies whether or not to include data in the transfer database operation.</span></span> <span data-ttu-id="b40b7-128">При наборе <strong>Да</strong>все данные включаются для всех таблиц, а также для всех структур данных, расширенных свойств и объектов базы данных.</span><span class="sxs-lookup"><span data-stu-id="b40b7-128">When set to <strong>Yes</strong>, all data is included for all the tables, along with all data structures, extended properties, and database objects.</span></span> <span data-ttu-id="b40b7-129">При наборе <strong>"Нет"</strong>данные из таблиц не включаются.</span><span class="sxs-lookup"><span data-stu-id="b40b7-129">When set to <strong>No</strong>, no data is included from the tables.</span></span> <span data-ttu-id="b40b7-130">На сервере назначения создаются только структура таблицы и расширенные свойства, а также все другие объекты базы данных (кроме схем баз данных).</span><span class="sxs-lookup"><span data-stu-id="b40b7-130">Only the table structure and extended properties are created on the destination server, along with all other database objects (except database diagrams).</span></span> <span data-ttu-id="b40b7-131">По умолчанию — <strong>Да.</strong></span><span class="sxs-lookup"><span data-stu-id="b40b7-131">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b40b7-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="b40b7-132">Remarks</span></span>

<span data-ttu-id="b40b7-133">Вы не можете выполнять другие операции во время переноса базы данных.</span><span class="sxs-lookup"><span data-stu-id="b40b7-133">You cannot perform other operations while the database is being transferred.</span></span>

<span data-ttu-id="b40b7-134">Действие **TransferSQLDatabase** по умолчанию копирует данные, определения данных, объекты баз данных и расширенные свойства, такие как значения по умолчанию, текстовые ограничения и значения поиска.</span><span class="sxs-lookup"><span data-stu-id="b40b7-134">The **TransferSQLDatabase** action, by default, copies data, data definitions, database objects, and extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="b40b7-135">Для передачи базы данных существуют требования:</span><span class="sxs-lookup"><span data-stu-id="b40b7-135">There are requirements for transferring a database:</span></span>

- <span data-ttu-id="b40b7-136">Вы должны быть членом роли sysadmin на сервере назначения (не требуется специальная роль на исходный сервер).</span><span class="sxs-lookup"><span data-stu-id="b40b7-136">You must be a member of the sysadmin role on the destination server (No special role is required on the source server).</span></span>

- <span data-ttu-id="b40b7-137">Текущий SQL, подключенный к проекту Access и серверу назначения, который вы переносите, должен быть SQL Server версии 7.0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="b40b7-137">The current SQL server connected to the Access project and the destination server you are transferring the database to must be SQL Server version 7.0 or later.</span></span>

  > [!NOTE]
  > <span data-ttu-id="b40b7-138">Связанные серверы не передаются во время операции передачи базы данных.</span><span class="sxs-lookup"><span data-stu-id="b40b7-138">Linked servers are not transferred during a database transfer operation.</span></span>

<span data-ttu-id="b40b7-139">Чтобы выполнить действие **TransferSQLDatabase** в модуле Visual Basic для приложений (VBA), используйте метод **TransferSQLDatabase** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="b40b7-139">To run the **TransferSQLDatabase** action in a Visual Basic for Applications (VBA) module, use the **TransferSQLDatabase** method of the **DoCmd** object.</span></span>

