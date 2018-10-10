---
title: Determining Edit Mode
TOCTitle: Determining Edit Mode
ms:assetid: 45e21fa7-94e8-3449-e062-09cbcf15cba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249215(v=office.15)
ms:contentKeyID: 48544563
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 53167d7438ecce673fed64f3c7b8d53fbbfbaa5d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483078"
---
# <a name="determining-edit-mode"></a>Determining Edit Mode


**Применимо к**: Access 2013 | Office 2013

ADO поддерживает редактирования буфера, связанного с текущей записи. Свойство **EditMode** указывает ли изменения были внесены в этот буфер или создан ли новую запись. Использование **EditMode** для определения статуса редактирования текущей записи. Можно проверить наличие ожидающих изменений, если редактирования процесс был прерван и определите, нужно ли использовать **обновления** или метод **CancelUpdate** .

**EditMode** возвращает одной из констант **EditModeEnum** , перечисленные в следующей таблице.

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
<td><p><strong>как таковые</strong></p></td>
<td><p>Указывает, что операция редактирования не находится в стадии разработки.</p></td>
</tr>
<tr class="even">
<td><p><strong>adEditInProgress</strong></p></td>
<td><p>Указывает, что данные в текущей записи были изменены, но не сохраняются.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adEditAdd</strong></p></td>
<td><p>Указывает, что был вызван метод <strong>AddNew</strong> , и текущую запись в буфер копирования не новую запись, не были сохранены в базу данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>adEditDelete</strong></p></td>
<td><p>Указывает, что текущая запись был удален.</p></td>
</tr>
</tbody>
</table>


**EditMode** можно вернуть допустимое значение только в том случае, если текущая запись. **EditMode** возвращает ошибку, если **справедливо **BOF** или **EOF** ** или текущей запись была удалена.

