---
title: Окно интерфейсы (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e6900ad7-c147-4816-93a9-5773170b115a
description: Интерфейсы Window и Windows — API-интерфейса OneNote 2013 объекты, позволяющий пользователям для работы с OneNote windows. Эти объекты позволяют пользователям нумерации внутри набора OneNote windows и изменении окно свойств.
ms.openlocfilehash: efc34312def588ecff54c63b3db84f8bf909352b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399951"
---
# <a name="window-interfaces-onenote"></a><span data-ttu-id="836b5-104">Окно интерфейсы (OneNote)</span><span class="sxs-lookup"><span data-stu-id="836b5-104">Window interfaces (OneNote)</span></span>

<span data-ttu-id="836b5-105">Интерфейсы **Window** и **Windows** — API-интерфейса OneNote 2013 объекты, позволяющий пользователям для работы с OneNote windows.</span><span class="sxs-lookup"><span data-stu-id="836b5-105">The **Window** and **Windows** interfaces are OneNote 2013 API objects that enables users to work with OneNote windows.</span></span> <span data-ttu-id="836b5-106">Эти объекты позволяют пользователям нумерации внутри набора OneNote windows и изменении окно свойств.</span><span class="sxs-lookup"><span data-stu-id="836b5-106">These objects allow users to enumerate through the set of OneNote windows and modify certain window properties.</span></span> 
  
## <a name="onenote-window-views"></a><span data-ttu-id="836b5-107">Представления окна OneNote</span><span class="sxs-lookup"><span data-stu-id="836b5-107">OneNote window views</span></span>

<span data-ttu-id="836b5-108">В следующем списке приведены режимы четыре представления, которые можно использовать для OneNote windows:</span><span class="sxs-lookup"><span data-stu-id="836b5-108">The following list shows the four view modes that you can use for OneNote windows:</span></span> 
  
- <span data-ttu-id="836b5-109">Стандартное представление — отображает окно OneNote по умолчанию, в котором отображаются области переходов записной книжки и страницы.</span><span class="sxs-lookup"><span data-stu-id="836b5-109">Normal view—Displays the default OneNote window in which the Notebook and Page navigation panes are visible.</span></span>
    
- <span data-ttu-id="836b5-110">Полный просмотр страницы — отображает минимальной пользовательского интерфейса (UI) Просмотр в котором области записной книжки и страницы, не отображаются.</span><span class="sxs-lookup"><span data-stu-id="836b5-110">Full Page view—Displays a minimal user-interface (UI) view in which the Notebook and Page panes are not displayed.</span></span>
    
- <span data-ttu-id="836b5-111">Небольшое примечание — отображает небольшое окно, которое позволяет пользователям короткий заметок.</span><span class="sxs-lookup"><span data-stu-id="836b5-111">Quick note—Displays a small window that allows users to take short notes.</span></span> <span data-ttu-id="836b5-112">Краткие заметки обычно будет доступ через значок OneNote в области уведомлений Windows, но вы также можете открыть их на вкладке **Вид** в OneNote.</span><span class="sxs-lookup"><span data-stu-id="836b5-112">You would usually access quick notes through the OneNote icon in the Windows notification area, but you can also access them through the **View** tab in OneNote.</span></span> 
    
- <span data-ttu-id="836b5-113">Прикрепить к рабочему столу — отображает окно OneNote, можно закрепить в любой части рабочего стола (аналогично панели задач).</span><span class="sxs-lookup"><span data-stu-id="836b5-113">Dock to Desktop—Displays a OneNote window that you can dock to any side of the desktop (similar to the taskbar).</span></span> <span data-ttu-id="836b5-114">В этом представлении уменьшает размер рабочего стола в окно.</span><span class="sxs-lookup"><span data-stu-id="836b5-114">This view reduces the size of the desktop to fit the window.</span></span> <span data-ttu-id="836b5-115">Только одно окно можно закрепить в любое время и окна всегда видна без блокировки рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="836b5-115">You can dock only one window at any time, and the window is always visible without blocking the desktop.</span></span> 
    
<span data-ttu-id="836b5-116">На следующем рисунке показаны какие целую страницу представления, закрепления в режим просмотра и памятки иметь вид на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="836b5-116">The following figure shows what the Full Page view, Dock to Desktop view, and quick notes look like on your desktop.</span></span>
  
<span data-ttu-id="836b5-117">**Представления OneNote**</span><span class="sxs-lookup"><span data-stu-id="836b5-117">**OneNote views**</span></span>

<span data-ttu-id="836b5-118">![Представления окна OneNote] (media/ON15Con_views.jpg "Представления окна OneNote")</span><span class="sxs-lookup"><span data-stu-id="836b5-118">![OneNote window views](media/ON15Con_views.jpg "OneNote window views")</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="836b5-119">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="836b5-119">Interfaces</span></span>

<span data-ttu-id="836b5-120">В этом разделе перечислены интерфейсы и члены, которые можно использовать для изменения OneNote windows программными средствами.</span><span class="sxs-lookup"><span data-stu-id="836b5-120">This section lists the interfaces and members that you can use to modify OneNote windows programmatically.</span></span>
  
### <a name="windows-interface"></a><span data-ttu-id="836b5-121">Интерфейс Windows</span><span class="sxs-lookup"><span data-stu-id="836b5-121">Windows interface</span></span>

<span data-ttu-id="836b5-122">Интерфейс **Windows** позволяет пользователям получать доступ к набор открытых окнах OneNote.</span><span class="sxs-lookup"><span data-stu-id="836b5-122">The **Windows** interface allows the user to access the set of opened OneNote windows.</span></span> <span data-ttu-id="836b5-123">Это свойство класса OneNote **приложения** , доступ к через **Application.Windows**.</span><span class="sxs-lookup"><span data-stu-id="836b5-123">It is a property of the OneNote **Application** class, accessed through **Application.Windows**.</span></span> <span data-ttu-id="836b5-124">При этом будет получен перечисляемые набор OneNote windows.</span><span class="sxs-lookup"><span data-stu-id="836b5-124">This returns the enumerated set of OneNote windows.</span></span> 
  
<span data-ttu-id="836b5-125">**Свойства**</span><span class="sxs-lookup"><span data-stu-id="836b5-125">**Properties**</span></span>

|<span data-ttu-id="836b5-126">**Имя**</span><span class="sxs-lookup"><span data-stu-id="836b5-126">**Name**</span></span>|<span data-ttu-id="836b5-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="836b5-127">**Type**</span></span>|<span data-ttu-id="836b5-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="836b5-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="836b5-129">**Count**</span><span class="sxs-lookup"><span data-stu-id="836b5-129">**Count**</span></span> <br/> |<span data-ttu-id="836b5-130">ulong</span><span class="sxs-lookup"><span data-stu-id="836b5-130">ulong</span></span>  <br/> |<span data-ttu-id="836b5-131">Возвращает количество объектов **Window** в наборе **Windows** .</span><span class="sxs-lookup"><span data-stu-id="836b5-131">Gets the number of **Window** objects in the **Windows** set.</span></span>  <br/> |
|<span data-ttu-id="836b5-132">**CurrentWindow**</span><span class="sxs-lookup"><span data-stu-id="836b5-132">**CurrentWindow**</span></span> <br/> |<span data-ttu-id="836b5-133">**Window**</span><span class="sxs-lookup"><span data-stu-id="836b5-133">**Window**</span></span> <br/> |<span data-ttu-id="836b5-134">Возвращает объект **Window** активного окна OneNote.</span><span class="sxs-lookup"><span data-stu-id="836b5-134">Gets the **Window** object of the active OneNote window.</span></span>  <br/> |
|<span data-ttu-id="836b5-135">**Items**</span><span class="sxs-lookup"><span data-stu-id="836b5-135">**Items**</span></span> <br/> |<span data-ttu-id="836b5-136">**Window**</span><span class="sxs-lookup"><span data-stu-id="836b5-136">**Window**</span></span> <br/> |<span data-ttu-id="836b5-137">Возвращает объект **Window** , соответствующий переданное значение индекса.</span><span class="sxs-lookup"><span data-stu-id="836b5-137">Returns the **Window** object that corresponds to the index value passed.</span></span> <span data-ttu-id="836b5-138">Это свойство не может осуществляться непосредственно.</span><span class="sxs-lookup"><span data-stu-id="836b5-138">This property cannot be accessed directly.</span></span> <span data-ttu-id="836b5-139">Чтобы вернуть объект **Window** , используйте **Windows [(uint) index]**.</span><span class="sxs-lookup"><span data-stu-id="836b5-139">To return a **Window** object, use **Windows [(uint) index]**.</span></span>  <br/> |
   
### <a name="window-interface"></a><span data-ttu-id="836b5-140">Интерфейс окна</span><span class="sxs-lookup"><span data-stu-id="836b5-140">Window interface</span></span>

<span data-ttu-id="836b5-141">Интерфейс **окна** позволяет пользователям получать доступ к определенных свойств каждого окна.</span><span class="sxs-lookup"><span data-stu-id="836b5-141">The **Window** interface allows the user to access certain properties of each window.</span></span> <span data-ttu-id="836b5-142">Каждое окно OneNote осуществляется путем перечисления через свойство **Windows** класса **приложения** .</span><span class="sxs-lookup"><span data-stu-id="836b5-142">Each OneNote window can be accessed by enumerating through the **Windows** property of the **Application** class.</span></span> 
  
<span data-ttu-id="836b5-143">**Свойства**</span><span class="sxs-lookup"><span data-stu-id="836b5-143">**Properties**</span></span>

|<span data-ttu-id="836b5-144">**Имя**</span><span class="sxs-lookup"><span data-stu-id="836b5-144">**Name**</span></span>|<span data-ttu-id="836b5-145">**Тип**</span><span class="sxs-lookup"><span data-stu-id="836b5-145">**Type**</span></span>|<span data-ttu-id="836b5-146">**Описание**</span><span class="sxs-lookup"><span data-stu-id="836b5-146">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="836b5-147">**Active**</span><span class="sxs-lookup"><span data-stu-id="836b5-147">**Active**</span></span> <br/> |<span data-ttu-id="836b5-148">bool</span><span class="sxs-lookup"><span data-stu-id="836b5-148">bool</span></span>  <br/> |<span data-ttu-id="836b5-149">Получает или задает значение, указывающее, является ли окно активным окном OneNote.</span><span class="sxs-lookup"><span data-stu-id="836b5-149">Gets or sets a value that indicates whether the window is the active OneNote window.</span></span>  <br/> |
|<span data-ttu-id="836b5-150">**Приложение**</span><span class="sxs-lookup"><span data-stu-id="836b5-150">**Application**</span></span> <br/> |<span data-ttu-id="836b5-151">**Приложение**</span><span class="sxs-lookup"><span data-stu-id="836b5-151">**Application**</span></span> <br/> |<span data-ttu-id="836b5-152">Получает объект OneNote **приложения** , связанный с окном.</span><span class="sxs-lookup"><span data-stu-id="836b5-152">Gets the OneNote **Application** object that is associated with the window.</span></span>  <br/> |
|<span data-ttu-id="836b5-153">**CurrentPageId**</span><span class="sxs-lookup"><span data-stu-id="836b5-153">**CurrentPageId**</span></span> <br/> |<span data-ttu-id="836b5-154">string</span><span class="sxs-lookup"><span data-stu-id="836b5-154">string</span></span>  <br/> |<span data-ttu-id="836b5-155">Получает идентификатор объекта активную страницу OneNote окна.</span><span class="sxs-lookup"><span data-stu-id="836b5-155">Gets the object ID of the active OneNote page of the window.</span></span>  <br/> |
|<span data-ttu-id="836b5-156">**CurrentSectionId**</span><span class="sxs-lookup"><span data-stu-id="836b5-156">**CurrentSectionId**</span></span> <br/> |<span data-ttu-id="836b5-157">string</span><span class="sxs-lookup"><span data-stu-id="836b5-157">string</span></span>  <br/> |<span data-ttu-id="836b5-158">Получает идентификатор объекта разделе OneNote активного окна.</span><span class="sxs-lookup"><span data-stu-id="836b5-158">Gets the object ID of the active OneNote section of the window.</span></span>  <br/> |
|<span data-ttu-id="836b5-159">**CurrentSectionGroupId**</span><span class="sxs-lookup"><span data-stu-id="836b5-159">**CurrentSectionGroupId**</span></span> <br/> |<span data-ttu-id="836b5-160">string</span><span class="sxs-lookup"><span data-stu-id="836b5-160">string</span></span>  <br/> |<span data-ttu-id="836b5-161">Получает идентификатор объекта группы active OneNote раздела окна.</span><span class="sxs-lookup"><span data-stu-id="836b5-161">Gets the object ID of the active OneNote section group of the window.</span></span>  <br/> |
|<span data-ttu-id="836b5-162">**CurrentNotebookId**</span><span class="sxs-lookup"><span data-stu-id="836b5-162">**CurrentNotebookId**</span></span> <br/> |<span data-ttu-id="836b5-163">string</span><span class="sxs-lookup"><span data-stu-id="836b5-163">string</span></span>  <br/> |<span data-ttu-id="836b5-164">Получает идентификатор объекта active записной книжки OneNote окна.</span><span class="sxs-lookup"><span data-stu-id="836b5-164">Gets the object ID of the active OneNote notebook of the window.</span></span>  <br/> |
|<span data-ttu-id="836b5-165">**DockedLocation**</span><span class="sxs-lookup"><span data-stu-id="836b5-165">**DockedLocation**</span></span> <br/> |<span data-ttu-id="836b5-166">**DockedLocation**</span><span class="sxs-lookup"><span data-stu-id="836b5-166">**DockedLocation**</span></span> <br/> |<span data-ttu-id="836b5-167">Получает или задает расположение закрепленного окна OneNote.</span><span class="sxs-lookup"><span data-stu-id="836b5-167">Gets or sets the docked location of the OneNote window.</span></span>  <br/> |
|<span data-ttu-id="836b5-168">**FullPageView**</span><span class="sxs-lookup"><span data-stu-id="836b5-168">**FullPageView**</span></span> <br/> |<span data-ttu-id="836b5-169">bool</span><span class="sxs-lookup"><span data-stu-id="836b5-169">bool</span></span>  <br/> |<span data-ttu-id="836b5-170">Получает или задает значение, указывающее, является ли окно в режиме полного страницы (Минимальная представление пользовательского интерфейса).</span><span class="sxs-lookup"><span data-stu-id="836b5-170">Gets or sets a value that indicates whether the window is in Full Page view (minimal UI view).</span></span>  <br/> |
|<span data-ttu-id="836b5-171">**SideNote**</span><span class="sxs-lookup"><span data-stu-id="836b5-171">**SideNote**</span></span> <br/> |<span data-ttu-id="836b5-172">bool</span><span class="sxs-lookup"><span data-stu-id="836b5-172">bool</span></span>  <br/> |<span data-ttu-id="836b5-173">Получает или задает значение, указывающее, является ли окно окном небольшое примечание.</span><span class="sxs-lookup"><span data-stu-id="836b5-173">Gets or sets a value that indicates whether the window is a quick note window.</span></span>  <br/> |
|<span data-ttu-id="836b5-174">**WindowHandle**</span><span class="sxs-lookup"><span data-stu-id="836b5-174">**WindowHandle**</span></span> <br/> |<span data-ttu-id="836b5-175">ulong</span><span class="sxs-lookup"><span data-stu-id="836b5-175">ulong</span></span>  <br/> |<span data-ttu-id="836b5-176">Получает идентификатор дескриптор окна OneNote.</span><span class="sxs-lookup"><span data-stu-id="836b5-176">Gets the handle ID of the OneNote window.</span></span>  <br/> |
   
<span data-ttu-id="836b5-177">**Методы**</span><span class="sxs-lookup"><span data-stu-id="836b5-177">**Methods**</span></span>
  
<span data-ttu-id="836b5-178">Можно использовать следующие методы интерфейса **окна** для перехода для указанных объектов в окне OneNote или для указанного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="836b5-178">You can use the following methods of the **Window** interface to navigate to specified objects in the OneNote window or to specified URLs.</span></span> 
  
<span data-ttu-id="836b5-179">**NavigateTo**</span><span class="sxs-lookup"><span data-stu-id="836b5-179">**NavigateTo**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="836b5-180">**Описание**</span><span class="sxs-lookup"><span data-stu-id="836b5-180">**Description**</span></span> <br/> |<span data-ttu-id="836b5-181">Переход на указанный объект в окне OneNote.</span><span class="sxs-lookup"><span data-stu-id="836b5-181">Navigates to the specified object in the OneNote window.</span></span> <span data-ttu-id="836b5-182">Например можно перейти к разделов, страницы и элементы структуры в пределах страницы.</span><span class="sxs-lookup"><span data-stu-id="836b5-182">For example, you can navigate to sections, pages, and outline elements within pages.</span></span>  <br/> |
|<span data-ttu-id="836b5-183">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="836b5-183">**Syntax**</span></span> <br/> | <span data-ttu-id="836b5-184">`HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); `</span><span class="sxs-lookup"><span data-stu-id="836b5-184"></span></span> <br/> |
|<span data-ttu-id="836b5-185">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="836b5-185">**Parameters**</span></span> <br/> | <span data-ttu-id="836b5-186">_bstrHierarchyObjectID_— OneNote идентификатор объекта, чтобы перейти к иерархии.</span><span class="sxs-lookup"><span data-stu-id="836b5-186">_bstrHierarchyObjectID_—The hierarchy OneNote ID of the object you want to navigate to.</span></span> <span data-ttu-id="836b5-187">Идентификатор объекта можно ссылаться записной книжки OneNote, раздел, раздел группы или страницы.</span><span class="sxs-lookup"><span data-stu-id="836b5-187">The object ID can reference a OneNote notebook, section, section group, or page.</span></span>  <br/>  <span data-ttu-id="836b5-188">_bstrObjectID_— OneNote идентификатор для конкретного объекта, чтобы перейти на странице OneNote.</span><span class="sxs-lookup"><span data-stu-id="836b5-188">_bstrObjectID_—The OneNote ID of the specific object to navigate to within a OneNote page.</span></span> <span data-ttu-id="836b5-189">Если пользователь не требуется переход к объекту, определенные на странице, этому параметру присвоено значение null.</span><span class="sxs-lookup"><span data-stu-id="836b5-189">If the user does not want to navigate to a specific object on a page, this parameter is set to null.</span></span>  <br/> |
   
<span data-ttu-id="836b5-190">**NavigateToUrl**</span><span class="sxs-lookup"><span data-stu-id="836b5-190">**NavigateToUrl**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="836b5-191">**Описание**</span><span class="sxs-lookup"><span data-stu-id="836b5-191">**Description**</span></span> <br/> |<span data-ttu-id="836b5-192">Если передается ссылка OneNote (onenote: / /), открывается окно OneNote в соответствующем расположении в OneNote.</span><span class="sxs-lookup"><span data-stu-id="836b5-192">If passed a OneNote link (onenote://), opens the OneNote window to the corresponding location in OneNote.</span></span> <span data-ttu-id="836b5-193">Тем не менее если ссылки внешних ссылок, такие как https:// или file://, появится диалоговое окно безопасности.</span><span class="sxs-lookup"><span data-stu-id="836b5-193">However, if the link is an external link, such as https:// or file://, a security dialog box will appear.</span></span> <span data-ttu-id="836b5-194">После увольнение OneNote пытается открыть ссылку и возвращается сообщение об ошибке HResult.hrObjectDoesNotExist.</span><span class="sxs-lookup"><span data-stu-id="836b5-194">Upon dismissal, OneNote attempts to open up the link and an HResult.hrObjectDoesNotExist error is returned.</span></span>  <br/> |
|<span data-ttu-id="836b5-195">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="836b5-195">**Syntax**</span></span> <br/> | <span data-ttu-id="836b5-196">`HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); `</span><span class="sxs-lookup"><span data-stu-id="836b5-196"></span></span> <br/> |
|<span data-ttu-id="836b5-197">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="836b5-197">**Parameters**</span></span> <br/> | <span data-ttu-id="836b5-198">_bstrUrl_— URL-адрес для перехода.</span><span class="sxs-lookup"><span data-stu-id="836b5-198">_bstrUrl_—The URL to navigate to.</span></span>  <br/> |
   
<span data-ttu-id="836b5-199">**SetDockedLocation**</span><span class="sxs-lookup"><span data-stu-id="836b5-199">**SetDockedLocation**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="836b5-200">**Описание**</span><span class="sxs-lookup"><span data-stu-id="836b5-200">**Description**</span></span> <br/> |<span data-ttu-id="836b5-201">Закрепляет окне местоположение, указанное для монитора на **ptMonitor**и **dockLocation** .</span><span class="sxs-lookup"><span data-stu-id="836b5-201">Docks the window to the location specified by **dockLocation** and the monitor at **ptMonitor**.</span></span>  <br/> |
|<span data-ttu-id="836b5-202">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="836b5-202">**Syntax**</span></span> <br/> | <span data-ttu-id="836b5-203">`HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);`</span><span class="sxs-lookup"><span data-stu-id="836b5-203"></span></span> <br/> |
|<span data-ttu-id="836b5-204">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="836b5-204">**Parameters**</span></span> <br/> | <span data-ttu-id="836b5-205">_dockLocation_ - указывает расположение закрепленного окна OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="836b5-205">_dockLocation_ - Indicates the docked location of a OneNote 2013 window.</span></span>  <br/>  <span data-ttu-id="836b5-206">_ptMonitor_ - указывает (необязательно) в x, y координаты отслеживающие окна следует закрепить.</span><span class="sxs-lookup"><span data-stu-id="836b5-206">_ptMonitor_ - (Optional) Indicates in x,y co-ordinates which monitor the window should be docked to.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="836b5-207">Пример</span><span class="sxs-lookup"><span data-stu-id="836b5-207">Example</span></span>

<span data-ttu-id="836b5-208">Приведенный ниже код перебирает windows OneNote, чтобы найти закрепленного окна.</span><span class="sxs-lookup"><span data-stu-id="836b5-208">The following code iterates through the OneNote windows to find a docked window.</span></span> <span data-ttu-id="836b5-209">Если нет закрепленного окна, пример закрепляет активного окна.</span><span class="sxs-lookup"><span data-stu-id="836b5-209">If no docked window exists, the example docks the active window.</span></span> <span data-ttu-id="836b5-210">Если нет активного окна, код создает новый закрепленного окна.</span><span class="sxs-lookup"><span data-stu-id="836b5-210">If no active window exists, the code creates a new docked window.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="836b5-211">См. также</span><span class="sxs-lookup"><span data-stu-id="836b5-211">See also</span></span>

- [<span data-ttu-id="836b5-212">Справочник разработчика для OneNote</span><span class="sxs-lookup"><span data-stu-id="836b5-212">OneNote developer reference</span></span>](onenote-developer-reference.md)

