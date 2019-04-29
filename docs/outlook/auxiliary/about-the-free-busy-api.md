---
title: Сведения об API сведений о доступности
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 17c5e44e-ae56-8de7-3579-90171d996411
description: API сведений о доступности позволяет почтовым поставщикам предоставлять сведения о доступности для указанных учетных записей пользователей в указанном диапазоне времени.
ms.openlocfilehash: 1bcd191b57238771ede6f035216fe3997e82e03a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433761"
---
# <a name="about-the-freebusy-api"></a><span data-ttu-id="02520-103">Сведения об API сведений о доступности</span><span class="sxs-lookup"><span data-stu-id="02520-103">About the Free/Busy API</span></span>

<span data-ttu-id="02520-104">API сведений о доступности позволяет почтовым поставщикам предоставлять сведения о доступности для указанных учетных записей пользователей в указанном диапазоне времени.</span><span class="sxs-lookup"><span data-stu-id="02520-104">The Free/Busy API allows mail providers to provide free/busy status information for specified user accounts within a specified time range.</span></span> <span data-ttu-id="02520-105">Сведения о занятости в календаре пользователя находятся на одном из следующих периодов: "нет на месте", "занято", "под вопросом" или "свободен".</span><span class="sxs-lookup"><span data-stu-id="02520-105">The free/busy status of a block of time on a user's calendar is one of the following: out-of-office, busy, tentative, or free.</span></span>
  
## <a name="create-a-freebusy-provider"></a><span data-ttu-id="02520-106">Создание поставщика сведений о доступности</span><span class="sxs-lookup"><span data-stu-id="02520-106">Create a free/busy provider</span></span>

<span data-ttu-id="02520-107">Чтобы предоставить пользователям почты доступ к сведениям о доступности, поставщик услуг электронной почты создает поставщика сведений о доступности и регистрирует его в Outlook.</span><span class="sxs-lookup"><span data-stu-id="02520-107">To provide free/busy information to mail users, a mail provider creates a free/busy provider and registers it with Outlook.</span></span> <span data-ttu-id="02520-108">Поставщик сведений о доступности должен реализовывать следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="02520-108">The free/busy provider must implement the following interfaces.</span></span> <span data-ttu-id="02520-109">Обратите внимание, что количество членов в этих интерфейсах не поддерживается и должно возвращать указанные возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="02520-109">Note that a number of members in these interfaces are not supported and must return the specified return values.</span></span> <span data-ttu-id="02520-110">В частности, API сведений о доступности не поддерживает запись сведений о доступности и делегирование доступа к учетным записям.</span><span class="sxs-lookup"><span data-stu-id="02520-110">In particular, the Free/Busy API does not support write access to free/busy information and delegate access to accounts.</span></span>
  
- <span data-ttu-id="02520-111">[Ифрибусисуппорт](ifreebusysupport.md) — этот интерфейс поддерживает спецификацию интерфейсов, которые обращаются к данным о занятости для указанных пользователей.</span><span class="sxs-lookup"><span data-stu-id="02520-111">[IFreeBusySupport](ifreebusysupport.md) —This interface supports specification of interfaces that access free/busy data for specified users.</span></span> <span data-ttu-id="02520-112">Он использует [фбусер](fbuser.md) для идентификации пользователя.</span><span class="sxs-lookup"><span data-stu-id="02520-112">It uses [FBUser](fbuser.md) to identify a user.</span></span> 
    
- <span data-ttu-id="02520-113">[Ифрибусидата](ifreebusydata.md) — этот интерфейс получает и задает диапазон времени для заданного пользователя и возвращает интерфейс для перечисления блоков сведений о занятости для данных в пределах этого диапазона времени.</span><span class="sxs-lookup"><span data-stu-id="02520-113">[IFreeBusyData](ifreebusydata.md) —This interface gets and sets a time range for a given user and returns an interface for enumerating free/busy blocks of data within this time range.</span></span> <span data-ttu-id="02520-114">Он использует относительное время для получения и задания этого диапазона времени.</span><span class="sxs-lookup"><span data-stu-id="02520-114">It uses relative time to get and set this time range.</span></span> <span data-ttu-id="02520-115">Дополнительные сведения см. [в разделе Использование относительного времени для доступа к данным о занятости](how-to-use-relative-time-to-access-free-busy-data.md).</span><span class="sxs-lookup"><span data-stu-id="02520-115">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
- <span data-ttu-id="02520-116">[Иенумфбблокк](ienumfbblock.md) — этот интерфейс поддерживает доступ и перечисление блоков сведений о занятости для пользователя в диапазоне времени.</span><span class="sxs-lookup"><span data-stu-id="02520-116">[IEnumFBBlock](ienumfbblock.md) —This interface supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="02520-117">Перечисление содержит блоки сведений о занятости, которые указывают сведения о занятости периодов времени в календаре пользователя в диапазоне времени (указывается с помощью [ифрибусидата:: енумблоккс](ifreebusydata-enumblocks.md)).</span><span class="sxs-lookup"><span data-stu-id="02520-117">An enumeration contains free/busy blocks that indicate the free/busy status of periods of time on a user's calendar, within a time range (specified by [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)).</span></span> <span data-ttu-id="02520-118">Элементы в календаре, такие как встречи и приглашения на собрания, блоки форм в перечислении.</span><span class="sxs-lookup"><span data-stu-id="02520-118">Items on a calendar, such as appointments and meeting requests, form blocks in the enumeration.</span></span> <span data-ttu-id="02520-119">Элементы, расположенные рядом друг с другом в календаре и имеющие одинаковое состояние занятости, объединяются в один блок.</span><span class="sxs-lookup"><span data-stu-id="02520-119">Items that are adjacent to one another on the calendar and have the same free/busy status are combined to form one single block.</span></span> <span data-ttu-id="02520-120">Свободный период времени в календаре также образует блок.</span><span class="sxs-lookup"><span data-stu-id="02520-120">A free period of time on a calendar also forms a block.</span></span> <span data-ttu-id="02520-121">Поэтому никакие два последовательных блока в перечислении не будут иметь одинаковые сведения о доступности.</span><span class="sxs-lookup"><span data-stu-id="02520-121">Therefore, no two consecutive blocks in an enumeration would have the same free/busy status.</span></span> <span data-ttu-id="02520-122">Эти блоки не перекрываются по времени.</span><span class="sxs-lookup"><span data-stu-id="02520-122">These blocks do not overlap in time.</span></span> <span data-ttu-id="02520-123">При наличии перекрывающихся элементов в календаре Outlook выполняет слияние этих элементов для формирования неперекрывающихся блоков сведений о занятости в перечислении на основе следующего порядка приоритетов: "нет на месте", "занято" и "под вопросом".</span><span class="sxs-lookup"><span data-stu-id="02520-123">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span> 
  
<span data-ttu-id="02520-124">Чтобы зарегистрировать поставщика сведений о доступности в Outlook, Поставщик почты должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="02520-124">To register the free/busy provider with Outlook, the mail provider should do the following:</span></span>
  
1. <span data-ttu-id="02520-125">ЗаРегистрируйте поставщик сведений о доступности в COM, предоставив CLSID, который предоставляет доступ к реализации поставщика **ифрибусисуппорт**.</span><span class="sxs-lookup"><span data-stu-id="02520-125">Register the free/busy provider with COM, providing a CLSID that allows access to the provider's implementation of **IFreeBusySupport**.</span></span> 
    
2. <span data-ttu-id="02520-126">Сообщите Outlook, что существует поставщик сведений о доступности, задав следующий ключ (где `<xx.x>` представляет версию Outlook) в системном реестре:</span><span class="sxs-lookup"><span data-stu-id="02520-126">Let Outlook know that the free/busy provider exists by setting the following key (where `<xx.x>` represents the version of Outlook) in the system registry:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\<xx.x>\Outlook\SchedulingInformation\FreeBusySupport`
    
   <span data-ttu-id="02520-127">Например, если поставщик транспорта является SMTP, для регистрации поставщика в Microsoft Outlook 2010 установите следующий ключ к данным в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="02520-127">For example, if the transport provider is SMTP, to register the provider with Microsoft Outlook 2010, set the following key to the data in the following table:</span></span> 
    
   `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook\SchedulingInformation\FreeBusySupport`
    
   |<span data-ttu-id="02520-128">Имя</span><span class="sxs-lookup"><span data-stu-id="02520-128">Name</span></span> |<span data-ttu-id="02520-129">Тип</span><span class="sxs-lookup"><span data-stu-id="02520-129">Type</span></span> |<span data-ttu-id="02520-130">Значение</span><span class="sxs-lookup"><span data-stu-id="02520-130">Value</span></span> |
   |:-----|:-----|:-----|
   |<span data-ttu-id="02520-131">SMTP</span><span class="sxs-lookup"><span data-stu-id="02520-131">SMTP</span></span>  |<span data-ttu-id="02520-132">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="02520-132">REG_SZ</span></span>  |<span data-ttu-id="02520-133">{CLSID для соответствующей реализации Ифрибусисуппорт</span><span class="sxs-lookup"><span data-stu-id="02520-133">{CLSID for respective implementation of IFreeBusySupport}</span></span>  |
   
   <span data-ttu-id="02520-134">В этом сценарии Outlook совместно создает COM-класс и использует его для получения сведений о занятости для всех почтовых пользователей SMTP.</span><span class="sxs-lookup"><span data-stu-id="02520-134">In this scenario, Outlook co-creates the COM class and uses it to retrieve free/busy information for any SMTP mail users.</span></span>
    
<span data-ttu-id="02520-135">Для поддержки адресной книги и поставщика транспорта, использующих тип записи адреса, отличный от SMTP, измените *имя* соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="02520-135">To support an address book and transport provider that use an address entry type other than SMTP, change the  *Name* accordingly.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="02520-136">Во время установки поставщики сведений о доступности должны проверить, существует ли параметр реестра для того же типа записи адреса.</span><span class="sxs-lookup"><span data-stu-id="02520-136">During installation, free/busy providers should check whether a registry setting for the the same address entry type already exists.</span></span> <span data-ttu-id="02520-137">Если это так, поставщик сведений о доступности должен перезаписать текущего поставщика для этого типа записи адреса и при удалении этого поставщика восстановить его.</span><span class="sxs-lookup"><span data-stu-id="02520-137">If it does, the free/busy provider should overwrite the current provider for that address entry type, and restore to that provider when it uninstalls.</span></span> <span data-ttu-id="02520-138">Тем не менее, если пользователь установил несколько поставщиков сведений о доступности для одного и того же типа записи адреса, пользователь должен удалить эти поставщики в обратном порядке по мере установки (то есть всегда удалять самого старого поставщика).</span><span class="sxs-lookup"><span data-stu-id="02520-138">However, if a user has installed more than one free/busy provider for the same address entry type, the user should uninstall these providers in the reverse order as installation (that is, always uninstall the latest provider).</span></span> <span data-ttu-id="02520-139">В противном случае реестр может указать поставщика, который уже был удален.</span><span class="sxs-lookup"><span data-stu-id="02520-139">Otherwise, the registry may point to a provider that has already been uninstalled.</span></span> 
  
## <a name="api-components"></a><span data-ttu-id="02520-140">Компоненты API</span><span class="sxs-lookup"><span data-stu-id="02520-140">API components</span></span>

<span data-ttu-id="02520-141">API сведений о доступности включает следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="02520-141">The Free/Busy API includes the following components:</span></span>
  
### <a name="definitions"></a><span data-ttu-id="02520-142">Определения</span><span class="sxs-lookup"><span data-stu-id="02520-142">Definitions</span></span>

- [<span data-ttu-id="02520-143">Константы (API сведений о доступности)</span><span class="sxs-lookup"><span data-stu-id="02520-143">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
    
### <a name="data-types"></a><span data-ttu-id="02520-144">Типы данных</span><span class="sxs-lookup"><span data-stu-id="02520-144">Data types</span></span>

- [<span data-ttu-id="02520-145">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="02520-145">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="02520-146">FBStatus</span><span class="sxs-lookup"><span data-stu-id="02520-146">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="02520-147">FBUser</span><span class="sxs-lookup"><span data-stu-id="02520-147">FBUser</span></span>](fbuser.md)
    
### <a name="interfaces"></a><span data-ttu-id="02520-148">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="02520-148">Interfaces</span></span>

- [<span data-ttu-id="02520-149">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="02520-149">IEnumFBBlock</span></span>](ienumfbblock.md)
- [<span data-ttu-id="02520-150">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="02520-150">IFreeBusyData</span></span>](ifreebusydata.md)
- [<span data-ttu-id="02520-151">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="02520-151">IFreeBusySupport</span></span>](ifreebusysupport.md)
    

