---
title: Customization File SQL Section
TOCTitle: Customization File SQL Section
ms:assetid: 002c544f-fe1b-6aeb-ba9a-97b1e1159516
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248776(v=office.15)
ms:contentKeyID: 48542901
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 09be671ba15727e3612ade78c5b54af12b1d1c57
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480114"
---
# <a name="customization-file-sql-section"></a>Customization File SQL Section


**Применимо к**: Access 2013 | Office 2013

В разделе **sql** может содержать строку SQL, которая заменяет строки команды клиента. Если строка не SQL в разделе разделе будет игнорироваться.

Создать строку SQL может быть *параметризованный*. То есть соответствующих аргументы в *идентификатор* в командной строке клиента (обозначенного разделенный запятыми список в скобки) могут быть заменены параметров в строке SQL раздел **sql** (обозначенного символ «?»). Идентификатор и список аргументов обрабатываются как вызов функции.

Предположим, например, строки команды клиента — «CustomerByID(4)», заголовок раздела SQL — \[SQL CustomerByID\] , и — это новый раздел строки SQL «ВЫБЕРИТЕ \* из клиентов WHERE CustomerID = ?». Будет создан обработчик, заголовок раздела SQL — \[SQL CustomerByID\] , и — это новый раздел строки SQL «ВЫБЕРИТЕ \* из клиентов WHERE CustomerID = ?». Будет создан обработчик «ВЫБЕРИТЕ \* из клиентов WHERE CustomerID = 4» и использовать эту строку для запроса источника данных.

Если новые инструкции SQL — это пустая строка ("»), а затем раздел пропускается.

Если создать строку инструкции SQL не является допустимым, выполнение инструкции завершится ошибкой. Параметр клиента эффективно игнорируется. Для этого специально для «отключения» все команды SQL клиента, указав:

```sql 
 
[SQL default] 
SQL = " " 
```

## <a name="syntax"></a>Синтаксис

Замена запись строки SQL не формы:

**SQL = * sqlString***

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
<td><p><strong>SQL</strong></p></td>
<td><p>Строковый литерал, которое указывает, это является записью раздел SQL.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>sqlString</em></strong></p></td>
<td><p>Строка SQL, которая заменяет строку клиента.</p></td>
</tr>
</tbody>
</table>

