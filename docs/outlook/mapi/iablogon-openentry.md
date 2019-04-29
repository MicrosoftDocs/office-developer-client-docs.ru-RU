---
title: Иаблогонопенентри
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenEntry
api_type:
- COM
ms.assetid: 1cfb82f7-5215-4faa-af25-5b1da7e31209
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 70f61ef553350f08eed96c1ee4e9ab790359d1fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409232"
---
# <a name="iablogonopenentry"></a><span data-ttu-id="e3c6e-103">IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="e3c6e-103">IABLogon::OpenEntry</span></span>

  
  
<span data-ttu-id="e3c6e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3c6e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3c6e-105">Открывает контейнер, пользователя обмена сообщениями или список рассылки и возвращает указатель на реализацию интерфейса для предоставления дальнейших прав доступа.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-105">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="e3c6e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3c6e-106">Parameters</span></span>

 <span data-ttu-id="e3c6e-107">_Кбентрид_</span><span class="sxs-lookup"><span data-stu-id="e3c6e-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="e3c6e-108">возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="e3c6e-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e3c6e-109">_Лпентрид_</span><span class="sxs-lookup"><span data-stu-id="e3c6e-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="e3c6e-110">возврата Указатель на идентификатор элемента контейнера, пользователя обмена сообщениями или списка рассылки, который необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-110">[in] A pointer to the entry identifier of the container, messaging user, or distribution list to open.</span></span>
    
 <span data-ttu-id="e3c6e-111">_Лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="e3c6e-111">_lpInterface_</span></span>
  
> <span data-ttu-id="e3c6e-112">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к открытому объекту.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the open object.</span></span> <span data-ttu-id="e3c6e-113">При передаче значения NULL возвращается идентификатор для стандартного интерфейса объекта.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-113">Passing NULL returns the identifier for the object's standard interface.</span></span> <span data-ttu-id="e3c6e-114">Для контейнеров стандартный интерфейс — [иабконтаинер: IMAPIContainer](iabcontainerimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="e3c6e-114">For containers, the standard interface is [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md).</span></span> <span data-ttu-id="e3c6e-115">Стандартные интерфейсы для объектов адресных книг [: идистлист: IMAPIContainer](idistlistimapicontainer.md) для списка рассылки и [имаилусер: IMAPIProp](imailuserimapiprop.md) для пользователя обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-115">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="e3c6e-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e3c6e-116">_ulFlags_</span></span>
  
> <span data-ttu-id="e3c6e-117">возврата Битовая маска флагов, определяющих способ открытия объекта.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="e3c6e-118">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="e3c6e-118">The following flags can be set:</span></span>
    
<span data-ttu-id="e3c6e-119">МАПИ_БЕСТ_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="e3c6e-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="e3c6e-120">Запрос на открытие объекта с максимальным количеством сетевых разрешений, разрешенных для пользователя, и максимальным доступом к клиентскому приложению.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-120">Requests that the object be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="e3c6e-121">Например, если у клиента есть разрешение на чтение и запись, объект должен быть открыт с разрешением на чтение и запись; Если клиент имеет разрешение только на чтение, объект должен быть открыт с разрешением только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-121">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only permission, the object should be opened with read-only permission.</span></span>
    
<span data-ttu-id="e3c6e-122">МАПИ_ДЕФЕРРЕД_ЕРРОРС</span><span class="sxs-lookup"><span data-stu-id="e3c6e-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="e3c6e-123">Позволяет методу **OpenEntry** успешно возвращать значение, возможно, перед тем, как вызывающий клиент полностью получил доступ к объекту.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-123">Allows the **OpenEntry** method to return successfully, possibly before the calling client has fully accessed the object.</span></span> <span data-ttu-id="e3c6e-124">Если доступ к объекту не осуществляется, выполнение следующего вызова объекта может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-124">If the object is not accessed, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="e3c6e-125">МАПИ_МОДИФИ</span><span class="sxs-lookup"><span data-stu-id="e3c6e-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="e3c6e-126">ЗаПрашивает разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-126">Requests read/write permission.</span></span> <span data-ttu-id="e3c6e-127">По умолчанию объекты открываются с доступом только для чтения, и клиенты не должны предполагать, что предоставлено разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-127">By default, objects are opened with read-only access, and clients should not assume that read/write permission has been granted.</span></span>
    
 <span data-ttu-id="e3c6e-128">_Лпулобжтипе_</span><span class="sxs-lookup"><span data-stu-id="e3c6e-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="e3c6e-129">вышли Указатель на тип открытого объекта.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="e3c6e-130">_Лппунк_</span><span class="sxs-lookup"><span data-stu-id="e3c6e-130">_lppUnk_</span></span>
  
> <span data-ttu-id="e3c6e-131">вышли Указатель на указатель на открытый объект.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e3c6e-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="e3c6e-132">Remarks</span></span>

<span data-ttu-id="e3c6e-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="e3c6e-133">S_OK</span></span> 
  
> <span data-ttu-id="e3c6e-134">Объект был успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="e3c6e-135">МАПИ_Е_НО_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="e3c6e-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="e3c6e-136">У пользователя недостаточно разрешений, чтобы открыть объект, или была предпринята попытка открыть объект, доступный только для чтения, с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-136">Either the user has insufficient permissions to open the object, or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="e3c6e-137">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="e3c6e-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="e3c6e-138">Идентификатор записи, заданный параметром _лпентрид_ , не представляет объект.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-138">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="e3c6e-139">МАПИ_Е_УНКНОВН_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="e3c6e-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="e3c6e-140">Идентификатор записи в параметре _лпентрид_ не является форматом, распознаваемым поставщиком адресной книги.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-140">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the address book provider.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e3c6e-141">Примечания</span><span class="sxs-lookup"><span data-stu-id="e3c6e-141">Remarks</span></span>

<span data-ttu-id="e3c6e-142">MAPI вызывает метод **OpenEntry** для открытия контейнера, пользователя обмена сообщениями или списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-142">MAPI calls the **OpenEntry** method to open a container, messaging user, or distribution list.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e3c6e-143">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="e3c6e-143">Notes to implementers</span></span>

<span data-ttu-id="e3c6e-144">Перед тем как MAPI вызывает метод **OpenEntry** , он определяет, что идентификатор записи в параметре _лпентрид_ принадлежит вам, а не другому поставщику.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-144">Before MAPI calls your **OpenEntry** method, it determines that the entry identifier in the  _lpEntryID_ parameter belongs to you and not to another provider.</span></span> <span data-ttu-id="e3c6e-145">MAPI выполняет это, сопоставляя структуру [мапиуид](mapiuid.md) в идентификаторе записи с **мапиуид** , который вы зарегистрировали, вызвав метод [имаписуппорт:: сетпровидеруид](imapisupport-setprovideruid.md) при запуске.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-145">MAPI does this by matching the [MAPIUID](mapiuid.md) structure in the entry identifier with the **MAPIUID** that you registered by calling the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method at startup.</span></span> 
  
<span data-ttu-id="e3c6e-146">Откройте объект только для чтения, если не установлен флаг МАПИ_МОДИФИ или МАПИ_БЕСТ_АКЦЕСС в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="e3c6e-146">Open the object as read-only, unless the MAPI_MODIFY or MAPI_BEST_ACCESS flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="e3c6e-147">Если вы не разрешаете изменять запрошенный объект, не открывайте этот объект и не возвращаете значение МАПИ_Е_НО_АКЦЕСС.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-147">If you do not allow modification for the requested object, do not open the object at all and return MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="e3c6e-148">Если MAPI передает значение NULL для _лпентрид_, откройте корневой контейнер в иерархии контейнера.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-148">If MAPI passes NULL for  _lpEntryID_, open the root container in your container hierarchy.</span></span>
  
<span data-ttu-id="e3c6e-149">Объект, который вы хотите открыть, может быть объектом, скопированным из другого поставщика.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-149">The object that you are being asked to open might be an object copied from another provider.</span></span> <span data-ttu-id="e3c6e-150">В этом случае он будет поддерживать свойство **пр_темплатеид** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e3c6e-150">In this case, it will support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="e3c6e-151">Если объект поддерживает это свойство, вызовите метод [имаписуппорт:: опентемплатеид](imapisupport-opentemplateid.md) для привязывания к коду этой записи в внешнем поставщике, передавая **пр_темплатеид** в параметре _лптемплатеид_ и 0 в _ултемплатефлагс _параметр.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-151">If the object does support this property, call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method to bind to code for this entry in the foreign provider, passing **PR_TEMPLATEID** in the  _lpTemplateID_ parameter and 0 in the  _ulTemplateFlags_ parameter.</span></span> <span data-ttu-id="e3c6e-152">**Имаписуппорт:: опентемплатеид** передает эту информацию внешнему поставщику при вызове метода [Иаблогон:: опентемплатеид](iablogon-opentemplateid.md) для внешнего поставщика.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-152">**IMAPISupport::OpenTemplateID** passes this information to the foreign provider in a call to the foreign provider's [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) method.</span></span> <span data-ttu-id="e3c6e-153">Если **имаписуппорт:: опентемплатеид** вызывает ошибку, обычно из-за того, что внешний поставщик недоступен или не включен в профиль, попробуйте продолжить, рассматривая несвязанную запись как доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e3c6e-153">If **IMAPISupport::OpenTemplateID** raises an error, usually because the foreign provider is unavailable or not included in the profile, try to continue by treating the unbound entry as read-only.</span></span> <span data-ttu-id="e3c6e-154">Дополнительные сведения об открытии записей для внешних адресных книг представлены в разделе Работа в [качестве поставщика адресНых книг узла](acting-as-a-host-address-book-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e3c6e-154">For more information about opening foreign address book entries, see [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e3c6e-155">См. также</span><span class="sxs-lookup"><span data-stu-id="e3c6e-155">See also</span></span>



[<span data-ttu-id="e3c6e-156">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e3c6e-156">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

