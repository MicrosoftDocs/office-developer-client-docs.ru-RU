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
# <a name="hrdoabdetailswithexchangecontext"></a><span data-ttu-id="0dbd0-103">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="0dbd0-103">HrDoABDetailsWithExchangeContext</span></span>

  
  
<span data-ttu-id="0dbd0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0dbd0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0dbd0-105">Обеспечивает открытие метода **OpenEntry** ожидаемым поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="0dbd0-106">Эта функция работает аналогично [IAddrBook::D etails,](iaddrbook-details.md)но открывает **entryID** с помощью адресной книги Exchange, определенной параметром _pEmsmdbUID._</span><span class="sxs-lookup"><span data-stu-id="0dbd0-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md), but opens the **entryID** using the Exchange address book identified by the  _pEmsmdbUID_ parameter.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0dbd0-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="0dbd0-107">Header file:</span></span>  <br/> |<span data-ttu-id="0dbd0-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="0dbd0-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="0dbd0-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="0dbd0-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="0dbd0-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="0dbd0-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="0dbd0-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="0dbd0-111">Called by:</span></span>  <br/> |<span data-ttu-id="0dbd0-112">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="0dbd0-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="0dbd0-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="0dbd0-113">Parameters</span></span>

 <span data-ttu-id="0dbd0-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="0dbd0-114">_pmsess_</span></span>
  
> <span data-ttu-id="0dbd0-115">Во время входа в **систему IMAPISession.**</span><span class="sxs-lookup"><span data-stu-id="0dbd0-115">The logged on **IMAPISession**.</span></span> <span data-ttu-id="0dbd0-116">Это не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="0dbd0-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="0dbd0-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="0dbd0-118">Указатель на **emsmdbUID,** который определяет службу Exchange, которая содержит поставщика адресной книги Exchange, который используется функцией для открытия идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-118">A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange address book provider that is used by the function to open the entry identifier.</span></span> <span data-ttu-id="0dbd0-119">Если идентификатор входной записи не является идентификатором записи поставщика адресной книги Exchange, этот параметр игнорируется, и функция ведет себя как [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="0dbd0-119">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function behaves like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="0dbd0-120">Если этот параметр имеет значение NULL или **mapIUID** нулевого уровня, эта функция также действует точно так же, как [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="0dbd0-120">If this parameter is NULL or a zero **MAPIUID**, this function also acts exactly like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> 
    
 <span data-ttu-id="0dbd0-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="0dbd0-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="0dbd0-122">[in] Адресная книга, используемая для открытия идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="0dbd0-123">Это не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="0dbd0-124">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0dbd0-124">_lpulUIParam_</span></span>
  
> <span data-ttu-id="0dbd0-125">[out] Handle to the parent window for the dialog box.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-125">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="0dbd0-126">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="0dbd0-126">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="0dbd0-127">[in] Указатель на функцию на основе **прототипа DISMISSMODELESS** или NULL.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-127">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="0dbd0-128">Этот член применяется только к неавтомантной версии диалогового окна, как указано DIALOG_SDI флагом.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-128">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="0dbd0-129">MAPI вызывает функцию **DISMISSMODELESS,** когда пользователь отклонять диалоговое окно без режима адресов, сообщая клиенту, который вызывает details, о том, что диалоговое окно больше не активно.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-129">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="0dbd0-130">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="0dbd0-130">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="0dbd0-131">[in] Указатель на контекстную информацию, которая передается функции **DISMISSMODELESS,** на которую указывает параметр _lpfnDismiss._</span><span class="sxs-lookup"><span data-stu-id="0dbd0-131">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="0dbd0-132">Этот параметр применяется только к безмежной версии диалоговых  окна, включив флаг DIALOG_SDI в параметр _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="0dbd0-132">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="0dbd0-133">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="0dbd0-133">_cbEntryID_</span></span>
  
> <span data-ttu-id="0dbd0-134">[in] Количество ветвей идентификатора записи, заданного параметром _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="0dbd0-134">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="0dbd0-135">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="0dbd0-135">_lpEntryID_</span></span>
  
> <span data-ttu-id="0dbd0-136">[in] Указатель на идентификатор записи, который представляет открываемую запись адресной книги.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-136">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="0dbd0-137">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="0dbd0-137">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="0dbd0-138">[in] Указатель на функцию на основе прототипа **функции LPFNBUTTON.**</span><span class="sxs-lookup"><span data-stu-id="0dbd0-138">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="0dbd0-139">Функция **LPFNBUTTON** добавляет кнопку в диалоговое окно сведений.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-139">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="0dbd0-140">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="0dbd0-140">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="0dbd0-141">[in] Указатель на данные, которые использовались в качестве параметра для функции, указанной параметром _lpfButtonCallback._</span><span class="sxs-lookup"><span data-stu-id="0dbd0-141">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="0dbd0-142">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="0dbd0-142">_lpszButtonText_</span></span>
  
> <span data-ttu-id="0dbd0-143">[in] Указатель на строку, содержаную текст, который необходимо применить к добавленной кнопке, если эта кнопка является выдержатой.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-143">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="0dbd0-144">Параметр  _lpszButtonText должен_ иметь NULL, если не требуется размягкаемая кнопка.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-144">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="0dbd0-145">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0dbd0-145">_ulFlags_</span></span>
  
> <span data-ttu-id="0dbd0-146">[in] Битоваяmas флагов, которая управляет типом текста для параметра _lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="0dbd0-146">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="0dbd0-147">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="0dbd0-147">The following flags can be set:</span></span> 
    
<span data-ttu-id="0dbd0-148">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="0dbd0-148">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="0dbd0-149">Указывает, что details возвращает true, если фактически в адрес были внесены изменения; в противном случае details возвращает false.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-149">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="0dbd0-150">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="0dbd0-150">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="0dbd0-151">Отображает модальной версии диалоговое окно общего адреса.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-151">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="0dbd0-152">Этот флаг является взаимоисключающими с DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-152">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="0dbd0-153">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="0dbd0-153">DIALOG_SDI</span></span>
  
> <span data-ttu-id="0dbd0-154">Отображает неавтомтную версию общего диалоговых окна адресов.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-154">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="0dbd0-155">Этот флаг является взаимоисключающими с DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-155">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="0dbd0-156">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0dbd0-156">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="0dbd0-157">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-157">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="0dbd0-158">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="0dbd0-158">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

