---
title: Объекты данных ActiveX (ADO) события
TOCTitle: ADO Events
ms:assetid: 84ca9525-99cb-4ba6-2a4d-172414b8f0cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249576(v=office.15)
ms:contentKeyID: 48546041
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d7a885d5fdd7736a37c2f195c3bf14b4af8a70d3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876234"
---
# <a name="ado-events"></a>События ADO


**Применимо к**: Access 2013, Office 2013

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">BeginTransComplete</a></p></td>
<td><p>Вызывается после <strong>BeginTrans</strong> операции.</p></td>
</tr>
<tr class="even">
<td><p><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">CommitTransComplete</a></p></td>
<td><p>Вызывается после <strong>CommitTrans</strong> операции.</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectcomplete-and-disconnect-events-ado.md">ConnectComplete</a></p></td>
<td><p>Вызывается после запуска подключения.</p></td>
</tr>
<tr class="even">
<td><p><a href="connectcomplete-and-disconnect-events-ado.md">Отключение</a></p></td>
<td><p>Вызывается после завершения подключения.</p></td>
</tr>
<tr class="odd">
<td><p><a href="endofrecordset-event-ado.md">EndOfRecordset</a></p></td>
<td><p>Вызывается, когда при попытке перейдите к строке за пределами <strong>набора записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="executecomplete-event-ado.md">ExecuteComplete</a></p></td>
<td><p>Вызывается после завершения выполнения команды.</p></td>
</tr>
<tr class="odd">
<td><p><a href="fetchcomplete-event-ado.md">FetchComplete</a></p></td>
<td><p>Вызывается после извлечения всех записей в объемных асинхронной операции в <strong>набора записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="fetchprogress-event-ado.md">FetchProgress</a></p></td>
<td><p>Вызывается периодически во время длительных асинхронной операции для отчета, сколько строк в настоящее время извлечения в <strong>набор записей</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">FieldChangeComplete</a></p></td>
<td><p>Вызывается после изменения значения одного или нескольких объектов <strong>поля</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="infomessage-event-ado.md">InfoMessage</a></p></td>
<td><p>Вызывается при каждом появлении предупреждения в процессе выполнения операции <strong>ConnectionEvent</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="willmove-and-movecomplete-events-ado.md">MoveComplete</a></p></td>
<td><p>Вызывается после текущей позиции в изменения <strong>записей</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">RecordChangeComplete</a></p></td>
<td><p>Вызывается после изменения одной или нескольких записей.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</a></p></td>
<td><p>Вызывается после изменения <strong>набора записей</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado.md">RollbackTransComplete</a></p></td>
<td><p>Вызывается после операции <strong>RollbackTrans</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangefield-and-fieldchangecomplete-events-ado.md">WillChangeField</a></p></td>
<td><p>Вызывается перед ожидающие операции изменяется значение один или несколько объектов <strong>поля</strong> в <strong>набора записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="willchangerecord-and-recordchangecomplete-events-ado.md">WillChangeRecord</a></p></td>
<td><p>Вызывается до изменения одного или нескольких записей (строк) в <strong>набор записей</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">WillChangeRecordset</a></p></td>
<td><p>Вызывается перед операцию ожидающие изменения <strong>набора записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="willconnect-event-ado.md">WillConnect</a></p></td>
<td><p>Вызывается до начала подключения.</p></td>
</tr>
<tr class="odd">
<td><p><a href="willexecute-event-ado.md">WillExecute</a></p></td>
<td><p>Вызывается непосредственно перед ожидающие команда выполняет для этого подключения и дает пользователю возможность проверки и изменения параметров ожидающих выполнения.</p></td>
</tr>
<tr class="even">
<td><p><a href="willmove-and-movecomplete-events-ado.md">WillMove</a></p></td>
<td><p>Событие <strong>WillMove</strong> вызывается <em>перед</em> ожидающие операции изменяет текущую позицию в наборе <strong>записей</strong>.</p></td>
</tr>
</tbody>
</table>

