---
title: MapiSvc. INF [Справка по соПоставлению файлов]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62aee641-b73f-4f53-9e8d-adf010c9ea1a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4760c9965975bb5d950e51b707d28bee647ef99a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269974"
---
# <a name="mapisvcinf-help-file-mappings-section"></a>MapiSvc. INF [Справка по соПоставлению файлов]

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Раздел **[Help File Mappings]** содержит записи, каждый из которых сопоставляет одну службу сообщений с файлом, который предоставляет справку по ошибкам, создаваемым службой. В записях этого раздела используется следующий формат: 
  
 **[Сопоставления файлов справки]** _имя службы сообщений_  =   _Имя файла справки_
  
Имя службы сообщений — это имя установленной службы сообщений; имя файла справки — это имя файла, в котором находятся сведения об ошибке. Ниже приведен пример типичного раздела **[сопоставления файлов справки]** , который содержит записи для трех служб: MAPI, служба мсгсервице и служба MS. 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```


