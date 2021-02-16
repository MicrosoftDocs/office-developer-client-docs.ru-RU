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
ms.openlocfilehash: e43a1d7c57668ba930b4c4af7194bd298971e6ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432382"
---
# <a name="servicewizarddlgproc"></a><span data-ttu-id="17558-103">SERVICEWIZARDDLGPROC</span><span class="sxs-lookup"><span data-stu-id="17558-103">SERVICEWIZARDDLGPROC</span></span>
 
<span data-ttu-id="17558-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17558-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17558-105">Определяет функцию ответного вызова, вызываемую мастером профилей, чтобы поставщик службы реагировал на события пользователей при от показании таблиц или страниц свойств поставщика.</span><span class="sxs-lookup"><span data-stu-id="17558-105">Defines a callback function invoked by the Profile Wizard to allow a service provider to react to user events when the provider's property sheets or pages are being shown.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="17558-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="17558-106">Header file:</span></span>  <br/> |<span data-ttu-id="17558-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="17558-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="17558-108">Определяемая функция, реализованная в:</span><span class="sxs-lookup"><span data-stu-id="17558-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="17558-109">Поставщики служб</span><span class="sxs-lookup"><span data-stu-id="17558-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="17558-110">Определяемая функция, вызванная:</span><span class="sxs-lookup"><span data-stu-id="17558-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="17558-111">Мастер профилей MAPI</span><span class="sxs-lookup"><span data-stu-id="17558-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
BOOL SERVICEWIZARDDLGPROC(
  HWND hDlg,
  UINT wMsgID,
  WPARAM wParam,
  LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="17558-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="17558-112">Parameters</span></span>

<span data-ttu-id="17558-113">_hDlg_</span><span class="sxs-lookup"><span data-stu-id="17558-113">_hDlg_</span></span>
  
> <span data-ttu-id="17558-114">[in] Десналь окна в диалоговом окне "Мастер профилей".</span><span class="sxs-lookup"><span data-stu-id="17558-114">[in] Window handle to the Profile Wizard dialog box.</span></span> 
    
<span data-ttu-id="17558-115">_wMsgID_</span><span class="sxs-lookup"><span data-stu-id="17558-115">_wMsgID_</span></span>
  
> <span data-ttu-id="17558-116">[in] Сообщение окна, которое необходимо обработать.</span><span class="sxs-lookup"><span data-stu-id="17558-116">[in] The window message to be processed.</span></span> <span data-ttu-id="17558-117">Помимо обычных сообщений окна, ожидаемых модальным диалогом, можно получить следующие сообщения:</span><span class="sxs-lookup"><span data-stu-id="17558-117">In addition to the regular window messages expected by a modal dialog box, the following messages can be received:</span></span>
    
<span data-ttu-id="17558-118">WM_CLOSE</span><span class="sxs-lookup"><span data-stu-id="17558-118">WM_CLOSE</span></span> 
  
> <span data-ttu-id="17558-119">Мастер профилей завершен.</span><span class="sxs-lookup"><span data-stu-id="17558-119">The Profile Wizard has completed.</span></span> <span data-ttu-id="17558-120">Поставщик услуг должен сделать всю необходимую очистку, например распределить динамически выделяемую память.</span><span class="sxs-lookup"><span data-stu-id="17558-120">The service provider should do all required cleanup such as deallocating any dynamically allocated memory.</span></span> 
    
<span data-ttu-id="17558-121">WM_COMMAND</span><span class="sxs-lookup"><span data-stu-id="17558-121">WM_COMMAND</span></span> 
  
> <span data-ttu-id="17558-122">Был выбран один из элементов управления поставщика  или нажата кнопка "Далее"  или "Назад".</span><span class="sxs-lookup"><span data-stu-id="17558-122">One of the provider's controls has been selected, or the **Next** or **Back** button has been clicked.</span></span> <span data-ttu-id="17558-123">Значение параметра  _wParam_ указывает, какое из этих пользовательских событий произошло.</span><span class="sxs-lookup"><span data-stu-id="17558-123">The value in the  _wParam_ parameter indicates which of these user events has occurred.</span></span> 
    
<span data-ttu-id="17558-124">WM_INITDIALOG</span><span class="sxs-lookup"><span data-stu-id="17558-124">WM_INITDIALOG</span></span> 
  
> <span data-ttu-id="17558-125">Пользователь перешел на другую страницу свойств, для которой необходимо инициализировать диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="17558-125">The user has moved to another property page, for which the dialog box must be initialized.</span></span> <span data-ttu-id="17558-126">Поставщик должен инициализировать элементы управления, добавленные мастером профилей в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="17558-126">The provider should initialize the controls that the Profile Wizard has added to the dialog box.</span></span> 
    
<span data-ttu-id="17558-127">WIZ_QUERYNUMPAGES</span><span class="sxs-lookup"><span data-stu-id="17558-127">WIZ_QUERYNUMPAGES</span></span> 
  
> <span data-ttu-id="17558-128">Мастер профилей выводит запрос на количество страниц, которые должен отобразить поставщик.</span><span class="sxs-lookup"><span data-stu-id="17558-128">The Profile Wizard is prompting for the number of pages that the provider needs to display.</span></span> <span data-ttu-id="17558-129">Поставщик должен возвращать количество страниц вместо TRUE или FALSE.</span><span class="sxs-lookup"><span data-stu-id="17558-129">The provider should return the number of pages instead of TRUE or FALSE.</span></span> <span data-ttu-id="17558-130">Например, используйте следующий возвращаемый отчет, чтобы указать, что должны отображаться три страницы:</span><span class="sxs-lookup"><span data-stu-id="17558-130">For example, use the following return statement to indicate that three pages should to be displayed:</span></span>
    
   ```cpp
return (BOOL)3;

   ```

<span data-ttu-id="17558-131">_wParam_</span><span class="sxs-lookup"><span data-stu-id="17558-131">_wParam_</span></span>
  
> <span data-ttu-id="17558-132">[in] 32-битный параметр, связанный с сообщениями окна.</span><span class="sxs-lookup"><span data-stu-id="17558-132">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="17558-133">Возможные значения зависят от сообщения, указанного в параметре _wMsgID._</span><span class="sxs-lookup"><span data-stu-id="17558-133">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> <span data-ttu-id="17558-134">Помимо значений, ожидаемых в обычных сообщениях окна для модального диалоговых окон, можно получить следующие значения:</span><span class="sxs-lookup"><span data-stu-id="17558-134">In addition to the values expected with the regular window messages for a modal dialog box, the following values can be received:</span></span> 
    
<span data-ttu-id="17558-135">WIZ_NEXT</span><span class="sxs-lookup"><span data-stu-id="17558-135">WIZ_NEXT</span></span> 
  
> <span data-ttu-id="17558-136">Если _wMsgID_ WM_COMMAND, пользователь нажал кнопку **"Далее".**</span><span class="sxs-lookup"><span data-stu-id="17558-136">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Next** button.</span></span> 
    
<span data-ttu-id="17558-137">WIZ_PREV</span><span class="sxs-lookup"><span data-stu-id="17558-137">WIZ_PREV</span></span> 
  
> <span data-ttu-id="17558-138">Если _wMsgID_ WM_COMMAND, пользователь нажал кнопку **"Назад".**</span><span class="sxs-lookup"><span data-stu-id="17558-138">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Back** button.</span></span> 
    
<span data-ttu-id="17558-139">_lParam_</span><span class="sxs-lookup"><span data-stu-id="17558-139">_lParam_</span></span>
  
> <span data-ttu-id="17558-140">[in] 32-битный параметр, связанный с сообщениями окна.</span><span class="sxs-lookup"><span data-stu-id="17558-140">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="17558-141">Возможные значения зависят от сообщения, указанного в параметре _wMsgID._</span><span class="sxs-lookup"><span data-stu-id="17558-141">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="17558-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17558-142">Return value</span></span>

<span data-ttu-id="17558-143">Значение, возвращаемое функцией на основе **SERVICEWIZARDDLGPROC,** зависит от полученного сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="17558-143">The value returned by a **SERVICEWIZARDDLGPROC** based function is dependent on the window message received.</span></span> <span data-ttu-id="17558-144">Обратите внимание, в частности, на исключительное возвращаемого значения для WIZ_QUERYNUMPAGES сообщения.</span><span class="sxs-lookup"><span data-stu-id="17558-144">Note in particular the exceptional return value for the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="17558-145">Нормальные возвращаемые значения:</span><span class="sxs-lookup"><span data-stu-id="17558-145">The normal return values are:</span></span> 
  
<span data-ttu-id="17558-146">TRUE</span><span class="sxs-lookup"><span data-stu-id="17558-146">TRUE</span></span> 
  
> <span data-ttu-id="17558-147">Поставщик услуг обработал полученное сообщение окна.</span><span class="sxs-lookup"><span data-stu-id="17558-147">The service provider has processed the received window message.</span></span> 
    
<span data-ttu-id="17558-148">FALSE</span><span class="sxs-lookup"><span data-stu-id="17558-148">FALSE</span></span> 
  
> <span data-ttu-id="17558-149">Поставщик услуг не обработал полученное сообщение окна.</span><span class="sxs-lookup"><span data-stu-id="17558-149">The service provider has not processed the received window message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="17558-150">Примечания</span><span class="sxs-lookup"><span data-stu-id="17558-150">Remarks</span></span>

<span data-ttu-id="17558-151">Когда пользователь переходит со страницы свойств на другую, поставщик отвечает за скрытие элементов управления старой страницы и отображение элементов управления для следующей или предыдущей страницы.</span><span class="sxs-lookup"><span data-stu-id="17558-151">When the user moves from one property page to another, the provider is responsible for hiding the old page's controls and showing the controls for the next or previous page.</span></span> <span data-ttu-id="17558-152">Когда пользователь нажимает  кнопку "Далее", функция на основе **SERVICEWIZARDDLGPROC** с сообщением WM_COMMAND и WIZ_NEXT в _параметре wParam._</span><span class="sxs-lookup"><span data-stu-id="17558-152">When the user clicks the **Next** button, the **SERVICEWIZARDDLGPROC** based function is called with the WM_COMMAND message and WIZ_NEXT in the  _wParam_ parameter.</span></span> <span data-ttu-id="17558-153">Далее описано, что происходит между нажатием кнопки "Далее" и временем отображения страниц конфигурации первого поставщика. </span><span class="sxs-lookup"><span data-stu-id="17558-153">The following steps describe what occurs between the time the user clicks **Next** and the time the first provider's configuration pages are rendered.</span></span> 
  
1. <span data-ttu-id="17558-154">Мастер профилей скрывает все элементы управления, которые находятся в окне.</span><span class="sxs-lookup"><span data-stu-id="17558-154">The Profile Wizard hides any controls that are on the window.</span></span> 
    
2. <span data-ttu-id="17558-155">Мастер профилей добавляет на страницу скрытые элементы управления поставщика.</span><span class="sxs-lookup"><span data-stu-id="17558-155">The Profile Wizard adds the provider's hidden controls to the page.</span></span> 
    
3. <span data-ttu-id="17558-156">Мастер профилей вызывает **SERVICEWIZARDDLGPROC,** отправляя сообщение WM_INITDIALOG, чтобы поставщик может инициализировать элементы управления.</span><span class="sxs-lookup"><span data-stu-id="17558-156">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_INITDIALOG message, so that the provider can initialize the controls.</span></span> 
    
4. <span data-ttu-id="17558-157">Мастер профилей вызывает **SERVICEWIZARDDLGPROC,** отправляя WIZ_QUERYNUMPAGES сообщения.</span><span class="sxs-lookup"><span data-stu-id="17558-157">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="17558-158">Поставщик возвращает количество страниц, которые должны быть показаны.</span><span class="sxs-lookup"><span data-stu-id="17558-158">The provider returns the number of pages that are to be shown.</span></span> 
    
5. <span data-ttu-id="17558-159">Мастер профилей вызывает **SERVICEWIZARDDLGPROC,** отправляя сообщение WM_COMMAND с параметром  _wParam,_ установленным WIZ_NEXT или WIZ_PREV.</span><span class="sxs-lookup"><span data-stu-id="17558-159">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV.</span></span> <span data-ttu-id="17558-160">На этом этапе поставщик возвращает FALSE {error} или открывает свои элементы управления и возвращает TRUE {success}.</span><span class="sxs-lookup"><span data-stu-id="17558-160">At this point, the provider either returns FALSE {error} or reveals its controls and returns TRUE {success}.</span></span> <span data-ttu-id="17558-161">Если мастер профилей передает ID_NEXT, отображается первая страница поставщика.</span><span class="sxs-lookup"><span data-stu-id="17558-161">If the Profile Wizard passes in ID_NEXT, the provider's first page is displayed.</span></span> <span data-ttu-id="17558-162">Если ID_PREV передается, отображается последняя страница.</span><span class="sxs-lookup"><span data-stu-id="17558-162">If ID_PREV is passed in, the last page is displayed.</span></span> 
    
6. <span data-ttu-id="17558-163">Мастер профилей вызывает функцию **SERVICEWIZARDDLGPROC** поставщика, отправляя сообщение WM_COMMAND с параметром  _wParam,_ установленным как WIZ_NEXT, так и WIZ_PREV (в зависимости от нажатия пользователем кнопки).</span><span class="sxs-lookup"><span data-stu-id="17558-163">The Profile Wizard calls the provider's **SERVICEWIZARDDLGPROC** function, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV (depending on which button the user clicked).</span></span> <span data-ttu-id="17558-164">Поставщик отвечает за отображение или скрытие своих элементов управления и запись данных в **IMAPIProp,** переданный мастеру профилей, чтобы пошаговая последовательность страниц.</span><span class="sxs-lookup"><span data-stu-id="17558-164">The provider is responsible for showing or hiding its controls and writing its data to the **IMAPIProp** passed to the Profile Wizard to step through its sequence of pages.</span></span> <span data-ttu-id="17558-165">Поставщик должен вернуть true, если следующая или предыдущая страница была успешно показана, и FALSE, если ни следующая, ни предыдущая страницы не могут быть показаны.</span><span class="sxs-lookup"><span data-stu-id="17558-165">The provider should return TRUE if the next or previous page was successfully shown, and FALSE if neither the next nor previous page could be shown.</span></span> <span data-ttu-id="17558-166">Поставщик должен знать, когда он находится за пределами своей последовательности страниц, и реагировать соответствующим образом, скрывая свои элементы управления и записыв данные в профиль.</span><span class="sxs-lookup"><span data-stu-id="17558-166">The provider needs to be aware of when it is stepping outside of its sequence of pages, and respond appropriately by hiding its controls and writing its data to the profile.</span></span> 
    
7. <span data-ttu-id="17558-167">Если пользователь находится за пределами диапазона страниц поставщика, мастер профилей удаляет скрытые элементы управления поставщика из диалоговых окна и вызывает следующего поставщика или отображает следующую страницу, если это был последний поставщик.</span><span class="sxs-lookup"><span data-stu-id="17558-167">If the user steps outside the provider's range of pages, the Profile Wizard deletes the provider's hidden controls from the dialog box and calls the next provider or displays its next page if that was the last provider.</span></span> 
    

