---
title: Действия макрокоманду УдалитьЗапись макроса
TOCTitle: DeleteRecord Macro Action
ms:assetid: c656a72c-c037-76a5-dc07-f6eccb6590dd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823132(v=office.15)
ms:contentKeyID: 48547624
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 17cc677ed5762c6274db80105cdf8e899565ecb9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880882"
---
# <a name="deleterecord-macro-action"></a>Действия макрокоманду УдалитьЗапись макроса

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

## <a name="remarks"></a>Замечания

Локальной переменной **LastCreateRecordIdentity** можно использовать для работы с последней записи, созданной в блоке данных **СоздатьЗапись** . Например используйте следующий синтаксис для ссылки на недавно созданного записи:

`[LastCreateRecordIdentity]`

