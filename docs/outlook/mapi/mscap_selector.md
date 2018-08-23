---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8c23788d64fe3703c7c46998cade0bd40d2f3dd2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588127"
---
# <a name="mscapselector"></a>MSCAP_SELECTOR

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Задает возможности, чтобы возвратить хранилища.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
typedef enum 
{ 
    MSCAP_SEL_RESERVED1 = 0, 
    MSCAP_SEL_RESERVED2, 
    MSCAP_SEL_FOLDER, 
    MSCAP_SEL_RESERVED3, 
    MSCAP_SEL_RESTRICTION, 
} MSCAP_SELECTOR;
```

## <a name="members"></a>Members

 *MSCAP_SEL_RESERVED1* 
  
> Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
 *MSCAP_SEL_RESERVED2* 
  
> Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
 *MSCAP_SEL_FOLDER* 
  
> Возможности о вспомогательных папок для хранилища.
    
 *MSCAP_SEL_RESERVED3* 
  
> Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
 *MSCAP_SEL_RESTRICTION* 
  
> Возможности о поддержке ограничения для хранилища.
    

