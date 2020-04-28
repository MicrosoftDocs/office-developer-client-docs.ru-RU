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
# <a name="adcprop_updateresync_enum"></a>Перечисление АДКПРОП\_упдатересинк\_

**Область применения**: Access 2013, Office 2013

Указывает, следует ли метод [UpdateBatch](updatebatch-method-ado.md) выполнить неявную операцию метода [Resync](resync-method-ado.md) и, если это так, область этой операции.

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
<td><p><strong>адресинкалл</strong></p></td>
<td><p>15 </p></td>
<td><p>Вызывает <strong>повторную синхронизацию</strong> со объединенным значением всех других элементов ADCPROP_UPDATERESYNC_ENUM.</p></td>
</tr>
<tr class="even">
<td><p><strong>адресинкаутоинкремент</strong></p></td>
<td><p>1,1</p></td>
<td><p>Значение, используемое по умолчанию. Пытается получить новое значение идентификатора для столбцов, которые автоматически увеличиваются или генерируются источником данных, например поля автонумерации Microsoft Jet или столбцы идентификаторов Microsoft SQL Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>адресинкконфликтс</strong></p></td>
<td><p>2</p></td>
<td><p>Вызывает <strong>повторную синхронизацию</strong> для всех строк, в которых произошел сбой операции обновления или удаления из-за конфликта параллелизма.</p></td>
</tr>
<tr class="even">
<td><p><strong>адресинЦинсертс</strong></p></td>
<td><p>8 </p></td>
<td><p>Вызывает <strong>повторную синхронизацию</strong> для всех успешно вставленных строк. Однако значения столбцов AutoIncrement не синхронизируются повторно. Вместо этого содержимое вновь вставленных строк синхронизируется в соответствии с существующим значением первичного ключа. Если первичный ключ является значением AutoIncrement, <strong>Повторная синхронизация</strong> не извлекает содержимое предполагаемой строки. Для автоматического увеличения значений первичных ключей автоприращения вызовите <strong>UpdateBatch</strong> с объединенным значением <strong>адресинкаутоинкремент</strong> + <strong>адресинЦинсертс</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>адресинкноне</strong></p></td>
<td><p>нуль</p></td>
<td><p>Не вызывает <strong>повторную синхронизацию</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>адресинкупдатес</strong></p></td>
<td><p>4 </p></td>
<td><p>Вызывает <strong>повторную синхронизацию</strong> для всех успешно обновленных строк.</p></td>
</tr>
</tbody>
</table>

