---
title: IMAPISupportReadReceipt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ReadReceipt
api_type:
- COM
ms.assetid: ef31b61a-93b6-4ae8-bc71-f5ef5caf43f4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1915004847fdfd27c97656223866aaab9d3e59c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425325"
---
# <a name="imapisupportreadreceipt"></a>IMAPISupport::ReadReceipt

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает отчет о прочтях или непрочитанных сообщениях.
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет тем, как создается отчет о прочтях или непрочитанных данных. Можно установить следующий флаг:
    
MAPI_NON_READ 
  
> Создается непрочитанные отчеты. Если MAPI_NON_READ не установлен, создается отчет о прочтях.
    
 _lpReadMessage_
  
> [in] Указатель на сообщение, о котором должен быть создан отчет.
    
 _lppEmptyMessage_
  
> [in, out] При вводе  _lppEmptyMessage_ указывает на указатель на пустое сообщение. При выходе  _lppEmptyMessage_ указывает на указатель на сообщение отчета. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Отчет успешно создан.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::ReadReceipt** реализован только для объектов поддержки поставщика службы хранения сообщений. Поставщики параметров хранения сообщений вызывают **ReadReceipt,** чтобы сообщить MAPI о том, что для сообщения, на которое указывает параметр  _lpReadMessage,_ создается отчет о прочтение или непрочитанности. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызовите **ReadReceipt,** если свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested)](pidtagreadreceiptrequested-canonical-property.md)установлено и одно из следующих условий:
  
- Сообщение прочитано.
    
- Сообщение было перемещено.
    
- Сообщение скопировано.
    
- Вызван метод [IMessage::SetReadFlag](imessage-setreadflag.md) сообщения. 
    
Не **вызывайте ReadReceipt** при удалении сообщения. 
  
Отчет о прочтях или непрочитанных сообщениях следует отправлять только один раз. Отслеживайте состояние чтения сообщения и не отправляйте несколько отчетов для одного сообщения.
  
Если параметр _lppEmptyMessage_ указывает на действительное сообщение отчета, когда MAPI возвращается из **ReadReceipt,** вызовите метод [IMessage::SubmitMessage,](imessage-submitmessage.md) чтобы отправить сообщение, а затем освободите указатель, вызывая его **метод IUnknown:s:Release.** 
  
Если **сбой ReadReceipt,** сообщение должно быть освобождено без отправки. Если вы сохраняете состояние чтения сообщения, вы можете попытаться создать отчет о прочтях или непрочитанные данные позже. 
  
Можно скрыть или отобразить отчеты о прочтение и непрочитанные отчеты, созданные хранилищами в папках. Хранение отчетов для чтения и непрочитания в скрытых папках позволяет реализовать более жесткие меры безопасности.
  
## <a name="see-also"></a>См. также



[IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[Каноническое свойство PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

