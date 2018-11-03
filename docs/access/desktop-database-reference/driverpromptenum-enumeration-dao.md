---
title: Перечисление DriverPromptEnum (DAO)
TOCTitle: DriverPromptEnum Enumeration
ms:assetid: 8dda5e9f-a58f-a62d-eb49-5966d4a1e086
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197361(v=office.15)
ms:contentKeyID: 48546266
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b6911e325b070a8c6d62b70dfcacf96ae1dc3dc
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943558"
---
# <a name="driverpromptenum-enumeration-dao"></a>Перечисление DriverPromptEnum (DAO)


**Применимо к**: Access 2013, Office 2013

Указывает, если и при пользователя для установки подключения.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbDriverComplete</p></td>
<td><p>0</p></td>
<td><p>Если строку подключения, предоставленную содержит ключевое слово уведомления о Доставке, диспетчер использует драйвер, строки в подключиться, в противном случае его ведет себя так что происходит, когда он указан <strong>dbDriverPrompt</strong> .</p></td>
</tr>
<tr class="even">
<td><p>dbDriverCompleteRequired</p></td>
<td><p>3</p></td>
<td><p>(По умолчанию) Действует как <strong>dbDriverComplete</strong> , за исключением драйвер отключение элементов управления для какие-либо сведения для выполнения подключения не требуется.</p></td>
</tr>
<tr class="odd">
<td><p>dbDriverNoPrompt</p></td>
<td><p>1</p></td>
<td><p>Подключите диспетчер использует драйвер, предоставленные в строке подключения. Если этот параметр не указан достаточно данных возвращается перехватываемые ошибки.</p></td>
</tr>
<tr class="even">
<td><p>dbDriverPrompt</p></td>
<td><p>2</p></td>
<td><p>Диспетчер драйверов отображает диалоговое окно <strong>Источники данных ODBC</strong> . Строку подключения, используемую для установление соединения состоит из имя источника данных (DSN), а для завершения пользователем с помощью диалоговых окон.</p></td>
</tr>
</tbody>
</table>

