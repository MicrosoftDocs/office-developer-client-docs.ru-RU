---
title: Сведения об API сведений о доступности
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: Свободен/занят API позволяет поставщиков почты для предоставления сведений о доступности состояния для заданным учетным записям пользователей в рамках в заданном диапазоне времени.
ms.openlocfilehash: 8b1559173297fbde9930b6f8f7fbc74f176273da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807677"
---
# <a name="about-the-freebusy-api"></a><span data-ttu-id="fe680-103">Сведения об API сведений о доступности</span><span class="sxs-lookup"><span data-stu-id="fe680-103">About the Free/Busy API</span></span>

<span data-ttu-id="fe680-104">Свободен/занят API позволяет поставщиков почты для предоставления сведений о доступности состояния для заданным учетным записям пользователей в рамках в заданном диапазоне времени.</span><span class="sxs-lookup"><span data-stu-id="fe680-104">The Free/Busy API allows mail providers to provide free/busy status information for specified user accounts within a specified time range.</span></span> <span data-ttu-id="fe680-105">Состояние занятости интервал времени в календаре пользователя — одно из следующих значений: документов office, «занят», под вопросом или бесплатное.</span><span class="sxs-lookup"><span data-stu-id="fe680-105">The free/busy status of a block of time on a user's calendar is one of the following: out-of-office, busy, tentative, or free.</span></span>
  
## <a name="create-a-freebusy-provider"></a><span data-ttu-id="fe680-106">Создание поставщика сведений о доступности</span><span class="sxs-lookup"><span data-stu-id="fe680-106">Create a free/busy provider</span></span>

<span data-ttu-id="fe680-107">Для предоставления сведений о доступности для пользователей почты, поставщик почты создает поставщика сведений о доступности и регистрирует его с помощью Outlook.</span><span class="sxs-lookup"><span data-stu-id="fe680-107">To provide free/busy information to mail users, a mail provider creates a free/busy provider and registers it with Outlook.</span></span> <span data-ttu-id="fe680-108">Поставщик занятости должен реализовывать следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="fe680-108">The free/busy provider must implement the following interfaces.</span></span> <span data-ttu-id="fe680-109">Обратите внимание, что число элементов в этих интерфейсов, не поддерживается и должен возвращать указанного возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="fe680-109">Note that a number of members in these interfaces are not supported and must return the specified return values.</span></span> <span data-ttu-id="fe680-110">В частности о доступности API не поддерживает доступ на запись к сведения о доступности и передача прав доступа к учетным записям.</span><span class="sxs-lookup"><span data-stu-id="fe680-110">In particular, the Free/Busy API does not support write access to free/busy information and delegate access to accounts.</span></span>
  
- <span data-ttu-id="fe680-111">[IFreeBusySupport](ifreebusysupport.md) — этот интерфейс поддерживает спецификации интерфейсов, доступ к сведениям о доступности данных для указанных пользователей.</span><span class="sxs-lookup"><span data-stu-id="fe680-111">[IFreeBusySupport](ifreebusysupport.md) —This interface supports specification of interfaces that access free/busy data for specified users.</span></span> <span data-ttu-id="fe680-112">[FBUser](fbuser.md) используется для идентификации пользователя.</span><span class="sxs-lookup"><span data-stu-id="fe680-112">It uses [FBUser](fbuser.md) to identify a user.</span></span> 
    
- <span data-ttu-id="fe680-113">[IFreeBusyData](ifreebusydata.md) — этот интерфейс возвращает и задает диапазон времени для определенного пользователя и возвращает интерфейс для перечисления сведений о доступности блоков данных в пределах этого диапазона времени.</span><span class="sxs-lookup"><span data-stu-id="fe680-113">[IFreeBusyData](ifreebusydata.md) —This interface gets and sets a time range for a given user and returns an interface for enumerating free/busy blocks of data within this time range.</span></span> <span data-ttu-id="fe680-114">Относительное время используется для получения и задания этот диапазон времени.</span><span class="sxs-lookup"><span data-stu-id="fe680-114">It uses relative time to get and set this time range.</span></span> <span data-ttu-id="fe680-115">Дополнительные сведения можно [Использовать относительное время для доступа к сведениям о доступности данных](how-to-use-relative-time-to-access-free-busy-data.md).</span><span class="sxs-lookup"><span data-stu-id="fe680-115">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
- <span data-ttu-id="fe680-116">[IEnumFBBlock](ienumfbblock.md) — этот интерфейс поддерживает доступ к и перечисление занятости блоков данных для пользователя в интервал времени.</span><span class="sxs-lookup"><span data-stu-id="fe680-116">[IEnumFBBlock](ienumfbblock.md) —This interface supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="fe680-117">Перечисление содержит блоки сведениям о доступности, которые указывают состояние занятости периодов времени в календаре пользователя, в интервал времени (указывается с [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span><span class="sxs-lookup"><span data-stu-id="fe680-117">An enumeration contains free/busy blocks that indicate the free/busy status of periods of time on a user's calendar, within a time range (specified by [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span></span> <span data-ttu-id="fe680-118">Элементы в календаре, например, встреч и приглашений на собрания, формирующие блоки в перечислении.</span><span class="sxs-lookup"><span data-stu-id="fe680-118">Items on a calendar, such as appointments and meeting requests, form blocks in the enumeration.</span></span> <span data-ttu-id="fe680-119">Элементы, которые располагаются вплотную друг с другом в календаре и с таким же статусом занятости объединяются форме одну один блок.</span><span class="sxs-lookup"><span data-stu-id="fe680-119">Items that are adjacent to one another on the calendar and have the same free/busy status are combined to form one single block.</span></span> <span data-ttu-id="fe680-120">Бесплатная период времени в календаре также форм блока.</span><span class="sxs-lookup"><span data-stu-id="fe680-120">A free period of time on a calendar also forms a block.</span></span> <span data-ttu-id="fe680-121">Таким образом не два последовательных блоков в перечислении будет иметь же состояние сведений о доступности.</span><span class="sxs-lookup"><span data-stu-id="fe680-121">Therefore, no two consecutive blocks in an enumeration would have the same free/busy status.</span></span> <span data-ttu-id="fe680-122">Эти блоки не перекрывались времени.</span><span class="sxs-lookup"><span data-stu-id="fe680-122">These blocks do not overlap in time.</span></span> <span data-ttu-id="fe680-123">Если есть перекрывающиеся элементы календаря, Outlook объединяет эти элементы для без перекрытия блоков сведений о доступности в перечисление, основанное на этом приоритет: документов office, «занят», под вопросом.</span><span class="sxs-lookup"><span data-stu-id="fe680-123">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span> 
  
<span data-ttu-id="fe680-124">Чтобы зарегистрировать поставщик сведениям о доступности с помощью Outlook, поставщик почты должен выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="fe680-124">To register the free/busy provider with Outlook, the mail provider should do the following:</span></span>
  
1. <span data-ttu-id="fe680-125">Зарегистрируйте поставщика занятости COM, предоставляя CLSID, который позволяет получить доступ к реализации поставщика **IFreeBusySupport**.</span><span class="sxs-lookup"><span data-stu-id="fe680-125">Register the free/busy provider with COM, providing a CLSID that allows access to the provider's implementation of **IFreeBusySupport**.</span></span> 
    
2. <span data-ttu-id="fe680-126">Программа Outlook знать, что поставщик занятости существует, установив следующий раздел (где `<xx.x>` представляет версию Outlook) в системном реестре:</span><span class="sxs-lookup"><span data-stu-id="fe680-126">Let Outlook know that the free/busy provider exists by setting the following key (where `<xx.x>` represents the version of Outlook) in the system registry:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   <span data-ttu-id="fe680-127">Например если поставщика транспорта SMTP, чтобы зарегистрировать поставщик с помощью Microsoft Outlook 2010 установите следующий раздел к данным в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="fe680-127">For example, if the transport provider is SMTP, to register the provider with Microsoft Outlook 2010, set the following key to the data in the following table:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |<span data-ttu-id="fe680-128">Имя</span><span class="sxs-lookup"><span data-stu-id="fe680-128">Name</span></span> |<span data-ttu-id="fe680-129">Тип</span><span class="sxs-lookup"><span data-stu-id="fe680-129">Type</span></span> |<span data-ttu-id="fe680-130">Значение</span><span class="sxs-lookup"><span data-stu-id="fe680-130">Value</span></span> |
   |:-----|:-----|:-----|
   |<span data-ttu-id="fe680-131">SMTP</span><span class="sxs-lookup"><span data-stu-id="fe680-131">SMTP</span></span>  |<span data-ttu-id="fe680-132">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="fe680-132">REG_SZ</span></span>  |<span data-ttu-id="fe680-133">{CLSID для соответствующих реализации IFreeBusySupport}</span><span class="sxs-lookup"><span data-stu-id="fe680-133">{CLSID for respective implementation of IFreeBusySupport}</span></span>  |
   
   <span data-ttu-id="fe680-134">В этом сценарии Outlook совместно создает класс COM и используется для получения сведений о доступности для всех пользователей почты SMTP.</span><span class="sxs-lookup"><span data-stu-id="fe680-134">In this scenario, Outlook co-creates the COM class and uses it to retrieve free/busy information for any SMTP mail users.</span></span>
    
<span data-ttu-id="fe680-135">Чтобы обеспечить поддержку адресной книги и транспорта поставщик, использовать запись адреса, отличного от SMTP, соответствующим образом измените *имя* .</span><span class="sxs-lookup"><span data-stu-id="fe680-135">To support an address book and transport provider that use an address entry type other than SMTP, change the  *Name* accordingly.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fe680-136">Во время установки, занятости поставщиков должен проверить, будет ли параметров реестра для того же типа записи адресов уже существует.</span><span class="sxs-lookup"><span data-stu-id="fe680-136">During installation, free/busy providers should check whether a registry setting for the the same address entry type already exists.</span></span> <span data-ttu-id="fe680-137">Если это так, поставщика сведениям о доступности следует перезапись текущего поставщика для этого типа адреса запись и восстановление этому поставщику во время удаления.</span><span class="sxs-lookup"><span data-stu-id="fe680-137">If it does, the free/busy provider should overwrite the current provider for that address entry type, and restore to that provider when it uninstalls.</span></span> <span data-ttu-id="fe680-138">Тем не менее, если пользователь установил более одного поставщика сведений о доступности для того же типа запись адреса, пользователя следует удалить эти поставщиков в порядке, обратном порядку установки (то есть, всегда удаление последних поставщика).</span><span class="sxs-lookup"><span data-stu-id="fe680-138">However, if a user has installed more than one free/busy provider for the same address entry type, the user should uninstall these providers in the reverse order as installation (that is, always uninstall the latest provider).</span></span> <span data-ttu-id="fe680-139">В противном случае реестра могут указывать поставщика, который уже удалено.</span><span class="sxs-lookup"><span data-stu-id="fe680-139">Otherwise, the registry may point to a provider that has already been uninstalled.</span></span> 
  
## <a name="api-components"></a><span data-ttu-id="fe680-140">Компоненты API</span><span class="sxs-lookup"><span data-stu-id="fe680-140">API components</span></span>

<span data-ttu-id="fe680-141">Свободен/занят API включает в себя следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="fe680-141">The Free/Busy API includes the following components:</span></span>
  
### <a name="definitions"></a><span data-ttu-id="fe680-142">Определения</span><span class="sxs-lookup"><span data-stu-id="fe680-142">Definitions</span></span>

- [<span data-ttu-id="fe680-143">Константы (занятости API)</span><span class="sxs-lookup"><span data-stu-id="fe680-143">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
    
### <a name="data-types"></a><span data-ttu-id="fe680-144">Типы данных</span><span class="sxs-lookup"><span data-stu-id="fe680-144">Data types</span></span>

- [<span data-ttu-id="fe680-145">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="fe680-145">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="fe680-146">FBStatus</span><span class="sxs-lookup"><span data-stu-id="fe680-146">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="fe680-147">FBUser</span><span class="sxs-lookup"><span data-stu-id="fe680-147">FBUser</span></span>](fbuser.md)
    
### <a name="interfaces"></a><span data-ttu-id="fe680-148">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="fe680-148">Interfaces</span></span>

- [<span data-ttu-id="fe680-149">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="fe680-149">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="fe680-150">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="fe680-150">IFreeBusyData</span></span>](ifreebusydata.md)
- [<span data-ttu-id="fe680-151">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="fe680-151">IFreeBusySupport</span></span>](ifreebusysupport.md)
    

