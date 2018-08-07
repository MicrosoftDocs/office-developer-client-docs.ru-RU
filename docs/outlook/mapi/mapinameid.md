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
ms.openlocfilehash: c3a21e8a6e69cae9d8b757a60fe56d63e079b3ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809875"
---
# <a name="mapinameid"></a>MAPINAMEID

  
  
**Относится к**: Outlook 
  
Описывает именованное свойство. 
  
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

## <a name="members"></a>Members

 **lpguid**
  
> Установите указатель на структуру [идентификатор GUID](guid.md) , определяющий определенное свойство; Этот член не может быть NULL. Допустимы следующие значения: 
    
PS_PUBLIC_STRINGS
  
> 
    
PS_MAPI
  
> 
    
Определенное значение клиента
  
> 
    
 **ulKind**
  
> Значение, указывающее тип значения в **Тип** элемента. Допустимы следующие значения: 
    
MNID_ID 
  
> Член **типа** содержит целое число, представляющее имя свойства. 
    
MNID_STRING 
  
> Член **типа** содержит строку символ Unicode, представляющую имя свойства. 
    
 **Тип**
  
> Объединение, описывающую имя именованное свойство. Имя может быть целое число, хранящиеся в **крышку**, или строка символов Юникод, хранящиеся в **lpwstrName**.
    
## <a name="remarks"></a>Замечания

Структура **MAPINAMEID** используется для описания свойства именованных свойств, имеющие идентификаторы свыше 0x8000. Набор свойств — важная часть именованное свойство. К примеру PS_PUBLIC_STRINGS или PS_ROUTING_ADDRTYPE, наборы свойств, определенные в MAPI. 
  
Именованные свойства для предоставления клиентам для определения пользовательских свойств в пространстве имен больше, чем доступно в диапазоне идентификатор MAPI определенные свойства. Имена свойств не может использоваться для получения значения свойств напрямую. они сначала должны сопоставляться с идентификаторами свойство через метод [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Для определенных объектов, такие как сообщения MAPI оставляет за собой диапазон идентификаторов свойств для настраиваемого свойства. Таким образом, для этих объектов клиентов нет необходимости использовать именованные свойства и можно сохранить связанные накладные расходы. 
  
Дополнительные сведения об именованных свойств в разделе [Свойства с именем](mapi-named-properties.md).
  
## <a name="see-also"></a>См. также



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)


[Структуры MAPI](mapi-structures.md)

