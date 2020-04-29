---
title: имаписуппортврапсторинтрид
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
# <a name="imapisupportwrapstoreentryid"></a><span data-ttu-id="038c4-103">IMAPISupport::WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="038c4-103">IMAPISupport::WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="038c4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="038c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="038c4-105">Преобразует внутренний идентификатор записи банка сообщений в идентификатор записи в стандартном формате MAPI.</span><span class="sxs-lookup"><span data-stu-id="038c4-105">Converts a message store's internal entry identifier to an entry identifier in the MAPI standard format.</span></span>
  
```cpp
HRESULT WrapStoreEntryID(
ULONG cbOrigEntry,
LPENTRYID lpOrigEntry,
ULONG FAR * lpcbWrappedEntry,
LPENTRYID FAR * lppWrappedEntry
);
```

## <a name="parameters"></a><span data-ttu-id="038c4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="038c4-106">Parameters</span></span>

 <span data-ttu-id="038c4-107">_кборижентри_</span><span class="sxs-lookup"><span data-stu-id="038c4-107">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="038c4-108">возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпорижентри_ .</span><span class="sxs-lookup"><span data-stu-id="038c4-108">[in] The byte count in the entry identifier pointed to by the  _lpOrigEntry_ parameter.</span></span> 
    
 <span data-ttu-id="038c4-109">_лпорижентри_</span><span class="sxs-lookup"><span data-stu-id="038c4-109">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="038c4-110">возврата Указатель на идентификатор частной записи для хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="038c4-110">[in] A pointer to the private entry identifier for the message store.</span></span>
    
 <span data-ttu-id="038c4-111">_лпкбвраппедентри_</span><span class="sxs-lookup"><span data-stu-id="038c4-111">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="038c4-112">вышли Указатель на число байтов в идентификаторе записи, на который указывает параметр _лппвраппедентри_ .</span><span class="sxs-lookup"><span data-stu-id="038c4-112">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
    
 <span data-ttu-id="038c4-113">_лппвраппедентри_</span><span class="sxs-lookup"><span data-stu-id="038c4-113">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="038c4-114">вышли Указатель на указатель на идентификатор заключенной в оболочку записи.</span><span class="sxs-lookup"><span data-stu-id="038c4-114">[out] A pointer to a pointer to the wrapped entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="038c4-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="038c4-115">Return value</span></span>

<span data-ttu-id="038c4-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="038c4-116">S_OK</span></span> 
  
> <span data-ttu-id="038c4-117">Идентификатор записи успешно заключен в оболочку.</span><span class="sxs-lookup"><span data-stu-id="038c4-117">The entry identifier was successfully wrapped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="038c4-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="038c4-118">Remarks</span></span>

<span data-ttu-id="038c4-119">Метод **имаписуппорт:: врапсторинтрид** реализован для всех объектов поддержки поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="038c4-119">The **IMAPISupport::WrapStoreEntryID** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="038c4-120">Поставщики услуг используют **врапсторинтрид** для создания идентификатора записи для хранилища сообщений, который создает оболочку для внутреннего идентификатора записи хранилища.</span><span class="sxs-lookup"><span data-stu-id="038c4-120">Service providers use **WrapStoreEntryID** to have MAPI generate an entry identifier for a message store that wraps the store's internal entry identifier.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="038c4-121">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="038c4-121">Notes to callers</span></span>

<span data-ttu-id="038c4-122">Когда клиент вызывает метод [IMAPIProp::-PROPS](imapiprop-getprops.md) хранилища сообщений для получения его свойства **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)), а хранилище сообщений использует идентификатор записи в частном формате, вызовите **врапсторинтрид** и возвратите идентификатор записи, на который указывает параметр _лппвраппедентри_ .</span><span class="sxs-lookup"><span data-stu-id="038c4-122">When a client calls your message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property, and your message store uses an entry identifier in a private format, call **WrapStoreEntryID** and return the entry identifier pointed to by the  _lppWrappedEntry_ parameter.</span></span> 
  
<span data-ttu-id="038c4-123">Вызовы методов [функцииimsprovider:: logon](imsprovider-logon.md) и [Имслогон:: метод compareentryids](imslogon-compareentryids.md) всегда получают личный идентификатор записи хранилища; Упакованная версия используется только между клиентскими приложениями и MAPI.</span><span class="sxs-lookup"><span data-stu-id="038c4-123">Calls to the [IMSProvider::Logon](imsprovider-logon.md) and [IMSLogon::CompareEntryIDs](imslogon-compareentryids.md) methods always obtain the store's private entry identifier; the wrapped version is used only between client applications and MAPI.</span></span> 
  
<span data-ttu-id="038c4-124">Освободите память для идентификатора записи, на которую указывает параметр _лппвраппедентри_ , с помощью функции [мапифрибуффер](mapifreebuffer.md) по завершении использования идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="038c4-124">Free the memory for the entry identifier pointed to by the  _lppWrappedEntry_ parameter by using the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished using the entry identifier.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="038c4-125">См. также</span><span class="sxs-lookup"><span data-stu-id="038c4-125">See also</span></span>



[<span data-ttu-id="038c4-126">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="038c4-126">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="038c4-127">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="038c4-127">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="038c4-128">IMSLogon::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="038c4-128">IMSLogon::CompareEntryIDs</span></span>](imslogon-compareentryids.md)
  
[<span data-ttu-id="038c4-129">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="038c4-129">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="038c4-130">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="038c4-130">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="038c4-131">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="038c4-131">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

