---
title: WillChangeRecord и RecordChangeComplete события (ADO)
TOCTitle: WillChangeRecord and RecordChangeComplete Events (ADO)
ms:assetid: b21229b2-74e6-0798-95bf-0252f041831c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249851(v=office.15)
ms:contentKeyID: 48547162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 895a80cf4810088b5f18f4a9416e7eadc54a004f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878131"
---
# <a name="willchangerecord-and-recordchangecomplete-events-ado"></a>WillChangeRecord и RecordChangeComplete события (ADO)


**Применимо к**: Access 2013, Office 2013


Событие **WillChangeRecord** вызывается перед измените один или несколько записей (строк) в [набора записей](recordset-object-ado.md) . Событие **RecordChangeComplete** вызывается после изменения одной или нескольких записей.

## <a name="syntax"></a>Синтаксис

WillChangeRecord*adReason*, *cRecords*, *adStatus*, *pRecordset*

RecordChangeComplete*adReason*, *cRecords*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Параметры

  - *adReason*

  - Значение [EventReasonEnum](eventreasonenum.md) , указывает причину это событие. Его значение может быть **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete**или **adRsnFirstChange**.

  - *cRecords*

  - Значение типа **Long** , показывает, сколько изменение записей (влияет на).

  - *pError*

  - Объект [Error](error-object-ado.md) . Описание ошибки, возникшей при имеет значение *adStatus* **adStatusErrorsOccurred**; в противном случае он не задан.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    При вызове **WillChangeRecord** этот параметр имеет значение **adStatusOK** , если операция, которая вызвала событие прошла успешно. Если это событие не могут запрашивать отмену ожидающие операции перейдут в **adStatusCantDeny** .
    
    При вызове **RecordChangeComplete** этот параметр имеет значение **adStatusOK** в случае успешного операцию, которая вызвала событие или **adStatusErrorsOccurred** , если операция завершилась неудачно.
    
    Прежде чем возвращает **WillChangeRecord** , присвойте этому параметру значение **adStatusCancel** для отмены запроса, которое вызвало это событие или присвойте этому параметру значение adStatusUnwantedEvent, чтобы запретить последующие notications операции.
    
    Прежде чем возвращает **RecordChangeComplete** , присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.

  - *pRecordset*

  - Объект **набора записей** . **Набор записей** , для которого произошло это событие.

## <a name="remarks"></a>Замечания

**WillChangeRecord** или **RecordChangeComplete** событие может произойти для первого измененные поля в строке из-за следующие операции **записей** : [обновление](update-method-ado.md), [Удаление](delete-method-ado-recordset.md), [CancelUpdate](cancelupdate-method-ado.md), [AddNew](addnew-method-ado.md), [ UpdateBatch](updatebatch-method-ado.md)и [CancelBatch](cancelbatch-method-ado.md). Значение **набора записей** [CursorType](cursortype-property-ado.md) определяет, какие операции приводят к возникновении событий.

Во время события **WillChangeRecord** **записей** [фильтра](filter-property-ado.md) задано значение **adFilterAffectedRecords**. Это свойство не может изменить при обработке события.

Параметр adStatus должен значение adStatusUnwantedEvent для каждого adReason возможные значения для полностью остановите noticiation событий для всех событий, который включает параметр adReason.

