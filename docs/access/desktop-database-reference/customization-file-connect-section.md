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

Поведение обработчика по умолчанию — запретить все подключения. В разделе **Connect** задаются исключения из этого правила. Например, если все разделы **Connect** отсутствовали или пусты, по умолчанию подключения не доводились.

Раздел **Connect** может содержать следующие компоненты:

- Запись доступа по умолчанию, указывающая на операции чтения и записи, разрешенные для данного подключения. Если в разделе нет записи доступа по умолчанию, раздел будет проигнорирован.

- Новая строка подключения, заменяющая строку подключения клиента.

## <a name="syntax"></a>Синтаксис

Запись доступа по умолчанию имеет вид:

`Access=accessRight`

Для записи строки подключения заменяется форма:

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
<td><p>Строка литерала, указывающая на запись строки подключения.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>connectionString</em></strong></p></td>
<td><p>Строка, заменяющая всю строку подключения клиента.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Access</strong></p></td>
<td><p>Строка литерала, указывающая, что это запись доступа.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>Акцессригхт</em></strong></p></td>
<td><p>Одно из следующих прав доступа:</p>
<p></p>
<ul>
<li><p>Нет <strong>доступа</strong> , пользователь не может получить доступ к источнику данных.</p></li>
<li><p><strong>ReadOnly</strong> — пользователь может читать источник данных.</p></li>
<li><p><strong>ReadWrite</strong> — пользователь может выполнять чтение или запись в источник данных.</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


Если требуется разрешить любое подключение (в результате чего отключается поведение обработчика по умолчанию), задайте запись доступа в разделе **подключить по умолчанию** , а затем удалите или закомментируйте любой другой раздел **Connect** *identifier* .

