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
ms.openlocfilehash: a4db4ed1c3098226891edca054621fe145daaa1f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425395"
---
# <a name="copying-a-message-service"></a>Копирование службы сообщений

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
 **Копирование службы сообщений в профиль**
  
- Call [имсгсервицеадмин:: копимсгсервице](imsgserviceadmin-copymsgservice.md).
    
При копировании службы сообщений новый экземпляр службы настраивается точно так же, как и в исходном. Иногда **копимсгсервице** возвращает MAPI_E_ACCESS_DENIED об ошибке. Наиболее распространенной причиной этого возврата ошибки является служба сообщений, которая не допускает дублирования. 
  

