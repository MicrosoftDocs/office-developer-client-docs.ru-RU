---
title: Имапиоффлинемградвисе
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
ms.openlocfilehash: 3ca7fdc39da8d3ee8ecf6f0f253284df10a392e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321429"
---
# <a name="imapiofflinemgradvise"></a>IMAPIOfflineMgr::Advise

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Регистрирует клиент для получения обратных вызовов в автономном объекте.
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
>  возврата Флаги, которые изменяют поведение. Поддерживается только значение МАПИОФФЛИНЕ_АДВИСЕ_ДЕФАУЛТ. 
    
 _Падвисеинфо_
  
> возврата Сведения о типе обратного вызова, когда для получения обратного вызова, интерфейса обратного вызова для вызывающего абонента и других сведений. Он также содержит маркер клиента, который Outlook использует при отправке последующего обратного вызова для клиентского абонента.
    
 _Пуладвисетокен_
  
> вышли Токен advise, возвращенный клиентскому абоненту для последовательного отмены обратного вызова для объекта.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Вызов выполнен успешно.
    
E_INVALIDARG
  
> Указан недопустимый параметр.
    
E_NOINTERFACE
  
> Интерфейс обратного вызова, указанный в *падвисеинфо* , является недопустимым. 
    
## <a name="remarks"></a>Замечания

При открытии автономного объекта с помощью **[хропеноффлинеобж](hropenofflineobj.md)** клиент получает автономный объект, поддерживающий **имапиоффлинемгр**. Клиент может проверить виды обратных вызовов, поддерживаемые объектом, с помощью **[имапиоффлине:: Capabilities](imapioffline-getcapabilities.md)**. Клиент может определить тип и другие сведения о обратном вызове, а затем вызвать метод **имапиоффлинемгр:: Advise** для регистрации, чтобы получать такие обратные вызовы для объекта. 
  
## <a name="see-also"></a>См. также



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)


[��������� MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

