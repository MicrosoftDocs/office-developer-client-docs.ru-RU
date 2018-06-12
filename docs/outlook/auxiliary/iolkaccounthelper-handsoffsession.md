---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: Освобождает объект сеанса MAPI, возвращаемые IOlkAccountHelper::GetMapiSession.
ms.openlocfilehash: 71931be73e75e858224d3da2c92071341ac45e72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807835"
---
# <a name="iolkaccounthelperhandsoffsession"></a>IOlkAccountHelper::HandsOffSession

Освобождает объект сеанса MAPI, возвращаемые - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|ЗНАЧЕНИЕ S_OK  <br/> |Если реализация **IOlkAccountHelper** создает собственный сеанса MAPI, который возвращается в **IOlkAccountHelper::GetMapiSession**, необходимо освобождать этого сеанса и возвращает значение S_OK.  <br/> |
|E_NOTIMPL  <br/> |Если реализация **IOlkAccountHelper** не была создана сеанса MAPI, должен возвращать только значение E_NOTIMPL. В этом случае это поддерживается только возвращаемое значение.  <br/> |
   
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md)

