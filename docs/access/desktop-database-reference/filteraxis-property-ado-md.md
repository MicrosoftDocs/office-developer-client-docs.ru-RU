---
title: Свойство FilterAxis (ADO MD)
TOCTitle: FilterAxis Property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f298acf3a9250a0376ba31f5d3afc6b079ce0c78
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867708"
---
# <a name="filteraxis-property-ado-md"></a>Свойство FilterAxis (ADO MD)


**Применимо к**: Access 2013, Office 2013

Указывает фильтр сведений о текущем ячеек.

## <a name="return-values"></a>Возвращаемые значения

Возвращает объект [ось](axis-object-ado-md.md) и доступен только для чтения.

## <a name="remarks"></a>Замечания

Свойство **FilterAxis** используется для возвращения сведений о измерений, которые использовались для среза данных. Свойство [DimensionCount](dimensioncount-property-ado-md.md) **ось** возвращает число измерений, срез. В этом ось обычно имеет только одну строку.

**Ось** , возвращаемые [FilterAxis](filteraxis-property-ado-md.md) не содержащихся в коллекции [осей](axes-collection-ado-md.md) для объекта [ячеек](cellset-object-ado-md.md) .

