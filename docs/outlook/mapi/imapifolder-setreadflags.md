---
title: IMAPIFolderSetReadFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetReadFlags
api_type:
- COM
ms.assetid: 95a40c8a-0a8b-46c7-a07a-cbc6a7de8a3c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 15504ecc88188ed7bc4eed0e64b1871dbc6a5e8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406915"
---
# <a name="imapifoldersetreadflags"></a>IMAPIFolder::SetReadFlags

**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает или очищает флаг MSGFLAG_READ в **PR_MESSAGE_FLAGS** [(PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)свойства одного или более сообщений папки и управляет отправкой отчетов о считывке. 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

_lpMsgList_
  
> [in] Указатель на массив структур [ENTRYLIST,](entrylist.md) которые определяют сообщения или сообщения, которые считывались флагами для набора или очистки. Если  _для lpMsgList_ установлено NULL, для всех сообщений папки установлены или очищаются флаги чтения. 
    
_ulUIParam_
  
> [in] Ручка родительского окна индикатора прогресса. Параметр _ulUIParam_ игнорируется, если флаг MESSAGE_DIALOG в параметре _ulFlags._ 
    
_lpProgress_
  
> [in] Указатель на объект progress, отображает индикатор прогресса. Если NULL передается в  _lpProgress,_ поставщик магазина сообщений отображает индикатор прогресса с помощью реализации MAPI. Параметр  _lpProgress_ игнорируется, если флаг MESSAGE_DIALOG не установлен в  _ulFlags_.
    
_ulFlags_
  
> [in] Битмашка флагов, контролирующих настройку флага чтения сообщения и обработку отчетов о считывке. Можно установить следующие флаги:
    
  - CLEAR_READ_FLAG: флаг MSGFLAG_READ должен быть очищен в  PR_MESSAGE_FLAGS и не следует отослать отчет о считыве. 
        
  - CLEAR_NRN_PENDING: флаг MSGFLAG_NRN_PENDING должен быть очищен в PR_MESSAGE_FLAGS  и нечитаемый отчет не должен быть отправлен. 
        
  - CLEAR_RN_PENDING: флаг MSGFLAG_RN_PENDING должен быть очищен в  PR_MESSAGE_FLAGS и не следует отослать отчет о считыве. 
        
  - GENERATE_RECEIPT_ONLY. Отчет о считыве должен быть отправлен, если он находится в ожидании, но не должно быть изменений в состоянии MSGFLAG_READ флага.
        
  - MAPI_DEFERRED_ERRORS: Позволяет **setReadFlags** успешно возвращаться, возможно, до завершения операции. 
        
  - MESSAGE_DIALOG: отображает индикатор прогресса во время выполнения операции.
    
  - SUPPRESS_RECEIPT: ожидающих чтения отчет должен быть отменен, если отчет о прочтя был запротезировали, и этот вызов изменяет состояние сообщения с непрочитанные для чтения. Если этот вызов не изменит состояние сообщения, поставщик магазина сообщений может игнорировать этот флаг.
    
## <a name="return-values"></a>Возвращаемые значения

S_OK 
  
> Флаг чтения указанного сообщения или сообщений был успешно задан или очищен.
    
MAPI_E_NO_SUPPRESS 
  
> Поставщик магазина сообщений не поддерживает подавление отчетов о считывке.
    
MAPI_E_INVALID_PARAMETER 
  
> Одна из следующих несовместимых комбинаций флагов задана в параметре _ulFlags:_ 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
MAPI_W_PARTIAL_COMPLETION 
  
> Вызов удался, но не все сообщения были успешно обработаны. Когда это предупреждение возвращается, вызов должен быть обработан как успешный. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Примечания

Метод **IMAPIFolder::SetReadFlags** задает или очищает флаг MSGFLAG_READ  в PR_MESSAGE_FLAGS свойстве одного или более сообщений папки. Установка флага MSGFLAG_READ означает сообщение как чтение, что не обязательно указывает на то, что получатель действительно прочитал сообщение. 
  
**SetReadFlags** также управляет отправкой отчетов для чтения. 
  
Флаг чтения не может быть изменен для следующих:
  
- Сообщения, которые не существуют.
    
- Сообщения, перенесенные в другое место.
    
- Сообщения, открытые с разрешения на чтение и написание.
    
- Сообщения, которые в настоящее время отправлены.
    
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Вы можете принять решение не поддерживать отправку отчетов о считыве и запрос на подавление отчетов о считыве. Чтобы не подавлять отчет о прочтение, MAPI_E_NO_SUPPRESS **когда setReadFlags** SUPPRESS_RECEIPT в параметре _ulFlags._ 
  
Когда  _параметр lpMsgList_ указывает на несколько сообщений, выполните операцию максимально полной для каждого сообщения. Не останавливайте операцию преждевременно, если не произойдет сбой, неподконтрольный вам, например из-за потери памяти, потери дискового пространства или повреждения в хранилище сообщений. 
  
Если ни один из флагов не задан в  _параметре ulFlags,_ применяются следующие правила: 
  
- Если MSGFLAG_READ уже установлен, ничего не делать.
    
- Если MSGFLAG_READ не установлено, установите его немедленно и отправьте все  ожидающих отчеты о прочтение, если PR_READ_RECEIPT_REQUESTED[(PidTagReadReceiptRequested)](pidtagreadreceiptrequested-canonical-property.md)свойство установлено.
    
При SUPPRESS_RECEIPT флаге применяются следующие правила:
  
- Если MSGFLAG_READ уже установлен, ничего не делать. 
    
- Если MSGFLAG_READ не установлено, установите его и отмените все ожидающих отчеты о прочтевом состоянии.
    
Когда за установлен CLEAR_READ_FLAG флаг, MSGFLAG_READ флаг в свойстве PR_MESSAGE_FLAGS сообщения и не **отправляйте** отчеты о считыве. 
  
Когда установлен GENERATE_RECEIPT_ONLY флаг, отправьте все ожидающих отчеты о прочтевом состоянии. Не устанавливай и не MSGFLAG_READ.
  
Когда установлены SUPPRESS_RECEIPT и GENERATE_RECEIPT_ONLY флаги, установите PR_READ_RECEIPT_REQUESTED  false, если он установлен, и не отправьте отчет о прочтителье. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Ожидайте этих значений возврата в следующих условиях.
  
|**Condition**|**Возвращаемое значение**|
|:-----|:-----|
|**SetReadFlags** успешно обработал каждое сообщение.  <br/> |S_OK  <br/> |
|**SetReadFlags** не удалось успешно обработать каждое сообщение.  <br/> |MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND  <br/> |
|**SetReadFlags** не удалось выполнить.  <br/> |Любое значение ошибки, кроме MAPI_E_NOT_FOUND  <br/> |
   
Если **SetReadFlags** не удается выполнить, не думайте, что работа не была сделана. **SetReadFlags,** возможно, удалось установить или очистить флаг MSGFLAG_READ для одного или более сообщений, прежде чем столкнуться с ошибкой. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI использует метод **IMAPIFolder::SetReadFlags,** чтобы вручную установить состояние чтения указанных сообщений.  <br/> |
   
## <a name="see-also"></a>См. также

- [ENTRYLIST](entrylist.md) 
- [IMessage::SetReadFlag](imessage-setreadflag.md)  
- [Каноническое свойство PidTagMessageFlags](pidtagmessageflags-canonical-property.md)  
- [Каноническое свойство PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)  
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
- [MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)  
- [Использование макроса для обработки ошибок](using-macros-for-error-handling.md)

