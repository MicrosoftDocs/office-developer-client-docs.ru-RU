---
title: Открытие контейнера адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: 'Последнее изменение: 08 ноября 2011 г.'
ms.openlocfilehash: 97fa9f9750174c112c431c62f6171f674856fa86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436743"
---
# <a name="opening-an-address-book-container"></a><span data-ttu-id="a73fb-103">Открытие контейнера адресной книги</span><span class="sxs-lookup"><span data-stu-id="a73fb-103">Opening an address book container</span></span>

<span data-ttu-id="a73fb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a73fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a73fb-105">После открытия интегрированной адресной книги MAPI откройте один или несколько контейнеров адресной книги, чтобы получить доступ к получателям в них.</span><span class="sxs-lookup"><span data-stu-id="a73fb-105">After opening the MAPI integrated address book, open one or more address book containers to access the recipients within them.</span></span>
  
<span data-ttu-id="a73fb-106">Чтобы открыть контейнер адресной книги верхнего уровня, позвоните [в IAddrBook::OpenEntry](iaddrbook-openentry.md) с идентификатором записи NULL.</span><span class="sxs-lookup"><span data-stu-id="a73fb-106">To open the top-level container of the address book, call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier.</span></span> 
  
<span data-ttu-id="a73fb-107">Контейнеры адресных книг можно реализовать только для чтения или чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a73fb-107">Address book containers can be implemented with read-only or read/write access.</span></span> <span data-ttu-id="a73fb-108">Контейнеры только для чтения используются только для просмотра.</span><span class="sxs-lookup"><span data-stu-id="a73fb-108">Read-only containers are used only for browsing.</span></span> <span data-ttu-id="a73fb-109">Контейнеры для чтения и записи можно изменять, позволяя клиентам создавать новые записи, удалять и изменять существующие записи.</span><span class="sxs-lookup"><span data-stu-id="a73fb-109">Read/write containers can be modified, allowing clients to create new entries and delete and modify existing entries.</span></span> <span data-ttu-id="a73fb-110">Все контейнеры личной адресной книги (PAB) реализуются в качестве контейнеров для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a73fb-110">All personal address book (PAB) containers are implemented as read/write containers.</span></span> 
  
<span data-ttu-id="a73fb-111">Чтобы открыть любой контейнер нижнего уровня, позвоните **в OpenEntry** и укажите идентификатор входа для открываемого контейнера.</span><span class="sxs-lookup"><span data-stu-id="a73fb-111">To open any lower level container, call **OpenEntry** and specify the entry identifier of the container to be opened.</span></span> 
  
## <a name="open-the-container-designated-as-the-pab"></a><span data-ttu-id="a73fb-112">Откройте контейнер, назначенный как PAB</span><span class="sxs-lookup"><span data-stu-id="a73fb-112">Open the container designated as the PAB</span></span>
  
1. <span data-ttu-id="a73fb-113">Позвоните [в IAddrBook::GetPAB,](iaddrbook-getpab.md) чтобы получить идентификатор записи PAB.</span><span class="sxs-lookup"><span data-stu-id="a73fb-113">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the PAB's entry identifier.</span></span> 
    
2. <span data-ttu-id="a73fb-114">Передай этот идентификатор [записи в IAddrBook::OpenEntry.](iaddrbook-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="a73fb-114">Pass this entry identifier to [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span>
    
## <a name="open-a-container-that-is-not-the-pab"></a><span data-ttu-id="a73fb-115">Откройте контейнер, который не является PAB</span><span class="sxs-lookup"><span data-stu-id="a73fb-115">Open a container that is not the PAB</span></span>
  
1. <span data-ttu-id="a73fb-116">Вызов [IAddrBook::OpenEntry](iaddrbook-openentry.md) с идентификатором входа NULL, чтобы открыть корневой контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a73fb-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier to open the address book's root container.</span></span> 
    
2. <span data-ttu-id="a73fb-117">Чтобы получить таблицу иерархии, вызовите метод [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) — список всех контейнеров верхнего уровня в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="a73fb-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to retrieve its hierarchy table — a list of all of the top-level containers in the address book.</span></span> 
    
3. <span data-ttu-id="a73fb-118">Если открытый контейнер имеет определенный тип:</span><span class="sxs-lookup"><span data-stu-id="a73fb-118">If the container to be opened is of a specific type:</span></span>
    
   - <span data-ttu-id="a73fb-119">Создайте **структуру SPropertyRestriction** с **PR_DISPLAY_TYPE** [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)для тега свойства, типа контейнера для значения свойства и RELOP_EQ для отношения.</span><span class="sxs-lookup"><span data-stu-id="a73fb-119">Create an **SPropertyRestriction** structure with **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) for the property tag, the container's type for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="a73fb-120">**PR_DISPLAY_TYPE** можно установить множество значений, среди которых:</span><span class="sxs-lookup"><span data-stu-id="a73fb-120">**PR_DISPLAY_TYPE** can be set to many values, among them:</span></span> 
    
   - <span data-ttu-id="a73fb-121">DT_GLOBAL ограничить таблицу иерархии контейнерами, которые входят в глобальный список адресов.</span><span class="sxs-lookup"><span data-stu-id="a73fb-121">DT_GLOBAL to limit the hierarchy table to containers that belong in the global address list.</span></span>
    
   - <span data-ttu-id="a73fb-122">DT_LOCAL ограничить таблицу контейнерами, принадлежащими локальной адресной книге.</span><span class="sxs-lookup"><span data-stu-id="a73fb-122">DT_LOCAL to limit the table to containers belonging to a local address book.</span></span>
    
   - <span data-ttu-id="a73fb-123">DT_MODIFIABLE ограничить таблицу контейнерами, которые можно изменить.</span><span class="sxs-lookup"><span data-stu-id="a73fb-123">DT_MODIFIABLE to limit the table to containers that can be modified.</span></span>
    
   - <span data-ttu-id="a73fb-124">Создайте [структуру SPropTagArray,](sproptagarray.md) которая включает **PR_ENTRYID,** **PR_DISPLAY_TYPE** и любые другие столбцы, интересуя.</span><span class="sxs-lookup"><span data-stu-id="a73fb-124">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID**, **PR_DISPLAY_TYPE**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="a73fb-125">Вызов [HrQueryAllRows,](hrqueryallrows.md)передавая ограничения свойств и массив тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="a73fb-125">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="a73fb-126">**HrQueryAllRows** возвращает ноль или несколько строк, по одной строке для каждого контейнера, который принадлежит указанному типу.</span><span class="sxs-lookup"><span data-stu-id="a73fb-126">**HrQueryAllRows** will return zero or more rows, one row for every container that belongs to the specified type.</span></span> <span data-ttu-id="a73fb-127">Будьте готовы обрабатывать возврат любого количества строк.</span><span class="sxs-lookup"><span data-stu-id="a73fb-127">Be prepared to handle the return of any number of rows.</span></span> 
    
   - <span data-ttu-id="a73fb-128">**Вызывай IAddrBook::OpenEntry** с идентификатором записи из столбца PR_ENTRYID строки, которая представляет контейнер с интересом. </span><span class="sxs-lookup"><span data-stu-id="a73fb-128">Call **IAddrBook::OpenEntry** with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> 
    
4. <span data-ttu-id="a73fb-129">Если открытый контейнер принадлежит конкретному поставщику адресной книги:</span><span class="sxs-lookup"><span data-stu-id="a73fb-129">If the container to be opened belongs to a specific address book provider:</span></span>
    
   - <span data-ttu-id="a73fb-130">Создайте [структуру SPropertyRestriction](spropertyrestriction.md) с **PR_AB_PROVIDERS** [(PidTagAbProviders)](pidtagabproviders-canonical-property.md)для тега свойства, значения для поставщика для свойства и RELOP_EQ для отношения.</span><span class="sxs-lookup"><span data-stu-id="a73fb-130">Create an [SPropertyRestriction](spropertyrestriction.md) structure with **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) for the property tag, a provider-specific value for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="a73fb-131">Как правило, значение для конкретного поставщика — это глобальный уникальный идентификатор или GUID.</span><span class="sxs-lookup"><span data-stu-id="a73fb-131">Typically the provider-specific value is a globally unique identifier or GUID.</span></span> <span data-ttu-id="a73fb-132">Это значение будет опубликовано в одном из заглавных файлов поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a73fb-132">You will find this value published in one of the address book provider's header files.</span></span> 
    
   - <span data-ttu-id="a73fb-133">Создайте [структуру SPropTagArray,](sproptagarray.md) которая включает PR_ENTRYID[(PidTagEntryId),](pidtagentryid-canonical-property.md)PR_AB_PROVIDERS и любые другие столбцы, интересуя.  </span><span class="sxs-lookup"><span data-stu-id="a73fb-133">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="a73fb-134">Вызов [HrQueryAllRows,](hrqueryallrows.md)передавая ограничения свойств и массив тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="a73fb-134">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="a73fb-135">**HrQueryAllRows** возвращает нулевые строки, если указанный поставщик адресной книги не указан в профиле.</span><span class="sxs-lookup"><span data-stu-id="a73fb-135">**HrQueryAllRows** will return zero rows if the specified address book provider is not in the profile.</span></span> <span data-ttu-id="a73fb-136">Он может возвращать одну или несколько строк для контейнеров верхнего уровня поставщика в зависимости от организации поставщика.</span><span class="sxs-lookup"><span data-stu-id="a73fb-136">It can return one or more rows for the provider's top-level containers, depending on how the provider is organized.</span></span> 
    
   - <span data-ttu-id="a73fb-137">[Вызывай IAddrBook::OpenEntry](iaddrbook-openentry.md) с идентификатором записи из столбца PR_ENTRYID строки, которая представляет контейнер с интересом. </span><span class="sxs-lookup"><span data-stu-id="a73fb-137">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> <span data-ttu-id="a73fb-138">Если контейнер, который вас интересует, не является контейнером верхнего уровня, найдите контейнер верхнего уровня и перейдите по иерархии.</span><span class="sxs-lookup"><span data-stu-id="a73fb-138">If the container that you are interested in is not a top-level container, find the top-level container and traverse the hierarchy.</span></span> 
    

