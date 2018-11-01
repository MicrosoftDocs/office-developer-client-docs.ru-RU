---
title: ConnectComplete и отключите события (ADO)
TOCTitle: ConnectComplete and Disconnect Events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f9233ba547ecf746d3b4db7b4e008976a813afff
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891186"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a>ConnectComplete и отключите события (ADO)


**Применимо к**: Access 2013, Office 2013

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

