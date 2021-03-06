---
title: Состояния форм
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dfc9fbf1-90d4-4756-92d9-032ac56a9c50
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 61d20ff7010151a82c53cafc69270e6925796a5c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429168"
---
# <a name="form-states"></a>Состояния форм

**Область применения**: Outlook 2013 | Outlook 2016 
  
Объекты формы могут быть в одном из пяти различных состояниях в зависимости от того, какие методы были вызваны в них и произошли ли ошибки при выполнении этих методов. Состояния описаны в следующих темах:
  
- [Единое состояние](uninitialized-state.md)
    
- [Нормальное состояние](normal-state.md)
    
- [Состояние NoScribble](noscribble-state.md)
    
- [Состояние HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal State](handsofffromnormal-state.md)
    
Состояния в основном связаны со статусом данных в объекте формы. Различные состояния отражают, нужно ли сохранять данные, должен ли объект формы вносить изменения в данные и какой момент в процессе сохранения данных находится форма. Таким образом, состояния форм и переходы между ними имеют большее отношения к реализации [IPersistMessage сервера форм: методы интерфейса IUnknown](ipersistmessageiunknown.md) больше, чем любые другие. Знание этих состояниях очень полезно для правильной реализации интерфейсов форм MAPI, которые должен реализовать ваш сервер форм. 
  
Темы в этом разделе описывают различные состояния, а также разрешенные действия, которые вызывают переходы в другие состояния. Любые переходы, не указанные в темах, не допускаются. Если объекты формы делают неостановимые переходы между состояниями, они не будут вести себя так, как ожидают клиенты обмена сообщениями, и это может привести к непредсказуемому поведению клиента или объекта формы.
  
> [!NOTE]
> Некоторые переходы состояния зависят от сведений из предыдущих состояниях. Скорее всего, серверу форм придется реализовать флаг в его объектах формы, чтобы указать, были ли изменены значения свойств сообщения для облегчения более поздних изменений состояния. 
  
## <a name="see-also"></a>См. также

- [Разработка серверов форм MAPI](developing-mapi-form-servers.md)

