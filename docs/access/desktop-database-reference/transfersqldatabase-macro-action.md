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
# <a name="transfersqldatabase-macro-action"></a><span data-ttu-id="88113-102">Макрокоманда TransferSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="88113-102">TransferSQLDatabase macro action</span></span>

<span data-ttu-id="88113-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="88113-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="88113-104">В проекте Access вы можете использовать действие **трансферсклдатабасе** для переноса базы данных Microsoft sql Server 7,0 или более поздней версии в другую базу данных SQL Server 7,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="88113-104">In an Access project, you can use the **TransferSQLDatabase** action to transfer a Microsoft SQL Server 7.0 or later database to another SQL Server 7.0 or later database.</span></span> <span data-ttu-id="88113-105">Дополнительные сведения о переносе базы данных можно найти в документации по SQL Server.</span><span class="sxs-lookup"><span data-stu-id="88113-105">For more information about transferring a database, see the SQL Server documentation.</span></span>

> [!NOTE]
> <span data-ttu-id="88113-106">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="88113-106">This action will not be allowed if the database is not trusted.</span></span>

## <a name="setting"></a><span data-ttu-id="88113-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="88113-107">Setting</span></span>

<span data-ttu-id="88113-108">Макрокоманда **трансферсклдатабасе** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="88113-108">The **TransferSQLDatabase** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="88113-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="88113-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="88113-110">Описание</span><span class="sxs-lookup"><span data-stu-id="88113-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88113-111"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="88113-111"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="88113-112">Имя сервера SQL Server 7,0 или более поздней версии, на который выполняется копирование.</span><span class="sxs-lookup"><span data-stu-id="88113-112">The name of the SQL Server 7.0 or later database server you are copying to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88113-113"><strong>База данных</strong></span><span class="sxs-lookup"><span data-stu-id="88113-113"><strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="88113-114">Имя новой базы данных, которая будет создана на целевом сервере.</span><span class="sxs-lookup"><span data-stu-id="88113-114">The name of the new database that will be created on the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88113-115"><strong>Использование доверенного подключения</strong></span><span class="sxs-lookup"><span data-stu-id="88113-115"><strong>Use Trusted Connection</strong></span></span></p></td>
<td><p><span data-ttu-id="88113-116">СпеЦифес, существует ли доверенное соединение с SQL Server.</span><span class="sxs-lookup"><span data-stu-id="88113-116">Specifes whether or not there is a trusted connection to the SQL Server.</span></span> <span data-ttu-id="88113-117">Если задано значение <strong>"Да"</strong>, то существует доверенное подключение, а аргументы <strong>входа</strong> и <strong>пароля</strong> не являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="88113-117">If set to <strong>Yes</strong>, then there is a trusted connection and the <strong>Login</strong> and <strong>Password</strong> arguments are not required.</span></span> <span data-ttu-id="88113-118">Если задано значение <strong>нет</strong>, аргументы <strong>входа</strong> и <strong>пароля</strong> являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="88113-118">If set to <strong>No</strong>, the <strong>Login</strong> and <strong>Password</strong> arguments are required.</span></span> <span data-ttu-id="88113-119">Значение по умолчанию — <strong>Yes</strong>.</span><span class="sxs-lookup"><span data-stu-id="88113-119">The default is <strong>Yes</strong>.</span></span> <span data-ttu-id="88113-120">При использовании доверенного подключения система безопасности SQL Server интегрируется с системой безопасности операционной системы Windows для предоставления единого входа в сеть и базу данных.</span><span class="sxs-lookup"><span data-stu-id="88113-120">When you use a trusted connection, SQL Server security integrates with the Windows operating system security to provide a single log on to the network and the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88113-121"><strong>Регистрацион</strong></span><span class="sxs-lookup"><span data-stu-id="88113-121"><strong>Login</strong></span></span></p></td>
<td><p><span data-ttu-id="88113-122">Имя входа на целевой сервер.</span><span class="sxs-lookup"><span data-stu-id="88113-122">The name of the Login to the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88113-123"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="88113-123"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="88113-124">Пароль для аргумента <strong>имени входа</strong> .</span><span class="sxs-lookup"><span data-stu-id="88113-124">The password for the <strong>Login</strong> argument.</span></span> <span data-ttu-id="88113-125">Этот пароль хранится в виде текста в проекте Access, но скрыт во время операции переноса базы данных.</span><span class="sxs-lookup"><span data-stu-id="88113-125">This password is stored as text in the Access project, but is hidden during the transfer database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88113-126"><strong>Передача данных копирования</strong></span><span class="sxs-lookup"><span data-stu-id="88113-126"><strong>Transfer Copy Data</strong></span></span></p></td>
<td><p><span data-ttu-id="88113-127">Указывает, следует ли включать данные в операцию переноса базы данных.</span><span class="sxs-lookup"><span data-stu-id="88113-127">Specifies whether or not to include data in the transfer database operation.</span></span> <span data-ttu-id="88113-128">Если задано значение <strong>"Да"</strong>, все данные включаются во все таблицы вместе со всеми структурами данных, расширенными свойствами и объектами базы данных.</span><span class="sxs-lookup"><span data-stu-id="88113-128">When set to <strong>Yes</strong>, all data is included for all the tables, along with all data structures, extended properties, and database objects.</span></span> <span data-ttu-id="88113-129">Если для этого параметра установлено значение <strong>нет</strong>, данные из таблиц не включаются.</span><span class="sxs-lookup"><span data-stu-id="88113-129">When set to <strong>No</strong>, no data is included from the tables.</span></span> <span data-ttu-id="88113-130">На целевом сервере создаются только структура таблицы и расширенные свойства, а также все остальные объекты базы данных (за исключением схем баз данных).</span><span class="sxs-lookup"><span data-stu-id="88113-130">Only the table structure and extended properties are created on the destination server, along with all other database objects (except database diagrams).</span></span> <span data-ttu-id="88113-131">Значение по умолчанию — <strong>Yes</strong>.</span><span class="sxs-lookup"><span data-stu-id="88113-131">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="88113-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="88113-132">Remarks</span></span>

<span data-ttu-id="88113-133">При передаче базы данных невозможно выполнить другие операции.</span><span class="sxs-lookup"><span data-stu-id="88113-133">You cannot perform other operations while the database is being transferred.</span></span>

<span data-ttu-id="88113-134">Действие **трансферсклдатабасе** по умолчанию копирует данные, определения данных, объекты базы данных и расширенные свойства, такие как значения по умолчанию, ограничения текста и значения подстановки.</span><span class="sxs-lookup"><span data-stu-id="88113-134">The **TransferSQLDatabase** action, by default, copies data, data definitions, database objects, and extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="88113-135">Существуют требования для переноса базы данных:</span><span class="sxs-lookup"><span data-stu-id="88113-135">There are requirements for transferring a database:</span></span>

- <span data-ttu-id="88113-136">Необходимо быть членом роли sysadmin на целевом сервере (на исходном сервере не требуется никаких дополнительных ролей).</span><span class="sxs-lookup"><span data-stu-id="88113-136">You must be a member of the sysadmin role on the destination server (No special role is required on the source server).</span></span>

- <span data-ttu-id="88113-137">Текущий SQL Server, подключенный к проекту Access и конечный сервер, на который вы передаете базу данных, должен быть SQL Server версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="88113-137">The current SQL server connected to the Access project and the destination server you are transferring the database to must be SQL Server version 7.0 or later.</span></span>

  > [!NOTE]
  > <span data-ttu-id="88113-138">Связанные серверы не передаются во время операции переноса базы данных.</span><span class="sxs-lookup"><span data-stu-id="88113-138">Linked servers are not transferred during a database transfer operation.</span></span>

<span data-ttu-id="88113-139">Чтобы запустить действие **трансферсклдатабасе** в модуле Visual Basic для приложений (VBA), используйте метод **трансферсклдатабасе** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="88113-139">To run the **TransferSQLDatabase** action in a Visual Basic for Applications (VBA) module, use the **TransferSQLDatabase** method of the **DoCmd** object.</span></span>

