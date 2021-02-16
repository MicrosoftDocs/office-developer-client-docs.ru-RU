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
# <a name="iablogonopentemplateid"></a><span data-ttu-id="8bc82-103">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="8bc82-103">IABLogon::OpenTemplateID</span></span>

  
  
<span data-ttu-id="8bc82-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bc82-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bc82-105">Открывает запись получателя с данными, которые есть в поставщике адресной книги хост-адреса.</span><span class="sxs-lookup"><span data-stu-id="8bc82-105">Opens a recipient entry that has data residing in a host address book provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="8bc82-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8bc82-106">Parameters</span></span>

 <span data-ttu-id="8bc82-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="8bc82-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="8bc82-108">[in] Количество byte в идентификаторе шаблона, на который указывает _параметр lpTemplateID._</span><span class="sxs-lookup"><span data-stu-id="8bc82-108">[in] The byte count in the template identifier pointed to by the  _lpTemplateID_ parameter.</span></span> 
    
 <span data-ttu-id="8bc82-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="8bc82-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="8bc82-110">[in] Указатель на идентификатор шаблона или **PR_TEMPLATEID** ([PidTagTemplateid)](pidtagtemplateid-canonical-property.md)записи получателя, которая должна быть открыта.</span><span class="sxs-lookup"><span data-stu-id="8bc82-110">[in] A pointer to the template identifier, or **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="8bc82-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="8bc82-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="8bc82-112">[in] Битоваяmas флагов, используемая для того, чтобы указать, как открыть запись, представленную идентификатором шаблона.</span><span class="sxs-lookup"><span data-stu-id="8bc82-112">[in] A bitmask of flags used to indicate how to open the entry represented by the template identifier.</span></span> <span data-ttu-id="8bc82-113">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="8bc82-113">The following flag can be set:</span></span>
    
<span data-ttu-id="8bc82-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="8bc82-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="8bc82-115">Поставщик услуг хоста создает новую запись в своем контейнере на основе записи, представленной идентификатором шаблона.</span><span class="sxs-lookup"><span data-stu-id="8bc82-115">The host provider is creating a new entry in its container based on the entry represented by the template identifier.</span></span> <span data-ttu-id="8bc82-116">Метод **IABLogon::OpenTemplateID** должен либо выполнять определенную инициализацию записи поставщика услуг хоста с помощью [реализации IMAPIProp : IUnknown](imapipropiunknown.md) в _параметре lpMAPIPropData,_ либо возвращать пользовательскую реализацию интерфейса **IMAPIProp** в _параметре lppMAPIPropNew._</span><span class="sxs-lookup"><span data-stu-id="8bc82-116">The **IABLogon::OpenTemplateID** method should either perform specific initialization of the host provider's entry by using the [IMAPIProp : IUnknown](imapipropiunknown.md) implementation in the  _lpMAPIPropData_ parameter, or return a custom **IMAPIProp** interface implementation in the  _lppMAPIPropNew_ parameter.</span></span> 
    
 <span data-ttu-id="8bc82-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="8bc82-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="8bc82-118">[in] Указатель на объект свойства поставщика услуг хоста и реализацию интерфейса, производного от **IMAPIProp.**</span><span class="sxs-lookup"><span data-stu-id="8bc82-118">[in] A pointer to the host provider's property object and implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="8bc82-119">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="8bc82-119">_lpInterface_</span></span>
  
> <span data-ttu-id="8bc82-120">[in] Указатель на идентификатор интерфейса ( IID), который представляет тип указателя интерфейса, возвращаемого в _параметре lppMAPIPropNew._</span><span class="sxs-lookup"><span data-stu-id="8bc82-120">[in] A pointer to the interface identifier (IID) that represents the type of interface pointer to be returned in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="8bc82-121">Передача **null** возвращает стандартный пользовательский интерфейс обмена сообщениями [IMailUser : IMAPIProp.](imailuserimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="8bc82-121">Passing **null** returns the standard messaging user interface, [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span>
    
 <span data-ttu-id="8bc82-122">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="8bc82-122">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="8bc82-123">[out] Указатель на объект привязанного свойства и реализацию интерфейса, производного от **IMAPIProp.**</span><span class="sxs-lookup"><span data-stu-id="8bc82-123">[out] A pointer to the bound property object and an implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="8bc82-124">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="8bc82-124">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="8bc82-125">[out] Зарезервировано; должно быть **null**.</span><span class="sxs-lookup"><span data-stu-id="8bc82-125">[out] Reserved; must be **null**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8bc82-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8bc82-126">Return value</span></span>

<span data-ttu-id="8bc82-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="8bc82-127">S_OK</span></span> 
  
> <span data-ttu-id="8bc82-128">Соответствующий код успешно привязан к связанным данным в поставщике услуг.</span><span class="sxs-lookup"><span data-stu-id="8bc82-128">The appropriate code was successfully bound to related data in the host provider.</span></span>
    
<span data-ttu-id="8bc82-129">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="8bc82-129">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="8bc82-130">Объект не поддерживает ИД шаблонов.</span><span class="sxs-lookup"><span data-stu-id="8bc82-130">The object does not support template IDs.</span></span>
    
<span data-ttu-id="8bc82-131">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="8bc82-131">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="8bc82-132">Идентификатор шаблона, переданный в  _параметре lpTemplateID,_ не распознается поставщиком адресной книги.</span><span class="sxs-lookup"><span data-stu-id="8bc82-132">The template identifier passed in the  _lpTemplateID_ parameter is not recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8bc82-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="8bc82-133">Remarks</span></span>

<span data-ttu-id="8bc82-134">Метод **IABLogon::OpenTemplateID** реализуется только поставщиками адресных книг, которые должны контролировать копии записей, расположенных в контейнерах поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="8bc82-134">The **IABLogon::OpenTemplateID** method is implemented only by address book providers that need to maintain control over copies of their entries that are located in the containers of host providers.</span></span> <span data-ttu-id="8bc82-135">Поставщики, реализуют **OpenTemplateID,** называются поставщиками внешних адресных книг.</span><span class="sxs-lookup"><span data-stu-id="8bc82-135">Providers that implement **OpenTemplateID** are known as foreign address book providers.</span></span> <span data-ttu-id="8bc82-136">Поставщики услуг host вызовите [IMAPISupport::OpenTemplateID,](imapisupport-opentemplateid.md) чтобы создать скопированную запись или открыть скопированную запись, и MAPI передает вызов **в IABLogon::OpenTemplateID.**</span><span class="sxs-lookup"><span data-stu-id="8bc82-136">Host providers call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to create a copied entry or open the copied entry, and MAPI passes on the call to **IABLogon::OpenTemplateID**.</span></span> <span data-ttu-id="8bc82-137">**IABLogon::OpenTemplateID** открывает запись и привязывает код, который управляет ее данными в поставщике услуг.</span><span class="sxs-lookup"><span data-stu-id="8bc82-137">**IABLogon::OpenTemplateID** opens the entry and binds the code that controls it to data in the host provider.</span></span> 
  
<span data-ttu-id="8bc82-138">Вместо использования идентификатора записи **IABLogon::OpenTemplateID** использует другое свойство, идентификатор шаблона записи, **PR_TEMPLATEID**.</span><span class="sxs-lookup"><span data-stu-id="8bc82-138">Rather than use an entry identifier, **IABLogon::OpenTemplateID** uses another property, the entry's template identifier, **PR_TEMPLATEID**.</span></span> <span data-ttu-id="8bc82-139">Идентификаторы шаблонов должны поддерживаться для записей, код которых должен быть привязан к данным в поставщике услуг.</span><span class="sxs-lookup"><span data-stu-id="8bc82-139">Template identifiers should be supported for entries whose code must be bound to data in a host provider.</span></span>
  
<span data-ttu-id="8bc82-140">Вот некоторые примеры, когда поставщик адресной книги должен реализовать **IABLogon::OpenTemplateID:**</span><span class="sxs-lookup"><span data-stu-id="8bc82-140">Some examples of when an address book provider should implement **IABLogon::OpenTemplateID** are as follows:</span></span> 
  
- <span data-ttu-id="8bc82-141">Периодическое обновление данных для скопированной записи, чтобы они оставались синхронизированными с исходным.</span><span class="sxs-lookup"><span data-stu-id="8bc82-141">To periodically update the data for a copied entry so that it stays synchronized with the original.</span></span>
    
- <span data-ttu-id="8bc82-142">Реализация функций, которые не удается реализовать поставщику услуг, например динамическое заполнение списка, который отображается в таблице сведений записи из данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="8bc82-142">To implement functionality that the host provider cannot implement, such as dynamically populating a list that appears in the entry's details table from data on a server.</span></span>
    
- <span data-ttu-id="8bc82-143">Для управления взаимодействием между свойствами в записи поставщика услуг размещения и исходной записью, например вычисление **PR_EMAIL_ADDRESS** ([PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)из значений элементов управления редактированием в сведениях, содержащих различные компоненты адреса.</span><span class="sxs-lookup"><span data-stu-id="8bc82-143">To control the interaction between properties in the host provider's entry and the original entry, such as computing the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) from the values of the edit controls in the details display that contain different components of the address.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="8bc82-144">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="8bc82-144">Notes to implementers</span></span>

<span data-ttu-id="8bc82-145">Когда поставщик услуг хоста копирует или создает запись у поставщика и вы передаете реализацию объекта свойства через **IABLogon::OpenTemplateID,** большинство вызовов обрабатываются для поддержания записи.</span><span class="sxs-lookup"><span data-stu-id="8bc82-145">When a host provider copies or creates an entry from your provider and you supply a property object implementation through **IABLogon::OpenTemplateID**, you handle most of the calls to maintain the entry.</span></span> <span data-ttu-id="8bc82-146">Однако, так как поставщик услуг связи может перенаададовывать эти вызовы вам, поставщик услуг хоста может перехватить любой вызов и выполнить пользовательскую обработку перед переад назад.</span><span class="sxs-lookup"><span data-stu-id="8bc82-146">However, because it is up to the host provider to forward these calls to you, the host provider can intercept any call and perform custom processing before forwarding the call.</span></span>
  
<span data-ttu-id="8bc82-147">В реализации объектов свойств следует использовать следующие рекомендации:</span><span class="sxs-lookup"><span data-stu-id="8bc82-147">You should use the following guidelines in your property object implementations:</span></span>
  
- <span data-ttu-id="8bc82-148">При [обращении к IMAPIProp::GetProps](imapiprop-getprops.md) определите, является ли запрос для вычисляемого свойства и, если это так, обработать его.</span><span class="sxs-lookup"><span data-stu-id="8bc82-148">When [IMAPIProp::GetProps](imapiprop-getprops.md) is called, determine whether the request is for a computed property and, if it is, handle it.</span></span> <span data-ttu-id="8bc82-149">Передать все запросы на несовершенные свойства поставщику услуг размещения.</span><span class="sxs-lookup"><span data-stu-id="8bc82-149">Transfer all requests for noncomputed properties to the host provider.</span></span> 
    
- <span data-ttu-id="8bc82-150">Когда [IMAPIProp::OpenProperty](imapiprop-openproperty.md) вызван для открытия любой таблицы, кроме отображаемой таблицы сведений, обрабатывают запрос.</span><span class="sxs-lookup"><span data-stu-id="8bc82-150">When [IMAPIProp::OpenProperty](imapiprop-openproperty.md) is called to open any table except the details display table, handle the request.</span></span> <span data-ttu-id="8bc82-151">Большинство таблиц не могут быть точно скопированы поставщику услуг.</span><span class="sxs-lookup"><span data-stu-id="8bc82-151">Most tables cannot be copied accurately to the host provider.</span></span> <span data-ttu-id="8bc82-152">Необходимо создать реализацию **IMAPITable** для этих запрашиваемых таблиц.</span><span class="sxs-lookup"><span data-stu-id="8bc82-152">You must generate the **IMAPITable** implementation for these requested tables.</span></span> <span data-ttu-id="8bc82-153">Таблица сведений **PR_DETAILS_TABLE** ([PidTagDetailsTable)](pidtagdetailstable-canonical-property.md)должна быть скопирована поставщику услуг.</span><span class="sxs-lookup"><span data-stu-id="8bc82-153">The details table **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property must be copied to the host provider.</span></span> <span data-ttu-id="8bc82-154">Это позволяет поставщику создавать таблицу локально.</span><span class="sxs-lookup"><span data-stu-id="8bc82-154">This allows this provider to generate the table locally.</span></span> <span data-ttu-id="8bc82-155">Вам может потребоваться обтекать реализацию таблицы отображения для создания уведомлений таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="8bc82-155">You might want to wrap the display table implementation to generate display table notifications.</span></span> 
    
- <span data-ttu-id="8bc82-156">При [наборе IMAPIProp::SetProps](imapiprop-setprops.md) поставщик услуг размещения может проверить данные, прежде чем устанавливать свойства.</span><span class="sxs-lookup"><span data-stu-id="8bc82-156">When [IMAPIProp::SetProps](imapiprop-setprops.md) is called, the host provider can validate the data before letting you set the properties.</span></span> <span data-ttu-id="8bc82-157">Вы можете убедиться, что все необходимые свойства установлены или вычислены.</span><span class="sxs-lookup"><span data-stu-id="8bc82-157">You can verify that all of the necessary properties were set or computed.</span></span> <span data-ttu-id="8bc82-158">Если ошибка обнаружена, вернетесь соответствующее значение ошибки и, если возможно, любое дополнительное объяснение с помощью [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span><span class="sxs-lookup"><span data-stu-id="8bc82-158">If an error is detected, return the appropriate error value and, if you can, any additional explanation through [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span></span>
    
- <span data-ttu-id="8bc82-159">При выполнении связи [IMAPIProp::SaveChanges](imapiprop-savechanges.md) поставщику услуг хоста может потребоваться выполнить обработку перед сохранением записи.</span><span class="sxs-lookup"><span data-stu-id="8bc82-159">When [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called, the host provider might want to perform processing before you save the entry.</span></span> <span data-ttu-id="8bc82-160">В записи поставщика услуг размещения необходимо сохранить все данные, на которые влияют измененные свойства, например новый адрес.</span><span class="sxs-lookup"><span data-stu-id="8bc82-160">You should save any data that is affected by the changed properties, such as a new address, in the host provider's entry.</span></span> 
    
<span data-ttu-id="8bc82-161">Как правило, реализация записи, передаемой поставщику услуг размещения, перехватывает все методы для выполнения обработки соответствующих свойств с учетом контекста.</span><span class="sxs-lookup"><span data-stu-id="8bc82-161">In general, make your implementation of the entry that you pass back to the host provider intercept all of the methods to perform context-specific manipulation of the relevant properties.</span></span> <span data-ttu-id="8bc82-162">Если флаг FILL_ENTRY передается в  _параметре ulTemplateFlags,_ установите все свойства записи.</span><span class="sxs-lookup"><span data-stu-id="8bc82-162">If the FILL_ENTRY flag is passed in the  _ulTemplateFlags_ parameter, set all properties for the entry.</span></span> 
  
<span data-ttu-id="8bc82-163">Если вы возвращаете новый объект свойства в параметре  _lppMAPIPropNew,_ вызовите метод [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) объекта свойства поставщика услуг хоста, чтобы сохранить ссылку.</span><span class="sxs-lookup"><span data-stu-id="8bc82-163">If you return a new property object in the  _lppMAPIPropNew_ parameter, call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method of the host provider's property object to maintain a reference.</span></span> <span data-ttu-id="8bc82-164">Все вызовы через привязанный объект, возвращенный реализацией **IMAPIProp** в  _lppMAPIPropNew,_ должны быть перенаправлены соответствующему методу в объекте свойства хоста после того, как объект привязана к ним.</span><span class="sxs-lookup"><span data-stu-id="8bc82-164">All calls through the bound object that the **IMAPIProp** implementation returned in  _lppMAPIPropNew_ should be routed to their corresponding method in the host property object after they are dealt with by the bound object.</span></span> 
  
<span data-ttu-id="8bc82-165">Идентификаторы свойств всех именуемого свойства, которые передаются через объект привязанного свойства, находятся в пространстве имен идентификатора поставщика.</span><span class="sxs-lookup"><span data-stu-id="8bc82-165">The property identifiers of any named properties that are passed through your bound property object are in your provider's identifier namespace.</span></span> <span data-ttu-id="8bc82-166">Реализация метода [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) должна определять имена свойств, чтобы он выполнял любые задачи, определенные в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="8bc82-166">Your implementation of the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method should determine the names of the properties so that it can perform any template-specific tasks.</span></span> <span data-ttu-id="8bc82-167">Аналогичным образом, свойства, которые поставщик передает поставщику услуг размещения, также должны быть в вашем пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="8bc82-167">Similarly, properties that your provider passes on to the host provider must also be in your namespace.</span></span> <span data-ttu-id="8bc82-168">Например, если в **OpenTemplateID** задано именовое свойство, следует использовать один из идентификаторов для имени — при необходимости создать его, вызывая метод [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="8bc82-168">For example, if you set a named property in **OpenTemplateID**, you should use one of your identifiers for the name—creating it, if necessary, by calling the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="8bc82-169">Если идентификатор записи, переданный в  _lpTemplateID,_ не распознается, MAPI_E_UNKNOWN_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="8bc82-169">If you do not recognize the entry identifier passed in  _lpTemplateID_, return MAPI_E_UNKNOWN_ENTRYID.</span></span>
  
<span data-ttu-id="8bc82-170">Дополнительные сведения о работе с идентификаторами шаблонов адресных книг см. в документе ["Действующие как поставщик внешних адресных книг".](acting-as-a-foreign-address-book-provider.md)</span><span class="sxs-lookup"><span data-stu-id="8bc82-170">For more information about how to work with address book template identifiers, see [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8bc82-171">См. также</span><span class="sxs-lookup"><span data-stu-id="8bc82-171">See also</span></span>



[<span data-ttu-id="8bc82-172">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="8bc82-172">IMAPISupport::OpenTemplateID</span></span>](imapisupport-opentemplateid.md)
  
[<span data-ttu-id="8bc82-173">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8bc82-173">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="8bc82-174">Каноническое свойство PidTagTemplateid</span><span class="sxs-lookup"><span data-stu-id="8bc82-174">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="8bc82-175">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8bc82-175">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

