---
title: IMAPISupportDoCopyProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoCopyProps
api_type:
- COM
ms.assetid: 2446ef52-578a-4004-9719-de9b0207ccad
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 24107ae1926c8590da6a823a354eeae72d72f248
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405585"
---
# <a name="imapisupportdocopyprops"></a><span data-ttu-id="6b237-103">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="6b237-103">IMAPISupport::DoCopyProps</span></span>

  
  
<span data-ttu-id="6b237-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b237-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b237-105">Копирует или перемещает одно или несколько свойств объекта на другой объект.</span><span class="sxs-lookup"><span data-stu-id="6b237-105">Copies or moves one or more properties of an object to another object.</span></span>
  
```cpp
HRESULT DoCopyProps(
  LPCIID lpSrcInterface,
  LPVOID lpSrcObj,
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpDestInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="6b237-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6b237-106">Parameters</span></span>

 <span data-ttu-id="6b237-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="6b237-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="6b237-108">[in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, который будет использоваться для доступа к объекту со свойствами, которые будут скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="6b237-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object with the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="6b237-109">_lpSrcObj_</span><span class="sxs-lookup"><span data-stu-id="6b237-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="6b237-110">[in] Указатель на объект, содержащий свойства, которые будут скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="6b237-110">[in] A pointer to the object that contains the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="6b237-111">_lpIncludeProps_</span><span class="sxs-lookup"><span data-stu-id="6b237-111">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="6b237-112">[in] Указатель на структуру [SPropTagArray,](sproptagarray.md) которая содержит засчитанный массив тегов свойств, которые указывают свойства копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="6b237-112">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains a counted array of property tags that indicate the properties to copy or move.</span></span> <span data-ttu-id="6b237-113">Параметр  _lpIncludeProps не_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="6b237-113">The  _lpIncludeProps_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="6b237-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6b237-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="6b237-115">[in] Ручка родительского окна индикатора прогресса.</span><span class="sxs-lookup"><span data-stu-id="6b237-115">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="6b237-116">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="6b237-116">_lpProgress_</span></span>
  
> <span data-ttu-id="6b237-117">[in] Указатель на реализацию индикатора прогресса.</span><span class="sxs-lookup"><span data-stu-id="6b237-117">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="6b237-118">Если NULL передается в  _параметре lpProgress,_ индикатор прогресса отображается с помощью реализации MAPI.</span><span class="sxs-lookup"><span data-stu-id="6b237-118">If NULL is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="6b237-119">Параметр _lpProgress_ игнорируется, если флаг MAPI_DIALOG в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="6b237-119">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="6b237-120">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="6b237-120">_lpDestInterface_</span></span>
  
> <span data-ttu-id="6b237-121">[in] Указатель на идентификатор интерфейса, который представляет интерфейс, используемый для доступа к объекту для получения скопированные или перемещенные свойства.</span><span class="sxs-lookup"><span data-stu-id="6b237-121">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the properties that are copied or moved.</span></span>
    
 <span data-ttu-id="6b237-122">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="6b237-122">_lpDestObj_</span></span>
  
> <span data-ttu-id="6b237-123">[in] Указатель на объект для получения скопированные или перенесенные свойства.</span><span class="sxs-lookup"><span data-stu-id="6b237-123">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="6b237-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6b237-124">_ulFlags_</span></span>
  
> <span data-ttu-id="6b237-125">[in] Битмаска флагов, которые контролируют, как выполняется операция копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="6b237-125">[in] A bitmask of flags that controls how the copy or move operation is performed.</span></span> <span data-ttu-id="6b237-126">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="6b237-126">The following flags can be set:</span></span>
    
<span data-ttu-id="6b237-127">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="6b237-127">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="6b237-128">Отображает индикатор прогресса.</span><span class="sxs-lookup"><span data-stu-id="6b237-128">Displays a progress indicator.</span></span>
    
<span data-ttu-id="6b237-129">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="6b237-129">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="6b237-130">**DoCopyProps** должен выполнять операцию перемещения вместо операции копирования.</span><span class="sxs-lookup"><span data-stu-id="6b237-130">**DoCopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="6b237-131">Если этот флаг не установлен, **DoCopyProps** выполняет операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="6b237-131">When this flag is not set, **DoCopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="6b237-132">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="6b237-132">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="6b237-133">Существующие свойства в объекте назначения не должны быть перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="6b237-133">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="6b237-134">Если этот флаг не установлен, **DoCopyProps** переопрестит существующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6b237-134">When this flag is not set, **DoCopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="6b237-135">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="6b237-135">_lppProblems_</span></span>
  
> <span data-ttu-id="6b237-136">[in, out] На входе указатель на указатель на [структуру SPropProblemArray;](spropproblemarray.md) в противном случае NULL, что не указывает на отсутствие необходимости в сведениях об ошибках.</span><span class="sxs-lookup"><span data-stu-id="6b237-136">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="6b237-137">Если  _lppProblems_ является допустимым указателем на входе, **DoCopyProps** возвращает подробные сведения об ошибках при копировании одного или более свойств.</span><span class="sxs-lookup"><span data-stu-id="6b237-137">If  _lppProblems_ is a valid pointer on input, **DoCopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6b237-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b237-138">Return value</span></span>

<span data-ttu-id="6b237-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="6b237-139">S_OK</span></span> 
  
> <span data-ttu-id="6b237-140">Свойства успешно копировали или перемещали.</span><span class="sxs-lookup"><span data-stu-id="6b237-140">Properties were successfully copied or moved.</span></span>
    
<span data-ttu-id="6b237-141">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="6b237-141">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="6b237-142">Свойство, которое будет скопировано или перемещено, уже существует в объекте назначения, MAPI_NOREPLACE задает флаг.</span><span class="sxs-lookup"><span data-stu-id="6b237-142">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="6b237-143">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="6b237-143">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="6b237-144">Исходный объект прямо или косвенно содержит объект назначения.</span><span class="sxs-lookup"><span data-stu-id="6b237-144">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="6b237-145">Перед обнаружением этого условия, возможно, была выполнена значительная работа, поэтому объекты источника и назначения могут быть частично изменены.</span><span class="sxs-lookup"><span data-stu-id="6b237-145">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="6b237-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="6b237-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="6b237-147">Интерфейс, идентифицированный  _параметром lpSrcInterface,_ не поддерживается исходным объектом, или интерфейс, идентифицированный  _параметром lpDestInterface,_ не поддерживается объектом назначения.</span><span class="sxs-lookup"><span data-stu-id="6b237-147">The interface identified by the  _lpSrcInterface_ parameter is not supported by the source object, or the interface identified by the  _lpDestInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="6b237-148">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="6b237-148">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="6b237-149">Была предпринята попытка доступа к объекту, для которого у вызываемого недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="6b237-149">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="6b237-150">Эта ошибка возвращается, если объект назначения является таким же, как и исходный объект.</span><span class="sxs-lookup"><span data-stu-id="6b237-150">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="6b237-151">Следующие значения могут быть возвращены в **структуре SPropProblemArray,** но не в качестве возвращаемой величины **для DoCopyProps.**</span><span class="sxs-lookup"><span data-stu-id="6b237-151">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyProps**.</span></span> <span data-ttu-id="6b237-152">Эти ошибки применимы к одному свойству.</span><span class="sxs-lookup"><span data-stu-id="6b237-152">These errors apply to a single property.</span></span>
  
<span data-ttu-id="6b237-153">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="6b237-153">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="6b237-154">Либо был MAPI_UNICODE флаг и **DoCopyProps** не поддерживает Юникод, либо MAPI_UNICODE не был установлен, а **DoCopyProps** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="6b237-154">Either the MAPI_UNICODE flag was set and **DoCopyProps** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="6b237-155">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="6b237-155">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="6b237-156">Свойство не может быть изменено вызываемой, так как оно является свойством только для чтения, вычисляется владельцем объекта назначения.</span><span class="sxs-lookup"><span data-stu-id="6b237-156">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="6b237-157">Эта ошибка не является серьезной; вызываемая должна разрешить продолжение операции копирования.</span><span class="sxs-lookup"><span data-stu-id="6b237-157">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="6b237-158">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="6b237-158">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="6b237-159">Тип свойства недействителен.</span><span class="sxs-lookup"><span data-stu-id="6b237-159">The property type is invalid.</span></span>
    
<span data-ttu-id="6b237-160">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="6b237-160">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="6b237-161">Тип свойства не тот тип, который ожидает вызываемого.</span><span class="sxs-lookup"><span data-stu-id="6b237-161">The property type is not the type that the caller expects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6b237-162">Примечания</span><span class="sxs-lookup"><span data-stu-id="6b237-162">Remarks</span></span>

<span data-ttu-id="6b237-163">Метод **IMAPISupport::D oCopyProps** реализован для объектов поддержки поставщиков сообщений.</span><span class="sxs-lookup"><span data-stu-id="6b237-163">The **IMAPISupport::DoCopyProps** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="6b237-164">Поставщики магазинов сообщений могут вызвать **DoCopyProps** для реализации метода [IMAPIProp::CopyProps](imapiprop-copyprops.md) для своих папок и сообщений.</span><span class="sxs-lookup"><span data-stu-id="6b237-164">Message store providers can call **DoCopyProps** to implement the [IMAPIProp::CopyProps](imapiprop-copyprops.md) method for their folders and messages.</span></span> <span data-ttu-id="6b237-165">**DoCopyProps** копирует или перемещает свойства, которые определены в массиве тегов свойств, на которые указывает  _lpIncludeProps_ и которые присутствуют в объекте, на который указывает  _lpSrcObj_.</span><span class="sxs-lookup"><span data-stu-id="6b237-165">**DoCopyProps** copies or moves the properties that are identified in the property tag array pointed to by  _lpIncludeProps_ and that are present in the object pointed to by  _lpSrcObj_.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6b237-166">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="6b237-166">Notes to callers</span></span>

<span data-ttu-id="6b237-167">При копировании свойств между объектами одного типа, например двумя сообщениями, параметры  _lpSrcInterface_ и  _lpDestInterface_ должны содержать один и тот же идентификатор интерфейса, а параметры  _lpSrcObj_ и  _lpDestObj_ должны указать на объекты одного типа.</span><span class="sxs-lookup"><span data-stu-id="6b237-167">When you copy properties between objects of the same type, such as two messages, the  _lpSrcInterface_ and  _lpDestInterface_ parameters must contain the same interface identifier, and the  _lpSrcObj_ and  _lpDestObj_ parameters must point to objects of the same type.</span></span> <span data-ttu-id="6b237-168">Если  _lpDestInterface_ задан nULL, **DoCopyProps** возвращает MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="6b237-168">If  _lpDestInterface_ is set to NULL, **DoCopyProps** returns MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="6b237-169">Если вы установите  _lpDestInterface_ в допустимый идентификатор интерфейса, но установите  _lpDestObj_ недействительным указателем, результаты непредсказуемы.</span><span class="sxs-lookup"><span data-stu-id="6b237-169">If you set  _lpDestInterface_ to an acceptable interface identifier, but set  _lpDestObj_ to an invalid pointer, the results are unpredictable.</span></span> <span data-ttu-id="6b237-170">Скорее всего, поставщик не справился с этой услугой.</span><span class="sxs-lookup"><span data-stu-id="6b237-170">Most likely your provider will fail.</span></span> 
  
<span data-ttu-id="6b237-171">Установите флаг MAPI_NOREPLACE, если вы не хотите, чтобы какие-либо свойства объекта назначения были перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="6b237-171">Set the MAPI_NOREPLACE flag if you do not want any of the properties in the destination object to be overwritten.</span></span> <span data-ttu-id="6b237-172">Свойства в объекте назначения, который существует в исходных объектах и не перезаписывается, не удаляются или не изменены.</span><span class="sxs-lookup"><span data-stu-id="6b237-172">Properties in the destination object that exist in the source object and are not overwritten are not deleted or modified.</span></span>
  
<span data-ttu-id="6b237-173">Чтобы скопировать список получателей **сообщения,** включаем свойство [PR_MESSAGE_RECIPIENTS (PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)в массив тегов свойств, на который указывает параметр _lpIncludeProps._</span><span class="sxs-lookup"><span data-stu-id="6b237-173">To copy a message's recipient list, include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array pointed to by the  _lpIncludeProps_ parameter.</span></span> <span data-ttu-id="6b237-174">Чтобы скопировать вложения сообщения, **включаем свойство** [PR_MESSAGE_ATTACHMENTS (PidTagMessageAttachments).](pidtagmessageattachments-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="6b237-174">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="6b237-175">Чтобы скопировать иерархию или таблицу содержимого контейнера папки или адресной **книги,** включите PR_CONTAINER_HIERARCHY [(PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)или **PR_CONTAINER_CONTENTS** [(PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)в массив тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="6b237-175">To copy a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag array.</span></span> <span data-ttu-id="6b237-176">Чтобы включить связанную таблицу содержимого папки, включайте **свойство PR_FOLDER_ASSOCIATED_CONTENTS** [(PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)в массиве.</span><span class="sxs-lookup"><span data-stu-id="6b237-176">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span>
  
<span data-ttu-id="6b237-177">Если подстановки копируется или перемещается, их содержимое копируется или перемещается в полном объеме, независимо от использования свойств, указанных структурой **SPropTagArray.**</span><span class="sxs-lookup"><span data-stu-id="6b237-177">If subfolders are copied or moved, their contents are copied or moved in their entirety, regardless of the use of properties indicated by the **SPropTagArray** structure.</span></span> 
  
 <span data-ttu-id="6b237-178">**DoCopyProps** сообщает о глобальных ошибках, которые происходят с операцией в целом, и отдельных ошибках, которые происходят с одним или более свойств.</span><span class="sxs-lookup"><span data-stu-id="6b237-178">**DoCopyProps** reports global errors that occur with the operation as a whole, and individual errors that occur with one or more of the properties.</span></span> <span data-ttu-id="6b237-179">Эти отдельные ошибки помещают в **структуру SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="6b237-179">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="6b237-180">Вы можете подавить отчет об ошибках на уровне свойств, передав параметру структуры массива проблем свойств NULL, а не допустимый указатель.</span><span class="sxs-lookup"><span data-stu-id="6b237-180">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="6b237-181">Если вы хотите получить сведения об ошибках, передай допустимый указатель **структуры SPropProblemArray** в _параметре lppProblems._</span><span class="sxs-lookup"><span data-stu-id="6b237-181">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="6b237-182">Когда **DoCopyProps** возвращает S_OK, проверьте возможные ошибки с отдельными свойствами в структуре.</span><span class="sxs-lookup"><span data-stu-id="6b237-182">When **DoCopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="6b237-183">Когда **DoCopyProps** возвращает ошибку, в **структуре SPropProblemArray** не возвращается информация.</span><span class="sxs-lookup"><span data-stu-id="6b237-183">When **DoCopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="6b237-184">Вместо этого вызовите [метод IMAPISupport::GetLastError,](imapisupport-getlasterror.md) чтобы получить подробные сведения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="6b237-184">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="6b237-185">Если **DoCopyProps** возвращает S_OK, освободите возвращенную структуру **SPropProblemArray,** позвонив в [функцию MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="6b237-185">If **DoCopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6b237-186">См. также</span><span class="sxs-lookup"><span data-stu-id="6b237-186">See also</span></span>



[<span data-ttu-id="6b237-187">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="6b237-187">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
  
[<span data-ttu-id="6b237-188">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="6b237-188">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="6b237-189">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="6b237-189">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="6b237-190">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="6b237-190">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="6b237-191">Каноническое свойство PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="6b237-191">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="6b237-192">Каноническое свойство PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="6b237-192">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="6b237-193">Каноническое свойство PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="6b237-193">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="6b237-194">Каноническое свойство PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="6b237-194">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="6b237-195">Каноническое свойство PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="6b237-195">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="6b237-196">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="6b237-196">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="6b237-197">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="6b237-197">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="6b237-198">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6b237-198">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

