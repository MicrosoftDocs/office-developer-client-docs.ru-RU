---
title: Relation Members (DAO)
TOCTitle: Relation Members
ms:assetid: 9ee36e7d-3825-1de8-65fb-64bbcada847c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198338(v=office.15)
ms:contentKeyID: 48546670
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d6aceacf462898628b0aee9e406860def9474c2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889919"
---
# <a name="relation-members-dao"></a><span data-ttu-id="298bc-102">Relation Members (DAO)</span><span class="sxs-lookup"><span data-stu-id="298bc-102">Relation Members (DAO)</span></span>


<span data-ttu-id="298bc-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="298bc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="298bc-104">Объект связи представляет связь между полями в таблицах и запросах (Microsoft Access базами данных, ядро только).</span><span class="sxs-lookup"><span data-stu-id="298bc-104">A Relation object represents a relationship between fields in tables or queries (Microsoft Access database engine databases only).</span></span>

## <a name="methods"></a><span data-ttu-id="298bc-105">Методы</span><span class="sxs-lookup"><span data-stu-id="298bc-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="298bc-106">Имя</span><span class="sxs-lookup"><span data-stu-id="298bc-106">Name</span></span></p></th>
<th><p><span data-ttu-id="298bc-107">Описание</span><span class="sxs-lookup"><span data-stu-id="298bc-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="298bc-108"><strong><a href="relation-createfield-method-dao.md">CreateField</a></strong></span><span class="sxs-lookup"><span data-stu-id="298bc-108"><strong><a href="relation-createfield-method-dao.md">CreateField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="298bc-109">Создает новый объект <strong><a href="field-object-dao.md">поля</a></strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="298bc-109">Creates a new <strong><a href="field-object-dao.md">Field</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="298bc-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="298bc-110">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="298bc-111">Имя</span><span class="sxs-lookup"><span data-stu-id="298bc-111">Name</span></span></p></th>
<th><p><span data-ttu-id="298bc-112">Описание</span><span class="sxs-lookup"><span data-stu-id="298bc-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="298bc-113"><strong><a href="relation-attributes-property-dao.md">Атрибуты</a></strong></span><span class="sxs-lookup"><span data-stu-id="298bc-113"><strong><a href="relation-attributes-property-dao.md">Attributes</a></strong></span></span></p></td>
<td><p><span data-ttu-id="298bc-114">Задает или возвращает значение, указывающее, один или несколько характеристик объект <strong>связи</strong> .</span><span class="sxs-lookup"><span data-stu-id="298bc-114">Sets or returns a value that indicates one or more characteristics of a <strong>Relation</strong> object.</span></span> <span data-ttu-id="298bc-115">Чтение и запись <strong>времени</strong>.</span><span class="sxs-lookup"><span data-stu-id="298bc-115">Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="298bc-116"><strong><a href="relation-fields-property-dao.md">Поля</a></strong></span><span class="sxs-lookup"><span data-stu-id="298bc-116"><strong><a href="relation-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="298bc-117">Возвращает коллекцию <strong>полей</strong> , представляющую все хранятся объекты <strong>поля</strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="298bc-117">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object.</span></span> <span data-ttu-id="298bc-118">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="298bc-118">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="298bc-119"><strong><a href="relation-foreigntable-property-dao.md">Таблицавнешнегоключа</a></strong></span><span class="sxs-lookup"><span data-stu-id="298bc-119"><strong><a href="relation-foreigntable-property-dao.md">ForeignTable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="298bc-120">Возвращает или задает имя таблицы внешнего в отношении (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="298bc-120">Sets or returns the name of the foreign table in a relationship (Microsoft Access workspaces only).</span></span> <span data-ttu-id="298bc-121">.</span><span class="sxs-lookup"><span data-stu-id="298bc-121"></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="298bc-122"><strong><a href="relation-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="298bc-122"><strong><a href="relation-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="298bc-123">Возвращает или задает имя указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="298bc-123">Returns or sets the name of the specified object.</span></span> <span data-ttu-id="298bc-124">Чтение и запись <strong>строки</strong> Если объект не были добавлены в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="298bc-124">Read/write <strong>String</strong> if the object has not been appended to a collection.</span></span> <span data-ttu-id="298bc-125">Только для чтения <strong>строка</strong> Если объект были добавлены в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="298bc-125">Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="298bc-126"><strong><a href="relation-partialreplica-property-dao.md">Значений этих</a></strong></span><span class="sxs-lookup"><span data-stu-id="298bc-126"><strong><a href="relation-partialreplica-property-dao.md">PartialReplica</a></strong></span></span></p></td>
<td><p><span data-ttu-id="298bc-127">Задает или возвращает значение, указывающее, следует ли этого отношения учитывать при заполнении реплику из полной реплики объекта <strong>связи</strong> .</span><span class="sxs-lookup"><span data-stu-id="298bc-127">Sets or returns a value on a <strong>Relation</strong> object indicating whether that relation should be considered when populating a partial replica from a full replica.</span></span> <span data-ttu-id="298bc-128">(База данных ядра базы данных Microsoft Access только).</span><span class="sxs-lookup"><span data-stu-id="298bc-128">(Microsoft Access database engine databases only).</span></span> <span data-ttu-id="298bc-129">Для чтения и записи, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="298bc-129">Read/write <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="298bc-130"><strong><a href="relation-properties-property-dao.md">Свойства</a></strong></span><span class="sxs-lookup"><span data-stu-id="298bc-130"><strong><a href="relation-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="298bc-131">Возвращает коллекцию <strong><a href="properties-collection-dao.md">свойств</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="298bc-131">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="298bc-132">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="298bc-132">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="298bc-133"><strong><a href="relation-table-property-dao.md">В таблице</a></strong></span><span class="sxs-lookup"><span data-stu-id="298bc-133"><strong><a href="relation-table-property-dao.md">Table</a></strong></span></span></p></td>
<td><p><span data-ttu-id="298bc-134">Указывает имя таблицы основной объект <strong><a href="relation-object-dao.md">связи</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="298bc-134">Indicates the name of a <strong><a href="relation-object-dao.md">Relation</a></strong> object's primary table.</span></span> <span data-ttu-id="298bc-135">Это должен быть равен <strong><a href="connection-name-property-dao.md">свойства Name объекта <strong><a href="tabledef-object-dao.md">TableDef</a></strong> или <strong><a href="querydef-object-dao.md">QueryDef</a></strong> (только для рабочих областей Microsoft Access)</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="298bc-135">This should be equal to the <strong><a href="connection-name-property-dao.md">Name</a></strong> property setting of a <strong><a href="tabledef-object-dao.md">TableDef</a></strong> or <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

