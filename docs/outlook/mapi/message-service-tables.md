---
title: Таблицы службы сообщений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 569c1bd7ee2f4ac6c321f234be2954a57715549b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576673"
---
# <a name="message-service-tables"></a><span data-ttu-id="0a72d-103">Таблицы службы сообщений</span><span class="sxs-lookup"><span data-stu-id="0a72d-103">Message Service Tables</span></span>

  
  
<span data-ttu-id="0a72d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a72d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a72d-105">Таблица службы сообщение содержит сведения о службах сообщения текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="0a72d-105">The message service table contains information about the message services in the current profile.</span></span> <span data-ttu-id="0a72d-106">Для каждого сеанса MAPI, реализованный MAPI и используется особого назначения клиентских приложений, которые обеспечивают поддержку конфигурации имеется одна таблица службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="0a72d-106">There is one message service table for every MAPI session, implemented by MAPI and used by special purpose client applications that provide configuration support.</span></span> 
  
<span data-ttu-id="0a72d-107">В таблице службы сообщений — это статическая таблица.</span><span class="sxs-lookup"><span data-stu-id="0a72d-107">The message service table is a static table.</span></span>
  
<span data-ttu-id="0a72d-108">Для доступа клиентов к таблице службы сообщения путем вызова метода [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) .</span><span class="sxs-lookup"><span data-stu-id="0a72d-108">Clients access the message service table by calling the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method.</span></span> 
  
<span data-ttu-id="0a72d-109">Следующие свойства составляют обязательный столбец, задайте в таблице служб сообщения:</span><span class="sxs-lookup"><span data-stu-id="0a72d-109">The following properties make up the required column set in the message service table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0a72d-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0a72d-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0a72d-111">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0a72d-111">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="0a72d-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0a72d-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0a72d-113">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0a72d-113">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="0a72d-114">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0a72d-114">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0a72d-115">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0a72d-115">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="0a72d-116">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0a72d-116">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="0a72d-117">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0a72d-117">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span></span>  <br/> |
   
 <span data-ttu-id="0a72d-118">**PR_DISPLAY_NAME** — отображаемое имя для службы сообщений и столбце ключа сортировки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0a72d-118">**PR_DISPLAY_NAME** is the displayable name for the message service and the default sort key column.</span></span> 
  
 <span data-ttu-id="0a72d-119">**PR_INSTANCE_KEY** выступает в качестве столбца индекса для таблицы, уникально идентифицирующий строку.</span><span class="sxs-lookup"><span data-stu-id="0a72d-119">**PR_INSTANCE_KEY** serves as the index column for the table, uniquely identifying a row.</span></span> 
  
 <span data-ttu-id="0a72d-120">**PR_RESOURCE_FLAGS** : описание возможностей службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="0a72d-120">**PR_RESOURCE_FLAGS** describes the message service's capabilities.</span></span> 
  
 <span data-ttu-id="0a72d-121">**PR_SERVICE_DLL_NAME** — это имя библиотеки DLL, которая содержит реализации службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="0a72d-121">**PR_SERVICE_DLL_NAME** is the name of the DLL that contains the message service implementation.</span></span> 
  
 <span data-ttu-id="0a72d-122">**PR_SERVICE_ENTRY_NAME** — это имя функции точки входа службы сообщений, который соответствует прототип [MSGSERVICEENTRY](msgserviceentry.md) .</span><span class="sxs-lookup"><span data-stu-id="0a72d-122">**PR_SERVICE_ENTRY_NAME** is the name of the message service's entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> 
  
 <span data-ttu-id="0a72d-123">**PR_SERVICE_NAME** является обязательным параметром в разделе **[Services]** в MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="0a72d-123">**PR_SERVICE_NAME** is a required entry in the **[Services]** section in MAPISVC.INF.</span></span> <span data-ttu-id="0a72d-124">Значение для этого свойства никогда не будет изменен или локализованное.</span><span class="sxs-lookup"><span data-stu-id="0a72d-124">The value for this property will never be changed or localized.</span></span> <span data-ttu-id="0a72d-125">**PR_SERVICE_NAME** можно использовать для идентификации службы сообщений программными средствами.</span><span class="sxs-lookup"><span data-stu-id="0a72d-125">**PR_SERVICE_NAME** can be used to programmatically identify the message service.</span></span> 
  
 <span data-ttu-id="0a72d-126">**PR_SERVICE_SUPPORT_FILES** — это список файлов, которые должны быть установлены с помощью службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="0a72d-126">**PR_SERVICE_SUPPORT_FILES** is a list of files that must be installed with the message service.</span></span> 
  
 <span data-ttu-id="0a72d-127">**PR_SERVICE_UID** — уникальный идентификатор для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="0a72d-127">**PR_SERVICE_UID** is a unique identifier for the message service.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0a72d-128">См. также</span><span class="sxs-lookup"><span data-stu-id="0a72d-128">See also</span></span>



[<span data-ttu-id="0a72d-129">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="0a72d-129">MAPI Tables</span></span>](mapi-tables.md)

