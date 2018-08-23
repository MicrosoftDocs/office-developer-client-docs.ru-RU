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
ms.openlocfilehash: 6b57ed45e067ce2debd40e033d386ad2b5ae895a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568520"
---
# <a name="followupstatus"></a>FollowUpStatus

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
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

