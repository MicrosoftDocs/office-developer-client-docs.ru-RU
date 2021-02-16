---
title: FollowUpStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c3d0f6c4-4597-784f-8d44-6e5d905895b4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2280ae9271ca73af33f395bf9e41a9ee8fa62f96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418332"
---
# <a name="followupstatus"></a>FollowUpStatus

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает различные состояния последующих сообщений.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a>Элементы

 _flwupNone_
  
> Не заданы последующие.
    
 _flwupComplete_
  
> Сообщение завершено.
    
 _flwupMarked_
  
> Сообщение помечается для последующего сообщения.
    
 _flwupMAX_
  
> Количество различных статусов, поддерживаемых для последующей работы.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagFlagStatus](pidtagflagstatus-canonical-property.md)

