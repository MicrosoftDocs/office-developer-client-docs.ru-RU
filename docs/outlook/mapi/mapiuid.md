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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Независимая от по порядку версия [структуры GUID,](guid.md) используемая для уникальной идентификации поставщика услуг. 
  
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
  
> Массив, содержащий 16-byte identifier.
    
## <a name="remarks"></a>Примечания

Структура **MAPIUID** — это **структура GUID,** помещаемая в ® процессора Intel. 
  
MAPI создает структуры **MAPIUID** таким образом, что для двух разных элементов очень редко требуется один и тот же идентификатор. **Структуры MAPIUID** могут храниться в двоичных свойствах или в качестве файлов без упорядочения в зависимости от порядка вбайтов компьютера, на который хранится информация, или доступа к ним. 
  
 **Используются структуры MAPIUID:** 
  
- Определение раздела профиля.
    
- В идентификаторах записей объектов хранения сообщений и адресной книги для идентификации ответственного поставщика услуг.
    
- В **свойстве PR_SEARCH_KEY** [(PidTagSearchKey)](pidtagsearchkey-canonical-property.md)сообщений.
    
Чтобы создать **идентификатор MAPIUID** для ключа поиска, поставщики услуг вызывают [IMAPISupport::NewUID.](imapisupport-newuid.md)
  
Когда клиент передает сообщение по сети, он должен использовать протокол или формат передачи, который не меняет порядок передачи данных **MAPIUID.** 
  
Дополнительные сведения об используемых **структурах MAPIUID** см. в следующих темах: 
  
[Регистрация уникальных идентификаторов поставщика услуг](registering-service-provider-unique-identifiers.md)
  
[Настройка порядка транспорта](setting-transport-order.md)
  
## <a name="see-also"></a>См. также



[GUID](guid.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::NewUID](imapisupport-newuid.md)


[Структуры MAPI](mapi-structures.md)

