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

Событие **WillChangeRecordset** вызвано до того, как ожидаемая операция изменяет [набор recordset.](recordset-object-ado.md) Событие **RecordsetChangeComplete** вызвано после изменения **recordset.**

## <a name="syntax"></a>Синтаксис

WillChangeRecordset *adReason*, *adStatus*, *pRecordset*

RecordsetChangeComplete *adReason,* *pError,* *adStatus*, *pRecordset*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*adReason* |Значение [EventReasonEnum,](eventreasonenum.md) которое указывает причину этого события. Его значение может быть **adRsnRequery,** **adRsnResynch,** **adRsnClose**, **adRsnOpen**.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). При **вызывается WillChangeRecordset,** этот параметр задан как **adStatusOK,** если операция, которая вызвала событие, была успешной. Если это событие не может запросить отмену ожидающей операции, ему задается **adStatusCantDeny.** <br/><br/>При вызывается **RecordsetChangeComplete,** этот параметр задан как **adStatusOK,** если операция, которая вызвала событие, была успешной, **adStatusErrorsOccurred,** если операция не удалась, или **adStatusCancel,** если операция, связанная с ранее принятым событием **WillChangeRecordset,** была отменена. <br/><br/>Перед возвратом **WillChangeRecordset** установите для этого параметра параметр **adStatusCancel** запрос отмены ожидающих операций или установите для этого параметра параметр adStatusUnwantedEvent, чтобы предотвратить последующие уведомления. <br/><br/>Перед **возвратом WillChangeRecordset** или **RecordsetChangeComplete** установите для этого параметра параметр **adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления.|
|*pError* |Объект [Error.](error-object-ado.md) В ней описывается ошибка, которая произошла, если *значением adStatus* является **adStatusErrorsOccurred;** в противном случае он не установлен.|
|*pRecordset* |Объект **Recordset.** Набор **записей,** для которого произошло это событие.|

## <a name="remarks"></a>Заметки

Событие **WillChangeRecordset** или **RecordsetChangeComplete** может возникать из-за методов **Recordset** [Requery](requery-method-ado.md) или [Open.](open-method-ado-recordset.md)

Если поставщик не поддерживает закладки, уведомление о событии **RecordsetChange** возникает при каждом извлечении новых строк от поставщика. Частота этого события зависит от свойства **RecordsetCacheSize.**

Необходимо установить для параметра **adStatus** значение **adStatusUnwantedEvent** для каждого возможного значения **adReason,** чтобы полностью остановить уведомление о событии, которое включает параметр **adReason.**

