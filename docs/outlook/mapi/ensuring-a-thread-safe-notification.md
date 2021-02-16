---
title: Обеспечение Thread-Safe уведомлений
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
# <a name="ensuring-a-thread-safe-notification"></a>Обеспечение Thread-Safe уведомлений

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Если клиент работает на многопотоковой платформе, может потребоваться подтверждение того, что вызовы ваших методов [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) происходят в определенном потоке. Так как вызовы **OnNotify** обычно могут происходить в любом потоке, можно получать уведомления о непредвиденных и нежелательных потоках, что приводит к ошибкам, которые сложно отлалать. 
  
Чтобы гарантировать, что **вызовы OnNotify** для определенного уведомления будут  делаться в том же потоке, который использовался для вызова advise, вызовите [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) перед вызовом **advise**. ** **HrThisThreadAdviseSink**** создает новый объект-замещений из объекта-мятора консультации. Передайте этот новый объект в вызове **"Сообщить".** Все клиенты с рекомендуемые объекты-тонкторы, которые могут не работать вне контекста определенного потока, всегда должны регистрировать объекты-тонкторы, созданные с помощью **HrThisThreadAdviseSink.**
  

