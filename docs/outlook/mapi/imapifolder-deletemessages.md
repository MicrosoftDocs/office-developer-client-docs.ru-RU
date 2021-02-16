---
title: IMAPIFolderDeleteMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteMessages
api_type:
- COM
ms.assetid: 5a16e62b-9d33-41cd-af2b-9abd403b6f2e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0f0523c01e163b57d9ed37d9b324ec858adbd685
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426074"
---
# <a name="imapifolderdeletemessages"></a>IMAPIFolder::DeleteMessages

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Удаляет одно или несколько сообщений.
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpMsgList_
  
> [in] Указатель на структуру [ENTRYLIST,](entrylist.md) которая содержит количество удаляемого сообщения, и массив структур [ENTRYID,](entryid.md) идентифицирует сообщения. 
    
 _ulUIParam_
  
> [in] Handle to the parent window of the progress indicator. Параметр _ulUIParam_ игнорируется, если MESSAGE_DIALOG флага в параметре _ulFlags._ 
    
 _lpProgress_
  
> [in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения. Если в  _lpProgress_ передается NULL, поставщик хранилище сообщений отображает индикатор хода выполнения с помощью реализации объекта хода выполнения MAPI. Параметр _lpProgress_ игнорируется, если MESSAGE_DIALOG флага в параметре _ulFlags._ 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет удалением сообщений. Можно установить следующие флаги:
    
DELETE_HARD_DELETE
  
> Окончательно удаляет все сообщения, включая сообщения, удаленные с удалением.
    
MESSAGE_DIALOG 
  
> Отображает индикатор хода выполнения операции.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Указанное сообщение или сообщения были успешно удалены.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Вызов был успешным, но не все сообщения были успешно удалены. При возвращении этого предупреждения вызов должен быть обработан как успешный. Чтобы проверить это предупреждение, используйте **макрос HR_FAILED.** Дополнительные сведения см. в [теме "Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Примечания

Метод **IMAPIFolder::D eleteMessages** удаляет сообщения из папки. Сообщения, которые не существуют, перемещены в другое место, открытые с разрешением на чтение и записи или отправленные в данный момент, не могут быть удалены. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если операция удаления включает несколько сообщений, выполните операцию для каждой папки максимально возможно, даже если одно или несколько сообщений не могут быть удалены. Не останавливайте операцию раньше времени, если не произойдет сбой, который находится вне вашего контроля, например, если недостаточно памяти, недостаточно места на диске или не будет повреждения в хранилище сообщений.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Эти возвращаемые значения следует ожидать при следующих условиях.
  
|**Condition**|**Возвращаемое значение**|
|:-----|:-----|
|**DeleteMessages** успешно удалил каждое сообщение.  <br/> |S_OK  <br/> |
|**DeleteMessages** не удалось успешно удалить все сообщения и в подкамеру.  <br/> |MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND  <br/> |
|**DeleteMessages** не удалось завершить.  <br/> |Любое значение ошибки, кроме MAPI_E_NOT_FOUND  <br/> |
   
Если **deleteMessages** не удается завершить, не предполагайте, что никаких работ не было сделано. **Возможно, deleteMessages** удалось удалить одно или несколько сообщений, прежде чем столкнуться с ошибкой. 
  
 **DeleteMessages** MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND в зависимости от реализации реализации в хранилище сообщений. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnDeleteSelectedItem  <br/> |MFCMAPI использует метод **IMAPIFolder::D eleteMessages** для удаления указанных сообщений.  <br/> |
   
## <a name="see-also"></a>См. также



[ENTRYID](entryid.md)
  
[ENTRYLIST](entrylist.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Использование макроса для обработки ошибок](using-macros-for-error-handling.md)

