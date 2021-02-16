---
title: MAPINAMEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPINAMEID
api_type:
- COM
ms.assetid: 9a92e9cd-8282-4cf0-93af-4089b3763594
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: baec750a460b3ba9becd2e1dddf967705424ac4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411682"
---
# <a name="mapinameid"></a>MAPINAMEID

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Описывает именуемую собственность. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _MAPINAMEID
{
  LPGUID lpguid;
  ULONG ulKind;
  union
  {
    LONG lID;
    LPWSTR lpwstrName;
  } Kind;
} MAPINAMEID, FAR *LPMAPINAMEID;

```

## <a name="members"></a>"Участники"

 **lpguid**
  
> Указатель на структуру [GUID,](guid.md) определяющей определенный набор свойств; этот член не может иметь NULL. Допустимы следующие значения: 
    
PS_PUBLIC_STRINGS
  
> 
    
PS_MAPI
  
> 
    
Определяемая клиентом величина
  
> 
    
 **ulKind**
  
> Значение, описывающие тип значения в члене **Kind.** Допустимы следующие значения: 
    
MNID_ID 
  
> Член **Kind** содержит многое значение, которое представляет имя свойства. 
    
MNID_STRING 
  
> Член **Kind** содержит строку символов Юникода, представляющую имя свойства. 
    
 **Kind**
  
> Объединение, описывающие имя именоваемого свойства. Это может быть либо одно или несколько значений, хранимые в **коде lID,** либо строка юникода, сохраненная в **lpwstrName.**
    
## <a name="remarks"></a>Примечания

Структура **MAPINAMEID** используется для описания именуемой свойства свойств с идентификаторами 0x8000. Набор свойств является важной частью именоваемом свойства. Например, PS_PUBLIC_STRINGS или PS_ROUTING_ADDRTYPE это наборы свойств, определенные в MAPI. 
  
Именуемые свойства позволяют клиентам определять настраиваемые свойства в большем пространстве имен, чем доступно в диапазоне идентификаторов свойств, определенных в MAPI. Имена свойств нельзя использовать для непосредственного получения значений свойств; Сначала их необходимо сопооставить с идентификаторами свойств с помощью метода [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) Для определенных объектов, таких как сообщения, MAPI резервировать диапазон идентификаторов свойств для настраиваемого свойства. Поэтому для этих объектов клиенты не должны использовать именуемые свойства и могут сохранять связанные накладные расходы. 
  
Дополнительные сведения об именуемом свойстве см. [в под названием "Свойства имен".](mapi-named-properties.md)
  
## <a name="see-also"></a>См. также



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)


[Структуры MAPI](mapi-structures.md)

