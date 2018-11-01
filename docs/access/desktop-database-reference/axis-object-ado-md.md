---
title: Объект Axis (ADO MD)
TOCTitle: Axis Object (ADO MD)
ms:assetid: a4332b69-8900-08f1-a4e2-9395d005ed42
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249763(v=office.15)
ms:contentKeyID: 48546807
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76fe2e0aa90397b32d95172318f3657741e1b1ec
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875023"
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

