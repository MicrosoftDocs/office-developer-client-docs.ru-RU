---
title: Перечислимые константы ADO
TOCTitle: ADO enumerated constants
ms:assetid: 7c983acd-8b38-dc3c-6704-46e649ebb7d6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249522(v=office.15)
ms:contentKeyID: 48545841
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 05e5d3a77dc7db5ef5a0d81a3f13d5fc5987f5de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283410"
---
# <a name="ado-enumerated-constants"></a>Перечислимые константы ADO

**Область применения**: Access 2013, Office 2013

Для отладки в списках ADO перечисляются значения для каждой константы. Однако это значение является исключительно рекомендациями и может измениться с одного выпуска ADO на другой. Код должен зависеть только от имени, а не фактического значения каждой константы.

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>Enumerated constant</th>
<th>Описание</th>
</tr>
<tr class="odd">
<td><p><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></p></td>
<td><p>Для объекта RDS <strong>Recordset</strong> указывает приоритет выполнения асинхронного потока, который извлекает данные.</p></td>
</tr>
<tr class="even">
<td><p><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></p></td>
<td><p>Указывает, когда поставщик <strong>MSDataShape</strong> повторно вычисляет сводные и вычисляемые столбцы в иерархическом <strong>наборе записей.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></p></td>
<td><p>Указывает, какие поля можно использовать для обнаружения конфликтов во время оптимистичного обновления строки источника данных с <strong>объектом Recordset.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></p></td>
<td><p>Указывает, следует ли за <strong>методом UpdateBatch</strong> неявную операцию метода <strong>Resync</strong> и, если да, область этой операции.</p></td>
</tr>
<tr class="odd">
<td><p><a href="affectenum.md">AffectEnum</a></p></td>
<td><p>Указывает, на какие записи влияет операция.</p></td>
</tr>
<tr class="even">
<td><p><a href="bookmarkenum.md">BookmarkEnum</a></p></td>
<td><p>Указывает закладку, указывающее место начала операции.</p></td>
</tr>
<tr class="odd">
<td><p><a href="commandtypeenum.md">CommandTypeEnum</a></p></td>
<td><p>Указывает, как следует интерпретировать аргумент команды.</p></td>
</tr>
<tr class="even">
<td><p><a href="compareenum.md">CompareEnum</a></p></td>
<td><p>Указывает относительное положение двух записей, представленных закладки.</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectmodeenum.md">ConnectModeEnum</a></p></td>
<td><p>Указывает доступные разрешения для изменения данных в <strong>connection,</strong>открытия записи или указания значений для свойства <strong>Mode</strong> объектов <strong>Record</strong> и <strong>Stream.</strong> <strong></strong></p></td>
</tr>
<tr class="even">
<td><p><a href="connectoptionenum.md">ConnectOptionEnum</a></p></td>
<td><p>Указывает, должен ли метод <strong>Open</strong> объекта <strong>Connection</strong> возвращаться после (синхронно) или до (асинхронно) подключения.</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectpromptenum.md">ConnectPromptEnum</a></p></td>
<td><p>Указывает, должно ли отображаться диалоговое окно с запросом отсутствующих параметров при открытии подключения к источнику данных ODBC.</p></td>
</tr>
<tr class="even">
<td><p><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></p></td>
<td><p>Указывает поведение метода <strong>CopyRecord.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="cursorlocationenum.md">CursorLocationEnum</a></p></td>
<td><p>Указывает расположение курсора.</p></td>
</tr>
<tr class="even">
<td><p><a href="cursoroptionenum.md">CursorOptionEnum</a></p></td>
<td><p>Указывает, для каких <strong></strong> функций должен тестироваться метод Supports.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursortypeenum.md">CursorTypeEnum</a></p></td>
<td><p>Указывает тип курсора, используемого в <strong>объекте Recordset.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="datatypeenum.md">DataTypeEnum</a></p></td>
<td><p>Указывает тип данных <strong>поля,</strong> <strong>параметра</strong>или <strong>свойства.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="editmodeenum.md">EditModeEnum</a></p></td>
<td><p>Указывает состояние редактирования записи.</p></td>
</tr>
<tr class="even">
<td><p><a href="errorvalueenum.md">ErrorValueEnum</a></p></td>
<td><p>Указывает тип ошибки во время работы ADO.</p></td>
</tr>
<tr class="odd">
<td><p><a href="eventreasonenum.md">EventReasonEnum</a></p></td>
<td><p>Указывает причину возникновения события.</p></td>
</tr>
<tr class="even">
<td><p><a href="eventstatusenum.md">EventStatusEnum</a></p></td>
<td><p>Указывает текущее состояние выполнения события.</p></td>
</tr>
<tr class="odd">
<td><p><a href="executeoptionenum.md">ExecuteOptionEnum</a></p></td>
<td><p>Указывает, как поставщик должен выполнять команду.</p></td>
</tr>
<tr class="even">
<td><p><a href="fieldenum.md">FieldEnum</a></p></td>
<td><p>Указывает специальные поля, на которые ссылается коллекция <strong>Fields</strong> объекта <strong>Record.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="fieldattributeenum.md">FieldAttributeEnum</a></p></td>
<td><p>Указывает один или несколько атрибутов объекта <strong>Field.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="fieldstatusenum.md">FieldStatusEnum</a></p></td>
<td><p>Указывает состояние объекта <strong>Field.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="filtergroupenum.md">FilterGroupEnum</a></p></td>
<td><p>Указывает группу записей, которые необходимо отфильтровать из <strong>наборов записей.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></p></td>
<td><p>Указывает количество записей, извлекаемого из <strong>recordset.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="isolationlevelenum.md">IsolationLevelEnum</a></p></td>
<td><p>Указывает уровень изоляции транзакций для объекта <strong>Connection.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></p></td>
<td><p>Указывает символ, используемый в качестве деспаратора строк в текстовых <strong>объектах Stream.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="locktypeenum.md">LockTypeEnum</a></p></td>
<td><p>Указывает тип блокировки записей во время редактирования.</p></td>
</tr>
<tr class="even">
<td><p><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></p></td>
<td><p>Указывает, какие записи должны быть возвращены на сервер.</p></td>
</tr>
<tr class="odd">
<td><p><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></p></td>
<td><p>Указывает поведение метода <strong></strong> <strong>MoveRecord</strong> объекта Record.</p></td>
</tr>
<tr class="even">
<td><p><a href="objectstateenum.md">ObjectStateEnum</a></p></td>
<td><p>Указывает, является ли объект открытым или закрытым, подключением к источнику данных, выполнением команды или извлечением данных.</p></td>
</tr>
<tr class="odd">
<td><p><a href="parameterattributesenum.md">ParameterAttributesEnum</a></p></td>
<td><p>Указывает атрибуты объекта <strong>Parameter.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></p></td>
<td><p>Указывает, является <strong></strong> ли параметр входным параметром, выходным параметром или и тем, и другим, или является ли параметр возвращаемой величиной из хранимой процедуры.</p></td>
</tr>
<tr class="odd">
<td><p><a href="persistformatenum.md">PersistFormatEnum</a></p></td>
<td><p>Указывает формат, в котором необходимо сохранить <strong>набор записей.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="positionenum.md">PositionEnum</a></p></td>
<td><p>Указывает текущую позицию указателя записи в <strong>наборе записей.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="propertyattributesenum.md">PropertyAttributesEnum</a></p></td>
<td><p>Указывает атрибуты объекта <strong>Property.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></p></td>
<td><p>Указывает для метода Open <strong>объекта</strong> <strong>Record,</strong> следует ли открывать существующую <strong></strong> запись или создавать новую запись. <strong></strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></p></td>
<td><p>Указывает параметры открытия <strong>записи.</strong> Эти значения могут быть объединены с помощью оператора OR.</p></td>
</tr>
<tr class="even">
<td><p><a href="recordstatusenum.md">RecordStatusEnum</a></p></td>
<td><p>Указывает состояние записи в отношении пакетных обновлений и других массовых операций.</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordtypeenum.md">RecordTypeEnum</a></p></td>
<td><p>Указывает тип объекта <strong>Record.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="resyncenum.md">ResyncEnum</a></p></td>
<td><p>Указывает, перезаписываются ли значения в результате вызова <strong>Resync.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="saveoptionsenum.md">SaveOptionsEnum</a></p></td>
<td><p>Указывает, следует ли создавать или перезаписывать файл при сохранении из <strong>объекта Stream.</strong> Значения можно объединить с оператором AND.</p></td>
</tr>
<tr class="even">
<td><p><a href="schemaenum.md">SchemaEnum</a></p></td>
<td><p>Указывает тип наборов <strong>записей</strong> схемы, извлекаемого <strong>методом OpenSchema.</strong> Указывает направление поиска записей в <strong>наборе записей.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="searchdirectionenum.md">SearchDirectionEnum</a></p></td>
<td><p>Указывает направление поиска записей в <strong>наборе записей.</strong> Указывает тип seek <strong>для</strong> выполнения.</p></td>
</tr>
<tr class="even">
<td><p><a href="seekenum.md">SeekEnum</a></p></td>
<td><p>Указывает тип seek <strong>для</strong> выполнения. Указывает параметры открытия объекта <strong>Stream.</strong> Значения можно объединить с оператором AND.</p></td>
</tr>
<tr class="odd">
<td><p><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></p></td>
<td><p>Указывает параметры открытия объекта <strong>Stream.</strong> Значения можно объединить с оператором AND. Указывает, следует ли читать весь поток или следующую строку из <strong>объекта Stream.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="streamreadenum.md">StreamReadEnum</a></p></td>
<td><p>Указывает, следует ли читать весь поток или следующую строку из <strong>объекта Stream.</strong> Указывает тип данных, хранимых в <strong>объекте Stream.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="streamtypeenum.md">StreamTypeEnum</a></p></td>
<td><p>Указывает тип данных, хранимых в <strong>объекте Stream.</strong> Указывает, будет ли к строке, записанной в объект Stream, будет ли к строке, записанной в <strong>объект Stream, будет ли сепаратор строки.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="streamwriteenum.md">StreamWriteEnum</a></p></td>
<td><p>Указывает, будет ли к строке, записанной в объект Stream, будет ли к строке, записанной в <strong>объект Stream, будет ли сепаратор строки.</strong> Указывает формат при искомом наборе <strong>записей в</strong> виде строки.</p></td>
</tr>
<tr class="odd">
<td><p><a href="stringformatenum.md">StringFormatEnum</a></p></td>
<td><p>Указывает формат при искомом наборе <strong>записей в</strong> виде строки. Указывает атрибуты транзакции объекта <strong>Connection.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="xactattributeenum.md">XactAttributeEnum</a></p></td>
<td><p>Указывает атрибуты транзакции объекта <strong>Connection.</strong></p></td>
</tr>
</tbody>
</table>

