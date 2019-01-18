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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713270"
---
# <a name="filteraxis-property-ado-md"></a>Свойство FilterAxis (ADO MD)


**Применимо к**: Access 2013, Office 2013

Указывает фильтр сведений о текущем ячеек.

## <a name="return-values"></a>Возвращаемые значения

Возвращает объект [ось](axis-object-ado-md.md) и доступен только для чтения.

## <a name="remarks"></a>Замечания

Свойство **FilterAxis** используется для возвращения сведений о измерений, которые использовались для среза данных. Свойство [DimensionCount](dimensioncount-property-ado-md.md) **ось** возвращает число измерений, срез. В этом ось обычно имеет только одну строку.

**Ось** , возвращаемые [FilterAxis](filteraxis-property-ado-md.md) не содержащихся в коллекции [осей](axes-collection-ado-md.md) для объекта [ячеек](cellset-object-ado-md.md) .

