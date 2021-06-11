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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Преобразует внутренний идентификатор входа в хранилище сообщений в идентификатор записи, который более угоден системе обмена сообщениями. 
  
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

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Bitmask флагов. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Строки находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI. 
    
 _szDLLName_
  
> [in] Имя поставщика DLL магазина сообщений. 
    
 _cbOrigEntry_
  
> [in] Размер в bytes исходного идентификатора записи для магазина сообщений. 
    
 _lpOrigEntry_
  
> [in] Указатель на [структуру ENTRYID,](entryid.md) которая содержит исходный идентификатор записи. 
    
 _lpcbWrappedEntry_
  
> [вышел] Указатель на размер в bytes нового идентификатора записи. 
    
 _lppWrappedEntry_
  
> [вышел] Указатель на указатель на **структуру ENTRYID,** которая содержит новый идентификатор записи. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Объект хранения сообщений сохраняет внутренний идентификатор записи, который имеет значение только для поставщиков услуг, в котором хранится сообщение. Для других компонентов обмена сообщениями MAPI поставляет завернутую версию внутреннего идентификатора записи, которая делает его узнаваемым как принадлежащий магазину сообщений. Поставщикам служб Coresident всегда должен быть предоставлен исходный идентификатор входа в хранилище сообщений. клиентские приложения всегда должны быть предоставлены завернутой версии, которая затем можно использовать в любом месте в домене обмена сообщениями и в других доменах. 
  
Поставщик служб может обернуть идентификатор входа в хранилище сообщений с помощью функции **WrapStoreEntryID** или [метода IMAPISupport::WrapStoreEntryID,](imapisupport-wrapstoreentryid.md) который вызывает функцию **WrapStoreEntryID.** Поставщик должен обернуть идентификатор записи при разоблачении свойства **PR_ENTRYID** магазина сообщений [(PidTagEntryId)](pidtagentryid-canonical-property.md)или записи его в профильный раздел, а также при разоблачении **свойства PR_STORE_ENTRYID** [(PidTagStoreEntryId).](pidtagstoreentryid-canonical-property.md) MAPI заворачивает идентификатор входа в хранилище сообщений при ответе на вызов [IMAPISession::OpenMsgStore.](imapisession-openmsgstore.md) 
  
Когда клиентская заявка передает идентификатор входа в хранилище сообщений в MAPI, например в [вызове IMAPISession::OpenEntry,](imapisession-openentry.md) MAPI развернет идентификатор записи, прежде чем использовать его для вызова метода поставщика, такого как [IMSProvider::Logon](imsprovider-logon.md) или [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md). 
  

