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

Для облегчения отладки перечисление ADO перечислит значения для каждой константы. Однако это значение является исключительно рекомендацией и может изменяться от одного выпуска ADO к другому. Код должен зависеть только от имени (а не фактического значения) каждой перечислимой константы.

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>Перечислимая константа</th>
<th>Описание</th>
</tr>
<tr class="odd">
<td><p><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></p></td>
<td><p>Для объекта <strong>RECORDSET</strong> RDS указывает приоритет выполнения асинхронного потока, который получает данные.</p></td>
</tr>
<tr class="even">
<td><p><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></p></td>
<td><p>Указывает, когда поставщик <strong>мсдаташапе</strong> выполняет повторное вычисление статистических и вычисляемых столбцов в иерархическом <strong>наборе записей</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></p></td>
<td><p>Указывает, какие поля можно использовать для обнаружения конфликтов во время оптимистического обновления строки источника данных с помощью объекта <strong>Recordset</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></p></td>
<td><p>Указывает, следует ли метод <strong>UpdateBatch</strong> выполнить неявную операцию метода <strong>Resync</strong> и, если это так, область этой операции.</p></td>
</tr>
<tr class="odd">
<td><p><a href="affectenum.md">AffectEnum</a></p></td>
<td><p>Указывает, какие записи затрагиваются операцией.</p></td>
</tr>
<tr class="even">
<td><p><a href="bookmarkenum.md">BookmarkEnum</a></p></td>
<td><p>Указывает на закладку, указывающую, где должна начинаться операция.</p></td>
</tr>
<tr class="odd">
<td><p><a href="commandtypeenum.md">CommandTypeEnum</a></p></td>
<td><p>Указывает, как должен интерпретироваться аргумент команды.</p></td>
</tr>
<tr class="even">
<td><p><a href="compareenum.md">CompareEnum</a></p></td>
<td><p>Задает относительное положение двух записей, представленных в закладках.</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectmodeenum.md">ConnectModeEnum</a></p></td>
<td><p>Указывает доступные разрешения для изменения данных в <strong>подключении</strong>, открытия <strong>записи</strong>или указания значений для свойства <strong>mode</strong> объектов <strong>Record</strong> и <strong>Stream</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="connectoptionenum.md">ConnectOptionEnum</a></p></td>
<td><p>Указывает, должен ли метод <strong>Open</strong> объекта <strong>Connection</strong> возвращаться (синхронно) или до (асинхронно) подключения.</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectpromptenum.md">ConnectPromptEnum</a></p></td>
<td><p>Указывает, следует ли отображать диалоговое окно с запросом на отсутствие параметров при открытии подключения к источнику данных ODBC.</p></td>
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
<td><p>Определяет, для каких функциональных возможностей метод <strong>поддерживает</strong> проверку.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursortypeenum.md">CursorTypeEnum</a></p></td>
<td><p>Указывает тип курсора, используемого в объекте <strong>Recordset</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="datatypeenum.md">DataTypeEnum</a></p></td>
<td><p>Указывает тип данных <strong>поля</strong>, <strong>параметра</strong>или <strong>Свойства</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="editmodeenum.md">EditModeEnum</a></p></td>
<td><p>Задает состояние редактирования записи.</p></td>
</tr>
<tr class="even">
<td><p><a href="errorvalueenum.md">ErrorValueEnum</a></p></td>
<td><p>Задает тип ошибки времени выполнения ADO.</p></td>
</tr>
<tr class="odd">
<td><p><a href="eventreasonenum.md">EventReasonEnum</a></p></td>
<td><p>Указывает причину, по которой возникло событие.</p></td>
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
<td><p>Указывает специальные поля, указанные в коллекции <strong>Fields</strong> объекта <strong>Record</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="fieldattributeenum.md">FieldAttributeEnum</a></p></td>
<td><p>Задает один или несколько атрибутов объекта <strong>field</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="fieldstatusenum.md">FieldStatusEnum</a></p></td>
<td><p>Задает состояние объекта <strong>field</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="filtergroupenum.md">FilterGroupEnum</a></p></td>
<td><p>Задает группу записей для фильтрации из <strong>набора записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></p></td>
<td><p>Указывает количество записей, извлекаемых из <strong>набора записей</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="isolationlevelenum.md">IsolationLevelEnum</a></p></td>
<td><p>Задает уровень изоляции транзакции для объекта <strong>подключения</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></p></td>
<td><p>Указывает символ, используемый в качестве разделителя строк в текстовых объектах <strong>потока</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="locktypeenum.md">LockTypeEnum</a></p></td>
<td><p>Указывает тип блокировки, помещаемой в записи во время редактирования.</p></td>
</tr>
<tr class="even">
<td><p><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></p></td>
<td><p>Указывает, какие записи должны возвращаться на сервер.</p></td>
</tr>
<tr class="odd">
<td><p><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></p></td>
<td><p>Задает поведение метода <strong>MoveRecord</strong> объекта <strong>Record</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="objectstateenum.md">ObjectStateEnum</a></p></td>
<td><p>Указывает, является ли объект открытым или закрытым, подключается к источнику данных, выполняя команду или извлечение данных.</p></td>
</tr>
<tr class="odd">
<td><p><a href="parameterattributesenum.md">ParameterAttributesEnum</a></p></td>
<td><p>Задает атрибуты объекта <strong>Parameter</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></p></td>
<td><p>Указывает, представляет ли <strong>параметр</strong> входной параметр, выходной параметр или и то, и другое, если параметр является возвращаемым значением из хранимой процедуры.</p></td>
</tr>
<tr class="odd">
<td><p><a href="persistformatenum.md">PersistFormatEnum</a></p></td>
<td><p>Задает формат, в котором будет сохранен <strong>набор записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="positionenum.md">PositionEnum</a></p></td>
<td><p>Задает текущее положение указателя записи в <strong>наборе записей</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="propertyattributesenum.md">PropertyAttributesEnum</a></p></td>
<td><p>Задает атрибуты объекта <strong>Property</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></p></td>
<td><p>Указывает, следует ли открыть существующую <strong>запись</strong> в методе <strong>Open</strong> объекта <strong>Record</strong> или создать новую <strong>запись</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></p></td>
<td><p>Задает параметры открытия <strong>записи</strong>. Эти значения можно объединять с помощью оператора OR.</p></td>
</tr>
<tr class="even">
<td><p><a href="recordstatusenum.md">RecordStatusEnum</a></p></td>
<td><p>Указывает состояние записи по отношению к пакетным обновлениям и другим массовым операциям.</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordtypeenum.md">RecordTypeEnum</a></p></td>
<td><p>Указывает тип объекта <strong>Record</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="resyncenum.md">ResyncEnum</a></p></td>
<td><p>Указывает, перезаписываются ли базовые значения при вызове метода повторной <strong>синхронизации</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="saveoptionsenum.md">SaveOptionsEnum</a></p></td>
<td><p>Указывает, следует ли создать или перезаписать файл при сохранении из объекта <strong>Stream</strong> . Значения можно сочетать с помощью оператора AND.</p></td>
</tr>
<tr class="even">
<td><p><a href="schemaenum.md">SchemaEnum</a></p></td>
<td><p>Указывает тип <strong>набора записей</strong> схемы, извлекаемый методом <strong>OpenSchema</strong> . Задает направление поиска записи в <strong>наборе записей</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="searchdirectionenum.md">SearchDirectionEnum</a></p></td>
<td><p>Задает направление поиска записи в <strong>наборе записей</strong>. Указывает тип выполняемого <strong>поиска</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="seekenum.md">SeekEnum</a></p></td>
<td><p>Указывает тип выполняемого <strong>поиска</strong> . Задает параметры открытия объекта <strong>Stream</strong> . Значения можно сочетать с помощью оператора AND.</p></td>
</tr>
<tr class="odd">
<td><p><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></p></td>
<td><p>Задает параметры открытия объекта <strong>Stream</strong> . Значения можно сочетать с помощью оператора AND. Указывает, следует ли считывать весь поток или следующую строку из объекта <strong>Stream</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="streamreadenum.md">StreamReadEnum</a></p></td>
<td><p>Указывает, следует ли считывать весь поток или следующую строку из объекта <strong>Stream</strong> . Указывает тип данных, хранящихся в объекте <strong>Stream</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="streamtypeenum.md">StreamTypeEnum</a></p></td>
<td><p>Указывает тип данных, хранящихся в объекте <strong>Stream</strong> . Указывает, добавляется ли разделитель строк в строку, записанную в объект <strong>Stream</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="streamwriteenum.md">StreamWriteEnum</a></p></td>
<td><p>Указывает, добавляется ли разделитель строк в строку, записанную в объект <strong>Stream</strong> . Задает формат при получении объекта <strong>Recordset</strong> в виде строки.</p></td>
</tr>
<tr class="odd">
<td><p><a href="stringformatenum.md">StringFormatEnum</a></p></td>
<td><p>Задает формат при получении объекта <strong>Recordset</strong> в виде строки. Задает атрибуты транзакции для объекта <strong>Connection</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="xactattributeenum.md">XactAttributeEnum</a></p></td>
<td><p>Задает атрибуты транзакции для объекта <strong>Connection</strong> .</p></td>
</tr>
</tbody>
</table>

