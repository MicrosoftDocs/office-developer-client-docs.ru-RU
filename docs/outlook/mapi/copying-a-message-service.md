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
ms.openlocfilehash: 7d1296ba74bbafcd26a8878dfb1eb2f359ab3e03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808185"
---
# <a name="copying-a-message-service"></a>Копирование службы сообщений

  
  
**Относится к**: Outlook 
  
 **Чтобы скопировать службы сообщений в профиль**
  
- Вызов [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).
    
При копировании службы сообщений нового экземпляра службы настроена в точно так же, что и исходный. В некоторых случаях **CopyMsgService** возвращает ошибку MAPI_E_ACCESS_DENIED. Самой распространенной причиной этой ошибки прибыли — это служба сообщение, которое не позволяет так, чтобы быть дублируются. 
  

