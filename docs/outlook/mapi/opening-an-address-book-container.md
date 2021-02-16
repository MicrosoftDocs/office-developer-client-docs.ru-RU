---
title: Открытие контейнера адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: 97fa9f9750174c112c431c62f6171f674856fa86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436743"
---
# <a name="opening-an-address-book-container"></a><span data-ttu-id="308b0-103">Открытие контейнера адресной книги</span><span class="sxs-lookup"><span data-stu-id="308b0-103">Opening an address book container</span></span>

<span data-ttu-id="308b0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="308b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="308b0-105">После открытия интегрированной адресной книги MAPI откройте один или несколько контейнеров адресной книги, чтобы получить доступ к получателям в них.</span><span class="sxs-lookup"><span data-stu-id="308b0-105">After opening the MAPI integrated address book, open one or more address book containers to access the recipients within them.</span></span>
  
<span data-ttu-id="308b0-106">Чтобы открыть контейнер верхнего уровня адресной книги, вызовите [IAddrBook::OpenEntry](iaddrbook-openentry.md) с идентификатором записи NULL.</span><span class="sxs-lookup"><span data-stu-id="308b0-106">To open the top-level container of the address book, call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier.</span></span> 
  
<span data-ttu-id="308b0-107">Контейнеры адресной книги можно реализовать с доступом только для чтения или чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="308b0-107">Address book containers can be implemented with read-only or read/write access.</span></span> <span data-ttu-id="308b0-108">Контейнеры только для чтения используются только для просмотра.</span><span class="sxs-lookup"><span data-stu-id="308b0-108">Read-only containers are used only for browsing.</span></span> <span data-ttu-id="308b0-109">Контейнеры для чтения и записи можно изменять, позволяя клиентам создавать новые записи, а также удалять и изменять существующие записи.</span><span class="sxs-lookup"><span data-stu-id="308b0-109">Read/write containers can be modified, allowing clients to create new entries and delete and modify existing entries.</span></span> <span data-ttu-id="308b0-110">Все контейнеры личной адресной книги реализованы как контейнеры чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="308b0-110">All personal address book (PAB) containers are implemented as read/write containers.</span></span> 
  
<span data-ttu-id="308b0-111">Чтобы открыть любой контейнер нижнего уровня, **вызовите OpenEntry** и укажите идентификатор записи открываемого контейнера.</span><span class="sxs-lookup"><span data-stu-id="308b0-111">To open any lower level container, call **OpenEntry** and specify the entry identifier of the container to be opened.</span></span> 
  
## <a name="open-the-container-designated-as-the-pab"></a><span data-ttu-id="308b0-112">Откройте контейнер, назначенный в качестве PAB</span><span class="sxs-lookup"><span data-stu-id="308b0-112">Open the container designated as the PAB</span></span>
  
1. <span data-ttu-id="308b0-113">Вызовите [IAddrBook::GetPAB,](iaddrbook-getpab.md) чтобы получить идентификатор записи PAB.</span><span class="sxs-lookup"><span data-stu-id="308b0-113">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the PAB's entry identifier.</span></span> 
    
2. <span data-ttu-id="308b0-114">Передав этот идентификатор записи [в IAddrBook::OpenEntry.](iaddrbook-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="308b0-114">Pass this entry identifier to [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span>
    
## <a name="open-a-container-that-is-not-the-pab"></a><span data-ttu-id="308b0-115">Открытие контейнера, который не является PAB</span><span class="sxs-lookup"><span data-stu-id="308b0-115">Open a container that is not the PAB</span></span>
  
1. <span data-ttu-id="308b0-116">Вызовите [IAddrBook::OpenEntry](iaddrbook-openentry.md) с идентификатором записи NULL, чтобы открыть корневой контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="308b0-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier to open the address book's root container.</span></span> 
    
2. <span data-ttu-id="308b0-117">Вызовите метод [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) корневого контейнера, чтобы получить таблицу иерархии — список всех контейнеров верхнего уровня в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="308b0-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to retrieve its hierarchy table — a list of all of the top-level containers in the address book.</span></span> 
    
3. <span data-ttu-id="308b0-118">Если открытый контейнер имеет определенный тип:</span><span class="sxs-lookup"><span data-stu-id="308b0-118">If the container to be opened is of a specific type:</span></span>
    
   - <span data-ttu-id="308b0-119">Создайте **структуру SPropertyRestriction** с **PR_DISPLAY_TYPE** ([PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)для тега свойства, тип контейнера для значения свойства и RELOP_EQ для отношения.</span><span class="sxs-lookup"><span data-stu-id="308b0-119">Create an **SPropertyRestriction** structure with **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) for the property tag, the container's type for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="308b0-120">**PR_DISPLAY_TYPE** может быть установлено множество значений, среди них:</span><span class="sxs-lookup"><span data-stu-id="308b0-120">**PR_DISPLAY_TYPE** can be set to many values, among them:</span></span> 
    
   - <span data-ttu-id="308b0-121">DT_GLOBAL ограничить таблицу иерархии контейнерами, которые входят в глобальный список адресов.</span><span class="sxs-lookup"><span data-stu-id="308b0-121">DT_GLOBAL to limit the hierarchy table to containers that belong in the global address list.</span></span>
    
   - <span data-ttu-id="308b0-122">DT_LOCAL можно ограничить таблицу контейнерами, принадлежащими локальной адресной книге.</span><span class="sxs-lookup"><span data-stu-id="308b0-122">DT_LOCAL to limit the table to containers belonging to a local address book.</span></span>
    
   - <span data-ttu-id="308b0-123">DT_MODIFIABLE можно ограничить таблицу контейнерами, которые можно изменить.</span><span class="sxs-lookup"><span data-stu-id="308b0-123">DT_MODIFIABLE to limit the table to containers that can be modified.</span></span>
    
   - <span data-ttu-id="308b0-124">Создайте [структуру SPropTagArray,](sproptagarray.md) **которая включает** PR_ENTRYID, **PR_DISPLAY_TYPE** и любые другие столбцы, которые будут интересны.</span><span class="sxs-lookup"><span data-stu-id="308b0-124">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID**, **PR_DISPLAY_TYPE**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="308b0-125">Вызовите [HrQueryAllRows, передав](hrqueryallrows.md)ограничение свойств и массив тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="308b0-125">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="308b0-126">**HrQueryAllRows** возвращает ноль или больше строк, по одной строке для каждого контейнера, который принадлежит указанному типу.</span><span class="sxs-lookup"><span data-stu-id="308b0-126">**HrQueryAllRows** will return zero or more rows, one row for every container that belongs to the specified type.</span></span> <span data-ttu-id="308b0-127">Будьте готовы обрабатывать возврат любого количества строк.</span><span class="sxs-lookup"><span data-stu-id="308b0-127">Be prepared to handle the return of any number of rows.</span></span> 
    
   - <span data-ttu-id="308b0-128">Вызовите **IAddrBook::OpenEntry** с идентификатором  записи из столбца PR_ENTRYID строки, которая представляет контейнер для интереса.</span><span class="sxs-lookup"><span data-stu-id="308b0-128">Call **IAddrBook::OpenEntry** with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> 
    
4. <span data-ttu-id="308b0-129">Если открытый контейнер принадлежит определенному поставщику адресной книги:</span><span class="sxs-lookup"><span data-stu-id="308b0-129">If the container to be opened belongs to a specific address book provider:</span></span>
    
   - <span data-ttu-id="308b0-130">Создайте [структуру SPropertyRestriction](spropertyrestriction.md) с **PR_AB_PROVIDERS** ([PidTagAbProviders)](pidtagabproviders-canonical-property.md)для тега свойства, значения для конкретного поставщика для значения свойства и RELOP_EQ для отношения.</span><span class="sxs-lookup"><span data-stu-id="308b0-130">Create an [SPropertyRestriction](spropertyrestriction.md) structure with **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) for the property tag, a provider-specific value for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="308b0-131">Как правило, значение для конкретного поставщика — это глобальный уникальный идентификатор или GUID.</span><span class="sxs-lookup"><span data-stu-id="308b0-131">Typically the provider-specific value is a globally unique identifier or GUID.</span></span> <span data-ttu-id="308b0-132">Это значение будет опубликовано в одном из файлов заголовок поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="308b0-132">You will find this value published in one of the address book provider's header files.</span></span> 
    
   - <span data-ttu-id="308b0-133">Создайте [структуру SPropTagArray,](sproptagarray.md) которая **включает** PR_ENTRYID ([PidTagEntryId),](pidtagentryid-canonical-property.md) **PR_AB_PROVIDERS** и любые другие столбцы, которые будут интересны.</span><span class="sxs-lookup"><span data-stu-id="308b0-133">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="308b0-134">Вызовите [HrQueryAllRows, передав](hrqueryallrows.md)ограничение свойств и массив тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="308b0-134">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="308b0-135">**HrQueryAllRows** возвращает ноль строк, если указанный поставщик адресной книги не указан в профиле.</span><span class="sxs-lookup"><span data-stu-id="308b0-135">**HrQueryAllRows** will return zero rows if the specified address book provider is not in the profile.</span></span> <span data-ttu-id="308b0-136">Он может возвращать одну или несколько строк для контейнеров верхнего уровня поставщика в зависимости от того, как организован поставщик.</span><span class="sxs-lookup"><span data-stu-id="308b0-136">It can return one or more rows for the provider's top-level containers, depending on how the provider is organized.</span></span> 
    
   - <span data-ttu-id="308b0-137">Вызовите [IAddrBook::OpenEntry](iaddrbook-openentry.md) с идентификатором  записи из столбца PR_ENTRYID строки, которая представляет контейнер для интереса.</span><span class="sxs-lookup"><span data-stu-id="308b0-137">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> <span data-ttu-id="308b0-138">Если контейнер, который вас интересует, не является контейнером верхнего уровня, найдите контейнер верхнего уровня и перейдите по иерархии.</span><span class="sxs-lookup"><span data-stu-id="308b0-138">If the container that you are interested in is not a top-level container, find the top-level container and traverse the hierarchy.</span></span> 
    

