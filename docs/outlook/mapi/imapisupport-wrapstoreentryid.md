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
# <a name="imapisupportwrapstoreentryid"></a><span data-ttu-id="371d0-103">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="371d0-103">IMAPISupport::WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="371d0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="371d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="371d0-105">Преобразует внутренний идентификатор входа в хранилище сообщений в идентификатор записи в стандартном формате MAPI.</span><span class="sxs-lookup"><span data-stu-id="371d0-105">Converts a message store's internal entry identifier to an entry identifier in the MAPI standard format.</span></span>
  
```cpp
HRESULT WrapStoreEntryID(
ULONG cbOrigEntry,
LPENTRYID lpOrigEntry,
ULONG FAR * lpcbWrappedEntry,
LPENTRYID FAR * lppWrappedEntry
);
```

## <a name="parameters"></a><span data-ttu-id="371d0-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="371d0-106">Parameters</span></span>

 <span data-ttu-id="371d0-107">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="371d0-107">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="371d0-108">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpOrigEntry._</span><span class="sxs-lookup"><span data-stu-id="371d0-108">[in] The byte count in the entry identifier pointed to by the  _lpOrigEntry_ parameter.</span></span> 
    
 <span data-ttu-id="371d0-109">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="371d0-109">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="371d0-110">[in] Указатель на идентификатор закрытой записи для магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="371d0-110">[in] A pointer to the private entry identifier for the message store.</span></span>
    
 <span data-ttu-id="371d0-111">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="371d0-111">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="371d0-112">[вышел] Указатель на количество byte в идентификаторе записи, на который указывает параметр _lppWrappedEntry._</span><span class="sxs-lookup"><span data-stu-id="371d0-112">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
    
 <span data-ttu-id="371d0-113">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="371d0-113">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="371d0-114">[вышел] Указатель на указатель на идентификатор завернутой записи.</span><span class="sxs-lookup"><span data-stu-id="371d0-114">[out] A pointer to a pointer to the wrapped entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="371d0-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="371d0-115">Return value</span></span>

<span data-ttu-id="371d0-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="371d0-116">S_OK</span></span> 
  
> <span data-ttu-id="371d0-117">Идентификатор записи был успешно завернут.</span><span class="sxs-lookup"><span data-stu-id="371d0-117">The entry identifier was successfully wrapped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="371d0-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="371d0-118">Remarks</span></span>

<span data-ttu-id="371d0-119">Метод **IMAPISupport::WrapStoreEntryID** реализован для всех объектов поддержки поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="371d0-119">The **IMAPISupport::WrapStoreEntryID** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="371d0-120">Поставщики услуг используют **WrapStoreEntryID** для создания идентификатора записи MAPI для магазина сообщений, который заворачивает внутренний идентификатор входа магазина.</span><span class="sxs-lookup"><span data-stu-id="371d0-120">Service providers use **WrapStoreEntryID** to have MAPI generate an entry identifier for a message store that wraps the store's internal entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="371d0-121">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="371d0-121">Notes to callers</span></span>

<span data-ttu-id="371d0-122">Когда клиент вызывает [IMAPIProp::GetProps](imapiprop-getprops.md) для получения свойства **PR_STORE_ENTRYID** [(PidTagStoreEntryId),](pidtagstoreentryid-canonical-property.md)а в хранилище сообщений используется идентификатор входа в частном формате, вызывайте **WrapStoreEntryID** и возвращайте идентификатор записи, на который указывает параметр _lppWrappedEntry._</span><span class="sxs-lookup"><span data-stu-id="371d0-122">When a client calls your message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property, and your message store uses an entry identifier in a private format, call **WrapStoreEntryID** and return the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
  
<span data-ttu-id="371d0-123">Вызовы к [методам IMSProvider::Logon](imsprovider-logon.md) и [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) всегда получают идентификатор частного входа магазина; завернутая версия используется только между клиентских приложений и MAPI.</span><span class="sxs-lookup"><span data-stu-id="371d0-123">Calls to the [IMSProvider::Logon](imsprovider-logon.md) and [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) methods always obtain the store's private entry identifier; the wrapped version is used only between client applications and MAPI.</span></span> 
  
<span data-ttu-id="371d0-124">Освободите память для идентификатора записи, на который указывает параметр  _lppWrappedEntry,_ используя функцию [MAPIFreeBuffer](mapifreebuffer.md) после завершения работы с идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="371d0-124">Free the memory for the entry identifier pointed to by the  _lppWrappedEntry_ parameter by using the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished using the entry identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="371d0-125">См. также</span><span class="sxs-lookup"><span data-stu-id="371d0-125">See also</span></span>



[<span data-ttu-id="371d0-126">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="371d0-126">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="371d0-127">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="371d0-127">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="371d0-128">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="371d0-128">IMSLogon::CompareEntryIDs</span></span>](imslogon-compareentryids.md)
  
[<span data-ttu-id="371d0-129">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="371d0-129">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="371d0-130">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="371d0-130">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="371d0-131">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="371d0-131">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

