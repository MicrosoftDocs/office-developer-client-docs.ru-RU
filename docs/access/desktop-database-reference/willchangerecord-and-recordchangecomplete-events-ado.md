---
title: События WillChangeRecord и RecordChangeComplete (ADO)
TOCTitle: WillChangeRecord and RecordChangeComplete events (ADO)
ms:assetid: b21229b2-74e6-0798-95bf-0252f041831c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249851(v=office.15)
ms:contentKeyID: 48547162
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0113a7b22d0bba8e843ce9583e93eef848f872a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305987"
---
# <a name="willchangerecord-and-recordchangecomplete-events-ado"></a>События WillChangeRecord и RecordChangeComplete (ADO)

**Область применения**: Access 2013, Office 2013

Событие **WillChangeRecord** вызвано перед изменением одной или более записей (строк) [в наборе записей.](recordset-object-ado.md) Событие **RecordChangeComplete** вызвано после изменения одной или более записей.

## <a name="syntax"></a>Синтаксис

WillChangeRecord *adReason,* *cRecords,* *adStatus*, *pRecordset*

RecordChangeComplete *adReason,* *cRecords,* *pError,* *adStatus*, *pRecordset*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*adReason* |Значение [EventReasonEnum,](eventreasonenum.md) которое указывает причину этого события. Его значение может быть **adRsnAddNew,** **adRsnDelete,** **adRsnUpdate,** **adRsnUndoUpdate,** **adRsnUndoAddNew,** **adRsnUndoDelete** или **adRsnFirstChange**.|
|*cRecords* |**Длинное** значение, которое указывает количество изменяющихся (затронутых) записей.|
|*pError* |Объект [Error.](error-object-ado.md) В ней описывается ошибка, которая произошла, если *значением adStatus* является **adStatusErrorsOccurred;** в противном случае он не установлен.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). При **вызывается WillChangeRecord,** этот параметр задан как **adStatusOK,** если операция, которая вызвала событие, была успешной. Если это событие не может запросить отмену ожидающей операции, ему задается **adStatusCantDeny.** <br/><br/>При вызывается **RecordChangeComplete,** этот параметр задан как **adStatusOK,** если операция, которая вызвала событие, была успешной, или **adStatusErrorsOccurred,** если операция не удалась. <br/><br/>Перед возвратом **WillChangeRecord** установите для этого параметра параметр **adStatusCancel** запрос отмены операции, которая вызвала это событие, или установите для этого параметра параметр adStatusUnwantedEvent, чтобы предотвратить последующие нотации. <br/><br/>Перед **возвратом RecordChangeComplete** установите для этого параметра **параметр adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления.|
|*pRecordset* |Объект **Recordset.** Набор **записей,** для которого произошло это событие.|

## <a name="remarks"></a>Заметки

Событие **WillChangeRecord** или **RecordChangeComplete** может возникать для первого измененного поля в строке из-за следующих операций **Recordset:** [Update,](update-method-ado.md) [Delete,](delete-method-ado-recordset.md) [CancelUpdate,](cancelupdate-method-ado.md) [AddNew,](addnew-method-ado.md) [UpdateBatch](updatebatch-method-ado.md)и [CancelBatch.](cancelbatch-method-ado.md) Значение **recordset** [CursorType](cursortype-property-ado.md) определяет, какие операции приводят к событиям.

Во время **события WillChangeRecord** свойству **Recordset** [Filter](filter-property-ado.md) задается свойство **adFilterAffectedRecords.** Это свойство нельзя изменить при обработке события.

Необходимо установить для параметра adStatus значение adStatusUnwantedEvent для каждого возможного значения adReason, чтобы полностью остановить событие для любого события, которое включает параметр adReason.

