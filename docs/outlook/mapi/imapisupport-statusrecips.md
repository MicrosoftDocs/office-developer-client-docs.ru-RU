---
title: IMAPISupportStatusRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StatusRecips
api_type:
- COM
ms.assetid: 9c34538e-5ba4-47c8-8002-85afa9d6c067
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 39d8786bf558ade4599d69e0a764f87fe60d99f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408770"
---
# <a name="imapisupportstatusrecips"></a>IMAPISupport::StatusRecips

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает отчеты о доставке и неделивстве.
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Parameters

 _lpMessage_
  
> [in] Указатель на сообщение, для которого должен быть создан отчет.
    
 _lpRecipList_
  
> [in] Указатель на структуру [ADRLIST,](adrlist.md) которая описывает получателей сообщения, на которое указывает _lpMessage._
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Отчет был успешно создан.
    
MAPI_W_ERRORS_RETURNED 
  
> В целом вызов удался, но для этого типа получателя нет параметров получателей. Когда это предупреждение возвращается, вызов должен быть обработан как успешный. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::StatusRecips** реализован для объектов поддержки поставщиков транспорта. Поставщики транспорта звонят **в StatusRecips,** чтобы попросить MAPI отправить отчет о доставке или неделивости набору одного или более получателей сообщения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Во время обработки сообщения можно несколько раз вызывать **StatusRecips.** Однако, если вы звоните **StatusRecips** для открытого сообщения, сделайте все возможное, чтобы собрать всю информацию о доставке и неделивации для получателей сообщений и вызвать **StatusRecips** для этого списка получателей. Важна одна точка коллекции, так как несколько вызовов **StatusRecips** для одного получателя могут привести к тому, что будет отправлено несколько идентичных отчетов. 
  
Хранить свойства, которые связаны с доставкой или неделиверией сообщений в структуре **ADRLIST,** обозначенной параметром _lpRecipList._ Полный список необходимых и необязательных свойств для отчетов о доставке и отчетов о неделивстве см. в рублях [Required Report Message Properties](required-report-message-properties.md) and [Optional Report Message Properties.](optional-report-message-properties.md) 
  
Выделение памяти для **структуры ADRLIST** в _lpRecipList_ с помощью функций [MAPIAllocateBuffer](mapiallocatebuffer.md) и [MAPIAllocateMore.](mapiallocatemore.md) MAPI выпускает память, вызывая функцию [MAPIFreeBuffer](mapifreebuffer.md) только в том случае, если **StatusRecips удастся.** 
  
Обзор отчетов о доставке и неделиверии см. в статью [MAPI Report Messages.](mapi-report-messages.md)
  
## <a name="see-also"></a>См. также



[ADRLIST](adrlist.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

