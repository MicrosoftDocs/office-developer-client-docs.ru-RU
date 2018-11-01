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
ms.openlocfilehash: 9cc2f5f3880466c0a70febedbc7aaec987b62bb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572095"
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

## <a name="parameters"></a>Параметры

 _lpInterface_
  
> [in] Указатель на интерфейс идентификатор, представляющий интерфейса, которые будут использоваться для доступа к сообщение (ИД интерфейса). Передача значение NULL, результаты в стандартный интерфейс сообщения или **IMessage**, возвращаемых. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет способ создания вложение. Можно задать следующий флаг:
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **CreateAttach** для возврата успешно, возможно перед вложением является полностью доступны для клиента. Если вложение не доступно, последующие подключения к нему может вызвать ошибку. 
    
 _lpulAttachmentNum_
  
> [out] Указатель на индекса номер, идентифицирующий только что созданный вложения. Этот номер является допустимым только в том случае, если сообщение открыто и является основой для свойства **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) вложения.
    
 _lppAttach_
  
> [out] Указатель на указатель на объект открыть вложение.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вложение успешно создан.
    
## <a name="remarks"></a>Замечания

Метод **IMessage::CreateAttach** создает новый вложения сообщения. Новое вложение и свойств, заданные для него, недоступны, пока называется клиента метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) вложения и метод **IMAPIProp::SaveChanges** сообщений. 
  
Номер вложения, на который указывает _lpulAttachmentNum_ — это уникальное и допускается только в контексте сообщения. То есть два вложений в двух разных сообщений может быть тот же номер, а два вложений в то же сообщение нельзя. 
  
## <a name="see-also"></a>См. также



[IMessage: IMAPIProp](imessageimapiprop.md)

