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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302487"
---
# <a name="willchangefield-and-fieldchangecomplete-events-ado"></a>События WillChangeField и FieldChangeComplete (ADO)

**Область применения**: Access 2013, Office 2013

Событие **WillChangeField** вызвано до того, как ожидаемая операция изменяет значение одного или более объектов [Field](field-object-ado.md) в [Наборе записей.](recordset-object-ado.md) Событие **FieldChangeComplete** вызвано после изменения значения одного или более объектов **Field.**

## <a name="syntax"></a>Синтаксис

CFields *WillChangeField*, *Fields*, *adStatus*, *pRecordset*

FieldChangeComplete *cFields*, *Fields*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*cFields* |**Long,** который указывает количество объектов **Field** в *Полях.*|
|*Fields* |Для **WillChangeField** параметр *Fields* — это массив **Вариантов,** содержащий **объекты Field** с исходными значениями. <br/><br/>Для **FieldChangeComplete** параметр *Fields* — это массив **Вариантов,** содержащий **объекты Field** с измененными значениями.|
|*pError* |Объект [Ошибки.](error-object-ado.md) Он описывает ошибку, которая произошла, если значение *adStatus* **является adStatusErrorsOccurred;** в противном случае она не установлена.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Когда **вызывается WillChangeField,** этот параметр задан **adStatusOK,** если операция, вызвавла событие, была успешной. Оно устанавливается **для adStatusCantDeny,** если это событие не может запросить отмену ожидающей операции. <br/><br/>Когда **вызван FieldChangeComplete,** этот параметр задан **adStatusOK,** если операция, вызвавла событие, была успешной, или **adStatusErrorsOccurred,** если операция не удалась. <br/><br/>Перед **возвращением WillChangeField** установите этот параметр **adStatusCancel** для запроса отмены ожидаемой операции. <br/><br/>Перед **возвращением FieldChangeComplete** установите этот параметр **adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления.|
|*pRecordset* |Объект **Recordset.** **Набор записей,** для которого произошло это событие.|

## <a name="remarks"></a>Примечания

Событие **WillChangeField или** **FieldChangeComplete** может возникать при настройке свойства [Value](value-property-ado.md) и вызове метода [Update](update-method-ado.md) с параметрами массива полей и значений.

