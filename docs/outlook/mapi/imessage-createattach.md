---
title: IMessageCreateAttach
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IMessage::CreateAttach
api_type:
- COM
ms.assetid: 01711aca-c598-438c-88d7-0719b6691e34
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f534912377aadb3c342030fc02fce26693857476
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417674"
---
# <a name="imessagecreateattach"></a>IMessage::CreateAttach

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает новое вложение.
  
```cpp
HRESULT CreateAttach(
LPCIID lpInterface,
ULONG ulFlags,
ULONG FAR * lpulAttachmentNum,
LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a>Parameters

 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к сообщению. Передача NULL приводит к возвращению стандартного интерфейса сообщения или **IMessage.** 
    
 _ulFlags_
  
> [in] Bitmask флагов, которые контролируют, как создается вложение. Можно установить следующий флаг:
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **CreateAttach** успешно возвращаться, возможно, до полного доступности вложения для вызываемого клиента. Если вложение не доступно, последующий вызов может привести к ошибке. 
    
 _lpulAttachmentNum_
  
> [вышел] Указатель на номер индекса, определяющий недавно созданное вложение. Этот номер действителен только в том случае, если сообщение  открыто и является основой для свойства[PR_ATTACH_NUM (PidTagAttachNumber).](pidtagattachnumber-canonical-property.md)
    
 _lppAttach_
  
> [вышел] Указатель на указатель на открытый объект вложения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вложение было успешно создано.
    
## <a name="remarks"></a>Примечания

Метод **IMessage::CreateAttach** создает новое вложение в сообщение. Новое вложение и все свойства, которые для него установлены, недоступны до тех пор, пока клиент не вызвал метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) и метод **IMAPIProp::SaveChanges.** 
  
Номер вложения, на который указывает  _lpulAttachmentNum,_ уникален и действителен только в контексте сообщения. То есть два вложения в двух разных сообщениях могут иметь одинаковое число, а два вложения в одном сообщении не могут. 
  
## <a name="see-also"></a>См. также



[IMessage: IMAPIProp](imessageimapiprop.md)

