---
title: Children Property (ADO MD)
TOCTitle: Children Property (ADO MD)
ms:assetid: 66eff203-68e5-a36d-eb2f-2e9faa80deb6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249400(v=office.15)
ms:contentKeyID: 48545352
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e126b203e2282f96070f1f3eb14a9b926c04f432
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480345"
---
# <a name="children-property-ado-md"></a>Children Property (ADO MD)


**Применимо к**: Access 2013 | Office 2013

Возвращает коллекцию [членов](members-collection-ado-md.md) , для которого текущий [элемент](member-object-ado-md.md) является родительской в иерархии.

## <a name="return-values"></a>Return Values

Возвращает коллекцию **элементов** и доступен только для чтения.

## <a name="remarks"></a>Замечания

**В свойстве** содержит коллекцию **Members** , для которого текущий **член** является иерархической родительского. Конечные объекты уровень **член** не содержат дочерние членов в коллекции **элементов** . Это свойство поддерживается только для объектов **члена** , принадлежащих к объекту [уровень](level-object-ado-md.md) . Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [позиции](position-object-ado-md.md) .

