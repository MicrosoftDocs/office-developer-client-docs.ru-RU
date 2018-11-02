---
title: IMsgServiceAdminMsgServiceTransportOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.MsgServiceTransportOrder
api_type:
- COM
ms.assetid: c57ada0e-b9a1-496b-8548-75686d8cba4e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 559f1c609000608d0eb920a0240ac8848e4bc2a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570795"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a>IMsgServiceAdmin::MsgServiceTransportOrder

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает порядок вызова поставщиков какие транспорта доставить сообщение.
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a>Параметры

 _cUID_
  
> [in] Число уникальных идентификаторов с помощью параметра _lpUIDList_ . 
    
 _lpUIDList_
  
> [in] Указатель на массив уникальные идентификаторы, представляющие поставщиками транспорта. Массив содержит один идентификатор для каждого поставщика транспорта, настроенных в текущий профиль.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Порядок транспорта успешно установлены.
    
MAPI_E_BUSY 
  
> Значение параметра _cUID_ отличается от числа поставщиками транспорта фактически в профиле. 
    
MAPI_E_NOT_FOUND 
  
> Одно или несколько из структур [MAPIUID](mapiuid.md) , переданной в параметре _lpUIDList_ относится к поставщика транспорта в настоящее время в профиле. 
    
## <a name="remarks"></a>Примечания

Метод **IMsgServiceAdmin::MsgServiceTransportOrder** задает порядок доставки поставщиками транспорта в профиле. Параметр _lpUIDList_ должен содержать отсортированный список идентификаторов запись поставщика транспорта, полученного из свойства **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) в таблице, возвращенный из [IMsgServiceAdmin:: GetProviderTable](imsgserviceadmin-getprovidertable.md) метод. Клиентское приложение должно передавать полный список в _lpUIDList_.
  
 **SetTransportOrder** переопределений транспорта параметры поставщика, такие как флаг STATUS_XP_PREFER_LAST в свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)). 
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

