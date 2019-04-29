---
title: IsEqualMAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IsEqualMAPIUID
api_type:
- COM
ms.assetid: 85d71b73-0630-4c5d-b0e3-b48d27a300d0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 44e3613338c8932bc80dd1150392033dfa3cd050
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426935"
---
# <a name="isequalmapiuid"></a>IsEqualMAPIUID

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Тестирует две структуры [мапиуид](mapiuid.md) , чтобы определить, содержат ли они один и тот же идентификатор. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанная структура:  <br/> |**MAPIUID** <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a>Параметры

 _lpuid1_
  
> Указатель на первую структуру **мапиуид** , которую необходимо протестировать. 
    
 _lpuid2_
  
> Указатель на вторую структуру **мапиуид** , которую необходимо протестировать. 
    
## <a name="remarks"></a>Примечания

Макрос **исекуалмапиуид** ВОЗВРАЩАЕТ значение true, если две структуры **мапиуид** содержат один и тот же идентификатор, и значение false в противном случае. 
  
Для макроса **исекуалмапиуид** необходимо включить файл заголовков Memory. h. 
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)


[Макросы, связанные со структурами](macros-related-to-structures.md)

