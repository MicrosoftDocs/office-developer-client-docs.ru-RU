---
title: HrDoABDetailsWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 27741887-8405-49ed-b080-613613faf91b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 47cf87fce0af3b866018bf03a34a05ea42cef82c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426683"
---
# <a name="hrdoabdetailswithprovideruid"></a><span data-ttu-id="ccf98-103">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="ccf98-103">HrDoABDetailsWithProviderUID</span></span>

  
  
<span data-ttu-id="ccf98-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccf98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccf98-105">Гарантирует, что метод **OpenEntry** открыт ожидаемым поставщиком адресных книг Exchange.</span><span class="sxs-lookup"><span data-stu-id="ccf98-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="ccf98-106">Эта функция работает аналогично [IAddrBook::D етаилс](iaddrbook-details.md) , но открывает код **entryID** , используя адресную книгу Exchange, определенную с помощью _пемсабпуид_.</span><span class="sxs-lookup"><span data-stu-id="ccf98-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) but opens **entryID** using the Exchange address book identified by  _pEmsabpUID_.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ccf98-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ccf98-107">Header file:</span></span>  <br/> |<span data-ttu-id="ccf98-108">абхелп. h</span><span class="sxs-lookup"><span data-stu-id="ccf98-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="ccf98-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="ccf98-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="ccf98-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="ccf98-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="ccf98-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="ccf98-111">Called by:</span></span>  <br/> |<span data-ttu-id="ccf98-112">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="ccf98-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithProviderUID(
  const MAPIUID   *pEmsabpUID,
  LPADRBOOK        pAddrBook,
  ULONG_PTR FAR *  lpulUIParam,
  LPFNDISMISS      lpfnDismiss,
  LPVOID           lpvDismissContext,
  ULONG            cbEntryID,
  LPENTRYID        lpEntryID,
  LPFNBUTTON       lpfButtonCallback,
  LPVOID           lpvButtonContext,
  LPSTR           lpszButtonText,
  ULONG            ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ccf98-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="ccf98-113">Parameters</span></span>

 <span data-ttu-id="ccf98-114">_пемсабпуид_</span><span class="sxs-lookup"><span data-stu-id="ccf98-114">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="ccf98-115">возврата Указатель на _емсабпуид_ , определяющий поставщика адресных книг Exchange, который должна использовать эта функция для отображения сведений об идентификаторе записи.</span><span class="sxs-lookup"><span data-stu-id="ccf98-115">[in] A pointer to an  _emsabpUID_ that identifies the Exchange address book provider this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="ccf98-116">Если входящий идентификатор записи не является идентификатором записи поставщика адресных книг Exchange, этот параметр игнорируется, а вызов функции выполняется точно так же, как [IAddrBook::D етаилс](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="ccf98-116">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="ccf98-117">Если этот параметр имеет значение NULL или нулевой МАПИУИД, эта функция также работает точно так же, как [IAddrBook::D етаилс](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="ccf98-117">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="ccf98-118">_паддрбук_</span><span class="sxs-lookup"><span data-stu-id="ccf98-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="ccf98-119">возврата Адресная книга, используемая для открытия идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="ccf98-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="ccf98-120">Он не может иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="ccf98-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="ccf98-121">_лпулуипарам_</span><span class="sxs-lookup"><span data-stu-id="ccf98-121">_lpulUIParam_</span></span>
  
> <span data-ttu-id="ccf98-122">вышли Дескриптор родительского окна для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="ccf98-122">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="ccf98-123">_лпфндисмисс_</span><span class="sxs-lookup"><span data-stu-id="ccf98-123">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="ccf98-124">возврата Указатель на функцию, основанную на прототипе **дисмиссмоделесс** , или значение null.</span><span class="sxs-lookup"><span data-stu-id="ccf98-124">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="ccf98-125">Этот элемент применяется только к немодальной версии диалогового окна, как указано в установленном флаге DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="ccf98-125">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="ccf98-126">MAPI вызывает функцию **дисмиссмоделесс** , когда пользователь закрывает диалоговое окно с немодальным адресом, что информирует клиента о вызове сведений о том, что диалоговое окно больше не активно.</span><span class="sxs-lookup"><span data-stu-id="ccf98-126">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="ccf98-127">_лпвдисмиссконтекст_</span><span class="sxs-lookup"><span data-stu-id="ccf98-127">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="ccf98-128">возврата Указатель на сведения о контексте, передаваемый функции **дисмиссмоделесс** , на которую указывает параметр _лпфндисмисс_ .</span><span class="sxs-lookup"><span data-stu-id="ccf98-128">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="ccf98-129">Этот параметр применяется только к немодальным версиям диалогового окна, включая флаг **DIALOG_SDI** в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="ccf98-129">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="ccf98-130">_кбентрид_</span><span class="sxs-lookup"><span data-stu-id="ccf98-130">_cbEntryID_</span></span>
  
> <span data-ttu-id="ccf98-131">возврата Количество байт в идентификаторе записи, заданном параметром _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="ccf98-131">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ccf98-132">_лпентрид_</span><span class="sxs-lookup"><span data-stu-id="ccf98-132">_lpEntryID_</span></span>
  
> <span data-ttu-id="ccf98-133">возврата Указатель на идентификатор записи, представляющий запись адресной книги, которую требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="ccf98-133">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="ccf98-134">_лпфбуттонкаллбакк_</span><span class="sxs-lookup"><span data-stu-id="ccf98-134">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="ccf98-135">возврата Указатель на функцию на основе прототипа функции **лпфнбуттон** .</span><span class="sxs-lookup"><span data-stu-id="ccf98-135">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="ccf98-136">Функция **лпфнбуттон** добавляет кнопку в диалоговое окно "сведения".</span><span class="sxs-lookup"><span data-stu-id="ccf98-136">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="ccf98-137">_лпвбуттонконтекст_</span><span class="sxs-lookup"><span data-stu-id="ccf98-137">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="ccf98-138">возврата Указатель на данные, которые использовались в качестве параметра для функции, заданной параметром _лпфбуттонкаллбакк_ .</span><span class="sxs-lookup"><span data-stu-id="ccf98-138">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="ccf98-139">_лпсзбуттонтекст_</span><span class="sxs-lookup"><span data-stu-id="ccf98-139">_lpszButtonText_</span></span>
  
> <span data-ttu-id="ccf98-140">возврата Указатель на строку, которая содержит текст, который будет применен к добавленной кнопке, если эта кнопка является расширяемой.</span><span class="sxs-lookup"><span data-stu-id="ccf98-140">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="ccf98-141">Если расширяемая кнопка не требуется, параметр _лпсзбуттонтекст_ должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="ccf98-141">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="ccf98-142">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ccf98-142">_ulFlags_</span></span>
  
> <span data-ttu-id="ccf98-143">возврата Битовая маска флагов, определяющая тип текста для параметра _лпсзбуттонтекст_ .</span><span class="sxs-lookup"><span data-stu-id="ccf98-143">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="ccf98-144">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="ccf98-144">The following flags can be set:</span></span> 
    
<span data-ttu-id="ccf98-145">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="ccf98-145">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="ccf98-146">Указывает, что Details возвращает TRUE, если изменения фактически вносятся в адрес; в противном случае сведения возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="ccf98-146">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="ccf98-147">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="ccf98-147">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="ccf98-148">Отображает модальную версию диалогового окна Общий адрес.</span><span class="sxs-lookup"><span data-stu-id="ccf98-148">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="ccf98-149">Этот флаг является взаимно исключающим с DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="ccf98-149">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="ccf98-150">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="ccf98-150">DIALOG_SDI</span></span>
  
> <span data-ttu-id="ccf98-151">Отображает немодальную версию диалогового окна общего адреса.</span><span class="sxs-lookup"><span data-stu-id="ccf98-151">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="ccf98-152">Этот флаг является взаимно исключающим с DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="ccf98-152">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="ccf98-153">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ccf98-153">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="ccf98-154">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="ccf98-154">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="ccf98-155">Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="ccf98-155">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

