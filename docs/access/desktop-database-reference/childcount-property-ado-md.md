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

Указывает количество членов, для которых текущий объект [Member](member-object-ado-md.md) является родителем в иерархии.

## <a name="return-values"></a>Возвращаемые значения

Возвращает длинный **ряд** и только для чтения.

## <a name="remarks"></a>Примечания

Используйте свойство **ChildCount,** чтобы вернуть оценку того, сколько детей у **участника.** Фактические дети **участника** могут быть возвращены [свойством Children.](children-property-ado-md.md)

Для **объектов Member** из объекта [Position](position-object-ado-md.md) максимальное число возвращаемого — 65536. Если фактическое число детей превышает 65536, возвращенные значения по-прежнему будут 65536. Поэтому приложение должно интерпретировать **childCount** 65536 как равное или больше 65536 детей.

Для **объектов Member** из [объекта Level](level-object-ado-md.md) используйте [](count-property-ado.md) свойство Граф коллекции ADO в коллекции **Children,** чтобы определить точное число детей. Определение точного числа детей может быть медленным, если количество детей в коллекции большое.

