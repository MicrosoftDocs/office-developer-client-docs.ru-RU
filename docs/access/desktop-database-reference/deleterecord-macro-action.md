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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725954"
---
# <a name="deleterecord-macro-action"></a>Макрокоманда DeleteRecord

**Применимо к**: Access 2013, Office 2013

Чтобы удалить запись, можно использовать **УдалитьЗапись** .

## <a name="setting"></a>Setting

Блок данных **СоздатьЗапись** имеет следующие аргументы.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Запись псевдонима</strong></p></td>
<td><p>Строка, идентифицирующая записи для удаления. Если аргумент <em>псевдоним</em> не указан, текущий запись удаляется.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Замечания

Локальной переменной **LastCreateRecordIdentity** можно использовать для работы с последней записи, созданной в блоке данных **СоздатьЗапись** . Например используйте следующий синтаксис для ссылки на недавно созданного записи:

`[LastCreateRecordIdentity]`

