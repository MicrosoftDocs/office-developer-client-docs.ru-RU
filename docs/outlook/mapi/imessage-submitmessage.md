---
title: IMessageSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SubmitMessage
api_type:
- COM
ms.assetid: 9ce93469-c55d-48d1-9abb-a637716ed4f2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 67c86f39898b4bd0c019b9b3095c9449e6e60b1b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567323"
---
# <a name="imessagesubmitmessage"></a>IMessage::SubmitMessage

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сохраняет все свойства сообщений и помечает сообщения как Готово к отправке.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, используемые для управления, как отправить сообщение. Можно задать следующий флаг:
    
FORCE_SUBMIT 
  
> MAPI следует отправить сообщение немедленно. Этот флаг не в настоящее время используется.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_RECIPIENTS 
  
> Таблица получателей сообщения будет пустым.
    
## <a name="remarks"></a>Примечания

Метод **IMessage::SubmitMessage** помечает сообщения как готовые для передачи. MAPI передает сообщения системы обмена сообщениями в том порядке, в котором они помечены как для отправки. Из-за эту функцию сообщение может оставаться в хранилище сообщений некоторое время вступления системы обмена сообщениями ответственность за его. Порядок получения в месте назначения находится в базовом обмена сообщениями системы управления и не соответствует порядке, в котором отправки сообщения. 
  
## <a name="notes-to-implementers"></a>Примечания для реализующих

Вызов метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) сообщения, сохраните его и проверьте свойство message **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). Если значение флага MSGFLAG_RESEND, вызовите [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md). **PrepareSubmit** обновления тип получателя и свойство **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) для всех получателей в повторная отправка сообщений.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

При возврате **SubmitMessage** , все указатели на сообщение и его сообщения связанных вложенных папок, вложения, потоки, таблицы и т. п. недействительны. MAPI не разрешает любых дополнительных операций на эти указатели, за исключением вызова их методов **функции IUnknown::Release** . Таким образом, что после вызова **SubmitMessage** освобождение сообщения и все связанные с ним вложенных предоставляет MAPI. Тем не менее если **SubmitMessage** возвращает значение, указывающее, отсутствующие или недопустимые данные ошибки, сообщение открыто и указатели остаются действительными. 
  
Чтобы отменить операцию отправки, получения и хранения указатель свойство message **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) перед отправкой сообщения. Так как идентификатор записи сообщения недействительными после отправки сообщения, это необходимо для сохранения до вызова метода **SubmitMessage**. Чтобы отменить отправить, выберите параметр _lpEntryId_ этот идентификатор записи и вызова [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |**CFolderDlg::OnSubmitMessage** <br/> |Mfcmapi (en) использует метод **IMessage::SubmitMessage** для отправки выбранного сообщения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

