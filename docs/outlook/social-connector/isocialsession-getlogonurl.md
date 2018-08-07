---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Получает строку, представляющую URL-адрес, используемый для представления формы на основе браузера для пользователя в ходе проверки подлинности web.
ms.openlocfilehash: 343919f194b238fc519bb8f6d808b44a8ab6e7b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812736"
---
# <a name="isocialsessiongetlogonurl"></a>ISocialSession::GetLogonUrl

Получает строку, представляющую URL-адрес, используемый для представления формы на основе браузера для пользователя в ходе проверки подлинности web.
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a>Параметры

_URL-адрес_
  
> [out] Строка, содержащая URL-адрес для формы, используемые в веб-проверка подлинности.
    
## <a name="remarks"></a>Замечания

После форма будет предоставлен пользователю, метод [ISocialSession::LogonWeb](isocialsession-logonweb.md) вызывается с пустая строка для параметра _connectIn_ . 
  
## <a name="see-also"></a>См. также

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

