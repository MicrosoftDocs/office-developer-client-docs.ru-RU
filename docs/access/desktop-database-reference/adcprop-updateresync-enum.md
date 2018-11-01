---
title: ADCPROP_UPDATERESYNC_ENUM
TOCTitle: ADCPROP_UPDATERESYNC_ENUM
ms:assetid: 890210c4-2290-ddb2-8814-022093c318de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249600(v=office.15)
ms:contentKeyID: 48546145
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 2407e412fe63b2cd8dc73927e2adfcd958a67a98
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869402"
---
# <a name="adcpropupdateresyncenum"></a>ADCPROP\_UPDATERESYNC\_ENUM

**Применимо к**: Access 2013, Office 2013

Указывает, будет ли метод [UpdateBatch](updatebatch-method-ado.md) следуют неявных [выполнить повторную синхронизацию](resync-method-ado.md) метод операции и, если да, области действия этой операции.

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
<td><p>15</p></td>
<td><p>Вызывает <strong>выполнить повторную синхронизацию</strong> с комбинацией всех других членов ADCPROP_UPDATERESYNC_ENUM.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncAutoIncrement</strong></p></td>
<td><p>1</p></td>
<td><p>Значение, используемое по умолчанию. Пытается получить новое значение identity для столбцов, которые автоматически увеличивается или создается источник данных, таких как полей Microsoft Jet счетчика или Microsoft SQL Server Identity столбцов.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adResyncConflicts</strong></p></td>
<td><p>2</p></td>
<td><p>Вызывает <strong>выполнить повторную синхронизацию</strong> для всех строк, в которых update или delete операция завершилась неудачно из-за конфликта параллелизма.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncInserts</strong></p></td>
<td><p>8</p></td>
<td><p>Вызывает <strong>выполнить повторную синхронизацию</strong> для всех успешно вставленных строк. Тем не менее значения в столбцах AutoIncrement не синхронизируются. Вместо этого содержимое вставленных новых строк синхронизируются, на основе существующего основного ключа значения. Если первичный ключ значение AutoIncrement <strong>выполнить повторную синхронизацию</strong> не извлечь содержимое предполагаемая строки. Для автоматически увеличивающееся AutoIncrement значения первичного ключа, вызовите <strong>UpdateBatch</strong> с <strong>adResyncAutoIncrement</strong> объединенное значение + <strong>adResyncInserts</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adResyncNone</strong></p></td>
<td><p>0</p></td>
<td><p>Не вызывает <strong>выполнить повторную синхронизацию</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncUpdates</strong></p></td>
<td><p>4</p></td>
<td><p>Вызывает <strong>выполнить повторную синхронизацию</strong> для всех успешно обновленных строк.</p></td>
</tr>
</tbody>
</table>

