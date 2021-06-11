---
title: Доступ к сообщению в хранилище IMAP без скачивания всего сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2a93ab3e-798f-5741-d5e0-bba8c6b437c7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 194131148cc36dfff791b4cfae01862e8bbef5cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299078"
---
# <a name="access-a-message-on-an-imap-store-without-downloading-the-entire-message"></a>Доступ к сообщению в хранилище IMAP без скачивания всего сообщения

**Область применения**: Outlook 2013 | Outlook 2016 
  
В этом разделе показан пример кода в C++, который запрашивает хранилище сообщений для интерфейса **[IProxyStoreObject](iproxystoreobject.md)** и использует возвращенный указатель и функцию **[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md)** для получения указателя на объект магазина IMAP, который был развернут. Использование этого разверзванного магазина позволяет получить доступ к сообщению в текущем состоянии, не названив загрузку всего сообщения. 
  
Так как **UnwrapNoRef** не добавляет количество ссылок для этого нового указателя на объект незавержденного магазина, после успешного вызова **UnwrapNoRef** необходимо вызвать [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) для поддержания эталонного подсчета. 
  
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


