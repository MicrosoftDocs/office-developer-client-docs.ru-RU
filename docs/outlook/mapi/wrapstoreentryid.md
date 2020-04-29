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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409211"
---
# <a name="wrapstoreentryid"></a><span data-ttu-id="2ec81-103">WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="2ec81-103">WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="2ec81-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ec81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ec81-105">Преобразует внутренний идентификатор записи хранилища сообщений в идентификатор записи, который больше используется системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="2ec81-105">Converts a message store's internal entry identifier to an entry identifier more usable by the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2ec81-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="2ec81-106">Header file:</span></span>  <br/> |<span data-ttu-id="2ec81-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="2ec81-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2ec81-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="2ec81-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2ec81-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2ec81-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2ec81-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="2ec81-110">Called by:</span></span>  <br/> |<span data-ttu-id="2ec81-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="2ec81-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="2ec81-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ec81-112">Parameters</span></span>

 <span data-ttu-id="2ec81-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2ec81-113">_ulFlags_</span></span>
  
> <span data-ttu-id="2ec81-114">возврата Битовая маска флагов.</span><span class="sxs-lookup"><span data-stu-id="2ec81-114">[in] Bitmask of flags.</span></span> <span data-ttu-id="2ec81-115">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="2ec81-115">The following flag can be set:</span></span>
    
<span data-ttu-id="2ec81-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2ec81-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2ec81-117">Строки представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="2ec81-117">The strings are in Unicode format.</span></span> <span data-ttu-id="2ec81-118">Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="2ec81-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="2ec81-119">_сздллнаме_</span><span class="sxs-lookup"><span data-stu-id="2ec81-119">_szDLLName_</span></span>
  
> <span data-ttu-id="2ec81-120">возврата Имя библиотеки DLL поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="2ec81-120">[in] The name of the message store provider DLL.</span></span> 
    
 <span data-ttu-id="2ec81-121">_кборижентри_</span><span class="sxs-lookup"><span data-stu-id="2ec81-121">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="2ec81-122">возврата Размер (в байтах) исходного идентификатора записи для хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="2ec81-122">[in] Size, in bytes, of the original entry identifier for the message store.</span></span> 
    
 <span data-ttu-id="2ec81-123">_лпорижентри_</span><span class="sxs-lookup"><span data-stu-id="2ec81-123">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="2ec81-124">возврата Указатель на структуру [EntryID](entryid.md) , содержащую исходный идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="2ec81-124">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the original entry identifier.</span></span> 
    
 <span data-ttu-id="2ec81-125">_лпкбвраппедентри_</span><span class="sxs-lookup"><span data-stu-id="2ec81-125">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="2ec81-126">вышли Указатель на размер нового идентификатора записи (в байтах).</span><span class="sxs-lookup"><span data-stu-id="2ec81-126">[out] Pointer to the size, in bytes, of the new entry identifier.</span></span> 
    
 <span data-ttu-id="2ec81-127">_лппвраппедентри_</span><span class="sxs-lookup"><span data-stu-id="2ec81-127">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="2ec81-128">вышли Указатель на структуру кода **EntryID** , которая содержит новый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="2ec81-128">[out] Pointer to a pointer to an **ENTRYID** structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2ec81-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ec81-129">Return value</span></span>

<span data-ttu-id="2ec81-130">Нет.</span><span class="sxs-lookup"><span data-stu-id="2ec81-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2ec81-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="2ec81-131">Remarks</span></span>

<span data-ttu-id="2ec81-132">Объект хранилища сообщений сохраняет внутренний идентификатор записи, который имеет смысл только для поставщиков услуг, сопоставленных с этим хранилищем сообщений.</span><span class="sxs-lookup"><span data-stu-id="2ec81-132">A message store object retains an internal entry identifier which is meaningful only to service providers coresident with that message store.</span></span> <span data-ttu-id="2ec81-133">Для других компонентов обмена сообщениями MAPI предоставляет упакованную версию внутреннего идентификатора записи, которая делает его распознаваемым, как принадлежащий к хранилищу сообщений.</span><span class="sxs-lookup"><span data-stu-id="2ec81-133">For other messaging components, MAPI supplies a wrapped version of the internal entry identifier that makes it recognizable as that belong to the message store.</span></span> <span data-ttu-id="2ec81-134">Поставщики услуг для сорезидентных служб всегда должны иметь исходный неупакованный идентификатор записи в банке сообщений; клиентским приложениям всегда следует переносить упакованную версию, которая затем будет использоваться в любом месте домена обмена сообщениями и других доменах.</span><span class="sxs-lookup"><span data-stu-id="2ec81-134">Coresident service providers should always be given the original unwrapped message store entry identifier; client applications should always be given the wrapped version, which is then usable anywhere in the messaging domain and in other domains.</span></span> 
  
<span data-ttu-id="2ec81-135">Поставщик услуг может создать оболочку для идентификатора записи хранилища сообщений с помощью функции **врапсторинтрид** или метода [Имаписуппорт:: врапсторинтрид](imapisupport-wrapstoreentryid.md) , который вызывает функцию **врапсторинтрид** .</span><span class="sxs-lookup"><span data-stu-id="2ec81-135">A service provider can wrap a message store entry identifier using either the **WrapStoreEntryID** function or the [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) method, which calls the **WrapStoreEntryID** function.</span></span> <span data-ttu-id="2ec81-136">Поставщик должен заключить идентификатор записи при предоставлении свойства **PR_ENTRYID** хранилища сообщений ([PidTagEntryId](pidtagentryid-canonical-property.md)) или его записи в раздел профиля и при предоставлении доступа к свойству **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2ec81-136">The provider must wrap the entry identifier when exposing the message store's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property or writing it into a profile section, and when exposing the **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="2ec81-137">MAPI заключает идентификатор записи хранилища сообщений при ответе на вызов [IMAPISession:: опенмсгсторе](imapisession-openmsgstore.md) .</span><span class="sxs-lookup"><span data-stu-id="2ec81-137">MAPI wraps a message store entry identifier when responding to an [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) call.</span></span> 
  
<span data-ttu-id="2ec81-138">Когда клиентское приложение передает идентификатор записи в формате MAPI, например, в вызове [IMAPISession:: OpenEntry](imapisession-openentry.md) , MAPI рассматривает его перед вызовом метода поставщика, например [Функцииimsprovider:: logon](imsprovider-logon.md) или [функцииimsprovider:: компарестореидс](imsprovider-comparestoreids.md).</span><span class="sxs-lookup"><span data-stu-id="2ec81-138">When a client application passes a wrapped message store entry identifier to MAPI, for example in an [IMAPISession::OpenEntry](imapisession-openentry.md) call, MAPI unwraps the entry identifier before using it to call a provider method such as [IMSProvider::Logon](imsprovider-logon.md) or [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span></span> 
  

