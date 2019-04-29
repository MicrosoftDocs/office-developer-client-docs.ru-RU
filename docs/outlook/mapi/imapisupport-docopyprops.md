---
title: Имаписуппортдокопипропс
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
# <a name="imapisupportdocopyprops"></a><span data-ttu-id="70090-103">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="70090-103">IMAPISupport::DoCopyProps</span></span>

  
  
<span data-ttu-id="70090-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70090-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70090-105">Копирует или перемещает одно или несколько свойств объекта в другой объект.</span><span class="sxs-lookup"><span data-stu-id="70090-105">Copies or moves one or more properties of an object to another object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="70090-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="70090-106">Parameters</span></span>

 <span data-ttu-id="70090-107">_ЛпсрЦинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="70090-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="70090-108">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к объекту со свойствами, которые необходимо скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="70090-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object with the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="70090-109">_Лпсркобж_</span><span class="sxs-lookup"><span data-stu-id="70090-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="70090-110">возврата Указатель на объект, содержащий свойства, которые необходимо скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="70090-110">[in] A pointer to the object that contains the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="70090-111">_Лпинклудепропс_</span><span class="sxs-lookup"><span data-stu-id="70090-111">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="70090-112">возврата Указатель на структуру [спроптагаррай](sproptagarray.md) , которая содержит считанный массив тегов свойств, указывающий свойства для копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="70090-112">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains a counted array of property tags that indicate the properties to copy or move.</span></span> <span data-ttu-id="70090-113">Параметр _лпинклудепропс_ не может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="70090-113">The  _lpIncludeProps_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="70090-114">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="70090-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="70090-115">возврата Дескриптор родительского окна индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="70090-115">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="70090-116">_Лппрогресс_</span><span class="sxs-lookup"><span data-stu-id="70090-116">_lpProgress_</span></span>
  
> <span data-ttu-id="70090-117">возврата Указатель на реализацию индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="70090-117">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="70090-118">Если в параметре _лппрогресс_ переДАЕТСЯ значение null, индикатор хода выполнения отображается с помощью реализации MAPI.</span><span class="sxs-lookup"><span data-stu-id="70090-118">If NULL is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="70090-119">Параметр _лппрогресс_ игнорируется, если не установлен флаг мапи_диалог в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="70090-119">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="70090-120">_Лпдестинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="70090-120">_lpDestInterface_</span></span>
  
> <span data-ttu-id="70090-121">возврата Указатель на идентификатор интерфейса, представляющий интерфейс, который будет использоваться для доступа к объекту для получения копируемых или перемещенных свойств.</span><span class="sxs-lookup"><span data-stu-id="70090-121">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the properties that are copied or moved.</span></span>
    
 <span data-ttu-id="70090-122">_Лпдестобж_</span><span class="sxs-lookup"><span data-stu-id="70090-122">_lpDestObj_</span></span>
  
> <span data-ttu-id="70090-123">возврата Указатель на объект, который будет получать скопированные или перемещенные свойства.</span><span class="sxs-lookup"><span data-stu-id="70090-123">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="70090-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="70090-124">_ulFlags_</span></span>
  
> <span data-ttu-id="70090-125">возврата Битовая маска флагов, которые управляют выполнением операции копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="70090-125">[in] A bitmask of flags that controls how the copy or move operation is performed.</span></span> <span data-ttu-id="70090-126">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="70090-126">The following flags can be set:</span></span>
    
<span data-ttu-id="70090-127">МАПИ_ДИАЛОГ</span><span class="sxs-lookup"><span data-stu-id="70090-127">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="70090-128">Отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="70090-128">Displays a progress indicator.</span></span>
    
<span data-ttu-id="70090-129">МАПИ_МОВЕ</span><span class="sxs-lookup"><span data-stu-id="70090-129">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="70090-130">**Докопипропс** должен выполнять операцию перемещения, а не операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="70090-130">**DoCopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="70090-131">Если этот флаг не задан, **докопипропс** выполняет операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="70090-131">When this flag is not set, **DoCopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="70090-132">МАПИ_НОРЕПЛАЦЕ</span><span class="sxs-lookup"><span data-stu-id="70090-132">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="70090-133">Существующие свойства в целевом объекте не должны быть перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="70090-133">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="70090-134">Если этот флаг не задан, **докопипропс** перезаписывает существующие свойства.</span><span class="sxs-lookup"><span data-stu-id="70090-134">When this flag is not set, **DoCopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="70090-135">_Лпппроблемс_</span><span class="sxs-lookup"><span data-stu-id="70090-135">_lppProblems_</span></span>
  
> <span data-ttu-id="70090-136">[вход, выход] На входе указатель на указатель на структуру [спроппроблемаррай](spropproblemarray.md) ; в противном случае — значение NULL, которое указывает на отсутствие необходимости в сведениях об ошибке.</span><span class="sxs-lookup"><span data-stu-id="70090-136">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="70090-137">Если _лпппроблемс_ является допустимым указателем на входе, **докопипропс** возвращает подробные сведения об ошибках при копировании одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="70090-137">If  _lppProblems_ is a valid pointer on input, **DoCopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="70090-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="70090-138">Return value</span></span>

<span data-ttu-id="70090-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="70090-139">S_OK</span></span> 
  
> <span data-ttu-id="70090-140">Свойства были успешно скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="70090-140">Properties were successfully copied or moved.</span></span>
    
<span data-ttu-id="70090-141">МАПИ_Е_КОЛЛИСИОН</span><span class="sxs-lookup"><span data-stu-id="70090-141">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="70090-142">Свойство, которое необходимо скопировать или переместить, уже существует в целевом объекте, а также установлен флаг МАПИ_НОРЕПЛАЦЕ.</span><span class="sxs-lookup"><span data-stu-id="70090-142">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="70090-143">МАПИ_Е_ФОЛДЕР_ЦИКЛЕ</span><span class="sxs-lookup"><span data-stu-id="70090-143">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="70090-144">Исходный объект напрямую или косвенно содержит целевой объект.</span><span class="sxs-lookup"><span data-stu-id="70090-144">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="70090-145">Прежде чем было обнаружено это условие, можно выполнить значительную работу, чтобы исходный и конечный объекты могли быть изменены частично.</span><span class="sxs-lookup"><span data-stu-id="70090-145">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="70090-146">МАПИ_Е_ИНТЕРФАЦЕ_НОТ_СУППОРТЕД</span><span class="sxs-lookup"><span data-stu-id="70090-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="70090-147">Интерфейс, определенный параметром _лпсрЦинтерфаце_ , не поддерживается исходным объектом, или интерфейс, определенный параметром _лпдестинтерфаце_ , не поддерживается целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="70090-147">The interface identified by the  _lpSrcInterface_ parameter is not supported by the source object, or the interface identified by the  _lpDestInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="70090-148">МАПИ_Е_НО_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="70090-148">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="70090-149">Предпринята попытка получить доступ к объекту, для которого вызывающая сторона не имеет достаточных разрешений.</span><span class="sxs-lookup"><span data-stu-id="70090-149">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="70090-150">Эта ошибка возвращается, если целевой объект совпадает с исходным объектом.</span><span class="sxs-lookup"><span data-stu-id="70090-150">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="70090-151">Следующие значения могут возвращаться в структуре **спроппроблемаррай** , но не в качестве возвращаемых значений для **докопипропс**.</span><span class="sxs-lookup"><span data-stu-id="70090-151">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyProps**.</span></span> <span data-ttu-id="70090-152">Эти ошибки относятся к одному свойству.</span><span class="sxs-lookup"><span data-stu-id="70090-152">These errors apply to a single property.</span></span>
  
<span data-ttu-id="70090-153">МАПИ_Е_БАД_ЧАРВИДС</span><span class="sxs-lookup"><span data-stu-id="70090-153">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="70090-154">Установлен либо флаг МАПИ_УНИКОДЕ, либо **докопипропс** не поддерживает Юникод, или мапи_уникоде не задано и **Докопипропс** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="70090-154">Either the MAPI_UNICODE flag was set and **DoCopyProps** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="70090-155">МАПИ_Е_КОМПУТЕД</span><span class="sxs-lookup"><span data-stu-id="70090-155">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="70090-156">Абонент не может изменить свойство, так как оно является свойством только для чтения, которое вычисляется владельцем целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="70090-156">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="70090-157">Эта ошибка не серьезна; вызывающая сторона должна разрешить продолжение операции копирования.</span><span class="sxs-lookup"><span data-stu-id="70090-157">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="70090-158">МАПИ_Е_ИНВАЛИД_ТИПЕ</span><span class="sxs-lookup"><span data-stu-id="70090-158">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="70090-159">Недопустимый тип свойства.</span><span class="sxs-lookup"><span data-stu-id="70090-159">The property type is invalid.</span></span>
    
<span data-ttu-id="70090-160">МАПИ_Е_УНЕКСПЕКТЕД_ТИПЕ</span><span class="sxs-lookup"><span data-stu-id="70090-160">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="70090-161">Тип свойства не является типом, ожидаемым вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="70090-161">The property type is not the type that the caller expects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="70090-162">Примечания</span><span class="sxs-lookup"><span data-stu-id="70090-162">Remarks</span></span>

<span data-ttu-id="70090-163">Метод **имаписуппорт::D окопипропс** реализован для объектов поддержки поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="70090-163">The **IMAPISupport::DoCopyProps** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="70090-164">Поставщики хранилища сообщений могут вызывать **докопипропс** для реализации метода [IMAPIProp:: копипропс](imapiprop-copyprops.md) для своих папок и сообщений.</span><span class="sxs-lookup"><span data-stu-id="70090-164">Message store providers can call **DoCopyProps** to implement the [IMAPIProp::CopyProps](imapiprop-copyprops.md) method for their folders and messages.</span></span> <span data-ttu-id="70090-165">**Докопипропс** копирует или перемещает свойства, указанные в массиве тегов свойств, на который указывает _лпинклудепропс_ , и присутствуют в объекте, на который указывает _лпсркобж_.</span><span class="sxs-lookup"><span data-stu-id="70090-165">**DoCopyProps** copies or moves the properties that are identified in the property tag array pointed to by  _lpIncludeProps_ and that are present in the object pointed to by  _lpSrcObj_.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="70090-166">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="70090-166">Notes to callers</span></span>

<span data-ttu-id="70090-167">При копировании свойств между объектами одного типа, например двумя сообщениями, параметры _лпсрЦинтерфаце_ и _лпдестинтерфаце_ должны содержать один и тот же идентификатор интерфейса, а параметры _лпсркобж_ и _лпдестобж_ должен направляться на объекты того же типа.</span><span class="sxs-lookup"><span data-stu-id="70090-167">When you copy properties between objects of the same type, such as two messages, the  _lpSrcInterface_ and  _lpDestInterface_ parameters must contain the same interface identifier, and the  _lpSrcObj_ and  _lpDestObj_ parameters must point to objects of the same type.</span></span> <span data-ttu-id="70090-168">Если для _лпдестинтерфаце_ ЗАДАНО значение null, **докопипропс** возвращает мапи_е_инвалид_параметер.</span><span class="sxs-lookup"><span data-stu-id="70090-168">If  _lpDestInterface_ is set to NULL, **DoCopyProps** returns MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="70090-169">Если для _лпдестинтерфаце_ задан допустимый идентификатор интерфейса, но для параметра _лпдестобж_ задан недопустимый указатель, результаты будут непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="70090-169">If you set  _lpDestInterface_ to an acceptable interface identifier, but set  _lpDestObj_ to an invalid pointer, the results are unpredictable.</span></span> <span data-ttu-id="70090-170">Вероятнее всего, ваш поставщик завершится с ошибками.</span><span class="sxs-lookup"><span data-stu-id="70090-170">Most likely your provider will fail.</span></span> 
  
<span data-ttu-id="70090-171">Установите флаг МАПИ_НОРЕПЛАЦЕ, если не требуется перезаписывать свойства конечного объекта.</span><span class="sxs-lookup"><span data-stu-id="70090-171">Set the MAPI_NOREPLACE flag if you do not want any of the properties in the destination object to be overwritten.</span></span> <span data-ttu-id="70090-172">Свойства в целевом объекте, которые существуют в исходном объекте и не перезаписываются, не удаляются и не изменяются.</span><span class="sxs-lookup"><span data-stu-id="70090-172">Properties in the destination object that exist in the source object and are not overwritten are not deleted or modified.</span></span>
  
<span data-ttu-id="70090-173">Чтобы скопировать список получателей сообщения, включите свойство **пр_мессаже_реЦипиентс** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) в массив тегов свойств, на который указывает параметр _лпинклудепропс_ .</span><span class="sxs-lookup"><span data-stu-id="70090-173">To copy a message's recipient list, include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array pointed to by the  _lpIncludeProps_ parameter.</span></span> <span data-ttu-id="70090-174">Чтобы скопировать вложения сообщения, включите свойство **пр_мессаже_аттачментс** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="70090-174">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="70090-175">Чтобы скопировать папку или таблицу иерархии контейнера или адресной книги, включите **пр_контаинер_хиерарчи** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) или **пр_контаинер_контентс** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) в массив тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="70090-175">To copy a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag array.</span></span> <span data-ttu-id="70090-176">Чтобы включить таблицу с содержимым, связанным с папкой, включите в массив свойство **пр_фолдер_ассоЦиатед_контентс** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="70090-176">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span>
  
<span data-ttu-id="70090-177">Если подпапки копируются или перемещаются, их содержимое копируется или перемещается целиком, независимо от использования свойств, указанных в структуре **спроптагаррай** .</span><span class="sxs-lookup"><span data-stu-id="70090-177">If subfolders are copied or moved, their contents are copied or moved in their entirety, regardless of the use of properties indicated by the **SPropTagArray** structure.</span></span> 
  
 <span data-ttu-id="70090-178">**Докопипропс** сообщает о глобальных ошибках, возникающих при выполнении операции, и отдельных ошибках, происходящих с одним или несколькими свойствами.</span><span class="sxs-lookup"><span data-stu-id="70090-178">**DoCopyProps** reports global errors that occur with the operation as a whole, and individual errors that occur with one or more of the properties.</span></span> <span data-ttu-id="70090-179">Эти отдельные ошибки помещаются в структуру **спроппроблемаррай** .</span><span class="sxs-lookup"><span data-stu-id="70090-179">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="70090-180">Вы можете отключить отчеты об ошибках на уровне свойств, передав значение NULL, а не действительный указатель для параметра структуры массива проблем свойств.</span><span class="sxs-lookup"><span data-stu-id="70090-180">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="70090-181">Если вы хотите получать сведения об ошибках, передайте допустимый указатель структуры **спроппроблемаррай** в параметр _лпппроблемс_ .</span><span class="sxs-lookup"><span data-stu-id="70090-181">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="70090-182">Когда **докопипропс** ВОЗВРАЩАЕТ значение S_OK, проверьте возможные ошибки с отдельными свойствами в структуре.</span><span class="sxs-lookup"><span data-stu-id="70090-182">When **DoCopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="70090-183">Когда **докопипропс** возвращает ошибку, в структуре **спроппроблемаррай** не возвращается никакой информации.</span><span class="sxs-lookup"><span data-stu-id="70090-183">When **DoCopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="70090-184">Вместо этого вызовите метод [имаписуппорт:: GetLastError](imapisupport-getlasterror.md) , чтобы получить подробные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="70090-184">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="70090-185">Если **докопипропс** ВОЗВРАЩАЕТ значение S_OK, то освободите возвращаемую структуру **спроппроблемаррай** , вызвав функцию [мапифрибуффер](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="70090-185">If **DoCopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="70090-186">См. также</span><span class="sxs-lookup"><span data-stu-id="70090-186">See also</span></span>



[<span data-ttu-id="70090-187">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="70090-187">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
  
[<span data-ttu-id="70090-188">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="70090-188">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="70090-189">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="70090-189">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="70090-190">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="70090-190">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="70090-191">Каноническое свойство PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="70090-191">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="70090-192">Каноническое свойство PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="70090-192">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="70090-193">Каноническое свойство PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="70090-193">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="70090-194">Каноническое свойство PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="70090-194">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="70090-195">Каноническое свойство PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="70090-195">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="70090-196">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="70090-196">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="70090-197">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="70090-197">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="70090-198">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="70090-198">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

