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
# <a name="wrapstoreentryid"></a><span data-ttu-id="9880d-103">WrapStoreEntryID</span><span class="sxs-lookup"><span data-stu-id="9880d-103">WrapStoreEntryID</span></span>

  
  
<span data-ttu-id="9880d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9880d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9880d-105">Преобразует внутренний идентификатор записи в хранилище сообщений в идентификатор записи, который может использовать система обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="9880d-105">Converts a message store's internal entry identifier to an entry identifier more usable by the messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9880d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9880d-106">Header file:</span></span>  <br/> |<span data-ttu-id="9880d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9880d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9880d-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="9880d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9880d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9880d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9880d-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="9880d-110">Called by:</span></span>  <br/> |<span data-ttu-id="9880d-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="9880d-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="9880d-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="9880d-112">Parameters</span></span>

 <span data-ttu-id="9880d-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9880d-113">_ulFlags_</span></span>
  
> <span data-ttu-id="9880d-114">[in] Битоваяmas флагов.</span><span class="sxs-lookup"><span data-stu-id="9880d-114">[in] Bitmask of flags.</span></span> <span data-ttu-id="9880d-115">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="9880d-115">The following flag can be set:</span></span>
    
<span data-ttu-id="9880d-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9880d-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9880d-117">Строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="9880d-117">The strings are in Unicode format.</span></span> <span data-ttu-id="9880d-118">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="9880d-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="9880d-119">_szDLLName_</span><span class="sxs-lookup"><span data-stu-id="9880d-119">_szDLLName_</span></span>
  
> <span data-ttu-id="9880d-120">[in] Имя DLL поставщика хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="9880d-120">[in] The name of the message store provider DLL.</span></span> 
    
 <span data-ttu-id="9880d-121">_cbOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="9880d-121">_cbOrigEntry_</span></span>
  
> <span data-ttu-id="9880d-122">[in] Размер (в bytes) исходного идентификатора записи для хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="9880d-122">[in] Size, in bytes, of the original entry identifier for the message store.</span></span> 
    
 <span data-ttu-id="9880d-123">_lpOrigEntry_</span><span class="sxs-lookup"><span data-stu-id="9880d-123">_lpOrigEntry_</span></span>
  
> <span data-ttu-id="9880d-124">[in] Указатель на [структуру ENTRYID,](entryid.md) которая содержит исходный идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="9880d-124">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the original entry identifier.</span></span> 
    
 <span data-ttu-id="9880d-125">_lpcbWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="9880d-125">_lpcbWrappedEntry_</span></span>
  
> <span data-ttu-id="9880d-126">[out] Указатель на размер нового идентификатора записи (в bytes).</span><span class="sxs-lookup"><span data-stu-id="9880d-126">[out] Pointer to the size, in bytes, of the new entry identifier.</span></span> 
    
 <span data-ttu-id="9880d-127">_lppWrappedEntry_</span><span class="sxs-lookup"><span data-stu-id="9880d-127">_lppWrappedEntry_</span></span>
  
> <span data-ttu-id="9880d-128">[out] Указатель на указатель на структуру **ENTRYID,** которая содержит новый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="9880d-128">[out] Pointer to a pointer to an **ENTRYID** structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9880d-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9880d-129">Return value</span></span>

<span data-ttu-id="9880d-130">Нет.</span><span class="sxs-lookup"><span data-stu-id="9880d-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9880d-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="9880d-131">Remarks</span></span>

<span data-ttu-id="9880d-132">Объект хранения сообщений сохраняет внутренний идентификатор записи, который имеет смысл только для поставщиков услуг, которые его не содержат.</span><span class="sxs-lookup"><span data-stu-id="9880d-132">A message store object retains an internal entry identifier which is meaningful only to service providers coresident with that message store.</span></span> <span data-ttu-id="9880d-133">Для других компонентов обмена сообщениями MAPI передает упакованную версию идентификатора внутренней записи, которая делает его узнаваемым, так как он принадлежит хранилищем сообщений.</span><span class="sxs-lookup"><span data-stu-id="9880d-133">For other messaging components, MAPI supplies a wrapped version of the internal entry identifier that makes it recognizable as that belong to the message store.</span></span> <span data-ttu-id="9880d-134">Поставщикам служб Coresident всегда должен быть предоставлен исходный идентификатор записи в хранилище сообщений без перехваченных данных; клиентские приложения всегда должны иметь завернутую версию, которую можно использовать в любом месте домена обмена сообщениями и в других доменах.</span><span class="sxs-lookup"><span data-stu-id="9880d-134">Coresident service providers should always be given the original unwrapped message store entry identifier; client applications should always be given the wrapped version, which is then usable anywhere in the messaging domain and in other domains.</span></span> 
  
<span data-ttu-id="9880d-135">Поставщик службы может обтекать идентификатор записи в хранилище сообщений с помощью функции **WrapStoreEntryID** или метода [IMAPISupport::WrapStoreEntryID,](imapisupport-wrapstoreentryid.md) который вызывает функцию **WrapStoreEntryID.**</span><span class="sxs-lookup"><span data-stu-id="9880d-135">A service provider can wrap a message store entry identifier using either the **WrapStoreEntryID** function or the [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) method, which calls the **WrapStoreEntryID** function.</span></span> <span data-ttu-id="9880d-136">Поставщик должен обтекать идентификатор записи при отобралении свойства **PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)в хранилище сообщений или его записи в раздел профиля, а также при отобралении свойства **PR_STORE_ENTRYID** ([PidTagStoreEntryId).](pidtagstoreentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="9880d-136">The provider must wrap the entry identifier when exposing the message store's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property or writing it into a profile section, and when exposing the **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="9880d-137">MAPI обтекает идентификатор записи в хранилище сообщений при ответе на вызов [IMAPISession::OpenMsgStore.](imapisession-openmsgstore.md)</span><span class="sxs-lookup"><span data-stu-id="9880d-137">MAPI wraps a message store entry identifier when responding to an [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) call.</span></span> 
  
<span data-ttu-id="9880d-138">Когда клиентские приложения передает идентификатор записи в хранилище упакованных сообщений MAPI, например в [вызове IMAPISession::OpenEntry,](imapisession-openentry.md) MAPI unwraps the entry identifier before using it to call a provider method such as [IMSProvider::Logon](imsprovider-logon.md) or [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span><span class="sxs-lookup"><span data-stu-id="9880d-138">When a client application passes a wrapped message store entry identifier to MAPI, for example in an [IMAPISession::OpenEntry](imapisession-openentry.md) call, MAPI unwraps the entry identifier before using it to call a provider method such as [IMSProvider::Logon](imsprovider-logon.md) or [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md).</span></span> 
  

