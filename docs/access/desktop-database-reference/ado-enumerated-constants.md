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

Чтобы помочь в отладке, перечисляния ADO перечисляют значение для каждой константы. Однако это значение носит чисто консультативный характер и может изменяться с одного выпуска ADO на другой. Код должен зависеть только от имени, а не от фактического значения каждой из перенамеренных констант.

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>Константа с перемерами</th>
<th>Description</th>
</tr>
<tr class="odd">
<td><p><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></p></td>
<td><p>Для объекта RDS <strong>Recordset</strong> указывается приоритет выполнения асинхронного потока, который извлекает данные.</p></td>
</tr>
<tr class="even">
<td><p><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></p></td>
<td><p>Указывает, когда <strong>поставщик MSDataShape</strong> повторно вычисляет совокупные и рассчитанные столбцы в иерархическом <strong>наборе записей.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></p></td>
<td><p>Указывает, какие поля можно использовать для обнаружения конфликтов при оптимистичном обновлении строки источника данных с объектом <strong>Recordset.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></p></td>
<td><p>Указывает, следует ли <strong>методу UpdateBatch</strong> неявная операция <strong>метода Resync</strong> и если да, то область этой операции.</p></td>
</tr>
<tr class="odd">
<td><p><a href="affectenum.md">AffectEnum</a></p></td>
<td><p>Указывает, на какие записи влияет операция.</p></td>
</tr>
<tr class="even">
<td><p><a href="bookmarkenum.md">BookmarkEnum</a></p></td>
<td><p>Указывает закладки, указывающие, где должна начаться операция.</p></td>
</tr>
<tr class="odd">
<td><p><a href="commandtypeenum.md">CommandTypeEnum</a></p></td>
<td><p>Указывает, как следует интерпретировать аргумент команды.</p></td>
</tr>
<tr class="even">
<td><p><a href="compareenum.md">CompareEnum</a></p></td>
<td><p>Указывает относительное положение двух записей, представленных их закладки.</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectmodeenum.md">ConnectModeEnum</a></p></td>
<td><p>Указывает доступные разрешения на изменение данных в <strong>подключениях,</strong>открытие записи <strong>или</strong>указание значений для свойства <strong>Mode</strong> объектов <strong>Record</strong> и <strong>Stream.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="connectoptionenum.md">ConnectOptionEnum</a></p></td>
<td><p>Указывает, должен <strong></strong> ли открытый метод объекта <strong>Подключения</strong> возвращаться после (синхронно) или до (асинхронно) подключения.</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectpromptenum.md">ConnectPromptEnum</a></p></td>
<td><p>Указывает, следует ли отображать диалоговое окно для запроса отсутствующих параметров при открытии подключения к источнику данных ODBC.</p></td>
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
<td><p>Указывает тип ошибки времени работы ADO.</p></td>
</tr>
<tr class="odd">
<td><p><a href="eventreasonenum.md">EventReasonEnum</a></p></td>
<td><p>Указывает причину, по которой произошло событие.</p></td>
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
<td><p>Указывает специальные поля, на которые ссылается коллекция <strong>Полей</strong> объекта <strong>Record.</strong></p></td>
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
<td><p>Указывает группу записей, которые необходимо отфильтровать из <strong>recordset.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></p></td>
<td><p>Указывает количество записей, которые необходимо получить из <strong>recordset.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="isolationlevelenum.md">IsolationLevelEnum</a></p></td>
<td><p>Указывает уровень изоляции транзакций для объекта <strong>Подключения.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></p></td>
<td><p>Указывает символ, используемый в качестве сепаратора строк в текстовых объектах <strong>Stream.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="locktypeenum.md">LockTypeEnum</a></p></td>
<td><p>Указывает тип блокировки, размещаемой на записях во время редактирования.</p></td>
</tr>
<tr class="even">
<td><p><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></p></td>
<td><p>Указывает, какие записи следует возвращать на сервер.</p></td>
</tr>
<tr class="odd">
<td><p><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></p></td>
<td><p>Указывает поведение метода <strong>Объекта</strong> <strong>Записи MoveRecord.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="objectstateenum.md">ObjectStateEnum</a></p></td>
<td><p>Указывает, открыт ли объект или закрыт, подключение к источнику данных, выполнение команды или извлечение данных.</p></td>
</tr>
<tr class="odd">
<td><p><a href="parameterattributesenum.md">ParameterAttributesEnum</a></p></td>
<td><p>Указывает атрибуты объекта <strong>Parameter.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></p></td>
<td><p>Указывает, является ли <strong>параметр</strong> параметром ввода, выходным параметром или и тем, и другим, или параметром является возвращаемая величина из сохраненной процедуры.</p></td>
</tr>
<tr class="odd">
<td><p><a href="persistformatenum.md">PersistFormatEnum</a></p></td>
<td><p>Указывает формат, в котором можно сохранить <strong>набор записей.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="positionenum.md">PositionEnum</a></p></td>
<td><p>Указывает текущее положение указателя записи в <strong>Наборе записей.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="propertyattributesenum.md">PropertyAttributesEnum</a></p></td>
<td><p>Указывает атрибуты объекта <strong>Property.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></p></td>
<td><p>Указывает для метода <strong></strong> <strong>Открыть объект Запись,</strong> следует ли открывать существующую <strong></strong> запись или создавать новую запись. <strong></strong></p></td>
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
<td><p>Указывает, перезаписываются ли значения по вызову <strong>в Resync.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="saveoptionsenum.md">SaveOptionsEnum</a></p></td>
<td><p>Указывает, следует ли создавать или перезаписывать файл при сохранении объекта <strong>Stream.</strong> Эти значения можно комбинировать с оператором AND.</p></td>
</tr>
<tr class="even">
<td><p><a href="schemaenum.md">SchemaEnum</a></p></td>
<td><p>Указывает тип схемы <strong>Recordset,</strong> который извлекает метод <strong>OpenSchema.</strong> Указывает направление поиска записи в <strong>Наборе записей.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="searchdirectionenum.md">SearchDirectionEnum</a></p></td>
<td><p>Указывает направление поиска записи в <strong>Наборе записей.</strong> Указывает тип <strong>поиска</strong> для выполнения.</p></td>
</tr>
<tr class="even">
<td><p><a href="seekenum.md">SeekEnum</a></p></td>
<td><p>Указывает тип <strong>поиска</strong> для выполнения. Указывает параметры открытия объекта <strong>Stream.</strong> Эти значения можно комбинировать с оператором AND.</p></td>
</tr>
<tr class="odd">
<td><p><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></p></td>
<td><p>Указывает параметры открытия объекта <strong>Stream.</strong> Эти значения можно комбинировать с оператором AND. Указывает, следует ли читать весь поток или следующую строку с объекта <strong>Stream.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="streamreadenum.md">StreamReadEnum</a></p></td>
<td><p>Указывает, следует ли читать весь поток или следующую строку с объекта <strong>Stream.</strong> Указывает тип данных, хранимых в <strong>объекте Stream.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="streamtypeenum.md">StreamTypeEnum</a></p></td>
<td><p>Указывает тип данных, хранимых в <strong>объекте Stream.</strong> Указывает, пристроен ли сепаратор строки к строке, написанной к объекту <strong>Stream.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="streamwriteenum.md">StreamWriteEnum</a></p></td>
<td><p>Указывает, пристроен ли сепаратор строки к строке, написанной к объекту <strong>Stream.</strong> Указывает формат при искомом <strong>наборе записей</strong> в виде строки.</p></td>
</tr>
<tr class="odd">
<td><p><a href="stringformatenum.md">StringFormatEnum</a></p></td>
<td><p>Указывает формат при искомом <strong>наборе записей</strong> в виде строки. Указывает атрибуты транзакции объекта <strong>Подключения.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="xactattributeenum.md">XactAttributeEnum</a></p></td>
<td><p>Указывает атрибуты транзакции объекта <strong>Подключения.</strong></p></td>
</tr>
</tbody>
</table>

