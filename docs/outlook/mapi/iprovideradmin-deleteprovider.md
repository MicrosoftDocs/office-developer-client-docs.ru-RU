---
title: IProviderAdminDeleteProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.DeleteProvider
api_type:
- COM
ms.assetid: 0065b50f-95f6-4af1-81c2-a73e5111eecf
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e0f8dc1beeb669532e3731b38a4f03966403f76c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809519"
---
# <a name="iprovideradmindeleteprovider"></a>IProviderAdmin::DeleteProvider

  
  
**Относится к**: Outlook 
  
Удаляет поставщика услуг службы сообщений.
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a>Параметры

 _lpUID_
  
> [in, out] Указатель на структуру [MAPIUID](mapiuid.md) , содержащую уникальный идентификатор, представляющий поставщика для удаления. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Поставщик успешно удален из службы сообщений.
    
MAPI_E_NOT_FOUND 
  
> **MAPIUID** указывает параметр _lpUID_ не распознается. 
    
## <a name="remarks"></a>Замечания

Метод **IProviderAdmin::DeleteProvider** удаляет поставщик службы от службы сообщений. **DeleteProvider** определяет поставщик услуг для удаления, сопоставляя структура **MAPIUID** указывает _lpUID_ с набором идентификаторов зарегистрирована поставщиками услуг активный. 
  
Большинство служб сообщения не разрешать поставщиков для удаления во время профиля. Если используется поставщик для удаления **DeleteProvider** помечает для удаления вместо немедленно и возвращает значение S_OK. Если поставщик больше не используется, она удаляется. 
  
 **DeleteProvider** вызывает функцию точки входа службы сообщений, перед удалением из службы поставщика. Параметр _ulContext_ имеет значение MSG_SERVICE_PROVIDER_DELETE. Функция точки входа службы сообщение выполняет следующие задачи: 
  
- Удаляет поставщика услуг.
    
- Удаление раздела профиля поставщика услуг.
    
После удаления поставщика функции точки входа службы сообщений не вызывает еще раз.
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)

