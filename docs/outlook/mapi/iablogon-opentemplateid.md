---
title: IABLogonOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenTemplateID
api_type:
- COM
ms.assetid: 751c36d3-c39e-4357-a60a-88685a378de0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bc68878a25873533162df7e1671e483c3bb77865
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334750"
---
# <a name="iablogonopentemplateid"></a><span data-ttu-id="ed8c3-103">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="ed8c3-103">IABLogon::OpenTemplateID</span></span>

  
  
<span data-ttu-id="ed8c3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed8c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed8c3-105">Открывает запись получателя, которая имеет данные, проживающие в поставщике адресной книги хост- адресов.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-105">Opens a recipient entry that has data residing in a host address book provider.</span></span>
  
```cpp
HRESULT OpenTemplateID(
  ULONG cbTemplateID,
  LPENTRYID lpTemplateID,
  ULONG ulTemplateFlags,
  LPMAPIPROP lpMAPIPropData,
  LPCIID lpInterface,
  LPMAPIPROP FAR * lppMAPIPropNew,
  LPMAPIPROP lpMAPIPropSibling
);
```

## <a name="parameters"></a><span data-ttu-id="ed8c3-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ed8c3-106">Parameters</span></span>

 <span data-ttu-id="ed8c3-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="ed8c3-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="ed8c3-108">[in] Количество byte в идентификаторе шаблона, на который указывает _параметр lpTemplateID._</span><span class="sxs-lookup"><span data-stu-id="ed8c3-108">[in] The byte count in the template identifier pointed to by the  _lpTemplateID_ parameter.</span></span> 
    
 <span data-ttu-id="ed8c3-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="ed8c3-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="ed8c3-110">[in] Указатель на идентификатор шаблона **или свойство** [PR_TEMPLATEID (PidTagTemplateid)](pidtagtemplateid-canonical-property.md)для открываемой записи получателя.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-110">[in] A pointer to the template identifier, or **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="ed8c3-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="ed8c3-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="ed8c3-112">[in] Битмашка флагов, используемых для того, чтобы указать, как открыть запись, представленную идентификатором шаблона.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-112">[in] A bitmask of flags used to indicate how to open the entry represented by the template identifier.</span></span> <span data-ttu-id="ed8c3-113">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="ed8c3-113">The following flag can be set:</span></span>
    
<span data-ttu-id="ed8c3-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="ed8c3-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="ed8c3-115">Поставщик хостов создает новую запись в контейнере на основе записи, представленной идентификатором шаблона.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-115">The host provider is creating a new entry in its container based on the entry represented by the template identifier.</span></span> <span data-ttu-id="ed8c3-116">Метод **IABLogon::OpenTemplateID** должен либо выполнять определенную инициализацию записи поставщика хостов с помощью [реализации IMAPIProp: IUnknown](imapipropiunknown.md) в параметре _lpMAPIPropData,_ либо возвращать настраиваемую реализацию интерфейса **IMAPIProp в** _параметре lppMAPIPropNew._</span><span class="sxs-lookup"><span data-stu-id="ed8c3-116">The **IABLogon::OpenTemplateID** method should either perform specific initialization of the host provider's entry by using the [IMAPIProp : IUnknown](imapipropiunknown.md) implementation in the  _lpMAPIPropData_ parameter, or return a custom **IMAPIProp** interface implementation in the  _lppMAPIPropNew_ parameter.</span></span> 
    
 <span data-ttu-id="ed8c3-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="ed8c3-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="ed8c3-118">[in] Указатель на объект свойства хост-поставщика и реализацию интерфейса, полученного из **IMAPIProp.**</span><span class="sxs-lookup"><span data-stu-id="ed8c3-118">[in] A pointer to the host provider's property object and implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="ed8c3-119">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="ed8c3-119">_lpInterface_</span></span>
  
> <span data-ttu-id="ed8c3-120">[in] Указатель на идентификатор интерфейса (IID), который представляет тип указателя интерфейса, возвращаемого в _параметре lppMAPIPropNew._</span><span class="sxs-lookup"><span data-stu-id="ed8c3-120">[in] A pointer to the interface identifier (IID) that represents the type of interface pointer to be returned in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="ed8c3-121">Передача **null** возвращает стандартный пользовательский интерфейс обмена сообщениями [IMailUser : IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="ed8c3-121">Passing **null** returns the standard messaging user interface, [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span>
    
 <span data-ttu-id="ed8c3-122">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="ed8c3-122">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="ed8c3-123">[вышел] Указатель на связанный объект свойства и реализация интерфейса, полученного из **IMAPIProp.**</span><span class="sxs-lookup"><span data-stu-id="ed8c3-123">[out] A pointer to the bound property object and an implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="ed8c3-124">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="ed8c3-124">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="ed8c3-125">[вышел] Зарезервировано; должно быть **null**.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-125">[out] Reserved; must be **null**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ed8c3-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed8c3-126">Return value</span></span>

<span data-ttu-id="ed8c3-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="ed8c3-127">S_OK</span></span> 
  
> <span data-ttu-id="ed8c3-128">Соответствующий код был успешно связан с связанными данными в принимающем поставщике.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-128">The appropriate code was successfully bound to related data in the host provider.</span></span>
    
<span data-ttu-id="ed8c3-129">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="ed8c3-129">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="ed8c3-130">Объект не поддерживает ИД шаблонов.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-130">The object does not support template IDs.</span></span>
    
<span data-ttu-id="ed8c3-131">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ed8c3-131">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="ed8c3-132">Идентификатор шаблона, переданный в  _параметре lpTemplateID,_ не распознается поставщиком адресной книги.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-132">The template identifier passed in the  _lpTemplateID_ parameter is not recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ed8c3-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="ed8c3-133">Remarks</span></span>

<span data-ttu-id="ed8c3-134">Метод **IABLogon::OpenTemplateID** реализуется только поставщиками адресных книг, которые должны контролировать копии записей, расположенных в контейнерах поставщиков хостов.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-134">The **IABLogon::OpenTemplateID** method is implemented only by address book providers that need to maintain control over copies of their entries that are located in the containers of host providers.</span></span> <span data-ttu-id="ed8c3-135">Поставщики, реализуют **OpenTemplateID,** известны как иностранные поставщики адресных книг.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-135">Providers that implement **OpenTemplateID** are known as foreign address book providers.</span></span> <span data-ttu-id="ed8c3-136">Поставщики хостов звонят [по вызову IMAPISupport::OpenTemplateID,](imapisupport-opentemplateid.md) чтобы создать скопированную запись или открыть скопированную запись, и MAPI передает вызов **в IABLogon::OpenTemplateID**.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-136">Host providers call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to create a copied entry or open the copied entry, and MAPI passes on the call to **IABLogon::OpenTemplateID**.</span></span> <span data-ttu-id="ed8c3-137">**IABLogon::OpenTemplateID** открывает запись и связывает код, который управляет этим кодом, с данными в принимающем поставщике.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-137">**IABLogon::OpenTemplateID** opens the entry and binds the code that controls it to data in the host provider.</span></span> 
  
<span data-ttu-id="ed8c3-138">Вместо использования идентификатора записи **IABLogon::OpenTemplateID** использует другое свойство, идентификатор шаблона **записи, PR_TEMPLATEID**.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-138">Rather than use an entry identifier, **IABLogon::OpenTemplateID** uses another property, the entry's template identifier, **PR_TEMPLATEID**.</span></span> <span data-ttu-id="ed8c3-139">Идентификаторы шаблонов должны поддерживаться для записей, код которых должен быть привязан к данным в принимающем поставщике.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-139">Template identifiers should be supported for entries whose code must be bound to data in a host provider.</span></span>
  
<span data-ttu-id="ed8c3-140">Примеры того, когда поставщик адресных книг должен реализовать **IABLogon::OpenTemplateID,** являются следующими:</span><span class="sxs-lookup"><span data-stu-id="ed8c3-140">Some examples of when an address book provider should implement **IABLogon::OpenTemplateID** are as follows:</span></span> 
  
- <span data-ttu-id="ed8c3-141">Чтобы периодически обновлять данные для скопированные записи, чтобы они оставались синхронизированными с оригиналом.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-141">To periodically update the data for a copied entry so that it stays synchronized with the original.</span></span>
    
- <span data-ttu-id="ed8c3-142">Реализация функций, которые не может реализовать поставщик хостов, например динамическое заполнение списка, который отображается в таблице сведений записи из данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-142">To implement functionality that the host provider cannot implement, such as dynamically populating a list that appears in the entry's details table from data on a server.</span></span>
    
- <span data-ttu-id="ed8c3-143">Управление взаимодействием между свойствами в записи поставщика размещения и исходной **записью,** например вычислением PR_EMAIL_ADDRESS [(PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)из значений элементов управления редактирования в отображения сведений, содержащих различные компоненты адреса.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-143">To control the interaction between properties in the host provider's entry and the original entry, such as computing the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) from the values of the edit controls in the details display that contain different components of the address.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="ed8c3-144">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="ed8c3-144">Notes to implementers</span></span>

<span data-ttu-id="ed8c3-145">Когда поставщик хостинга копирует или создает запись от поставщика, и вы поставляете реализацию объекта свойства через **IABLogon::OpenTemplateID,** вы обрабатываете большинство вызовов для поддержания записи.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-145">When a host provider copies or creates an entry from your provider and you supply a property object implementation through **IABLogon::OpenTemplateID**, you handle most of the calls to maintain the entry.</span></span> <span data-ttu-id="ed8c3-146">Однако, так как передаваемые вызовы должны быть перенаадчены поставщику хостов, он может перехватить любой вызов и выполнить настраиваемую обработку перед переададной.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-146">However, because it is up to the host provider to forward these calls to you, the host provider can intercept any call and perform custom processing before forwarding the call.</span></span>
  
<span data-ttu-id="ed8c3-147">В реализации объектов свойства следует использовать следующие рекомендации:</span><span class="sxs-lookup"><span data-stu-id="ed8c3-147">You should use the following guidelines in your property object implementations:</span></span>
  
- <span data-ttu-id="ed8c3-148">Когда [вызван IMAPIProp::GetProps,](imapiprop-getprops.md) определите, является ли запрос для вычислительного свойства и, если это так, обрабатывать его.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-148">When [IMAPIProp::GetProps](imapiprop-getprops.md) is called, determine whether the request is for a computed property and, if it is, handle it.</span></span> <span data-ttu-id="ed8c3-149">Передай все запросы на некомпьютерные свойства поставщику размещения.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-149">Transfer all requests for noncomputed properties to the host provider.</span></span> 
    
- <span data-ttu-id="ed8c3-150">Когда [IMAPIProp::OpenProperty](imapiprop-openproperty.md) вызван для открытия любой таблицы, кроме таблицы отображения сведений, обрабатывают запрос.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-150">When [IMAPIProp::OpenProperty](imapiprop-openproperty.md) is called to open any table except the details display table, handle the request.</span></span> <span data-ttu-id="ed8c3-151">Большинство таблиц не могут быть точно скопированы поставщику хостов.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-151">Most tables cannot be copied accurately to the host provider.</span></span> <span data-ttu-id="ed8c3-152">Для этих запрашиваемых таблиц необходимо создать **реализацию IMAPITable.**</span><span class="sxs-lookup"><span data-stu-id="ed8c3-152">You must generate the **IMAPITable** implementation for these requested tables.</span></span> <span data-ttu-id="ed8c3-153">В таблице **PR_DETAILS_TABLE** [(PidTagDetailsTable)](pidtagdetailstable-canonical-property.md)свойство должно быть скопировано с хост-провайдером.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-153">The details table **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property must be copied to the host provider.</span></span> <span data-ttu-id="ed8c3-154">Это позволяет этому поставщику создавать таблицу локально.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-154">This allows this provider to generate the table locally.</span></span> <span data-ttu-id="ed8c3-155">Может потребоваться обернуть реализацию таблицы отображения для создания уведомлений таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-155">You might want to wrap the display table implementation to generate display table notifications.</span></span> 
    
- <span data-ttu-id="ed8c3-156">Когда [вызван IMAPIProp::SetProps,](imapiprop-setprops.md) поставщик хостов может проверить данные, прежде чем дать вам задать свойства.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-156">When [IMAPIProp::SetProps](imapiprop-setprops.md) is called, the host provider can validate the data before letting you set the properties.</span></span> <span data-ttu-id="ed8c3-157">Вы можете убедиться, что все необходимые свойства были настроены или вычислены.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-157">You can verify that all of the necessary properties were set or computed.</span></span> <span data-ttu-id="ed8c3-158">Если ошибка обнаружена, верни соответствующее значение ошибки и, если можно, любое дополнительное объяснение через [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span><span class="sxs-lookup"><span data-stu-id="ed8c3-158">If an error is detected, return the appropriate error value and, if you can, any additional explanation through [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span></span>
    
- <span data-ttu-id="ed8c3-159">Когда [вызваны IMAPIProp::SaveChanges,](imapiprop-savechanges.md) поставщику хостов может потребоваться выполнить обработку перед сохранением записи.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-159">When [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called, the host provider might want to perform processing before you save the entry.</span></span> <span data-ttu-id="ed8c3-160">Необходимо сохранить все данные, которые влияют на измененные свойства, например новый адрес, в записи поставщика размещения.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-160">You should save any data that is affected by the changed properties, such as a new address, in the host provider's entry.</span></span> 
    
<span data-ttu-id="ed8c3-161">В общем, сделайте так, чтобы реализация записи, которую вы передаете поставщику хостов, перехватывала все методы для выполнения контекстных манипуляций с соответствующими свойствами.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-161">In general, make your implementation of the entry that you pass back to the host provider intercept all of the methods to perform context-specific manipulation of the relevant properties.</span></span> <span data-ttu-id="ed8c3-162">Если флаг FILL_ENTRY в  _параметре ulTemplateFlags,_ задай все свойства для входа.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-162">If the FILL_ENTRY flag is passed in the  _ulTemplateFlags_ parameter, set all properties for the entry.</span></span> 
  
<span data-ttu-id="ed8c3-163">Если вы возвращаете новый объект свойства в  _параметре lppMAPIPropNew,_ позвоните [методу IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) объекта свойства поставщика хостов, чтобы сохранить ссылку.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-163">If you return a new property object in the  _lppMAPIPropNew_ parameter, call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method of the host provider's property object to maintain a reference.</span></span> <span data-ttu-id="ed8c3-164">Все вызовы через связанный объект, возвращенный реализацией **IMAPIProp** в  _lppMAPIPropNew,_ должны быть перенаправлены в соответствующий метод в объекте свойства хост после их решения связанным объектом.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-164">All calls through the bound object that the **IMAPIProp** implementation returned in  _lppMAPIPropNew_ should be routed to their corresponding method in the host property object after they are dealt with by the bound object.</span></span> 
  
<span data-ttu-id="ed8c3-165">Идентификаторы свойств всех именных свойств, которые передаются через связанный объект свойства, находятся в пространстве имен идентификатора поставщика.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-165">The property identifiers of any named properties that are passed through your bound property object are in your provider's identifier namespace.</span></span> <span data-ttu-id="ed8c3-166">Реализация метода [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) должна определять имена свойств, чтобы он выполнял любые задачи, определенные шаблону.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-166">Your implementation of the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method should determine the names of the properties so that it can perform any template-specific tasks.</span></span> <span data-ttu-id="ed8c3-167">Кроме того, свойства, которые поставщик передает поставщику хостов, также должны быть в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-167">Similarly, properties that your provider passes on to the host provider must also be in your namespace.</span></span> <span data-ttu-id="ed8c3-168">Например, если в **OpenTemplateID** задано имя имени, следует использовать один из идентификаторов для имени, создав его, если это необходимо, позвонив по методу [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="ed8c3-168">For example, if you set a named property in **OpenTemplateID**, you should use one of your identifiers for the name—creating it, if necessary, by calling the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="ed8c3-169">Если вы не узнаете идентификатор записи, переданный  _в lpTemplateID,_ MAPI_E_UNKNOWN_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="ed8c3-169">If you do not recognize the entry identifier passed in  _lpTemplateID_, return MAPI_E_UNKNOWN_ENTRYID.</span></span>
  
<span data-ttu-id="ed8c3-170">Дополнительные сведения о работе с идентификаторами шаблонов адресных книг см. в книге [Acting as a Foreign Address Book Provider.](acting-as-a-foreign-address-book-provider.md)</span><span class="sxs-lookup"><span data-stu-id="ed8c3-170">For more information about how to work with address book template identifiers, see [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ed8c3-171">См. также</span><span class="sxs-lookup"><span data-stu-id="ed8c3-171">See also</span></span>



[<span data-ttu-id="ed8c3-172">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="ed8c3-172">IMAPISupport::OpenTemplateID</span></span>](imapisupport-opentemplateid.md)
  
[<span data-ttu-id="ed8c3-173">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ed8c3-173">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="ed8c3-174">Каноническое свойство PidTagTemplateid</span><span class="sxs-lookup"><span data-stu-id="ed8c3-174">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="ed8c3-175">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ed8c3-175">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

