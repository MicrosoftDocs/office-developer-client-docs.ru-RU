---
title: Состояние бездействия
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
# <a name="idle-state"></a>Состояние бездействия

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
 В этом разделе описывается, что происходит во время простоя конечного автомата репликации. 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Идентификатор состояния:  <br/> |**LR_SYNC_IDLE** <br/> |
|Связанная структура данных:  <br/> | *Нет*  <br/> |
|Из этого состояния:  <br/> | *Неприменимо*  <br/> |
|В этом состоянии:  <br/> |[Состояние синхронизации](synchronize-state.md) <br/> |
   
> [!NOTE]
> Этот автомат репликации является детерминируемым. Клиент, выступая из одного состояния в другое, должен в конечном итоге вернуться к одному из последних. 
  
## <a name="description"></a>Описание

В этом состоянии ничего не происходит. Локальное хранилище находится в этом состоянии до инициации репликации и после завершения репликации.
  
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)
  
[��������� MAPI](mapi-constants.md)
  
[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

