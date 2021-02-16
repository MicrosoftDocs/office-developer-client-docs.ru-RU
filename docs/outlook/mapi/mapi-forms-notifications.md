---
title: MAPI Forms Notifications
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97ff2733-a2b1-4da0-b628-00850fc7925b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e9c10f78af6dff2e0d0c59d0bfe59be07dccd4b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418612"
---
# <a name="mapi-forms-notifications"></a>MAPI Forms Notifications

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Процесс регистрации и обработки уведомлений от объектов форм отличается от процесса для других объектов MAPI. В обоймах для уведомлений форм реализован интерфейс **IMAPIViewAdviseSink** или **IMAPIFormAdviseSink,** а не **IMAPIAdviseSink.** [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) и [IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) каждое имеет несколько методов, по одному для каждого из возможных событий, которые может создавать соответствующий источник консультаций. Например, **IMAPIFormAdviseSink** имеет два метода: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) для обработки изменения состояния средства просмотра формы и [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md) для отображения нового сообщения с правильной формой. 
  
Стратегия обработки событий для форм аналогична стратегии обработки событий, реализованной в OLE. Клиенты не регистрируются для определенных типов событий, как для большинства объектов MAPI. Предположим, что регистрация уведомления позволяет им получать события любого типа, которые могут быть созданы конкретным источником консультаций. Так **как IMAPIAdviseSink::OnNotify** должен быть написан таким образом, чтобы обрабатывать все зарегистрированные события, его реализация может быть сложной для клиентов, которые регистрируют множество различных событий. Так как методы в форме рекомендуемые объекты приемника нацелены на одно событие, реализовать эти методы проще. 
  

