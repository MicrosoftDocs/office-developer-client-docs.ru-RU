---
title: Метод Indexes.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0c725919b6509b5c802502fc8280823c407516f6
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998828"
---
# <a name="indexesdelete-method-dao"></a>Метод Indexes.Delete (DAO)

**Применимо к**: Access 2013, Office 2013

Удаляет указанный **индекс** из набора **индексов** .

## <a name="syntax"></a>Синтаксис

*выражение* . Удаление (***имя***)

*выражение* Переменная, которая представляет объект **индексов** .

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
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>Имя индекс, который требуется удалить.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Метод **Delete** поддерживается только в том случае, когда объект **индекса** новые и еще не был добавлен к базе данных.

