---
title: Объект Axis (ADO MD)
TOCTitle: Axis object (ADO MD)
ms:assetid: a4332b69-8900-08f1-a4e2-9395d005ed42
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249763(v=office.15)
ms:contentKeyID: 48546807
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 23fdb0d9ba636ae58fa19b42d5a8a47cb01d4ab2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720732"
---
# <a name="axis-object-ado-md"></a>Объект Axis (ADO MD)


**Применимо к**: Access 2013, Office 2013

Представляет позиционные или оси фильтра набора ячеек, содержащий выбранные элементы из одного или нескольких измерений.

## <a name="remarks"></a>Замечания

Объект **оси** можно заключенный в коллекцию [осей](axes-collection-ado-md.md) или возвращается свойством [FilterAxis](filteraxis-property-ado-md.md) [ячеек](cellset-object-ado-md.md).

С помощью семейств сайтов и свойствам объекта **ось** сделайте следующее:

- Определение **оси** с помощью свойства [Name](name-property-ado-md.md) .

- Выполните итерацию по каждой позиции по **оси** с использованием [положения](positions-collection-ado-md.md) коллекции.

- Получите число измерений на **оси** со свойством [DimensionCount](dimensioncount-property-ado-md.md) .

- Получение атрибутов поставщика **ось** , коллекции стандартных ADO [Свойства](properties-collection-ado.md) .

