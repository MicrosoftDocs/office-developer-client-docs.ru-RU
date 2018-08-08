---
title: IMAPIOfflineMgrUnadvise
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
ms.openlocfilehash: b52dcd87c8714ad59db560a5ae4a8300f9cc83ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809008"
---
# <a name="imapiofflinemgrunadvise"></a>IMAPIOfflineMgr::Unadvise

  
  
**Относится к**: Outlook 
  
Отменяет обратных вызовов для объекта в автономном режиме.
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Флаги для отмены обратного вызова. Поддерживается только значение MAPIOFFLINE_UNADVISE_DEFAULT.
    
 _ulAdviseToken_
  
> [in] Маркер уведомлений, определяющий регистрацию обратного вызова, который должен быть отменен. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK
  
> Вызов выполнен успешно. Этот вызов должен возвращать значение S_OK.
    
## <a name="remarks"></a>Замечания

Удаляет регистрацию для обратного вызова, которая была связана с *ulAdviseToken* возвращаются из предыдущего вызова **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Использует объект **IMAPIOfflineMgr** для освобождения ссылку на объект **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** , связанный с *ulAdviseToken* . 
  
## <a name="see-also"></a>См. также



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[��������� MAPI](mapi-constants.md)

