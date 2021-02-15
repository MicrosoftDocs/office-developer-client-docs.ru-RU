---
title: Метод Relations.Append (DAO)
TOCTitle: Append Method
ms:assetid: dafcc7b8-b30d-2ba2-631d-eca0f882fc2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835334(v=office.15)
ms:contentKeyID: 48548094
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052904
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b8374832ad6cd6bac30fa9d129e54fb6ab4c8fd4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306988"
---
# <a name="relationsappend-method-dao"></a>Метод Relations.Append (DAO)

**Область применения**: Access 2013, Office 2013

Добавляет новое **отношение к** коллекции **Relations.**

## <a name="syntax"></a>Синтаксис

*выражение* .Append(***Object***)

*выражение* Переменная, представляюная объект **Relations.**

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
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Object</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Object</strong></p></td>
<td><p>Объектная переменная, представляющая поле, которое добавляется в коллекцию.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Добавляемый объект становится постоянным объектом, хранящимся на диске, пока вы не удалите его с помощью метода **Delete**.

Добавление нового объекта происходит незамедлительно, но следует применить метод **Refresh** для любых других коллекций, которые могут быть затронуты изменениями в структуре базы данных.

Если добавляемый объект неполный (например, если не добавлены объекты **Field** в коллекцию **Fields** объекта **Index** перед его добавлением в коллекцию **Indexes**) или заданы неверные свойства в одном или нескольких подчиненных объектах, применение метода **Append** вызывает ошибку. Например, если не указан тип поля и выполняется попытка добавить объект **Field** в коллекцию **Fields** объекта **TableDef**, применение метода **Append** вызывает ошибку во время выполнения.

