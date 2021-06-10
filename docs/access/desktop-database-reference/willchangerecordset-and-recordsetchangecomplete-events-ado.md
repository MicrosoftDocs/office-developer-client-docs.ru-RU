---
title: События WillChangeRecordset и RecordsetChangeComplete (ADO)
TOCTitle: WillChangeRecordset and RecordsetChangeComplete events (ADO)
ms:assetid: 2cec4cf9-a4e9-c386-5202-04e86f4cf8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249068(v=office.15)
ms:contentKeyID: 48543963
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bfb304f41ada88e1b0546aaa4a54240b931017cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302823"
---
# <a name="willchangerecordset-and-recordsetchangecomplete-events-ado"></a>События WillChangeRecordset и RecordsetChangeComplete (ADO)

**Область применения**: Access 2013, Office 2013

Событие **WillChangeRecordset** вызвано до того, как ожидаемая операция изменяет [набор Recordset.](recordset-object-ado.md) Событие **RecordsetChangeComplete** вызвано после изменения **recordset.**

## <a name="syntax"></a>Синтаксис

WillChangeRecordset *adReason*, *adStatus*, *pRecordset*

RecordsetChangeComplete *adReason*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*adReason* |Значение [EventReasonEnum,](eventreasonenum.md) которое указывает причину этого события. Его значение может быть **adRsnRequery**, **adRsnResynch**, **adRsnClose**, **adRsnOpen**.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Когда **вызывается WillChangeRecordset,** этот параметр задан **adStatusOK,** если операция, вызвавла событие, была успешной. Оно устанавливается **для adStatusCantDeny,** если это событие не может запросить отмену ожидающей операции. <br/><br/>Когда **вызывается RecordsetChangeComplete,** этот параметр задан **adStatusOK,** если операция, вызвавла событие, была успешной, **adStatusErrorsOccurred,** если операция не удалась, или **adStatusCancel,** если операция, связанная с ранее принятым событием **WillChangeRecordset,** была отменена. <br/><br/>Перед возвращением **WillChangeRecordset** установите этот параметр **adStatusCancel** для запроса отмены ожидаемой операции или установите этот параметр adStatusUnwantedEvent для предотвращения последующих уведомлений. <br/><br/>Перед **возвращением WillChangeRecordset** или **RecordsetChangeComplete** установите этот параметр **adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления.|
|*pError* |Объект [Ошибки.](error-object-ado.md) Он описывает ошибку, которая произошла, если значение *adStatus* **является adStatusErrorsOccurred;** в противном случае она не установлена.|
|*pRecordset* |Объект **Recordset.** **Набор записей,** для которого произошло это событие.|

## <a name="remarks"></a>Примечания

Событие **WillChangeRecordset** или **RecordsetChangeComplete** может происходить из-за методов [Requery](requery-method-ado.md) **recordset** или [Open.](open-method-ado-recordset.md)

Если поставщик не поддерживает закладки, уведомление о событии **RecordsetChange** возникает при каждом извлечении новых строк у поставщика. Частота этого события зависит от свойства **RecordsetCacheSize.**

Параметр **adStatus** необходимо задать **adStatusUnwantedEvent** для каждого возможного значения **adReason,** чтобы полностью остановить уведомление о событии для любого события, которое включает параметр **adReason.**

