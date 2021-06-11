---
title: Обеспечение уведомления Thread-Safe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 88c58d14893f2ac561dc56441eb38b7f4bd0db32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424849"
---
# <a name="ensuring-a-thread-safe-notification"></a>Обеспечение уведомления Thread-Safe

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Если клиент работает на многоуровневой платформе, может потребоваться гарантия того, что вызовы в [методы IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) происходят в определенном потоке. Поскольку **вызовы OnNotify** обычно могут возникать в любом потоке, можно получать уведомления о неожиданных и нежелательных потоках, что приводит к ошибкам, которые сложно отлагировать. 
  
Чтобы гарантировать, что вызовы **в OnNotify** для определенного уведомления  будут сделаны на том же потоке, который использовался для вызова "Советы", перед вызовом сообщите [hrThisThreadAdviseSink](hrthisthreadadvisesink.md) **.** ** **HrThisThisThreadAdviseSink**** создает новый объект раковины рекомендации из объекта раковины рекомендации. Передай этот новый объект в вызове **Посоветуйте.** Все клиенты, которые могут не работать вне контекста определенного потока, должны всегда регистрировать объекты раковины, созданные **с помощью HrThisThreadAdviseSink.**
  

