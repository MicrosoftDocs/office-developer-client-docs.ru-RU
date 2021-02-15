---
title: Метод Indexes.Append (DAO)
TOCTitle: Append Method
ms:assetid: 60dce80f-505b-e988-3ac1-8ecaae3d3d09
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194835(v=office.15)
ms:contentKeyID: 48545191
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bcebcf2f7fbce59c6050100f1763923a6025526e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291653"
---
# <a name="indexesappend-method-dao"></a>Метод Indexes.Append (DAO)

**Область применения**: Access 2013, Office 2013

Добавляет новый **индекс** в коллекцию **Indexes.**

## <a name="syntax"></a>Синтаксис

*выражение* .Append(***Object***)

*выражение* Переменная, представляюная объект **Indexes.**

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
<td><p>Объектная переменная, представляюная элемент, который будет придан коллекции.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

Добавляемый объект становится постоянным объектом, хранящимся на диске, пока вы не удалите его с помощью метода **Delete**.

Добавление нового объекта происходит незамедлительно, но следует применить метод **Refresh** для любых других коллекций, которые могут быть затронуты изменениями в структуре базы данных.

Если добавляемый объект неполный (например, если не добавлены объекты **Field** в коллекцию **Fields** объекта **Index** перед его добавлением в коллекцию **Indexes**) или заданы неверные свойства в одном или нескольких подчиненных объектах, применение метода **Append** вызывает ошибку. Например, если не указан тип поля и выполняется попытка добавить объект **Field** в коллекцию **Fields** объекта **TableDef**, применение метода **Append** вызывает ошибку во время выполнения.

