---
title: Метод indexes. append (DAO)
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
# <a name="indexesappend-method-dao"></a>Метод indexes. append (DAO)

**Область применения**: Access 2013, Office 2013

Добавляет новый **индекс** в коллекцию **indexes** .

## <a name="syntax"></a>Синтаксис

*Expression* . Append (***объект***)

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
<td><p><em>Object</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Object</strong></p></td>
<td><p>Объектная переменная, представляющая элемент, добавляемый в коллекцию.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Добавленный объект становится постоянным объектом, который хранится на диске, пока не будет удален с помощью метода **Delete** .

Добавление нового объекта выполняется немедленно, но необходимо использовать метод **Refresh** для всех остальных коллекций, на которые могут повлиять изменения структуры базы данных.

Если объект, который вы добавляете, не завершен (например, если вы не добавите объекты **field** в коллекцию **Fields** объекта **index** перед добавлением в коллекцию индексов) или **** если свойства задаются в одном или нескольких подчиненные объекты являются неправильными, при использовании метода **append** возникает ошибка. Например, если вы не указали тип поля, а затем пытаетесь добавить объект **field** в коллекцию Fields **** объекта **tabledef** , использование метода **append** вызывает ошибку во время выполнения.

