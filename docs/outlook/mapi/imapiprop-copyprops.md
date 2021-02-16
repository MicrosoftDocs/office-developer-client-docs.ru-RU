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
# <a name="imapipropcopyprops"></a><span data-ttu-id="1446c-103">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="1446c-103">IMAPIProp::CopyProps</span></span>

  
  
<span data-ttu-id="1446c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1446c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1446c-105">Копирует или перемещает выбранные свойства.</span><span class="sxs-lookup"><span data-stu-id="1446c-105">Copies or moves selected properties.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="1446c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1446c-106">Parameters</span></span>

 <span data-ttu-id="1446c-107">_lpIncludeProps_</span><span class="sxs-lookup"><span data-stu-id="1446c-107">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="1446c-108">[in] Указатель на массив тегов свойств, который указывает свойства для копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="1446c-108">[in] A pointer to a property tag array that specifies the properties to copy or move.</span></span> <span data-ttu-id="1446c-109">**PR_NULL** ([PidTagNull)](pidtagnull-canonical-property.md)не могут быть включены в массив.</span><span class="sxs-lookup"><span data-stu-id="1446c-109">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) cannot be included in the array.</span></span> <span data-ttu-id="1446c-110">Параметр _lpIncludeProps_ не может иметь **null.**</span><span class="sxs-lookup"><span data-stu-id="1446c-110">The  _lpIncludeProps_ parameter cannot be **null**.</span></span>
    
 <span data-ttu-id="1446c-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1446c-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="1446c-112">[in] Handle to the parent window of the progress indicator.</span><span class="sxs-lookup"><span data-stu-id="1446c-112">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="1446c-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="1446c-113">_lpProgress_</span></span>
  
> <span data-ttu-id="1446c-114">[in] Указатель на реализацию индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="1446c-114">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="1446c-115">Если **в параметре**  _lpProgress_ передается null, индикатор хода выполнения отображается с помощью реализации MAPI.</span><span class="sxs-lookup"><span data-stu-id="1446c-115">If **null** is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="1446c-116">Параметр _lpProgress_ игнорируется, если MAPI_DIALOG флага в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="1446c-116">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="1446c-117">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="1446c-117">_lpInterface_</span></span>
  
> <span data-ttu-id="1446c-118">[in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, который должен использоваться для доступа к объекту, на который указывает параметр _lpDestObj._</span><span class="sxs-lookup"><span data-stu-id="1446c-118">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="1446c-119">Параметр _lpInterface_ не должен иметь **null.**</span><span class="sxs-lookup"><span data-stu-id="1446c-119">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="1446c-120">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="1446c-120">_lpDestObj_</span></span>
  
> <span data-ttu-id="1446c-121">[in] Указатель на объект для получения скопированные или перемещенные свойства.</span><span class="sxs-lookup"><span data-stu-id="1446c-121">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="1446c-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1446c-122">_ulFlags_</span></span>
  
> <span data-ttu-id="1446c-123">[in] Битоваяmas флагов, которая управляет операцией копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="1446c-123">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="1446c-124">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="1446c-124">The following flags can be set:</span></span>
    
<span data-ttu-id="1446c-125">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="1446c-125">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="1446c-126">Если **CopyProps** вызывает метод [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md) для обработки операции копирования или перемещения, он должен возвращаться немедленно со значением MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="1446c-126">If **CopyProps** calls the [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="1446c-127">MapI MAPI_DECLINE_OK флага для ограничения рекурсии.</span><span class="sxs-lookup"><span data-stu-id="1446c-127">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="1446c-128">Клиенты не устанавливают этот флаг.</span><span class="sxs-lookup"><span data-stu-id="1446c-128">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="1446c-129">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="1446c-129">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="1446c-130">Отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="1446c-130">Displays a progress indicator.</span></span>
    
<span data-ttu-id="1446c-131">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="1446c-131">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="1446c-132">**CopyProps** следует выполнить операцию перемещения вместо операции копирования.</span><span class="sxs-lookup"><span data-stu-id="1446c-132">**CopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="1446c-133">Если этот флаг не установлен, **CopyProps** выполняет операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="1446c-133">When this flag is not set, **CopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="1446c-134">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="1446c-134">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="1446c-135">Существующие свойства в объекте назначения не следует перезаписывать.</span><span class="sxs-lookup"><span data-stu-id="1446c-135">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="1446c-136">Если этот флаг не установлен, **CopyProps** переопредирует существующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1446c-136">When this flag is not set, **CopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="1446c-137">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="1446c-137">_lppProblems_</span></span>
  
> <span data-ttu-id="1446c-138">[in, out] При вводе указатель на указатель на [структуру SPropProblemArray;](spropproblemarray.md) в **противном случае — null,** указывающее на отсутствие необходимости в сведениях об ошибках.</span><span class="sxs-lookup"><span data-stu-id="1446c-138">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, **null**, indicating that there is no need for error information.</span></span> <span data-ttu-id="1446c-139">Если  _lppProblems_ является допустимым указателем при вводе, **CopyProps** возвращает подробные сведения об ошибках при копировании одного или более свойств.</span><span class="sxs-lookup"><span data-stu-id="1446c-139">If  _lppProblems_ is a valid pointer on input, **CopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1446c-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1446c-140">Return value</span></span>

<span data-ttu-id="1446c-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="1446c-141">S_OK</span></span> 
  
> <span data-ttu-id="1446c-142">Свойства успешно скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="1446c-142">Properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="1446c-143">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="1446c-143">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="1446c-144">Подобект нельзя скопировать, так как в объекте назначения уже существует подпроект с таким же отображаемым именем, определенным свойством **PR_DISPLAY_NAME** ([PidTagDisplayName).](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1446c-144">A subobject cannot be copied because a subobject with the same display name, defined by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, already exists in the destination object.</span></span> 
    
<span data-ttu-id="1446c-145">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="1446c-145">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="1446c-146">Поставщик услуг не реализует операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="1446c-146">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="1446c-147">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="1446c-147">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="1446c-148">Исходный объект, который выполняет операцию копирования или перемещения прямо или косвенно, содержит объект назначения.</span><span class="sxs-lookup"><span data-stu-id="1446c-148">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="1446c-149">Перед обнаружением этого условия могли быть выполнены значительные трудоемкие работы, поэтому исходные и назначения объектов могут быть частично изменены.</span><span class="sxs-lookup"><span data-stu-id="1446c-149">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="1446c-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="1446c-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="1446c-151">Интерфейс, заданный  _параметром lpInterface,_ не поддерживается объектом назначения.</span><span class="sxs-lookup"><span data-stu-id="1446c-151">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="1446c-152">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="1446c-152">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="1446c-153">Предпринята попытка доступа к объекту, у которого у вызываемого объекта недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="1446c-153">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="1446c-154">Эта ошибка возвращается, если объект назначения такой же, как и исходный объект.</span><span class="sxs-lookup"><span data-stu-id="1446c-154">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="1446c-155">Следующие значения могут быть возвращены в структуре **SPropProblemArray,** но не в качестве возвращаемой величины **для CopyProps.**</span><span class="sxs-lookup"><span data-stu-id="1446c-155">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyProps**.</span></span> <span data-ttu-id="1446c-156">Эти ошибки относятся к одному свойству.</span><span class="sxs-lookup"><span data-stu-id="1446c-156">These errors apply to a single property.</span></span>
  
<span data-ttu-id="1446c-157">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="1446c-157">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="1446c-158">Либо флаг MAPI_UNICODE установлен, а **CopyProps** не поддерживает Юникод, либо MAPI_UNICODE не установлен, а **CopyProps** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="1446c-158">Either the MAPI_UNICODE flag was set and **CopyProps** does not support Unicode, or MAPI_UNICODE was not set and **CopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="1446c-159">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="1446c-159">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="1446c-160">Вызываемая не может изменить свойство, так как это свойство, предназначенное только для чтения, вычисленное владельцем конечного объекта.</span><span class="sxs-lookup"><span data-stu-id="1446c-160">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="1446c-161">Эта ошибка не является серьезной; Вызываемая должна разрешить продолжение операции копирования.</span><span class="sxs-lookup"><span data-stu-id="1446c-161">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="1446c-162">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="1446c-162">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="1446c-163">Недопустимый тип свойства.</span><span class="sxs-lookup"><span data-stu-id="1446c-163">The property type is invalid.</span></span>
    
<span data-ttu-id="1446c-164">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="1446c-164">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="1446c-165">Тип свойства не является типом, ожидаемым для вызываемого объекта.</span><span class="sxs-lookup"><span data-stu-id="1446c-165">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1446c-166">Примечания</span><span class="sxs-lookup"><span data-stu-id="1446c-166">Remarks</span></span>

<span data-ttu-id="1446c-167">Метод **IMAPIProp::CopyProps** копирует или перемещает выбранные свойства из текущего объекта в объект назначения.</span><span class="sxs-lookup"><span data-stu-id="1446c-167">The **IMAPIProp::CopyProps** method copies or moves selected properties from the current object to a destination object.</span></span> <span data-ttu-id="1446c-168">**CopyProps** используется главным образом для ответов на сообщения и переадовки сообщений, где только некоторые свойства исходного сообщения перенаправят с ответом или перенапраздной копией.</span><span class="sxs-lookup"><span data-stu-id="1446c-168">**CopyProps** is used mainly for replying to and forwarding messages, where only some of the properties from the original message travel with the reply or forwarded copy.</span></span> 
  
<span data-ttu-id="1446c-169">Любые подобъекты в объекте-источнике автоматически включаются в операцию и копируются или перемещаются полностью независимо от использования свойств, указанных в структуре [SPropTagArray.](sproptagarray.md)</span><span class="sxs-lookup"><span data-stu-id="1446c-169">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety, regardless of the use of properties indicated by the [SPropTagArray](sproptagarray.md) structure.</span></span> <span data-ttu-id="1446c-170">По умолчанию **CopyProps** переописает все свойства в объекте назначения, которые соответствуют свойствам из объекта-источника.</span><span class="sxs-lookup"><span data-stu-id="1446c-170">By default, **CopyProps** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="1446c-171">Если какие-либо из скопированные или перемещенных свойств уже существуют в объекте назначения, существующие свойства перезаписываются новыми свойствами, если в параметре  _ulFlags_ не установлен флаг MAPI_NOREPLACE.</span><span class="sxs-lookup"><span data-stu-id="1446c-171">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="1446c-172">Существующие сведения в объекте назначения, который не перезаписан, не будут затронуты.</span><span class="sxs-lookup"><span data-stu-id="1446c-172">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1446c-173">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="1446c-173">Notes to implementers</span></span>

<span data-ttu-id="1446c-174">Вы можете предоставить полную реализацию **CopyProps** или полагаться на реализацию, предоставляемую MAPI в объекте поддержки.</span><span class="sxs-lookup"><span data-stu-id="1446c-174">You can provide a full implementation of **CopyProps** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="1446c-175">Если вы хотите использовать реализацию MAPI, вызовите метод **IMAPISupport::D oCopyProps.**</span><span class="sxs-lookup"><span data-stu-id="1446c-175">If you want to use the MAPI implementation, call the **IMAPISupport::DoCopyProps** method.</span></span> <span data-ttu-id="1446c-176">Однако если вы делегируете обработку **в DoCopyProps** и передаете флаг MAPI_DECLINE_OK, избегайте вызова в службу поддержки и MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="1446c-176">However, if you do delegate processing to **DoCopyProps** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="1446c-177">MAPI будет вызван с этим флагом, чтобы избежать возможной рекурсии, которая может произойти при копировании папок.</span><span class="sxs-lookup"><span data-stu-id="1446c-177">You will be called with this flag by MAPI to avoid the possible recursion that can occur when you copy folders.</span></span> 
  
<span data-ttu-id="1446c-178">Поскольку операция копирования может быть продолжительной, необходимо отобразить индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="1446c-178">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="1446c-179">Используйте [реализацию IMAPIProgress,](imapiprogressiunknown.md) которая передается в  _параметре lpProgress,_ если она существует.</span><span class="sxs-lookup"><span data-stu-id="1446c-179">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation that is passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="1446c-180">Если  _lpProgress_ имеет **null,** вызовите метод [IMAPISupport::D oProgressDialog,](imapisupport-doprogressdialog.md) чтобы использовать реализацию MAPI.</span><span class="sxs-lookup"><span data-stu-id="1446c-180">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1446c-181">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="1446c-181">Notes to callers</span></span>

<span data-ttu-id="1446c-182">Не устанавливать флаг MAPI_DECLINE_OK; он используется MAPI в вызовах к реализациям **поставщика службы copyProps** для хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="1446c-182">Do not set the MAPI_DECLINE_OK flag; it is used by MAPI in its calls to message store provider **CopyProps** implementations.</span></span> 
  
<span data-ttu-id="1446c-183">Поскольку операции копирования и перемещения могут занять некоторое время, разумно запросить отображение индикатора хода выполнения, установив MAPI_DIALOG флага.</span><span class="sxs-lookup"><span data-stu-id="1446c-183">Because copy and move operations can take time, it is wise to request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="1446c-184">Вы можете установить для _параметра lpProgress_ реализацию **IMAPIProgress**, если она есть, или иметь **null.**</span><span class="sxs-lookup"><span data-stu-id="1446c-184">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="1446c-185">Если  _lpProgress_ имеет **значение NULL,** **CopyProps** будет использовать индикатор хода выполнения по умолчанию, предоставленный MAPI.</span><span class="sxs-lookup"><span data-stu-id="1446c-185">If  _lpProgress_ is **null**, **CopyProps** will use the default progress indicator provided by MAPI.</span></span> 
  
<span data-ttu-id="1446c-186">Вы можете подавить отображение индикатора хода выполнения, не устанавливая MAPI_DIALOG флага.</span><span class="sxs-lookup"><span data-stu-id="1446c-186">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="1446c-187">**CopyProps** игнорирует  _параметры ulUIParam_ и  _lpProgress_ и не отображает индикатор.</span><span class="sxs-lookup"><span data-stu-id="1446c-187">**CopyProps** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and avoid displaying the indicator.</span></span> 
  
 <span data-ttu-id="1446c-188">**CopyProps** может сообщать о глобальных и отдельных ошибках или ошибках, которые возникают с одним или более свойствами.</span><span class="sxs-lookup"><span data-stu-id="1446c-188">**CopyProps** can report global and individual errors, or errors that occur with one or more of the properties.</span></span> <span data-ttu-id="1446c-189">Эти отдельные ошибки помещаются в структуру **SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="1446c-189">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="1446c-190">Отчеты об ошибках можно подавить на уровне свойства, передав **null** вместо допустимого указателя для параметра структуры массива проблем свойств.</span><span class="sxs-lookup"><span data-stu-id="1446c-190">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="1446c-191">Если вы хотите получить сведения об ошибках, передав допустимый указатель структуры **SPropProblemArray** в _параметре lppProblems._</span><span class="sxs-lookup"><span data-stu-id="1446c-191">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="1446c-192">Когда **CopyProps** возвращает S_OK, проверьте возможные ошибки с отдельными свойствами в структуре.</span><span class="sxs-lookup"><span data-stu-id="1446c-192">When **CopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="1446c-193">Когда **CopyProps** возвращает ошибку, данные в структуре **SPropProblemArray** не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="1446c-193">When **CopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="1446c-194">Вместо этого вызовите метод [IMAPIProp::GetLastError,](imapiprop-getlasterror.md) чтобы получить подробные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="1446c-194">Instead, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="1446c-195">Если **CopyProps** возвращает S_OK, освободите возвращенную **структуру SPropProblemArray,** вызывая функцию [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="1446c-195">If **CopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="1446c-196">При копировании свойств, уникальных для типа источника объекта, необходимо убедиться, что объект назначения имеет тот же тип.</span><span class="sxs-lookup"><span data-stu-id="1446c-196">If you are copying properties that are unique to the source object type, you must make sure that the destination object is of the same type.</span></span> <span data-ttu-id="1446c-197">**CopyProps** не препятствует связыванию свойств, которые обычно относятся к одному типу объекта, с другим типом объекта.</span><span class="sxs-lookup"><span data-stu-id="1446c-197">**CopyProps** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="1446c-198">Вы можете копировать свойства, которые имеют смысл для объекта назначения.</span><span class="sxs-lookup"><span data-stu-id="1446c-198">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="1446c-199">Например, не следует копировать свойства сообщения в контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1446c-199">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="1446c-200">Чтобы убедиться, что вы копируете объекты одного типа, убедитесь, что источник и объект назначения имеют одинаковый тип, сравнивая указатели объектов или вызывая метод [IUnknown::QueryInterface.](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1446c-200">To ensure that you are copying between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="1446c-201">Установите для идентификатора интерфейса, на который указывает  _lpInterface,_ стандартный интерфейс для объекта-источника.</span><span class="sxs-lookup"><span data-stu-id="1446c-201">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="1446c-202">Кроме того, убедитесь, что тип или **PR_OBJECT_TYPE** объекта ([PidTagObjectType)](pidtagobjecttype-canonical-property.md)одинаковы для двух объектов.</span><span class="sxs-lookup"><span data-stu-id="1446c-202">Also, ensure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="1446c-203">Например, если вы копируете из сообщения, установите для _lpInterface_ IID_IMessage и PR_OBJECT_TYPE для обоих объектов MAPI_MESSAGE. </span><span class="sxs-lookup"><span data-stu-id="1446c-203">For example, if you are copying from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="1446c-204">Если в параметре  _lpDestObj_ передается недопустимый указатель, результаты будут непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="1446c-204">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="1446c-205">Чтобы скопировать список получателей сообщения, вызовите метод **CopyProps** сообщения и включим свойство **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)в массив тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="1446c-205">To copy a message's recipient list, call the message's **CopyProps** method and include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array.</span></span> <span data-ttu-id="1446c-206">Чтобы скопировать вложения сообщения, **включаем свойство PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments).](pidtagmessageattachments-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1446c-206">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="1446c-207">Чтобы скопировать иерархию или таблицу содержимого контейнера папки или адресной книги, включите свойства **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)или **PR_CONTAINER_CONTENTS** ([PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)в массив тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="1446c-207">To copy a folder or address book container's hierarchy or contents table, include the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) properties in the property tag array.</span></span> <span data-ttu-id="1446c-208">Чтобы включить связанную с папкой таблицу содержимого, включайте **свойство PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)в массив.</span><span class="sxs-lookup"><span data-stu-id="1446c-208">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1446c-209">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1446c-209">MFCMAPI reference</span></span>

<span data-ttu-id="1446c-210">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="1446c-210">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1446c-211">**Файл**</span><span class="sxs-lookup"><span data-stu-id="1446c-211">**File**</span></span>|<span data-ttu-id="1446c-212">**Функция**</span><span class="sxs-lookup"><span data-stu-id="1446c-212">**Function**</span></span>|<span data-ttu-id="1446c-213">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="1446c-213">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1446c-214">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="1446c-214">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1446c-215">CopyNamedProps</span><span class="sxs-lookup"><span data-stu-id="1446c-215">CopyNamedProps</span></span>  <br/> |<span data-ttu-id="1446c-216">MFCMAPI использует метод **IMAPIProp::CopyProps** для копирования именуемого свойства из одного сообщения в другое.</span><span class="sxs-lookup"><span data-stu-id="1446c-216">MFCMAPI uses the **IMAPIProp::CopyProps** method to copy named properties from one message to another.</span></span>  <br/> |
|<span data-ttu-id="1446c-217">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="1446c-217">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="1446c-218">CSingleMAPIPropListCtrl::OnPasteProperty</span><span class="sxs-lookup"><span data-stu-id="1446c-218">CSingleMAPIPropListCtrl::OnPasteProperty</span></span>  <br/> |<span data-ttu-id="1446c-219">MFCMAPI использует метод **IMAPIProp::CopyProps,** чтобы вкопировать свойство, скопированные из другого объекта.</span><span class="sxs-lookup"><span data-stu-id="1446c-219">MFCMAPI uses the **IMAPIProp::CopyProps** method to paste a property that has been copied from another object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1446c-220">См. также</span><span class="sxs-lookup"><span data-stu-id="1446c-220">See also</span></span>



[<span data-ttu-id="1446c-221">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="1446c-221">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="1446c-222">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1446c-222">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="1446c-223">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="1446c-223">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="1446c-224">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="1446c-224">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="1446c-225">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="1446c-225">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
  
[<span data-ttu-id="1446c-226">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="1446c-226">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="1446c-227">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1446c-227">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1446c-228">Каноническое свойство PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="1446c-228">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="1446c-229">Каноническое свойство PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="1446c-229">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="1446c-230">Каноническое свойство PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="1446c-230">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="1446c-231">Каноническое свойство PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="1446c-231">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="1446c-232">Каноническое свойство PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="1446c-232">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="1446c-233">Каноническое свойство PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="1446c-233">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="1446c-234">Каноническое свойство PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="1446c-234">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="1446c-235">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="1446c-235">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="1446c-236">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="1446c-236">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="1446c-237">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1446c-237">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="1446c-238">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="1446c-238">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

