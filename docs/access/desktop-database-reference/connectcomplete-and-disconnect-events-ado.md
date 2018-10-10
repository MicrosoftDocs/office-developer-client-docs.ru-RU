---
title: ConnectComplete and Disconnect Events (ADO)
TOCTitle: ConnectComplete and Disconnect Events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 731879abf181f64c24b1012e45ea23435f965574
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482419"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a>ConnectComplete and Disconnect Events (ADO)


**Применимо к**: Access 2013 | Office 2013

Событие **ConnectComplete** вызывается после подключения *запускается*. После подключения *завершается*вызывает события **Disconnect** .

## <a name="syntax"></a>Синтаксис

ConnectComplete*pError*, *adStatus* *pConnection*

Отключите*adStatus*, *pConnection*

## <a name="parameters"></a>Параметры

  - *pError*

  - Объект [Error](error-object-ado.md) . Описание ошибки, возникшей при имеет значение *adStatus* **adStatusErrorsOccurred**; в противном случае он не задан.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    При вызове **ConnectComplete** этот параметр имеет значение **adStatusCancel** , если событие **WillConnect** запросил отмену ожидающие подключения.
    
    Прежде чем возвращает либо события, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления. Тем не менее закрыть и повторно открыть [подключение](connection-object-ado.md) вызывает эти события к еще раз.

  - *pConnection*

  - Объект **подключения** , для которого применяется данное событие.

