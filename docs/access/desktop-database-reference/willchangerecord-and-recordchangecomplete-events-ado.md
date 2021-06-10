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

Событие **WillChangeRecord** вызвано перед одним или более записями (строками) в [изменении Recordset.](recordset-object-ado.md) Событие **RecordChangeComplete** вызвано после изменения одной или более записей.

## <a name="syntax"></a>Синтаксис

WillChangeRecord *adReason*, *cRecords*, *adStatus*, *pRecordset*

RecordChangeComplete *adReason*, *cRecords*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*adReason* |Значение [EventReasonEnum,](eventreasonenum.md) которое указывает причину этого события. Его значение может быть **adRsnAddNew,** **adRsnDelete,** **adRsnUpdate,** **adRsnUndoUpdate,** **adRsnUndoAddNew,** **adRsnUndoDelete** или **adRsnFirstChange**.|
|*cRecords* |**Длинное** значение, которое указывает количество изменяющихся (затронутых) записей.|
|*pError* |Объект [Ошибки.](error-object-ado.md) Он описывает ошибку, которая произошла, если значение *adStatus* **является adStatusErrorsOccurred;** в противном случае она не установлена.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Когда **вызывается WillChangeRecord,** этот параметр задан **adStatusOK,** если операция, вызвавла событие, была успешной. Оно устанавливается **для adStatusCantDeny,** если это событие не может запросить отмену ожидающей операции. <br/><br/>Когда **вызывается RecordChangeComplete,** этот параметр задан **adStatusOK,** если операция, вызвавла событие, была успешной, или **adStatusErrorsOccurred,** если операция не удалась. <br/><br/>Перед возвращением **WillChangeRecord** установите этот параметр **adStatusCancel** для запроса отмены операции, вызвавской это событие, или установите этот параметр adStatusUnwantedEvent для предотвращения последующих заметок. <br/><br/>Перед **возвращением RecordChangeComplete** установите этот параметр **adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления.|
|*pRecordset* |Объект **Recordset.** **Набор записей,** для которого произошло это событие.|

## <a name="remarks"></a>Примечания

Событие **WillChangeRecord** или **RecordChangeComplete** может произойти для первого измененного поля подряд из-за следующих операций **Recordset:** [Update](update-method-ado.md), [Delete](delete-method-ado-recordset.md), [CancelUpdate](cancelupdate-method-ado.md), [AddNew](addnew-method-ado.md), [UpdateBatch](updatebatch-method-ado.md)и [CancelBatch](cancelbatch-method-ado.md). Значение курсора **Recordset** [определяет,](cursortype-property-ado.md) какие операции вызывают события.

Во время **события WillChangeRecord** свойство **фильтра Recordset** [](filter-property-ado.md) задалось **adFilterAffectedRecords.** Это свойство нельзя изменить при обработке события.

Параметр adStatus необходимо задать adStatusUnwantedEvent для каждого возможного значения adReason, чтобы полностью остановить замеление событий для любого события, которое включает параметр adReason.

