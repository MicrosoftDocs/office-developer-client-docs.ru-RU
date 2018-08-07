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
ms.openlocfilehash: 7c6c763e918947c423c5dae283b0d4ab2f880616
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809528"
---
# <a name="iproxystoreobjectunwrapnoref"></a><span data-ttu-id="6293a-103">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="6293a-103">IProxyStoreObject::UnwrapNoRef</span></span>

  
  
<span data-ttu-id="6293a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6293a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6293a-105">Получает указатель на развернутый объект хранилища протокола доступа сообщения Интернета (IMAP), который предоставляет доступ к базовым файл личных папок (PST) без вызова синхронизации и загрузку элементов.</span><span class="sxs-lookup"><span data-stu-id="6293a-105">Gets a pointer to an unwrapped Internet Message Access Protocol (IMAP) store object that provides access to the underlying Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a><span data-ttu-id="6293a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6293a-106">Parameters</span></span>

 <span data-ttu-id="6293a-107">_ppvObject_</span><span class="sxs-lookup"><span data-stu-id="6293a-107">_ppvObject_</span></span>
  
> <span data-ttu-id="6293a-108">[out] Указатель на [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) объекта хранилища, который является оболочку.</span><span class="sxs-lookup"><span data-stu-id="6293a-108">[out] Pointer to an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) store object that is unwrapped.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="6293a-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="6293a-109">Return values</span></span>

<span data-ttu-id="6293a-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="6293a-110">S_OK</span></span>
  
- <span data-ttu-id="6293a-111">Вызов прошла успешно и возврата указатель на интерфейс развернуть в _ppvObject_.</span><span class="sxs-lookup"><span data-stu-id="6293a-111">The call was successful and a pointer to an unwrapped interface has been returned in  _ppvObject_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6293a-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="6293a-112">Remarks</span></span>

<span data-ttu-id="6293a-113">Без первого развертывания хранилище IMAP, доступ к сообщению в хранилище можно принудительно синхронизации, который пытается загрузить сообщение целиком.</span><span class="sxs-lookup"><span data-stu-id="6293a-113">Without first unwrapping an IMAP store, accessing a message in the store can force a synchronization that attempts to download the entire message.</span></span> <span data-ttu-id="6293a-114">С помощью оболочку store позволяет получить доступ к сообщению в ее текущем состоянии без активации для загрузки.</span><span class="sxs-lookup"><span data-stu-id="6293a-114">Using the unwrapped store allows access to the message in its current state without triggering a download.</span></span>
  
<span data-ttu-id="6293a-115">Так как **UnwrapNoRef** не увеличивает счетчик ссылок для этого нового указателя на объект оболочку хранилище после успешного вызова **UnwrapNoRef**, должны вызывать [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) для поддержки счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="6293a-115">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6293a-116">См. также</span><span class="sxs-lookup"><span data-stu-id="6293a-116">See also</span></span>



[<span data-ttu-id="6293a-117">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="6293a-117">IProxyStoreObject</span></span>](iproxystoreobject.md)

