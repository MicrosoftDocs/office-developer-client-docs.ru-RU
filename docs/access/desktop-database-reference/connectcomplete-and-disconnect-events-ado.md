---
title: События ConnectComplete и Disconnect (ADO)
TOCTitle: ConnectComplete and Disconnect events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e1e1d4487eb113c25e25ce6b9de051e33a4536b3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699389"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a>События ConnectComplete и Disconnect (ADO)

**Применимо к**: Access 2013, Office 2013

Событие **ConnectComplete** вызывается после подключения *запускается*. После подключения *завершается*вызывает события **Disconnect** .

## <a name="syntax"></a>Синтаксис

ConnectComplete*pError*, *adStatus* *pConnection*

Отключите*adStatus*, *pConnection*

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*pError* |Объект [Error](error-object-ado.md) . Описание ошибки, возникшей при имеет значение *adStatus* **adStatusErrorsOccurred**; в противном случае он не задан.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). При вызове **ConnectComplete** этот параметр имеет значение **adStatusCancel** , если событие **WillConnect** запросил отмену ожидающие подключения.<br/><br/>Прежде чем возвращает либо события, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления. Тем не менее закрыть и повторно открыть [подключение](connection-object-ado.md) вызывает эти события к еще раз.|
|*pConnection* |Объект **подключения** , для которого применяется данное событие.|

