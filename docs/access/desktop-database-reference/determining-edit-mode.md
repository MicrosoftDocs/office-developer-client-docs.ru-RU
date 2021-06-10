---
title: Определение режима редактирования
TOCTitle: Determining Edit mode
ms:assetid: 45e21fa7-94e8-3449-e062-09cbcf15cba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249215(v=office.15)
ms:contentKeyID: 48544563
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5b62bc282a99472d0e7399ee9f3dd9d0648f0c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293919"
---
# <a name="determining-edit-mode"></a>Определение режима редактирования


**Область применения**: Access 2013, Office 2013

ADO поддерживает буфер редактирования, связанный с текущей записью. Свойство **EditMode** указывает, были ли внесены изменения в этот буфер или создана новая запись. Чтобы определить состояние редактирования текущей записи, используйте **EditMode.** Вы можете проверить ожидающие изменения, если процесс редактирования был прерван, и определить, нужно ли использовать метод **Update** или **CancelUpdate.**

**EditMode** возвращает одну из **констант EditModeEnum,** перечисленных в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adEditNone</strong></p></td>
<td><p>Указывает, что операция редактирования не продолжается.</p></td>
</tr>
<tr class="even">
<td><p><strong>adEditInProgress</strong></p></td>
<td><p>Указывает, что данные в текущей записи были изменены, но не сохранены.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adEditAdd</strong></p></td>
<td><p>Указывает, что метод <strong>AddNew</strong> был вызван, а текущая запись в буфере копирования — это новая запись, которая не была сохранена в базе данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>adEditDelete</strong></p></td>
<td><p>Указывает, что текущая запись удалена.</p></td>
</tr>
</tbody>
</table>


**EditMode** может вернуть допустимые значения только при текущей записи. **EditMode** возвращает ошибку, если **boF** или **EOF** является **true** или если текущая запись удалена.

