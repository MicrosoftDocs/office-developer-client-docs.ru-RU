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
ms.openlocfilehash: 3675c6a8ee2ee208f175dd5f7d219447aa52e9ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809917"
---
# <a name="mapiuid"></a>MAPIUID

  
  
**Относится к**: Outlook 
  
Порядок байтов независимой версия структуру [идентификатор GUID](guid.md) , который используется для уникальной идентификации поставщика услуг. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макрос:  <br/> |[IsEqualMAPIUID](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a>Members

 **AB**
  
> Массив, содержащий 16-разрядный идентификатор.
    
## <a name="remarks"></a>Замечания

Структура **MAPIUID** — это **идентификатор GUID** структура, поместить в байтовом формате Intel® процессора. 
  
MAPI создает **MAPIUID** структуры, чтобы он очень редко для двух различных элементов требуются тот же идентификатор. **MAPIUID** структуры могут храниться как свойства двоичных файлов или файлов, независимо от порядка байтов компьютера, хранения и доступа к сведениям. 
  
 **MAPIUID** структуры используются: 
  
- Для идентификации профиля.
    
- В операции идентификаторы сообщения хранения и адресной книги объекты для идентификации поставщика услуг ответственность.
    
- В свойстве **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) сообщений.
    
Для создания идентификатор **MAPIUID** для поиска ключ, поставщиков услуг вызвать [IMAPISupport::NewUID](imapisupport-newuid.md).
  
Если клиент передает сообщения по сети, следует использовать протокол или передачи формат, не изменяйте байтовом **MAPIUID** данных. 
  
Дополнительные сведения об использовании структур **MAPIUID** в следующих разделах: 
  
[Регистрация уникальных идентификаторов поставщиков служб](registering-service-provider-unique-identifiers.md)
  
[Установка порядка транспорта](setting-transport-order.md)
  
## <a name="see-also"></a>См. также



[GUID](guid.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::NewUID](imapisupport-newuid.md)


[Структуры MAPI](mapi-structures.md)

