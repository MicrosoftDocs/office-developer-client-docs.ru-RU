---
title: Перечисление Дриверпромптенум (DAO)
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
# <a name="driverpromptenum-enumeration-dao"></a>Перечисление Дриверпромптенум (DAO)


**Область применения**: Access 2013, Office 2013

Указывает, следует ли и когда предлагать пользователю установить подключение.

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
<td><p>дбдриверкомплете</p></td>
<td><p>нуль</p></td>
<td><p>Если предоставленная строка подключения включает ключевое слово DSN, диспетчер драйверов использует строку, предоставленную в Connect, в противном случае она ведет себя так, как при указании <strong>дбдриверпромпт</strong> .</p></td>
</tr>
<tr class="even">
<td><p>дбдриверкомплетерекуиред</p></td>
<td><p>4</p></td>
<td><p>Умолчани Аналогично <strong>дбдриверкомплете</strong> , за исключением того, что для всех элементов управления не требуется никаких сведений для завершения подключения.</p></td>
</tr>
<tr class="odd">
<td><p>дбдривернопромпт</p></td>
<td><p>1,1</p></td>
<td><p>Диспетчер драйверов использует строку подключения, указанную в разделе Connect. Если не указано достаточное количество сведений, возвращается Перехватываемая ошибка.</p></td>
</tr>
<tr class="even">
<td><p>дбдриверпромпт</p></td>
<td><p>2</p></td>
<td><p>Диспетчер драйверов отображает диалоговое окно " <strong>Источники данных ODBC</strong> ". Строка подключения, используемая для установки подключения, строится на основе имени источника данных (DSN), выбранного и выполненного пользователем с помощью диалоговых окон.</p></td>
</tr>
</tbody>
</table>

