---
title: Relation Members (DAO)
TOCTitle: Relation Members
ms:assetid: 9ee36e7d-3825-1de8-65fb-64bbcada847c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198338(v=office.15)
ms:contentKeyID: 48546670
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0d8395425f10f12d515956a07cd9a190d3544527
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482235"
---
# <a name="relation-members-dao"></a><span data-ttu-id="5c798-102">Relation Members (DAO)</span><span class="sxs-lookup"><span data-stu-id="5c798-102">Relation Members (DAO)</span></span>


<span data-ttu-id="5c798-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5c798-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5c798-104">Объект связи представляет связь между полями в таблицах и запросах (Microsoft Access базами данных, ядро только).</span><span class="sxs-lookup"><span data-stu-id="5c798-104">A Relation object represents a relationship between fields in tables or queries (Microsoft Access database engine databases only).</span></span>

## <a name="methods"></a><span data-ttu-id="5c798-105">Методы</span><span class="sxs-lookup"><span data-stu-id="5c798-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5c798-106">Имя</span><span class="sxs-lookup"><span data-stu-id="5c798-106">Name</span></span></p></th>
<th><p><span data-ttu-id="5c798-107">Описание</span><span class="sxs-lookup"><span data-stu-id="5c798-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c798-108"><strong><a href="relation-createfield-method-dao.md">CreateField</a></strong></span><span class="sxs-lookup"><span data-stu-id="5c798-108"><strong><a href="relation-createfield-method-dao.md">CreateField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5c798-109">Создает новый объект <strong><a href="field-object-dao.md">поля</a></strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="5c798-109">Creates a new <strong><a href="field-object-dao.md">Field</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="5c798-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="5c798-110">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5c798-111">Имя</span><span class="sxs-lookup"><span data-stu-id="5c798-111">Name</span></span></p></th>
<th><p><span data-ttu-id="5c798-112">Описание</span><span class="sxs-lookup"><span data-stu-id="5c798-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c798-113"><strong><a href="relation-attributes-property-dao.md">Атрибуты</a></strong></span><span class="sxs-lookup"><span data-stu-id="5c798-113"><strong><a href="relation-attributes-property-dao.md">Attributes</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5c798-114">Задает или возвращает значение, указывающее, один или несколько характеристик объект <strong>связи</strong> .</span><span class="sxs-lookup"><span data-stu-id="5c798-114">Sets or returns a value that indicates one or more characteristics of a <strong>Relation</strong> object.</span></span> <span data-ttu-id="5c798-115">Чтение и запись <strong>времени</strong>.</span><span class="sxs-lookup"><span data-stu-id="5c798-115">Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c798-116"><strong><a href="relation-fields-property-dao.md">Поля</a></strong></span><span class="sxs-lookup"><span data-stu-id="5c798-116"><strong><a href="relation-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5c798-117">Возвращает коллекцию <strong>полей</strong> , представляющую все хранятся объекты <strong>поля</strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="5c798-117">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object.</span></span> <span data-ttu-id="5c798-118">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5c798-118">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c798-119"><strong><a href="relation-foreigntable-property-dao.md">Таблицавнешнегоключа</a></strong></span><span class="sxs-lookup"><span data-stu-id="5c798-119"><strong><a href="relation-foreigntable-property-dao.md">ForeignTable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5c798-120">Возвращает или задает имя таблицы внешнего в отношении (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="5c798-120">Sets or returns the name of the foreign table in a relationship (Microsoft Access workspaces only).</span></span> <span data-ttu-id="5c798-121">.</span><span class="sxs-lookup"><span data-stu-id="5c798-121"></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c798-122"><strong><a href="relation-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="5c798-122"><strong><a href="relation-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5c798-123">Возвращает или задает имя указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="5c798-123">Returns or sets the name of the specified object.</span></span> <span data-ttu-id="5c798-124">Чтение и запись <strong>строки</strong> Если объект не были добавлены в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="5c798-124">Read/write <strong>String</strong> if the object has not been appended to a collection.</span></span> <span data-ttu-id="5c798-125">Только для чтения <strong>строка</strong> Если объект были добавлены в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="5c798-125">Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c798-126"><strong><a href="relation-partialreplica-property-dao.md">Значений этих</a></strong></span><span class="sxs-lookup"><span data-stu-id="5c798-126"><strong><a href="relation-partialreplica-property-dao.md">PartialReplica</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5c798-127">Задает или возвращает значение, указывающее, следует ли этого отношения учитывать при заполнении реплику из полной реплики объекта <strong>связи</strong> .</span><span class="sxs-lookup"><span data-stu-id="5c798-127">Sets or returns a value on a <strong>Relation</strong> object indicating whether that relation should be considered when populating a partial replica from a full replica.</span></span> <span data-ttu-id="5c798-128">(База данных ядра базы данных Microsoft Access только).</span><span class="sxs-lookup"><span data-stu-id="5c798-128">(Microsoft Access database engine databases only).</span></span> <span data-ttu-id="5c798-129">Для чтения и записи, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="5c798-129">Read/write <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c798-130"><strong><a href="relation-properties-property-dao.md">Свойства</a></strong></span><span class="sxs-lookup"><span data-stu-id="5c798-130"><strong><a href="relation-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5c798-131">Возвращает коллекцию <strong><a href="properties-collection-dao.md">свойств</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="5c798-131">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="5c798-132">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5c798-132">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c798-133"><strong><a href="relation-table-property-dao.md">В таблице</a></strong></span><span class="sxs-lookup"><span data-stu-id="5c798-133"><strong><a href="relation-table-property-dao.md">Table</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5c798-134">Указывает имя таблицы основной объект <strong><a href="relation-object-dao.md">связи</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="5c798-134">Indicates the name of a <strong><a href="relation-object-dao.md">Relation</a></strong> object's primary table.</span></span> <span data-ttu-id="5c798-135">Это должен быть равен <strong><a href="connection-name-property-dao.md">свойства Name объекта <strong><a href="tabledef-object-dao.md">TableDef</a></strong> или <strong><a href="querydef-object-dao.md">QueryDef</a></strong> (только для рабочих областей Microsoft Access)</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="5c798-135">This should be equal to the <strong><a href="connection-name-property-dao.md">Name</a></strong> property setting of a <strong><a href="tabledef-object-dao.md">TableDef</a></strong> or <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

