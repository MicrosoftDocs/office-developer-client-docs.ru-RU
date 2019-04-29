---
title: Открытие контейнера адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: 'Дата последнего изменения: 08 ноября 2011 г.'
ms.openlocfilehash: 97fa9f9750174c112c431c62f6171f674856fa86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436743"
---
# <a name="opening-an-address-book-container"></a><span data-ttu-id="09768-103">Открытие контейнера адресной книги</span><span class="sxs-lookup"><span data-stu-id="09768-103">Opening an address book container</span></span>

<span data-ttu-id="09768-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09768-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09768-105">После открытия встроенной адресной книги MAPI откройте один или несколько контейнеров адресных книг, чтобы получить доступ к получателям в них.</span><span class="sxs-lookup"><span data-stu-id="09768-105">After opening the MAPI integrated address book, open one or more address book containers to access the recipients within them.</span></span>
  
<span data-ttu-id="09768-106">Чтобы открыть контейнер верхнего уровня адресной книги, вызовите [IAddrBook:: OpenEntry](iaddrbook-openentry.md) с идентификатором записи null.</span><span class="sxs-lookup"><span data-stu-id="09768-106">To open the top-level container of the address book, call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier.</span></span> 
  
<span data-ttu-id="09768-107">Контейнеры адресной книги могут быть реализованы с доступом только для чтения или для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="09768-107">Address book containers can be implemented with read-only or read/write access.</span></span> <span data-ttu-id="09768-108">Контейнеры, доступные только для чтения, используются только для просмотра.</span><span class="sxs-lookup"><span data-stu-id="09768-108">Read-only containers are used only for browsing.</span></span> <span data-ttu-id="09768-109">Можно изменять контейнеры для чтения и записи, позволяя клиентам создавать новые записи, а также удалять и изменять существующие.</span><span class="sxs-lookup"><span data-stu-id="09768-109">Read/write containers can be modified, allowing clients to create new entries and delete and modify existing entries.</span></span> <span data-ttu-id="09768-110">Все контейнеры личной адресной книги (PAB) реализуются как контейнеры для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="09768-110">All personal address book (PAB) containers are implemented as read/write containers.</span></span> 
  
<span data-ttu-id="09768-111">Чтобы открыть контейнер нижнего уровня, вызовите **OpenEntry** и укажите идентификатор записи для открываемого контейнера.</span><span class="sxs-lookup"><span data-stu-id="09768-111">To open any lower level container, call **OpenEntry** and specify the entry identifier of the container to be opened.</span></span> 
  
## <a name="open-the-container-designated-as-the-pab"></a><span data-ttu-id="09768-112">Открытие контейнера, назначенного в качестве личной АДРЕСНОЙ книги</span><span class="sxs-lookup"><span data-stu-id="09768-112">Open the container designated as the PAB</span></span>
  
1. <span data-ttu-id="09768-113">Call [IAddrBook:: жетпаб](iaddrbook-getpab.md) для получения идентификатора записи личной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="09768-113">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the PAB's entry identifier.</span></span> 
    
2. <span data-ttu-id="09768-114">Передайте этот идентификатор записи в [IAddrBook:: OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="09768-114">Pass this entry identifier to [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span>
    
## <a name="open-a-container-that-is-not-the-pab"></a><span data-ttu-id="09768-115">Открытие контейнера, не являющийся личной АДРЕСНОЙ КНИГой</span><span class="sxs-lookup"><span data-stu-id="09768-115">Open a container that is not the PAB</span></span>
  
1. <span data-ttu-id="09768-116">Call [IAddrBook:: OpenEntry](iaddrbook-openentry.md) с идентификатором записи null, чтобы открыть корневой контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="09768-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with a NULL entry identifier to open the address book's root container.</span></span> 
    
2. <span data-ttu-id="09768-117">ВыЗовите метод [IMAPIContainer:: жесиерарчитабле](imapicontainer-gethierarchytable.md) корневого контейнера, чтобы получить свою таблицу иерархии — список всех контейнеров верхнего уровня в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="09768-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to retrieve its hierarchy table — a list of all of the top-level containers in the address book.</span></span> 
    
3. <span data-ttu-id="09768-118">Если открываемый контейнер относится к определенному типу:</span><span class="sxs-lookup"><span data-stu-id="09768-118">If the container to be opened is of a specific type:</span></span>
    
   - <span data-ttu-id="09768-119">Создайте структуру **спропертирестриктион** с **пр_дисплай_типе** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) для тега свойства, тип контейнера для значения свойства и релоп_ек для отношения.</span><span class="sxs-lookup"><span data-stu-id="09768-119">Create an **SPropertyRestriction** structure with **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) for the property tag, the container's type for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="09768-120">Для **пр_дисплай_типе** можно задать множество значений, среди прочего:</span><span class="sxs-lookup"><span data-stu-id="09768-120">**PR_DISPLAY_TYPE** can be set to many values, among them:</span></span> 
    
   - <span data-ttu-id="09768-121">ДТ_ГЛОБАЛ для ограничения таблицы иерархии на контейнеры, принадлежащие глобальному списку адресов.</span><span class="sxs-lookup"><span data-stu-id="09768-121">DT_GLOBAL to limit the hierarchy table to containers that belong in the global address list.</span></span>
    
   - <span data-ttu-id="09768-122">ДТ_ЛОКАЛ для ограничения таблицы на контейнеры, принадлежащие локальной адресной книге.</span><span class="sxs-lookup"><span data-stu-id="09768-122">DT_LOCAL to limit the table to containers belonging to a local address book.</span></span>
    
   - <span data-ttu-id="09768-123">ДТ_МОДИФИАБЛЕ для ограничения таблицы на контейнеры, которые можно изменить.</span><span class="sxs-lookup"><span data-stu-id="09768-123">DT_MODIFIABLE to limit the table to containers that can be modified.</span></span>
    
   - <span data-ttu-id="09768-124">Создайте структуру [спроптагаррай](sproptagarray.md) , включающую **пр_ентрид**, **пр_дисплай_типе**и любые другие интересующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="09768-124">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID**, **PR_DISPLAY_TYPE**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="09768-125">ВыЗовите [хркуеряллровс](hrqueryallrows.md), передав ограничение свойства и массив тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="09768-125">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="09768-126">**Хркуеряллровс** возвращает ноль или более строк, по одной строке для каждого контейнера, относящегося к указанному типу.</span><span class="sxs-lookup"><span data-stu-id="09768-126">**HrQueryAllRows** will return zero or more rows, one row for every container that belongs to the specified type.</span></span> <span data-ttu-id="09768-127">Будьте готовы обрабатывать возврат любого количества строк.</span><span class="sxs-lookup"><span data-stu-id="09768-127">Be prepared to handle the return of any number of rows.</span></span> 
    
   - <span data-ttu-id="09768-128">Call **IAddrBook:: OpenEntry** с идентификатором записи из столбца **пр_ентрид** строки, представляющей интересующий контейнер.</span><span class="sxs-lookup"><span data-stu-id="09768-128">Call **IAddrBook::OpenEntry** with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> 
    
4. <span data-ttu-id="09768-129">Если открываемый контейнер принадлежит определенному поставщику адресных книг:</span><span class="sxs-lookup"><span data-stu-id="09768-129">If the container to be opened belongs to a specific address book provider:</span></span>
    
   - <span data-ttu-id="09768-130">Создайте структуру [спропертирестриктион](spropertyrestriction.md) с **пр_аб_провидерс** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) для тега свойства, зависящее от поставщика значение значения свойства и релоп_ек для отношения.</span><span class="sxs-lookup"><span data-stu-id="09768-130">Create an [SPropertyRestriction](spropertyrestriction.md) structure with **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) for the property tag, a provider-specific value for the property value, and RELOP_EQ for the relation.</span></span> <span data-ttu-id="09768-131">Обычно значение, зависящее от поставщика, является глобальным уникальным идентификатором или ИДЕНТИФИКАТОРом GUID.</span><span class="sxs-lookup"><span data-stu-id="09768-131">Typically the provider-specific value is a globally unique identifier or GUID.</span></span> <span data-ttu-id="09768-132">Вы найдете это значение, опубликованное в одном из файлов заголовков поставщика адресных книг.</span><span class="sxs-lookup"><span data-stu-id="09768-132">You will find this value published in one of the address book provider's header files.</span></span> 
    
   - <span data-ttu-id="09768-133">Создайте структуру [спроптагаррай](sproptagarray.md) , которая включает **пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **пр_аб_провидерс**и любые другие интересующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="09768-133">Create an [SPropTagArray](sproptagarray.md) structure that includes **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**, and any other columns of interest.</span></span> 
    
   - <span data-ttu-id="09768-134">ВыЗовите [хркуеряллровс](hrqueryallrows.md), передав ограничение свойства и массив тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="09768-134">Call [HrQueryAllRows](hrqueryallrows.md), passing your property restriction and property tag array.</span></span> <span data-ttu-id="09768-135">**Хркуеряллровс** возвращает нулевые строки, если указанный поставщик адресных книг отсутствует в профиле.</span><span class="sxs-lookup"><span data-stu-id="09768-135">**HrQueryAllRows** will return zero rows if the specified address book provider is not in the profile.</span></span> <span data-ttu-id="09768-136">Он может вернуть одну или несколько строк для контейнеров верхнего уровня поставщика в зависимости от способа организации поставщика.</span><span class="sxs-lookup"><span data-stu-id="09768-136">It can return one or more rows for the provider's top-level containers, depending on how the provider is organized.</span></span> 
    
   - <span data-ttu-id="09768-137">Call [IAddrBook:: OpenEntry](iaddrbook-openentry.md) с идентификатором записи из столбца **пр_ентрид** строки, представляющей интересующий контейнер.</span><span class="sxs-lookup"><span data-stu-id="09768-137">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) with the entry identifier from the **PR_ENTRYID** column of the row that represents the container of interest.</span></span> <span data-ttu-id="09768-138">Если интересующий контейнер не является контейнером верхнего уровня, найдите контейнер верхнего уровня и прохождение по иерархии.</span><span class="sxs-lookup"><span data-stu-id="09768-138">If the container that you are interested in is not a top-level container, find the top-level container and traverse the hierarchy.</span></span> 
    

