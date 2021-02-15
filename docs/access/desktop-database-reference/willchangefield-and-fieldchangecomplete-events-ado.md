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

Событие **WillChangeField** вызвано перед изменением ожидающих операций значения одного или более объектов [Field](field-object-ado.md) в [наборе записей.](recordset-object-ado.md) Событие **FieldChangeComplete** вызвано после изменения значения одного или более объектов **Field.**

## <a name="syntax"></a>Синтаксис

WillChangeField *cFields,* *Fields,* *adStatus*, *pRecordset*

FieldChangeComplete *cFields,* *Fields,* *pError,* *adStatus*, *pRecordset*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*cFields* |**Длинное,** которое указывает количество объектов **Field** в *полях.*|
|*Fields* |Для **WillChangeField** параметр *Fields* — это массив **variant,** содержащий **объекты Field** с исходными значениями. <br/><br/>Для **FieldChangeComplete** параметр *Fields* — это массив **вариантов,** содержащий **объекты Field** с измененными значениями.|
|*pError* |Объект [Error.](error-object-ado.md) В ней описывается ошибка, которая произошла, если *значением adStatus* является **adStatusErrorsOccurred;** в противном случае он не установлен.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). При **вызывается WillChangeField,** этот параметр задан как **adStatusOK,** если операция, которая вызвала событие, была успешной. Если это событие не может запросить отмену ожидающей операции, ему задается **adStatusCantDeny.** <br/><br/>При вызывается **FieldChangeComplete,** этот параметр задан как **adStatusOK,** если операция, которая привела к событию, была успешной, или **adStatusErrorsOccurred,** если операция не удалась. <br/><br/>Перед **возвратом WillChangeField** установите для этого параметра **параметр adStatusCancel** запрос на отмену ожидающих операций. <br/><br/>Перед **возвратом FieldChangeComplete** установите для этого параметра **параметр adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления.|
|*pRecordset* |Объект **Recordset.** Набор **записей,** для которого произошло это событие.|

## <a name="remarks"></a>Заметки

Событие **WillChangeField** или **FieldChangeComplete** может возникать при установке свойства [Value](value-property-ado.md) и вызове метода [Update](update-method-ado.md) с параметрами массива полей и значений.

