---
title: WillChangeRecordset и RecordsetChangeComplete события (ADO)
TOCTitle: WillChangeRecordset and RecordsetChangeComplete Events (ADO)
ms:assetid: 2cec4cf9-a4e9-c386-5202-04e86f4cf8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249068(v=office.15)
ms:contentKeyID: 48543963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0a7bf9a69fd5a648efc86f698e82ca0ba9413a30
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886314"
---
# <a name="willchangerecordset-and-recordsetchangecomplete-events-ado"></a>WillChangeRecordset и RecordsetChangeComplete события (ADO)


**Применимо к**: Access 2013, Office 2013


Событие **WillChangeRecordset** вызывается перед операцию ожидающие изменения [набора записей](recordset-object-ado.md). Событие **RecordsetChangeComplete** вызывается после изменения **набора записей** .

## <a name="syntax"></a>Синтаксис

WillChangeRecordset*adReason*, *adStatus* *pRecordset*

RecordsetChangeComplete*adReason*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Параметры

  - *adReason*

  - Значение [EventReasonEnum](eventreasonenum.md) , указывает причину это событие. Его значение может быть **adRsnRequery**, **adRsnResynch**, **adRsnClose**, **adRsnOpen**.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    При вызове **WillChangeRecordset** этот параметр имеет значение **adStatusOK** , если операция, которая вызвала событие прошла успешно. Если это событие не могут запрашивать отмену ожидающие операции перейдут в **adStatusCantDeny** .
    
    При вызове **RecordsetChangeComplete** этот параметр имеет значение **adStatusOK** , если операция, которая вызвала событие прошла успешно, **adStatusErrorsOccurred** , если операция завершилась неудачно или **adStatusCancel** при операции связанные с ранее обслуживаемых событие **WillChangeRecordset** было отменено.
    
    Прежде чем возвращает **WillChangeRecordset** , присвойте этому параметру значение **adStatusCancel** для запроса отмены ожидающие операции или присвойте этому параметру значение adStatusUnwantedEvent, чтобы запретить последующие уведомления.
    
    Прежде чем **WillChangeRecordset** или возвращает **RecordsetChangeComplete** присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.

  - *pError*

  - Объект [Error](error-object-ado.md) . Описание ошибки, возникшей при имеет значение *adStatus* **adStatusErrorsOccurred**; в противном случае он не задан.

  - *pRecordset*

  - Объект **набора записей** . **Набор записей** , для которого произошло это событие.

## <a name="remarks"></a>Замечания

**WillChangeRecordset** или **RecordsetChangeComplete** события могут быть вызваны методы **записей** [повторный запрос](requery-method-ado.md) или [Открыть](open-method-ado-recordset.md) .

Если поставщик поддерживает закладки, уведомления о событии **RecordsetChange** возникает каждый раз, когда новые строки извлекаются из поставщика. Частота это событие зависит от свойства **RecordsetCacheSize** .

Параметр **adStatus** должен значение **adStatusUnwantedEvent** для каждого **adReason** возможные значения для полностью остановите уведомления о событиях для любого события, которое включает параметр **adReason** .

