---
title: Имсгсервицеадминмсгсервицетранспортордер
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
  
Задает порядок, в котором будут вызываться поставщики транспорта для доставки сообщения.
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a>Параметры

 _Куид_
  
> возврата Количество уникальных идентификаторов в параметре _лпуидлист_ . 
    
 _Лпуидлист_
  
> возврата Указатель на массив уникальных идентификаторов, представляющих поставщики транспорта. Массив содержит один идентификатор для каждого поставщика транспорта, настроенного в текущем профиле.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Транспортный заказ успешно установлен.
    
МАПИ_Е_БУСИ 
  
> Значение параметра _куид_ отличается от количества поставщиков транспорта в профиле. 
    
МАПИ_Е_НОТ_ФАУНД 
  
> Одна или несколько структур [мапиуид](mapiuid.md) , переданных в параметре _лпуидлист_ , не ссылаются на поставщика транспорта, находящихся в данный момент в профиле. 
    
## <a name="remarks"></a>Примечания

Метод **имсгсервицеадмин:: мсгсервицетранспортордер** устанавливает порядок доставки поставщиков транспорта в профиле. Параметр _лпуидлист_ должен содержать отсортированный список идентификаторов записей поставщика транспорта, полученных из свойства **пр_провидер_уид** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) таблицы, возвращаемой из [имсгсервицеадмин:: Метод Жетпровидертабле](imsgserviceadmin-getprovidertable.md) . Клиентское приложение должно передать полный список в _лпуидлист_.
  
 **Сеттранспортордер** переопределяет параметры поставщика транспорта, такие как флаг статус_ксп_префер_ласт, установленный в свойстве **пр_ресаурце_флагс** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)). 
  
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

