---
title: Раздел UserList файл настройки
TOCTitle: Customization File UserList section
ms:assetid: b60ba3b0-37d4-bb59-d3cd-2ab44d178b8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249873(v=office.15)
ms:contentKeyID: 48547263
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62aaba79fa010de62fb1ac35939673b2056be3f7
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944097"
---
# <a name="customization-file-userlist-section"></a>Раздел UserList файл настройки


**Применимо к**: Access 2013, Office 2013

В разделе **userlist** относится к раздел **подключиться** с того же параметра *идентификатор* раздела.

В этом разделе может содержать с *доступом пользователя*, которая определяет права доступа для указанного пользователя и переопределяет *по умолчанию* *доступом* в соответствующий раздел **подключение** .

## <a name="syntax"></a>Синтаксис

Запись доступом пользователей имеет форму:

*имя пользователя *** =* accessRights ***

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Часть</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>userName</em></p></td>
<td><p><em>Имя пользователя</em> человека, используя это подключение. Диалоговое окно служб IIS <strong>Manager службы</strong> устанавливаются имен пользователей.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>accessRights</em></strong></p></td>
<td><p>Один из следующих прав доступа.<br />
</p>
<ul>
<li><p><strong>NoAccess</strong> — пользователь не может получить доступ к источнику данных.</p></li>
<li><p><strong>ReadOnly</strong> — пользователи могут читать источника данных.</p></li>
<li><p><strong>ReadWrite</strong> — пользователь может чтение или запись в источник данных.</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

