---
title: IProxyStoreObjectUnwrapNoRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject.UnwrapNoRef
api_type:
- COM
ms.assetid: 1122b6e0-e7e1-e68a-e090-435777343d04
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ef9f506c1a95fec86c7f092b0299198e6149d3ba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382934"
---
# <a name="iproxystoreobjectunwrapnoref"></a><span data-ttu-id="26f6b-103">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="26f6b-103">IProxyStoreObject::UnwrapNoRef</span></span>

  
  
<span data-ttu-id="26f6b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26f6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26f6b-105">Получает указатель на развернутый объект хранилища протокола доступа сообщения Интернета (IMAP), который предоставляет доступ к базовым файл личных папок (PST) без вызова синхронизации и загрузку элементов.</span><span class="sxs-lookup"><span data-stu-id="26f6b-105">Gets a pointer to an unwrapped Internet Message Access Protocol (IMAP) store object that provides access to the underlying Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a><span data-ttu-id="26f6b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="26f6b-106">Parameters</span></span>

 <span data-ttu-id="26f6b-107">_ppvObject_</span><span class="sxs-lookup"><span data-stu-id="26f6b-107">_ppvObject_</span></span>
  
> <span data-ttu-id="26f6b-108">[out] Указатель на [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) объекта хранилища, который является оболочку.</span><span class="sxs-lookup"><span data-stu-id="26f6b-108">[out] Pointer to an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) store object that is unwrapped.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="26f6b-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="26f6b-109">Return values</span></span>

<span data-ttu-id="26f6b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="26f6b-110">S_OK</span></span>
  
- <span data-ttu-id="26f6b-111">Вызов прошла успешно и возврата указатель на интерфейс развернуть в _ppvObject_.</span><span class="sxs-lookup"><span data-stu-id="26f6b-111">The call was successful and a pointer to an unwrapped interface has been returned in  _ppvObject_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="26f6b-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="26f6b-112">Remarks</span></span>

<span data-ttu-id="26f6b-113">Без первого развертывания хранилище IMAP, доступ к сообщению в хранилище можно принудительно синхронизации, который пытается загрузить сообщение целиком.</span><span class="sxs-lookup"><span data-stu-id="26f6b-113">Without first unwrapping an IMAP store, accessing a message in the store can force a synchronization that attempts to download the entire message.</span></span> <span data-ttu-id="26f6b-114">С помощью оболочку store позволяет получить доступ к сообщению в ее текущем состоянии без активации для загрузки.</span><span class="sxs-lookup"><span data-stu-id="26f6b-114">Using the unwrapped store allows access to the message in its current state without triggering a download.</span></span>
  
<span data-ttu-id="26f6b-115">Так как **UnwrapNoRef** не увеличивает счетчик ссылок для этого нового указателя на объект оболочку хранилище после успешного вызова **UnwrapNoRef**, должны вызывать [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) для поддержки счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="26f6b-115">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="26f6b-116">См. также</span><span class="sxs-lookup"><span data-stu-id="26f6b-116">See also</span></span>



[<span data-ttu-id="26f6b-117">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="26f6b-117">IProxyStoreObject</span></span>](iproxystoreobject.md)

