---
title: ChildCount Property (ADO MD)
TOCTitle: ChildCount Property (ADO MD)
ms:assetid: ff1872f0-d5f6-174e-0473-7997a462ca81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250309(v=office.15)
ms:contentKeyID: 48548956
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 84e2e9873e076128c42e9fa7ae46d902f47865c7
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606027"
---
# <a name="childcount-property-ado-md"></a>ChildCount Property (ADO MD)


**Применимо к**: Access 2013 | Office 2013

Указывает число участников, для которых текущего объекта [член](member-object-ado-md.md) является родительской в иерархии.

<<<<<<< HEAD
## <a name="return-values"></a>Return Values
=======
## <a name="return-values"></a>Возвращаемые значения
>>>>>>> master

Возвращает значение типа **Long** integer и доступен только для чтения.

## <a name="remarks"></a>Замечания

Свойство **ChildCount** Возвращает оценку сколько потомки **члена** имеет. Фактические потомки **члена** можно возвращается свойством [дочерних элементов](children-property-ado-md.md) .

Для объектов **члена** из [положение](position-object-ado-md.md) объекта возвращается не более 65536. Если фактическое число дочерних элементов превышает 65536, возвращаемое значение будет по-прежнему 65536. Таким образом приложение следует воспринимать **ChildCount** из 65536 как равно или больше, чем 65536 дочерних элементов.

Для объектов **члена** из объекта [уровень](level-object-ado-md.md) используйте свойство [Count](count-property-ado.md) коллекции ADO на коллекцию **дочерних элементов** , чтобы определить точное количество дочерних элементов. Определение точное количество дочерних элементов может быть медленным, если большое число дочерних объектов в коллекции.

