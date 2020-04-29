---
title: имаписуппортопенаддрессбук
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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к адресной книге.
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a>Параметры

 _лпинтерфаце_
  
> возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к адресной книге. Допустимые значения: NULL, указывающие на стандартную адресную книгу [IAddrBook](iaddrbookimapiprop.md)и IID_IAddrBook.
    
 _ulFlags_
  
> Резервирования должно быть равно нулю.
    
 _лппадрбук_
  
> вышли Указатель на указатель на адресную книгу.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Предоставлен доступ к адресной книге.
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов выполнен успешно, но не удалось загрузить одного или нескольких поставщиков адресных книг. При возвращении этого предупреждения вызов должен обрабатываться как успешный. Чтобы проверить это предупреждение, используйте макрос **HR_FAILED** . Дополнительные сведения см. [в разделе Использование макросов для обработки ошибок](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Примечания

Метод **имаписуппорт:: опенаддрессбук** реализован для всех объектов поддержки поставщика услуг. Поставщики услуг, обычно тесно связанные с хранилищем сообщений и поставщиками транспорта, вызывают **опенаддрессбук** , чтобы получить доступ к адресной книге. Возвращенный указатель **IAddrBook** можно использовать для различных задач адресной книги, включая открытие контейнеров адресных книг, Поиск пользователей обмена сообщениями и отображение диалоговых окон адресов. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **Опенаддрессбук** могут возвращать MAPI_W_ERRORS_RETURNED, если не удается загрузить одного или нескольких поставщиков адресной книги в текущем профиле. Это значение является предупреждением, и вы должны считать вызов успешным. Даже если не удалось загрузить все поставщики адресных книг, **опенаддрессбук** по-прежнему завершается успешно, возвращается MAPI_W_ERRORS_RETURNED и указатель **IAddrBook** в параметре _лппадрбук_ . Так как **опенаддрессбук** всегда возвращает допустимый указатель **IAddrBook** , его необходимо освободить после завершения использования. 
  
Если одному или нескольким поставщикам адресных книг не удалось загрузить, вызовите метод [имаписуппорт:: GetLastError](imapisupport-getlasterror.md) , чтобы получить структуру [мапиеррор](mapierror.md) , содержащую сведения о незагруженных поставщиках. 
  
## <a name="see-also"></a>См. также



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

