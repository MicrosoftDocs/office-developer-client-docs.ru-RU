---
title: Имапиоффлинемгрунадвисе
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Unadvise
api_type:
- COM
ms.assetid: 250b9137-facb-81a2-41b1-96a57366c04e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 800f79179f999ba193d4177abb7341095b8b896d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321219"
---
# <a name="imapiofflinemgrunadvise"></a>IMAPIOfflineMgr::Unadvise

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
ОтМеняет обратные вызовы для автономного объекта.
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Флаги для отмены обратного вызова. Поддерживается только значение МАПИОФФЛИНЕ_УНАДВИСЕ_ДЕФАУЛТ.
    
 _Уладвисетокен_
  
> возврата Токен advise, определяющий регистрацию обратного вызова, которая должна быть отменена. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Вызов выполнен успешно. Этот вызов должен возвращать значение S_OK.
    
## <a name="remarks"></a>Замечания

Удаляет регистрацию для обратного вызова, который был связан с *уладвисетокен* , возвращенный при предыдущем вызове метода **[Имапиоффлинемгр:: Advise](imapiofflinemgr-advise.md)**. Заставляет объект **имапиоффлинемгр** освобождать ссылку на объект **[имапиоффлиненотифи](imapiofflinenotifyiunknown.md)** , связанный с *уладвисетокен* . 
  
## <a name="see-also"></a>См. также



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[Константы MAPI](mapi-constants.md)

