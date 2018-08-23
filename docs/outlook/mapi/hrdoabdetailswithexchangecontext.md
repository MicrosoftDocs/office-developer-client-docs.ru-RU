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
ms.openlocfilehash: d882fa1e705969ae06da46710fc7216625ca932e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566378"
---
# <a name="hrdoabdetailswithexchangecontext"></a><span data-ttu-id="22c8e-103">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="22c8e-103">HrDoABDetailsWithExchangeContext</span></span>

  
  
<span data-ttu-id="22c8e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22c8e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22c8e-105">Гарантирует, что метод **OpenEntry** открывается с ожидаемый Exchange доступа к адресной книге.</span><span class="sxs-lookup"><span data-stu-id="22c8e-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="22c8e-106">Эта функция работает так же, [IAddrBook::Details](iaddrbook-details.md), но открывает **entryID** , с помощью адресная книга Exchange, определенного параметром _pEmsmdbUID_ .</span><span class="sxs-lookup"><span data-stu-id="22c8e-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md), but opens the **entryID** using the Exchange address book identified by the  _pEmsmdbUID_ parameter.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="22c8e-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="22c8e-107">Header file:</span></span>  <br/> |<span data-ttu-id="22c8e-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="22c8e-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="22c8e-109">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="22c8e-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="22c8e-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="22c8e-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="22c8e-111">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="22c8e-111">Called by:</span></span>  <br/> |<span data-ttu-id="22c8e-112">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="22c8e-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="22c8e-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="22c8e-113">Parameters</span></span>

 <span data-ttu-id="22c8e-114">_pmsess_</span><span class="sxs-lookup"><span data-stu-id="22c8e-114">_pmsess_</span></span>
  
> <span data-ttu-id="22c8e-115">Система на **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="22c8e-115">The logged on **IMAPISession**.</span></span> <span data-ttu-id="22c8e-116">Он не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="22c8e-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="22c8e-117">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="22c8e-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="22c8e-118">Указатель на **emsmdbUID** , который определяет службу Exchange, которая содержит поставщик адресной книги Exchange, которая используется для открытия идентификатор записи с помощью функции.</span><span class="sxs-lookup"><span data-stu-id="22c8e-118">A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange address book provider that is used by the function to open the entry identifier.</span></span> <span data-ttu-id="22c8e-119">Если входящий идентификатор записи не идентификатор записи адресной книги Exchange поставщика, этот параметр игнорируется и функцию действует как [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="22c8e-119">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function behaves like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="22c8e-120">Если этот параметр имеет значение NULL или ноль **MAPIUID**, эта функция также работает так же, как [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="22c8e-120">If this parameter is NULL or a zero **MAPIUID**, this function also acts exactly like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> 
    
 <span data-ttu-id="22c8e-121">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="22c8e-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="22c8e-122">[in] В адресной книге используется для открытия идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="22c8e-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="22c8e-123">Он не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="22c8e-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="22c8e-124">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="22c8e-124">_lpulUIParam_</span></span>
  
> <span data-ttu-id="22c8e-125">[out] Дескриптор родительского окна для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="22c8e-125">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="22c8e-126">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="22c8e-126">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="22c8e-127">[in] Указатель на функцию, на основе **DISMISSMODELESS** прототип, или значение NULL.</span><span class="sxs-lookup"><span data-stu-id="22c8e-127">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="22c8e-128">Этот член применим только к безрежимным версии диалоговом окне, указанной флагом DIALOG_SDI задаваемая.</span><span class="sxs-lookup"><span data-stu-id="22c8e-128">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="22c8e-129">MAPI вызывает **DISMISSMODELESS** функцию, если пользователь не закрывает диалоговом окне безрежимным адреса клиента, который вызывает диалоговое окно не является активной подробные сведения о том.</span><span class="sxs-lookup"><span data-stu-id="22c8e-129">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="22c8e-130">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="22c8e-130">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="22c8e-131">[in] Указатель на сведения о контексте для передачи **DISMISSMODELESS** функции, с помощью параметра _lpfnDismiss_ .</span><span class="sxs-lookup"><span data-stu-id="22c8e-131">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="22c8e-132">Этот параметр применяется только к безрежимным версии диалогового окна, включая флаг **DIALOG_SDI** с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="22c8e-132">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="22c8e-133">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="22c8e-133">_cbEntryID_</span></span>
  
> <span data-ttu-id="22c8e-134">[in] Количество байтов идентификатор записи, указанные с помощью параметра _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="22c8e-134">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="22c8e-135">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="22c8e-135">_lpEntryID_</span></span>
  
> <span data-ttu-id="22c8e-136">[in] Указатель на идентификатор записи, который представляет записи адресной книги, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="22c8e-136">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="22c8e-137">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="22c8e-137">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="22c8e-138">[in] Указатель на функцию на основании прототипа функции **LPFNBUTTON** .</span><span class="sxs-lookup"><span data-stu-id="22c8e-138">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="22c8e-139">В функции **LPFNBUTTON** добавляется кнопка в диалоговом окне "Подробности".</span><span class="sxs-lookup"><span data-stu-id="22c8e-139">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="22c8e-140">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="22c8e-140">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="22c8e-141">[in] Указатель на данные, используемый в качестве параметра для функции, указанного с помощью параметра _lpfButtonCallback_ .</span><span class="sxs-lookup"><span data-stu-id="22c8e-141">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="22c8e-142">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="22c8e-142">_lpszButtonText_</span></span>
  
> <span data-ttu-id="22c8e-143">[in] Указатель на строку, которая содержит текст, который применяется для кнопки добавлены, если эта кнопка является расширяемым.</span><span class="sxs-lookup"><span data-stu-id="22c8e-143">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="22c8e-144">Значение параметра _lpszButtonText_ должно быть значение NULL, когда расширяемая кнопка не требуется.</span><span class="sxs-lookup"><span data-stu-id="22c8e-144">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="22c8e-145">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="22c8e-145">_ulFlags_</span></span>
  
> <span data-ttu-id="22c8e-146">[in] Битовая маска флаги, определяющее тип текста для параметра _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="22c8e-146">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="22c8e-147">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="22c8e-147">The following flags can be set:</span></span> 
    
<span data-ttu-id="22c8e-148">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="22c8e-148">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="22c8e-149">Указывает, что сведения о возвращает TRUE, если фактически изменений на адрес; в противном случае сведения о возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="22c8e-149">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="22c8e-150">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="22c8e-150">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="22c8e-151">Отображает модальное версию стандартным диалоговым окном адрес.</span><span class="sxs-lookup"><span data-stu-id="22c8e-151">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="22c8e-152">Этот флаг является взаимоисключающим с DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="22c8e-152">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="22c8e-153">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="22c8e-153">DIALOG_SDI</span></span>
  
> <span data-ttu-id="22c8e-154">Отображает безрежимным версию стандартным диалоговым окном адрес.</span><span class="sxs-lookup"><span data-stu-id="22c8e-154">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="22c8e-155">Этот флаг является взаимоисключающим с DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="22c8e-155">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="22c8e-156">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="22c8e-156">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="22c8e-157">Строки переданное хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="22c8e-157">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="22c8e-158">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="22c8e-158">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

