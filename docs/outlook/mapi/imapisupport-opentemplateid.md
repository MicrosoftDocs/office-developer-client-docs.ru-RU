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
ms.openlocfilehash: 855810f7ac3bc1bd433ddd56aba3fe1f938b9559
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575387"
---
# <a name="imapisupportopentemplateid"></a><span data-ttu-id="b301b-103">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="b301b-103">IMAPISupport::OpenTemplateID</span></span>

  
  
<span data-ttu-id="b301b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b301b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b301b-105">Открывает запись получателя в поставщик внешнего адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b301b-105">Opens a recipient entry in a foreign address book provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="b301b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b301b-106">Parameters</span></span>

 <span data-ttu-id="b301b-107">_cbTemplateID_</span><span class="sxs-lookup"><span data-stu-id="b301b-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="b301b-108">[in] Число байтов в идентификатор шаблона, на который указывает _lpTemplateID_.</span><span class="sxs-lookup"><span data-stu-id="b301b-108">[in] The byte count in the template identifier pointed to by  _lpTemplateID_.</span></span> 
    
 <span data-ttu-id="b301b-109">_lpTemplateID_</span><span class="sxs-lookup"><span data-stu-id="b301b-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="b301b-110">[in] Указатель на идентификатор шаблона свойство **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) получателей записи для открытия.</span><span class="sxs-lookup"><span data-stu-id="b301b-110">[in] A pointer to the template identifier **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="b301b-111">_ulTemplateFlags_</span><span class="sxs-lookup"><span data-stu-id="b301b-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="b301b-112">[in] Битовая маска флаги, описывается, как открыть запись.</span><span class="sxs-lookup"><span data-stu-id="b301b-112">[in] A bitmask of flags used to describe how to open the entry.</span></span> <span data-ttu-id="b301b-113">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="b301b-113">The following flag can be set:</span></span>
    
<span data-ttu-id="b301b-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="b301b-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="b301b-115">Создается новая запись.</span><span class="sxs-lookup"><span data-stu-id="b301b-115">A new entry is being created.</span></span> <span data-ttu-id="b301b-116">При последующих вызовов [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) получает внешнего поставщика из MAPI, его можно управлять как операция создается путем изменения свойств, на который указывает параметр _lpMAPIPropData_ или возвращением определенного интерфейса Реализация в _lppMAPIPropNew_ для управления, как задать свойства для нового элемента.</span><span class="sxs-lookup"><span data-stu-id="b301b-116">When the foreign provider receives the subsequent [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) call from MAPI, it can control how the entry is created by modifying properties pointed to by the  _lpMAPIPropData_ parameter or by returning a specific interface implementation in  _lppMAPIPropNew_ to control how properties for the new entry are set.</span></span> 
    
 <span data-ttu-id="b301b-117">_lpMAPIPropData_</span><span class="sxs-lookup"><span data-stu-id="b301b-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="b301b-118">[in] Указатель на реализации интерфейса, используемый вызывающим объектом для доступа к операции.</span><span class="sxs-lookup"><span data-stu-id="b301b-118">[in] A pointer to the interface implementation that the caller uses to access the entry.</span></span> <span data-ttu-id="b301b-119">Это реализация, которые могут переносить собственные реализации и возврата в параметре _lppMAPIPropNew_ внешнего поставщика.</span><span class="sxs-lookup"><span data-stu-id="b301b-119">This is the implementation that the foreign provider can wrap with its own implementation and return in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="b301b-120">Параметр _lpMAPIPropData_ должен указывать на реализацию интерфейса чтения и записи, которая является производным от [IMAPIProp: IUnknown](imapipropiunknown.md) и поддерживает интерфейс, запрашиваемый с помощью параметра _lpInterface_ .</span><span class="sxs-lookup"><span data-stu-id="b301b-120">The  _lpMAPIPropData_ parameter must point to a read/write interface implementation that derives from [IMAPIProp : IUnknown](imapipropiunknown.md) and supports the interface being requested in the  _lpInterface_ parameter.</span></span> 
    
 <span data-ttu-id="b301b-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="b301b-121">_lpInterface_</span></span>
  
> <span data-ttu-id="b301b-122">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к операции.</span><span class="sxs-lookup"><span data-stu-id="b301b-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the entry.</span></span> <span data-ttu-id="b301b-123">Параметр _lppMAPIPropNew_ указывает на интерфейс типа, указанного параметром _lpInterface_.</span><span class="sxs-lookup"><span data-stu-id="b301b-123">The  _lppMAPIPropNew_ parameter points to an interface of the type specified by  _lpInterface_.</span></span> <span data-ttu-id="b301b-124">Передача NULL Возвращает стандартный интерфейс для обмена сообщениями пользователя IID_IMailUser.</span><span class="sxs-lookup"><span data-stu-id="b301b-124">Passing NULL returns the standard interface for a messaging user, IID_IMailUser.</span></span> 
    
 <span data-ttu-id="b301b-125">_lppMAPIPropNew_</span><span class="sxs-lookup"><span data-stu-id="b301b-125">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="b301b-126">[out] Указатель на реализации интерфейса, который предоставляет внешнего поставщика для доступа к операции.</span><span class="sxs-lookup"><span data-stu-id="b301b-126">[out] A pointer to the interface implementation that the foreign provider supplies for accessing the entry.</span></span>
    
 <span data-ttu-id="b301b-127">_lpMAPIPropSibling_</span><span class="sxs-lookup"><span data-stu-id="b301b-127">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="b301b-128">Зарезервировано; должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="b301b-128">Reserved; must be NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b301b-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b301b-129">Return value</span></span>

<span data-ttu-id="b301b-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="b301b-130">S_OK</span></span> 
  
> <span data-ttu-id="b301b-131">Процесс привязки прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="b301b-131">The binding process was successful.</span></span>
    
<span data-ttu-id="b301b-132">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b301b-132">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="b301b-133">Поставщик внешних адресной книги не существует.</span><span class="sxs-lookup"><span data-stu-id="b301b-133">The foreign address book provider doesn't exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b301b-134">Замечания</span><span class="sxs-lookup"><span data-stu-id="b301b-134">Remarks</span></span>

<span data-ttu-id="b301b-135">Метод **IMAPISupport::OpenTemplateID** применяется только для объектов поддержки поставщик адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b301b-135">The **IMAPISupport::OpenTemplateID** method is implemented only for address book provider support objects.</span></span> <span data-ttu-id="b301b-136">**OpenTemplateID** вызывается только с поставщиками адресных книг, которые могут выступать в качестве узлов для записи, которые принадлежат другим поставщиками адресной книги также известной как внешнего поставщиков.</span><span class="sxs-lookup"><span data-stu-id="b301b-136">**OpenTemplateID** is called only by address book providers that can act as hosts for entries that belong to other address book providers, also known as foreign providers.</span></span> <span data-ttu-id="b301b-137">Поставщики узла вызова **OpenTemplateID** Открытие внешнего запись, которая возникает, когда с привязкой к данным в поставщике узла к коду в внешнего поставщика.</span><span class="sxs-lookup"><span data-stu-id="b301b-137">Host providers call **OpenTemplateID** to open a foreign entry, which occurs when data in the host provider is bound to code in the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b301b-138">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="b301b-138">Notes to callers</span></span>

<span data-ttu-id="b301b-139">Вызов **OpenTemplateID** только в том случае, если вы поддерживаете хранилища записей с идентификаторами шаблон с поставщиками внешнего адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b301b-139">Call **OpenTemplateID** only if you support the storage of entries with template identifiers from foreign address book providers.</span></span> <span data-ttu-id="b301b-140">Такая поддержка помещает Дополнительные требования к реализации [IABContainer::CreateEntry](iabcontainer-createentry.md) и [IABLogon::OpenEntry](iablogon-openentry.md) .</span><span class="sxs-lookup"><span data-stu-id="b301b-140">Such support places additional requirements on your [IABContainer::CreateEntry](iabcontainer-createentry.md) and [IABLogon::OpenEntry](iablogon-openentry.md) implementations.</span></span> <span data-ttu-id="b301b-141">Для получения дополнительных сведений см эти методы и [используется в качестве узла адресной книге](acting-as-a-host-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b301b-141">For more information, see the descriptions of these methods and [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
<span data-ttu-id="b301b-142">Если звонок **OpenTemplateID** возвращает как привязанной интерфейс же реализация объекта свойство, которое передается в, могут освобождать ссылку на объект свойство.</span><span class="sxs-lookup"><span data-stu-id="b301b-142">If the **OpenTemplateID** call returns as the bound interface the same property object implementation that you passed in, you can release your reference to your property object.</span></span> <span data-ttu-id="b301b-143">Это называется метод **AddRef** объекта для хранения собственный ссылку внешнего поставщика.</span><span class="sxs-lookup"><span data-stu-id="b301b-143">This is because the foreign provider has called the object's **AddRef** method to keep its own reference.</span></span> <span data-ttu-id="b301b-144">Если внешний поставщик не требуется хранить ссылку на объект свойство, **OpenTemplateID** возвращает объект свободной свойств.</span><span class="sxs-lookup"><span data-stu-id="b301b-144">If the foreign provider does not need to keep a reference to the property object, then **OpenTemplateID** will return the unbound property object.</span></span> 
  
<span data-ttu-id="b301b-145">В случае сбоя **OpenTemplateID** с MAPI_E_UNKNOWN_ENTRYID продолжать путем обработки записи с доступом только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b301b-145">If **OpenTemplateID** fails with MAPI_E_UNKNOWN_ENTRYID, try to continue by treating the entry as read-only.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b301b-146">См. также</span><span class="sxs-lookup"><span data-stu-id="b301b-146">See also</span></span>



[<span data-ttu-id="b301b-147">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="b301b-147">IABLogon::OpenTemplateID</span></span>](iablogon-opentemplateid.md)
  
[<span data-ttu-id="b301b-148">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b301b-148">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="b301b-149">Каноническое свойство PidTagTemplateid</span><span class="sxs-lookup"><span data-stu-id="b301b-149">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="b301b-150">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b301b-150">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

