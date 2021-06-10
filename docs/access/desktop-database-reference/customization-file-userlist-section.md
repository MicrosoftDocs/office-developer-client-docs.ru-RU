---
title: Раздел UserList в файле настройки
TOCTitle: Customization File UserList section
ms:assetid: b60ba3b0-37d4-bb59-d3cd-2ab44d178b8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249873(v=office.15)
ms:contentKeyID: 48547263
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ecaf77765051a202925449d0221f0a68a2a06622
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295158"
---
# <a name="customization-file-userlist-section"></a>Раздел UserList в файле настройки


**Область применения**: Access 2013, Office 2013

Раздел **userlist** относится к разделу **connect** с тем же параметром *идентификатора* раздела.

В этом разделе может содержаться запись доступа *пользователя,* которая указывает права   доступа для указанного пользователя и переопределяет запись доступа по умолчанию в разделе **соединяемого** подключения.

## <a name="syntax"></a>Синтаксис

Запись доступа к пользователю имеет форму:

*userName***=* accessRights***

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Part</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>userName</em></p></td>
<td><p>Имя <em>пользователя пользователя,</em> используемого для этого подключения. Допустимые имена пользователей устанавливаются в диалоговом окантове Диспетчер <strong>служб</strong> IIS.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>accessRights</em></strong></p></td>
<td><p>Одно из следующих прав доступа:<br />
</p>
<ul>
<li><p><strong>NoAccess —</strong> пользователь не может получить доступ к источнику данных.</p></li>
<li><p><strong>ReadOnly</strong> — пользователь может читать источник данных.</p></li>
<li><p><strong>ReadWrite</strong> — пользователь может читать или писать в источник данных.</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

