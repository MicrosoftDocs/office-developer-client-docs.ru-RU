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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Завершает список получателей сообщения, расширяя определенные списки рассылки.
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpMessage_
  
> [in] Указатель на сообщение, для обработки в списке получателей.
    
 _lpulFlags_
  
> [out] Указатель на битовуюmask флагов, которая управляет типом обработки, которая происходит. Можно установить следующие флаги:
    
NEEDS_PREPROCESSING 
  
> Перед его отправлением сообщение должно быть предварительно разобрано.
    
NEEDS_SPOOLER 
  
> Сообщение должно отправляться пулом MAPI (а не поставщиком транспорта, к которому тесно совмещение вызываемой службы).
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Список получателей сообщения успешно обработан.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::ExpandRecips** реализован для объектов поддержки поставщика store сообщений. Поставщики store сообщений **звонят в ExpandRecips,** чтобы отправить запрос MAPI на выполнение следующих задач: 
  
- Разорите некоторые личные списки рассылки до получателей компонентов.
    
- Замените все отображаемые имена, которые были изменены, на исходные имена.
    
- Пометить все повторяющиеся записи.
    
- Разрешите все одновключные адреса. 
    
- Проверьте, требуется ли предварительной подготовке сообщения, и, если да, установите для флага, на который указывает  _lpulFlags,_ значение NEEDS_PREPROCESSING. 
    
 **ExpandRecips** расширяет все списки рассылки с типом адреса обмена сообщениями MAPIPDL. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Всегда **вызывайте ExpandRecips** в рамках обработки сообщений. Сделайте вызов **ExpandRecips** одним из первых вызовов в реализации метода [IMessage::SubmitMessage.](imessage-submitmessage.md) 
  
## <a name="see-also"></a>См. также



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

