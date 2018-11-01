---
title: IAddrBookUnadvise
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
ms.openlocfilehash: e06f78317a1e98d47a37cb7059042b254567fe8b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573686"
---
# <a name="iaddrbookunadvise"></a>IAddrBook::Unadvise

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Отмена регистрации уведомлений, ранее созданные записи адресной книги.
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Параметры

 _ulConnection_
  
> [in] Номер подключения, который представляет регистрации отменяется. Параметр _ulConnection_ должен содержать значение, возвращаемое во время предыдущего вызова метода [IAddrBook::Advise](iaddrbook-advise.md) . 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация успешно отменена.
    
## <a name="remarks"></a>Замечания

Клиенты вызовите метод **Unadvise** прекратить получение уведомлений об изменениях в записи определенного адресной книги. После отмены регистрации уведомлений адресная книга указатель вызывающего абонента уведомить выпусков поставщика приемника. Тем не менее выпуска могут возникнуть во время вызова **Unadvise** или позже, если другой поток находится в процессе вызова метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) . Если уведомление о ходе выполнения, выпуска откладывается до возвращения методом **OnNotify** . 
  
## <a name="see-also"></a>См. также



[IAddrBook::Advise](iaddrbook-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

