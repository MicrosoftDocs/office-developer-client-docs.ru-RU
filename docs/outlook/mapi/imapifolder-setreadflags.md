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

**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает или очищает флаг MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)одного или более сообщений папки и управляет отправкой отчетов о прочтенных сообщениях. 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

_lpMsgList_
  
> [in] Указатель на массив структур [ENTRYLIST,](entrylist.md) которые определяют сообщения с флагами чтения, которые необходимо установить или очистить. Если  _для lpMsgList_ установлено NULL, флаги чтения для всех сообщений папки устанавливаются или очищаются. 
    
_ulUIParam_
  
> [in] Handle to the parent window of the progress indicator. Параметр _ulUIParam_ игнорируется, если MESSAGE_DIALOG флага в параметре _ulFlags._ 
    
_lpProgress_
  
> [in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения. Если в  _lpProgress_ передается NULL, поставщик хранилище сообщений отображает индикатор хода выполнения с помощью реализации MAPI. Параметр _lpProgress_ игнорируется, если флаг MESSAGE_DIALOG не установлен в _ulFlags._
    
_ulFlags_
  
> [in] Битоваяmas флагов, которая управляет установкой флага чтения сообщения и обработкой отчетов о прочте.. Можно установить следующие флаги:
    
  - CLEAR_READ_FLAG: флаг MSGFLAG_READ должен быть очищен в  PR_MESSAGE_FLAGS и не должен быть отправлен отчет о прочтях. 
        
  - CLEAR_NRN_PENDING: флаг MSGFLAG_NRN_PENDING должен быть очищен в PR_MESSAGE_FLAGS  и не должен быть отправлен непрочитанные отчеты. 
        
  - CLEAR_RN_PENDING: флаг MSGFLAG_RN_PENDING должен быть очищен в  PR_MESSAGE_FLAGS и не должен быть отправлен отчет о прочтях. 
        
  - GENERATE_RECEIPT_ONLY. Если отчет находится в состоянии ожидания, должен быть отправлен отчет о MSGFLAG_READ состояния.
        
  - MAPI_DEFERRED_ERRORS: позволяет **SetReadFlags** успешно возвращаться, возможно, до завершения операции. 
        
  - MESSAGE_DIALOG: отображает индикатор хода выполнения во время выполнения операции.
    
  - SUPPRESS_RECEIPT: отчет об ожидающих чтениях должен быть отменен, если запросят отчет о прочтечении и этот вызов изменяет состояние сообщения с непрочитанного на прочитанные. Если этот вызов не меняет состояние сообщения, поставщик store сообщений может игнорировать этот флаг.
    
## <a name="return-values"></a>Возвращаемые значения

S_OK 
  
> Флаг чтения для указанного сообщения или сообщений успешно установлен или очищен.
    
MAPI_E_NO_SUPPRESS 
  
> Поставщик store сообщений не поддерживает подавление отчетов о прочтениях.
    
MAPI_E_INVALID_PARAMETER 
  
> В параметре  _ulFlags_ задана одна из следующих несовместимых комбинаций флагов: 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
MAPI_W_PARTIAL_COMPLETION 
  
> Вызов был успешным, но не все сообщения были успешно обработаны. При возврате этого предупреждения вызов должен быть обработан как успешный. Чтобы проверить это предупреждение, используйте **макрос HR_FAILED.** Дополнительные сведения см. в теме ["Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Примечания

Метод **IMAPIFolder::SetReadFlags** задает или очищает флаг MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** одного или более сообщений папки. Установка флага MSGFLAG_READ помечания сообщения как прочитаного, что необязательно указывает на то, что указанный получатель действительно прочитал сообщение. 
  
**SetReadFlags** также управляет отправкой отчетов чтения. 
  
Флаг чтения нельзя изменить для следующих ок.
  
- Сообщения, которые не существуют.
    
- Сообщения, которые были перемещены в другое место.
    
- Сообщения, которые открываются с разрешением на чтение и записи.
    
- Отправленные в данный момент сообщения.
    
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Вы можете не поддерживать отправку отчетов о прочтях и запрос на подавление отчетов о прочтях. Чтобы избежать подавления отчета о прочтение, MAPI_E_NO_SUPPRESS при SUPPRESS_RECEIPT **SetReadFlags** в _параметре ulFlags._ 
  
Если параметр  _lpMsgList_ указывает на несколько сообщений, выполните операцию как можно точнее для каждого сообщения. Не останавливайте операцию раньше времени, если не произойдет сбой, который находится вне вашего контроля, например, если недостаточно памяти, недостаточно места на диске или не будет повреждения в хранилище сообщений. 
  
Если ни один из флагов не задан в параметре  _ulFlags,_ применяются следующие правила: 
  
- Если MSGFLAG_READ уже установлен, ничего не делать.
    
- Если MSGFLAG_READ не установлен, задайте его немедленно и отправьте все ожидающих отчетов о прочтение, если установлено свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested).](pidtagreadreceiptrequested-canonical-property.md)
    
При SUPPRESS_RECEIPT флага применяются следующие правила:
  
- Если MSGFLAG_READ уже установлен, ничего не делать. 
    
- Если MSGFLAG_READ не установлен, установите его и отмените все ожидающих отчетов о прочте..
    
Когда флаг CLEAR_READ_FLAG установлен, MSGFLAG_READ флага в свойстве PR_MESSAGE_FLAGS сообщения  и не отправляйте отчеты о прочтенных сообщениях. 
  
Когда флаг GENERATE_RECEIPT_ONLY, отправьте все ожидающих отчетов о прочте.. Не устанавливать и не очищать MSGFLAG_READ.
  
Если установлены SUPPRESS_RECEIPT и GENERATE_RECEIPT_ONLY, установите PR_READ_RECEIPT_REQUESTED false,  если он установлен, и не отправляйте отчет о прочтях. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Эти возвращаемые значения следует ожидать при следующих условиях.
  
|**Condition**|**Возвращаемое значение**|
|:-----|:-----|
|**SetReadFlags успешно** обработал каждое сообщение.  <br/> |S_OK  <br/> |
|**SetReadFlags** не удалось успешно обработать каждое сообщение.  <br/> |MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND  <br/> |
|Не удалось завершить **setReadFlags.**  <br/> |Любое значение ошибки, кроме MAPI_E_NOT_FOUND  <br/> |
   
Если **SetReadFlags** не удается завершить работу, не предполагать, что ничего не было сделано. **SetReadFlags** мог установить или очистить флаг MSGFLAG_READ для одного или более сообщений, прежде чем столкнуться с ошибкой. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI использует метод **IMAPIFolder::SetReadFlags,** чтобы вручную установить состояние чтения для указанных сообщений.  <br/> |
   
## <a name="see-also"></a>См. также

- [ENTRYLIST](entrylist.md) 
- [IMessage::SetReadFlag](imessage-setreadflag.md)  
- [Каноническое свойство PidTagMessageFlags](pidtagmessageflags-canonical-property.md)  
- [Каноническое свойство PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)  
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
- [MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)  
- [Использование макроса для обработки ошибок](using-macros-for-error-handling.md)

