---
title: Интерфейсы окон (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e6900ad7-c147-4816-93a9-5773170b115a
description: Интерфейсы Window и Windows являются объектами API 2013 OneNote, которые позволяют пользователям работать с OneNote окнами. Эти объекты позволяют пользователям применять перечисление в наборе окон OneNote и изменять определенные свойства окон.
ms.openlocfilehash: efc34312def588ecff54c63b3db84f8bf909352b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317039"
---
# <a name="window-interfaces-onenote"></a><span data-ttu-id="b3c65-104">Интерфейсы окон (OneNote)</span><span class="sxs-lookup"><span data-stu-id="b3c65-104">Window interfaces (OneNote)</span></span>

<span data-ttu-id="b3c65-105">Интерфейсы **Window** **и Windows** являются объектами API 2013 OneNote, что позволяет пользователям работать с OneNote окнами.</span><span class="sxs-lookup"><span data-stu-id="b3c65-105">The **Window** and **Windows** interfaces are OneNote 2013 API objects that enables users to work with OneNote windows.</span></span> <span data-ttu-id="b3c65-106">Эти объекты позволяют пользователям применять перечисление в наборе окон OneNote и изменять определенные свойства окон.</span><span class="sxs-lookup"><span data-stu-id="b3c65-106">These objects allow users to enumerate through the set of OneNote windows and modify certain window properties.</span></span> 
  
## <a name="onenote-window-views"></a><span data-ttu-id="b3c65-107">Представления окна OneNote</span><span class="sxs-lookup"><span data-stu-id="b3c65-107">OneNote window views</span></span>

<span data-ttu-id="b3c65-108">В следующем списке показаны четыре режима представления, которые можно использовать для OneNote windows:</span><span class="sxs-lookup"><span data-stu-id="b3c65-108">The following list shows the four view modes that you can use for OneNote windows:</span></span> 
  
- <span data-ttu-id="b3c65-109">Нормальное представление — отображает окно OneNote, в котором видны области навигации блокнота и страницы.</span><span class="sxs-lookup"><span data-stu-id="b3c65-109">Normal view—Displays the default OneNote window in which the Notebook and Page navigation panes are visible.</span></span>
    
- <span data-ttu-id="b3c65-110">Полное представление страницы — отображает минимальное представление пользовательского интерфейса (пользовательского интерфейса), в котором не отображаются области блокнота и страницы.</span><span class="sxs-lookup"><span data-stu-id="b3c65-110">Full Page view—Displays a minimal user-interface (UI) view in which the Notebook and Page panes are not displayed.</span></span>
    
- <span data-ttu-id="b3c65-111">Быстрая заметка— отображает небольшое окно, которое позволяет пользователям делать короткие заметки.</span><span class="sxs-lookup"><span data-stu-id="b3c65-111">Quick note—Displays a small window that allows users to take short notes.</span></span> <span data-ttu-id="b3c65-112">Обычно можно получить доступ к быстрым заметкам через значок OneNote в области уведомлений Windows, но вы также можете получить доступ к ним через вкладку **Просмотр** в OneNote.</span><span class="sxs-lookup"><span data-stu-id="b3c65-112">You would usually access quick notes through the OneNote icon in the Windows notification area, but you can also access them through the **View** tab in OneNote.</span></span> 
    
- <span data-ttu-id="b3c65-113">Стыковка с настольным компьютером — отображает окно OneNote, которое можно пристыковать к любой стороне рабочего стола (аналогично панели задач).</span><span class="sxs-lookup"><span data-stu-id="b3c65-113">Dock to Desktop—Displays a OneNote window that you can dock to any side of the desktop (similar to the taskbar).</span></span> <span data-ttu-id="b3c65-114">Это представление уменьшает размер рабочего стола, чтобы соответствовать окну.</span><span class="sxs-lookup"><span data-stu-id="b3c65-114">This view reduces the size of the desktop to fit the window.</span></span> <span data-ttu-id="b3c65-115">Вы можете состыковать только одно окно в любое время, и окно всегда видно, не блокируя рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="b3c65-115">You can dock only one window at any time, and the window is always visible without blocking the desktop.</span></span> 
    
<span data-ttu-id="b3c65-116">На следующем рисунке показано, как выглядит представление "Полная страница", "Стыковка с настольным компьютером" и быстрые заметки на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="b3c65-116">The following figure shows what the Full Page view, Dock to Desktop view, and quick notes look like on your desktop.</span></span>
  
<span data-ttu-id="b3c65-117">**Представления OneNote**</span><span class="sxs-lookup"><span data-stu-id="b3c65-117">**OneNote views**</span></span>

<span data-ttu-id="b3c65-118">![OneNote представления OneNote](media/ON15Con_views.jpg "окна")</span><span class="sxs-lookup"><span data-stu-id="b3c65-118">![OneNote window views](media/ON15Con_views.jpg "OneNote window views")</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="b3c65-119">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="b3c65-119">Interfaces</span></span>

<span data-ttu-id="b3c65-120">В этом разделе перечислены интерфейсы и члены, которые можно использовать для программных OneNote Windows.</span><span class="sxs-lookup"><span data-stu-id="b3c65-120">This section lists the interfaces and members that you can use to modify OneNote windows programmatically.</span></span>
  
### <a name="windows-interface"></a><span data-ttu-id="b3c65-121">Windows интерфейс</span><span class="sxs-lookup"><span data-stu-id="b3c65-121">Windows interface</span></span>

<span data-ttu-id="b3c65-122">Интерфейс **Windows** позволяет пользователю получить доступ к набору открытых OneNote окон.</span><span class="sxs-lookup"><span data-stu-id="b3c65-122">The **Windows** interface allows the user to access the set of opened OneNote windows.</span></span> <span data-ttu-id="b3c65-123">Это свойство класса **OneNote,** доступ к нему через **Application.Windows.**</span><span class="sxs-lookup"><span data-stu-id="b3c65-123">It is a property of the OneNote **Application** class, accessed through **Application.Windows**.</span></span> <span data-ttu-id="b3c65-124">В этом случае возвращается набор OneNote окон.</span><span class="sxs-lookup"><span data-stu-id="b3c65-124">This returns the enumerated set of OneNote windows.</span></span> 
  
<span data-ttu-id="b3c65-125">**Свойства**</span><span class="sxs-lookup"><span data-stu-id="b3c65-125">**Properties**</span></span>

|<span data-ttu-id="b3c65-126">**Имя**</span><span class="sxs-lookup"><span data-stu-id="b3c65-126">**Name**</span></span>|<span data-ttu-id="b3c65-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b3c65-127">**Type**</span></span>|<span data-ttu-id="b3c65-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b3c65-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b3c65-129">**Count**</span><span class="sxs-lookup"><span data-stu-id="b3c65-129">**Count**</span></span> <br/> |<span data-ttu-id="b3c65-130">ulong</span><span class="sxs-lookup"><span data-stu-id="b3c65-130">ulong</span></span>  <br/> |<span data-ttu-id="b3c65-131">Получает число объектов **Window** в **Windows** наборе.</span><span class="sxs-lookup"><span data-stu-id="b3c65-131">Gets the number of **Window** objects in the **Windows** set.</span></span>  <br/> |
|<span data-ttu-id="b3c65-132">**CurrentWindow**</span><span class="sxs-lookup"><span data-stu-id="b3c65-132">**CurrentWindow**</span></span> <br/> |<span data-ttu-id="b3c65-133">**Window**</span><span class="sxs-lookup"><span data-stu-id="b3c65-133">**Window**</span></span> <br/> |<span data-ttu-id="b3c65-134">Получает **объект Window** в окне active OneNote.</span><span class="sxs-lookup"><span data-stu-id="b3c65-134">Gets the **Window** object of the active OneNote window.</span></span>  <br/> |
|<span data-ttu-id="b3c65-135">**Items**</span><span class="sxs-lookup"><span data-stu-id="b3c65-135">**Items**</span></span> <br/> |<span data-ttu-id="b3c65-136">**Window**</span><span class="sxs-lookup"><span data-stu-id="b3c65-136">**Window**</span></span> <br/> |<span data-ttu-id="b3c65-137">Возвращает объект **Window,** соответствующий пройденным значениям индекса.</span><span class="sxs-lookup"><span data-stu-id="b3c65-137">Returns the **Window** object that corresponds to the index value passed.</span></span> <span data-ttu-id="b3c65-138">Это свойство не может быть напрямую доступны.</span><span class="sxs-lookup"><span data-stu-id="b3c65-138">This property cannot be accessed directly.</span></span> <span data-ttu-id="b3c65-139">Чтобы вернуть **объект Window,** **Windows [(uint) index].**</span><span class="sxs-lookup"><span data-stu-id="b3c65-139">To return a **Window** object, use **Windows [(uint) index]**.</span></span>  <br/> |
   
### <a name="window-interface"></a><span data-ttu-id="b3c65-140">Интерфейс окна</span><span class="sxs-lookup"><span data-stu-id="b3c65-140">Window interface</span></span>

<span data-ttu-id="b3c65-141">Интерфейс **Window** позволяет пользователю получать доступ к определенным свойствам каждого окна.</span><span class="sxs-lookup"><span data-stu-id="b3c65-141">The **Window** interface allows the user to access certain properties of each window.</span></span> <span data-ttu-id="b3c65-142">К OneNote окна можно получить доступ путем Windows **свойства** класса **Application.**</span><span class="sxs-lookup"><span data-stu-id="b3c65-142">Each OneNote window can be accessed by enumerating through the **Windows** property of the **Application** class.</span></span> 
  
<span data-ttu-id="b3c65-143">**Свойства**</span><span class="sxs-lookup"><span data-stu-id="b3c65-143">**Properties**</span></span>

|<span data-ttu-id="b3c65-144">**Имя**</span><span class="sxs-lookup"><span data-stu-id="b3c65-144">**Name**</span></span>|<span data-ttu-id="b3c65-145">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b3c65-145">**Type**</span></span>|<span data-ttu-id="b3c65-146">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b3c65-146">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b3c65-147">**Active**</span><span class="sxs-lookup"><span data-stu-id="b3c65-147">**Active**</span></span> <br/> |<span data-ttu-id="b3c65-148">bool</span><span class="sxs-lookup"><span data-stu-id="b3c65-148">bool</span></span>  <br/> |<span data-ttu-id="b3c65-149">Получает или задает значение, которое указывает, является ли окно активным OneNote окном.</span><span class="sxs-lookup"><span data-stu-id="b3c65-149">Gets or sets a value that indicates whether the window is the active OneNote window.</span></span>  <br/> |
|<span data-ttu-id="b3c65-150">**Application**</span><span class="sxs-lookup"><span data-stu-id="b3c65-150">**Application**</span></span> <br/> |<span data-ttu-id="b3c65-151">**Application**</span><span class="sxs-lookup"><span data-stu-id="b3c65-151">**Application**</span></span> <br/> |<span data-ttu-id="b3c65-152">Получает объект OneNote **приложения,** связанный с окном.</span><span class="sxs-lookup"><span data-stu-id="b3c65-152">Gets the OneNote **Application** object that is associated with the window.</span></span>  <br/> |
|<span data-ttu-id="b3c65-153">**CurrentPageId**</span><span class="sxs-lookup"><span data-stu-id="b3c65-153">**CurrentPageId**</span></span> <br/> |<span data-ttu-id="b3c65-154">string</span><span class="sxs-lookup"><span data-stu-id="b3c65-154">string</span></span>  <br/> |<span data-ttu-id="b3c65-155">Получает объектный ID активной OneNote страницы окна.</span><span class="sxs-lookup"><span data-stu-id="b3c65-155">Gets the object ID of the active OneNote page of the window.</span></span>  <br/> |
|<span data-ttu-id="b3c65-156">**CurrentSectionId**</span><span class="sxs-lookup"><span data-stu-id="b3c65-156">**CurrentSectionId**</span></span> <br/> |<span data-ttu-id="b3c65-157">string</span><span class="sxs-lookup"><span data-stu-id="b3c65-157">string</span></span>  <br/> |<span data-ttu-id="b3c65-158">Получает объектный ID активного OneNote окна.</span><span class="sxs-lookup"><span data-stu-id="b3c65-158">Gets the object ID of the active OneNote section of the window.</span></span>  <br/> |
|<span data-ttu-id="b3c65-159">**CurrentSectionGroupId**</span><span class="sxs-lookup"><span data-stu-id="b3c65-159">**CurrentSectionGroupId**</span></span> <br/> |<span data-ttu-id="b3c65-160">string</span><span class="sxs-lookup"><span data-stu-id="b3c65-160">string</span></span>  <br/> |<span data-ttu-id="b3c65-161">Получает объектный ID активной OneNote группы раздела окна.</span><span class="sxs-lookup"><span data-stu-id="b3c65-161">Gets the object ID of the active OneNote section group of the window.</span></span>  <br/> |
|<span data-ttu-id="b3c65-162">**CurrentNotebookId**</span><span class="sxs-lookup"><span data-stu-id="b3c65-162">**CurrentNotebookId**</span></span> <br/> |<span data-ttu-id="b3c65-163">string</span><span class="sxs-lookup"><span data-stu-id="b3c65-163">string</span></span>  <br/> |<span data-ttu-id="b3c65-164">Получает объектный ID активного OneNote записной книжки окна.</span><span class="sxs-lookup"><span data-stu-id="b3c65-164">Gets the object ID of the active OneNote notebook of the window.</span></span>  <br/> |
|<span data-ttu-id="b3c65-165">**DockedLocation**</span><span class="sxs-lookup"><span data-stu-id="b3c65-165">**DockedLocation**</span></span> <br/> |<span data-ttu-id="b3c65-166">**DockedLocation**</span><span class="sxs-lookup"><span data-stu-id="b3c65-166">**DockedLocation**</span></span> <br/> |<span data-ttu-id="b3c65-167">Получает или задает пристыкованное расположение окна OneNote.</span><span class="sxs-lookup"><span data-stu-id="b3c65-167">Gets or sets the docked location of the OneNote window.</span></span>  <br/> |
|<span data-ttu-id="b3c65-168">**FullPageView**</span><span class="sxs-lookup"><span data-stu-id="b3c65-168">**FullPageView**</span></span> <br/> |<span data-ttu-id="b3c65-169">bool</span><span class="sxs-lookup"><span data-stu-id="b3c65-169">bool</span></span>  <br/> |<span data-ttu-id="b3c65-170">Получает или задает значение, которое указывает, находится ли окно в представлении full Page (минимальное представление пользовательского интерфейса).</span><span class="sxs-lookup"><span data-stu-id="b3c65-170">Gets or sets a value that indicates whether the window is in Full Page view (minimal UI view).</span></span>  <br/> |
|<span data-ttu-id="b3c65-171">**SideNote**</span><span class="sxs-lookup"><span data-stu-id="b3c65-171">**SideNote**</span></span> <br/> |<span data-ttu-id="b3c65-172">bool</span><span class="sxs-lookup"><span data-stu-id="b3c65-172">bool</span></span>  <br/> |<span data-ttu-id="b3c65-173">Получает или задает значение, которое указывает, является ли окно окном быстрой заметки.</span><span class="sxs-lookup"><span data-stu-id="b3c65-173">Gets or sets a value that indicates whether the window is a quick note window.</span></span>  <br/> |
|<span data-ttu-id="b3c65-174">**WindowHandle**</span><span class="sxs-lookup"><span data-stu-id="b3c65-174">**WindowHandle**</span></span> <br/> |<span data-ttu-id="b3c65-175">ulong</span><span class="sxs-lookup"><span data-stu-id="b3c65-175">ulong</span></span>  <br/> |<span data-ttu-id="b3c65-176">Получает ID ручки окна OneNote.</span><span class="sxs-lookup"><span data-stu-id="b3c65-176">Gets the handle ID of the OneNote window.</span></span>  <br/> |
   
<span data-ttu-id="b3c65-177">**Методы**</span><span class="sxs-lookup"><span data-stu-id="b3c65-177">**Methods**</span></span>
  
<span data-ttu-id="b3c65-178">Вы можете использовать следующие методы интерфейса **Window** для навигации по указанным объектам в окне OneNote или к указанным URL-адресам.</span><span class="sxs-lookup"><span data-stu-id="b3c65-178">You can use the following methods of the **Window** interface to navigate to specified objects in the OneNote window or to specified URLs.</span></span> 
  
<span data-ttu-id="b3c65-179">**NavigateTo**</span><span class="sxs-lookup"><span data-stu-id="b3c65-179">**NavigateTo**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b3c65-180">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b3c65-180">**Description**</span></span> <br/> |<span data-ttu-id="b3c65-181">Переходит к указанному объекту в OneNote окне.</span><span class="sxs-lookup"><span data-stu-id="b3c65-181">Navigates to the specified object in the OneNote window.</span></span> <span data-ttu-id="b3c65-182">Например, можно перейти к разделам, страницам и элементам набросков на страницах.</span><span class="sxs-lookup"><span data-stu-id="b3c65-182">For example, you can navigate to sections, pages, and outline elements within pages.</span></span>  <br/> |
|<span data-ttu-id="b3c65-183">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="b3c65-183">**Syntax**</span></span> <br/> | <span data-ttu-id="b3c65-184">`HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); `</span><span class="sxs-lookup"><span data-stu-id="b3c65-184">`HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); `</span></span> <br/> |
|<span data-ttu-id="b3c65-185">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="b3c65-185">**Parameters**</span></span> <br/> | <span data-ttu-id="b3c65-186">_bstrHierarchyObjectID_— иерархия OneNote ИД объекта, на который необходимо ориентироваться.</span><span class="sxs-lookup"><span data-stu-id="b3c65-186">_bstrHierarchyObjectID_—The hierarchy OneNote ID of the object you want to navigate to.</span></span> <span data-ttu-id="b3c65-187">ID объекта может ссылаться на OneNote, раздел, группу разделов или страницу.</span><span class="sxs-lookup"><span data-stu-id="b3c65-187">The object ID can reference a OneNote notebook, section, section group, or page.</span></span>  <br/>  <span data-ttu-id="b3c65-188">_bstrObjectID_— OneNote ID определенного объекта для перемещения в OneNote странице.</span><span class="sxs-lookup"><span data-stu-id="b3c65-188">_bstrObjectID_—The OneNote ID of the specific object to navigate to within a OneNote page.</span></span> <span data-ttu-id="b3c65-189">Если пользователь не хочет переходить к определенному объекту на странице, этот параметр задан как null.</span><span class="sxs-lookup"><span data-stu-id="b3c65-189">If the user does not want to navigate to a specific object on a page, this parameter is set to null.</span></span>  <br/> |
   
<span data-ttu-id="b3c65-190">**NavigateToUrl**</span><span class="sxs-lookup"><span data-stu-id="b3c65-190">**NavigateToUrl**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b3c65-191">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b3c65-191">**Description**</span></span> <br/> |<span data-ttu-id="b3c65-192">Если передана ссылка OneNote (onenote://), откроется окно OneNote для соответствующего расположения в OneNote.</span><span class="sxs-lookup"><span data-stu-id="b3c65-192">If passed a OneNote link (onenote://), opens the OneNote window to the corresponding location in OneNote.</span></span> <span data-ttu-id="b3c65-193">Однако если ссылка является внешней ссылкой, например https:// или file://, появится диалоговое окно безопасности.</span><span class="sxs-lookup"><span data-stu-id="b3c65-193">However, if the link is an external link, such as https:// or file://, a security dialog box will appear.</span></span> <span data-ttu-id="b3c65-194">После увольнения OneNote открыть ссылку и возвращается ошибка HResult.hrObjectDoesNotExist.</span><span class="sxs-lookup"><span data-stu-id="b3c65-194">Upon dismissal, OneNote attempts to open up the link and an HResult.hrObjectDoesNotExist error is returned.</span></span>  <br/> |
|<span data-ttu-id="b3c65-195">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="b3c65-195">**Syntax**</span></span> <br/> | <span data-ttu-id="b3c65-196">`HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); `</span><span class="sxs-lookup"><span data-stu-id="b3c65-196">`HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); `</span></span> <br/> |
|<span data-ttu-id="b3c65-197">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="b3c65-197">**Parameters**</span></span> <br/> | <span data-ttu-id="b3c65-198">_bstrUrl_— URL-адрес для навигации.</span><span class="sxs-lookup"><span data-stu-id="b3c65-198">_bstrUrl_—The URL to navigate to.</span></span>  <br/> |
   
<span data-ttu-id="b3c65-199">**SetDockedLocation**</span><span class="sxs-lookup"><span data-stu-id="b3c65-199">**SetDockedLocation**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b3c65-200">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b3c65-200">**Description**</span></span> <br/> |<span data-ttu-id="b3c65-201">Пристыковает окно к расположению, указанному **в dockLocation** и монитору **в ptMonitor.**</span><span class="sxs-lookup"><span data-stu-id="b3c65-201">Docks the window to the location specified by **dockLocation** and the monitor at **ptMonitor**.</span></span>  <br/> |
|<span data-ttu-id="b3c65-202">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="b3c65-202">**Syntax**</span></span> <br/> | <span data-ttu-id="b3c65-203">`HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);`</span><span class="sxs-lookup"><span data-stu-id="b3c65-203">`HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);`</span></span> <br/> |
|<span data-ttu-id="b3c65-204">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="b3c65-204">**Parameters**</span></span> <br/> | <span data-ttu-id="b3c65-205">_dockLocation_ — указывает пристыкованное расположение окна OneNote 2013 года.</span><span class="sxs-lookup"><span data-stu-id="b3c65-205">_dockLocation_ - Indicates the docked location of a OneNote 2013 window.</span></span>  <br/>  <span data-ttu-id="b3c65-206">_ptMonitor_ — (необязательный) указывает в x,y координирует, к которому следует пристыковать окно.</span><span class="sxs-lookup"><span data-stu-id="b3c65-206">_ptMonitor_ - (Optional) Indicates in x,y co-ordinates which monitor the window should be docked to.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="b3c65-207">Пример</span><span class="sxs-lookup"><span data-stu-id="b3c65-207">Example</span></span>

<span data-ttu-id="b3c65-208">Следующий код итерирует через OneNote, чтобы найти пристыкованное окно.</span><span class="sxs-lookup"><span data-stu-id="b3c65-208">The following code iterates through the OneNote windows to find a docked window.</span></span> <span data-ttu-id="b3c65-209">Если не существует пристыкованного окна, в примере пристыковано активное окно.</span><span class="sxs-lookup"><span data-stu-id="b3c65-209">If no docked window exists, the example docks the active window.</span></span> <span data-ttu-id="b3c65-210">Если нет активного окна, код создает новое пристыкованное окно.</span><span class="sxs-lookup"><span data-stu-id="b3c65-210">If no active window exists, the code creates a new docked window.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="b3c65-211">См. также</span><span class="sxs-lookup"><span data-stu-id="b3c65-211">See also</span></span>

- [<span data-ttu-id="b3c65-212">Справочник разработчика для OneNote</span><span class="sxs-lookup"><span data-stu-id="b3c65-212">OneNote developer reference</span></span>](onenote-developer-reference.md)

