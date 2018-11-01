---
title: Свойство Status (записей ADO)
TOCTitle: Status Property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c053ec9f84de4aa56513081144e23f044c72effc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876633"
---
# <a name="status-property-ado-recordset"></a>Свойство Status (записей ADO)


**Применимо к**: Access 2013, Office 2013

Указывает состояние текущей записи в отношении пакета обновлений или других массовых операций.

## <a name="return-value"></a>Возвращаемое значение

Возвращает сумму значений [RecordStatusEnum](recordstatusenum.md) один или несколько.

## <a name="remarks"></a>Замечания

Используйте свойство **состояние** для просмотра изменений, ожидающих установки для записей, измененные во время обновления пакета. Также можно использовать свойство **состояние** для просмотра состояния с ошибкой во время массовых операций, таких как при вызове метода [выполнить повторную синхронизацию](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md)или [CancelBatch](cancelbatch-method-ado.md) методы для объекта [набора записей](recordset-object-ado.md) и задать [фильтра записи ](filter-property-ado.md)свойство объекта **набора записей** в массив закладки. Это свойство можно определить, как данной записи не удалось и соответствующим образом ее решения.

