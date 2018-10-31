---
title: DBEngine Members (DAO)
TOCTitle: DBEngine Members
ms:assetid: 740b6a85-585f-0e1d-710b-84ba24825325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195868(v=office.15)
ms:contentKeyID: 48545652
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7b534d4595bd003c76e756c44d6e88f53a725cc8
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861787"
---
# <a name="dbengine-members-dao"></a><span data-ttu-id="5994b-102">DBEngine Members (DAO)</span><span class="sxs-lookup"><span data-stu-id="5994b-102">DBEngine Members (DAO)</span></span>


<span data-ttu-id="5994b-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5994b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5994b-104">Объект DBEngine — это объект верхнего уровня в объектной модели DAO.</span><span class="sxs-lookup"><span data-stu-id="5994b-104">The DBEngine object is the top level object in the DAO object model.</span></span>

## <a name="methods"></a><span data-ttu-id="5994b-105">Методы</span><span class="sxs-lookup"><span data-stu-id="5994b-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5994b-106">Имя</span><span class="sxs-lookup"><span data-stu-id="5994b-106">Name</span></span></p></th>
<th><p><span data-ttu-id="5994b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="5994b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5994b-108"><strong><a href="dbengine-begintrans-method-dao.md">BeginTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="5994b-108"><strong><a href="dbengine-begintrans-method-dao.md">BeginTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5994b-109">Начало новой транзакции.</span><span class="sxs-lookup"><span data-stu-id="5994b-109">Begins a new transaction.</span></span> <span data-ttu-id="5994b-110">Чтение и запись <strong>базы данных</strong>.</span><span class="sxs-lookup"><span data-stu-id="5994b-110">Read/write <strong>Database</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5994b-111"><strong><a href="dbengine-committrans-method-dao.md">CommitTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="5994b-111"><strong><a href="dbengine-committrans-method-dao.md">CommitTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5994b-112">Завершает текущий транзакций и сохраняет изменения.</span><span class="sxs-lookup"><span data-stu-id="5994b-112">Ends the current transaction and saves the changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5994b-113"><strong><a href="dbengine-compactdatabase-method-dao.md">CompactDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="5994b-113"><strong><a href="dbengine-compactdatabase-method-dao.md">CompactDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5994b-114">Копирует и сжимает закрытой базы данных и позволяет изменить его версию, сортировки порядок и шифрования.</span><span class="sxs-lookup"><span data-stu-id="5994b-114">Copies and compacts a closed database, and gives you the option of changing its version, collating order, and encryption.</span></span> <span data-ttu-id="5994b-115">(Microsoft Access рабочие области только).</span><span class="sxs-lookup"><span data-stu-id="5994b-115">(Microsoft Access workspaces only).</span></span> <span data-ttu-id="5994b-116">.</span><span class="sxs-lookup"><span data-stu-id="5994b-116"></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5994b-117"><strong><a href="dbengine-createdatabase-method-dao.md">CreateDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="5994b-117"><strong><a href="dbengine-createdatabase-method-dao.md">CreateDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5994b-118">Создает новый объект <strong><a href="database-object-dao.md">базы данных</a></strong> , сохраняет базы данных на диск и возвращает объект открыт <strong>базы данных</strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="5994b-118">Creates a new <strong><a href="database-object-dao.md">Database</a></strong> object, saves the database to disk, and returns an opened <strong>Database</strong> object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="5994b-119">.</span><span class="sxs-lookup"><span data-stu-id="5994b-119"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5994b-120"><strong><a href="dbengine-createworkspace-method-dao.md">CreateWorkspace</a></strong></span><span class="sxs-lookup"><span data-stu-id="5994b-120"><strong><a href="dbengine-createworkspace-method-dao.md">CreateWorkspace</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5994b-121">Создает новый объект <strong><a href="workspace-object-dao.md">рабочей области</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="5994b-121">Creates a new <strong><a href="workspace-object-dao.md">Workspace</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5994b-122"><strong><a href="dbengine-idle-method-dao.md">Простоя</a></strong></span><span class="sxs-lookup"><span data-stu-id="5994b-122"><strong><a href="dbengine-idle-method-dao.md">Idle</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5994b-123">Выполняется приостановка обработки данных, позволяя ядро базы данных Microsoft Access завершить все ожидающие задач, таких как оптимизации памяти или время ожидания страницы (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="5994b-123">Suspends data processing, enabling the Microsoft Access database engine to complete any pending tasks, such as memory optimization or page timeouts (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5994b-124"><strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong></span><span class="sxs-lookup"><span data-stu-id="5994b-124"><strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="5994b-125">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="5994b-125">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="5994b-126">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="5994b-126">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="5994b-127">Открывает объект <strong><a href="connection-object-dao.md">подключения</a></strong> для источника данных ODBC (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="5994b-127">Opens a <strong><a href="connection-object-dao.md">Connection</a></strong> object on an ODBC data source (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5994b-128"><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="5994b-128"><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5994b-129">Открывает указанной базы данных и возвращает ссылку на объект <strong><a href="database-object-dao.md">базы данных</a></strong> , который представляет его.</span><span class="sxs-lookup"><span data-stu-id="5994b-129">Opens a specified database and returns a reference to the <strong><a href="database-object-dao.md">Database</a></strong> object that represents it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5994b-130"><strong><a href="dbengine-registerdatabase-method-dao.md">RegisterDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="5994b-130"><strong><a href="dbengine-registerdatabase-method-dao.md">RegisterDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5994b-131">Вводит сведения о подключении к источнику данных ODBC в реестре Windows.</span><span class="sxs-lookup"><span data-stu-id="5994b-131">Enters connection information for an ODBC data source in the Windows Registry.</span></span> <span data-ttu-id="5994b-132">Драйвер ODBC требуются данные подключения при открытии источника данных во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="5994b-132">The ODBC driver needs connection information when the ODBC data source is opened during a session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5994b-133"><strong><a href="dbengine-rollback-method-dao.md">Откат</a></strong></span><span class="sxs-lookup"><span data-stu-id="5994b-133"><strong><a href="dbengine-rollback-method-dao.md">Rollback</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5994b-134">Завершает текущий транзакцию и восстановление базы данных в объекте <strong>рабочей области</strong> для состояния, в котором они были на момент начала текущей транзакции.</span><span class="sxs-lookup"><span data-stu-id="5994b-134">Ends the current transaction and restores the databases in the <strong>Workspace</strong> object to the state they were in when the current transaction began.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5994b-135"><strong><a href="dbengine-setoption-method-dao.md">SetOption</a></strong></span><span class="sxs-lookup"><span data-stu-id="5994b-135"><strong><a href="dbengine-setoption-method-dao.md">SetOption</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5994b-136">Временно переопределяет значения для клавиш ядра базы данных Microsoft Access в реестре Windows (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="5994b-136">Temporarily overrides values for the Microsoft Access database engine keys in the Windows Registry (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="5994b-137">Свойства</span><span class="sxs-lookup"><span data-stu-id="5994b-137">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5994b-138">Имя</span><span class="sxs-lookup"><span data-stu-id="5994b-138">Name</span></span></p></th>
<th><p><span data-ttu-id="5994b-139">Описание</span><span class="sxs-lookup"><span data-stu-id="5994b-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5994b-140"><strong><a href="dbengine-defaultpassword-property-dao.md">DefaultPassword</a></strong></span><span class="sxs-lookup"><span data-stu-id="5994b-140"><strong><a href="dbengine-defaultpassword-property-dao.md">DefaultPassword</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5994b-141">Задает пароль, используемый для создания <strong>рабочей области</strong> по умолчанию при ее инициализации.</span><span class="sxs-lookup"><span data-stu-id="5994b-141">Sets the password used to create the default <strong>Workspace</strong> when it is initialized.</span></span> <span data-ttu-id="5994b-142">Для чтения и записи, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="5994b-142">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5994b-143"><strong><a href="dbengine-defaulttype-property-dao.md">DefaultType</a></strong></span><span class="sxs-lookup"><span data-stu-id="5994b-143"><strong><a href="dbengine-defaulttype-property-dao.md">DefaultType</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5994b-144">Задает или возвращает значение, указывающее, какой тип рабочей области будет использоваться далее созданный объект <strong><a href="workspace-object-dao.md">рабочей области</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="5994b-144">Sets or returns a value that indicates what type of workspace will be used by the next <strong><a href="workspace-object-dao.md">Workspace</a></strong> object created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5994b-145"><strong><a href="dbengine-defaultuser-property-dao.md">DefaultUser</a></strong></span><span class="sxs-lookup"><span data-stu-id="5994b-145"><strong><a href="dbengine-defaultuser-property-dao.md">DefaultUser</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5994b-146">Задает имя пользователя, используемое для создания <strong>рабочей области</strong> по умолчанию при ее инициализации.</span><span class="sxs-lookup"><span data-stu-id="5994b-146">Sets the user name used to create the default <strong>Workspace</strong> when it is initialized.</span></span> <span data-ttu-id="5994b-147">Для чтения и записи, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="5994b-147">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5994b-148"><strong><a href="dbengine-errors-property-dao.md">Ошибки</a></strong></span><span class="sxs-lookup"><span data-stu-id="5994b-148"><strong><a href="dbengine-errors-property-dao.md">Errors</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5994b-149">Возвращает коллекцию <strong>ошибок</strong> , который содержит все хранимые объекты <strong>об ошибках</strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="5994b-149">Returns an <strong>Errors</strong> collection that contains all of the stored <strong>Error</strong> objects for the specified object.</span></span> <span data-ttu-id="5994b-150">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5994b-150">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5994b-151"><strong><a href="dbengine-inipath-property-dao.md">IniPath</a></strong></span><span class="sxs-lookup"><span data-stu-id="5994b-151"><strong><a href="dbengine-inipath-property-dao.md">IniPath</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5994b-152">Задает или возвращает сведения о раздел реестра Windows, который содержит значения для ядро базы данных Microsoft Access (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="5994b-152">Sets or returns information about the Windows Registry key that contains values for the Microsoft Access database engine (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5994b-153"><strong><a href="dbengine-logintimeout-property-dao.md">LoginTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="5994b-153"><strong><a href="dbengine-logintimeout-property-dao.md">LoginTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5994b-154">Задает или возвращает число секунд, прежде чем возникает ошибка при попытке выполнить вход в базе данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="5994b-154">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5994b-155"><strong><a href="dbengine-properties-property-dao.md">Свойства</a></strong></span><span class="sxs-lookup"><span data-stu-id="5994b-155"><strong><a href="dbengine-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5994b-156">Возвращает коллекцию <strong><a href="properties-collection-dao.md">свойств</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="5994b-156">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="5994b-157">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5994b-157">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5994b-158"><strong><a href="dbengine-version-property-dao.md">Версия</a></strong></span><span class="sxs-lookup"><span data-stu-id="5994b-158"><strong><a href="dbengine-version-property-dao.md">Version</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5994b-159">Возвращает версию DAO в настоящее время используется.</span><span class="sxs-lookup"><span data-stu-id="5994b-159">Rreturns the version of DAO currently in use.</span></span> <span data-ttu-id="5994b-160">Только для чтения, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="5994b-160">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5994b-161"><strong><a href="dbengine-workspaces-property-dao.md">Рабочие области</a></strong></span><span class="sxs-lookup"><span data-stu-id="5994b-161"><strong><a href="dbengine-workspaces-property-dao.md">Workspaces</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5994b-162">Возвращает коллекцию <strong>рабочих областей</strong> , содержащий все объекты active, Показать <strong>рабочей области</strong> .</span><span class="sxs-lookup"><span data-stu-id="5994b-162">Returns a <strong>Workspaces</strong> collection that contains all of the active, unhidden <strong>Workspace</strong> objects.</span></span> <span data-ttu-id="5994b-163">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5994b-163">Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

