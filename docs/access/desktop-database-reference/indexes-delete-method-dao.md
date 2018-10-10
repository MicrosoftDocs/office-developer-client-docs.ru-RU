---
title: Indexes.Delete Method (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b30748c0a1388a1175512e3b8d3fd1970795b821
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480640"
---
# <a name="indexesdelete-method-dao"></a>Indexes.Delete Method (DAO)


**Применимо к**: Access 2013 | Office 2013

Удаляет указанный **индекс** из набора **индексов** .

## <a name="syntax"></a>Синтаксис

*выражение* . Удаление (***имя***)

*выражение* Переменная, которая представляет объект **индексов** .

### <a name="parameters"></a>Параметры

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
<td><p>Имя</p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>Имя индекс, который требуется удалить.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Метод **Delete** поддерживается только в том случае, когда объект **индекса** новые и еще не был добавлен к базе данных.

