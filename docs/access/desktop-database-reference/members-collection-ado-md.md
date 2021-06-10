---
title: Коллекция членов (ADO MD)
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
# <a name="members-collection-ado-md"></a>Коллекция членов (ADO MD)


**Область применения**: Access 2013, Office 2013

Содержит [объекты Member](member-object-ado-md.md) из уровня или положения вдоль оси.

## <a name="remarks"></a>Примечания

Коллекция **Членов** используется для того, чтобы содержать следующие типы участников:

  - Участники, которые составляют уровень куба. Они содержатся в коллекции **Members** объекта [Level.](level-object-ado-md.md) Например, используя пример из [обзоров](overview-of-multidimensional-schemas-and-data.md)многомерных схем и данных, четыре члена уровня стран — Канада, США, Великобритания и Германия.

  - Члены, которые являются детьми определенного члена в иерархии. Эти члены возвращаются [свойством Children](children-property-ado-md.md) объекта **родительского** члена. Например, опять же с использованием того же примера, два ребенка члена Канады являются Canada-East и Канада-Запад.

  - Участники, которые определяют определенное положение вдоль оси [ячейки.](cellset-object-ado-md.md) В качестве примера используется ячейки из ["Работа](working-with-multidimensional-data.md) с многомерными данными", два члена первой позиции на оси x являются Валентина и Сиэтл. Эти члены содержатся в коллекции **Members** объекта [Position.](position-object-ado-md.md)

**Members** — это стандартная коллекция ADO. С помощью свойств и методов коллекции можно сделать следующее:

  - Получение количества объектов в коллекции с помощью свойства [Count.](count-property-ado.md)

  - Возвращаем объект из коллекции с свойством [Item по](item-property-ado.md) умолчанию.

  - Обновление объектов в коллекции от поставщика с помощью метода [Обновления.](refresh-method-ado.md)

