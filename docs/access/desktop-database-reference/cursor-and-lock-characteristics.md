---
title: Характеристики курсора и блокировки
TOCTitle: Cursor and lock characteristics
ms:assetid: 5f8b6700-14f6-d342-42f6-cc8e89c71a1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249347(v=office.15)
ms:contentKeyID: 48545164
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b3d518ccd82ae2dbc3f280954848d58d8e617cd
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944993"
---
# <a name="cursor-and-lock-characteristics"></a>Характеристики курсора и блокировки

**Применимо к**: Access 2013, Office 2013

Во время характеристики курсора зависят от возможностей поставщика, следующие преимущества и недостатки обычно относятся к различные типы курсоров и блокировок.

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
<li><p>Требования к нехватки ресурсов</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Не удается Прокрутка назад</p></li>
<li><p>Нет данных параллелизма</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p></p>
<ul>
<li><p>Прокручиваемой</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Нет данных параллелизма</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p></p>
<ul>
<li><p>Некоторые данные параллелизма</p></li>
<li><p>Прокручиваемой</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Выше требований к ресурсам</p></li>
<li><p>Недоступно в отключенные сценарии</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p></p>
<ul>
<li><p>Параллелизм высокой данных</p></li>
<li><p>Прокручиваемой</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Наибольший требований к ресурсам</p></li>
<li><p>Недоступно в отключенные сценарии</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>adLockReadOnly</strong></p></td>
<td><p></p>
<ul>
<li><p>Требования к нехватки ресурсов</p></li>
<li><p>Хорошо масштабируемое</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Данные не обновляемых до текущей позиции</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adLockBatchOptimistic</strong></p></td>
<td><p></p>
<ul>
<li><p>Пакет обновления</p></li>
<li><p>Позволяет без подключения к сети</p></li>
<li><p>Другие пользователи могут получить доступ к данным</p></li>
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
<li><p>Данные не могут менять другие пользователи во время блокировки</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Пользователям запрещается доступ к данным во время блокировки</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adLockOptimistic</strong></p></td>
<td><p></p>
<ul>
<li><p>Другие пользователи могут получить доступ к данным</p></li>
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

