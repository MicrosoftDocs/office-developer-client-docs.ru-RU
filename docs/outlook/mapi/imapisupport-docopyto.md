---
title: IMAPISupportDoCopyTo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyTo
api_type:
- COM
ms.assetid: 84019475-5176-4fc5-a3ee-871095077498
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6f6c802f1d5ead1750c05fafc54533487fe3732a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331810"
---
# <a name="imapisupportdocopyto"></a><span data-ttu-id="6f74d-103">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="6f74d-103">IMAPISupport::DoCopyTo</span></span>

  
  
<span data-ttu-id="6f74d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f74d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f74d-105">Копирует или перемещает все свойства одного объекта, кроме специально исключенных, в другой объект.</span><span class="sxs-lookup"><span data-stu-id="6f74d-105">Copies or moves all properties of one object, except for specifically excluded properties, to another object.</span></span>
  
```cpp
HRESULT DoCopyTo(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  ULONG ciidExclude,
  LPCIID rgiidExclude,
  LPSPropTagArray lpExcludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpDestInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="6f74d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f74d-106">Parameters</span></span>

 <span data-ttu-id="6f74d-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="6f74d-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="6f74d-108">[in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, который будет использоваться для доступа к объекту, который имеет свойства для копирования или перемещений.</span><span class="sxs-lookup"><span data-stu-id="6f74d-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="6f74d-109">_lpSrcObj_</span><span class="sxs-lookup"><span data-stu-id="6f74d-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="6f74d-110">[in] Указатель на объект, свойства для копирования или перемещении.</span><span class="sxs-lookup"><span data-stu-id="6f74d-110">[in] A pointer to the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="6f74d-111">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="6f74d-111">_ciidExclude_</span></span>
  
> <span data-ttu-id="6f74d-112">[in] Количество интерфейсов, которые необходимо исключить при копировании или перемещение свойств.</span><span class="sxs-lookup"><span data-stu-id="6f74d-112">[in] The count of interfaces to exclude when you copy or move properties.</span></span>
    
 <span data-ttu-id="6f74d-113">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="6f74d-113">_rgiidExclude_</span></span>
  
> <span data-ttu-id="6f74d-114">[in] Массив идентификаторов интерфейса, который указывает интерфейсы, которые не следует использовать при копировании или перемещение дополнительных сведений в объект назначения.</span><span class="sxs-lookup"><span data-stu-id="6f74d-114">[in] An array of interface identifiers that indicates interfaces that should not be used when you copy or move supplemental information to the destination object.</span></span>
    
 <span data-ttu-id="6f74d-115">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="6f74d-115">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="6f74d-116">[in] Указатель на массив тегов свойств, который определяет теги свойств, которые необходимо исключить из операции копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="6f74d-116">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="6f74d-117">Передача NULL в параметр  _lpExcludeProps_ означает, что все свойства объекта необходимо скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="6f74d-117">Passing NULL in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="6f74d-118">**DoCopyTo** возвращает MAPI_E_INVALID_PARAMETER, когда для члена **cValues** структуры [SPropTagArray,](sproptagarray.md) на который указывает  _lpExcludeProps,_ установлено 0.</span><span class="sxs-lookup"><span data-stu-id="6f74d-118">**DoCopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="6f74d-119">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6f74d-119">_ulUIParam_</span></span>
  
> <span data-ttu-id="6f74d-120">[in] Handle to the parent window of the progress indicator.</span><span class="sxs-lookup"><span data-stu-id="6f74d-120">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="6f74d-121">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="6f74d-121">_lpProgress_</span></span>
  
> <span data-ttu-id="6f74d-122">[in] Указатель на реализацию индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="6f74d-122">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="6f74d-123">Если в параметре  _lpProgress_ передается NULL, MAPI обеспечивает реализацию хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="6f74d-123">If NULL is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="6f74d-124">Параметр _lpProgress_ игнорируется, если MAPI_DIALOG флага в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="6f74d-124">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="6f74d-125">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="6f74d-125">_lpDestInterface_</span></span>
  
> <span data-ttu-id="6f74d-126">[in] Указатель на идентификатор интерфейса, который представляет интерфейс, используемый для доступа к объекту для получения скопированные или перемещенные свойства.</span><span class="sxs-lookup"><span data-stu-id="6f74d-126">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="6f74d-127">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="6f74d-127">_lpDestObj_</span></span>
  
> <span data-ttu-id="6f74d-128">[in] Указатель на объект для получения скопированные или перемещенные свойства.</span><span class="sxs-lookup"><span data-stu-id="6f74d-128">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="6f74d-129">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6f74d-129">_ulFlags_</span></span>
  
> <span data-ttu-id="6f74d-130">[in] Битоваяmas флагов, которая управляет операцией копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="6f74d-130">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="6f74d-131">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="6f74d-131">The following flags can be set:</span></span>
    
<span data-ttu-id="6f74d-132">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="6f74d-132">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="6f74d-133">Отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="6f74d-133">Displays a progress indicator.</span></span> 
    
<span data-ttu-id="6f74d-134">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="6f74d-134">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="6f74d-135">**DoCopyTo** следует выполнить операцию перемещения вместо операции копирования.</span><span class="sxs-lookup"><span data-stu-id="6f74d-135">**DoCopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="6f74d-136">Если этот флаг не установлен, **DoCopyTo** выполняет операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="6f74d-136">When this flag is not set, **DoCopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="6f74d-137">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="6f74d-137">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="6f74d-138">Существующие свойства в объекте назначения не следует перезаписывать.</span><span class="sxs-lookup"><span data-stu-id="6f74d-138">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="6f74d-139">Если этот флаг не установлен, **DoCopyTo** переописает существующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6f74d-139">When this flag is not set, **DoCopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="6f74d-140">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="6f74d-140">_lppProblems_</span></span>
  
> <span data-ttu-id="6f74d-141">[out] При вводе указатель на указатель на [структуру SPropProblemArray;](spropproblemarray.md) в противном случае NULL, что указывает на отсутствие необходимости в сведениях об ошибках.</span><span class="sxs-lookup"><span data-stu-id="6f74d-141">[out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="6f74d-142">Если  _lppProblems_ является допустимым указателем при вводе, **DoCopyTo** возвращает подробные сведения об ошибках при копировании одного или более свойств.</span><span class="sxs-lookup"><span data-stu-id="6f74d-142">If  _lppProblems_ is a valid pointer on input, **DoCopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6f74d-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6f74d-143">Return value</span></span>

<span data-ttu-id="6f74d-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="6f74d-144">S_OK</span></span> 
  
> <span data-ttu-id="6f74d-145">Свойства успешно скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="6f74d-145">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="6f74d-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="6f74d-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="6f74d-147">Свойство, которое необходимо скопировать или перемещено, уже существует в объекте назначения, MAPI_NOREPLACE установлен флаг.</span><span class="sxs-lookup"><span data-stu-id="6f74d-147">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="6f74d-148">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="6f74d-148">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="6f74d-149">Исходный объект прямо или косвенно содержит объект назначения.</span><span class="sxs-lookup"><span data-stu-id="6f74d-149">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="6f74d-150">Перед обнаружением этого условия могли быть выполнены значительные трудоемкие работы, поэтому исходные и назначения объектов могут быть частично изменены.</span><span class="sxs-lookup"><span data-stu-id="6f74d-150">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="6f74d-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="6f74d-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="6f74d-152">Интерфейс, заданный параметром _lpSrcInterface,_ не поддерживается объектом, на который указывает _lpSrcObj,_ или интерфейс, заданный параметром _lpDestInterface,_ не поддерживается объектом, на который указывает _lpDestObj._</span><span class="sxs-lookup"><span data-stu-id="6f74d-152">The interface identified by the  _lpSrcInterface_ parameter is not supported by the object pointed to by  _lpSrcObj_, or the interface identified by the  _lpDestInterface_ parameter is not supported by the object pointed to by  _lpDestObj_.</span></span> 
    
<span data-ttu-id="6f74d-153">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="6f74d-153">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="6f74d-154">Предпринята попытка доступа к объекту, у которого у вызываемого объекта недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="6f74d-154">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="6f74d-155">Эта ошибка возвращается, если объект назначения такой же, как и исходный объект.</span><span class="sxs-lookup"><span data-stu-id="6f74d-155">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="6f74d-156">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6f74d-156">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="6f74d-157">Параметр  _lpSrcInterface_ имеет NULL.</span><span class="sxs-lookup"><span data-stu-id="6f74d-157">The  _lpSrcInterface_ parameter is NULL.</span></span> 
    
<span data-ttu-id="6f74d-158">Следующие значения могут быть возвращены в структуре **SPropProblemArray,** но не в качестве возвращаемой величины **для DoCopyTo.**</span><span class="sxs-lookup"><span data-stu-id="6f74d-158">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyTo**.</span></span> <span data-ttu-id="6f74d-159">Эти ошибки относятся к одному свойству.</span><span class="sxs-lookup"><span data-stu-id="6f74d-159">These errors apply to a single property.</span></span>
  
<span data-ttu-id="6f74d-160">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="6f74d-160">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="6f74d-161">Либо флаг MAPI_UNICODE установлен, а **DoCopyTo** не поддерживает Юникод, либо MAPI_UNICODE не установлен, а **DoCopyTo** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="6f74d-161">Either the MAPI_UNICODE flag was set and **DoCopyTo** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="6f74d-162">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="6f74d-162">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="6f74d-163">Вызываемая не может изменить свойство, так как это свойство, предназначенное только для чтения, вычисляется владельцем конечного объекта.</span><span class="sxs-lookup"><span data-stu-id="6f74d-163">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="6f74d-164">Эта ошибка не является серьезной; Вызываемая должна разрешить продолжение операции копирования.</span><span class="sxs-lookup"><span data-stu-id="6f74d-164">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="6f74d-165">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="6f74d-165">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="6f74d-166">Недопустимый тип свойства.</span><span class="sxs-lookup"><span data-stu-id="6f74d-166">The property type is invalid.</span></span>
    
<span data-ttu-id="6f74d-167">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="6f74d-167">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="6f74d-168">Тип свойства не является типом, ожидаемым для вызываемого объекта.</span><span class="sxs-lookup"><span data-stu-id="6f74d-168">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6f74d-169">Примечания</span><span class="sxs-lookup"><span data-stu-id="6f74d-169">Remarks</span></span>

<span data-ttu-id="6f74d-170">Метод **IMAPISupport::D oCopyTo** реализован для объектов поддержки поставщика store сообщений.</span><span class="sxs-lookup"><span data-stu-id="6f74d-170">The **IMAPISupport::DoCopyTo** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="6f74d-171">Поставщики store сообщений могут вызвать **DoCopyTo** для реализации метода [IMAPIProp::CopyTo](imapiprop-copyto.md) для своих папок и сообщений.</span><span class="sxs-lookup"><span data-stu-id="6f74d-171">Message store providers can call **DoCopyTo** to implement the [IMAPIProp::CopyTo](imapiprop-copyto.md) method for their folders and messages.</span></span> 
  
<span data-ttu-id="6f74d-172">По умолчанию **DoCopyTo** копирует или перемещает все свойства одного объекта в другой.</span><span class="sxs-lookup"><span data-stu-id="6f74d-172">By default, **DoCopyTo** copies or moves all of the properties of one object to another object.</span></span> <span data-ttu-id="6f74d-173">Любые подпроекты в объекте-источнике автоматически включаются в операцию и копируются или перемещаются полностью.</span><span class="sxs-lookup"><span data-stu-id="6f74d-173">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety.</span></span> 
  
<span data-ttu-id="6f74d-174">Если какие-либо из скопированные или перемещенных свойств уже существуют в объекте назначения, существующие свойства перезаписываются новыми свойствами, если в параметре  _ulFlags_ не установлен флаг MAPI_NOREPLACE.</span><span class="sxs-lookup"><span data-stu-id="6f74d-174">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="6f74d-175">Существующие сведения в объекте назначения, который не перезаписан, не будут затронуты.</span><span class="sxs-lookup"><span data-stu-id="6f74d-175">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6f74d-176">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="6f74d-176">Notes to callers</span></span>

<span data-ttu-id="6f74d-177">Чтобы исключить свойства из операции копирования или перемещения, включаем их теги свойств в параметр _lpExcludeProps._</span><span class="sxs-lookup"><span data-stu-id="6f74d-177">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="6f74d-178">Если передать результаты использования макроса [PROP_TAG](prop_tag.md) для создания тега свойства из определенного идентификатора в массиве тегов свойств, все свойства с этим идентификатором будут исключены.</span><span class="sxs-lookup"><span data-stu-id="6f74d-178">If you pass the results of using the [PROP_TAG](prop_tag.md) macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="6f74d-179">Например, следующая запись в массиве тегов свойств приводит к исключению всех свойств с идентификатором 0x8002, независимо от типа:</span><span class="sxs-lookup"><span data-stu-id="6f74d-179">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="6f74d-180">Чтобы избежать копирования времени доставки сообщения при копировании сообщения в другую папку, укажите PR_MESSAGE_DELIVERY_TIME **(** [PidTagMessageDeliveryTime)](pidtagmessagedeliverytime-canonical-property.md)в теге свойства исключить массив.</span><span class="sxs-lookup"><span data-stu-id="6f74d-180">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="6f74d-181">Чтобы исключить список получателей сообщения, добавьте **свойство PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)в массив исключений.</span><span class="sxs-lookup"><span data-stu-id="6f74d-181">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="6f74d-182">Чтобы исключить вложения сообщения, **добавьте** свойство PR_MESSAGE_ATTACHMENTS [(PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)в массив.</span><span class="sxs-lookup"><span data-stu-id="6f74d-182">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="6f74d-183">Аналогичным образом, чтобы предотвратить копирование или перемещение иерархии или таблицы содержимого контейнера папки или адресной книги, включите **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)или **PR_CONTAINER_CONTENTS** ([PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)в тег свойства исключить массив.</span><span class="sxs-lookup"><span data-stu-id="6f74d-183">Similarly, to prevent the copying or moving of a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="6f74d-184">Игнорируйте MAPI_E_COMPUTED ошибки, возвращенные в **структуре SPropProblemArray** в _параметре lppProblems._</span><span class="sxs-lookup"><span data-stu-id="6f74d-184">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
<span data-ttu-id="6f74d-185">Идентификатор интерфейса, на который _указывает lpSrcInterface,_ обычно такой же, как идентификатор интерфейса, на который указывает _lpDestInterface._</span><span class="sxs-lookup"><span data-stu-id="6f74d-185">The interface identifier that  _lpSrcInterface_ points to is usually the same as the interface identifier that  _lpDestInterface_ points to.</span></span> 
  
<span data-ttu-id="6f74d-186">Если передать допустимый идентификатор интерфейса в  _lpDestInterface,_ но недопустимый указатель в  _lpDestObj,_ результаты будут непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="6f74d-186">If you pass an acceptable interface identifier in  _lpDestInterface_ but an invalid pointer in  _lpDestObj_, the results are unpredictable.</span></span> <span data-ttu-id="6f74d-187">Скорее всего, это приведет к сбойу поставщика.</span><span class="sxs-lookup"><span data-stu-id="6f74d-187">Most likely this will cause your provider to fail.</span></span> 
  
<span data-ttu-id="6f74d-188">И наоборот, если известно о дополнительных сведениях, которые не следует копировать или перемещать, добавьте идентификаторы интерфейса для интерфейсов, которые необходимо исключить в массиве, передаваемом в _параметре rgiidExclude._</span><span class="sxs-lookup"><span data-stu-id="6f74d-188">Conversely, if you are aware of supplemental information that should not be copied or moved, add the interface identifiers for the interfaces to be excluded in the array passed in the  _rgiidExclude_ parameter.</span></span> <span data-ttu-id="6f74d-189">Например, если вы копируете сообщения, но не вложения в них, IID_IMessage массив _rgiidExclude._</span><span class="sxs-lookup"><span data-stu-id="6f74d-189">For example, if you are copying messages, but not any of their message attachments, pass IID_IMessage in the  _rgiidExclude_ array.</span></span> <span data-ttu-id="6f74d-190">**DoCopyTo** игнорирует все интерфейсы, перечисленные в  _rgiidExclude,_ которые не распознают.</span><span class="sxs-lookup"><span data-stu-id="6f74d-190">**DoCopyTo** ignores any interfaces listed in  _rgiidExclude_ that it does not recognize.</span></span> 
  
<span data-ttu-id="6f74d-191">При использовании  _параметра rgiidExclude_ для исключения интерфейса он также исключает все интерфейсы, производные от этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6f74d-191">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="6f74d-192">Например, исключение интерфейса [IMAPIContainer](imapicontainerimapiprop.md) приводит к исключению папок или контейнеров адресной книги в зависимости от типа поставщика.</span><span class="sxs-lookup"><span data-stu-id="6f74d-192">For example, excluding the [IMAPIContainer](imapicontainerimapiprop.md) interface causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="6f74d-193">Не исключать [IMAPIProp](imapipropiunknown.md) или [IUnknown,](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) так как так много интерфейсов являются наивны от них.</span><span class="sxs-lookup"><span data-stu-id="6f74d-193">Do not exclude [IMAPIProp](imapipropiunknown.md) or [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) because so many interfaces derive from them.</span></span> 
  
 <span data-ttu-id="6f74d-194">**DoCopyTo** сообщает о глобальных ошибках, которые применяются к операции в целом, и отдельных ошибках, которые применяются к отдельным свойствам.</span><span class="sxs-lookup"><span data-stu-id="6f74d-194">**DoCopyTo** reports global errors that apply to the operation as a whole, and individual errors that apply to individual properties.</span></span> <span data-ttu-id="6f74d-195">Эти отдельные ошибки помещаются в структуру **SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="6f74d-195">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="6f74d-196">Отчеты об ошибках можно подавить на уровне свойства, передав NULL вместо допустимого указателя для параметра структуры массива проблем свойств.</span><span class="sxs-lookup"><span data-stu-id="6f74d-196">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="6f74d-197">Если вы хотите получить сведения об ошибках, передав допустимый указатель структуры **SPropProblemArray** в _параметре lppProblems._</span><span class="sxs-lookup"><span data-stu-id="6f74d-197">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="6f74d-198">Когда **DoCopyTo** возвращает S_OK, проверьте возможные ошибки с отдельными свойствами в структуре.</span><span class="sxs-lookup"><span data-stu-id="6f74d-198">When **DoCopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="6f74d-199">Когда **DoCopyTo** возвращает ошибку, данные в **структуре SPropProblemArray** не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="6f74d-199">When **DoCopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="6f74d-200">Вместо этого вызовите метод [IMAPISupport::GetLastError,](imapisupport-getlasterror.md) чтобы получить подробные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="6f74d-200">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="6f74d-201">Если **DoCopyTo** возвращает S_OK, освободите возвращенную **структуру SPropProblemArray,** вызывая функцию [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="6f74d-201">If **DoCopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="6f74d-202">Если при вызове **DoCopyTo** возникает глобальная ошибка, не используйте или не освободите **структуру SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="6f74d-202">If a global error occurs on the **DoCopyTo** call, do not use or free the **SPropProblemArray** structure.</span></span> <span data-ttu-id="6f74d-203">Поставщики должны игнорировать член _ulIndex_ в **структурах SPropProblemArray,** возвращаемом **DoCopyTo.**</span><span class="sxs-lookup"><span data-stu-id="6f74d-203">Providers should ignore the  _ulIndex_ member in **SPropProblemArray** structures returned by **DoCopyTo**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6f74d-204">См. также</span><span class="sxs-lookup"><span data-stu-id="6f74d-204">See also</span></span>



[<span data-ttu-id="6f74d-205">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="6f74d-205">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="6f74d-206">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="6f74d-206">IMAPISupport::CopyFolder</span></span>](imapisupport-copyfolder.md)
  
[<span data-ttu-id="6f74d-207">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="6f74d-207">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="6f74d-208">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="6f74d-208">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="6f74d-209">Каноническое свойство PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="6f74d-209">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="6f74d-210">Каноническое свойство PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="6f74d-210">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="6f74d-211">Каноническое свойство PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="6f74d-211">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="6f74d-212">Каноническое свойство PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="6f74d-212">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="6f74d-213">Каноническое свойство PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="6f74d-213">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="6f74d-214">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="6f74d-214">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="6f74d-215">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="6f74d-215">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="6f74d-216">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6f74d-216">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

