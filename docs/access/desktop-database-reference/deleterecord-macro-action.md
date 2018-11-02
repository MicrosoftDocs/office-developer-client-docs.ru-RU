---
title: Макрокоманда DeleteRecord
TOCTitle: DeleteRecord macro action
ms:assetid: c656a72c-c037-76a5-dc07-f6eccb6590dd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823132(v=office.15)
ms:contentKeyID: 48547624
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 052e7a489eaec526db1552ced89b095f65f652df
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921588"
---
# <a name="deleterecord-macro-action"></a>Макрокоманда DeleteRecord

**Применимо к**: Access 2013, Office 2013

Чтобы удалить запись, можно использовать **УдалитьЗапись** .

## <a name="setting"></a>Параметр

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

## <a name="remarks"></a>Примечания

Локальной переменной **LastCreateRecordIdentity** можно использовать для работы с последней записи, созданной в блоке данных **СоздатьЗапись** . Например используйте следующий синтаксис для ссылки на недавно созданного записи:

`[LastCreateRecordIdentity]`

