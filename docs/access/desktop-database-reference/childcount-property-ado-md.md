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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296383"
---
# <a name="childcount-property-ado-md"></a>Свойство ChildCount (ADO MD)


**Область применения**: Access 2013, Office 2013

Указывает количество элементов, для которых текущий объект [member](member-object-ado-md.md) является родительским в иерархии.

## <a name="return-values"></a>Возвращаемые значения

Возвращает целое значение **типа Long** и доступно только для чтения.

## <a name="remarks"></a>Замечания

Используйте свойство **ChildCount** для возврата оценки количества дочерних элементов, которые содержит **элемент** . Фактические дочерние элементы **элемента** могут быть возвращены свойством [Children](children-property-ado-md.md) .

Для объектов **member** из объекта [position](position-object-ado-md.md) максимальное возвращаемое значение равно 65536. Если фактическое число потомков превышает 65536, возвращаемое значение по-прежнему будет 65536. Таким образом, приложение должно интерпретировать **ChildCount** из 65536 как равное или более 65536 потомков.

Для объектов **member** из объекта [Level](level-object-ado-md.md) используйте свойство [Count](count-property-ado.md) Collections коллекции ADO для коллекции **Children** , чтобы определить точное количество дочерних элементов. Определение точного числа дочерних элементов может быть медленным, если количество дочерних элементов в коллекции велико.

