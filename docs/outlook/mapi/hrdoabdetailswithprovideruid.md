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
ms.openlocfilehash: fada57c45602f0a0b07276034101fa23a7525f5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808662"
---
# <a name="hrdoabdetailswithprovideruid"></a><span data-ttu-id="f7813-103">HrDoABDetailsWithProviderUID</span><span class="sxs-lookup"><span data-stu-id="f7813-103">HrDoABDetailsWithProviderUID</span></span>

  
  
<span data-ttu-id="f7813-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f7813-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f7813-105">Гарантирует, что метод **OpenEntry** открывается с ожидаемый Exchange доступа к адресной книге.</span><span class="sxs-lookup"><span data-stu-id="f7813-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="f7813-106">Эта функция работает так же, [IAddrBook::Details](iaddrbook-details.md) , но открывается с помощью адресная книга Exchange, определяемую средством _pEmsabpUID_ **entryID** .</span><span class="sxs-lookup"><span data-stu-id="f7813-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md) but opens **entryID** using the Exchange address book identified by  _pEmsabpUID_.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f7813-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f7813-107">Header file:</span></span>  <br/> |<span data-ttu-id="f7813-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="f7813-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="f7813-109">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="f7813-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="f7813-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="f7813-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="f7813-111">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="f7813-111">Called by:</span></span>  <br/> |<span data-ttu-id="f7813-112">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="f7813-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="f7813-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7813-113">Parameters</span></span>

 <span data-ttu-id="f7813-114">_pEmsabpUID_</span><span class="sxs-lookup"><span data-stu-id="f7813-114">_pEmsabpUID_</span></span>
  
> <span data-ttu-id="f7813-115">[in] Указатель на _emsabpUID_ , который определяет поставщик адресной книги Exchange этой функции следует использовать для отображения сведений на идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="f7813-115">[in] A pointer to an  _emsabpUID_ that identifies the Exchange address book provider this function should use to display details on the entry identifier.</span></span> <span data-ttu-id="f7813-116">Если входящий идентификатор записи не идентификатор записи адресной книги Exchange поставщика, этот параметр игнорируется и действует вызова функции аналогично [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="f7813-116">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function call acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span> <span data-ttu-id="f7813-117">Если этот параметр имеет значение NULL или ноль MAPIUID, эта функция также работает так же, как [IAddrBook::Details](iaddrbook-details.md).</span><span class="sxs-lookup"><span data-stu-id="f7813-117">If this parameter is NULL or a zero MAPIUID, this function also acts exactly like [IAddrBook::Details](iaddrbook-details.md).</span></span>
    
 <span data-ttu-id="f7813-118">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="f7813-118">_pAddrBook_</span></span>
  
> <span data-ttu-id="f7813-119">[in] В адресной книге используется для открытия идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="f7813-119">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="f7813-120">Он не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="f7813-120">It cannot be NULL.</span></span>
    
 <span data-ttu-id="f7813-121">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f7813-121">_lpulUIParam_</span></span>
  
> <span data-ttu-id="f7813-122">[out] Дескриптор родительского окна для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="f7813-122">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="f7813-123">_lpfnDismiss_</span><span class="sxs-lookup"><span data-stu-id="f7813-123">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="f7813-124">[in] Указатель на функцию, на основе **DISMISSMODELESS** прототип, или значение NULL.</span><span class="sxs-lookup"><span data-stu-id="f7813-124">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="f7813-125">Этот член применим только к безрежимным версии диалоговом окне, указанной флагом DIALOG_SDI задаваемая.</span><span class="sxs-lookup"><span data-stu-id="f7813-125">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="f7813-126">MAPI вызывает **DISMISSMODELESS** функцию, если пользователь не закрывает диалоговом окне безрежимным адреса клиента, который вызывает диалоговое окно не является активной подробные сведения о том.</span><span class="sxs-lookup"><span data-stu-id="f7813-126">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="f7813-127">_lpvDismissContext_</span><span class="sxs-lookup"><span data-stu-id="f7813-127">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="f7813-128">[in] Указатель на сведения о контексте для передачи **DISMISSMODELESS** функции, с помощью параметра _lpfnDismiss_ .</span><span class="sxs-lookup"><span data-stu-id="f7813-128">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="f7813-129">Этот параметр применяется только к безрежимным версии диалогового окна, включая флаг **DIALOG_SDI** с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="f7813-129">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="f7813-130">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f7813-130">_cbEntryID_</span></span>
  
> <span data-ttu-id="f7813-131">[in] Количество байтов идентификатор записи, указанные с помощью параметра _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="f7813-131">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f7813-132">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="f7813-132">_lpEntryID_</span></span>
  
> <span data-ttu-id="f7813-133">[in] Указатель на идентификатор записи, который представляет записи адресной книги, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="f7813-133">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="f7813-134">_lpfButtonCallback_</span><span class="sxs-lookup"><span data-stu-id="f7813-134">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="f7813-135">[in] Указатель на функцию на основании прототипа функции **LPFNBUTTON** .</span><span class="sxs-lookup"><span data-stu-id="f7813-135">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="f7813-136">В функции **LPFNBUTTON** добавляется кнопка в диалоговом окне "Подробности".</span><span class="sxs-lookup"><span data-stu-id="f7813-136">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="f7813-137">_lpvButtonContext_</span><span class="sxs-lookup"><span data-stu-id="f7813-137">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="f7813-138">[in] Указатель на данные, используемый в качестве параметра для функции, указанного с помощью параметра _lpfButtonCallback_ .</span><span class="sxs-lookup"><span data-stu-id="f7813-138">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="f7813-139">_lpszButtonText_</span><span class="sxs-lookup"><span data-stu-id="f7813-139">_lpszButtonText_</span></span>
  
> <span data-ttu-id="f7813-140">[in] Указатель на строку, которая содержит текст, который применяется для кнопки добавлены, если эта кнопка является расширяемым.</span><span class="sxs-lookup"><span data-stu-id="f7813-140">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="f7813-141">Значение параметра _lpszButtonText_ должно быть значение NULL, когда расширяемая кнопка не требуется.</span><span class="sxs-lookup"><span data-stu-id="f7813-141">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="f7813-142">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f7813-142">_ulFlags_</span></span>
  
> <span data-ttu-id="f7813-143">[in] Битовая маска флаги, определяющее тип текста для параметра _lpszButtonText_ .</span><span class="sxs-lookup"><span data-stu-id="f7813-143">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="f7813-144">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="f7813-144">The following flags can be set:</span></span> 
    
<span data-ttu-id="f7813-145">AB_TELL_DETAILS_CHANGE</span><span class="sxs-lookup"><span data-stu-id="f7813-145">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="f7813-146">Указывает, что сведения о возвращает TRUE, если фактически изменений на адрес; в противном случае сведения о возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="f7813-146">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="f7813-147">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="f7813-147">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="f7813-148">Отображает модальное версию стандартным диалоговым окном адрес.</span><span class="sxs-lookup"><span data-stu-id="f7813-148">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="f7813-149">Этот флаг является взаимоисключающим с DIALOG_SDI.</span><span class="sxs-lookup"><span data-stu-id="f7813-149">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="f7813-150">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="f7813-150">DIALOG_SDI</span></span>
  
> <span data-ttu-id="f7813-151">Отображает безрежимным версию стандартным диалоговым окном адрес.</span><span class="sxs-lookup"><span data-stu-id="f7813-151">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="f7813-152">Этот флаг является взаимоисключающим с DIALOG_MODAL.</span><span class="sxs-lookup"><span data-stu-id="f7813-152">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="f7813-153">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f7813-153">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="f7813-154">Строки переданное хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="f7813-154">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="f7813-155">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="f7813-155">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

