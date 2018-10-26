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
ms.openlocfilehash: 88185efea344844016547d0844277de6e0d661db
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578320"
---
# <a name="imapifoldersetreadflags"></a>IMAPIFolder::SetReadFlags

**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает или сбрасывает MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) из одного или нескольких сообщений, папок и управляет Отправка чтения отчеты. 
  
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
  
> [in] Указатель на массив структур [ENTRYLIST](entrylist.md) , чтобы указать сообщения или сообщения, прочли флаги, установите или снимите флажок. Если _lpMsgList_ имеет значение NULL, прочтите помечает для всех установить или снять папки сообщений. 
    
_ulUIParam_
  
> [in] Дескриптор родительского окна индикатор хода выполнения. Параметр _ulUIParam_ игнорируется, пока флаг MESSAGE_DIALOG будет выполнен с помощью параметра _ulFlags_ . 
    
_lpProgress_
  
> [in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения. Если в _lpProgress_передается значение NULL, поставщика хранилища сообщений отображает индикатор хода выполнения с помощью реализации MAPI's. Параметр _lpProgress_ используется только флаг MESSAGE_DIALOG установлен в _ulFlags_.
    
_ulFlags_
  
> [in] Битовая маска флаги, которыми управляет состояние флага чтения сообщения и обработку чтение отчеты. Можно задать следующие флажки:
    
  - CLEAR_READ_FLAG: Флаг MSGFLAG_READ должен быть снят в **PR_MESSAGE_FLAGS** и не будут отправляться просмотра отчета. 
        
  - CLEAR_NRN_PENDING: Флаг MSGFLAG_NRN_PENDING должен быть снят в **PR_MESSAGE_FLAGS** и не будут отправляться непрочитанные сообщения отчета. 
        
  - CLEAR_RN_PENDING: Флаг MSGFLAG_RN_PENDING должен быть снят в **PR_MESSAGE_FLAGS** и не будут отправляться просмотра отчета. 
        
  - GENERATE_RECEIPT_ONLY: Чтения отчет следует отправить один ожидающий, когда должно быть никаких изменений в состояние флага MSGFLAG_READ.
        
  - MAPI_DEFERRED_ERRORS: Разрешает **SetReadFlags** для возврата успешно, возможно до завершения операции. 
        
  - MESSAGE_DIALOG: Отображает индикатор хода выполнения во время операции.
    
  - SUPPRESS_RECEIPT: Ожидающие чтения отчета должна быть отменена Если запрошен чтения отчета, и этот вызов изменяет состояние сообщения из непрочитанные сообщения для чтения. Если этот вызов не изменяет состояние сообщения, поставщик хранения сообщений можно игнорировать этот флаг.
    
## <a name="return-values"></a>Возвращаемые значения

S_OK 
  
> Чтение флаг для указанного сообщения или сообщения успешно задание или снят.
    
MAPI_E_NO_SUPPRESS 
  
> Поставщик хранения сообщения не поддерживает подавления чтения отчеты.
    
MAPI_E_INVALID_PARAMETER 
  
> Один из следующих комбинаций несовместимых флагов задано с помощью параметра _ulFlags_ : 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
MAPI_W_PARTIAL_COMPLETION 
  
> Вызов завершился успешно, но не все сообщения были успешно обработан. При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Замечания

Метод **IMAPIFolder::SetReadFlags** устанавливает или сбрасывает MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** одной или нескольких папок сообщений. Установка флага MSGFLAG_READ помечает сообщения как прочитанного, который не обязательно означает, что получателю фактически имеет чтение сообщения. 
  
Кроме того, **SetReadFlags** управляет Отправка просмотра отчетов. 
  
Чтение флаг нельзя изменить в следующих:
  
- Сообщения, не существует.
    
- Сообщения, которые были перемещены в другом месте.
    
- Сообщения, открытые с разрешением на чтение и запись.
    
- Сообщения, которые передаются в настоящее время.
    
## <a name="notes-to-implementers"></a>Примечания для реализующих

Можно указать, кто не поддерживает отправку чтения отчетов и запроса для отмены вывода чтения отчеты. Чтобы избежать подавления чтения отчета, возврата MAPI_E_NO_SUPPRESS при вызове **SetReadFlags** с SUPPRESS_RECEIPT задавать в параметре _ulFlags_ . 
  
Если параметр _lpMsgList_ указывает на более одного сообщения, как можно выполните операцию для каждого сообщения. Не останавливайте операции преждевременно Если произошла ошибка, которая находится за пределами элементу управления, такие как хватает памяти, недостаточно места на диске или повреждение в хранилище сообщений. 
  
Если ни один из флагов в параметре _ulFlags_ , применяются следующие правила: 
  
- Если MSGFLAG_READ уже задано, ничего не предпринимать.
    
- Если MSGFLAG_READ не установлен, установите его сразу же и отправить все ожидающие просмотра отчетов, если свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) имеет значение.
    
Если для флага SUPPRESS_RECEIPT, применяются следующие правила:
  
- Если MSGFLAG_READ уже задано, ничего не предпринимать. 
    
- Если MSGFLAG_READ не установлен, установите его и отменить ожидающие просмотра отчетов.
    
Если флаг CLEAR_READ_FLAG, снимите флаг MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** каждого сообщения и не отправлять чтения отчеты. 
  
Если для флага GENERATE_RECEIPT_ONLY, отправьте все ожидающие чтения отчеты. Выполните MSGFLAG_READ не установлен или clear.
  
Когда SUPPRESS_RECEIPT и GENERATE_RECEIPT_ONLY флаги, задайте **PR_READ_RECEIPT_REQUESTED** значение FALSE, если оно установлено и не отправлять просмотра отчета. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Ожидается, что эти возвращаемые значения в следующих случаях.
  
|**Условие**|**Возвращаемое значение**|
|:-----|:-----|
|**SetReadFlags** успешно обработал каждого сообщения.  <br/> |S_OK  <br/> |
|**SetReadFlags** не удалось успешно обработать каждого сообщения.  <br/> |MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND  <br/> |
|**SetReadFlags** не удалось завершить.  <br/> |Любое значение ошибки, за исключением MAPI_E_NOT_FOUND  <br/> |
   
При **SetReadFlags** не удается завершить, не предполагают, что работа не выполнена. **SetReadFlags** мог установить или сбросить флаг MSGFLAG_READ для одного или нескольких сообщений перед ошибок. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |Mfcmapi (en) использует метод **IMAPIFolder::SetReadFlags** Чтобы вручную задать состояние чтения на указанные сообщения.  <br/> |
   
## <a name="see-also"></a>См. также

- [ENTRYLIST](entrylist.md) 
- [IMessage::SetReadFlag](imessage-setreadflag.md)  
- [Каноническое свойство PidTagMessageFlags](pidtagmessageflags-canonical-property.md)  
- [Каноническое свойство PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)  
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
- [MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)  
- [Использование макросов для обработки ошибок](using-macros-for-error-handling.md)

