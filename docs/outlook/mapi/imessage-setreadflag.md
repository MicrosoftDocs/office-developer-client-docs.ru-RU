---
title: имессажесетреадфлаг
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
  
Задает или снимает флаг MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) сообщения и управляет отправкой отчетов о прочтении.
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

_ulFlags_
  
> возврата Битовая маска флагов, которые управляют параметром флага чтения сообщения, флаг MSGFLAG_READ сообщения в свойстве **PR_MESSAGE_FLAGS** и обработки отчетов о прочтении. Можно задать следующие флаги: 
    
  - CLEAR_READ_FLAG: флажок MSGFLAG_READ должен быть снят в **PR_MESSAGE_FLAGS** , а отчет о прочтении не должен быть отправлен. 
      
  - CLEAR_NRN_PENDING: флажок MSGFLAG_NRN_PENDING должен быть снят в **PR_MESSAGE_FLAGS** , а отчет о состоянии, не являющемся отчетом о прочтении, не должен отправляться. 
      
  - CLEAR_RN_PENDING: флажок MSGFLAG_RN_PENDING должен быть снят в **PR_MESSAGE_FLAGS** , а отчет о прочтении не должен быть отправлен. 
      
  - GENERATE_RECEIPT_ONLY: отчет о прочтении должен быть отправлен, если он находится в состоянии ожидания, но в состоянии флага MSGFLAG_READ не должно быть никаких изменений.
      
  - MAPI_DEFERRED_ERRORS: разрешает успешно возвращаться **сетреадфлаг** , возможно, до завершения операции. 
      
  - SUPPRESS_RECEIPT: ожидающий отчет о прочтении должен быть отменен, если был запрошен отчет о прочтении, и этот вызов изменяет состояние сообщения с "непрочтено" на "чтение". Если этот вызов не изменяет состояние сообщения, поставщик хранилища сообщений может игнорировать этот флаг.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Флаг чтения сообщения успешно установлен или снят.
    
MAPI_E_NO_SUPPRESS 
  
> Поставщик хранилища сообщений не поддерживает отдавление отчетов о прочтении.
    
MAPI_E_INVALID_PARAMETER 
  
> В параметре _ulFlags_ задано одно из следующих сочетаний флагов: 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
## <a name="remarks"></a>Примечания

Метод **iMessage:: сетреадфлаг** задает или очищает флаг MSGFLAG_READ сообщения в свойстве **PR_MESSAGE_FLAGS** и вызывает [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) для сохранения сообщения. При установке флага MSGFLAG_READ сообщение помечается как прочитанное, что не обязательно свидетельствует о том, что предполагаемый получатель действительно прочитал сообщение. 
  
**Сетреадфлагс** также управляет отправкой отчетов о прочтении. Отчет о прочтении отправляются только в том случае, если отправитель запросил его. 
  
Невозможно изменить флаг чтения для:
  
- Несуществующие сообщения.
    
- Сообщения, перемещенные в другое место.
    
- Сообщения, открытые с разрешениями на чтение и запись.
    
- Отправленные в настоящее время сообщения.
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если ни один из флагов не задан в параметре _ulFlags_ , применяются следующие правила. 
  
- Если MSGFLAG_READ уже заданы, ничего делать не нужно.
    
- Если MSGFLAG_READ не задано, установите его и отправьте все ожидающие отчеты о прочтении, если задано свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)).
    
Если установлены флаги SUPPRESS_RECEIPT и GENERATE_RECEIPT_ONLY, то PR_READ_RECEIPT_REQUESTED бит (если он установлен) должен быть снят, а отчет о прочтении не должен быть отправлен.
  
Если установлен флаг SUPPRESS_RECEIPT:
  
- Если MSGFLAG_READ уже заданы, ничего делать не нужно. 
    
- Если MSGFLAG_READ не задано, установите его и отмените все ожидающие отчеты о прочтении.
    
Если установлен флаг CLEAR_READ_FLAG, снимите флаг MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** каждого сообщения и не отправляются отчеты о прочтении. 
  
Когда установлен флаг GENERATE_RECEIPT_ONLY, отправьте все ожидающие отчеты о прочтении. Не задавайте и не снимайте MSGFLAG_READ.
  
Если установлены флаги SUPPRESS_RECEIPT и GENERATE_RECEIPT_ONLY, задайте для свойства PR_READ_RECEIPT_REQUESTED значение FALSE, если оно задано и не отправляет отчет о прочтении.
  
Вы можете оптимизировать поведение отчета, отменив создание отчетов о прочтении при определенных условиях. Тем не менее, если вы не поддерживаете отдавление отчетов и клиент вызывает **сетреадфлаг** с установленным флагом SUPPRESS_RECEIPT, возвращайте MAPI_E_NO_SUPPRESS. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Фолдердлг. cpp  <br/> |Кфолдердлг:: Онсетреадфлаг  <br/> |MFCMAPI использует метод **iMessage:: сетреадфлаг** для установки флагов чтения для выбранных сообщений.  <br/> |
   
## <a name="see-also"></a>См. также

- [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)  
- [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)  
- [IMAPIProp::GetProps](imapiprop-getprops.md)  
- [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 
- [Каноническое свойство PidTagMessageFlags](pidtagmessageflags-canonical-property.md) 
- [IMessage: IMAPIProp](imessageimapiprop.md)
- [Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

