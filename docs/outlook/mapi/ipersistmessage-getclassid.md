---
title: иперсистмессажежетклассид
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetClassID
api_type:
- COM
ms.assetid: 77eeb468-3432-4ccd-9c1e-1df9ce605193
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3f0d98b8ffa13fe238fc0fcf8ff0ec76a3a284eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309627"
---
# <a name="ipersistmessagegetclassid"></a>IPersistMessage::GetClassID

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает идентификатор, представляющий сервер форм, который может управлять формой. 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a>Параметры

 _лпклассид_
  
> [вход, выход] Указатель на идентификатор класса (CLSID) формы.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Идентификатор класса был успешно возвращен.
    
## <a name="remarks"></a>Примечания

Метод **иперсистмессже::** задает содержимое параметра _лпклассид_ для идентификатора класса сервера форм и возвращает S_OK. Если средство просмотра **форм вызывает метод** вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов [Uninitialized](uninitialized-state.md) вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов. 
  
Дополнительные сведения о том, как идентификаторы класса используются с структурированными объектами хранения, представлены в документации по методу [иперсист::::](https://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) . 
  
## <a name="see-also"></a>См. также



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

