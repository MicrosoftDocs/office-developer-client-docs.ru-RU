---
title: Свойство FilterAxis (ADO MD)
TOCTitle: FilterAxis property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3b1f9c2bcc4ed4f3314a697d4a0eae8415bc4f62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292456"
---
# <a name="filteraxis-property-ado-md"></a>Свойство FilterAxis (ADO MD)


**Область применения**: Access 2013, Office 2013

Показывает данные фильтра о текущем наборе ячеек.

## <a name="return-values"></a>Возвращаемые значения

Возвращает объект [Axis](axis-object-ado-md.md) и доступен только для чтения.

## <a name="remarks"></a>Примечания

Используйте свойство **FilterAxis** , чтобы получить сведения об измерениях, использованных для среза данных. Свойство [DimensionCount](dimensioncount-property-ado-md.md) **оси** возвращает число измерений среза. Эта ось обычно содержит только одну строку.

**Ось** , возвращаемая методом [FilterAxis](filteraxis-property-ado-md.md) , не входит в коллекцию [осей](axes-collection-ado-md.md) для объекта набора [ячеек](cellset-object-ado-md.md) .

