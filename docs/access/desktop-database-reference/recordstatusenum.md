---
title: RecordStatusEnum (Справочник по для настольных баз данных Access)
TOCTitle: RecordStatusEnum
ms:assetid: 302915b8-494d-0be2-6dce-eaf91a0ea8ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249080(v=office.15)
ms:contentKeyID: 48544022
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 88929ced56583316c42f2d5195054e51e98a1d5b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481169"
---
# <a name="recordstatusenum"></a>RecordStatusEnum


**Применимо к**: Access 2013 | Office 2013

Указывает состояние записи по отношению к пакета обновлений и других массовых операций.

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
<td><p><strong>adRecCanceled</strong></p></td>
<td><p>0x100</p></td>
<td><p>Указывает, что запись не была сохранена, так как операция отменена.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecCantRelease</strong></p></td>
<td><p>0x400</p></td>
<td><p>Указывает, что новую запись не был сохранен, так как существующей записи был заблокирован.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecConcurrencyViolation</strong></p></td>
<td><p>0x800</p></td>
<td><p>Указывает, что запись не была сохранена оптимистичный параллелизм использовался в.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecDBDeleted</strong></p></td>
<td><p>0x40000</p></td>
<td><p>Указывает, что запись уже была удалена из источника данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecDeleted</strong></p></td>
<td><p>0x4</p></td>
<td><p>Указывает, что запись была удалена.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecIntegrityViolation</strong></p></td>
<td><p>0x1000</p></td>
<td><p>Указывает, что запись не была сохранена, так как пользователь нарушает ограничения целостности данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecInvalid</strong></p></td>
<td><p>0x10</p></td>
<td><p>Указывает, что запись не была сохранена, так как ее закладки является недопустимым.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecMaxChangesExceeded</strong></p></td>
<td><p>0x2000</p></td>
<td><p>Указывает, что запись не была сохранена из-за слишком много ожидающих изменений.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecModified</strong></p></td>
<td><p>0x2</p></td>
<td><p>Указывает, что запись была изменена.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecMultipleChanges</strong></p></td>
<td><p>0x40</p></td>
<td><p>Указывает, что запись не была сохранена, так как он бы влияет несколько записей.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecNew</strong></p></td>
<td><p>0x1</p></td>
<td><p>Указывает, что запись является новой.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecObjectOpen</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Указывает, что запись не была сохранена из-за конфликта с помощью объекта open хранилища.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecOK</strong></p></td>
<td><p>0</p></td>
<td><p>Указывает, что запись успешно обновлены.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecOutOfMemory</strong></p></td>
<td><p>0x8000</p></td>
<td><p>Указывает, что запись не была сохранена, так как компьютер хватает памяти.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecPendingChanges</strong></p></td>
<td><p>0x80</p></td>
<td><p>Указывает, что запись не была сохранена, так как она ссылается на очередь вставки.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecPermissionDenied</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Указывает, что запись не была сохранена, так как пользователь не имеет разрешений.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecSchemaViolation</strong></p></td>
<td><p>0x20000</p></td>
<td><p>Указывает, что запись не была сохранена, поскольку оно нарушает структуры базы данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecUnmodified</strong></p></td>
<td><p>0x8</p></td>
<td><p>Указывает, что записи не были изменены.</p></td>
</tr>
</tbody>
</table>


**Эквивалент ADO/WFC**

AdoEnums.RecordStatus.

Пакет: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.CANCELED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.CANTRELEASE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.CONCURRENCYVIOLATION</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.DBDELETED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.DELETED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.INTEGRITYVIOLATION</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.INVALID</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.MAXCHANGESEXCEEDED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.MODIFIED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.MULTIPLECHANGES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.NEW</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.OBJECTOPEN</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.OK</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.OUTOFMEMORY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.PENDINGCHANGES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.PERMISSIONDENIED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.RecordStatus.SCHEMAVIOLATION</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.RecordStatus.UNMODIFIED</p></td>
</tr>
</tbody>
</table>

