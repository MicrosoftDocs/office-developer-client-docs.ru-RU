---
title: IPersistMessageGetClassID
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
ms.openlocfilehash: c9d769e6a32fad22750a965debbbdce83e4de539
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586461"
---
# <a name="ipersistmessagegetclassid"></a>IPersistMessage::GetClassID

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Возвращает идентификатор, представляющий сервера форм для управления формы. 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a>Параметры

 _lpClassID_
  
> [in, out] Указатель на идентификатор класса (CLSID) формы.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Идентификатор класса успешно возвращен.
    
## <a name="remarks"></a>Замечания

Метод **IPersistMessge::GetClassID** задает содержимое параметра _lpClassID_ идентификатор класса сервера форм и возвращает значение S_OK. Когда форма просмотра вызывает **GetClassID** и его пройдет успешно, формы переводится в состояние [не инициализировано](uninitialized-state.md) . 
  
Дополнительные сведения об использовании идентификаторов классов в структурированных объектов хранилища метод [IPersist::GetClassID](http://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) см. 
  
## <a name="see-also"></a>См. также



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

