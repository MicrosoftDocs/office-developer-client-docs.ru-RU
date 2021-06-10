---
title: Макрокоманда DeleteRecord
TOCTitle: DeleteRecord macro action
ms:assetid: c656a72c-c037-76a5-dc07-f6eccb6590dd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823132(v=office.15)
ms:contentKeyID: 48547624
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8fb20068052972696b09ea0d2165b344e97ea922
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294017"
---
# <a name="deleterecord-macro-action"></a>Макрокоманда DeleteRecord

**Область применения**: Access 2013, Office 2013

Для удаления записи можно использовать действие **DeleteRecord.**

## <a name="setting"></a>Параметр

Блок **данных CreateRecord** имеет следующие аргументы.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргументация</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Запись псевдонима</strong></p></td>
<td><p>Строка, идентифицируемая для удаления записи. Если аргумент <em>Alias</em> не указан, текущая запись удаляется.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Примечания

Для работы с последней записью, созданной в блоке данных CreateRecord, можно использовать локализованную переменную **LastCreateRecordIdentity.**  Например, используйте следующий синтаксис для ссылки на недавно созданную запись:

`[LastCreateRecordIdentity]`

