---
title: IMAPIPropCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyProps
api_type:
- COM
ms.assetid: f65da1c8-d49b-44e8-8c66-9c53d088d334
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7319f1abb4a74ee17b0a4a1220215c29434d256b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345509"
---
# <a name="imapipropcopyprops"></a><span data-ttu-id="8bba6-103">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="8bba6-103">IMAPIProp::CopyProps</span></span>

  
  
<span data-ttu-id="8bba6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bba6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bba6-105">Копирует или перемещает выбранные свойства.</span><span class="sxs-lookup"><span data-stu-id="8bba6-105">Copies or moves selected properties.</span></span> 
  
```cpp
HRESULT CopyProps(
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="8bba6-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="8bba6-106">Parameters</span></span>

 <span data-ttu-id="8bba6-107">_lpIncludeProps_</span><span class="sxs-lookup"><span data-stu-id="8bba6-107">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="8bba6-108">[in] Указатель на массив тегов свойств, который указывает свойства для копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="8bba6-108">[in] A pointer to a property tag array that specifies the properties to copy or move.</span></span> <span data-ttu-id="8bba6-109">**PR_NULL** [(PidTagNull)](pidtagnull-canonical-property.md)не может быть включена в массив.</span><span class="sxs-lookup"><span data-stu-id="8bba6-109">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) cannot be included in the array.</span></span> <span data-ttu-id="8bba6-110">Параметр  _lpIncludeProps_ не может быть **null**.</span><span class="sxs-lookup"><span data-stu-id="8bba6-110">The  _lpIncludeProps_ parameter cannot be **null**.</span></span>
    
 <span data-ttu-id="8bba6-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="8bba6-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="8bba6-112">[in] Ручка родительского окна индикатора прогресса.</span><span class="sxs-lookup"><span data-stu-id="8bba6-112">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="8bba6-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="8bba6-113">_lpProgress_</span></span>
  
> <span data-ttu-id="8bba6-114">[in] Указатель на реализацию индикатора прогресса.</span><span class="sxs-lookup"><span data-stu-id="8bba6-114">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="8bba6-115">Если **null** передается в  _параметре lpProgress,_ индикатор прогресса отображается с помощью реализации MAPI.</span><span class="sxs-lookup"><span data-stu-id="8bba6-115">If **null** is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="8bba6-116">Параметр _lpProgress_ игнорируется, если флаг MAPI_DIALOG в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="8bba6-116">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="8bba6-117">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="8bba6-117">_lpInterface_</span></span>
  
> <span data-ttu-id="8bba6-118">[in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, который должен использоваться для доступа к объекту, на который указывает параметр _lpDestObj._</span><span class="sxs-lookup"><span data-stu-id="8bba6-118">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="8bba6-119">Параметр  _lpInterface_ не должен быть **null**.</span><span class="sxs-lookup"><span data-stu-id="8bba6-119">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="8bba6-120">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="8bba6-120">_lpDestObj_</span></span>
  
> <span data-ttu-id="8bba6-121">[in] Указатель на объект для получения скопированные или перенесенные свойства.</span><span class="sxs-lookup"><span data-stu-id="8bba6-121">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="8bba6-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8bba6-122">_ulFlags_</span></span>
  
> <span data-ttu-id="8bba6-123">[in] Битмашка флагов, которые контролируют операцию копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="8bba6-123">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="8bba6-124">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="8bba6-124">The following flags can be set:</span></span>
    
<span data-ttu-id="8bba6-125">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="8bba6-125">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="8bba6-126">Если **CopyProps** вызывает метод [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md) для обработки операции копирования или перемещения, вместо этого следует немедленно вернуться со значением MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="8bba6-126">If **CopyProps** calls the [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="8bba6-127">Флажок MAPI_DECLINE_OK mapi, чтобы ограничить повторную рекурсию.</span><span class="sxs-lookup"><span data-stu-id="8bba6-127">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="8bba6-128">Клиенты не устанавливают этот флаг.</span><span class="sxs-lookup"><span data-stu-id="8bba6-128">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="8bba6-129">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="8bba6-129">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="8bba6-130">Отображает индикатор прогресса.</span><span class="sxs-lookup"><span data-stu-id="8bba6-130">Displays a progress indicator.</span></span>
    
<span data-ttu-id="8bba6-131">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="8bba6-131">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="8bba6-132">**CopyProps** должна выполнять операцию перемещения вместо операции копирования.</span><span class="sxs-lookup"><span data-stu-id="8bba6-132">**CopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="8bba6-133">Если этот флаг не установлен, **CopyProps** выполняет операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="8bba6-133">When this flag is not set, **CopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="8bba6-134">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="8bba6-134">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="8bba6-135">Существующие свойства в объекте назначения не должны быть перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="8bba6-135">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="8bba6-136">Если этот флаг не установлен, **CopyProps** переопредирует существующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8bba6-136">When this flag is not set, **CopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="8bba6-137">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="8bba6-137">_lppProblems_</span></span>
  
> <span data-ttu-id="8bba6-138">[in, out] На входе указатель на указатель на [структуру SPropProblemArray;](spropproblemarray.md) в **противном случае null** указывает на отсутствие необходимости в сведениях об ошибках.</span><span class="sxs-lookup"><span data-stu-id="8bba6-138">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, **null**, indicating that there is no need for error information.</span></span> <span data-ttu-id="8bba6-139">Если  _lppProblems_ является допустимым указателем на входе, **CopyProps** возвращает подробные сведения об ошибках при копировании одного или более свойств.</span><span class="sxs-lookup"><span data-stu-id="8bba6-139">If  _lppProblems_ is a valid pointer on input, **CopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8bba6-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8bba6-140">Return value</span></span>

<span data-ttu-id="8bba6-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="8bba6-141">S_OK</span></span> 
  
> <span data-ttu-id="8bba6-142">Свойства успешно копировали или перемещали.</span><span class="sxs-lookup"><span data-stu-id="8bba6-142">Properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="8bba6-143">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="8bba6-143">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="8bba6-144">Субобъект не может быть скопирован, так как в объекте назначения уже существует субобъект с тем же именем отображения, определенным свойством **PR_DISPLAY_NAME** [(PidTagDisplayName).](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8bba6-144">A subobject cannot be copied because a subobject with the same display name, defined by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, already exists in the destination object.</span></span> 
    
<span data-ttu-id="8bba6-145">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="8bba6-145">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="8bba6-146">Поставщик услуг не реализует операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="8bba6-146">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="8bba6-147">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="8bba6-147">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="8bba6-148">Исходный объект, который выполняет операцию копирования или перемещения, прямо или косвенно содержит объект назначения.</span><span class="sxs-lookup"><span data-stu-id="8bba6-148">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="8bba6-149">Перед обнаружением этого условия, возможно, была выполнена значительная работа, поэтому объекты источника и назначения могут быть частично изменены.</span><span class="sxs-lookup"><span data-stu-id="8bba6-149">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="8bba6-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="8bba6-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="8bba6-151">Интерфейс, определенные параметром  _lpInterface,_ не поддерживается объектом назначения.</span><span class="sxs-lookup"><span data-stu-id="8bba6-151">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="8bba6-152">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8bba6-152">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="8bba6-153">Была предпринята попытка доступа к объекту, для которого у вызываемого недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="8bba6-153">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="8bba6-154">Эта ошибка возвращается, если объект назначения является таким же, как и исходный объект.</span><span class="sxs-lookup"><span data-stu-id="8bba6-154">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="8bba6-155">Следующие значения могут быть возвращены в **структуре SPropProblemArray,** но не в качестве возвращаемой **величины для CopyProps.**</span><span class="sxs-lookup"><span data-stu-id="8bba6-155">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyProps**.</span></span> <span data-ttu-id="8bba6-156">Эти ошибки применимы к одному свойству.</span><span class="sxs-lookup"><span data-stu-id="8bba6-156">These errors apply to a single property.</span></span>
  
<span data-ttu-id="8bba6-157">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="8bba6-157">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="8bba6-158">Либо флаг MAPI_UNICODE, а **CopyProps** не поддерживает Юникод, либо MAPI_UNICODE не установлен, а **CopyProps** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="8bba6-158">Either the MAPI_UNICODE flag was set and **CopyProps** does not support Unicode, or MAPI_UNICODE was not set and **CopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="8bba6-159">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="8bba6-159">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="8bba6-160">Свойство не может быть изменено вызываемой, так как оно является свойством только для чтения, вычисляется владельцем объекта назначения.</span><span class="sxs-lookup"><span data-stu-id="8bba6-160">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="8bba6-161">Эта ошибка не является серьезной; вызываемая должна разрешить продолжение операции копирования.</span><span class="sxs-lookup"><span data-stu-id="8bba6-161">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="8bba6-162">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="8bba6-162">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="8bba6-163">Тип свойства недействителен.</span><span class="sxs-lookup"><span data-stu-id="8bba6-163">The property type is invalid.</span></span>
    
<span data-ttu-id="8bba6-164">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="8bba6-164">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="8bba6-165">Тип свойства не является типом, ожидаемым вызываемой.</span><span class="sxs-lookup"><span data-stu-id="8bba6-165">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8bba6-166">Примечания</span><span class="sxs-lookup"><span data-stu-id="8bba6-166">Remarks</span></span>

<span data-ttu-id="8bba6-167">Метод **IMAPIProp::CopyProps** копирует или перемещает выбранные свойства из текущего объекта в объект назначения.</span><span class="sxs-lookup"><span data-stu-id="8bba6-167">The **IMAPIProp::CopyProps** method copies or moves selected properties from the current object to a destination object.</span></span> <span data-ttu-id="8bba6-168">**CopyProps** используется главным образом для ответа на сообщения и для их переададки, где только некоторые свойства исходного сообщения путешествуют с ответом или переададной копией.</span><span class="sxs-lookup"><span data-stu-id="8bba6-168">**CopyProps** is used mainly for replying to and forwarding messages, where only some of the properties from the original message travel with the reply or forwarded copy.</span></span> 
  
<span data-ttu-id="8bba6-169">Любые подобъекты в исходный объект автоматически включаются в операцию и копируются или перемещаются в полном объеме независимо от использования свойств, указанных структурой [SPropTagArray.](sproptagarray.md)</span><span class="sxs-lookup"><span data-stu-id="8bba6-169">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety, regardless of the use of properties indicated by the [SPropTagArray](sproptagarray.md) structure.</span></span> <span data-ttu-id="8bba6-170">По умолчанию **CopyProps** переописывает все свойства в объекте назначения, которые соответствуют свойствам из объекта-источника.</span><span class="sxs-lookup"><span data-stu-id="8bba6-170">By default, **CopyProps** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="8bba6-171">Если какие-либо из скопированные или перемещенные свойства уже существуют в объекте назначения, существующие свойства перезаписываются новыми свойствами, если флаг MAPI_NOREPLACE не задан в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="8bba6-171">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="8bba6-172">Существующая информация в объекте назначения, который не перезаписан, остается нетронутой.</span><span class="sxs-lookup"><span data-stu-id="8bba6-172">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8bba6-173">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="8bba6-173">Notes to implementers</span></span>

<span data-ttu-id="8bba6-174">Вы можете предоставить полную реализацию **CopyProps** или полагаться на реализацию, которую MAPI предоставляет в объекте поддержки.</span><span class="sxs-lookup"><span data-stu-id="8bba6-174">You can provide a full implementation of **CopyProps** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="8bba6-175">Если вы хотите использовать реализацию MAPI, вызовите **метод IMAPISupport::D oCopyProps.**</span><span class="sxs-lookup"><span data-stu-id="8bba6-175">If you want to use the MAPI implementation, call the **IMAPISupport::DoCopyProps** method.</span></span> <span data-ttu-id="8bba6-176">Однако, если вы делегируете обработку **в DoCopyProps** и вам будет передан флаг MAPI_DECLINE_OK, избеги вызова поддержки и MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="8bba6-176">However, if you do delegate processing to **DoCopyProps** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="8bba6-177">Вы будете вызваны с этим флагом MAPI, чтобы избежать возможного повторения, которое может произойти при копировании папок.</span><span class="sxs-lookup"><span data-stu-id="8bba6-177">You will be called with this flag by MAPI to avoid the possible recursion that can occur when you copy folders.</span></span> 
  
<span data-ttu-id="8bba6-178">Так как операция копирования может быть длительной, необходимо отобразить индикатор прогресса.</span><span class="sxs-lookup"><span data-stu-id="8bba6-178">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="8bba6-179">Используйте [реализацию IMAPIProgress,](imapiprogressiunknown.md) которая передается в  _параметре lpProgress,_ если она есть.</span><span class="sxs-lookup"><span data-stu-id="8bba6-179">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation that is passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="8bba6-180">Если  _lpProgress_ является **null,** позвоните в [метод IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) для использования реализации MAPI.</span><span class="sxs-lookup"><span data-stu-id="8bba6-180">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8bba6-181">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="8bba6-181">Notes to callers</span></span>

<span data-ttu-id="8bba6-182">Не установите флаг MAPI_DECLINE_OK; он используется MAPI в своих вызовах для реализации поставщика хранения сообщений **CopyProps.**</span><span class="sxs-lookup"><span data-stu-id="8bba6-182">Do not set the MAPI_DECLINE_OK flag; it is used by MAPI in its calls to message store provider **CopyProps** implementations.</span></span> 
  
<span data-ttu-id="8bba6-183">Поскольку операции копирования и перемещения могут занять время, целесообразно запросить отображение индикатора прогресса, установив MAPI_DIALOG флага.</span><span class="sxs-lookup"><span data-stu-id="8bba6-183">Because copy and move operations can take time, it is wise to request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="8bba6-184">Вы можете установить  _параметр lpProgress_ для реализации **IMAPIProgress,** если он у вас есть, или **null**.</span><span class="sxs-lookup"><span data-stu-id="8bba6-184">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="8bba6-185">Если  _lpProgress_ является **null,** **CopyProps** будет использовать индикатор прогресса по умолчанию, предоставляемый MAPI.</span><span class="sxs-lookup"><span data-stu-id="8bba6-185">If  _lpProgress_ is **null**, **CopyProps** will use the default progress indicator provided by MAPI.</span></span> 
  
<span data-ttu-id="8bba6-186">Вы можете подавить отображение индикатора прогресса, не установив MAPI_DIALOG флага.</span><span class="sxs-lookup"><span data-stu-id="8bba6-186">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="8bba6-187">**CopyProps** будет игнорировать  _параметры ulUIParam_ и  _lpProgress_ и избегать отображения индикатора.</span><span class="sxs-lookup"><span data-stu-id="8bba6-187">**CopyProps** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and avoid displaying the indicator.</span></span> 
  
 <span data-ttu-id="8bba6-188">**CopyProps** может сообщать о глобальных и отдельных ошибках или ошибках, которые возникают с одним или более свойств.</span><span class="sxs-lookup"><span data-stu-id="8bba6-188">**CopyProps** can report global and individual errors, or errors that occur with one or more of the properties.</span></span> <span data-ttu-id="8bba6-189">Эти отдельные ошибки помещают в **структуру SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="8bba6-189">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="8bba6-190">Вы можете подавить отчет об ошибках на уровне свойств, передав **null** вместо допустимого указателя для параметра структуры массива проблем свойств.</span><span class="sxs-lookup"><span data-stu-id="8bba6-190">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="8bba6-191">Если вы хотите получить сведения об ошибках, передай допустимый указатель **структуры SPropProblemArray** в _параметре lppProblems._</span><span class="sxs-lookup"><span data-stu-id="8bba6-191">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="8bba6-192">Когда **CopyProps** возвращает S_OK, проверьте возможные ошибки с отдельными свойствами в структуре.</span><span class="sxs-lookup"><span data-stu-id="8bba6-192">When **CopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="8bba6-193">Когда **CopyProps** возвращает ошибку, в **структуре SPropProblemArray** не возвращается информация.</span><span class="sxs-lookup"><span data-stu-id="8bba6-193">When **CopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="8bba6-194">Вместо этого вызовите [метод IMAPIProp::GetLastError,](imapiprop-getlasterror.md) чтобы получить подробные сведения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="8bba6-194">Instead, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="8bba6-195">Если **CopyProps** возвращает S_OK, освободите возвращенную структуру **SPropProblemArray,** позвонив в [функцию MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="8bba6-195">If **CopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="8bba6-196">Если вы копируете свойства, уникальные для типа исходных объектов, необходимо убедиться, что объект назначения имеет один и тот же тип.</span><span class="sxs-lookup"><span data-stu-id="8bba6-196">If you are copying properties that are unique to the source object type, you must make sure that the destination object is of the same type.</span></span> <span data-ttu-id="8bba6-197">**CopyProps** не мешает связывать свойства, которые обычно принадлежат одному типу объекта с другим типом объекта.</span><span class="sxs-lookup"><span data-stu-id="8bba6-197">**CopyProps** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="8bba6-198">Вам необходимо скопировать свойства, которые имеют смысл для объекта назначения.</span><span class="sxs-lookup"><span data-stu-id="8bba6-198">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="8bba6-199">Например, не следует копировать свойства сообщений в контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="8bba6-199">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="8bba6-200">Чтобы убедиться, что вы копируете объекты одного типа, убедитесь, что источник и объект назначения являются одним и тем же типом, сравнивая указатели объектов или вызывая метод [IUnknown::QueryInterface.](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bba6-200">To ensure that you are copying between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="8bba6-201">Установите идентификатор интерфейса, на который  _указывает lpInterface,_ в стандартный интерфейс для объекта-источника.</span><span class="sxs-lookup"><span data-stu-id="8bba6-201">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="8bba6-202">Кроме того, убедитесь, что **свойство типа или PR_OBJECT_TYPE** объекта [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)одинаково для этих двух объектов.</span><span class="sxs-lookup"><span data-stu-id="8bba6-202">Also, ensure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="8bba6-203">Например, если вы копируете сообщение, установите _lpInterface_ IID_IMessage  и PR_OBJECT_TYPE для обоих объектов MAPI_MESSAGE.</span><span class="sxs-lookup"><span data-stu-id="8bba6-203">For example, if you are copying from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="8bba6-204">Если недействительный указатель передается в  _параметре lpDestObj,_ результаты непредсказуемы.</span><span class="sxs-lookup"><span data-stu-id="8bba6-204">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="8bba6-205">Чтобы скопировать список получателей сообщения, вызывай метод **CopyProps** сообщения и **включив** свойство [PR_MESSAGE_RECIPIENTS (PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)в массив тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="8bba6-205">To copy a message's recipient list, call the message's **CopyProps** method and include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array.</span></span> <span data-ttu-id="8bba6-206">Чтобы скопировать вложения сообщения, **включаем свойство** [PR_MESSAGE_ATTACHMENTS (PidTagMessageAttachments).](pidtagmessageattachments-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="8bba6-206">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="8bba6-207">Чтобы скопировать иерархию или таблицу содержимого контейнера папки или адресной **книги,** включите свойства PR_CONTAINER_HIERARCHY [(PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)или **PR_CONTAINER_CONTENTS** [(PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)в массиве тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="8bba6-207">To copy a folder or address book container's hierarchy or contents table, include the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) properties in the property tag array.</span></span> <span data-ttu-id="8bba6-208">Чтобы включить связанную таблицу содержимого папки, включайте **свойство PR_FOLDER_ASSOCIATED_CONTENTS** [(PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)в массиве.</span><span class="sxs-lookup"><span data-stu-id="8bba6-208">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8bba6-209">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="8bba6-209">MFCMAPI reference</span></span>

<span data-ttu-id="8bba6-210">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="8bba6-210">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8bba6-211">**Файл**</span><span class="sxs-lookup"><span data-stu-id="8bba6-211">**File**</span></span>|<span data-ttu-id="8bba6-212">**Функция**</span><span class="sxs-lookup"><span data-stu-id="8bba6-212">**Function**</span></span>|<span data-ttu-id="8bba6-213">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="8bba6-213">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8bba6-214">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="8bba6-214">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="8bba6-215">CopyNamedProps</span><span class="sxs-lookup"><span data-stu-id="8bba6-215">CopyNamedProps</span></span>  <br/> |<span data-ttu-id="8bba6-216">MFCMAPI использует **метод IMAPIProp::CopyProps** для копирования именных свойств из одного сообщения в другое.</span><span class="sxs-lookup"><span data-stu-id="8bba6-216">MFCMAPI uses the **IMAPIProp::CopyProps** method to copy named properties from one message to another.</span></span>  <br/> |
|<span data-ttu-id="8bba6-217">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="8bba6-217">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="8bba6-218">CSingleMAPIPropListCtrl::OnPasteProperty</span><span class="sxs-lookup"><span data-stu-id="8bba6-218">CSingleMAPIPropListCtrl::OnPasteProperty</span></span>  <br/> |<span data-ttu-id="8bba6-219">MFCMAPI использует **метод IMAPIProp::CopyProps** для вклейки свойства, скопированные с другого объекта.</span><span class="sxs-lookup"><span data-stu-id="8bba6-219">MFCMAPI uses the **IMAPIProp::CopyProps** method to paste a property that has been copied from another object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8bba6-220">См. также</span><span class="sxs-lookup"><span data-stu-id="8bba6-220">See also</span></span>



[<span data-ttu-id="8bba6-221">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="8bba6-221">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="8bba6-222">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8bba6-222">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="8bba6-223">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="8bba6-223">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="8bba6-224">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="8bba6-224">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="8bba6-225">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="8bba6-225">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
  
[<span data-ttu-id="8bba6-226">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="8bba6-226">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="8bba6-227">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="8bba6-227">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="8bba6-228">Каноническое свойство PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="8bba6-228">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="8bba6-229">Каноническое свойство PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="8bba6-229">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="8bba6-230">Каноническое свойство PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="8bba6-230">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="8bba6-231">Каноническое свойство PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="8bba6-231">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="8bba6-232">Каноническое свойство PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="8bba6-232">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="8bba6-233">Каноническое свойство PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="8bba6-233">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="8bba6-234">Каноническое свойство PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="8bba6-234">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="8bba6-235">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="8bba6-235">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="8bba6-236">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="8bba6-236">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="8bba6-237">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8bba6-237">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="8bba6-238">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="8bba6-238">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

