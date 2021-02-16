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
# <a name="imapisupportdetails"></a><span data-ttu-id="eab4f-103">IMAPISupport::Details</span><span class="sxs-lookup"><span data-stu-id="eab4f-103">IMAPISupport::Details</span></span>

  
  
<span data-ttu-id="eab4f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eab4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eab4f-105">Отображает диалоговое окно с подробными сведениями об определенной записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="eab4f-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="eab4f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eab4f-106">Parameters</span></span>

 <span data-ttu-id="eab4f-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="eab4f-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="eab4f-108">[out] Указатель на ладработку родительского окна возвращенного диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="eab4f-108">[out] A pointer to the handle to the parent window of the returned dialog box.</span></span>
    
 <span data-ttu-id="eab4f-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="eab4f-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="eab4f-110">[in] Указатель на функцию на основе [прототипа DISMISSMODELESS](dismissmodeless.md) или NULL.</span><span class="sxs-lookup"><span data-stu-id="eab4f-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="eab4f-111">Этот член применяется только к неавтомантной версии диалогового окна, как указано DIALOG_SDI флагом.</span><span class="sxs-lookup"><span data-stu-id="eab4f-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="eab4f-112">MAPI вызывает функцию **DISMISSMODELESS,** когда пользователь отклонять диалоговое окно без режима адресов, сообщая клиенту, который вызывает **IMAPISupport::D etails,** что диалоговое окно больше не активно.</span><span class="sxs-lookup"><span data-stu-id="eab4f-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **IMAPISupport::Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="eab4f-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="eab4f-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="eab4f-114">[in] Указатель на контекстную информацию, которая передается функции **DISMISSMODELESS,** на которую указывает параметр _lpfnDismiss._</span><span class="sxs-lookup"><span data-stu-id="eab4f-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="eab4f-115">Этот параметр применяется только к безмежной версии диалоговых окна, включив флаг DIALOG_SDI в параметр _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="eab4f-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="eab4f-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="eab4f-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="eab4f-117">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="eab4f-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="eab4f-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="eab4f-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="eab4f-119">[in] Указатель на идентификатор записи, для которого отображаются сведения.</span><span class="sxs-lookup"><span data-stu-id="eab4f-119">[in] A pointer to the entry identifier for which details are displayed.</span></span>
    
 <span data-ttu-id="eab4f-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="eab4f-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="eab4f-121">[in] Указатель на функцию на основе прототипа [функции LPFNBUTTON.](lpfnbutton.md)</span><span class="sxs-lookup"><span data-stu-id="eab4f-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="eab4f-122">Функция **LPFNBUTTON** добавляет кнопку в диалоговое окно сведений.</span><span class="sxs-lookup"><span data-stu-id="eab4f-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="eab4f-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="eab4f-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="eab4f-124">[in] Указатель на данные, используемые в качестве параметра для функции, указанной параметром _lpfButtonCallback._</span><span class="sxs-lookup"><span data-stu-id="eab4f-124">[in] A pointer to data used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="eab4f-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="eab4f-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="eab4f-126">[in] Указатель на строку, содержаную текст, который будет применен к добавленной кнопке, если эта кнопка является выдержатой.</span><span class="sxs-lookup"><span data-stu-id="eab4f-126">[in] A pointer to a string that contains text to be applied to the added button if that button is extensible.</span></span> <span data-ttu-id="eab4f-127">Параметр  _lpszButtonText должен_ иметь NULL, если вы не хотите использовать эту кнопку.</span><span class="sxs-lookup"><span data-stu-id="eab4f-127">The  _lpszButtonText_ parameter should be NULL if an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="eab4f-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="eab4f-128">_ulFlags_</span></span>
  
> <span data-ttu-id="eab4f-129">[in] Битоваяmas флагов, которая управляет типом текста для параметра _lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="eab4f-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="eab4f-130">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="eab4f-130">The following flag can be set:</span></span> 
    
<span data-ttu-id="eab4f-131">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="eab4f-131">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="eab4f-132">Отображение модальной версии общего диалоговых окна адресов.</span><span class="sxs-lookup"><span data-stu-id="eab4f-132">Display the modal version of the common address dialog box.</span></span> <span data-ttu-id="eab4f-133">Этот флаг является взаимоисключающими с DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="eab4f-133">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="eab4f-134">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="eab4f-134">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="eab4f-135">Отображает неавтомтную версию общего диалоговых окна адресов.</span><span class="sxs-lookup"><span data-stu-id="eab4f-135">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="eab4f-136">Этот флаг является взаимоисключающими с DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="eab4f-136">This flag is mutually exclusive with DIALOG_MODAL.</span></span> 
    
<span data-ttu-id="eab4f-137">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="eab4f-137">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="eab4f-138">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="eab4f-138">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="eab4f-139">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="eab4f-139">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="eab4f-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eab4f-140">Return value</span></span>

<span data-ttu-id="eab4f-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="eab4f-141">S_OK</span></span> 
  
> <span data-ttu-id="eab4f-142">Диалоговое окно сведений успешно отобразилось для записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="eab4f-142">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eab4f-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="eab4f-143">Remarks</span></span>

<span data-ttu-id="eab4f-144">Метод **IMAPISupport::D etails** реализован для объектов поддержки поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="eab4f-144">The **IMAPISupport::Details** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="eab4f-145">Поставщики адресных книг **звонят** в "Сведения", чтобы отобразить диалоговое окно с подробными сведениями об определенной записи в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="eab4f-145">Address book providers call **Details** to display a dialog box that gives details on a particular entry in the address book.</span></span> <span data-ttu-id="eab4f-146">Параметры  _lpfButtonCallback,_  _lpvButtonContext_ и  _lpszButtonText_ можно использовать для добавления в диалоговое окно определяемой клиентом кнопки.</span><span class="sxs-lookup"><span data-stu-id="eab4f-146">The  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters can be used to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="eab4f-147">При нажатии кнопки MAPI вызывает функцию вызова, на которая указывает _lpfButtonCallback,_ передавая идентификатор записи кнопки и данные _в lpvButtonContext._</span><span class="sxs-lookup"><span data-stu-id="eab4f-147">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="eab4f-148">Если вы не хотите использовать эту кнопку,  _lpszButtonText_ должен иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="eab4f-148">If an extensible button is not needed,  _lpszButtonText_ should be NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eab4f-149">См. также</span><span class="sxs-lookup"><span data-stu-id="eab4f-149">See also</span></span>



[<span data-ttu-id="eab4f-150">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="eab4f-150">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="eab4f-151">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="eab4f-151">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="eab4f-152">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="eab4f-152">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="eab4f-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="eab4f-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

