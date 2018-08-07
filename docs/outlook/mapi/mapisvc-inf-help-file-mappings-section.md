---
title: 'MapiSvc.inf: раздел [Справка по сопоставлению файлов]'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62aee641-b73f-4f53-9e8d-adf010c9ea1a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 776f797d0c96d9173e114fd499d6cca0494a0a43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809911"
---
# <a name="mapisvcinf-help-file-mappings-section"></a>MapiSvc.inf: раздел [Справка по сопоставлению файлов]

  
  
**Относится к**: Outlook 
  
В разделе **[Help File Mappings]** содержит записи, что каждый сопоставление одной службы сообщений к файлу, который содержит справки для ошибки, возникающие в службе. Записи в этом разделе используйте следующий формат: 
  
 **[Справка сопоставлению файлов]** _имя службы сообщений_  =   _Имя файла справки_
  
Имя службы сообщений — это имя службы, установленные сообщения; Имя файла справки — это имя файла, в котором хранятся сведения об ошибке. В следующем примере показано типичное раздел **[Help File Mappings]** содержит записи для трех служб: MAPI, MsgService службы и службы мс. 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```


