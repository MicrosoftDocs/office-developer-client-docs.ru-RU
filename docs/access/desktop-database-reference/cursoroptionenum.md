---
title: CursorOptionEnum (Справочник по для настольных баз данных Access)
TOCTitle: CursorOptionEnum
ms:assetid: 3c118c08-02f2-5290-1cef-29e97c35fddc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249155(v=office.15)
ms:contentKeyID: 48544303
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7443e0cb29954fae9dfc193ffc6aa8dee9886089
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701069"
---
# <a name="cursoroptionenum"></a>CursorOptionEnum

**Применимо к**: Access 2013, Office 2013

Указывает, какие функции [поддерживает](supports-method-ado.md) метод, следует проверить наличие.

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
<td><p><strong>adAddNew</strong></p></td>
<td><p>0x1000400</p></td>
<td><p>Поддерживает метод <a href="addnew-method-ado.md">AddNew</a> для добавления новых записей.</p></td>
</tr>
<tr class="even">
<td><p><strong>adApproxPosition</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Поддерживает свойства <a href="absoluteposition-property-ado.md">AbsolutePosition</a> и <a href="absolutepage-property-ado.md">AbsolutePage</a> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>adBookmark</strong></p></td>
<td><p>0x2000</p></td>
<td><p>Поддерживает свойства <a href="bookmark-property-ado.md">закладку</a> для получения доступа к определенным записей.</p></td>
</tr>
<tr class="even">
<td><p><strong>adDelete</strong></p></td>
<td><p>0x1000800</p></td>
<td><p>Поддерживает метод <a href="delete-method-ado-recordset.md">Delete</a> для удаления записей.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFind</strong></p></td>
<td><p>0x80000</p></td>
<td><p>Поддерживает метод <a href="find-method-ado.md">поиска</a> для поиска строки в <a href="recordset-object-ado.md">набора записей</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adHoldRecords</strong></p></td>
<td><p>0x100</p></td>
<td><p>Извлекает несколько записей или изменяет следующей позиции без фиксации все ожидающие изменения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adIndex</strong></p></td>
<td><p>0x100000</p></td>
<td><p>Поддерживает свойства <a href="index-property-ado.md">Index</a> одно имя индекса.</p></td>
</tr>
<tr class="even">
<td><p><strong>adMovePrevious</strong></p></td>
<td><p>0x200</p></td>
<td><p>Поддерживает <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a> и <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a> методы и методы <a href="move-method-ado.md">перемещения</a> или <a href="getrows-method-ado.md">Получение строк</a> для перемещения положения текущей записи обратной без необходимости установки закладки.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adNotify</strong></p></td>
<td><p>0x40000</p></td>
<td><p>Указывает, что базовый поставщик данных поддерживает уведомления (что определяет, поддерживается ли события <strong>набора записей</strong> ).</p></td>
</tr>
<tr class="even">
<td><p><strong>adResync</strong></p></td>
<td><p>0x20000</p></td>
<td><p>Поддерживает метод <a href="resync-method-ado.md">выполнить повторную синхронизацию</a> для обновления курсора с данными, который будет отображаться в основной базе данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSeek</strong></p></td>
<td><p>0x200000</p></td>
<td><p>Поддерживает метод <a href="seek-method-ado.md">поиска</a> для поиска строки в <strong>набора записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adUpdate</strong></p></td>
<td><p>0x1008000</p></td>
<td><p>Поддерживает метод <a href="update-method-ado.md">Update</a> для изменения существующих данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUpdateBatch</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Поддерживает пакетного обновления (методы<a href="updatebatch-method-ado.md">UpdateBatch</a> и <a href="cancelbatch-method-ado.md">CancelBatch</a> ) для передачи группы об изменениях в поставщик.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Пакет: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.CursorOption.ADDNEW</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.APPROXPOSITION</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.BOOKMARK</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.DELETE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.FIND</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.HOLDRECORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.INDEX</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.MOVEPREVIOUS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.NOTIFY</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.RESYNC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.SEEK</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorOption.UPDATE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorOption.UPDATEBATCH</p></td>
</tr>
</tbody>
</table>

