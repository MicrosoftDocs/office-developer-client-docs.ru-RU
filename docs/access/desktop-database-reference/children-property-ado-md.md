---
title: Свойство Children (ADO MD)
TOCTitle: Children Property (ADO MD)
ms:assetid: 66eff203-68e5-a36d-eb2f-2e9faa80deb6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249400(v=office.15)
ms:contentKeyID: 48545352
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 57049e0e68e4620664687cd261881af953de189f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875212"
---
# <a name="children-property-ado-md"></a>Свойство Children (ADO MD)


**Применимо к**: Access 2013, Office 2013

Возвращает коллекцию [членов](members-collection-ado-md.md) , для которого текущий [элемент](member-object-ado-md.md) является родительской в иерархии.

## <a name="return-values"></a>Возвращаемые значения

Возвращает коллекцию **элементов** и доступен только для чтения.

## <a name="remarks"></a>Замечания

**В свойстве** содержит коллекцию **Members** , для которого текущий **член** является иерархической родительского. Конечные объекты уровень **член** не содержат дочерние членов в коллекции **элементов** . Это свойство поддерживается только для объектов **члена** , принадлежащих к объекту [уровень](level-object-ado-md.md) . Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [позиции](position-object-ado-md.md) .

