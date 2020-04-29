---
title: имапипропкопипропс
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
# <a name="imapipropcopyprops"></a><span data-ttu-id="b0a64-103">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="b0a64-103">IMAPIProp::CopyProps</span></span>

  
  
<span data-ttu-id="b0a64-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0a64-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0a64-105">Копирование или перемещение выбранных свойств.</span><span class="sxs-lookup"><span data-stu-id="b0a64-105">Copies or moves selected properties.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="b0a64-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0a64-106">Parameters</span></span>

 <span data-ttu-id="b0a64-107">_лпинклудепропс_</span><span class="sxs-lookup"><span data-stu-id="b0a64-107">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="b0a64-108">возврата Указатель на массив тегов свойств, указывающий свойства, которые необходимо скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="b0a64-108">[in] A pointer to a property tag array that specifies the properties to copy or move.</span></span> <span data-ttu-id="b0a64-109">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) невозможно включить в массив.</span><span class="sxs-lookup"><span data-stu-id="b0a64-109">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) cannot be included in the array.</span></span> <span data-ttu-id="b0a64-110">Параметр _лпинклудепропс_ не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b0a64-110">The  _lpIncludeProps_ parameter cannot be **null**.</span></span>
    
 <span data-ttu-id="b0a64-111">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="b0a64-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="b0a64-112">возврата Дескриптор родительского окна индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="b0a64-112">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="b0a64-113">_лппрогресс_</span><span class="sxs-lookup"><span data-stu-id="b0a64-113">_lpProgress_</span></span>
  
> <span data-ttu-id="b0a64-114">возврата Указатель на реализацию индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="b0a64-114">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="b0a64-115">Если в параметре _лппрогресс_ передается **значение NULL** , индикатор хода выполнения отображается с помощью реализации MAPI.</span><span class="sxs-lookup"><span data-stu-id="b0a64-115">If **null** is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="b0a64-116">Параметр _лппрогресс_ игнорируется, если в параметре _ulFlags_ не задан флаг MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="b0a64-116">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="b0a64-117">_лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="b0a64-117">_lpInterface_</span></span>
  
> <span data-ttu-id="b0a64-118">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который должен использоваться для доступа к объекту, на который указывает параметр _лпдестобж_ .</span><span class="sxs-lookup"><span data-stu-id="b0a64-118">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="b0a64-119">Параметр _лпинтерфаце_ не должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b0a64-119">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="b0a64-120">_лпдестобж_</span><span class="sxs-lookup"><span data-stu-id="b0a64-120">_lpDestObj_</span></span>
  
> <span data-ttu-id="b0a64-121">возврата Указатель на объект, который будет получать скопированные или перемещенные свойства.</span><span class="sxs-lookup"><span data-stu-id="b0a64-121">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="b0a64-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b0a64-122">_ulFlags_</span></span>
  
> <span data-ttu-id="b0a64-123">возврата Битовая маска флагов, управляющих операциями копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="b0a64-123">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="b0a64-124">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="b0a64-124">The following flags can be set:</span></span>
    
<span data-ttu-id="b0a64-125">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="b0a64-125">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="b0a64-126">Если **копипропс** вызывает метод [Имаписуппорт::D окопипропс](imapisupport-docopyprops.md) для обработки операции копирования или перемещения, он должен вместо этого возвращаться сразу со значением ошибки MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="b0a64-126">If **CopyProps** calls the [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="b0a64-127">Флаг MAPI_DECLINE_OK задается MAPI для ограничения рекурсии.</span><span class="sxs-lookup"><span data-stu-id="b0a64-127">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="b0a64-128">Клиенты не устанавливают этот флаг.</span><span class="sxs-lookup"><span data-stu-id="b0a64-128">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="b0a64-129">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="b0a64-129">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="b0a64-130">Отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="b0a64-130">Displays a progress indicator.</span></span>
    
<span data-ttu-id="b0a64-131">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="b0a64-131">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="b0a64-132">**Копипропс** должен выполнять операцию перемещения, а не операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="b0a64-132">**CopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="b0a64-133">Если этот флаг не задан, **копипропс** выполняет операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="b0a64-133">When this flag is not set, **CopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="b0a64-134">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="b0a64-134">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="b0a64-135">Существующие свойства в целевом объекте не должны быть перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="b0a64-135">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="b0a64-136">Если этот флаг не задан, **копипропс** перезаписывает существующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b0a64-136">When this flag is not set, **CopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="b0a64-137">_лпппроблемс_</span><span class="sxs-lookup"><span data-stu-id="b0a64-137">_lppProblems_</span></span>
  
> <span data-ttu-id="b0a64-138">[вход, выход] На входе указатель на указатель на структуру [спроппроблемаррай](spropproblemarray.md) ; в противном случае — **значение NULL**, указывающее, что нет необходимости в сведениях об ошибке.</span><span class="sxs-lookup"><span data-stu-id="b0a64-138">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, **null**, indicating that there is no need for error information.</span></span> <span data-ttu-id="b0a64-139">Если _лпппроблемс_ является допустимым указателем на входе, **копипропс** возвращает подробные сведения об ошибках при копировании одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="b0a64-139">If  _lppProblems_ is a valid pointer on input, **CopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b0a64-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0a64-140">Return value</span></span>

<span data-ttu-id="b0a64-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="b0a64-141">S_OK</span></span> 
  
> <span data-ttu-id="b0a64-142">Свойства успешно скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="b0a64-142">Properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="b0a64-143">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="b0a64-143">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="b0a64-144">Невозможно скопировать подобъект, так как в целевом объекте уже существует **доPR_DISPLAY_NAME** с таким же отображаемым именем, которое определяется свойством ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b0a64-144">A subobject cannot be copied because a subobject with the same display name, defined by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, already exists in the destination object.</span></span> 
    
<span data-ttu-id="b0a64-145">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="b0a64-145">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="b0a64-146">Поставщик услуг не реализует операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="b0a64-146">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="b0a64-147">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="b0a64-147">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="b0a64-148">Исходный объект, выполняющий операцию копирования или перемещения напрямую или косвенно, содержит целевой объект.</span><span class="sxs-lookup"><span data-stu-id="b0a64-148">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="b0a64-149">Прежде чем было обнаружено это условие, можно выполнить значительную работу, чтобы исходный и конечный объекты могли быть изменены частично.</span><span class="sxs-lookup"><span data-stu-id="b0a64-149">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="b0a64-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="b0a64-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="b0a64-151">Интерфейс, определенный параметром _лпинтерфаце_ , не поддерживается целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="b0a64-151">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="b0a64-152">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b0a64-152">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="b0a64-153">Предпринята попытка получить доступ к объекту, для которого вызывающая сторона не имеет достаточных разрешений.</span><span class="sxs-lookup"><span data-stu-id="b0a64-153">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="b0a64-154">Эта ошибка возвращается, если целевой объект совпадает с исходным объектом.</span><span class="sxs-lookup"><span data-stu-id="b0a64-154">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="b0a64-155">Следующие значения могут возвращаться в структуре **спроппроблемаррай** , но не в качестве возвращаемых значений для **копипропс**.</span><span class="sxs-lookup"><span data-stu-id="b0a64-155">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyProps**.</span></span> <span data-ttu-id="b0a64-156">Эти ошибки относятся к одному свойству.</span><span class="sxs-lookup"><span data-stu-id="b0a64-156">These errors apply to a single property.</span></span>
  
<span data-ttu-id="b0a64-157">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="b0a64-157">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="b0a64-158">Установлен установленный флаг MAPI_UNICODE и **копипропс** не поддерживает Юникод, или MAPI_UNICODE не задан и **Копипропс** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="b0a64-158">Either the MAPI_UNICODE flag was set and **CopyProps** does not support Unicode, or MAPI_UNICODE was not set and **CopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="b0a64-159">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="b0a64-159">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="b0a64-160">Абонент не может изменить свойство, так как оно является свойством только для чтения, которое вычисляется владельцем целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="b0a64-160">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="b0a64-161">Эта ошибка не серьезна; вызывающая сторона должна разрешить продолжение операции копирования.</span><span class="sxs-lookup"><span data-stu-id="b0a64-161">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="b0a64-162">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="b0a64-162">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="b0a64-163">Недопустимый тип свойства.</span><span class="sxs-lookup"><span data-stu-id="b0a64-163">The property type is invalid.</span></span>
    
<span data-ttu-id="b0a64-164">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="b0a64-164">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="b0a64-165">Тип свойства не является типом, ожидаемым вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="b0a64-165">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b0a64-166">Примечания</span><span class="sxs-lookup"><span data-stu-id="b0a64-166">Remarks</span></span>

<span data-ttu-id="b0a64-167">Метод **IMAPIProp:: копипропс** копирует или перемещает выбранные свойства из текущего объекта в целевой объект.</span><span class="sxs-lookup"><span data-stu-id="b0a64-167">The **IMAPIProp::CopyProps** method copies or moves selected properties from the current object to a destination object.</span></span> <span data-ttu-id="b0a64-168">**Копипропс** используется в основном для ответа и пересылки сообщений, в которых только некоторые свойства из исходного сообщения передаются вместе с ответом или с переадресованной копией.</span><span class="sxs-lookup"><span data-stu-id="b0a64-168">**CopyProps** is used mainly for replying to and forwarding messages, where only some of the properties from the original message travel with the reply or forwarded copy.</span></span> 
  
<span data-ttu-id="b0a64-169">Любые подобъекты в исходном объекте автоматически включаются в операцию и копируются или перемещаются целиком, независимо от использования свойств, указанных в структуре [спроптагаррай](sproptagarray.md) .</span><span class="sxs-lookup"><span data-stu-id="b0a64-169">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety, regardless of the use of properties indicated by the [SPropTagArray](sproptagarray.md) structure.</span></span> <span data-ttu-id="b0a64-170">По умолчанию **копипропс** перезаписывает все свойства в целевом объекте, которые совпадают со свойствами исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="b0a64-170">By default, **CopyProps** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="b0a64-171">Если какие-либо из скопированных или перемещенных свойств уже существуют в целевом объекте, существующие свойства перезаписываются новыми свойствами, если не установлен флаг MAPI_NOREPLACE в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="b0a64-171">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="b0a64-172">Существующие сведения в целевом объекте, которые не перезаписываются, остаются нетронутыми.</span><span class="sxs-lookup"><span data-stu-id="b0a64-172">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b0a64-173">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="b0a64-173">Notes to implementers</span></span>

<span data-ttu-id="b0a64-174">Вы можете предоставить полную реализацию **копипропс** или использовать реализацию MAPI в своем объекте поддержки.</span><span class="sxs-lookup"><span data-stu-id="b0a64-174">You can provide a full implementation of **CopyProps** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="b0a64-175">Если вы хотите использовать реализацию MAPI, вызовите метод **имаписуппорт::D окопипропс** .</span><span class="sxs-lookup"><span data-stu-id="b0a64-175">If you want to use the MAPI implementation, call the **IMAPISupport::DoCopyProps** method.</span></span> <span data-ttu-id="b0a64-176">Тем не менее, если вы выполняете обработку делегата в **докопипропс** , а флаг MAPI_DECLINE_OK передается, избегайте вызова поддержки и возврата MAPI_E_DECLINE_COPY вместо этого.</span><span class="sxs-lookup"><span data-stu-id="b0a64-176">However, if you do delegate processing to **DoCopyProps** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="b0a64-177">Этот флаг будет вызываться с помощью MAPI, чтобы избежать возможной рекурсии, которая может возникнуть при копировании папок.</span><span class="sxs-lookup"><span data-stu-id="b0a64-177">You will be called with this flag by MAPI to avoid the possible recursion that can occur when you copy folders.</span></span> 
  
<span data-ttu-id="b0a64-178">Так как операция копирования может быть длительной, необходимо отобразить индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="b0a64-178">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="b0a64-179">Используйте реализацию [IMAPIProgress](imapiprogressiunknown.md) , которая передается в параметре _лппрогресс_ , если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="b0a64-179">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation that is passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="b0a64-180">Если _лппрогресс_ имеет **значение NULL**, вызовите метод [имаписуппорт::D ОПРОГРЕССДИАЛОГ](imapisupport-doprogressdialog.md) , чтобы использовать реализацию MAPI.</span><span class="sxs-lookup"><span data-stu-id="b0a64-180">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b0a64-181">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="b0a64-181">Notes to callers</span></span>

<span data-ttu-id="b0a64-182">Не задавайте флаг MAPI_DECLINE_OK; Он используется MAPI в вызовах реализаций поставщика хранилища сообщений **копипропс** .</span><span class="sxs-lookup"><span data-stu-id="b0a64-182">Do not set the MAPI_DECLINE_OK flag; it is used by MAPI in its calls to message store provider **CopyProps** implementations.</span></span> 
  
<span data-ttu-id="b0a64-183">Так как операции копирования и перемещения могут занимать некоторое время, рекомендуется запрашивать отображение индикатора хода выполнения путем установки флага MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="b0a64-183">Because copy and move operations can take time, it is wise to request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="b0a64-184">Вы можете задать для параметра _лппрогресс_ реализацию **IMAPIProgress**, если таковая имеется, или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b0a64-184">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="b0a64-185">Если _лппрогресс_ имеет **значение NULL**, **копипропс** будет использовать индикатор хода выполнения по умолчанию, предоставляемый MAPI.</span><span class="sxs-lookup"><span data-stu-id="b0a64-185">If  _lpProgress_ is **null**, **CopyProps** will use the default progress indicator provided by MAPI.</span></span> 
  
<span data-ttu-id="b0a64-186">Вы можете отключить отображение индикатора хода выполнения, не устанавливая флаг MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="b0a64-186">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="b0a64-187">**Копипропс** будет игнорировать параметры _улуипарам_ и _лппрогресс_ и не отображать индикатор.</span><span class="sxs-lookup"><span data-stu-id="b0a64-187">**CopyProps** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and avoid displaying the indicator.</span></span> 
  
 <span data-ttu-id="b0a64-188">**Копипропс** может сообщать о глобальных и индивидуальных ошибках, а также об ошибках, происходящих с одним или несколькими свойствами.</span><span class="sxs-lookup"><span data-stu-id="b0a64-188">**CopyProps** can report global and individual errors, or errors that occur with one or more of the properties.</span></span> <span data-ttu-id="b0a64-189">Эти отдельные ошибки помещаются в структуру **спроппроблемаррай** .</span><span class="sxs-lookup"><span data-stu-id="b0a64-189">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="b0a64-190">Вы можете отключить отчеты об ошибках на уровне свойств, передав **значение NULL**вместо допустимого указателя для параметра структуры массива проблем свойств.</span><span class="sxs-lookup"><span data-stu-id="b0a64-190">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="b0a64-191">Если вы хотите получать сведения об ошибках, передайте допустимый указатель структуры **спроппроблемаррай** в параметр _лпппроблемс_ .</span><span class="sxs-lookup"><span data-stu-id="b0a64-191">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="b0a64-192">Когда **копипропс** возвращает S_OK, проверьте возможные ошибки с отдельными свойствами в структуре.</span><span class="sxs-lookup"><span data-stu-id="b0a64-192">When **CopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="b0a64-193">Когда **копипропс** возвращает ошибку, в структуре **спроппроблемаррай** не возвращается никакой информации.</span><span class="sxs-lookup"><span data-stu-id="b0a64-193">When **CopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="b0a64-194">Вместо этого вызовите метод [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) , чтобы получить подробные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="b0a64-194">Instead, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="b0a64-195">Если **копипропс** возвращает S_OK, освободите возвращаемую структуру **спроппроблемаррай** , вызвав функцию [мапифрибуффер](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="b0a64-195">If **CopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="b0a64-196">При копировании свойств, которые являются уникальными для типа исходного объекта, необходимо убедиться в том, что целевой объект относится к тому же типу.</span><span class="sxs-lookup"><span data-stu-id="b0a64-196">If you are copying properties that are unique to the source object type, you must make sure that the destination object is of the same type.</span></span> <span data-ttu-id="b0a64-197">**Копипропс** не запрещает присоединение свойств, которые обычно относятся к одному типу объекта, с другим типом объекта.</span><span class="sxs-lookup"><span data-stu-id="b0a64-197">**CopyProps** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="b0a64-198">Вы можете скопировать свойства, которые имеют смысл для целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="b0a64-198">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="b0a64-199">Например, не следует копировать свойства сообщений в контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b0a64-199">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="b0a64-200">Чтобы гарантировать копирование между объектами одного типа, убедитесь, что исходный объект и целевой объект имеют один и тот же тип, либо сравнивая указатели объектов, либо вызывая метод [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b0a64-200">To ensure that you are copying between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="b0a64-201">Присвойте идентификатору интерфейса, на который указывает _лпинтерфаце_ , стандартный интерфейс для исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="b0a64-201">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="b0a64-202">Кроме того, убедитесь, что для двух объектов используется одинаковый тип объекта или свойство **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b0a64-202">Also, ensure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="b0a64-203">Например, при копировании из сообщения задайте для параметра _лпинтерфаце_ значение IID_IMessage и **PR_OBJECT_TYPE** для обоих объектов MAPI_MESSAGE.</span><span class="sxs-lookup"><span data-stu-id="b0a64-203">For example, if you are copying from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="b0a64-204">Если в параметре _лпдестобж_ передан недопустимый указатель, результаты будут непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="b0a64-204">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="b0a64-205">Чтобы скопировать список получателей сообщения, вызовите метод **копипропс** сообщения и добавьте свойство **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) в массиве тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="b0a64-205">To copy a message's recipient list, call the message's **CopyProps** method and include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array.</span></span> <span data-ttu-id="b0a64-206">Чтобы скопировать вложения сообщения, включите свойство **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b0a64-206">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="b0a64-207">Чтобы скопировать иерархию или таблицу контента контейнера папки или адресной книги, включите свойства **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) или **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) в массиве тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="b0a64-207">To copy a folder or address book container's hierarchy or contents table, include the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) properties in the property tag array.</span></span> <span data-ttu-id="b0a64-208">Чтобы включить таблицу с содержимым, связанным с папкой, включите в массив свойство **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b0a64-208">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b0a64-209">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b0a64-209">MFCMAPI reference</span></span>

<span data-ttu-id="b0a64-210">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="b0a64-210">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b0a64-211">**Файл**</span><span class="sxs-lookup"><span data-stu-id="b0a64-211">**File**</span></span>|<span data-ttu-id="b0a64-212">**Функция**</span><span class="sxs-lookup"><span data-stu-id="b0a64-212">**Function**</span></span>|<span data-ttu-id="b0a64-213">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="b0a64-213">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b0a64-214">Мапифунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="b0a64-214">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="b0a64-215">копинамедпропс</span><span class="sxs-lookup"><span data-stu-id="b0a64-215">CopyNamedProps</span></span>  <br/> |<span data-ttu-id="b0a64-216">MFCMAPI использует метод **IMAPIProp:: копипропс** для копирования именованных свойств из одного сообщения в другое.</span><span class="sxs-lookup"><span data-stu-id="b0a64-216">MFCMAPI uses the **IMAPIProp::CopyProps** method to copy named properties from one message to another.</span></span>  <br/> |
|<span data-ttu-id="b0a64-217">Синглемапипроплистктрл. cpp</span><span class="sxs-lookup"><span data-stu-id="b0a64-217">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="b0a64-218">Ксинглемапипроплистктрл:: Онпастепроперти</span><span class="sxs-lookup"><span data-stu-id="b0a64-218">CSingleMAPIPropListCtrl::OnPasteProperty</span></span>  <br/> |<span data-ttu-id="b0a64-219">MFCMAPI использует метод **IMAPIProp:: копипропс** для вставки свойства, которое было скопировано из другого объекта.</span><span class="sxs-lookup"><span data-stu-id="b0a64-219">MFCMAPI uses the **IMAPIProp::CopyProps** method to paste a property that has been copied from another object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b0a64-220">См. также</span><span class="sxs-lookup"><span data-stu-id="b0a64-220">See also</span></span>



[<span data-ttu-id="b0a64-221">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="b0a64-221">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="b0a64-222">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b0a64-222">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="b0a64-223">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="b0a64-223">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="b0a64-224">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b0a64-224">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="b0a64-225">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="b0a64-225">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
  
[<span data-ttu-id="b0a64-226">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="b0a64-226">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="b0a64-227">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b0a64-227">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b0a64-228">Каноническое свойство PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="b0a64-228">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="b0a64-229">Каноническое свойство PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="b0a64-229">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="b0a64-230">Каноническое свойство PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="b0a64-230">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="b0a64-231">Каноническое свойство PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="b0a64-231">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="b0a64-232">Каноническое свойство PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="b0a64-232">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="b0a64-233">Каноническое свойство PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="b0a64-233">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="b0a64-234">Каноническое свойство PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="b0a64-234">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="b0a64-235">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="b0a64-235">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="b0a64-236">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="b0a64-236">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="b0a64-237">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b0a64-237">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="b0a64-238">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="b0a64-238">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

