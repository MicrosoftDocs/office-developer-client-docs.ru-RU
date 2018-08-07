---
title: SERVICEWIZARDDLGPROC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SERVICEWIZARDDLGPROC
api_type:
- COM
ms.assetid: 3e2d5190-e67a-470d-8177-0f0ba20c7b82
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 649046aa48f293caa5bd71cc670481b5c205459a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812268"
---
# <a name="servicewizarddlgproc"></a><span data-ttu-id="01f69-103">SERVICEWIZARDDLGPROC</span><span class="sxs-lookup"><span data-stu-id="01f69-103">SERVICEWIZARDDLGPROC</span></span>
 
<span data-ttu-id="01f69-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="01f69-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="01f69-105">Определяет функцию обратного вызова вызывается мастером профилей, чтобы разрешить поставщика услуг реагировать на события пользователя при поставщика свойств или страниц выводимыми на экран.</span><span class="sxs-lookup"><span data-stu-id="01f69-105">Defines a callback function invoked by the Profile Wizard to allow a service provider to react to user events when the provider's property sheets or pages are being shown.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01f69-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="01f69-106">Header file:</span></span>  <br/> |<span data-ttu-id="01f69-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="01f69-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="01f69-108">Функция реализован:</span><span class="sxs-lookup"><span data-stu-id="01f69-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="01f69-109">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="01f69-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="01f69-110">Вызывается функция:</span><span class="sxs-lookup"><span data-stu-id="01f69-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="01f69-111">Мастер профилей MAPI</span><span class="sxs-lookup"><span data-stu-id="01f69-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
BOOL SERVICEWIZARDDLGPROC(
  HWND hDlg,
  UINT wMsgID,
  WPARAM wParam,
  LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="01f69-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="01f69-112">Parameters</span></span>

<span data-ttu-id="01f69-113">_hDlg_</span><span class="sxs-lookup"><span data-stu-id="01f69-113">_hDlg_</span></span>
  
> <span data-ttu-id="01f69-114">[in] Дескриптор окна в диалоговое окно мастера профилей.</span><span class="sxs-lookup"><span data-stu-id="01f69-114">[in] Window handle to the Profile Wizard dialog box.</span></span> 
    
<span data-ttu-id="01f69-115">_wMsgID_</span><span class="sxs-lookup"><span data-stu-id="01f69-115">_wMsgID_</span></span>
  
> <span data-ttu-id="01f69-116">[in] Окно сообщения для обработки.</span><span class="sxs-lookup"><span data-stu-id="01f69-116">[in] The window message to be processed.</span></span> <span data-ttu-id="01f69-117">В дополнение к регулярным окно сообщения, ожидаемый модального диалогового окна могут быть получены следующие сообщения:</span><span class="sxs-lookup"><span data-stu-id="01f69-117">In addition to the regular window messages expected by a modal dialog box, the following messages can be received:</span></span>
    
<span data-ttu-id="01f69-118">WM_CLOSE</span><span class="sxs-lookup"><span data-stu-id="01f69-118">WM_CLOSE</span></span> 
  
> <span data-ttu-id="01f69-119">Завершения работы мастера профилей.</span><span class="sxs-lookup"><span data-stu-id="01f69-119">The Profile Wizard has completed.</span></span> <span data-ttu-id="01f69-120">Поставщика услуг следует делать все необходимые очистки, такие как освобождение какие-либо динамически выделить память.</span><span class="sxs-lookup"><span data-stu-id="01f69-120">The service provider should do all required cleanup such as deallocating any dynamically allocated memory.</span></span> 
    
<span data-ttu-id="01f69-121">WM_COMMAND</span><span class="sxs-lookup"><span data-stu-id="01f69-121">WM_COMMAND</span></span> 
  
> <span data-ttu-id="01f69-122">Один из элементов управления поставщика был выбран или была нажата кнопка **Далее** или **Назад** .</span><span class="sxs-lookup"><span data-stu-id="01f69-122">One of the provider's controls has been selected, or the **Next** or **Back** button has been clicked.</span></span> <span data-ttu-id="01f69-123">Значение в параметре _wParam_ указывает, какой из этих событий пользователя произошло.</span><span class="sxs-lookup"><span data-stu-id="01f69-123">The value in the  _wParam_ parameter indicates which of these user events has occurred.</span></span> 
    
<span data-ttu-id="01f69-124">WM_INITDIALOG</span><span class="sxs-lookup"><span data-stu-id="01f69-124">WM_INITDIALOG</span></span> 
  
> <span data-ttu-id="01f69-125">Пользователь переходит на другую страницу свойства, для которого должен быть инициализирован диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="01f69-125">The user has moved to another property page, for which the dialog box must be initialized.</span></span> <span data-ttu-id="01f69-126">Поставщик должны инициализировать элементы управления, добавленные в диалоговое окно мастера профилей.</span><span class="sxs-lookup"><span data-stu-id="01f69-126">The provider should initialize the controls that the Profile Wizard has added to the dialog box.</span></span> 
    
<span data-ttu-id="01f69-127">WIZ_QUERYNUMPAGES</span><span class="sxs-lookup"><span data-stu-id="01f69-127">WIZ_QUERYNUMPAGES</span></span> 
  
> <span data-ttu-id="01f69-128">Мастер профиля запроса на число страниц, которые необходимо отобразить.</span><span class="sxs-lookup"><span data-stu-id="01f69-128">The Profile Wizard is prompting for the number of pages that the provider needs to display.</span></span> <span data-ttu-id="01f69-129">Поставщик должен возвращать число страниц, а не значение TRUE или FALSE.</span><span class="sxs-lookup"><span data-stu-id="01f69-129">The provider should return the number of pages instead of TRUE or FALSE.</span></span> <span data-ttu-id="01f69-130">Например используйте следующий оператор возврата для указания, что три страницы должны отображаться:</span><span class="sxs-lookup"><span data-stu-id="01f69-130">For example, use the following return statement to indicate that three pages should to be displayed:</span></span>
    
   ```cpp
return (BOOL)3;

   ```

<span data-ttu-id="01f69-131">_wParam_</span><span class="sxs-lookup"><span data-stu-id="01f69-131">_wParam_</span></span>
  
> <span data-ttu-id="01f69-132">[in] Параметр 32-разрядная версия, связанный с окном сообщения.</span><span class="sxs-lookup"><span data-stu-id="01f69-132">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="01f69-133">Возможные значения зависят от сообщения, указанный в параметре _wMsgID_ .</span><span class="sxs-lookup"><span data-stu-id="01f69-133">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> <span data-ttu-id="01f69-134">В дополнение к значениям, ожидаемый с регулярным окно сообщения для модального диалогового окна могут быть получены следующие значения:</span><span class="sxs-lookup"><span data-stu-id="01f69-134">In addition to the values expected with the regular window messages for a modal dialog box, the following values can be received:</span></span> 
    
<span data-ttu-id="01f69-135">WIZ_NEXT</span><span class="sxs-lookup"><span data-stu-id="01f69-135">WIZ_NEXT</span></span> 
  
> <span data-ttu-id="01f69-136">При _wMsgID_ содержит WM_COMMAND, пользователь нажатии кнопки **Далее** .</span><span class="sxs-lookup"><span data-stu-id="01f69-136">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Next** button.</span></span> 
    
<span data-ttu-id="01f69-137">WIZ_PREV</span><span class="sxs-lookup"><span data-stu-id="01f69-137">WIZ_PREV</span></span> 
  
> <span data-ttu-id="01f69-138">Если _wMsgID_ содержит WM_COMMAND, нажата кнопка **Назад** .</span><span class="sxs-lookup"><span data-stu-id="01f69-138">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Back** button.</span></span> 
    
<span data-ttu-id="01f69-139">_lParam_</span><span class="sxs-lookup"><span data-stu-id="01f69-139">_lParam_</span></span>
  
> <span data-ttu-id="01f69-140">[in] Параметр 32-разрядная версия, связанный с окном сообщения.</span><span class="sxs-lookup"><span data-stu-id="01f69-140">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="01f69-141">Возможные значения зависят от сообщения, указанный в параметре _wMsgID_ .</span><span class="sxs-lookup"><span data-stu-id="01f69-141">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="01f69-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2">Return value</span></span>

<span data-ttu-id="01f69-143">Значение, возвращаемое функцией **SERVICEWIZARDDLGPROC** на основе зависит от получено сообщение окна.</span><span class="sxs-lookup"><span data-stu-id="01f69-143">The value returned by a **SERVICEWIZARDDLGPROC** based function is dependent on the window message received.</span></span> <span data-ttu-id="01f69-144">В частности, обратите внимание, что исключительных возвращаемое значение для сообщения WIZ_QUERYNUMPAGES.</span><span class="sxs-lookup"><span data-stu-id="01f69-144">Note in particular the exceptional return value for the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="01f69-145">Обычный значения будут возвращены:</span><span class="sxs-lookup"><span data-stu-id="01f69-145">The normal return values are:</span></span> 
  
<span data-ttu-id="01f69-146">TRUE</span><span class="sxs-lookup"><span data-stu-id="01f69-146">TRUE</span></span> 
  
> <span data-ttu-id="01f69-147">Поставщик услуг обработал сообщение получено окна.</span><span class="sxs-lookup"><span data-stu-id="01f69-147">The service provider has processed the received window message.</span></span> 
    
<span data-ttu-id="01f69-148">FALSE</span><span class="sxs-lookup"><span data-stu-id="01f69-148">FALSE</span></span> 
  
> <span data-ttu-id="01f69-149">Поставщик услуг не обработал сообщение получено окна.</span><span class="sxs-lookup"><span data-stu-id="01f69-149">The service provider has not processed the received window message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="01f69-150">Замечания</span><span class="sxs-lookup"><span data-stu-id="01f69-150">Remarks</span></span>

<span data-ttu-id="01f69-151">Когда пользователь перемещается с одного свойства страницы, поставщик несет ответственность за скрытие элементов управления на странице старые и отображение элементов управления для страницы следующий или предыдущий.</span><span class="sxs-lookup"><span data-stu-id="01f69-151">When the user moves from one property page to another, the provider is responsible for hiding the old page's controls and showing the controls for the next or previous page.</span></span> <span data-ttu-id="01f69-152">При нажатии кнопки **Далее** функция **SERVICEWIZARDDLGPROC** на основе вызывается с сообщение WM_COMMAND и WIZ_NEXT в параметре _wParam_ .</span><span class="sxs-lookup"><span data-stu-id="01f69-152">When the user clicks the **Next** button, the **SERVICEWIZARDDLGPROC** based function is called with the WM_COMMAND message and WIZ_NEXT in the  _wParam_ parameter.</span></span> <span data-ttu-id="01f69-153">Далее описано, что происходит между нажатии кнопки **Далее** и время, когда отображаются страницы настройки первого поставщика.</span><span class="sxs-lookup"><span data-stu-id="01f69-153">The following steps describe what occurs between the time the user clicks **Next** and the time the first provider's configuration pages are rendered.</span></span> 
  
1. <span data-ttu-id="01f69-154">Мастер профиля скрывает все элементы управления, которые находятся на окна.</span><span class="sxs-lookup"><span data-stu-id="01f69-154">The Profile Wizard hides any controls that are on the window.</span></span> 
    
2. <span data-ttu-id="01f69-155">Мастер профиля добавляет поставщика скрытые элементы управления на страницу.</span><span class="sxs-lookup"><span data-stu-id="01f69-155">The Profile Wizard adds the provider's hidden controls to the page.</span></span> 
    
3. <span data-ttu-id="01f69-156">Мастер профиля вызывает **SERVICEWIZARDDLGPROC**, отправка сообщение WM_INITDIALOG, чтобы поставщик может инициализации элементов управления.</span><span class="sxs-lookup"><span data-stu-id="01f69-156">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_INITDIALOG message, so that the provider can initialize the controls.</span></span> 
    
4. <span data-ttu-id="01f69-157">Мастер профиля вызывает **SERVICEWIZARDDLGPROC**, отправив сообщение WIZ_QUERYNUMPAGES.</span><span class="sxs-lookup"><span data-stu-id="01f69-157">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="01f69-158">Поставщик возвращает число страниц, которые требуется отобразить.</span><span class="sxs-lookup"><span data-stu-id="01f69-158">The provider returns the number of pages that are to be shown.</span></span> 
    
5. <span data-ttu-id="01f69-159">Мастер профиля вызывает **SERVICEWIZARDDLGPROC**, отправив сообщение WM_COMMAND с параметром _wParam_ , задайте значение WIZ_NEXT или WIZ_PREV.</span><span class="sxs-lookup"><span data-stu-id="01f69-159">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV.</span></span> <span data-ttu-id="01f69-160">На этом этапе поставщик либо возвращает FALSE {ошибка} или выявляет ее элементов управления и возвращает значение TRUE {успеха}.</span><span class="sxs-lookup"><span data-stu-id="01f69-160">At this point, the provider either returns FALSE {error} or reveals its controls and returns TRUE {success}.</span></span> <span data-ttu-id="01f69-161">Если мастер профиля передает ID_NEXT, отображается первая страница поставщика.</span><span class="sxs-lookup"><span data-stu-id="01f69-161">If the Profile Wizard passes in ID_NEXT, the provider's first page is displayed.</span></span> <span data-ttu-id="01f69-162">Если ID_PREV передается, отображается последней странице.</span><span class="sxs-lookup"><span data-stu-id="01f69-162">If ID_PREV is passed in, the last page is displayed.</span></span> 
    
6. <span data-ttu-id="01f69-163">Мастер профиля вызывает функцию **SERVICEWIZARDDLGPROC** поставщика, отправив сообщение WM_COMMAND с параметром _wParam_ , задайте значение WIZ_NEXT или WIZ_PREV (в зависимости от того, какая кнопка нажата).</span><span class="sxs-lookup"><span data-stu-id="01f69-163">The Profile Wizard calls the provider's **SERVICEWIZARDDLGPROC** function, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV (depending on which button the user clicked).</span></span> <span data-ttu-id="01f69-164">Поставщик отвечает за отображение и скрытие элементов управления и записи данных в **IMAPIProp** передается мастер профиля для пошагового выполнения последовательности страниц.</span><span class="sxs-lookup"><span data-stu-id="01f69-164">The provider is responsible for showing or hiding its controls and writing its data to the **IMAPIProp** passed to the Profile Wizard to step through its sequence of pages.</span></span> <span data-ttu-id="01f69-165">Поставщик должен возвращать значение TRUE, если был успешно показано следующей или предыдущей странице, и значение FALSE, если ни Далее, ни предыдущей страницы может отображаться.</span><span class="sxs-lookup"><span data-stu-id="01f69-165">The provider should return TRUE if the next or previous page was successfully shown, and FALSE if neither the next nor previous page could be shown.</span></span> <span data-ttu-id="01f69-166">Поставщика необходимо принять во внимание при захода вне его последовательность страниц и отреагировать, скрытие элементов управления и записи данных в профиль.</span><span class="sxs-lookup"><span data-stu-id="01f69-166">The provider needs to be aware of when it is stepping outside of its sequence of pages, and respond appropriately by hiding its controls and writing its data to the profile.</span></span> 
    
7. <span data-ttu-id="01f69-167">Если пользователь действия вне диапазона поставщика страниц, мастер профиля Удаляет поставщика скрытые элементы управления из диалогового окна и вызывает следующий поставщик или отображает его следующей страницы, если последний поставщика, который был.</span><span class="sxs-lookup"><span data-stu-id="01f69-167">If the user steps outside the provider's range of pages, the Profile Wizard deletes the provider's hidden controls from the dialog box and calls the next provider or displays its next page if that was the last provider.</span></span> 
    

