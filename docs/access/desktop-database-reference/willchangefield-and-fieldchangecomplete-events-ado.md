---
title: WillChangeField and FieldChangeComplete Events (ADO)
TOCTitle: WillChangeField and FieldChangeComplete Events (ADO)
ms:assetid: bc4455a6-2925-33dc-d04f-8ea570e5e370
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249904(v=office.15)
ms:contentKeyID: 48547407
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 40e9572988ca3335ef93ecf46d00a716ba29c595
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481959"
---
# <a name="willchangefield-and-fieldchangecomplete-events-ado"></a>WillChangeField and FieldChangeComplete Events (ADO)


**Применимо к**: Access 2013 | Office 2013

Событие **WillChangeField** вызывается перед ожидающие операции изменяется значение один или несколько объектов [поля](field-object-ado.md) в [набора записей](recordset-object-ado.md). Событие **FieldChangeComplete** вызывается после изменения значения одного или нескольких объектов **поля** .

## <a name="syntax"></a>Синтаксис

WillChangeField*cFields*, *поля* *adStatus*, *pRecordset*

*CFields*, *полей*, FieldChangeComplete *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Параметры

  - *cFields*

  - **Long** , указывающее количество объектов **поля** в *полях*.

  - *Поля*

  - Для **WillChangeField**параметр *поля* представляет собой массив **типа Variant** , которая содержит **поля** объекты на основе исходных значений.  
      
    Для **FieldChangeComplete**параметр *поля* представляет собой массив **типа Variant** , которая содержит объекты **поля** с измененными значениями.

  - *pError*

  - Объект [Error](error-object-ado.md) . Описание ошибки, возникшей при имеет значение *adStatus* **adStatusErrorsOccurred**; в противном случае он не задан.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    При вызове **WillChangeField** этот параметр имеет значение **adStatusOK** , если операция, которая вызвала событие прошла успешно. Если это событие не могут запрашивать отмену ожидающие операции перейдут в **adStatusCantDeny** .
    
    При вызове **FieldChangeComplete** этот параметр имеет значение **adStatusOK** в случае успешного операцию, которая вызвала событие или **adStatusErrorsOccurred** , если операция завершилась неудачно.
    
    Прежде чем возвращает **WillChangeField** , присвойте этому параметру значение **adStatusCancel** , чтобы запросить отмену ожидающие операции.
    
    Прежде чем возвращает **FieldChangeComplete** , присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.

  - *pRecordset*

  - Объект **набора записей** . **Набор записей** , для которого произошло это событие.

## <a name="remarks"></a>Замечания

Событие **WillChangeField** или **FieldChangeComplete** может возникнуть при установке свойства [Value](value-property-ado.md) и вызова метода [обновления](update-method-ado.md) с поля и значения массива параметров.

