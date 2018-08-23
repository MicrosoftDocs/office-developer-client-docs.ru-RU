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
ms.openlocfilehash: 91c69489e1a72c5cd702a3c4d0392220a89c38fd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580385"
---
# <a name="mapisvcinf-help-file-mappings-section"></a>MapiSvc.inf: раздел [Справка по сопоставлению файлов]

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
В разделе **[Help File Mappings]** содержит записи, что каждый сопоставление одной службы сообщений к файлу, который содержит справки для ошибки, возникающие в службе. Записи в этом разделе используйте следующий формат: 
  
 **[Справка сопоставлению файлов]** _имя службы сообщений_  =   _Имя файла справки_
  
Имя службы сообщений — это имя службы, установленные сообщения; Имя файла справки — это имя файла, в котором хранятся сведения об ошибке. В следующем примере показано типичное раздел **[Help File Mappings]** содержит записи для трех служб: MAPI, MsgService службы и службы мс. 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```


