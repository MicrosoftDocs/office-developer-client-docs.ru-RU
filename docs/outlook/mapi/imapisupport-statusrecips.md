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
ms.openlocfilehash: f3642c890c3922611d57dea6f03aca5606876864
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809192"
---
# <a name="imapisupportstatusrecips"></a>IMAPISupport::StatusRecips

  
  
**Относится к**: Outlook 
  
Создает отчеты о доставке и недоставке.
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Параметры

 _lpMessage_
  
> [in] Указатель на сообщение, для которого будет создан отчет.
    
 _lpRecipList_
  
> [in] Указатель на структуру [ADRLIST](adrlist.md) , описывающий получателей сообщения, на который указывает _lpMessage_.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Отчет создан успешно.
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов завершился успешно в целом, но параметры не получателей для этого типа получателя. При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::StatusRecips** реализуется для объектов поддержки поставщика транспорта. Поставщики транспорта вызов **StatusRecips** для запроса, MAPI отправить отчет о доставке или недоставке с набором из одного или нескольких получателей сообщения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно вызвать несколько раз **StatusRecips** во время обработки сообщения. Тем не менее если **StatusRecips** вызван для открытия сообщения, сделать все для сбора все сведения о доставке и недоставке для получателей сообщений и вызовите **StatusRecips** для этого списка получателей. Единая точка коллекции важно, потому что несколько вызовов **StatusRecips** для одного получателя может привести к нескольким отчетам идентичными, отправляемых. 
  
Хранилище свойств, относящихся к доставки сообщений или недоставке в структуре **ADRLIST** , указанное с помощью параметра _lpRecipList_ . Полный список необходимые и дополнительные свойства для отчетов о доставке и отчеты о недоставке в разделе [Необходимые свойства сообщения отчета](required-report-message-properties.md) и [Дополнительные свойства сообщения отчета](optional-report-message-properties.md). 
  
Выделите память для структуры **ADRLIST** в _lpRecipList_ с помощью функции [MAPIAllocateBuffer](mapiallocatebuffer.md) и [MAPIAllocateMore](mapiallocatemore.md) . MAPI освобождается память, путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) только в том случае, если **StatusRecips** успешно. 
  
Общие сведения о доставке и недоставке отчетов сообщения [MAPI отчета](mapi-report-messages.md).
  
## <a name="see-also"></a>См. также



[ADRLIST](adrlist.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

