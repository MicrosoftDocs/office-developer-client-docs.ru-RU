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
ms.openlocfilehash: 5d860135d846df8ef1ea0784d7430c71ad0fe64e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809903"
---
# <a name="mapisvcinf-default-services-section"></a>MapiSvc.inf: раздел [Службы по умолчанию]

  
  
**Относится к**: Outlook 
  
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


