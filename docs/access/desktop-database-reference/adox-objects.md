---
title: Объекты ADOX (Справочник по базам данных Access на компьютере)
TOCTitle: ADOX objects
ms:assetid: d7db1aed-251b-888b-bc44-f61caeeac403
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250087(v=office.15)
ms:contentKeyID: 48548018
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d5051a9842645ac8f93be26bf6309dd05da7ec24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280303"
---
# <a name="adox-objects"></a><span data-ttu-id="9e8ac-102">Объекты ADOX</span><span class="sxs-lookup"><span data-stu-id="9e8ac-102">ADOX objects</span></span>

<span data-ttu-id="9e8ac-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e8ac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9e8ac-104">Каждый объект может содержаться в соответствующей коллекции.</span><span class="sxs-lookup"><span data-stu-id="9e8ac-104">Each object can be contained in its corresponding collection.</span></span> <span data-ttu-id="9e8ac-105">Например, объект **Table** может содержаться в коллекции [Tables](tables-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="9e8ac-105">For example, a **Table** object can be contained in a [Tables](tables-collection-adox.md) collection.</span></span> <span data-ttu-id="9e8ac-106">Дополнительные сведения можно найти в статье [Collections ADOX Collections](adox-collections.md) or of a specific Collection.</span><span class="sxs-lookup"><span data-stu-id="9e8ac-106">For more information, see [ADOX collections](adox-collections.md) or a specific collection topic.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9e8ac-107">Объект</span><span class="sxs-lookup"><span data-stu-id="9e8ac-107">Object</span></span></p></th>
<th><p><span data-ttu-id="9e8ac-108">Описание</span><span class="sxs-lookup"><span data-stu-id="9e8ac-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e8ac-109"><a href="catalog-object-adox.md">Каталог</a></span><span class="sxs-lookup"><span data-stu-id="9e8ac-109"><a href="catalog-object-adox.md">Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="9e8ac-110">Содержит коллекции, описывающие каталог схем источника данных.</span><span class="sxs-lookup"><span data-stu-id="9e8ac-110">Contains collections that describe the schema catalog of a data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e8ac-111"><a href="column-object-adox.md">Столбец</a></span><span class="sxs-lookup"><span data-stu-id="9e8ac-111"><a href="column-object-adox.md">Column</a></span></span></p></td>
<td><p><span data-ttu-id="9e8ac-112">Представляет столбец из таблицы, индекса или ключа.</span><span class="sxs-lookup"><span data-stu-id="9e8ac-112">Represents a column from a table, index, or key.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e8ac-113"><a href="group-object-adox.md">group</a></span><span class="sxs-lookup"><span data-stu-id="9e8ac-113"><a href="group-object-adox.md">Group</a></span></span></p></td>
<td><p><span data-ttu-id="9e8ac-114">Представляет учетную запись группы, имеющую разрешения на доступ в защищенной базе данных.</span><span class="sxs-lookup"><span data-stu-id="9e8ac-114">Represents a group account that has access permissions within a secured database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e8ac-115"><a href="index-object-adox.md">Индекс</a></span><span class="sxs-lookup"><span data-stu-id="9e8ac-115"><a href="index-object-adox.md">Index</a></span></span></p></td>
<td><p><span data-ttu-id="9e8ac-116">Представляет индекс из таблицы базы данных.</span><span class="sxs-lookup"><span data-stu-id="9e8ac-116">Represents an index from a database table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e8ac-117"><a href="key-object-adox.md">Key</a></span><span class="sxs-lookup"><span data-stu-id="9e8ac-117"><a href="key-object-adox.md">Key</a></span></span></p></td>
<td><p><span data-ttu-id="9e8ac-118">Представляет первичное, внешнее или уникальное ключевое поле из таблицы базы данных.</span><span class="sxs-lookup"><span data-stu-id="9e8ac-118">Represents a primary, foreign, or unique key field from a database table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e8ac-119"><a href="procedure-object-adox.md">Процедура</a></span><span class="sxs-lookup"><span data-stu-id="9e8ac-119"><a href="procedure-object-adox.md">Procedure</a></span></span></p></td>
<td><p><span data-ttu-id="9e8ac-120">Представляет хранимую процедуру.</span><span class="sxs-lookup"><span data-stu-id="9e8ac-120">Represents a stored procedure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e8ac-121"><a href="table-object-adox.md">Table</a></span><span class="sxs-lookup"><span data-stu-id="9e8ac-121"><a href="table-object-adox.md">Table</a></span></span></p></td>
<td><p><span data-ttu-id="9e8ac-122">Представляет таблицу базы данных, включая столбцы, индексы и ключи.</span><span class="sxs-lookup"><span data-stu-id="9e8ac-122">Represents a database table, including columns, indexes, and keys.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e8ac-123"><a href="user-object-adox.md">User</a></span><span class="sxs-lookup"><span data-stu-id="9e8ac-123"><a href="user-object-adox.md">User</a></span></span></p></td>
<td><p><span data-ttu-id="9e8ac-124">Представляет учетную запись пользователя, имеющую разрешения на доступ в защищенной базе данных.</span><span class="sxs-lookup"><span data-stu-id="9e8ac-124">Represents a user account that has access permissions within a secured database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e8ac-125"><a href="view-object-adox.md">Просмотр</a></span><span class="sxs-lookup"><span data-stu-id="9e8ac-125"><a href="view-object-adox.md">View</a></span></span></p></td>
<td><p><span data-ttu-id="9e8ac-126">Представляет отфильтрованный набор записей или виртуальную таблицу.</span><span class="sxs-lookup"><span data-stu-id="9e8ac-126">Represents a filtered set of records or a virtual table.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>



