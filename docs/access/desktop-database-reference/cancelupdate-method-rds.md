---
title: Метод CancelUpdate (RDS)
TOCTitle: CancelUpdate Method (RDS)
ms:assetid: 373a3feb-125d-915a-fd56-d4b04b20db54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249130(v=office.15)
ms:contentKeyID: 48544188
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28216cbeb98a0ebc7dfbc6115ea8bc05fadc057f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887749"
---
# <a name="cancelupdate-method-rds"></a>Метод CancelUpdate (RDS)


**Применимо к**: Access 2013, Office 2013



Отменяет все изменения, внесенные в строку текущей или новый объект [набора записей](recordset-object-ado.md) .

## <a name="syntax"></a>Синтаксис

*DataControl*. CancelUpdate

## <a name="parameters"></a>Параметры

  - *DataControl*

  - Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.

## <a name="remarks"></a>Замечания

Служба курсора для OLE DB сохраняет как копию исходных значений, так и в кэш изменений. При вызове **CancelUpdate**выполнен сброс кэша изменения пустая строка, и все привязки элементов управления обновляется с исходными данными.

