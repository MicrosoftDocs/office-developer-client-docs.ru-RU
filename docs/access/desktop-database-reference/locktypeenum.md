---
title: LockTypeEnum (Справочник по для настольных баз данных Access)
TOCTitle: LockTypeEnum
ms:assetid: 966b4952-5591-4a99-82d5-99cb9ae3fc72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249667(v=office.15)
ms:contentKeyID: 48546448
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cf882c6a63edbf3df067016a6ed793e05f41e74c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481366"
---
# <a name="locktypeenum"></a>LockTypeEnum


**Применимо к**: Access 2013 | Office 2013

Указывает тип блокировки, помещенные на записей во время редактирования.

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
<td><p><strong>adLockBatchOptimistic</strong></p></td>
<td><p>4</p></td>
<td><p>Указывает оптимистичный пакета обновлений. Требуется для пакетного обновления.</p></td>
</tr>
<tr class="even">
<td><p><strong>adLockOptimistic</strong></p></td>
<td><p>3</p></td>
<td><p>Указывает, оптимистичный блокировки, записи по. Поставщик использует оптимистичный блокировки блокировка записи только при вызове метода <a href="update-method-ado.md">Update</a> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>adLockPessimistic</strong></p></td>
<td><p>2</p></td>
<td><p>Указывает, жесткой блокировки, записи по. Поставщик выполняет, что является обязательным для обеспечения успешной редактирования записей, обычно путем блокировки сразу же после изменения записи в источнике данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>adLockReadOnly</strong></p></td>
<td><p>1</p></td>
<td><p>Указывает записи только для чтения. Невозможно изменить данные.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adLockUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Не указан тип блокировки. Для копирует копия создается с тем же типом блокировки, что и исходный.</p></td>
</tr>
</tbody>
</table>


**Эквивалент ADO/WFC**

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
<td><p>AdoEnums.LockType.BATCHOPTIMISTIC</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.LockType.OPTIMISTIC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.LockType.PESSIMISTIC</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.LockType.READONLY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.LockType.UNSPECIFIED</p></td>
</tr>
</tbody>
</table>
