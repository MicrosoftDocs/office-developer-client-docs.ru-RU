---
title: FilterAxis Property (ADO MD)
TOCTitle: FilterAxis Property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 32ddf737ae0d6aa9a7b2daf8adc2a07707c91c0c
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603058"
---
# <a name="filteraxis-property-ado-md"></a>FilterAxis Property (ADO MD)


**Применимо к**: Access 2013 | Office 2013

Указывает фильтр сведений о текущем ячеек.

<<<<<<< HEAD
## <a name="return-values"></a>Return Values
=======
## <a name="return-values"></a>Возвращаемые значения
>>>>>>> master

Возвращает объект [ось](axis-object-ado-md.md) и доступен только для чтения.

## <a name="remarks"></a>Замечания

Свойство **FilterAxis** используется для возвращения сведений о измерений, которые использовались для среза данных. Свойство [DimensionCount](dimensioncount-property-ado-md.md) **ось** возвращает число измерений, срез. В этом ось обычно имеет только одну строку.

**Ось** , возвращаемые [FilterAxis](filteraxis-property-ado-md.md) не содержащихся в коллекции [осей](axes-collection-ado-md.md) для объекта [ячеек](cellset-object-ado-md.md) .

