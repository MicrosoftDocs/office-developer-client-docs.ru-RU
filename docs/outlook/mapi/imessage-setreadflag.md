---
title: IMessageSetReadFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SetReadFlag
api_type:
- COM
ms.assetid: 2d02ebf6-bb8b-42bb-9bd0-870dbae9aeb4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 874dba4aa18190792a52e29064155f5afa0ef44d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439872"
---
# <a name="imessagesetreadflag"></a>IMessage::SetReadFlag

**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает или очищает MSGFLAG_READ флага в **PR_MESSAGE_FLAGS** [(PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)свойства сообщения и управляет отправкой отчетов для чтения.
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

_ulFlags_
  
> [in] Bitmask флагов, которые контролируют параметр флага чтения сообщения, то есть флага MSGFLAG_READ  в его свойстве PR_MESSAGE_FLAGS и обработки отчетов о считывке. Можно установить следующие флаги: 
    
  - CLEAR_READ_FLAG: флаг MSGFLAG_READ должен быть очищен в  PR_MESSAGE_FLAGS и не должен быть отправлен отчет о считыве. 
      
  - CLEAR_NRN_PENDING: флаг MSGFLAG_NRN_PENDING должен быть очищен в  PR_MESSAGE_FLAGS и не читать отчет не должен быть отправлен. 
      
  - CLEAR_RN_PENDING: флаг MSGFLAG_RN_PENDING должен быть очищен в PR_MESSAGE_FLAGS  и не следует отослать отчет о считыве. 
      
  - GENERATE_RECEIPT_ONLY. Отчет о считыве должен быть отправлен, если он находится в ожидании, но не должно быть изменений в состоянии MSGFLAG_READ флага.
      
  - MAPI_DEFERRED_ERRORS. Позволяет **SetReadFlag** успешно возвращаться, возможно, до завершения операции. 
      
  - SUPPRESS_RECEIPT: ожидающих чтения отчет должен быть отменен, если отчет о прочтя был запротезировали, и этот вызов изменяет состояние сообщения с непрочитанные для чтения. Если этот вызов не изменит состояние сообщения, поставщик магазина сообщений может игнорировать этот флаг.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Флаг чтения сообщения успешно установлен или очищен.
    
MAPI_E_NO_SUPPRESS 
  
> Поставщик магазина сообщений не поддерживает подавление отчетов о считывке.
    
MAPI_E_INVALID_PARAMETER 
  
> Одна из следующих комбинаций флагов задана в параметре _ulFlags:_ 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
## <a name="remarks"></a>Примечания

Метод **IMessage::SetReadFlag** задает или очищает флаг MSGFLAG_READ сообщения в  свойстве PR_MESSAGE_FLAGS и вызывает [IMAPIProp::SaveChanges](imapiprop-savechanges.md) для сохранения сообщения. Установка флага MSGFLAG_READ означает, что сообщение было прочитано, что не обязательно указывает на то, что получатель действительно прочитал сообщение. 
  
**SetReadFlags** также управляет отправкой отчетов для чтения. Отчет о считывке отправляется только в том случае, если отправитель запросил его. 
  
Флаг чтения нельзя изменить для:
  
- Сообщения, которые не существуют.
    
- Сообщения, перенесенные в другое место.
    
- Сообщения, открытые с разрешения на чтение и написание.
    
- Сообщения, которые в настоящее время отправлены.
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если ни один из флагов не задан в  _параметре ulFlags,_ применяются следующие правила: 
  
- Если MSGFLAG_READ уже установлен, ничего не делать.
    
- Если MSGFLAG_READ не установлено, установите его и отправьте все  ожидающих отчеты о прочтение, если PR_READ_RECEIPT_REQUESTED[(PidTagReadReceiptRequested)](pidtagreadreceiptrequested-canonical-property.md)свойство установлено.
    
Если установлены SUPPRESS_RECEIPT и GENERATE_RECEIPT_ONLY флаги, PR_READ_RECEIPT_REQUESTED, если установлено, должно быть очищено и не следует отправить отчет о считыве.
  
Когда SUPPRESS_RECEIPT флаг:
  
- Если MSGFLAG_READ уже установлен, ничего не делать. 
    
- Если MSGFLAG_READ не установлено, установите его и отмените все ожидающих отчеты о прочтевом состоянии.
    
Когда за установлен CLEAR_READ_FLAG флаг, MSGFLAG_READ флаг в свойстве PR_MESSAGE_FLAGS сообщения и не **отправляйте** отчеты о считыве. 
  
Когда установлен GENERATE_RECEIPT_ONLY флаг, отправьте все ожидающих отчеты о прочтевом состоянии. Не устанавливай и не MSGFLAG_READ.
  
Если за установлены SUPPRESS_RECEIPT и GENERATE_RECEIPT_ONLY, установите свойство PR_READ_RECEIPT_REQUESTED FALSE, если оно за установлено, и не отправьте отчет о считыве.
  
Вы можете оптимизировать поведение отчетов, подавлив генерацию отчетов для чтения при определенных условиях. Однако, если вы не поддерживаете подавление отчетов и клиент вызывает **SetReadFlag** с набором флага SUPPRESS_RECEIPT, MAPI_E_NO_SUPPRESS. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI использует **метод IMessage::SetReadFlag** для набора флагов чтения в выбранных сообщениях.  <br/> |
   
## <a name="see-also"></a>См. также

- [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)  
- [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)  
- [IMAPIProp::GetProps](imapiprop-getprops.md)  
- [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 
- [Каноническое свойство PidTagMessageFlags](pidtagmessageflags-canonical-property.md) 
- [IMessage: IMAPIProp](imessageimapiprop.md)
- [Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

