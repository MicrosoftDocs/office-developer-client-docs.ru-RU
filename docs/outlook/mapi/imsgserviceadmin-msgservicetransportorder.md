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
ms.openlocfilehash: 3d532e0eb46daa412711344421936a58da309b7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420096"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a>IMsgServiceAdmin::MsgServiceTransportOrder

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает порядок, в котором будут вызваны поставщики транспорта для доставки сообщения.
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a>Параметры

 _cUID_
  
> [in] Количество уникальных идентификаторов в параметре _lpUIDList._ 
    
 _lpUIDList_
  
> [in] Указатель на массив уникальных идентификаторов, которые представляют поставщиков транспорта. Массив содержит один идентификатор для каждого поставщика транспорта, настроенного в текущем профиле.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Порядок транспорта успешно установлен.
    
MAPI_E_BUSY 
  
> Значение параметра  _cUID_ отличается от числа поставщиков транспорта в профиле. 
    
MAPI_E_NOT_FOUND 
  
> Одна или несколько структур [MAPIUID,](mapiuid.md) переданных в  _параметре lpUIDList,_ не ссылаются на поставщика транспорта, который в данный момент находится в профиле. 
    
## <a name="remarks"></a>Примечания

Метод **IMsgServiceAdmin::MsgServiceTransportOrder** задает порядок доставки поставщиков транспорта в профиле. Параметр _lpUIDList_ должен содержать отсортируемый список идентификаторов записей поставщика транспорта, полученных из свойства **PR_PROVIDER_UID** ([PidTagProviderUid)](pidtagprovideruid-canonical-property.md)таблицы, возвращаемой методом [IMsgServiceAdmin::GetProviderTable.](imsgserviceadmin-getprovidertable.md) Клиентские приложения должны передавать полный список  _в lpUIDList_.
  
 **SetTransportOrder** переопределяет параметры поставщика транспорта, такие как флаг STATUS_XP_PREFER_LAST, установленный в свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags).](pidtagresourceflags-canonical-property.md) 
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

