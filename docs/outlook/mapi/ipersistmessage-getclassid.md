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
ms.openlocfilehash: e0937eed2e8ca61bc18ee45ff20337267808ea70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809486"
---
# <a name="ipersistmessagegetclassid"></a>IPersistMessage::GetClassID

  
  
**Относится к**: Outlook 
  
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

