---
title: 'MapiSvc.inf: раздел [Службы по умолчанию]'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a7270bce12f6d91dbb5632f739f4644df866924d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573147"
---
# <a name="mapisvcinf-default-services-section"></a>MapiSvc.inf: раздел [Службы по умолчанию]

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
В разделе **[Службы по умолчанию]** перечислены все службы сообщений, выбранные как службы сообщений по умолчанию. Эти службы сообщений по умолчанию являются подмножеством службы сообщений, перечисленных в разделе **[Services]** . Если программа настройки профиля создает профиль по умолчанию, службы сообщений в этом разделе устанавливаются автоматически. 
  
Операции использовать тот же формат как операции в разделе **[Services]** , как показано ниже: 
  
 **[Службы по умолчанию]**
  
 _Имя раздела службы сообщений_ =  _имя службы сообщений_
  
Следующие записи должны быть включены в разделе **[Службы по умолчанию]** для mapisvc.inf, показанные на предыдущем рисунке. 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


