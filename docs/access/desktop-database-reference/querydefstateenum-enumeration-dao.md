---
title: QueryDefStateEnum Enumeration (DAO)
TOCTitle: QueryDefStateEnum Enumeration
ms:assetid: edfa3085-f8b4-b813-0828-2ba2a9dc0b9d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836359(v=office.15)
ms:contentKeyID: 48548549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 68f6f1e96ae57508d94ea341b36e3a6b32cac660
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481838"
---
# <a name="querydefstateenum-enumeration-dao"></a>QueryDefStateEnum Enumeration (DAO)


**Применимо к**: Access 2013 | Office 2013

Используется со свойством **подготовить** для указания метода используется, чтобы указать, как следует подготовить запрос.

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
<td><p>dbQPrepare</p></td>
<td><p>1</p></td>
<td><p>(По умолчанию) Инструкция подготовлена (то есть, вызывается ODBC SQLPrepare API).</p></td>
</tr>
<tr class="even">
<td><p>dbQUnprepare</p></td>
<td><p>2</p></td>
<td><p>Оператор не подготовлен (то есть, вызывается ODBC SQLExecDirect API).</p></td>
</tr>
</tbody>
</table>

