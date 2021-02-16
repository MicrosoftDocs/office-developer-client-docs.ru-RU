---
title: Интерфейсы window (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e6900ad7-c147-4816-93a9-5773170b115a
description: Интерфейсы Window и Windows — это объекты API OneNote 2013, которые позволяют пользователям работать с окнами OneNote. Эти объекты позволяют пользователям применять перечисление в наборе окон OneNote и изменять определенные свойства окон.
ms.openlocfilehash: efc34312def588ecff54c63b3db84f8bf909352b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317039"
---
# <a name="window-interfaces-onenote"></a><span data-ttu-id="1dae1-104">Интерфейсы window (OneNote)</span><span class="sxs-lookup"><span data-stu-id="1dae1-104">Window interfaces (OneNote)</span></span>

<span data-ttu-id="1dae1-105">Интерфейсы **Window** и **Windows** — это объекты API OneNote 2013, которые позволяют пользователям работать с окнами OneNote.</span><span class="sxs-lookup"><span data-stu-id="1dae1-105">The **Window** and **Windows** interfaces are OneNote 2013 API objects that enables users to work with OneNote windows.</span></span> <span data-ttu-id="1dae1-106">Эти объекты позволяют пользователям применять перечисление в наборе окон OneNote и изменять определенные свойства окон.</span><span class="sxs-lookup"><span data-stu-id="1dae1-106">These objects allow users to enumerate through the set of OneNote windows and modify certain window properties.</span></span> 
  
## <a name="onenote-window-views"></a><span data-ttu-id="1dae1-107">Представления окна OneNote</span><span class="sxs-lookup"><span data-stu-id="1dae1-107">OneNote window views</span></span>

<span data-ttu-id="1dae1-108">В следующем списке показаны четыре режима просмотра, которые можно использовать для окон OneNote:</span><span class="sxs-lookup"><span data-stu-id="1dae1-108">The following list shows the four view modes that you can use for OneNote windows:</span></span> 
  
- <span data-ttu-id="1dae1-109">Обычное представление — отображает окно OneNote по умолчанию, в котором отображаются области навигации "Записная книжка" и "Страница".</span><span class="sxs-lookup"><span data-stu-id="1dae1-109">Normal view—Displays the default OneNote window in which the Notebook and Page navigation panes are visible.</span></span>
    
- <span data-ttu-id="1dae1-110">Представление "Полная страница" — отображает минимальное представление пользовательского интерфейса, в котором области "Записная книжка" и "Страница" не отображаются.</span><span class="sxs-lookup"><span data-stu-id="1dae1-110">Full Page view—Displays a minimal user-interface (UI) view in which the Notebook and Page panes are not displayed.</span></span>
    
- <span data-ttu-id="1dae1-111">Краткое примечание. Отображает небольшое окно, которое позволяет пользователям делать короткие заметки.</span><span class="sxs-lookup"><span data-stu-id="1dae1-111">Quick note—Displays a small window that allows users to take short notes.</span></span> <span data-ttu-id="1dae1-112">Как правило, доступ к быстрым заметкам можно получить с помощью значка  OneNote в области уведомлений Windows, но вы также можете получить к ним доступ с помощью вкладки "Просмотр" в OneNote.</span><span class="sxs-lookup"><span data-stu-id="1dae1-112">You would usually access quick notes through the OneNote icon in the Windows notification area, but you can also access them through the **View** tab in OneNote.</span></span> 
    
- <span data-ttu-id="1dae1-113">Закрепление на рабочем столе — отображает окно OneNote, которое можно пристыковать к любой стороне рабочего стола (аналогично панели задач).</span><span class="sxs-lookup"><span data-stu-id="1dae1-113">Dock to Desktop—Displays a OneNote window that you can dock to any side of the desktop (similar to the taskbar).</span></span> <span data-ttu-id="1dae1-114">Это представление уменьшает размер рабочего стола в зависимости от размера окна.</span><span class="sxs-lookup"><span data-stu-id="1dae1-114">This view reduces the size of the desktop to fit the window.</span></span> <span data-ttu-id="1dae1-115">В любое время можно пристыковать только одно окно, и окно всегда отображается, не блокируя рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="1dae1-115">You can dock only one window at any time, and the window is always visible without blocking the desktop.</span></span> 
    
<span data-ttu-id="1dae1-116">На следующем рисунке показано, как выглядит представление "Полная страница", "Док-станция до рабочего стола" и краткие заметки на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="1dae1-116">The following figure shows what the Full Page view, Dock to Desktop view, and quick notes look like on your desktop.</span></span>
  
<span data-ttu-id="1dae1-117">**Представления OneNote**</span><span class="sxs-lookup"><span data-stu-id="1dae1-117">**OneNote views**</span></span>

<span data-ttu-id="1dae1-118">![В окне OneNote представления](media/ON15Con_views.jpg "окон OneNote")</span><span class="sxs-lookup"><span data-stu-id="1dae1-118">![OneNote window views](media/ON15Con_views.jpg "OneNote window views")</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="1dae1-119">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="1dae1-119">Interfaces</span></span>

<span data-ttu-id="1dae1-120">В этом разделе перечислены интерфейсы и члены, которые можно использовать для изменения Windows OneNote программным путем.</span><span class="sxs-lookup"><span data-stu-id="1dae1-120">This section lists the interfaces and members that you can use to modify OneNote windows programmatically.</span></span>
  
### <a name="windows-interface"></a><span data-ttu-id="1dae1-121">Интерфейс Windows</span><span class="sxs-lookup"><span data-stu-id="1dae1-121">Windows interface</span></span>

<span data-ttu-id="1dae1-122">Интерфейс **Windows** позволяет пользователю получить доступ к набору открытых окон OneNote.</span><span class="sxs-lookup"><span data-stu-id="1dae1-122">The **Windows** interface allows the user to access the set of opened OneNote windows.</span></span> <span data-ttu-id="1dae1-123">Это свойство класса приложения **OneNote,** доступ к нему можно получить через **Application.Windows.**</span><span class="sxs-lookup"><span data-stu-id="1dae1-123">It is a property of the OneNote **Application** class, accessed through **Application.Windows**.</span></span> <span data-ttu-id="1dae1-124">Возвращается enumerated набор окон OneNote.</span><span class="sxs-lookup"><span data-stu-id="1dae1-124">This returns the enumerated set of OneNote windows.</span></span> 
  
<span data-ttu-id="1dae1-125">**Свойства**</span><span class="sxs-lookup"><span data-stu-id="1dae1-125">**Properties**</span></span>

|<span data-ttu-id="1dae1-126">**Имя**</span><span class="sxs-lookup"><span data-stu-id="1dae1-126">**Name**</span></span>|<span data-ttu-id="1dae1-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1dae1-127">**Type**</span></span>|<span data-ttu-id="1dae1-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1dae1-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1dae1-129">**Count**</span><span class="sxs-lookup"><span data-stu-id="1dae1-129">**Count**</span></span> <br/> |<span data-ttu-id="1dae1-130">ulong</span><span class="sxs-lookup"><span data-stu-id="1dae1-130">ulong</span></span>  <br/> |<span data-ttu-id="1dae1-131">Получает количество объектов **Window** в **наборе Windows.**</span><span class="sxs-lookup"><span data-stu-id="1dae1-131">Gets the number of **Window** objects in the **Windows** set.</span></span>  <br/> |
|<span data-ttu-id="1dae1-132">**CurrentWindow**</span><span class="sxs-lookup"><span data-stu-id="1dae1-132">**CurrentWindow**</span></span> <br/> |<span data-ttu-id="1dae1-133">**Window**</span><span class="sxs-lookup"><span data-stu-id="1dae1-133">**Window**</span></span> <br/> |<span data-ttu-id="1dae1-134">Получает объект **Window** активного окна OneNote.</span><span class="sxs-lookup"><span data-stu-id="1dae1-134">Gets the **Window** object of the active OneNote window.</span></span>  <br/> |
|<span data-ttu-id="1dae1-135">**Items**</span><span class="sxs-lookup"><span data-stu-id="1dae1-135">**Items**</span></span> <br/> |<span data-ttu-id="1dae1-136">**Window**</span><span class="sxs-lookup"><span data-stu-id="1dae1-136">**Window**</span></span> <br/> |<span data-ttu-id="1dae1-137">Возвращает объект **Window,** соответствующий переданным значению индекса.</span><span class="sxs-lookup"><span data-stu-id="1dae1-137">Returns the **Window** object that corresponds to the index value passed.</span></span> <span data-ttu-id="1dae1-138">Доступ к этому свойству напрямую не перейти.</span><span class="sxs-lookup"><span data-stu-id="1dae1-138">This property cannot be accessed directly.</span></span> <span data-ttu-id="1dae1-139">Чтобы вернуть объект **Window,** используйте **windows [(uint) index]**.</span><span class="sxs-lookup"><span data-stu-id="1dae1-139">To return a **Window** object, use **Windows [(uint) index]**.</span></span>  <br/> |
   
### <a name="window-interface"></a><span data-ttu-id="1dae1-140">Интерфейс окна</span><span class="sxs-lookup"><span data-stu-id="1dae1-140">Window interface</span></span>

<span data-ttu-id="1dae1-141">Интерфейс **Window** позволяет пользователю получать доступ к определенным свойствам каждого окна.</span><span class="sxs-lookup"><span data-stu-id="1dae1-141">The **Window** interface allows the user to access certain properties of each window.</span></span> <span data-ttu-id="1dae1-142">Для доступа к каждому окну OneNote можно использовать свойство **Windows** класса **Application.**</span><span class="sxs-lookup"><span data-stu-id="1dae1-142">Each OneNote window can be accessed by enumerating through the **Windows** property of the **Application** class.</span></span> 
  
<span data-ttu-id="1dae1-143">**Свойства**</span><span class="sxs-lookup"><span data-stu-id="1dae1-143">**Properties**</span></span>

|<span data-ttu-id="1dae1-144">**Имя**</span><span class="sxs-lookup"><span data-stu-id="1dae1-144">**Name**</span></span>|<span data-ttu-id="1dae1-145">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1dae1-145">**Type**</span></span>|<span data-ttu-id="1dae1-146">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1dae1-146">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1dae1-147">**Active**</span><span class="sxs-lookup"><span data-stu-id="1dae1-147">**Active**</span></span> <br/> |<span data-ttu-id="1dae1-148">bool</span><span class="sxs-lookup"><span data-stu-id="1dae1-148">bool</span></span>  <br/> |<span data-ttu-id="1dae1-149">Получает или задает значение, которое указывает, является ли окно активным окном OneNote.</span><span class="sxs-lookup"><span data-stu-id="1dae1-149">Gets or sets a value that indicates whether the window is the active OneNote window.</span></span>  <br/> |
|<span data-ttu-id="1dae1-150">**Application**</span><span class="sxs-lookup"><span data-stu-id="1dae1-150">**Application**</span></span> <br/> |<span data-ttu-id="1dae1-151">**Application**</span><span class="sxs-lookup"><span data-stu-id="1dae1-151">**Application**</span></span> <br/> |<span data-ttu-id="1dae1-152">Получает объект приложения  OneNote, связанный с окном.</span><span class="sxs-lookup"><span data-stu-id="1dae1-152">Gets the OneNote **Application** object that is associated with the window.</span></span>  <br/> |
|<span data-ttu-id="1dae1-153">**CurrentPageId**</span><span class="sxs-lookup"><span data-stu-id="1dae1-153">**CurrentPageId**</span></span> <br/> |<span data-ttu-id="1dae1-154">string</span><span class="sxs-lookup"><span data-stu-id="1dae1-154">string</span></span>  <br/> |<span data-ttu-id="1dae1-155">Получает ИД объекта активной страницы OneNote окна.</span><span class="sxs-lookup"><span data-stu-id="1dae1-155">Gets the object ID of the active OneNote page of the window.</span></span>  <br/> |
|<span data-ttu-id="1dae1-156">**CurrentSectionId**</span><span class="sxs-lookup"><span data-stu-id="1dae1-156">**CurrentSectionId**</span></span> <br/> |<span data-ttu-id="1dae1-157">string</span><span class="sxs-lookup"><span data-stu-id="1dae1-157">string</span></span>  <br/> |<span data-ttu-id="1dae1-158">Получает ИД объекта активного раздела OneNote окна.</span><span class="sxs-lookup"><span data-stu-id="1dae1-158">Gets the object ID of the active OneNote section of the window.</span></span>  <br/> |
|<span data-ttu-id="1dae1-159">**CurrentSectionGroupId**</span><span class="sxs-lookup"><span data-stu-id="1dae1-159">**CurrentSectionGroupId**</span></span> <br/> |<span data-ttu-id="1dae1-160">string</span><span class="sxs-lookup"><span data-stu-id="1dae1-160">string</span></span>  <br/> |<span data-ttu-id="1dae1-161">Получает ИД объекта активной группы разделов OneNote окна.</span><span class="sxs-lookup"><span data-stu-id="1dae1-161">Gets the object ID of the active OneNote section group of the window.</span></span>  <br/> |
|<span data-ttu-id="1dae1-162">**CurrentNotebookId**</span><span class="sxs-lookup"><span data-stu-id="1dae1-162">**CurrentNotebookId**</span></span> <br/> |<span data-ttu-id="1dae1-163">string</span><span class="sxs-lookup"><span data-stu-id="1dae1-163">string</span></span>  <br/> |<span data-ttu-id="1dae1-164">Получает ИД объекта активной записной книжки OneNote окна.</span><span class="sxs-lookup"><span data-stu-id="1dae1-164">Gets the object ID of the active OneNote notebook of the window.</span></span>  <br/> |
|<span data-ttu-id="1dae1-165">**DockedLocation**</span><span class="sxs-lookup"><span data-stu-id="1dae1-165">**DockedLocation**</span></span> <br/> |<span data-ttu-id="1dae1-166">**DockedLocation**</span><span class="sxs-lookup"><span data-stu-id="1dae1-166">**DockedLocation**</span></span> <br/> |<span data-ttu-id="1dae1-167">Получает или задает закрепленное расположение окна OneNote.</span><span class="sxs-lookup"><span data-stu-id="1dae1-167">Gets or sets the docked location of the OneNote window.</span></span>  <br/> |
|<span data-ttu-id="1dae1-168">**FullPageView**</span><span class="sxs-lookup"><span data-stu-id="1dae1-168">**FullPageView**</span></span> <br/> |<span data-ttu-id="1dae1-169">bool</span><span class="sxs-lookup"><span data-stu-id="1dae1-169">bool</span></span>  <br/> |<span data-ttu-id="1dae1-170">Получает или задает значение, которое указывает, находится ли окно в представлении "Полная страница" (минимальное представление пользовательского интерфейса).</span><span class="sxs-lookup"><span data-stu-id="1dae1-170">Gets or sets a value that indicates whether the window is in Full Page view (minimal UI view).</span></span>  <br/> |
|<span data-ttu-id="1dae1-171">**SideNote**</span><span class="sxs-lookup"><span data-stu-id="1dae1-171">**SideNote**</span></span> <br/> |<span data-ttu-id="1dae1-172">bool</span><span class="sxs-lookup"><span data-stu-id="1dae1-172">bool</span></span>  <br/> |<span data-ttu-id="1dae1-173">Получает или задает значение, которое указывает, является ли окно окном с кратким примечанием.</span><span class="sxs-lookup"><span data-stu-id="1dae1-173">Gets or sets a value that indicates whether the window is a quick note window.</span></span>  <br/> |
|<span data-ttu-id="1dae1-174">**WindowHandle**</span><span class="sxs-lookup"><span data-stu-id="1dae1-174">**WindowHandle**</span></span> <br/> |<span data-ttu-id="1dae1-175">ulong</span><span class="sxs-lookup"><span data-stu-id="1dae1-175">ulong</span></span>  <br/> |<span data-ttu-id="1dae1-176">Получает ИД работки окна OneNote.</span><span class="sxs-lookup"><span data-stu-id="1dae1-176">Gets the handle ID of the OneNote window.</span></span>  <br/> |
   
<span data-ttu-id="1dae1-177">**Методы**</span><span class="sxs-lookup"><span data-stu-id="1dae1-177">**Methods**</span></span>
  
<span data-ttu-id="1dae1-178">Для навигации по указанным объектам в окне OneNote или по указанным URL-адресам можно использовать следующие методы интерфейса **Window.**</span><span class="sxs-lookup"><span data-stu-id="1dae1-178">You can use the following methods of the **Window** interface to navigate to specified objects in the OneNote window or to specified URLs.</span></span> 
  
<span data-ttu-id="1dae1-179">**NavigateTo**</span><span class="sxs-lookup"><span data-stu-id="1dae1-179">**NavigateTo**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1dae1-180">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1dae1-180">**Description**</span></span> <br/> |<span data-ttu-id="1dae1-181">Переход к указанному объекту в окне OneNote.</span><span class="sxs-lookup"><span data-stu-id="1dae1-181">Navigates to the specified object in the OneNote window.</span></span> <span data-ttu-id="1dae1-182">Например, можно перейти к разделам, страницам и элементам структур на страницах.</span><span class="sxs-lookup"><span data-stu-id="1dae1-182">For example, you can navigate to sections, pages, and outline elements within pages.</span></span>  <br/> |
|<span data-ttu-id="1dae1-183">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="1dae1-183">**Syntax**</span></span> <br/> | <span data-ttu-id="1dae1-184">`HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); `</span><span class="sxs-lookup"><span data-stu-id="1dae1-184">`HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); `</span></span> <br/> |
|<span data-ttu-id="1dae1-185">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="1dae1-185">**Parameters**</span></span> <br/> | <span data-ttu-id="1dae1-186">_bstrHierarchyObjectID_— ид иерархии OneNote объекта, к который нужно перейти.</span><span class="sxs-lookup"><span data-stu-id="1dae1-186">_bstrHierarchyObjectID_—The hierarchy OneNote ID of the object you want to navigate to.</span></span> <span data-ttu-id="1dae1-187">ИД объекта может ссылаться на записную книжку, раздел, группу разделов или страницу OneNote.</span><span class="sxs-lookup"><span data-stu-id="1dae1-187">The object ID can reference a OneNote notebook, section, section group, or page.</span></span>  <br/>  <span data-ttu-id="1dae1-188">_bstrObjectID_— ИД OneNote конкретного объекта для перемещения на страницу OneNote.</span><span class="sxs-lookup"><span data-stu-id="1dae1-188">_bstrObjectID_—The OneNote ID of the specific object to navigate to within a OneNote page.</span></span> <span data-ttu-id="1dae1-189">Если пользователь не хочет переходить к определенному объекту на странице, этому параметру задано null.</span><span class="sxs-lookup"><span data-stu-id="1dae1-189">If the user does not want to navigate to a specific object on a page, this parameter is set to null.</span></span>  <br/> |
   
<span data-ttu-id="1dae1-190">**NavigateToUrl**</span><span class="sxs-lookup"><span data-stu-id="1dae1-190">**NavigateToUrl**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1dae1-191">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1dae1-191">**Description**</span></span> <br/> |<span data-ttu-id="1dae1-192">Если передана ссылка OneNote (onenote://), откроется окно OneNote для соответствующего расположения в OneNote.</span><span class="sxs-lookup"><span data-stu-id="1dae1-192">If passed a OneNote link (onenote://), opens the OneNote window to the corresponding location in OneNote.</span></span> <span data-ttu-id="1dae1-193">Однако если ссылка является внешней ссылкой, например https:// или file://, появится диалоговое окно безопасности.</span><span class="sxs-lookup"><span data-stu-id="1dae1-193">However, if the link is an external link, such as https:// or file://, a security dialog box will appear.</span></span> <span data-ttu-id="1dae1-194">После этого OneNote пытается открыть ссылку, и возвращается ошибка HResult.hrObjectDoesNotExist.</span><span class="sxs-lookup"><span data-stu-id="1dae1-194">Upon dismissal, OneNote attempts to open up the link and an HResult.hrObjectDoesNotExist error is returned.</span></span>  <br/> |
|<span data-ttu-id="1dae1-195">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="1dae1-195">**Syntax**</span></span> <br/> | <span data-ttu-id="1dae1-196">`HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); `</span><span class="sxs-lookup"><span data-stu-id="1dae1-196">`HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); `</span></span> <br/> |
|<span data-ttu-id="1dae1-197">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="1dae1-197">**Parameters**</span></span> <br/> | <span data-ttu-id="1dae1-198">_bstrUrl_— URL-адрес для навигации.</span><span class="sxs-lookup"><span data-stu-id="1dae1-198">_bstrUrl_—The URL to navigate to.</span></span>  <br/> |
   
<span data-ttu-id="1dae1-199">**SetDockedLocation**</span><span class="sxs-lookup"><span data-stu-id="1dae1-199">**SetDockedLocation**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1dae1-200">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1dae1-200">**Description**</span></span> <br/> |<span data-ttu-id="1dae1-201">Пристыковка окна к расположению, указанному **dockLocation** и монитором **в ptMonitor.**</span><span class="sxs-lookup"><span data-stu-id="1dae1-201">Docks the window to the location specified by **dockLocation** and the monitor at **ptMonitor**.</span></span>  <br/> |
|<span data-ttu-id="1dae1-202">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="1dae1-202">**Syntax**</span></span> <br/> | <span data-ttu-id="1dae1-203">`HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);`</span><span class="sxs-lookup"><span data-stu-id="1dae1-203">`HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);`</span></span> <br/> |
|<span data-ttu-id="1dae1-204">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="1dae1-204">**Parameters**</span></span> <br/> | <span data-ttu-id="1dae1-205">_dockLocation_ — указывает закрепленное расположение окна OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="1dae1-205">_dockLocation_ - Indicates the docked location of a OneNote 2013 window.</span></span>  <br/>  <span data-ttu-id="1dae1-206">_ptMonitor_ ( Необязательный) — указывает в координатах x,y, на которые следует пристыковать окно.</span><span class="sxs-lookup"><span data-stu-id="1dae1-206">_ptMonitor_ - (Optional) Indicates in x,y co-ordinates which monitor the window should be docked to.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="1dae1-207">Пример</span><span class="sxs-lookup"><span data-stu-id="1dae1-207">Example</span></span>

<span data-ttu-id="1dae1-208">Следующий код проходит через окна OneNote, чтобы найти закрепленное окно.</span><span class="sxs-lookup"><span data-stu-id="1dae1-208">The following code iterates through the OneNote windows to find a docked window.</span></span> <span data-ttu-id="1dae1-209">Если закрепленное окно не существует, пример пристыковит активное окно.</span><span class="sxs-lookup"><span data-stu-id="1dae1-209">If no docked window exists, the example docks the active window.</span></span> <span data-ttu-id="1dae1-210">Если активного окна нет, код создает новое закрепленное окно.</span><span class="sxs-lookup"><span data-stu-id="1dae1-210">If no active window exists, the code creates a new docked window.</span></span>
  
```cs
using System;
using System.Diagnostics;
using Microsoft.Office.Interop.OneNote;
namespace SampleWND
{
    class DockOneNoteWindow
    {
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = new Microsoft.Office.Interop.OneNote.Application();
            // Search through all OneNote windows for a docked window and activate it.
            bool foundDockedWND = false;
            for (int i = 0; i < app.Windows.Count; i++)
            {
                if (app.Windows[(uint) i].DockedLocation != DockLocation.dlNone)
                {
                    foundDockedWND = true;
                    app.Windows[(uint) i].Active = true;
                }
            }
            
            // If no docked window exists, dock the active window.
            if (!foundDockedWND && (app.Windows.Count > 0))
                app.Windows.CurrentWindow.DockedLocation = DockLocation.dlDefault;
            // If no active window exists, create a new docked window.
            if (app.Windows.Count < 1)
            {
                Process oneProc = new Process();
                oneProc.StartInfo.FileName = "onenote.exe";
                oneProc.StartInfo.Arguments = "/docked";
                oneProc.Start();
            }
        }
    }
}

```

## <a name="see-also"></a><span data-ttu-id="1dae1-211">См. также</span><span class="sxs-lookup"><span data-stu-id="1dae1-211">See also</span></span>

- [<span data-ttu-id="1dae1-212">Справочник разработчика для OneNote</span><span class="sxs-lookup"><span data-stu-id="1dae1-212">OneNote developer reference</span></span>](onenote-developer-reference.md)

