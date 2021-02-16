---
title: MapiSvc.inf [Default Services] Section
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
# <a name="mapisvcinf-default-services-section"></a>MapiSvc.inf [Default Services] Section

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
В **разделе [Службы по умолчанию]** перечислены все службы сообщений, выбранные в качестве служб сообщений по умолчанию. Эти службы сообщений по умолчанию являются подмножество служб сообщений, перечисленных в разделе **[Службы].** Когда программа настройки профилей создает профиль по умолчанию, службы сообщений в этом разделе включаются автоматически. 
  
Эти записи используют тот же формат, что и записи в разделе **[Службы],** как показано ниже: 
  
 **[Службы по умолчанию]**
  
 _имя раздела службы сообщений_  =   _имя службы сообщений_
  
Следующие записи будут включены в раздел **[Службы** по умолчанию] для mapisvc.inf, показанного на предыдущей иллюстрации: 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


