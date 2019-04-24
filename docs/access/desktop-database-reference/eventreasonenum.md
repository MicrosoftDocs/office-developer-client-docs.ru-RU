---
title: Евентреасоненум (Справочник по базам данных Access на компьютере)
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

Указывает причину, по которой возникло событие.

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
<td><p><strong>Адрснадднев</strong></p></td>
<td><p>1,1</p></td>
<td><p>Операция добавила новую запись.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адрснклосе</strong></p></td>
<td><p>10</p></td>
<td><p>Операция закрыла <strong>набор записей</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адрснделете</strong></p></td>
<td><p>2</p></td>
<td><p>Операция удалила запись.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адрснфирстчанже</strong></p></td>
<td><p>-11:00</p></td>
<td><p>Операция выполняла первое изменение записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адрснмове</strong></p></td>
<td><p>десяти</p></td>
<td><p>Операция переместила указатель записи в <strong>набор записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адрснмовефирст</strong></p></td>
<td><p>12</p></td>
<td><p>Операция переместила указатель записи на первую запись в <strong>наборе записей</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адрснмовеласт</strong></p></td>
<td><p>означает</p></td>
<td><p>Операция переместила указатель записи на последнюю запись в <strong>наборе записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адрснмовенекст</strong></p></td>
<td><p>13</p></td>
<td><p>Операция переместила указатель записи на следующую запись в <strong>наборе записей</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адрснмовепревиаус</strong></p></td>
<td><p>14</p></td>
<td><p>Операция переместила указатель записи на предыдущую запись в наборе <strong>записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адрснрекуери</strong></p></td>
<td><p>см</p></td>
<td><p>Операция запросила <a href="recordset-object-ado.md">набор записей</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адрснресинч</strong></p></td>
<td><p>8,5</p></td>
<td><p>Операция повторно синхронизирует объект <strong>Recordset</strong> с базой данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адрснундоадднев</strong></p></td>
<td><p>17:00</p></td>
<td><p>Операция отменяет добавление новой записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адрснундоделете</strong></p></td>
<td><p>ICMPv6</p></td>
<td><p>Операция отменяет удаление записи.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адрснундаупдате</strong></p></td>
<td><p>SP4</p></td>
<td><p>Операция отменяет обновление записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адрснупдате</strong></p></td>
<td><p>4</p></td>
<td><p>Операция обновила существующую запись.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Пакет: **com. MS. WFC. Data**

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
<td><p>Адоенумс. Евентреасон. ADDNEW</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Евентреасон. CLOSE</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Евентреасон. DELETE</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Евентреасон. ФИРСТЧАНЖЕ</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Евентреасон. MOVE</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Евентреасон. MOVEFIRST</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Евентреасон. MOVELAST</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Евентреасон. MOVENEXT</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Евентреасон. MOVEPREVIOUS</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Евентреасон. reQUERY</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Евентреасон. reSYNCH</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Евентреасон. УНДОАДДНЕВ</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Евентреасон. УНДОДЕЛЕТЕ</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Евентреасон. УНДАУПДАТЕ</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Евентреасон. UPDATE</p></td>
</tr>
</tbody>
</table>

