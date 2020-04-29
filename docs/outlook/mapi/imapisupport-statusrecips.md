---
title: имаписуппортстатусреЦипс
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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создание отчетов о доставке и недоставке.
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Параметры

 _лпмессаже_
  
> возврата Указатель на сообщение, для которого должен быть создан отчет.
    
 _лпреЦиплист_
  
> возврата Указатель на структуру [ADRLIST](adrlist.md) , которая описывает получателей сообщения, на которое указывает _лпмессаже_.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Отчет успешно создан.
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов выполнен в целом, но для этого типа получателя не заданы параметры получателя. При возвращении этого предупреждения вызов должен обрабатываться как успешный. Чтобы проверить это предупреждение, используйте макрос **HR_FAILED** . Дополнительные сведения см. [в разделе Использование макросов для обработки ошибок](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Примечания

Метод **имаписуппорт:: статусреЦипс** реализован для объектов поддержки поставщика транспорта. Поставщики транспорта вызывают **статусреЦипс** , чтобы запросить отправку отчета о доставке или недоставке в набор из одного или нескольких получателей сообщения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы можете вызвать **статусреЦипс** несколько раз во время обработки сообщения. Однако при вызове **статусреЦипс** для открытого сообщения рекомендуется собрать все сведения о доставке и недоставке для получателей сообщения и вызвать **статусреЦипс** для этого списка получателей. Единственная точка семейства важна, так как несколько вызовов **статусреЦипс** для одного получателя могут привести к отправке нескольких одинаковых отчетов. 
  
Хранение свойств, которые относятся к доставке или доставке сообщений, в структуре **ADRLIST** , указанной параметром _лпреЦиплист_ . Полный список обязательных и необязательных свойств для отчетов о доставке и отчетов о недоставке см. в разделе [обязательные свойства сообщений отчета](required-report-message-properties.md) и [необязательные свойства сообщения отчета](optional-report-message-properties.md). 
  
Выделение памяти для структуры **ADRLIST** в _лпреЦиплист_ с помощью функций [мапиаллокатебуффер](mapiallocatebuffer.md) и [мапиаллокатеморе](mapiallocatemore.md) . MAPI освобождает память, вызывая функцию [мапифрибуффер](mapifreebuffer.md) только в случае успешного выполнения **статусреЦипс** . 
  
Обзор отчетов о доставке и недоставке можно найти в разделе [сообщения отчетов MAPI](mapi-report-messages.md).
  
## <a name="see-also"></a>См. также



[ADRLIST](adrlist.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

