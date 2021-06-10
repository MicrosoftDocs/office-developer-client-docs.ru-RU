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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295991"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a>События ConnectComplete и Disconnect (ADO)

**Область применения**: Access 2013, Office 2013

Событие **ConnectComplete** вызвано после начала *подключения.* Событие **Отключение** вызвано после окончания *подключения.*

## <a name="syntax"></a>Синтаксис

ConnectComplete *pError*, *adStatus*, *pConnection*

*Отключение adStatus*, *pConnection*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*pError* |Объект [Ошибки.](error-object-ado.md) Он описывает ошибку, которая произошла, если значение *adStatus* **является adStatusErrorsOccurred;** в противном случае она не установлена.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Когда **вызвана ConnectComplete,** этот параметр задан **adStatusCancel,** если событие **WillConnect** запрашивало отмену ожидаемого подключения.<br/><br/>Перед возвращением любого события установите этот параметр **adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления. Однако закрытие и открытие подключения приводит [к](connection-object-ado.md) повторному повтору этих событий.|
|*pConnection* |Объект **Connection,** для которого применяется это событие.|

