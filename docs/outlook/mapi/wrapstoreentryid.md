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
ms.openlocfilehash: e797a80cf8659baa7ca935f94b3ab65c200530a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325671"
---
# <a name="wrapstoreentryid"></a><span data-ttu-id="d8448-103">WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="d8448-103">WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="d8448-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8448-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8448-105">Преобразует внутренний идентификатор записи хранилища сообщений в идентификатор записи, который больше используется системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="d8448-105">Converts a message store's internal entry identifier to an entry identifier more usable by the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d8448-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d8448-106">Header file:</span></span>  <br/> |<span data-ttu-id="d8448-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="d8448-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d8448-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="d8448-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d8448-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d8448-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d8448-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="d8448-110">Called by:</span></span>  <br/> |<span data-ttu-id="d8448-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="d8448-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="d8448-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8448-112">Parameters</span></span>

 <span data-ttu-id="d8448-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d8448-113">_ulFlags_</span></span>
  
> <span data-ttu-id="d8448-114">возврата Битовая маска флагов.</span><span class="sxs-lookup"><span data-stu-id="d8448-114">[in] Bitmask of flags.</span></span> <span data-ttu-id="d8448-115">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="d8448-115">The following flag can be set:</span></span>
    
<span data-ttu-id="d8448-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d8448-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d8448-117">Строки представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="d8448-117">The strings are in Unicode format.</span></span> <span data-ttu-id="d8448-118">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="d8448-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="d8448-119">_Сздллнаме_</span><span class="sxs-lookup"><span data-stu-id="d8448-119">_szDLLName_</span></span>
  
> <span data-ttu-id="d8448-120">возврата Имя библиотеки DLL поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="d8448-120">[in] The name of the message store provider DLL.</span></span> 
    
 <span data-ttu-id="d8448-121">_Кборижентри_</span><span class="sxs-lookup"><span data-stu-id="d8448-121">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="d8448-122">возврата Размер (в байтах) исходного идентификатора записи для хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="d8448-122">[in] Size, in bytes, of the original entry identifier for the message store.</span></span> 
    
 <span data-ttu-id="d8448-123">_Лпорижентри_</span><span class="sxs-lookup"><span data-stu-id="d8448-123">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="d8448-124">возврата Указатель на структуру [EntryID](entryid.md) , содержащую исходный идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="d8448-124">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the original entry identifier.</span></span> 
    
 <span data-ttu-id="d8448-125">_Лпкбвраппедентри_</span><span class="sxs-lookup"><span data-stu-id="d8448-125">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="d8448-126">вышли Указатель на размер нового идентификатора записи (в байтах).</span><span class="sxs-lookup"><span data-stu-id="d8448-126">[out] Pointer to the size, in bytes, of the new entry identifier.</span></span> 
    
 <span data-ttu-id="d8448-127">_Лппвраппедентри_</span><span class="sxs-lookup"><span data-stu-id="d8448-127">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="d8448-128">вышли Указатель на структуру кода **EntryID** , которая содержит новый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="d8448-128">[out] Pointer to a pointer to an **ENTRYID** structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d8448-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8448-129">Return value</span></span>

<span data-ttu-id="d8448-130">Нет.</span><span class="sxs-lookup"><span data-stu-id="d8448-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d8448-131">Замечания</span><span class="sxs-lookup"><span data-stu-id="d8448-131">Remarks</span></span>

<span data-ttu-id="d8448-132">Объект хранилища сообщений сохраняет внутренний идентификатор записи, который имеет смысл только для поставщиков услуг, сопоставленных с этим хранилищем сообщений.</span><span class="sxs-lookup"><span data-stu-id="d8448-132">A message store object retains an internal entry identifier which is meaningful only to service providers coresident with that message store.</span></span> <span data-ttu-id="d8448-133">Для других компонентов обмена сообщениями MAPI предоставляет упакованную версию внутреннего идентификатора записи, которая делает его распознаваемым, как принадлежащий к хранилищу сообщений.</span><span class="sxs-lookup"><span data-stu-id="d8448-133">For other messaging components, MAPI supplies a wrapped version of the internal entry identifier that makes it recognizable as that belong to the message store.</span></span> <span data-ttu-id="d8448-134">Поставщики услуг для сорезидентных служб всегда должны иметь исходный неупакованный идентификатор записи в банке сообщений; клиентским приложениям всегда следует переносить упакованную версию, которая затем будет использоваться в любом месте домена обмена сообщениями и других доменах.</span><span class="sxs-lookup"><span data-stu-id="d8448-134">Coresident service providers should always be given the original unwrapped message store entry identifier; client applications should always be given the wrapped version, which is then usable anywhere in the messaging domain and in other domains.</span></span> 
  
<span data-ttu-id="d8448-135">Поставщик услуг может создать оболочку для идентификатора записи хранилища сообщений с помощью функции **врапсторинтрид** или метода [Имаписуппорт:: врапсторинтрид](imapisupport-wrapstoreentryid.md) , который вызывает функцию **врапсторинтрид** .</span><span class="sxs-lookup"><span data-stu-id="d8448-135">A service provider can wrap a message store entry identifier using either the **WrapStoreEntryID** function or the [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) method, which calls the **WrapStoreEntryID** function.</span></span> <span data-ttu-id="d8448-136">Поставщик должен заключить идентификатор записи при предоставлении доступа к свойству **пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)) хранилища сообщений или его записи в раздел профиля и при предоставлении доступа к **пр_сторе_ентрид** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)). свойств.</span><span class="sxs-lookup"><span data-stu-id="d8448-136">The provider must wrap the entry identifier when exposing the message store's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property or writing it into a profile section, and when exposing the **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="d8448-137">MAPI заключает идентификатор записи хранилища сообщений при ответе на вызов [IMAPISession:: опенмсгсторе](imapisession-openmsgstore.md) .</span><span class="sxs-lookup"><span data-stu-id="d8448-137">MAPI wraps a message store entry identifier when responding to an [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) call.</span></span> 
  
<span data-ttu-id="d8448-138">Когда клиентское приложение передает зашифрованный идентификатор записи банка сообщений в MAPI, например в вызове [IMAPISession:: OpenEntry](imapisession-openentry.md) , MAPI разворачивает идентификатор записи перед его использованием для вызова метода поставщика, такого как [Функцииimsprovider:: logon](imsprovider-logon.md) или [ Функцииimsprovider:: Компарестореидс](imsprovider-comparestoreids.md).</span><span class="sxs-lookup"><span data-stu-id="d8448-138">When a client application passes a wrapped message store entry identifier to MAPI, for example in an [IMAPISession::OpenEntry](imapisession-openentry.md) call, MAPI unwraps the entry identifier before using it to call a provider method such as [IMSProvider::Logon](imsprovider-logon.md) or [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span></span> 
  

