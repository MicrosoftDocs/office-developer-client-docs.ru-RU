---
title: EventReasonEnum (Ссылка на настольные базы данных)
TOCTitle: EventReasonEnum
ms:assetid: 0639928e-d0ef-3db3-887e-f3da03913bc7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248815(v=office.15)
ms:contentKeyID: 48543047
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4948cd9a5f1436e4e1afc61bef87b63675e115ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293331"
---
# <a name="eventreasonenum"></a>EventReasonEnum

**Область применения**: Access 2013, Office 2013

Указывает причину, по которой произошло событие.

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
<td><p><strong>adRsnAddNew</strong></p></td>
<td><p>1</p></td>
<td><p>Операция добавила новую запись.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnClose</strong></p></td>
<td><p>9 </p></td>
<td><p>Операция закрыла <strong>Набор записей.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnDelete</strong></p></td>
<td><p>2</p></td>
<td><p>Операция удалила запись.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnFirstChange</strong></p></td>
<td><p>11</p></td>
<td><p>Операция сделала первое изменение записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnMove</strong></p></td>
<td><p>10 </p></td>
<td><p>Операция переместила указатель записи в <strong>recordset.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnMoveFirst</strong></p></td>
<td><p>12 </p></td>
<td><p>Операция переместила указатель записи на первую запись <strong>в Наборе записей.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnMoveLast</strong></p></td>
<td><p>15</p></td>
<td><p>Операция переместила указатель записи на последнюю запись <strong>в Наборе записей.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnMoveNext</strong></p></td>
<td><p>13</p></td>
<td><p>Операция переместила указатель записи на следующую запись <strong>в Наборе записей.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnMovePrevious</strong></p></td>
<td><p>14 </p></td>
<td><p>Операция переместила указатель записи к предыдущей записи в <strong>Наборе записей.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnRequery</strong></p></td>
<td><p>7 </p></td>
<td><p>Операция повторного <a href="recordset-object-ado.md">recordset</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnResynch</strong></p></td>
<td><p>8 </p></td>
<td><p>Операция ресинхронизировала <strong>набор recordset</strong> с базой данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnUndoAddNew</strong></p></td>
<td><p>5 </p></td>
<td><p>Операция отменила добавление новой записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnUndoDelete</strong></p></td>
<td><p>6 </p></td>
<td><p>Операция отменила удаление записи.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnUndoUpdate</strong></p></td>
<td><p>4 </p></td>
<td><p>Операция отменила обновление записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnUpdate</strong></p></td>
<td><p>3</p></td>
<td><p>Операция обновила существующую запись.</p></td>
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
<td><p>AdoEnums.EventReason.ADDNEW</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventReason.CLOSE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventReason.DELETE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventReason.FIRSTCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventReason.MOVE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventReason.MOVEFIRST</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventReason.MOVELAST</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventReason.MOVENEXT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventReason.MOVEPREVIOUS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventReason.REQUERY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventReason.RESYNCH</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventReason.UNDOADDNEW</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventReason.UNDODELETE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.EventReason.UNDOUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.EventReason.UPDATE</p></td>
</tr>
</tbody>
</table>

