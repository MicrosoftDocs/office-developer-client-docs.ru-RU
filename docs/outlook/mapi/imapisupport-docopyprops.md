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
# <a name="imapisupportdocopyprops"></a><span data-ttu-id="04ef4-103">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="04ef4-103">IMAPISupport::DoCopyProps</span></span>

  
  
<span data-ttu-id="04ef4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04ef4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04ef4-105">Копирует или перемещает одно или несколько свойств объекта в другой объект.</span><span class="sxs-lookup"><span data-stu-id="04ef4-105">Copies or moves one or more properties of an object to another object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="04ef4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="04ef4-106">Parameters</span></span>

 <span data-ttu-id="04ef4-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="04ef4-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="04ef4-108">[in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, который будет использоваться для доступа к объекту со свойствами, которые необходимо скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="04ef4-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object with the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="04ef4-109">_lpSrcObj_</span><span class="sxs-lookup"><span data-stu-id="04ef4-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="04ef4-110">[in] Указатель на объект, содержащий свойства для копирования или перемещений.</span><span class="sxs-lookup"><span data-stu-id="04ef4-110">[in] A pointer to the object that contains the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="04ef4-111">_lpIncludeProps_</span><span class="sxs-lookup"><span data-stu-id="04ef4-111">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="04ef4-112">[in] Указатель на структуру [SPropTagArray,](sproptagarray.md) которая содержит подсчетный массив тегов свойств, которые указывают свойства для копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="04ef4-112">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains a counted array of property tags that indicate the properties to copy or move.</span></span> <span data-ttu-id="04ef4-113">Параметр  _lpIncludeProps_ не может иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="04ef4-113">The  _lpIncludeProps_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="04ef4-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="04ef4-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="04ef4-115">[in] Handle to the parent window of the progress indicator.</span><span class="sxs-lookup"><span data-stu-id="04ef4-115">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="04ef4-116">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="04ef4-116">_lpProgress_</span></span>
  
> <span data-ttu-id="04ef4-117">[in] Указатель на реализацию индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="04ef4-117">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="04ef4-118">Если в параметре  _lpProgress_ передается NULL, индикатор хода выполнения отображается с помощью реализации MAPI.</span><span class="sxs-lookup"><span data-stu-id="04ef4-118">If NULL is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="04ef4-119">Параметр _lpProgress_ игнорируется, если MAPI_DIALOG флага в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="04ef4-119">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="04ef4-120">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="04ef4-120">_lpDestInterface_</span></span>
  
> <span data-ttu-id="04ef4-121">[in] Указатель на идентификатор интерфейса, который представляет интерфейс, используемый для доступа к объекту для получения скопированные или перемещенные свойства.</span><span class="sxs-lookup"><span data-stu-id="04ef4-121">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the properties that are copied or moved.</span></span>
    
 <span data-ttu-id="04ef4-122">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="04ef4-122">_lpDestObj_</span></span>
  
> <span data-ttu-id="04ef4-123">[in] Указатель на объект для получения скопированные или перемещенные свойства.</span><span class="sxs-lookup"><span data-stu-id="04ef4-123">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="04ef4-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="04ef4-124">_ulFlags_</span></span>
  
> <span data-ttu-id="04ef4-125">[in] Битоваяmas флагов, которая управляет выполнением операции копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="04ef4-125">[in] A bitmask of flags that controls how the copy or move operation is performed.</span></span> <span data-ttu-id="04ef4-126">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="04ef4-126">The following flags can be set:</span></span>
    
<span data-ttu-id="04ef4-127">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="04ef4-127">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="04ef4-128">Отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="04ef4-128">Displays a progress indicator.</span></span>
    
<span data-ttu-id="04ef4-129">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="04ef4-129">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="04ef4-130">**DoCopyProps** должен выполнять операцию перемещения вместо операции копирования.</span><span class="sxs-lookup"><span data-stu-id="04ef4-130">**DoCopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="04ef4-131">Если этот флаг не установлен, **DoCopyProps** выполняет операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="04ef4-131">When this flag is not set, **DoCopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="04ef4-132">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="04ef4-132">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="04ef4-133">Существующие свойства в объекте назначения не следует перезаписывать.</span><span class="sxs-lookup"><span data-stu-id="04ef4-133">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="04ef4-134">Если этот флаг не установлен, **DoCopyProps** переопредирует существующие свойства.</span><span class="sxs-lookup"><span data-stu-id="04ef4-134">When this flag is not set, **DoCopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="04ef4-135">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="04ef4-135">_lppProblems_</span></span>
  
> <span data-ttu-id="04ef4-136">[in, out] При вводе указатель на указатель на [структуру SPropProblemArray;](spropproblemarray.md) в противном случае NULL, что указывает на отсутствие необходимости в сведениях об ошибках.</span><span class="sxs-lookup"><span data-stu-id="04ef4-136">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="04ef4-137">Если  _lppProblems_ является допустимым указателем при вводе, **DoCopyProps** возвращает подробные сведения об ошибках при копировании одного или более свойств.</span><span class="sxs-lookup"><span data-stu-id="04ef4-137">If  _lppProblems_ is a valid pointer on input, **DoCopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="04ef4-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04ef4-138">Return value</span></span>

<span data-ttu-id="04ef4-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="04ef4-139">S_OK</span></span> 
  
> <span data-ttu-id="04ef4-140">Свойства были успешно скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="04ef4-140">Properties were successfully copied or moved.</span></span>
    
<span data-ttu-id="04ef4-141">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="04ef4-141">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="04ef4-142">Свойство, которое необходимо скопировать или сдвинуто, уже существует в объекте назначения, MAPI_NOREPLACE установлен флаг.</span><span class="sxs-lookup"><span data-stu-id="04ef4-142">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="04ef4-143">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="04ef4-143">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="04ef4-144">Исходный объект прямо или косвенно содержит объект назначения.</span><span class="sxs-lookup"><span data-stu-id="04ef4-144">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="04ef4-145">Перед обнаружением этого условия могли быть выполнены значительные трудоемкие работы, поэтому исходные и назначения объектов могут быть частично изменены.</span><span class="sxs-lookup"><span data-stu-id="04ef4-145">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="04ef4-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="04ef4-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="04ef4-147">Интерфейс, заданный параметром  _lpSrcInterface,_ не поддерживается исходным объектом, или интерфейс, заданный параметром  _lpDestInterface,_ не поддерживается объектом назначения.</span><span class="sxs-lookup"><span data-stu-id="04ef4-147">The interface identified by the  _lpSrcInterface_ parameter is not supported by the source object, or the interface identified by the  _lpDestInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="04ef4-148">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="04ef4-148">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="04ef4-149">Предпринята попытка доступа к объекту, у которого у вызываемого объекта недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="04ef4-149">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="04ef4-150">Эта ошибка возвращается, если объект назначения такой же, как и исходный объект.</span><span class="sxs-lookup"><span data-stu-id="04ef4-150">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="04ef4-151">Следующие значения могут быть возвращены в структуре **SPropProblemArray,** но не в качестве возвращаемой величины **для DoCopyProps.**</span><span class="sxs-lookup"><span data-stu-id="04ef4-151">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyProps**.</span></span> <span data-ttu-id="04ef4-152">Эти ошибки относятся к одному свойству.</span><span class="sxs-lookup"><span data-stu-id="04ef4-152">These errors apply to a single property.</span></span>
  
<span data-ttu-id="04ef4-153">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="04ef4-153">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="04ef4-154">Либо флаг MAPI_UNICODE установлен, а **DoCopyProps** не поддерживает Юникод, либо MAPI_UNICODE не установлен, и **DoCopyProps** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="04ef4-154">Either the MAPI_UNICODE flag was set and **DoCopyProps** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="04ef4-155">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="04ef4-155">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="04ef4-156">Вызываемая не может изменить свойство, так как это свойство, предназначенное только для чтения, вычисляется владельцем конечного объекта.</span><span class="sxs-lookup"><span data-stu-id="04ef4-156">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="04ef4-157">Эта ошибка не является серьезной; Вызываемая должна разрешить продолжение операции копирования.</span><span class="sxs-lookup"><span data-stu-id="04ef4-157">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="04ef4-158">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="04ef4-158">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="04ef4-159">Недопустимый тип свойства.</span><span class="sxs-lookup"><span data-stu-id="04ef4-159">The property type is invalid.</span></span>
    
<span data-ttu-id="04ef4-160">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="04ef4-160">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="04ef4-161">Тип свойства не является типом, который ожидает вызываемая.</span><span class="sxs-lookup"><span data-stu-id="04ef4-161">The property type is not the type that the caller expects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="04ef4-162">Примечания</span><span class="sxs-lookup"><span data-stu-id="04ef4-162">Remarks</span></span>

<span data-ttu-id="04ef4-163">Метод **IMAPISupport::D oCopyProps** реализован для объектов поддержки поставщика службы хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="04ef4-163">The **IMAPISupport::DoCopyProps** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="04ef4-164">Поставщики store сообщений могут вызывать **DoCopyProps** для реализации метода [IMAPIProp::CopyProps](imapiprop-copyprops.md) для своих папок и сообщений.</span><span class="sxs-lookup"><span data-stu-id="04ef4-164">Message store providers can call **DoCopyProps** to implement the [IMAPIProp::CopyProps](imapiprop-copyprops.md) method for their folders and messages.</span></span> <span data-ttu-id="04ef4-165">**DoCopyProps** копирует или перемещает свойства, которые определены в массиве тегов свойств, на которые указывает _lpIncludeProps_ и которые присутствуют в объекте, на который указывает _lpSrcObj._</span><span class="sxs-lookup"><span data-stu-id="04ef4-165">**DoCopyProps** copies or moves the properties that are identified in the property tag array pointed to by  _lpIncludeProps_ and that are present in the object pointed to by  _lpSrcObj_.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="04ef4-166">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="04ef4-166">Notes to callers</span></span>

<span data-ttu-id="04ef4-167">При копировании свойств между объектами одного типа, например двумя сообщениями,  _параметры lpSrcInterface_ и  _lpDestInterface_ должны содержать один и тот же идентификатор интерфейса, а  _параметры lpSrcObj_ и  _lpDestObj_ должны указать объекты одного типа.</span><span class="sxs-lookup"><span data-stu-id="04ef4-167">When you copy properties between objects of the same type, such as two messages, the  _lpSrcInterface_ and  _lpDestInterface_ parameters must contain the same interface identifier, and the  _lpSrcObj_ and  _lpDestObj_ parameters must point to objects of the same type.</span></span> <span data-ttu-id="04ef4-168">Если  _для lpDestInterface задано_ NULL, **DoCopyProps** возвращает MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="04ef4-168">If  _lpDestInterface_ is set to NULL, **DoCopyProps** returns MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="04ef4-169">Если для  _lpDestInterface задан_ допустимый идентификатор интерфейса, но для  _lpDestObj_ задан недопустимый указатель, результаты будут непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="04ef4-169">If you set  _lpDestInterface_ to an acceptable interface identifier, but set  _lpDestObj_ to an invalid pointer, the results are unpredictable.</span></span> <span data-ttu-id="04ef4-170">Скорее всего, поставщик не будет работать.</span><span class="sxs-lookup"><span data-stu-id="04ef4-170">Most likely your provider will fail.</span></span> 
  
<span data-ttu-id="04ef4-171">Установите флаг MAPI_NOREPLACE, если не нужно перезаписывать какие-либо свойства в объекте назначения.</span><span class="sxs-lookup"><span data-stu-id="04ef4-171">Set the MAPI_NOREPLACE flag if you do not want any of the properties in the destination object to be overwritten.</span></span> <span data-ttu-id="04ef4-172">Свойства в объекте назначения, которые существуют в объекте-источнике и не перезаписываются, не удаляются и не изменяются.</span><span class="sxs-lookup"><span data-stu-id="04ef4-172">Properties in the destination object that exist in the source object and are not overwritten are not deleted or modified.</span></span>
  
<span data-ttu-id="04ef4-173">Чтобы скопировать список получателей сообщения, включаем свойство **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)в массив тегов свойств, на который указывает параметр _lpIncludeProps._</span><span class="sxs-lookup"><span data-stu-id="04ef4-173">To copy a message's recipient list, include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array pointed to by the  _lpIncludeProps_ parameter.</span></span> <span data-ttu-id="04ef4-174">Чтобы скопировать вложения сообщения, **включаем свойство PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments).](pidtagmessageattachments-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="04ef4-174">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="04ef4-175">Чтобы скопировать иерархию или таблицу содержимого контейнера папки или адресной книги, включите **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)или **PR_CONTAINER_CONTENTS** ([PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)в массив тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="04ef4-175">To copy a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag array.</span></span> <span data-ttu-id="04ef4-176">Чтобы включить связанную с папкой таблицу содержимого, включайте **свойство PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)в массив.</span><span class="sxs-lookup"><span data-stu-id="04ef4-176">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span>
  
<span data-ttu-id="04ef4-177">Если вупапки копируется или перемещается, их содержимое копируется или перемещается полностью независимо от использования свойств, указанных в **структуре SPropTagArray.**</span><span class="sxs-lookup"><span data-stu-id="04ef4-177">If subfolders are copied or moved, their contents are copied or moved in their entirety, regardless of the use of properties indicated by the **SPropTagArray** structure.</span></span> 
  
 <span data-ttu-id="04ef4-178">**DoCopyProps** сообщает о глобальных ошибках, которые возникают с помощью операции в целом, и отдельных ошибках, которые возникают с одним или более свойствами.</span><span class="sxs-lookup"><span data-stu-id="04ef4-178">**DoCopyProps** reports global errors that occur with the operation as a whole, and individual errors that occur with one or more of the properties.</span></span> <span data-ttu-id="04ef4-179">Эти отдельные ошибки помещаются в структуру **SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="04ef4-179">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="04ef4-180">Отчеты об ошибках можно подавить на уровне свойства, передав NULL вместо допустимого указателя для параметра структуры массива проблем свойств.</span><span class="sxs-lookup"><span data-stu-id="04ef4-180">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="04ef4-181">Если вы хотите получить сведения об ошибках, передав допустимый указатель структуры **SPropProblemArray** в _параметре lppProblems._</span><span class="sxs-lookup"><span data-stu-id="04ef4-181">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="04ef4-182">Когда **DoCopyProps** возвращает S_OK, проверьте возможные ошибки с отдельными свойствами в структуре.</span><span class="sxs-lookup"><span data-stu-id="04ef4-182">When **DoCopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="04ef4-183">Когда **DoCopyProps** возвращает ошибку, данные в структуре **SPropProblemArray** не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="04ef4-183">When **DoCopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="04ef4-184">Вместо этого вызовите метод [IMAPISupport::GetLastError,](imapisupport-getlasterror.md) чтобы получить подробные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="04ef4-184">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="04ef4-185">Если **DoCopyProps** возвращает S_OK, освободите возвращенную **структуру SPropProblemArray,** вызывая функцию [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="04ef4-185">If **DoCopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="04ef4-186">См. также</span><span class="sxs-lookup"><span data-stu-id="04ef4-186">See also</span></span>



[<span data-ttu-id="04ef4-187">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="04ef4-187">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
  
[<span data-ttu-id="04ef4-188">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="04ef4-188">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="04ef4-189">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="04ef4-189">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="04ef4-190">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="04ef4-190">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="04ef4-191">Каноническое свойство PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="04ef4-191">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="04ef4-192">Каноническое свойство PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="04ef4-192">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="04ef4-193">Каноническое свойство PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="04ef4-193">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="04ef4-194">Каноническое свойство PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="04ef4-194">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="04ef4-195">Каноническое свойство PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="04ef4-195">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="04ef4-196">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="04ef4-196">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="04ef4-197">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="04ef4-197">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="04ef4-198">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="04ef4-198">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

