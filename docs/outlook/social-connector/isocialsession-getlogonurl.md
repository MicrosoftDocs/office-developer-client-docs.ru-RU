---
title: ISocialSessionGetLogonUrl
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61bab07-acb3-433b-8783-c3fe110a5582
description: Получает строку, представляюную URL-адрес, используемый для представления пользователю браузерной формы во время веб-проверки подлинности.
ms.openlocfilehash: 83867282922ea136b9673609cc2ba2f1a206f6ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427915"
---
# <a name="isocialsessiongetlogonurl"></a>ISocialSession::GetLogonUrl

Получает строку, представляюную URL-адрес, используемый для представления пользователю браузерной формы во время веб-проверки подлинности.
  
```cpp
HRESULT _stdcall GetLogonUrl([out, retval] BSTR* url);
```

## <a name="parameters"></a>Параметры

_url_
  
> [out] Строка, содержаная URL-адрес формы, используемой для веб-проверки подлинности.
    
## <a name="remarks"></a>Примечания

После того как форма будет представлена пользователю, метод [ISocialSession::LogonWeb](isocialsession-logonweb.md) будет вызван с пустой строкой для _параметра connectIn._ 
  
## <a name="see-also"></a>См. также

- [ISocialSession : IUnknown](isocialsessioniunknown.md)

