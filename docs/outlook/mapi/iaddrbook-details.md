---
title: иаддрбукдетаилс
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
# <a name="iaddrbookdetails"></a><span data-ttu-id="40f03-103">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="40f03-103">IAddrBook::Details</span></span>

  
  
<span data-ttu-id="40f03-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40f03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40f03-105">Отображает диалоговое окно, в котором отображаются сведения о конкретной записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="40f03-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="40f03-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="40f03-106">Parameters</span></span>

 <span data-ttu-id="40f03-107">_лпулуипарам_</span><span class="sxs-lookup"><span data-stu-id="40f03-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="40f03-108">возврата Указатель на дескриптор родительского окна для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="40f03-108">[in] A pointer to a handle of the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="40f03-109">_лпфндисмисс_</span><span class="sxs-lookup"><span data-stu-id="40f03-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="40f03-110">возврата Указатель на функцию, основанную на прототипе [дисмиссмоделесс](dismissmodeless.md) , или значение null.</span><span class="sxs-lookup"><span data-stu-id="40f03-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="40f03-111">Этот элемент применяется только к немодальной версии диалогового окна, как указано в установленном флаге DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="40f03-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="40f03-112">MAPI вызывает функцию **дисмиссмоделесс** , когда пользователь закрывает диалоговое окно с немодальным адресом, что информирует клиента о вызове **сведений о** том, что диалоговое окно больше не активно.</span><span class="sxs-lookup"><span data-stu-id="40f03-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="40f03-113">_лпвдисмиссконтекст_</span><span class="sxs-lookup"><span data-stu-id="40f03-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="40f03-114">возврата Указатель на сведения о контексте, передаваемый функции **дисмиссмоделесс** , на которую указывает параметр _лпфндисмисс_ .</span><span class="sxs-lookup"><span data-stu-id="40f03-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="40f03-115">Этот параметр применяется только к немодальным версиям диалогового окна, включая флаг DIALOG_SDI в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="40f03-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="40f03-116">_кбентрид_</span><span class="sxs-lookup"><span data-stu-id="40f03-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="40f03-117">возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="40f03-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="40f03-118">_лпентрид_</span><span class="sxs-lookup"><span data-stu-id="40f03-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="40f03-119">возврата Указатель на идентификатор записи, для которой отображаются сведения.</span><span class="sxs-lookup"><span data-stu-id="40f03-119">[in] A pointer to the entry identifier for the entry for which details are displayed.</span></span>
    
 <span data-ttu-id="40f03-120">_лпфбуттонкаллбакк_</span><span class="sxs-lookup"><span data-stu-id="40f03-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="40f03-121">возврата Указатель на функцию на основе прототипа функции [лпфнбуттон](lpfnbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="40f03-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="40f03-122">Функция **лпфнбуттон** добавляет кнопку в диалоговое окно "сведения".</span><span class="sxs-lookup"><span data-stu-id="40f03-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="40f03-123">_лпвбуттонконтекст_</span><span class="sxs-lookup"><span data-stu-id="40f03-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="40f03-124">возврата Указатель на данные, которые использовались в качестве параметра для функции, заданной параметром _лпфбуттонкаллбакк_ .</span><span class="sxs-lookup"><span data-stu-id="40f03-124">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="40f03-125">_лпсзбуттонтекст_</span><span class="sxs-lookup"><span data-stu-id="40f03-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="40f03-126">возврата Указатель на строку, которая содержит текст, который будет применен к добавленной кнопке, если эта кнопка является расширяемой.</span><span class="sxs-lookup"><span data-stu-id="40f03-126">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="40f03-127">Если не требуется расширяемая кнопка, параметр _лпсзбуттонтекст_ должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="40f03-127">The  _lpszButtonText_ parameter should be NULL if you do not need an extensible button.</span></span> 
    
 <span data-ttu-id="40f03-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="40f03-128">_ulFlags_</span></span>
  
> <span data-ttu-id="40f03-129">возврата Битовая маска флагов, определяющая тип текста для параметра _лпсзбуттонтекст_ .</span><span class="sxs-lookup"><span data-stu-id="40f03-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="40f03-130">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="40f03-130">The following flags can be set:</span></span> 
    
<span data-ttu-id="40f03-131">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="40f03-131">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="40f03-132">Указывает, что **сведения** возвращаются S_OK, если изменения фактически вносятся в адрес; в противном случае **сведения** возвращаются S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="40f03-132">Indicates that **Details** returns S_OK if changes are actually made to the address; otherwise, **Details** returns S_FALSE.</span></span> 
    
<span data-ttu-id="40f03-133">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="40f03-133">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="40f03-134">Отображение модальной версии диалогового окна Общий адрес, которая всегда отображается в клиентах, не относящихся к Outlook.</span><span class="sxs-lookup"><span data-stu-id="40f03-134">Display the modal version of the common address dialog box, which is always shown in non-Outlook clients.</span></span> <span data-ttu-id="40f03-135">Этот флаг является взаимно исключающим с DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="40f03-135">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="40f03-136">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="40f03-136">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="40f03-137">Отображение немодальной версии диалогового окна Общий адрес.</span><span class="sxs-lookup"><span data-stu-id="40f03-137">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="40f03-138">Этот флаг игнорируется для клиентов, не относящихся к Outlook.</span><span class="sxs-lookup"><span data-stu-id="40f03-138">This flag is ignored for non-Outlook clients.</span></span> 
    
<span data-ttu-id="40f03-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="40f03-139">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="40f03-140">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="40f03-140">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="40f03-141">Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="40f03-141">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="40f03-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="40f03-142">Return value</span></span>

<span data-ttu-id="40f03-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="40f03-143">S_OK</span></span> 
  
> <span data-ttu-id="40f03-144">Диалоговое окно "сведения" успешно отображено для записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="40f03-144">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="40f03-145">Примечания</span><span class="sxs-lookup"><span data-stu-id="40f03-145">Remarks</span></span>

<span data-ttu-id="40f03-146">Клиентские приложения вызывают метод **Details** для отображения диалогового окна, в котором представлены сведения о конкретной записи в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="40f03-146">Client applications call the **Details** method to display a dialog box that provides details about a particular entry in the address book.</span></span> <span data-ttu-id="40f03-147">С помощью параметров _лпфбуттонкаллбакк_, _лпвбуттонконтекст_и _лпсзбуттонтекст_ можно добавить клиентскую кнопку в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="40f03-147">You can use the  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="40f03-148">При нажатии кнопки MAPI вызывает функцию обратного вызова, на которую указывает _лпфбуттонкаллбакк_, передавая как идентификатор элемента кнопки, так и данные в _лпвбуттонконтекст_.</span><span class="sxs-lookup"><span data-stu-id="40f03-148">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="40f03-149">Если расширяемая кнопка не нужна, _лпсзбуттонтекст_ должна иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="40f03-149">If you do not need an extensible button,  _lpszButtonText_ should be NULL.</span></span> 
  
 <span data-ttu-id="40f03-150">**Details** поддерживает строки символов Юникода; Строки Юникод преобразуются в формат многобайтовых символов (MBCS), прежде чем они будут отображаться в диалоговом окне сведения.</span><span class="sxs-lookup"><span data-stu-id="40f03-150">**Details** supports Unicode character strings; Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the details dialog box.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="40f03-151">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="40f03-151">MFCMAPI reference</span></span>

<span data-ttu-id="40f03-152">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="40f03-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="40f03-153">**Файл**</span><span class="sxs-lookup"><span data-stu-id="40f03-153">**File**</span></span>|<span data-ttu-id="40f03-154">**Функция**</span><span class="sxs-lookup"><span data-stu-id="40f03-154">**Function**</span></span>|<span data-ttu-id="40f03-155">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="40f03-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="40f03-156">Баседиалог. cpp</span><span class="sxs-lookup"><span data-stu-id="40f03-156">BaseDialog.cpp</span></span>  <br/> |<span data-ttu-id="40f03-157">Кбаседиалог:: Онопенентрид</span><span class="sxs-lookup"><span data-stu-id="40f03-157">CBaseDialog::OnOpenEntryID</span></span>  <br/> |<span data-ttu-id="40f03-158">MFCMAPI использует метод **Details** для отображения диалогового окна, в котором отображаются сведения для записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="40f03-158">MFCMAPI uses the **Details** method to display a dialog box that shows the details for an address book entry.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="40f03-159">См. также</span><span class="sxs-lookup"><span data-stu-id="40f03-159">See also</span></span>



[<span data-ttu-id="40f03-160">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="40f03-160">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="40f03-161">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="40f03-161">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="40f03-162">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="40f03-162">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="40f03-163">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="40f03-163">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="40f03-164">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="40f03-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

