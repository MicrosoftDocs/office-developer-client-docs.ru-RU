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
ms.openlocfilehash: e797a80cf8659baa7ca935f94b3ab65c200530a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409211"
---
# <a name="wrapstoreentryid"></a>WrapStoreEntryID

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Преобразует внутренний идентификатор записи в хранилище сообщений в идентификатор записи, который может использовать система обмена сообщениями. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
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

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Строки имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI. 
    
 _szDLLName_
  
> [in] Имя DLL поставщика хранения сообщений. 
    
 _cbOrigEntry_
  
> [in] Размер (в bytes) исходного идентификатора записи для хранения сообщений. 
    
 _lpOrigEntry_
  
> [in] Указатель на [структуру ENTRYID,](entryid.md) которая содержит исходный идентификатор записи. 
    
 _lpcbWrappedEntry_
  
> [out] Указатель на размер нового идентификатора записи (в bytes). 
    
 _lppWrappedEntry_
  
> [out] Указатель на указатель на структуру **ENTRYID,** которая содержит новый идентификатор записи. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Объект хранения сообщений сохраняет внутренний идентификатор записи, который имеет смысл только для поставщиков услуг, которые его не содержат. Для других компонентов обмена сообщениями MAPI передает упакованную версию идентификатора внутренней записи, которая делает его узнаваемым, так как он принадлежит хранилищем сообщений. Поставщикам служб Coresident всегда должен быть предоставлен исходный идентификатор записи в хранилище сообщений без перехваченных данных; клиентские приложения всегда должны иметь завернутую версию, которую можно использовать в любом месте домена обмена сообщениями и в других доменах. 
  
Поставщик службы может обтекать идентификатор записи в хранилище сообщений с помощью функции **WrapStoreEntryID** или метода [IMAPISupport::WrapStoreEntryID,](imapisupport-wrapstoreentryid.md) который вызывает функцию **WrapStoreEntryID.** Поставщик должен обтекать идентификатор записи при отобралении свойства **PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)в хранилище сообщений или его записи в раздел профиля, а также при отобралении свойства **PR_STORE_ENTRYID** ([PidTagStoreEntryId).](pidtagstoreentryid-canonical-property.md) MAPI обтекает идентификатор записи в хранилище сообщений при ответе на вызов [IMAPISession::OpenMsgStore.](imapisession-openmsgstore.md) 
  
Когда клиентские приложения передает идентификатор записи в хранилище упакованных сообщений MAPI, например в [вызове IMAPISession::OpenEntry,](imapisession-openentry.md) MAPI unwraps the entry identifier before using it to call a provider method such as [IMSProvider::Logon](imsprovider-logon.md) or [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md). 
  

