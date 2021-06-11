---
title: MAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIUID
api_type:
- COM
ms.assetid: 63eac3ee-e59b-4a06-8bb9-f72764d84bda
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: da314205f7d2dd746b72aa7e2b5ff2a13bb0c21b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432207"
---
# <a name="mapiuid"></a>MAPIUID

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Независимая версия структуры [GUID,](guid.md) используемая для уникальной идентификации поставщика услуг. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанный макрос:  <br/> |[IsEqualMAPIUID](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a>"Участники"

 **ab**
  
> Массив, содержащий идентификатор 16-byte.
    
## <a name="remarks"></a>Примечания

Структура **MAPIUID** — это **структура GUID,** помещаемая в порядок ® процессора Intel. 
  
MAPI создает **структуры MAPIUID** таким образом, что для двух различных элементов очень редко бывает иметь один и тот же идентификатор. **Структуры MAPIUID** могут храниться в качестве двоичных свойств или файлов без упорядочения byte для хранения компьютера или доступа к информации. 
  
 **Используются структуры MAPIUID:** 
  
- Определение раздела профилей.
    
- В идентификаторах записи объектов хранения сообщений и адресной книги для идентификации ответственного поставщика услуг.
    
- В **PR_SEARCH_KEY** [(PidTagSearchKey)](pidtagsearchkey-canonical-property.md)свойство сообщений.
    
Чтобы создать **идентификатор MAPIUID** для ключа поиска, поставщики служб вызывают [IMAPISupport::NewUID](imapisupport-newuid.md).
  
Когда клиент передает сообщение по сети, он должен использовать протокол или формат передачи, которые не изменяют порядок byte данных **MAPIUID.** 
  
Дополнительные сведения об используемых **структурах MAPIUID** см. в следующих темах: 
  
[Регистрация уникальных идентификаторов поставщика услуг](registering-service-provider-unique-identifiers.md)
  
[Настройка порядка транспортировки](setting-transport-order.md)
  
## <a name="see-also"></a>См. также



[GUID](guid.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::NewUID](imapisupport-newuid.md)


[Структуры MAPI](mapi-structures.md)

