---
title: MapiSvc. INF [службы по умолчанию] раздел
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
# <a name="mapisvcinf-default-services-section"></a>MapiSvc. INF [службы по умолчанию] раздел

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
В разделе **[службы по умолчанию]** перечислены все службы сообщений, выбранные в качестве служб сообщений по умолчанию. Эти службы сообщений по умолчанию являются подмножеством служб сообщений, перечисленных в разделе **[службы]** . Когда программа настройки профилей создает профиль по умолчанию, службы сообщений в этом разделе автоматически включаются. 
  
Записи используют тот же формат, что и записи в разделе **[Services]** , как показано ниже: 
  
 **[Службы по умолчанию]**
  
 _имя раздела "_ =  служба сообщений" имя_службы сообщений_
  
Следующие записи будут включены в раздел **[службы по умолчанию]** для файла Mapisvc. INF, показанного на предыдущем рисунке: 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


