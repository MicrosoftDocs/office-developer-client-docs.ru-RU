---
title: Коллекция Axes (ADO MD)
TOCTitle: Axes collection (ADO MD)
ms:assetid: 7c719197-45f1-a5b9-665d-25cb693b1eb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249520(v=office.15)
ms:contentKeyID: 48545836
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8183b0bad1dcbaba33088dffcf21959f5b9fd993
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296936"
---
# <a name="axes-collection-ado-md"></a>Коллекция Axes (ADO MD)


**Область применения**: Access 2013, Office 2013

Содержит [объекты Axis,](axis-object-ado-md.md) которые определяют ячейки.

## <a name="remarks"></a>Примечания

Объект [Cellset](cellset-object-ado-md.md) содержит коллекцию **Axes.** После открытия **cellset** эта коллекция будет содержать по крайней мере одну **ось.** Подробнее об использовании [объектов Axis](axis-object-ado-md.md) см. в описании объекта **Axis.**


> [!NOTE]
> Ось фильтра **ячейки не** содержится в коллекции **Axes.** Дополнительные сведения см. в свойстве [FilterAxis.](filteraxis-property-ado-md.md)



**Axes** — это стандартная коллекция ADO. С помощью свойств и методов коллекции можно сделать следующее:

- Получение количества объектов в коллекции с помощью свойства [Count.](count-property-ado.md)

- Возвращаем объект из коллекции с свойством [Item по](item-property-ado.md) умолчанию.

- Обновление объектов в коллекции от поставщика с помощью метода [Обновления.](refresh-method-ado.md)

