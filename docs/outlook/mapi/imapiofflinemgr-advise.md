---
title: IMAPIOfflineMgrAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Advise
api_type:
- COM
ms.assetid: 784b6218-548d-817a-caaa-cf9be6bc3d2f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 53fa6bd49190bb88daeb0438dc0112e34322383e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809002"
---
# <a name="imapiofflinemgradvise"></a>IMAPIOfflineMgr::Advise

  
  
**Относится к**: Outlook 
  
Регистрация клиента для получения обратных вызовов для автономного объекта.
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
>  [in] Флаги, которые изменяют поведение. Поддерживается только значение MAPIOFFLINE_ADVISE_DEFAULT. 
    
 _pAdviseInfo_
  
> [in] Сведения о типе обратного вызова, когда получать обратного вызова, интерфейс обратного вызова для вызывающего абонента и другие сведения. Он также содержит маркер клиента, который использует Outlook при отправке обратных вызовов последующим уведомлением вызывающего клиента.
    
 _pulAdviseToken_
  
> [out] Маркер уведомлений, возвращаются вызывающему клиента для впоследствии Отмена обратного вызова для объекта.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK
  
> Вызов выполнен успешно.
    
E_INVALIDARG
  
> Указан недопустимый параметр.
    
E_NOINTERFACE
  
> Недопустимый интерфейс обратного вызова, указанного в *pAdviseInfo* . 
    
## <a name="remarks"></a>Замечания

При открытии автономного объекта с помощью **[HrOpenOfflineObj](hropenofflineobj.md)**, клиент получает автономного объекта, который поддерживает **IMAPIOfflineMgr**. Клиент можно проверить наличие видов поддерживается объектом с помощью **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** обратных вызовов. Клиент можно определить тип и другие сведения о обратного вызова, он хочет, а затем вызвать **IMAPIOfflineMgr::Advise** для получения таких обратных вызовов об объекте. 
  
## <a name="see-also"></a>См. также



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)


[��������� MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)
