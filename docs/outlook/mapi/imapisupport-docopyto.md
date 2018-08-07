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
ms.openlocfilehash: 1040a0730c4b26b51d3c2b7763488502b2c5323c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809131"
---
# <a name="imapisupportdocopyto"></a><span data-ttu-id="4e088-103">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="4e088-103">IMAPISupport::DoCopyTo</span></span>

  
  
<span data-ttu-id="4e088-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4e088-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4e088-105">Копирование или перемещение всех свойств одного объекта, за исключением специально исключенные свойства на другой объект.</span><span class="sxs-lookup"><span data-stu-id="4e088-105">Copies or moves all properties of one object, except for specifically excluded properties, to another object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="4e088-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e088-106">Parameters</span></span>

 <span data-ttu-id="4e088-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="4e088-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="4e088-108">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к объекту, который имеет свойства, которые нужно скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="4e088-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="4e088-109">_lpSrcObj_</span><span class="sxs-lookup"><span data-stu-id="4e088-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="4e088-110">[in] Указатель на объект, который содержит свойства, которые нужно скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="4e088-110">[in] A pointer to the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="4e088-111">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="4e088-111">_ciidExclude_</span></span>
  
> <span data-ttu-id="4e088-112">[in] Число интерфейсов следует исключить при скопируйте или переместите свойства.</span><span class="sxs-lookup"><span data-stu-id="4e088-112">[in] The count of interfaces to exclude when you copy or move properties.</span></span>
    
 <span data-ttu-id="4e088-113">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="4e088-113">_rgiidExclude_</span></span>
  
> <span data-ttu-id="4e088-114">[in] Массив идентификаторов интерфейса, которое указывает, интерфейсы, которые не должны использоваться при скопируйте или переместите дополнительную информацию в целевой объект.</span><span class="sxs-lookup"><span data-stu-id="4e088-114">[in] An array of interface identifiers that indicates interfaces that should not be used when you copy or move supplemental information to the destination object.</span></span>
    
 <span data-ttu-id="4e088-115">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="4e088-115">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="4e088-116">[in] Указатель в массив тег свойства, который определяет свойство теги, которые следует исключить из копии или операции перемещения.</span><span class="sxs-lookup"><span data-stu-id="4e088-116">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="4e088-117">Указать значение NULL для параметра _lpExcludeProps_ указывает, что все свойства объекта следует скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="4e088-117">Passing NULL in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="4e088-118">**DoCopyTo** возвращает MAPI_E_INVALID_PARAMETER при член **cValues** структуры [SPropTagArray](sproptagarray.md) указывает _lpExcludeProps_ имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="4e088-118">**DoCopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="4e088-119">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="4e088-119">_ulUIParam_</span></span>
  
> <span data-ttu-id="4e088-120">[in] Дескриптор родительского окна индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="4e088-120">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="4e088-121">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="4e088-121">_lpProgress_</span></span>
  
> <span data-ttu-id="4e088-122">[in] Указатель на реализацию индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="4e088-122">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="4e088-123">Если значение NULL передается в параметре _lpProgress_ , MAPI предоставляет реализацию хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="4e088-123">If NULL is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="4e088-124">Параметр _lpProgress_ игнорируется, пока флаг MAPI_DIALOG будет выполнен с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="4e088-124">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="4e088-125">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="4e088-125">_lpDestInterface_</span></span>
  
> <span data-ttu-id="4e088-126">[in] Указатель на интерфейс идентификатор, который представляет интерфейс, который будет использоваться для доступа к объекту для получения свойства копируемые или перемещения.</span><span class="sxs-lookup"><span data-stu-id="4e088-126">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="4e088-127">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="4e088-127">_lpDestObj_</span></span>
  
> <span data-ttu-id="4e088-128">[in] Указатель на объект для получения свойств копируемые или перемещения.</span><span class="sxs-lookup"><span data-stu-id="4e088-128">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="4e088-129">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4e088-129">_ulFlags_</span></span>
  
> <span data-ttu-id="4e088-130">[in] Битовая маска флаги, который определяет операцию копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="4e088-130">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="4e088-131">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="4e088-131">The following flags can be set:</span></span>
    
<span data-ttu-id="4e088-132">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="4e088-132">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="4e088-133">Отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="4e088-133">Displays a progress indicator.</span></span> 
    
<span data-ttu-id="4e088-134">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="4e088-134">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="4e088-135">**DoCopyTo** следует выполнять операции перемещения вместо операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="4e088-135">**DoCopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="4e088-136">Если этот флаг не задан, **DoCopyTo** выполняет операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="4e088-136">When this flag is not set, **DoCopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="4e088-137">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="4e088-137">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="4e088-138">Не следует перезаписывать существующие свойства в целевой объект.</span><span class="sxs-lookup"><span data-stu-id="4e088-138">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="4e088-139">Если этот флаг не задан, **DoCopyTo** перезаписывает существующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4e088-139">When this flag is not set, **DoCopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="4e088-140">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="4e088-140">_lppProblems_</span></span>
  
> <span data-ttu-id="4e088-141">[out] На входе указатель указатель на структуру [SPropProblemArray](spropproblemarray.md) ; в противном случае — значение NULL, указывает, не требуется выполнять сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="4e088-141">[out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="4e088-142">Если _lppProblems_ допустимый указатель на входные данные, **DoCopyTo** возвращает подробные сведения об ошибках в копирование одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="4e088-142">If  _lppProblems_ is a valid pointer on input, **DoCopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4e088-143">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="4e088-143">Return value</span></span>

<span data-ttu-id="4e088-144">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="4e088-144">S_OK</span></span> 
  
> <span data-ttu-id="4e088-145">Свойства успешно копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="4e088-145">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="4e088-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="4e088-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="4e088-147">Свойство так, чтобы скопировать или переместить уже существует в целевой объект и флаг MAPI_NOREPLACE.</span><span class="sxs-lookup"><span data-stu-id="4e088-147">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="4e088-148">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="4e088-148">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="4e088-149">Исходный объект прямо или косвенно содержит целевой объект.</span><span class="sxs-lookup"><span data-stu-id="4e088-149">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="4e088-150">Важные может быть выполнено перед был обнаружен это условие, поэтому исходный и целевой объекты частично могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="4e088-150">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="4e088-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="4e088-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="4e088-152">Интерфейс, определенного параметром _lpSrcInterface_ не поддерживается объектом, на который указывает _lpSrcObj_или интерфейса, определенного параметром _lpDestInterface_ не поддерживается объектом, на который указывает _lpDestObj _.</span><span class="sxs-lookup"><span data-stu-id="4e088-152">The interface identified by the  _lpSrcInterface_ parameter is not supported by the object pointed to by  _lpSrcObj_, or the interface identified by the  _lpDestInterface_ parameter is not supported by the object pointed to by  _lpDestObj_.</span></span> 
    
<span data-ttu-id="4e088-153">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="4e088-153">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="4e088-154">Предпринята попытка получить доступ к объекту, для которого вызывающий не имеет разрешений.</span><span class="sxs-lookup"><span data-stu-id="4e088-154">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="4e088-155">Эта ошибка возвращается в том случае, если в целевой объект совпадает с исходным объектом.</span><span class="sxs-lookup"><span data-stu-id="4e088-155">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="4e088-156">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4e088-156">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="4e088-157">Параметр _lpSrcInterface_ имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="4e088-157">The  _lpSrcInterface_ parameter is NULL.</span></span> 
    
<span data-ttu-id="4e088-158">Возможные значения могут быть возвращены в структуре **SPropProblemArray** , но не как возвращаемые значения для **DoCopyTo**.</span><span class="sxs-lookup"><span data-stu-id="4e088-158">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyTo**.</span></span> <span data-ttu-id="4e088-159">Эти ошибки относятся к одному свойству.</span><span class="sxs-lookup"><span data-stu-id="4e088-159">These errors apply to a single property.</span></span>
  
<span data-ttu-id="4e088-160">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="4e088-160">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="4e088-161">Либо был установлен флажок MAPI_UNICODE и **DoCopyTo** не поддерживает Юникод, или MAPI_UNICODE не было установлено и **DoCopyTo** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="4e088-161">Either the MAPI_UNICODE flag was set and **DoCopyTo** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="4e088-162">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="4e088-162">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="4e088-163">Невозможно изменить свойство вызывающим абонентом, так как он является свойством только для чтения, вычисленный владельцем конечного объекта.</span><span class="sxs-lookup"><span data-stu-id="4e088-163">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="4e088-164">Эта ошибка не является очень неблагоприятных; вызывающего абонента, должна поддерживать операции копирования для продолжения.</span><span class="sxs-lookup"><span data-stu-id="4e088-164">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="4e088-165">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="4e088-165">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="4e088-166">Недопустимый тип свойства.</span><span class="sxs-lookup"><span data-stu-id="4e088-166">The property type is invalid.</span></span>
    
<span data-ttu-id="4e088-167">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="4e088-167">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="4e088-168">Тип свойства не типа, вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="4e088-168">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4e088-169">Замечания</span><span class="sxs-lookup"><span data-stu-id="4e088-169">Remarks</span></span>

<span data-ttu-id="4e088-170">Метод **IMAPISupport::DoCopyTo** реализуется для объектов поддержки поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="4e088-170">The **IMAPISupport::DoCopyTo** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="4e088-171">Поставщики хранилища сообщений можно вызвать **DoCopyTo** , чтобы реализовать метод [IMAPIProp::CopyTo](imapiprop-copyto.md) для своих папок и сообщений.</span><span class="sxs-lookup"><span data-stu-id="4e088-171">Message store providers can call **DoCopyTo** to implement the [IMAPIProp::CopyTo](imapiprop-copyto.md) method for their folders and messages.</span></span> 
  
<span data-ttu-id="4e088-172">По умолчанию **DoCopyTo** копирует или переносит все свойства одного объекта на другой объект.</span><span class="sxs-lookup"><span data-stu-id="4e088-172">By default, **DoCopyTo** copies or moves all of the properties of one object to another object.</span></span> <span data-ttu-id="4e088-173">Вложенными объектами в объекте источника автоматически включены в операции и скопировать или переместить полностью.</span><span class="sxs-lookup"><span data-stu-id="4e088-173">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety.</span></span> 
  
<span data-ttu-id="4e088-174">Если какие-либо свойства скопированной или перемещенной уже существует в целевом объекте, существующие свойства перезаписываются новых свойств, пока флаг MAPI_NOREPLACE будет выполнен с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="4e088-174">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="4e088-175">Существующие данные в целевой объект, который не перезаписывается остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="4e088-175">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4e088-176">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="4e088-176">Notes to callers</span></span>

<span data-ttu-id="4e088-177">Чтобы исключить свойства из копии или операции перемещения, включают теги их свойства с помощью параметра _lpExcludeProps_ .</span><span class="sxs-lookup"><span data-stu-id="4e088-177">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="4e088-178">При передаче результатов с помощью макроса [PROP_TAG](prop_tag.md) для построения тега свойства из указанный идентификатор в массиве тега свойства будут исключены все свойства с этим идентификатором.</span><span class="sxs-lookup"><span data-stu-id="4e088-178">If you pass the results of using the [PROP_TAG](prop_tag.md) macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="4e088-179">Например следующую запись в массиве тега свойства вызывает все свойства с идентификатором 0x8002, чтобы исключить, независимо от типа:</span><span class="sxs-lookup"><span data-stu-id="4e088-179">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="4e088-180">Чтобы предотвратить копирование время доставки сообщений, при копировании сообщения в другую папку, укажите **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) в массиве свойство tag исключить.</span><span class="sxs-lookup"><span data-stu-id="4e088-180">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="4e088-181">Чтобы исключить список получателей сообщения, добавьте свойство **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) в массиве исключить.</span><span class="sxs-lookup"><span data-stu-id="4e088-181">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="4e088-182">Чтобы исключить вложений сообщений, добавьте свойство **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) в массиве.</span><span class="sxs-lookup"><span data-stu-id="4e088-182">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="4e088-183">Аналогичным образом чтобы предотвратить копирование или перемещение папки или иерархии контейнер адресной книги или таблицу содержимого, включите **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) или **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) в свойстве тег исключить массива.</span><span class="sxs-lookup"><span data-stu-id="4e088-183">Similarly, to prevent the copying or moving of a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="4e088-184">Пропуск MAPI_E_COMPUTED ошибок, возвращаемых в структуре **SPropProblemArray** в параметре _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="4e088-184">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
<span data-ttu-id="4e088-185">Идентификатор, который _lpSrcInterface_ моменты, которые обычно является то же, что идентификатор интерфейса, указывающего _lpDestInterface_ .</span><span class="sxs-lookup"><span data-stu-id="4e088-185">The interface identifier that  _lpSrcInterface_ points to is usually the same as the interface identifier that  _lpDestInterface_ points to.</span></span> 
  
<span data-ttu-id="4e088-186">Если передать идентификатор приемлемой интерфейса в _lpDestInterface_ , но недопустимый указатель в _lpDestObj_результаты непредсказуемы.</span><span class="sxs-lookup"><span data-stu-id="4e088-186">If you pass an acceptable interface identifier in  _lpDestInterface_ but an invalid pointer in  _lpDestObj_, the results are unpredictable.</span></span> <span data-ttu-id="4e088-187">Вероятнее всего это приведет к поставщику могут быть.</span><span class="sxs-lookup"><span data-stu-id="4e088-187">Most likely this will cause your provider to fail.</span></span> 
  
<span data-ttu-id="4e088-188">С другой стороны Если принять во внимание дополнительную информацию, которая не должна быть скопированы или перемещены, добавьте идентификаторы интерфейса для интерфейсов исключить в массиве, переданной в параметре _rgiidExclude_ .</span><span class="sxs-lookup"><span data-stu-id="4e088-188">Conversely, if you are aware of supplemental information that should not be copied or moved, add the interface identifiers for the interfaces to be excluded in the array passed in the  _rgiidExclude_ parameter.</span></span> <span data-ttu-id="4e088-189">Например при копировании сообщения, но не какие-либо из их вложений сообщений передайте IID_IMessage в массиве _rgiidExclude_ .</span><span class="sxs-lookup"><span data-stu-id="4e088-189">For example, if you are copying messages, but not any of their message attachments, pass IID_IMessage in the  _rgiidExclude_ array.</span></span> <span data-ttu-id="4e088-190">**DoCopyTo** игнорирует любые интерфейсов, перечисленных в _rgiidExclude_ , который не распознается.</span><span class="sxs-lookup"><span data-stu-id="4e088-190">**DoCopyTo** ignores any interfaces listed in  _rgiidExclude_ that it does not recognize.</span></span> 
  
<span data-ttu-id="4e088-191">Если используется параметр _rgiidExclude_ следует исключить интерфейс также исключаются все интерфейсы, производные от этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4e088-191">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="4e088-192">К примеру за исключением интерфейса [IMAPIContainer](imapicontainerimapiprop.md) включен, папки или контейнеров адресной книги для исключения, в зависимости от типа поставщика.</span><span class="sxs-lookup"><span data-stu-id="4e088-192">For example, excluding the [IMAPIContainer](imapicontainerimapiprop.md) interface causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="4e088-193">Не исключить [IMAPIProp](imapipropiunknown.md) или [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) из-за слишком большом числе интерфейсы производные от них.</span><span class="sxs-lookup"><span data-stu-id="4e088-193">Do not exclude [IMAPIProp](imapipropiunknown.md) or [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) because so many interfaces derive from them.</span></span> 
  
 <span data-ttu-id="4e088-194">**DoCopyTo** отчетов глобальной ошибки, которые применяются к операции в целом и отдельных ошибок, которые применяются для отдельных свойств.</span><span class="sxs-lookup"><span data-stu-id="4e088-194">**DoCopyTo** reports global errors that apply to the operation as a whole, and individual errors that apply to individual properties.</span></span> <span data-ttu-id="4e088-195">Эти отдельные ошибки помещаются в структуре **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="4e088-195">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="4e088-196">Отчеты на уровне свойств, передав значение NULL, а не является допустимым указателем, для параметра свойство массива проблема структура об ошибках, можно отключить.</span><span class="sxs-lookup"><span data-stu-id="4e088-196">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="4e088-197">Если вы хотите получать сведения об ошибках, передайте допустимый указатель структура **SPropProblemArray** с помощью параметра _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="4e088-197">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="4e088-198">При **DoCopyTo** возвращает значение S_OK, проверьте наличие возможных ошибок с помощью отдельных свойств в структуре.</span><span class="sxs-lookup"><span data-stu-id="4e088-198">When **DoCopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="4e088-199">Когда **DoCopyTo** возвращает ошибку, не информация возвращается в структуре **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="4e088-199">When **DoCopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="4e088-200">Вместо этого вызовите метод [IMAPISupport::GetLastError](imapisupport-getlasterror.md) , чтобы получить подробные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="4e088-200">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="4e088-201">Если **DoCopyTo** возвращает значение S_OK, освободите возвращенные структура **SPropProblemArray** путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="4e088-201">If **DoCopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="4e088-202">Если глобальные ошибка возникает при вызове **DoCopyTo** , не используйте или Бесплатная загрузка структуры **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="4e088-202">If a global error occurs on the **DoCopyTo** call, do not use or free the **SPropProblemArray** structure.</span></span> <span data-ttu-id="4e088-203">Поставщики следует игнорировать член _ulIndex_ в **SPropProblemArray** структуры, возвращаемые **DoCopyTo**.</span><span class="sxs-lookup"><span data-stu-id="4e088-203">Providers should ignore the  _ulIndex_ member in **SPropProblemArray** structures returned by **DoCopyTo**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4e088-204">См. также</span><span class="sxs-lookup"><span data-stu-id="4e088-204">See also</span></span>



[<span data-ttu-id="4e088-205">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="4e088-205">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="4e088-206">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="4e088-206">IMAPISupport::CopyFolder</span></span>](imapisupport-copyfolder.md)
  
[<span data-ttu-id="4e088-207">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="4e088-207">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="4e088-208">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="4e088-208">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="4e088-209">Каноническое свойство PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="4e088-209">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="4e088-210">Каноническое свойство PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="4e088-210">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="4e088-211">Каноническое свойство PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="4e088-211">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="4e088-212">Каноническое свойство PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="4e088-212">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="4e088-213">Каноническое свойство PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="4e088-213">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="4e088-214">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="4e088-214">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="4e088-215">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="4e088-215">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="4e088-216">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4e088-216">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

