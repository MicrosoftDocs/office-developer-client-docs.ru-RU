---
title: IAddrBookDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Details
api_type:
- COM
ms.assetid: 4eee4382-98c3-4714-8920-8d72edef00b8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5fbd20a6b5d5598b8fa51f9c369eefac9a1ea2e9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424681"
---
# <a name="iaddrbookdetails"></a><span data-ttu-id="feb19-103">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="feb19-103">IAddrBook::Details</span></span>

  
  
<span data-ttu-id="feb19-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="feb19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="feb19-105">Отображает диалоговое окно, в которое отображаются сведения о конкретной записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="feb19-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="feb19-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="feb19-106">Parameters</span></span>

 <span data-ttu-id="feb19-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="feb19-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="feb19-108">[in] Указатель на ручку родительского окна диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="feb19-108">[in] A pointer to a handle of the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="feb19-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="feb19-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="feb19-110">[in] Указатель на функцию на основе прототипа [DISMISSMODELESS](dismissmodeless.md) или NULL.</span><span class="sxs-lookup"><span data-stu-id="feb19-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="feb19-111">Этот член применяется только к безмежной версии диалогового окна, как указывается в заданной DIALOG_SDI флаге.</span><span class="sxs-lookup"><span data-stu-id="feb19-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="feb19-112">MAPI вызывает функцию **DISMISSMODELESS,** когда пользователь отклонять диалоговое окно без  режима адреса, информируя клиента, который вызывает Details, что диалоговое окно больше не активен.</span><span class="sxs-lookup"><span data-stu-id="feb19-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="feb19-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="feb19-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="feb19-114">[in] Указатель для контекстной информации, чтобы передать функции **DISMISSMODELESS,** указываемую _параметром lpfnDismiss._</span><span class="sxs-lookup"><span data-stu-id="feb19-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="feb19-115">Этот параметр применяется только к бесключевой версии диалогового окна, включив флаг DIALOG_SDI в параметр _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="feb19-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="feb19-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="feb19-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="feb19-117">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="feb19-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="feb19-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="feb19-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="feb19-119">[in] Указатель на идентификатор записи для записи, для которой отображаются сведения.</span><span class="sxs-lookup"><span data-stu-id="feb19-119">[in] A pointer to the entry identifier for the entry for which details are displayed.</span></span>
    
 <span data-ttu-id="feb19-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="feb19-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="feb19-121">[in] Указатель на функцию на основе прототипа [функции LPFNBUTTON.](lpfnbutton.md)</span><span class="sxs-lookup"><span data-stu-id="feb19-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="feb19-122">Функция **LPFNBUTTON добавляет** кнопку в диалоговое окно подробностей.</span><span class="sxs-lookup"><span data-stu-id="feb19-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="feb19-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="feb19-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="feb19-124">[in] Указатель на данные, которые использовались в качестве параметра для функции, указанной _параметром lpfButtonCallback._</span><span class="sxs-lookup"><span data-stu-id="feb19-124">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="feb19-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="feb19-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="feb19-126">[in] Указатель на строку, содержавшую текст, который необходимо применить к добавленной кнопке, если эта кнопка является размежещенной.</span><span class="sxs-lookup"><span data-stu-id="feb19-126">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="feb19-127">Параметр  _lpszButtonText должен_ быть NULL, если вам не нужна неопределяемая кнопка.</span><span class="sxs-lookup"><span data-stu-id="feb19-127">The  _lpszButtonText_ parameter should be NULL if you do not need an extensible button.</span></span> 
    
 <span data-ttu-id="feb19-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="feb19-128">_ulFlags_</span></span>
  
> <span data-ttu-id="feb19-129">[in] Немного флагов, которые контролируют тип текста для _параметра lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="feb19-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="feb19-130">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="feb19-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="feb19-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="feb19-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="feb19-132">Указывает, что **details** возвращает S_OK, если на самом деле в адрес внесены изменения; в **противном** случае Details возвращает S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="feb19-132">Indicates that **Details** returns S_OK if changes are actually made to the address; otherwise, **Details** returns S_FALSE.</span></span> 
    
<span data-ttu-id="feb19-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="feb19-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="feb19-134">Отображение модальной версии диалогового окна общего адреса, которое всегда отображается в Outlook клиентах.</span><span class="sxs-lookup"><span data-stu-id="feb19-134">Display the modal version of the common address dialog box, which is always shown in non-Outlook clients.</span></span> <span data-ttu-id="feb19-135">Этот флаг является взаимоисключающими с DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="feb19-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="feb19-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="feb19-136">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="feb19-137">Отображение бес режимной версии диалогового окна общего адреса.</span><span class="sxs-lookup"><span data-stu-id="feb19-137">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="feb19-138">Этот флаг игнорируется для Outlook клиентов.</span><span class="sxs-lookup"><span data-stu-id="feb19-138">This flag is ignored for non-Outlook clients.</span></span> 
    
<span data-ttu-id="feb19-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="feb19-139">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="feb19-140">Переданные строки находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="feb19-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="feb19-141">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="feb19-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="feb19-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="feb19-142">Return value</span></span>

<span data-ttu-id="feb19-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="feb19-143">S_OK</span></span> 
  
> <span data-ttu-id="feb19-144">Диалоговое окно с подробными сведениями было успешно отображно для записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="feb19-144">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="feb19-145">Примечания</span><span class="sxs-lookup"><span data-stu-id="feb19-145">Remarks</span></span>

<span data-ttu-id="feb19-146">Клиентские приложения звонят **методу Details,** чтобы отобразить диалоговое окно, которое содержит сведения о конкретной записи в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="feb19-146">Client applications call the **Details** method to display a dialog box that provides details about a particular entry in the address book.</span></span> <span data-ttu-id="feb19-147">Параметры  _lpfButtonCallback,_  _lpvButtonContext_ и  _lpszButtonText_ можно использовать для добавления кнопки, определенной клиентом, в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="feb19-147">You can use the  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="feb19-148">При нажатии кнопки MAPI вызывает функцию вызова, указанную  _lpfButtonCallback,_ передавая как идентификатор входа кнопки, так и данные  _в lpvButtonContext_.</span><span class="sxs-lookup"><span data-stu-id="feb19-148">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="feb19-149">Если вам не нужна неопределяемая кнопка,  _lpszButtonText_ должен быть NULL.</span><span class="sxs-lookup"><span data-stu-id="feb19-149">If you do not need an extensible button,  _lpszButtonText_ should be NULL.</span></span> 
  
 <span data-ttu-id="feb19-150">**Сведения** поддерживают строки символов Юникод; Строки Юникод преобразуются в формат многобайтной строки символов (MBCS) перед их отображением в диалоговом окне подробностей.</span><span class="sxs-lookup"><span data-stu-id="feb19-150">**Details** supports Unicode character strings; Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the details dialog box.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="feb19-151">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="feb19-151">MFCMAPI reference</span></span>

<span data-ttu-id="feb19-152">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="feb19-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="feb19-153">**Файл**</span><span class="sxs-lookup"><span data-stu-id="feb19-153">**File**</span></span>|<span data-ttu-id="feb19-154">**Функция**</span><span class="sxs-lookup"><span data-stu-id="feb19-154">**Function**</span></span>|<span data-ttu-id="feb19-155">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="feb19-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="feb19-156">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="feb19-156">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="feb19-157">CBaseDialog::OnOpenEntryID</span><span class="sxs-lookup"><span data-stu-id="feb19-157">CBaseDialog::OnOpenEntryID</span></span>  <br/> |<span data-ttu-id="feb19-158">MFCMAPI использует метод **Details** для отображения диалоговое окно, в которое отображаются сведения для записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="feb19-158">MFCMAPI uses the **Details** method to display a dialog box that shows the details for an address book entry.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="feb19-159">См. также</span><span class="sxs-lookup"><span data-stu-id="feb19-159">See also</span></span>



[<span data-ttu-id="feb19-160">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="feb19-160">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="feb19-161">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="feb19-161">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="feb19-162">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="feb19-162">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="feb19-163">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="feb19-163">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="feb19-164">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="feb19-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

