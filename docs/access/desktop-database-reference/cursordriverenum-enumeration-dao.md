---
title: Перечисление Курсордриверенум (DAO)
TOCTitle: CursorDriverEnum enumeration
ms:assetid: d0312ece-c30a-7d61-d5f3-75edf0d0afc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834707(v=office.15)
ms:contentKeyID: 48547832
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f2bf52943a84d6f2e60891d63810bc0bbb6ecb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295249"
---
# <a name="cursordriverenum-enumeration-dao"></a>Перечисление Курсордриверенум (DAO)

**Область применения**: Access 2013, Office 2013

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
<td><p>Дбусеклиентбатчкурсор</p></td>
<td><p>4</p></td>
<td><p>Всегда использует библиотеку курсоров FoxPro. Этот параметр необходим для выполнения пакетных обновлений.</p></td>
</tr>
<tr class="even">
<td><p>Дбуседефаулткурсор</p></td>
<td><p>–1</p></td>
<td><p>Умолчани Использует курсоры на стороне сервера, если они поддерживаются сервером; в противном случае используется библиотека курсоров ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>Дбусенокурсор</p></td>
<td><p>SP4</p></td>
<td><p>Открывает все курсоры (то есть объекты <strong>Recordset</strong> ) в качестве однонаправленного типа, доступного только для чтения, с размером набора строк 1. Также называются &quot;запросами без курсора.&quot;</p></td>
</tr>
<tr class="even">
<td><p>Дбусеодбккурсор</p></td>
<td><p>1,1</p></td>
<td><p>Всегда использует библиотеку курсоров ODBC. Этот параметр обеспечивает лучшую производительность для небольших наборов результатов, но быстро уменьшает масштаб для наборов результатов.</p></td>
</tr>
<tr class="odd">
<td><p>Дбусесерверкурсор</p></td>
<td><p>2</p></td>
<td><p>Всегда использует курсоры на стороне сервера. Для большинства операций этот вариант обеспечивает лучшую производительность, но может привести к увеличению объема сетевого трафика.</p></td>
</tr>
</tbody>
</table>

