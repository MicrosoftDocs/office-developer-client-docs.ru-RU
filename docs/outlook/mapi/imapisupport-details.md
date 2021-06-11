---
title: IMAPISupportDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Details
api_type:
- COM
ms.assetid: 1a62efa2-dd6b-4acb-a760-defa601c20c9
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bdc57a6e951e54640fe3c638977c6a5f16986e68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426781"
---
# <a name="imapisupportdetails"></a><span data-ttu-id="2de19-103">IMAPISupport::Details</span><span class="sxs-lookup"><span data-stu-id="2de19-103">IMAPISupport::Details</span></span>

  
  
<span data-ttu-id="2de19-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2de19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2de19-105">Отображает диалоговое окно, в которое отображаются сведения о конкретной записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="2de19-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
```cpp
HRESULT Details(
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="2de19-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="2de19-106">Parameters</span></span>

 <span data-ttu-id="2de19-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="2de19-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="2de19-108">[вышел] Указатель на ручку родительского окна возвращаемого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="2de19-108">[out] A pointer to the handle to the parent window of the returned dialog box.</span></span>
    
 <span data-ttu-id="2de19-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="2de19-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="2de19-110">[in] Указатель на функцию на основе прототипа [DISMISSMODELESS](dismissmodeless.md) или NULL.</span><span class="sxs-lookup"><span data-stu-id="2de19-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="2de19-111">Этот член применяется только к безмежной версии диалогового окна, как указывается в заданной DIALOG_SDI флаге.</span><span class="sxs-lookup"><span data-stu-id="2de19-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="2de19-112">MAPI вызывает функцию **DISMISSMODELESS,** когда пользователь отклонять диалоговое окно без режима адреса, информируя клиента, который вызывает **IMAPISupport::D etails,** что диалоговое окно больше не активен.</span><span class="sxs-lookup"><span data-stu-id="2de19-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **IMAPISupport::Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="2de19-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="2de19-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="2de19-114">[in] Указатель для контекстной информации, чтобы передать функции **DISMISSMODELESS,** указываемую _параметром lpfnDismiss._</span><span class="sxs-lookup"><span data-stu-id="2de19-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="2de19-115">Этот параметр применяется только к бесключевой версии диалогового окна, включив флаг DIALOG_SDI в параметр _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="2de19-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="2de19-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="2de19-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="2de19-117">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="2de19-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="2de19-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="2de19-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="2de19-119">[in] Указатель на идентификатор записи, для которого отображаются сведения.</span><span class="sxs-lookup"><span data-stu-id="2de19-119">[in] A pointer to the entry identifier for which details are displayed.</span></span>
    
 <span data-ttu-id="2de19-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="2de19-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="2de19-121">[in] Указатель на функцию на основе прототипа [функции LPFNBUTTON.](lpfnbutton.md)</span><span class="sxs-lookup"><span data-stu-id="2de19-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="2de19-122">Функция **LPFNBUTTON добавляет** кнопку в диалоговое окно подробностей.</span><span class="sxs-lookup"><span data-stu-id="2de19-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="2de19-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="2de19-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="2de19-124">[in] Указатель на данные, используемые в качестве параметра для функции, указанной _параметром lpfButtonCallback._</span><span class="sxs-lookup"><span data-stu-id="2de19-124">[in] A pointer to data used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="2de19-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="2de19-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="2de19-126">[in] Указатель на строку, содержавшую текст, который будет применяться к добавленной кнопке, если эта кнопка является размежещенной.</span><span class="sxs-lookup"><span data-stu-id="2de19-126">[in] A pointer to a string that contains text to be applied to the added button if that button is extensible.</span></span> <span data-ttu-id="2de19-127">Параметр  _lpszButtonText должен_ быть NULL, если не требуется размягкаемая кнопка.</span><span class="sxs-lookup"><span data-stu-id="2de19-127">The  _lpszButtonText_ parameter should be NULL if an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="2de19-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2de19-128">_ulFlags_</span></span>
  
> <span data-ttu-id="2de19-129">[in] Немного флагов, которые контролируют тип текста для _параметра lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="2de19-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="2de19-130">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="2de19-130">The following flag can be set:</span></span> 
    
<span data-ttu-id="2de19-131">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="2de19-131">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="2de19-132">Отображение модальной версии диалогового окна общего адреса.</span><span class="sxs-lookup"><span data-stu-id="2de19-132">Display the modal version of the common address dialog box.</span></span> <span data-ttu-id="2de19-133">Этот флаг является взаимоисключающими с DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="2de19-133">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="2de19-134">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="2de19-134">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="2de19-135">Отображение бес режимной версии диалогового окна общего адреса.</span><span class="sxs-lookup"><span data-stu-id="2de19-135">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="2de19-136">Этот флаг является взаимоисключающими с DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="2de19-136">This flag is mutually exclusive with DIALOG_MODAL.</span></span> 
    
<span data-ttu-id="2de19-137">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2de19-137">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2de19-138">Переданные строки находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="2de19-138">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="2de19-139">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="2de19-139">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2de19-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2de19-140">Return value</span></span>

<span data-ttu-id="2de19-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="2de19-141">S_OK</span></span> 
  
> <span data-ttu-id="2de19-142">Диалоговое окно с подробными сведениями было успешно отображно для записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="2de19-142">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2de19-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="2de19-143">Remarks</span></span>

<span data-ttu-id="2de19-144">Метод **IMAPISupport::D etails** реализован для объектов поддержки поставщиков адресных книг.</span><span class="sxs-lookup"><span data-stu-id="2de19-144">The **IMAPISupport::Details** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="2de19-145">Поставщики адресных книг **звонят в Details,** чтобы отобразить диалоговое окно, в которое будут представлены сведения о конкретной записи в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="2de19-145">Address book providers call **Details** to display a dialog box that gives details on a particular entry in the address book.</span></span> <span data-ttu-id="2de19-146">Параметры  _lpfButtonCallback,_  _lpvButtonContext_ и  _lpszButtonText_ можно использовать для добавления кнопки, определенной клиентом, в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="2de19-146">The  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters can be used to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="2de19-147">При нажатии кнопки MAPI вызывает функцию вызова, указанную  _lpfButtonCallback,_ передавая как идентификатор входа кнопки, так и данные  _в lpvButtonContext_.</span><span class="sxs-lookup"><span data-stu-id="2de19-147">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="2de19-148">Если не требуется размягкаемая кнопка,  _lpszButtonText_ должен быть NULL.</span><span class="sxs-lookup"><span data-stu-id="2de19-148">If an extensible button is not needed,  _lpszButtonText_ should be NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2de19-149">См. также</span><span class="sxs-lookup"><span data-stu-id="2de19-149">See also</span></span>



[<span data-ttu-id="2de19-150">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="2de19-150">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="2de19-151">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="2de19-151">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="2de19-152">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="2de19-152">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="2de19-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="2de19-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

