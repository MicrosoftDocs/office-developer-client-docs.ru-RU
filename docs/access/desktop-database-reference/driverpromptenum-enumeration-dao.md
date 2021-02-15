---
title: DriverPromptEnum enumeration (DAO)
TOCTitle: DriverPromptEnum Enumeration
ms:assetid: 8dda5e9f-a58f-a62d-eb49-5966d4a1e086
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197361(v=office.15)
ms:contentKeyID: 48546266
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9612c0713a86ed6ad34a5eff61e45efcddf6cf24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293667"
---
# <a name="driverpromptenum-enumeration-dao"></a>DriverPromptEnum enumeration (DAO)


**Область применения**: Access 2013, Office 2013

Указывает, нужно ли и когда пользователю предложено установить подключение.

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
<td><p>Если указанная строка подключения содержит ключевое слово DSN, диспетчер драйверов использует строку, указанную при подключении, в противном случае она ведет себя так же, как при указании <strong>dbDriverPrompt.</strong></p></td>
</tr>
<tr class="even">
<td><p>dbDriverCompleteRequired</p></td>
<td><p>3 </p></td>
<td><p>(По умолчанию) Ведет себя как <strong>dbDriverComplete,</strong> за исключением того, что драйвер отключает элементы управления для любых сведений, не необходимых для завершения подключения.</p></td>
</tr>
<tr class="odd">
<td><p>dbDriverNoPrompt</p></td>
<td><p>1 </p></td>
<td><p>Диспетчер драйверов использует строку подключения, предоставленную при подключении. Если достаточные сведения не предоставлены, возвращается захватимая ошибка.</p></td>
</tr>
<tr class="even">
<td><p>dbDriverPrompt</p></td>
<td><p>2 </p></td>
<td><p>Диспетчер драйверов отображает диалоговое окно "Источники данных <strong>ODBC".</strong> Строка подключения, используемая для установления подключения, создается из имени источника данных (DSN), выбранного и заполненного пользователем через диалоговое окно.</p></td>
</tr>
</tbody>
</table>

