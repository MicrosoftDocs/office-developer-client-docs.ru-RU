---
title: IMsgStoreAbortSubmit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.AbortSubmit
api_type:
- COM
ms.assetid: 9be6b88e-2510-4b82-8b35-5f20a0f99fc0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1486730dfa2d76bf8e97439213851b195504962f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414384"
---
# <a name="imsgstoreabortsubmit"></a>IMsgStore::AbortSubmit

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Пытается удалить сообщение из исходя такой очереди.
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _cbEntryID_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи сообщения, удаляемого из исходяской очереди. 
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Сообщение успешно удалено из исходяной очереди.
    
MAPI_E_NOT_IN_QUEUE 
  
> Сообщение, определенное  _lpEntryID,_ больше не находится в очереди исходяющих сообщений, как правило, так как оно уже отправлено. 
    
MAPI_E_UNABLE_TO_ABORT 
  
> Сообщение, идентифицированное  _lpEntryID,_ заблокировано пулом MAPI, и операцию нельзя прерывать. 
    
## <a name="remarks"></a>Примечания

Метод **IMsgStore::AbortSubmit** пытается удалить отправленное сообщение из исходявой очереди хранилищ сообщений. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

После отправки сообщения единственным действием, которое может быть выполнено с сообщением, является прекращение отправки путем вызова **AbortSubmit.** Не **ожидайте, что abortSubmit** всегда будет успешным. В зависимости от того, как реализована система обмена сообщениями, отменить отправку сообщения может быть невозможно. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnAbortSubmit  <br/> |MFCMAPI использует метод **IMsgStore::AbortSubmit,** чтобы отменить отправку выбранного сообщения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

