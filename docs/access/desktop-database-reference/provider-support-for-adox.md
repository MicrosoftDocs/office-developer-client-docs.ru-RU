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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301101"
---
# <a name="provider-support-for-adox"></a><span data-ttu-id="1e829-102">Поддержка поставщиков для ADOX</span><span class="sxs-lookup"><span data-stu-id="1e829-102">Provider support for ADOX</span></span>


<span data-ttu-id="1e829-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1e829-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1e829-104">Некоторые функции ADOX неподтверждются в зависимости от поставщика данных OLE DB.</span><span class="sxs-lookup"><span data-stu-id="1e829-104">Certain features of ADOX are unsupported, depending upon your OLE DB data provider.</span></span> <span data-ttu-id="1e829-105">ADOX полностью поддерживается с [поставщиком OLE DB для Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md).</span><span class="sxs-lookup"><span data-stu-id="1e829-105">ADOX is fully supported with the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md).</span></span> <span data-ttu-id="1e829-106">Неподтвержденные функции с поставщиком DB Microsoft OLE для [SQL Server,](microsoft-ole-db-provider-for-sql-server.md)поставщиком DB Microsoft OLE для [ODBC](microsoft-ole-db-provider-for-odbc.md)или поставщик OLE DB для Oracle (Майкрософт) ниже. [](microsoft-ole-db-provider-for-oracle.md)</span><span class="sxs-lookup"><span data-stu-id="1e829-106">The unsupported features with the [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), the [Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md), or the [Microsoft OLE DB Provider for Oracle](microsoft-ole-db-provider-for-oracle.md) are listed below.</span></span> <span data-ttu-id="1e829-107">ADOX не поддерживается другими поставщиками Microsoft OLE DB.</span><span class="sxs-lookup"><span data-stu-id="1e829-107">ADOX is not supported by any other Microsoft OLE DB providers.</span></span>

## <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="1e829-108">Поставщик Microsoft OLE DB для SQL Server</span><span class="sxs-lookup"><span data-stu-id="1e829-108">Microsoft OLE DB Provider for SQL Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1e829-109">Объект или коллекция</span><span class="sxs-lookup"><span data-stu-id="1e829-109">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="1e829-110">Ограничение использования</span><span class="sxs-lookup"><span data-stu-id="1e829-110">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e829-111"><strong>Объект Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-111"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="1e829-112">Метод <strong>Create</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1e829-112">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e829-113"><strong>Коллекция таблиц</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-113"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="1e829-114">Свойства читают или записывают перед созданием объектов и только при ссылке на существующий объект.</span><span class="sxs-lookup"><span data-stu-id="1e829-114">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e829-115"><strong>Коллекция представлений</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-115"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="1e829-116"><strong>Представления</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1e829-116"><strong>Views</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e829-117"><strong>Коллекция процедур</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-117"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="1e829-118">Методы <strong>приложения и</strong> <strong>удаления</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1e829-118">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e829-119"><strong>Объект Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-119"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="1e829-120">Свойство <strong>Command</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1e829-120">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e829-121"><strong>Коллекция ключей</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-121"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="1e829-122">Методы <strong>приложения и</strong> <strong>удаления</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1e829-122">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e829-123"><strong>Коллекция пользователей</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-123"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="1e829-124"><strong>Пользователи</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1e829-124"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e829-125"><strong>Коллекция групп</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-125"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="1e829-126"><strong>Группы</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1e829-126"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="1e829-127">Поставщик Microsoft OLE DB для ODBC</span><span class="sxs-lookup"><span data-stu-id="1e829-127">Microsoft OLE DB Provider for ODBC</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1e829-128">Объект или коллекция</span><span class="sxs-lookup"><span data-stu-id="1e829-128">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="1e829-129">Ограничение использования</span><span class="sxs-lookup"><span data-stu-id="1e829-129">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e829-130"><strong>Объект Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-130"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="1e829-131">Метод <strong>Create</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1e829-131">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e829-132"><strong>Коллекция таблиц</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-132"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="1e829-133">Методы <strong>приложения и</strong> <strong>удаления</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1e829-133">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="1e829-134">Свойства читают или записывают перед созданием объектов и только при ссылке на существующий объект.</span><span class="sxs-lookup"><span data-stu-id="1e829-134">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e829-135"><strong>Коллекция процедур</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-135"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="1e829-136">Методы <strong>приложения и</strong> <strong>удаления</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1e829-136">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e829-137"><strong>Объект Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-137"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="1e829-138">Свойство <strong>Command</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1e829-138">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e829-139"><strong>Коллекция индексов</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-139"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="1e829-140">Методы <strong>приложения и</strong> <strong>удаления</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1e829-140">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e829-141"><strong>Коллекция ключей</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-141"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="1e829-142">Методы <strong>приложения и</strong> <strong>удаления</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1e829-142">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e829-143"><strong>Коллекция пользователей</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-143"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="1e829-144"><strong>Пользователи</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1e829-144"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e829-145"><strong>Коллекция групп</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-145"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="1e829-146"><strong>Группы</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1e829-146"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-oracle"></a><span data-ttu-id="1e829-147">Поставщик Microsoft OLE DB для Oracle</span><span class="sxs-lookup"><span data-stu-id="1e829-147">Microsoft OLE DB Provider for Oracle</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1e829-148">Объект или коллекция</span><span class="sxs-lookup"><span data-stu-id="1e829-148">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="1e829-149">Ограничение использования</span><span class="sxs-lookup"><span data-stu-id="1e829-149">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e829-150"><strong>Объект Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-150"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="1e829-151">Метод <strong>Create</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1e829-151">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e829-152"><strong>Коллекция таблиц</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-152"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="1e829-153">Методы <strong>приложения и</strong> <strong>удаления</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1e829-153">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="1e829-154">Свойства читают или записывают перед созданием объектов и только при ссылке на существующий объект.</span><span class="sxs-lookup"><span data-stu-id="1e829-154">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e829-155"><strong>Коллекция представлений</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-155"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="1e829-156">Методы <strong>приложения и</strong> <strong>удаления</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1e829-156">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e829-157"><strong>Просмотр</strong> объекта</span><span class="sxs-lookup"><span data-stu-id="1e829-157"><strong>View</strong> object</span></span></p></td>
<td><p><span data-ttu-id="1e829-158">Свойство <strong>Command</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1e829-158">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e829-159"><strong>Объект Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-159"><strong>Procedures</strong> object</span></span></p></td>
<td><p><span data-ttu-id="1e829-160">Методы <strong>приложения и</strong> <strong>удаления</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1e829-160">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e829-161"><strong>Объект Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-161"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="1e829-162">Свойство <strong>Command</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1e829-162">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e829-163"><strong>Коллекция индексов</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-163"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="1e829-164">Методы <strong>приложения и</strong> <strong>удаления</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1e829-164">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e829-165"><strong>Коллекция ключей</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-165"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="1e829-166">Методы <strong>приложения и</strong> <strong>удаления</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1e829-166">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e829-167"><strong>Коллекция пользователей</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-167"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="1e829-168"><strong>Пользователи</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1e829-168"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e829-169"><strong>Коллекция групп</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-169"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="1e829-170"><strong>Группы</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="1e829-170"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>

