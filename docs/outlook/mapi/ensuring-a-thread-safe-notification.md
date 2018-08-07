---
title: Обеспечение потокобезопасности уведомлений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 70e594057f2d654e0527b0caa0951e44842df809
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808381"
---
# <a name="ensuring-a-thread-safe-notification"></a>Обеспечение потокобезопасности уведомлений

  
  
**Относится к**: Outlook 
  
Если клиент работает на многопоточные платформы, может потребоваться возникновения вызовы методов [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) в определенном потоке Software assurance. Так как вызовы **OnNotify** обычно могут выполняться в любом потоке, можно получать уведомления на непредвиденные и нежелательного потоки, приводят к ошибкам, которые трудно отладки. 
  
Чтобы гарантировать, что вызовы **OnNotify** для конкретного уведомления выполняются в том же потоке, который использовался для **уведомлений** звонков, вызвать [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) перед вызовом **уведомлений**. ** ** HrThisThreadAdviseSink *** создает новый объект приемника уведомлений из объекта приемник уведомлений. Передайте этот новый объект в вызове **уведомлений**. Все клиенты с приемник уведомлений, объекты, которые могут работать вне контекста определенного потока всегда следует регистрировать уведомить приемника объектов, созданных с помощью **HrThisThreadAdviseSink**.
  

