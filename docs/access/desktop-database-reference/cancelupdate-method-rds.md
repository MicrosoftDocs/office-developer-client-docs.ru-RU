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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296670"
---
# <a name="cancelupdate-method-rds"></a>Метод CancelUpdate (RDS)

**Область применения**: Access 2013, Office 2013

Отменяет изменения, внесенные в текущую или новую строку объекта [Recordset.](recordset-object-ado.md)

## <a name="syntax"></a>Синтаксис

*DataControl*. CancelUpdate

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Переменная объекта, представляюая [RDS. Объект DataControl.](datacontrol-object-rds.md)|

## <a name="remarks"></a>Примечания

Служба cursor для OLE DB хранит копию исходных значений и кэш изменений. При вызове **CancelUpdate** кэш изменений сбрасывается до пустого, а все связанные элементы управления обновляются с помощью исходных данных.

