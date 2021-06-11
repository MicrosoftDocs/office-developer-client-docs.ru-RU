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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Удаляет одно или несколько сообщений.
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpMsgList_
  
> [in] Указатель на структуру [ENTRYLIST,](entrylist.md) которая содержит количество удаляемого сообщения, и массив [структур ENTRYID,](entryid.md) которые идентифицируют сообщения. 
    
 _ulUIParam_
  
> [in] Ручка родительского окна индикатора прогресса. Параметр _ulUIParam_ игнорируется, если флаг MESSAGE_DIALOG в параметре _ulFlags._ 
    
 _lpProgress_
  
> [in] Указатель на объект progress, отображает индикатор прогресса. Если NULL передается в  _lpProgress,_ поставщик магазина сообщений отображает индикатор прогресса с помощью реализации объекта progress MAPI. Параметр _lpProgress_ игнорируется, если флаг MESSAGE_DIALOG в параметре _ulFlags._ 
    
 _ulFlags_
  
> [in] Немного флагов, которые контролируют удаление сообщений. Можно установить следующие флаги:
    
DELETE_HARD_DELETE
  
> Постоянно удаляет все сообщения, в том числе удаленные с мягкими сообщениями.
    
MESSAGE_DIALOG 
  
> Отображает индикатор прогресса по мере выполнения операции.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Указанное сообщение или сообщения были успешно удалены.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Вызов удался, но не все сообщения были успешно удалены. Когда это предупреждение возвращается, вызов должен быть обработан как успешный. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Примечания

Метод **IMAPIFolder::D eleteMessages** удаляет сообщения из папки. Сообщения, которые не существуют, которые были перемещены в другое место, открытые с разрешения чтения или записи или отправленные в настоящее время, не могут быть удалены. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если операция удаления включает несколько сообщений, выполните операцию как можно более полной для каждой папки, даже если одно или несколько сообщений невозможно удалить. Не останавливайте операцию преждевременно, если не произойдет сбой, неподконтрольный вам, например из-за потери памяти, потери дискового пространства или повреждения в хранилище сообщений.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Ожидайте этих значений возврата в следующих условиях.
  
|**Condition**|**Возвращаемое значение**|
|:-----|:-----|
|**DeleteMessages** успешно удалил каждое сообщение.  <br/> |S_OK  <br/> |
|**DeleteMessages** не удалось успешно удалить каждое сообщение и подмостки.  <br/> |MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND  <br/> |
|**DeleteMessages** не удалось выполнить.  <br/> |Любое значение ошибки, кроме MAPI_E_NOT_FOUND  <br/> |
   
Если **DeleteMessages** не удается выполнить, не думайте, что работы не было сделано. **DeleteMessages,** возможно, удалось удалить одно или несколько сообщений, прежде чем столкнуться с ошибкой. 
  
 **DeleteMessages** возвращает MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND в зависимости от реализации магазина сообщений. 
  
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

