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
ms.openlocfilehash: c644e89511033234aa45c5f82738e4c471ef646d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422497"
---
# <a name="message-service-tables"></a><span data-ttu-id="8d03c-103">Таблицы службы сообщений</span><span class="sxs-lookup"><span data-stu-id="8d03c-103">Message Service Tables</span></span>

  
  
<span data-ttu-id="8d03c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d03c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d03c-105">Таблица служба сообщений содержит сведения о службах сообщений в текущем профиле.</span><span class="sxs-lookup"><span data-stu-id="8d03c-105">The message service table contains information about the message services in the current profile.</span></span> <span data-ttu-id="8d03c-106">Для каждого сеанса MAPI существует одна таблица службы сообщений, реализованная MAPI и используемая клиентскими приложениями специального назначения, которые обеспечивают поддержку конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8d03c-106">There is one message service table for every MAPI session, implemented by MAPI and used by special purpose client applications that provide configuration support.</span></span> 
  
<span data-ttu-id="8d03c-107">Таблица службы сообщений — это статическая таблица.</span><span class="sxs-lookup"><span data-stu-id="8d03c-107">The message service table is a static table.</span></span>
  
<span data-ttu-id="8d03c-108">Клиенты получают доступ к таблице службы сообщений, вызывая метод [имсгсервицеадмин:: жетмсгсервицетабле](imsgserviceadmin-getmsgservicetable.md) .</span><span class="sxs-lookup"><span data-stu-id="8d03c-108">Clients access the message service table by calling the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method.</span></span> 
  
<span data-ttu-id="8d03c-109">Следующие свойства составляют обязательный набор столбцов в таблице службы сообщений:</span><span class="sxs-lookup"><span data-stu-id="8d03c-109">The following properties make up the required column set in the message service table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8d03c-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8d03c-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8d03c-111">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8d03c-111">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="8d03c-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8d03c-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8d03c-113">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8d03c-113">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="8d03c-114">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8d03c-114">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8d03c-115">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8d03c-115">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="8d03c-116">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8d03c-116">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="8d03c-117">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="8d03c-117">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span></span>  <br/> |
   
 <span data-ttu-id="8d03c-118">**PR_DISPLAY_NAME** — отображаемое имя для службы сообщений и столбец ключа сортировки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8d03c-118">**PR_DISPLAY_NAME** is the displayable name for the message service and the default sort key column.</span></span> 
  
 <span data-ttu-id="8d03c-119">**PR_INSTANCE_KEY** выступает в качестве столбца индекса для таблицы, уникальным образом идентифицирующего строку.</span><span class="sxs-lookup"><span data-stu-id="8d03c-119">**PR_INSTANCE_KEY** serves as the index column for the table, uniquely identifying a row.</span></span> 
  
 <span data-ttu-id="8d03c-120">**PR_RESOURCE_FLAGS** рассказывается о возможностях службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="8d03c-120">**PR_RESOURCE_FLAGS** describes the message service's capabilities.</span></span> 
  
 <span data-ttu-id="8d03c-121">**PR_SERVICE_DLL_NAME** — это имя библиотеки DLL, которая содержит реализацию службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="8d03c-121">**PR_SERVICE_DLL_NAME** is the name of the DLL that contains the message service implementation.</span></span> 
  
 <span data-ttu-id="8d03c-122">**PR_SERVICE_ENTRY_NAME** — это имя функции точки входа службы сообщений, которая соответствует прототипу [мсгсервицеентри](msgserviceentry.md) .</span><span class="sxs-lookup"><span data-stu-id="8d03c-122">**PR_SERVICE_ENTRY_NAME** is the name of the message service's entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> 
  
 <span data-ttu-id="8d03c-123">**PR_SERVICE_NAME** является обязательной записью в разделе **[Services]** in Mapisvc. INF.</span><span class="sxs-lookup"><span data-stu-id="8d03c-123">**PR_SERVICE_NAME** is a required entry in the **[Services]** section in MAPISVC.INF.</span></span> <span data-ttu-id="8d03c-124">Значение этого свойства никогда не будет изменено или локализовано.</span><span class="sxs-lookup"><span data-stu-id="8d03c-124">The value for this property will never be changed or localized.</span></span> <span data-ttu-id="8d03c-125">**PR_SERVICE_NAME** можно использовать для программного определения службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="8d03c-125">**PR_SERVICE_NAME** can be used to programmatically identify the message service.</span></span> 
  
 <span data-ttu-id="8d03c-126">**PR_SERVICE_SUPPORT_FILES** — это список файлов, которые необходимо установить вместе со службой сообщений.</span><span class="sxs-lookup"><span data-stu-id="8d03c-126">**PR_SERVICE_SUPPORT_FILES** is a list of files that must be installed with the message service.</span></span> 
  
 <span data-ttu-id="8d03c-127">**PR_SERVICE_UID** — это уникальный идентификатор службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="8d03c-127">**PR_SERVICE_UID** is a unique identifier for the message service.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8d03c-128">См. также</span><span class="sxs-lookup"><span data-stu-id="8d03c-128">See also</span></span>



[<span data-ttu-id="8d03c-129">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="8d03c-129">MAPI Tables</span></span>](mapi-tables.md)

