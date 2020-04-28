---
title: Свойство Status (Recordset в ADO)
TOCTitle: Status property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4017ff216c17479a69d6d07d0abe51b30fd5e680
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308521"
---
# <a name="status-property-ado-recordset"></a>Свойство Status (Recordset в ADO)


**Область применения**: Access 2013, Office 2013

Указывает состояние текущей записи по отношению к пакетным обновлениям или другим массовым операциям.

## <a name="return-value"></a>Возвращаемое значение

Возвращает сумму одного или нескольких значений [RecordStatusEnum](recordstatusenum.md) .

## <a name="remarks"></a>Примечания

Используйте свойство **Status** , чтобы узнать, какие изменения ожидаются для записей, измененных во время пакетного обновления. Кроме того, можно использовать свойство **Status** для просмотра состояния записей, которые не удалось выполнить во время массовых операций, например, при вызове методов [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md)или [CancelBatch](cancelbatch-method-ado.md) для объекта [Recordset](recordset-object-ado.md) , или задать для свойства [Filter](filter-property-ado.md) объекта **Recordset** массив закладок. С помощью этого свойства можно определить, как ошибка заданной записи, и устранить ее соответствующим образом.

