---
title: IMAPISecureMessageGetBaseMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISecureMessage.GetBaseMessage
api_type:
- COM
ms.assetid: 573f40c5-e0d2-4281-8c22-10a1ae1f0dee
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a2da3f6851e45a70dcd4604396a85430c539a830
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428580"
---
# <a name="imapisecuremessagegetbasemessage"></a>IMAPISecureMessage::GetBaseMessage

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Извлекает в основном [IMessage : IMAPIProp,](imessageimapiprop.md) что это [IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md) является инкапсуляция. 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a>Parameters

 _ppmsg_
  
> [вышел] Объект безопасного сообщения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="see-also"></a>См. также



[IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

