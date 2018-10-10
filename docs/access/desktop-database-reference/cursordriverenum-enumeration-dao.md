---
title: CursorDriverEnum Enumeration (DAO)
TOCTitle: CursorDriverEnum Enumeration
ms:assetid: d0312ece-c30a-7d61-d5f3-75edf0d0afc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834707(v=office.15)
ms:contentKeyID: 48547832
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bcce8eefad7fcad7dee7e46274ffc45125dc36c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482127"
---
# <a name="cursordriverenum-enumeration-dao"></a>CursorDriverEnum Enumeration (DAO)


**Применимо к**: Access 2013 | Office 2013

Указывает тип драйвера курсора.

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
<td><p>dbUseClientBatchCursor</p></td>
<td><p>3</p></td>
<td><p>Всегда использует библиотеку FoxPro курсора. Этот параметр является обязательным для выполнения пакета обновлений.</p></td>
</tr>
<tr class="even">
<td><p>dbUseDefaultCursor</p></td>
<td><p>-1</p></td>
<td><p>(По умолчанию) Использует записей на стороне сервера, если поддерживается сервером в противном случае используется библиотека курсора ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>dbUseNoCursor</p></td>
<td><p>4</p></td>
<td><p>Открывает все курсоры (то есть, объекты <strong>набора записей</strong> ) в качестве типа, последовательного доступа только для чтения, имеющее размер строк 1. Также известной как &quot;cursorless запросов.&quot;</p></td>
</tr>
<tr class="even">
<td><p>dbUseODBCCursor</p></td>
<td><p>1</p></td>
<td><p>Всегда используется библиотека курсора ODBC. Этот параметр обеспечивает более высокую производительность на небольшой результирующий набор, но снижает быстро для больших наборов результатов.</p></td>
</tr>
<tr class="odd">
<td><p>dbUseServerCursor</p></td>
<td><p>2</p></td>
<td><p>Всегда использует записей на стороне сервера. Для самых больших операций этого параметра обеспечивает более высокую производительность, но может привести к более сетевого трафика.</p></td>
</tr>
</tbody>
</table>

