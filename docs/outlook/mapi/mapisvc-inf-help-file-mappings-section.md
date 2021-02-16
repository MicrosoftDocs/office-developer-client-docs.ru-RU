---
title: MapiSvc.inf [Help File Mappings] Section
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
# <a name="mapisvcinf-help-file-mappings-section"></a>MapiSvc.inf [Help File Mappings] Section

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Раздел **[Сопоставления файлов справки]** содержит записи, которые каждая служба сообщений соемуется с файлом, который предоставляет справку для ошибок, созданных службой. Записи в этом разделе используют следующий формат: 
  
 **[Сопоставления файлов справки] Имя** _файла справки_ для  =   _службы сообщений_
  
Имя службы сообщений — это имя установленной службы сообщений; Имя файла справки — это имя файла, в котором находятся сведения об ошибке. В примере ниже показан типичный **раздел [Сопоставления** файлов справки], содержащий записи для трех служб: MAPI, службы MsgService и службы MS. 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```


