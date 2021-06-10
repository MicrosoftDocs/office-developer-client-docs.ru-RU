---
title: Событие WillConnect (ADO)
TOCTitle: WillConnect event (ADO)
ms:assetid: 8b0e9955-4e7a-7af8-ce6c-7a4ba569a5bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249611(v=office.15)
ms:contentKeyID: 48546208
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6e62a01d274752b33f7bf3f6f4af6171e7efb16b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305889"
---
# <a name="willconnect-event-ado"></a>Событие WillConnect (ADO)

**Область применения**: Access 2013, Office 2013

Событие **WillConnect** вызвано перед началом подключения.

## <a name="syntax"></a>Синтаксис

WillConnect *ConnectionString*, *UserID*, *Пароль*, *Параметры*, *adStatus*, *pConnection*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*ConnectionString* |**Строка,** содержаная сведения о подключении для ожидающих подключения.|
|*UserID* |**Строка,** которая содержит имя пользователя для ожидающих подключения.|
|*Password* |**Строка,** которая содержит пароль для ожидающих подключения.|
|*Options* |**Длинное** значение, которое указывает, как поставщик должен оценивать *ConnectionString.* Единственным вариантом **является adAsyncOpen**.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Когда это событие называется, этот параметр по умолчанию задан **adStatusOK.** Он задается **adStatusCantDeny,** если событие не может запросить отмену ожидающей операции.<br/><br/>Перед возвращением этого события установите этот параметр **adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления. Установите этот параметр **в adStatusCancel** для запроса операции подключения, которая вызвала отмену этого уведомления.|
|*pConnection* |Объект [Connection,](connection-object-ado.md) для которого применяется это уведомление о событии. Изменения параметров подключения  обработиктором **событий WillConnect** не влияют на **подключение.**|

## <a name="remarks"></a>Примечания

Когда **вызывается WillConnect,** параметры *ConnectionString,* *UserID,* *Password* и *Options* заданы значениям, установленным операцией, которая вызвала это событие (ожидающий подключения), и могут быть изменены до возвращения события. **WillConnect** может вернуть запрос об отмене ожидаемой подключения.

Когда это событие отменяется, **connectComplete** будет вызван с его *параметром adStatus,* заданным **adStatusErrorsOccurred**.

