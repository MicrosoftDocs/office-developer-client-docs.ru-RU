---
title: Члены Field2 (DAO)
TOCTitle: Field2 Members
ms:assetid: 27829bbc-8b4e-c7eb-f29b-bcbef341f9fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191913(v=office.15)
ms:contentKeyID: 48543839
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf3deac487f1e114bea2a69d5423a210a51a5944
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292799"
---
# <a name="field2-members-dao"></a>Члены Field2 (DAO)


**Область применения**: Access 2013, Office 2013

Объект Field2 представляет столбец данных с общим типом данных и общим набором свойств.

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
<td><p><strong><a href="field2-appendchunk-method-dao.md">AppendChunk</a></strong></p></td>
<td><p>Appends data from a string expression to a Memo or Long Binary <strong>Field2</strong> object in a <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Создает объект свойства, определяемого <strong><a href="property-object-dao.md">пользователем</a></strong> (только для рабочих пространств Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-getchunk-method-dao.md">GetChunk</a></strong></p></td>
<td><p>Возвращает все или часть содержимого объекта <strong>Memo</strong> или <strong>Long BinaryField2</strong> в коллекции <strong><a href="fields-collection-dao.md">Fields</a></strong> объекта <strong><a href="recordset-object-dao.md">Recordset.</a></strong></p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-loadfromfile-method-dao.md">LoadFromFile</a></strong></p></td>
<td><p>Загружает указанный файл с диска.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-savetofile-method-dao.md">SaveToFile</a></strong></p></td>
<td><p>Сохраняет вложение на диске. .</p></td>
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
<td><p><strong><a href="field2-allowzerolength-property-dao.md">AllowZeroLength</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, является ли строка нулевой длины () допустимым параметром для свойства Value объекта Field2 с типом данных Text или &quot; &quot; Memo (только <strong><a href="field-value-property-dao.md"></a></strong> <strong></strong> для рабочей области Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-appendonly-property-dao.md">AppendOnly</a></strong></p></td>
<td><p>Возвращает или задает значение <strong>boolean,</strong> которое указывает, установлено ли в поле spcified новые значения для существующего содержимого поля при их добавлении. Для чтения и записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-attributes-property-dao.md">Атрибуты</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает одну или несколько характеристик <strong>объекта Field2.</strong> Для чтения и записи, <strong>Long</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-collatingorder-property-dao.md">CollatingOrder</a></strong></p></td>
<td><p>Возвращает значение, которое указывает последовательность порядка сортировки в тексте для сравнения или сортировки строк (только для рабочей области Microsoft Access). Только для чтения, <strong>Long</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-complextype-property-dao.md">ComplexType</a></strong></p></td>
<td><p>Возвращает объект <strong><a href="complextype-object-dao.md">ComplexType,</a></strong> который представляет поле с несколькими значениями. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-dataupdatable-property-dao.md">DataUpdatable</a></strong></p></td>
<td><p>Возвращает значение, которое указывает, могут ли данные в поле, представляемом объектом <strong>Field2,</strong> быть updatable.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-defaultvalue-property-dao.md">DefaultValue</a></strong></p></td>
<td><p>Задает или возвращает значение по умолчанию для <strong>объекта Field2.</strong> Для объекта <strong>Field2,</strong> еще не присоединенного к коллекции <strong><a href="fields-collection-dao.md">Fields,</a></strong> это свойство доступно только для чтения и записи (только для рабочей области Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-expression-property-dao.md">Expression</a></strong></p></td>
<td><p>Чтение и запись</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-fieldsize-property-dao.md">FieldSize</a></strong></p></td>
<td><p>Возвращает количество ветвей, используемых в базе данных (а не в памяти) объекта Memo или Long Binary <strong>Field2</strong> в коллекции <strong><a href="fields-collection-dao.md">Fields</a></strong> объекта <strong><a href="recordset-object-dao.md">Recordset.</a></strong></p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-foreignname-property-dao.md">ForeignName</a></strong></p></td>
<td><p>Задает или возвращает значение, которое задает имя объекта <strong>Field2</strong> во внешней таблице, которое соответствует полю в основной таблице для связи (только для рабочей области Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-iscomplex-property-dao.md">IsComplex</a></strong></p></td>
<td><p>Возвращает <strong>значение Boolean,</strong> которое указывает, является ли указанное поле типом данных с несколькими значениями. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-name-property-dao.md">Name</a></strong></p></td>
<td><p>Возвращает или задает имя указанного объекта. Строка <strong>чтения</strong> и записи, если объект не был appended к коллекции. Строка <strong>только</strong> для чтения, если объект был appended к коллекции.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-ordinalposition-property-dao.md">OrdinalPosition</a></strong></p></td>
<td><p>Задает или возвращает относительную позицию объекта <strong>Field2</strong> в коллекции <strong><a href="fields-collection-dao.md">Fields.</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-originalvalue-property-dao.md">OriginalValue</a></strong></p></td>
<td><p>Одно из <strong><a href="workspacetypeenum-enumeration-dao.md">значений WorkspaceTypeEnum.</a></strong></p>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Возвращает значение поля <strong>2</strong> в базе данных, существовавшей при последнем пакетном обновлении (только для рабочей области ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-required-property-dao.md">Обязательно</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, требуется ли для объекта <strong>Field2</strong> значение, не относящеся к NULL.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-size-property-dao.md">Размер</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает максимальный размер объекта <strong>Field2</strong> (в bytes).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-sourcefield-property-dao.md">SourceField</a></strong></p></td>
<td><p>Возвращает значение, которое указывает имя поля, которое является исходным источником данных для <strong>объекта Field2.</strong> Только для чтения, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-sourcetable-property-dao.md">SourceTable</a></strong></p></td>
<td><p>Возвращает значение, которое указывает имя таблицы, которая является исходным источником данных для <strong>объекта Field2.</strong> Только для чтения, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-type-property-dao.md">Type</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее операционный тип или тип данных объекта. Для чтения и записи, <strong>Integer</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-validateonset-property-dao.md">ValidateOnSet</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, проверяется ли значение объекта <strong>Field2</strong> немедленно, если задано свойство <strong>Value</strong> объекта (только для рабочей области Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>Задает или возвращает значение, которое проверяет данные в поле при их изменениях или добавлении в таблицу (только для рабочей области Microsoft Access). Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-validationtext-property-dao.md">ValidationText</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает текст сообщения, отображаемого приложением, если значение объекта <strong>Field2</strong> не удовлетворяет правилу проверки, указанному в параметре свойства <strong>ValidationRule</strong> (только для рабочей области Microsoft Access). Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-value-property-dao.md">Значение</a></strong></p></td>
<td><p>Задает или возвращает значение объекта. Для чтения и записи, <strong>Variant</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-visiblevalue-property-dao.md">VisibleValue</a></strong></p></td>
<td><p>Одно из <strong><a href="workspacetypeenum-enumeration-dao.md">значений WorkspaceTypeEnum.</a></strong></p>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Возвращает значение, которое в настоящее время находится в базе данных, новее свойства <strong>OriginalValue,</strong> определяемой конфликтом пакетного обновления (только для рабочей области ODBCDirect).</p></td>
</tr>
</tbody>
</table>

