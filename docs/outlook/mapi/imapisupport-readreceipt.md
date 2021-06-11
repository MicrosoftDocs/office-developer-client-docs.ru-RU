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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает отчет о прочтях или непрочитанных сообщениях.
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Битмаска флагов, которая управляет тем, как создается отчет о считывке или непрочитанке. Можно установить следующий флаг:
    
MAPI_NON_READ 
  
> Создается непрочитаемый отчет. Если MAPI_NON_READ не установлено, создается отчет о считыве.
    
 _lpReadMessage_
  
> [in] Указатель на сообщение, о котором должен быть создан отчет.
    
 _lppEmptyMessage_
  
> [in, out] На входе  _lppEmptyMessage_ указывает на указатель на пустое сообщение. На выходе  _lppEmptyMessage_ указывает указатель на сообщение отчета. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Отчет был успешно создан.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::ReadReceipt** реализуется только для объектов поддержки поставщиков сообщений. Поставщики магазинов сообщений вызывают **ReadReceipt,** чтобы поручить MAPI создать отчет о считывке или непрочитанности для сообщения, на которое указывает _параметр lpReadMessage._ 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызов **ReadReceipt** **при PR_READ_RECEIPT_REQUESTED** свойства [(PidTagReadReceiptRequested)](pidtagreadreceiptrequested-canonical-property.md)и верно одно из следующих условий:
  
- Сообщение было прочитано.
    
- Сообщение было перемещено.
    
- Сообщение было скопировано.
    
- Был вызван метод [IMessage::SetReadFlag.](imessage-setreadflag.md) 
    
Не **вызывайте ReadReceipt** при удалении сообщения. 
  
Отчет о считываемом или непрочитаемом тексте должен отправляться только один раз для сообщения. Отслеживайте состояние чтения сообщения и не отправляйте несколько отчетов для одного сообщения.
  
Если параметр _lppEmptyMessage_ указывает на действительное сообщение отчета при возвращении MAPI из **ReadReceipt,** позвоните в [метод IMessage::SubmitMessage,](imessage-submitmessage.md) чтобы отправить сообщение, а затем отпустите указатель, назвав метод **IUnknown:s:Release.** 
  
Если **readReceipt** не удается, сообщение должно быть выпущено без отправки. Если вы сохраняете состояние чтения сообщения, можно попытаться создать отчет о считывке или непрочитанном тексте в более позднее время. 
  
Можно скрыть или отобразить отчеты о считываемых и непрочитаемых данных, созданные в магазинах в папках. Хранение отчетов о прочтение и непрочитание в скрытых папках позволяет реализовать более жесткую безопасность.
  
## <a name="see-also"></a>См. также



[IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[Каноническое свойство PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

