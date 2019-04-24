---
title: События begintranscomplete, CommitTransComplete, RollbackTransComplete события (ADO)
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
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a>События события begintranscomplete, CommitTransComplete и RollbackTransComplete (ADO)

**Область применения**: Access 2013, Office 2013

Эти события будут вызваны после завершения выполнения связанной операции над объектом [Connection](connection-object-ado.md) .

- **События begintranscomplete** вызывается после операции [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) .

- **CommitTransComplete** вызывается после операции [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) .

- **RollbackTransComplete** вызывается после операции [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) .

## <a name="syntax"></a>Синтаксис

События begintranscomplete*трансактионлевел*, *перрор*, *адстатус*, *пконнектион*

CommitTransComplete*перрор*, *адстатус*, *пконнектион*

RollbackTransComplete*перрор*, *адстатус*, *пконнектион*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Трансактионлевел* |**Длинное** значение, которое содержит новый уровень транзакций **BeginTrans** , вызвавших это событие.|
|*Перрор* |Объект [Error](error-object-ado.md) . В нем описывается ошибка, которая возникла, если значение Евентстатусенум равно **адстатусеррорсоккурред**; в противном случае он не задается.|
|*Адстатус* |[Евентстатусенум](eventstatusenum.md). Эти события могут препятствовать последующим уведомлениям, присвоив этому параметру значение **адстатусунвантедевент** , прежде чем событие будет возвращено.|
|*Пконнектион* |Объект **Connection** , для которого произошло это событие.|

## <a name="remarks"></a>Замечания

В Visual C++ несколько **подключений** могут совместно использовать один метод обработки события. Метод использует возвращенный объект **Connection** для определения объекта, вызвавшего событие.

Если для [](attributes-property-ado.md) свойства Attributes задано значение **адксакткоммитретаининг** или **адксактабортретаининг**, Новая транзакция начинается после фиксации или отката транзакции. Используйте событие **события begintranscomplete** для пропуска всех событий запуска Transaction, кроме первого.

