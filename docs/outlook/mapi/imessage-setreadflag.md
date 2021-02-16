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

**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает или очищает MSGFLAG_READ флага в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)сообщения и управляет отправкой отчетов о прочтенных сообщениях.
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

_ulFlags_
  
> [in] Битовая почта флагов, которая управляет установкой флага чтения сообщения, то есть флагом MSGFLAG_READ сообщения в его свойстве **PR_MESSAGE_FLAGS** и обработкой отчетов о прочтовке. Можно установить следующие флаги: 
    
  - CLEAR_READ_FLAG: флаг MSGFLAG_READ должен быть очищен в  PR_MESSAGE_FLAGS и не должен быть отправлен отчет о прочтях. 
      
  - CLEAR_NRN_PENDING: флаг MSGFLAG_NRN_PENDING должен быть очищен в  PR_MESSAGE_FLAGS и не должен быть отправлен отчет о непрочитанных сообщениях. 
      
  - CLEAR_RN_PENDING: флаг MSGFLAG_RN_PENDING должен быть очищен в PR_MESSAGE_FLAGS  и не должен быть отправлен отчет о прочтях. 
      
  - GENERATE_RECEIPT_ONLY. Если отчет находится в состоянии ожидания, должен быть отправлен отчет о MSGFLAG_READ состояния.
      
  - MAPI_DEFERRED_ERRORS: позволяет **SetReadFlag** успешно возвращаться, возможно, до завершения операции. 
      
  - SUPPRESS_RECEIPT: отчет об ожидающих чтениях должен быть отменен, если запросят отчет о прочтечении и этот вызов изменяет состояние сообщения с непрочитанного на прочитанные. Если этот вызов не меняет состояние сообщения, поставщик store сообщений может игнорировать этот флаг.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Флаг чтения сообщения успешно установлен или очищен.
    
MAPI_E_NO_SUPPRESS 
  
> Поставщик store сообщений не поддерживает подавление отчетов о прочтениях.
    
MAPI_E_INVALID_PARAMETER 
  
> В параметре  _ulFlags_ задано одно из следующих сочетаний флагов: 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
## <a name="remarks"></a>Примечания

Метод **IMessage::SetReadFlag** задает или очищает флаг MSGFLAG_READ сообщения в свойстве **PR_MESSAGE_FLAGS** и вызывает [IMAPIProp::SaveChanges,](imapiprop-savechanges.md) чтобы сохранить сообщение. Установка флага MSGFLAG_READ помечания сообщения как прочитаного, что необязательно указывает на то, что указанный получатель действительно прочитал сообщение. 
  
**SetReadFlags** также управляет отправкой отчетов чтения. Отчет о прочтовке отправляется только в том случае, если отправитель запросил его. 
  
Флаг чтения нельзя изменить для:
  
- Сообщения, которые не существуют.
    
- Сообщения, которые были перемещены в другое место.
    
- Сообщения, которые открываются с разрешением на чтение и записи.
    
- Отправленные в данный момент сообщения.
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если ни один из флагов не задан в параметре  _ulFlags,_ применяются следующие правила: 
  
- Если MSGFLAG_READ уже установлен, ничего не делать.
    
- Если MSGFLAG_READ не установлен, задайте его и отправьте все ожидающих отчетов о прочтение, если установлено свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested).](pidtagreadreceiptrequested-canonical-property.md)
    
Если установлены SUPPRESS_RECEIPT и GENERATE_RECEIPT_ONLY, следует очистить бит PR_READ_RECEIPT_REQUESTED, если он установлен, и не отправить отчет о прочтях.
  
Если установлен SUPPRESS_RECEIPT флага:
  
- Если MSGFLAG_READ уже установлен, ничего не делать. 
    
- Если MSGFLAG_READ не установлен, установите его и отмените все ожидающих отчетов о прочте..
    
Когда флаг CLEAR_READ_FLAG установлен, MSGFLAG_READ флага в свойстве PR_MESSAGE_FLAGS сообщения  и не отправляйте отчеты о прочтенных сообщениях. 
  
Когда флаг GENERATE_RECEIPT_ONLY, отправьте все ожидающих отчетов о прочте.. Не устанавливать и не очищать MSGFLAG_READ.
  
Если установлены SUPPRESS_RECEIPT и GENERATE_RECEIPT_ONLY, установите для свойства PR_READ_RECEIPT_REQUESTED false, если оно установлено, и не отправьте отчет о прочте.
  
Вы можете оптимизировать поведение отчетов, подавляя генерацию отчетов о прочтение при определенных условиях. Однако если вы не поддерживаете подавление отчетов и клиент вызывает **SetReadFlag** с установленным флагом SUPPRESS_RECEIPT, MAPI_E_NO_SUPPRESS. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI использует метод **IMessage::SetReadFlag,** чтобы установить флаги чтения для выбранных сообщений.  <br/> |
   
## <a name="see-also"></a>См. также

- [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)  
- [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)  
- [IMAPIProp::GetProps](imapiprop-getprops.md)  
- [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 
- [Каноническое свойство PidTagMessageFlags](pidtagmessageflags-canonical-property.md) 
- [IMessage: IMAPIProp](imessageimapiprop.md)
- [Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

