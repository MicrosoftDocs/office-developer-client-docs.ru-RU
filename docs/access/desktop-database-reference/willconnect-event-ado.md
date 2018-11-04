---
title: Событие WillConnect (ADO)
TOCTitle: WillConnect event (ADO)
ms:assetid: 8b0e9955-4e7a-7af8-ce6c-7a4ba569a5bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249611(v=office.15)
ms:contentKeyID: 48546208
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c8ac4ab83062d9297483b7ee4883ab0b289af227
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949833"
---
# <a name="willconnect-event-ado"></a>Событие WillConnect (ADO)

**Применимо к**: Access 2013, Office 2013

Событие **WillConnect** вызывается до начала подключения.

## <a name="syntax"></a>Синтаксис

WillConnect*ConnectionString*, *идентификатор пользователя*, *пароль*, *Параметры*, *adStatus*, *pConnection*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*ConnectionString* |**Строка** , которая содержит сведения о подключении для ожидания подключения.|
|*Идентификатор пользователя* |**Строка** , содержащая имя пользователя для подключения к ожидающие.|
|*Password* |**Строка** , содержащая пароль для ожидающие подключения.|
|*Варианты* |**Длинное** значение, которое указывает, как поставщик необходимо решить, *ConnectionString*. Единственным вариантом является **adAsyncOpen**.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Когда это событие вызывается, этот параметр имеет значение **adStatusOK** по умолчанию. Если событие не могут запрашивать отмену ожидающие операции перейдут в **adStatusCantDeny** .<br/><br/>Прежде чем возвращает это событие, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления. Присвойте этому параметру значение **adStatusCancel** для запроса операции подключения, в которой обнаружен отмены это уведомление.|
|*pConnection* |Объект [подключения](connection-object-ado.md) , для которого применяется этого уведомления о событиях. Изменения параметров **подключения** обработчика событий **WillConnect** не повлияет на **подключение**.|

## <a name="remarks"></a>Примечания

При вызове **WillConnect** *ConnectionString*, *идентификатор пользователя*, *пароль*и *Параметры* — значение значения, заданные в операцию, которая вызвала это событие (ожидающие подключения) и может быть изменено Прежде чем возвращает события. **WillConnect** может возвратить запрос на отменить ожидающие подключения.

Когда это событие отменяется, **ConnectComplete** вызывается с его *adStatus* параметру присвоено значение **adStatusErrorsOccurred**.

