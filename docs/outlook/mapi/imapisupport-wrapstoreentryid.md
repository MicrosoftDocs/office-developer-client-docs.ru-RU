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
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 25c04f8dee012f4985db98df7d1b3ae5536ef6b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809179"
---
# <a name="imapisupportwrapstoreentryid"></a>IMAPISupport::WrapStoreEntryID

  
  
**Применимо к**: Outlook 
  
Преобразует идентификатор внутренней записи хранилища сообщений идентификатор записи в стандартный формат MAPI.
  
```cpp
HRESULT WrapStoreEntryID(
ULONG cbOrigEntry,
LPENTRYID lpOrigEntry,
ULONG FAR * lpcbWrappedEntry,
LPENTRYID FAR * lppWrappedEntry
);
```

## <a name="parameters"></a>Parameters

 _cbOrigEntry_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpOrigEntry_ . 
    
 _lpOrigEntry_
  
> [in] Указатель на идентификатор частной запись для хранилища сообщений.
    
 _lpcbWrappedEntry_
  
> [out] Указатель на число байтов в идентификатор записи, на который указывает параметр _lppWrappedEntry_ . 
    
 _lppWrappedEntry_
  
> [out] Указатель на указатель на идентификатор оболочку записи.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Идентификатор записи успешно оболочку.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::WrapStoreEntryID** применяется для всех объектов поддержки поставщика службы. Поставщики услуг использовать **WrapStoreEntryID** для создающего запись идентификатор хранилища сообщений, которое имеет идентификатор внутренней записи хранилища MAPI. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Когда клиент вызывает метод [IMAPIProp::GetProps](imapiprop-getprops.md) хранилища сообщений для получения его свойство **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) и хранения сообщений используется идентификатор записи в виде частный, вызвать **WrapStoreEntryID **и возвращает идентификатор записи, на который указывает параметр _lppWrappedEntry_ . 
  
Вызовы методов [IMSProvider::Logon](imsprovider-logon.md) и [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) всегда получить идентификатор хранилища закрытый записи; Перенос версии используется только между клиентскими приложениями и MAPI. 
  
Освободите память для идентификатора запись указывает параметр _lppWrappedEntry_ с помощью функции [MAPIFreeBuffer](mapifreebuffer.md) после завершения с помощью идентификатор записи. 
  
## <a name="see-also"></a>См. также



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[IMSLogon::CompareEntryIDs](imslogon-compareentryids.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

