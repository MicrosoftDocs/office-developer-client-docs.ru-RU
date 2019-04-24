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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356415"
---
# <a name="servicewizarddlgproc"></a><span data-ttu-id="18ffe-103">SERVICEWIZARDDLGPROC</span><span class="sxs-lookup"><span data-stu-id="18ffe-103">SERVICEWIZARDDLGPROC</span></span>
 
<span data-ttu-id="18ffe-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18ffe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18ffe-105">Определяет функцию обратного вызова, вызываемую мастером профилей, чтобы разрешить поставщику услуг реагировать на события пользователя при отображении страниц свойств или страниц свойств поставщика.</span><span class="sxs-lookup"><span data-stu-id="18ffe-105">Defines a callback function invoked by the Profile Wizard to allow a service provider to react to user events when the provider's property sheets or pages are being shown.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18ffe-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="18ffe-106">Header file:</span></span>  <br/> |<span data-ttu-id="18ffe-107">Мапивз. h</span><span class="sxs-lookup"><span data-stu-id="18ffe-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="18ffe-108">Определенная функция реализована следующим образом:</span><span class="sxs-lookup"><span data-stu-id="18ffe-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="18ffe-109">Поставщики служб</span><span class="sxs-lookup"><span data-stu-id="18ffe-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="18ffe-110">Определенная функция, вызываемая:</span><span class="sxs-lookup"><span data-stu-id="18ffe-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="18ffe-111">Мастер профилей MAPI</span><span class="sxs-lookup"><span data-stu-id="18ffe-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
BOOL SERVICEWIZARDDLGPROC(
  HWND hDlg,
  UINT wMsgID,
  WPARAM wParam,
  LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="18ffe-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="18ffe-112">Parameters</span></span>

<span data-ttu-id="18ffe-113">_Хдлг_</span><span class="sxs-lookup"><span data-stu-id="18ffe-113">_hDlg_</span></span>
  
> <span data-ttu-id="18ffe-114">возврата Диалоговое окно "дескриптор окна" в диалоговом окне мастера профилей.</span><span class="sxs-lookup"><span data-stu-id="18ffe-114">[in] Window handle to the Profile Wizard dialog box.</span></span> 
    
<span data-ttu-id="18ffe-115">_Вмсгид_</span><span class="sxs-lookup"><span data-stu-id="18ffe-115">_wMsgID_</span></span>
  
> <span data-ttu-id="18ffe-116">возврата Сообщение окна, которое необходимо обработать.</span><span class="sxs-lookup"><span data-stu-id="18ffe-116">[in] The window message to be processed.</span></span> <span data-ttu-id="18ffe-117">В дополнение к обычным сообщениям окон, ожидаемым модальным диалоговым окном, могут быть получены следующие сообщения:</span><span class="sxs-lookup"><span data-stu-id="18ffe-117">In addition to the regular window messages expected by a modal dialog box, the following messages can be received:</span></span>
    
<span data-ttu-id="18ffe-118">ВМ_КЛОСЕ</span><span class="sxs-lookup"><span data-stu-id="18ffe-118">WM_CLOSE</span></span> 
  
> <span data-ttu-id="18ffe-119">Работа мастера профилей завершена.</span><span class="sxs-lookup"><span data-stu-id="18ffe-119">The Profile Wizard has completed.</span></span> <span data-ttu-id="18ffe-120">Поставщик услуг должен выполнить всю необходимую очистку, например освобождение динамической выделенной памяти.</span><span class="sxs-lookup"><span data-stu-id="18ffe-120">The service provider should do all required cleanup such as deallocating any dynamically allocated memory.</span></span> 
    
<span data-ttu-id="18ffe-121">ВМ_КОММАНД</span><span class="sxs-lookup"><span data-stu-id="18ffe-121">WM_COMMAND</span></span> 
  
> <span data-ttu-id="18ffe-122">Был выбран один из элементов управления поставщика или нажата кнопка " **Далее** " или " **назад** ".</span><span class="sxs-lookup"><span data-stu-id="18ffe-122">One of the provider's controls has been selected, or the **Next** or **Back** button has been clicked.</span></span> <span data-ttu-id="18ffe-123">Значение в параметре _wParam_ указывает, какие из этих пользовательских событий произошли.</span><span class="sxs-lookup"><span data-stu-id="18ffe-123">The value in the  _wParam_ parameter indicates which of these user events has occurred.</span></span> 
    
<span data-ttu-id="18ffe-124">ВМ_ИНИТДИАЛОГ</span><span class="sxs-lookup"><span data-stu-id="18ffe-124">WM_INITDIALOG</span></span> 
  
> <span data-ttu-id="18ffe-125">Пользователь переместился на другую страницу свойств, для которой должно быть инициализировано диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="18ffe-125">The user has moved to another property page, for which the dialog box must be initialized.</span></span> <span data-ttu-id="18ffe-126">Поставщик должен инициализировать элементы управления, добавленные мастером профилей в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="18ffe-126">The provider should initialize the controls that the Profile Wizard has added to the dialog box.</span></span> 
    
<span data-ttu-id="18ffe-127">ВИЗ_КУЕРИНУМПАЖЕС</span><span class="sxs-lookup"><span data-stu-id="18ffe-127">WIZ_QUERYNUMPAGES</span></span> 
  
> <span data-ttu-id="18ffe-128">Мастер профилей запрашивает количество страниц, которое должен отображать поставщик.</span><span class="sxs-lookup"><span data-stu-id="18ffe-128">The Profile Wizard is prompting for the number of pages that the provider needs to display.</span></span> <span data-ttu-id="18ffe-129">Поставщик должен возвратить количество страниц, а не TRUE или FALSE.</span><span class="sxs-lookup"><span data-stu-id="18ffe-129">The provider should return the number of pages instead of TRUE or FALSE.</span></span> <span data-ttu-id="18ffe-130">Например, используйте приведенный ниже оператор return, чтобы указать, что должны отображаться три страницы:</span><span class="sxs-lookup"><span data-stu-id="18ffe-130">For example, use the following return statement to indicate that three pages should to be displayed:</span></span>
    
   ```cpp
return (BOOL)3;

   ```

<span data-ttu-id="18ffe-131">_wParam_</span><span class="sxs-lookup"><span data-stu-id="18ffe-131">_wParam_</span></span>
  
> <span data-ttu-id="18ffe-132">возврата 32 — битовый параметр, связанный с сообщениями окон.</span><span class="sxs-lookup"><span data-stu-id="18ffe-132">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="18ffe-133">Возможные значения зависят от сообщения, указанного в параметре _вмсгид_ .</span><span class="sxs-lookup"><span data-stu-id="18ffe-133">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> <span data-ttu-id="18ffe-134">Помимо значений, ожидаемых обычными сообщениями окон для модального диалогового окна, можно получить следующие значения:</span><span class="sxs-lookup"><span data-stu-id="18ffe-134">In addition to the values expected with the regular window messages for a modal dialog box, the following values can be received:</span></span> 
    
<span data-ttu-id="18ffe-135">ВИЗ_НЕКСТ</span><span class="sxs-lookup"><span data-stu-id="18ffe-135">WIZ_NEXT</span></span> 
  
> <span data-ttu-id="18ffe-136">Когда _вмсгид_ содержит вм_комманд, пользователь выбрал кнопку **Далее** .</span><span class="sxs-lookup"><span data-stu-id="18ffe-136">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Next** button.</span></span> 
    
<span data-ttu-id="18ffe-137">ВИЗ_ПРЕВ</span><span class="sxs-lookup"><span data-stu-id="18ffe-137">WIZ_PREV</span></span> 
  
> <span data-ttu-id="18ffe-138">Когда _вмсгид_ содержит вм_комманд, пользователь наСтроил кнопку Back ( **назад** ).</span><span class="sxs-lookup"><span data-stu-id="18ffe-138">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Back** button.</span></span> 
    
<span data-ttu-id="18ffe-139">_lParam_</span><span class="sxs-lookup"><span data-stu-id="18ffe-139">_lParam_</span></span>
  
> <span data-ttu-id="18ffe-140">возврата 32 — битовый параметр, связанный с сообщениями окон.</span><span class="sxs-lookup"><span data-stu-id="18ffe-140">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="18ffe-141">Возможные значения зависят от сообщения, указанного в параметре _вмсгид_ .</span><span class="sxs-lookup"><span data-stu-id="18ffe-141">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="18ffe-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18ffe-142">Return value</span></span>

<span data-ttu-id="18ffe-143">Значение, возвращаемое функцией на основе **сервицевизарддлгпрок** , зависит от полученного сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="18ffe-143">The value returned by a **SERVICEWIZARDDLGPROC** based function is dependent on the window message received.</span></span> <span data-ttu-id="18ffe-144">Обратите внимание, что в частности, для сообщения ВИЗ_КУЕРИНУМПАЖЕС возвращается исключительное значение.</span><span class="sxs-lookup"><span data-stu-id="18ffe-144">Note in particular the exceptional return value for the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="18ffe-145">Обычные возвращаемые значения:</span><span class="sxs-lookup"><span data-stu-id="18ffe-145">The normal return values are:</span></span> 
  
<span data-ttu-id="18ffe-146">TRUE</span><span class="sxs-lookup"><span data-stu-id="18ffe-146">TRUE</span></span> 
  
> <span data-ttu-id="18ffe-147">Поставщик услуг обработал сообщение Received Window.</span><span class="sxs-lookup"><span data-stu-id="18ffe-147">The service provider has processed the received window message.</span></span> 
    
<span data-ttu-id="18ffe-148">FALSE</span><span class="sxs-lookup"><span data-stu-id="18ffe-148">FALSE</span></span> 
  
> <span data-ttu-id="18ffe-149">Поставщик услуг не обработал сообщение Received Window.</span><span class="sxs-lookup"><span data-stu-id="18ffe-149">The service provider has not processed the received window message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="18ffe-150">Примечания</span><span class="sxs-lookup"><span data-stu-id="18ffe-150">Remarks</span></span>

<span data-ttu-id="18ffe-151">Когда пользователь перемещается с одной страницы свойств на другую, поставщик отвечает за скрытие элементов управления старой страницы и отображение элементов управления для следующей или предыдущей страницы.</span><span class="sxs-lookup"><span data-stu-id="18ffe-151">When the user moves from one property page to another, the provider is responsible for hiding the old page's controls and showing the controls for the next or previous page.</span></span> <span data-ttu-id="18ffe-152">Когда пользователь нажимает кнопку " **Далее** ", функция на основе **сервицевизарддлгпрок** вызываетСЯ с сообщением вм_комманд и Виз_некст в параметре _wParam_ .</span><span class="sxs-lookup"><span data-stu-id="18ffe-152">When the user clicks the **Next** button, the **SERVICEWIZARDDLGPROC** based function is called with the WM_COMMAND message and WIZ_NEXT in the  _wParam_ parameter.</span></span> <span data-ttu-id="18ffe-153">В следующих шагах описывается, что происходит между моментом, когда пользователь нажимает кнопку **Далее** и отображается время отображения страниц конфигурации первого поставщика.</span><span class="sxs-lookup"><span data-stu-id="18ffe-153">The following steps describe what occurs between the time the user clicks **Next** and the time the first provider's configuration pages are rendered.</span></span> 
  
1. <span data-ttu-id="18ffe-154">Мастер профилей скрывает все элементы управления, наявляющиесяся в окне.</span><span class="sxs-lookup"><span data-stu-id="18ffe-154">The Profile Wizard hides any controls that are on the window.</span></span> 
    
2. <span data-ttu-id="18ffe-155">Мастер профилей добавляет на страницу скрытые элементы управления поставщика.</span><span class="sxs-lookup"><span data-stu-id="18ffe-155">The Profile Wizard adds the provider's hidden controls to the page.</span></span> 
    
3. <span data-ttu-id="18ffe-156">Мастер профилей вызывает **сервицевизарддлгпрок**, отправляя сообщение вм_инитдиалог, чтобы поставщик мог инициализировать элементы управления.</span><span class="sxs-lookup"><span data-stu-id="18ffe-156">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_INITDIALOG message, so that the provider can initialize the controls.</span></span> 
    
4. <span data-ttu-id="18ffe-157">Мастер профилей вызывает **сервицевизарддлгпрок**, отправляя сообщение виз_куеринумпажес.</span><span class="sxs-lookup"><span data-stu-id="18ffe-157">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="18ffe-158">Поставщик возвращает число страниц, которые должны отображаться.</span><span class="sxs-lookup"><span data-stu-id="18ffe-158">The provider returns the number of pages that are to be shown.</span></span> 
    
5. <span data-ttu-id="18ffe-159">Мастер профилей вызывает **сервицевизарддлгпрок**, отправляя сообщение вм_комманд с параметром _wParam_ , равным виз_некст или виз_прев.</span><span class="sxs-lookup"><span data-stu-id="18ffe-159">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV.</span></span> <span data-ttu-id="18ffe-160">На этом шаге поставщик возвращает значение FALSE {Error} или открывает его элементы управления и возвращает значение TRUE {Success}.</span><span class="sxs-lookup"><span data-stu-id="18ffe-160">At this point, the provider either returns FALSE {error} or reveals its controls and returns TRUE {success}.</span></span> <span data-ttu-id="18ffe-161">Если мастер профилей передается в ИД_НЕКСТ, отображается первая страница поставщика.</span><span class="sxs-lookup"><span data-stu-id="18ffe-161">If the Profile Wizard passes in ID_NEXT, the provider's first page is displayed.</span></span> <span data-ttu-id="18ffe-162">Если ИД_ПРЕВ передается, отображается последняя страница.</span><span class="sxs-lookup"><span data-stu-id="18ffe-162">If ID_PREV is passed in, the last page is displayed.</span></span> 
    
6. <span data-ttu-id="18ffe-163">Мастер профилей вызывает функцию **сервицевизарддлгпрок** поставщика, отправляя сообщение вм_комманд с параметром _wParam_ , равным виз_некст или виз_прев (в зависимости от того, какую кнопку пользователь настроил).</span><span class="sxs-lookup"><span data-stu-id="18ffe-163">The Profile Wizard calls the provider's **SERVICEWIZARDDLGPROC** function, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV (depending on which button the user clicked).</span></span> <span data-ttu-id="18ffe-164">Поставщик отвечает за отображение или скрытие элементов управления и запись их данных в **IMAPIProp** , передаваемый мастеру профилей для пошаговой последовательности страниц.</span><span class="sxs-lookup"><span data-stu-id="18ffe-164">The provider is responsible for showing or hiding its controls and writing its data to the **IMAPIProp** passed to the Profile Wizard to step through its sequence of pages.</span></span> <span data-ttu-id="18ffe-165">Поставщик должен возвращать значение TRUE, если следующая или Предыдущая страница была успешно отображена, и FALSE, если не удается отобразить ни следующую, ни предыдущую страницу.</span><span class="sxs-lookup"><span data-stu-id="18ffe-165">The provider should return TRUE if the next or previous page was successfully shown, and FALSE if neither the next nor previous page could be shown.</span></span> <span data-ttu-id="18ffe-166">Поставщику необходимо знать, когда он выполняет шаг с заходом вне последовательности страниц и отвечает соответствующим образом, скрывая элементы управления и записывает данные в профиль.</span><span class="sxs-lookup"><span data-stu-id="18ffe-166">The provider needs to be aware of when it is stepping outside of its sequence of pages, and respond appropriately by hiding its controls and writing its data to the profile.</span></span> 
    
7. <span data-ttu-id="18ffe-167">Если пользователь выполняет действия за пределами диапазона страниц поставщика, мастер профилей удаляет скрытые элементы управления поставщика из диалогового окна и вызывает следующего поставщика или отображает следующую страницу, если это последний поставщик.</span><span class="sxs-lookup"><span data-stu-id="18ffe-167">If the user steps outside the provider's range of pages, the Profile Wizard deletes the provider's hidden controls from the dialog box and calls the next provider or displays its next page if that was the last provider.</span></span> 
    

