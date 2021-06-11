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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Попытки удалить сообщение из исходятой очереди.
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи сообщения, удаляемого из исходятой очереди. 
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Сообщение было успешно удалено из исходятой очереди.
    
MAPI_E_NOT_IN_QUEUE 
  
> Сообщение, идентифицированное  _lpEntryID,_ больше не находится в исходя из очереди магазина сообщений, как правило, потому, что оно уже отправлено. 
    
MAPI_E_UNABLE_TO_ABORT 
  
> Сообщение, идентифицированное  _lpEntryID,_ заблокировано пулером MAPI, и операция не может быть прервана. 
    
## <a name="remarks"></a>Примечания

Метод **IMsgStore::AbortSubmit** пытается удалить отправленное сообщение из исходявой очереди магазина сообщений. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

После отправки сообщения прерывание отправки по вызову **AbortSubmit** является единственным действием, которое может быть выполнено в сообщении. Не **ожидайте, что AbortSubmit** всегда будет успешной. В зависимости от того, как реализована система обмена сообщениями, отмена отправки сообщения может оказаться невозможной. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnAbortSubmit  <br/> |MFCMAPI использует **метод IMsgStore::AbortSubmit,** чтобы прервать отправку выбранного сообщения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

