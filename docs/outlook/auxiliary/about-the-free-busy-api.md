---
title: Сведения об API сведений о доступности
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: API сведений о занятости позволяет поставщикам почты предоставлять сведения о занятости для указанных учетных записей пользователей в заданный период времени.
ms.openlocfilehash: 1bcd191b57238771ede6f035216fe3997e82e03a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433761"
---
# <a name="about-the-freebusy-api"></a><span data-ttu-id="39f73-103">Сведения об API сведений о доступности</span><span class="sxs-lookup"><span data-stu-id="39f73-103">About the Free/Busy API</span></span>

<span data-ttu-id="39f73-104">API сведений о занятости позволяет поставщикам почты предоставлять сведения о занятости для указанных учетных записей пользователей в заданный период времени.</span><span class="sxs-lookup"><span data-stu-id="39f73-104">The Free/Busy API allows mail providers to provide free/busy status information for specified user accounts within a specified time range.</span></span> <span data-ttu-id="39f73-105">Состояние занятости блока времени в календаре пользователя может быть одним из следующих: "нет на офисе", "занят", "под вопросом" или "свободен".</span><span class="sxs-lookup"><span data-stu-id="39f73-105">The free/busy status of a block of time on a user's calendar is one of the following: out-of-office, busy, tentative, or free.</span></span>
  
## <a name="create-a-freebusy-provider"></a><span data-ttu-id="39f73-106">Создание поставщика услуг занятости</span><span class="sxs-lookup"><span data-stu-id="39f73-106">Create a free/busy provider</span></span>

<span data-ttu-id="39f73-107">Чтобы предоставить пользователям почты сведения о занятости, поставщик почты создает поставщика услуг занятости и регистрирует его в Outlook.</span><span class="sxs-lookup"><span data-stu-id="39f73-107">To provide free/busy information to mail users, a mail provider creates a free/busy provider and registers it with Outlook.</span></span> <span data-ttu-id="39f73-108">Поставщик услуг занятости должен реализовать следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="39f73-108">The free/busy provider must implement the following interfaces.</span></span> <span data-ttu-id="39f73-109">Обратите внимание, что некоторые члены в этих интерфейсах не поддерживаются и должны возвращать указанные возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="39f73-109">Note that a number of members in these interfaces are not supported and must return the specified return values.</span></span> <span data-ttu-id="39f73-110">В частности, API занятости не поддерживает доступ на запись к сведениям о доступности и делегирование доступа к учетным записям.</span><span class="sxs-lookup"><span data-stu-id="39f73-110">In particular, the Free/Busy API does not support write access to free/busy information and delegate access to accounts.</span></span>
  
- <span data-ttu-id="39f73-111">[IFreeBusySupport](ifreebusysupport.md) — этот интерфейс поддерживает спецификацию интерфейсов, которые имеют доступ к сведениям о доступности для указанных пользователей.</span><span class="sxs-lookup"><span data-stu-id="39f73-111">[IFreeBusySupport](ifreebusysupport.md) —This interface supports specification of interfaces that access free/busy data for specified users.</span></span> <span data-ttu-id="39f73-112">Для [идентификации пользователя используется FBUser.](fbuser.md)</span><span class="sxs-lookup"><span data-stu-id="39f73-112">It uses [FBUser](fbuser.md) to identify a user.</span></span> 
    
- <span data-ttu-id="39f73-113">[IFreeBusyData](ifreebusydata.md) — этот интерфейс получает и задает диапазон времени для данного пользователя и возвращает интерфейс для нумерации блоков данных о занятости в пределах этого диапазона времени.</span><span class="sxs-lookup"><span data-stu-id="39f73-113">[IFreeBusyData](ifreebusydata.md) —This interface gets and sets a time range for a given user and returns an interface for enumerating free/busy blocks of data within this time range.</span></span> <span data-ttu-id="39f73-114">Для получения и применения этого диапазона времени используется относительное время.</span><span class="sxs-lookup"><span data-stu-id="39f73-114">It uses relative time to get and set this time range.</span></span> <span data-ttu-id="39f73-115">Дополнительные сведения см. в сведениях [об использовании относительного времени для доступа к сведениям о доступности.](how-to-use-relative-time-to-access-free-busy-data.md)</span><span class="sxs-lookup"><span data-stu-id="39f73-115">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
- <span data-ttu-id="39f73-116">[IEnumFBBlock](ienumfbblock.md) — этот интерфейс поддерживает доступ к блокам данных о доступности и их нумерации для пользователя в течение задающегося диапазона времени.</span><span class="sxs-lookup"><span data-stu-id="39f73-116">[IEnumFBBlock](ienumfbblock.md) —This interface supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="39f73-117">Enumeration contains free/busy blocks that indicate the free/busy status of periods of time on a user's calendar, within a time range (specified by [IFreeBusyData::EnumBlocks).](ifreebusydata-enumblocks.md)</span><span class="sxs-lookup"><span data-stu-id="39f73-117">An enumeration contains free/busy blocks that indicate the free/busy status of periods of time on a user's calendar, within a time range (specified by [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span></span> <span data-ttu-id="39f73-118">Элементы в календаре, такие как встречи и запросы на собрания, блоки формы в этом нумерации.</span><span class="sxs-lookup"><span data-stu-id="39f73-118">Items on a calendar, such as appointments and meeting requests, form blocks in the enumeration.</span></span> <span data-ttu-id="39f73-119">Элементы, которые находятся рядом друг с другом в календаре и имеют одинаковое состояние занятости, объединяются в один блок.</span><span class="sxs-lookup"><span data-stu-id="39f73-119">Items that are adjacent to one another on the calendar and have the same free/busy status are combined to form one single block.</span></span> <span data-ttu-id="39f73-120">Бесплатный период времени в календаре также формирует блок.</span><span class="sxs-lookup"><span data-stu-id="39f73-120">A free period of time on a calendar also forms a block.</span></span> <span data-ttu-id="39f73-121">Таким образом, два последовательных блока в нумерации не будут иметь одинаковое состояние занятости.</span><span class="sxs-lookup"><span data-stu-id="39f73-121">Therefore, no two consecutive blocks in an enumeration would have the same free/busy status.</span></span> <span data-ttu-id="39f73-122">Эти блоки не перекрываются во времени.</span><span class="sxs-lookup"><span data-stu-id="39f73-122">These blocks do not overlap in time.</span></span> <span data-ttu-id="39f73-123">Если в календаре имеются перекрывающиеся элементы, Outlook объединяет эти элементы для формирования не перекрывающихся блоков занятости и занятости в порядке приоритета: "нет на офисе", "занят", "под вопросом".</span><span class="sxs-lookup"><span data-stu-id="39f73-123">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span> 
  
<span data-ttu-id="39f73-124">Чтобы зарегистрировать поставщика услуг занятости в Outlook, поставщик почты должен сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="39f73-124">To register the free/busy provider with Outlook, the mail provider should do the following:</span></span>
  
1. <span data-ttu-id="39f73-125">Зарегистрируйте поставщика услуг занятости в COM, предоставив CLSID, который предоставляет доступ к реализации **IFreeBusySupport** поставщиком.</span><span class="sxs-lookup"><span data-stu-id="39f73-125">Register the free/busy provider with COM, providing a CLSID that allows access to the provider's implementation of **IFreeBusySupport**.</span></span> 
    
2. <span data-ttu-id="39f73-126">Let Outlook know that the free/busy provider exists by setting the following key (where `<xx.x>` represents the version of Outlook) in the system registry:</span><span class="sxs-lookup"><span data-stu-id="39f73-126">Let Outlook know that the free/busy provider exists by setting the following key (where `<xx.x>` represents the version of Outlook) in the system registry:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   <span data-ttu-id="39f73-127">Например, если поставщиком транспорта является SMTP, чтобы зарегистрировать его в Microsoft Outlook 2010, русская версия, установите следующий ключ для данных в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="39f73-127">For example, if the transport provider is SMTP, to register the provider with Microsoft Outlook 2010, set the following key to the data in the following table:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |<span data-ttu-id="39f73-128">Имя</span><span class="sxs-lookup"><span data-stu-id="39f73-128">Name</span></span> |<span data-ttu-id="39f73-129">Тип</span><span class="sxs-lookup"><span data-stu-id="39f73-129">Type</span></span> |<span data-ttu-id="39f73-130">Значение</span><span class="sxs-lookup"><span data-stu-id="39f73-130">Value</span></span> |
   |:-----|:-----|:-----|
   |<span data-ttu-id="39f73-131">SMTP</span><span class="sxs-lookup"><span data-stu-id="39f73-131">SMTP</span></span>  |<span data-ttu-id="39f73-132">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="39f73-132">REG_SZ</span></span>  |<span data-ttu-id="39f73-133">{CLSID для соответствующей реализации IFreeBusySupport}</span><span class="sxs-lookup"><span data-stu-id="39f73-133">{CLSID for respective implementation of IFreeBusySupport}</span></span>  |
   
   <span data-ttu-id="39f73-134">В этом сценарии Outlook совместно создает класс COM и использует его для получения сведений о занятости для всех пользователей почты SMTP.</span><span class="sxs-lookup"><span data-stu-id="39f73-134">In this scenario, Outlook co-creates the COM class and uses it to retrieve free/busy information for any SMTP mail users.</span></span>
    
<span data-ttu-id="39f73-135">Для поддержки адресной книги и поставщика транспорта, которые используют тип записи адреса, кроме SMTP, измените  *имя* соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="39f73-135">To support an address book and transport provider that use an address entry type other than SMTP, change the  *Name* accordingly.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="39f73-136">Во время установки поставщики услуг занятости должны проверить, существует ли параметр реестра для того же типа записи адреса.</span><span class="sxs-lookup"><span data-stu-id="39f73-136">During installation, free/busy providers should check whether a registry setting for the the same address entry type already exists.</span></span> <span data-ttu-id="39f73-137">В этом случае поставщик услуг занятости должен переописать текущего поставщика для этого типа записи адреса и восстановить его при его восстановлении.</span><span class="sxs-lookup"><span data-stu-id="39f73-137">If it does, the free/busy provider should overwrite the current provider for that address entry type, and restore to that provider when it uninstalls.</span></span> <span data-ttu-id="39f73-138">Однако если пользователь установил несколько поставщиков услуг занятости для одного типа записи адреса, он должен удалить этих поставщиков в обратном порядке в качестве установки (то есть всегда удалить последнего поставщика).</span><span class="sxs-lookup"><span data-stu-id="39f73-138">However, if a user has installed more than one free/busy provider for the same address entry type, the user should uninstall these providers in the reverse order as installation (that is, always uninstall the latest provider).</span></span> <span data-ttu-id="39f73-139">В противном случае реестр может указать на поставщика, который уже был установлен.</span><span class="sxs-lookup"><span data-stu-id="39f73-139">Otherwise, the registry may point to a provider that has already been uninstalled.</span></span> 
  
## <a name="api-components"></a><span data-ttu-id="39f73-140">Компоненты API</span><span class="sxs-lookup"><span data-stu-id="39f73-140">API components</span></span>

<span data-ttu-id="39f73-141">API занятости включает следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="39f73-141">The Free/Busy API includes the following components:</span></span>
  
### <a name="definitions"></a><span data-ttu-id="39f73-142">Определения</span><span class="sxs-lookup"><span data-stu-id="39f73-142">Definitions</span></span>

- [<span data-ttu-id="39f73-143">Constants (Free/busy API)</span><span class="sxs-lookup"><span data-stu-id="39f73-143">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
    
### <a name="data-types"></a><span data-ttu-id="39f73-144">Типы данных</span><span class="sxs-lookup"><span data-stu-id="39f73-144">Data types</span></span>

- [<span data-ttu-id="39f73-145">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="39f73-145">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="39f73-146">FBStatus</span><span class="sxs-lookup"><span data-stu-id="39f73-146">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="39f73-147">FBUser</span><span class="sxs-lookup"><span data-stu-id="39f73-147">FBUser</span></span>](fbuser.md)
    
### <a name="interfaces"></a><span data-ttu-id="39f73-148">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="39f73-148">Interfaces</span></span>

- [<span data-ttu-id="39f73-149">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="39f73-149">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="39f73-150">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="39f73-150">IFreeBusyData</span></span>](ifreebusydata.md)
- [<span data-ttu-id="39f73-151">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="39f73-151">IFreeBusySupport</span></span>](ifreebusysupport.md)
    

