---
title: Открытие контейнер адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: 'Последнее изменение: 08 ноября 2011 г.'
ms.openlocfilehash: 28f60154524065bd2c818e2e4b7db37ca33276b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810067"
---
# <a name="opening-an-address-book-container"></a><span data-ttu-id="f352a-103">Открытие контейнер адресной книги</span><span class="sxs-lookup"><span data-stu-id="f352a-103">Opening an address book container</span></span>

<span data-ttu-id="f352a-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f352a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f352a-105">После открытия MAPI интегрированное адресную книгу, откройте один или несколько контейнеров адресной книги для доступа к получателям внутри них.</span><span class="sxs-lookup"><span data-stu-id="f352a-105">After opening the MAPI integrated address book, open one or more address book containers to access the recipients within them.</span></span>
  
<span data-ttu-id="f352a-106">Чтобы открыть верхнего уровня контейнер адресной книги, вызовите [IAddrBook::OpenEntry](iaddrbook-openentry.md) с идентификатором записи NULL.</span><span class="sxs-lookup"><span data-stu-id="f352a-106">To open the top-level container of the address book, call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier.</span></span> 
  
<span data-ttu-id="f352a-107">Контейнеры адресной книги можно реализовать с помощью только для чтения или чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f352a-107">Address book containers can be implemented with read-only or read/write access.</span></span> <span data-ttu-id="f352a-108">Контейнеры только для чтения, используются только для просмотра.</span><span class="sxs-lookup"><span data-stu-id="f352a-108">Read-only containers are used only for browsing.</span></span> <span data-ttu-id="f352a-109">Чтение и запись контейнеров может быть изменено, позволяя клиентам для создания новых записей и удаления и изменения существующих записей.</span><span class="sxs-lookup"><span data-stu-id="f352a-109">Read/write containers can be modified, allowing clients to create new entries and delete and modify existing entries.</span></span> <span data-ttu-id="f352a-110">Все контейнеров адресной книге пользователя реализованы в виде контейнеров чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f352a-110">All personal address book (PAB) containers are implemented as read/write containers.</span></span> 
  
<span data-ttu-id="f352a-111">Для открытия любого нижнего уровня контейнера, вызовите **OpenEntry** и укажите идентификатор записи контейнера для открытия.</span><span class="sxs-lookup"><span data-stu-id="f352a-111">To open any lower level container, call **OpenEntry** and specify the entry identifier of the container to be opened.</span></span> 
  
## <a name="open-the-container-designated-as-the-pab"></a><span data-ttu-id="f352a-112">Откройте контейнер обозначены как личной адресной книги</span><span class="sxs-lookup"><span data-stu-id="f352a-112">Open the container designated as the PAB</span></span>
  
1. <span data-ttu-id="f352a-113">Вызовите [IAddrBook::GetPAB](iaddrbook-getpab.md) , чтобы получить идентификатор записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="f352a-113">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the PAB's entry identifier.</span></span> 
    
2. <span data-ttu-id="f352a-114">Передайте этот идентификатор записи [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="f352a-114">Pass this entry identifier to [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span>
    
## <a name="open-a-container-that-is-not-the-pab"></a><span data-ttu-id="f352a-115">Откройте контейнер, который не является личной адресной книги</span><span class="sxs-lookup"><span data-stu-id="f352a-115">Open a container that is not the PAB</span></span>
  
1. <span data-ttu-id="f352a-116">Вызов [IAddrBook::OpenEntry](iaddrbook-openentry.md) с идентификатором записи NULL для открытия корневой контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="f352a-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier to open the address book's root container.</span></span> 
    
2. <span data-ttu-id="f352a-117">Вызовите метод [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) корневой контейнер для получения его иерархии таблицы — список всех контейнеров верхнего уровня в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="f352a-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to retrieve its hierarchy table — a list of all of the top-level containers in the address book.</span></span> 
    
3. <span data-ttu-id="f352a-118">Если контейнер для открытия определенного типа:</span><span class="sxs-lookup"><span data-stu-id="f352a-118">If the container to be opened is of a specific type:</span></span>
    
   - <span data-ttu-id="f352a-119">Создайте структуру **SPropertyRestriction** с **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) для тега свойства, типа контейнера значение свойства и RELOP_EQ для связи.</span><span class="sxs-lookup"><span data-stu-id="f352a-119">Create an **SPropertyRestriction** structure with **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) for the property tag, the container's type for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="f352a-120">**PR_DISPLAY_TYPE** можно установить множество значений, между ними.</span><span class="sxs-lookup"><span data-stu-id="f352a-120">**PR_DISPLAY_TYPE** can be set to many values, among them:</span></span> 
    
   - <span data-ttu-id="f352a-121">DT_GLOBAL для ограничения таблицы иерархии контейнеров, входящие в глобальном списке адресов.</span><span class="sxs-lookup"><span data-stu-id="f352a-121">DT_GLOBAL to limit the hierarchy table to containers that belong in the global address list.</span></span>
    
   - <span data-ttu-id="f352a-122">DT_LOCAL для ограничения таблице для контейнеров, относящегося к локальной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="f352a-122">DT_LOCAL to limit the table to containers belonging to a local address book.</span></span>
    
   - <span data-ttu-id="f352a-123">DT_MODIFIABLE для ограничения таблице для контейнеров, которые могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="f352a-123">DT_MODIFIABLE to limit the table to containers that can be modified.</span></span>
    
   - <span data-ttu-id="f352a-124">Создание структуры [SPropTagArray](sproptagarray.md) , который включает в себя **PR_ENTRYID**, **PR_DISPLAY_TYPE**и другие столбцы интересов.</span><span class="sxs-lookup"><span data-stu-id="f352a-124">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID**, **PR_DISPLAY_TYPE**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="f352a-125">Вызовите [HrQueryAllRows](hrqueryallrows.md), передав ограничение свойства и свойства tag массива.</span><span class="sxs-lookup"><span data-stu-id="f352a-125">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="f352a-126">**HrQueryAllRows** возвращает ноль или несколько строк, одна строка для каждого контейнера, к которой принадлежит указанный тип.</span><span class="sxs-lookup"><span data-stu-id="f352a-126">**HrQueryAllRows** will return zero or more rows, one row for every container that belongs to the specified type.</span></span> <span data-ttu-id="f352a-127">Подготовиться к обработке return любое число строк.</span><span class="sxs-lookup"><span data-stu-id="f352a-127">Be prepared to handle the return of any number of rows.</span></span> 
    
   - <span data-ttu-id="f352a-128">Вызов **IAddrBook::OpenEntry** с идентификатором записи из столбца **PR_ENTRYID** строку, которая представляет контейнер интересов.</span><span class="sxs-lookup"><span data-stu-id="f352a-128">Call **IAddrBook::OpenEntry** with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> 
    
4. <span data-ttu-id="f352a-129">Если контейнер для открытия относится к определенным адресной книге:</span><span class="sxs-lookup"><span data-stu-id="f352a-129">If the container to be opened belongs to a specific address book provider:</span></span>
    
   - <span data-ttu-id="f352a-130">Создайте структуру [SPropertyRestriction](spropertyrestriction.md) с **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) для тега свойства, значение от поставщика для значения свойства и RELOP_EQ для связи.</span><span class="sxs-lookup"><span data-stu-id="f352a-130">Create an [SPropertyRestriction](spropertyrestriction.md) structure with **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) for the property tag, a provider-specific value for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="f352a-131">Обычно значение от поставщика — это глобальный уникальный идентификатор или идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="f352a-131">Typically the provider-specific value is a globally unique identifier or GUID.</span></span> <span data-ttu-id="f352a-132">Можно найти это значение, опубликованной в один из файлов заголовка поставщик адресной книги.</span><span class="sxs-lookup"><span data-stu-id="f352a-132">You will find this value published in one of the address book provider's header files.</span></span> 
    
   - <span data-ttu-id="f352a-133">Создание структуры [SPropTagArray](sproptagarray.md) , который включает в себя **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**и другие столбцы интересов.</span><span class="sxs-lookup"><span data-stu-id="f352a-133">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="f352a-134">Вызовите [HrQueryAllRows](hrqueryallrows.md), передав ограничение свойства и свойства tag массива.</span><span class="sxs-lookup"><span data-stu-id="f352a-134">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="f352a-135">**HrQueryAllRows** возвращает нуль строк, если поставщик указанного адресной книги не входит в профиле.</span><span class="sxs-lookup"><span data-stu-id="f352a-135">**HrQueryAllRows** will return zero rows if the specified address book provider is not in the profile.</span></span> <span data-ttu-id="f352a-136">Возвращается одна или несколько строк для контейнеров поставщика верхнего уровня, в зависимости от того, как организованы поставщика.</span><span class="sxs-lookup"><span data-stu-id="f352a-136">It can return one or more rows for the provider's top-level containers, depending on how the provider is organized.</span></span> 
    
   - <span data-ttu-id="f352a-137">Вызов [IAddrBook::OpenEntry](iaddrbook-openentry.md) с идентификатором записи из столбца **PR_ENTRYID** строку, которая представляет контейнер интересов.</span><span class="sxs-lookup"><span data-stu-id="f352a-137">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> <span data-ttu-id="f352a-138">Если контейнер, в котором вы заинтересованы в не является контейнером верхнего уровня, найдите контейнер верхнего уровня и проходят через иерархии.</span><span class="sxs-lookup"><span data-stu-id="f352a-138">If the container that you are interested in is not a top-level container, find the top-level container and traverse the hierarchy.</span></span> 
    

