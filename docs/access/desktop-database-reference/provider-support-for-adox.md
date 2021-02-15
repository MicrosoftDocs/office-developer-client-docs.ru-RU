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
# <a name="provider-support-for-adox"></a><span data-ttu-id="95445-102">Поддержка поставщиков для ADOX</span><span class="sxs-lookup"><span data-stu-id="95445-102">Provider support for ADOX</span></span>


<span data-ttu-id="95445-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="95445-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="95445-104">Некоторые функции ADOX неподтверчены в зависимости от поставщика данных OLE DB.</span><span class="sxs-lookup"><span data-stu-id="95445-104">Certain features of ADOX are unsupported, depending upon your OLE DB data provider.</span></span> <span data-ttu-id="95445-105">ADOX полностью поддерживается поставщиком [OLE DB для Microsoft Jet.](microsoft-ole-db-provider-for-microsoft-jet.md)</span><span class="sxs-lookup"><span data-stu-id="95445-105">ADOX is fully supported with the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md).</span></span> <span data-ttu-id="95445-106">Ниже перечислены неподтверченные функции поставщика [Microsoft OLE DB](microsoft-ole-db-provider-for-sql-server.md)для SQL Server, поставщика [Microsoft OLE DB для ODBC](microsoft-ole-db-provider-for-odbc.md)или поставщика Microsoft [OLE DB для Oracle.](microsoft-ole-db-provider-for-oracle.md)</span><span class="sxs-lookup"><span data-stu-id="95445-106">The unsupported features with the [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), the [Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md), or the [Microsoft OLE DB Provider for Oracle](microsoft-ole-db-provider-for-oracle.md) are listed below.</span></span> <span data-ttu-id="95445-107">ADOX не поддерживается другими поставщиками Microsoft OLE DB.</span><span class="sxs-lookup"><span data-stu-id="95445-107">ADOX is not supported by any other Microsoft OLE DB providers.</span></span>

## <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="95445-108">Поставщик Microsoft OLE DB для SQL Server</span><span class="sxs-lookup"><span data-stu-id="95445-108">Microsoft OLE DB Provider for SQL Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95445-109">Объект или коллекция</span><span class="sxs-lookup"><span data-stu-id="95445-109">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="95445-110">Ограничение использования</span><span class="sxs-lookup"><span data-stu-id="95445-110">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95445-111"><strong>Объект Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="95445-111"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="95445-112">Метод <strong>Create</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="95445-112">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95445-113"><strong>Коллекция Tables</strong></span><span class="sxs-lookup"><span data-stu-id="95445-113"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="95445-114">Свойства считывать и записывать до создания объекта и только для чтения при ссылке на существующий объект.</span><span class="sxs-lookup"><span data-stu-id="95445-114">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95445-115"><strong>Коллекция Views</strong></span><span class="sxs-lookup"><span data-stu-id="95445-115"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="95445-116"><strong>Представления</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="95445-116"><strong>Views</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95445-117"><strong>Коллекция Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="95445-117"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="95445-118">Методы <strong>Append</strong> и <strong>Delete</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="95445-118">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95445-119"><strong>Объект Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="95445-119"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="95445-120">Свойство <strong>Command</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="95445-120">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95445-121"><strong>Коллекция Keys</strong></span><span class="sxs-lookup"><span data-stu-id="95445-121"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="95445-122">Методы <strong>Append</strong> и <strong>Delete</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="95445-122">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95445-123"><strong>Коллекция Users</strong></span><span class="sxs-lookup"><span data-stu-id="95445-123"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="95445-124"><strong>Пользователи</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="95445-124"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95445-125"><strong>Коллекция Groups</strong></span><span class="sxs-lookup"><span data-stu-id="95445-125"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="95445-126"><strong>Группы</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="95445-126"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="95445-127">Поставщик Microsoft OLE DB для ODBC</span><span class="sxs-lookup"><span data-stu-id="95445-127">Microsoft OLE DB Provider for ODBC</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95445-128">Объект или коллекция</span><span class="sxs-lookup"><span data-stu-id="95445-128">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="95445-129">Ограничение использования</span><span class="sxs-lookup"><span data-stu-id="95445-129">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95445-130"><strong>Объект Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="95445-130"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="95445-131">Метод <strong>Create</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="95445-131">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95445-132"><strong>Коллекция Tables</strong></span><span class="sxs-lookup"><span data-stu-id="95445-132"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="95445-133">Методы <strong>Append</strong> и <strong>Delete</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="95445-133">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="95445-134">Свойства считывать и записывать до создания объекта и только для чтения при ссылке на существующий объект.</span><span class="sxs-lookup"><span data-stu-id="95445-134">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95445-135"><strong>Коллекция Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="95445-135"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="95445-136">Методы <strong>Append</strong> и <strong>Delete</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="95445-136">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95445-137"><strong>Объект Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="95445-137"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="95445-138">Свойство <strong>Command</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="95445-138">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95445-139"><strong>Коллекция Indexes</strong></span><span class="sxs-lookup"><span data-stu-id="95445-139"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="95445-140">Методы <strong>Append</strong> и <strong>Delete</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="95445-140">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95445-141"><strong>Коллекция Keys</strong></span><span class="sxs-lookup"><span data-stu-id="95445-141"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="95445-142">Методы <strong>Append</strong> и <strong>Delete</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="95445-142">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95445-143"><strong>Коллекция Users</strong></span><span class="sxs-lookup"><span data-stu-id="95445-143"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="95445-144"><strong>Пользователи</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="95445-144"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95445-145"><strong>Коллекция Groups</strong></span><span class="sxs-lookup"><span data-stu-id="95445-145"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="95445-146"><strong>Группы</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="95445-146"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-oracle"></a><span data-ttu-id="95445-147">Поставщик Microsoft OLE DB для Oracle</span><span class="sxs-lookup"><span data-stu-id="95445-147">Microsoft OLE DB Provider for Oracle</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95445-148">Объект или коллекция</span><span class="sxs-lookup"><span data-stu-id="95445-148">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="95445-149">Ограничение использования</span><span class="sxs-lookup"><span data-stu-id="95445-149">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95445-150"><strong>Объект Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="95445-150"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="95445-151">Метод <strong>Create</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="95445-151">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95445-152"><strong>Коллекция Tables</strong></span><span class="sxs-lookup"><span data-stu-id="95445-152"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="95445-153">Методы <strong>Append</strong> и <strong>Delete</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="95445-153">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="95445-154">Свойства считывать и записывать до создания объекта и только для чтения при ссылке на существующий объект.</span><span class="sxs-lookup"><span data-stu-id="95445-154">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95445-155"><strong>Коллекция Views</strong></span><span class="sxs-lookup"><span data-stu-id="95445-155"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="95445-156">Методы <strong>Append</strong> и <strong>Delete</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="95445-156">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95445-157"><strong>Объект View</strong></span><span class="sxs-lookup"><span data-stu-id="95445-157"><strong>View</strong> object</span></span></p></td>
<td><p><span data-ttu-id="95445-158">Свойство <strong>Command</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="95445-158">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95445-159"><strong>Объект Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="95445-159"><strong>Procedures</strong> object</span></span></p></td>
<td><p><span data-ttu-id="95445-160">Методы <strong>Append</strong> и <strong>Delete</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="95445-160">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95445-161"><strong>Объект Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="95445-161"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="95445-162">Свойство <strong>Command</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="95445-162">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95445-163"><strong>Коллекция Indexes</strong></span><span class="sxs-lookup"><span data-stu-id="95445-163"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="95445-164">Методы <strong>Append</strong> и <strong>Delete</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="95445-164">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95445-165"><strong>Коллекция Keys</strong></span><span class="sxs-lookup"><span data-stu-id="95445-165"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="95445-166">Методы <strong>Append</strong> и <strong>Delete</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="95445-166">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95445-167"><strong>Коллекция Users</strong></span><span class="sxs-lookup"><span data-stu-id="95445-167"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="95445-168"><strong>Пользователи</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="95445-168"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95445-169"><strong>Коллекция Groups</strong></span><span class="sxs-lookup"><span data-stu-id="95445-169"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="95445-170"><strong>Группы</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="95445-170"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>

