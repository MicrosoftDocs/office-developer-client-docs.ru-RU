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
# <a name="iaddrbookdetails"></a><span data-ttu-id="b71d8-103">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="b71d8-103">IAddrBook::Details</span></span>

  
  
<span data-ttu-id="b71d8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b71d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b71d8-105">Отображает диалоговое окно с подробными сведениями об определенной записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b71d8-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="b71d8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b71d8-106">Parameters</span></span>

 <span data-ttu-id="b71d8-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b71d8-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="b71d8-108">[in] Указатель на окне родительского окна для диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="b71d8-108">[in] A pointer to a handle of the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="b71d8-109">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="b71d8-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="b71d8-110">[in] Указатель на функцию на основе [прототипа DISMISSMODELESS](dismissmodeless.md) или NULL.</span><span class="sxs-lookup"><span data-stu-id="b71d8-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="b71d8-111">Этот член применяется только к неавтомантной версии диалогового окна, как указано DIALOG_SDI флага.</span><span class="sxs-lookup"><span data-stu-id="b71d8-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="b71d8-112">MAPI вызывает функцию **DISMISSMODELESS,** когда пользователь отклонять диалоговое окно без  режима адресов, сообщая клиенту, который вызывает details, о том, что диалоговое окно больше не активно.</span><span class="sxs-lookup"><span data-stu-id="b71d8-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="b71d8-113">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="b71d8-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="b71d8-114">[in] Указатель на контекстную информацию, которая передается функции **DISMISSMODELESS,** на которую указывает параметр _lpfnDismiss._</span><span class="sxs-lookup"><span data-stu-id="b71d8-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="b71d8-115">Этот параметр применяется только к безмежной версии диалоговых окна, включив флаг DIALOG_SDI в параметр _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="b71d8-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="b71d8-116">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b71d8-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="b71d8-117">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="b71d8-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b71d8-118">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="b71d8-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="b71d8-119">[in] Указатель на идентификатор записи, для которой отображаются сведения.</span><span class="sxs-lookup"><span data-stu-id="b71d8-119">[in] A pointer to the entry identifier for the entry for which details are displayed.</span></span>
    
 <span data-ttu-id="b71d8-120">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="b71d8-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="b71d8-121">[in] Указатель на функцию на основе прототипа [функции LPFNBUTTON.](lpfnbutton.md)</span><span class="sxs-lookup"><span data-stu-id="b71d8-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="b71d8-122">Функция **LPFNBUTTON** добавляет кнопку в диалоговое окно сведений.</span><span class="sxs-lookup"><span data-stu-id="b71d8-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="b71d8-123">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="b71d8-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="b71d8-124">[in] Указатель на данные, которые использовались в качестве параметра для функции, указанной параметром _lpfButtonCallback._</span><span class="sxs-lookup"><span data-stu-id="b71d8-124">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="b71d8-125">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="b71d8-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="b71d8-126">[in] Указатель на строку, содержаную текст, который необходимо применить к добавленной кнопке, если эта кнопка является выдержатой.</span><span class="sxs-lookup"><span data-stu-id="b71d8-126">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="b71d8-127">Параметр  _lpszButtonText_ должен иметь NULL, если не требуется кнопка с возможностью".</span><span class="sxs-lookup"><span data-stu-id="b71d8-127">The  _lpszButtonText_ parameter should be NULL if you do not need an extensible button.</span></span> 
    
 <span data-ttu-id="b71d8-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b71d8-128">_ulFlags_</span></span>
  
> <span data-ttu-id="b71d8-129">[in] Битоваяmas флагов, которая управляет типом текста для параметра _lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="b71d8-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="b71d8-130">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="b71d8-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="b71d8-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="b71d8-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="b71d8-132">Указывает, что **подробные** сведения S_OK, если фактически были внесены изменения в адрес; в **противном случае details** возвращает S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="b71d8-132">Indicates that **Details** returns S_OK if changes are actually made to the address; otherwise, **Details** returns S_FALSE.</span></span> 
    
<span data-ttu-id="b71d8-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="b71d8-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="b71d8-134">Отображение модальной версии общего диалоговых окна адресов, которая всегда отображается в клиентах, не в которых используется Outlook.</span><span class="sxs-lookup"><span data-stu-id="b71d8-134">Display the modal version of the common address dialog box, which is always shown in non-Outlook clients.</span></span> <span data-ttu-id="b71d8-135">Этот флаг является взаимоисключающими с DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="b71d8-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="b71d8-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="b71d8-136">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="b71d8-137">Отображает неавтомтную версию общего диалоговых окна адресов.</span><span class="sxs-lookup"><span data-stu-id="b71d8-137">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="b71d8-138">Этот флаг игнорируется для клиентов, не в том случае, если они не являются клиентами Outlook.</span><span class="sxs-lookup"><span data-stu-id="b71d8-138">This flag is ignored for non-Outlook clients.</span></span> 
    
<span data-ttu-id="b71d8-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b71d8-139">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b71d8-140">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="b71d8-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="b71d8-141">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="b71d8-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b71d8-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b71d8-142">Return value</span></span>

<span data-ttu-id="b71d8-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="b71d8-143">S_OK</span></span> 
  
> <span data-ttu-id="b71d8-144">Диалоговое окно сведений успешно отобразилось для записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b71d8-144">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b71d8-145">Примечания</span><span class="sxs-lookup"><span data-stu-id="b71d8-145">Remarks</span></span>

<span data-ttu-id="b71d8-146">Клиентские приложения **звонят методу Details,** чтобы отобразить диалоговое окно с подробными сведениями об определенной записи в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="b71d8-146">Client applications call the **Details** method to display a dialog box that provides details about a particular entry in the address book.</span></span> <span data-ttu-id="b71d8-147">Для добавления в диалоговое окно определяемой клиентом кнопки можно использовать параметры _lpfButtonCallback,_ _lpvButtonContext_ и _lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="b71d8-147">You can use the  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="b71d8-148">При нажатии кнопки MAPI вызывает функцию вызова, на которая указывает  _lpfButtonCallback,_ передавая идентификатор записи кнопки и данные  _в lpvButtonContext_.</span><span class="sxs-lookup"><span data-stu-id="b71d8-148">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="b71d8-149">Если вы не хотите использовать эту кнопку,  _lpszButtonText_ должен иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="b71d8-149">If you do not need an extensible button,  _lpszButtonText_ should be NULL.</span></span> 
  
 <span data-ttu-id="b71d8-150">**Подробные** сведения поддерживают строки символов Юникода; Строки Юникода преобразуются в формат многобайтовых строк (MBCS) перед их отображением в диалоговом окне сведений.</span><span class="sxs-lookup"><span data-stu-id="b71d8-150">**Details** supports Unicode character strings; Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the details dialog box.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b71d8-151">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b71d8-151">MFCMAPI reference</span></span>

<span data-ttu-id="b71d8-152">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="b71d8-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b71d8-153">**Файл**</span><span class="sxs-lookup"><span data-stu-id="b71d8-153">**File**</span></span>|<span data-ttu-id="b71d8-154">**Функция**</span><span class="sxs-lookup"><span data-stu-id="b71d8-154">**Function**</span></span>|<span data-ttu-id="b71d8-155">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="b71d8-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b71d8-156">BaseDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="b71d8-156">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="b71d8-157">CBaseDialog::OnOpenEntryID</span><span class="sxs-lookup"><span data-stu-id="b71d8-157">CBaseDialog::OnOpenEntryID</span></span>  <br/> |<span data-ttu-id="b71d8-158">MFCMAPI использует метод **Details,** чтобы отобразить диалоговое окно с подробными сведениями о записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b71d8-158">MFCMAPI uses the **Details** method to display a dialog box that shows the details for an address book entry.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b71d8-159">См. также</span><span class="sxs-lookup"><span data-stu-id="b71d8-159">See also</span></span>



[<span data-ttu-id="b71d8-160">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="b71d8-160">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="b71d8-161">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="b71d8-161">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="b71d8-162">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="b71d8-162">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="b71d8-163">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b71d8-163">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="b71d8-164">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="b71d8-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

