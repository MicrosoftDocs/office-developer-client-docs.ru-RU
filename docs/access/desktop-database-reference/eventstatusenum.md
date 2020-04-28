---
title: Евентстатусенум (Справочник по базам данных Access на компьютере)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 654d2a485c9273072d1daa61321e73418a15e969
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293275"
---
# <a name="eventstatusenum"></a>EventStatusEnum

**Область применения**: Access 2013, Office 2013

Указывает текущее состояние выполнения события.

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
<td><p><strong>адстатусканцел</strong></p></td>
<td><p>4 </p></td>
<td><p>Запрашивает отмену операции, которая привела к возникновению события.</p></td>
</tr>
<tr class="even">
<td><p><strong>адстатускантдени</strong></p></td>
<td><p>4</p></td>
<td><p>Указывает, что операция не может запросить отмену ожидающей операции.</p></td>
</tr>
<tr class="odd">
<td><p><strong>адстатусеррорсоккурред</strong></p></td>
<td><p>2</p></td>
<td><p>Указывает, что операция, вызвавшая событие, не удалась из-за ошибки или ошибок.</p></td>
</tr>
<tr class="even">
<td><p><strong>адстатусок</strong></p></td>
<td><p>1,1</p></td>
<td><p>Указывает, что операция, вызвавшая событие, выполнена успешно.</p></td>
</tr>
<tr class="odd">
<td><p><strong>адстатусунвантедевент</strong></p></td>
<td><p>5 </p></td>
<td><p>Предотвращает последующие уведомления до завершения выполнения метода события.</p></td>
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
<td><p>Адоенумс. Евентстатус. CANCEL</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Евентстатус. КАНТДЕНИ</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Евентстатус. ЕРРОРСОККУРРЕД</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Евентстатус. ОК</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Евентстатус. УНВАНТЕДЕВЕНТ</p></td>
</tr>
</tbody>
</table>

