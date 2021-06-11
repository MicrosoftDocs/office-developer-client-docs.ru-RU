---
title: IMAPISupportExpandRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ExpandRecips
api_type:
- COM
ms.assetid: 78edd549-d557-489a-85f5-adfb5c44a7d4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 105219fe430cd8746c3aa6cf5cd90629d5f72080
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411248"
---
# <a name="imapisupportexpandrecips"></a>IMAPISupport::ExpandRecips

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Завершает список получателей сообщения, расширяя определенные списки рассылки.
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpMessage_
  
> [in] Указатель на сообщение, которое должно обрабатывать список получателей.
    
 _lpulFlags_
  
> [вышел] Указатель на битмаску флагов, которая контролирует тип обработки, которая происходит. Можно установить следующие флаги:
    
NEEDS_PREPROCESSING 
  
> Перед отправлением сообщение должно быть предварительно отправлено.
    
NEEDS_SPOOLER 
  
> Spooler MAPI (а не поставщик транспорта, к которому вызываемая тесная пара) должен отправить сообщение.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Список получателей сообщения был успешно обработан.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::ExpandRecips** реализован для объектов поддержки поставщиков сообщений. Поставщики магазинов сообщений **звонят в ExpandRecips,** чтобы побудить MAPI выполнить следующие задачи: 
  
- Расширь некоторые списки личных рассылки до получателей компонентов.
    
- Замените все имена отображения, которые были изменены, на исходные имена.
    
- Пометить все дублирующиеся записи.
    
- Устранение всех разных адресов. 
    
- Проверьте, требуется ли предварительное препроцессинг сообщения, и, если оно имеется, установите флаг, на который указывает  _lpulFlags,_ NEEDS_PREPROCESSING. 
    
 **ExpandRecips** расширяет списки рассылки, которые имеют тип адреса обмена сообщениями MAPIPDL. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Всегда **вызывайте ExpandRecips** в рамках обработки сообщений. Сделайте вызов **в ExpandRecips** одним из первых вызовов в реализации метода [IMessage::SubmitMessage.](imessage-submitmessage.md) 
  
## <a name="see-also"></a>См. также



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

