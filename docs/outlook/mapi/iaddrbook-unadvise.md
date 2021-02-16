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
ms.openlocfilehash: 2988f1fc149bbfc2d724b62b12bd12ae4f4664a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436155"
---
# <a name="iaddrbookunadvise"></a>IAddrBook::Unadvise

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Отменяет регистрацию уведомлений, ранее установленную для записи адресной книги.
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Параметры

 _ulConnection_
  
> [in] Номер подключения, который представляет регистрацию, которую необходимо отменить. Параметр _ulConnection_ должен содержать значение, возвращаемого при предыдущем вызове метода [IAddrBook::Advise.](iaddrbook-advise.md) 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация успешно отменена.
    
## <a name="remarks"></a>Примечания

Клиенты **звонят методу Unadvise,** чтобы прекратить получение уведомлений об изменениях определенной записи адресной книги. При отмене регистрации уведомления поставщик адресной книги отпускает указатель на сигнальный сигнал звонящего. Однако выпуск может произойти во время вызова **Unadvise** или позднее, если другой поток вызывает метод [IMAPIAdviseSink::OnNotify.](imapiadvisesink-onnotify.md) При уведомлении выпуск откладывается до тех пор, пока не будет возвращен метод **OnNotify.** 
  
## <a name="see-also"></a>См. также



[IAddrBook::Advise](iaddrbook-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

