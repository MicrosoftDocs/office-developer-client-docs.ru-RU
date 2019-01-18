---
title: События WillChangeField и FieldChangeComplete (ADO)
TOCTitle: WillChangeField and FieldChangeComplete events (ADO)
ms:assetid: bc4455a6-2925-33dc-d04f-8ea570e5e370
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249904(v=office.15)
ms:contentKeyID: 48547407
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0fd952cc09f410752f3eb7b5963059f8d6ee7c2c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700187"
---
# <a name="willchangefield-and-fieldchangecomplete-events-ado"></a>События WillChangeField и FieldChangeComplete (ADO)

**Применимо к**: Access 2013, Office 2013

Событие **WillChangeField** вызывается перед ожидающие операции изменяется значение один или несколько объектов [поля](field-object-ado.md) в [набора записей](recordset-object-ado.md). Событие **FieldChangeComplete** вызывается после изменения значения одного или нескольких объектов **поля** .

## <a name="syntax"></a>Синтаксис

WillChangeField*cFields*, *поля* *adStatus*, *pRecordset*

*CFields*, *полей*, FieldChangeComplete *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*cFields* |**Long** , указывающее количество объектов **поля** в *полях*.|
|*Fields* |Для **WillChangeField**параметр *поля* представляет собой массив **типа Variant** , которая содержит **поля** объекты на основе исходных значений. <br/><br/>Для **FieldChangeComplete**параметр *поля* представляет собой массив **типа Variant** , которая содержит объекты **поля** с измененными значениями.|
|*pError* |Объект [Error](error-object-ado.md) . Описание ошибки, возникшей при имеет значение *adStatus* **adStatusErrorsOccurred**; в противном случае он не задан.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). При вызове **WillChangeField** этот параметр имеет значение **adStatusOK** , если операция, которая вызвала событие прошла успешно. Если это событие не могут запрашивать отмену ожидающие операции перейдут в **adStatusCantDeny** . <br/><br/>При вызове **FieldChangeComplete** этот параметр имеет значение **adStatusOK** в случае успешного операцию, которая вызвала событие или **adStatusErrorsOccurred** , если операция завершилась неудачно. <br/><br/>Прежде чем возвращает **WillChangeField** , присвойте этому параметру значение **adStatusCancel** , чтобы запросить отмену ожидающие операции. <br/><br/>Прежде чем возвращает **FieldChangeComplete** , присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.|
|*pRecordset* |Объект **набора записей** . **Набор записей** , для которого произошло это событие.|

## <a name="remarks"></a>Замечания

Событие **WillChangeField** или **FieldChangeComplete** может возникнуть при установке свойства [Value](value-property-ado.md) и вызова метода [обновления](update-method-ado.md) с поля и значения массива параметров.

