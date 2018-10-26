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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388583"
---
# <a name="imapipropcopyto"></a><span data-ttu-id="80d78-103">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="80d78-103">IMAPIProp::CopyTo</span></span>

  
  
<span data-ttu-id="80d78-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80d78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80d78-105">Копирует или переносит все свойства, за исключением специально исключенные свойства.</span><span class="sxs-lookup"><span data-stu-id="80d78-105">Copies or moves all properties, except for specifically excluded properties.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="80d78-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="80d78-106">Parameters</span></span>

 <span data-ttu-id="80d78-107">_ciidExclude_</span><span class="sxs-lookup"><span data-stu-id="80d78-107">_ciidExclude_</span></span>
  
> <span data-ttu-id="80d78-108">[in] Число интерфейсов следует исключить при копировании или перемещении свойства.</span><span class="sxs-lookup"><span data-stu-id="80d78-108">[in] The count of interfaces to exclude when properties are copied or moved.</span></span>
    
 <span data-ttu-id="80d78-109">_rgiidExclude_</span><span class="sxs-lookup"><span data-stu-id="80d78-109">_rgiidExclude_</span></span>
  
> <span data-ttu-id="80d78-110">[in] Массив идентификаторов интерфейса (идентификаторы IID), которые определяют интерфейсы, которые не должны использоваться при дополнительную информацию, копируется или переносится в целевой объект.</span><span class="sxs-lookup"><span data-stu-id="80d78-110">[in] An array of interface identifiers (IIDs) that specify interfaces that should not be used when supplemental information is copied or moved to the destination object.</span></span>
    
 <span data-ttu-id="80d78-111">_lpExcludeProps_</span><span class="sxs-lookup"><span data-stu-id="80d78-111">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="80d78-112">[in] Указатель в массив тег свойства, который определяет свойство теги, которые следует исключить из копии или операции перемещения.</span><span class="sxs-lookup"><span data-stu-id="80d78-112">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="80d78-113">Передача **значение null,** с помощью параметра _lpExcludeProps_ означает, что все свойства объекта следует скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="80d78-113">Passing **null** in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="80d78-114">**CopyTo** возвращает MAPI_E_INVALID_PARAMETER при член **cValues** структуры [SPropProblemArray](spropproblemarray.md) указывает _lpExcludeProps_ имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="80d78-114">**CopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropProblemArray](spropproblemarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="80d78-115">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="80d78-115">_ulUIParam_</span></span>
  
> <span data-ttu-id="80d78-116">[in] Дескриптор родительского окна индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="80d78-116">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="80d78-117">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="80d78-117">_lpProgress_</span></span>
  
> <span data-ttu-id="80d78-118">[in] Указатель на реализацию индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="80d78-118">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="80d78-119">Если **значение null,** передается в параметре _lpProgress_ , MAPI предоставляет реализацию хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="80d78-119">If **null** is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="80d78-120">Параметр _lpProgress_ игнорируется, пока флаг MAPI_DIALOG будет выполнен с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="80d78-120">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="80d78-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="80d78-121">_lpInterface_</span></span>
  
> <span data-ttu-id="80d78-122">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к объекту, на который указывает параметр _lpDestObj_ .</span><span class="sxs-lookup"><span data-stu-id="80d78-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="80d78-123">Параметр _lpInterface_ не должно быть **значение null**.</span><span class="sxs-lookup"><span data-stu-id="80d78-123">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="80d78-124">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="80d78-124">_lpDestObj_</span></span>
  
> <span data-ttu-id="80d78-125">[in] Указатель на объект для получения свойств копируемые или перемещения.</span><span class="sxs-lookup"><span data-stu-id="80d78-125">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="80d78-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="80d78-126">_ulFlags_</span></span>
  
> <span data-ttu-id="80d78-127">[in] Битовая маска флаги, который определяет операцию копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="80d78-127">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="80d78-128">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="80d78-128">The following flags can be set:</span></span>
    
<span data-ttu-id="80d78-129">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="80d78-129">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="80d78-130">Если **CopyTo** вызывает метод [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) для обработки копировать или перемещать операции, она немедленно вместо этого возвращает со значением ошибки MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="80d78-130">If **CopyTo** calls the [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="80d78-131">Флаг MAPI_DECLINE_OK задается MAPI для ограничения рекурсии.</span><span class="sxs-lookup"><span data-stu-id="80d78-131">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="80d78-132">Клиенты не задан этот флаг.</span><span class="sxs-lookup"><span data-stu-id="80d78-132">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="80d78-133">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="80d78-133">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="80d78-134">Отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="80d78-134">Displays a progress indicator.</span></span>
    
<span data-ttu-id="80d78-135">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="80d78-135">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="80d78-136">**CopyTo** следует выполнять операции перемещения вместо операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="80d78-136">**CopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="80d78-137">Если этот флаг не задан, **CopyTo** выполняет операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="80d78-137">When this flag is not set, **CopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="80d78-138">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="80d78-138">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="80d78-139">Не следует перезаписывать существующие свойства в целевой объект.</span><span class="sxs-lookup"><span data-stu-id="80d78-139">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="80d78-140">Если этот флаг не задан, **CopyTo** перезаписывает существующие свойства.</span><span class="sxs-lookup"><span data-stu-id="80d78-140">When this flag is not set, **CopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="80d78-141">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="80d78-141">_lppProblems_</span></span>
  
> <span data-ttu-id="80d78-142">[in, out] На входе указатель указатель на структуру **SPropProblemArray** ; в противном случае — **значение null**, указывает, не требуется выполнять сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="80d78-142">[in, out] On input, a pointer to a pointer to an **SPropProblemArray** structure; otherwise, **null**, indicating no need for error information.</span></span> <span data-ttu-id="80d78-143">Если _lppProblems_ допустимый указатель на входные данные, **CopyTo** возвращает подробные сведения об ошибках в копирование одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="80d78-143">If  _lppProblems_ is a valid pointer on input, **CopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="80d78-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80d78-144">Return value</span></span>

<span data-ttu-id="80d78-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="80d78-145">S_OK</span></span> 
  
> <span data-ttu-id="80d78-146">Свойства успешно копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="80d78-146">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="80d78-147">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="80d78-147">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="80d78-148">Вложенные объекты, которые не могут быть скопированы, так как вложенные объекты с тем же отображаемое имя, заданное свойством **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) — уже существует в целевой объект.</span><span class="sxs-lookup"><span data-stu-id="80d78-148">A subobject cannot be copied because a subobject with the same display name — specified by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property — already exists in the destination object.</span></span> 
    
<span data-ttu-id="80d78-149">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="80d78-149">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="80d78-150">Поставщик услуг не реализует операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="80d78-150">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="80d78-151">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="80d78-151">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="80d78-152">Исходный объект для выполнения операции копирования или перемещения прямо или косвенно содержит целевой объект.</span><span class="sxs-lookup"><span data-stu-id="80d78-152">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="80d78-153">Важные может быть выполнено перед был обнаружен это условие, поэтому исходный и целевой объекты частично могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="80d78-153">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="80d78-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="80d78-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="80d78-155">Интерфейс, определенного параметром _lpInterface_ не поддерживается в целевой объект.</span><span class="sxs-lookup"><span data-stu-id="80d78-155">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="80d78-156">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="80d78-156">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="80d78-157">Предпринята попытка получить доступ к объекту, для которого вызывающий не имеет разрешений.</span><span class="sxs-lookup"><span data-stu-id="80d78-157">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="80d78-158">Эта ошибка возвращается в том случае, если в целевой объект совпадает с исходным объектом.</span><span class="sxs-lookup"><span data-stu-id="80d78-158">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="80d78-159">Возможные значения могут быть возвращены в структуре **SPropProblemArray** , но не как возвращаемые значения для **CopyTo**.</span><span class="sxs-lookup"><span data-stu-id="80d78-159">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyTo**.</span></span> <span data-ttu-id="80d78-160">Следующие ошибки относятся к одному свойству:</span><span class="sxs-lookup"><span data-stu-id="80d78-160">The following errors apply to a single property:</span></span>
  
<span data-ttu-id="80d78-161">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="80d78-161">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="80d78-162">Либо был установлен флажок MAPI_UNICODE и **CopyTo** не поддерживает Юникод, или MAPI_UNICODE не было установлено и **CopyTo** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="80d78-162">Either the MAPI_UNICODE flag was set and **CopyTo** does not support Unicode, or MAPI_UNICODE was not set and **CopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="80d78-163">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="80d78-163">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="80d78-164">Невозможно изменить свойство вызывающим абонентом, так как он является свойством только для чтения, вычисленный владельцем конечного объекта.</span><span class="sxs-lookup"><span data-stu-id="80d78-164">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="80d78-165">Эта ошибка не является очень неблагоприятных; вызывающего абонента, должна поддерживать операции копирования для продолжения.</span><span class="sxs-lookup"><span data-stu-id="80d78-165">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="80d78-166">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="80d78-166">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="80d78-167">Недопустимый тип свойства.</span><span class="sxs-lookup"><span data-stu-id="80d78-167">The property type is invalid.</span></span>
    
<span data-ttu-id="80d78-168">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="80d78-168">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="80d78-169">Тип свойства не типа, вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="80d78-169">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="80d78-170">Замечания</span><span class="sxs-lookup"><span data-stu-id="80d78-170">Remarks</span></span>

<span data-ttu-id="80d78-171">По умолчанию метод **IMAPIProp::CopyTo** копирует или переносит все свойства текущего объекта в конечный объект.</span><span class="sxs-lookup"><span data-stu-id="80d78-171">By default, the **IMAPIProp::CopyTo** method copies or moves all of the current object's properties to a destination object.</span></span> <span data-ttu-id="80d78-172">**CopyTo** используется, когда объект следует скопировать или переместить точно, со всех или большая часть их свойств без изменений.</span><span class="sxs-lookup"><span data-stu-id="80d78-172">**CopyTo** is used when an object should be copied or moved exactly, with all or most of its properties intact.</span></span> 
  
<span data-ttu-id="80d78-173">Вложенными объектами в объекте источника автоматически включается в операцию и перемещаются или копируются полностью.</span><span class="sxs-lookup"><span data-stu-id="80d78-173">Any subobjects in the source object are automatically included in the operation and are copied or moved in their entirety.</span></span> <span data-ttu-id="80d78-174">По умолчанию **CopyTo** перезаписывает любые свойства в целевом объекте, соответствующие свойства из исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="80d78-174">By default, **CopyTo** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="80d78-175">Если какие-либо свойства скопированной или перемещенной уже существует в целевом объекте, существующие свойства перезаписываются новых свойств, пока флаг MAPI_NOREPLACE будет выполнен с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="80d78-175">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="80d78-176">Существующие данные в целевой объект, который не перезаписывается остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="80d78-176">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="80d78-177">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="80d78-177">Notes to implementers</span></span>

<span data-ttu-id="80d78-178">Можно предоставить полная реализация **CopyTo** или зависеть от реализации, предоставляющий MAPI в своем объекте поддержки.</span><span class="sxs-lookup"><span data-stu-id="80d78-178">You can provide a full implementation of **CopyTo** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="80d78-179">Если вы хотите использовать в реализации интерфейса MAPI, вызовите **IMAPISupport::DoCopyTo**.</span><span class="sxs-lookup"><span data-stu-id="80d78-179">If you want to use the MAPI implementation, call **IMAPISupport::DoCopyTo**.</span></span> <span data-ttu-id="80d78-180">Если делегирование обработки для **DoCopyTo** и передаются флаг MAPI_DECLINE_OK, избежать вызова поддержки и вместо этого возвращать MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="80d78-180">However, if you do delegate processing to **DoCopyTo** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="80d78-181">MAPI выполняется звонок с помощью этот флаг, чтобы избежать возможных рекурсии, которая может произойти при копировании папки.</span><span class="sxs-lookup"><span data-stu-id="80d78-181">MAPI will call with this flag to avoid the possible recursion that can happen when folders are copied.</span></span> 
  
<span data-ttu-id="80d78-182">Так как операция копирования может быть длинным, должны отображать индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="80d78-182">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="80d78-183">Используйте реализации [IMAPIProgress](imapiprogressiunknown.md) , переданной в параметре _lpProgress_ , если он существует.</span><span class="sxs-lookup"><span data-stu-id="80d78-183">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="80d78-184">Если _lpProgress_ имеет **значение null**, вызовите метод [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) для использования в реализации интерфейса MAPI.</span><span class="sxs-lookup"><span data-stu-id="80d78-184">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
<span data-ttu-id="80d78-185">Не пытайтесь задать все известные свойства только для чтения в целевом объекте; Вместо этого возвратите MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="80d78-185">Do not attempt to set any known read-only properties in the destination object; return MAPI_E_NO_ACCESS instead.</span></span>
  
<span data-ttu-id="80d78-186">Исходный и целевой объекты следует использовать те же интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="80d78-186">The source and destination objects should use the same interfaces.</span></span> <span data-ttu-id="80d78-187">Возвращает MAPI_E_INVALID_PARAMETER, если _lpInterface_ не задано.</span><span class="sxs-lookup"><span data-stu-id="80d78-187">Return MAPI_E_INVALID_PARAMETER if  _lpInterface_ is not set.</span></span> 
  
<span data-ttu-id="80d78-188">Возвращает MAPI_E_INTERFACE_NOT_SUPPORTED, если не включены все известные интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="80d78-188">Return MAPI_E_INTERFACE_NOT_SUPPORTED if all known interfaces are excluded.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="80d78-189">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="80d78-189">Notes to callers</span></span>

<span data-ttu-id="80d78-190">Не задан флаг MAPI_DECLINE_OK; MAPI используется в его вызовы для сообщения **CopyTo** реализации поставщика хранилища.</span><span class="sxs-lookup"><span data-stu-id="80d78-190">Do not set the MAPI_DECLINE_OK flag; MAPI uses it in its calls to message store provider **CopyTo** implementations.</span></span> 
  
<span data-ttu-id="80d78-191">Так как операции копирования и перемещения может потребоваться времени, путем установки флага MAPI_DIALOG должен запрашивать отображения индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="80d78-191">Because copy and move operations can take time, you should request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="80d78-192">Можно задать параметр _lpProgress_ для внедрения **IMAPIProgress**, если такой существует, или значение **null**.</span><span class="sxs-lookup"><span data-stu-id="80d78-192">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="80d78-193">Если _lpProgress_ имеет **значение null**, **CopyTo** будет использовать индикатор хода выполнения по умолчанию, который предоставляет MAPI.</span><span class="sxs-lookup"><span data-stu-id="80d78-193">If  _lpProgress_ is **null**, **CopyTo** will use the default progress indicator that MAPI provides.</span></span> 
  
<span data-ttu-id="80d78-194">Можно отключить отображение индикатора хода выполнения, не задав флаг MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="80d78-194">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="80d78-195">**CopyTo** будет игнорировать параметры _ulUIParam_ и _lpProgress_ и не будет отображаться значок.</span><span class="sxs-lookup"><span data-stu-id="80d78-195">**CopyTo** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and will not display the indicator.</span></span> 
  
 <span data-ttu-id="80d78-196">**CopyTo** можно сообщить о глобальном уровне и на отдельные ошибки или ошибки, возникающие при работе с одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="80d78-196">**CopyTo** can report global and individual errors, or errors that occur with one or more properties.</span></span> <span data-ttu-id="80d78-197">Эти отдельные ошибки помещаются в структуре **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="80d78-197">These individual errors are placed in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="80d78-198">Отчеты на уровне свойств, передав **значение null**, а не является допустимым указателем, для параметра свойство массива проблема структура об ошибках, можно отключить.</span><span class="sxs-lookup"><span data-stu-id="80d78-198">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="80d78-199">Если вы хотите получать сведения об ошибках, передайте допустимый указатель структура **SPropProblemArray** с помощью параметра _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="80d78-199">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="80d78-200">При **CopyTo** возвращает значение S_OK, проверьте наличие возможных ошибок с помощью отдельных свойств в структуре.</span><span class="sxs-lookup"><span data-stu-id="80d78-200">When **CopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="80d78-201">Когда **CopyTo** возвращает ошибку, не информация возвращается в структуре **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="80d78-201">When **CopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="80d78-202">Вместо этого вызов [IMAPIProp::GetLastError](imapiprop-getlasterror.md) , чтобы получить подробные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="80d78-202">Instead, call [IMAPIProp::GetLastError](imapiprop-getlasterror.md) to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="80d78-203">Если **CopyTo** возвращает значение S_OK, освободите возвращенные структура **SPropProblemArray** путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="80d78-203">If **CopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="80d78-204">При копировании свойств, которые являются уникальными для тип объекта, необходимо убедиться, что в целевой объект является одного типа.</span><span class="sxs-lookup"><span data-stu-id="80d78-204">If you copy properties that are unique to the source object type, you must ensure that the destination object is of the same type.</span></span> <span data-ttu-id="80d78-205">**CopyTo** не запрещает связывания свойства, которые обычно относятся к один тип объекта, с другой тип объекта.</span><span class="sxs-lookup"><span data-stu-id="80d78-205">**CopyTo** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="80d78-206">Зависит от пользователя для копирования свойств, которые нужны для конечного объекта.</span><span class="sxs-lookup"><span data-stu-id="80d78-206">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="80d78-207">К примеру не следует копировать свойства сообщений к контейнеру адресной книги.</span><span class="sxs-lookup"><span data-stu-id="80d78-207">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="80d78-208">Чтобы скопировать между объектами одного типа, убедитесь, что установлен исходный и конечный объект того же типа, путем сравнения указателей объектов или вызов [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="80d78-208">To ensure that you copy between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="80d78-209">Задайте идентификатор интерфейса, на который указывает _lpInterface_ стандартный интерфейс для объекта источника.</span><span class="sxs-lookup"><span data-stu-id="80d78-209">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="80d78-210">Кроме того убедитесь, что тип объекта или свойство **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) является общим для двух объектов.</span><span class="sxs-lookup"><span data-stu-id="80d78-210">Also, be sure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="80d78-211">Например при копировании из сообщения, задайте _lpInterface_ IID_IMessage и **PR_OBJECT_TYPE** объекты MAPI_MESSAGE.</span><span class="sxs-lookup"><span data-stu-id="80d78-211">For example, if you copy from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="80d78-212">Если недопустимый указатель передается в параметре _lpDestObj_ , результаты непредсказуемы.</span><span class="sxs-lookup"><span data-stu-id="80d78-212">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="80d78-213">Исключение свойств на **CopyTo** звонка можно использовать.</span><span class="sxs-lookup"><span data-stu-id="80d78-213">Excluding properties on a **CopyTo** call can be useful.</span></span> <span data-ttu-id="80d78-214">Например некоторые объекты имеют свойства, которые специфичны для одного экземпляра объекта, таких как дата и время доставки сообщения.</span><span class="sxs-lookup"><span data-stu-id="80d78-214">For example, some objects have properties that are specific to a single instance of the object, such as the date and time of message delivery.</span></span> <span data-ttu-id="80d78-215">Чтобы предотвратить копирование время доставки сообщений, при копировании сообщения в другую папку, укажите **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) в массиве свойство tag исключить.</span><span class="sxs-lookup"><span data-stu-id="80d78-215">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="80d78-216">Чтобы исключить список получателей сообщения, добавьте свойство **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) в массиве исключить.</span><span class="sxs-lookup"><span data-stu-id="80d78-216">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="80d78-217">Чтобы исключить вложений сообщений, добавьте свойство **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) в массиве.</span><span class="sxs-lookup"><span data-stu-id="80d78-217">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="80d78-218">Аналогично предотвратить копирование или перемещение папки или иерархии или содержимое таблицы контейнер адресной книги, включая **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) или **PR_CONTAINER_CONTENTS** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) в свойстве тег исключить массива.</span><span class="sxs-lookup"><span data-stu-id="80d78-218">Similarly, prevent the copying or moving of a folder or address book container's hierarchy or contents table by including **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="80d78-219">Чтобы исключить свойства из копии или операции перемещения, включают теги их свойства с помощью параметра _lpExcludeProps_ .</span><span class="sxs-lookup"><span data-stu-id="80d78-219">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="80d78-220">При передаче результаты макрос **PROP_TAG** для построения тега свойства из указанный идентификатор в массиве тега свойства будут исключены все свойства с этим идентификатором.</span><span class="sxs-lookup"><span data-stu-id="80d78-220">If you pass the results of the **PROP_TAG** macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="80d78-221">Например следующую запись в массиве тега свойства вызывает все свойства с идентификатором 0x8002, чтобы исключить, независимо от типа:</span><span class="sxs-lookup"><span data-stu-id="80d78-221">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="80d78-222">Тег свойства **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) нельзя включить в массиве _lpExcludeProps_ .</span><span class="sxs-lookup"><span data-stu-id="80d78-222">The **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag cannot be included in the  _lpExcludeProps_ array.</span></span> 
  
<span data-ttu-id="80d78-223">Полезность функции **CopyTo** для исключения интерфейсы не может быть очевидные полезность исключение свойств.</span><span class="sxs-lookup"><span data-stu-id="80d78-223">The usefulness of the **CopyTo** feature for excluding interfaces is perhaps not as obvious as the usefulness of excluding properties.</span></span> <span data-ttu-id="80d78-224">Интерфейс можно исключить при копировании объект, который не знает группа свойств.</span><span class="sxs-lookup"><span data-stu-id="80d78-224">You can exclude an interface when you copy to an object that has no knowledge of a group of properties.</span></span> <span data-ttu-id="80d78-225">Например при копировании свойств из папки вложения, только свойства, которые вложение может работать с: общие свойства, доступные с любой реализации [IMAPIProp](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="80d78-225">For example, if you copy properties from a folder to an attachment, the only properties that the attachment can work with are the generic properties available with any [IMAPIProp](imapipropiunknown.md) implementation.</span></span> <span data-ttu-id="80d78-226">Исключив [IMAPIFolder](imapifolderimapicontainer.md) из операции копирования, вложение не будет получать более детальную свойства папки.</span><span class="sxs-lookup"><span data-stu-id="80d78-226">By excluding [IMAPIFolder](imapifolderimapicontainer.md) from the copy operation, the attachment will not receive any of the more specific folder properties.</span></span> 
  
<span data-ttu-id="80d78-227">Если используется параметр _rgiidExclude_ следует исключить интерфейс также исключаются все интерфейсы, производные от этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="80d78-227">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="80d78-228">Например за исключением [IMAPIContainer](imapicontainerimapiprop.md) включен, папки или контейнеров адресной книги для исключения, в зависимости от типа поставщика.</span><span class="sxs-lookup"><span data-stu-id="80d78-228">For example, excluding [IMAPIContainer](imapicontainerimapiprop.md) causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="80d78-229">Не исключить **IMAPIProp** или [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) из-за слишком большом числе интерфейсы производные от них.</span><span class="sxs-lookup"><span data-stu-id="80d78-229">Do not exclude **IMAPIProp** or [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) because so many interfaces derive from them.</span></span> 
  
<span data-ttu-id="80d78-230">Пропуск MAPI_E_COMPUTED ошибок, возвращаемых в структуре **SPropProblemArray** в параметре _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="80d78-230">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="80d78-231">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="80d78-231">MFCMAPI reference</span></span>

<span data-ttu-id="80d78-232">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="80d78-232">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="80d78-233">**Файл**</span><span class="sxs-lookup"><span data-stu-id="80d78-233">**File**</span></span>|<span data-ttu-id="80d78-234">**Функция**</span><span class="sxs-lookup"><span data-stu-id="80d78-234">**Function**</span></span>|<span data-ttu-id="80d78-235">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="80d78-235">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="80d78-236">File.cpp</span><span class="sxs-lookup"><span data-stu-id="80d78-236">File.cpp</span></span>  <br/> |<span data-ttu-id="80d78-237">LoadFromMSG</span><span class="sxs-lookup"><span data-stu-id="80d78-237">LoadFromMSG</span></span>  <br/> |<span data-ttu-id="80d78-238">Mfcmapi (en) использует метод **IMAPIProp::CopyTo** для копирования свойств из MSG-файл на объект [IMAPIMessageSite](imapimessagesiteiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="80d78-238">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a .msg file to an [IMAPIMessageSite](imapimessagesiteiunknown.md) object.</span></span>  <br/> |
|<span data-ttu-id="80d78-239">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="80d78-239">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="80d78-240">CFolderDlg::HandlePaste</span><span class="sxs-lookup"><span data-stu-id="80d78-240">CFolderDlg::HandlePaste</span></span>  <br/> |<span data-ttu-id="80d78-241">Mfcmapi (en) использует метод **IMAPIProp::CopyTo** для копирования сообщений конечного свойства из исходного сообщения во время операции вставки.</span><span class="sxs-lookup"><span data-stu-id="80d78-241">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a source message to a target message during a paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="80d78-242">См. также</span><span class="sxs-lookup"><span data-stu-id="80d78-242">See also</span></span>



[<span data-ttu-id="80d78-243">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="80d78-243">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="80d78-244">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="80d78-244">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="80d78-245">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="80d78-245">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="80d78-246">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="80d78-246">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="80d78-247">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="80d78-247">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="80d78-248">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="80d78-248">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="80d78-249">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="80d78-249">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="80d78-250">Каноническое свойство PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="80d78-250">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="80d78-251">Каноническое свойство PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="80d78-251">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="80d78-252">Каноническое свойство PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="80d78-252">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="80d78-253">Каноническое свойство PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="80d78-253">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="80d78-254">Каноническое свойство PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="80d78-254">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="80d78-255">Каноническое свойство PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="80d78-255">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="80d78-256">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="80d78-256">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="80d78-257">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="80d78-257">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="80d78-258">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="80d78-258">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="80d78-259">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="80d78-259">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

