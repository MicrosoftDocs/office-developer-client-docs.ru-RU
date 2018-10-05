---
title: Доступ к сообщению в хранилище IMAP без загрузки всего сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2a93ab3e-798f-5741-d5e0-bba8c6b437c7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 194131148cc36dfff791b4cfae01862e8bbef5cb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398446"
---
# <a name="access-a-message-on-an-imap-store-without-downloading-the-entire-message"></a>Доступ к сообщению в хранилище IMAP без загрузки всего сообщения

**Относится к**: Outlook 2013 | Outlook 2016 
  
В этом разделе приводится пример кода c++, который запрашивает хранилищем сообщений для интерфейса **[IProxyStoreObject](iproxystoreobject.md)** и использует возвращенный указатель и функцию **[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md)** для получения указателя на объект хранилища IMAP, которое было развернуть. С помощью этой зоны хранения позволяет получить доступ к сообщению в ее текущем состоянии без вызова для загрузки всего сообщения. 
  
Так как **UnwrapNoRef** не увеличивает счетчик ссылок для этого нового указателя на объект оболочку хранилище после успешного вызова **UnwrapNoRef**, необходимо вызвать [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) на обслуживание счетчик ссылок. 
  
```cpp
HRESULT HrUnWrapMDB(LPMDB lpMDBIn, LPMDB* lppMDBOut) 
{ 
    HRESULT hRes = S_OK; 
    IProxyStoreObject* lpProxyObj = NULL; 
    LPMDB lpUnwrappedMDB = NULL; 
    hRes = lpMDBIn->QueryInterface(IID_IProxyStoreObject,(void**)&lpProxyObj); 
    if (SUCCEEDED(hRes) && lpProxyObj) 
    { 
        hRes = lpProxyObj->UnwrapNoRef((LPVOID*)&lpUnwrappedMDB); 
        if (SUCCEEDED(hRes) && lpUnwrappedMDB) 
        { 
            // UnwrapNoRef doesn't addref, so do it here 
            lpUnwrappedMDB->AddRef(); 
            (*lppMDBOut) = lpUnwrappedMDB; 
        } 
    } 
    if (lpProxyObj) lpProxyObj->Release(); 
    return hRes; 
}
```


