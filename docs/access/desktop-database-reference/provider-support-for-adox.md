---
title: Поддержка ADOX
TOCTitle: Provider support for ADOX
ms:assetid: 32ea3236-d69f-df94-1685-d8791aeb9e0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249100(v=office.15)
ms:contentKeyID: 48544091
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bdd9ca9a2274f03f1592f73c3da5a6837101fda2
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947828"
---
# <a name="provider-support-for-adox"></a><span data-ttu-id="fc07e-102">Поддержка ADOX</span><span class="sxs-lookup"><span data-stu-id="fc07e-102">Provider support for ADOX</span></span>


<span data-ttu-id="fc07e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc07e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fc07e-104">Некоторые возможности ADOX не поддерживаются, в зависимости от поставщика данных OLE DB.</span><span class="sxs-lookup"><span data-stu-id="fc07e-104">Certain features of ADOX are unsupported, depending upon your OLE DB data provider.</span></span> <span data-ttu-id="fc07e-105">ADOX полностью поддерживаются с помощью [Поставщика OLE DB для Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md).</span><span class="sxs-lookup"><span data-stu-id="fc07e-105">ADOX is fully supported with the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md).</span></span> <span data-ttu-id="fc07e-106">Неподдерживаемые функции с помощью [Поставщик Microsoft OLE DB для SQL Server](microsoft-ole-db-provider-for-sql-server.md), [Поставщик Microsoft OLE DB для ODBC](microsoft-ole-db-provider-for-odbc.md)или [Поставщик Microsoft OLE DB для Oracle](microsoft-ole-db-provider-for-oracle.md) , перечислены ниже.</span><span class="sxs-lookup"><span data-stu-id="fc07e-106">The unsupported features with the [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), the [Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md), or the [Microsoft OLE DB Provider for Oracle](microsoft-ole-db-provider-for-oracle.md) are listed below.</span></span> <span data-ttu-id="fc07e-107">Другие поставщики OLE DB для Microsoft ADOX не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc07e-107">ADOX is not supported by any other Microsoft OLE DB providers.</span></span>

## <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="fc07e-108">Поставщик Microsoft OLE DB для SQL Server</span><span class="sxs-lookup"><span data-stu-id="fc07e-108">Microsoft OLE DB Provider for SQL Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc07e-109">Объект или семейства сайтов</span><span class="sxs-lookup"><span data-stu-id="fc07e-109">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="fc07e-110">Ограничение использования</span><span class="sxs-lookup"><span data-stu-id="fc07e-110">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc07e-111">Объект <strong>каталога</strong></span><span class="sxs-lookup"><span data-stu-id="fc07e-111"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="fc07e-112">Метод <strong>Create</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc07e-112">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc07e-113">Коллекция <strong>таблиц</strong></span><span class="sxs-lookup"><span data-stu-id="fc07e-113"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="fc07e-114">Свойства чтения/записи до создания объекта и только для чтения — это при обращении существующий объект.</span><span class="sxs-lookup"><span data-stu-id="fc07e-114">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc07e-115">Коллекции <strong>представлений</strong></span><span class="sxs-lookup"><span data-stu-id="fc07e-115"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="fc07e-116"><strong>Представления,</strong> не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="fc07e-116"><strong>Views</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc07e-117"><strong>Процедуры</strong> семейства сайтов</span><span class="sxs-lookup"><span data-stu-id="fc07e-117"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="fc07e-118"><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="fc07e-118">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc07e-119">Объект <strong>процедуры</strong></span><span class="sxs-lookup"><span data-stu-id="fc07e-119"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="fc07e-120">Свойство <strong>Command</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc07e-120">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc07e-121">Коллекция <strong>ключей</strong></span><span class="sxs-lookup"><span data-stu-id="fc07e-121"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="fc07e-122"><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="fc07e-122">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc07e-123"><strong>Пользователи</strong> семейства сайтов</span><span class="sxs-lookup"><span data-stu-id="fc07e-123"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="fc07e-124"><strong>Пользователи</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc07e-124"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc07e-125">Семейства сайтов <strong>групп</strong></span><span class="sxs-lookup"><span data-stu-id="fc07e-125"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="fc07e-126"><strong>Группы</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc07e-126"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="fc07e-127">Поставщик Microsoft OLE DB для ODBC</span><span class="sxs-lookup"><span data-stu-id="fc07e-127">Microsoft OLE DB Provider for ODBC</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc07e-128">Объект или семейства сайтов</span><span class="sxs-lookup"><span data-stu-id="fc07e-128">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="fc07e-129">Ограничение использования</span><span class="sxs-lookup"><span data-stu-id="fc07e-129">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc07e-130">Объект <strong>каталога</strong></span><span class="sxs-lookup"><span data-stu-id="fc07e-130"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="fc07e-131">Метод <strong>Create</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc07e-131">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc07e-132">Коллекция <strong>таблиц</strong></span><span class="sxs-lookup"><span data-stu-id="fc07e-132"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="fc07e-133"><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="fc07e-133">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="fc07e-134">Свойства чтения/записи до создания объекта и только для чтения — это при обращении существующий объект.</span><span class="sxs-lookup"><span data-stu-id="fc07e-134">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc07e-135"><strong>Процедуры</strong> семейства сайтов</span><span class="sxs-lookup"><span data-stu-id="fc07e-135"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="fc07e-136"><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="fc07e-136">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc07e-137">Объект <strong>процедуры</strong></span><span class="sxs-lookup"><span data-stu-id="fc07e-137"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="fc07e-138">Свойство <strong>Command</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc07e-138">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc07e-139">Коллекции <strong>индексов</strong></span><span class="sxs-lookup"><span data-stu-id="fc07e-139"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="fc07e-140"><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="fc07e-140">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc07e-141">Коллекция <strong>ключей</strong></span><span class="sxs-lookup"><span data-stu-id="fc07e-141"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="fc07e-142"><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="fc07e-142">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc07e-143"><strong>Пользователи</strong> семейства сайтов</span><span class="sxs-lookup"><span data-stu-id="fc07e-143"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="fc07e-144"><strong>Пользователи</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc07e-144"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc07e-145">Семейства сайтов <strong>групп</strong></span><span class="sxs-lookup"><span data-stu-id="fc07e-145"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="fc07e-146"><strong>Группы</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc07e-146"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-oracle"></a><span data-ttu-id="fc07e-147">Поставщик Microsoft OLE DB для Oracle</span><span class="sxs-lookup"><span data-stu-id="fc07e-147">Microsoft OLE DB Provider for Oracle</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc07e-148">Объект или семейства сайтов</span><span class="sxs-lookup"><span data-stu-id="fc07e-148">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="fc07e-149">Ограничение использования</span><span class="sxs-lookup"><span data-stu-id="fc07e-149">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc07e-150">Объект <strong>каталога</strong></span><span class="sxs-lookup"><span data-stu-id="fc07e-150"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="fc07e-151">Метод <strong>Create</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc07e-151">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc07e-152">Коллекция <strong>таблиц</strong></span><span class="sxs-lookup"><span data-stu-id="fc07e-152"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="fc07e-153"><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="fc07e-153">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="fc07e-154">Свойства чтения/записи до создания объекта и только для чтения — это при обращении существующий объект.</span><span class="sxs-lookup"><span data-stu-id="fc07e-154">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc07e-155">Коллекции <strong>представлений</strong></span><span class="sxs-lookup"><span data-stu-id="fc07e-155"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="fc07e-156"><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="fc07e-156">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc07e-157"><strong>Просмотр</strong> объектов</span><span class="sxs-lookup"><span data-stu-id="fc07e-157"><strong>View</strong> object</span></span></p></td>
<td><p><span data-ttu-id="fc07e-158">Свойство <strong>Command</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc07e-158">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc07e-159">Объект <strong>процедур</strong></span><span class="sxs-lookup"><span data-stu-id="fc07e-159"><strong>Procedures</strong> object</span></span></p></td>
<td><p><span data-ttu-id="fc07e-160"><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="fc07e-160">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc07e-161">Объект <strong>процедуры</strong></span><span class="sxs-lookup"><span data-stu-id="fc07e-161"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="fc07e-162">Свойство <strong>Command</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc07e-162">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc07e-163">Коллекции <strong>индексов</strong></span><span class="sxs-lookup"><span data-stu-id="fc07e-163"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="fc07e-164"><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="fc07e-164">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc07e-165">Коллекция <strong>ключей</strong></span><span class="sxs-lookup"><span data-stu-id="fc07e-165"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="fc07e-166"><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="fc07e-166">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc07e-167"><strong>Пользователи</strong> семейства сайтов</span><span class="sxs-lookup"><span data-stu-id="fc07e-167"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="fc07e-168"><strong>Пользователи</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc07e-168"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc07e-169">Семейства сайтов <strong>групп</strong></span><span class="sxs-lookup"><span data-stu-id="fc07e-169"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="fc07e-170"><strong>Группы</strong> не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fc07e-170"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>

