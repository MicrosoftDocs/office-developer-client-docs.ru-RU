---
title: Раздел MapiSvc.inf [Службы по умолчанию]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a7906a9a5e953332dba5c4776c63bb433a937a5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435322"
---
# <a name="mapisvcinf-default-services-section"></a>Раздел MapiSvc.inf [Службы по умолчанию]

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
В **разделе [Службы по умолчанию]** перечислены все службы сообщений, выбранные как службы сообщений по умолчанию. Эти службы сообщений по умолчанию являются подмножество служб сообщений, перечисленных в **разделе [Services].** Когда программа конфигурации профиля создает профиль по умолчанию, службы сообщений в этом разделе включаются автоматически. 
  
Записи используют тот же формат, что и записи в **разделе [Services],** как показано ниже: 
  
 **[Службы по умолчанию]**
  
 _Имя раздела "служба сообщений"_  =   _Имя службы сообщений_
  
Следующие записи будут включены в раздел **[Службы** по умолчанию] для mapisvc.inf, показанный на более ранней иллюстрации: 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


