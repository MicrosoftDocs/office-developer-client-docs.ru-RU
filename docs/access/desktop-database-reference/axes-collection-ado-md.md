---
title: Коллекция осей (ADO MD)
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
# <a name="axes-collection-ado-md"></a>Коллекция осей (ADO MD)


**Область применения**: Access 2013, Office 2013

Содержит объекты [осей](axis-object-ado-md.md) , определяющие набор ячеек.

## <a name="remarks"></a>Замечания

Объект набора [ячеек](cellset-object-ado-md.md) содержит коллекцию **осей** . После открытия набора **ячеек** эта коллекция будет содержать по крайней мере одну **ось**. Более подробное описание использования объектов **осей** показано на объекте [Axis](axis-object-ado-md.md) .


> [!NOTE]
> Ось фильтра для набора **ячеек** не находится в коллекции **осей** . Дополнительные сведения см. в свойстве [FilterAxis](filteraxis-property-ado-md.md) .



**Оси** — это стандартная коллекция ADO. С помощью свойств и методов коллекции можно выполнить следующие действия:

- Получите число объектов в коллекции со свойством [Count](count-property-ado.md) .

- Возвращает объект из коллекции со свойством [Item](item-property-ado.md) по умолчанию.

- Обновление объектов в коллекции от поставщика с помощью метода [Refresh](refresh-method-ado.md) .

