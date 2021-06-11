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
ms.openlocfilehash: 28786f483c4d2031c334d7b9697db7c5e627fe93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437366"
---
# <a name="imessagesubmitmessage"></a>IMessage::SubmitMessage

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сохраняет все свойства сообщения и отмечает сообщение как готовое к отправлению.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Bitmask флагов, используемых для управления отправкой сообщения. Можно установить следующий флаг:
    
FORCE_SUBMIT 
  
> MAPI должен немедленно отправить сообщение. Этот флаг в настоящее время не используется.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_RECIPIENTS 
  
> Таблица получателей сообщения пуста.
    
## <a name="remarks"></a>Примечания

Метод **IMessage::SubmitMessage** отмечает сообщение как готовое к передаче. MAPI передает сообщения в систему обмена сообщениями в порядке, в котором они помечены для отправки. Из-за этой функции сообщение может находиться в хранилище сообщений в течение некоторого времени, прежде чем система обмена сообщениями может взять на себя ответственность за это. Порядок получения в пункте назначения находится в системе управления системой обмена сообщениями и не обязательно соответствует порядку отправки сообщений. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Чтобы сохранить его, позвоните по методу [IMAPIProp::SaveChanges,](imapiprop-savechanges.md) а затем **проверьте** свойство [PR_MESSAGE_FLAGS (PidTagMessageFlags).](pidtagmessageflags-canonical-property.md) Если флаг MSGFLAG_RESEND, позвоните [по телефону IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md). **PrepareSubmit** обновляет свойство **PR_RESPONSIBILITY** [(PidTagResponsibility)](pidtagresponsibility-canonical-property.md)для всех получателей в повторном сообщении.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

При **возвращении SubmitMessage** все указатели на сообщение и связанные с ним подобекты сообщения, папки, вложения, потоки, таблицы и т. д. больше не допустимы. MAPI не разрешает дальнейшие операции по этим указателям, за исключением вызова их **методов IUnknown::Release.** MAPI разработан таким образом, что после того, как **будет вызвано сообщение SubmitMessage,** необходимо освободить сообщение и все связанные субобпроекты. Однако если **SubmitMessage** возвращает значение ошибки с указанием отсутствующих или недействительных сведений, сообщение остается открытым, а указатели остаются действительными. 
  
Чтобы отменить операцию отправки, перед отправкой сообщения **получите и храните указатель** на свойство PR_ENTRYID [(PidTagEntryId).](pidtagentryid-canonical-property.md) Так как идентификатор записи сообщения недействителен после отправки сообщения, необходимо сохранить его перед вызовом **SubmitMessage.** Чтобы отменить отправку, указывайте параметр  _lpEntryId_ на этот идентификатор записи и позвоните [в IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |**CFolderDlg::OnSubmitMessage** <br/> |MFCMAPI использует **метод IMessage::SubmitMessage** для отправки выбранного сообщения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

