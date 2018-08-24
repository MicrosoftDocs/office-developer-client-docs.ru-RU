---
title: Копирование службы сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8388d14446a230b032e49ad0d614c85e79b8ece8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573721"
---
# <a name="copying-a-message-service"></a>Копирование службы сообщений

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
 **Чтобы скопировать службы сообщений в профиль**
  
- Вызов [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).
    
При копировании службы сообщений нового экземпляра службы настроена в точно так же, что и исходный. В некоторых случаях **CopyMsgService** возвращает ошибку MAPI_E_ACCESS_DENIED. Самой распространенной причиной этой ошибки прибыли — это служба сообщение, которое не позволяет так, чтобы быть дублируются. 
  

