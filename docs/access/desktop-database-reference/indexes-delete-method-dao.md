---
title: Метод indexes. Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ab52f353b7a3e636f64ff2ad6ad5354d62bed48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291554"
---
# <a name="indexesdelete-method-dao"></a>Метод indexes. Delete (DAO)

**Область применения**: Access 2013, Office 2013

Удаляет указанный **индекс** из коллекции **индексов** .

## <a name="syntax"></a>Синтаксис

*Expression* . Delete (***имя***)

*Expression (выражение* ) Переменная, представляющая объект **индексов** .

## <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательно/необязательно</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Имя индекса, который требуется удалить.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Метод **Delete** поддерживается только в том случае, если объект **index** является новым и не добавлен в базу данных.

