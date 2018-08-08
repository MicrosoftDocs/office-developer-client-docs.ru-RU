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
ms.openlocfilehash: f2fedd98fe84d7359aebaca8d03a20f392dae2b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808734"
---
# <a name="iablogonopentemplateid"></a><span data-ttu-id="06d96-103">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="06d96-103">IABLogon::OpenTemplateID</span></span>

  
  
<span data-ttu-id="06d96-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="06d96-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="06d96-105">Открывает запись получателя, который содержит данные, хранимые в адресной книге узла.</span><span class="sxs-lookup"><span data-stu-id="06d96-105">Opens a recipient entry that has data residing in a host address book provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="06d96-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="06d96-106">Parameters</span></span>

 <span data-ttu-id="06d96-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="06d96-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="06d96-108">[in] Число байтов в идентификатор шаблона, на который указывает параметр _lpTemplateID_ .</span><span class="sxs-lookup"><span data-stu-id="06d96-108">[in] The byte count in the template identifier pointed to by the  _lpTemplateID_ parameter.</span></span> 
    
 <span data-ttu-id="06d96-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="06d96-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="06d96-110">[in] Указатель на идентификатор шаблона или свойство **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) получателей записи, которую требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="06d96-110">[in] A pointer to the template identifier, or **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="06d96-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="06d96-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="06d96-112">[in] Битовая маска флагов, используемых для указания того, как открыть запись, представленное идентификатор шаблона.</span><span class="sxs-lookup"><span data-stu-id="06d96-112">[in] A bitmask of flags used to indicate how to open the entry represented by the template identifier.</span></span> <span data-ttu-id="06d96-113">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="06d96-113">The following flag can be set:</span></span>
    
<span data-ttu-id="06d96-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="06d96-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="06d96-115">Поставщик узла создания записи в контейнера на основе записи, представленного идентификатор шаблона.</span><span class="sxs-lookup"><span data-stu-id="06d96-115">The host provider is creating a new entry in its container based on the entry represented by the template identifier.</span></span> <span data-ttu-id="06d96-116">Метод **IABLogon::OpenTemplateID** либо должен выполнять определенные инициализации запись узла поставщика с помощью [IMAPIProp: IUnknown](imapipropiunknown.md) реализации в параметре _lpMAPIPropData_ или return настраиваемую **IMAPIProp **реализация с помощью параметра _lppMAPIPropNew_ интерфейса.</span><span class="sxs-lookup"><span data-stu-id="06d96-116">The **IABLogon::OpenTemplateID** method should either perform specific initialization of the host provider's entry by using the [IMAPIProp : IUnknown](imapipropiunknown.md) implementation in the  _lpMAPIPropData_ parameter, or return a custom **IMAPIProp** interface implementation in the  _lppMAPIPropNew_ parameter.</span></span> 
    
 <span data-ttu-id="06d96-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="06d96-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="06d96-118">[in] Указатель на объект свойств и реализация интерфейса поставщика узла на основе **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="06d96-118">[in] A pointer to the host provider's property object and implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="06d96-119">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="06d96-119">_lpInterface_</span></span>
  
> <span data-ttu-id="06d96-120">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет тип указателя интерфейса должно быть возвращено с помощью параметра _lppMAPIPropNew_ .</span><span class="sxs-lookup"><span data-stu-id="06d96-120">[in] A pointer to the interface identifier (IID) that represents the type of interface pointer to be returned in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="06d96-121">Передача **null** Возвращает стандартный пользовательский интерфейс системы обмена сообщениями [IMailUser: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="06d96-121">Passing **null** returns the standard messaging user interface, [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span>
    
 <span data-ttu-id="06d96-122">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="06d96-122">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="06d96-123">[out] Указатель на объект привязки свойств и реализация интерфейса на основе **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="06d96-123">[out] A pointer to the bound property object and an implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="06d96-124">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="06d96-124">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="06d96-125">[out] Зарезервировано; должен иметь **значение null**.</span><span class="sxs-lookup"><span data-stu-id="06d96-125">[out] Reserved; must be **null**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="06d96-126">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="06d96-126">Return value</span></span>

<span data-ttu-id="06d96-127">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="06d96-127">S_OK</span></span> 
  
> <span data-ttu-id="06d96-128">Соответствующий код был успешно привязан к связанных данных в поставщике узла.</span><span class="sxs-lookup"><span data-stu-id="06d96-128">The appropriate code was successfully bound to related data in the host provider.</span></span>
    
<span data-ttu-id="06d96-129">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="06d96-129">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="06d96-130">Объект не поддерживает идентификаторы шаблонов.</span><span class="sxs-lookup"><span data-stu-id="06d96-130">The object does not support template IDs.</span></span>
    
<span data-ttu-id="06d96-131">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="06d96-131">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="06d96-132">Идентификатор шаблона, переданной в параметре _lpTemplateID_ не распознается поставщик адресной книги.</span><span class="sxs-lookup"><span data-stu-id="06d96-132">The template identifier passed in the  _lpTemplateID_ parameter is not recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="06d96-133">Замечания</span><span class="sxs-lookup"><span data-stu-id="06d96-133">Remarks</span></span>

<span data-ttu-id="06d96-134">Метод **IABLogon::OpenTemplateID** реализована только с поставщиками адресных книг, которые необходимо контролировать копий своих записей, которые расположены в контейнерах поставщиков услуг размещения.</span><span class="sxs-lookup"><span data-stu-id="06d96-134">The **IABLogon::OpenTemplateID** method is implemented only by address book providers that need to maintain control over copies of their entries that are located in the containers of host providers.</span></span> <span data-ttu-id="06d96-135">Поставщики, которые реализуют **OpenTemplateID** называются поставщиками внешнего адресной книги.</span><span class="sxs-lookup"><span data-stu-id="06d96-135">Providers that implement **OpenTemplateID** are known as foreign address book providers.</span></span> <span data-ttu-id="06d96-136">Поставщики узла вызова [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) для создания скопированной записи или откройте скопированный запись, и передает MAPI на вызов **IABLogon::OpenTemplateID**.</span><span class="sxs-lookup"><span data-stu-id="06d96-136">Host providers call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to create a copied entry or open the copied entry, and MAPI passes on the call to **IABLogon::OpenTemplateID**.</span></span> <span data-ttu-id="06d96-137">**IABLogon::OpenTemplateID** открывает запись и связывает код, который управляет к данным в поставщике узла.</span><span class="sxs-lookup"><span data-stu-id="06d96-137">**IABLogon::OpenTemplateID** opens the entry and binds the code that controls it to data in the host provider.</span></span> 
  
<span data-ttu-id="06d96-138">А не использовать запись идентификатора, **IABLogon::OpenTemplateID** используется другой свойство, идентификатор шаблона элемента, **PR_TEMPLATEID**.</span><span class="sxs-lookup"><span data-stu-id="06d96-138">Rather than use an entry identifier, **IABLogon::OpenTemplateID** uses another property, the entry's template identifier, **PR_TEMPLATEID**.</span></span> <span data-ttu-id="06d96-139">Идентификаторы шаблон должен поддерживается для записей, код должен быть привязан к данным в этот поставщик.</span><span class="sxs-lookup"><span data-stu-id="06d96-139">Template identifiers should be supported for entries whose code must be bound to data in a host provider.</span></span>
  
<span data-ttu-id="06d96-140">Некоторые примеры когда поставщика адресных книг должна реализовать **IABLogon::OpenTemplateID** , как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="06d96-140">Some examples of when an address book provider should implement **IABLogon::OpenTemplateID** are as follows:</span></span> 
  
- <span data-ttu-id="06d96-141">Периодически обновлять данные в скопированной записи, чтобы он остается синхронизированы с исходной.</span><span class="sxs-lookup"><span data-stu-id="06d96-141">To periodically update the data for a copied entry so that it stays synchronized with the original.</span></span>
    
- <span data-ttu-id="06d96-142">Чтобы реализовать функциональные возможности, которые не могут реализовать поставщик узла, такие как динамическое заполнение списка, который отображается в таблице запись сведений на основе данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="06d96-142">To implement functionality that the host provider cannot implement, such as dynamically populating a list that appears in the entry's details table from data on a server.</span></span>
    
- <span data-ttu-id="06d96-143">Для управления взаимодействием между свойствами в запись узла поставщика и исходной операции, такие как вычисления **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) из значений редактирования элементов управления в окне сведений, которые содержат различные компоненты адреса.</span><span class="sxs-lookup"><span data-stu-id="06d96-143">To control the interaction between properties in the host provider's entry and the original entry, such as computing the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) from the values of the edit controls in the details display that contain different components of the address.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="06d96-144">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="06d96-144">Notes to implementers</span></span>

<span data-ttu-id="06d96-145">Когда этот поставщик копирует или создает запись у поставщика и предоставить реализацию свойства объекта через **IABLogon::OpenTemplateID**, обрабатывать большинство вызовов на обслуживание операция.</span><span class="sxs-lookup"><span data-stu-id="06d96-145">When a host provider copies or creates an entry from your provider and you supply a property object implementation through **IABLogon::OpenTemplateID**, you handle most of the calls to maintain the entry.</span></span> <span data-ttu-id="06d96-146">Тем не менее так как это до узла поставщика для переадресации звонков, эти вам поставщик узла можно перехвата любой вызов и выполнять настраиваемые функции обработки перед переадресацией звонка.</span><span class="sxs-lookup"><span data-stu-id="06d96-146">However, because it is up to the host provider to forward these calls to you, the host provider can intercept any call and perform custom processing before forwarding the call.</span></span>
  
<span data-ttu-id="06d96-147">В реализации объекта свойства следует использовать следующие рекомендации:</span><span class="sxs-lookup"><span data-stu-id="06d96-147">You should use the following guidelines in your property object implementations:</span></span>
  
- <span data-ttu-id="06d96-148">При вызове [IMAPIProp::GetProps](imapiprop-getprops.md) определите, являются ли запрос для вычисляемого свойства и, если он установлен, его обработки.</span><span class="sxs-lookup"><span data-stu-id="06d96-148">When [IMAPIProp::GetProps](imapiprop-getprops.md) is called, determine whether the request is for a computed property and, if it is, handle it.</span></span> <span data-ttu-id="06d96-149">Перенос всех запросов для невычисляемого свойств для размещения поставщика.</span><span class="sxs-lookup"><span data-stu-id="06d96-149">Transfer all requests for noncomputed properties to the host provider.</span></span> 
    
- <span data-ttu-id="06d96-150">При вызове [IMAPIProp::OpenProperty](imapiprop-openproperty.md) для открытия любой таблицы, за исключением сведения отображения таблицы, обработать запрос.</span><span class="sxs-lookup"><span data-stu-id="06d96-150">When [IMAPIProp::OpenProperty](imapiprop-openproperty.md) is called to open any table except the details display table, handle the request.</span></span> <span data-ttu-id="06d96-151">Большинство таблицы не удается скопировать точно для размещения поставщика.</span><span class="sxs-lookup"><span data-stu-id="06d96-151">Most tables cannot be copied accurately to the host provider.</span></span> <span data-ttu-id="06d96-152">Необходимо создать **IMAPITable** реализации для этих запрошенные таблиц.</span><span class="sxs-lookup"><span data-stu-id="06d96-152">You must generate the **IMAPITable** implementation for these requested tables.</span></span> <span data-ttu-id="06d96-153">Свойство **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) сведения о таблице нужно скопировать поставщик узла.</span><span class="sxs-lookup"><span data-stu-id="06d96-153">The details table **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property must be copied to the host provider.</span></span> <span data-ttu-id="06d96-154">Это позволяет данного поставщика для создания таблицы локально.</span><span class="sxs-lookup"><span data-stu-id="06d96-154">This allows this provider to generate the table locally.</span></span> <span data-ttu-id="06d96-155">Может потребоваться перенос реализации отображения таблицы для создания уведомлений в таблице отображения.</span><span class="sxs-lookup"><span data-stu-id="06d96-155">You might want to wrap the display table implementation to generate display table notifications.</span></span> 
    
- <span data-ttu-id="06d96-156">При вызове [IMAPIProp::SetProps](imapiprop-setprops.md) поставщик узла можно проверить данные перед предоставлением можно задать свойства.</span><span class="sxs-lookup"><span data-stu-id="06d96-156">When [IMAPIProp::SetProps](imapiprop-setprops.md) is called, the host provider can validate the data before letting you set the properties.</span></span> <span data-ttu-id="06d96-157">Вы можете проверить, что все необходимые свойства задайте или вычислить.</span><span class="sxs-lookup"><span data-stu-id="06d96-157">You can verify that all of the necessary properties were set or computed.</span></span> <span data-ttu-id="06d96-158">Если обнаружена ошибка возврата соответствующего значения ошибки и, если это возможно, любые дополнительные объяснение через [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span><span class="sxs-lookup"><span data-stu-id="06d96-158">If an error is detected, return the appropriate error value and, if you can, any additional explanation through [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span></span>
    
- <span data-ttu-id="06d96-159">При вызове [IMAPIProp::SaveChanges](imapiprop-savechanges.md) узла поставщика может потребоваться обработка перед сохраните запись.</span><span class="sxs-lookup"><span data-stu-id="06d96-159">When [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called, the host provider might want to perform processing before you save the entry.</span></span> <span data-ttu-id="06d96-160">Следует сохранить все данные, которые были затронуты измененных свойств, например новый адрес в запись узла поставщика.</span><span class="sxs-lookup"><span data-stu-id="06d96-160">You should save any data that is affected by the changed properties, such as a new address, in the host provider's entry.</span></span> 
    
<span data-ttu-id="06d96-161">В общем случае внести внедрения записи, передаваемого поставщик узла перехватывать все методы для выполнения обработки контекстные соответствующих свойств.</span><span class="sxs-lookup"><span data-stu-id="06d96-161">In general, make your implementation of the entry that you pass back to the host provider intercept all of the methods to perform context-specific manipulation of the relevant properties.</span></span> <span data-ttu-id="06d96-162">Если флаг FILL_ENTRY передается в параметре _ulTemplateFlags_ , необходимо задайте все свойства для записи.</span><span class="sxs-lookup"><span data-stu-id="06d96-162">If the FILL_ENTRY flag is passed in the  _ulTemplateFlags_ parameter, set all properties for the entry.</span></span> 
  
<span data-ttu-id="06d96-163">Если новый объект свойство вернуться в параметре _lppMAPIPropNew_ , вызовите метод [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) объекта свойство поставщика узла на обслуживание ссылку.</span><span class="sxs-lookup"><span data-stu-id="06d96-163">If you return a new property object in the  _lppMAPIPropNew_ parameter, call the [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) method of the host provider's property object to maintain a reference.</span></span> <span data-ttu-id="06d96-164">Все вызовы через присоединенного объекта, возвращаемого реализации **IMAPIProp** в _lppMAPIPropNew_ должны направляться их соответствующий метод в объекте свойство узла после они обрабатываются объектом привязки.</span><span class="sxs-lookup"><span data-stu-id="06d96-164">All calls through the bound object that the **IMAPIProp** implementation returned in  _lppMAPIPropNew_ should be routed to their corresponding method in the host property object after they are dealt with by the bound object.</span></span> 
  
<span data-ttu-id="06d96-165">Идентификаторы свойств именованные свойства, которые передаются через объект связанное свойство находятся в пространстве имен идентификатор ваш поставщик.</span><span class="sxs-lookup"><span data-stu-id="06d96-165">The property identifiers of any named properties that are passed through your bound property object are in your provider's identifier namespace.</span></span> <span data-ttu-id="06d96-166">Реализация метода [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) необходимо определить имена свойств, чтобы он может выполнять любые задачи, связанные с шаблоном.</span><span class="sxs-lookup"><span data-stu-id="06d96-166">Your implementation of the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method should determine the names of the properties so that it can perform any template-specific tasks.</span></span> <span data-ttu-id="06d96-167">Аналогично свойства, которые ваш поставщик передается поставщик узла также должен быть в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="06d96-167">Similarly, properties that your provider passes on to the host provider must also be in your namespace.</span></span> <span data-ttu-id="06d96-168">Например, если значение именованного свойства в **OpenTemplateID**, следует использовать один из вашего идентификаторов для имени — создание его, если это необходимо, путем вызова метода [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="06d96-168">For example, if you set a named property in **OpenTemplateID**, you should use one of your identifiers for the name—creating it, if necessary, by calling the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="06d96-169">Если идентификатор записи, переданные в _lpTemplateID_не распознают, возвратите MAPI_E_UNKNOWN_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="06d96-169">If you do not recognize the entry identifier passed in  _lpTemplateID_, return MAPI_E_UNKNOWN_ENTRYID.</span></span>
  
<span data-ttu-id="06d96-170">Дополнительные сведения о работе с идентификаторами шаблон адресной книги можно [используется в качестве внешнего поставщик адресной книги](acting-as-a-foreign-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="06d96-170">For more information about how to work with address book template identifiers, see [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="06d96-171">См. также</span><span class="sxs-lookup"><span data-stu-id="06d96-171">See also</span></span>



[<span data-ttu-id="06d96-172">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="06d96-172">IMAPISupport::OpenTemplateID</span></span>](imapisupport-opentemplateid.md)
  
[<span data-ttu-id="06d96-173">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="06d96-173">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="06d96-174">Каноническое свойство PidTagTemplateid</span><span class="sxs-lookup"><span data-stu-id="06d96-174">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="06d96-175">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="06d96-175">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

