---
title: Раздел SQL в файле настройки
TOCTitle: Customization File SQL section
ms:assetid: 002c544f-fe1b-6aeb-ba9a-97b1e1159516
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248776(v=office.15)
ms:contentKeyID: 48542901
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ae259589cc8d4945068901c59105425599edc64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295137"
---
# <a name="customization-file-sql-section"></a>Раздел SQL в файле настройки


**Область применения**: Access 2013, Office 2013

Раздел **sql** может содержать новую строку SQL, которая заменяет строку команды клиента. Если строки SQL в разделе нет, раздел будет игнорироваться.

Новая строка SQL может быть *параметризирована.* То есть параметры в разделе **sql** SQL строки (назначенные по символу '?')  можно заменить соответствующими аргументами в идентификаторе в строке команд клиента (назначенный запятой-делимитированный список в скобки). Идентификатор и список аргументов ведут себя как вызов функции.

Например, предположим, что строка команды клиента — "CustomerByID(4)", заглавная строка раздела SQL — SQL CustomerByID, а новая строка раздела SQL " \[ SELECT FROM Customers WHERE \] \* CustomerID = ?". Обработщик будет создавать, SQL раздела SQL CustomerByID, а новая строка раздела SQL \[ \] будет "SELECT FROM Customers WHERE \* CustomerID =?". Обработник будет создавать строку "SELECT FROM Customers WHERE CustomerID = 4" и использовать эту строку для \* запроса источника данных.

Если новое SQL является строкой null (""), то раздел игнорируется.

Если новая строка SQL не является допустимой, то выполнение этого утверждения будет неудачным. Параметр клиента фактически игнорируется. Это можно сделать намеренно, чтобы "отключить" SQL клиентские команды, указав:

```sql 
 
[SQL default] 
SQL = " " 
```

## <a name="syntax"></a>Синтаксис

Замена SQL строки имеет форму:

**SQL=*sqlString***

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
<td><p><strong>SQL</strong></p></td>
<td><p>Буквальная строка, которая указывает, что это запись SQL раздела.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>sqlString</em></strong></p></td>
<td><p>Строка SQL, которая заменяет клиентскую строку.</p></td>
</tr>
</tbody>
</table>

