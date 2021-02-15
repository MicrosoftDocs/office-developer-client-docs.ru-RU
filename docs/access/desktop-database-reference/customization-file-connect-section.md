---
title: Раздел Connect в файле настройки
TOCTitle: Customization File Connect section
ms:assetid: 037abfb4-798d-4b09-6133-356969aee95c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248802(v=office.15)
ms:contentKeyID: 48542985
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8652aa2c028350aab79cdf101cba189026b9a5ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295144"
---
# <a name="customization-file-connect-section"></a>Раздел Connect в файле настройки

**Область применения**: Access 2013, Office 2013

По умолчанию обработтель отрегулировать все подключения. В **разделе** "Подключение" указаны исключения из этого поведения. Например, если все разделы **подключения** отсутствуют или пусты, по умолчанию подключения не могут быть подключены.

Раздел **"Подключение"** может содержать:

- Запись доступа по умолчанию, которая определяет операции чтения и записи по умолчанию, разрешенные для этого подключения. Если в разделе нет записи доступа по умолчанию, раздел будет игнорироваться.

- Новая строка подключения, которая заменяет строку клиентского подключения.

## <a name="syntax"></a>Синтаксис

Запись доступа по умолчанию имеет форму:

`Access=accessRight`

Замещаемая строка подключения имеет форму:

`Connect=connectionString`

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
<td><p><strong>Connect</strong></p></td>
<td><p>Строка литералов, которая указывает, что это запись строки подключения.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>connectionString</em></strong></p></td>
<td><p>Строка, которая заменяет всю строку клиентского подключения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Access</strong></p></td>
<td><p>Строка литералов, которая указывает, что это запись доступа.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>accessRight</em></strong></p></td>
<td><p>Одно из следующих прав доступа:</p>
<p></p>
<ul>
<li><p><strong>NoAccess</strong> — пользователь не может получить доступ к источнику данных.</p></li>
<li><p><strong>ReadOnly</strong> — пользователь может читать источник данных.</p></li>
<li><p><strong>ReadWrite</strong> — пользователь может читать или записывать данные в источник данных.</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


Если вы хотите разрешить любое подключение (по сути, отключив поведение обработера по умолчанию), установите для   записи доступа в разделе подключения значение по умолчанию, а также удалите или закомментировать любой другой раздел идентификатора подключения. 

