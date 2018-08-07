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
ms.openlocfilehash: 70c8bd36142d18b541ad6a2e0ded3bebcfb6dbb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809043"
---
# <a name="imapisecuremessagegetbasemessage"></a>IMAPISecureMessage::GetBaseMessage

  
  
**Относится к**: Outlook 
  
Получает базовый [IMessage: IMAPIProp](imessageimapiprop.md) , это [IMAPISecureMessage: IUnknown](imapisecuremessageiunknown.md) является инкапсуляции. 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a>Параметры

 _ppmsg_
  
> [out] Объект защищенного сообщения.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="see-also"></a>См. также



[IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

