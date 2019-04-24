---
title: Имаписуппортдокопито
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
ms.openlocfilehash: 6f6c802f1d5ead1750c05fafc54533487fe3732a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331810"
---
# <a name="imapisupportdocopyto"></a><span data-ttu-id="22bd2-103">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="22bd2-103">IMAPISupport::DoCopyTo</span></span>

  
  
<span data-ttu-id="22bd2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22bd2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22bd2-105">Копирует или перемещает все свойства одного объекта, за исключением явно исключенных свойств, в другой объект.</span><span class="sxs-lookup"><span data-stu-id="22bd2-105">Copies or moves all properties of one object, except for specifically excluded properties, to another object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="22bd2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="22bd2-106">Parameters</span></span>

 <span data-ttu-id="22bd2-107">_ЛпсрЦинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="22bd2-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="22bd2-108">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к объекту, свойства которого необходимо скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="22bd2-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="22bd2-109">_Лпсркобж_</span><span class="sxs-lookup"><span data-stu-id="22bd2-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="22bd2-110">возврата Указатель на объект, содержащий свойства, которые необходимо скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="22bd2-110">[in] A pointer to the object that has the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="22bd2-111">_Циидексклуде_</span><span class="sxs-lookup"><span data-stu-id="22bd2-111">_ciidExclude_</span></span>
  
> <span data-ttu-id="22bd2-112">возврата Количество интерфейсов, которые необходимо исключить при копировании или перемещении свойств.</span><span class="sxs-lookup"><span data-stu-id="22bd2-112">[in] The count of interfaces to exclude when you copy or move properties.</span></span>
    
 <span data-ttu-id="22bd2-113">_Ргиидексклуде_</span><span class="sxs-lookup"><span data-stu-id="22bd2-113">_rgiidExclude_</span></span>
  
> <span data-ttu-id="22bd2-114">возврата Массив идентификаторов интерфейса, указывающий интерфейсы, которые не следует использовать при копировании или перемещении дополнительных сведений в целевой объект.</span><span class="sxs-lookup"><span data-stu-id="22bd2-114">[in] An array of interface identifiers that indicates interfaces that should not be used when you copy or move supplemental information to the destination object.</span></span>
    
 <span data-ttu-id="22bd2-115">_Лпексклудепропс_</span><span class="sxs-lookup"><span data-stu-id="22bd2-115">_lpExcludeProps_</span></span>
  
> <span data-ttu-id="22bd2-116">возврата Указатель на массив тегов свойств, определяющий теги свойств, которые следует исключить из операции копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="22bd2-116">[in] A pointer to a property tag array that identifies the property tags that should be excluded from the copy or move operation.</span></span> <span data-ttu-id="22bd2-117">При передаче значения NULL в параметре _лпексклудепропс_ показывается, что все свойства объекта должны быть скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="22bd2-117">Passing NULL in the  _lpExcludeProps_ parameter indicates that all of the object's properties should be copied or moved.</span></span> <span data-ttu-id="22bd2-118">**Докопито** возвращает мапи_е_инвалид_параметер, если элемент **квалуес** структуры [Спроптагаррай](sproptagarray.md) , на который указывает _лпексклудепропс_ , имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="22bd2-118">**DoCopyTo** returns MAPI_E_INVALID_PARAMETER when the **cValues** member of the [SPropTagArray](sproptagarray.md) structure pointed to by  _lpExcludeProps_ is set to 0.</span></span> 
    
 <span data-ttu-id="22bd2-119">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="22bd2-119">_ulUIParam_</span></span>
  
> <span data-ttu-id="22bd2-120">возврата Дескриптор родительского окна индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="22bd2-120">[in] A handle to the parent window of the progress indicator.</span></span> 
    
 <span data-ttu-id="22bd2-121">_Лппрогресс_</span><span class="sxs-lookup"><span data-stu-id="22bd2-121">_lpProgress_</span></span>
  
> <span data-ttu-id="22bd2-122">возврата Указатель на реализацию индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="22bd2-122">[in] A pointer to a progress indicator implementation.</span></span> <span data-ttu-id="22bd2-123">Если в параметре _лппрогресс_ переДАЕТСЯ значение null, MAPI предоставляет реализацию хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="22bd2-123">If NULL is passed in the  _lpProgress_ parameter, MAPI provides the progress implementation.</span></span> <span data-ttu-id="22bd2-124">Параметр _лппрогресс_ игнорируется, если не установлен флаг мапи_диалог в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="22bd2-124">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="22bd2-125">_Лпдестинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="22bd2-125">_lpDestInterface_</span></span>
  
> <span data-ttu-id="22bd2-126">возврата Указатель на идентификатор интерфейса, представляющий интерфейс, который будет использоваться для доступа к объекту для получения скопированных или перемещенных свойств.</span><span class="sxs-lookup"><span data-stu-id="22bd2-126">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="22bd2-127">_Лпдестобж_</span><span class="sxs-lookup"><span data-stu-id="22bd2-127">_lpDestObj_</span></span>
  
> <span data-ttu-id="22bd2-128">возврата Указатель на объект, который будет получать скопированные или перемещенные свойства.</span><span class="sxs-lookup"><span data-stu-id="22bd2-128">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="22bd2-129">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="22bd2-129">_ulFlags_</span></span>
  
> <span data-ttu-id="22bd2-130">возврата Битовая маска флагов, управляющих операциями копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="22bd2-130">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="22bd2-131">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="22bd2-131">The following flags can be set:</span></span>
    
<span data-ttu-id="22bd2-132">МАПИ_ДИАЛОГ</span><span class="sxs-lookup"><span data-stu-id="22bd2-132">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="22bd2-133">Отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="22bd2-133">Displays a progress indicator.</span></span> 
    
<span data-ttu-id="22bd2-134">МАПИ_МОВЕ</span><span class="sxs-lookup"><span data-stu-id="22bd2-134">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="22bd2-135">**Докопито** должен выполнять операцию перемещения, а не операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="22bd2-135">**DoCopyTo** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="22bd2-136">Если этот флаг не задан, **докопито** выполняет операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="22bd2-136">When this flag is not set, **DoCopyTo** performs a copy operation.</span></span> 
    
<span data-ttu-id="22bd2-137">МАПИ_НОРЕПЛАЦЕ</span><span class="sxs-lookup"><span data-stu-id="22bd2-137">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="22bd2-138">Существующие свойства в целевом объекте не должны быть перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="22bd2-138">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="22bd2-139">Если этот флаг не задан, **докопито** перезаписывает существующие свойства.</span><span class="sxs-lookup"><span data-stu-id="22bd2-139">When this flag is not set, **DoCopyTo** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="22bd2-140">_Лпппроблемс_</span><span class="sxs-lookup"><span data-stu-id="22bd2-140">_lppProblems_</span></span>
  
> <span data-ttu-id="22bd2-141">вышли На входе указатель на указатель на структуру [спроппроблемаррай](spropproblemarray.md) ; в противном случае — значение NULL, которое указывает на отсутствие необходимости в сведениях об ошибке.</span><span class="sxs-lookup"><span data-stu-id="22bd2-141">[out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="22bd2-142">Если _лпппроблемс_ является допустимым указателем на входе, **докопито** возвращает подробные сведения об ошибках при копировании одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="22bd2-142">If  _lppProblems_ is a valid pointer on input, **DoCopyTo** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="22bd2-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="22bd2-143">Return value</span></span>

<span data-ttu-id="22bd2-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="22bd2-144">S_OK</span></span> 
  
> <span data-ttu-id="22bd2-145">Свойства успешно скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="22bd2-145">The properties have been successfully copied or moved.</span></span>
    
<span data-ttu-id="22bd2-146">МАПИ_Е_КОЛЛИСИОН</span><span class="sxs-lookup"><span data-stu-id="22bd2-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="22bd2-147">Свойство, которое необходимо скопировать или переместить, уже существует в целевом объекте, а также установлен флаг МАПИ_НОРЕПЛАЦЕ.</span><span class="sxs-lookup"><span data-stu-id="22bd2-147">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="22bd2-148">МАПИ_Е_ФОЛДЕР_ЦИКЛЕ</span><span class="sxs-lookup"><span data-stu-id="22bd2-148">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="22bd2-149">Исходный объект напрямую или косвенно содержит целевой объект.</span><span class="sxs-lookup"><span data-stu-id="22bd2-149">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="22bd2-150">Прежде чем было обнаружено это условие, можно выполнить значительную работу, чтобы исходный и конечный объекты могли быть изменены частично.</span><span class="sxs-lookup"><span data-stu-id="22bd2-150">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="22bd2-151">МАПИ_Е_ИНТЕРФАЦЕ_НОТ_СУППОРТЕД</span><span class="sxs-lookup"><span data-stu-id="22bd2-151">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="22bd2-152">Интерфейс, определенный параметром _лпсрЦинтерфаце_ , не поддерживается объектом, на который указывает _лпсркобж_, или интерфейс, определенный параметром _лпдестинтерфаце_ , не поддерживается объектом, на который указывает _лпдестобж _.</span><span class="sxs-lookup"><span data-stu-id="22bd2-152">The interface identified by the  _lpSrcInterface_ parameter is not supported by the object pointed to by  _lpSrcObj_, or the interface identified by the  _lpDestInterface_ parameter is not supported by the object pointed to by  _lpDestObj_.</span></span> 
    
<span data-ttu-id="22bd2-153">МАПИ_Е_НО_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="22bd2-153">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="22bd2-154">Предпринята попытка получить доступ к объекту, для которого вызывающая сторона не имеет достаточных разрешений.</span><span class="sxs-lookup"><span data-stu-id="22bd2-154">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="22bd2-155">Эта ошибка возвращается, если целевой объект совпадает с исходным объектом.</span><span class="sxs-lookup"><span data-stu-id="22bd2-155">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="22bd2-156">МАПИ_Е_ИНВАЛИД_ПАРАМЕТЕР</span><span class="sxs-lookup"><span data-stu-id="22bd2-156">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="22bd2-157">Параметр _лпсрЦинтерфаце_ имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="22bd2-157">The  _lpSrcInterface_ parameter is NULL.</span></span> 
    
<span data-ttu-id="22bd2-158">Следующие значения могут возвращаться в структуре **спроппроблемаррай** , но не в качестве возвращаемых значений для **докопито**.</span><span class="sxs-lookup"><span data-stu-id="22bd2-158">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyTo**.</span></span> <span data-ttu-id="22bd2-159">Эти ошибки относятся к одному свойству.</span><span class="sxs-lookup"><span data-stu-id="22bd2-159">These errors apply to a single property.</span></span>
  
<span data-ttu-id="22bd2-160">МАПИ_Е_БАД_ЧАРВИДС</span><span class="sxs-lookup"><span data-stu-id="22bd2-160">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="22bd2-161">Установлен либо флаг МАПИ_УНИКОДЕ, либо **докопито** не поддерживает Юникод, или мапи_уникоде не задано и **Докопито** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="22bd2-161">Either the MAPI_UNICODE flag was set and **DoCopyTo** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyTo** supports only Unicode.</span></span> 
    
<span data-ttu-id="22bd2-162">МАПИ_Е_КОМПУТЕД</span><span class="sxs-lookup"><span data-stu-id="22bd2-162">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="22bd2-163">Абонент не может изменить свойство, так как оно является свойством только для чтения, которое вычисляется владельцем целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="22bd2-163">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="22bd2-164">Эта ошибка не серьезна; вызывающая сторона должна разрешить продолжение операции копирования.</span><span class="sxs-lookup"><span data-stu-id="22bd2-164">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="22bd2-165">МАПИ_Е_ИНВАЛИД_ТИПЕ</span><span class="sxs-lookup"><span data-stu-id="22bd2-165">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="22bd2-166">Недопустимый тип свойства.</span><span class="sxs-lookup"><span data-stu-id="22bd2-166">The property type is invalid.</span></span>
    
<span data-ttu-id="22bd2-167">МАПИ_Е_УНЕКСПЕКТЕД_ТИПЕ</span><span class="sxs-lookup"><span data-stu-id="22bd2-167">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="22bd2-168">Тип свойства не является типом, ожидаемым вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="22bd2-168">The property type is not the type expected by the caller.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="22bd2-169">Комментарии</span><span class="sxs-lookup"><span data-stu-id="22bd2-169">Remarks</span></span>

<span data-ttu-id="22bd2-170">Метод **имаписуппорт::D окопито** реализован для объектов поддержки поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="22bd2-170">The **IMAPISupport::DoCopyTo** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="22bd2-171">Поставщики хранилища сообщений могут вызывать **докопито** для реализации метода [IMAPIProp:: CopyTo](imapiprop-copyto.md) для своих папок и сообщений.</span><span class="sxs-lookup"><span data-stu-id="22bd2-171">Message store providers can call **DoCopyTo** to implement the [IMAPIProp::CopyTo](imapiprop-copyto.md) method for their folders and messages.</span></span> 
  
<span data-ttu-id="22bd2-172">По умолчанию **докопито** копирует или перемещает все свойства одного объекта в другой объект.</span><span class="sxs-lookup"><span data-stu-id="22bd2-172">By default, **DoCopyTo** copies or moves all of the properties of one object to another object.</span></span> <span data-ttu-id="22bd2-173">Любые подобъекты в исходном объекте автоматически включаются в операцию, а затем копируются или перемещаются целиком.</span><span class="sxs-lookup"><span data-stu-id="22bd2-173">Any subobjects in the source object are automatically included in the operation and copied or moved in their entirety.</span></span> 
  
<span data-ttu-id="22bd2-174">Если какие-либо из скопированных или перемещенных свойств уже существуют в целевом объекте, существующие свойства перезаписываются новыми свойствами, если в параметре _ulFlags_ не задано значение флага мапи_нореплаце.</span><span class="sxs-lookup"><span data-stu-id="22bd2-174">If any of the copied or moved properties already exist in the destination object, the existing properties are overwritten by the new properties, unless the MAPI_NOREPLACE flag is set in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="22bd2-175">Существующие сведения в целевом объекте, которые не перезаписываются, остаются нетронутыми.</span><span class="sxs-lookup"><span data-stu-id="22bd2-175">Existing information in the destination object that is not overwritten is left untouched.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="22bd2-176">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="22bd2-176">Notes to callers</span></span>

<span data-ttu-id="22bd2-177">Чтобы исключить свойства из операции копирования или перемещения, добавьте их теги свойств в параметр _лпексклудепропс_ .</span><span class="sxs-lookup"><span data-stu-id="22bd2-177">To exclude properties from the copy or move operation, include their property tags in the  _lpExcludeProps_ parameter.</span></span> <span data-ttu-id="22bd2-178">Если вы передаете результаты с помощью макроса [проп_таг](prop_tag.md) для создания тега свойства из определенного идентификатора в массиве тегов свойств, все свойства с этим идентификатором будут исключены.</span><span class="sxs-lookup"><span data-stu-id="22bd2-178">If you pass the results of using the [PROP_TAG](prop_tag.md) macro to build a property tag from a specific identifier in the property tag array, all properties with that identifier will be excluded.</span></span> <span data-ttu-id="22bd2-179">Например, следующая запись в массиве тегов свойств вызывает исключение всех свойств с идентификатором 0x8002, независимо от типа.</span><span class="sxs-lookup"><span data-stu-id="22bd2-179">For example, the following entry in the property tag array causes all properties with an identifier of 0x8002 to be excluded, regardless of type:</span></span> 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
<span data-ttu-id="22bd2-180">Чтобы избежать копирования времени доставки сообщения при копировании сообщения в другую папку, укажите **пр_мессаже_деливери_тиме** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) в теге свойства Exclude Array.</span><span class="sxs-lookup"><span data-stu-id="22bd2-180">To avoid copying a message's delivery time when you copy the message to a different folder, specify **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) in the property tag exclude array.</span></span> <span data-ttu-id="22bd2-181">Чтобы исключить список получателей сообщения, добавьте в массив Exclude свойство **пр_мессаже_реЦипиентс** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="22bd2-181">To exclude a message's recipient list, add the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property to the exclude array.</span></span> <span data-ttu-id="22bd2-182">Чтобы исключить вложения сообщения, добавьте в массив свойство **пр_мессаже_аттачментс** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="22bd2-182">To exclude a message's attachments, add the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property to the array.</span></span>
  
<span data-ttu-id="22bd2-183">Аналогичным образом, чтобы не допустить копирование или перемещение папки или таблицы иерархии контейнеров или содержимого, включите **пр_контаинер_хиерарчи** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) или **пр_контаинер_контентс** ([ PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) в теге свойства Exclude Array.</span><span class="sxs-lookup"><span data-stu-id="22bd2-183">Similarly, to prevent the copying or moving of a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag exclude array.</span></span>
  
<span data-ttu-id="22bd2-184">Игнорировать ошибки МАПИ_Е_КОМПУТЕД, возвращенные в структуре **спроппроблемаррай** в параметре _лпппроблемс_ .</span><span class="sxs-lookup"><span data-stu-id="22bd2-184">Ignore MAPI_E_COMPUTED errors returned in the **SPropProblemArray** structure in the  _lppProblems_ parameter.</span></span> 
  
<span data-ttu-id="22bd2-185">Идентификатор интерфейса, на который указывает _лпсрЦинтерфаце_ , обычно совпадает с идентификатором интерфейса, на который указывает _лпдестинтерфаце_ .</span><span class="sxs-lookup"><span data-stu-id="22bd2-185">The interface identifier that  _lpSrcInterface_ points to is usually the same as the interface identifier that  _lpDestInterface_ points to.</span></span> 
  
<span data-ttu-id="22bd2-186">Если вы передаете допустимый идентификатор интерфейса в _лпдестинтерфаце_ , но недопустимый указатель в _лпдестобж_, результаты будут непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="22bd2-186">If you pass an acceptable interface identifier in  _lpDestInterface_ but an invalid pointer in  _lpDestObj_, the results are unpredictable.</span></span> <span data-ttu-id="22bd2-187">Скорее всего, это приведет к сбою поставщика.</span><span class="sxs-lookup"><span data-stu-id="22bd2-187">Most likely this will cause your provider to fail.</span></span> 
  
<span data-ttu-id="22bd2-188">И наоборот, если вы узнаете о дополнительной информации, которую не следует копировать или переместить, добавьте идентификаторы интерфейсов для интерфейсов, исключаемых из массива, переданного в параметре _ргиидексклуде_ .</span><span class="sxs-lookup"><span data-stu-id="22bd2-188">Conversely, if you are aware of supplemental information that should not be copied or moved, add the interface identifiers for the interfaces to be excluded in the array passed in the  _rgiidExclude_ parameter.</span></span> <span data-ttu-id="22bd2-189">Например, если вы копируете сообщения, но не любые вложения сообщений, передавайте Иид_имессаже в массив _ргиидексклуде_ .</span><span class="sxs-lookup"><span data-stu-id="22bd2-189">For example, if you are copying messages, but not any of their message attachments, pass IID_IMessage in the  _rgiidExclude_ array.</span></span> <span data-ttu-id="22bd2-190">**Докопито** игнорирует все интерфейсы, перечисленные в _ргиидексклуде_ , которые не распознаются.</span><span class="sxs-lookup"><span data-stu-id="22bd2-190">**DoCopyTo** ignores any interfaces listed in  _rgiidExclude_ that it does not recognize.</span></span> 
  
<span data-ttu-id="22bd2-191">При использовании параметра _ргиидексклуде_ для исключения интерфейса он также исключает все интерфейсы, полученные из этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="22bd2-191">When you use the  _rgiidExclude_ parameter to exclude an interface, it also excludes all interfaces derived from that interface.</span></span> <span data-ttu-id="22bd2-192">Например, исключение из интерфейса [IMAPIContainer](imapicontainerimapiprop.md) приводит к исключению папок или контейнеров адресных книг в зависимости от типа поставщика.</span><span class="sxs-lookup"><span data-stu-id="22bd2-192">For example, excluding the [IMAPIContainer](imapicontainerimapiprop.md) interface causes folders or address book containers to be excluded, depending on the type of provider.</span></span> <span data-ttu-id="22bd2-193">Не следует исключать [IMAPIProp](imapipropiunknown.md) или [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) , так как многие интерфейсы являются производными от них.</span><span class="sxs-lookup"><span data-stu-id="22bd2-193">Do not exclude [IMAPIProp](imapipropiunknown.md) or [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) because so many interfaces derive from them.</span></span> 
  
 <span data-ttu-id="22bd2-194">**Докопито** сообщает о глобальных ошибках, которые применяются к операции в целом, и отдельных ошибках, которые применяются к отдельным свойствам.</span><span class="sxs-lookup"><span data-stu-id="22bd2-194">**DoCopyTo** reports global errors that apply to the operation as a whole, and individual errors that apply to individual properties.</span></span> <span data-ttu-id="22bd2-195">Эти отдельные ошибки помещаются в структуру **спроппроблемаррай** .</span><span class="sxs-lookup"><span data-stu-id="22bd2-195">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="22bd2-196">Вы можете отключить отчеты об ошибках на уровне свойств, передав значение NULL, а не действительный указатель для параметра структуры массива проблем свойств.</span><span class="sxs-lookup"><span data-stu-id="22bd2-196">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="22bd2-197">Если вы хотите получать сведения об ошибках, передайте допустимый указатель структуры **спроппроблемаррай** в параметр _лпппроблемс_ .</span><span class="sxs-lookup"><span data-stu-id="22bd2-197">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="22bd2-198">Когда **докопито** ВОЗВРАЩАЕТ значение S_OK, проверьте возможные ошибки с отдельными свойствами в структуре.</span><span class="sxs-lookup"><span data-stu-id="22bd2-198">When **DoCopyTo** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="22bd2-199">Когда **докопито** возвращает ошибку, в структуре **спроппроблемаррай** не возвращается никакой информации.</span><span class="sxs-lookup"><span data-stu-id="22bd2-199">When **DoCopyTo** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="22bd2-200">Вместо этого вызовите метод [имаписуппорт:: GetLastError](imapisupport-getlasterror.md) , чтобы получить подробные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="22bd2-200">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="22bd2-201">Если **докопито** ВОЗВРАЩАЕТ значение S_OK, то освободите возвращаемую структуру **спроппроблемаррай** , вызвав функцию [мапифрибуффер](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="22bd2-201">If **DoCopyTo** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="22bd2-202">Если в вызове **докопито** возникает глобальная ошибка, не используйте и не освобождайте структуру **спроппроблемаррай** .</span><span class="sxs-lookup"><span data-stu-id="22bd2-202">If a global error occurs on the **DoCopyTo** call, do not use or free the **SPropProblemArray** structure.</span></span> <span data-ttu-id="22bd2-203">Поставщики должны игнорировать элемент _улиндекс_ в структурах **спроппроблемаррай** , возвращаемых **докопито**.</span><span class="sxs-lookup"><span data-stu-id="22bd2-203">Providers should ignore the  _ulIndex_ member in **SPropProblemArray** structures returned by **DoCopyTo**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="22bd2-204">См. также</span><span class="sxs-lookup"><span data-stu-id="22bd2-204">See also</span></span>



[<span data-ttu-id="22bd2-205">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="22bd2-205">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
  
[<span data-ttu-id="22bd2-206">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="22bd2-206">IMAPISupport::CopyFolder</span></span>](imapisupport-copyfolder.md)
  
[<span data-ttu-id="22bd2-207">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="22bd2-207">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="22bd2-208">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="22bd2-208">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="22bd2-209">Каноническое свойство PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="22bd2-209">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="22bd2-210">Каноническое свойство PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="22bd2-210">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="22bd2-211">Каноническое свойство PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="22bd2-211">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="22bd2-212">Каноническое свойство PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="22bd2-212">PidTagMessageDeliveryTime Canonical Property</span></span>](pidtagmessagedeliverytime-canonical-property.md)
  
[<span data-ttu-id="22bd2-213">Каноническое свойство PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="22bd2-213">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="22bd2-214">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="22bd2-214">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="22bd2-215">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="22bd2-215">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="22bd2-216">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="22bd2-216">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

