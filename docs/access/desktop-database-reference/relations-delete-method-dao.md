---
title: Метод отношениях. Delete (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e0b7fbf20a8732e8f4db525fd32bf4e5737b4d79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306967"
---
# <a name="relationsdelete-method-dao"></a>Метод отношениях. Delete (DAO)

**Область применения**: Access 2013, Office 2013

Удаляет указанное **отношение** из коллекции **связей** .

## <a name="syntax"></a>Синтаксис

*Expression* . Delete (***имя***)

*Expression (выражение* ) Переменная, представляющая объект **отношений** .

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
<td><p>Имя отношения, которое требуется удалить.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Метод **Delete** поддерживается, только если объект **relation** является новым, неприсоединенным объектом.

