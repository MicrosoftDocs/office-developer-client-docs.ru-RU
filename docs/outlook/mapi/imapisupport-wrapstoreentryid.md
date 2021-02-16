---
title: IMAPISupportWrapStoreEntryID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.WrapStoreEntryID
api_type:
- COM
ms.assetid: 923fb879-5f32-4fe2-8920-2ec17002256c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a623ef24f76dae93bfc13e6613e885a120f3278e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430450"
---
# <a name="imapisupportwrapstoreentryid"></a><span data-ttu-id="8d3a1-103">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="8d3a1-103">IMAPISupport::WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="8d3a1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d3a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d3a1-105">Преобразует внутренний идентификатор записи в хранилище сообщений в идентификатор записи в стандартном формате MAPI.</span><span class="sxs-lookup"><span data-stu-id="8d3a1-105">Converts a message store's internal entry identifier to an entry identifier in the MAPI standard format.</span></span>
  
```cpp
HRESULT WrapStoreEntryID(
ULONG cbOrigEntry,
LPENTRYID lpOrigEntry,
ULONG FAR * lpcbWrappedEntry,
LPENTRYID FAR * lppWrappedEntry
);
```

## <a name="parameters"></a><span data-ttu-id="8d3a1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d3a1-106">Parameters</span></span>

 <span data-ttu-id="8d3a1-107">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="8d3a1-107">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="8d3a1-108">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpOrigEntry._</span><span class="sxs-lookup"><span data-stu-id="8d3a1-108">[in] The byte count in the entry identifier pointed to by the  _lpOrigEntry_ parameter.</span></span> 
    
 <span data-ttu-id="8d3a1-109">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="8d3a1-109">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="8d3a1-110">[in] Указатель на идентификатор закрытой записи для хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="8d3a1-110">[in] A pointer to the private entry identifier for the message store.</span></span>
    
 <span data-ttu-id="8d3a1-111">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="8d3a1-111">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="8d3a1-112">[out] Указатель на количество byte в идентификаторе записи, на который указывает параметр _lppWrappedEntry._</span><span class="sxs-lookup"><span data-stu-id="8d3a1-112">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
    
 <span data-ttu-id="8d3a1-113">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="8d3a1-113">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="8d3a1-114">[out] Указатель на указатель на идентификатор завернутой записи.</span><span class="sxs-lookup"><span data-stu-id="8d3a1-114">[out] A pointer to a pointer to the wrapped entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8d3a1-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d3a1-115">Return value</span></span>

<span data-ttu-id="8d3a1-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="8d3a1-116">S_OK</span></span> 
  
> <span data-ttu-id="8d3a1-117">Идентификатор записи успешно упакован.</span><span class="sxs-lookup"><span data-stu-id="8d3a1-117">The entry identifier was successfully wrapped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8d3a1-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="8d3a1-118">Remarks</span></span>

<span data-ttu-id="8d3a1-119">Метод **IMAPISupport::WrapStoreEntryID реализован** для всех объектов поддержки поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="8d3a1-119">The **IMAPISupport::WrapStoreEntryID** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="8d3a1-120">Поставщики услуг используют **WrapStoreEntryID,** чтобы MAPI генерирул идентификатор записи для хранения сообщений, которое создает внутренний идентификатор записи в хранилище.</span><span class="sxs-lookup"><span data-stu-id="8d3a1-120">Service providers use **WrapStoreEntryID** to have MAPI generate an entry identifier for a message store that wraps the store's internal entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8d3a1-121">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="8d3a1-121">Notes to callers</span></span>

<span data-ttu-id="8d3a1-122">Когда клиент вызывает метод [IMAPIProp::GetProps](imapiprop-getprops.md) вашего магазина сообщений для получения его **свойства PR_STORE_ENTRYID** ([PidTagStoreEntryId),](pidtagstoreentryid-canonical-property.md)а хранилище сообщений использует идентификатор записи в частном формате, вызовите **WrapStoreEntryID** и верните идентификатор записи, на который указывает параметр _lppWrappedEntry._</span><span class="sxs-lookup"><span data-stu-id="8d3a1-122">When a client calls your message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property, and your message store uses an entry identifier in a private format, call **WrapStoreEntryID** and return the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
  
<span data-ttu-id="8d3a1-123">Вызовы методов [IMSProvider::Logon](imsprovider-logon.md) и [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) всегда получают идентификатор закрытой записи магазина; Версия оболочки используется только между клиентские приложения и MAPI.</span><span class="sxs-lookup"><span data-stu-id="8d3a1-123">Calls to the [IMSProvider::Logon](imsprovider-logon.md) and [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) methods always obtain the store's private entry identifier; the wrapped version is used only between client applications and MAPI.</span></span> 
  
<span data-ttu-id="8d3a1-124">Освободите память для идентификатора записи, на который указывает параметр  _lppWrappedEntry,_ с помощью функции [MAPIFreeBuffer](mapifreebuffer.md) после завершения использования идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="8d3a1-124">Free the memory for the entry identifier pointed to by the  _lppWrappedEntry_ parameter by using the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished using the entry identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8d3a1-125">См. также</span><span class="sxs-lookup"><span data-stu-id="8d3a1-125">See also</span></span>



[<span data-ttu-id="8d3a1-126">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="8d3a1-126">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="8d3a1-127">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="8d3a1-127">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="8d3a1-128">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="8d3a1-128">IMSLogon::CompareEntryIDs</span></span>](imslogon-compareentryids.md)
  
[<span data-ttu-id="8d3a1-129">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="8d3a1-129">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="8d3a1-130">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="8d3a1-130">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="8d3a1-131">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8d3a1-131">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

