---
title: FieldStatusEnum (Ссылка на настольные базы данных)
TOCTitle: FieldStatusEnum
ms:assetid: 49570042-8435-8618-3ba1-7006c47735e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249225(v=office.15)
ms:contentKeyID: 48544635
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ccf98f2a740e2a077d6e2451102bfc72bcd1b40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292519"
---
# <a name="fieldstatusenum"></a>FieldStatusEnum

**Область применения**: Access 2013, Office 2013

Указывает состояние объекта **Field.**

Значения **adFieldPending указывают \*** на операцию, которая вызвала задание состояния, и может быть совмещена с другими значениями состояния.

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
<td><p>Указывает, что указанное поле уже существует.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldBadStatus</strong></p></td>
<td><p>12 </p></td>
<td><p>Указывает, что значение недействительных статусов было отправлено из ADO поставщику OLE DB. Возможные причины включают поставщик OLE DB 1.0 или 1.1 или неправильное сочетание <a href="value-property-ado.md">значения и</a> <a href="status-property-ado-field.md">состояния.</a></p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldCannotComplete</strong></p></td>
<td><p>20</p></td>
<td><p>Указывает, что сервер URL-адреса, заданного <a href="source-property-ado-record.md">Source,</a> не смог завершить операцию.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldCannotDeleteSource</strong></p></td>
<td><p>23</p></td>
<td><p>Указывает, что во время операции перемещения дерево или подтрий перемещалось в новое расположение, но не удалось удалить источник.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldCantConvertValue</strong></p></td>
<td><p>2</p></td>
<td><p>Указывает, что поле не может быть извлечено или сохранено без потери данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldCantCreate</strong></p></td>
<td><p>7 </p></td>
<td><p>Указывает, что поле не может быть добавлено, так как поставщик превысил ограничение (например, количество разрешенных полей).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldDataOverflow</strong></p></td>
<td><p>6 </p></td>
<td><p>Указывает, что данные, возвращающиеся от поставщика, переполнили тип данных поля.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldDefault</strong></p></td>
<td><p>13</p></td>
<td><p>Указывает, что значение по умолчанию для поля использовалось при настройке данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldDoesNotExist</strong></p></td>
<td><p>16 </p></td>
<td><p>Указывает, что указанное поле не существует.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldIgnore</strong></p></td>
<td><p>15</p></td>
<td><p>Указывает, что это поле было пропущено при настройке значений данных в источнике. Поставщик не устанавливал значения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldIntegrityViolation</strong></p></td>
<td><p>10 </p></td>
<td><p>Указывает, что поле не может быть изменено, так как это вычисляемая или полученная сущность.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldInvalidURL</strong></p></td>
<td><p>17 </p></td>
<td><p>Указывает, что URL-адрес источника данных содержит недопустимые символы.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldIsNull</strong></p></td>
<td><p>3</p></td>
<td><p>Указывает, что поставщик вернул значение VARIANT типа VT_NULL и поле не пустое.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldOK</strong></p></td>
<td><p>0</p></td>
<td><p>Значение, используемое по умолчанию. Указывает, что поле было успешно добавлено или удалено.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldOutOfSpace</strong></p></td>
<td><p>22</p></td>
<td><p>Указывает, что поставщик не может получить достаточно места для хранения для выполнения операции перемещения или копирования.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldPendingChange</strong></p></td>
<td><p>0x40000</p></td>
<td><p>Указывает либо на то, что поле было удалено, а затем добавлено повторно, возможно, с другим типом данных, либо что значение поля, которое ранее было состоянием adFieldOK, изменилось. Окончательная форма поля изменит коллекцию <a href="fields-collection-ado.md">Полей</a> после того, как будет вызван метод <a href="update-method-ado.md">Update.</a></p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldPendingDelete</strong></p></td>
<td><p>0x20000</p></td>
<td><p>Указывает на то, что операция <strong>Удаление</strong> привела к набору состояния. Поле было отмечено для удаления из коллекции <strong>Fields</strong> после того, как будет вызван метод <strong>Update.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldPendingInsert</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Указывает, что <strong>операция Приложения</strong> привела к заданию состояния. Поле <strong>было</strong> отмечено, что будет добавлено в коллекцию <strong>Fields</strong> после того, как будет вызван метод <strong>Update.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldPendingUnknown</strong></p></td>
<td><p>0x80000</p></td>
<td><p>Указывает, что поставщик не может определить, какая операция вызвала заопредельное состояние поля.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldPendingUnknownDelete</strong></p></td>
<td><p>0x100000</p></td>
<td><p>Указывает, что поставщик не может определить, какая операция вызвала заочное состояние поля, и что поле будет удалено из коллекции <strong>Fields</strong> после того, как будет вызван метод <strong>Update.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldPermissionDenied</strong></p></td>
<td><p>9 </p></td>
<td><p>Указывает, что поле не может быть изменено, так как оно определяется только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldReadOnly</strong></p></td>
<td><p>24</p></td>
<td><p>Указывает, что поле в источнике данных определяется как только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldResourceExists</strong></p></td>
<td><p>19</p></td>
<td><p>Указывает, что поставщик не смог выполнить операцию, так как объект уже существует в URL-адресе назначения и не может переписать объект.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldResourceLocked</strong></p></td>
<td><p>18 </p></td>
<td><p>Указывает, что поставщик не смог выполнить операцию, так как источник данных заблокирован одним или более другим приложением или процессом.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldResourceOutOfScope</strong></p></td>
<td><p>25</p></td>
<td><p>Указывает, что URL-адрес источника или адреса не является областью текущей записи.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldSchemaViolation</strong></p></td>
<td><p>11</p></td>
<td><p>Указывает, что значение нарушило ограничение схемы источника данных для поля.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldSignMismatch</strong></p></td>
<td><p>5 </p></td>
<td><p>Указывает, что значение данных, возвращенное поставщиком, было подписано, но тип данных значения поля ADO был не подписан.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldTruncated</strong></p></td>
<td><p>4 </p></td>
<td><p>Указывает, что данные переменной длины были усечены при чтении из источника данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldUnavailable</strong></p></td>
<td><p>8 </p></td>
<td><p>Указывает, что поставщик не мог определить значение при чтении из источника данных. Например, строка только что была создана, значение по умолчанию для столбца было недоступным, а новое значение еще не было задано.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldVolumeNotFound</strong></p></td>
<td><p>21</p></td>
<td><p>Указывает, что поставщик не может найти объем хранилища, указанный URL-адресом.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы не имеют эквивалентов ADO/WFC.

