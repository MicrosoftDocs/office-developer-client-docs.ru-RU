---
title: Элементы Field (DAO)
TOCTitle: Field Members
ms:assetid: 4b6a587f-1fd0-37fb-db7d-75b587a8dc60
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193511(v=office.15)
ms:contentKeyID: 48544689
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1a0e448662384572163fca074e554a5e30be30a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293093"
---
# <a name="field-members-dao"></a><span data-ttu-id="1ff72-102">Элементы Field (DAO)</span><span class="sxs-lookup"><span data-stu-id="1ff72-102">Field members (DAO)</span></span>


<span data-ttu-id="1ff72-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1ff72-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1ff72-104">Объект Field представляет столбец данных с общим типом данных и общим набором свойств.</span><span class="sxs-lookup"><span data-stu-id="1ff72-104">A Field object represents a column of data with a common data type and a common set of properties.</span></span>

## <a name="methods"></a><span data-ttu-id="1ff72-105">Методы</span><span class="sxs-lookup"><span data-stu-id="1ff72-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ff72-106">Имя</span><span class="sxs-lookup"><span data-stu-id="1ff72-106">Name</span></span></p></th>
<th><p><span data-ttu-id="1ff72-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1ff72-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ff72-108"><strong><a href="field-appendchunk-method-dao.md">AppendChunk</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-108"><strong><a href="field-appendchunk-method-dao.md">AppendChunk</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-109">Применит данные из строки к объекту Memo или Long Binary <strong><a href="field-object-dao.md">Field</a></strong> в <strong><a href="recordset-object-dao.md">Наборе записей.</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-109">Appends data from a string expression to a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in a <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ff72-110"><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-110"><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-111">Создает новый объект Свойства, определенный <strong><a href="property-object-dao.md">пользователем</a></strong> (только рабочие пространства Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="1ff72-111">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ff72-112"><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-112"><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-113">Возвращает все или часть содержимого объекта <strong>Memo</strong> или <strong>Long Binary</strong> <strong><a href="field-object-dao.md">Field</a></strong> в коллекции <strong><a href="fields-collection-dao.md">Поля</a></strong> объекта <strong><a href="recordset-object-dao.md">Recordset.</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-113">Returns all or a portion of the contents of a <strong>Memo</strong> or <strong>Long Binary</strong> <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="1ff72-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="1ff72-114">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ff72-115">Имя</span><span class="sxs-lookup"><span data-stu-id="1ff72-115">Name</span></span></p></th>
<th><p><span data-ttu-id="1ff72-116">Описание</span><span class="sxs-lookup"><span data-stu-id="1ff72-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ff72-117"><strong><a href="field-allowzerolength-property-dao.md">AllowZeroLength</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-117"><strong><a href="field-allowzerolength-property-dao.md">AllowZeroLength</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-118">Задает или возвращает значение, которое указывает, является ли строка нулевой длины допустимым параметром для свойства Value объекта Field с типом данных Text или &quot; &quot; Memo (только <strong><a href="field-value-property-dao.md"></a></strong> <strong><a href="field-object-dao.md"></a></strong> в рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="1ff72-118">Sets or returns a value that indicates whether a zero-length string (&quot;&quot;) is a valid setting for the <strong><a href="field-value-property-dao.md">Value</a></strong> property of the <strong><a href="field-object-dao.md">Field</a></strong> object with a Text or Memo data type (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ff72-119"><strong><a href="field-attributes-property-dao.md">Attributes</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-119"><strong><a href="field-attributes-property-dao.md">Attributes</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-120">Задает или возвращает значение, которое определяет одну или несколько характеристик объекта <strong><a href="field-object-dao.md">Field</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="1ff72-120">Sets or returns a value that indicates one or more characteristics of a <strong><a href="field-object-dao.md">Field</a></strong> object.</span></span> <span data-ttu-id="1ff72-121">Для чтения и записи, <strong>Long</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ff72-121">Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ff72-122"><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-122"><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-123">Возвращает значение, которое указывает последовательность порядка сортировки в тексте для сравнения строк или сортировки (только в рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="1ff72-123">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="1ff72-124">Только для чтения, <strong>Long</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ff72-124">Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ff72-125"><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-125"><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-126">Возвращает значение, которое указывает, являются ли данные в поле, представленного объектом <strong><a href="field-object-dao.md">Field,</a></strong> updatable.</span><span class="sxs-lookup"><span data-stu-id="1ff72-126">Returns a value that indicates whether the data in the field represented by a <strong><a href="field-object-dao.md">Field</a></strong> object is updatable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ff72-127"><strong><a href="field-defaultvalue-property-dao.md">DefaultValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-127"><strong><a href="field-defaultvalue-property-dao.md">DefaultValue</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-128">Задает или возвращает значение по умолчанию объекта <strong><a href="field-object-dao.md">Field.</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-128">Sets or returns the default value of a <strong><a href="field-object-dao.md">Field</a></strong> object.</span></span> <span data-ttu-id="1ff72-129">Для объекта <strong>Field,</strong> еще не присоединенного к коллекции <strong><a href="fields-collection-dao.md">Fields,</a></strong> это свойство является чтением или записью (только в рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="1ff72-129">For a <strong>Field</strong> object not yet appended to the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection, this property is read/write (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ff72-130"><strong><a href="field-fieldsize-property-dao.md">FieldSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-130"><strong><a href="field-fieldsize-property-dao.md">FieldSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-131">Возвращает количество bytes, используемых в базе данных (а не в памяти) объекта Memo или Long Binary <strong><a href="field-object-dao.md">Field</a></strong> в коллекции <strong><a href="fields-collection-dao.md">Fields</a></strong> объекта <strong><a href="recordset-object-dao.md">Recordset.</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-131">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ff72-132"><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-132"><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-133">Задает или возвращает значение, которое указывает имя объекта <strong><a href="field-object-dao.md">Field</a></strong> в иностранной таблице, соответствующее полю в основной таблице для связи (только в рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="1ff72-133">Sets or returns a value that specifies the name of the <strong><a href="field-object-dao.md">Field</a></strong> object in a foreign table that corresponds to a field in a primary table for a relationship (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ff72-134"><strong><a href="field-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-134"><strong><a href="field-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-135">Возвращает или задает имя указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="1ff72-135">Returns or sets the name of the specified object.</span></span> <span data-ttu-id="1ff72-136">Строка <strong>read/write,</strong> если объект не был придан коллекции.</span><span class="sxs-lookup"><span data-stu-id="1ff72-136">Read/write <strong>String</strong> if the object has not been appended to a collection.</span></span> <span data-ttu-id="1ff72-137">Строка <strong>только для</strong> чтения, если объект был придан коллекции.</span><span class="sxs-lookup"><span data-stu-id="1ff72-137">Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ff72-138"><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-138"><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-139">Задает или возвращает относительное положение объекта <strong><a href="field-object-dao.md">Field</a></strong> в коллекции <strong><a href="fields-collection-dao.md">Fields.</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-139">Sets or returns the relative position of a <strong><a href="field-object-dao.md">Field</a></strong> object within a <strong><a href="fields-collection-dao.md">Fields</a></strong> collection.</span></span> <span data-ttu-id="1ff72-140">.</span><span class="sxs-lookup"><span data-stu-id="1ff72-140">.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ff72-141"><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-141"><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-142">Одно из <strong><a href="workspacetypeenum-enumeration-dao.md">значений WorkspaceTypeEnum.</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-142">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>
<td><p><span data-ttu-id="1ff72-143"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="1ff72-143"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="1ff72-144">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="1ff72-144">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="1ff72-145">Возвращает значение поля <strong></strong> в базе данных, существовавшей при последнем пакетном обновлении (только в рабочей области ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="1ff72-145">Returns the value of a <strong>Field</strong> in the database that existed when the last batch update began (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ff72-146"><strong><a href="field-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-146"><strong><a href="field-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-147">Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="1ff72-147">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="1ff72-148">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1ff72-148">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ff72-149"><strong><a href="field-required-property-dao.md">Обязательно</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-149"><strong><a href="field-required-property-dao.md">Required</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-150">Задает или возвращает значение, которое указывает, требуется ли <strong><a href="field-object-dao.md">объекту Field</a></strong> значение non-Null.</span><span class="sxs-lookup"><span data-stu-id="1ff72-150">Sets or returns a value that indicates whether a <strong><a href="field-object-dao.md">Field</a></strong> object requires a non-Null value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ff72-151"><strong><a href="field-fieldsize-property-dao.md">Размер</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-151"><strong><a href="field-fieldsize-property-dao.md">Size</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-152">Возвращает количество bytes, используемых в базе данных (а не в памяти) объекта Memo или Long Binary <strong><a href="field-object-dao.md">Field</a></strong> в коллекции <strong><a href="fields-collection-dao.md">Fields</a></strong> объекта <strong><a href="recordset-object-dao.md">Recordset.</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-152">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ff72-153"><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-153"><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-154">Возвращает значение, которое указывает имя поля, которое является исходным источником данных для <strong>объекта Field.</strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-154">Returns a value that indicates the name of the field that is the original source of the data for a <strong>Field</strong> object.</span></span> <span data-ttu-id="1ff72-155">Только для чтения, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ff72-155">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ff72-156"><strong><a href="field-sourcetable-property-dao.md">SourceTable</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-156"><strong><a href="field-sourcetable-property-dao.md">SourceTable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-157">Возвращает значение, которое указывает имя таблицы, которая является исходным источником данных для <strong>объекта Field.</strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-157">Returns a value that indicates the name of the table that is the original source of the data for a <strong>Field</strong> object.</span></span> <span data-ttu-id="1ff72-158">Только для чтения, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ff72-158">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ff72-159"><strong><a href="field-type-property-dao.md">Тип</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-159"><strong><a href="field-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-160">Задает или возвращает значение, указывающее операционный тип или тип данных объекта.</span><span class="sxs-lookup"><span data-stu-id="1ff72-160">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="1ff72-161">Для чтения и записи, <strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ff72-161">Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ff72-162"><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-162"><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-163">Задает или возвращает значение, которое указывает, проверяется ли значение объекта <strong><a href="field-object-dao.md">Field</a></strong> сразу же при задании свойства <strong><a href="field-value-property-dao.md">Value</a></strong> объекта (только в рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="1ff72-163">Sets or returns a value that specifies whether or not the value of a <strong><a href="field-object-dao.md">Field</a></strong> object is immediately validated when the object's <strong><a href="field-value-property-dao.md">Value</a></strong> property is set (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ff72-164"><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-164"><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-165">Задает или возвращает значение, которое проверяет данные в поле при их изменениях или добавлении в таблицу (только в рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="1ff72-165">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).</span></span> <span data-ttu-id="1ff72-166">Для чтения и записи, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ff72-166">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ff72-167"><strong><a href="field-validationtext-property-dao.md">ValidationText</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-167"><strong><a href="field-validationtext-property-dao.md">ValidationText</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-168">Задает или возвращает значение, определяющее текст сообщения, которое отображает ваше приложение, если значение объекта <strong>Field</strong> не удовлетворяют правилу проверки, задаваемому настройкой параметра <strong>ValidationRule</strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="1ff72-168">Sets or returns a value that specifies the text of the message that your application displays if the value of a <strong>Field</strong> object doesn't satisfy the validation rule specified by the <strong>ValidationRule</strong> property setting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="1ff72-169">Для чтения и записи, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ff72-169">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ff72-170"><strong><a href="field-value-property-dao.md">Значение</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-170"><strong><a href="field-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-171">Задает или возвращает значение объекта.</span><span class="sxs-lookup"><span data-stu-id="1ff72-171">Sets or returns the value of an object.</span></span> <span data-ttu-id="1ff72-172">Для чтения и записи, <strong>Variant</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ff72-172">Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ff72-173"><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-173"><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></span></span></p></td>
<td><p><span data-ttu-id="1ff72-174">Одно из <strong><a href="workspacetypeenum-enumeration-dao.md">значений WorkspaceTypeEnum.</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ff72-174">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>
<td><p><span data-ttu-id="1ff72-175"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="1ff72-175"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="1ff72-176">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="1ff72-176">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="1ff72-177">Возвращает значение в настоящее время в базе данных, которое является более новым, чем свойство <strong>OriginalValue,</strong> как определяется конфликтом пакетного обновления (только в рабочей области ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="1ff72-177">Returns a value currently in the database that is newer than the <strong>OriginalValue</strong> property as determined by a batch update conflict (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

