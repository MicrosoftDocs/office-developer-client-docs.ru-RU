---
title: IMSProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.Shutdown
api_type:
- COM
ms.assetid: 9ca1861d-9bc9-485a-9807-a598b869e5a2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 77688f8a09c1d990201a247a3c4e3a11ba0963b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438626"
---
# <a name="imsprovidershutdown"></a>IMSProvider::Shutdown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Закрывает поставщика магазина сообщений упорядоченным способом.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpulFlags_
  
> [in] Зарезервировано; должно быть указателем на ноль.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов удался и возвращает ожидаемое значение или значения.
    
## <a name="remarks"></a>Примечания

MAPI вызывает **метод IMSProvider::Shutdown** непосредственно перед выпуском объекта поставщика магазина сообщений. MAPI выпускает все объекты с логотипом для поставщика перед вызовом **выключения** для этого поставщика. 
  
## <a name="see-also"></a>См. также



[IMSProvider : IUnknown](imsprovideriunknown.md)

