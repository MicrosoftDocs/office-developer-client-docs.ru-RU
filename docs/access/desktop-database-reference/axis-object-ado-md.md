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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296901"
---
# <a name="axis-object-ado-md"></a>Объект Axis (ADO MD)


**Область применения**: Access 2013, Office 2013

Представляет положение или ось фильтра для набора ячеек, содержащего выбранные элементы одного или нескольких измерений.

## <a name="remarks"></a>Примечания

Объект **Axis** может содержаться в коллекции [осей](axes-collection-ado-md.md) или возвращен свойством [FilterAxis](filteraxis-property-ado-md.md) набора [ячеек](cellset-object-ado-md.md).

С помощью коллекций и свойств объекта **Axis** можно выполнить следующие действия:

- Определите **ось** со свойством [Name](name-property-ado-md.md) .

- Выполните итерацию по каждой позиции вдоль **оси** с помощью коллекции [Positions](positions-collection-ado-md.md) .

- Получите количество измерений на **оси** со свойством [DimensionCount](dimensioncount-property-ado-md.md) .

- Получите атрибуты **оси** , зависящие от поставщика, с помощью стандартной коллекции [свойств](properties-collection-ado.md) ADO.

