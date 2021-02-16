---
title: FPropExists
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropExists
api_type:
- COM
ms.assetid: 33c00752-cdc1-4cbe-8fca-6b06c78bd362
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7190065c687524302bae362a2e25d3848e17d1bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429490"
---
# <a name="fpropexists"></a>FPropExists

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Выполняет поиск заданного тега свойства в интерфейсе [IMAPIProp](imapipropiunknown.md) или интерфейсе, производного от **IMAPIProp,** например [IMessage](imessageimapiprop.md) или [IMAPIFolder.](imapifolderimapicontainer.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Параметры

 _pobj_
  
> [in] Указатель на интерфейс **IMAPIProp** или интерфейс, производный от **IMAPIProp,** в котором необходимо искать тег свойства. 
    
 _ulPropTag_
  
> [in] Тег свойства, по которому необходимо искать.
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Обнаружено совпадение для заданного тега свойства. 
    
FALSE 
  
> Совпадение для заданного тега свойства не найдено.
    
## <a name="remarks"></a>Примечания

Если тег свойства в параметре  _ulPropTag_ имеет тип PT_UNSPECIFIED, функция **FPropExists** ищет совпадение только на основе идентификатора свойства. В противном случае совпадение со всем тегом свойства, включая тип. 
  

