---
title: HrDoABDetailsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b4e7fed2-88e4-4e14-90b6-913a1b7e338a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 353a663071a9f23f0d2330169d3ac7747e047c2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421370"
---
# <a name="hrdoabdetailswithexchangecontext"></a><span data-ttu-id="e7921-103">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="e7921-103">HrDoABDetailsWithExchangeContext</span></span>

  
  
<span data-ttu-id="e7921-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7921-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7921-105">Гарантирует, что метод **OpenEntry** откроется ожидаемым поставщиком Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="e7921-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="e7921-106">Эта функция работает аналогично [IAddrBook::D etails,](iaddrbook-details.md)но открывает **entryID** с помощью Exchange адресной книги, определенной _параметром pEmsmdbUID._</span><span class="sxs-lookup"><span data-stu-id="e7921-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md), but opens the **entryID** using the Exchange address book identified by the  _pEmsmdbUID_ parameter.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e7921-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e7921-107">Header file:</span></span>  <br/> |<span data-ttu-id="e7921-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="e7921-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="e7921-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="e7921-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="e7921-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="e7921-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="e7921-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="e7921-111">Called by:</span></span>  <br/> |<span data-ttu-id="e7921-112">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="e7921-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithExchangeContext(
  LPMAPISESSION   pmsess,
  const MAPIUID  *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags,
);
```

## <a name="parameters"></a><span data-ttu-id="e7921-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="e7921-113">Parameters</span></span>

 <span data-ttu-id="e7921-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="e7921-114">_pmsess_</span></span>
  
> <span data-ttu-id="e7921-115">Журнал на **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="e7921-115">The logged on **IMAPISession**.</span></span> <span data-ttu-id="e7921-116">Это не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="e7921-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="e7921-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="e7921-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="e7921-118">Указатель на **emsmdbUID,** который определяет службу Exchange, которая содержит поставщик Exchange адресной книги, который используется функцией для открытия идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="e7921-118">A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange address book provider that is used by the function to open the entry identifier.</span></span> <span data-ttu-id="e7921-119">Если идентификатор входной записи не является идентификатором записи поставщика Exchange адресной книги, этот параметр игнорируется, и функция ведет себя как [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="e7921-119">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function behaves like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="e7921-120">Если этот параметр NULL или нулевой **MAPIUID,** эта функция также действует точно так же, как [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="e7921-120">If this parameter is NULL or a zero **MAPIUID**, this function also acts exactly like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> 
    
 <span data-ttu-id="e7921-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="e7921-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="e7921-122">[in] Адресная книга, используемая для открытия идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="e7921-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="e7921-123">Это не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="e7921-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="e7921-124">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="e7921-124">_lpulUIParam_</span></span>
  
> <span data-ttu-id="e7921-125">[вышел] Ручка родительского окна для диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e7921-125">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="e7921-126">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="e7921-126">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="e7921-127">[in] Указатель на функцию на основе прототипа **DISMISSMODELESS** или NULL.</span><span class="sxs-lookup"><span data-stu-id="e7921-127">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="e7921-128">Этот член применяется только к безмежной версии диалогового окна, как указывается в заданной DIALOG_SDI флаге.</span><span class="sxs-lookup"><span data-stu-id="e7921-128">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="e7921-129">MAPI вызывает функцию **DISMISSMODELESS,** когда пользователь отклонять диалоговое окно без режима адреса, информируя клиента, который вызывает Details, что диалоговое окно больше не активен.</span><span class="sxs-lookup"><span data-stu-id="e7921-129">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="e7921-130">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="e7921-130">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="e7921-131">[in] Указатель для контекстной информации, чтобы передать функции **DISMISSMODELESS,** указываемую _параметром lpfnDismiss._</span><span class="sxs-lookup"><span data-stu-id="e7921-131">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="e7921-132">Этот параметр применяется только к бесключевой версии диалогового окна, включив **флаг** DIALOG_SDI в _параметр ulFlags._</span><span class="sxs-lookup"><span data-stu-id="e7921-132">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="e7921-133">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e7921-133">_cbEntryID_</span></span>
  
> <span data-ttu-id="e7921-134">[in] Byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span><span class="sxs-lookup"><span data-stu-id="e7921-134">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e7921-135">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="e7921-135">_lpEntryID_</span></span>
  
> <span data-ttu-id="e7921-136">[in] Указатель на идентификатор записи, который представляет открытую запись адресной книги.</span><span class="sxs-lookup"><span data-stu-id="e7921-136">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="e7921-137">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="e7921-137">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="e7921-138">[in] Указатель на функцию на основе прототипа **функции LPFNBUTTON.**</span><span class="sxs-lookup"><span data-stu-id="e7921-138">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="e7921-139">Функция **LPFNBUTTON добавляет** кнопку в диалоговое окно подробностей.</span><span class="sxs-lookup"><span data-stu-id="e7921-139">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="e7921-140">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="e7921-140">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="e7921-141">[in] Указатель на данные, которые использовались в качестве параметра для функции, указанной _параметром lpfButtonCallback._</span><span class="sxs-lookup"><span data-stu-id="e7921-141">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="e7921-142">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="e7921-142">_lpszButtonText_</span></span>
  
> <span data-ttu-id="e7921-143">[in] Указатель на строку, содержавшую текст, который необходимо применить к добавленной кнопке, если эта кнопка является размежещенной.</span><span class="sxs-lookup"><span data-stu-id="e7921-143">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="e7921-144">Параметр  _lpszButtonText должен_ быть NULL, если не требуется размягкаемая кнопка.</span><span class="sxs-lookup"><span data-stu-id="e7921-144">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="e7921-145">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e7921-145">_ulFlags_</span></span>
  
> <span data-ttu-id="e7921-146">[in] Немного флагов, которые контролируют тип текста для _параметра lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="e7921-146">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="e7921-147">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="e7921-147">The following flags can be set:</span></span> 
    
<span data-ttu-id="e7921-148">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="e7921-148">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="e7921-149">Указывает, что Details возвращает TRUE, если на самом деле в адрес внесены изменения; в противном случае Details возвращает FALSE.</span><span class="sxs-lookup"><span data-stu-id="e7921-149">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="e7921-150">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="e7921-150">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="e7921-151">Отображает модную версию диалогового окна общего адреса.</span><span class="sxs-lookup"><span data-stu-id="e7921-151">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="e7921-152">Этот флаг является взаимоисключающими с DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="e7921-152">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="e7921-153">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="e7921-153">DIALOG_SDI</span></span>
  
> <span data-ttu-id="e7921-154">Отображает бес режимную версию диалогового окна общего адреса.</span><span class="sxs-lookup"><span data-stu-id="e7921-154">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="e7921-155">Этот флаг является взаимоисключающими с DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="e7921-155">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="e7921-156">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e7921-156">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="e7921-157">Переданные строки находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="e7921-157">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="e7921-158">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="e7921-158">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

