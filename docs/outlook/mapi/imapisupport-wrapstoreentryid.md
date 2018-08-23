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
ms.openlocfilehash: b3850da2917dbf463590643b9e7ba8420f4ea219
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576059"
---
# <a name="imapisupportwrapstoreentryid"></a><span data-ttu-id="1e849-103">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="1e849-103">IMAPISupport::WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="1e849-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e849-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e849-105">Преобразует идентификатор внутренней записи хранилища сообщений идентификатор записи в стандартный формат MAPI.</span><span class="sxs-lookup"><span data-stu-id="1e849-105">Converts a message store's internal entry identifier to an entry identifier in the MAPI standard format.</span></span>
  
```cpp
HRESULT WrapStoreEntryID(
ULONG cbOrigEntry,
LPENTRYID lpOrigEntry,
ULONG FAR * lpcbWrappedEntry,
LPENTRYID FAR * lppWrappedEntry
);
```

## <a name="parameters"></a><span data-ttu-id="1e849-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e849-106">Parameters</span></span>

 <span data-ttu-id="1e849-107">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="1e849-107">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="1e849-108">[in] Число байтов в идентификатор записи, на который указывает параметр _lpOrigEntry_ .</span><span class="sxs-lookup"><span data-stu-id="1e849-108">[in] The byte count in the entry identifier pointed to by the  _lpOrigEntry_ parameter.</span></span> 
    
 <span data-ttu-id="1e849-109">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="1e849-109">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="1e849-110">[in] Указатель на идентификатор частной запись для хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="1e849-110">[in] A pointer to the private entry identifier for the message store.</span></span>
    
 <span data-ttu-id="1e849-111">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="1e849-111">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="1e849-112">[out] Указатель на число байтов в идентификатор записи, на который указывает параметр _lppWrappedEntry_ .</span><span class="sxs-lookup"><span data-stu-id="1e849-112">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
    
 <span data-ttu-id="1e849-113">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="1e849-113">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="1e849-114">[out] Указатель на указатель на идентификатор оболочку записи.</span><span class="sxs-lookup"><span data-stu-id="1e849-114">[out] A pointer to a pointer to the wrapped entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1e849-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="1e849-115">Return value</span></span>

<span data-ttu-id="1e849-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="1e849-116">S_OK</span></span> 
  
> <span data-ttu-id="1e849-117">Идентификатор записи успешно оболочку.</span><span class="sxs-lookup"><span data-stu-id="1e849-117">The entry identifier was successfully wrapped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1e849-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="1e849-118">Remarks</span></span>

<span data-ttu-id="1e849-119">Метод **IMAPISupport::WrapStoreEntryID** применяется для всех объектов поддержки поставщика службы.</span><span class="sxs-lookup"><span data-stu-id="1e849-119">The **IMAPISupport::WrapStoreEntryID** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="1e849-120">Поставщики услуг использовать **WrapStoreEntryID** для создающего запись идентификатор хранилища сообщений, которое имеет идентификатор внутренней записи хранилища MAPI.</span><span class="sxs-lookup"><span data-stu-id="1e849-120">Service providers use **WrapStoreEntryID** to have MAPI generate an entry identifier for a message store that wraps the store's internal entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1e849-121">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="1e849-121">Notes to callers</span></span>

<span data-ttu-id="1e849-122">Когда клиент вызывает метод [IMAPIProp::GetProps](imapiprop-getprops.md) хранилища сообщений для получения его свойство **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) и хранения сообщений используется идентификатор записи в виде частный, вызвать **WrapStoreEntryID **и возвращает идентификатор записи, на который указывает параметр _lppWrappedEntry_ .</span><span class="sxs-lookup"><span data-stu-id="1e849-122">When a client calls your message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property, and your message store uses an entry identifier in a private format, call **WrapStoreEntryID** and return the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
  
<span data-ttu-id="1e849-123">Вызовы методов [IMSProvider::Logon](imsprovider-logon.md) и [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) всегда получить идентификатор хранилища закрытый записи; Перенос версии используется только между клиентскими приложениями и MAPI.</span><span class="sxs-lookup"><span data-stu-id="1e849-123">Calls to the [IMSProvider::Logon](imsprovider-logon.md) and [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) methods always obtain the store's private entry identifier; the wrapped version is used only between client applications and MAPI.</span></span> 
  
<span data-ttu-id="1e849-124">Освободите память для идентификатора запись указывает параметр _lppWrappedEntry_ с помощью функции [MAPIFreeBuffer](mapifreebuffer.md) после завершения с помощью идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="1e849-124">Free the memory for the entry identifier pointed to by the  _lppWrappedEntry_ parameter by using the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished using the entry identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1e849-125">См. также</span><span class="sxs-lookup"><span data-stu-id="1e849-125">See also</span></span>



[<span data-ttu-id="1e849-126">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="1e849-126">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="1e849-127">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="1e849-127">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="1e849-128">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="1e849-128">IMSLogon::CompareEntryIDs</span></span>](imslogon-compareentryids.md)
  
[<span data-ttu-id="1e849-129">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="1e849-129">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="1e849-130">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1e849-130">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1e849-131">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1e849-131">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

