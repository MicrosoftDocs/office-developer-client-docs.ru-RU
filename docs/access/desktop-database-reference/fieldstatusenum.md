---
title: FieldStatusEnum (Справочник по для настольных баз данных Access)
TOCTitle: FieldStatusEnum
ms:assetid: 49570042-8435-8618-3ba1-7006c47735e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249225(v=office.15)
ms:contentKeyID: 48544635
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 22c5d53427d1380273ea82b3a28ae044e103b179
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860611"
---
# <a name="fieldstatusenum"></a>FieldStatusEnum

**Применимо к**: Access 2013 | Office 2013

Указывает состояние объекта **поля** .

**AdFieldPending\* ** , то это означает операцию, которая вызвала состояние нужно задать и может использоваться в сочетании с другими значения состояния.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adFieldAlreadyExists</strong></p></td>
<td><p>26</p></td>
<td><p>Указывает, что указанного поля уже существует.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldBadStatus</strong></p></td>
<td><p>12</p></td>
<td><p>Указывает, что значение недопустимый статус был отправлен ADO для поставщика OLE DB. Возможные причины OLE DB 1.0 или 1.1 поставщика или неправильное сочетание <a href="value-property-ado.md">значения</a> и <a href="status-property-ado-field.md">состояние</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldCannotComplete</strong></p></td>
<td><p>20</p></td>
<td><p>Указывает, что сервер URL-адрес, указанный с <a href="source-property-ado-record.md">источника</a> не удалось завершить операцию.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldCannotDeleteSource</strong></p></td>
<td><p>23</p></td>
<td><p>Указывает, что во время операции перемещения дерево или поддерево был перемещен в новое место, но не удалось удалить источник.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldCantConvertValue</strong></p></td>
<td><p>2</p></td>
<td><p>Указывает поля извлекается или хранятся без потери данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldCantCreate</strong></p></td>
<td><p>7</p></td>
<td><p>Указывает, что поле не удается добавить так как поставщик превысила ограничение (например, допустимое число полей).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldDataOverflow</strong></p></td>
<td><p>6</p></td>
<td><p>Указывает, что данные, возвращаемые от поставщика переполнена тип данных поля.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldDefault</strong></p></td>
<td><p>13</p></td>
<td><p>Указывает, что значение по умолчанию для поля было использовано при задании данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldDoesNotExist</strong></p></td>
<td><p>16</p></td>
<td><p>Указывает, что поле не существует.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldIgnore</strong></p></td>
<td><p>15</p></td>
<td><p>Указывает, что это поле была пропущена при значения параметра данных в источнике. Поставщик значение Нет.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldIntegrityViolation</strong></p></td>
<td><p>10</p></td>
<td><p>Указывает, что поле нельзя изменить, так как они вычисляемые или производные сущности.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldInvalidURL</strong></p></td>
<td><p>17</p></td>
<td><p>Указывает, что URL-адрес источника данных содержит недопустимые символы.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldIsNull</strong></p></td>
<td><p>3</p></td>
<td><p>Указывает, что поставщик возвращаемое значение типа VARIANT типа VT_NULL и поле не является пустым.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldOK</strong></p></td>
<td><p>0</p></td>
<td><p>Значение, используемое по умолчанию. Указывает, что поле было успешно добавлено или удалено.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldOutOfSpace</strong></p></td>
<td><p>22</p></td>
<td><p>Указывает, что поставщик не удается получить достаточно дискового пространства для выполнения перемещения или копирования операции.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldPendingChange</strong></p></td>
<td><p>0x40000</p></td>
<td><p>Указывает, что поле удаленного и затем повторно добавлена, возможно, с другой тип данных, либо, что значение поля, который ранее нахождения в состоянии adFieldOK был изменен. После вызова метода <a href="update-method-ado.md">Update</a> окончательной форме поле будет изменять коллекции <a href="fields-collection-ado.md">полей</a> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldPendingDelete</strong></p></td>
<td><p>0x20000</p></td>
<td><p>Указывает, что операция <strong>удаления</strong> привело состояние должно быть задано. Поле был помечен для удаления из коллекции <strong>полей</strong> после вызова метода <strong>Update</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldPendingInsert</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Указывает, что операции <strong>добавления</strong> привело состояние должно быть задано. В <strong>поле</strong> был помечен для добавления в коллекцию <strong>полей</strong> после вызова метода <strong>Update</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldPendingUnknown</strong></p></td>
<td><p>0x80000</p></td>
<td><p>Указывает, что поставщик может определить, какие вызвало поле Состояние операции должно быть задано.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldPendingUnknownDelete</strong></p></td>
<td><p>0x100000</p></td>
<td><p>Указывает, что поставщик не может определить, какие операции, возникающие состояние поля должно быть задано и что поля будут удалены из коллекции <strong>полей</strong> , после вызова метода <strong>Update</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldPermissionDenied</strong></p></td>
<td><p>9</p></td>
<td><p>Указывает, что поле нельзя изменить, так как оно определяется только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldReadOnly</strong></p></td>
<td><p>24</p></td>
<td><p>Указывает, что поля в источнике данных только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldResourceExists</strong></p></td>
<td><p>19</p></td>
<td><p>Указывает, что поставщик не удалось выполнить операцию, поскольку объект уже существует в URL-адрес конечного и не удается перезаписать объекта.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldResourceLocked</strong></p></td>
<td><p>18</p></td>
<td><p>Указывает, что поставщик не удалось выполнить операцию, так как источник данных заблокирован один или несколько других приложений или процессом.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldResourceOutOfScope</strong></p></td>
<td><p>25</p></td>
<td><p>Указывает, что URL-адрес источника и назначения выходят за рамки текущей записи.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldSchemaViolation</strong></p></td>
<td><p>11</p></td>
<td><p>Указывает, что значение нарушает ограничения схемы источника данных для поля.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldSignMismatch</strong></p></td>
<td><p>5</p></td>
<td><p>Указывает, что подписанных данных значение, возвращаемое поставщиком, но тип данных значения поля ADO не был подписан.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldTruncated</strong></p></td>
<td><p>4</p></td>
<td><p>Указывает, что данные переменной длины усечено при чтении из источника данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldUnavailable</strong></p></td>
<td><p>8</p></td>
<td><p>Указывает, что поставщик не удается определить значение при чтении из источника данных. Например строку только что был создан, значение по умолчанию для столбца были недоступны и новое значение было еще не был указан.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldVolumeNotFound</strong></p></td>
<td><p>21</p></td>
<td><p>Указывает, что поставщик не удается найти тома хранилища, указанный в параметре URL-адрес.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы нет ADO/WFC эквивалентами.

