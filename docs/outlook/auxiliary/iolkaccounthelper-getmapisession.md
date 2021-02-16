---
title: IOlkAccountHelperGetMapiSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a431787c-6e9a-9be1-165f-98c778d12e3e
description: Открывает сеанс MAPI и сохраняет ссылку на сеанс для диспетчера учетных записей.
ms.openlocfilehash: 5886ac1ae1bb8f3b43e09f49e48434d9a73656ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322178"
---
# <a name="iolkaccounthelpergetmapisession"></a>IOlkAccountHelper::GetMapiSession

Открывает сеанс MAPI и сохраняет ссылку на сеанс для диспетчера учетных записей.
  
## <a name="quick-info"></a>Краткие сведения

См. [IOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::GetMapiSession(  
    LPUNKNOWN *ppmsess 
);
```

## <a name="parameters"></a>Параметры

_ppmsess_
  
> [out] Текущий сеанс MAPI.
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Примечания

Из-за проблем с цикликой ссылок диспетчер учетных записей не может поддерживать ссылку для сеанса MAPI.
  
## <a name="see-also"></a>См. также

- [IOlkAccountHelper::HandsOffSession](iolkaccounthelper-handsoffsession.md)
- [IMAPISession: IUnknown](https://msdn.microsoft.com/library/5650fa2a-6e62-451c-964e-363f7bee2344%28Office.15%29.aspx)

