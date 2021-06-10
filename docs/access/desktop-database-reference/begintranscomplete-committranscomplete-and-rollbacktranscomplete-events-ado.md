---
title: События BeginTransComplete, CommitTransComplete, RollbackTransComplete (ADO)
TOCTitle: BeginTransComplete, CommitTransComplete, and RollbackTransComplete events (ADO)
ms:assetid: 9d0ae38e-530a-7a89-a344-f3ab401c2e35
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249713(v=office.15)
ms:contentKeyID: 48546615
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6f86e17a44ec0813176a023a02710fded627488
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296824"
---
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a>События BeginTransComplete, CommitTransComplete и RollbackTransComplete (ADO)

**Область применения**: Access 2013, Office 2013

Эти события будут вызваны после выполнения связанной операции на [объекте Connection.](connection-object-ado.md)

- **BeginTransComplete** вызван после операции [BeginTrans.](begintrans-committrans-and-rollbacktrans-methods-ado.md)

- **CommitTransComplete** вызван после операции [CommitTrans.](begintrans-committrans-and-rollbacktrans-methods-ado.md)

- **RollbackTransComplete** вызван после операции [RollbackTrans.](begintrans-committrans-and-rollbacktrans-methods-ado.md)

## <a name="syntax"></a>Синтаксис

BeginTransComplete *TransactionLevel*, *pError*, *adStatus*, *pConnection*

CommitTransComplete *pError*, *adStatus*, *pConnection*

RollbackTransComplete *pError*, *adStatus*, *pConnection*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*TransactionLevel* |**Длинное** значение, содержаное новый уровень транзакции **BeginTrans,** вызвав этот случай.|
|*pError* |Объект [Ошибки.](error-object-ado.md) Он описывает ошибку, которая произошла, если значение EventStatusEnum **adStatusErrorsOccurred;** в противном случае это не установлено.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Эти события могут предотвратить последующие уведомления, задав этот параметр **adStatusUnwantedEvent** перед возвращением события.|
|*pConnection* |Объект **Connection,** для которого произошло это событие.|

## <a name="remarks"></a>Примечания

В Visual C++несколько **подключений** могут использовать один и тот же метод обработки событий. Метод использует возвращенный объект **Подключения,** чтобы определить, какой объект вызвал событие.

Если свойство [Attributes](attributes-property-ado.md) настроено на **adXactCommitRetaining** или **adXactAbortRetaining,** после совершения или отката транзакции начинается новая транзакция. Используйте событие **StartTransComplete,** чтобы игнорировать все события, кроме первого запуска транзакции.

