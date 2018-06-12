---
title: IOlkAccountHelperGetMapiSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a431787c-6e9a-9be1-165f-98c778d12e3e
description: Открытие сеанса MAPI и поддерживает ссылку на сеанс для диспетчера учетных записей.
ms.openlocfilehash: 50809a00d13fd9f2a93bebc2961a134b3625e82c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807860"
---
# <a name="iolkaccounthelpergetmapisession"></a>IOlkAccountHelper::GetMapiSession

Открытие сеанса MAPI и поддерживает ссылку на сеанс для диспетчера учетных записей.
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::GetMapiSession(  
    LPUNKNOWN *ppmsess 
);
```

## <a name="parameters"></a>Parameters

_ppmsess_
  
> [out] Текущий сеанс MAPI.
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="remarks"></a>Remarks

Из-за проблем с циклические ссылки диспетчер учетных записей самого не может поддерживать ссылку для сеанса MAPI.
  
## <a name="see-also"></a>См. также

- [IOlkAccountHelper::HandsOffSession](iolkaccounthelper-handsoffsession.md)
- [IMAPISession: IUnknown](http://msdn.microsoft.com/library/5650fa2a-6e62-451c-964e-363f7bee2344%28Office.15%29.aspx)

