---
title: Событие FetchComplete (ADO)
TOCTitle: FetchComplete event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f4c1cb1379d1faec39fd44fa8273fba4aadca548
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701965"
---
# <a name="fetchcomplete-event-ado"></a>Событие FetchComplete (ADO)

**Применимо к**: Access 2013, Office 2013

Событие **FetchComplete** вызывается после извлечения всех записей в объемных асинхронной операции в [набора записей](recordset-object-ado.md).

## <a name="syntax"></a>Синтаксис

FetchComplete*pError*, *adStatus* *pRecordset*

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*pError* |Объект [Error](error-object-ado.md) . Описание ошибки, возникшей при имеет значение **adStatus** **adStatusErrorsOccurred**; в противном случае он не задан.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Прежде чем возвращает это событие, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.|
|*pRecordset* |Объект **набора записей** . Объект, для которого возвращенных записей.|

## <a name="remarks"></a>Замечания

Чтобы использовать **FetchComplete** с помощью Microsoft Visual Basic, необходим Visual Basic 6.0 или более поздней версии.

