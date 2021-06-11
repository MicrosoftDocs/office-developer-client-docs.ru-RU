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
# <a name="hrdoabdetailswithprovideruid"></a><span data-ttu-id="f0a54-103">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="f0a54-103">HrDoABDetailsWithProviderUID</span></span>

  
  
<span data-ttu-id="f0a54-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0a54-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0a54-105">Гарантирует, что метод **OpenEntry** откроется ожидаемым поставщиком Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="f0a54-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="f0a54-106">Эта функция работает аналогично [IAddrBook::D etails,](iaddrbook-details.md) но открывает **entryID** с помощью Exchange адресной книги, определенной _pEmsabpUID_.</span><span class="sxs-lookup"><span data-stu-id="f0a54-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) but opens **entryID** using the Exchange address book identified by  _pEmsabpUID_.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f0a54-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f0a54-107">Header file:</span></span>  <br/> |<span data-ttu-id="f0a54-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="f0a54-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="f0a54-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="f0a54-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="f0a54-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="f0a54-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="f0a54-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="f0a54-111">Called by:</span></span>  <br/> |<span data-ttu-id="f0a54-112">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="f0a54-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="f0a54-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="f0a54-113">Parameters</span></span>

 <span data-ttu-id="f0a54-114">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="f0a54-114">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="f0a54-115">[in] Указатель на _emsabpUID,_ который определяет поставщика Exchange адресной книги, которую эта функция должна использовать для отображения сведений об идентификаторе записи.</span><span class="sxs-lookup"><span data-stu-id="f0a54-115">[in] A pointer to an  _emsabpUID_ that identifies the Exchange address book provider this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="f0a54-116">Если идентификатор входной записи не является идентификатором записи поставщика Exchange адресной книги, этот параметр игнорируется, и вызов функции действует точно так же, как [iAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="f0a54-116">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="f0a54-117">Если этот параметр является NULL или нулевой MAPIUID, эта функция также действует точно так же, как [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="f0a54-117">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="f0a54-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="f0a54-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="f0a54-119">[in] Адресная книга, используемая для открытия идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="f0a54-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="f0a54-120">Это не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="f0a54-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="f0a54-121">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f0a54-121">_lpulUIParam_</span></span>
  
> <span data-ttu-id="f0a54-122">[вышел] Ручка родительского окна для диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f0a54-122">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="f0a54-123">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="f0a54-123">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="f0a54-124">[in] Указатель на функцию на основе прототипа **DISMISSMODELESS** или NULL.</span><span class="sxs-lookup"><span data-stu-id="f0a54-124">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="f0a54-125">Этот член применяется только к безмежной версии диалогового окна, как указывается в заданной DIALOG_SDI флаге.</span><span class="sxs-lookup"><span data-stu-id="f0a54-125">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="f0a54-126">MAPI вызывает функцию **DISMISSMODELESS,** когда пользователь отклонять диалоговое окно без режима адреса, информируя клиента, который вызывает Details, что диалоговое окно больше не активен.</span><span class="sxs-lookup"><span data-stu-id="f0a54-126">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="f0a54-127">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="f0a54-127">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="f0a54-128">[in] Указатель для контекстной информации, чтобы передать функции **DISMISSMODELESS,** указываемую _параметром lpfnDismiss._</span><span class="sxs-lookup"><span data-stu-id="f0a54-128">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="f0a54-129">Этот параметр применяется только к бесключевой версии диалогового окна, включив **флаг** DIALOG_SDI в _параметр ulFlags._</span><span class="sxs-lookup"><span data-stu-id="f0a54-129">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="f0a54-130">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f0a54-130">_cbEntryID_</span></span>
  
> <span data-ttu-id="f0a54-131">[in] Byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span><span class="sxs-lookup"><span data-stu-id="f0a54-131">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f0a54-132">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="f0a54-132">_lpEntryID_</span></span>
  
> <span data-ttu-id="f0a54-133">[in] Указатель на идентификатор записи, который представляет открытую запись адресной книги.</span><span class="sxs-lookup"><span data-stu-id="f0a54-133">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="f0a54-134">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="f0a54-134">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="f0a54-135">[in] Указатель на функцию на основе прототипа **функции LPFNBUTTON.**</span><span class="sxs-lookup"><span data-stu-id="f0a54-135">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="f0a54-136">Функция **LPFNBUTTON добавляет** кнопку в диалоговое окно подробностей.</span><span class="sxs-lookup"><span data-stu-id="f0a54-136">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="f0a54-137">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="f0a54-137">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="f0a54-138">[in] Указатель на данные, которые использовались в качестве параметра для функции, указанной _параметром lpfButtonCallback._</span><span class="sxs-lookup"><span data-stu-id="f0a54-138">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="f0a54-139">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="f0a54-139">_lpszButtonText_</span></span>
  
> <span data-ttu-id="f0a54-140">[in] Указатель на строку, содержавшую текст, который необходимо применить к добавленной кнопке, если эта кнопка является размежещенной.</span><span class="sxs-lookup"><span data-stu-id="f0a54-140">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="f0a54-141">Параметр  _lpszButtonText должен_ быть NULL, если не требуется размягкаемая кнопка.</span><span class="sxs-lookup"><span data-stu-id="f0a54-141">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="f0a54-142">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f0a54-142">_ulFlags_</span></span>
  
> <span data-ttu-id="f0a54-143">[in] Немного флагов, которые контролируют тип текста для _параметра lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="f0a54-143">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="f0a54-144">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="f0a54-144">The following flags can be set:</span></span> 
    
<span data-ttu-id="f0a54-145">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="f0a54-145">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="f0a54-146">Указывает, что Details возвращает TRUE, если на самом деле в адрес внесены изменения; в противном случае Details возвращает FALSE.</span><span class="sxs-lookup"><span data-stu-id="f0a54-146">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="f0a54-147">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="f0a54-147">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="f0a54-148">Отображает модную версию диалогового окна общего адреса.</span><span class="sxs-lookup"><span data-stu-id="f0a54-148">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="f0a54-149">Этот флаг является взаимоисключающими с DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="f0a54-149">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="f0a54-150">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="f0a54-150">DIALOG_SDI</span></span>
  
> <span data-ttu-id="f0a54-151">Отображает бес режимную версию диалогового окна общего адреса.</span><span class="sxs-lookup"><span data-stu-id="f0a54-151">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="f0a54-152">Этот флаг является взаимоисключающими с DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="f0a54-152">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="f0a54-153">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f0a54-153">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="f0a54-154">Переданные строки находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="f0a54-154">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="f0a54-155">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="f0a54-155">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

