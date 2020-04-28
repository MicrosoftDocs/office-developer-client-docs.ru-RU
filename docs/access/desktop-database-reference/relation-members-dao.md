---
title: Элементы отношений (DAO)
TOCTitle: Relation Members
ms:assetid: 9ee36e7d-3825-1de8-65fb-64bbcada847c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198338(v=office.15)
ms:contentKeyID: 48546670
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84e18afe4a11e53d68397efad71ac6136c779143
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307039"
---
# <a name="relation-members-dao"></a><span data-ttu-id="17fab-102">Элементы отношений (DAO)</span><span class="sxs-lookup"><span data-stu-id="17fab-102">Relation members (DAO)</span></span>


<span data-ttu-id="17fab-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="17fab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="17fab-104">Объект relation представляет связь между полями в таблицах или запросах (только базы данных ядра СУБД Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="17fab-104">A Relation object represents a relationship between fields in tables or queries (Microsoft Access database engine databases only).</span></span>

## <a name="methods"></a><span data-ttu-id="17fab-105">Методы</span><span class="sxs-lookup"><span data-stu-id="17fab-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="17fab-106">Имя</span><span class="sxs-lookup"><span data-stu-id="17fab-106">Name</span></span></p></th>
<th><p><span data-ttu-id="17fab-107">Описание</span><span class="sxs-lookup"><span data-stu-id="17fab-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17fab-108"><strong><a href="relation-createfield-method-dao.md">CreateField</a></strong></span><span class="sxs-lookup"><span data-stu-id="17fab-108"><strong><a href="relation-createfield-method-dao.md">CreateField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="17fab-109">Создает новый объект <strong><a href="field-object-dao.md">Field</a></strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="17fab-109">Creates a new <strong><a href="field-object-dao.md">Field</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="17fab-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="17fab-110">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="17fab-111">Имя</span><span class="sxs-lookup"><span data-stu-id="17fab-111">Name</span></span></p></th>
<th><p><span data-ttu-id="17fab-112">Описание</span><span class="sxs-lookup"><span data-stu-id="17fab-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17fab-113"><strong><a href="relation-attributes-property-dao.md">Attributes</a></strong></span><span class="sxs-lookup"><span data-stu-id="17fab-113"><strong><a href="relation-attributes-property-dao.md">Attributes</a></strong></span></span></p></td>
<td><p><span data-ttu-id="17fab-114">Задает или возвращает значение, которое указывает одну или несколько характеристик объекта <strong>связи</strong> .</span><span class="sxs-lookup"><span data-stu-id="17fab-114">Sets or returns a value that indicates one or more characteristics of a <strong>Relation</strong> object.</span></span> <span data-ttu-id="17fab-115">Для чтения и записи, <strong>Long</strong>.</span><span class="sxs-lookup"><span data-stu-id="17fab-115">Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17fab-116"><strong><a href="relation-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="17fab-116"><strong><a href="relation-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="17fab-117">Возвращает коллекцию <strong>Fields</strong>, которая представляет все объекты <strong>Field</strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="17fab-117">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object.</span></span> <span data-ttu-id="17fab-118">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="17fab-118">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17fab-119"><strong><a href="relation-foreigntable-property-dao.md">ForeignTable</a></strong></span><span class="sxs-lookup"><span data-stu-id="17fab-119"><strong><a href="relation-foreigntable-property-dao.md">ForeignTable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="17fab-120">Задает или возвращает имя внешней таблицы в отношении (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="17fab-120">Sets or returns the name of the foreign table in a relationship (Microsoft Access workspaces only).</span></span> <span data-ttu-id="17fab-121">.</span><span class="sxs-lookup"><span data-stu-id="17fab-121">.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17fab-122"><strong><a href="relation-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="17fab-122"><strong><a href="relation-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="17fab-123">Возвращает или задает имя указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="17fab-123">Returns or sets the name of the specified object.</span></span> <span data-ttu-id="17fab-124"><strong>Строка</strong> для чтения и записи, если объект не был добавлен в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="17fab-124">Read/write <strong>String</strong> if the object has not been appended to a collection.</span></span> <span data-ttu-id="17fab-125"><strong>Строка</strong> , доступная только для чтения, если объект добавлен в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="17fab-125">Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17fab-126"><strong><a href="relation-partialreplica-property-dao.md">партиалреплика</a></strong></span><span class="sxs-lookup"><span data-stu-id="17fab-126"><strong><a href="relation-partialreplica-property-dao.md">PartialReplica</a></strong></span></span></p></td>
<td><p><span data-ttu-id="17fab-127">Задает или возвращает значение объекта <strong>relation</strong> , указывающее, следует ли учитывать это отношение при заполнении частичной реплики из полной реплики.</span><span class="sxs-lookup"><span data-stu-id="17fab-127">Sets or returns a value on a <strong>Relation</strong> object indicating whether that relation should be considered when populating a partial replica from a full replica.</span></span> <span data-ttu-id="17fab-128">(Только базы данных ядра СУБД Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="17fab-128">(Microsoft Access database engine databases only).</span></span> <span data-ttu-id="17fab-129">Для чтения и записи, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="17fab-129">Read/write <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17fab-130"><strong><a href="relation-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="17fab-130"><strong><a href="relation-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="17fab-131">Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="17fab-131">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="17fab-132">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="17fab-132">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17fab-133"><strong><a href="relation-table-property-dao.md">Table</a></strong></span><span class="sxs-lookup"><span data-stu-id="17fab-133"><strong><a href="relation-table-property-dao.md">Table</a></strong></span></span></p></td>
<td><p><span data-ttu-id="17fab-134">Указывает имя основной таблицы объекта <strong><a href="relation-object-dao.md">связи</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="17fab-134">Indicates the name of a <strong><a href="relation-object-dao.md">Relation</a></strong> object's primary table.</span></span> <span data-ttu-id="17fab-135">Это значение должно совпадать с параметром свойства <strong><a href="connection-name-property-dao.md">Name</a></strong> объекта <strong><a href="tabledef-object-dao.md">tabledef</a></strong> или <strong><a href="querydef-object-dao.md">QueryDef</a></strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="17fab-135">This should be equal to the <strong><a href="connection-name-property-dao.md">Name</a></strong> property setting of a <strong><a href="tabledef-object-dao.md">TableDef</a></strong> or <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

