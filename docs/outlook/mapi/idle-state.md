---
title: Состояние простоя
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3db4ead7e2485bbbae82f2a07659c934b394d6d5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419480"
---
# <a name="idle-state"></a>Состояние простоя

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
 В этом разделе описывается, что происходит во время простоя конечного автомата репликации. 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Идентификатор состояния:  <br/> |**LR_SYNC_IDLE** <br/> |
|Связанная структура данных:  <br/> | *Нет*  <br/> |
|Из этого состояния:  <br/> | *Неприменимо*  <br/> |
|В это состояние:  <br/> |[Состояние синхронизации](synchronize-state.md) <br/> |
   
> [!NOTE]
> Конечный автомат репликации — это детерминированный конечный автомат. Клиент, который отменяет от одного состояния к другому, должен, в конечном итоге, вернуться к предыдущему из последнего. 
  
## <a name="description"></a>Описание

В этом состоянии ничего не происходит. Локальное хранилище находится в этом состоянии до начала репликации и после завершения репликации.
  
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)
  
[��������� MAPI](mapi-constants.md)
  
[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

