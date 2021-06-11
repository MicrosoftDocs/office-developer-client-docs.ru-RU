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
ms.openlocfilehash: 28dbbb98c9810bb688b9ecdd730ef6c4ada5f60b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404864"
---
# <a name="iprovideradmindeleteprovider"></a>IProviderAdmin::DeleteProvider

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Удаляет поставщика услуг из службы сообщений.
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a>Parameters

 _lpUID_
  
> [in, out] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит уникальный идентификатор, который представляет поставщика для удаления. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Поставщик был успешно удален из службы сообщений.
    
MAPI_E_NOT_FOUND 
  
> **MapIUID,** на который указывает _параметр lpUID,_ не был распознан. 
    
## <a name="remarks"></a>Примечания

Метод **IProviderAdmin::D eleteProvider** удаляет поставщика услуг из службы сообщений. **DeleteProvider** определяет поставщика услуг для удаления путем совпадения структуры **MAPIUID,** на которые указывает  _lpUID,_ с набором идентификаторов, зарегистрированных активными поставщиками услуг. 
  
Большинство служб сообщений не позволяют удалять поставщиков во время использования профиля. Если поставщик для удаления используется, **DeleteProvider** пометит его для удаления, а не удалить его немедленно и возвращает S_OK. Если поставщик больше не используется, он удаляется. 
  
 **DeleteProvider** вызывает функцию точки входа службы сообщений перед удалением поставщика из службы. Параметр  _ulContext_ задан для MSG_SERVICE_PROVIDER_DELETE. Функция точки входа службы сообщений выполняет следующие задачи: 
  
- Удаляет поставщика услуг.
    
- Удаляет раздел профилей поставщика услуг.
    
Функция точки входа службы сообщений после удаления поставщика не будет снова вызвана.
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)

