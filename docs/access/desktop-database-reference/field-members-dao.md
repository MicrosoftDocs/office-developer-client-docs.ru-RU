---
title: Члены поля (DAO)
TOCTitle: Field Members
ms:assetid: 4b6a587f-1fd0-37fb-db7d-75b587a8dc60
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193511(v=office.15)
ms:contentKeyID: 48544689
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 497c0375496310c27c134792e01bd17e5533a452
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922204"
---
# <a name="field-members-dao"></a><span data-ttu-id="5565f-102">Члены поля (DAO)</span><span class="sxs-lookup"><span data-stu-id="5565f-102">Field members (DAO)</span></span>


<span data-ttu-id="5565f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5565f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5565f-104">Объект поля представляет столбец данных с типом данных и общий набор свойств.</span><span class="sxs-lookup"><span data-stu-id="5565f-104">A Field object represents a column of data with a common data type and a common set of properties.</span></span>

## <a name="methods"></a><span data-ttu-id="5565f-105">Методы</span><span class="sxs-lookup"><span data-stu-id="5565f-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5565f-106">Имя</span><span class="sxs-lookup"><span data-stu-id="5565f-106">Name</span></span></p></th>
<th><p><span data-ttu-id="5565f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="5565f-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5565f-108"><strong><a href="field-appendchunk-method-dao.md">AppendChunk</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-108"><strong><a href="field-appendchunk-method-dao.md">AppendChunk</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5565f-109">Добавление данных из строковое выражение Memo или Long Binary <strong><a href="field-object-dao.md">поля</a></strong> объект в <strong><a href="recordset-object-dao.md">набора записей</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="5565f-109">Appends data from a string expression to a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in a <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5565f-110"><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-110"><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5565f-111">Создание пользовательских <strong><a href="property-object-dao.md">свойств</a></strong> объекта (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="5565f-111">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5565f-112"><strong><a href="field-getchunk-method-dao.md">Методы GetChunk</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-112"><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5565f-113">Возвращает все или часть содержимого объекта <strong>Memo</strong> или <strong>Long Binary</strong> <strong><a href="field-object-dao.md">поле</a></strong> в коллекции <strong><a href="fields-collection-dao.md">полей</a></strong> объекта <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="5565f-113">Returns all or a portion of the contents of a <strong>Memo</strong> or <strong>Long Binary</strong> <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="5565f-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="5565f-114">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5565f-115">Имя</span><span class="sxs-lookup"><span data-stu-id="5565f-115">Name</span></span></p></th>
<th><p><span data-ttu-id="5565f-116">Описание</span><span class="sxs-lookup"><span data-stu-id="5565f-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5565f-117"><strong><a href="field-allowzerolength-property-dao.md">Пустые строки</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-117"><strong><a href="field-allowzerolength-property-dao.md">AllowZeroLength</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5565f-118">Задает или возвращает значение, указывающее, является ли строка нулевой длины (&quot;&quot;) имеет недопустимое значение для свойства <strong><a href="field-value-property-dao.md">Value</a></strong> объекта <strong><a href="field-object-dao.md">поле</a></strong> с типом данных Text или Memo (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="5565f-118">Sets or returns a value that indicates whether a zero-length string (&quot;&quot;) is a valid setting for the <strong><a href="field-value-property-dao.md">Value</a></strong> property of the <strong><a href="field-object-dao.md">Field</a></strong> object with a Text or Memo data type (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5565f-119"><strong><a href="field-attributes-property-dao.md">Атрибуты</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-119"><strong><a href="field-attributes-property-dao.md">Attributes</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5565f-120">Задает или возвращает значение, указывающее, один или несколько характеристик объекта <strong><a href="field-object-dao.md">поля</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="5565f-120">Sets or returns a value that indicates one or more characteristics of a <strong><a href="field-object-dao.md">Field</a></strong> object.</span></span> <span data-ttu-id="5565f-121">Чтение и запись <strong>времени</strong>.</span><span class="sxs-lookup"><span data-stu-id="5565f-121">Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5565f-122"><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-122"><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5565f-123">Возвращает значение, указывающее последовательность порядок сортировки в текст для сравнения строк или сортировка (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="5565f-123">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="5565f-124">Только для чтения <strong>времени</strong>.</span><span class="sxs-lookup"><span data-stu-id="5565f-124">Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5565f-125"><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-125"><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5565f-126">Возвращает значение, указывающее, является ли данные в поля, представленного объектом <strong><a href="field-object-dao.md">поля</a></strong> обновляемым.</span><span class="sxs-lookup"><span data-stu-id="5565f-126">Returns a value that indicates whether the data in the field represented by a <strong><a href="field-object-dao.md">Field</a></strong> object is updatable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5565f-127"><strong><a href="field-defaultvalue-property-dao.md">Значение по умолчанию</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-127"><strong><a href="field-defaultvalue-property-dao.md">DefaultValue</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5565f-128">Задает или возвращает значение по умолчанию объекта <strong><a href="field-object-dao.md">поля</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="5565f-128">Sets or returns the default value of a <strong><a href="field-object-dao.md">Field</a></strong> object.</span></span> <span data-ttu-id="5565f-129">Для объекта <strong>поля</strong> , еще не добавляется в конец коллекции <strong><a href="fields-collection-dao.md">полей</a></strong> это свойство является чтение/запись (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="5565f-129">For a <strong>Field</strong> object not yet appended to the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection, this property is read/write (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5565f-130"><strong><a href="field-fieldsize-property-dao.md">FieldSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-130"><strong><a href="field-fieldsize-property-dao.md">FieldSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5565f-131">Возвращает число байтов, используемых в базе данных (а не в памяти) объекта Memo или Long Binary <strong><a href="field-object-dao.md">поле</a></strong> в коллекции <strong><a href="fields-collection-dao.md">полей</a></strong> объекта <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="5565f-131">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5565f-132"><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-132"><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5565f-133">Задает или возвращает значение, указывающее имя объекта <strong><a href="field-object-dao.md">поля</a></strong> внешней таблицы, соответствующее поле в основной таблицы для связи (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="5565f-133">Sets or returns a value that specifies the name of the <strong><a href="field-object-dao.md">Field</a></strong> object in a foreign table that corresponds to a field in a primary table for a relationship (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5565f-134"><strong><a href="field-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-134"><strong><a href="field-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5565f-135">Возвращает или задает имя указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="5565f-135">Returns or sets the name of the specified object.</span></span> <span data-ttu-id="5565f-136">Чтение и запись <strong>строки</strong> Если объект не были добавлены в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="5565f-136">Read/write <strong>String</strong> if the object has not been appended to a collection.</span></span> <span data-ttu-id="5565f-137">Только для чтения <strong>строка</strong> Если объект были добавлены в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="5565f-137">Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5565f-138"><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-138"><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5565f-139">Задает или возвращает относительное положение объекта <strong><a href="field-object-dao.md">поля</a></strong> в коллекции <strong><a href="fields-collection-dao.md">полей</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="5565f-139">Sets or returns the relative position of a <strong><a href="field-object-dao.md">Field</a></strong> object within a <strong><a href="fields-collection-dao.md">Fields</a></strong> collection.</span></span> <span data-ttu-id="5565f-140">.</span><span class="sxs-lookup"><span data-stu-id="5565f-140"></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5565f-141"><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-141"><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="5565f-142">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="5565f-142">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="5565f-143">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="5565f-143">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="5565f-144">Возвращает значение <strong>поля</strong> в базе данных, которое существовало во время начала последнего обновления пакета (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="5565f-144">Returns the value of a <strong>Field</strong> in the database that existed when the last batch update began (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5565f-145"><strong><a href="field-properties-property-dao.md">Свойства</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-145"><strong><a href="field-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5565f-146">Возвращает коллекцию <strong><a href="properties-collection-dao.md">свойств</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="5565f-146">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="5565f-147">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5565f-147">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5565f-148"><strong><a href="field-required-property-dao.md">Обязательно</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-148"><strong><a href="field-required-property-dao.md">Required</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5565f-149">Задает или возвращает значение, которое указывает, требуется ли объект <strong><a href="field-object-dao.md">поля</a></strong> ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="5565f-149">Sets or returns a value that indicates whether a <strong><a href="field-object-dao.md">Field</a></strong> object requires a non-Null value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5565f-150"><strong><a href="field-fieldsize-property-dao.md">Размер</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-150"><strong><a href="field-fieldsize-property-dao.md">Size</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5565f-151">Возвращает число байтов, используемых в базе данных (а не в памяти) объекта Memo или Long Binary <strong><a href="field-object-dao.md">поле</a></strong> в коллекции <strong><a href="fields-collection-dao.md">полей</a></strong> объекта <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="5565f-151">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5565f-152"><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-152"><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5565f-153">Возвращает значение, указывающее имя поля, который является оригинального источника данных для объекта <strong>поля</strong> .</span><span class="sxs-lookup"><span data-stu-id="5565f-153">Returns a value that indicates the name of the field that is the original source of the data for a <strong>Field</strong> object.</span></span> <span data-ttu-id="5565f-154">Только для чтения, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="5565f-154">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5565f-155"><strong><a href="field-sourcetable-property-dao.md">Таблица</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-155"><strong><a href="field-sourcetable-property-dao.md">SourceTable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5565f-156">Возвращает значение, указывающее имя таблицы, который является оригинального источника данных для объекта <strong>поля</strong> .</span><span class="sxs-lookup"><span data-stu-id="5565f-156">Returns a value that indicates the name of the table that is the original source of the data for a <strong>Field</strong> object.</span></span> <span data-ttu-id="5565f-157">Только для чтения, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="5565f-157">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5565f-158"><strong><a href="field-type-property-dao.md">Тип</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-158"><strong><a href="field-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5565f-159">Задает или возвращает значение, указывающее действующие типа или данных тип объекта.</span><span class="sxs-lookup"><span data-stu-id="5565f-159">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="5565f-160">Чтение и запись <strong>целое число</strong>.</span><span class="sxs-lookup"><span data-stu-id="5565f-160">Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5565f-161"><strong><a href="field-validateonset-property-dao.md">Проверка набора</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-161"><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5565f-162">Задает или возвращает значение, указывает ли значение <strong><a href="field-object-dao.md">поля</a></strong> объекта сразу же проверке, если свойство <strong><a href="field-value-property-dao.md">Value</a></strong> объекта установлено (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="5565f-162">Sets or returns a value that specifies whether or not the value of a <strong><a href="field-object-dao.md">Field</a></strong> object is immediately validated when the object's <strong><a href="field-value-property-dao.md">Value</a></strong> property is set (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5565f-163"><strong><a href="field-validationrule-property-dao.md">Значение</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-163"><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5565f-164">Задает или возвращает значение, которое проверяет данные в поля, как она изменен или добавлен в таблицу (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="5565f-164">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).</span></span> <span data-ttu-id="5565f-165">Для чтения и записи, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="5565f-165">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5565f-166"><strong><a href="field-validationtext-property-dao.md">Сообщение об ошибке</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-166"><strong><a href="field-validationtext-property-dao.md">ValidationText</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5565f-167">Задает или возвращает значение, указывающее, текст сообщения, приложение, если значение <strong>поля</strong> объекта не удовлетворяют правило проверки, указанного идентификатором <strong>условие на значение</strong> свойства поля (только для рабочих областей Microsoft Access) .</span><span class="sxs-lookup"><span data-stu-id="5565f-167">Sets or returns a value that specifies the text of the message that your application displays if the value of a <strong>Field</strong> object doesn't satisfy the validation rule specified by the <strong>ValidationRule</strong> property setting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="5565f-168">Для чтения и записи, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="5565f-168">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5565f-169"><strong><a href="field-value-property-dao.md">Значение</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-169"><strong><a href="field-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="5565f-170">Задает или возвращает значение объекта.</span><span class="sxs-lookup"><span data-stu-id="5565f-170">Sets or returns the value of an object.</span></span> <span data-ttu-id="5565f-171">Чтение и запись <strong>типа Variant</strong>.</span><span class="sxs-lookup"><span data-stu-id="5565f-171">Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5565f-172"><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="5565f-172"><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="5565f-173">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="5565f-173">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="5565f-174">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="5565f-174">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="5565f-175">Возвращает значение в настоящее время в базе данных, больше, чем свойство <strong>OriginalValue</strong> согласно конфликт обновления пакета (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="5565f-175">Returns a value currently in the database that is newer than the <strong>OriginalValue</strong> property as determined by a batch update conflict (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

