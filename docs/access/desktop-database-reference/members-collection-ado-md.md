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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721327"
---
# <a name="members-collection-ado-md"></a>Коллекция Members (ADO MD)


**Применимо к**: Access 2013, Office 2013

Содержит объекты [члена](member-object-ado-md.md) с уровнем или положение оси.

## <a name="remarks"></a>Замечания

**Члены** коллекции используется содержат следующие типы элементов:

  - Члены, которые составляют уровень в кубе. Эти содержащихся в коллекции **элементы** объекта [уровень](level-object-ado-md.md) . Например с помощью образца из [Обзор многомерные схемы и данных](overview-of-multidimensional-schemas-and-data.md), четырех элементов уровня странах, Канада, США, Великобритании и Германии.

  - Члены, которые являются дочерними конкретный элемент в иерархии. Эти элементы возвращаются свойством [потомки](children-property-ado-md.md) **члена** родительского объекта. Например два дочерних элементов элемента Канада еще раз с помощью же пример, Канада-Восток и запад Канада.

  - Элементы, определяющие определенного положения оси набора [ячеек](cellset-object-ado-md.md). Использование ячеек от [работы с многомерные данные](working-with-multidimensional-data.md) в качестве примера, два членов первого положение на оси x являются любимая и Seattle. Эти элементы содержащихся в коллекции **элементы** объекта [положение](position-object-ado-md.md) .

**Члены** — это обычная коллекция ADO. С помощью свойства и методы коллекции сделайте следующее:

  - Получите число объектов в коллекции со свойством [Count](count-property-ado.md) .

  - Возвращает объект из коллекции с помощью свойства [элемента](item-property-ado.md) по умолчанию.

  - Обновление объектов в коллекции от поставщика с помощью метода [обновления](refresh-method-ado.md) .

