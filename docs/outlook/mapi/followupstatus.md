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
ms.openlocfilehash: e59c0ba7810741943883b9e86e84c6fe141f3050
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808461"
---
# <a name="followupstatus"></a>FollowUpStatus

  
  
**Относится к**: Outlook 
  
Указывает различные состояния обработки результатов для сообщения.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a>Members

 _flwupNone_
  
> Нет исполнения не указана.
    
 _flwupComplete_
  
> Сообщение будет завершена.
    
 _flwupMarked_
  
> Сообщение помечено для исполнения.
    
 _flwupMAX_
  
> Количество различных статусов, поддерживаемые для исполнения.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagFlagStatus](pidtagflagstatus-canonical-property.md)

