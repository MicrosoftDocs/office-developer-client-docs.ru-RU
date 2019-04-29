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
# <a name="hrdoabdetailswithexchangecontext"></a><span data-ttu-id="d2953-103">HrDoABDetailsWithExchangeContext</span><span class="sxs-lookup"><span data-stu-id="d2953-103">HrDoABDetailsWithExchangeContext</span></span>

  
  
<span data-ttu-id="d2953-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2953-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2953-105">Гарантирует, что метод **OpenEntry** открыт ожидаемым поставщиком адресных книг Exchange.</span><span class="sxs-lookup"><span data-stu-id="d2953-105">Ensures that the **OpenEntry** method is opened by the expected Exchange address book provider.</span></span> <span data-ttu-id="d2953-106">Эта функция работает аналогично [IAddrBook::D етаилс](iaddrbook-details.md), но открывает **entryID** с помощью адресной книги Exchange, определенной параметром _пемсмдбуид_ .</span><span class="sxs-lookup"><span data-stu-id="d2953-106">This function works similarly to [IAddrBook::Details](iaddrbook-details.md), but opens the **entryID** using the Exchange address book identified by the  _pEmsmdbUID_ parameter.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d2953-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d2953-107">Header file:</span></span>  <br/> |<span data-ttu-id="d2953-108">абхелп. h</span><span class="sxs-lookup"><span data-stu-id="d2953-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="d2953-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="d2953-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="d2953-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="d2953-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="d2953-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="d2953-111">Called by:</span></span>  <br/> |<span data-ttu-id="d2953-112">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="d2953-112">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="d2953-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2953-113">Parameters</span></span>

 <span data-ttu-id="d2953-114">_пмсесс_</span><span class="sxs-lookup"><span data-stu-id="d2953-114">_pmsess_</span></span>
  
> <span data-ttu-id="d2953-115">Вошедший в систему **IMAPISession**.</span><span class="sxs-lookup"><span data-stu-id="d2953-115">The logged on **IMAPISession**.</span></span> <span data-ttu-id="d2953-116">Он не может иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="d2953-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="d2953-117">_Пемсмдбуид_</span><span class="sxs-lookup"><span data-stu-id="d2953-117">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="d2953-118">Указатель на **емсмдбуид** , определяющий службу Exchange, которая содержит поставщика адресных книг Exchange, который используется функцией для открытия идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="d2953-118">A pointer to an **emsmdbUID** that identifies the Exchange Service that contains the Exchange address book provider that is used by the function to open the entry identifier.</span></span> <span data-ttu-id="d2953-119">Если входящий идентификатор записи не является идентификатором записи поставщика адресных книг Exchange, этот параметр игнорируется, а функция работает так же, как [IAddrBook:: OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="d2953-119">If the incoming entry identifier is not an Exchange address book provider entry identifier, this parameter is ignored and the function behaves like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="d2953-120">Если этот параметр имеет значение NULL или нулевой **мапиуид**, эта функция также действует точно так же, как [IAddrBook:: OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="d2953-120">If this parameter is NULL or a zero **MAPIUID**, this function also acts exactly like [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> 
    
 <span data-ttu-id="d2953-121">_Паддрбук_</span><span class="sxs-lookup"><span data-stu-id="d2953-121">_pAddrBook_</span></span>
  
> <span data-ttu-id="d2953-122">возврата Адресная книга, используемая для открытия идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="d2953-122">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="d2953-123">Он не может иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="d2953-123">It cannot be NULL.</span></span>
    
 <span data-ttu-id="d2953-124">_Лпулуипарам_</span><span class="sxs-lookup"><span data-stu-id="d2953-124">_lpulUIParam_</span></span>
  
> <span data-ttu-id="d2953-125">вышли Дескриптор родительского окна для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="d2953-125">[out] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="d2953-126">_Лпфндисмисс_</span><span class="sxs-lookup"><span data-stu-id="d2953-126">_lpfnDismiss_</span></span>
  
> <span data-ttu-id="d2953-127">возврата Указатель на функцию, основанную на прототипе **дисмиссмоделесс** , или значение null.</span><span class="sxs-lookup"><span data-stu-id="d2953-127">[in] A pointer to a function based on the **DISMISSMODELESS** prototype, or NULL.</span></span> <span data-ttu-id="d2953-128">Этот элемент применяется только к немодальной версии диалогового окна, как указано в установленном флаге ДИАЛОГ_СДИ.</span><span class="sxs-lookup"><span data-stu-id="d2953-128">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="d2953-129">MAPI вызывает функцию **дисмиссмоделесс** , когда пользователь закрывает диалоговое окно с немодальным адресом, что информирует клиента о вызове сведений о том, что диалоговое окно больше не активно.</span><span class="sxs-lookup"><span data-stu-id="d2953-129">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client that is calling Details that the dialog box is no longer active.</span></span> 
    
 <span data-ttu-id="d2953-130">_Лпвдисмиссконтекст_</span><span class="sxs-lookup"><span data-stu-id="d2953-130">_lpvDismissContext_</span></span>
  
> <span data-ttu-id="d2953-131">возврата Указатель на сведения о контексте, передаваемый функции **дисмиссмоделесс** , на которую указывает параметр _лпфндисмисс_ .</span><span class="sxs-lookup"><span data-stu-id="d2953-131">[in] A pointer to context information to pass to the **DISMISSMODELESS** function pointed to by the  _lpfnDismiss_ parameter.</span></span> <span data-ttu-id="d2953-132">Этот параметр применяется только к немодальным версиям диалогового окна, включая флаг **диалог_сди** в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="d2953-132">This parameter applies only to the modeless version of the dialog box by including the **DIALOG_SDI** flag in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="d2953-133">_Кбентрид_</span><span class="sxs-lookup"><span data-stu-id="d2953-133">_cbEntryID_</span></span>
  
> <span data-ttu-id="d2953-134">возврата Количество байт в идентификаторе записи, заданном параметром _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="d2953-134">[in] The byte count of the entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="d2953-135">_Лпентрид_</span><span class="sxs-lookup"><span data-stu-id="d2953-135">_lpEntryID_</span></span>
  
> <span data-ttu-id="d2953-136">возврата Указатель на идентификатор записи, представляющий запись адресной книги, которую требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="d2953-136">[in] A pointer to the entry identifier that represents the address book entry to open.</span></span>
    
 <span data-ttu-id="d2953-137">_Лпфбуттонкаллбакк_</span><span class="sxs-lookup"><span data-stu-id="d2953-137">_lpfButtonCallback_</span></span>
  
> <span data-ttu-id="d2953-138">возврата Указатель на функцию на основе прототипа функции **лпфнбуттон** .</span><span class="sxs-lookup"><span data-stu-id="d2953-138">[in] A pointer to a function based on the **LPFNBUTTON** function prototype.</span></span> <span data-ttu-id="d2953-139">Функция **лпфнбуттон** добавляет кнопку в диалоговое окно "сведения".</span><span class="sxs-lookup"><span data-stu-id="d2953-139">An **LPFNBUTTON** function adds a button to the details dialog box.</span></span> 
    
 <span data-ttu-id="d2953-140">_Лпвбуттонконтекст_</span><span class="sxs-lookup"><span data-stu-id="d2953-140">_lpvButtonContext_</span></span>
  
> <span data-ttu-id="d2953-141">возврата Указатель на данные, которые использовались в качестве параметра для функции, заданной параметром _лпфбуттонкаллбакк_ .</span><span class="sxs-lookup"><span data-stu-id="d2953-141">[in] A pointer to data that was used as a parameter for the function specified by the  _lpfButtonCallback_ parameter.</span></span> 
    
 <span data-ttu-id="d2953-142">_Лпсзбуттонтекст_</span><span class="sxs-lookup"><span data-stu-id="d2953-142">_lpszButtonText_</span></span>
  
> <span data-ttu-id="d2953-143">возврата Указатель на строку, которая содержит текст, который будет применен к добавленной кнопке, если эта кнопка является расширяемой.</span><span class="sxs-lookup"><span data-stu-id="d2953-143">[in] A pointer to a string that contains text to be applied to the added button, if that button is extensible.</span></span> <span data-ttu-id="d2953-144">Если расширяемая кнопка не требуется, параметр _лпсзбуттонтекст_ должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="d2953-144">The  _lpszButtonText_ parameter should be NULL when an extensible button is not needed.</span></span> 
    
 <span data-ttu-id="d2953-145">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d2953-145">_ulFlags_</span></span>
  
> <span data-ttu-id="d2953-146">возврата Битовая маска флагов, определяющая тип текста для параметра _лпсзбуттонтекст_ .</span><span class="sxs-lookup"><span data-stu-id="d2953-146">[in] A bitmask of flags that controls the type of the text for the  _lpszButtonText_ parameter.</span></span> <span data-ttu-id="d2953-147">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="d2953-147">The following flags can be set:</span></span> 
    
<span data-ttu-id="d2953-148">АБ_ТЕЛЛ_ДЕТАИЛС_ЧАНЖЕ</span><span class="sxs-lookup"><span data-stu-id="d2953-148">AB_TELL_DETAILS_CHANGE</span></span>
  
> <span data-ttu-id="d2953-149">Указывает, что Details возвращает TRUE, если изменения фактически вносятся в адрес; в противном случае сведения возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="d2953-149">Indicates that Details returns TRUE if changes are actually made to the address; otherwise, Details returns FALSE.</span></span>
    
<span data-ttu-id="d2953-150">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="d2953-150">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="d2953-151">Отображает модальную версию диалогового окна Общий адрес.</span><span class="sxs-lookup"><span data-stu-id="d2953-151">Displays the modal version of the common address dialog box.</span></span> <span data-ttu-id="d2953-152">Этот флаг является взаимно исключающим с ДИАЛОГ_СДИ.</span><span class="sxs-lookup"><span data-stu-id="d2953-152">This flag is mutually exclusive with DIALOG_SDI.</span></span>
    
<span data-ttu-id="d2953-153">ДИАЛОГ_СДИ</span><span class="sxs-lookup"><span data-stu-id="d2953-153">DIALOG_SDI</span></span>
  
> <span data-ttu-id="d2953-154">Отображает немодальную версию диалогового окна общего адреса.</span><span class="sxs-lookup"><span data-stu-id="d2953-154">Displays the modeless version of the common address dialog box.</span></span> <span data-ttu-id="d2953-155">Этот флаг является взаимно исключающим с ДИАЛОГ_МОДАЛ.</span><span class="sxs-lookup"><span data-stu-id="d2953-155">This flag is mutually exclusive with DIALOG_MODAL.</span></span>
    
<span data-ttu-id="d2953-156">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d2953-156">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="d2953-157">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="d2953-157">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="d2953-158">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="d2953-158">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    

