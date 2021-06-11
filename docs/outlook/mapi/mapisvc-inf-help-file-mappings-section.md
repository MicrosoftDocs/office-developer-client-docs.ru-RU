---
title: Раздел MapiSvc.inf [Сопоставления файлов справки]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62aee641-b73f-4f53-9e8d-adf010c9ea1a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4760c9965975bb5d950e51b707d28bee647ef99a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407559"
---
# <a name="mapisvcinf-help-file-mappings-section"></a>Раздел MapiSvc.inf [Сопоставления файлов справки]

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
В **разделе [Сопоставления файлов справки]** содержатся записи, в которых каждая служба сообщений сопоставлена с файлом, который предоставляет справку по ошибкам, созданным службой. Записи в этом разделе используют следующий формат: 
  
 **[Справка сопоставления файлов]** _имя службы сообщений_  =   _Справка имя файла_
  
Имя службы сообщений — это имя установленной службы сообщений; Имя файла справки — это имя файла, в котором находится информация об ошибке. В следующем примере показан типичный **раздел [Сопоставления** файлов справки], содержащий записи для трех служб: MAPI, службы MsgService и службы MS. 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```


