---
title: IProfSect IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfSect
api_type:
- COM
ms.assetid: 4e704044-5230-4521-a0d2-b7c2f981c954
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 99ce944bec94a1e832f77fa8b0916ac1c76f6dc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406600"
---
# <a name="iprofsect--imapiprop"></a><span data-ttu-id="6bad0-103">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6bad0-103">IProfSect : IMAPIProp</span></span>

  
  
<span data-ttu-id="6bad0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6bad0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6bad0-105">Работает со свойствами объектов раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="6bad0-105">Works with the properties of profile section objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6bad0-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6bad0-106">Header file:</span></span>  <br/> |<span data-ttu-id="6bad0-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="6bad0-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="6bad0-108">Выставим:</span><span class="sxs-lookup"><span data-stu-id="6bad0-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="6bad0-109">Объекты раздела профиля</span><span class="sxs-lookup"><span data-stu-id="6bad0-109">Profile section objects</span></span>  <br/> |
|<span data-ttu-id="6bad0-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="6bad0-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="6bad0-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="6bad0-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="6bad0-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="6bad0-112">Called by:</span></span>  <br/> |<span data-ttu-id="6bad0-113">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="6bad0-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="6bad0-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="6bad0-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6bad0-115">IID_IProfSect</span><span class="sxs-lookup"><span data-stu-id="6bad0-115">IID_IProfSect</span></span>  <br/> |
|<span data-ttu-id="6bad0-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="6bad0-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="6bad0-117">LPPROFSECT</span><span class="sxs-lookup"><span data-stu-id="6bad0-117">LPPROFSECT</span></span>  <br/> |
|<span data-ttu-id="6bad0-118">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="6bad0-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="6bad0-119">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="6bad0-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6bad0-120">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="6bad0-120">Vtable order</span></span>

<span data-ttu-id="6bad0-121">Этот интерфейс не имеет уникальных методов.</span><span class="sxs-lookup"><span data-stu-id="6bad0-121">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="6bad0-122">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="6bad0-122">**Required properties**</span></span>|<span data-ttu-id="6bad0-123">**Access**</span><span class="sxs-lookup"><span data-stu-id="6bad0-123">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6bad0-124">**PR_OBJECT_TYPE** ([PidTagObjectType)](pidtagobjecttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="6bad0-124">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6bad0-125">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="6bad0-125">Read-only</span></span>  <br/> |
|<span data-ttu-id="6bad0-126">**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6bad0-126">**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6bad0-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="6bad0-127">Read-only</span></span>  <br/> |
   
## <a name="notes-to-callers"></a><span data-ttu-id="6bad0-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="6bad0-128">Notes to callers</span></span>

<span data-ttu-id="6bad0-129">Интерфейс **IProfSect** не имеет собственных уникальных методов, но можно вызвать методы [IMAPIProp](imapipropiunknown.md) раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="6bad0-129">The **IProfSect** interface does not have any unique methods of its own, but you can call the profile section's [IMAPIProp](imapipropiunknown.md) methods.</span></span> <span data-ttu-id="6bad0-130">Между реализацией **IProfSect** и другими реализациями **IMAPIProp** существуют некоторые различия:</span><span class="sxs-lookup"><span data-stu-id="6bad0-130">There are some differences between the **IProfSect** implementation and other implementations of **IMAPIProp**:</span></span>
  
- <span data-ttu-id="6bad0-131">**IProfSect** не поддерживает модель транзакций.</span><span class="sxs-lookup"><span data-stu-id="6bad0-131">**IProfSect** does not support a transaction model.</span></span> 
    
- <span data-ttu-id="6bad0-132">**IProfSect** не поддерживает именуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="6bad0-132">**IProfSect** does not support named properties.</span></span> 
    
- <span data-ttu-id="6bad0-133">**IProfSect** резервировать диапазон 0x67F0 0x67ff для безопасных свойств.</span><span class="sxs-lookup"><span data-stu-id="6bad0-133">**IProfSect** reserves the identifier range 0x67F0 to 0x67ff for secure properties.</span></span> 
    
<span data-ttu-id="6bad0-134">Если модель транзакций не поддерживается, все изменения, внесенные в раздел профиля после вызовов методов [IMAPIProp::CopyProps](imapiprop-copyprops.md) и [IMAPIProp::CopyTo,](imapiprop-copyto.md) происходят немедленно.</span><span class="sxs-lookup"><span data-stu-id="6bad0-134">Not supporting a transaction model means that all changes that were made to a profile section following calls to the [IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md) methods occur immediately.</span></span> <span data-ttu-id="6bad0-135">Вызовы метода [IMAPIProp::SaveChanges будут](imapiprop-savechanges.md) успешными, но фактически не будут сохранять изменения.</span><span class="sxs-lookup"><span data-stu-id="6bad0-135">Calls to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method succeed but do not actually save any changes.</span></span> 
  
<span data-ttu-id="6bad0-136">Чтобы защититься от преждевременных изменений, поставщики услуг должны создавать копии своих разделов профилей, которые отображаются для пользователей с помощью таблиц свойств.</span><span class="sxs-lookup"><span data-stu-id="6bad0-136">To be protected from changes that occur prematurely, service providers need to make copies of their profile sections that are displayed to users through property sheets.</span></span> <span data-ttu-id="6bad0-137">Листы свойств должны работать с копией, а не с реальным разделом профиля.</span><span class="sxs-lookup"><span data-stu-id="6bad0-137">The property sheets should work with the copy, instead of the real profile section.</span></span> <span data-ttu-id="6bad0-138">Когда пользователь нажимает  кнопку "ОК", чтобы проверить правильность изменений, изменения можно сохранить в реальном разделе профиля.</span><span class="sxs-lookup"><span data-stu-id="6bad0-138">When the user clicks the **OK** button to verify that the changes are accurate, the changes can be saved to the real profile section.</span></span> 
  
<span data-ttu-id="6bad0-139">Чтобы реализовать лист свойств с помощью скопированные разделы профиля, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="6bad0-139">To implement a property sheet by using a copied profile section, use the following procedure:</span></span>
  
1. <span data-ttu-id="6bad0-140">Откройте раздел профиля, вызывая метод [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) или [IProviderAdmin::OpenProfileSection.](iprovideradmin-openprofilesection.md)</span><span class="sxs-lookup"><span data-stu-id="6bad0-140">Open the profile section by calling the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> 
    
2. <span data-ttu-id="6bad0-141">Вызовите [функцию CreateIProp,](createiprop.md) чтобы получить объект данных свойства — объект, который поддерживает **интерфейс IPropData.**</span><span class="sxs-lookup"><span data-stu-id="6bad0-141">Call the [CreateIProp](createiprop.md) function to retrieve a property data object — an object that supports the **IPropData** interface.</span></span> 
    
3. <span data-ttu-id="6bad0-142">Вызовите метод [IMAPIProp::CopyTo](imapiprop-copyto.md) раздела профиля, чтобы скопировать свойства, которые будут отображаться на листе свойств, из раздела профиля в объект данных свойства.</span><span class="sxs-lookup"><span data-stu-id="6bad0-142">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties that will appear on the property sheet from the profile section to the property data object.</span></span> 
    
4. <span data-ttu-id="6bad0-143">Вызовите метод [IMAPISupport::D oConfigPropSheet,](imapisupport-doconfigpropsheet.md) чтобы запросить, чтобы поставщик услуг отображал лист свойств, и передать указатель на объект данных свойства в параметре _lpConfigData._</span><span class="sxs-lookup"><span data-stu-id="6bad0-143">Call the [IMAPISupport::DoConfigPropSheet](imapisupport-doconfigpropsheet.md) method to request that the service provider display a property sheet, and pass a pointer to the property data object in the  _lpConfigData_ parameter.</span></span> 
    
5. <span data-ttu-id="6bad0-144">Когда пользователь сохраняет изменения свойств конфигурации на листе свойств, вызовите метод [IMAPIProp::CopyTo,](imapiprop-copyto.md) чтобы скопировать свойства из объекта данных свойства обратно в раздел профиля.</span><span class="sxs-lookup"><span data-stu-id="6bad0-144">When the user saves changes to configuration properties in the property sheet, call the [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties from the property data object back to the profile section.</span></span> 
    
<span data-ttu-id="6bad0-145">Разделы профилей, в отличие от других объектов, не поддерживают именуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="6bad0-145">Profile sections, unlike other objects, do not support named properties.</span></span> <span data-ttu-id="6bad0-146">Методы [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) и [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) возвращают MAPI_E_NO_SUPPORT, если они вызваны в объекте раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="6bad0-146">The [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) methods return MAPI_E_NO_SUPPORT if they are called on a profile section object.</span></span> <span data-ttu-id="6bad0-147">Если вы используете метод [IMAPIProp::SetProps,](imapiprop-setprops.md) чтобы установить идентификаторы свойств в диапазоне выше 0x8000, будет возвращен тип PT_ERROR свойства.</span><span class="sxs-lookup"><span data-stu-id="6bad0-147">If you use the [IMAPIProp::SetProps](imapiprop-setprops.md) method to set property identifiers in the range above 0x8000, the PT_ERROR property type will be returned.</span></span> 
  
<span data-ttu-id="6bad0-148">Разделы профилей резервировать диапазон 0x67F0 0x67FF для безопасных свойств.</span><span class="sxs-lookup"><span data-stu-id="6bad0-148">Profile sections reserve the identifier range 0x67F0 to 0x67FF for secure properties.</span></span> <span data-ttu-id="6bad0-149">Поставщики услуг могут использовать этот диапазон для хранения паролей и других учетных данных, характерных для конкретного поставщика.</span><span class="sxs-lookup"><span data-stu-id="6bad0-149">Service providers can use this range to store passwords and other provider-specific credentials.</span></span> <span data-ttu-id="6bad0-150">Свойства в этом диапазоне не возвращаются в полном списке свойств, когда NULL передается в _параметре lpPropTag_ метода [IMAPIProp::GetProps,](imapiprop-getprops.md) и не возвращаются в _параметре lppPropTagArray_ метода [IMAPIProp::GetPropList.](imapiprop-getproplist.md)</span><span class="sxs-lookup"><span data-stu-id="6bad0-150">Properties in this range are not returned in the complete list of properties when NULL is passed in the  _lpPropTag_ parameter of the [IMAPIProp::GetProps](imapiprop-getprops.md) method, nor are they returned in the  _lppPropTagArray_ parameter of the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> <span data-ttu-id="6bad0-151">Защищенные свойства должны запрашиваться в частности их идентификаторами.</span><span class="sxs-lookup"><span data-stu-id="6bad0-151">Secure properties must be requested specifically by their identifiers.</span></span> 
  
<span data-ttu-id="6bad0-152">MAPI передает раздел профиля с жестко заданная константой MUID_PROFILE_INSTANCE в качестве идентификатора, а PR_SEARCH_KEY **(** [PidTagSearchKey)](pidtagsearchkey-canonical-property.md)в качестве своего единственного свойства.</span><span class="sxs-lookup"><span data-stu-id="6bad0-152">MAPI furnishes a profile section with the hard-coded constant MUID_PROFILE_INSTANCE as its identifier and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) as its single property.</span></span> <span data-ttu-id="6bad0-153">MAPI гарантирует, что **PR_SEARCH_KEY** свойства будет уникальным для всех созданных профилей.</span><span class="sxs-lookup"><span data-stu-id="6bad0-153">MAPI ensures that the **PR_SEARCH_KEY** property value will be unique among all created profiles.</span></span> <span data-ttu-id="6bad0-154">Используйте **PR_SEARCH_KEY** вместо **PR_PROFILE_NAME,** если важна уникальность, так как за удаленным профилем может следовать другой профиль с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="6bad0-154">Use **PR_SEARCH_KEY** instead of **PR_PROFILE_NAME** when uniqueness is important, because it is possible for a deleted profile to be followed by another profile with the same name.</span></span> 
  
<span data-ttu-id="6bad0-155">Дополнительные сведения об использовании разделов профилей см. в разделах ["Администрирование профилей и служб сообщений".](administering-profiles-and-message-services.md)</span><span class="sxs-lookup"><span data-stu-id="6bad0-155">For more information about how to use profile sections, see [Administering Profiles and Message Services](administering-profiles-and-message-services.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6bad0-156">См. также</span><span class="sxs-lookup"><span data-stu-id="6bad0-156">See also</span></span>



[<span data-ttu-id="6bad0-157">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="6bad0-157">MAPI Interfaces</span></span>](mapi-interfaces.md)

