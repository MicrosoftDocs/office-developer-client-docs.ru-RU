---
title: MapiSvc. INF [Справка по сопоставлению файлов]
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
# <a name="mapisvcinf-help-file-mappings-section"></a>MapiSvc. INF [Справка по сопоставлению файлов]

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Раздел **[Help File Mappings]** содержит записи, каждый из которых сопоставляет одну службу сообщений с файлом, который предоставляет справку по ошибкам, создаваемым службой. В записях этого раздела используется следующий формат: 
  
 **[Справочные сведения о сопоставлении файлов]** имя_файла справки_ для _службы сообщений_ =  
  
Имя службы сообщений — это имя установленной службы сообщений; имя файла справки — это имя файла, в котором находятся сведения об ошибке. Ниже приведен пример типичного раздела **[сопоставления файлов справки]** , который содержит записи для трех служб: MAPI, служба мсгсервице и служба MS. 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```


