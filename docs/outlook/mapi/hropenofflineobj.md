---
title: HrOpenOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrOpenOfflineObj
api_type:
- HeaderDef
ms.assetid: cee1a940-fe01-d364-5d7c-c9e9dfeb8979
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3ef929bf778fabc4350f553d185838dd5cb2cf0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347749"
---
# <a name="hropenofflineobj"></a>HrOpenOfflineObj

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Открывает автономный объект на основе заданных профилей.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортировано:  <br/> |MSMapi32. dll  <br/> |
|Вызывающая сторона:  <br/> |Client  <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
   
```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
      ULONG ulReserved, 
      LPCWSTR pwszProfileNameIn, 
      const GUID* pGUID, 
      const GUID* pReserved, 
      IMAPIOfflineMgr** ppOfflineObj); 

```

## <a name="parameters"></a>Параметры

 _улресервед_
  
> возврата Этот параметр не используется. Значение должно быть равно 0.
    
 _пвсзпрофиленамеин_
  
> возврата Имя профиля, для которого предназначен автономный объект. Он должен быть выражен в Юникоде. 
    
 _пгуид_
  
> возврата Указатель на GUID, который можно использовать для уникальной идентификации этого объекта из других автономных объектов. Необходимо **GUID_GlobalState**.
    
 _Сохранен_
  
> возврата Этот параметр не используется. Он должен иметь **значение NULL**.
    
 _ппоффлинеобж_
  
> вышли Указатель на запрошенный автономный объект. Вызывающий абонент может использовать этот указатель для доступа к интерфейсу [имапиоффлинемгр: имапиоффлине](imapiofflinemgrimapioffline.md) для поиска обратных вызовов, поддерживаемых этим объектом, а также для настройки обратных вызовов для него. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK 
  
- Вызов функции выполнен успешно.
    
MAPI_E_NOT_FOUND
  
- Сбой при вызове функции.
    
## <a name="remarks"></a>Примечания

Это первый вызов, который выполняет клиент, когда клиент хочет получать уведомления о любых изменениях состояния подключения для данного профиля. При вызове **хропеноффлинеобж**клиент получает автономный объект, поддерживающий **имапиоффлинемгр**. Клиент может проверить виды обратных вызовов, поддерживаемые объектом (с помощью [имапиоффлине::-Capabilities](imapioffline-getcapabilities.md)), а затем настроить для него обратные вызовы (с помощью [Имапиоффлинемгр:: Advise](imapiofflinemgr-advise.md)).
  
При использовании [GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) для поиска адреса этой функции в MSMapi32. dll укажите **HrOpenOfflineObj@20** в качестве имени процедуры. 
  
 **Хропеноффлинеобж** работает только для клиентов, которые являются поставщиками MAPI, надстройками COM и клиентскими расширениями Exchange, запущенными в процессе Outlook. В противном случае **хропеноффлинеобж** возвращает **MAPI_E_NOT_FOUND**. 
  
## <a name="see-also"></a>См. также



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Об API автономного режима](about-the-offline-state-api.md)
  
[Константы MAPI](mapi-constants.md)

