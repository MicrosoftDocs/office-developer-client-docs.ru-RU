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
# <a name="provider-support-for-adox"></a><span data-ttu-id="26fdc-102">Поддержка поставщиков для ADOX</span><span class="sxs-lookup"><span data-stu-id="26fdc-102">Provider support for ADOX</span></span>


<span data-ttu-id="26fdc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="26fdc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="26fdc-104">Некоторые функции ADOX не поддерживаются в зависимости от поставщика данных OLE DB.</span><span class="sxs-lookup"><span data-stu-id="26fdc-104">Certain features of ADOX are unsupported, depending upon your OLE DB data provider.</span></span> <span data-ttu-id="26fdc-105">ADOX полностью поддерживается [поставщиком OLE DB для Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md).</span><span class="sxs-lookup"><span data-stu-id="26fdc-105">ADOX is fully supported with the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md).</span></span> <span data-ttu-id="26fdc-106">Ниже перечислены неподдерживаемые возможности [поставщика Microsoft OLE DB для SQL Server](microsoft-ole-db-provider-for-sql-server.md), [поставщика Microsoft OLE DB для ODBC](microsoft-ole-db-provider-for-odbc.md)или [поставщика Microsoft OLE DB для Oracle](microsoft-ole-db-provider-for-oracle.md) .</span><span class="sxs-lookup"><span data-stu-id="26fdc-106">The unsupported features with the [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), the [Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md), or the [Microsoft OLE DB Provider for Oracle](microsoft-ole-db-provider-for-oracle.md) are listed below.</span></span> <span data-ttu-id="26fdc-107">ADOX не поддерживается какими-либо другими поставщиками Microsoft OLE DB.</span><span class="sxs-lookup"><span data-stu-id="26fdc-107">ADOX is not supported by any other Microsoft OLE DB providers.</span></span>

## <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="26fdc-108">Поставщик Microsoft OLE DB для SQL Server</span><span class="sxs-lookup"><span data-stu-id="26fdc-108">Microsoft OLE DB Provider for SQL Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="26fdc-109">Объект или коллекция</span><span class="sxs-lookup"><span data-stu-id="26fdc-109">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="26fdc-110">Ограничение использования</span><span class="sxs-lookup"><span data-stu-id="26fdc-110">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26fdc-111">Объект <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="26fdc-111"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="26fdc-112">Метод <strong>CREATE</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="26fdc-112">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26fdc-113"><strong></strong> Коллекция Tables</span><span class="sxs-lookup"><span data-stu-id="26fdc-113"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="26fdc-114">Свойства доступны для чтения и записи перед созданием объекта и доступны только для чтения при обращении к существующему объекту.</span><span class="sxs-lookup"><span data-stu-id="26fdc-114">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26fdc-115"><strong></strong> Коллекция views</span><span class="sxs-lookup"><span data-stu-id="26fdc-115"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="26fdc-116"><strong>Представления</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="26fdc-116"><strong>Views</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26fdc-117">Коллекция <strong>процедур</strong></span><span class="sxs-lookup"><span data-stu-id="26fdc-117"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="26fdc-118">Методы <strong>append</strong> и <strong>Delete</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="26fdc-118">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26fdc-119">Объект <strong>PROCEDURE</strong></span><span class="sxs-lookup"><span data-stu-id="26fdc-119"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="26fdc-120">Свойство <strong>Command</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="26fdc-120">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26fdc-121">Коллекция <strong>Keys</strong></span><span class="sxs-lookup"><span data-stu-id="26fdc-121"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="26fdc-122">Методы <strong>append</strong> и <strong>Delete</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="26fdc-122">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26fdc-123"><strong></strong> Коллекция Users</span><span class="sxs-lookup"><span data-stu-id="26fdc-123"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="26fdc-124"><strong>Пользователи</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="26fdc-124"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26fdc-125">Коллекция <strong>Groups</strong></span><span class="sxs-lookup"><span data-stu-id="26fdc-125"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="26fdc-126"><strong>Группы</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="26fdc-126"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="26fdc-127">Поставщик Microsoft OLE DB для ODBC</span><span class="sxs-lookup"><span data-stu-id="26fdc-127">Microsoft OLE DB Provider for ODBC</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="26fdc-128">Объект или коллекция</span><span class="sxs-lookup"><span data-stu-id="26fdc-128">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="26fdc-129">Ограничение использования</span><span class="sxs-lookup"><span data-stu-id="26fdc-129">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26fdc-130">Объект <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="26fdc-130"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="26fdc-131">Метод <strong>CREATE</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="26fdc-131">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26fdc-132"><strong></strong> Коллекция Tables</span><span class="sxs-lookup"><span data-stu-id="26fdc-132"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="26fdc-133">Методы <strong>append</strong> и <strong>Delete</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="26fdc-133">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="26fdc-134">Свойства доступны для чтения и записи перед созданием объекта и доступны только для чтения при обращении к существующему объекту.</span><span class="sxs-lookup"><span data-stu-id="26fdc-134">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26fdc-135">Коллекция <strong>процедур</strong></span><span class="sxs-lookup"><span data-stu-id="26fdc-135"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="26fdc-136">Методы <strong>append</strong> и <strong>Delete</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="26fdc-136">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26fdc-137">Объект <strong>PROCEDURE</strong></span><span class="sxs-lookup"><span data-stu-id="26fdc-137"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="26fdc-138">Свойство <strong>Command</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="26fdc-138">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26fdc-139">Коллекция <strong>indexes</strong></span><span class="sxs-lookup"><span data-stu-id="26fdc-139"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="26fdc-140">Методы <strong>append</strong> и <strong>Delete</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="26fdc-140">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26fdc-141">Коллекция <strong>Keys</strong></span><span class="sxs-lookup"><span data-stu-id="26fdc-141"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="26fdc-142">Методы <strong>append</strong> и <strong>Delete</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="26fdc-142">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26fdc-143"><strong></strong> Коллекция Users</span><span class="sxs-lookup"><span data-stu-id="26fdc-143"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="26fdc-144"><strong>Пользователи</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="26fdc-144"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26fdc-145">Коллекция <strong>Groups</strong></span><span class="sxs-lookup"><span data-stu-id="26fdc-145"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="26fdc-146"><strong>Группы</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="26fdc-146"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-oracle"></a><span data-ttu-id="26fdc-147">Поставщик Microsoft OLE DB для Oracle</span><span class="sxs-lookup"><span data-stu-id="26fdc-147">Microsoft OLE DB Provider for Oracle</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="26fdc-148">Объект или коллекция</span><span class="sxs-lookup"><span data-stu-id="26fdc-148">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="26fdc-149">Ограничение использования</span><span class="sxs-lookup"><span data-stu-id="26fdc-149">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26fdc-150">Объект <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="26fdc-150"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="26fdc-151">Метод <strong>CREATE</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="26fdc-151">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26fdc-152"><strong></strong> Коллекция Tables</span><span class="sxs-lookup"><span data-stu-id="26fdc-152"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="26fdc-153">Методы <strong>append</strong> и <strong>Delete</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="26fdc-153">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="26fdc-154">Свойства доступны для чтения и записи перед созданием объекта и доступны только для чтения при обращении к существующему объекту.</span><span class="sxs-lookup"><span data-stu-id="26fdc-154">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26fdc-155"><strong></strong> Коллекция views</span><span class="sxs-lookup"><span data-stu-id="26fdc-155"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="26fdc-156">Методы <strong>append</strong> и <strong>Delete</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="26fdc-156">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26fdc-157">Объект <strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="26fdc-157"><strong>View</strong> object</span></span></p></td>
<td><p><span data-ttu-id="26fdc-158">Свойство <strong>Command</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="26fdc-158">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26fdc-159">Объект <strong>процедур</strong></span><span class="sxs-lookup"><span data-stu-id="26fdc-159"><strong>Procedures</strong> object</span></span></p></td>
<td><p><span data-ttu-id="26fdc-160">Методы <strong>append</strong> и <strong>Delete</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="26fdc-160">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26fdc-161">Объект <strong>PROCEDURE</strong></span><span class="sxs-lookup"><span data-stu-id="26fdc-161"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="26fdc-162">Свойство <strong>Command</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="26fdc-162">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26fdc-163">Коллекция <strong>indexes</strong></span><span class="sxs-lookup"><span data-stu-id="26fdc-163"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="26fdc-164">Методы <strong>append</strong> и <strong>Delete</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="26fdc-164">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26fdc-165">Коллекция <strong>Keys</strong></span><span class="sxs-lookup"><span data-stu-id="26fdc-165"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="26fdc-166">Методы <strong>append</strong> и <strong>Delete</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="26fdc-166">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26fdc-167"><strong></strong> Коллекция Users</span><span class="sxs-lookup"><span data-stu-id="26fdc-167"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="26fdc-168"><strong>Пользователи</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="26fdc-168"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26fdc-169">Коллекция <strong>Groups</strong></span><span class="sxs-lookup"><span data-stu-id="26fdc-169"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="26fdc-170"><strong>Группы</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="26fdc-170"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>

