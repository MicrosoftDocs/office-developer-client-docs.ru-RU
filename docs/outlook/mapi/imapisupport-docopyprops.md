---
title: IMAPISupportDoCopyProps
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
ms.openlocfilehash: c93e01b1e4621cddc4c98d528e5f5339cba21dae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809109"
---
# <a name="imapisupportdocopyprops"></a><span data-ttu-id="52fba-103">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="52fba-103">IMAPISupport::DoCopyProps</span></span>

  
  
<span data-ttu-id="52fba-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="52fba-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="52fba-105">Копирование или Перемещение одного или нескольких свойств объекта на другой объект.</span><span class="sxs-lookup"><span data-stu-id="52fba-105">Copies or moves one or more properties of an object to another object.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="52fba-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="52fba-106">Parameters</span></span>

 <span data-ttu-id="52fba-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="52fba-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="52fba-108">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к объекту с помощью свойства, которые нужно скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="52fba-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object with the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="52fba-109">_lpSrcObj_</span><span class="sxs-lookup"><span data-stu-id="52fba-109">_lpSrcObj_</span></span>
  
> <span data-ttu-id="52fba-110">[in] Указатель на объект, содержащий свойства, которые нужно скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="52fba-110">[in] A pointer to the object that contains the properties to be copied or moved.</span></span>
    
 <span data-ttu-id="52fba-111">_lpIncludeProps_</span><span class="sxs-lookup"><span data-stu-id="52fba-111">_lpIncludeProps_</span></span>
  
> <span data-ttu-id="52fba-112">[in] Указатель на структуру [SPropTagArray](sproptagarray.md) , содержащий инвентаризации массив тегов свойств, которые указывают свойства, которые нужно скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="52fba-112">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains a counted array of property tags that indicate the properties to copy or move.</span></span> <span data-ttu-id="52fba-113">Параметр _lpIncludeProps_ не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="52fba-113">The  _lpIncludeProps_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="52fba-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="52fba-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="52fba-115">[in] Дескриптор родительского окна индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="52fba-115">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="52fba-116">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="52fba-116">_lpProgress_</span></span>
  
> <span data-ttu-id="52fba-117">[in] Указатель на реализацию индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="52fba-117">[in] A pointer to an implementation of a progress indicator.</span></span> <span data-ttu-id="52fba-118">Если значение NULL передается в параметре _lpProgress_ , с помощью реализации интерфейса MAPI отображается индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="52fba-118">If NULL is passed in the  _lpProgress_ parameter, the progress indicator is displayed by using the MAPI implementation.</span></span> <span data-ttu-id="52fba-119">Параметр _lpProgress_ игнорируется, пока флаг MAPI_DIALOG будет выполнен с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="52fba-119">The  _lpProgress_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="52fba-120">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="52fba-120">_lpDestInterface_</span></span>
  
> <span data-ttu-id="52fba-121">[in] Указатель на идентификатор интерфейса, который представляет интерфейс, который будет использоваться для доступа к объекту для получения свойства, которые копируются или перемещаются.</span><span class="sxs-lookup"><span data-stu-id="52fba-121">[in] A pointer to the interface identifier that represents the interface to be used to access the object to receive the properties that are copied or moved.</span></span>
    
 <span data-ttu-id="52fba-122">_lpDestObj_</span><span class="sxs-lookup"><span data-stu-id="52fba-122">_lpDestObj_</span></span>
  
> <span data-ttu-id="52fba-123">[in] Указатель на объект для получения свойств копируемые или перемещения.</span><span class="sxs-lookup"><span data-stu-id="52fba-123">[in] A pointer to the object to receive the copied or moved properties.</span></span>
    
 <span data-ttu-id="52fba-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="52fba-124">_ulFlags_</span></span>
  
> <span data-ttu-id="52fba-125">[in] Битовая маска флаги, который определяет, как выполняется операция копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="52fba-125">[in] A bitmask of flags that controls how the copy or move operation is performed.</span></span> <span data-ttu-id="52fba-126">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="52fba-126">The following flags can be set:</span></span>
    
<span data-ttu-id="52fba-127">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="52fba-127">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="52fba-128">Отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="52fba-128">Displays a progress indicator.</span></span>
    
<span data-ttu-id="52fba-129">MAPI_MOVE</span><span class="sxs-lookup"><span data-stu-id="52fba-129">MAPI_MOVE</span></span> 
  
> <span data-ttu-id="52fba-130">**DoCopyProps** следует выполнять операции перемещения вместо операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="52fba-130">**DoCopyProps** should perform a move operation instead of a copy operation.</span></span> <span data-ttu-id="52fba-131">Если этот флаг не задан, **DoCopyProps** выполняет операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="52fba-131">When this flag is not set, **DoCopyProps** performs a copy operation.</span></span> 
    
<span data-ttu-id="52fba-132">MAPI_NOREPLACE</span><span class="sxs-lookup"><span data-stu-id="52fba-132">MAPI_NOREPLACE</span></span> 
  
> <span data-ttu-id="52fba-133">Не следует перезаписывать существующие свойства в целевой объект.</span><span class="sxs-lookup"><span data-stu-id="52fba-133">Existing properties in the destination object should not be overwritten.</span></span> <span data-ttu-id="52fba-134">Если этот флаг не задан, **DoCopyProps** перезаписывает существующие свойства.</span><span class="sxs-lookup"><span data-stu-id="52fba-134">When this flag is not set, **DoCopyProps** overwrites existing properties.</span></span> 
    
 <span data-ttu-id="52fba-135">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="52fba-135">_lppProblems_</span></span>
  
> <span data-ttu-id="52fba-136">[in, out] На входе указатель указатель на структуру [SPropProblemArray](spropproblemarray.md) ; в противном случае — значение NULL, указывает, не требуется выполнять сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="52fba-136">[in, out] On input, a pointer to a pointer to an [SPropProblemArray](spropproblemarray.md) structure; otherwise, NULL, which indicates no need for error information.</span></span> <span data-ttu-id="52fba-137">Если _lppProblems_ допустимый указатель на входные данные, **DoCopyProps** возвращает подробные сведения об ошибках в копирование одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="52fba-137">If  _lppProblems_ is a valid pointer on input, **DoCopyProps** returns detailed information about errors in copying one or more properties.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="52fba-138">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="52fba-138">Return value</span></span>

<span data-ttu-id="52fba-139">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="52fba-139">S_OK</span></span> 
  
> <span data-ttu-id="52fba-140">Свойства были успешно скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="52fba-140">Properties were successfully copied or moved.</span></span>
    
<span data-ttu-id="52fba-141">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="52fba-141">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="52fba-142">Свойство так, чтобы скопировать или переместить уже существует в целевой объект и флаг MAPI_NOREPLACE.</span><span class="sxs-lookup"><span data-stu-id="52fba-142">A property to be copied or moved already exists in the destination object and the MAPI_NOREPLACE flag is set.</span></span> 
    
<span data-ttu-id="52fba-143">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="52fba-143">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="52fba-144">Исходный объект прямо или косвенно содержит целевой объект.</span><span class="sxs-lookup"><span data-stu-id="52fba-144">The source object directly or indirectly contains the destination object.</span></span> <span data-ttu-id="52fba-145">Важные может быть выполнено перед был обнаружен это условие, поэтому исходный и целевой объекты частично могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="52fba-145">Significant work might have been performed before this condition was discovered, so the source and destination objects might be partially modified.</span></span> 
    
<span data-ttu-id="52fba-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="52fba-146">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="52fba-147">Интерфейс, определенного параметром _lpSrcInterface_ не поддерживается объектом источника или интерфейса, определенного параметром _lpDestInterface_ не поддерживается в целевой объект.</span><span class="sxs-lookup"><span data-stu-id="52fba-147">The interface identified by the  _lpSrcInterface_ parameter is not supported by the source object, or the interface identified by the  _lpDestInterface_ parameter is not supported by the destination object.</span></span> 
    
<span data-ttu-id="52fba-148">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="52fba-148">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="52fba-149">Предпринята попытка получить доступ к объекту, для которого вызывающий не имеет разрешений.</span><span class="sxs-lookup"><span data-stu-id="52fba-149">An attempt was made to access an object for which the caller has insufficient permissions.</span></span> <span data-ttu-id="52fba-150">Эта ошибка возвращается в том случае, если в целевой объект совпадает с исходным объектом.</span><span class="sxs-lookup"><span data-stu-id="52fba-150">This error is returned if the destination object is the same as the source object.</span></span>
    
<span data-ttu-id="52fba-151">Возможные значения могут быть возвращены в структуре **SPropProblemArray** , но не как возвращаемые значения для **DoCopyProps**.</span><span class="sxs-lookup"><span data-stu-id="52fba-151">The following values can be returned in the **SPropProblemArray** structure, but not as return values for **DoCopyProps**.</span></span> <span data-ttu-id="52fba-152">Эти ошибки относятся к одному свойству.</span><span class="sxs-lookup"><span data-stu-id="52fba-152">These errors apply to a single property.</span></span>
  
<span data-ttu-id="52fba-153">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="52fba-153">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="52fba-154">Либо был установлен флажок MAPI_UNICODE и **DoCopyProps** не поддерживает Юникод, или MAPI_UNICODE не было установлено и **DoCopyProps** поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="52fba-154">Either the MAPI_UNICODE flag was set and **DoCopyProps** does not support Unicode, or MAPI_UNICODE was not set and **DoCopyProps** supports only Unicode.</span></span> 
    
<span data-ttu-id="52fba-155">MAPI_E_COMPUTED</span><span class="sxs-lookup"><span data-stu-id="52fba-155">MAPI_E_COMPUTED</span></span> 
  
> <span data-ttu-id="52fba-156">Невозможно изменить свойство вызывающим абонентом, так как он является свойством только для чтения, вычисленный владельцем конечного объекта.</span><span class="sxs-lookup"><span data-stu-id="52fba-156">The property cannot be modified by the caller because it is a read-only property, computed by the owner of the destination object.</span></span> <span data-ttu-id="52fba-157">Эта ошибка не является очень неблагоприятных; вызывающего абонента, должна поддерживать операции копирования для продолжения.</span><span class="sxs-lookup"><span data-stu-id="52fba-157">This error is not severe; the caller should allow the copy operation to continue.</span></span>
    
<span data-ttu-id="52fba-158">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="52fba-158">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="52fba-159">Недопустимый тип свойства.</span><span class="sxs-lookup"><span data-stu-id="52fba-159">The property type is invalid.</span></span>
    
<span data-ttu-id="52fba-160">MAPI_E_UNEXPECTED_TYPE</span><span class="sxs-lookup"><span data-stu-id="52fba-160">MAPI_E_UNEXPECTED_TYPE</span></span> 
  
> <span data-ttu-id="52fba-161">Тип свойства не является типом, требующей вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="52fba-161">The property type is not the type that the caller expects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="52fba-162">Замечания</span><span class="sxs-lookup"><span data-stu-id="52fba-162">Remarks</span></span>

<span data-ttu-id="52fba-163">Метод **IMAPISupport::DoCopyProps** реализуется для объектов поддержки поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="52fba-163">The **IMAPISupport::DoCopyProps** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="52fba-164">Поставщики хранилища сообщений можно вызвать **DoCopyProps** , чтобы реализовать метод [IMAPIProp::CopyProps](imapiprop-copyprops.md) для своих папок и сообщений.</span><span class="sxs-lookup"><span data-stu-id="52fba-164">Message store providers can call **DoCopyProps** to implement the [IMAPIProp::CopyProps](imapiprop-copyprops.md) method for their folders and messages.</span></span> <span data-ttu-id="52fba-165">**DoCopyProps** копирование или перемещение свойств, который определяются в массиве тег свойства, на который указывает _lpIncludeProps_ , и, представленные в объект, на который указывает _lpSrcObj_.</span><span class="sxs-lookup"><span data-stu-id="52fba-165">**DoCopyProps** copies or moves the properties that are identified in the property tag array pointed to by  _lpIncludeProps_ and that are present in the object pointed to by  _lpSrcObj_.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="52fba-166">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="52fba-166">Notes to callers</span></span>

<span data-ttu-id="52fba-167">При копировании свойств между объектами одного типа, таких как два сообщения параметры _lpSrcInterface_ и _lpDestInterface_ должен содержать те же интерфейс идентификатор и _lpSrcObj_ и _lpDestObj_ параметров должен указывать на объекты одного типа.</span><span class="sxs-lookup"><span data-stu-id="52fba-167">When you copy properties between objects of the same type, such as two messages, the  _lpSrcInterface_ and  _lpDestInterface_ parameters must contain the same interface identifier, and the  _lpSrcObj_ and  _lpDestObj_ parameters must point to objects of the same type.</span></span> <span data-ttu-id="52fba-168">Если _lpDestInterface_ имеет значение NULL, **DoCopyProps** возвращает MAPI_E_INVALID_PARAMETER.</span><span class="sxs-lookup"><span data-stu-id="52fba-168">If  _lpDestInterface_ is set to NULL, **DoCopyProps** returns MAPI_E_INVALID_PARAMETER.</span></span> <span data-ttu-id="52fba-169">Если значение _lpDestInterface_ идентификатор приемлемой интерфейса, но набор _lpDestObj_ недопустимый указатель результаты непредсказуемы.</span><span class="sxs-lookup"><span data-stu-id="52fba-169">If you set  _lpDestInterface_ to an acceptable interface identifier, but set  _lpDestObj_ to an invalid pointer, the results are unpredictable.</span></span> <span data-ttu-id="52fba-170">Вероятнее всего поставщика завершится с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="52fba-170">Most likely your provider will fail.</span></span> 
  
<span data-ttu-id="52fba-171">Установите для флага MAPI_NOREPLACE не любое из свойств в целевой объект, требуется перезаписать.</span><span class="sxs-lookup"><span data-stu-id="52fba-171">Set the MAPI_NOREPLACE flag if you do not want any of the properties in the destination object to be overwritten.</span></span> <span data-ttu-id="52fba-172">Свойства в целевом объекте, существующих в исходном объекте и не перезаписываются не удалить или изменить.</span><span class="sxs-lookup"><span data-stu-id="52fba-172">Properties in the destination object that exist in the source object and are not overwritten are not deleted or modified.</span></span>
  
<span data-ttu-id="52fba-173">Чтобы скопировать список получателей сообщения, включите свойство **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) в массиве тег свойство указывает параметр _lpIncludeProps_ .</span><span class="sxs-lookup"><span data-stu-id="52fba-173">To copy a message's recipient list, include the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in the property tag array pointed to by the  _lpIncludeProps_ parameter.</span></span> <span data-ttu-id="52fba-174">Чтобы скопировать вложений сообщений, включите свойство **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="52fba-174">To copy the message's attachments, include the **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property.</span></span> 
  
<span data-ttu-id="52fba-175">Чтобы скопировать папку или иерархии контейнер адресной книги или таблицу содержимого, включают **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) или **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) в массиве тега свойства.</span><span class="sxs-lookup"><span data-stu-id="52fba-175">To copy a folder or address book container's hierarchy or contents table, include **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) or **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) in the property tag array.</span></span> <span data-ttu-id="52fba-176">Чтобы включить таблицу связанного содержимого папки, добавьте свойство **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) в массиве.</span><span class="sxs-lookup"><span data-stu-id="52fba-176">To include a folder's associated contents table, include the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property in the array.</span></span>
  
<span data-ttu-id="52fba-177">Если вложенные папки копирования или перемещения, их содержимое перемещаются или копируются полностью, независимо от того, использование свойств, указанный в параметре **SPropTagArray** структуры.</span><span class="sxs-lookup"><span data-stu-id="52fba-177">If subfolders are copied or moved, their contents are copied or moved in their entirety, regardless of the use of properties indicated by the **SPropTagArray** structure.</span></span> 
  
 <span data-ttu-id="52fba-178">**DoCopyProps** отчетов глобального ошибки, возникающие при работе с операции в целом и отдельных ошибки, возникающие при работе с одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="52fba-178">**DoCopyProps** reports global errors that occur with the operation as a whole, and individual errors that occur with one or more of the properties.</span></span> <span data-ttu-id="52fba-179">Эти отдельные ошибки помещаются в структуре **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="52fba-179">These individual errors are put in an **SPropProblemArray** structure.</span></span> <span data-ttu-id="52fba-180">Отчеты на уровне свойств, передав значение NULL, а не является допустимым указателем, для параметра свойство массива проблема структура об ошибках, можно отключить.</span><span class="sxs-lookup"><span data-stu-id="52fba-180">You can suppress error reporting at the property level by passing NULL, rather than a valid pointer, for the property problem array structure parameter.</span></span> 
  
<span data-ttu-id="52fba-181">Если вы хотите получать сведения об ошибках, передайте допустимый указатель структура **SPropProblemArray** с помощью параметра _lppProblems_ .</span><span class="sxs-lookup"><span data-stu-id="52fba-181">If you want to receive information about errors, pass a valid **SPropProblemArray** structure pointer in the  _lppProblems_ parameter.</span></span> <span data-ttu-id="52fba-182">При **DoCopyProps** возвращает значение S_OK, проверьте наличие возможных ошибок с помощью отдельных свойств в структуре.</span><span class="sxs-lookup"><span data-stu-id="52fba-182">When **DoCopyProps** returns S_OK, check for possible errors with individual properties in the structure.</span></span> <span data-ttu-id="52fba-183">Когда **DoCopyProps** возвращает ошибку, не информация возвращается в структуре **SPropProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="52fba-183">When **DoCopyProps** returns an error, no information is returned in the **SPropProblemArray** structure.</span></span> <span data-ttu-id="52fba-184">Вместо этого вызовите метод [IMAPISupport::GetLastError](imapisupport-getlasterror.md) , чтобы получить подробные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="52fba-184">Instead, call the [IMAPISupport::GetLastError](imapisupport-getlasterror.md) method to retrieve detailed error information.</span></span> 
  
<span data-ttu-id="52fba-185">Если **DoCopyProps** возвращает значение S_OK, освободите возвращенные структура **SPropProblemArray** путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="52fba-185">If **DoCopyProps** returns S_OK, free the returned **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="52fba-186">См. также</span><span class="sxs-lookup"><span data-stu-id="52fba-186">See also</span></span>



[<span data-ttu-id="52fba-187">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="52fba-187">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
  
[<span data-ttu-id="52fba-188">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="52fba-188">IMAPISupport::CopyMessages</span></span>](imapisupport-copymessages.md)
  
[<span data-ttu-id="52fba-189">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="52fba-189">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
  
[<span data-ttu-id="52fba-190">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="52fba-190">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="52fba-191">Каноническое свойство PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="52fba-191">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="52fba-192">Каноническое свойство PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="52fba-192">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="52fba-193">Каноническое свойство PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="52fba-193">PidTagFolderAssociatedContents Canonical Property</span></span>](pidtagfolderassociatedcontents-canonical-property.md)
  
[<span data-ttu-id="52fba-194">Каноническое свойство PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="52fba-194">PidTagMessageAttachments Canonical Property</span></span>](pidtagmessageattachments-canonical-property.md)
  
[<span data-ttu-id="52fba-195">Каноническое свойство PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="52fba-195">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="52fba-196">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="52fba-196">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="52fba-197">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="52fba-197">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="52fba-198">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="52fba-198">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

