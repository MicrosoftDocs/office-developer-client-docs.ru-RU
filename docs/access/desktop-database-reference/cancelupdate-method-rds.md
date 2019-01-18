---
title: Метод CancelUpdate (RDS)
TOCTitle: CancelUpdate method (RDS)
ms:assetid: 373a3feb-125d-915a-fd56-d4b04b20db54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249130(v=office.15)
ms:contentKeyID: 48544188
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b0c02a9ca72add763e1d3ccf62d5ede8adaecc6b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718618"
---
# <a name="cancelupdate-method-rds"></a>Метод CancelUpdate (RDS)

**Применимо к**: Access 2013, Office 2013

Отменяет все изменения, внесенные в строку текущей или новый объект [набора записей](recordset-object-ado.md) .

## <a name="syntax"></a>Синтаксис

*DataControl*. CancelUpdate

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.|

## <a name="remarks"></a>Замечания

Служба курсора для OLE DB сохраняет как копию исходных значений, так и в кэш изменений. При вызове **CancelUpdate**выполнен сброс кэша изменения пустая строка, и все привязки элементов управления обновляется с исходными данными.

