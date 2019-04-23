---
title: Методы TableDef. Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63f543fd86e309372e0432c3e45513cd9d3942ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313995"
---
# <a name="tabledefsdelete-method-dao"></a>Методы TableDef. Delete (DAO)

**Область применения**: Access 2013, Office 2013

Удаляет указанный объект **tabledef** из коллекции **tabledef** .

## <a name="syntax"></a>Синтаксис

*Expression* . Delete (***имя***)

*Expression (выражение* ) Переменная, представляющая объект **TableDefs** .

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
<td><p>Имя объекта TableDef, который необходимо удалить.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Метод Delete поддерживается только в том случае, если объект **tabledef** является новым и не был добавлен в базу данных, или если для **** свойства объекта **tabledef** задано значение **true**.

