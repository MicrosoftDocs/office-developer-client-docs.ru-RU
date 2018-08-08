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
ms.openlocfilehash: ff8f13a1dcf678e1d05b6e8e083597156422b83d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809045"
---
# <a name="imapipropcopyprops"></a><span data-ttu-id="89969-103">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="89969-103">IMAPIProp::CopyProps</span></span>

  
  
<span data-ttu-id="89969-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="89969-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="89969-105">Копирование или Перемещение выбранных свойств.</span><span class="sxs-lookup"><span data-stu-id="89969-105">Copies or moves selected properties.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="89969-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="89969-106">Parameters</span></span>

 <span data-ttu-id="89969-107">_lpIncludeProps_</span><span class="sxs-lookup"><span data-stu-id="89969-107">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="89969-108">[in] Указатель в массив тега свойства, который задает свойства, которые нужно скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="89969-108">[in] A pointer to a property tag array that specifies the properties to copy or move.</span></span> <span data-ttu-id="89969-109">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) нельзя включить в массиве.</span><span class="sxs-lookup"><span data-stu-id="89969-109">**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) cannot be included in the array.</span></span> <span data-ttu-id="89969-110">Параметр _lpIncludeProps_ не может быть **null**.</span><span class="sxs-lookup"><span data-stu-id="89969-110">The  _lpIncludeProps_ parameter cannot be **null**.</span></span>
    
 <span data-ttu-id="89969-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="89969-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="89969-112">[in] Дескриптор родительского окна индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="89969-112">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="89969-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="89969-113">_lpProgress_</span></span>
  
> <span data-ttu-id="89969-114">[in] Указатель на реализацию индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="89969-114">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="89969-115">Если **значение null,** передается в параметре _lpProgress_ , с помощью реализации интерфейса MAPI отображается индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="89969-115">If **null** is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="89969-116">Параметр _lpProgress_ игнорируется, пока флаг MAPI_DIALOG будет выполнен с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="89969-116">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="89969-117">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="89969-117">_lpInterface_</span></span>
  
> <span data-ttu-id="89969-118">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который должен использоваться для доступа к объекту, на который указывает параметр _lpDestObj_ .</span><span class="sxs-lookup"><span data-stu-id="89969-118">[in] A pointer to the interface identifier (IID) that represents the interface that must be used to access the object pointed to by the  _lpDestObj_ parameter.</span></span> <span data-ttu-id="89969-119">Параметр _lpInterface_ не должно быть **значение null**.</span><span class="sxs-lookup"><span data-stu-id="89969-119">The  _lpInterface_ parameter must not be **null**.</span></span>
    
 <span data-ttu-id="89969-120">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="89969-120">_lpDestObj_</span></span>
  
> <span data-ttu-id="89969-121">[in] Указатель на объект для получения свойств копируемые или перемещения.</span><span class="sxs-lookup"><span data-stu-id="89969-121">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="89969-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="89969-122">_ulFlags_</span></span>
  
> <span data-ttu-id="89969-123">[in] Битовая маска флаги, который определяет операцию копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="89969-123">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="89969-124">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="89969-124">The following flags can be set:</span></span>
    
<span data-ttu-id="89969-125">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="89969-125">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="89969-126">Если **CopyProps** вызывает метод [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) для обработки копировать или перемещать операции, она немедленно вместо этого возвращает со значением ошибки MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="89969-126">If **CopyProps** calls the [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method to handle the copy or move operation, it should instead return immediately with the error value MAPI_E_DECLINE_COPY.</span></span> <span data-ttu-id="89969-127">Флаг MAPI_DECLINE_OK задается MAPI для ограничения рекурсии.</span><span class="sxs-lookup"><span data-stu-id="89969-127">The MAPI_DECLINE_OK flag is set by MAPI to limit recursion.</span></span> <span data-ttu-id="89969-128">Клиенты не задан этот флаг.</span><span class="sxs-lookup"><span data-stu-id="89969-128">Clients do not set this flag.</span></span> 
    
<span data-ttu-id="89969-129">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="89969-129">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="89969-130">Отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="89969-130">Displays a progress indicator.</span></span>
    
<span data-ttu-id="89969-131">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="89969-131">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="89969-132">**CopyProps** следует выполнять операции перемещения вместо операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="89969-132">**CopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="89969-133">Если этот флаг не задан, **CopyProps** выполняет операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="89969-133">When this flag is not set, **CopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="89969-134">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="89969-134">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="89969-135">Не следует перезаписывать существующие свойства в целевой объект.</span><span class="sxs-lookup"><span data-stu-id="89969-135">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="89969-136">Если этот флаг не задан, **CopyProps** перезаписывает существующие свойства.</span><span class="sxs-lookup"><span data-stu-id="89969-136">When this flag is not set, **CopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="89969-137">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="89969-137">_lppProblems_</span></span>
  
> <span data-ttu-id="89969-138">[in, out] На входе указатель указатель на структуру [SPropProblemArray](spropproblemarray.md) ; в противном случае — **значение null**, указывающего на то, что нет необходимости для получения сведений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="89969-138">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, **null**, indicating that there is no need for error information.</span></span> <span data-ttu-id="89969-139">Если _lppProblems_ допустимый указатель на входные данные, **CopyProps** возвращает подробные сведения об ошибках в копирование одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="89969-139">If  _lppProblems_ is a valid pointer on input, **CopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="89969-140">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="89969-140">Return value</span></span>

<span data-ttu-id="89969-141">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="89969-141">S_OK</span></span> 
  
> <span data-ttu-id="89969-142">Свойства успешно копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="89969-142">Properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="89969-143">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="89969-143">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="89969-144">Не удается скопировать вложенные объекты, так как вложенные объекты с одинаковыми именами display, определенные в свойстве **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) уже существует в целевой объект.</span><span class="sxs-lookup"><span data-stu-id="89969-144">A subobject cannot be copied because a subobject with the same display name, defined by the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, already exists in the destination object.</span></span> 
    
<span data-ttu-id="89969-145">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="89969-145">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="89969-146">Поставщик услуг не реализует операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="89969-146">The service provider does not implement the copy operation.</span></span>
    
<span data-ttu-id="89969-147">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="89969-147">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="89969-148">Исходный объект для выполнения операции копирования или перемещения прямо или косвенно содержит целевой объект.</span><span class="sxs-lookup"><span data-stu-id="89969-148">The source object performing the copy or move operation directly or indirectly contains the destination object.</span></span> <span data-ttu-id="89969-149">Важные может быть выполнено перед был обнаружен это условие, поэтому исходный и целевой объекты частично могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="89969-149">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="89969-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="89969-150">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="89969-151">Интерфейс, определенного параметром _lpInterface_ не поддерживается в целевой объект.</span><span class="sxs-lookup"><span data-stu-id="89969-151">The interface identified by the  _lpInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="89969-152">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="89969-152">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="89969-153">Предпринята попытка получить доступ к объекту, для которого вызывающий не имеет разрешений.</span><span class="sxs-lookup"><span data-stu-id="89969-153">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="89969-154">Эта ошибка возвращается в том случае, если в целевой объект совпадает с исходным объектом.</span><span class="sxs-lookup"><span data-stu-id="89969-154">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="89969-155">Возможные значения могут быть возвращены в структуре **SPropProblemArray** , но не как возвращаемые значения для **CopyProps**.</span><span class="sxs-lookup"><span data-stu-id="89969-155">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **CopyProps**.</span></span> <span data-ttu-id="89969-156">Эти ошибки относятся к одному свойству.</span><span class="sxs-lookup"><span data-stu-id="89969-156">These errors apply to a single property.</span></span>
  
<span data-ttu-id="89969-157">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="89969-157">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="89969-158">Либо был установлен флажок MAPI_UNICODE и **CopyProps** не поддерживает Юникод, или MAPI_UNICODE не было установлено и **CopyProps** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="89969-158">Either the MAPI_UNICODE flag was set and **CopyProps** does not support Unicode, or MAPI_UNICODE was not set and **CopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="89969-159">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="89969-159">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="89969-160">Невозможно изменить свойство вызывающим абонентом, так как он является свойством только для чтения, вычисленный владельцем конечного объекта.</span><span class="sxs-lookup"><span data-stu-id="89969-160">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="89969-161">Эта ошибка не является очень неблагоприятных; вызывающего абонента, должна поддерживать операции копирования для продолжения.</span><span class="sxs-lookup"><span data-stu-id="89969-161">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="89969-162">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="89969-162">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="89969-163">Недопустимый тип свойства.</span><span class="sxs-lookup"><span data-stu-id="89969-163">The property type is invalid.</span></span>
    
<span data-ttu-id="89969-164">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="89969-164">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="89969-165">Тип свойства не типа, вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="89969-165">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="89969-166">Замечания</span><span class="sxs-lookup"><span data-stu-id="89969-166">Remarks</span></span>

<span data-ttu-id="89969-167">Метод **IMAPIProp::CopyProps** копирует или перемещает выбранные свойства из текущего объекта в целевой объект.</span><span class="sxs-lookup"><span data-stu-id="89969-167">The **IMAPIProp::CopyProps** method copies or moves selected properties from the current object to a destination object.</span></span> <span data-ttu-id="89969-168">**CopyProps** используется в основном для ответа и пересылки сообщений, где только некоторые свойства из исходного сообщения организации, ответ или перенаправлять копии.</span><span class="sxs-lookup"><span data-stu-id="89969-168">**CopyProps** is used mainly for replying to and forwarding messages, where only some of the properties from the original message travel with the reply or forwarded copy.</span></span> 
  
<span data-ttu-id="89969-169">Вложенными объектами в объекте источника автоматически включены в операции и перемещаются или копируются полностью, независимо от того, использование свойств, указанный в параметре [SPropTagArray](sproptagarray.md) структуры.</span><span class="sxs-lookup"><span data-stu-id="89969-169">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety, regardless of the use of properties indicated by the [SPropTagArray](sproptagarray.md) structure.</span></span> <span data-ttu-id="89969-170">По умолчанию **CopyProps** перезаписывает любые свойства в целевом объекте, соответствующие свойства из исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="89969-170">By default, **CopyProps** overwrites any properties in the destination object that match properties from the source object.</span></span> <span data-ttu-id="89969-171">Если какие-либо свойства скопированной или перемещенной уже существует в целевом объекте, существующие свойства перезаписываются новых свойств, пока флаг MAPI_NOREPLACE будет выполнен с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="89969-171">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="89969-172">Существующие данные в целевой объект, который не перезаписывается остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="89969-172">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="89969-173">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="89969-173">Notes to implementers</span></span>

<span data-ttu-id="89969-174">Можно предоставить полная реализация **CopyProps** или зависеть от реализации, предоставляющий MAPI в своем объекте поддержки.</span><span class="sxs-lookup"><span data-stu-id="89969-174">You can provide a full implementation of **CopyProps** or rely on the implementation that MAPI provides in its support object.</span></span> <span data-ttu-id="89969-175">Если вы хотите использовать в реализации интерфейса MAPI, вызовите метод **IMAPISupport::DoCopyProps** .</span><span class="sxs-lookup"><span data-stu-id="89969-175">If you want to use the MAPI implementation, call the **IMAPISupport::DoCopyProps** method.</span></span> <span data-ttu-id="89969-176">Если делегирование обработки для **DoCopyProps** и передаются флаг MAPI_DECLINE_OK, избежать вызова поддержки и вместо этого возвращать MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="89969-176">However, if you do delegate processing to **DoCopyProps** and you are passed the MAPI_DECLINE_OK flag, avoid the support call and return MAPI_E_DECLINE_COPY instead.</span></span> <span data-ttu-id="89969-177">Этот флаг вызываемого с MAPI, чтобы избежать возможных рекурсии, которая может возникнуть при копировании папки.</span><span class="sxs-lookup"><span data-stu-id="89969-177">You will be called with this flag by MAPI to avoid the possible recursion that can occur when you copy folders.</span></span> 
  
<span data-ttu-id="89969-178">Так как операция копирования может быть длинным, должны отображать индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="89969-178">Because the copy operation can be lengthy, you should display a progress indicator.</span></span> <span data-ttu-id="89969-179">Описание использования реализации [IMAPIProgress](imapiprogressiunknown.md) , переданной в параметре _lpProgress_ , если он существует.</span><span class="sxs-lookup"><span data-stu-id="89969-179">Use the [IMAPIProgress](imapiprogressiunknown.md) implementation that is passed in the  _lpProgress_ parameter, if there is one.</span></span> <span data-ttu-id="89969-180">Если _lpProgress_ имеет **значение null**, вызовите метод [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) для использования в реализации интерфейса MAPI.</span><span class="sxs-lookup"><span data-stu-id="89969-180">If  _lpProgress_ is **null**, call the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to use the MAPI implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="89969-181">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="89969-181">Notes to callers</span></span>

<span data-ttu-id="89969-182">Не задан флаг MAPI_DECLINE_OK; он используется MAPI при его вызове для сообщения **CopyProps** реализации поставщика хранилища.</span><span class="sxs-lookup"><span data-stu-id="89969-182">Do not set the MAPI_DECLINE_OK flag; it is used by MAPI in its calls to message store provider **CopyProps** implementations.</span></span> 
  
<span data-ttu-id="89969-183">Так как операции копирования и перемещения может потребоваться времени, имеет смысл запросить отображение индикатор хода выполнения, установив флаг MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="89969-183">Because copy and move operations can take time, it is wise to request the display of a progress indicator by setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="89969-184">Можно задать параметр _lpProgress_ для внедрения **IMAPIProgress**, если такой существует, или значение **null**.</span><span class="sxs-lookup"><span data-stu-id="89969-184">You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**.</span></span> <span data-ttu-id="89969-185">Если _lpProgress_ имеет **значение null**, **CopyProps** будет использовать индикатор хода выполнения по умолчанию, предоставленные MAPI.</span><span class="sxs-lookup"><span data-stu-id="89969-185">If  _lpProgress_ is **null**, **CopyProps** will use the default progress indicator provided by MAPI.</span></span> 
  
<span data-ttu-id="89969-186">Можно отключить отображение индикатора хода выполнения, не задав флаг MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="89969-186">You can suppress the display of a progress indicator by not setting the MAPI_DIALOG flag.</span></span> <span data-ttu-id="89969-187">**CopyProps** будет игнорировать параметры _ulUIParam_ и _lpProgress_ и избежать отображения индикатора.</span><span class="sxs-lookup"><span data-stu-id="89969-187">**CopyProps** will ignore the  _ulUIParam_ and  _lpProgress_ parameters and avoid displaying the indicator.</span></span> 
  
 <span data-ttu-id="89969-188">**CopyProps** можно сообщить о глобальном уровне и на отдельные ошибки или ошибки, возникающие при работе с одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="89969-188">**CopyProps** can report global and individual errors, or errors that occur with one or more of the properties.</span></span> <span data-ttu-id="89969-189">Эти отдельные ошибки помещаются в структуре **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="89969-189">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="89969-190">Отчеты на уровне свойств, передав **значение null**, а не является допустимым указателем, для параметра свойство массива проблема структура об ошибках, можно отключить.</span><span class="sxs-lookup"><span data-stu-id="89969-190">You can suppress error reporting at the property level by passing **null**, instead of a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="89969-191">Если вы хотите получать сведения об ошибках, передайте допустимый указатель структура **SPropProblemArray** с помощью параметра _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="89969-191">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="89969-192">При **CopyProps** возвращает значение S_OK, проверьте наличие возможных ошибок с помощью отдельных свойств в структуре.</span><span class="sxs-lookup"><span data-stu-id="89969-192">When **CopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="89969-193">Когда **CopyProps** возвращает ошибку, не информация возвращается в структуре **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="89969-193">When **CopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="89969-194">Вместо этого вызовите метод [IMAPIProp::GetLastError](imapiprop-getlasterror.md) , чтобы получить подробные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="89969-194">Instead, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="89969-195">Если **CopyProps** возвращает значение S_OK, освободите возвращенные структура **SPropProblemArray** путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="89969-195">If **CopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="89969-196">При копировании свойств, которые являются уникальными для объекта тип источника данных, необходимо убедиться, что целевой объект является одного типа.</span><span class="sxs-lookup"><span data-stu-id="89969-196">If you are copying properties that are unique to the source object type, you must make sure that the destination object is of the same type.</span></span> <span data-ttu-id="89969-197">**CopyProps** не запрещает связывания свойства, которые обычно относятся к один тип объекта, с другой тип объекта.</span><span class="sxs-lookup"><span data-stu-id="89969-197">**CopyProps** does not prevent you from associating properties that typically belong to one type of object with another type of object.</span></span> <span data-ttu-id="89969-198">Зависит от пользователя для копирования свойств, которые нужны для конечного объекта.</span><span class="sxs-lookup"><span data-stu-id="89969-198">It is up to you to copy properties that make sense for the destination object.</span></span> <span data-ttu-id="89969-199">К примеру не следует копировать свойства сообщений к контейнеру адресной книги.</span><span class="sxs-lookup"><span data-stu-id="89969-199">For example, you should not copy message properties to an address book container.</span></span> 
  
<span data-ttu-id="89969-200">Чтобы убедиться, что выполняется копирование между объектами одного типа, убедитесь, что установлен исходный и конечный объект того же типа, путем сравнения указателей объектов или вызова метода [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="89969-200">To ensure that you are copying between objects of the same type, check that the source and destination object are the same type, either by comparing object pointers or calling the [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="89969-201">Задайте идентификатор интерфейса, на который указывает _lpInterface_ стандартный интерфейс для объекта источника.</span><span class="sxs-lookup"><span data-stu-id="89969-201">Set the interface identifier pointed to by  _lpInterface_ to the standard interface for the source object.</span></span> <span data-ttu-id="89969-202">Кроме того убедитесь, что тип объекта или свойство **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) является общим для двух объектов.</span><span class="sxs-lookup"><span data-stu-id="89969-202">Also, ensure that the object type or **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property is the same for the two objects.</span></span> <span data-ttu-id="89969-203">Например при копировании из сообщения значение _lpInterface_ IID_IMessage и **PR_OBJECT_TYPE** объекты MAPI_MESSAGE.</span><span class="sxs-lookup"><span data-stu-id="89969-203">For example, if you are copying from a message, set  _lpInterface_ to IID_IMessage and the **PR_OBJECT_TYPE** for both objects to MAPI_MESSAGE.</span></span> 
  
<span data-ttu-id="89969-204">Если недопустимый указатель передается в параметре _lpDestObj_ , результаты непредсказуемы.</span><span class="sxs-lookup"><span data-stu-id="89969-204">If an invalid pointer is passed in the  _lpDestObj_ parameter, the results are unpredictable.</span></span> 
  
<span data-ttu-id="89969-205">Чтобы скопировать список получателей сообщения, вызовите метод **CopyProps** сообщение и включите свойство **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) в массиве тега свойства.</span><span class="sxs-lookup"><span data-stu-id="89969-205">To copy a message's recipient list, call the message's **CopyProps** method and include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array.</span></span> <span data-ttu-id="89969-206">Чтобы скопировать вложений сообщений, включите свойство **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="89969-206">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="89969-207">Для копирования папки или иерархии контейнер адресной книги или таблицу содержимого, включают **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) или свойств **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) Свойство tag массива.</span><span class="sxs-lookup"><span data-stu-id="89969-207">To copy a folder or address book container's hierarchy or contents table, include the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) properties in the property tag array.</span></span> <span data-ttu-id="89969-208">Чтобы включить таблицу связанного содержимого папки, добавьте свойство **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) в массиве.</span><span class="sxs-lookup"><span data-stu-id="89969-208">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="89969-209">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="89969-209">MFCMAPI reference</span></span>

<span data-ttu-id="89969-210">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="89969-210">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="89969-211">**����**</span><span class="sxs-lookup"><span data-stu-id="89969-211">**File**</span></span>|<span data-ttu-id="89969-212">**�������**</span><span class="sxs-lookup"><span data-stu-id="89969-212">**Function**</span></span>|<span data-ttu-id="89969-213">**�����������**</span><span class="sxs-lookup"><span data-stu-id="89969-213">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="89969-214">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="89969-214">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="89969-215">CopyNamedProps</span><span class="sxs-lookup"><span data-stu-id="89969-215">CopyNamedProps</span></span>  <br/> |<span data-ttu-id="89969-216">Mfcmapi (en) использует метод **IMAPIProp::CopyProps** для копирования одного сообщения именованных свойств.</span><span class="sxs-lookup"><span data-stu-id="89969-216">MFCMAPI uses the **IMAPIProp::CopyProps** method to copy named properties from one message to another.</span></span>  <br/> |
|<span data-ttu-id="89969-217">SingleMAPIPropListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="89969-217">SingleMAPIPropListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="89969-218">CSingleMAPIPropListCtrl::OnPasteProperty</span><span class="sxs-lookup"><span data-stu-id="89969-218">CSingleMAPIPropListCtrl::OnPasteProperty</span></span>  <br/> |<span data-ttu-id="89969-219">Mfcmapi (en) использует метод **IMAPIProp::CopyProps** для вставки свойства, скопированный из другого объекта.</span><span class="sxs-lookup"><span data-stu-id="89969-219">MFCMAPI uses the **IMAPIProp::CopyProps** method to paste a property that has been copied from another object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89969-220">См. также</span><span class="sxs-lookup"><span data-stu-id="89969-220">See also</span></span>



[<span data-ttu-id="89969-221">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="89969-221">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="89969-222">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="89969-222">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="89969-223">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="89969-223">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="89969-224">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="89969-224">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="89969-225">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="89969-225">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
  
[<span data-ttu-id="89969-226">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="89969-226">IMAPISupport::DoProgressDialog</span></span>](imapisupport-doprogressdialog.md)
  
[<span data-ttu-id="89969-227">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="89969-227">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="89969-228">Каноническое свойство PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="89969-228">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="89969-229">Каноническое свойство PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="89969-229">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="89969-230">Каноническое свойство PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="89969-230">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="89969-231">Каноническое свойство PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="89969-231">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="89969-232">Каноническое свойство PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="89969-232">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="89969-233">Каноническое свойство PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="89969-233">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="89969-234">Каноническое свойство PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="89969-234">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="89969-235">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="89969-235">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="89969-236">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="89969-236">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="89969-237">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="89969-237">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="89969-238">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="89969-238">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

