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
ms.openlocfilehash: c0653caec5f3cac531206e1bb9c4330cac5f3133
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809535"
---
# <a name="iprofsect--imapiprop"></a><span data-ttu-id="4a857-103">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4a857-103">IProfSect : IMAPIProp</span></span>

  
  
<span data-ttu-id="4a857-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4a857-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4a857-105">Works со свойствами объектов раздела профилей.</span><span class="sxs-lookup"><span data-stu-id="4a857-105">Works with the properties of profile section objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4a857-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="4a857-106">Header file:</span></span>  <br/> |<span data-ttu-id="4a857-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="4a857-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="4a857-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="4a857-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="4a857-109">Объекты раздела профиля</span><span class="sxs-lookup"><span data-stu-id="4a857-109">Profile section objects</span></span>  <br/> |
|<span data-ttu-id="4a857-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="4a857-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="4a857-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="4a857-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="4a857-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="4a857-112">Called by:</span></span>  <br/> |<span data-ttu-id="4a857-113">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="4a857-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="4a857-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="4a857-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4a857-115">IID_IProfSect</span><span class="sxs-lookup"><span data-stu-id="4a857-115">IID_IProfSect</span></span>  <br/> |
|<span data-ttu-id="4a857-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="4a857-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="4a857-117">LPPROFSECT</span><span class="sxs-lookup"><span data-stu-id="4a857-117">LPPROFSECT</span></span>  <br/> |
|<span data-ttu-id="4a857-118">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="4a857-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="4a857-119">Не входящих в транзакции</span><span class="sxs-lookup"><span data-stu-id="4a857-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4a857-120">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="4a857-120">Vtable order</span></span>

<span data-ttu-id="4a857-121">Этот интерфейс не имеет каких-либо уникальных методов.</span><span class="sxs-lookup"><span data-stu-id="4a857-121">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="4a857-122">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="4a857-122">**Required properties**</span></span>|<span data-ttu-id="4a857-123">**Access**</span><span class="sxs-lookup"><span data-stu-id="4a857-123">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4a857-124">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4a857-124">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4a857-125">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a857-125">Read-only</span></span>  <br/> |
|<span data-ttu-id="4a857-126">**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4a857-126">**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4a857-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a857-127">Read-only</span></span>  <br/> |
   
## <a name="notes-to-callers"></a><span data-ttu-id="4a857-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="4a857-128">Notes to callers</span></span>

<span data-ttu-id="4a857-129">Интерфейс **IProfSect** не имеет уникальное методы свои собственные, но профиля можно вызвать методы [IMAPIProp](imapipropiunknown.md) раздела.</span><span class="sxs-lookup"><span data-stu-id="4a857-129">The **IProfSect** interface does not have any unique methods of its own, but you can call the profile section's [IMAPIProp](imapipropiunknown.md) methods.</span></span> <span data-ttu-id="4a857-130">Существуют различия между реализации **IProfSect** и другими реализациями **IMAPIProp**:</span><span class="sxs-lookup"><span data-stu-id="4a857-130">There are some differences between the **IProfSect** implementation and other implementations of **IMAPIProp**:</span></span>
  
- <span data-ttu-id="4a857-131">**IProfSect** не поддерживает модели транзакции.</span><span class="sxs-lookup"><span data-stu-id="4a857-131">**IProfSect** does not support a transaction model.</span></span> 
    
- <span data-ttu-id="4a857-132">**IProfSect** не поддерживает именованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4a857-132">**IProfSect** does not support named properties.</span></span> 
    
- <span data-ttu-id="4a857-133">**IProfSect** оставляет за собой диапазон идентификатор 0x67F0 для 0x67ff для свойства безопасности.</span><span class="sxs-lookup"><span data-stu-id="4a857-133">**IProfSect** reserves the identifier range 0x67F0 to 0x67ff for secure properties.</span></span> 
    
<span data-ttu-id="4a857-134">Отсутствие поддержки модели транзакций означает, что все изменения, внесенные в раздел профиля следующие вызовы [IMAPIProp::CopyProps](imapiprop-copyprops.md) и [IMAPIProp::CopyTo](imapiprop-copyto.md) методы возникают сразу же.</span><span class="sxs-lookup"><span data-stu-id="4a857-134">Not supporting a transaction model means that all changes that were made to a profile section following calls to the [IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md) methods occur immediately.</span></span> <span data-ttu-id="4a857-135">Вызовы метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) успешно, но не фактически сохранить все изменения.</span><span class="sxs-lookup"><span data-stu-id="4a857-135">Calls to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method succeed but do not actually save any changes.</span></span> 
  
<span data-ttu-id="4a857-136">Для защиты от изменения, внесенные преждевременно, поставщиков услуг необходимо принять копий своих профилей разделов, отображаемых для пользователей с помощью страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="4a857-136">To be protected from changes that occur prematurely, service providers need to make copies of their profile sections that are displayed to users through property sheets.</span></span> <span data-ttu-id="4a857-137">Страницы свойств должны работать с копией, вместо раздела реальных профилей.</span><span class="sxs-lookup"><span data-stu-id="4a857-137">The property sheets should work with the copy, instead of the real profile section.</span></span> <span data-ttu-id="4a857-138">Когда пользователь нажимает кнопку **ОК** , чтобы проверить правильность изменения, можно сохранить изменения в раздел реальных профилей.</span><span class="sxs-lookup"><span data-stu-id="4a857-138">When the user clicks the **OK** button to verify that the changes are accurate, the changes can be saved to the real profile section.</span></span> 
  
<span data-ttu-id="4a857-139">Для реализации свойств с помощью скопированного профиля, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="4a857-139">To implement a property sheet by using a copied profile section, use the following procedure:</span></span>
  
1. <span data-ttu-id="4a857-140">Откройте раздел профиля путем вызова метода [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) или [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) .</span><span class="sxs-lookup"><span data-stu-id="4a857-140">Open the profile section by calling the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> 
    
2. <span data-ttu-id="4a857-141">Вызовите функцию [CreateIProp](createiprop.md) для получения данных свойства объекта — объект, который поддерживает интерфейс **IPropData** .</span><span class="sxs-lookup"><span data-stu-id="4a857-141">Call the [CreateIProp](createiprop.md) function to retrieve a property data object — an object that supports the **IPropData** interface.</span></span> 
    
3. <span data-ttu-id="4a857-142">Вызов метода [IMAPIProp::CopyTo](imapiprop-copyto.md) раздела профиля для копирования свойства, которые будут отображаться на странице свойств из раздела профиля объект данных свойства.</span><span class="sxs-lookup"><span data-stu-id="4a857-142">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties that will appear on the property sheet from the profile section to the property data object.</span></span> 
    
4. <span data-ttu-id="4a857-143">Вызовите метод [IMAPISupport::DoConfigPropSheet](imapisupport-doconfigpropsheet.md) для запроса, что поставщик услуг открыть окно свойств и передать указатель на объект данных свойства с помощью параметра _lpConfigData_ .</span><span class="sxs-lookup"><span data-stu-id="4a857-143">Call the [IMAPISupport::DoConfigPropSheet](imapisupport-doconfigpropsheet.md) method to request that the service provider display a property sheet, and pass a pointer to the property data object in the  _lpConfigData_ parameter.</span></span> 
    
5. <span data-ttu-id="4a857-144">Когда пользователь сохраняет изменения свойства конфигурации в окне свойств, вызовите метод [IMAPIProp::CopyTo](imapiprop-copyto.md) , чтобы скопировать свойства из объекта данных свойства раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="4a857-144">When the user saves changes to configuration properties in the property sheet, call the [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties from the property data object back to the profile section.</span></span> 
    
<span data-ttu-id="4a857-145">Разделы профилей, в отличие от других объектов, не поддерживают именованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4a857-145">Profile sections, unlike other objects, do not support named properties.</span></span> <span data-ttu-id="4a857-146">Методы [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) и [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) возвращает MAPI_E_NO_SUPPORT, если они называются для объекта раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="4a857-146">The [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) methods return MAPI_E_NO_SUPPORT if they are called on a profile section object.</span></span> <span data-ttu-id="4a857-147">При использовании метода [IMAPIProp::SetProps](imapiprop-setprops.md) для определения идентификаторов свойств в диапазоне выше 0x8000 тип свойства PT_ERROR будут возвращены.</span><span class="sxs-lookup"><span data-stu-id="4a857-147">If you use the [IMAPIProp::SetProps](imapiprop-setprops.md) method to set property identifiers in the range above 0x8000, the PT_ERROR property type will be returned.</span></span> 
  
<span data-ttu-id="4a857-148">Разделы профилей зарезервировать идентификатор диапазон 0x67F0 для 0x67FF для свойства безопасности.</span><span class="sxs-lookup"><span data-stu-id="4a857-148">Profile sections reserve the identifier range 0x67F0 to 0x67FF for secure properties.</span></span> <span data-ttu-id="4a857-149">Поставщики услуг могут использовать этот диапазон для хранения паролей и других учетных данных от поставщика.</span><span class="sxs-lookup"><span data-stu-id="4a857-149">Service providers can use this range to store passwords and other provider-specific credentials.</span></span> <span data-ttu-id="4a857-150">В этот диапазон не возвращаются свойства в полный список свойств при передается в параметр _lpPropTag_ метода [IMAPIProp::GetProps](imapiprop-getprops.md) , а также их возвращаются в параметре _lppPropTagArray_ [ IMAPIProp::GetPropList](imapiprop-getproplist.md) метод.</span><span class="sxs-lookup"><span data-stu-id="4a857-150">Properties in this range are not returned in the complete list of properties when NULL is passed in the  _lpPropTag_ parameter of the [IMAPIProp::GetProps](imapiprop-getprops.md) method, nor are they returned in the  _lppPropTagArray_ parameter of the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> <span data-ttu-id="4a857-151">Защищенные свойства должны быть затребованы специально идентификаторам.</span><span class="sxs-lookup"><span data-stu-id="4a857-151">Secure properties must be requested specifically by their identifiers.</span></span> 
  
<span data-ttu-id="4a857-152">MAPI предоставляющей профиля с жестко MUID_PROFILE_INSTANCE константу как его идентификатор и **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)), как его отдельное свойство.</span><span class="sxs-lookup"><span data-stu-id="4a857-152">MAPI furnishes a profile section with the hard-coded constant MUID_PROFILE_INSTANCE as its identifier and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) as its single property.</span></span> <span data-ttu-id="4a857-153">MAPI гарантирует, что значение свойства **PR_SEARCH_KEY** будет уникальным во всех созданных профилей.</span><span class="sxs-lookup"><span data-stu-id="4a857-153">MAPI ensures that the **PR_SEARCH_KEY** property value will be unique among all created profiles.</span></span> <span data-ttu-id="4a857-154">Используйте **PR_SEARCH_KEY** вместо **PR_PROFILE_NAME** уникальности важна, так как это возможно, для удаленного профиль, который необходимо следовать другого профиля с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="4a857-154">Use **PR_SEARCH_KEY** instead of **PR_PROFILE_NAME** when uniqueness is important, because it is possible for a deleted profile to be followed by another profile with the same name.</span></span> 
  
<span data-ttu-id="4a857-155">Дополнительные сведения об использовании профилей разделах содержатся в разделе [профили, Администрирование и службы сообщений](administering-profiles-and-message-services.md).</span><span class="sxs-lookup"><span data-stu-id="4a857-155">For more information about how to use profile sections, see [Administering Profiles and Message Services](administering-profiles-and-message-services.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4a857-156">См. также</span><span class="sxs-lookup"><span data-stu-id="4a857-156">See also</span></span>



[<span data-ttu-id="4a857-157">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="4a857-157">MAPI Interfaces</span></span>](mapi-interfaces.md)

