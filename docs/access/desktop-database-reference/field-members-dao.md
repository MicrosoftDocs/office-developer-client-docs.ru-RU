---
title: Field Members (DAO)
TOCTitle: Field Members
ms:assetid: 4b6a587f-1fd0-37fb-db7d-75b587a8dc60
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193511(v=office.15)
ms:contentKeyID: 48544689
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 649cfa4dd14ed0068aeb333ffc8e5799426ac52d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870424"
---
# <a name="field-members-dao"></a>Field Members (DAO)


**Применимо к**: Access 2013, Office 2013

Объект поля представляет столбец данных с типом данных и общий набор свойств.

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
<td><p>Добавление данных из строковое выражение Memo или Long Binary <strong><a href="field-object-dao.md">поля</a></strong> объект в <strong><a href="recordset-object-dao.md">набора записей</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Создание пользовательских <strong><a href="property-object-dao.md">свойств</a></strong> объекта (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-getchunk-method-dao.md">Методы GetChunk</a></strong></p></td>
<td><p>Возвращает все или часть содержимого объекта <strong>Memo</strong> или <strong>Long Binary</strong> <strong><a href="field-object-dao.md">поле</a></strong> в коллекции <strong><a href="fields-collection-dao.md">полей</a></strong> объекта <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</p></td>
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
<td><p><strong><a href="field-allowzerolength-property-dao.md">Пустые строки</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее, является ли строка нулевой длины (&quot;&quot;) имеет недопустимое значение для свойства <strong><a href="field-value-property-dao.md">Value</a></strong> объекта <strong><a href="field-object-dao.md">поле</a></strong> с типом данных Text или Memo (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-attributes-property-dao.md">Атрибуты</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее, один или несколько характеристик объекта <strong><a href="field-object-dao.md">поля</a></strong> . Чтение и запись <strong>времени</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></p></td>
<td><p>Возвращает значение, указывающее последовательность порядок сортировки в текст для сравнения строк или сортировка (только для рабочих областей Microsoft Access). Только для чтения <strong>времени</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></p></td>
<td><p>Возвращает значение, указывающее, является ли данные в поля, представленного объектом <strong><a href="field-object-dao.md">поля</a></strong> обновляемым.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-defaultvalue-property-dao.md">Значение по умолчанию</a></strong></p></td>
<td><p>Задает или возвращает значение по умолчанию объекта <strong><a href="field-object-dao.md">поля</a></strong> . Для объекта <strong>поля</strong> , еще не добавляется в конец коллекции <strong><a href="fields-collection-dao.md">полей</a></strong> это свойство является чтение/запись (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-fieldsize-property-dao.md">FieldSize</a></strong></p></td>
<td><p>Возвращает число байтов, используемых в базе данных (а не в памяти) объекта Memo или Long Binary <strong><a href="field-object-dao.md">поле</a></strong> в коллекции <strong><a href="fields-collection-dao.md">полей</a></strong> объекта <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее имя объекта <strong><a href="field-object-dao.md">поля</a></strong> внешней таблицы, соответствующее поле в основной таблицы для связи (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-name-property-dao.md">Name</a></strong></p></td>
<td><p>Возвращает или задает имя указанного объекта. Чтение и запись <strong>строки</strong> Если объект не были добавлены в коллекцию. Только для чтения <strong>строка</strong> Если объект были добавлены в коллекцию.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></p></td>
<td><p>Задает или возвращает относительное положение объекта <strong><a href="field-object-dao.md">поля</a></strong> в коллекции <strong><a href="fields-collection-dao.md">полей</a></strong> . .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></p></td>
<td><p></p>

> [!NOTE]
> Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.


<p>Возвращает значение <strong>поля</strong> в базе данных, которое существовало во время начала последнего обновления пакета (только для рабочих областей технология ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-properties-property-dao.md">Свойства</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">свойств</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-required-property-dao.md">Обязательный</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, требуется ли объект <strong><a href="field-object-dao.md">поля</a></strong> ненулевое значение.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-fieldsize-property-dao.md">Размер</a></strong></p></td>
<td><p>Возвращает число байтов, используемых в базе данных (а не в памяти) объекта Memo или Long Binary <strong><a href="field-object-dao.md">поле</a></strong> в коллекции <strong><a href="fields-collection-dao.md">полей</a></strong> объекта <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></p></td>
<td><p>Возвращает значение, указывающее имя поля, который является оригинального источника данных для объекта <strong>поля</strong> . Только для чтения, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-sourcetable-property-dao.md">Таблица</a></strong></p></td>
<td><p>Возвращает значение, указывающее имя таблицы, который является оригинального источника данных для объекта <strong>поля</strong> . Только для чтения, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-type-property-dao.md">Тип</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее действующие типа или данных тип объекта. Чтение и запись <strong>целое число</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-validateonset-property-dao.md">Проверка набора</a></strong></p></td>
<td><p>Задает или возвращает значение, указывает ли значение <strong><a href="field-object-dao.md">поля</a></strong> объекта сразу же проверке, если свойство <strong><a href="field-value-property-dao.md">Value</a></strong> объекта установлено (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-validationrule-property-dao.md">Значение</a></strong></p></td>
<td><p>Задает или возвращает значение, которое проверяет данные в поля, как она изменен или добавлен в таблицу (только для рабочих областей Microsoft Access). Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-validationtext-property-dao.md">Сообщение об ошибке</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее, текст сообщения, приложение, если значение <strong>поля</strong> объекта не удовлетворяют правило проверки, указанного идентификатором <strong>условие на значение</strong> свойства поля (только для рабочих областей Microsoft Access) . Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-value-property-dao.md">Значение</a></strong></p></td>
<td><p>Задает или возвращает значение объекта. Чтение и запись <strong>типа Variant</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></p></td>
<td><p></p>

> [!NOTE]
> Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.


<p>Возвращает значение в настоящее время в базе данных, больше, чем свойство <strong>OriginalValue</strong> согласно конфликт обновления пакета (только для рабочих областей технология ODBCDirect).</p></td>
</tr>
</tbody>
</table>

