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
ms.openlocfilehash: a176b51577c7d4616d988a0b28f2afcfb554e9f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564985"
---
# <a name="imsgstoreabortsubmit"></a>IMsgStore::AbortSubmit

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Пытается удалить сообщения из очереди исходящих сообщений.
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _cbEntryID_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи сообщения для удаления из очереди исходящих сообщений. 
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Сообщение успешно удалено из исходящей очереди.
    
MAPI_E_NOT_IN_QUEUE 
  
> Сообщение, определяемую средством _lpEntryID_ больше не в хранилище сообщений исходящей очереди, как правило, так как он уже был отправлен. 
    
MAPI_E_UNABLE_TO_ABORT 
  
> Сообщение, определяемую средством _lpEntryID_ заблокирована диспетчером очереди MAPI, операция не может быть отменена. 
    
## <a name="remarks"></a>Замечания

Метод **IMsgStore::AbortSubmit** пытается удалить отправленное сообщение из очереди исходящих хранилища сообщений. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

После отправки сообщения прерывание подачи путем вызова **AbortSubmit** — это единственный действие, которое может выполняться в окне сообщения. Не ожидается **AbortSubmit** всегда выполняются успешно. В зависимости от того, как реализуется системы обмена сообщениями может оказаться невозможно отменить отправку сообщения. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnAbortSubmit  <br/> |Mfcmapi (en) использует метод **IMsgStore::AbortSubmit** для прекращения предоставления выбранного сообщения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

