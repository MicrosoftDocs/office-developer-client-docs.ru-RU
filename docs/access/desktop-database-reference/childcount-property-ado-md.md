---
title: Свойство ChildCount (ADO MD)
TOCTitle: ChildCount property (ADO MD)
ms:assetid: ff1872f0-d5f6-174e-0473-7997a462ca81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250309(v=office.15)
ms:contentKeyID: 48548956
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f8e0fc98d7868eb5462bd7d8714e1a8eda1cfcf
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720753"
---
# <a name="childcount-property-ado-md"></a>Свойство ChildCount (ADO MD)


**Применимо к**: Access 2013, Office 2013

Указывает число участников, для которых текущего объекта [член](member-object-ado-md.md) является родительской в иерархии.

## <a name="return-values"></a>Возвращаемые значения

Возвращает значение типа **Long** integer и доступен только для чтения.

## <a name="remarks"></a>Замечания

Свойство **ChildCount** Возвращает оценку сколько потомки **члена** имеет. Фактические потомки **члена** можно возвращается свойством [дочерних элементов](children-property-ado-md.md) .

Для объектов **члена** из [положение](position-object-ado-md.md) объекта возвращается не более 65536. Если фактическое число дочерних элементов превышает 65536, возвращаемое значение будет по-прежнему 65536. Таким образом приложение следует воспринимать **ChildCount** из 65536 как равно или больше, чем 65536 дочерних элементов.

Для объектов **члена** из объекта [уровень](level-object-ado-md.md) используйте свойство [Count](count-property-ado.md) коллекции ADO на коллекцию **дочерних элементов** , чтобы определить точное количество дочерних элементов. Определение точное количество дочерних элементов может быть медленным, если большое число дочерних объектов в коллекции.

