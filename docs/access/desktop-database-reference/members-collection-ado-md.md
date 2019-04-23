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

Содержит объекты [member](member-object-ado-md.md) на уровне или позиции вдоль оси.

## <a name="remarks"></a>Замечания

Коллекция **Members** используется для хранения следующих типов элементов:

  - Элементы, составляющие уровень в Кубе. Они включены в коллекцию **Members** объекта [Level](level-object-ado-md.md) . Например, используя пример из [обзора многомерНых схем и данных](overview-of-multidimensional-schemas-and-data.md), четыре члена уровня стран — Канады, США, Великобритании и Германии.

  - Элементы, которые являются дочерними по отношению к определенному члену в иерархии. Эти элементы возвращаются свойством [Children](children-property-ado-md.md) родительского объекта **member** . Например, при использовании того же примера двумя дочерними элементами члена Канады являются Канада — Канада и Канада (запад).

  - Элементы, определяющие определенную позицию вдоль оси набора [ячеек](cellset-object-ado-md.md). Используя набор ячеек для [работы с многомерНыми данными](working-with-multidimensional-data.md) в качестве примера, два элемента первой позиции на оси x — любимая и Сиэтл. Эти элементы входят в коллекцию **Members** объекта [position](position-object-ado-md.md) .

**Members** — это стандартная коллекция ADO. С помощью свойств и методов коллекции можно выполнить следующие действия:

  - Получите число объектов в коллекции со свойством [Count](count-property-ado.md) .

  - Возвращает объект из коллекции со свойством [Item](item-property-ado.md) по умолчанию.

  - Обновление объектов в коллекции от поставщика с помощью метода [Refresh](refresh-method-ado.md) .

