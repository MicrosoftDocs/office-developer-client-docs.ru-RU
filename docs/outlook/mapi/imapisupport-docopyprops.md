---
title: имаписуппортдокопипропс
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
# <a name="imapisupportdocopyprops"></a><span data-ttu-id="b1cf2-103">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="b1cf2-103">IMAPISupport::DoCopyProps</span></span>

  
  
<span data-ttu-id="b1cf2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1cf2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1cf2-105">Копирует или перемещает одно или несколько свойств объекта в другой объект.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-105">Copies or moves one or more properties of an object to another object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="b1cf2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1cf2-106">Parameters</span></span>

 <span data-ttu-id="b1cf2-107">_лпсрЦинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="b1cf2-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="b1cf2-108">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к объекту со свойствами, которые необходимо скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object with the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="b1cf2-109">_лпсркобж_</span><span class="sxs-lookup"><span data-stu-id="b1cf2-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="b1cf2-110">возврата Указатель на объект, содержащий свойства, которые необходимо скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-110">[in] A pointer to the object that contains the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="b1cf2-111">_лпинклудепропс_</span><span class="sxs-lookup"><span data-stu-id="b1cf2-111">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="b1cf2-112">возврата Указатель на структуру [спроптагаррай](sproptagarray.md) , которая содержит считанный массив тегов свойств, указывающий свойства для копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-112">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains a counted array of property tags that indicate the properties to copy or move.</span></span> <span data-ttu-id="b1cf2-113">Параметр _лпинклудепропс_ не может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-113">The  _lpIncludeProps_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="b1cf2-114">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="b1cf2-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="b1cf2-115">возврата Дескриптор родительского окна индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-115">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="b1cf2-116">_лппрогресс_</span><span class="sxs-lookup"><span data-stu-id="b1cf2-116">_lpProgress_</span></span>
  
> <span data-ttu-id="b1cf2-117">возврата Указатель на реализацию индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-117">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="b1cf2-118">Если в параметре _лппрогресс_ передается значение null, индикатор хода выполнения отображается с помощью реализации MAPI.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-118">If NULL is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="b1cf2-119">Параметр _лппрогресс_ игнорируется, если в параметре _ulFlags_ не задан флаг MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-119">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="b1cf2-120">_лпдестинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="b1cf2-120">_lpDestInterface_</span></span>
  
> <span data-ttu-id="b1cf2-121">возврата Указатель на идентификатор интерфейса, представляющий интерфейс, который будет использоваться для доступа к объекту для получения копируемых или перемещенных свойств.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-121">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the properties that are copied or moved.</span></span>
    
 <span data-ttu-id="b1cf2-122">_лпдестобж_</span><span class="sxs-lookup"><span data-stu-id="b1cf2-122">_lpDestObj_</span></span>
  
> <span data-ttu-id="b1cf2-123">возврата Указатель на объект, который будет получать скопированные или перемещенные свойства.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-123">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="b1cf2-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b1cf2-124">_ulFlags_</span></span>
  
> <span data-ttu-id="b1cf2-125">возврата Битовая маска флагов, которые управляют выполнением операции копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-125">[in] A bitmask of flags that controls how the copy or move operation is performed.</span></span> <span data-ttu-id="b1cf2-126">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="b1cf2-126">The following flags can be set:</span></span>
    
<span data-ttu-id="b1cf2-127">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="b1cf2-127">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="b1cf2-128">Отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-128">Displays a progress indicator.</span></span>
    
<span data-ttu-id="b1cf2-129">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="b1cf2-129">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="b1cf2-130">**Докопипропс** должен выполнять операцию перемещения, а не операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-130">**DoCopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="b1cf2-131">Если этот флаг не задан, **докопипропс** выполняет операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-131">When this flag is not set, **DoCopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="b1cf2-132">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="b1cf2-132">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="b1cf2-133">Существующие свойства в целевом объекте не должны быть перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-133">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="b1cf2-134">Если этот флаг не задан, **докопипропс** перезаписывает существующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-134">When this flag is not set, **DoCopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="b1cf2-135">_лпппроблемс_</span><span class="sxs-lookup"><span data-stu-id="b1cf2-135">_lppProblems_</span></span>
  
> <span data-ttu-id="b1cf2-136">[вход, выход] На входе указатель на указатель на структуру [спроппроблемаррай](spropproblemarray.md) ; в противном случае — значение NULL, которое указывает на отсутствие необходимости в сведениях об ошибке.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-136">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="b1cf2-137">Если _лпппроблемс_ является допустимым указателем на входе, **докопипропс** возвращает подробные сведения об ошибках при копировании одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-137">If  _lppProblems_ is a valid pointer on input, **DoCopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b1cf2-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1cf2-138">Return value</span></span>

<span data-ttu-id="b1cf2-139">S_OK</span><span class="sxs-lookup"><span data-stu-id="b1cf2-139">S_OK</span></span> 
  
> <span data-ttu-id="b1cf2-140">Свойства были успешно скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-140">Properties were successfully copied or moved.</span></span>
    
<span data-ttu-id="b1cf2-141">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="b1cf2-141">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="b1cf2-142">Свойство, которое необходимо скопировать или переместить, уже существует в целевом объекте, а флаг MAPI_NOREPLACE установлен.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-142">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="b1cf2-143">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="b1cf2-143">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="b1cf2-144">Исходный объект напрямую или косвенно содержит целевой объект.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-144">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="b1cf2-145">Прежде чем было обнаружено это условие, можно выполнить значительную работу, чтобы исходный и конечный объекты могли быть изменены частично.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-145">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="b1cf2-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="b1cf2-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="b1cf2-147">Интерфейс, определенный параметром _лпсрЦинтерфаце_ , не поддерживается исходным объектом, или интерфейс, определенный параметром _лпдестинтерфаце_ , не поддерживается целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-147">The interface identified by the  _lpSrcInterface_ parameter is not supported by the source object, or the interface identified by the  _lpDestInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="b1cf2-148">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="b1cf2-148">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="b1cf2-149">Предпринята попытка получить доступ к объекту, для которого вызывающая сторона не имеет достаточных разрешений.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-149">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="b1cf2-150">Эта ошибка возвращается, если целевой объект совпадает с исходным объектом.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-150">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="b1cf2-151">Следующие значения могут возвращаться в структуре **спроппроблемаррай** , но не в качестве возвращаемых значений для **докопипропс**.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-151">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyProps**.</span></span> <span data-ttu-id="b1cf2-152">Эти ошибки относятся к одному свойству.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-152">These errors apply to a single property.</span></span>
  
<span data-ttu-id="b1cf2-153">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="b1cf2-153">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="b1cf2-154">Установлен установленный флаг MAPI_UNICODE и **докопипропс** не поддерживает Юникод, или MAPI_UNICODE не задан и **Докопипропс** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-154">Either the MAPI_UNICODE flag was set and **DoCopyProps** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="b1cf2-155">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="b1cf2-155">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="b1cf2-156">Абонент не может изменить свойство, так как оно является свойством только для чтения, которое вычисляется владельцем целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-156">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="b1cf2-157">Эта ошибка не серьезна; вызывающая сторона должна разрешить продолжение операции копирования.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-157">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="b1cf2-158">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="b1cf2-158">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="b1cf2-159">Недопустимый тип свойства.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-159">The property type is invalid.</span></span>
    
<span data-ttu-id="b1cf2-160">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="b1cf2-160">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="b1cf2-161">Тип свойства не является типом, ожидаемым вызывающим абонентом.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-161">The property type is not the type that the caller expects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b1cf2-162">Примечания</span><span class="sxs-lookup"><span data-stu-id="b1cf2-162">Remarks</span></span>

<span data-ttu-id="b1cf2-163">Метод **имаписуппорт::D окопипропс** реализован для объектов поддержки поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-163">The **IMAPISupport::DoCopyProps** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="b1cf2-164">Поставщики хранилища сообщений могут вызывать **докопипропс** для реализации метода [IMAPIProp:: копипропс](imapiprop-copyprops.md) для своих папок и сообщений.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-164">Message store providers can call **DoCopyProps** to implement the [IMAPIProp::CopyProps](imapiprop-copyprops.md) method for their folders and messages.</span></span> <span data-ttu-id="b1cf2-165">**Докопипропс** копирует или перемещает свойства, указанные в массиве тегов свойств, на который указывает _лпинклудепропс_ , и присутствуют в объекте, на который указывает _лпсркобж_.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-165">**DoCopyProps** copies or moves the properties that are identified in the property tag array pointed to by  _lpIncludeProps_ and that are present in the object pointed to by  _lpSrcObj_.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b1cf2-166">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="b1cf2-166">Notes to callers</span></span>

<span data-ttu-id="b1cf2-167">При копировании свойств между объектами одного типа, например двумя сообщениями, параметры _лпсрЦинтерфаце_ и _лпдестинтерфаце_ должны содержать один и тот же идентификатор интерфейса, а параметры _лпсркобж_ и _лпдестобж_ должны указать на объекты того же типа.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-167">When you copy properties between objects of the same type, such as two messages, the  _lpSrcInterface_ and  _lpDestInterface_ parameters must contain the same interface identifier, and the  _lpSrcObj_ and  _lpDestObj_ parameters must point to objects of the same type.</span></span> <span data-ttu-id="b1cf2-168">Если для _лпдестинтерфаце_ ЗАДАНО значение null, **докопипропс** возвращает MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-168">If  _lpDestInterface_ is set to NULL, **DoCopyProps** returns MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="b1cf2-169">Если для _лпдестинтерфаце_ задан допустимый идентификатор интерфейса, но для параметра _лпдестобж_ задан недопустимый указатель, результаты будут непредсказуемыми.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-169">If you set  _lpDestInterface_ to an acceptable interface identifier, but set  _lpDestObj_ to an invalid pointer, the results are unpredictable.</span></span> <span data-ttu-id="b1cf2-170">Вероятнее всего, ваш поставщик завершится с ошибками.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-170">Most likely your provider will fail.</span></span> 
  
<span data-ttu-id="b1cf2-171">Установите флаг MAPI_NOREPLACE, если вы не хотите перезаписывать свойства конечного объекта.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-171">Set the MAPI_NOREPLACE flag if you do not want any of the properties in the destination object to be overwritten.</span></span> <span data-ttu-id="b1cf2-172">Свойства в целевом объекте, которые существуют в исходном объекте и не перезаписываются, не удаляются и не изменяются.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-172">Properties in the destination object that exist in the source object and are not overwritten are not deleted or modified.</span></span>
  
<span data-ttu-id="b1cf2-173">Чтобы скопировать список получателей сообщения, включите свойство **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) в массив тегов свойств, на который указывает параметр _лпинклудепропс_ .</span><span class="sxs-lookup"><span data-stu-id="b1cf2-173">To copy a message's recipient list, include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array pointed to by the  _lpIncludeProps_ parameter.</span></span> <span data-ttu-id="b1cf2-174">Чтобы скопировать вложения сообщения, включите свойство **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b1cf2-174">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="b1cf2-175">Чтобы скопировать иерархию или таблицу контента контейнера или адресной книги, укажите **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) или **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) в массиве тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-175">To copy a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag array.</span></span> <span data-ttu-id="b1cf2-176">Чтобы включить таблицу с содержимым, связанным с папкой, включите в массив свойство **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b1cf2-176">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span>
  
<span data-ttu-id="b1cf2-177">Если подпапки копируются или перемещаются, их содержимое копируется или перемещается целиком, независимо от использования свойств, указанных в структуре **спроптагаррай** .</span><span class="sxs-lookup"><span data-stu-id="b1cf2-177">If subfolders are copied or moved, their contents are copied or moved in their entirety, regardless of the use of properties indicated by the **SPropTagArray** structure.</span></span> 
  
 <span data-ttu-id="b1cf2-178">**Докопипропс** сообщает о глобальных ошибках, возникающих при выполнении операции, и отдельных ошибках, происходящих с одним или несколькими свойствами.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-178">**DoCopyProps** reports global errors that occur with the operation as a whole, and individual errors that occur with one or more of the properties.</span></span> <span data-ttu-id="b1cf2-179">Эти отдельные ошибки помещаются в структуру **спроппроблемаррай** .</span><span class="sxs-lookup"><span data-stu-id="b1cf2-179">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="b1cf2-180">Вы можете отключить отчеты об ошибках на уровне свойств, передав значение NULL, а не действительный указатель для параметра структуры массива проблем свойств.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-180">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="b1cf2-181">Если вы хотите получать сведения об ошибках, передайте допустимый указатель структуры **спроппроблемаррай** в параметр _лпппроблемс_ .</span><span class="sxs-lookup"><span data-stu-id="b1cf2-181">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="b1cf2-182">Когда **докопипропс** возвращает S_OK, проверьте возможные ошибки с отдельными свойствами в структуре.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-182">When **DoCopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="b1cf2-183">Когда **докопипропс** возвращает ошибку, в структуре **спроппроблемаррай** не возвращается никакой информации.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-183">When **DoCopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="b1cf2-184">Вместо этого вызовите метод [имаписуппорт:: GetLastError](imapisupport-getlasterror.md) , чтобы получить подробные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="b1cf2-184">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="b1cf2-185">Если **докопипропс** возвращает S_OK, освободите возвращаемую структуру **спроппроблемаррай** , вызвав функцию [мапифрибуффер](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="b1cf2-185">If **DoCopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b1cf2-186">См. также</span><span class="sxs-lookup"><span data-stu-id="b1cf2-186">See also</span></span>



[<span data-ttu-id="b1cf2-187">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="b1cf2-187">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
  
[<span data-ttu-id="b1cf2-188">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="b1cf2-188">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="b1cf2-189">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="b1cf2-189">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="b1cf2-190">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b1cf2-190">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="b1cf2-191">Каноническое свойство PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="b1cf2-191">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="b1cf2-192">Каноническое свойство PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="b1cf2-192">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="b1cf2-193">Каноническое свойство PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="b1cf2-193">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="b1cf2-194">Каноническое свойство PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="b1cf2-194">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="b1cf2-195">Каноническое свойство PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="b1cf2-195">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="b1cf2-196">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="b1cf2-196">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="b1cf2-197">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="b1cf2-197">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="b1cf2-198">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b1cf2-198">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

