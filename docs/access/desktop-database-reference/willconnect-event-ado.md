---
title: WillConnect event (ADO)
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
# <a name="willconnect-event-ado"></a>WillConnect event (ADO)

**Область применения**: Access 2013, Office 2013

Событие **WillConnect** вызвано перед началом подключения.

## <a name="syntax"></a>Синтаксис

WillConnect *ConnectionString*, *UserID*, *Password*, *Options*, *adStatus*, *pConnection*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*ConnectionString* |**Строка,** содержаная сведения о под соединении для ожидающих подключений.|
|*UserID* |**Строка,** содержаная имя пользователя для ожидающих подключений.|
|*Password* |**Строка,** содержаная пароль для ожидающих подключений.|
|*Options* |**Длинное** значение, которое указывает, как поставщик должен оценить *ConnectionString.* Единственным вариантом **является adAsyncOpen.**|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). При этом событии этот параметр по умолчанию имеет значение **adStatusOK.** Если событие не может запросить отмену ожидающей операции, ему задается **adStatusCantDeny.**<br/><br/>Перед возвращением этого события установите для этого параметра **параметр adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления. Установите для этого параметра **параметр adStatusCancel,** чтобы запросить операцию подключения, которая вызвала отмену этого уведомления.|
|*pConnection* |Объект [Connection,](connection-object-ado.md) к которому применяется это уведомление о событии. Изменения параметров подключения  с помощью обработера **событий WillConnect** не влияют на **подключение.**|

## <a name="remarks"></a>Заметки

Когда **вызывается WillConnect,** параметры *ConnectionString,* *UserID,* *Password* и *Options* устанавливаются в значения, установленные операцией, которая вызвала это событие (ожидающие подключения), и могут быть изменены до возврата события. **WillConnect** может возвращать запрос на отмену ожидающих подключений.

При отмене этого события будет вызван **ConnectComplete** с параметром *adStatus,* заданным **как adStatusErrorsOccurred.**

