---
title: Свойство PageCount (ADO)
TOCTitle: PageCount property (ADO)
ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15)
ms:contentKeyID: 48546609
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b37ccc0c9a61e00b3c2e8f5eb3367831e5ddea43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288121"
---
# <a name="pagecount-property-ado"></a>Свойство PageCount (ADO)


**Область применения**: Access 2013, Office 2013

Указывает количество страниц данных, содержащихся в объекте [Recordset](recordset-object-ado.md) .

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **типа Long** , которое указывает количество страниц в **наборе записей**.

## <a name="remarks"></a>Примечания

Используйте свойство **PageCount** , чтобы определить, сколько страниц данных находится в объекте **Recordset** . *Страницы* — это группы записей, размер которых равен значению свойства [pageSize](pagesize-property-ado.md) . Даже если последняя страница неполна, так как число записей меньше, чем значение **pageSize** , оно считается дополнительной страницей в значении **PageCount** . Если объект **Recordset** не поддерживает это свойство, значение будет равно-1, чтобы указать, что **PageCount** недоступен.

Чтобы узнать больше о функциональных возможностях страниц, ознакомьтесь со статьей свойства **pageSize** и [AbsolutePage](absolutepage-property-ado.md) .

