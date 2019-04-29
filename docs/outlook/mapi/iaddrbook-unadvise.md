---
title: Иаддрбукунадвисе
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Unadvise
api_type:
- COM
ms.assetid: e0db9e86-9528-43de-b8ba-a5af8b7bda4b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2988f1fc149bbfc2d724b62b12bd12ae4f4664a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436155"
---
# <a name="iaddrbookunadvise"></a>IAddrBook::Unadvise

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
ОтМеняет регистрацию уведомления, установленную ранее для записи адресной книги.
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Параметры

 _Улконнектион_
  
> возврата Номер подключения, представляющий отмену регистрации. Параметр _улконнектион_ должен содержать значение, возвращенное при предыдущем вызове метода [IAddrBook:: Advise](iaddrbook-advise.md) . 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация успешно отменена.
    
## <a name="remarks"></a>Примечания

Клиенты вызывают метод **unadvise** для прекращения получения уведомлений об изменениях в определенной записи адресной книги. При отмене регистрации уведомления поставщик адресных книг освобождает свой указатель приемника уведомлений вызывающего абонента. Тем не менее, при вызове метода **unadvise** может произойти освобождение, если другой поток находится в процессе вызова метода [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) . При выполнении уведомления выпуск откладывается до тех пор, пока не **** будет возвращен метод OnNotify. 
  
## <a name="see-also"></a>См. также



[IAddrBook::Advise](iaddrbook-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

