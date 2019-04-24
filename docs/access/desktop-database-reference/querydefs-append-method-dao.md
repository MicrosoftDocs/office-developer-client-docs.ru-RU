---
title: Метод QueryDef. append (DAO)
TOCTitle: Append Method
ms:assetid: 9b62a26b-3b7c-6d26-7707-177b00a23178
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198041(v=office.15)
ms:contentKeyID: 48546570
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b4183a7b438d3f55d73eb63adb2d124da7eeecc1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300940"
---
# <a name="querydefsappend-method-dao"></a>Метод QueryDef. append (DAO)

**Область применения**: Access 2013, Office 2013

Добавляет новый объект **QueryDef** в коллекцию **QueryDef** .

## <a name="syntax"></a>Синтаксис

*Expression* . Append (***объект***)

*Expression (выражение* ) Переменная, представляющая объект **QueryDef** .

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
<td><p><em>Object</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Object</strong></p></td>
<td><p>Объектная переменная, представляющая поле, добавляемое в коллекцию.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Добавленный объект становится постоянным объектом, который хранится на диске, пока не будет удален с помощью метода **Delete** .

Добавление нового объекта выполняется немедленно, но необходимо использовать метод **Refresh** для всех остальных коллекций, на которые могут повлиять изменения структуры базы данных.

Если объект, который вы добавляете, не завершен (например, если вы не добавите объекты **field** в коллекцию **Fields** объекта **index** перед добавлением в коллекцию индексов) или **** если свойства задаются в одном или нескольких подчиненные объекты являются неправильными, при использовании метода **append** возникает ошибка. Например, если вы не указали тип поля, а затем пытаетесь добавить объект **field** в коллекцию Fields **** объекта **tabledef** , использование метода **append** вызывает ошибку во время выполнения.

