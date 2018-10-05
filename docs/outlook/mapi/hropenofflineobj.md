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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395800"
---
# <a name="hropenofflineobj"></a>HrOpenOfflineObj

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Открывает автономные объекта на основе заданного профиля.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортировать с:  <br/> |Msmapi32.dll  <br/> |
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
  
> [in] Этот параметр не используется. Он должен иметь значение 0.
    
 _pwszProfileNameIn_
  
> [in] Имя профиля, автономного объекта. Должны быть выражены в Юникод. 
    
 _pGUID_
  
> [in] Указатель на идентификатор GUID, который можно использовать для уникальной идентификации данного объекта от других автономных объектов. Это должен быть **GUID_GlobalState**.
    
 _Сохраняются_
  
> [in] Этот параметр не используется. Должен иметь **значение null**.
    
 _ppOfflineObj_
  
> [out] Указатель на запрошенный объект автономной. Абонент может использовать этот указатель для доступа к [IMAPIOfflineMgr: IMAPIOffline](imapiofflinemgrimapioffline.md) интерфейс для определения обратных вызовов, которые поддерживает этот объект и настройка обратных вызовов для него. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK 
  
- Вызов функции выполнен успешно.
    
MAPI_E_NOT_FOUND
  
- Сбой вызова функции.
    
## <a name="remarks"></a>Замечания

Это первый вызов, с помощью клиента, когда клиенту требуется получать уведомления о изменения состояния подключения для заданного профиля. При вызове **HrOpenOfflineObj**, клиент получает автономного объекта, который поддерживает **IMAPIOfflineMgr**. Клиент можно проверить для видов обратных вызовов, поддерживаемые объектом (с помощью [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)) и затем настроить обратных вызовов для него (с помощью [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).
  
При использовании [GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) следует искать адреса этой функции msmapi32.dll, укажите **HrOpenOfflineObj@20** в качестве имени процедуры. 
  
 **HrOpenOfflineObj** работает только для клиентов, которые являются поставщики MAPI, COM-надстройки и расширения клиента Exchange, выполняемых в рамках процесса Outlook. В противном случае **HrOpenOfflineObj** возвращает **MAPI_E_NOT_FOUND**. 
  
## <a name="see-also"></a>См. также



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Сведения об API автономного состояния](about-the-offline-state-api.md)
  
[��������� MAPI](mapi-constants.md)

