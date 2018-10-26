---
title: IMAPISupportOpenAddressBook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenAddressBook
api_type:
- COM
ms.assetid: d8da8be1-3efe-410a-bcce-49e522602d80
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 26550691ef959fa7cefa83827dd1391538bd2d38
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588176"
---
# <a name="imapisupportopenaddressbook"></a>IMAPISupport::OpenAddressBook

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к адресной книге.
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a>Параметры

 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к адресной книге. Допустимые значения: NULL, которое указывает стандартный адресной книги интерфейс [IAddrBook](iaddrbookimapiprop.md)и IID_IAddrBook.
    
 _ulFlags_
  
> Зарезервировано; должно быть равно нулю.
    
 _lppAdrBook_
  
> [out] Указатель на указатель в адресной книге.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Был предоставлен доступ к адресной книге.
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов завершился успешно, но не удалось загрузить один или несколько поставщиками адресной книги. При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::OpenAddressBook** применяется для всех объектов поддержки поставщика службы. Поставщики услуг, обычно тесно связанных сообщений хранилища и поставщиками транспорта, вызовите **OpenAddressBook** , чтобы получить доступ к адресной книге. Возвращенный указатель **IAddrBook** можно использовать для различных задач адресной книги, включая Открытие адресной книги контейнеров, поиск пользователей обмена мгновенными сообщениями и отображение диалоговых окон адрес. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **OpenAddressBook** может вернуть MAPI_W_ERRORS_RETURNED, если не удается загрузить один или несколько поставщиками адресной книги в текущий профиль. Это значение — предупреждения и вызова следует рассматривать как успешно. Даже в том случае, если все поставщиками адресной книги не удалось загрузить, **OpenAddressBook** по-прежнему завершается успешно, возвращая MAPI_W_ERRORS_RETURNED и указатель **IAddrBook** с помощью параметра _lppAdrBook_ . Так как **OpenAddressBook** всегда возвращает указатель на допустимый **IAddrBook** , необходимо удалить после завершения с помощью его. 
  
Если не удалось загрузить один или несколько поставщиками адресной книги, вызовите [IMAPISupport::GetLastError](imapisupport-getlasterror.md) для получения [MAPIERROR](mapierror.md) структура, содержащая сведения о поставщиках, которые не были загружены. 
  
## <a name="see-also"></a>См. также



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

