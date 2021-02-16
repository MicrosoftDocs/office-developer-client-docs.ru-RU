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
  
Открывает автономный объект на основе заданного профиля.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортируется с помощью:  <br/> |msmapi32.dll  <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
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

 _ulReserved_
  
> [in] Этот параметр не используется. Должно быть 0.
    
 _pwszProfileNameIn_
  
> [in] Имя профиля, для которого является автономный объект. Оно должно быть выражено в Юникоде. 
    
 _pGUID_
  
> [in] Указатель на GUID, который можно использовать для уникальной идентификации этого объекта из других автономных объектов. Он должен быть **GUID_GlobalState.**
    
 _pReserved_
  
> [in] Этот параметр не используется. Оно должно иметь **null.**
    
 _ppOfflineObj_
  
> [out] Указатель на запрашиваемого автономного объекта. Этот указатель можно использовать для доступа к интерфейсу [IMAPIOfflineMgr : IMAPIOffline,](imapiofflinemgrimapioffline.md) чтобы найти поддерживаемые объектом вызовы и настроить для него их. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK 
  
- Вызов функции успешно.
    
MAPI_E_NOT_FOUND
  
- Сбой вызова функции.
    
## <a name="remarks"></a>Примечания

Это первый вызов, который клиент совершает, когда клиент хочет получить уведомление о любых изменениях состояния подключения для данного профиля. После вызова **HrOpenOfflineObj** клиент получает автономный объект, который поддерживает **IMAPIOfflineMgr.** Клиент может проверить виды вызовов, поддерживаемые объектом (с помощью [IMAPIOffline::GetCapabilities),](imapioffline-getcapabilities.md)а затем настроить для него вызовы (с помощью [IMAPIOfflineMgr::Advise).](imapiofflinemgr-advise.md)
  
При использовании [GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) для искомого адреса этой функции в msmapi32.dll укажите HrOpenOfflineObj@20 **в** качестве имени процедуры. 
  
 **HrOpenOfflineObj** работает только для клиентов, которые являются поставщиками MAPI, надстройки COM и клиентские расширения Exchange, запущенные в процессе Outlook. В **противном случае HrOpenOfflineObj** **возвращает** MAPI_E_NOT_FOUND . 
  
## <a name="see-also"></a>См. также



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Об API автономного режима](about-the-offline-state-api.md)
  
[Константы MAPI](mapi-constants.md)

