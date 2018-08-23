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
ms.openlocfilehash: e240ec4e7a61b9e7484f467926501f8c5f5a59f8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592348"
---
# <a name="iaddrbookdetails"></a><span data-ttu-id="b3a53-103">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="b3a53-103">IAddrBook::Details</span></span>

  
  
<span data-ttu-id="b3a53-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3a53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3a53-105">Отображает диалоговое окно, которое предоставляет подробные сведения о записи определенного адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b3a53-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="b3a53-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b3a53-106">Parameters</span></span>

 <span data-ttu-id="b3a53-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b3a53-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="b3a53-108">[in] Указатель на дескриптор родительского окна для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="b3a53-108">[in] A pointer to a handle of the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="b3a53-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="b3a53-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="b3a53-110">[in] Указатель на функцию, на основе [DISMISSMODELESS](dismissmodeless.md) прототип, или значение NULL.</span><span class="sxs-lookup"><span data-stu-id="b3a53-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="b3a53-111">Этот член применим только к безрежимным версии диалоговом окне, указанной флагом DIALOG_SDI задаваемая.</span><span class="sxs-lookup"><span data-stu-id="b3a53-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="b3a53-112">MAPI вызывает **DISMISSMODELESS** функцию, если пользователь не закрывает диалоговом окне безрежимным адреса клиента, который вызывает диалоговое окно не является активной **Подробные сведения** о том.</span><span class="sxs-lookup"><span data-stu-id="b3a53-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="b3a53-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="b3a53-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="b3a53-114">[in] Указатель на сведения о контексте для передачи **DISMISSMODELESS** функции, с помощью параметра _lpfnDismiss_ .</span><span class="sxs-lookup"><span data-stu-id="b3a53-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="b3a53-115">Этот параметр применяется только к безрежимным версии диалоговом окне, включая флаг DIALOG_SDI с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="b3a53-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="b3a53-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b3a53-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="b3a53-117">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b3a53-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b3a53-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="b3a53-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="b3a53-119">[in] Указатель на идентификатор записи для входа, для которого отображаются подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="b3a53-119">[in] A pointer to the entry identifier for the entry for which details are displayed.</span></span>
    
 <span data-ttu-id="b3a53-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="b3a53-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="b3a53-121">[in] Указатель на функцию на основании прототипа функции [LPFNBUTTON](lpfnbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="b3a53-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="b3a53-122">В функции **LPFNBUTTON** добавляется кнопка в диалоговом окне "Подробности".</span><span class="sxs-lookup"><span data-stu-id="b3a53-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="b3a53-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="b3a53-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="b3a53-124">[in] Указатель на данные, используемый в качестве параметра для функции, указанного с помощью параметра _lpfButtonCallback_ .</span><span class="sxs-lookup"><span data-stu-id="b3a53-124">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="b3a53-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="b3a53-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="b3a53-126">[in] Указатель на строку, которая содержит текст, который применяется для кнопки добавлены, если эта кнопка является расширяемым.</span><span class="sxs-lookup"><span data-stu-id="b3a53-126">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="b3a53-127">Параметр _lpszButtonText_ должен иметь значение NULL, если нет необходимости расширяемая кнопка.</span><span class="sxs-lookup"><span data-stu-id="b3a53-127">The  _lpszButtonText_ parameter should be NULL if you do not need an extensible button.</span></span> 
    
 <span data-ttu-id="b3a53-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b3a53-128">_ulFlags_</span></span>
  
> <span data-ttu-id="b3a53-129">[in] Битовая маска флаги, определяющее тип текста для параметра _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="b3a53-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="b3a53-130">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="b3a53-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="b3a53-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="b3a53-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="b3a53-132">Указывает, что **сведения о** возвращает значение S_OK при внесении фактически изменений на адрес; в противном случае **сведения о** возвращает S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="b3a53-132">Indicates that **Details** returns S_OK if changes are actually made to the address; otherwise, **Details** returns S_FALSE.</span></span> 
    
<span data-ttu-id="b3a53-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="b3a53-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="b3a53-134">Отображение модального версии общие адреса диалогового окна, которая всегда находится в отличные от Outlook.</span><span class="sxs-lookup"><span data-stu-id="b3a53-134">Display the modal version of the common address dialog box, which is always shown in non-Outlook clients.</span></span> <span data-ttu-id="b3a53-135">Этот флаг является взаимоисключающим с DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="b3a53-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="b3a53-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="b3a53-136">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="b3a53-137">Отображение безрежимным версии стандартным диалоговым окном адрес.</span><span class="sxs-lookup"><span data-stu-id="b3a53-137">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="b3a53-138">Этот флаг игнорируется для клиентов, не являющиеся Outlook.</span><span class="sxs-lookup"><span data-stu-id="b3a53-138">This flag is ignored for non-Outlook clients.</span></span> 
    
<span data-ttu-id="b3a53-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b3a53-139">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b3a53-140">Строки переданное хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="b3a53-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="b3a53-141">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="b3a53-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b3a53-142">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="b3a53-142">Return value</span></span>

<span data-ttu-id="b3a53-143">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="b3a53-143">S_OK</span></span> 
  
> <span data-ttu-id="b3a53-144">Для записи адресной книги был успешно отображается диалоговое окно "Подробности".</span><span class="sxs-lookup"><span data-stu-id="b3a53-144">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b3a53-145">Замечания</span><span class="sxs-lookup"><span data-stu-id="b3a53-145">Remarks</span></span>

<span data-ttu-id="b3a53-146">Клиентские приложения вызовите метод **сведений** для отображения диалогового окна, который предоставляет подробные сведения о конкретной записи в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="b3a53-146">Client applications call the **Details** method to display a dialog box that provides details about a particular entry in the address book.</span></span> <span data-ttu-id="b3a53-147">Чтобы добавить кнопку определенного клиента в диалоговое окно, можно использовать параметры _lpfButtonCallback_, _lpvButtonContext_и _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="b3a53-147">You can use the  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="b3a53-148">При нажатии кнопки MAPI вызывает функцию обратного вызова, на который указывает _lpfButtonCallback_, передав запись идентификатора кнопки и данные в _lpvButtonContext_.</span><span class="sxs-lookup"><span data-stu-id="b3a53-148">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="b3a53-149">Если вам не требуется расширяемая кнопка, _lpszButtonText_ должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="b3a53-149">If you do not need an extensible button,  _lpszButtonText_ should be NULL.</span></span> 
  
 <span data-ttu-id="b3a53-150">**Сведения о** поддерживает Юникод строк символов; Строки Юникод преобразуются в формат многобайтовой строки (MBCS), прежде чем они будут отображаться в диалоговом окне сведения о.</span><span class="sxs-lookup"><span data-stu-id="b3a53-150">**Details** supports Unicode character strings; Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the details dialog box.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b3a53-151">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="b3a53-151">MFCMAPI reference</span></span>

<span data-ttu-id="b3a53-152">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="b3a53-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b3a53-153">**����**</span><span class="sxs-lookup"><span data-stu-id="b3a53-153">**File**</span></span>|<span data-ttu-id="b3a53-154">**�������**</span><span class="sxs-lookup"><span data-stu-id="b3a53-154">**Function**</span></span>|<span data-ttu-id="b3a53-155">**�����������**</span><span class="sxs-lookup"><span data-stu-id="b3a53-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b3a53-156">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="b3a53-156">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="b3a53-157">CBaseDialog::OnOpenEntryID</span><span class="sxs-lookup"><span data-stu-id="b3a53-157">CBaseDialog::OnOpenEntryID</span></span>  <br/> |<span data-ttu-id="b3a53-158">Mfcmapi (en) использует метод **сведений** для отображения диалогового окна, который показывает сведения для записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b3a53-158">MFCMAPI uses the **Details** method to display a dialog box that shows the details for an address book entry.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b3a53-159">См. также</span><span class="sxs-lookup"><span data-stu-id="b3a53-159">See also</span></span>



[<span data-ttu-id="b3a53-160">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="b3a53-160">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="b3a53-161">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="b3a53-161">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="b3a53-162">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="b3a53-162">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="b3a53-163">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b3a53-163">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="b3a53-164">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="b3a53-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

