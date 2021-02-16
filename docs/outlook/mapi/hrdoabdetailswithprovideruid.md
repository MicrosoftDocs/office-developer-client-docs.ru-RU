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
# <a name="hrdoabdetailswithprovideruid"></a><span data-ttu-id="27b01-103">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="27b01-103">HrDoABDetailsWithProviderUID</span></span>

  
  
<span data-ttu-id="27b01-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27b01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27b01-105">Обеспечивает открытие метода **OpenEntry** ожидаемым поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="27b01-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="27b01-106">Эта функция работает аналогично [IAddrBook::D etails,](iaddrbook-details.md) но открывает **entryID** с помощью адресной книги Exchange, определенной _pEmsabpUID._</span><span class="sxs-lookup"><span data-stu-id="27b01-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) but opens **entryID** using the Exchange address book identified by  _pEmsabpUID_.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="27b01-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="27b01-107">Header file:</span></span>  <br/> |<span data-ttu-id="27b01-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="27b01-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="27b01-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="27b01-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="27b01-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="27b01-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="27b01-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="27b01-111">Called by:</span></span>  <br/> |<span data-ttu-id="27b01-112">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="27b01-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="27b01-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="27b01-113">Parameters</span></span>

 <span data-ttu-id="27b01-114">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="27b01-114">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="27b01-115">[in] Указатель на  _emsabpUID,_ идентифицирует поставщика адресной книги Exchange, который эта функция должна использовать для отображения сведений об идентификаторе записи.</span><span class="sxs-lookup"><span data-stu-id="27b01-115">[in] A pointer to an  _emsabpUID_ that identifies the Exchange address book provider this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="27b01-116">Если идентификатор входной записи не является идентификатором записи поставщика адресной книги Exchange, этот параметр игнорируется, и вызов функции действует точно так же, как [IAddrBook::D etails](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="27b01-116">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="27b01-117">Если этот параметр имеет значение NULL или mapIUID нулевого уровня, эта функция также действует точно так же, как [IAddrBook::D etails.](iaddrbook-details.md)</span><span class="sxs-lookup"><span data-stu-id="27b01-117">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="27b01-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="27b01-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="27b01-119">[in] Адресная книга, используемая для открытия идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="27b01-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="27b01-120">Это не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="27b01-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="27b01-121">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="27b01-121">_lpulUIParam_</span></span>
  
> <span data-ttu-id="27b01-122">[out] Handle to the parent window for the dialog box.</span><span class="sxs-lookup"><span data-stu-id="27b01-122">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="27b01-123">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="27b01-123">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="27b01-124">[in] Указатель на функцию на основе **прототипа DISMISSMODELESS** или NULL.</span><span class="sxs-lookup"><span data-stu-id="27b01-124">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="27b01-125">Этот член применяется только к неавтомантной версии диалогового окна, как указано DIALOG_SDI флага.</span><span class="sxs-lookup"><span data-stu-id="27b01-125">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="27b01-126">MAPI вызывает функцию **DISMISSMODELESS,** когда пользователь отклонять диалоговое окно без режима адресов, сообщая клиенту, который вызывает details, о том, что диалоговое окно больше не активно.</span><span class="sxs-lookup"><span data-stu-id="27b01-126">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="27b01-127">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="27b01-127">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="27b01-128">[in] Указатель на контекстную информацию, которая передается функции **DISMISSMODELESS,** на которую указывает параметр _lpfnDismiss._</span><span class="sxs-lookup"><span data-stu-id="27b01-128">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="27b01-129">Этот параметр применяется только к неавтомантной версии  диалоговых окно, включив флаг DIALOG_SDI в параметр _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="27b01-129">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="27b01-130">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="27b01-130">_cbEntryID_</span></span>
  
> <span data-ttu-id="27b01-131">[in] Количество ветвей идентификатора записи, заданного параметром _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="27b01-131">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="27b01-132">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="27b01-132">_lpEntryID_</span></span>
  
> <span data-ttu-id="27b01-133">[in] Указатель на идентификатор записи, который представляет открываемую запись адресной книги.</span><span class="sxs-lookup"><span data-stu-id="27b01-133">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="27b01-134">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="27b01-134">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="27b01-135">[in] Указатель на функцию на основе прототипа **функции LPFNBUTTON.**</span><span class="sxs-lookup"><span data-stu-id="27b01-135">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="27b01-136">Функция **LPFNBUTTON** добавляет кнопку в диалоговое окно сведений.</span><span class="sxs-lookup"><span data-stu-id="27b01-136">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="27b01-137">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="27b01-137">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="27b01-138">[in] Указатель на данные, которые использовались в качестве параметра для функции, указанной параметром _lpfButtonCallback._</span><span class="sxs-lookup"><span data-stu-id="27b01-138">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="27b01-139">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="27b01-139">_lpszButtonText_</span></span>
  
> <span data-ttu-id="27b01-140">[in] Указатель на строку, содержаную текст, который необходимо применить к добавленной кнопке, если эта кнопка является выдержатой.</span><span class="sxs-lookup"><span data-stu-id="27b01-140">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="27b01-141">Параметр  _lpszButtonText должен_ иметь NULL, если не требуется размягкаемая кнопка.</span><span class="sxs-lookup"><span data-stu-id="27b01-141">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="27b01-142">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="27b01-142">_ulFlags_</span></span>
  
> <span data-ttu-id="27b01-143">[in] Битоваяmas флагов, которая управляет типом текста для параметра _lpszButtonText._</span><span class="sxs-lookup"><span data-stu-id="27b01-143">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="27b01-144">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="27b01-144">The following flags can be set:</span></span> 
    
<span data-ttu-id="27b01-145">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="27b01-145">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="27b01-146">Указывает, что details возвращает true, если фактически в адрес были внесены изменения; в противном случае details возвращает false.</span><span class="sxs-lookup"><span data-stu-id="27b01-146">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="27b01-147">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="27b01-147">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="27b01-148">Отображает модальные версии общего диалоговых окна адресов.</span><span class="sxs-lookup"><span data-stu-id="27b01-148">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="27b01-149">Этот флаг является взаимоисключающими с DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="27b01-149">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="27b01-150">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="27b01-150">DIALOG_SDI</span></span>
  
> <span data-ttu-id="27b01-151">Отображает неавтомтную версию общего диалоговых окна адресов.</span><span class="sxs-lookup"><span data-stu-id="27b01-151">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="27b01-152">Этот флаг является взаимоисключающими с DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="27b01-152">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="27b01-153">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="27b01-153">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="27b01-154">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="27b01-154">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="27b01-155">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="27b01-155">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

