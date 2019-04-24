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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269925"
---
# <a name="mapiuid"></a>MAPIUID

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Независимая от порядка байтов версия структуры [GUID](guid.md) , которая используется для уникальной идентификации поставщика услуг. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанный макрос:  <br/> |[IsEqualMAPIUID](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a>Members

 **поисков**
  
> Массив, содержащий 16 байтового идентификатора.
    
## <a name="remarks"></a>Замечания

Структура **мапиуид** — это структура **GUID** , помещенная в последовательность байтов процессора Intel ®. 
  
MAPI создает структуры **мапиуид** таким образом, что два разных элемента могут иметь один и тот же идентификатор. Структуры **мапиуид** могут храниться в виде двоичных свойств или файлов, вне зависимости от порядка байтов на компьютере, на котором хранится или осуществляется доступ к данным. 
  
 Используются структуры **мапиуид** : 
  
- Для определения раздела профиля.
    
- В идентификаторах записей хранилища сообщений и объектов адресной книги, чтобы определить поставщика ответственного поставщика услуг.
    
- В свойстве **пр_сеарч_кэй** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) messages.
    
Чтобы создать идентификатор **мапиуид** для ключа поиска, поставщики услуг вызывают [Имаписуппорт:: невуид](imapisupport-newuid.md).
  
Когда клиент передает сообщение по сети, он должен использовать протокол или формат передачи, который не изменяет порядок байтов данных **мапиуид** . 
  
Дополнительные сведения о том, как используются структуры **мапиуид** , приведены в следующих разделах: 
  
[Регистрация уникальных идентификаторов поставщиков служб](registering-service-provider-unique-identifiers.md)
  
[Настройка трансПортного заказа](setting-transport-order.md)
  
## <a name="see-also"></a>См. также



[GUID](guid.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::NewUID](imapisupport-newuid.md)


[Структуры MAPI](mapi-structures.md)

