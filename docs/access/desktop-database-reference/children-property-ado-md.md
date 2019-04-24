---
title: Свойство Children (ADO MD)
TOCTitle: Children property (ADO MD)
ms:assetid: 66eff203-68e5-a36d-eb2f-2e9faa80deb6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249400(v=office.15)
ms:contentKeyID: 48545352
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 27d69e760b65a917270b0851743c108692c601e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296369"
---
# <a name="children-property-ado-md"></a>Свойство Children (ADO MD)


**Область применения**: Access 2013, Office 2013

Возвращает коллекцию [Members](members-collection-ado-md.md) , для которой текущий [элемент](member-object-ado-md.md) является родительским в иерархии.

## <a name="return-values"></a>Возвращаемые значения

Возвращает коллекцию **Members** и доступна только для чтения.

## <a name="remarks"></a>Замечания

Свойство **Children** содержит коллекцию **Members** , для которой текущий **участник** является иерархическим родителем. Объекты **member** конечного уровня не имеют дочерних элементов в коллекции **Members** . Это свойство поддерживается только для объектов **member** , принадлежащих объекту [уровня](level-object-ado-md.md) . При обращении к этому свойству из объектов **member** , принадлежащих объекту [position](position-object-ado-md.md) , возникает ошибка.

