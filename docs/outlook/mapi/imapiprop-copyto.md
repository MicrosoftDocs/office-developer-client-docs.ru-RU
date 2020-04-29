---
title: имапипропкопито
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
# <a name="imapipropcopyto"></a><span data-ttu-id="ce762-103">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="ce762-103">IMAPIProp::CopyTo</span></span>

  
  
<span data-ttu-id="ce762-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce762-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce762-105">Копирует или перемещает все свойства, кроме специально исключенных свойств.</span><span class="sxs-lookup"><span data-stu-id="ce762-105">Copies or moves all properties, except for specifically excluded properties.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="ce762-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce762-106">Parameters</span></span>

 <span data-ttu-id="ce762-107">_Циидексклуде_</span><span class="sxs-lookup"><span data-stu-id="ce762-107">_ciidExclude_</span></span>
  
> <span data-ttu-id="ce762-108">возврата Количество интерфейсов, исключаемых при копировании или перемещении свойств.</span><span class="sxs-lookup"><span data-stu-id="ce762-108">[in] The count of interfaces to exclude when properties are copied or moved.</span></span>
    
 <span data-ttu-id="ce762-109">_ргиидексклуде_</span><span class="sxs-lookup"><span data-stu-id="ce762-109">_rgiidExclude_</span></span>
  
> <span data-ttu-id="ce762-110">возврата Массив идентификаторов интерфейса (ИИДС), указывающих интерфейсы, которые не следует использовать при копировании или перемещении дополнительных данных в целевой объект.</span><span class="sxs-lookup"><span data-stu-id="ce762-110">[in] An array of interface identifiers (IIDs) that specify interfaces that should not be used when supplemental information is copied or moved to the destination object.</span></span>
    
 <span data-ttu-id="ce762-111">_лпексклудепропс_</span><span class="sxs-lookup"><span data-stu-id="ce762-111">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="ce762-112">возврата Указатель на массив тегов свойств, определяющий теги свойств, которые следует исключить из операции копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="ce762-112">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="ce762-113">При передаче **значения NULL** в параметре _лпексклудепропс_ показывается, что все свойства объекта должны быть скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="ce762-113">Passing **null** in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="ce762-114">**CopyTo** возвращает MAPI_E_INVALID_PARAMETER, когда элемент **квалуес** структуры [Спроппроблемаррай](spropproblemarray.md) , на который указывает _лпексклудепропс_ , имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="ce762-114">**CopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropProblemArray](spropproblemarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="ce762-115">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="ce762-115">_ulUIParam_</span></span>
  
> <span data-ttu-id="ce762-116">возврата Дескриптор родительского окна индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="ce762-116">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="ce762-117">_лппрогресс_</span><span class="sxs-lookup"><span data-stu-id="ce762-117">_lpProgress_</span></span>
  
> <span data-ttu-id="ce762-118">возврата Указатель на реализацию индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="ce762-118">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="ce762-119">Если в параметре _лппрогресс_ передается **значение NULL** , MAPI предоставляет реализацию хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="ce762-119">If **null** is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="ce762-120">Параметр _лппрогресс_ игнорируется, если в параметре _ulFlags_ не задан флаг MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="ce762-120">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="ce762-121">_лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="ce762-121">_lpInterface_</span></span>
  
> <span data-ttu-id="ce762-122">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к объекту, на который указывает параметр _лпдестобж_ .</span><span class="sxs-lookup"><span data-stu-id="ce762-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="ce762-123">Параметр _лпинтерфаце_ не должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ce762-123">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="ce762-124">_лпдестобж_</span><span class="sxs-lookup"><span data-stu-id="ce762-124">_lpDestObj_</span></span>
  
> <span data-ttu-id="ce762-125">возврата Указатель на объект, который будет получать скопированные или перемещенные свойства.</span><span class="sxs-lookup"><span data-stu-id="ce762-125">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="ce762-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ce762-126">_ulFlags_</span></span>
  
> <span data-ttu-id="ce762-127">возврата Битовая маска флагов, управляющих операциями копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="ce762-127">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="ce762-128">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="ce762-128">The following flags can be set:</span></span>
    
<span data-ttu-id="ce762-129">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="ce762-129">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="ce762-130">Если **CopyTo** вызывает метод [Имаписуппорт::D окопито](imapisupport-docopyto.md) для обработки операции копирования или перемещения, он должен вместо этого возвращаться сразу со значением ошибки MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="ce762-130">If **CopyTo** calls the [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="ce762-131">Флаг MAPI_DECLINE_OK задается MAPI для ограничения рекурсии.</span><span class="sxs-lookup"><span data-stu-id="ce762-131">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="ce762-132">Клиенты не устанавливают этот флаг.</span><span class="sxs-lookup"><span data-stu-id="ce762-132">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="ce762-133">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="ce762-133">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="ce762-134">Отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="ce762-134">Displays a progress indicator.</span></span>
    
<span data-ttu-id="ce762-135">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="ce762-135">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="ce762-136">**CopyTo** должен выполнять операцию перемещения, а не операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="ce762-136">**CopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="ce762-137">Если этот флаг не установлен, **CopyTo** выполняет операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="ce762-137">When this flag is not set, **CopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="ce762-138">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="ce762-138">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="ce762-139">Существующие свойства в целевом объекте не должны быть перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="ce762-139">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="ce762-140">Если этот флаг не установлен, **CopyTo** перезаписывает существующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ce762-140">When this flag is not set, **CopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="ce762-141">_лпппроблемс_</span><span class="sxs-lookup"><span data-stu-id="ce762-141">_lppProblems_</span></span>
  
> <span data-ttu-id="ce762-142">[вход, выход] На входе указатель на указатель на структуру **спроппроблемаррай** ; в противном случае — **значение NULL**, которое указывает на отсутствие необходимости в сведениях об ошибке.</span><span class="sxs-lookup"><span data-stu-id="ce762-142">[in, out] On input, a pointer to a pointer to an **SPropProblemArray** structure; otherwise, **null**, indicating no need for error information.</span></span> <span data-ttu-id="ce762-143">Если _лпппроблемс_ является допустимым указателем на входе, **CopyTo** возвращает подробные сведения об ошибках при копировании одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="ce762-143">If  _lppProblems_ is a valid pointer on input, **CopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ce762-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce762-144">Return value</span></span>

<span data-ttu-id="ce762-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="ce762-145">S_OK</span></span> 
  
> <span data-ttu-id="ce762-146">Свойства успешно скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="ce762-146">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="ce762-147">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="ce762-147">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="ce762-148">Не удается скопировать подобъект, так как в целевом объекте уже существует **доPR_DISPLAY_NAME** с таким же отображаемым именем, что и в свойстве ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ce762-148">A subobject cannot be copied because a subobject with the same display name — specified by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property — already exists in the destination object.</span></span> 
    
<span data-ttu-id="ce762-149">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="ce762-149">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="ce762-150">Поставщик услуг не реализует операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="ce762-150">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="ce762-151">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="ce762-151">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="ce762-152">Исходный объект, выполняющий операцию копирования или перемещения напрямую или косвенно, содержит целевой объект.</span><span class="sxs-lookup"><span data-stu-id="ce762-152">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="ce762-153">Прежде чем было обнаружено это условие, можно выполнить значительную работу, чтобы исходный и конечный объекты могли быть изменены частично.</span><span class="sxs-lookup"><span data-stu-id="ce762-153">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="ce762-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="ce762-154">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="ce762-155">Интерфейс, определенный параметром _лпинтерфаце_ , не поддерживается целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="ce762-155">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="ce762-156">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ce762-156">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="ce762-157">Предпринята попытка получить доступ к объекту, для которого вызывающая сторона не имеет достаточных разрешений.</span><span class="sxs-lookup"><span data-stu-id="ce762-157">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="ce762-158">Эта ошибка возвращается, если целевой объект совпадает с исходным объектом.</span><span class="sxs-lookup"><span data-stu-id="ce762-158">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="ce762-159">Следующие значения могут возвращаться в структуре **спроппроблемаррай** , но не в качестве возвращаемых значений для **CopyTo**.</span><span class="sxs-lookup"><span data-stu-id="ce762-159">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyTo**.</span></span> <span data-ttu-id="ce762-160">Следующие ошибки относятся к одному свойству:</span><span class="sxs-lookup"><span data-stu-id="ce762-160">The following errors apply to a single property:</span></span>
  
<span data-ttu-id="ce762-161">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="ce762-161">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="ce762-162">Установлен установленный флаг MAPI_UNICODE, а **CopyTo** не поддерживает Юникод, или MAPI_UNICODE не задан, а **CopyTo** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="ce762-162">Either the MAPI_UNICODE flag was set and **CopyTo** does not support Unicode, or MAPI_UNICODE was not set and **CopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="ce762-163">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="ce762-163">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="ce762-164">Абонент не может изменить свойство, так как оно является свойством только для чтения, которое вычисляется владельцем целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="ce762-164">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="ce762-165">Эта ошибка не серьезна; вызывающая сторона должна разрешить продолжение операции копирования.</span><span class="sxs-lookup"><span data-stu-id="ce762-165">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="ce762-166">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce762-166">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="ce762-167">Недопустимый тип свойства.</span><span class="sxs-lookup"><span data-stu-id="ce762-167">The property type is invalid.</span></span>
    
<span data-ttu-id="ce762-168">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="ce762-168">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="ce762-169">Тип свойства не является типом, ожидаемым вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="ce762-169">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ce762-170">Примечания</span><span class="sxs-lookup"><span data-stu-id="ce762-170">Remarks</span></span>

<span data-ttu-id="ce762-171">По умолчанию метод **IMAPIProp:: CopyTo** копирует или перемещает все свойства текущего объекта в целевой объект.</span><span class="sxs-lookup"><span data-stu-id="ce762-171">By default, the **IMAPIProp::CopyTo** method copies or moves all of the current object's properties to a destination object.</span></span> <span data-ttu-id="ce762-172">**CopyTo** используется при точном копировании или перемещении объекта со всеми или большинством его свойств без изменения.</span><span class="sxs-lookup"><span data-stu-id="ce762-172">**CopyTo** is used when an object should be copied or moved exactly, with all or most of its properties intact.</span></span> 
  
<span data-ttu-id="ce762-173">Любые подобъекты в исходном объекте автоматически включаются в операцию, и они полностью копируются или перемещаются.</span><span class="sxs-lookup"><span data-stu-id="ce762-173">Any subobjects in the source object are automatically included in the operation and are copied or moved in their entirety.</span></span> <span data-ttu-id="ce762-174">По умолчанию **CopyTo** перезаписывает все свойства в целевом объекте, которые совпадают со свойствами исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="ce762-174">By default, **CopyTo** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="ce762-175">Если какие-либо из скопированных или перемещенных свойств уже существуют в целевом объекте, существующие свойства перезаписываются новыми свойствами, если не установлен флаг MAPI_NOREPLACE в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="ce762-175">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="ce762-176">Существующие сведения в целевом объекте, которые не перезаписываются, остаются нетронутыми.</span><span class="sxs-lookup"><span data-stu-id="ce762-176">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ce762-177">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="ce762-177">Notes to implementers</span></span>

<span data-ttu-id="ce762-178">Вы можете предоставить полную реализацию **CopyTo** или использовать реализацию MAPI в своем объекте поддержки.</span><span class="sxs-lookup"><span data-stu-id="ce762-178">You can provide a full implementation of **CopyTo** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="ce762-179">Если вы хотите использовать реализацию MAPI, вызовите **имаписуппорт::D окопито**.</span><span class="sxs-lookup"><span data-stu-id="ce762-179">If you want to use the MAPI implementation, call **IMAPISupport::DoCopyTo**.</span></span> <span data-ttu-id="ce762-180">Тем не менее, если вы выполняете обработку делегата в **докопито** , а флаг MAPI_DECLINE_OK передается, избегайте вызова поддержки и возврата MAPI_E_DECLINE_COPY вместо этого.</span><span class="sxs-lookup"><span data-stu-id="ce762-180">However, if you do delegate processing to **DoCopyTo** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="ce762-181">Интерфейс MAPI вызывает этот флаг, чтобы избежать возможной рекурсии при копировании папок.</span><span class="sxs-lookup"><span data-stu-id="ce762-181">MAPI will call with this flag to avoid the possible recursion that can happen when folders are copied.</span></span> 
  
<span data-ttu-id="ce762-182">Так как операция копирования может быть длительной, необходимо отобразить индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="ce762-182">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="ce762-183">Используйте реализацию [IMAPIProgress](imapiprogressiunknown.md) , переданную в параметре _лппрогресс_ , если таковая имеется.</span><span class="sxs-lookup"><span data-stu-id="ce762-183">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="ce762-184">Если _лппрогресс_ имеет **значение NULL**, вызовите метод [имаписуппорт::D ОПРОГРЕССДИАЛОГ](imapisupport-doprogressdialog.md) , чтобы использовать реализацию MAPI.</span><span class="sxs-lookup"><span data-stu-id="ce762-184">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
<span data-ttu-id="ce762-185">Не пытайтесь задать в целевом объекте все известные свойства, предназначенные только для чтения; Вместо этого возвращается MAPI_E_NO_ACCESS.</span><span class="sxs-lookup"><span data-stu-id="ce762-185">Do not attempt to set any known read-only properties in the destination object; return MAPI_E_NO_ACCESS instead.</span></span>
  
<span data-ttu-id="ce762-186">Исходный и конечный объекты должны использовать одни и те же интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="ce762-186">The source and destination objects should use the same interfaces.</span></span> <span data-ttu-id="ce762-187">Возвращает MAPI_E_INVALID_PARAMETER, если _лпинтерфаце_ не задан.</span><span class="sxs-lookup"><span data-stu-id="ce762-187">Return MAPI_E_INVALID_PARAMETER if  _lpInterface_ is not set.</span></span> 
  
<span data-ttu-id="ce762-188">Возвращает MAPI_E_INTERFACE_NOT_SUPPORTED, если все известные интерфейсы исключены.</span><span class="sxs-lookup"><span data-stu-id="ce762-188">Return MAPI_E_INTERFACE_NOT_SUPPORTED if all known interfaces are excluded.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="ce762-189">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="ce762-189">Notes to callers</span></span>

<span data-ttu-id="ce762-190">Не задавайте флаг MAPI_DECLINE_OK; MAPI использует его в вызовах реализаций **CopyTo** для поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="ce762-190">Do not set the MAPI_DECLINE_OK flag; MAPI uses it in its calls to message store provider **CopyTo** implementations.</span></span> 
  
<span data-ttu-id="ce762-191">Так как операции копирования и перемещения могут занимать некоторое время, вы должны запросить отображение индикатора хода выполнения, установив флаг MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="ce762-191">Because copy and move operations can take time, you should request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="ce762-192">Вы можете задать для параметра _лппрогресс_ реализацию **IMAPIProgress**, если таковая имеется, или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ce762-192">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="ce762-193">Если _лппрогресс_ имеет **значение NULL**, то **CopyTo** будет использовать индикатор хода выполнения по умолчанию, предоставляемый MAPI.</span><span class="sxs-lookup"><span data-stu-id="ce762-193">If  _lpProgress_ is **null**, **CopyTo** will use the default progress indicator that MAPI provides.</span></span> 
  
<span data-ttu-id="ce762-194">Вы можете отключить отображение индикатора хода выполнения, не устанавливая флаг MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="ce762-194">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="ce762-195">**CopyTo** будет игнорировать параметры _улуипарам_ и _лппрогресс_ и не будет отображать индикатор.</span><span class="sxs-lookup"><span data-stu-id="ce762-195">**CopyTo** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and will not display the indicator.</span></span> 
  
 <span data-ttu-id="ce762-196">**CopyTo** может сообщать о глобальных и отдельных ошибках, а также об ошибках, произошедших с одним или несколькими свойствами.</span><span class="sxs-lookup"><span data-stu-id="ce762-196">**CopyTo** can report global and individual errors, or errors that occur with one or more properties.</span></span> <span data-ttu-id="ce762-197">Эти отдельные ошибки помещаются в структуру **спроппроблемаррай** .</span><span class="sxs-lookup"><span data-stu-id="ce762-197">These individual errors are placed in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="ce762-198">Вы можете отключить отчеты об ошибках на уровне свойств, передав **значение NULL**вместо допустимого указателя для параметра структуры массива проблем свойств.</span><span class="sxs-lookup"><span data-stu-id="ce762-198">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="ce762-199">Если вы хотите получать сведения об ошибках, передайте допустимый указатель структуры **спроппроблемаррай** в параметр _лпппроблемс_ .</span><span class="sxs-lookup"><span data-stu-id="ce762-199">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="ce762-200">Когда **CopyTo** возвращает S_OK, проверьте наличие ошибок с отдельными свойствами в структуре.</span><span class="sxs-lookup"><span data-stu-id="ce762-200">When **CopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="ce762-201">Когда **CopyTo** возвращает ошибку, в структуре **спроппроблемаррай** никакие данные не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="ce762-201">When **CopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="ce762-202">Вместо этого вызовите [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) , чтобы получить подробные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="ce762-202">Instead, call [IMAPIProp::GetLastError](imapiprop-getlasterror.md) to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="ce762-203">Если **CopyTo** возвращает S_OK, освободите возвращенную структуру **спроппроблемаррай** , вызвав функцию [мапифрибуффер](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="ce762-203">If **CopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="ce762-204">При копировании свойств, которые являются уникальными для типа исходного объекта, необходимо убедиться в том, что целевой объект относится к тому же типу.</span><span class="sxs-lookup"><span data-stu-id="ce762-204">If you copy properties that are unique to the source object type, you must ensure that the destination object is of the same type.</span></span> <span data-ttu-id="ce762-205">**CopyTo** не препятствует связыванию свойств, которые обычно принадлежат одному типу объекта с другим типом объекта.</span><span class="sxs-lookup"><span data-stu-id="ce762-205">**CopyTo** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="ce762-206">Вы можете скопировать свойства, которые имеют смысл для целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="ce762-206">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="ce762-207">Например, не следует копировать свойства сообщений в контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="ce762-207">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="ce762-208">Чтобы гарантировать копирование между объектами одного типа, убедитесь, что исходный объект и целевой объект имеют один и тот же тип, сравнивая указатели объектов или вызывая [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ce762-208">To ensure that you copy between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx).</span></span> <span data-ttu-id="ce762-209">Присвойте идентификатору интерфейса, на который указывает _лпинтерфаце_ , стандартный интерфейс для исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="ce762-209">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="ce762-210">Кроме того, убедитесь, что для двух объектов используется одинаковый тип объекта или свойство **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ce762-210">Also, be sure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="ce762-211">Например, при копировании из сообщения задайте для параметра _лпинтерфаце_ значение IID_IMessage и **PR_OBJECT_TYPE** для обоих объектов MAPI_MESSAGE.</span><span class="sxs-lookup"><span data-stu-id="ce762-211">For example, if you copy from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="ce762-212">Если в параметре _лпдестобж_ передан недопустимый указатель, результаты будут непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="ce762-212">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="ce762-213">Кроме того, можно использовать свойства, не включенные в вызов **CopyTo** .</span><span class="sxs-lookup"><span data-stu-id="ce762-213">Excluding properties on a **CopyTo** call can be useful.</span></span> <span data-ttu-id="ce762-214">Например, у некоторых объектов есть свойства, характерные для одного экземпляра объекта, такие как Дата и время доставки сообщения.</span><span class="sxs-lookup"><span data-stu-id="ce762-214">For example, some objects have properties that are specific to a single instance of the object, such as the date and time of message delivery.</span></span> <span data-ttu-id="ce762-215">Чтобы избежать копирования времени доставки сообщения при копировании сообщения в другую папку, укажите **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) в теге свойства Exclude Array.</span><span class="sxs-lookup"><span data-stu-id="ce762-215">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="ce762-216">Чтобы исключить список получателей сообщения, добавьте свойство **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) в массив Exclude.</span><span class="sxs-lookup"><span data-stu-id="ce762-216">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="ce762-217">Чтобы исключить вложения сообщения, добавьте в массив свойство **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ce762-217">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="ce762-218">Аналогичным образом, не следует блокировать копирование или перемещение папки или таблицы иерархии контейнера или адресной книги, включив **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) или **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) в тег свойства Exclude Array.</span><span class="sxs-lookup"><span data-stu-id="ce762-218">Similarly, prevent the copying or moving of a folder or address book container's hierarchy or contents table by including **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="ce762-219">Чтобы исключить свойства из операции копирования или перемещения, добавьте их теги свойств в параметр _лпексклудепропс_ .</span><span class="sxs-lookup"><span data-stu-id="ce762-219">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="ce762-220">Если вы передаете результаты макроса **PROP_TAG** для создания тега свойства из определенного идентификатора в массиве тегов свойств, все свойства с этим идентификатором будут исключены.</span><span class="sxs-lookup"><span data-stu-id="ce762-220">If you pass the results of the **PROP_TAG** macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="ce762-221">Например, следующая запись в массиве тегов свойств вызывает исключение всех свойств с идентификатором 0x8002, независимо от типа.</span><span class="sxs-lookup"><span data-stu-id="ce762-221">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="ce762-222">Тег свойства **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) не может быть включен в массив _лпексклудепропс_ .</span><span class="sxs-lookup"><span data-stu-id="ce762-222">The **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) property tag cannot be included in the  _lpExcludeProps_ array.</span></span> 
  
<span data-ttu-id="ce762-223">Возможность использования функции **CopyTo** для исключения интерфейсов, вероятно, не очевидна для использования при исключении свойств.</span><span class="sxs-lookup"><span data-stu-id="ce762-223">The usefulness of the **CopyTo** feature for excluding interfaces is perhaps not as obvious as the usefulness of excluding properties.</span></span> <span data-ttu-id="ce762-224">Вы можете исключить интерфейс при копировании в объект, не имеющий сведений о группе свойств.</span><span class="sxs-lookup"><span data-stu-id="ce762-224">You can exclude an interface when you copy to an object that has no knowledge of a group of properties.</span></span> <span data-ttu-id="ce762-225">Например, если вы копируете свойства из папки во вложение, единственными свойствами, с которыми может работать вложение, являются универсальные свойства, доступные в любой реализации [IMAPIProp](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="ce762-225">For example, if you copy properties from a folder to an attachment, the only properties that the attachment can work with are the generic properties available with any [IMAPIProp](imapipropiunknown.md) implementation.</span></span> <span data-ttu-id="ce762-226">При исключении [IMAPIFolder](imapifolderimapicontainer.md) из операции копирования вложение не будет получать какие – либо более конкретные свойства папки.</span><span class="sxs-lookup"><span data-stu-id="ce762-226">By excluding [IMAPIFolder](imapifolderimapicontainer.md) from the copy operation, the attachment will not receive any of the more specific folder properties.</span></span> 
  
<span data-ttu-id="ce762-227">При использовании параметра _ргиидексклуде_ для исключения интерфейса он также исключает все интерфейсы, полученные из этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ce762-227">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="ce762-228">Например, исключение [IMAPIContainer](imapicontainerimapiprop.md) вызывает исключение папок или контейнеров адресных книг, в зависимости от типа поставщика.</span><span class="sxs-lookup"><span data-stu-id="ce762-228">For example, excluding [IMAPIContainer](imapicontainerimapiprop.md) causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="ce762-229">Не следует исключать **IMAPIProp** или [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) , так как многие интерфейсы являются производными от них.</span><span class="sxs-lookup"><span data-stu-id="ce762-229">Do not exclude **IMAPIProp** or [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) because so many interfaces derive from them.</span></span> 
  
<span data-ttu-id="ce762-230">Пропускать ошибки MAPI_E_COMPUTED, возвращаемые в структуре **спроппроблемаррай** в параметре _лпппроблемс_ .</span><span class="sxs-lookup"><span data-stu-id="ce762-230">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ce762-231">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ce762-231">MFCMAPI reference</span></span>

<span data-ttu-id="ce762-232">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="ce762-232">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ce762-233">**Файл**</span><span class="sxs-lookup"><span data-stu-id="ce762-233">**File**</span></span>|<span data-ttu-id="ce762-234">**Функция**</span><span class="sxs-lookup"><span data-stu-id="ce762-234">**Function**</span></span>|<span data-ttu-id="ce762-235">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="ce762-235">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ce762-236">Файл. cpp</span><span class="sxs-lookup"><span data-stu-id="ce762-236">File.cpp</span></span>  <br/> |<span data-ttu-id="ce762-237">лоадфроммсг</span><span class="sxs-lookup"><span data-stu-id="ce762-237">LoadFromMSG</span></span>  <br/> |<span data-ttu-id="ce762-238">MFCMAPI использует метод **IMAPIProp:: CopyTo** для копирования свойств из MSG – файла в объект [имапимессажесите](imapimessagesiteiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="ce762-238">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a .msg file to an [IMAPIMessageSite](imapimessagesiteiunknown.md) object.</span></span>  <br/> |
|<span data-ttu-id="ce762-239">Фолдердлг. cpp</span><span class="sxs-lookup"><span data-stu-id="ce762-239">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="ce762-240">Кфолдердлг:: Хандлепасте</span><span class="sxs-lookup"><span data-stu-id="ce762-240">CFolderDlg::HandlePaste</span></span>  <br/> |<span data-ttu-id="ce762-241">MFCMAPI использует метод **IMAPIProp:: CopyTo** для копирования свойств из исходного сообщения в целевое сообщение во время операции вставки.</span><span class="sxs-lookup"><span data-stu-id="ce762-241">MFCMAPI uses the **IMAPIProp::CopyTo** method to copy properties from a source message to a target message during a paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce762-242">См. также</span><span class="sxs-lookup"><span data-stu-id="ce762-242">See also</span></span>



[<span data-ttu-id="ce762-243">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="ce762-243">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="ce762-244">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="ce762-244">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="ce762-245">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ce762-245">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="ce762-246">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ce762-246">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="ce762-247">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="ce762-247">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="ce762-248">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="ce762-248">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="ce762-249">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ce762-249">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ce762-250">Каноническое свойство PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="ce762-250">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="ce762-251">Каноническое свойство PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="ce762-251">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="ce762-252">Каноническое свойство PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="ce762-252">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="ce762-253">Каноническое свойство PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="ce762-253">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="ce762-254">Каноническое свойство PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="ce762-254">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="ce762-255">Каноническое свойство PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="ce762-255">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="ce762-256">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="ce762-256">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="ce762-257">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="ce762-257">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="ce762-258">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ce762-258">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="ce762-259">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="ce762-259">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

