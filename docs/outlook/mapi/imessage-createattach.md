---
title: Имессажекреатеаттач
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351116"
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

 _Лпинтерфаце_
  
> возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к сообщению. Передача результатов NULL в стандартный интерфейс сообщения (или **iMessage**) возвращается. 
    
 _ulFlags_
  
> возврата Битовая маска флагов, определяющих способ создания вложения. Можно задать следующий флаг:
    
МАПИ_ДЕФЕРРЕД_ЕРРОРС 
  
> Разрешает успешное возвращение **креатеаттач** , возможно, перед тем, как вложение будет полностью доступно для вызывающего клиента. Если вложение недоступно, то выполнение последующих вызовов может привести к ошибке. 
    
 _Лпулаттачментнум_
  
> вышли Указатель на номер индекса, идентифицирующий вновь созданное вложение. Это значение действительно только в том случае, если сообщение открыто и является основой для свойства **пр_аттач_нум** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) вложения.
    
 _Лппаттач_
  
> вышли Указатель на указатель на открытый объект вложения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вложение успешно создано.
    
## <a name="remarks"></a>Примечания

Метод **iMessage:: креатеаттач** создает новое вложение для сообщения. Новое вложение и все свойства, заданные для него, недоступны до тех пор, пока клиент не вызовет метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) для вложения и сообщение **IMAPIProp:: SaveChanges** . 
  
Номер вложения, на который указывает _лпулаттачментнум_ , является уникальным и действительным только в пределах контекста сообщения. То есть два вложения в двух разных сообщениях могут иметь одинаковый номер, в то время как два вложения в одном сообщении не могут. 
  
## <a name="see-also"></a>См. также



[IMessage: IMAPIProp](imessageimapiprop.md)

