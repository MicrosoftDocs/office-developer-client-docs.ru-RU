---
title: Ипрофсект IMAPIProp
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344795"
---
# <a name="iprofsect--imapiprop"></a><span data-ttu-id="80695-103">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="80695-103">IProfSect : IMAPIProp</span></span>

  
  
<span data-ttu-id="80695-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80695-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80695-105">Работает со свойствами объектов раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="80695-105">Works with the properties of profile section objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="80695-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="80695-106">Header file:</span></span>  <br/> |<span data-ttu-id="80695-107">Мапикс. h</span><span class="sxs-lookup"><span data-stu-id="80695-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="80695-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="80695-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="80695-109">Объекты раздела профиля</span><span class="sxs-lookup"><span data-stu-id="80695-109">Profile section objects</span></span>  <br/> |
|<span data-ttu-id="80695-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="80695-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="80695-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="80695-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="80695-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="80695-112">Called by:</span></span>  <br/> |<span data-ttu-id="80695-113">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="80695-113">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="80695-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="80695-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="80695-115">Иид_ипрофсект</span><span class="sxs-lookup"><span data-stu-id="80695-115">IID_IProfSect</span></span>  <br/> |
|<span data-ttu-id="80695-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="80695-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="80695-117">ЛППРОФСЕКТ</span><span class="sxs-lookup"><span data-stu-id="80695-117">LPPROFSECT</span></span>  <br/> |
|<span data-ttu-id="80695-118">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="80695-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="80695-119">Не transactd</span><span class="sxs-lookup"><span data-stu-id="80695-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="80695-120">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="80695-120">Vtable order</span></span>

<span data-ttu-id="80695-121">У этого интерфейса нет уникальных методов.</span><span class="sxs-lookup"><span data-stu-id="80695-121">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="80695-122">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="80695-122">**Required properties**</span></span>|<span data-ttu-id="80695-123">**Access**</span><span class="sxs-lookup"><span data-stu-id="80695-123">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="80695-124">**Пр_обжект_типе** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80695-124">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="80695-125">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="80695-125">Read-only</span></span>  <br/> |
|<span data-ttu-id="80695-126">**Пр_профиле_наме** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="80695-126">**PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="80695-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="80695-127">Read-only</span></span>  <br/> |
   
## <a name="notes-to-callers"></a><span data-ttu-id="80695-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="80695-128">Notes to callers</span></span>

<span data-ttu-id="80695-129">Интерфейс **ипрофсект** не обладает уникальными методами, но вы можете вызвать методы [IMAPIProp](imapipropiunknown.md) раздела profile.</span><span class="sxs-lookup"><span data-stu-id="80695-129">The **IProfSect** interface does not have any unique methods of its own, but you can call the profile section's [IMAPIProp](imapipropiunknown.md) methods.</span></span> <span data-ttu-id="80695-130">Существуют некоторые различия между реализацией **ипрофсект** и другими реализациями **IMAPIProp**:</span><span class="sxs-lookup"><span data-stu-id="80695-130">There are some differences between the **IProfSect** implementation and other implementations of **IMAPIProp**:</span></span>
  
- <span data-ttu-id="80695-131">**Ипрофсект** не поддерживает модель транзакции.</span><span class="sxs-lookup"><span data-stu-id="80695-131">**IProfSect** does not support a transaction model.</span></span> 
    
- <span data-ttu-id="80695-132">**Ипрофсект** не поддерживает именованные свойства.</span><span class="sxs-lookup"><span data-stu-id="80695-132">**IProfSect** does not support named properties.</span></span> 
    
- <span data-ttu-id="80695-133">**Ипрофсект** резервирует диапазон идентификаторов 0x67F0 в 0x67ff для обеспечения безопасности свойств.</span><span class="sxs-lookup"><span data-stu-id="80695-133">**IProfSect** reserves the identifier range 0x67F0 to 0x67ff for secure properties.</span></span> 
    
<span data-ttu-id="80695-134">Не поддерживающая модель транзакции означает, что все изменения, внесенные в раздел профиля, выполняются сразу же после вызова методов [IMAPIProp:: копипропс](imapiprop-copyprops.md) и [IMAPIProp:: CopyTo](imapiprop-copyto.md) .</span><span class="sxs-lookup"><span data-stu-id="80695-134">Not supporting a transaction model means that all changes that were made to a profile section following calls to the [IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md) methods occur immediately.</span></span> <span data-ttu-id="80695-135">Вызовы метода [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) успешно выполняются, но фактически не сохраняют изменения.</span><span class="sxs-lookup"><span data-stu-id="80695-135">Calls to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method succeed but do not actually save any changes.</span></span> 
  
<span data-ttu-id="80695-136">Чтобы защититься от изменений, которые происходят преждевременно, поставщику услуг необходимо создать копии разделов профилей, отображаемых пользователям с помощью страниц свойств.</span><span class="sxs-lookup"><span data-stu-id="80695-136">To be protected from changes that occur prematurely, service providers need to make copies of their profile sections that are displayed to users through property sheets.</span></span> <span data-ttu-id="80695-137">Страницы свойств должны работать с копией, а не с разделом "реальный профиль".</span><span class="sxs-lookup"><span data-stu-id="80695-137">The property sheets should work with the copy, instead of the real profile section.</span></span> <span data-ttu-id="80695-138">Когда пользователь нажимает кнопку **ОК** , чтобы убедиться, что изменения верны, изменения можно сохранить в разделе Real Profile.</span><span class="sxs-lookup"><span data-stu-id="80695-138">When the user clicks the **OK** button to verify that the changes are accurate, the changes can be saved to the real profile section.</span></span> 
  
<span data-ttu-id="80695-139">Чтобы реализовать страницу свойств с помощью скопированного раздела профиля, выполните следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="80695-139">To implement a property sheet by using a copied profile section, use the following procedure:</span></span>
  
1. <span data-ttu-id="80695-140">Откройте раздел profile, вызвав метод [имаписуппорт:: опенпрофилесектион](imapisupport-openprofilesection.md) или [Ипровидерадмин:: опенпрофилесектион](iprovideradmin-openprofilesection.md) .</span><span class="sxs-lookup"><span data-stu-id="80695-140">Open the profile section by calling the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) or [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) method.</span></span> 
    
2. <span data-ttu-id="80695-141">ВыЗовите функцию [креатеипроп](createiprop.md) , чтобы получить объект данных свойства, объект, который поддерживает интерфейс **ипропдата** .</span><span class="sxs-lookup"><span data-stu-id="80695-141">Call the [CreateIProp](createiprop.md) function to retrieve a property data object — an object that supports the **IPropData** interface.</span></span> 
    
3. <span data-ttu-id="80695-142">ВыЗовите метод [IMAPIProp:: CopyTo](imapiprop-copyto.md) раздела profile, чтобы скопировать свойства, которые будут отображаться на странице свойств, из раздела профиля в объект данных свойства.</span><span class="sxs-lookup"><span data-stu-id="80695-142">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties that will appear on the property sheet from the profile section to the property data object.</span></span> 
    
4. <span data-ttu-id="80695-143">ВыЗовите метод [имаписуппорт::D оконфигпропшит](imapisupport-doconfigpropsheet.md) , чтобы запросить у поставщика услуг отображение страницы свойств, и передайте указатель на объект данных свойства в параметре _лпконфигдата_ .</span><span class="sxs-lookup"><span data-stu-id="80695-143">Call the [IMAPISupport::DoConfigPropSheet](imapisupport-doconfigpropsheet.md) method to request that the service provider display a property sheet, and pass a pointer to the property data object in the  _lpConfigData_ parameter.</span></span> 
    
5. <span data-ttu-id="80695-144">Когда пользователь сохраняет изменения свойств конфигурации на странице свойств, вызовите метод [IMAPIProp:: CopyTo](imapiprop-copyto.md) , чтобы скопировать свойства из объекта данных свойства обратно в раздел profile.</span><span class="sxs-lookup"><span data-stu-id="80695-144">When the user saves changes to configuration properties in the property sheet, call the [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy the properties from the property data object back to the profile section.</span></span> 
    
<span data-ttu-id="80695-145">Разделы профиля, в отличие от других объектов, не поддерживают именованные свойства.</span><span class="sxs-lookup"><span data-stu-id="80695-145">Profile sections, unlike other objects, do not support named properties.</span></span> <span data-ttu-id="80695-146">Методы [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) и [IMAPIProp:: ЖЕТНАМЕСФРОМИДС](imapiprop-getnamesfromids.md) возвращают мапи_е_но_суппорт, если они вызываются для объекта раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="80695-146">The [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) and [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) methods return MAPI_E_NO_SUPPORT if they are called on a profile section object.</span></span> <span data-ttu-id="80695-147">При использовании метода [IMAPIProp:: SetProps](imapiprop-setprops.md) для задания идентификаторов свойств в диапазоне выше 0x8000 возвращается тип свойства пт_еррор.</span><span class="sxs-lookup"><span data-stu-id="80695-147">If you use the [IMAPIProp::SetProps](imapiprop-setprops.md) method to set property identifiers in the range above 0x8000, the PT_ERROR property type will be returned.</span></span> 
  
<span data-ttu-id="80695-148">В разделах профилей резервируется диапазон идентификаторов 0x67F0 to 0x67FF для свойств Secure.</span><span class="sxs-lookup"><span data-stu-id="80695-148">Profile sections reserve the identifier range 0x67F0 to 0x67FF for secure properties.</span></span> <span data-ttu-id="80695-149">Поставщики услуг могут использовать этот диапазон для хранения паролей и других учетных данных, относящихся к конкретному поставщику.</span><span class="sxs-lookup"><span data-stu-id="80695-149">Service providers can use this range to store passwords and other provider-specific credentials.</span></span> <span data-ttu-id="80695-150">Свойства в этом диапазоне не возвращаются в полном списке свойств, когда значение NULL передается в параметре _лппроптаг_ метода [IMAPIProp::](imapiprop-getprops.md) -Props, и они возвращаются в параметре _лпппроптагаррай_ [ IMAPIProp:: метод Жетпроплист](imapiprop-getproplist.md) .</span><span class="sxs-lookup"><span data-stu-id="80695-150">Properties in this range are not returned in the complete list of properties when NULL is passed in the  _lpPropTag_ parameter of the [IMAPIProp::GetProps](imapiprop-getprops.md) method, nor are they returned in the  _lppPropTagArray_ parameter of the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> <span data-ttu-id="80695-151">Свойства безопасности должны запрашиваться именно их идентификаторами.</span><span class="sxs-lookup"><span data-stu-id="80695-151">Secure properties must be requested specifically by their identifiers.</span></span> 
  
<span data-ttu-id="80695-152">MAPI представляя раздел профиля с жестко заданными константами МУИД_ПРОФИЛЕ_ИНСТАНЦЕ в качестве идентификатора и **пр_сеарч_кэй** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) в качестве единого свойства.</span><span class="sxs-lookup"><span data-stu-id="80695-152">MAPI furnishes a profile section with the hard-coded constant MUID_PROFILE_INSTANCE as its identifier and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) as its single property.</span></span> <span data-ttu-id="80695-153">MAPI гарантирует, что значение свойства **пр_сеарч_кэй** будет уникальным среди всех созданных профилей.</span><span class="sxs-lookup"><span data-stu-id="80695-153">MAPI ensures that the **PR_SEARCH_KEY** property value will be unique among all created profiles.</span></span> <span data-ttu-id="80695-154">Используйте **пр_сеарч_кэй** вместо **пр_профиле_наме** , если важна уникальность, так как за удаленным профилем может следовать другой профиль с таким же именем.</span><span class="sxs-lookup"><span data-stu-id="80695-154">Use **PR_SEARCH_KEY** instead of **PR_PROFILE_NAME** when uniqueness is important, because it is possible for a deleted profile to be followed by another profile with the same name.</span></span> 
  
<span data-ttu-id="80695-155">Более подробную информацию об использовании разделов профилей можно узнать в статье [Администрирование профилей и служб сообщений](administering-profiles-and-message-services.md).</span><span class="sxs-lookup"><span data-stu-id="80695-155">For more information about how to use profile sections, see [Administering Profiles and Message Services](administering-profiles-and-message-services.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="80695-156">См. также</span><span class="sxs-lookup"><span data-stu-id="80695-156">See also</span></span>



[<span data-ttu-id="80695-157">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="80695-157">MAPI Interfaces</span></span>](mapi-interfaces.md)

