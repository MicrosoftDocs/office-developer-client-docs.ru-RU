---
title: Перечисление UpdateTypeEnum (DAO)
TOCTitle: UpdateTypeEnum Enumeration
ms:assetid: 7ac38bae-27fc-f3d0-5b75-569bce547954
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196186(v=office.15)
ms:contentKeyID: 48545800
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d1e4ecbc216ab4a00dabd85f623bc134772dfd4c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706165"
---
# <a name="updatetypeenum-enumeration-dao"></a>Перечисление UpdateTypeEnum (DAO)


**Применимо к**: Access 2013, Office 2013

Используется с методом **обновления** для указания необходимых обновлений для записи на диск.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbUpdateBatch</p></td>
<td><p>4</p></td>
<td><p>Все ожидающие изменения в кэше обновления записываются на диск.</p></td>
</tr>
<tr class="even">
<td><p>dbUpdateCurrentRecord</p></td>
<td><p>2</p></td>
<td><p>Только для текущей записи ожидающие изменения записываются на диск.</p></td>
</tr>
<tr class="odd">
<td><p>dbUpdateRegular</p></td>
<td><p>1</p></td>
<td><p>(По умолчанию) Отложенные изменения не кэшируются и записи на диск немедленно.</p></td>
</tr>
</tbody>
</table>

