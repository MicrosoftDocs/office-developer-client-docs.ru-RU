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
# <a name="field-members-dao"></a>Элементы Field (DAO)


**Область применения**: Access 2013, Office 2013

Объект Field представляет столбец данных с общим типом данных и общим набором свойств.

## <a name="methods"></a>Методы

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="field-appendchunk-method-dao.md">AppendChunk</a></strong></p></td>
<td><p>Appends data from a string expression to a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in a <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Создает объект Property, определенный <strong><a href="property-object-dao.md">пользователем</a></strong> (только для рабочих пространств Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></p></td>
<td><p>Возвращает все или часть содержимого объекта <strong>Memo</strong> или <strong>Long Binary</strong> <strong><a href="field-object-dao.md">Field</a></strong> в коллекции <strong><a href="fields-collection-dao.md">Fields</a></strong> объекта <strong><a href="recordset-object-dao.md">Recordset.</a></strong></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>Свойства

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="field-allowzerolength-property-dao.md">AllowZeroLength</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, является ли строка нулевой длины () допустимым параметром свойства Value объекта Field с типом данных Text или &quot; &quot; Memo (только <strong><a href="field-value-property-dao.md"></a></strong> <strong><a href="field-object-dao.md"></a></strong> для рабочей области Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-attributes-property-dao.md">Атрибуты</a></strong></p></td>
<td><p>Задает или возвращает значение, которое определяет одну или несколько характеристик объекта <strong><a href="field-object-dao.md">Field</a></strong>. Для чтения и записи, <strong>Long</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></p></td>
<td><p>Возвращает значение, которое указывает последовательность порядка сортировки в тексте для сравнения строк или сортировки (только для рабочей области Microsoft Access). Только для чтения, <strong>Long</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></p></td>
<td><p>Возвращает значение, которое указывает, могут ли данные в поле, представляемом объектом <strong><a href="field-object-dao.md">Field,</a></strong> быть updatable.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-defaultvalue-property-dao.md">DefaultValue</a></strong></p></td>
<td><p>Задает или возвращает значение по умолчанию для объекта <strong><a href="field-object-dao.md">Field.</a></strong> Для объекта <strong>Field,</strong> еще не присоединенного к коллекции <strong><a href="fields-collection-dao.md">Fields,</a></strong> это свойство доступно только для чтения и записи (только для рабочей области Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-fieldsize-property-dao.md">FieldSize</a></strong></p></td>
<td><p>Возвращает количество используемых в базе данных (а не в памяти) данных объекта Memo или Long Binary <strong><a href="field-object-dao.md">Field</a></strong> в коллекции <strong><a href="fields-collection-dao.md">Fields</a></strong> объекта <strong><a href="recordset-object-dao.md">Recordset.</a></strong></p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></p></td>
<td><p>Задает или возвращает значение, которое задает имя объекта <strong><a href="field-object-dao.md">Field</a></strong> во внешней таблице, соответствующее полю в основной таблице для связи (только для рабочей области Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-name-property-dao.md">Name</a></strong></p></td>
<td><p>Возвращает или задает имя указанного объекта. Строка <strong>чтения</strong> и записи, если объект не был appended к коллекции. Строка только <strong>для</strong> чтения, если объект был appended к коллекции.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></p></td>
<td><p>Задает или возвращает относительное положение объекта <strong><a href="field-object-dao.md">Field</a></strong> в коллекции <strong><a href="fields-collection-dao.md">Fields.</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></p></td>
<td><p>Одно из <strong><a href="workspacetypeenum-enumeration-dao.md">значений WorkspaceTypeEnum.</a></strong></p>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Возвращает значение поля <strong></strong> в базе данных, существовавшей при последнем пакетном обновлении (только для рабочей области ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-required-property-dao.md">Обязательно</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, требуется ли для объекта <strong><a href="field-object-dao.md">Field</a></strong> значение, не относящеся к NULL.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-fieldsize-property-dao.md">Размер</a></strong></p></td>
<td><p>Возвращает количество используемых в базе данных (а не в памяти) данных объекта Memo или Long Binary <strong><a href="field-object-dao.md">Field</a></strong> в коллекции <strong><a href="fields-collection-dao.md">Fields</a></strong> объекта <strong><a href="recordset-object-dao.md">Recordset.</a></strong></p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></p></td>
<td><p>Возвращает значение, которое указывает имя поля, которое является исходным источником данных для <strong>объекта Field.</strong> Только для чтения, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-sourcetable-property-dao.md">SourceTable</a></strong></p></td>
<td><p>Возвращает значение, которое указывает имя таблицы, которая является исходным источником данных для <strong>объекта Field.</strong> Только для чтения, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-type-property-dao.md">Type</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее операционный тип или тип данных объекта. Для чтения и записи, <strong>Integer</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, проверяется ли значение объекта <strong><a href="field-object-dao.md">Field</a></strong> немедленно, если задано свойство <strong><a href="field-value-property-dao.md">Value</a></strong> объекта (только для рабочей области Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>Задает или возвращает значение, которое проверяет данные в поле при их изменениях или добавлении в таблицу (только для рабочей области Microsoft Access). Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-validationtext-property-dao.md">ValidationText</a></strong></p></td>
<td><p>Задает или возвращает значение, определяющее текст сообщения, которое отображает ваше приложение, если значение объекта <strong>Field</strong> не удовлетворяют правилу проверки, задаваемому настройкой параметра <strong>ValidationRule</strong> (только для рабочих областей Microsoft Access). Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-value-property-dao.md">Значение</a></strong></p></td>
<td><p>Задает или возвращает значение объекта. Для чтения и записи, <strong>Variant</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></p></td>
<td><p>Одно из <strong><a href="workspacetypeenum-enumeration-dao.md">значений WorkspaceTypeEnum.</a></strong></p>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Возвращает значение, которое в настоящее время находится в базе данных, новее свойства <strong>OriginalValue,</strong> определяемой конфликтом пакетного обновления (только для рабочей области ODBCDirect).</p></td>
</tr>
</tbody>
</table>

