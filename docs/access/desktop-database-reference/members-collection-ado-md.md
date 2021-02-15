---
title: Коллекция Members (ADO MD)
TOCTitle: Members collection (ADO MD)
ms:assetid: 1389c554-e4f1-107d-22c6-7fe851d53d23
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248910(v=office.15)
ms:contentKeyID: 48543371
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: adc8ed771bcba6a4b6532b33b27980f8aab695c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289243"
---
# <a name="members-collection-ado-md"></a>Коллекция Members (ADO MD)


**Область применения**: Access 2013, Office 2013

Содержит [объекты Member](member-object-ado-md.md) из уровня или положения вдоль оси.

## <a name="remarks"></a>Заметки

Коллекция **Members** содержит следующие типы членов:

  - Члены, которые составляют уровень куба. Они содержатся в коллекции **Members** объекта [Level.](level-object-ado-md.md) Например, используя пример из обзора многомерных схем и [данных,](overview-of-multidimensional-schemas-and-data.md)четыре члена уровня стран : Канада, США, Соединенное Королевство и Германия.

  - Члены, которые являются детами определенного члена в иерархии. Эти члены возвращаются [свойством Children](children-property-ado-md.md) родительского **объекта Member.** Например, еще раз, используя тот же пример, два потомка члена группы «КанадаCanada-East и Канада—Запад.

  - Члены, которые определяют определенное положение вдоль оси [ячеек.](cellset-object-ado-md.md) В качестве примера [](working-with-multidimensional-data.md) можно использовать ячейки из "Работа с многомерными данными", двумя членами первой позиции на оси X являются "Сиэтл" и "Сиэтл". Эти члены содержатся в коллекции **Members** объекта [Position.](position-object-ado-md.md)

**Members** — это стандартная коллекция ADO. С помощью свойств и методов коллекции можно сделать следующее:

  - Получите количество объектов в коллекции с помощью свойства [Count.](count-property-ado.md)

  - Возвращает объект из коллекции со свойством [Item по](item-property-ado.md) умолчанию.

  - Обновите объекты в коллекции от поставщика с помощью [метода Refresh.](refresh-method-ado.md)

