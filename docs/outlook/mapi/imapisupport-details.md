---
title: Имаписуппортдетаилс
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322360"
---
# <a name="imapisupportdetails"></a><span data-ttu-id="d4748-103">IMAPISupport::Details</span><span class="sxs-lookup"><span data-stu-id="d4748-103">IMAPISupport::Details</span></span>

  
  
<span data-ttu-id="d4748-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4748-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4748-105">Отображает диалоговое окно, в котором отображаются сведения о конкретной записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="d4748-105">Displays a dialog box that shows details about a particular address book entry.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="d4748-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4748-106">Parameters</span></span>

 <span data-ttu-id="d4748-107">_Лпулуипарам_</span><span class="sxs-lookup"><span data-stu-id="d4748-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="d4748-108">вышли Указатель на дескриптор родительского окна возвращаемого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="d4748-108">[out] A pointer to the handle to the parent window of the returned dialog box.</span></span>
    
 <span data-ttu-id="d4748-109">_Лпфндисмисс_</span><span class="sxs-lookup"><span data-stu-id="d4748-109">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="d4748-110">возврата Указатель на функцию, основанную на прототипе [дисмиссмоделесс](dismissmodeless.md) , или значение null.</span><span class="sxs-lookup"><span data-stu-id="d4748-110">[in] A pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype, or NULL.</span></span> <span data-ttu-id="d4748-111">Этот элемент применяется только к немодальной версии диалогового окна, как указано в установленном флаге ДИАЛОГ_СДИ.</span><span class="sxs-lookup"><span data-stu-id="d4748-111">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="d4748-112">MAPI вызывает функцию **дисмиссмоделесс** , когда пользователь закрывает диалоговое окно с немодальным адресом, которое сообщает клиенту, вызывающему **имаписуппорт::D етаилс** , что диалоговое окно больше не является активным.</span><span class="sxs-lookup"><span data-stu-id="d4748-112">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling **IMAPISupport::Details** that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="d4748-113">_Лпвдисмиссконтекст_</span><span class="sxs-lookup"><span data-stu-id="d4748-113">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="d4748-114">возврата Указатель на сведения о контексте, передаваемый функции **дисмиссмоделесс** , на которую указывает параметр _лпфндисмисс_ .</span><span class="sxs-lookup"><span data-stu-id="d4748-114">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="d4748-115">Этот параметр применяется только к немодальным версиям диалогового окна, включая флаг ДИАЛОГ_СДИ в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="d4748-115">This parameter applies only to the modeless version of the dialog box, by including the DIALOG_SDI flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="d4748-116">_Кбентрид_</span><span class="sxs-lookup"><span data-stu-id="d4748-116">_cbEntryID_</span></span>
  
> <span data-ttu-id="d4748-117">возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="d4748-117">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="d4748-118">_Лпентрид_</span><span class="sxs-lookup"><span data-stu-id="d4748-118">_lpEntryID_</span></span>
  
> <span data-ttu-id="d4748-119">возврата Указатель на идентификатор записи, для которого отображаются сведения.</span><span class="sxs-lookup"><span data-stu-id="d4748-119">[in] A pointer to the entry identifier for which details are displayed.</span></span>
    
 <span data-ttu-id="d4748-120">_Лпфбуттонкаллбакк_</span><span class="sxs-lookup"><span data-stu-id="d4748-120">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="d4748-121">возврата Указатель на функцию на основе прототипа функции [лпфнбуттон](lpfnbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="d4748-121">[in] A pointer to a function based on the [LPFNBUTTON](lpfnbutton.md) function prototype.</span></span> <span data-ttu-id="d4748-122">Функция **лпфнбуттон** добавляет кнопку в диалоговое окно "сведения".</span><span class="sxs-lookup"><span data-stu-id="d4748-122">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="d4748-123">_Лпвбуттонконтекст_</span><span class="sxs-lookup"><span data-stu-id="d4748-123">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="d4748-124">возврата Указатель на данные, используемые в качестве параметра для функции, заданной параметром _лпфбуттонкаллбакк_ .</span><span class="sxs-lookup"><span data-stu-id="d4748-124">[in] A pointer to data used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="d4748-125">_Лпсзбуттонтекст_</span><span class="sxs-lookup"><span data-stu-id="d4748-125">_lpszButtonText_</span></span>
  
> <span data-ttu-id="d4748-126">возврата Указатель на строку, которая содержит текст, который будет применен к добавленной кнопке, если эта кнопка является расширяемой.</span><span class="sxs-lookup"><span data-stu-id="d4748-126">[in] A pointer to a string that contains text to be applied to the added button if that button is extensible.</span></span> <span data-ttu-id="d4748-127">Если расширяемая кнопка не требуется, параметр _лпсзбуттонтекст_ должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="d4748-127">The  _lpszButtonText_ parameter should be NULL if an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="d4748-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d4748-128">_ulFlags_</span></span>
  
> <span data-ttu-id="d4748-129">возврата Битовая маска флагов, определяющая тип текста для параметра _лпсзбуттонтекст_ .</span><span class="sxs-lookup"><span data-stu-id="d4748-129">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="d4748-130">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="d4748-130">The following flag can be set:</span></span> 
    
<span data-ttu-id="d4748-131">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="d4748-131">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="d4748-132">Отображение модальной версии диалогового окна Общий адрес.</span><span class="sxs-lookup"><span data-stu-id="d4748-132">Display the modal version of the common address dialog box.</span></span> <span data-ttu-id="d4748-133">Этот флаг является взаимно исключающим с ДИАЛОГ_СДИ.</span><span class="sxs-lookup"><span data-stu-id="d4748-133">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="d4748-134">ДИАЛОГ_СДИ</span><span class="sxs-lookup"><span data-stu-id="d4748-134">DIALOG_SDI</span></span>
  
>  <span data-ttu-id="d4748-135">Отображение немодальной версии диалогового окна Общий адрес.</span><span class="sxs-lookup"><span data-stu-id="d4748-135">Display the modeless version of the common address dialog box.</span></span> <span data-ttu-id="d4748-136">Этот флаг является взаимно исключающим с ДИАЛОГ_МОДАЛ.</span><span class="sxs-lookup"><span data-stu-id="d4748-136">This flag is mutually exclusive with DIALOG_MODAL.</span></span> 
    
<span data-ttu-id="d4748-137">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d4748-137">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d4748-138">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="d4748-138">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="d4748-139">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="d4748-139">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d4748-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4748-140">Return value</span></span>

<span data-ttu-id="d4748-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="d4748-141">S_OK</span></span> 
  
> <span data-ttu-id="d4748-142">Диалоговое окно "сведения" успешно отображено для записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="d4748-142">The details dialog box was successfully displayed for the address book entry.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d4748-143">Замечания</span><span class="sxs-lookup"><span data-stu-id="d4748-143">Remarks</span></span>

<span data-ttu-id="d4748-144">Метод **имаписуппорт::D етаилс** реализован для объектов поддержки поставщика адресных книг.</span><span class="sxs-lookup"><span data-stu-id="d4748-144">The **IMAPISupport::Details** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="d4748-145">Поставщики адресных книг вызывают **сведения** для отображения диалогового окна, в котором содержатся сведения о конкретной записи в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="d4748-145">Address book providers call **Details** to display a dialog box that gives details on a particular entry in the address book.</span></span> <span data-ttu-id="d4748-146">С помощью параметров _лпфбуттонкаллбакк_, _лпвбуттонконтекст_и _лпсзбуттонтекст_ можно добавить клиентскую кнопку в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="d4748-146">The  _lpfButtonCallback_,  _lpvButtonContext_, and  _lpszButtonText_ parameters can be used to add a client-defined button to the dialog box.</span></span> <span data-ttu-id="d4748-147">При нажатии кнопки MAPI вызывает функцию обратного вызова, на которую указывает _лпфбуттонкаллбакк_, передавая как идентификатор элемента кнопки, так и данные в _лпвбуттонконтекст_.</span><span class="sxs-lookup"><span data-stu-id="d4748-147">When the button is clicked, MAPI calls the callback function pointed to by  _lpfButtonCallback_, passing both the entry identifier of the button and the data in  _lpvButtonContext_.</span></span> <span data-ttu-id="d4748-148">Если расширяемая кнопка не требуется, _лпсзбуттонтекст_ должна иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="d4748-148">If an extensible button is not needed,  _lpszButtonText_ should be NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d4748-149">См. также</span><span class="sxs-lookup"><span data-stu-id="d4748-149">See also</span></span>



[<span data-ttu-id="d4748-150">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="d4748-150">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="d4748-151">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="d4748-151">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="d4748-152">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="d4748-152">LPFNBUTTON</span></span>](lpfnbutton.md)
  
[<span data-ttu-id="d4748-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d4748-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

