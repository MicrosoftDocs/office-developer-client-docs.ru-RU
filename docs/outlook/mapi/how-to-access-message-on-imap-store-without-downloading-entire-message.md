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
# <a name="access-a-message-on-an-imap-store-without-downloading-the-entire-message"></a><span data-ttu-id="12846-103">Доступ к сообщению в хранилище IMAP без скачивания всего сообщения</span><span class="sxs-lookup"><span data-stu-id="12846-103">Access a message on an IMAP store without downloading the entire message</span></span>

<span data-ttu-id="12846-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12846-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12846-105">В этом разделе показан пример кода на C++, который запрашивает хранилище сообщений для интерфейса **[IProxyStoreObject](iproxystoreobject.md)** и использует возвращенный указатель и функцию **[IProxyStoreObject::UnwrapNoRef,](iproxystoreobject-unwrapnoref.md)** чтобы получить указатель на объект хранения IMAP, который был разобран.</span><span class="sxs-lookup"><span data-stu-id="12846-105">This topic shows a code sample in C++ that queries a message store for the **[IProxyStoreObject](iproxystoreobject.md)** interface, and uses the returned pointer and the **[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md)** function to obtain a pointer to an IMAP store object that has been unwrapped.</span></span> <span data-ttu-id="12846-106">Использование этого неподдерживаемого хранения позволяет получить доступ к сообщению в текущем состоянии, не внося при этом скачивание всего сообщения.</span><span class="sxs-lookup"><span data-stu-id="12846-106">Using this unwrapped store allows access to a message in its current state without invoking a download of the entire message.</span></span> 
  
<span data-ttu-id="12846-107">Поскольку **UnwrapNoRef** не добавит количество ссылок для этого нового указателя на объект неподтвержденного хранения, после успешного вызова **UnwrapNoRef** необходимо вызвать [IUnknown::AddRef,](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) чтобы сохранить количество ссылок.</span><span class="sxs-lookup"><span data-stu-id="12846-107">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you must call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) to maintain the reference count.</span></span> 
  
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


