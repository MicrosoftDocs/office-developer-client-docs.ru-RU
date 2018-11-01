---
title: WrapStoreEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WrapStoreEntryID
api_type:
- HeaderDef
ms.assetid: b20107e3-5e23-4cde-9cd6-670c914ea70a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 45263396e69852a9ae17ff6fce284663bdf2fb07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585138"
---
# <a name="wrapstoreentryid"></a><span data-ttu-id="6dab5-103">WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="6dab5-103">WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="6dab5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6dab5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6dab5-105">Преобразует идентификатор внутренней записи хранилища сообщений в более удобный идентификатор записи системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="6dab5-105">Converts a message store's internal entry identifier to an entry identifier more usable by the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6dab5-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6dab5-106">Header file:</span></span>  <br/> |<span data-ttu-id="6dab5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6dab5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6dab5-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="6dab5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6dab5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6dab5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6dab5-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="6dab5-110">Called by:</span></span>  <br/> |<span data-ttu-id="6dab5-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="6dab5-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
WrapStoreEntryID(
  ULONG ulFlags,
  LPSTR szDLLName,
  ULONG cbOrigEntry,
  LPENTRYID lpOrigEntry,
  ULONG * lpcbWrappedEntry,
  LPENTRYID * lppWrappedEntry
);
```

## <a name="parameters"></a><span data-ttu-id="6dab5-112">���������</span><span class="sxs-lookup"><span data-stu-id="6dab5-112">Parameters</span></span>

 <span data-ttu-id="6dab5-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6dab5-113">_ulFlags_</span></span>
  
> <span data-ttu-id="6dab5-114">[in] Битовая маска флаги.</span><span class="sxs-lookup"><span data-stu-id="6dab5-114">[in] Bitmask of flags.</span></span> <span data-ttu-id="6dab5-115">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="6dab5-115">The following flag can be set:</span></span>
    
<span data-ttu-id="6dab5-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6dab5-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6dab5-117">Они в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="6dab5-117">The strings are in Unicode format.</span></span> <span data-ttu-id="6dab5-118">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="6dab5-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="6dab5-119">_szDLLName_</span><span class="sxs-lookup"><span data-stu-id="6dab5-119">_szDLLName_</span></span>
  
> <span data-ttu-id="6dab5-120">[in] Имя поставщика хранилища сообщений DLL.</span><span class="sxs-lookup"><span data-stu-id="6dab5-120">[in] The name of the message store provider DLL.</span></span> 
    
 <span data-ttu-id="6dab5-121">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="6dab5-121">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="6dab5-122">[in] Размер, в байтах, исходный идентификатор записи для хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="6dab5-122">[in] Size, in bytes, of the original entry identifier for the message store.</span></span> 
    
 <span data-ttu-id="6dab5-123">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="6dab5-123">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="6dab5-124">[in] Указатель на структуру [ENTRYID](entryid.md) , которая содержит исходный идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="6dab5-124">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the original entry identifier.</span></span> 
    
 <span data-ttu-id="6dab5-125">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="6dab5-125">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="6dab5-126">[out] Указатель на размер, в байтах, новый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="6dab5-126">[out] Pointer to the size, in bytes, of the new entry identifier.</span></span> 
    
 <span data-ttu-id="6dab5-127">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="6dab5-127">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="6dab5-128">[out] Указатель на указатель на структуру **ENTRYID** , который содержит новый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="6dab5-128">[out] Pointer to a pointer to an **ENTRYID** structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6dab5-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6dab5-129">Return value</span></span>

<span data-ttu-id="6dab5-130">Нет.</span><span class="sxs-lookup"><span data-stu-id="6dab5-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6dab5-131">Замечания</span><span class="sxs-lookup"><span data-stu-id="6dab5-131">Remarks</span></span>

<span data-ttu-id="6dab5-132">Объект хранилища сообщений сохраняет внутренний запись идентификатора, который применяется только к coresident поставщики службы с помощью этого хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="6dab5-132">A message store object retains an internal entry identifier which is meaningful only to service providers coresident with that message store.</span></span> <span data-ttu-id="6dab5-133">Для других компонентов системы обмена сообщениями MAPI предоставляет оболочку версии идентификатор внутренняя запись HTML, которое распознается как принадлежат хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="6dab5-133">For other messaging components, MAPI supplies a wrapped version of the internal entry identifier that makes it recognizable as that belong to the message store.</span></span> <span data-ttu-id="6dab5-134">Поставщики услуг coresident всегда должны быть заданы исходного развернуть хранилища запись идентификатор сообщения; клиентские приложения всегда должны быть предоставлены оболочку версии, которые затем можно использовать в любом месте в домене, обмена мгновенными сообщениями и в других доменах.</span><span class="sxs-lookup"><span data-stu-id="6dab5-134">Coresident service providers should always be given the original unwrapped message store entry identifier; client applications should always be given the wrapped version, which is then usable anywhere in the messaging domain and in other domains.</span></span> 
  
<span data-ttu-id="6dab5-135">Поставщик службы можно включить с помощью функции **WrapStoreEntryID** или метод [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) , который вызывает функцию **WrapStoreEntryID** идентификатор записи хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="6dab5-135">A service provider can wrap a message store entry identifier using either the **WrapStoreEntryID** function or the [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) method, which calls the **WrapStoreEntryID** function.</span></span> <span data-ttu-id="6dab5-136">Поставщик должен быть оболочкой идентификатор записи при предоставлении хранилища сообщений **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) свойства или записи в раздел профилей и при предоставлении **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) свойство.</span><span class="sxs-lookup"><span data-stu-id="6dab5-136">The provider must wrap the entry identifier when exposing the message store's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property or writing it into a profile section, and when exposing the **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="6dab5-137">MAPI имеет идентификатор записи хранилища сообщений при ответе на вызов [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) .</span><span class="sxs-lookup"><span data-stu-id="6dab5-137">MAPI wraps a message store entry identifier when responding to an [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) call.</span></span> 
  
<span data-ttu-id="6dab5-138">Если клиентское приложение передает идентификатор записи хранилища оболочку сообщения для MAPI, например в вызове [IMAPISession::OpenEntry](imapisession-openentry.md) MAPI распаковывает идентификатор записи перед его использованием для вызова метода поставщика, например [IMSProvider::Logon](imsprovider-logon.md) или [ IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span><span class="sxs-lookup"><span data-stu-id="6dab5-138">When a client application passes a wrapped message store entry identifier to MAPI, for example in an [IMAPISession::OpenEntry](imapisession-openentry.md) call, MAPI unwraps the entry identifier before using it to call a provider method such as [IMSProvider::Logon](imsprovider-logon.md) or [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span></span> 
  

