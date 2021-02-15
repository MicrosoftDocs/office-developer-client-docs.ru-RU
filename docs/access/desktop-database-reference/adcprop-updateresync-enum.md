---
title: ADCPROP_UPDATERESYNC_ENUM
TOCTitle: ADCPROP_UPDATERESYNC_ENUM
ms:assetid: 890210c4-2290-ddb2-8814-022093c318de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249600(v=office.15)
ms:contentKeyID: 48546145
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1952d473b51048a271a689498ae844cee761b001
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280441"
---
# <a name="adcprop_updateresync_enum"></a>ADCPROP \_ UPDATERESYNC \_ ENUM

**Область применения**: Access 2013, Office 2013

Указывает, следует ли за [методом UpdateBatch](updatebatch-method-ado.md) неявную операцию метода [Resync](resync-method-ado.md) и, если да, область этой операции.

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
<td><p><strong>adResyncAll</strong></p></td>
<td><p>15 </p></td>
<td><p>Вызывает <strong>Resync с</strong> объединенным значением всех остальных ADCPROP_UPDATERESYNC_ENUM участников.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncAutoIncrement</strong></p></td>
<td><p>1 </p></td>
<td><p>Значение, используемое по умолчанию. Пытается получить новое значение удостоверения для столбцов, которые автоматически приращены или генерируются источником данных, например полей автонума Microsoft Jet или Microsoft SQL Server идентификатора.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adResyncConflicts</strong></p></td>
<td><p>2 </p></td>
<td><p>Вызывает <strong>Resync для</strong> всех строк, в которых произошел сбой операции обновления или удаления из-за конфликта.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncInserts</strong></p></td>
<td><p>8 </p></td>
<td><p>Вызывает <strong>Resync для</strong> всех успешно вставленных строк. Однако значения столбцов autoIncrement не синхронизируются повторно. Вместо этого содержимое новых строк повторно синхронизируется на основе существующего значения первичного ключа. Если первичный ключ имеет значение AutoIncrement, <strong>Resync</strong> не будет получать содержимое нужной строки. Для автоматического приращения значений первичного ключа autoIncrement вызовите <strong>UpdateBatch</strong> с объединенным значением <strong>adResyncAutoIncrement</strong> + <strong>adResyncInserts.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>adResyncNone</strong></p></td>
<td><p>0</p></td>
<td><p>Не вызывает <strong>Resync</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncUpdates</strong></p></td>
<td><p>4 </p></td>
<td><p>Вызывает <strong>Resync для</strong> всех успешно обновленных строк.</p></td>
</tr>
</tbody>
</table>

