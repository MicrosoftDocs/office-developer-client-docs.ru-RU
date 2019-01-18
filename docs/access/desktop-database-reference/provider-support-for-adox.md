---
title: Поддержка поставщиков для ADOX
TOCTitle: Provider support for ADOX
ms:assetid: 32ea3236-d69f-df94-1685-d8791aeb9e0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249100(v=office.15)
ms:contentKeyID: 48544091
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a92ffe9b4b713518330d9dbfd9979d904a5abe8e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703512"
---
# <a name="provider-support-for-adox"></a><span data-ttu-id="93356-102">Поддержка поставщиков для ADOX</span><span class="sxs-lookup"><span data-stu-id="93356-102">Provider support for ADOX</span></span>


<span data-ttu-id="93356-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="93356-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="93356-104">Некоторые возможности ADOX не поддерживаются, в зависимости от поставщика данных OLE DB.</span><span class="sxs-lookup"><span data-stu-id="93356-104">Certain features of ADOX are unsupported, depending upon your OLE DB data provider.</span></span> <span data-ttu-id="93356-105">ADOX полностью поддерживаются с помощью [Поставщика OLE DB для Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md).</span><span class="sxs-lookup"><span data-stu-id="93356-105">ADOX is fully supported with the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md).</span></span> <span data-ttu-id="93356-106">Неподдерживаемые функции с помощью [Поставщик Microsoft OLE DB для SQL Server](microsoft-ole-db-provider-for-sql-server.md), [Поставщик Microsoft OLE DB для ODBC](microsoft-ole-db-provider-for-odbc.md)или [Поставщик Microsoft OLE DB для Oracle](microsoft-ole-db-provider-for-oracle.md) , перечислены ниже.</span><span class="sxs-lookup"><span data-stu-id="93356-106">The unsupported features with the [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), the [Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md), or the [Microsoft OLE DB Provider for Oracle](microsoft-ole-db-provider-for-oracle.md) are listed below.</span></span> <span data-ttu-id="93356-107">Другие поставщики OLE DB для Microsoft ADOX не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="93356-107">ADOX is not supported by any other Microsoft OLE DB providers.</span></span>

## <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="93356-108">Поставщик Microsoft OLE DB для SQL Server</span><span class="sxs-lookup"><span data-stu-id="93356-108">Microsoft OLE DB Provider for SQL Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="93356-109">Объект или семейства сайтов</span><span class="sxs-lookup"><span data-stu-id="93356-109">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="93356-110">Ограничение использования</span><span class="sxs-lookup"><span data-stu-id="93356-110">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93356-111">Объект <strong>каталога</strong></span><span class="sxs-lookup"><span data-stu-id="93356-111"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="93356-112">Метод <strong>Create</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="93356-112">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93356-113">Коллекция <strong>таблиц</strong></span><span class="sxs-lookup"><span data-stu-id="93356-113"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="93356-114">Свойства чтения/записи до создания объекта и только для чтения — это при обращении существующий объект.</span><span class="sxs-lookup"><span data-stu-id="93356-114">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93356-115">Коллекции <strong>представлений</strong></span><span class="sxs-lookup"><span data-stu-id="93356-115"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="93356-116"><strong>Представления,</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="93356-116"><strong>Views</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93356-117"><strong>Процедуры</strong> семейства сайтов</span><span class="sxs-lookup"><span data-stu-id="93356-117"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="93356-118"><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="93356-118">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93356-119">Объект <strong>процедуры</strong></span><span class="sxs-lookup"><span data-stu-id="93356-119"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="93356-120">Свойство <strong>Command</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="93356-120">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93356-121">Коллекция <strong>ключей</strong></span><span class="sxs-lookup"><span data-stu-id="93356-121"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="93356-122"><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="93356-122">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93356-123"><strong>Пользователи</strong> семейства сайтов</span><span class="sxs-lookup"><span data-stu-id="93356-123"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="93356-124"><strong>Пользователи</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="93356-124"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93356-125">Семейства сайтов <strong>групп</strong></span><span class="sxs-lookup"><span data-stu-id="93356-125"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="93356-126"><strong>Группы</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="93356-126"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="93356-127">Поставщик Microsoft OLE DB для ODBC</span><span class="sxs-lookup"><span data-stu-id="93356-127">Microsoft OLE DB Provider for ODBC</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="93356-128">Объект или семейства сайтов</span><span class="sxs-lookup"><span data-stu-id="93356-128">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="93356-129">Ограничение использования</span><span class="sxs-lookup"><span data-stu-id="93356-129">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93356-130">Объект <strong>каталога</strong></span><span class="sxs-lookup"><span data-stu-id="93356-130"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="93356-131">Метод <strong>Create</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="93356-131">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93356-132">Коллекция <strong>таблиц</strong></span><span class="sxs-lookup"><span data-stu-id="93356-132"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="93356-133"><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="93356-133">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="93356-134">Свойства чтения/записи до создания объекта и только для чтения — это при обращении существующий объект.</span><span class="sxs-lookup"><span data-stu-id="93356-134">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93356-135"><strong>Процедуры</strong> семейства сайтов</span><span class="sxs-lookup"><span data-stu-id="93356-135"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="93356-136"><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="93356-136">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93356-137">Объект <strong>процедуры</strong></span><span class="sxs-lookup"><span data-stu-id="93356-137"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="93356-138">Свойство <strong>Command</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="93356-138">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93356-139">Коллекции <strong>индексов</strong></span><span class="sxs-lookup"><span data-stu-id="93356-139"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="93356-140"><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="93356-140">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93356-141">Коллекция <strong>ключей</strong></span><span class="sxs-lookup"><span data-stu-id="93356-141"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="93356-142"><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="93356-142">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93356-143"><strong>Пользователи</strong> семейства сайтов</span><span class="sxs-lookup"><span data-stu-id="93356-143"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="93356-144"><strong>Пользователи</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="93356-144"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93356-145">Семейства сайтов <strong>групп</strong></span><span class="sxs-lookup"><span data-stu-id="93356-145"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="93356-146"><strong>Группы</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="93356-146"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-oracle"></a><span data-ttu-id="93356-147">Поставщик Microsoft OLE DB для Oracle</span><span class="sxs-lookup"><span data-stu-id="93356-147">Microsoft OLE DB Provider for Oracle</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="93356-148">Объект или семейства сайтов</span><span class="sxs-lookup"><span data-stu-id="93356-148">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="93356-149">Ограничение использования</span><span class="sxs-lookup"><span data-stu-id="93356-149">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93356-150">Объект <strong>каталога</strong></span><span class="sxs-lookup"><span data-stu-id="93356-150"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="93356-151">Метод <strong>Create</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="93356-151">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93356-152">Коллекция <strong>таблиц</strong></span><span class="sxs-lookup"><span data-stu-id="93356-152"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="93356-153"><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="93356-153">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="93356-154">Свойства чтения/записи до создания объекта и только для чтения — это при обращении существующий объект.</span><span class="sxs-lookup"><span data-stu-id="93356-154">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93356-155">Коллекции <strong>представлений</strong></span><span class="sxs-lookup"><span data-stu-id="93356-155"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="93356-156"><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="93356-156">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93356-157"><strong>Просмотр</strong> объектов</span><span class="sxs-lookup"><span data-stu-id="93356-157"><strong>View</strong> object</span></span></p></td>
<td><p><span data-ttu-id="93356-158">Свойство <strong>Command</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="93356-158">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93356-159">Объект <strong>процедур</strong></span><span class="sxs-lookup"><span data-stu-id="93356-159"><strong>Procedures</strong> object</span></span></p></td>
<td><p><span data-ttu-id="93356-160"><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="93356-160">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93356-161">Объект <strong>процедуры</strong></span><span class="sxs-lookup"><span data-stu-id="93356-161"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="93356-162">Свойство <strong>Command</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="93356-162">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93356-163">Коллекции <strong>индексов</strong></span><span class="sxs-lookup"><span data-stu-id="93356-163"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="93356-164"><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="93356-164">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93356-165">Коллекция <strong>ключей</strong></span><span class="sxs-lookup"><span data-stu-id="93356-165"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="93356-166"><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="93356-166">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93356-167"><strong>Пользователи</strong> семейства сайтов</span><span class="sxs-lookup"><span data-stu-id="93356-167"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="93356-168"><strong>Пользователи</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="93356-168"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93356-169">Семейства сайтов <strong>групп</strong></span><span class="sxs-lookup"><span data-stu-id="93356-169"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="93356-170"><strong>Группы</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="93356-170"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>

