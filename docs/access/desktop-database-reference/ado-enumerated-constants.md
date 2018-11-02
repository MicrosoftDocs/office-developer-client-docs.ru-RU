---
title: Перечислимые константы ADO
TOCTitle: ADO enumerated constants
ms:assetid: 7c983acd-8b38-dc3c-6704-46e649ebb7d6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249522(v=office.15)
ms:contentKeyID: 48545841
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0e6a6dee6d2882b1d7d1c277584ca8ba46d6db28
ms.sourcegitcommit: 48bfe5ab15b11105f4f52937b886c92bdc26525a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25910952"
---
# <a name="ado-enumerated-constants"></a>Перечислимые константы ADO

**Применимо к**: Access 2013, Office 2013

Чтобы помочь в отладке, перечислений ADO списка значение для каждого константу. Тем не менее это значение исключительно рекомендации и может измениться в разных выпусках ADO в другую. Код должен только зависят от имени, а не фактические значения каждого перечисляемые константы.

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>Константа перечисления</th>
<th>Описание</th>
</tr>
<tr class="odd">
<td><p><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></p></td>
<td><p>Объект служб удаленных рабочих СТОЛОВ <strong>записей</strong> указывает приоритет выполнения асинхронного потока, который получает данные.</p></td>
</tr>
<tr class="even">
<td><p><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></p></td>
<td><p>Указывает, когда поставщик <strong>MSDataShape</strong> повторно вычисляет статистические и вычисляемые столбцы в иерархической <strong>набора записей</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></p></td>
<td><p>Задает поля, которые можно использовать для определения конфликтов при обновлении оптимистичный строки из источника данных с помощью объекта <strong>набора записей</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></p></td>
<td><p>Указывает, будет ли метод <strong>UpdateBatch</strong> следуют неявных <strong>выполнить повторную синхронизацию</strong> метод операции и, если да, области действия этой операции.</p></td>
</tr>
<tr class="odd">
<td><p><a href="affectenum.md">AffectEnum</a></p></td>
<td><p>Указывает, какие записи, влияют операции.</p></td>
</tr>
<tr class="even">
<td><p><a href="bookmarkenum.md">BookmarkEnum</a></p></td>
<td><p>Указывает, указывающее, где следует начать операцию закладку.</p></td>
</tr>
<tr class="odd">
<td><p><a href="commandtypeenum.md">CommandTypeEnum</a></p></td>
<td><p>Указывает, как интерпретировать аргумент команды.</p></td>
</tr>
<tr class="even">
<td><p><a href="compareenum.md">CompareEnum</a></p></td>
<td><p>Задает относительное положение двух записей, представленное закладок.</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectmodeenum.md">ConnectModeEnum</a></p></td>
<td><p>Задает разрешения, доступные для изменения данных в <strong>подключения</strong>, открытие <strong>записи</strong>или указания значения для свойства <strong>режима</strong> объектов <strong>потока</strong> и <strong>запись</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="connectoptionenum.md">ConnectOptionEnum</a></p></td>
<td><p>Указывает, должен ли возвращать метод <strong>Open</strong> объекта <strong>подключения</strong> после (синхронно) или до (асинхронно) подключения.</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectpromptenum.md">ConnectPromptEnum</a></p></td>
<td><p>Указывает, следует ли отображать диалоговое окно запрашивать отсутствующие параметры при открытии подключения к источнику данных ODBC.</p></td>
</tr>
<tr class="even">
<td><p><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></p></td>
<td><p>Задает поведение метода <strong>CopyRecord</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursorlocationenum.md">CursorLocationEnum</a></p></td>
<td><p>Указывает расположение обработчика курсора.</p></td>
</tr>
<tr class="even">
<td><p><a href="cursoroptionenum.md">CursorOptionEnum</a></p></td>
<td><p>Указывает, какие функции <strong>поддерживает</strong> метод, следует проверить наличие.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursortypeenum.md">CursorTypeEnum</a></p></td>
<td><p>Указывает тип курсора, используемого в объекте <strong>набора записей</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="datatypeenum.md">DataTypeEnum</a></p></td>
<td><p>Указывает тип данных <strong>параметра</strong>, <strong>поля</strong>или <strong>Свойства</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="editmodeenum.md">EditModeEnum</a></p></td>
<td><p>Указывает состояние редактирования записи.</p></td>
</tr>
<tr class="even">
<td><p><a href="errorvalueenum.md">ErrorValueEnum</a></p></td>
<td><p>Указывает тип ADO ошибка во время выполнения.</p></td>
</tr>
<tr class="odd">
<td><p><a href="eventreasonenum.md">EventReasonEnum</a></p></td>
<td><p>Указывает причину, вызвавшего событие будет выполнена.</p></td>
</tr>
<tr class="even">
<td><p><a href="eventstatusenum.md">EventStatusEnum</a></p></td>
<td><p>Указывает текущее состояние выполнения события.</p></td>
</tr>
<tr class="odd">
<td><p><a href="executeoptionenum.md">ExecuteOptionEnum</a></p></td>
<td><p>Указывает, как поставщик должен выполнить команду.</p></td>
</tr>
<tr class="even">
<td><p><a href="fieldenum.md">FieldEnum</a></p></td>
<td><p>Задает особых полей, указанных в коллекции <strong>полей</strong> объект <strong>записи</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="fieldattributeenum.md">FieldAttributeEnum</a></p></td>
<td><p>Задает один или несколько атрибутов объекта <strong>поля</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="fieldstatusenum.md">FieldStatusEnum</a></p></td>
<td><p>Указывает состояние объекта <strong>поля</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="filtergroupenum.md">FilterGroupEnum</a></p></td>
<td><p>Указывает группу записей для фильтрации из <strong>набора записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></p></td>
<td><p>Указывает количество записей для извлечения из <strong>набора записей</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="isolationlevelenum.md">IsolationLevelEnum</a></p></td>
<td><p>Указывает уровень изоляции транзакций для объекта <strong>подключения</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></p></td>
<td><p>Указывает символ, используемый в качестве разделителя строки в объектах <strong>потока</strong> текста.</p></td>
</tr>
<tr class="odd">
<td><p><a href="locktypeenum.md">LockTypeEnum</a></p></td>
<td><p>Указывает тип блокировки, помещенные на записей во время редактирования.</p></td>
</tr>
<tr class="even">
<td><p><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></p></td>
<td><p>Указывает, какие записи должны быть возвращены на сервер.</p></td>
</tr>
<tr class="odd">
<td><p><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></p></td>
<td><p>Задает поведение объекта <strong>записи</strong> метод <strong>MoveRecord</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="objectstateenum.md">ObjectStateEnum</a></p></td>
<td><p>Указывает, является ли объект открытой или закрытой, подключение к источнику данных, выполнение команды или извлечение данных.</p></td>
</tr>
<tr class="odd">
<td><p><a href="parameterattributesenum.md">ParameterAttributesEnum</a></p></td>
<td><p>Определяет атрибуты объект <strong>параметра</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></p></td>
<td><p>Задает <strong>параметр</strong> представляет входного параметра и выходной параметр, или если параметр имеет значение, возвращаемое хранимой процедуры.</p></td>
</tr>
<tr class="odd">
<td><p><a href="persistformatenum.md">PersistFormatEnum</a></p></td>
<td><p>Задает формат для сохранения <strong>записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="positionenum.md">PositionEnum</a></p></td>
<td><p>Указывает текущую позицию указателя записи в наборе <strong>записей</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="propertyattributesenum.md">PropertyAttributesEnum</a></p></td>
<td><p>Указывает атрибуты <strong>Свойства</strong> объекта.</p></td>
</tr>
<tr class="even">
<td><p><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></p></td>
<td><p>Указывает метод <strong>Open</strong> объекта <strong>записи</strong> ли открывать существующей <strong>записи</strong> или новую <strong>запись</strong> должен быть создан.</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></p></td>
<td><p>Задает параметры открытия для <strong>записи</strong>. Эти значения можно объединять с помощью оператора OR.</p></td>
</tr>
<tr class="even">
<td><p><a href="recordstatusenum.md">RecordStatusEnum</a></p></td>
<td><p>Указывает состояние записи по отношению к пакета обновлений и других массовых операций.</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordtypeenum.md">RecordTypeEnum</a></p></td>
<td><p>Указывает тип объекта <strong>записи</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="resyncenum.md">ResyncEnum</a></p></td>
<td><p>Указывает, будут перезаписаны ли базовых значений с помощью вызова <strong>выполнить повторную синхронизацию</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="saveoptionsenum.md">SaveOptionsEnum</a></p></td>
<td><p>Указывает, создан или перезаписан при сохранении из объекта <strong>потока</strong> файла. Значения может использоваться совместно с оператора AND.</p></td>
</tr>
<tr class="even">
<td><p><a href="schemaenum.md">SchemaEnum</a></p></td>
<td><p>Указывает тип схемы <strong>OpenSchema</strong> метод извлекает <strong>набора записей</strong> . Задает направление поиска записи в наборе <strong>записей</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="searchdirectionenum.md">SearchDirectionEnum</a></p></td>
<td><p>Задает направление поиска записи в наборе <strong>записей</strong>. Указывает тип <strong>поиска</strong> для выполнения.</p></td>
</tr>
<tr class="even">
<td><p><a href="seekenum.md">SeekEnum</a></p></td>
<td><p>Указывает тип <strong>поиска</strong> для выполнения. Задает параметры открытия объект <strong>Stream</strong> . Значения может использоваться совместно с оператора AND.</p></td>
</tr>
<tr class="odd">
<td><p><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></p></td>
<td><p>Задает параметры открытия объект <strong>Stream</strong> . Значения может использоваться совместно с оператора AND. Указывает, следует ли считывать весь поток или следующую строку из объекта <strong>потока</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="streamreadenum.md">StreamReadEnum</a></p></td>
<td><p>Указывает, следует ли считывать весь поток или следующую строку из объекта <strong>потока</strong> . Указывает тип данных, сохраненных в объект <strong>потока</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="streamtypeenum.md">StreamTypeEnum</a></p></td>
<td><p>Указывает тип данных, сохраненных в объект <strong>потока</strong> . Указывает, добавлены ли разделитель к строке, записанные в объект <strong>потока</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="streamwriteenum.md">StreamWriteEnum</a></p></td>
<td><p>Указывает, добавлены ли разделитель к строке, записанные в объект <strong>потока</strong> . Задает формат при извлечении <strong>набора записей</strong> как строку.</p></td>
</tr>
<tr class="odd">
<td><p><a href="stringformatenum.md">StringFormatEnum</a></p></td>
<td><p>Задает формат при извлечении <strong>набора записей</strong> как строку. Задает атрибуты транзакций объект <strong>подключения</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="xactattributeenum.md">XactAttributeEnum</a></p></td>
<td><p>Задает атрибуты транзакций объект <strong>подключения</strong> .</p></td>
</tr>
</tbody>
</table>

