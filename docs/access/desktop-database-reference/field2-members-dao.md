---
title: Участники Field2 (DAO)
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
# <a name="field2-members-dao"></a>Участники Field2 (DAO)


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
<td><p>Применит данные из строки к объекту Memo или Long Binary <strong>Field2</strong> в <strong><a href="recordset-object-dao.md">Наборе записей.</a></strong></p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Создает новый объект Свойства, определенный <strong><a href="property-object-dao.md">пользователем</a></strong> (только рабочие пространства Microsoft Access).</p></td>
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
<td><p>Задает или возвращает значение, которое указывает, является ли строка нулевой длины допустимым параметром для свойства Value объекта Field2 с типом данных Text или &quot; &quot; Memo (только <strong><a href="field-value-property-dao.md"></a></strong> <strong></strong> в рабочей области Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-appendonly-property-dao.md">AppendOnly</a></strong></p></td>
<td><p>Получает или задает <strong>поле Boolean,</strong> которое указывает, настроено ли spcified поле для приложения новых значений к существующему содержимому поля при их добавлении. Для чтения и записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-attributes-property-dao.md">Attributes</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает одну или несколько характеристик объекта <strong>Field2.</strong> Для чтения и записи, <strong>Long</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-collatingorder-property-dao.md">CollatingOrder</a></strong></p></td>
<td><p>Возвращает значение, которое указывает последовательность порядка сортировки в тексте для сравнения строк или сортировки (только в рабочей области Microsoft Access). Только для чтения, <strong>Long</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-complextype-property-dao.md">ComplexType</a></strong></p></td>
<td><p>Возвращает объект <strong><a href="complextype-object-dao.md">ComplexType,</a></strong> который представляет многомерное поле. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-dataupdatable-property-dao.md">DataUpdatable</a></strong></p></td>
<td><p>Возвращает значение, которое указывает, являются ли данные в поле, представленного объектом <strong>Field2,</strong> updatable.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-defaultvalue-property-dao.md">DefaultValue</a></strong></p></td>
<td><p>Задает или возвращает по умолчанию значение <strong>объекта Field2.</strong> Для объекта <strong>Field2,</strong> еще не присоединенного к коллекции <strong><a href="fields-collection-dao.md">Fields,</a></strong> это свойство является чтением или записью (только в рабочей области Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-expression-property-dao.md">Expression</a></strong></p></td>
<td><p>Чтение и запись</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-fieldsize-property-dao.md">FieldSize</a></strong></p></td>
<td><p>Возвращает количество bytes, используемых в базе данных (а не в памяти) объекта Memo или Long Binary <strong>Field2</strong> в коллекции <strong><a href="fields-collection-dao.md">Fields</a></strong> объекта <strong><a href="recordset-object-dao.md">Recordset.</a></strong></p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-foreignname-property-dao.md">ForeignName</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает имя объекта <strong>Field2</strong> в иностранной таблице, соответствующее полю в основной таблице для связи (только в рабочей области Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-iscomplex-property-dao.md">IsComplex</a></strong></p></td>
<td><p>Возвращает <strong>boolean,</strong> который указывает, является ли указанное поле многомерным типом данных. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-name-property-dao.md">Name</a></strong></p></td>
<td><p>Возвращает или задает имя указанного объекта. Строка <strong>read/write,</strong> если объект не был придан коллекции. Строка <strong>только для</strong> чтения, если объект был придан коллекции.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-ordinalposition-property-dao.md">OrdinalPosition</a></strong></p></td>
<td><p>Задает или возвращает относительное положение объекта <strong>Field2</strong> в коллекции <strong><a href="fields-collection-dao.md">Fields.</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-originalvalue-property-dao.md">OriginalValue</a></strong></p></td>
<td><p>Одно из <strong><a href="workspacetypeenum-enumeration-dao.md">значений WorkspaceTypeEnum.</a></strong></p>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Возвращает значение <strong>Field2</strong> в базе данных, существовавшей при последнем пакетном обновлении (только в рабочей области ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-required-property-dao.md">Обязательно</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, требуется ли <strong>объекту Field2</strong> значение non-Null.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-size-property-dao.md">Размер</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает максимальный размер в bytes объекта <strong>Field2.</strong></p></td>
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
<td><p><strong><a href="field2-type-property-dao.md">Тип</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее операционный тип или тип данных объекта. Для чтения и записи, <strong>Integer</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-validateonset-property-dao.md">ValidateOnSet</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, проверяется ли значение объекта <strong>Field2</strong> сразу же при задании свойства <strong>Value</strong> объекта (только в рабочей области Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>Задает или возвращает значение, которое проверяет данные в поле при их изменениях или добавлении в таблицу (только в рабочей области Microsoft Access). Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-validationtext-property-dao.md">ValidationText</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает текст сообщения, отображаемого приложением, если значение объекта <strong>Field2</strong> не удовлетворяет правилу проверки, указанному параметром <strong>validationRule</strong> (только в рабочей области Microsoft Access). Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-value-property-dao.md">Значение</a></strong></p></td>
<td><p>Задает или возвращает значение объекта. Для чтения и записи, <strong>Variant</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-visiblevalue-property-dao.md">VisibleValue</a></strong></p></td>
<td><p>Одно из <strong><a href="workspacetypeenum-enumeration-dao.md">значений WorkspaceTypeEnum.</a></strong></p>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Возвращает значение в настоящее время в базе данных, которое является более новым, чем свойство <strong>OriginalValue,</strong> как определяется конфликтом пакетного обновления (только в рабочей области ODBCDirect).</p></td>
</tr>
</tbody>
</table>

