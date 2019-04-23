---
title: События объектов данных ActiveX (ADO)
TOCTitle: ADO events
ms:assetid: 84ca9525-99cb-4ba6-2a4d-172414b8f0cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249576(v=office.15)
ms:contentKeyID: 48546041
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cc2ef73798dca18e00c42768fde78da2abdb56a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283340"
---
# <a name="ado-events"></a>События ADO

**Область применения**: Access 2013, Office 2013

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>Событие</th>
<th>Описание</th>
</tr>
<tr class="odd">
<td><p><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">События begintranscomplete</a></p></td>
<td><p>Вызывается после операции <strong>BeginTrans</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></p></td>
<td><p>Вызывается после операции <strong>CommitTrans</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectcomplete-and-disconnect-events-ado.md">События connectcomplete</a></p></td>
<td><p>Вызывается после запуска подключения.</p></td>
</tr>
<tr class="even">
<td><p><a href="connectcomplete-and-disconnect-events-ado.md">Disconnect</a></p></td>
<td><p>Вызывается после завершения подключения.</p></td>
</tr>
<tr class="odd">
<td><p><a href="endofrecordset-event-ado.md">Событие endofrecordset</a></p></td>
<td><p>Вызывается при попытке переместиться в строку, находящиеся за концом объекта <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="executecomplete-event-ado.md">Событие executecomplete</a></p></td>
<td><p>Вызывается после завершения выполнения команды.</p></td>
</tr>
<tr class="odd">
<td><p><a href="fetchcomplete-event-ado.md">Событие fetchcomplete</a></p></td>
<td><p>Вызывается после того, как все записи в длительной асинхронной операции были получены в <strong>набор записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="fetchprogress-event-ado.md">Событие fetchprogress</a></p></td>
<td><p>Вызывается периодически в ходе длительной асинхронной операции, чтобы сообщить, сколько строк в данный момент было извлечено в <strong>набор записей</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></p></td>
<td><p>Вызывается после изменения значения одного или нескольких объектов <strong>field</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="infomessage-event-ado.md">InfoMessage</a></p></td>
<td><p>Вызывается при возникновении предупреждения в ходе операции <strong>коннектионевент</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></p></td>
<td><p>Вызывается после изменения текущей позиции в <strong>наборе записей</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></p></td>
<td><p>Вызывается после изменения одной или нескольких записей.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></p></td>
<td><p>Вызывается после изменения объекта <strong>Recordset</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></p></td>
<td><p>Вызывается после операции <strong>RollbackTrans</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">События willchangefield</a></p></td>
<td><p>Вызывается до того, как ожидающая операция изменяет значение одного или нескольких объектов <strong>field</strong> в <strong>наборе записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">События willchangerecord</a></p></td>
<td><p>Вызывается перед одной или несколькими записями (строк) в изменении <strong>набора записей</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">События willchangerecordset</a></p></td>
<td><p>Вызывается до того, как ожидающая операция изменит объект <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="willconnect-event-ado.md">Событие willconnect</a></p></td>
<td><p>Вызывается перед запуском подключения.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willexecute-event-ado.md">WillExecute</a></p></td>
<td><p>Вызывается непосредственно перед выполнением ожидающей команды для этого подключения и предоставляет пользователю возможность просматривать и изменять параметры, ожидающие выполнения.</p></td>
</tr>
<tr class="even">
<td><p><a href="willmove-and-movecomplete-events-ado.md">События WillMove</a></p></td>
<td><p>Событие <strong>события WillMove</strong> вызывается до того, <em>как</em> ожидающая операция меняет текущую позицию в <strong>наборе записей</strong>.</p></td>
</tr>
</tbody>
</table>

<br/>
