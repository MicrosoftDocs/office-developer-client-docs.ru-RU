---
title: IMAPIPropCopyTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyTo
api_type:
- COM
ms.assetid: e56042e9-5bb7-4a99-b6de-1546d4ca07f0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f76b0a5482647fe3e181a36d7dcd8cb60ffc8985
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356394"
---
# <a name="imapipropcopyto"></a><span data-ttu-id="dbe38-103">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="dbe38-103">IMAPIProp::CopyTo</span></span>

  
  
<span data-ttu-id="dbe38-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dbe38-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dbe38-105">Копирует или перемещает все свойства, кроме специально исключенных.</span><span class="sxs-lookup"><span data-stu-id="dbe38-105">Copies or moves all properties, except for specifically excluded properties.</span></span>
  
```cpp
HRESULT CopyTo(
 ULONG ciidExclude,
 LPCIID rgiidExclude,
 LPSPropTagArray lpExcludeProps,
 ULONG_PTR ulUIParam,
 LPMAPIPROGRESS lpProgress,
 LPCIID lpInterface,
 LPVOID lpDestObj,
 ULONG ulFlags,
 LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="dbe38-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dbe38-106">Parameters</span></span>

 <span data-ttu-id="dbe38-107">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="dbe38-107">_ciidExclude_</span></span>
  
> <span data-ttu-id="dbe38-108">[in] Количество интерфейсов, которые необходимо исключить при копировании или перемещении свойств.</span><span class="sxs-lookup"><span data-stu-id="dbe38-108">[in] The count of interfaces to exclude when properties are copied or moved.</span></span>
    
 <span data-ttu-id="dbe38-109">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="dbe38-109">_rgiidExclude_</span></span>
  
> <span data-ttu-id="dbe38-110">[in] Массив идентификаторов интерфейса (IID), которые указывают интерфейсы, которые не следует использовать при копировании или перемещении дополнительных сведений в объект назначения.</span><span class="sxs-lookup"><span data-stu-id="dbe38-110">[in] An array of interface identifiers (IIDs) that specify interfaces that should not be used when supplemental information is copied or moved to the destination object.</span></span>
    
 <span data-ttu-id="dbe38-111">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="dbe38-111">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="dbe38-112">[in] Указатель на массив тегов свойств, который определяет теги свойств, которые необходимо исключить из операции копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="dbe38-112">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="dbe38-113">Передача **null** в параметр  _lpExcludeProps_ означает, что все свойства объекта должны быть скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="dbe38-113">Passing **null** in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="dbe38-114">**CopyTo** возвращает MAPI_E_INVALID_PARAMETER, когда для члена **cValues** структуры [SPropProblemArray,](spropproblemarray.md) на который указывает  _lpExcludeProps,_ установлено 0.</span><span class="sxs-lookup"><span data-stu-id="dbe38-114">**CopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropProblemArray](spropproblemarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="dbe38-115">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="dbe38-115">_ulUIParam_</span></span>
  
> <span data-ttu-id="dbe38-116">[in] Handle to the parent window of the progress indicator.</span><span class="sxs-lookup"><span data-stu-id="dbe38-116">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="dbe38-117">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="dbe38-117">_lpProgress_</span></span>
  
> <span data-ttu-id="dbe38-118">[in] Указатель на реализацию индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="dbe38-118">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="dbe38-119">Если **в параметре**  _lpProgress_ передается null, MAPI обеспечивает реализацию хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="dbe38-119">If **null** is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="dbe38-120">Параметр _lpProgress_ игнорируется, если MAPI_DIALOG флага в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="dbe38-120">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="dbe38-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="dbe38-121">_lpInterface_</span></span>
  
> <span data-ttu-id="dbe38-122">[in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, используемый для доступа к объекту, на который указывает параметр _lpDestObj._</span><span class="sxs-lookup"><span data-stu-id="dbe38-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="dbe38-123">Параметр _lpInterface_ не должен иметь **null.**</span><span class="sxs-lookup"><span data-stu-id="dbe38-123">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="dbe38-124">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="dbe38-124">_lpDestObj_</span></span>
  
> <span data-ttu-id="dbe38-125">[in] Указатель на объект для получения скопированные или перемещенные свойства.</span><span class="sxs-lookup"><span data-stu-id="dbe38-125">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="dbe38-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dbe38-126">_ulFlags_</span></span>
  
> <span data-ttu-id="dbe38-127">[in] Битоваяmas флагов, которая управляет операцией копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="dbe38-127">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="dbe38-128">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="dbe38-128">The following flags can be set:</span></span>
    
<span data-ttu-id="dbe38-129">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="dbe38-129">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="dbe38-130">Если **CopyTo вызывает** метод [IMAPISupport::D oCopyTo](imapisupport-docopyto.md) для обработки операции копирования или перемещения, он должен возвращаться немедленно со значением MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="dbe38-130">If **CopyTo** calls the [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="dbe38-131">MapI MAPI_DECLINE_OK флага для ограничения рекурсии.</span><span class="sxs-lookup"><span data-stu-id="dbe38-131">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="dbe38-132">Клиенты не устанавливают этот флаг.</span><span class="sxs-lookup"><span data-stu-id="dbe38-132">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="dbe38-133">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="dbe38-133">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="dbe38-134">Отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="dbe38-134">Displays a progress indicator.</span></span>
    
<span data-ttu-id="dbe38-135">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="dbe38-135">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="dbe38-136">**CopyTo** должен выполнять операцию перемещения вместо операции копирования.</span><span class="sxs-lookup"><span data-stu-id="dbe38-136">**CopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="dbe38-137">Если этот флаг не установлен, **CopyTo выполняет** операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="dbe38-137">When this flag is not set, **CopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="dbe38-138">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="dbe38-138">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="dbe38-139">Существующие свойства в объекте назначения не следует перезаписывать.</span><span class="sxs-lookup"><span data-stu-id="dbe38-139">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="dbe38-140">Если этот флаг не установлен, **CopyTo** переописает существующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dbe38-140">When this flag is not set, **CopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="dbe38-141">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="dbe38-141">_lppProblems_</span></span>
  
> <span data-ttu-id="dbe38-142">[in, out] При вводе указатель на указатель на **структуру SPropProblemArray;** в **противном случае имеется null,** указывающее на отсутствие необходимости в сведениях об ошибках.</span><span class="sxs-lookup"><span data-stu-id="dbe38-142">[in, out] On input, a pointer to a pointer to an **SPropProblemArray** structure; otherwise, **null**, indicating no need for error information.</span></span> <span data-ttu-id="dbe38-143">Если  _lppProblems_ является допустимым указателем при вводе, **CopyTo** возвращает подробные сведения об ошибках при копировании одного или более свойств.</span><span class="sxs-lookup"><span data-stu-id="dbe38-143">If  _lppProblems_ is a valid pointer on input, **CopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dbe38-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dbe38-144">Return value</span></span>

<span data-ttu-id="dbe38-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="dbe38-145">S_OK</span></span> 
  
> <span data-ttu-id="dbe38-146">Свойства успешно скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="dbe38-146">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="dbe38-147">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="dbe38-147">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="dbe38-148">Подобект нельзя скопировать, так как в объекте назначения уже существует подпроект с таким же отображаемым **именем,** указанным свойством PR_DISPLAY_NAME ([PidTagDisplayName).](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="dbe38-148">A subobject cannot be copied because a subobject with the same display name — specified by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property — already exists in the destination object.</span></span> 
    
<span data-ttu-id="dbe38-149">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="dbe38-149">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="dbe38-150">Поставщик услуг не реализует операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="dbe38-150">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="dbe38-151">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="dbe38-151">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="dbe38-152">Исходный объект, который выполняет операцию копирования или перемещения прямо или косвенно, содержит объект назначения.</span><span class="sxs-lookup"><span data-stu-id="dbe38-152">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="dbe38-153">Перед обнаружением этого условия могли быть выполнены значительные трудоемкие работы, поэтому исходные и назначения объектов могут быть частично изменены.</span><span class="sxs-lookup"><span data-stu-id="dbe38-153">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="dbe38-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="dbe38-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="dbe38-155">Интерфейс, заданный  _параметром lpInterface,_ не поддерживается объектом назначения.</span><span class="sxs-lookup"><span data-stu-id="dbe38-155">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="dbe38-156">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="dbe38-156">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="dbe38-157">Предпринята попытка доступа к объекту, у которого у вызываемого объекта недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="dbe38-157">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="dbe38-158">Эта ошибка возвращается, если объект назначения такой же, как и исходный объект.</span><span class="sxs-lookup"><span data-stu-id="dbe38-158">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="dbe38-159">Следующие значения могут быть возвращены в структуре **SPropProblemArray,** но не в качестве возвращаемой величины **для CopyTo.**</span><span class="sxs-lookup"><span data-stu-id="dbe38-159">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyTo**.</span></span> <span data-ttu-id="dbe38-160">К одному свойству применяются следующие ошибки:</span><span class="sxs-lookup"><span data-stu-id="dbe38-160">The following errors apply to a single property:</span></span>
  
<span data-ttu-id="dbe38-161">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="dbe38-161">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="dbe38-162">Либо флаг MAPI_UNICODE установлен, а **CopyTo** не поддерживает Юникод, либо MAPI_UNICODE не установлен, а **CopyTo** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="dbe38-162">Either the MAPI_UNICODE flag was set and **CopyTo** does not support Unicode, or MAPI_UNICODE was not set and **CopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="dbe38-163">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="dbe38-163">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="dbe38-164">Вызываемая не может изменить свойство, так как это свойство, предназначенное только для чтения, вычисленное владельцем конечного объекта.</span><span class="sxs-lookup"><span data-stu-id="dbe38-164">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="dbe38-165">Эта ошибка не является серьезной; Вызываемая должна разрешить продолжение операции копирования.</span><span class="sxs-lookup"><span data-stu-id="dbe38-165">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="dbe38-166">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="dbe38-166">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="dbe38-167">Недопустимый тип свойства.</span><span class="sxs-lookup"><span data-stu-id="dbe38-167">The property type is invalid.</span></span>
    
<span data-ttu-id="dbe38-168">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="dbe38-168">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="dbe38-169">Тип свойства не является типом, ожидаемым для вызываемого объекта.</span><span class="sxs-lookup"><span data-stu-id="dbe38-169">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dbe38-170">Примечания</span><span class="sxs-lookup"><span data-stu-id="dbe38-170">Remarks</span></span>

<span data-ttu-id="dbe38-171">По умолчанию метод **IMAPIProp::CopyTo** копирует или перемещает все свойства текущего объекта в объект назначения.</span><span class="sxs-lookup"><span data-stu-id="dbe38-171">By default, the **IMAPIProp::CopyTo** method copies or moves all of the current object's properties to a destination object.</span></span> <span data-ttu-id="dbe38-172">**CopyTo** используется, когда объект должен быть точно скопирован или перемещен, со всеми или большинством его свойств без изменений.</span><span class="sxs-lookup"><span data-stu-id="dbe38-172">**CopyTo** is used when an object should be copied or moved exactly, with all or most of its properties intact.</span></span> 
  
<span data-ttu-id="dbe38-173">Любые подпроекты в объекте-источнике автоматически включаются в операцию и копируются или перемещаются полностью.</span><span class="sxs-lookup"><span data-stu-id="dbe38-173">Any subobjects in the source object are automatically included in the operation and are copied or moved in their entirety.</span></span> <span data-ttu-id="dbe38-174">По умолчанию **CopyTo** переописает все свойства в объекте назначения, которые соответствуют свойствам из объекта-источника.</span><span class="sxs-lookup"><span data-stu-id="dbe38-174">By default, **CopyTo** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="dbe38-175">Если какие-либо из скопированные или перемещенных свойств уже существуют в объекте назначения, существующие свойства перезаписываются новыми свойствами, если в параметре  _ulFlags_ не установлен флаг MAPI_NOREPLACE.</span><span class="sxs-lookup"><span data-stu-id="dbe38-175">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="dbe38-176">Существующие сведения в объекте назначения, который не перезаписан, не будут затронуты.</span><span class="sxs-lookup"><span data-stu-id="dbe38-176">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="dbe38-177">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="dbe38-177">Notes to implementers</span></span>

<span data-ttu-id="dbe38-178">Вы можете предоставить полную реализацию **CopyTo** или полагаться на реализацию, предоставляемую MAPI в объекте поддержки.</span><span class="sxs-lookup"><span data-stu-id="dbe38-178">You can provide a full implementation of **CopyTo** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="dbe38-179">Если вы хотите использовать реализацию MAPI, вызовите **IMAPISupport::D oCopyTo**.</span><span class="sxs-lookup"><span data-stu-id="dbe38-179">If you want to use the MAPI implementation, call **IMAPISupport::DoCopyTo**.</span></span> <span data-ttu-id="dbe38-180">Однако если вы делегируете обработку **в DoCopyTo** и передаете флаг MAPI_DECLINE_OK, избегайте вызова в службу поддержки и MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="dbe38-180">However, if you do delegate processing to **DoCopyTo** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="dbe38-181">MAPI будет вызываться с этим флагом, чтобы избежать возможной рекурсии, которая может произойти при копировании папок.</span><span class="sxs-lookup"><span data-stu-id="dbe38-181">MAPI will call with this flag to avoid the possible recursion that can happen when folders are copied.</span></span> 
  
<span data-ttu-id="dbe38-182">Поскольку операция копирования может быть продолжительной, необходимо отобразить индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="dbe38-182">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="dbe38-183">Используйте [реализацию IMAPIProgress,](imapiprogressiunknown.md) переданную в  _параметре lpProgress,_ если она существует.</span><span class="sxs-lookup"><span data-stu-id="dbe38-183">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="dbe38-184">Если  _lpProgress_ имеет **null,** вызовите метод [IMAPISupport::D oProgressDialog,](imapisupport-doprogressdialog.md) чтобы использовать реализацию MAPI.</span><span class="sxs-lookup"><span data-stu-id="dbe38-184">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
<span data-ttu-id="dbe38-185">Не пытайтесь установить какие-либо известные свойства только для чтения в объекте назначения; вместо MAPI_E_NO_ACCESS возвращается.</span><span class="sxs-lookup"><span data-stu-id="dbe38-185">Do not attempt to set any known read-only properties in the destination object; return MAPI_E_NO_ACCESS instead.</span></span>
  
<span data-ttu-id="dbe38-186">Исходные и назначения объектов должны использовать одинаковые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="dbe38-186">The source and destination objects should use the same interfaces.</span></span> <span data-ttu-id="dbe38-187">Возвращает MAPI_E_INVALID_PARAMETER,  _если lpInterface_ не задан.</span><span class="sxs-lookup"><span data-stu-id="dbe38-187">Return MAPI_E_INVALID_PARAMETER if  _lpInterface_ is not set.</span></span> 
  
<span data-ttu-id="dbe38-188">Возвращает MAPI_E_INTERFACE_NOT_SUPPORTED, если все известные интерфейсы исключены.</span><span class="sxs-lookup"><span data-stu-id="dbe38-188">Return MAPI_E_INTERFACE_NOT_SUPPORTED if all known interfaces are excluded.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="dbe38-189">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="dbe38-189">Notes to callers</span></span>

<span data-ttu-id="dbe38-190">Не устанавливать флаг MAPI_DECLINE_OK; MAPI использует его в вызовах к реализациям поставщика службы хранения сообщений **CopyTo.**</span><span class="sxs-lookup"><span data-stu-id="dbe38-190">Do not set the MAPI_DECLINE_OK flag; MAPI uses it in its calls to message store provider **CopyTo** implementations.</span></span> 
  
<span data-ttu-id="dbe38-191">Поскольку операции копирования и перемещения могут занять некоторое время, следует запросить отображение индикатора хода выполнения, установив MAPI_DIALOG флага.</span><span class="sxs-lookup"><span data-stu-id="dbe38-191">Because copy and move operations can take time, you should request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="dbe38-192">Вы можете установить для _параметра lpProgress_ реализацию **IMAPIProgress**, если она есть, или иметь **null.**</span><span class="sxs-lookup"><span data-stu-id="dbe38-192">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="dbe38-193">Если  _lpProgress_ имеет **значение NULL,** **CopyTo** будет использовать индикатор хода выполнения по умолчанию, который предоставляет MAPI.</span><span class="sxs-lookup"><span data-stu-id="dbe38-193">If  _lpProgress_ is **null**, **CopyTo** will use the default progress indicator that MAPI provides.</span></span> 
  
<span data-ttu-id="dbe38-194">Вы можете подавить отображение индикатора хода выполнения, не устанавливая MAPI_DIALOG флага.</span><span class="sxs-lookup"><span data-stu-id="dbe38-194">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="dbe38-195">**CopyTo** игнорирует  _параметры ulUIParam_ и  _lpProgress_ и не отображает индикатор.</span><span class="sxs-lookup"><span data-stu-id="dbe38-195">**CopyTo** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and will not display the indicator.</span></span> 
  
 <span data-ttu-id="dbe38-196">**CopyTo** может сообщать о глобальных и отдельных ошибках или ошибках, которые возникают с одним или более свойствами.</span><span class="sxs-lookup"><span data-stu-id="dbe38-196">**CopyTo** can report global and individual errors, or errors that occur with one or more properties.</span></span> <span data-ttu-id="dbe38-197">Эти отдельные ошибки размещаются в структуре **SPropProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="dbe38-197">These individual errors are placed in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="dbe38-198">Отчеты об ошибках можно подавить на уровне свойства, передав **null** вместо допустимого указателя для параметра структуры массива проблем свойств.</span><span class="sxs-lookup"><span data-stu-id="dbe38-198">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="dbe38-199">Если вы хотите получить сведения об ошибках, передав допустимый указатель структуры **SPropProblemArray** в _параметре lppProblems._</span><span class="sxs-lookup"><span data-stu-id="dbe38-199">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="dbe38-200">Когда **CopyTo** возвращает S_OK, проверьте возможные ошибки с отдельными свойствами в структуре.</span><span class="sxs-lookup"><span data-stu-id="dbe38-200">When **CopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="dbe38-201">Когда **CopyTo** возвращает ошибку, данные в структуре **SPropProblemArray** не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="dbe38-201">When **CopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="dbe38-202">Вместо этого вызовите [IMAPIProp::GetLastError,](imapiprop-getlasterror.md) чтобы получить подробные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="dbe38-202">Instead, call [IMAPIProp::GetLastError](imapiprop-getlasterror.md) to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="dbe38-203">Если **CopyTo** возвращает S_OK, освободите возвращенную **структуру SPropProblemArray,** вызывая функцию [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="dbe38-203">If **CopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="dbe38-204">При копировании свойств, уникальных для типа источника объекта, необходимо убедиться, что объект назначения имеет тот же тип.</span><span class="sxs-lookup"><span data-stu-id="dbe38-204">If you copy properties that are unique to the source object type, you must ensure that the destination object is of the same type.</span></span> <span data-ttu-id="dbe38-205">**CopyTo** не препятствует связыванию свойств, которые обычно относятся к одному типу объекта, с другим типом объекта.</span><span class="sxs-lookup"><span data-stu-id="dbe38-205">**CopyTo** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="dbe38-206">Вы можете копировать свойства, которые имеют смысл для объекта назначения.</span><span class="sxs-lookup"><span data-stu-id="dbe38-206">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="dbe38-207">Например, не следует копировать свойства сообщения в контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="dbe38-207">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="dbe38-208">Чтобы обеспечить копирование между объектами одного типа, убедитесь, что источник и объект назначения имеют одинаковый тип, сравнивая указатели объектов или вызывая [IUnknown::QueryInterface.](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dbe38-208">To ensure that you copy between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="dbe38-209">Установите для идентификатора интерфейса, на который указывает  _lpInterface,_ стандартный интерфейс для объекта-источника.</span><span class="sxs-lookup"><span data-stu-id="dbe38-209">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="dbe38-210">Кроме того, убедитесь, что тип или **PR_OBJECT_TYPE** объекта ([PidTagObjectType)](pidtagobjecttype-canonical-property.md)одинаковы для двух объектов.</span><span class="sxs-lookup"><span data-stu-id="dbe38-210">Also, be sure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="dbe38-211">Например, если вы копируете из сообщения, установите для _lpInterface_ IID_IMessage и PR_OBJECT_TYPE для обоих MAPI_MESSAGE. </span><span class="sxs-lookup"><span data-stu-id="dbe38-211">For example, if you copy from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="dbe38-212">Если в параметре  _lpDestObj_ передается недопустимый указатель, результаты будут непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="dbe38-212">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="dbe38-213">Исключение свойств при вызове **CopyTo** может быть полезным.</span><span class="sxs-lookup"><span data-stu-id="dbe38-213">Excluding properties on a **CopyTo** call can be useful.</span></span> <span data-ttu-id="dbe38-214">Например, некоторые объекты имеют свойства, специфичная для одного экземпляра объекта, например дата и время доставки сообщения.</span><span class="sxs-lookup"><span data-stu-id="dbe38-214">For example, some objects have properties that are specific to a single instance of the object, such as the date and time of message delivery.</span></span> <span data-ttu-id="dbe38-215">Чтобы избежать копирования времени доставки сообщения при копировании сообщения в другую папку, укажите PR_MESSAGE_DELIVERY_TIME **(** [PidTagMessageDeliveryTime)](pidtagmessagedeliverytime-canonical-property.md)в теге свойства исключить массив.</span><span class="sxs-lookup"><span data-stu-id="dbe38-215">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="dbe38-216">Чтобы исключить список получателей сообщения, добавьте **свойство PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)в массив исключений.</span><span class="sxs-lookup"><span data-stu-id="dbe38-216">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="dbe38-217">Чтобы исключить вложения сообщения, **добавьте** свойство PR_MESSAGE_ATTACHMENTS [(PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)в массив.</span><span class="sxs-lookup"><span data-stu-id="dbe38-217">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="dbe38-218">Аналогичным образом, предотвращают копирование или перемещение иерархии или таблицы содержимого контейнера папки или адресной **книги,** включив PR_CONTAINER_HIERARCHY ([PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)или **PR_CONTAINER_CONTENTS** ([PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)в тег свойства, исключающий массив.</span><span class="sxs-lookup"><span data-stu-id="dbe38-218">Similarly, prevent the copying or moving of a folder or address book container's hierarchy or contents table by including **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="dbe38-219">Чтобы исключить свойства из операции копирования или перемещения, включаем их теги свойств в параметр _lpExcludeProps._</span><span class="sxs-lookup"><span data-stu-id="dbe38-219">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="dbe38-220">Если передать результаты **макроса PROP_TAG** для создания тега свойства из определенного идентификатора в массиве тегов свойств, все свойства с этим идентификатором будут исключены.</span><span class="sxs-lookup"><span data-stu-id="dbe38-220">If you pass the results of the **PROP_TAG** macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="dbe38-221">Например, следующая запись в массиве тегов свойств приводит к исключению всех свойств с идентификатором 0x8002, независимо от типа:</span><span class="sxs-lookup"><span data-stu-id="dbe38-221">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="dbe38-222">Тег **PR_NULL** ([PidTagNull)](pidtagnull-canonical-property.md)нельзя включить в массив _lpExcludeProps._</span><span class="sxs-lookup"><span data-stu-id="dbe38-222">The **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag cannot be included in the  _lpExcludeProps_ array.</span></span> 
  
<span data-ttu-id="dbe38-223">Полезность функции **CopyTo** для исключения интерфейсов, возможно, не так очевидна, как полезность исключения свойств.</span><span class="sxs-lookup"><span data-stu-id="dbe38-223">The usefulness of the **CopyTo** feature for excluding interfaces is perhaps not as obvious as the usefulness of excluding properties.</span></span> <span data-ttu-id="dbe38-224">Интерфейс можно исключить при копировании в объект, который не имеет знаний о группе свойств.</span><span class="sxs-lookup"><span data-stu-id="dbe38-224">You can exclude an interface when you copy to an object that has no knowledge of a group of properties.</span></span> <span data-ttu-id="dbe38-225">Например, если скопировать свойства из папки во вложение, вложение сможет работать только с общими свойствами, доступными при любой реализации [IMAPIProp.](imapipropiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="dbe38-225">For example, if you copy properties from a folder to an attachment, the only properties that the attachment can work with are the generic properties available with any [IMAPIProp](imapipropiunknown.md) implementation.</span></span> <span data-ttu-id="dbe38-226">Исключив [IMAPIFolder](imapifolderimapicontainer.md) из операции копирования, вложение не получит никаких более конкретных свойств папки.</span><span class="sxs-lookup"><span data-stu-id="dbe38-226">By excluding [IMAPIFolder](imapifolderimapicontainer.md) from the copy operation, the attachment will not receive any of the more specific folder properties.</span></span> 
  
<span data-ttu-id="dbe38-227">При использовании  _параметра rgiidExclude_ для исключения интерфейса он также исключает все интерфейсы, производные от этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="dbe38-227">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="dbe38-228">Например, исключение [IMAPIContainer](imapicontainerimapiprop.md) приводит к исключению папок или контейнеров адресной книги в зависимости от типа поставщика.</span><span class="sxs-lookup"><span data-stu-id="dbe38-228">For example, excluding [IMAPIContainer](imapicontainerimapiprop.md) causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="dbe38-229">Не исключать **IMAPIProp** или [IUnknown,](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) так как так много интерфейсов являются от них на основе.</span><span class="sxs-lookup"><span data-stu-id="dbe38-229">Do not exclude **IMAPIProp** or [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) because so many interfaces derive from them.</span></span> 
  
<span data-ttu-id="dbe38-230">Игнорируйте MAPI_E_COMPUTED ошибки, возвращенные в **структуре SPropProblemArray** в _параметре lppProblems._</span><span class="sxs-lookup"><span data-stu-id="dbe38-230">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dbe38-231">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="dbe38-231">MFCMAPI reference</span></span>

<span data-ttu-id="dbe38-232">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="dbe38-232">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dbe38-233">**Файл**</span><span class="sxs-lookup"><span data-stu-id="dbe38-233">**File**</span></span>|<span data-ttu-id="dbe38-234">**Функция**</span><span class="sxs-lookup"><span data-stu-id="dbe38-234">**Function**</span></span>|<span data-ttu-id="dbe38-235">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="dbe38-235">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dbe38-236">File.cpp</span><span class="sxs-lookup"><span data-stu-id="dbe38-236">File.cpp</span></span>  <br/> |<span data-ttu-id="dbe38-237">LoadFromMSG</span><span class="sxs-lookup"><span data-stu-id="dbe38-237">LoadFromMSG</span></span>  <br/> |<span data-ttu-id="dbe38-238">MFCMAPI использует метод **IMAPIProp::CopyTo** для копирования свойств из MSG-файла в объект [IMAPIMessageSite.](imapimessagesiteiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="dbe38-238">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a .msg file to an [IMAPIMessageSite](imapimessagesiteiunknown.md) object.</span></span>  <br/> |
|<span data-ttu-id="dbe38-239">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="dbe38-239">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="dbe38-240">CFolderDlg::HandlePaste</span><span class="sxs-lookup"><span data-stu-id="dbe38-240">CFolderDlg::HandlePaste</span></span>  <br/> |<span data-ttu-id="dbe38-241">MFCMAPI использует метод **IMAPIProp::CopyTo** для копирования свойств из сообщения источника в целевое сообщение во время операции в paste.</span><span class="sxs-lookup"><span data-stu-id="dbe38-241">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a source message to a target message during a paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dbe38-242">См. также</span><span class="sxs-lookup"><span data-stu-id="dbe38-242">See also</span></span>



[<span data-ttu-id="dbe38-243">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="dbe38-243">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="dbe38-244">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="dbe38-244">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="dbe38-245">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dbe38-245">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="dbe38-246">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dbe38-246">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="dbe38-247">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="dbe38-247">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="dbe38-248">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="dbe38-248">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="dbe38-249">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="dbe38-249">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="dbe38-250">Каноническое свойство PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="dbe38-250">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="dbe38-251">Каноническое свойство PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="dbe38-251">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="dbe38-252">Каноническое свойство PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="dbe38-252">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="dbe38-253">Каноническое свойство PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="dbe38-253">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="dbe38-254">Каноническое свойство PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="dbe38-254">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="dbe38-255">Каноническое свойство PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="dbe38-255">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="dbe38-256">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="dbe38-256">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="dbe38-257">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="dbe38-257">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="dbe38-258">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dbe38-258">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="dbe38-259">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="dbe38-259">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

