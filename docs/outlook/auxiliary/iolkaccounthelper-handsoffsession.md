---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: Выпускает объект сеанса MAPI, возвращенный IOlkAccountHelper::GetMapiSession.
ms.openlocfilehash: c481cee1ecb8c2bd3997cdee8ae86c9c3b5a712e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418633"
---
# <a name="iolkaccounthelperhandsoffsession"></a>IOlkAccountHelper::HandsOffSession

Выпускает объект сеанса MAPI, который был возвращен - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).
  
## <a name="quick-info"></a>Краткие сведения

См. [iOlkAccountHelper](iolkaccounthelper.md).
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Если при реализации **IOlkAccountHelper** создается собственный сеанс MAPI, который возвращается в **IOlkAccountHelper::GetMapiSession,** необходимо освободить сеанс здесь и вернуться S_OK.  <br/> |
|E_NOTIMPL  <br/> |Если реализация **IOlkAccountHelper** не создает собственную сессию MAPI, необходимо возвращать только E_NOTIMPL. В этом случае это единственное поддерживаемые значения возврата.  <br/> |
   
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md)

