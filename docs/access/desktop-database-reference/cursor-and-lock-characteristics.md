---
title: Характеристики курсоров и блокировок
TOCTitle: Cursor and lock characteristics
ms:assetid: 5f8b6700-14f6-d342-42f6-cc8e89c71a1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249347(v=office.15)
ms:contentKeyID: 48545164
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 41a42aa3b0c49a5d871fa7b079a26c7d8076116a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295291"
---
# <a name="cursor-and-lock-characteristics"></a>Характеристики курсоров и блокировок

**Область применения**: Access 2013, Office 2013

Хотя характеристики курсора зависят от возможностей поставщика, следующие преимущества и недостатки обычно применяются к различным типам курсоров и блокировок.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Тип курсора или блокировки</p></th>
<th><p>Преимущества</p></th>
<th><p>Недостатки</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p></p>
<ul>
<li><p>Низкие требования к ресурсам</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Не удается прокрутить назад</p></li>
<li><p>Нет данных совмее-</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p></p>
<ul>
<li><p>Прокручиваемая</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Нет данных совмее-</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p></p>
<ul>
<li><p>Некоторые данные concurrency</p></li>
<li><p>Прокручиваемая</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Более высокие требования к ресурсам</p></li>
<li><p>Отсутствует в сценарии отключения</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p></p>
<ul>
<li><p>Высокая емка данных</p></li>
<li><p>Прокручиваемая</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Самые высокие требования к ресурсам</p></li>
<li><p>Отсутствует в сценарии отключения</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>adLockReadOnly</strong></p></td>
<td><p></p>
<ul>
<li><p>Низкие требования к ресурсам</p></li>
<li><p>Высокая масштабируемость</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Данные, которые не могут быть updatable с помощью курсора</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adLockBatchOptimistic</strong></p></td>
<td><p></p>
<ul>
<li><p>Пакетные обновления</p></li>
<li><p>Разрешает отключенные сценарии</p></li>
<li><p>Другие пользователи, которые могут получить доступ к данным</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Данные могут быть изменены несколькими пользователями одновременно</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>adLockPessimistic</strong></p></td>
<td><p></p>
<ul>
<li><p>Данные не могут быть изменены другими пользователями во время блокировки</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Запретить другим пользователям доступ к данным во время блокировки</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adLockOptimistic</strong></p></td>
<td><p></p>
<ul>
<li><p>Другие пользователи, которые могут получать доступ к данным</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Данные могут быть изменены несколькими пользователями одновременно</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

