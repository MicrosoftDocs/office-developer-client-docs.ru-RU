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
ms.openlocfilehash: 47a62b331ff9f1c96576d42797ebb23ed61cd362
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416883"
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

## <a name="parameters"></a>Parameters

 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, который будет использоваться для доступа к адресной книге. Допустимые значения NULL, которые указывают стандартный интерфейс адресной книги [IAddrBook](iaddrbookimapiprop.md)и IID_IAddrBook.
    
 _ulFlags_
  
> Зарезервировано; должно быть нулевой.
    
 _lppAdrBook_
  
> [вышел] Указатель на указатель на адресную книгу.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Был предоставлен доступ к адресной книге.
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов удался, но один или несколько поставщиков адресной книги не удалось загрузить. Когда это предупреждение возвращается, вызов должен быть обработан как успешный. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::OpenAddressBook** реализован для всех объектов поддержки поставщика услуг. Поставщики услуг, как правило, тесно соединяемый магазин сообщений и поставщики транспорта, звонят **в OpenAddressBook,** чтобы получить доступ к адресной книге. Возвращенный указатель **IAddrBook** можно использовать для различных задач адресной книги, в том числе для открытия контейнеров адресной книги, поиска пользователей сообщений и отображения диалогов адресов. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **OpenAddressBook** может MAPI_W_ERRORS_RETURNED, если не может загрузить один или несколько поставщиков адресной книги в текущем профиле. Это значение является предупреждением, и вы должны относиться к вызову как к успешному. Даже если все поставщики адресных книг не загрузили, **OpenAddressBook** по-прежнему успешно MAPI_W_ERRORS_RETURNED и **указатель IAddrBook** в _параметре lppAdrBook._ Так **как OpenAddressBook** всегда возвращает допустимый указатель **IAddrBook,** его необходимо освободить по завершению использования. 
  
Если один или несколько поставщиков адресных книг не загрузили, позвоните по адресу [IMAPISupport::GetLastError,](imapisupport-getlasterror.md) чтобы получить структуру [MAPIERROR,](mapierror.md) которая содержит сведения о не загруженных поставщиках. 
  
## <a name="see-also"></a>См. также



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

