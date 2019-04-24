---
title: Определение режима правки
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
# <a name="determining-edit-mode"></a>Определение режима правки


**Область применения**: Access 2013, Office 2013

ADO поддерживает буфер редактирования, связанный с текущей записью. Свойство **EditMode** указывает, были ли внесены изменения в этот буфер или создана ли новая запись. Используйте **EditMode** для определения состояния редактирования текущей записи. Вы можете протестировать ожидающие изменения, если процесс редактирования был прерван, и определить, нужно ли использовать метод **Update** или **CancelUpdate** .

**EditMode** возвращает одну из констант **едитмодинум** , перечисленных в следующей таблице.

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
<td><p><strong>Адедитноне</strong></p></td>
<td><p>Указывает, что операции редактирования не выполняются.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адедитинпрогресс</strong></p></td>
<td><p>Указывает, что данные в текущей записи были изменены, но не были сохранены.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адедитадд</strong></p></td>
<td><p>Указывает, что был вызван метод <strong>AddNew</strong> , а текущая запись в буфере копирования — это новая запись, которая не была сохранена в базе данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адедитделете</strong></p></td>
<td><p>Указывает, что текущая запись была удалена.</p></td>
</tr>
</tbody>
</table>


**EditMode** может возвращать допустимое значение только при наличии текущей записи. **EditMode** возвращает ошибку, если **BOF** или **EOF** имеет **значение true** , или если текущая запись была удалена.

