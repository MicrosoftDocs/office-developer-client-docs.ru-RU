---
title: Свойство ChildCount (ADO MD)
TOCTitle: ChildCount property (ADO MD)
ms:assetid: ff1872f0-d5f6-174e-0473-7997a462ca81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250309(v=office.15)
ms:contentKeyID: 48548956
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8a55f54bfe796f9dfa0fc3ec157c8f7cfe9fa11
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925221"
---
# <a name="childcount-property-ado-md"></a>Свойство ChildCount (ADO MD)


**Применимо к**: Access 2013, Office 2013

Указывает число участников, для которых текущего объекта [член](member-object-ado-md.md) является родительской в иерархии.

## <a name="return-values"></a>Возвращаемые значения

Возвращает значение типа **Long** integer и доступен только для чтения.

## <a name="remarks"></a>Примечания

Свойство **ChildCount** Возвращает оценку сколько потомки **члена** имеет. Фактические потомки **члена** можно возвращается свойством [дочерних элементов](children-property-ado-md.md) .

Для объектов **члена** из [положение](position-object-ado-md.md) объекта возвращается не более 65536. Если фактическое число дочерних элементов превышает 65536, возвращаемое значение будет по-прежнему 65536. Таким образом приложение следует воспринимать **ChildCount** из 65536 как равно или больше, чем 65536 дочерних элементов.

Для объектов **члена** из объекта [уровень](level-object-ado-md.md) используйте свойство [Count](count-property-ado.md) коллекции ADO на коллекцию **дочерних элементов** , чтобы определить точное количество дочерних элементов. Определение точное количество дочерних элементов может быть медленным, если большое число дочерних объектов в коллекции.

