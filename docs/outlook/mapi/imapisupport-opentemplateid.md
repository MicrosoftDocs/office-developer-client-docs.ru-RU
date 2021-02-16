---
title: IMAPISupportOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenTemplateID
api_type:
- COM
ms.assetid: 532f7af0-b2cc-49dd-b1de-e3ec1dc9a3e7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 07aa508b473f4a87d5b4909f83771549c301a600
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418507"
---
# <a name="imapisupportopentemplateid"></a><span data-ttu-id="1109d-103">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="1109d-103">IMAPISupport::OpenTemplateID</span></span>

  
  
<span data-ttu-id="1109d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1109d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1109d-105">Открывает запись получателя во внешнем поставщике адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1109d-105">Opens a recipient entry in a foreign address book provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="1109d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1109d-106">Parameters</span></span>

 <span data-ttu-id="1109d-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="1109d-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="1109d-108">[in] Количество byte в идентификаторе шаблона, на который указывает _lpTemplateID._</span><span class="sxs-lookup"><span data-stu-id="1109d-108">[in] The byte count in the template identifier pointed to by  _lpTemplateID_.</span></span> 
    
 <span data-ttu-id="1109d-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="1109d-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="1109d-110">[in] Указатель на идентификатор шаблона PR_TEMPLATEID **(** [PidTagTemplateid)](pidtagtemplateid-canonical-property.md)открываемой записи получателя.</span><span class="sxs-lookup"><span data-stu-id="1109d-110">[in] A pointer to the template identifier **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="1109d-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="1109d-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="1109d-112">[in] Битоваяmas флагов, используемая для описания открытия записи.</span><span class="sxs-lookup"><span data-stu-id="1109d-112">[in] A bitmask of flags used to describe how to open the entry.</span></span> <span data-ttu-id="1109d-113">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="1109d-113">The following flag can be set:</span></span>
    
<span data-ttu-id="1109d-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="1109d-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="1109d-115">Создается новая запись.</span><span class="sxs-lookup"><span data-stu-id="1109d-115">A new entry is being created.</span></span> <span data-ttu-id="1109d-116">Когда внешнее поставщик получает последующий вызов [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) из MAPI, он может управлять тем, как создается запись, изменяя свойства, на которые указывает параметр  _lpMAPIPropData,_ или возвращая определенную реализацию интерфейса  _в lppMAPIPropNew,_ чтобы управлять тем, как заданы свойства новой записи.</span><span class="sxs-lookup"><span data-stu-id="1109d-116">When the foreign provider receives the subsequent [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) call from MAPI, it can control how the entry is created by modifying properties pointed to by the  _lpMAPIPropData_ parameter or by returning a specific interface implementation in  _lppMAPIPropNew_ to control how properties for the new entry are set.</span></span> 
    
 <span data-ttu-id="1109d-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="1109d-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="1109d-118">[in] Указатель на реализацию интерфейса, которую звоняя использует для доступа к записи.</span><span class="sxs-lookup"><span data-stu-id="1109d-118">[in] A pointer to the interface implementation that the caller uses to access the entry.</span></span> <span data-ttu-id="1109d-119">Это реализация, которую внешнее поставщик может обтекать собственной реализацией и вернуть в параметр _lppMAPIPropNew._</span><span class="sxs-lookup"><span data-stu-id="1109d-119">This is the implementation that the foreign provider can wrap with its own implementation and return in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="1109d-120">Параметр _lpMAPIPropData_ должен указать на реализацию интерфейса чтения и записи, которая является потомком [IMAPIProp : IUnknown](imapipropiunknown.md) и поддерживает интерфейс, запрашивается в _параметре lpInterface._</span><span class="sxs-lookup"><span data-stu-id="1109d-120">The  _lpMAPIPropData_ parameter must point to a read/write interface implementation that derives from [IMAPIProp : IUnknown](imapipropiunknown.md) and supports the interface being requested in the  _lpInterface_ parameter.</span></span> 
    
 <span data-ttu-id="1109d-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="1109d-121">_lpInterface_</span></span>
  
> <span data-ttu-id="1109d-122">[in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, который будет использоваться для доступа к записи.</span><span class="sxs-lookup"><span data-stu-id="1109d-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the entry.</span></span> <span data-ttu-id="1109d-123">Параметр _lppMAPIPropNew_ указывает на интерфейс типа, заданного _lpInterface._</span><span class="sxs-lookup"><span data-stu-id="1109d-123">The  _lppMAPIPropNew_ parameter points to an interface of the type specified by  _lpInterface_.</span></span> <span data-ttu-id="1109d-124">Передача NULL возвращает стандартный интерфейс для пользователя обмена сообщениями, IID_IMailUser.</span><span class="sxs-lookup"><span data-stu-id="1109d-124">Passing NULL returns the standard interface for a messaging user, IID_IMailUser.</span></span> 
    
 <span data-ttu-id="1109d-125">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="1109d-125">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="1109d-126">[out] Указатель на реализацию интерфейса, которую поставщик внешних поставщиков обеспечивает доступ к записи.</span><span class="sxs-lookup"><span data-stu-id="1109d-126">[out] A pointer to the interface implementation that the foreign provider supplies for accessing the entry.</span></span>
    
 <span data-ttu-id="1109d-127">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="1109d-127">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="1109d-128">Зарезервировано; должно быть NULL.</span><span class="sxs-lookup"><span data-stu-id="1109d-128">Reserved; must be NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1109d-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1109d-129">Return value</span></span>

<span data-ttu-id="1109d-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="1109d-130">S_OK</span></span> 
  
> <span data-ttu-id="1109d-131">Процесс привязки был успешным.</span><span class="sxs-lookup"><span data-stu-id="1109d-131">The binding process was successful.</span></span>
    
<span data-ttu-id="1109d-132">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1109d-132">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="1109d-133">Поставщик внешней адресной книги не существует.</span><span class="sxs-lookup"><span data-stu-id="1109d-133">The foreign address book provider doesn't exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1109d-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="1109d-134">Remarks</span></span>

<span data-ttu-id="1109d-135">Метод **IMAPISupport::OpenTemplateID** реализован только для объектов поддержки поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1109d-135">The **IMAPISupport::OpenTemplateID** method is implemented only for address book provider support objects.</span></span> <span data-ttu-id="1109d-136">**OpenTemplateID** вызвано только поставщиками адресных книг, которые могут выступать в качестве хостов для записей, принадлежащих другим поставщикам адресных книг, также называемым внешних поставщиков.</span><span class="sxs-lookup"><span data-stu-id="1109d-136">**OpenTemplateID** is called only by address book providers that can act as hosts for entries that belong to other address book providers, also known as foreign providers.</span></span> <span data-ttu-id="1109d-137">Поставщики услуг хоста **звонят openTemplateID** для открытия внешней записи, которая возникает, когда данные в поставщике хоста привязаны к коду во внешнем поставщике.</span><span class="sxs-lookup"><span data-stu-id="1109d-137">Host providers call **OpenTemplateID** to open a foreign entry, which occurs when data in the host provider is bound to code in the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1109d-138">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="1109d-138">Notes to callers</span></span>

<span data-ttu-id="1109d-139">Вызовите **OpenTemplateID** только в том случае, если поддерживается хранение записей с идентификаторами шаблонов от поставщиков внешних адресных книг.</span><span class="sxs-lookup"><span data-stu-id="1109d-139">Call **OpenTemplateID** only if you support the storage of entries with template identifiers from foreign address book providers.</span></span> <span data-ttu-id="1109d-140">Такая поддержка предъявляет дополнительные требования к реализациям [IABContainer::CreateEntry](iabcontainer-createentry.md) и [IABLogon::OpenEntry.](iablogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="1109d-140">Such support places additional requirements on your [IABContainer::CreateEntry](iabcontainer-createentry.md) and [IABLogon::OpenEntry](iablogon-openentry.md) implementations.</span></span> <span data-ttu-id="1109d-141">Дополнительные сведения см. в описании этих методов и действия [в качестве поставщика адресной книги для хост-адресов.](acting-as-a-host-address-book-provider.md)</span><span class="sxs-lookup"><span data-stu-id="1109d-141">For more information, see the descriptions of these methods and [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
<span data-ttu-id="1109d-142">Если вызов **OpenTemplateID** возвращает в качестве привязанного интерфейса ту же реализацию объекта свойства, которую вы передали, вы можете освободить ссылку на объект свойства.</span><span class="sxs-lookup"><span data-stu-id="1109d-142">If the **OpenTemplateID** call returns as the bound interface the same property object implementation that you passed in, you can release your reference to your property object.</span></span> <span data-ttu-id="1109d-143">Это вызвано тем, что внешние поставщики вызвали метод **AddRef** объекта, чтобы сохранить собственную ссылку.</span><span class="sxs-lookup"><span data-stu-id="1109d-143">This is because the foreign provider has called the object's **AddRef** method to keep its own reference.</span></span> <span data-ttu-id="1109d-144">Если внешнему поставщику не нужно сохранять ссылку на объект свойства, **OpenTemplateID** возвращает объект свойства unbound.</span><span class="sxs-lookup"><span data-stu-id="1109d-144">If the foreign provider does not need to keep a reference to the property object, then **OpenTemplateID** will return the unbound property object.</span></span> 
  
<span data-ttu-id="1109d-145">Если **сбой OpenTemplateID** MAPI_E_UNKNOWN_ENTRYID, попробуйте продолжить, обрабатывая запись как доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1109d-145">If **OpenTemplateID** fails with MAPI_E_UNKNOWN_ENTRYID, try to continue by treating the entry as read-only.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1109d-146">См. также</span><span class="sxs-lookup"><span data-stu-id="1109d-146">See also</span></span>



[<span data-ttu-id="1109d-147">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="1109d-147">IABLogon::OpenTemplateID</span></span>](iablogon-opentemplateid.md)
  
[<span data-ttu-id="1109d-148">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1109d-148">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="1109d-149">Каноническое свойство PidTagTemplateid</span><span class="sxs-lookup"><span data-stu-id="1109d-149">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="1109d-150">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1109d-150">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

