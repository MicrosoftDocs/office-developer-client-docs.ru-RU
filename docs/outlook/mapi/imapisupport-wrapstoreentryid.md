---
title: Имаписуппортврапсторинтрид
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341288"
---
# <a name="imapisupportwrapstoreentryid"></a>IMAPISupport::WrapStoreEntryID

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Преобразует внутренний идентификатор записи банка сообщений в идентификатор записи в стандартном формате MAPI.
  
```cpp
HRESULT WrapStoreEntryID(
ULONG cbOrigEntry,
LPENTRYID lpOrigEntry,
ULONG FAR * lpcbWrappedEntry,
LPENTRYID FAR * lppWrappedEntry
);
```

## <a name="parameters"></a>Параметры

 _Кборижентри_
  
> возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпорижентри_ . 
    
 _Лпорижентри_
  
> возврата Указатель на идентификатор частной записи для хранилища сообщений.
    
 _Лпкбвраппедентри_
  
> вышли Указатель на число байтов в идентификаторе записи, на который указывает параметр _лппвраппедентри_ . 
    
 _Лппвраппедентри_
  
> вышли Указатель на указатель на идентификатор заключенной в оболочку записи.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Идентификатор записи успешно заключен в оболочку.
    
## <a name="remarks"></a>Комментарии

Метод **имаписуппорт:: врапсторинтрид** реализован для всех объектов поддержки поставщика услуг. Поставщики услуг используют **врапсторинтрид** для создания идентификатора записи для хранилища сообщений, который создает оболочку для внутреннего идентификатора записи хранилища. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Когда клиент вызывает метод [IMAPIProp::](imapiprop-getprops.md) -PROPS хранилища сообщений для получения свойства **пр_сторе_ентрид** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)), а хранилище сообщений использует идентификатор записи в частном формате, вызывает **врапсторинтрид **и возвратить идентификатор записи, на который указывает параметр _лппвраппедентри_ . 
  
Вызовы методов [функцииimsprovider:: logon](imsprovider-logon.md) и [Имслогон:: метод compareentryids](imslogon-compareentryids.md) всегда получают личный идентификатор записи хранилища; Упакованная версия используется только между клиентскими приложениями и MAPI. 
  
Освободите память для идентификатора записи, на которую указывает параметр _лппвраппедентри_ , с помощью функции [мапифрибуффер](mapifreebuffer.md) по завершении использования идентификатора записи. 
  
## <a name="see-also"></a>См. также



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[IMSLogon::CompareEntryIDs](imslogon-compareentryids.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

