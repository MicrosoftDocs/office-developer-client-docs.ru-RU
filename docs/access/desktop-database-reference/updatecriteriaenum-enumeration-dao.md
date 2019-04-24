---
title: Перечисление UpdateCriteriaEnum (DAO)
TOCTitle: UpdateCriteriaEnum Enumeration
ms:assetid: 1f83a0c6-bdc8-9c3e-380b-524f611f6476
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845853(v=office.15)
ms:contentKeyID: 48543644
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e27eb1bdfb9b393df76af8bdf54bc7f05fd82c2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306372"
---
# <a name="updatecriteriaenum-enumeration-dao"></a>Перечисление UpdateCriteriaEnum (DAO)


**Область применения**: Access 2013, Office 2013

Используется с методом **UpdateOptions** для указания способа создания пакетного обновления.

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
<td><p>Дбкритериааллколс</p></td>
<td><p>SP4</p></td>
<td><p>Использует ключевые столбцы и все столбцы в предложении WHERE.</p></td>
</tr>
<tr class="even">
<td><p>Дбкритериаделетеинсерт</p></td>
<td><p>столбцов</p></td>
<td><p>Использует сочетание операторов DELETE и INSERT для каждой измененной строки.</p></td>
</tr>
<tr class="odd">
<td><p>Дбкритериакэй</p></td>
<td><p>1,1</p></td>
<td><p>Использует только ключевые столбцы в предложении WHERE.</p></td>
</tr>
<tr class="even">
<td><p>Дбкритериамодвалуес</p></td>
<td><p>2</p></td>
<td><p>Использует ключевые столбцы и все обновленные столбцы в предложении WHERE.</p></td>
</tr>
<tr class="odd">
<td><p>Дбкритериатиместамп</p></td>
<td><p>8,5</p></td>
<td><p>Использует только столбец timestamp (если он доступен) (при отсутствии столбца timestamp в наборе результатов будет создано сообщение об ошибке во время выполнения).</p></td>
</tr>
<tr class="even">
<td><p>Дбкритериаупдате</p></td>
<td><p>32</p></td>
<td><p>Использует инструкцию UPDATE для каждой измененной строки.</p></td>
</tr>
</tbody>
</table>

