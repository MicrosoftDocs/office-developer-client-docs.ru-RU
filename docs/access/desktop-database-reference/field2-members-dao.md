---
title: Члены поле2 (DAO)
TOCTitle: Field2 Members
ms:assetid: 27829bbc-8b4e-c7eb-f29b-bcbef341f9fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191913(v=office.15)
ms:contentKeyID: 48543839
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f7d368077e94a24dfd7b3d20dcdaafb0ee7d3c84
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937794"
---
# <a name="field2-members-dao"></a>Члены поле2 (DAO)


**Применимо к**: Access 2013, Office 2013

Объект поле2 представляет столбец данных с типом данных и общий набор свойств.

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
<td><p>Добавление данных из строковое выражение Memo или Long Binary <strong>поле2</strong> объект в <strong><a href="recordset-object-dao.md">набора записей</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Создание пользовательских <strong><a href="property-object-dao.md">свойств</a></strong> объекта (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-getchunk-method-dao.md">Методы GetChunk</a></strong></p></td>
<td><p>Возвращает все или часть содержимого <strong>Memo</strong> или <strong>Длинный BinaryField2</strong> объекта в коллекции <strong><a href="fields-collection-dao.md">полей</a></strong> объекта <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-loadfromfile-method-dao.md">LoadFromFile</a></strong></p></td>
<td><p>Загружает указанный файл с диска.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-savetofile-method-dao.md">SaveToFile</a></strong></p></td>
<td><p>Сохранение вложений на диске. .</p></td>
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
<td><p><strong><a href="field2-allowzerolength-property-dao.md">Пустые строки</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее, является ли строка нулевой длины (&quot;&quot;) имеет недопустимое значение для свойства <strong><a href="field-value-property-dao.md">Value</a></strong> объекта <strong>поле2</strong> с типом данных Text или Memo (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-appendonly-property-dao.md">AppendOnly</a></strong></p></td>
<td><p>Получает или задает значение <strong>Boolean</strong> , указывающее, задано ли для указанного поля для добавления нового значения существующего содержимого поля как их добавления. Для чтения и записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-attributes-property-dao.md">Атрибуты</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее, один или несколько характеристик объекта <strong>поле2</strong> . Чтение и запись <strong>времени</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-collatingorder-property-dao.md">CollatingOrder</a></strong></p></td>
<td><p>Возвращает значение, указывающее последовательность порядок сортировки в текст для сравнения строк или сортировка (только для рабочих областей Microsoft Access). Только для чтения <strong>времени</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-complextype-property-dao.md">ComplexType</a></strong></p></td>
<td><p>Возвращает объект <strong><a href="complextype-object-dao.md">ComplexType</a></strong> , который представляет многозначное поле. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-dataupdatable-property-dao.md">DataUpdatable</a></strong></p></td>
<td><p>Возвращает значение, указывающее, является ли данные в поля, представленного объектом <strong>поле2</strong> обновляемым.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-defaultvalue-property-dao.md">Значение по умолчанию</a></strong></p></td>
<td><p>Задает или возвращает значение по умолчанию объекта <strong>поле2</strong> . Для объекта <strong>поле2</strong> , еще не добавляется в конец коллекции <strong><a href="fields-collection-dao.md">полей</a></strong> это свойство является чтение/запись (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-expression-property-dao.md">Выражение</a></strong></p></td>
<td><p>Чтение и запись</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-fieldsize-property-dao.md">FieldSize</a></strong></p></td>
<td><p>Возвращает число байтов, используемых в базе данных (а не в памяти) Memo или Long Binary <strong>поле2</strong> объекта в коллекции <strong><a href="fields-collection-dao.md">полей</a></strong> объекта <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-foreignname-property-dao.md">ForeignName</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее имя объекта <strong>поле2</strong> внешней таблицы, соответствующее поле в основной таблицы для связи (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-iscomplex-property-dao.md">IsComplex</a></strong></p></td>
<td><p>Возвращает значение <strong>типа Boolean</strong> , указывающее, является ли указанное поле Тип данных, поддерживающий несколько значений. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-name-property-dao.md">Имя</a></strong></p></td>
<td><p>Возвращает или задает имя указанного объекта. Чтение и запись <strong>строки</strong> Если объект не были добавлены в коллекцию. Только для чтения <strong>строка</strong> Если объект были добавлены в коллекцию.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-ordinalposition-property-dao.md">OrdinalPosition</a></strong></p></td>
<td><p>Задает или возвращает относительное положение объекта <strong>поле2</strong> в коллекции <strong><a href="fields-collection-dao.md">полей</a></strong> . .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-originalvalue-property-dao.md">OriginalValue</a></strong></p></td>
<td><p>Одно из значений <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> .</p>
<td><p><strong>Примечание</strong>: технология ODBCDirect рабочие области, не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</p>
<p>Возвращает значение <strong>поле2</strong> в базе данных, которое существовало во время начала последнего обновления пакета (только для рабочих областей технология ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-properties-property-dao.md">Свойства</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">свойств</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-required-property-dao.md">Обязательно</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, требуется ли объект <strong>поле2</strong> ненулевое значение.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-size-property-dao.md">Размер</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает максимальный размер в байтах, <strong>поле2</strong> объекта.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-sourcefield-property-dao.md">SourceField</a></strong></p></td>
<td><p>Возвращает значение, указывающее имя поля, который является оригинального источника данных для объекта <strong>поле2</strong> . Только для чтения, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-sourcetable-property-dao.md">Таблица</a></strong></p></td>
<td><p>Возвращает значение, указывающее имя таблицы, который является оригинального источника данных для объекта <strong>поле2</strong> . Только для чтения, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-type-property-dao.md">Тип</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее действующие типа или данных тип объекта. Чтение и запись <strong>целое число</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-validateonset-property-dao.md">Проверка набора</a></strong></p></td>
<td><p>Задает или возвращает значение, указывает ли значение объекта <strong>поле2</strong> сразу же проверке, если свойство <strong>Value</strong> объекта установлено (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-validationrule-property-dao.md">Значение</a></strong></p></td>
<td><p>Задает или возвращает значение, которое проверяет данные в поля, как она изменен или добавлен в таблицу (только для рабочих областей Microsoft Access). Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-validationtext-property-dao.md">Сообщение об ошибке</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее, текст сообщения, приложение, если значение объекта <strong>поле2</strong> не соответствует правило проверки, указанного идентификатором <strong>условие на значение</strong> свойства поля (Microsoft Access рабочие области только ). Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-value-property-dao.md">Значение</a></strong></p></td>
<td><p>Задает или возвращает значение объекта. Чтение и запись <strong>типа Variant</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-visiblevalue-property-dao.md">VisibleValue</a></strong></p></td>
<td><p>Одно из значений <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> .</p>
<td><p><strong>Примечание</strong>: технология ODBCDirect рабочие области, не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</p>
<p>Возвращает значение в настоящее время в базе данных, больше, чем свойство <strong>OriginalValue</strong> согласно конфликт обновления пакета (только для рабочих областей технология ODBCDirect).</p></td>
</tr>
</tbody>
</table>

