---
title: Состояние бездействия
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7b74ecb44d9a38fc73ceed4077d6f7a939f92f5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591802"
---
# <a name="idle-state"></a>Состояние бездействия

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
 В этом разделе описывается, что происходит во время простоя состояние конечного автомата репликации. 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Идентификатор состояний:  <br/> |**LR_SYNC_IDLE** <br/> |
|Структура связанных данных:  <br/> | *None*  <br/> |
|Из этого состояния:  <br/> | *Неприменимо*  <br/> |
|Это состояние:  <br/> |[Синхронизировать состояние](synchronize-state.md) <br/> |
   
> [!NOTE]
> Конечный автомат репликации является детерминированным конечного автомата. Клиент отправления одного состояния в другое должны в конечном счете возврата на первый из последний. 
  
## <a name="description"></a>Описание

Ничего не происходит в этом состоянии. Локальное хранилище находится в этом состоянии до инициализации репликации и после завершения репликации.
  
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)
  
[��������� MAPI](mapi-constants.md)
  
[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[СОСТОЯНИЕ](syncstate.md)

