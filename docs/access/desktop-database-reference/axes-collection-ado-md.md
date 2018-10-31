---
title: Коллекция осей (ADO MD)
TOCTitle: Axes Collection (ADO MD)
ms:assetid: 7c719197-45f1-a5b9-665d-25cb693b1eb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249520(v=office.15)
ms:contentKeyID: 48545836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 612a78d8ac99a070f133fd3804f5b69c8093d47c
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862603"
---
# <a name="axes-collection-ado-md"></a>Коллекция осей (ADO MD)


**Применимо к**: Access 2013 | Office 2013

Содержит объекты [ось](axis-object-ado-md.md) , определяющие набора ячеек.

## <a name="remarks"></a>Замечания

Объект [ячеек](cellset-object-ado-md.md) содержит коллекцию **осей** . После запуска **ячеек** этой коллекции будет содержать по крайней мере один **оси**. В разделе [ось](axis-object-ado-md.md) объект для подробное объяснение того, как использовать объекты **оси** .


> [!NOTE]
> Оси фильтра набора **ячеек** не содержащихся в коллекции **осей** . Свойству [FilterAxis](filteraxis-property-ado-md.md) для получения дополнительных сведений см.



**Осей** — это обычная коллекция ADO. С помощью свойства и методы коллекции сделайте следующее:

  - Получите число объектов в коллекции со свойством [Count](count-property-ado.md) .

  - Возвращает объект из коллекции с помощью свойства [элемента](item-property-ado.md) по умолчанию.

  - Обновление объектов в коллекции от поставщика с помощью метода [обновления](refresh-method-ado.md) .

