---
title: WrapStoreEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WrapStoreEntryID
api_type:
- HeaderDef
ms.assetid: b20107e3-5e23-4cde-9cd6-670c914ea70a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 45263396e69852a9ae17ff6fce284663bdf2fb07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585138"
---
# <a name="wrapstoreentryid"></a>WrapStoreEntryID

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Преобразует идентификатор внутренней записи хранилища сообщений в более удобный идентификатор записи системой обмена сообщениями. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
WrapStoreEntryID(
  ULONG ulFlags,
  LPSTR szDLLName,
  ULONG cbOrigEntry,
  LPENTRYID lpOrigEntry,
  ULONG * lpcbWrappedEntry,
  LPENTRYID * lppWrappedEntry
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Они в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI. 
    
 _szDLLName_
  
> [in] Имя поставщика хранилища сообщений DLL. 
    
 _cbOrigEntry_
  
> [in] Размер, в байтах, исходный идентификатор записи для хранилища сообщений. 
    
 _lpOrigEntry_
  
> [in] Указатель на структуру [ENTRYID](entryid.md) , которая содержит исходный идентификатор записи. 
    
 _lpcbWrappedEntry_
  
> [out] Указатель на размер, в байтах, новый идентификатор записи. 
    
 _lppWrappedEntry_
  
> [out] Указатель на указатель на структуру **ENTRYID** , который содержит новый идентификатор записи. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Замечания

Объект хранилища сообщений сохраняет внутренний запись идентификатора, который применяется только к coresident поставщики службы с помощью этого хранилища сообщений. Для других компонентов системы обмена сообщениями MAPI предоставляет оболочку версии идентификатор внутренняя запись HTML, которое распознается как принадлежат хранилища сообщений. Поставщики услуг coresident всегда должны быть заданы исходного развернуть хранилища запись идентификатор сообщения; клиентские приложения всегда должны быть предоставлены оболочку версии, которые затем можно использовать в любом месте в домене, обмена мгновенными сообщениями и в других доменах. 
  
Поставщик службы можно включить с помощью функции **WrapStoreEntryID** или метод [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) , который вызывает функцию **WrapStoreEntryID** идентификатор записи хранилища сообщений. Поставщик должен быть оболочкой идентификатор записи при предоставлении хранилища сообщений **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) свойства или записи в раздел профилей и при предоставлении **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) свойство. MAPI имеет идентификатор записи хранилища сообщений при ответе на вызов [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) . 
  
Если клиентское приложение передает идентификатор записи хранилища оболочку сообщения для MAPI, например в вызове [IMAPISession::OpenEntry](imapisession-openentry.md) MAPI распаковывает идентификатор записи перед его использованием для вызова метода поставщика, например [IMSProvider::Logon](imsprovider-logon.md) или [ IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md). 
  

