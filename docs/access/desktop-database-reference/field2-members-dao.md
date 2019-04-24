---
title: Элементы field2 (DAO)
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
# <a name="field2-members-dao"></a>Элементы field2 (DAO)


**Область применения**: Access 2013, Office 2013

Объект field2 представляет столбец данных с общим типом данных и общим набором свойств.

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
<td><p>Добавляет данные из строкового выражения в объект MEMO или большой двоичный объект <strong>field2</strong> в <strong><a href="recordset-object-dao.md">наборе записей</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Создает новый объект определяемого пользователем <strong><a href="property-object-dao.md">Свойства</a></strong> (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-getchunk-method-dao.md">GetChunk</a></strong></p></td>
<td><p>Возвращает полностью или часть содержимого объекта <strong>MEMO</strong> или длинного объекта <strong>BinaryField2</strong> в коллекции Fields объекта <strong><a href="fields-collection-dao.md"></a></strong> <strong><a href="recordset-object-dao.md">Recordset</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-loadfromfile-method-dao.md">LoadFromFile</a></strong></p></td>
<td><p>ЗаГружает указанный файл с диска.</p></td>
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
<td><p>Задает или возвращает значение, которое указывает, является ли строка нулевой длины&quot;&quot;() допустимым параметром для свойства <strong><a href="field-value-property-dao.md">value</a></strong> объекта <strong>field2</strong> с типом данных text или MEMO (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-appendonly-property-dao.md">Аппендонли</a></strong></p></td>
<td><p>Получает или задает <strong>логическое</strong> значение, указывающее, задано ли для поля спЦифиед Добавление новых значений к существующему содержимому поля при их добавлении. Для чтения и записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-attributes-property-dao.md">Attributes</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает одну или несколько характеристик объекта <strong>field2</strong> . Для чтения и записи, <strong>Long</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-collatingorder-property-dao.md">Коллатингордер</a></strong></p></td>
<td><p>Возвращает значение, задающее последовательность порядка сортировки в тексте для сравнения строк или сортировки (только для рабочих областей Microsoft Access). Только для чтения, <strong>Long</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-complextype-property-dao.md">ComplexType</a></strong></p></td>
<td><p>Возвращает объект <strong><a href="complextype-object-dao.md">complexType</a></strong> , представляющий Многозначное поле. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-dataupdatable-property-dao.md">Обновляемые с возможностью обновления</a></strong></p></td>
<td><p>Возвращает значение, которое указывает, является ли данные в поле, представленном объектом <strong>field2</strong> , обновляемым.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-defaultvalue-property-dao.md">DefaultValue</a></strong></p></td>
<td><p>Задает или возвращает значение, заданное по умолчанию для объекта <strong>field2</strong> . Для объекта <strong>field2</strong> , еще не добавленного в коллекцию <strong><a href="fields-collection-dao.md">Fields</a></strong> , это свойство доступно для чтения и записи (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-expression-property-dao.md">Expression</a></strong></p></td>
<td><p>Чтение и запись</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-fieldsize-property-dao.md">(</a></strong></p></td>
<td><p>Возвращает число байтов, используемых в базе данных (а не в памяти) объекта MEMO или длинного двоичного объекта <strong>field2</strong> в коллекции <strong><a href="fields-collection-dao.md">Fields</a></strong> объекта <strong><a href="recordset-object-dao.md">Recordset</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-foreignname-property-dao.md">Фореигннаме</a></strong></p></td>
<td><p>Задает или возвращает значение, задающее имя объекта <strong>field2</strong> в внешней таблице, которая соответствует полю в главной таблице для отношения (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-iscomplex-property-dao.md">Сложный</a></strong></p></td>
<td><p>Возвращает <strong>логическое значение</strong> , которое указывает, является ли указанное поле многозначным типом данных. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-name-property-dao.md">Name</a></strong></p></td>
<td><p>Возвращает или задает имя указанного объекта. <strong>Строка</strong> для чтения и записи, если объект не был добавлен в коллекцию. <strong>Строка</strong> , доступная только для чтения, если объект добавлен в коллекцию.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-ordinalposition-property-dao.md">Ординалпоситион</a></strong></p></td>
<td><p>Задает или возвращает относительное положение объекта <strong>field2</strong> в коллекции Fields <strong><a href="fields-collection-dao.md"></a></strong> . .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-originalvalue-property-dao.md">OriginalValue</a></strong></p></td>
<td><p>Одно из значений <strong><a href="workspacetypeenum-enumeration-dao.md">воркспацетипинум</a></strong> .</p>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Возвращает значение <strong>field2</strong> в базе данных, существовавшее после последнего начала пакетного обновления (только для рабочих областей ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-required-property-dao.md">Обязательно</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, требуется ли для объекта <strong>field2</strong> значение, отличное от NULL.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-size-property-dao.md">Size</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает максимальный размер объекта <strong>field2</strong> в байтах.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-sourcefield-property-dao.md">Саурцефиелд</a></strong></p></td>
<td><p>Возвращает значение, которое указывает имя поля, которое является исходным источником данных для объекта <strong>field2</strong> . Только для чтения, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-sourcetable-property-dao.md">Саурцетабле</a></strong></p></td>
<td><p>Возвращает значение, которое указывает имя таблицы, которая является исходным источником данных для объекта <strong>field2</strong> . Только для чтения, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-type-property-dao.md">Тип</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает операционный тип или тип данных объекта. Чтение и запись <strong>целоГо числа</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-validateonset-property-dao.md">Валидатеонсет</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее, является ли значение объекта <strong>field2</strong> немедленно проверенным, когда задано свойство <strong>value</strong> объекта (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>Задает или возвращает значение, которое проверяет данные в поле по мере их изменения или добавления в таблицу (только для рабочих областей Microsoft Access). Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-validationtext-property-dao.md">ValidationText</a></strong></p></td>
<td><p>Задает или возвращает значение, задающее текст сообщения, которое отображается в приложении, если значение объекта <strong>field2</strong> не удовлетворяет правилу проверки, заданному значением свойства <strong>ValidationRule</strong> (только для рабочих областей Microsoft Access ). Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-value-property-dao.md">Значение</a></strong></p></td>
<td><p>Задает или возвращает значение объекта. Для чтения и записи, <strong>Variant</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-visiblevalue-property-dao.md">Висиблевалуе</a></strong></p></td>
<td><p>Одно из значений <strong><a href="workspacetypeenum-enumeration-dao.md">воркспацетипинум</a></strong> .</p>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Возвращает значение, которое в настоящее время находится в базе данных, которое новее свойства <strong>originalValue</strong> , определенного конфликтом пакетного обновления (только для рабочих областей ODBCDirect).</p></td>
</tr>
</tbody>
</table>

