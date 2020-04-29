---
title: иаблогонопентемплатеид
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
# <a name="iablogonopentemplateid"></a><span data-ttu-id="53ac3-103">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="53ac3-103">IABLogon::OpenTemplateID</span></span>

  
  
<span data-ttu-id="53ac3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53ac3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53ac3-105">Открывает запись получателя, которая содержит данные, находящиеся в поставщике адресной книги узла.</span><span class="sxs-lookup"><span data-stu-id="53ac3-105">Opens a recipient entry that has data residing in a host address book provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="53ac3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="53ac3-106">Parameters</span></span>

 <span data-ttu-id="53ac3-107">_кбтемплатеид_</span><span class="sxs-lookup"><span data-stu-id="53ac3-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="53ac3-108">возврата Число байтов в идентификаторе шаблона, на которое указывает параметр _лптемплатеид_ .</span><span class="sxs-lookup"><span data-stu-id="53ac3-108">[in] The byte count in the template identifier pointed to by the  _lpTemplateID_ parameter.</span></span> 
    
 <span data-ttu-id="53ac3-109">_лптемплатеид_</span><span class="sxs-lookup"><span data-stu-id="53ac3-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="53ac3-110">возврата Указатель на идентификатор шаблона или свойство **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) для записи получателя, которую нужно открыть.</span><span class="sxs-lookup"><span data-stu-id="53ac3-110">[in] A pointer to the template identifier, or **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="53ac3-111">_ултемплатефлагс_</span><span class="sxs-lookup"><span data-stu-id="53ac3-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="53ac3-112">возврата Битовая маска флагов, используемая для указания способа открытия записи, представленной идентификатором шаблона.</span><span class="sxs-lookup"><span data-stu-id="53ac3-112">[in] A bitmask of flags used to indicate how to open the entry represented by the template identifier.</span></span> <span data-ttu-id="53ac3-113">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="53ac3-113">The following flag can be set:</span></span>
    
<span data-ttu-id="53ac3-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="53ac3-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="53ac3-115">Поставщик узла создает новую запись в своем контейнере на основе записи, представленной идентификатором шаблона.</span><span class="sxs-lookup"><span data-stu-id="53ac3-115">The host provider is creating a new entry in its container based on the entry represented by the template identifier.</span></span> <span data-ttu-id="53ac3-116">Метод **иаблогон:: опентемплатеид** должен выполнять определенную инициализацию записи поставщика узла с помощью реализации интерфейса [IMAPIProp: IUnknown](imapipropiunknown.md) в параметре _лпмапипропдата_ или возвращать реализацию пользовательского интерфейса **IMAPIProp** в параметре _лппмапипропнев_ .</span><span class="sxs-lookup"><span data-stu-id="53ac3-116">The **IABLogon::OpenTemplateID** method should either perform specific initialization of the host provider's entry by using the [IMAPIProp : IUnknown](imapipropiunknown.md) implementation in the  _lpMAPIPropData_ parameter, or return a custom **IMAPIProp** interface implementation in the  _lppMAPIPropNew_ parameter.</span></span> 
    
 <span data-ttu-id="53ac3-117">_лпмапипропдата_</span><span class="sxs-lookup"><span data-stu-id="53ac3-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="53ac3-118">возврата Указатель на объект Property поставщика ведущего приложения и реализацию интерфейса, производного от **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="53ac3-118">[in] A pointer to the host provider's property object and implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="53ac3-119">_лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="53ac3-119">_lpInterface_</span></span>
  
> <span data-ttu-id="53ac3-120">возврата Указатель на идентификатор интерфейса (IID), представляющий тип указателя интерфейса, возвращаемого в параметре _лппмапипропнев_ .</span><span class="sxs-lookup"><span data-stu-id="53ac3-120">[in] A pointer to the interface identifier (IID) that represents the type of interface pointer to be returned in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="53ac3-121">При передаче **значения NULL** возвращается стандартный пользовательский интерфейс обмена сообщениями, [имаилусер: IMAPIProp](imailuserimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="53ac3-121">Passing **null** returns the standard messaging user interface, [IMailUser : IMAPIProp](imailuserimapiprop.md).</span></span>
    
 <span data-ttu-id="53ac3-122">_лппмапипропнев_</span><span class="sxs-lookup"><span data-stu-id="53ac3-122">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="53ac3-123">вышли Указатель на связанный объект Property и реализацию интерфейса, производного от **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="53ac3-123">[out] A pointer to the bound property object and an implementation of an interface derived from **IMAPIProp**.</span></span>
    
 <span data-ttu-id="53ac3-124">_лпмапипропсиблинг_</span><span class="sxs-lookup"><span data-stu-id="53ac3-124">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="53ac3-125">вышли Резервирования должно иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="53ac3-125">[out] Reserved; must be **null**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="53ac3-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53ac3-126">Return value</span></span>

<span data-ttu-id="53ac3-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="53ac3-127">S_OK</span></span> 
  
> <span data-ttu-id="53ac3-128">Соответствующий код был успешно привязан к связанным данным в поставщике узла.</span><span class="sxs-lookup"><span data-stu-id="53ac3-128">The appropriate code was successfully bound to related data in the host provider.</span></span>
    
<span data-ttu-id="53ac3-129">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="53ac3-129">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="53ac3-130">Объект не поддерживает идентификаторы шаблонов.</span><span class="sxs-lookup"><span data-stu-id="53ac3-130">The object does not support template IDs.</span></span>
    
<span data-ttu-id="53ac3-131">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="53ac3-131">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="53ac3-132">Поставщику адресной книги не удается распознать идентификатор шаблона, переданный в параметре _лптемплатеид_ .</span><span class="sxs-lookup"><span data-stu-id="53ac3-132">The template identifier passed in the  _lpTemplateID_ parameter is not recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="53ac3-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="53ac3-133">Remarks</span></span>

<span data-ttu-id="53ac3-134">Метод **иаблогон:: опентемплатеид** реализован только поставщиками адресных книг, которые должны поддерживать Управление копиями записей, которые находятся в контейнерах поставщиков узла.</span><span class="sxs-lookup"><span data-stu-id="53ac3-134">The **IABLogon::OpenTemplateID** method is implemented only by address book providers that need to maintain control over copies of their entries that are located in the containers of host providers.</span></span> <span data-ttu-id="53ac3-135">Поставщики, которые реализуют **опентемплатеид** , называются внешними поставщиками адресных книг.</span><span class="sxs-lookup"><span data-stu-id="53ac3-135">Providers that implement **OpenTemplateID** are known as foreign address book providers.</span></span> <span data-ttu-id="53ac3-136">Поставщики узла вызывают [имаписуппорт:: опентемплатеид](imapisupport-opentemplateid.md) для создания скопированной записи или открытия скопированной записи, а MAPI передается на вызов **Иаблогон:: опентемплатеид**.</span><span class="sxs-lookup"><span data-stu-id="53ac3-136">Host providers call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to create a copied entry or open the copied entry, and MAPI passes on the call to **IABLogon::OpenTemplateID**.</span></span> <span data-ttu-id="53ac3-137">**Иаблогон:: опентемплатеид** открывает запись и применяет к ней код, который управляет им данных в поставщике узла.</span><span class="sxs-lookup"><span data-stu-id="53ac3-137">**IABLogon::OpenTemplateID** opens the entry and binds the code that controls it to data in the host provider.</span></span> 
  
<span data-ttu-id="53ac3-138">Вместо использования идентификатора записи **иаблогон:: опентемплатеид** использует другое свойство, идентификатор шаблона записи **PR_TEMPLATEID**.</span><span class="sxs-lookup"><span data-stu-id="53ac3-138">Rather than use an entry identifier, **IABLogon::OpenTemplateID** uses another property, the entry's template identifier, **PR_TEMPLATEID**.</span></span> <span data-ttu-id="53ac3-139">Идентификаторы шаблонов должны поддерживаться записями, код которых должен быть связан с данными в поставщике узла.</span><span class="sxs-lookup"><span data-stu-id="53ac3-139">Template identifiers should be supported for entries whose code must be bound to data in a host provider.</span></span>
  
<span data-ttu-id="53ac3-140">Некоторые примеры, когда поставщик адресных книг должен реализовать **иаблогон:: опентемплатеид** , следующие:</span><span class="sxs-lookup"><span data-stu-id="53ac3-140">Some examples of when an address book provider should implement **IABLogon::OpenTemplateID** are as follows:</span></span> 
  
- <span data-ttu-id="53ac3-141">Для периодического обновления данных скопированной записи, чтобы она оставалась синхронизированной с оригиналом.</span><span class="sxs-lookup"><span data-stu-id="53ac3-141">To periodically update the data for a copied entry so that it stays synchronized with the original.</span></span>
    
- <span data-ttu-id="53ac3-142">Реализация функциональных возможностей, которые поставщик узла не может реализовать, например динамического заполнения списка, который отображается в таблице сведений записи, из данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="53ac3-142">To implement functionality that the host provider cannot implement, such as dynamically populating a list that appears in the entry's details table from data on a server.</span></span>
    
- <span data-ttu-id="53ac3-143">Для управления взаимодействием между свойствами в записи поставщика узла и исходной записью, например вычисления **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), из значений элементов управления редактирования в отображаемом сведения, которые содержат различные компоненты адреса.</span><span class="sxs-lookup"><span data-stu-id="53ac3-143">To control the interaction between properties in the host provider's entry and the original entry, such as computing the **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) from the values of the edit controls in the details display that contain different components of the address.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="53ac3-144">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="53ac3-144">Notes to implementers</span></span>

<span data-ttu-id="53ac3-145">Когда поставщик узла копирует или создает запись из поставщика, и вы предоставляете реализацию объекта Property с помощью **иаблогон:: опентемплатеид**, вы обрабатываете большинство вызовов для поддержки записи.</span><span class="sxs-lookup"><span data-stu-id="53ac3-145">When a host provider copies or creates an entry from your provider and you supply a property object implementation through **IABLogon::OpenTemplateID**, you handle most of the calls to maintain the entry.</span></span> <span data-ttu-id="53ac3-146">Тем не менее, так как поставщик узла отправляет эти вызовы, поставщик узла может перехватить любой вызов и выполнить настраиваемую обработку перед пересылкой вызова.</span><span class="sxs-lookup"><span data-stu-id="53ac3-146">However, because it is up to the host provider to forward these calls to you, the host provider can intercept any call and perform custom processing before forwarding the call.</span></span>
  
<span data-ttu-id="53ac3-147">В реализациях объектов свойств необходимо придерживаться следующих рекомендаций:</span><span class="sxs-lookup"><span data-stu-id="53ac3-147">You should use the following guidelines in your property object implementations:</span></span>
  
- <span data-ttu-id="53ac3-148">Когда вызывается [IMAPIProp::-PROPS](imapiprop-getprops.md) , определите, предназначен ли запрос для вычисляемого свойства, и обработайте его.</span><span class="sxs-lookup"><span data-stu-id="53ac3-148">When [IMAPIProp::GetProps](imapiprop-getprops.md) is called, determine whether the request is for a computed property and, if it is, handle it.</span></span> <span data-ttu-id="53ac3-149">Передача всех запросов для невычисляемых свойств поставщику узла.</span><span class="sxs-lookup"><span data-stu-id="53ac3-149">Transfer all requests for noncomputed properties to the host provider.</span></span> 
    
- <span data-ttu-id="53ac3-150">Когда [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) вызывается для открытия любой таблицы, кроме таблицы отображения сведений, обработайте запрос.</span><span class="sxs-lookup"><span data-stu-id="53ac3-150">When [IMAPIProp::OpenProperty](imapiprop-openproperty.md) is called to open any table except the details display table, handle the request.</span></span> <span data-ttu-id="53ac3-151">Большинство таблиц не удается точно скопировать в поставщик узла.</span><span class="sxs-lookup"><span data-stu-id="53ac3-151">Most tables cannot be copied accurately to the host provider.</span></span> <span data-ttu-id="53ac3-152">Необходимо создать реализацию **IMAPITable** для этих запрошенных таблиц.</span><span class="sxs-lookup"><span data-stu-id="53ac3-152">You must generate the **IMAPITable** implementation for these requested tables.</span></span> <span data-ttu-id="53ac3-153">Свойство таблицы сведений **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) должно быть скопировано в поставщик узла.</span><span class="sxs-lookup"><span data-stu-id="53ac3-153">The details table **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property must be copied to the host provider.</span></span> <span data-ttu-id="53ac3-154">Это позволяет этому поставщику создать таблицу локально.</span><span class="sxs-lookup"><span data-stu-id="53ac3-154">This allows this provider to generate the table locally.</span></span> <span data-ttu-id="53ac3-155">Вы можете заключить реализацию таблицы отображения для создания уведомлений для отображения таблицы.</span><span class="sxs-lookup"><span data-stu-id="53ac3-155">You might want to wrap the display table implementation to generate display table notifications.</span></span> 
    
- <span data-ttu-id="53ac3-156">Когда [IMAPIProp:: SetProps](imapiprop-setprops.md) вызывается, поставщик узла может проверить данные, прежде чем позволить задать свойства.</span><span class="sxs-lookup"><span data-stu-id="53ac3-156">When [IMAPIProp::SetProps](imapiprop-setprops.md) is called, the host provider can validate the data before letting you set the properties.</span></span> <span data-ttu-id="53ac3-157">Вы можете убедиться, что все необходимые свойства заданы или вычислены.</span><span class="sxs-lookup"><span data-stu-id="53ac3-157">You can verify that all of the necessary properties were set or computed.</span></span> <span data-ttu-id="53ac3-158">Если обнаружена ошибка, возвращайте соответствующее значение ошибки и, если возможно, любое дополнительное объяснение через [IMAPIProp:: GetLastError](imapiprop-getlasterror.md).</span><span class="sxs-lookup"><span data-stu-id="53ac3-158">If an error is detected, return the appropriate error value and, if you can, any additional explanation through [IMAPIProp::GetLastError](imapiprop-getlasterror.md).</span></span>
    
- <span data-ttu-id="53ac3-159">Когда [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) вызывается, поставщику узла может потребоваться выполнить обработку перед сохранением записи.</span><span class="sxs-lookup"><span data-stu-id="53ac3-159">When [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called, the host provider might want to perform processing before you save the entry.</span></span> <span data-ttu-id="53ac3-160">Необходимо сохранить все данные, на которые влияет измененные свойства, например новый адрес, в записи поставщика узла.</span><span class="sxs-lookup"><span data-stu-id="53ac3-160">You should save any data that is affected by the changed properties, such as a new address, in the host provider's entry.</span></span> 
    
<span data-ttu-id="53ac3-161">В общем случае сделайте реализацию записи, которая передается обратно поставщику узла, перехватить все методы для выполнения контекстной обработки соответствующих свойств.</span><span class="sxs-lookup"><span data-stu-id="53ac3-161">In general, make your implementation of the entry that you pass back to the host provider intercept all of the methods to perform context-specific manipulation of the relevant properties.</span></span> <span data-ttu-id="53ac3-162">Если флаг FILL_ENTRY передается в параметре _ултемплатефлагс_ , установите все свойства записи.</span><span class="sxs-lookup"><span data-stu-id="53ac3-162">If the FILL_ENTRY flag is passed in the  _ulTemplateFlags_ parameter, set all properties for the entry.</span></span> 
  
<span data-ttu-id="53ac3-163">Если вы возвращаете новый объект Property в параметре _лппмапипропнев_ , вызовите метод [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) объекта Property поставщика узла для поддержки ссылки.</span><span class="sxs-lookup"><span data-stu-id="53ac3-163">If you return a new property object in the  _lppMAPIPropNew_ parameter, call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method of the host provider's property object to maintain a reference.</span></span> <span data-ttu-id="53ac3-164">Все вызовы через привязанный объект, возвращаемый в _лппмапипропнев_ реализацией **IMAPIProp** , должны перенаправляться в соответствующий метод объекта Property узла после того, как они обрабатываются связанным объектом.</span><span class="sxs-lookup"><span data-stu-id="53ac3-164">All calls through the bound object that the **IMAPIProp** implementation returned in  _lppMAPIPropNew_ should be routed to their corresponding method in the host property object after they are dealt with by the bound object.</span></span> 
  
<span data-ttu-id="53ac3-165">Идентификаторы свойств любых именованных свойств, которые передаются через объект связанного свойства, находятся в пространстве имен идентификатора поставщика.</span><span class="sxs-lookup"><span data-stu-id="53ac3-165">The property identifiers of any named properties that are passed through your bound property object are in your provider's identifier namespace.</span></span> <span data-ttu-id="53ac3-166">Реализация метода [IMAPIProp:: жетнамесфромидс](imapiprop-getnamesfromids.md) должна определять имена свойств, чтобы она могла выполнять любые задачи, связанные с шаблоном.</span><span class="sxs-lookup"><span data-stu-id="53ac3-166">Your implementation of the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) method should determine the names of the properties so that it can perform any template-specific tasks.</span></span> <span data-ttu-id="53ac3-167">Аналогично свойства, которые поставщик передает поставщику узла, также должны находиться в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="53ac3-167">Similarly, properties that your provider passes on to the host provider must also be in your namespace.</span></span> <span data-ttu-id="53ac3-168">Например, если вы задаете именованное свойство в **опентемплатеид**, то при необходимости необходимо использовать один из идентификаторов для имени (при необходимости), вызвав метод [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="53ac3-168">For example, if you set a named property in **OpenTemplateID**, you should use one of your identifiers for the name—creating it, if necessary, by calling the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="53ac3-169">Если вы не узнаете идентификатор записи, переданный в _лптемплатеид_, возвращается MAPI_E_UNKNOWN_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="53ac3-169">If you do not recognize the entry identifier passed in  _lpTemplateID_, return MAPI_E_UNKNOWN_ENTRYID.</span></span>
  
<span data-ttu-id="53ac3-170">Для получения дополнительных сведений о том, как работать с идентификаторами шаблонов адресных книг, обратитесь к разделу "работа в [качестве поставщика внешних адресных книг](acting-as-a-foreign-address-book-provider.md)".</span><span class="sxs-lookup"><span data-stu-id="53ac3-170">For more information about how to work with address book template identifiers, see [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="53ac3-171">См. также</span><span class="sxs-lookup"><span data-stu-id="53ac3-171">See also</span></span>



[<span data-ttu-id="53ac3-172">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="53ac3-172">IMAPISupport::OpenTemplateID</span></span>](imapisupport-opentemplateid.md)
  
[<span data-ttu-id="53ac3-173">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="53ac3-173">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="53ac3-174">Каноническое свойство PidTagTemplateid</span><span class="sxs-lookup"><span data-stu-id="53ac3-174">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="53ac3-175">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="53ac3-175">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

