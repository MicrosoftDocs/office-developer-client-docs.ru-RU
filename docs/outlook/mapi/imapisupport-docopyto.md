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
# <a name="imapisupportdocopyto"></a><span data-ttu-id="0385f-103">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="0385f-103">IMAPISupport::DoCopyTo</span></span>

  
  
<span data-ttu-id="0385f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0385f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0385f-105">Копирует или перемещает все свойства одного объекта, за исключением специально исключенных свойств, в другой объект.</span><span class="sxs-lookup"><span data-stu-id="0385f-105">Copies or moves all properties of one object, except for specifically excluded properties, to another object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="0385f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="0385f-106">Parameters</span></span>

 <span data-ttu-id="0385f-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="0385f-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="0385f-108">[in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, который будет использоваться для доступа к объекту, который имеет свойства, которые необходимо скопировать или перена перемещать.</span><span class="sxs-lookup"><span data-stu-id="0385f-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="0385f-109">_lpSrcObj_</span><span class="sxs-lookup"><span data-stu-id="0385f-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="0385f-110">[in] Указатель на объект, у него есть свойства, которые необходимо скопировать или перена перемещать.</span><span class="sxs-lookup"><span data-stu-id="0385f-110">[in] A pointer to the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="0385f-111">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="0385f-111">_ciidExclude_</span></span>
  
> <span data-ttu-id="0385f-112">[in] Количество интерфейсов, которые необходимо исключить при копировании или перемещения свойств.</span><span class="sxs-lookup"><span data-stu-id="0385f-112">[in] The count of interfaces to exclude when you copy or move properties.</span></span>
    
 <span data-ttu-id="0385f-113">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="0385f-113">_rgiidExclude_</span></span>
  
> <span data-ttu-id="0385f-114">[in] Массив идентификаторов интерфейса, который указывает интерфейсы, которые не следует использовать при копировании или перемещение дополнительных сведений в объект назначения.</span><span class="sxs-lookup"><span data-stu-id="0385f-114">[in] An array of interface identifiers that indicates interfaces that should not be used when you copy or move supplemental information to the destination object.</span></span>
    
 <span data-ttu-id="0385f-115">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="0385f-115">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="0385f-116">[in] Указатель на массив тегов свойств, который определяет теги свойств, которые следует исключить из операции копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="0385f-116">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="0385f-117">Передача NULL в  _параметре lpExcludeProps_ указывает на то, что все свойства объекта должны быть скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="0385f-117">Passing NULL in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="0385f-118">**DoCopyTo** возвращает MAPI_E_INVALID_PARAMETER, когда член **cValues** структуры [SPropTagArray,](sproptagarray.md) на который указывает  _lpExcludeProps,_ задает 0.</span><span class="sxs-lookup"><span data-stu-id="0385f-118">**DoCopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="0385f-119">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0385f-119">_ulUIParam_</span></span>
  
> <span data-ttu-id="0385f-120">[in] Ручка родительского окна индикатора прогресса.</span><span class="sxs-lookup"><span data-stu-id="0385f-120">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="0385f-121">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="0385f-121">_lpProgress_</span></span>
  
> <span data-ttu-id="0385f-122">[in] Указатель на реализацию индикатора прогресса.</span><span class="sxs-lookup"><span data-stu-id="0385f-122">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="0385f-123">Если NULL передается в  _параметре lpProgress,_ MAPI обеспечивает реализацию прогресса.</span><span class="sxs-lookup"><span data-stu-id="0385f-123">If NULL is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="0385f-124">Параметр _lpProgress_ игнорируется, если флаг MAPI_DIALOG в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="0385f-124">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="0385f-125">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="0385f-125">_lpDestInterface_</span></span>
  
> <span data-ttu-id="0385f-126">[in] Указатель на идентификатор интерфейса, который представляет интерфейс, который будет использоваться для доступа к объекту для получения скопированные или перенесенные свойства.</span><span class="sxs-lookup"><span data-stu-id="0385f-126">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="0385f-127">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="0385f-127">_lpDestObj_</span></span>
  
> <span data-ttu-id="0385f-128">[in] Указатель на объект для получения скопированные или перенесенные свойства.</span><span class="sxs-lookup"><span data-stu-id="0385f-128">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="0385f-129">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0385f-129">_ulFlags_</span></span>
  
> <span data-ttu-id="0385f-130">[in] Битмашка флагов, которые контролируют операцию копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="0385f-130">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="0385f-131">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="0385f-131">The following flags can be set:</span></span>
    
<span data-ttu-id="0385f-132">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="0385f-132">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="0385f-133">Отображает индикатор прогресса.</span><span class="sxs-lookup"><span data-stu-id="0385f-133">Displays a progress indicator.</span></span> 
    
<span data-ttu-id="0385f-134">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="0385f-134">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="0385f-135">**DoCopyTo** должен выполнять операцию перемещения вместо операции копирования.</span><span class="sxs-lookup"><span data-stu-id="0385f-135">**DoCopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="0385f-136">Если этот флаг не установлен, **DoCopyTo** выполняет операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="0385f-136">When this flag is not set, **DoCopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="0385f-137">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="0385f-137">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="0385f-138">Существующие свойства в объекте назначения не должны быть перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="0385f-138">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="0385f-139">Если этот флаг не установлен, **DoCopyTo** переописает существующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0385f-139">When this flag is not set, **DoCopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="0385f-140">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="0385f-140">_lppProblems_</span></span>
  
> <span data-ttu-id="0385f-141">[вышел] На входе указатель на указатель на [структуру SPropProblemArray;](spropproblemarray.md) в противном случае NULL, что не указывает на отсутствие необходимости в сведениях об ошибках.</span><span class="sxs-lookup"><span data-stu-id="0385f-141">[out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="0385f-142">Если  _lppProblems_ является допустимым указателем на входе, **DoCopyTo** возвращает подробные сведения об ошибках при копировании одного или более свойств.</span><span class="sxs-lookup"><span data-stu-id="0385f-142">If  _lppProblems_ is a valid pointer on input, **DoCopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0385f-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0385f-143">Return value</span></span>

<span data-ttu-id="0385f-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="0385f-144">S_OK</span></span> 
  
> <span data-ttu-id="0385f-145">Свойства были успешно скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="0385f-145">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="0385f-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="0385f-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="0385f-147">Свойство, которое будет скопировано или перемещено, уже существует в объекте назначения, MAPI_NOREPLACE задает флаг.</span><span class="sxs-lookup"><span data-stu-id="0385f-147">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="0385f-148">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="0385f-148">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="0385f-149">Исходный объект прямо или косвенно содержит объект назначения.</span><span class="sxs-lookup"><span data-stu-id="0385f-149">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="0385f-150">Перед обнаружением этого условия, возможно, была выполнена значительная работа, поэтому объекты источника и назначения могут быть частично изменены.</span><span class="sxs-lookup"><span data-stu-id="0385f-150">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="0385f-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="0385f-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="0385f-152">Интерфейс, идентифицированный параметром  _lpSrcInterface,_ не поддерживается объектом, на который указывает  _lpSrcObj,_ или интерфейс, идентифицированный параметром  _lpDestInterface,_ не поддерживается объектом, на который указывает  _lpDestObj_.</span><span class="sxs-lookup"><span data-stu-id="0385f-152">The interface identified by the  _lpSrcInterface_ parameter is not supported by the object pointed to by  _lpSrcObj_, or the interface identified by the  _lpDestInterface_ parameter is not supported by the object pointed to by  _lpDestObj_.</span></span> 
    
<span data-ttu-id="0385f-153">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="0385f-153">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="0385f-154">Была предпринята попытка доступа к объекту, для которого у вызываемого недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="0385f-154">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="0385f-155">Эта ошибка возвращается, если объект назначения является таким же, как и исходный объект.</span><span class="sxs-lookup"><span data-stu-id="0385f-155">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="0385f-156">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0385f-156">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="0385f-157">Параметр  _lpSrcInterface_ — NULL.</span><span class="sxs-lookup"><span data-stu-id="0385f-157">The  _lpSrcInterface_ parameter is NULL.</span></span> 
    
<span data-ttu-id="0385f-158">Следующие значения могут быть возвращены в **структуре SPropProblemArray,** но не в качестве значений возврата **для DoCopyTo.**</span><span class="sxs-lookup"><span data-stu-id="0385f-158">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyTo**.</span></span> <span data-ttu-id="0385f-159">Эти ошибки применимы к одному свойству.</span><span class="sxs-lookup"><span data-stu-id="0385f-159">These errors apply to a single property.</span></span>
  
<span data-ttu-id="0385f-160">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="0385f-160">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="0385f-161">Либо флаг MAPI_UNICODE был установлен, а **DoCopyTo** не поддерживает Юникод, либо MAPI_UNICODE не задавалось, а **DoCopyTo** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="0385f-161">Either the MAPI_UNICODE flag was set and **DoCopyTo** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="0385f-162">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="0385f-162">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="0385f-163">Свойство не может быть изменено вызываемой, так как оно является свойством только для чтения, вычисляется владельцем объекта назначения.</span><span class="sxs-lookup"><span data-stu-id="0385f-163">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="0385f-164">Эта ошибка не является серьезной; вызываемая должна разрешить продолжение операции копирования.</span><span class="sxs-lookup"><span data-stu-id="0385f-164">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="0385f-165">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="0385f-165">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="0385f-166">Тип свойства недействителен.</span><span class="sxs-lookup"><span data-stu-id="0385f-166">The property type is invalid.</span></span>
    
<span data-ttu-id="0385f-167">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="0385f-167">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="0385f-168">Тип свойства не является типом, ожидаемым вызываемой.</span><span class="sxs-lookup"><span data-stu-id="0385f-168">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0385f-169">Примечания</span><span class="sxs-lookup"><span data-stu-id="0385f-169">Remarks</span></span>

<span data-ttu-id="0385f-170">Метод **IMAPISupport::D oCopyTo** реализован для объектов поддержки поставщиков сообщений.</span><span class="sxs-lookup"><span data-stu-id="0385f-170">The **IMAPISupport::DoCopyTo** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="0385f-171">Поставщики магазинов сообщений могут вызвать **DoCopyTo** для реализации метода [IMAPIProp::CopyTo](imapiprop-copyto.md) для своих папок и сообщений.</span><span class="sxs-lookup"><span data-stu-id="0385f-171">Message store providers can call **DoCopyTo** to implement the [IMAPIProp::CopyTo](imapiprop-copyto.md) method for their folders and messages.</span></span> 
  
<span data-ttu-id="0385f-172">По умолчанию **DoCopyTo** копирует или перемещает все свойства одного объекта на другой объект.</span><span class="sxs-lookup"><span data-stu-id="0385f-172">By default, **DoCopyTo** copies or moves all of the properties of one object to another object.</span></span> <span data-ttu-id="0385f-173">Любые подобъекты в объекте источника автоматически включаются в операцию и копируются или перемещаются в полном объеме.</span><span class="sxs-lookup"><span data-stu-id="0385f-173">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety.</span></span> 
  
<span data-ttu-id="0385f-174">Если какие-либо из скопированные или перемещенные свойства уже существуют в объекте назначения, существующие свойства перезаписываются новыми свойствами, если флаг MAPI_NOREPLACE не задан в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="0385f-174">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="0385f-175">Существующая информация в объекте назначения, который не перезаписан, остается нетронутой.</span><span class="sxs-lookup"><span data-stu-id="0385f-175">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0385f-176">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="0385f-176">Notes to callers</span></span>

<span data-ttu-id="0385f-177">Чтобы исключить свойства из операции копирования или перемещения, включи их теги свойств в параметр _lpExcludeProps._</span><span class="sxs-lookup"><span data-stu-id="0385f-177">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="0385f-178">Если вы передаете результаты использования [макроса PROP_TAG](prop_tag.md) для создания тега свойств из определенного идентификатора в массиве тегов свойств, все свойства с этим идентификатором будут исключены.</span><span class="sxs-lookup"><span data-stu-id="0385f-178">If you pass the results of using the [PROP_TAG](prop_tag.md) macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="0385f-179">Например, следующая запись в массиве тегов свойств приводит к исключению всех свойств с идентификатором 0x8002, независимо от типа:</span><span class="sxs-lookup"><span data-stu-id="0385f-179">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="0385f-180">Чтобы избежать копирования времени доставки сообщения при копировании сообщения в  другую папку, укажите PR_MESSAGE_DELIVERY_TIME[(PidTagMessageDeliveryTime)](pidtagmessagedeliverytime-canonical-property.md)в теге свойства исключить массив.</span><span class="sxs-lookup"><span data-stu-id="0385f-180">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="0385f-181">Чтобы исключить список получателей сообщения, **добавьте свойство PR_MESSAGE_RECIPIENTS** [(PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)в массив исключений.</span><span class="sxs-lookup"><span data-stu-id="0385f-181">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="0385f-182">Чтобы исключить вложения сообщения, **добавьте свойство** [PR_MESSAGE_ATTACHMENTS (PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)в массив.</span><span class="sxs-lookup"><span data-stu-id="0385f-182">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="0385f-183">Аналогично, чтобы предотвратить копирование или перемещение иерархии или таблицы содержимого контейнера папки или адресной **книги,** включите PR_CONTAINER_HIERARCHY [(PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)или **PR_CONTAINER_CONTENTS** [(PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)в массив исключений тега свойств.</span><span class="sxs-lookup"><span data-stu-id="0385f-183">Similarly, to prevent the copying or moving of a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="0385f-184">Игнорируйте MAPI_E_COMPUTED ошибки, возвращаемые в **структуре SPropProblemArray** в _параметре lppProblems._</span><span class="sxs-lookup"><span data-stu-id="0385f-184">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
<span data-ttu-id="0385f-185">Идентификатор интерфейса, на который _указывает lpSrcInterface,_ обычно такой же, как и идентификатор интерфейса, на который указывает _lpDestInterface._</span><span class="sxs-lookup"><span data-stu-id="0385f-185">The interface identifier that  _lpSrcInterface_ points to is usually the same as the interface identifier that  _lpDestInterface_ points to.</span></span> 
  
<span data-ttu-id="0385f-186">Если вы передаете допустимый идентификатор интерфейса  _в lpDestInterface,_ но недействительный указатель  _в lpDestObj,_ результаты непредсказуемы.</span><span class="sxs-lookup"><span data-stu-id="0385f-186">If you pass an acceptable interface identifier in  _lpDestInterface_ but an invalid pointer in  _lpDestObj_, the results are unpredictable.</span></span> <span data-ttu-id="0385f-187">Скорее всего, это приведет к сбой поставщика.</span><span class="sxs-lookup"><span data-stu-id="0385f-187">Most likely this will cause your provider to fail.</span></span> 
  
<span data-ttu-id="0385f-188">И наоборот, если вам известно о дополнительных сведениях, которые не следует копировать или перемещать, добавьте идентификаторы интерфейса для исключенных интерфейсов в массиве, переданного в _параметре rgiidExclude._</span><span class="sxs-lookup"><span data-stu-id="0385f-188">Conversely, if you are aware of supplemental information that should not be copied or moved, add the interface identifiers for the interfaces to be excluded in the array passed in the  _rgiidExclude_ parameter.</span></span> <span data-ttu-id="0385f-189">Например, если вы копируете сообщения, но не какие-либо из их вложений сообщений, IID_IMessage в _массиве rgiidExclude._</span><span class="sxs-lookup"><span data-stu-id="0385f-189">For example, if you are copying messages, but not any of their message attachments, pass IID_IMessage in the  _rgiidExclude_ array.</span></span> <span data-ttu-id="0385f-190">**DoCopyTo игнорирует** все интерфейсы, указанные в  _rgiidExclude,_ которые он не распознает.</span><span class="sxs-lookup"><span data-stu-id="0385f-190">**DoCopyTo** ignores any interfaces listed in  _rgiidExclude_ that it does not recognize.</span></span> 
  
<span data-ttu-id="0385f-191">При использовании  _параметра rgiidExclude_ для исключения интерфейса он также исключает все интерфейсы, полученные из этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0385f-191">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="0385f-192">Например, исключение интерфейса [IMAPIContainer](imapicontainerimapiprop.md) приводит к исключению папок или контейнеров адресной книги в зависимости от типа поставщика.</span><span class="sxs-lookup"><span data-stu-id="0385f-192">For example, excluding the [IMAPIContainer](imapicontainerimapiprop.md) interface causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="0385f-193">Не исключайте [IMAPIProp](imapipropiunknown.md) или [IUnknown,](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) так как из них вытекает так много интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="0385f-193">Do not exclude [IMAPIProp](imapipropiunknown.md) or [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) because so many interfaces derive from them.</span></span> 
  
 <span data-ttu-id="0385f-194">**DoCopyTo** сообщает о глобальных ошибках, которые применяются к операции в целом, и об отдельных ошибках, которые применяются к отдельным свойствам.</span><span class="sxs-lookup"><span data-stu-id="0385f-194">**DoCopyTo** reports global errors that apply to the operation as a whole, and individual errors that apply to individual properties.</span></span> <span data-ttu-id="0385f-195">Эти отдельные ошибки помещают в **структуру SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="0385f-195">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="0385f-196">Вы можете подавить отчет об ошибках на уровне свойств, передав параметру структуры массива проблем свойств NULL, а не допустимый указатель.</span><span class="sxs-lookup"><span data-stu-id="0385f-196">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="0385f-197">Если вы хотите получить сведения об ошибках, передай допустимый указатель **структуры SPropProblemArray** в _параметре lppProblems._</span><span class="sxs-lookup"><span data-stu-id="0385f-197">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="0385f-198">Когда **DoCopyTo** возвращает S_OK, проверьте возможные ошибки с отдельными свойствами в структуре.</span><span class="sxs-lookup"><span data-stu-id="0385f-198">When **DoCopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="0385f-199">Когда **DoCopyTo** возвращает ошибку, в структуре **SPropProblemArray** не возвращается информация.</span><span class="sxs-lookup"><span data-stu-id="0385f-199">When **DoCopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="0385f-200">Вместо этого вызовите [метод IMAPISupport::GetLastError,](imapisupport-getlasterror.md) чтобы получить подробные сведения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="0385f-200">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="0385f-201">Если **DoCopyTo** возвращает S_OK, освободите возвращенную структуру **SPropProblemArray,** позвонив функцию [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="0385f-201">If **DoCopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="0385f-202">Если в вызове **DoCopyTo** возникает глобальная ошибка, не используйте или освободите **структуру SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="0385f-202">If a global error occurs on the **DoCopyTo** call, do not use or free the **SPropProblemArray** structure.</span></span> <span data-ttu-id="0385f-203">Поставщики должны игнорировать _участника ulIndex_ в **структурах SPropProblemArray,** возвращенных **DoCopyTo.**</span><span class="sxs-lookup"><span data-stu-id="0385f-203">Providers should ignore the  _ulIndex_ member in **SPropProblemArray** structures returned by **DoCopyTo**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0385f-204">См. также</span><span class="sxs-lookup"><span data-stu-id="0385f-204">See also</span></span>



[<span data-ttu-id="0385f-205">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="0385f-205">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="0385f-206">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="0385f-206">IMAPISupport::CopyFolder</span></span>](imapisupport-copyfolder.md)
  
[<span data-ttu-id="0385f-207">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="0385f-207">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="0385f-208">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0385f-208">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="0385f-209">Каноническое свойство PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="0385f-209">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="0385f-210">Каноническое свойство PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="0385f-210">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="0385f-211">Каноническое свойство PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="0385f-211">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="0385f-212">Каноническое свойство PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="0385f-212">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="0385f-213">Каноническое свойство PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="0385f-213">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="0385f-214">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="0385f-214">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="0385f-215">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="0385f-215">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="0385f-216">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0385f-216">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

