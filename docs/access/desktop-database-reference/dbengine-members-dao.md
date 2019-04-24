---
title: Элементы DBEngine (DAO)
TOCTitle: DBEngine Members
ms:assetid: 740b6a85-585f-0e1d-710b-84ba24825325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195868(v=office.15)
ms:contentKeyID: 48545652
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1128b27385ef9f8c898fb79d05ae28d596c4af6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294283"
---
# <a name="dbengine-members-dao"></a><span data-ttu-id="9ca56-102">Элементы DBEngine (DAO)</span><span class="sxs-lookup"><span data-stu-id="9ca56-102">DBEngine members (DAO)</span></span>


<span data-ttu-id="9ca56-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ca56-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9ca56-104">Объект DBEngine — это объект верхнего уровня объектной модели DAO.</span><span class="sxs-lookup"><span data-stu-id="9ca56-104">The DBEngine object is the top level object in the DAO object model.</span></span>

## <a name="methods"></a><span data-ttu-id="9ca56-105">Методы</span><span class="sxs-lookup"><span data-stu-id="9ca56-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9ca56-106">Имя</span><span class="sxs-lookup"><span data-stu-id="9ca56-106">Name</span></span></p></th>
<th><p><span data-ttu-id="9ca56-107">Описание</span><span class="sxs-lookup"><span data-stu-id="9ca56-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ca56-108"><strong><a href="dbengine-begintrans-method-dao.md">BeginTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ca56-108"><strong><a href="dbengine-begintrans-method-dao.md">BeginTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ca56-109">Начинает новую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="9ca56-109">Begins a new transaction.</span></span> <span data-ttu-id="9ca56-110">Чтение и запись <strong>базы данных</strong>.</span><span class="sxs-lookup"><span data-stu-id="9ca56-110">Read/write <strong>Database</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ca56-111"><strong><a href="dbengine-committrans-method-dao.md">CommitTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ca56-111"><strong><a href="dbengine-committrans-method-dao.md">CommitTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ca56-112">Завершает текущую транзакцию и сохраняет изменения.</span><span class="sxs-lookup"><span data-stu-id="9ca56-112">Ends the current transaction and saves the changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ca56-113"><strong><a href="dbengine-compactdatabase-method-dao.md">CompactDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ca56-113"><strong><a href="dbengine-compactdatabase-method-dao.md">CompactDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ca56-114">Копирует и сжимает закрытую базу данных, а также позволяет изменить ее версию, порядок сортировки и шифрование.</span><span class="sxs-lookup"><span data-stu-id="9ca56-114">Copies and compacts a closed database, and gives you the option of changing its version, collating order, and encryption.</span></span> <span data-ttu-id="9ca56-115">(Только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9ca56-115">(Microsoft Access workspaces only).</span></span> <span data-ttu-id="9ca56-116">.</span><span class="sxs-lookup"><span data-stu-id="9ca56-116"></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ca56-117"><strong><a href="dbengine-createdatabase-method-dao.md">CreateDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ca56-117"><strong><a href="dbengine-createdatabase-method-dao.md">CreateDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ca56-118">Создает новый объект <strong><a href="database-object-dao.md">Database</a></strong> , сохраняет базу данных на диске и возвращает открытый объект <strong>базы данных</strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9ca56-118">Creates a new <strong><a href="database-object-dao.md">Database</a></strong> object, saves the database to disk, and returns an opened <strong>Database</strong> object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="9ca56-119">.</span><span class="sxs-lookup"><span data-stu-id="9ca56-119"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ca56-120"><strong><a href="dbengine-createworkspace-method-dao.md">CreateWorkspace</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ca56-120"><strong><a href="dbengine-createworkspace-method-dao.md">CreateWorkspace</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ca56-121">Создает новый объект <strong><a href="workspace-object-dao.md">Workspace</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="9ca56-121">Creates a new <strong><a href="workspace-object-dao.md">Workspace</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ca56-122"><strong><a href="dbengine-idle-method-dao.md">Простоя</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ca56-122"><strong><a href="dbengine-idle-method-dao.md">Idle</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ca56-123">ПриОстанавливает обработку данных, позволяя ядру СУБД Microsoft Access выполнять все ожидающие задачи, такие как оптимизация памяти или время ожидания страниц (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9ca56-123">Suspends data processing, enabling the Microsoft Access database engine to complete any pending tasks, such as memory optimization or page timeouts (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ca56-124"><strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ca56-124"><strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ca56-125">Одно из значений <strong><a href="workspacetypeenum-enumeration-dao.md">воркспацетипинум</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="9ca56-125">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>
<td><p><span data-ttu-id="9ca56-126"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="9ca56-126"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="9ca56-127">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="9ca56-127">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="9ca56-128">Открывает объект <strong><a href="connection-object-dao.md">Connection</a></strong> в источнике данных ODBC (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="9ca56-128">Opens a <strong><a href="connection-object-dao.md">Connection</a></strong> object on an ODBC data source (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ca56-129"><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ca56-129"><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ca56-130">Открывает указанную базу данных и возвращает ссылку на объект <strong><a href="database-object-dao.md">базы данных</a></strong> , представляющий эту базу данных.</span><span class="sxs-lookup"><span data-stu-id="9ca56-130">Opens a specified database and returns a reference to the <strong><a href="database-object-dao.md">Database</a></strong> object that represents it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ca56-131"><strong><a href="dbengine-registerdatabase-method-dao.md">RegisterDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ca56-131"><strong><a href="dbengine-registerdatabase-method-dao.md">RegisterDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ca56-132">Вводит сведения о подключении для источника данных ODBC в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="9ca56-132">Enters connection information for an ODBC data source in the Windows Registry.</span></span> <span data-ttu-id="9ca56-133">Драйверу ODBC необходимы сведения о подключении при открытии источника данных ODBC во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="9ca56-133">The ODBC driver needs connection information when the ODBC data source is opened during a session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ca56-134"><strong><a href="dbengine-rollback-method-dao.md">Отката</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ca56-134"><strong><a href="dbengine-rollback-method-dao.md">Rollback</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ca56-135">Завершает текущую транзакцию и восстанавливает базы данных в объекте <strong>Workspace</strong> в том состоянии, в котором они были в момент начала текущей транзакции.</span><span class="sxs-lookup"><span data-stu-id="9ca56-135">Ends the current transaction and restores the databases in the <strong>Workspace</strong> object to the state they were in when the current transaction began.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ca56-136"><strong><a href="dbengine-setoption-method-dao.md">SetOption</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ca56-136"><strong><a href="dbengine-setoption-method-dao.md">SetOption</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ca56-137">Временно переопределяет значения ключей ядра СУБД Microsoft Access в реестре Windows (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9ca56-137">Temporarily overrides values for the Microsoft Access database engine keys in the Windows Registry (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="9ca56-138">Свойства</span><span class="sxs-lookup"><span data-stu-id="9ca56-138">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9ca56-139">Имя</span><span class="sxs-lookup"><span data-stu-id="9ca56-139">Name</span></span></p></th>
<th><p><span data-ttu-id="9ca56-140">Описание</span><span class="sxs-lookup"><span data-stu-id="9ca56-140">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ca56-141"><strong><a href="dbengine-defaultpassword-property-dao.md">DefaultPassword</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ca56-141"><strong><a href="dbengine-defaultpassword-property-dao.md">DefaultPassword</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ca56-142">Задает пароль, используемый для создания <strong>рабочей области</strong> по умолчанию при ее инициализации.</span><span class="sxs-lookup"><span data-stu-id="9ca56-142">Sets the password used to create the default <strong>Workspace</strong> when it is initialized.</span></span> <span data-ttu-id="9ca56-143">Для чтения и записи, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="9ca56-143">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ca56-144"><strong><a href="dbengine-defaulttype-property-dao.md">DefaultType</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ca56-144"><strong><a href="dbengine-defaulttype-property-dao.md">DefaultType</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ca56-145">Задает или возвращает значение, указывающее тип рабочей области, который будет использоваться при создании следующего объекта <strong><a href="workspace-object-dao.md">Workspace</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="9ca56-145">Sets or returns a value that indicates what type of workspace will be used by the next <strong><a href="workspace-object-dao.md">Workspace</a></strong> object created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ca56-146"><strong><a href="dbengine-defaultuser-property-dao.md">DefaultUser</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ca56-146"><strong><a href="dbengine-defaultuser-property-dao.md">DefaultUser</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ca56-147">Задает имя пользователя, используемое для создания <strong>рабочей области</strong> по умолчанию при ее инициализации.</span><span class="sxs-lookup"><span data-stu-id="9ca56-147">Sets the user name used to create the default <strong>Workspace</strong> when it is initialized.</span></span> <span data-ttu-id="9ca56-148">Для чтения и записи, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="9ca56-148">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ca56-149"><strong><a href="dbengine-errors-property-dao.md">Обнаружен</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ca56-149"><strong><a href="dbengine-errors-property-dao.md">Errors</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ca56-150">Возвращает коллекцию <strong>Errors</strong> , содержащую все хранимые объекты <strong>Error</strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="9ca56-150">Returns an <strong>Errors</strong> collection that contains all of the stored <strong>Error</strong> objects for the specified object.</span></span> <span data-ttu-id="9ca56-151">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9ca56-151">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ca56-152"><strong><a href="dbengine-inipath-property-dao.md">IniPath</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ca56-152"><strong><a href="dbengine-inipath-property-dao.md">IniPath</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ca56-153">Задает или возвращает сведения о разделе реестра Windows, который содержит значения для ядра СУБД Microsoft Access (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9ca56-153">Sets or returns information about the Windows Registry key that contains values for the Microsoft Access database engine (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ca56-154"><strong><a href="dbengine-logintimeout-property-dao.md">LoginTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ca56-154"><strong><a href="dbengine-logintimeout-property-dao.md">LoginTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ca56-155">Задает или возвращает число секунд до возникновения ошибки при попытке входа в базу данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="9ca56-155">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ca56-156"><strong><a href="dbengine-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ca56-156"><strong><a href="dbengine-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ca56-157">Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="9ca56-157">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="9ca56-158">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9ca56-158">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ca56-159"><strong><a href="dbengine-version-property-dao.md">Версия</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ca56-159"><strong><a href="dbengine-version-property-dao.md">Version</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ca56-160">Рретурнс используемая версия объекта DAO.</span><span class="sxs-lookup"><span data-stu-id="9ca56-160">Rreturns the version of DAO currently in use.</span></span> <span data-ttu-id="9ca56-161">Только для чтения, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="9ca56-161">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ca56-162"><strong><a href="dbengine-workspaces-property-dao.md">Workspaces</a></strong></span><span class="sxs-lookup"><span data-stu-id="9ca56-162"><strong><a href="dbengine-workspaces-property-dao.md">Workspaces</a></strong></span></span></p></td>
<td><p><span data-ttu-id="9ca56-163">Возвращает коллекцию <strong>workspaces</strong> , содержащую все активные, нескрытые объекты <strong>рабочей области</strong> .</span><span class="sxs-lookup"><span data-stu-id="9ca56-163">Returns a <strong>Workspaces</strong> collection that contains all of the active, unhidden <strong>Workspace</strong> objects.</span></span> <span data-ttu-id="9ca56-164">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9ca56-164">Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

