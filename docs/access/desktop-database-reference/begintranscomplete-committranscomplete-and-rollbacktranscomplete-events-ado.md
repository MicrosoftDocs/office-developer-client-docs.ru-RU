---
title: События BeginTransComplete, CommitTransComplete, RollbackTransComplete (ADO)
TOCTitle: BeginTransComplete, CommitTransComplete, and RollbackTransComplete Events (ADO)
ms:assetid: 9d0ae38e-530a-7a89-a344-f3ab401c2e35
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249713(v=office.15)
ms:contentKeyID: 48546615
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bf38a106a8cb53c1603628f0c3c0096be4b73d52
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888638"
---
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a>BeginTransComplete, CommitTransComplete и RollbackTransComplete события (ADO)


**Применимо к**: Access 2013, Office 2013


Эти события будет вызван после завершения выполнения операцию связанный объект [подключения](connection-object-ado.md) .

  - После выполнения операции [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) называется **BeginTransComplete** .

  - После выполнения операции [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) называется **CommitTransComplete** .

  - **RollbackTransComplete** вызывается после операции [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) .

## <a name="syntax"></a>Синтаксис

BeginTransComplete*TransactionLevel*, *pError*, *adStatus*, *pConnection*

CommitTransComplete*pError*, *adStatus* *pConnection*

RollbackTransComplete*pError*, *adStatus* *pConnection*

## <a name="parameters"></a>Параметры

  - *TransactionLevel*

  - Значение типа **Long** , содержит новый уровень транзакций **BeginTrans** , вызвавшего это событие.

  - *pError*

  - Объект [Error](error-object-ado.md) . Описание ошибки, возникшей при имеет значение EventStatusEnum **adStatusErrorsOccurred**; в противном случае он не задан.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Эти события могут запретить последующие уведомления по этому параметру **adStatusUnwantedEvent** перед Возвращает событие.

  - *pConnection*

  - Объект **подключения** , для которого произошло это событие.

## <a name="remarks"></a>Замечания

В Visual C++ несколько **подключения** могут совместно использовать же метод обработки событий. Метод использует возвращенный объект **подключения** для определения, какой объект вызвала событие.

Если свойство [Attributes](attributes-property-ado.md) **adXactCommitRetaining** или **adXactAbortRetaining**, новые транзакции начинается после фиксации или откате транзакции. Используйте событие **BeginTransComplete** игнорировать все, но первое событие начала операции.

