---
title: Ипроксистореобжектунврапнореф
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320155"
---
# <a name="iproxystoreobjectunwrapnoref"></a><span data-ttu-id="dea36-103">IProxyStoreObject::UnwrapNoRef</span><span class="sxs-lookup"><span data-stu-id="dea36-103">IProxyStoreObject::UnwrapNoRef</span></span>

  
  
<span data-ttu-id="dea36-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dea36-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dea36-105">Получает указатель на неупакованный объект хранилища протокола IMAP, который предоставляет доступ к основному файлу личных папок (PST), не вызывая синхронизацию и не загружая элементы.</span><span class="sxs-lookup"><span data-stu-id="dea36-105">Gets a pointer to an unwrapped Internet Message Access Protocol (IMAP) store object that provides access to the underlying Personal Folders file (PST) without invoking synchronization and downloading the items.</span></span>
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a><span data-ttu-id="dea36-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dea36-106">Parameters</span></span>

 <span data-ttu-id="dea36-107">_Ппвобжект_</span><span class="sxs-lookup"><span data-stu-id="dea36-107">_ppvObject_</span></span>
  
> <span data-ttu-id="dea36-108">вышли Указатель на объект [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) , который переключается в оболочку.</span><span class="sxs-lookup"><span data-stu-id="dea36-108">[out] Pointer to an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) store object that is unwrapped.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="dea36-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="dea36-109">Return values</span></span>

<span data-ttu-id="dea36-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="dea36-110">S_OK</span></span>
  
- <span data-ttu-id="dea36-111">Вызов выполнен успешно, и в _ппвобжект_возвращен указатель на неупакованный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="dea36-111">The call was successful and a pointer to an unwrapped interface has been returned in  _ppvObject_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dea36-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="dea36-112">Remarks</span></span>

<span data-ttu-id="dea36-113">Без предварительного развертывания хранилища IMAP доступ к сообщению в хранилище может вызвать принудительную синхронизацию, которая пытается скачать все сообщение.</span><span class="sxs-lookup"><span data-stu-id="dea36-113">Without first unwrapping an IMAP store, accessing a message in the store can force a synchronization that attempts to download the entire message.</span></span> <span data-ttu-id="dea36-114">Использование неупакованного хранилища позволяет получить доступ к сообщению в текущем состоянии, не запуская загрузку.</span><span class="sxs-lookup"><span data-stu-id="dea36-114">Using the unwrapped store allows access to the message in its current state without triggering a download.</span></span>
  
<span data-ttu-id="dea36-115">Так как **унврапнореф** не увеличивает значение счетчика ссылок для нового указателя на неупакованный объект Store после успешного вызова **унврапнореф**, необходимо вызвать метод [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) для поддержания счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="dea36-115">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you should call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) to maintain the reference count.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dea36-116">См. также</span><span class="sxs-lookup"><span data-stu-id="dea36-116">See also</span></span>



[<span data-ttu-id="dea36-117">IProxyStoreObject</span><span class="sxs-lookup"><span data-stu-id="dea36-117">IProxyStoreObject</span></span>](iproxystoreobject.md)

