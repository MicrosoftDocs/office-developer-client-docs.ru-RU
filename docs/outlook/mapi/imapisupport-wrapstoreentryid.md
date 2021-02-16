---
title: IMAPISupportWrapStoreEntryID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.WrapStoreEntryID
api_type:
- COM
ms.assetid: 923fb879-5f32-4fe2-8920-2ec17002256c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a623ef24f76dae93bfc13e6613e885a120f3278e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430450"
---
# <a name="imapisupportwrapstoreentryid"></a>IMAPISupport::WrapStoreEntryID

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Преобразует внутренний идентификатор записи в хранилище сообщений в идентификатор записи в стандартном формате MAPI.
  
```cpp
HRESULT WrapStoreEntryID(
ULONG cbOrigEntry,
LPENTRYID lpOrigEntry,
ULONG FAR * lpcbWrappedEntry,
LPENTRYID FAR * lppWrappedEntry
);
```

## <a name="parameters"></a>Параметры

 _cbOrigEntry_
  
> [in] Количество byte в идентификаторе записи, на который указывает параметр _lpOrigEntry._ 
    
 _lpOrigEntry_
  
> [in] Указатель на идентификатор закрытой записи для хранения сообщений.
    
 _lpcbWrappedEntry_
  
> [out] Указатель на количество byte в идентификаторе записи, на который указывает параметр _lppWrappedEntry._ 
    
 _lppWrappedEntry_
  
> [out] Указатель на указатель на идентификатор завернутой записи.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Идентификатор записи успешно упакован.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::WrapStoreEntryID реализован** для всех объектов поддержки поставщика услуг. Поставщики услуг используют **WrapStoreEntryID,** чтобы MAPI генерирул идентификатор записи для хранения сообщений, которое создает внутренний идентификатор записи в хранилище. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Когда клиент вызывает метод [IMAPIProp::GetProps](imapiprop-getprops.md) вашего магазина сообщений для получения его **свойства PR_STORE_ENTRYID** ([PidTagStoreEntryId),](pidtagstoreentryid-canonical-property.md)а хранилище сообщений использует идентификатор записи в частном формате, вызовите **WrapStoreEntryID** и верните идентификатор записи, на который указывает параметр _lppWrappedEntry._ 
  
Вызовы методов [IMSProvider::Logon](imsprovider-logon.md) и [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) всегда получают идентификатор закрытой записи магазина; Версия оболочки используется только между клиентские приложения и MAPI. 
  
Освободите память для идентификатора записи, на который указывает параметр  _lppWrappedEntry,_ с помощью функции [MAPIFreeBuffer](mapifreebuffer.md) после завершения использования идентификатора записи. 
  
## <a name="see-also"></a>См. также



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[IMSLogon::CompareEntryIDs](imslogon-compareentryids.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

