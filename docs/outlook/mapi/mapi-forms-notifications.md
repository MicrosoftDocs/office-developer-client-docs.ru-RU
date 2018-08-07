---
title: MAPI Forms уведомлений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97ff2733-a2b1-4da0-b628-00850fc7925b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7064aee2ccd35b6b372bc6f911c7508113c26162
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809757"
---
# <a name="mapi-forms-notifications"></a>MAPI Forms уведомлений

  
  
**Относится к**: Outlook 
  
Для регистрации и обработки уведомлений из объектов формы — это же процессе для других объектов MAPI. Приемников для реализации уведомлений формы либо уведомлений **IMAPIViewAdviseSink** или **IMAPIFormAdviseSink** интерфейс, а не **IMAPIAdviseSink**. [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) и [IMAPIFormAdviseSink: IUnknown](imapiformadvisesinkiunknown.md) иметь несколько методов, другая — для каждого из возможных событий, что соответствующий уведомить источник может создавать. Например, **IMAPIFormAdviseSink** имеет два метода: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) для обработки изменений в состояние просмотра формы и [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md) для отображения нового сообщения с правильной формы. 
  
Стратегия для форм обработки событий аналогичен стратегия, реализованный в OLE обработки событий. Клиенты не регистрируются для определенных типов событий, как для большинства объектов MAPI. Предполагается, что регистрация для получения уведомлений позволяет им принимать любой тип события, вызвавшего источником определенного уведомлений. Так как **IMAPIAdviseSink::OnNotify** должен быть написан таким образом, чтобы обрабатывать все зарегистрированные события, его реализация может быть сложным для клиентов, которые регистрируют для различные события. Одно событие, внедрение этих методов проще, так как методы в виде уведомить целевой объектов приемника. 
  

