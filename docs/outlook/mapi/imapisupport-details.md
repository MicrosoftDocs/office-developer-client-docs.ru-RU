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
ms.openlocfilehash: 3c1bfccf635b96dd0744d888e69b4af5b8df0fa2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587875"
---
# <a name="imapisupportdetails"></a><span data-ttu-id="25e10-103">IMAPISupport::Details</span><span class="sxs-lookup"><span data-stu-id="25e10-103">IMAPISupport::Details</span></span>

  
  
<span data-ttu-id="25e10-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25e10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25e10-105">Отображает диалоговое окно, которое предоставляет подробные сведения о записи определенного адресной книги.</span><span class="sxs-lookup"><span data-stu-id="25e10-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="25e10-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="25e10-106">Parameters</span></span>

 <span data-ttu-id="25e10-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="25e10-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="25e10-108">[out] Указатель на дескриптор родительского окна, возвращенные диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="25e10-108">[out] A pointer to the handle to the parent window of the returned dialog box.</span></span>
    
 <span data-ttu-id="25e10-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="25e10-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="25e10-110">[in] Указатель на функцию, на основе [DISMISSMODELESS](dismissmodeless.md) прототип, или значение NULL.</span><span class="sxs-lookup"><span data-stu-id="25e10-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="25e10-111">Этот член применим только к безрежимным версии диалоговом окне, указанной флагом DIALOG_SDI задаваемая.</span><span class="sxs-lookup"><span data-stu-id="25e10-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="25e10-112">MAPI вызывает **DISMISSMODELESS** функцию, если пользователь не закрывает диалоговое окно безрежимным адрес, уведомляющее о клиента, который вызывает **IMAPISupport::Details** диалоговое окно не является активной.</span><span class="sxs-lookup"><span data-stu-id="25e10-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **IMAPISupport::Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="25e10-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="25e10-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="25e10-114">[in] Указатель на сведения о контексте для передачи **DISMISSMODELESS** функции, с помощью параметра _lpfnDismiss_ .</span><span class="sxs-lookup"><span data-stu-id="25e10-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="25e10-115">Этот параметр применяется только к безрежимным версии диалоговом окне, включая флаг DIALOG_SDI с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="25e10-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="25e10-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="25e10-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="25e10-117">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="25e10-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="25e10-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="25e10-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="25e10-119">[in] Указатель на идентификатор записи, для которого отображаются подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="25e10-119">[in] A pointer to the entry identifier for which details are displayed.</span></span>
    
 <span data-ttu-id="25e10-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="25e10-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="25e10-121">[in] Указатель на функцию на основании прототипа функции [LPFNBUTTON](lpfnbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="25e10-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="25e10-122">В функции **LPFNBUTTON** добавляется кнопка в диалоговом окне "Подробности".</span><span class="sxs-lookup"><span data-stu-id="25e10-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="25e10-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="25e10-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="25e10-124">[in] Указатель на данные, используемые как параметр для функции, указанного с помощью параметра _lpfButtonCallback_ .</span><span class="sxs-lookup"><span data-stu-id="25e10-124">[in] A pointer to data used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="25e10-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="25e10-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="25e10-126">[in] Указатель на строку, которая содержит текст, который будет применяться к добавлена кнопка Если кнопки является расширяемым.</span><span class="sxs-lookup"><span data-stu-id="25e10-126">[in] A pointer to a string that contains text to be applied to the added button if that button is extensible.</span></span> <span data-ttu-id="25e10-127">Параметр _lpszButtonText_ должен иметь значение NULL, если расширяемая кнопка не требуется.</span><span class="sxs-lookup"><span data-stu-id="25e10-127">The  _lpszButtonText_ parameter should be NULL if an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="25e10-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="25e10-128">_ulFlags_</span></span>
  
> <span data-ttu-id="25e10-129">[in] Битовая маска флаги, определяющее тип текста для параметра _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="25e10-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="25e10-130">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="25e10-130">The following flag can be set:</span></span> 
    
<span data-ttu-id="25e10-131">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="25e10-131">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="25e10-132">Отображение модального версии стандартным диалоговым окном адрес.</span><span class="sxs-lookup"><span data-stu-id="25e10-132">Display the modal version of the common address dialog box.</span></span> <span data-ttu-id="25e10-133">Этот флаг является взаимоисключающим с DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="25e10-133">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="25e10-134">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="25e10-134">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="25e10-135">Отображение безрежимным версии стандартным диалоговым окном адрес.</span><span class="sxs-lookup"><span data-stu-id="25e10-135">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="25e10-136">Этот флаг является взаимоисключающим с DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="25e10-136">This flag is mutually exclusive with DIALOG_MODAL.</span></span> 
    
<span data-ttu-id="25e10-137">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="25e10-137">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="25e10-138">Строки переданное хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="25e10-138">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="25e10-139">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="25e10-139">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="25e10-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="25e10-140">Return value</span></span>

<span data-ttu-id="25e10-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="25e10-141">S_OK</span></span> 
  
> <span data-ttu-id="25e10-142">Для записи адресной книги был успешно отображается диалоговое окно "Подробности".</span><span class="sxs-lookup"><span data-stu-id="25e10-142">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="25e10-143">Замечания</span><span class="sxs-lookup"><span data-stu-id="25e10-143">Remarks</span></span>

<span data-ttu-id="25e10-144">Метод **IMAPISupport::Details** реализуется для объектов поддержки поставщик адресной книги.</span><span class="sxs-lookup"><span data-stu-id="25e10-144">The **IMAPISupport::Details** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="25e10-145">Поставщиками адресной книги вызовите **сведений** для отображения диалогового окна, подробные сведения о конкретной записи в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="25e10-145">Address book providers call **Details** to display a dialog box that gives details on a particular entry in the address book.</span></span> <span data-ttu-id="25e10-146">Параметры _lpfButtonCallback_, _lpvButtonContext_и _lpszButtonText_ можно использовать для добавления кнопки определенные клиента в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="25e10-146">The  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters can be used to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="25e10-147">При нажатии кнопки MAPI вызывает функцию обратного вызова, на который указывает _lpfButtonCallback_, передав запись идентификатора кнопки и данные в _lpvButtonContext_.</span><span class="sxs-lookup"><span data-stu-id="25e10-147">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="25e10-148">Если не требуется расширяемая кнопка, _lpszButtonText_ должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="25e10-148">If an extensible button is not needed,  _lpszButtonText_ should be NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="25e10-149">См. также</span><span class="sxs-lookup"><span data-stu-id="25e10-149">See also</span></span>



[<span data-ttu-id="25e10-150">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="25e10-150">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="25e10-151">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="25e10-151">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="25e10-152">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="25e10-152">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="25e10-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="25e10-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

