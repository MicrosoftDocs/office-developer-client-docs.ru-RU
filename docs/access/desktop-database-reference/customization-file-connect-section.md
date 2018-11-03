---
title: Раздел подключение файла настройки
TOCTitle: Customization File Connect section
ms:assetid: 037abfb4-798d-4b09-6133-356969aee95c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248802(v=office.15)
ms:contentKeyID: 48542985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 49e2d6cc8579f064df3e752268fce5b47c9b1ada
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944188"
---
# <a name="customization-file-connect-section"></a>Раздел подключение файла настройки

**Применимо к**: Access 2013, Office 2013

Поведение по умолчанию обработчика является запретить все подключения. В разделе **подключение** указывает исключения, чтобы это поведение. Например если все разделы **подключение** отсутствует или пустой, затем по умолчанию подключения не удалось выполнить.

В разделе **подключение** может содержать:

- Запись доступа по умолчанию определяет значение по умолчанию операций чтения и записи на этом компьютере. Если отсутствует запись доступа по умолчанию в разделе, разделе будет игнорироваться.

- Новую строку подключения, которая заменяет строка подключения клиента.

## <a name="syntax"></a>Синтаксис

Запись доступа по умолчанию имеет вид:

`Access=accessRight`

Запись строки подключения замены имеет форму:

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
<td><p><strong>Подключение</strong></p></td>
<td><p>Строковый литерал, которое указывает, это является запись строки подключения.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>connectionString</em></strong></p></td>
<td><p>Строка, которая заменяет строка подключения всей клиента.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Access</strong></p></td>
<td><p>Строковый литерал, которое указывает, это является записью доступа.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>accessRight</em></strong></p></td>
<td><p>Один из следующих прав доступа.</p>
<p></p>
<ul>
<li><p><strong>NoAccess</strong> — пользователь не может получить доступ к источнику данных.</p></li>
<li><p><strong>ReadOnly</strong> — пользователи могут читать источника данных.</p></li>
<li><p><strong>ReadWrite</strong> — пользователь может чтение или запись в источник данных.</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


Если вы хотите разрешить любые подключения (в силу, отключение обработчика поведение по умолчанию), запись доступа к набора в разделе **Подключение по умолчанию** и удалите или закомментировать любые другие **подключения** *идентификатор* раздела.

