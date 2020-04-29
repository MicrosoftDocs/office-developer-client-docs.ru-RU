---
title: имаписуппортопентемплатеид
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
# <a name="imapisupportopentemplateid"></a><span data-ttu-id="82fb7-103">IMAPISupport::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="82fb7-103">IMAPISupport::OpenTemplateID</span></span>

  
  
<span data-ttu-id="82fb7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82fb7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82fb7-105">Открывает запись получателя в поставщике внешней адресной книги.</span><span class="sxs-lookup"><span data-stu-id="82fb7-105">Opens a recipient entry in a foreign address book provider.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="82fb7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="82fb7-106">Parameters</span></span>

 <span data-ttu-id="82fb7-107">_кбтемплатеид_</span><span class="sxs-lookup"><span data-stu-id="82fb7-107">_cbTemplateID_</span></span>
  
> <span data-ttu-id="82fb7-108">возврата Количество байтов в идентификаторе шаблона, на который указывает _лптемплатеид_.</span><span class="sxs-lookup"><span data-stu-id="82fb7-108">[in] The byte count in the template identifier pointed to by  _lpTemplateID_.</span></span> 
    
 <span data-ttu-id="82fb7-109">_лптемплатеид_</span><span class="sxs-lookup"><span data-stu-id="82fb7-109">_lpTemplateID_</span></span>
  
> <span data-ttu-id="82fb7-110">возврата Указатель на свойство идентификатора шаблона **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) записи получателя, которое нужно открыть.</span><span class="sxs-lookup"><span data-stu-id="82fb7-110">[in] A pointer to the template identifier **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property of the recipient entry to be opened.</span></span>
    
 <span data-ttu-id="82fb7-111">_ултемплатефлагс_</span><span class="sxs-lookup"><span data-stu-id="82fb7-111">_ulTemplateFlags_</span></span>
  
> <span data-ttu-id="82fb7-112">возврата Битовая маска флагов, используемых для описания способа открытия записи.</span><span class="sxs-lookup"><span data-stu-id="82fb7-112">[in] A bitmask of flags used to describe how to open the entry.</span></span> <span data-ttu-id="82fb7-113">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="82fb7-113">The following flag can be set:</span></span>
    
<span data-ttu-id="82fb7-114">FILL_ENTRY</span><span class="sxs-lookup"><span data-stu-id="82fb7-114">FILL_ENTRY</span></span> 
  
> <span data-ttu-id="82fb7-115">Создается новая запись.</span><span class="sxs-lookup"><span data-stu-id="82fb7-115">A new entry is being created.</span></span> <span data-ttu-id="82fb7-116">Когда внешний поставщик получает последующий вызов [иаблогон:: опентемплатеид](iablogon-opentemplateid.md) из MAPI, он может управлять способом создания записи, изменяя свойства, на которые указывает параметр _лпмапипропдата_ , или возвращая определенную реализацию интерфейса в _лппмапипропнев_ для управления заданными свойствами новой записи.</span><span class="sxs-lookup"><span data-stu-id="82fb7-116">When the foreign provider receives the subsequent [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) call from MAPI, it can control how the entry is created by modifying properties pointed to by the  _lpMAPIPropData_ parameter or by returning a specific interface implementation in  _lppMAPIPropNew_ to control how properties for the new entry are set.</span></span> 
    
 <span data-ttu-id="82fb7-117">_лпмапипропдата_</span><span class="sxs-lookup"><span data-stu-id="82fb7-117">_lpMAPIPropData_</span></span>
  
> <span data-ttu-id="82fb7-118">возврата Указатель на реализацию интерфейса, который абонент использует для доступа к записи.</span><span class="sxs-lookup"><span data-stu-id="82fb7-118">[in] A pointer to the interface implementation that the caller uses to access the entry.</span></span> <span data-ttu-id="82fb7-119">Это реализация, которую внешний поставщик может переносить в собственную реализацию и возвращать параметр _лппмапипропнев_ .</span><span class="sxs-lookup"><span data-stu-id="82fb7-119">This is the implementation that the foreign provider can wrap with its own implementation and return in the  _lppMAPIPropNew_ parameter.</span></span> <span data-ttu-id="82fb7-120">Параметр _лпмапипропдата_ должен указать на реализацию интерфейса чтения и записи, производную от [IMAPIProp: IUnknown](imapipropiunknown.md) и поддерживающая интерфейс, запрашиваемый в параметре _лпинтерфаце_ .</span><span class="sxs-lookup"><span data-stu-id="82fb7-120">The  _lpMAPIPropData_ parameter must point to a read/write interface implementation that derives from [IMAPIProp : IUnknown](imapipropiunknown.md) and supports the interface being requested in the  _lpInterface_ parameter.</span></span> 
    
 <span data-ttu-id="82fb7-121">_лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="82fb7-121">_lpInterface_</span></span>
  
> <span data-ttu-id="82fb7-122">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к записи.</span><span class="sxs-lookup"><span data-stu-id="82fb7-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the entry.</span></span> <span data-ttu-id="82fb7-123">Параметр _лппмапипропнев_ указывает на интерфейс типа, указанного с помощью _лпинтерфаце_.</span><span class="sxs-lookup"><span data-stu-id="82fb7-123">The  _lppMAPIPropNew_ parameter points to an interface of the type specified by  _lpInterface_.</span></span> <span data-ttu-id="82fb7-124">При передаче значения NULL возвращается стандартный интерфейс для пользователя обмена сообщениями, IID_IMailUser.</span><span class="sxs-lookup"><span data-stu-id="82fb7-124">Passing NULL returns the standard interface for a messaging user, IID_IMailUser.</span></span> 
    
 <span data-ttu-id="82fb7-125">_лппмапипропнев_</span><span class="sxs-lookup"><span data-stu-id="82fb7-125">_lppMAPIPropNew_</span></span>
  
> <span data-ttu-id="82fb7-126">вышли Указатель на реализацию интерфейса, предоставленный внешним поставщиком для доступа к записи.</span><span class="sxs-lookup"><span data-stu-id="82fb7-126">[out] A pointer to the interface implementation that the foreign provider supplies for accessing the entry.</span></span>
    
 <span data-ttu-id="82fb7-127">_лпмапипропсиблинг_</span><span class="sxs-lookup"><span data-stu-id="82fb7-127">_lpMAPIPropSibling_</span></span>
  
> <span data-ttu-id="82fb7-128">Резервирования должно иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="82fb7-128">Reserved; must be NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="82fb7-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82fb7-129">Return value</span></span>

<span data-ttu-id="82fb7-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="82fb7-130">S_OK</span></span> 
  
> <span data-ttu-id="82fb7-131">Процесс привязки выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="82fb7-131">The binding process was successful.</span></span>
    
<span data-ttu-id="82fb7-132">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="82fb7-132">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="82fb7-133">Поставщик внешней адресной книги не существует.</span><span class="sxs-lookup"><span data-stu-id="82fb7-133">The foreign address book provider doesn't exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="82fb7-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="82fb7-134">Remarks</span></span>

<span data-ttu-id="82fb7-135">Метод **имаписуппорт:: опентемплатеид** реализован только для объектов поддержки поставщика адресных книг.</span><span class="sxs-lookup"><span data-stu-id="82fb7-135">The **IMAPISupport::OpenTemplateID** method is implemented only for address book provider support objects.</span></span> <span data-ttu-id="82fb7-136">**Опентемплатеид** вызывается только поставщиками адресных книг, которые могут выполнять роль ведущих элементов для записей, принадлежащих другим поставщикам адресных книг, также называемым внешними поставщиками.</span><span class="sxs-lookup"><span data-stu-id="82fb7-136">**OpenTemplateID** is called only by address book providers that can act as hosts for entries that belong to other address book providers, also known as foreign providers.</span></span> <span data-ttu-id="82fb7-137">Поставщики узла вызывают **опентемплатеид** , чтобы открыть внешнюю запись, которая происходит, когда данные в поставщике узла привязаны к коду в внешнем поставщике.</span><span class="sxs-lookup"><span data-stu-id="82fb7-137">Host providers call **OpenTemplateID** to open a foreign entry, which occurs when data in the host provider is bound to code in the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="82fb7-138">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="82fb7-138">Notes to callers</span></span>

<span data-ttu-id="82fb7-139">Вызовите **опентемплатеид** только в том случае, если вы поддерживаете хранение записей с идентификаторами шаблонов от поставщиков внешних адресных книг.</span><span class="sxs-lookup"><span data-stu-id="82fb7-139">Call **OpenTemplateID** only if you support the storage of entries with template identifiers from foreign address book providers.</span></span> <span data-ttu-id="82fb7-140">Такая поддержка размещает дополнительные требования к реализациям [иабконтаинер:: креатинтри](iabcontainer-createentry.md) и [Иаблогон:: OpenEntry](iablogon-openentry.md) .</span><span class="sxs-lookup"><span data-stu-id="82fb7-140">Such support places additional requirements on your [IABContainer::CreateEntry](iabcontainer-createentry.md) and [IABLogon::OpenEntry](iablogon-openentry.md) implementations.</span></span> <span data-ttu-id="82fb7-141">Дополнительные сведения см. в описании этих способов и [действуют как поставщик адресной книги узла](acting-as-a-host-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="82fb7-141">For more information, see the descriptions of these methods and [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
<span data-ttu-id="82fb7-142">Если вызов **опентемплатеид** возвращает в качестве связанного интерфейса ту же реализацию объекта Property, что вы передали, вы можете освободить ссылку на объект Property.</span><span class="sxs-lookup"><span data-stu-id="82fb7-142">If the **OpenTemplateID** call returns as the bound interface the same property object implementation that you passed in, you can release your reference to your property object.</span></span> <span data-ttu-id="82fb7-143">Это связано с тем, что внешний поставщик вызвал метод **AddRef** объекта для хранения собственной ссылки.</span><span class="sxs-lookup"><span data-stu-id="82fb7-143">This is because the foreign provider has called the object's **AddRef** method to keep its own reference.</span></span> <span data-ttu-id="82fb7-144">Если внешнему поставщику не требуется хранить ссылку на объект Property, то **опентемплатеид** возвратит непривязанный объект Property.</span><span class="sxs-lookup"><span data-stu-id="82fb7-144">If the foreign provider does not need to keep a reference to the property object, then **OpenTemplateID** will return the unbound property object.</span></span> 
  
<span data-ttu-id="82fb7-145">Если **опентемплатеид** не работает с MAPI_E_UNKNOWN_ENTRYID, попробуйте продолжить, рассматривая запись как доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="82fb7-145">If **OpenTemplateID** fails with MAPI_E_UNKNOWN_ENTRYID, try to continue by treating the entry as read-only.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="82fb7-146">См. также</span><span class="sxs-lookup"><span data-stu-id="82fb7-146">See also</span></span>



[<span data-ttu-id="82fb7-147">IABLogon::OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="82fb7-147">IABLogon::OpenTemplateID</span></span>](iablogon-opentemplateid.md)
  
[<span data-ttu-id="82fb7-148">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="82fb7-148">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="82fb7-149">Каноническое свойство PidTagTemplateid</span><span class="sxs-lookup"><span data-stu-id="82fb7-149">PidTagTemplateid Canonical Property</span></span>](pidtagtemplateid-canonical-property.md)
  
[<span data-ttu-id="82fb7-150">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="82fb7-150">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

