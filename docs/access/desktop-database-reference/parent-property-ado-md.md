---
title: Свойство Parent (ADO MD)
TOCTitle: Parent property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e0c0eef638cb76676cd2287a34c0e4b17bd89c4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287792"
---
# <a name="parent-property-ado-md"></a>Свойство Parent (ADO MD)


**Область применения**: Access 2013, Office 2013

Указывает члена, который является родительским для текущего элемента в иерархии.

## <a name="return-values"></a>Возвращаемые значения

Возвращает объект [member](member-object-ado-md.md) и доступен только для чтения.

## <a name="remarks"></a>Замечания

Элемент, расположенный на верхнем уровне иерархии (корень), не имеет родителя. Это свойство поддерживается только для объектов **member** , принадлежащих объекту [уровня](level-object-ado-md.md) . При обращении к этому свойству из объектов **member** , принадлежащих объекту [position](position-object-ado-md.md) , возникает ошибка.

