---
title: Уведомления о формах MAPI
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
# <a name="mapi-forms-notifications"></a>Уведомления о формах MAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Регистрация и обработка уведомлений из объектов форм — это другой процесс, чем для других объектов MAPI. Советую раковинам для уведомлений форм реализовать **интерфейс IMAPIViewAdviseSink** или **интерфейс IMAPIFormAdviseSink,** а не **интерфейс IMAPIAdviseSink**. [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) и [IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) каждый из них имеет несколько методов, по одному для каждого из возможных событий, которые соответствующий источник консультации способен генерировать. Например, **IMAPIFormAdviseSink** имеет два метода: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) для обработки изменения состояния просмотра формы и [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md) для отображения нового сообщения с правильной формой. 
  
Стратегия обработки событий для форм аналогична стратегии обработки событий, реализованной в OLE. Клиенты не регистрируются для определенных типов событий, как для большинства объектов MAPI. Предположение состоит в том, что регистрация для уведомления позволяет им получать любое событие, которое может быть сгенерировано конкретным источником консультаций. Так как **IMAPIAdviseSink::OnNotify** необходимо написать, чтобы обрабатывать все зарегистрированные события, его реализация может быть сложной для клиентов, которые регистрируются для многих различных событий. Так как методы в форме советуют объектам раковины нацелить одно событие, реализация этих методов проще. 
  

