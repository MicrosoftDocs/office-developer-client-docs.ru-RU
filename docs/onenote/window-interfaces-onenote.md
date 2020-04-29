---
title: Интерфейсы окон (OneNote)
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
# <a name="window-interfaces-onenote"></a><span data-ttu-id="079e9-104">Интерфейсы окон (OneNote)</span><span class="sxs-lookup"><span data-stu-id="079e9-104">Window interfaces (OneNote)</span></span>

<span data-ttu-id="079e9-105">Интерфейсы **Window** и **Windows** — это объекты API OneNote 2013, которые позволяют пользователям работать с окнами OneNote.</span><span class="sxs-lookup"><span data-stu-id="079e9-105">The **Window** and **Windows** interfaces are OneNote 2013 API objects that enables users to work with OneNote windows.</span></span> <span data-ttu-id="079e9-106">Эти объекты позволяют пользователям применять перечисление в наборе окон OneNote и изменять определенные свойства окон.</span><span class="sxs-lookup"><span data-stu-id="079e9-106">These objects allow users to enumerate through the set of OneNote windows and modify certain window properties.</span></span> 
  
## <a name="onenote-window-views"></a><span data-ttu-id="079e9-107">Представления окна OneNote</span><span class="sxs-lookup"><span data-stu-id="079e9-107">OneNote window views</span></span>

<span data-ttu-id="079e9-108">В следующем списке показаны четыре режима просмотра, которые можно использовать для Windows в Windows:</span><span class="sxs-lookup"><span data-stu-id="079e9-108">The following list shows the four view modes that you can use for OneNote windows:</span></span> 
  
- <span data-ttu-id="079e9-109">Обычное представление — отображает окно OneNote по умолчанию, в котором отображаются области навигации для записной книжки и страниц.</span><span class="sxs-lookup"><span data-stu-id="079e9-109">Normal view—Displays the default OneNote window in which the Notebook and Page navigation panes are visible.</span></span>
    
- <span data-ttu-id="079e9-110">Полное представление страницы — отображает минимальное представление пользовательского интерфейса, в котором записные книжки и области страниц не отображаются.</span><span class="sxs-lookup"><span data-stu-id="079e9-110">Full Page view—Displays a minimal user-interface (UI) view in which the Notebook and Page panes are not displayed.</span></span>
    
- <span data-ttu-id="079e9-111">Быстрая заметка — отображает небольшое окно, позволяющее пользователям делать короткие заметки.</span><span class="sxs-lookup"><span data-stu-id="079e9-111">Quick note—Displays a small window that allows users to take short notes.</span></span> <span data-ttu-id="079e9-112">Обычно вы можете получать доступ к быстрой заметкам с помощью значка OneNote в области уведомлений Windows, но вы также можете получить к ним доступ на вкладке **вид** в OneNote.</span><span class="sxs-lookup"><span data-stu-id="079e9-112">You would usually access quick notes through the OneNote icon in the Windows notification area, but you can also access them through the **View** tab in OneNote.</span></span> 
    
- <span data-ttu-id="079e9-113">Закрепить на рабочем столе — отображается окно OneNote, которое можно закрепить на любой стороне рабочего стола (аналогично панели задач).</span><span class="sxs-lookup"><span data-stu-id="079e9-113">Dock to Desktop—Displays a OneNote window that you can dock to any side of the desktop (similar to the taskbar).</span></span> <span data-ttu-id="079e9-114">Это представление уменьшает размер рабочего стола в соответствии с окном.</span><span class="sxs-lookup"><span data-stu-id="079e9-114">This view reduces the size of the desktop to fit the window.</span></span> <span data-ttu-id="079e9-115">Вы можете прикрепить только одно окно в любое время, и окно всегда отображается без блокировки рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="079e9-115">You can dock only one window at any time, and the window is always visible without blocking the desktop.</span></span> 
    
<span data-ttu-id="079e9-116">На следующем рисунке показано, что такое представление страницы, закрепление в режиме рабочего стола и быстрые заметки на настольном компьютере.</span><span class="sxs-lookup"><span data-stu-id="079e9-116">The following figure shows what the Full Page view, Dock to Desktop view, and quick notes look like on your desktop.</span></span>
  
<span data-ttu-id="079e9-117">**Представления OneNote**</span><span class="sxs-lookup"><span data-stu-id="079e9-117">**OneNote views**</span></span>

<span data-ttu-id="079e9-118">![OneNote window views](media/ON15Con_views.jpg "Представления окна") OneNote</span><span class="sxs-lookup"><span data-stu-id="079e9-118">![OneNote window views](media/ON15Con_views.jpg "OneNote window views")</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="079e9-119">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="079e9-119">Interfaces</span></span>

<span data-ttu-id="079e9-120">В этом разделе перечислены интерфейсы и члены, которые можно использовать для программного изменения OneNote.</span><span class="sxs-lookup"><span data-stu-id="079e9-120">This section lists the interfaces and members that you can use to modify OneNote windows programmatically.</span></span>
  
### <a name="windows-interface"></a><span data-ttu-id="079e9-121">Интерфейс Windows</span><span class="sxs-lookup"><span data-stu-id="079e9-121">Windows interface</span></span>

<span data-ttu-id="079e9-122">С помощью интерфейса **Windows** пользователь получает доступ к набору открытых окон OneNote.</span><span class="sxs-lookup"><span data-stu-id="079e9-122">The **Windows** interface allows the user to access the set of opened OneNote windows.</span></span> <span data-ttu-id="079e9-123">Это свойство класса **приложения** OneNote, доступ к которому осуществляется с помощью **Application. Windows**.</span><span class="sxs-lookup"><span data-stu-id="079e9-123">It is a property of the OneNote **Application** class, accessed through **Application.Windows**.</span></span> <span data-ttu-id="079e9-124">При этом возвращается перечисленный набор окон OneNote.</span><span class="sxs-lookup"><span data-stu-id="079e9-124">This returns the enumerated set of OneNote windows.</span></span> 
  
<span data-ttu-id="079e9-125">**Свойства**</span><span class="sxs-lookup"><span data-stu-id="079e9-125">**Properties**</span></span>

|<span data-ttu-id="079e9-126">**Имя**</span><span class="sxs-lookup"><span data-stu-id="079e9-126">**Name**</span></span>|<span data-ttu-id="079e9-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="079e9-127">**Type**</span></span>|<span data-ttu-id="079e9-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="079e9-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="079e9-129">**Count**</span><span class="sxs-lookup"><span data-stu-id="079e9-129">**Count**</span></span> <br/> |<span data-ttu-id="079e9-130">ulong</span><span class="sxs-lookup"><span data-stu-id="079e9-130">ulong</span></span>  <br/> |<span data-ttu-id="079e9-131">Получает число объектов **Window** в наборе **окон** .</span><span class="sxs-lookup"><span data-stu-id="079e9-131">Gets the number of **Window** objects in the **Windows** set.</span></span>  <br/> |
|<span data-ttu-id="079e9-132">**куррентвиндов**</span><span class="sxs-lookup"><span data-stu-id="079e9-132">**CurrentWindow**</span></span> <br/> |<span data-ttu-id="079e9-133">**Window**</span><span class="sxs-lookup"><span data-stu-id="079e9-133">**Window**</span></span> <br/> |<span data-ttu-id="079e9-134">Возвращает объект **окна** активного окна OneNote.</span><span class="sxs-lookup"><span data-stu-id="079e9-134">Gets the **Window** object of the active OneNote window.</span></span>  <br/> |
|<span data-ttu-id="079e9-135">**Items**</span><span class="sxs-lookup"><span data-stu-id="079e9-135">**Items**</span></span> <br/> |<span data-ttu-id="079e9-136">**Window**</span><span class="sxs-lookup"><span data-stu-id="079e9-136">**Window**</span></span> <br/> |<span data-ttu-id="079e9-137">Возвращает объект **Window** , соответствующий переданному значению индекса.</span><span class="sxs-lookup"><span data-stu-id="079e9-137">Returns the **Window** object that corresponds to the index value passed.</span></span> <span data-ttu-id="079e9-138">Доступ к этому свойству напрямую невозможен.</span><span class="sxs-lookup"><span data-stu-id="079e9-138">This property cannot be accessed directly.</span></span> <span data-ttu-id="079e9-139">Чтобы вернуть объект **Window** , используйте **Windows [(UINT) index]**.</span><span class="sxs-lookup"><span data-stu-id="079e9-139">To return a **Window** object, use **Windows [(uint) index]**.</span></span>  <br/> |
   
### <a name="window-interface"></a><span data-ttu-id="079e9-140">Интерфейс окна</span><span class="sxs-lookup"><span data-stu-id="079e9-140">Window interface</span></span>

<span data-ttu-id="079e9-141">Интерфейс **окна** позволяет пользователю получать доступ к определенным свойствам каждого окна.</span><span class="sxs-lookup"><span data-stu-id="079e9-141">The **Window** interface allows the user to access certain properties of each window.</span></span> <span data-ttu-id="079e9-142">Каждое окно OneNote можно получить, перечисляя с помощью свойства **Windows** класса **Application** .</span><span class="sxs-lookup"><span data-stu-id="079e9-142">Each OneNote window can be accessed by enumerating through the **Windows** property of the **Application** class.</span></span> 
  
<span data-ttu-id="079e9-143">**Свойства**</span><span class="sxs-lookup"><span data-stu-id="079e9-143">**Properties**</span></span>

|<span data-ttu-id="079e9-144">**Имя**</span><span class="sxs-lookup"><span data-stu-id="079e9-144">**Name**</span></span>|<span data-ttu-id="079e9-145">**Тип**</span><span class="sxs-lookup"><span data-stu-id="079e9-145">**Type**</span></span>|<span data-ttu-id="079e9-146">**Описание**</span><span class="sxs-lookup"><span data-stu-id="079e9-146">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="079e9-147">**Active**</span><span class="sxs-lookup"><span data-stu-id="079e9-147">**Active**</span></span> <br/> |<span data-ttu-id="079e9-148">логический</span><span class="sxs-lookup"><span data-stu-id="079e9-148">bool</span></span>  <br/> |<span data-ttu-id="079e9-149">Получает или задает значение, указывающее, является ли окно активным окном OneNote.</span><span class="sxs-lookup"><span data-stu-id="079e9-149">Gets or sets a value that indicates whether the window is the active OneNote window.</span></span>  <br/> |
|<span data-ttu-id="079e9-150">**Application**</span><span class="sxs-lookup"><span data-stu-id="079e9-150">**Application**</span></span> <br/> |<span data-ttu-id="079e9-151">**Application**</span><span class="sxs-lookup"><span data-stu-id="079e9-151">**Application**</span></span> <br/> |<span data-ttu-id="079e9-152">Получает объект **приложения** OneNote, связанный с окном.</span><span class="sxs-lookup"><span data-stu-id="079e9-152">Gets the OneNote **Application** object that is associated with the window.</span></span>  <br/> |
|<span data-ttu-id="079e9-153">**куррентпажеид**</span><span class="sxs-lookup"><span data-stu-id="079e9-153">**CurrentPageId**</span></span> <br/> |<span data-ttu-id="079e9-154">string</span><span class="sxs-lookup"><span data-stu-id="079e9-154">string</span></span>  <br/> |<span data-ttu-id="079e9-155">Получает идентификатор объекта активной страницы OneNote в окне.</span><span class="sxs-lookup"><span data-stu-id="079e9-155">Gets the object ID of the active OneNote page of the window.</span></span>  <br/> |
|<span data-ttu-id="079e9-156">**куррентсектионид**</span><span class="sxs-lookup"><span data-stu-id="079e9-156">**CurrentSectionId**</span></span> <br/> |<span data-ttu-id="079e9-157">string</span><span class="sxs-lookup"><span data-stu-id="079e9-157">string</span></span>  <br/> |<span data-ttu-id="079e9-158">Получает идентификатор объекта активного раздела OneNote в окне.</span><span class="sxs-lookup"><span data-stu-id="079e9-158">Gets the object ID of the active OneNote section of the window.</span></span>  <br/> |
|<span data-ttu-id="079e9-159">**куррентсектионграупид**</span><span class="sxs-lookup"><span data-stu-id="079e9-159">**CurrentSectionGroupId**</span></span> <br/> |<span data-ttu-id="079e9-160">string</span><span class="sxs-lookup"><span data-stu-id="079e9-160">string</span></span>  <br/> |<span data-ttu-id="079e9-161">Получает идентификатор объекта активной группы разделов OneNote в окне.</span><span class="sxs-lookup"><span data-stu-id="079e9-161">Gets the object ID of the active OneNote section group of the window.</span></span>  <br/> |
|<span data-ttu-id="079e9-162">**куррентнотебукид**</span><span class="sxs-lookup"><span data-stu-id="079e9-162">**CurrentNotebookId**</span></span> <br/> |<span data-ttu-id="079e9-163">string</span><span class="sxs-lookup"><span data-stu-id="079e9-163">string</span></span>  <br/> |<span data-ttu-id="079e9-164">Получает идентификатор активной записной книжки OneNote в окне.</span><span class="sxs-lookup"><span data-stu-id="079e9-164">Gets the object ID of the active OneNote notebook of the window.</span></span>  <br/> |
|<span data-ttu-id="079e9-165">**доккедлокатион**</span><span class="sxs-lookup"><span data-stu-id="079e9-165">**DockedLocation**</span></span> <br/> |<span data-ttu-id="079e9-166">**доккедлокатион**</span><span class="sxs-lookup"><span data-stu-id="079e9-166">**DockedLocation**</span></span> <br/> |<span data-ttu-id="079e9-167">Получает или задает закрепленное расположение окна OneNote.</span><span class="sxs-lookup"><span data-stu-id="079e9-167">Gets or sets the docked location of the OneNote window.</span></span>  <br/> |
|<span data-ttu-id="079e9-168">**фуллпажевиев**</span><span class="sxs-lookup"><span data-stu-id="079e9-168">**FullPageView**</span></span> <br/> |<span data-ttu-id="079e9-169">логический</span><span class="sxs-lookup"><span data-stu-id="079e9-169">bool</span></span>  <br/> |<span data-ttu-id="079e9-170">Получает или задает значение, указывающее, находится ли окно в режиме полного просмотра страницы (минимальное представление пользовательского интерфейса).</span><span class="sxs-lookup"><span data-stu-id="079e9-170">Gets or sets a value that indicates whether the window is in Full Page view (minimal UI view).</span></span>  <br/> |
|<span data-ttu-id="079e9-171">**сиденоте**</span><span class="sxs-lookup"><span data-stu-id="079e9-171">**SideNote**</span></span> <br/> |<span data-ttu-id="079e9-172">логический</span><span class="sxs-lookup"><span data-stu-id="079e9-172">bool</span></span>  <br/> |<span data-ttu-id="079e9-173">Получает или задает значение, указывающее, является ли окно окном с быстрой заметкой.</span><span class="sxs-lookup"><span data-stu-id="079e9-173">Gets or sets a value that indicates whether the window is a quick note window.</span></span>  <br/> |
|<span data-ttu-id="079e9-174">**виндовхандле**</span><span class="sxs-lookup"><span data-stu-id="079e9-174">**WindowHandle**</span></span> <br/> |<span data-ttu-id="079e9-175">ulong</span><span class="sxs-lookup"><span data-stu-id="079e9-175">ulong</span></span>  <br/> |<span data-ttu-id="079e9-176">Получает идентификатор дескриптора окна OneNote.</span><span class="sxs-lookup"><span data-stu-id="079e9-176">Gets the handle ID of the OneNote window.</span></span>  <br/> |
   
<span data-ttu-id="079e9-177">**Методы**</span><span class="sxs-lookup"><span data-stu-id="079e9-177">**Methods**</span></span>
  
<span data-ttu-id="079e9-178">С помощью следующих методов интерфейса **окна** можно переходить к указанным объектам в окне OneNote или по указанным URL-адресам.</span><span class="sxs-lookup"><span data-stu-id="079e9-178">You can use the following methods of the **Window** interface to navigate to specified objects in the OneNote window or to specified URLs.</span></span> 
  
<span data-ttu-id="079e9-179">**NavigateTo**</span><span class="sxs-lookup"><span data-stu-id="079e9-179">**NavigateTo**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="079e9-180">**Описание**</span><span class="sxs-lookup"><span data-stu-id="079e9-180">**Description**</span></span> <br/> |<span data-ttu-id="079e9-181">Переходит к указанному объекту в окне OneNote.</span><span class="sxs-lookup"><span data-stu-id="079e9-181">Navigates to the specified object in the OneNote window.</span></span> <span data-ttu-id="079e9-182">Например, вы можете перейти к разделам, страницам и элементам структуры на страницах.</span><span class="sxs-lookup"><span data-stu-id="079e9-182">For example, you can navigate to sections, pages, and outline elements within pages.</span></span>  <br/> |
|<span data-ttu-id="079e9-183">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="079e9-183">**Syntax**</span></span> <br/> | <span data-ttu-id="079e9-184">`HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); `</span><span class="sxs-lookup"><span data-stu-id="079e9-184">`HRESULT NavigateTo(`           ` [in]BSTR bstrHierarchyObjectID, `           ` [in]BSTR bstrObjectID); `</span></span> <br/> |
|<span data-ttu-id="079e9-185">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="079e9-185">**Parameters**</span></span> <br/> | <span data-ttu-id="079e9-186">_бстрхиерарчйобжектид_— идентификатор OneNote иерархии объекта, к которому необходимо перейти.</span><span class="sxs-lookup"><span data-stu-id="079e9-186">_bstrHierarchyObjectID_—The hierarchy OneNote ID of the object you want to navigate to.</span></span> <span data-ttu-id="079e9-187">Идентификатор объекта может ссылаться на записную книжку OneNote, раздел, группу разделов или страницу.</span><span class="sxs-lookup"><span data-stu-id="079e9-187">The object ID can reference a OneNote notebook, section, section group, or page.</span></span>  <br/>  <span data-ttu-id="079e9-188">_бстробжектид_— идентификатор OneNote для конкретного объекта, на который выполняется переход на странице OneNote.</span><span class="sxs-lookup"><span data-stu-id="079e9-188">_bstrObjectID_—The OneNote ID of the specific object to navigate to within a OneNote page.</span></span> <span data-ttu-id="079e9-189">Если пользователю не нужно переходить к определенному объекту на странице, этому параметру присвоено значение null.</span><span class="sxs-lookup"><span data-stu-id="079e9-189">If the user does not want to navigate to a specific object on a page, this parameter is set to null.</span></span>  <br/> |
   
<span data-ttu-id="079e9-190">**навигатетаурл**</span><span class="sxs-lookup"><span data-stu-id="079e9-190">**NavigateToUrl**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="079e9-191">**Описание**</span><span class="sxs-lookup"><span data-stu-id="079e9-191">**Description**</span></span> <br/> |<span data-ttu-id="079e9-192">Если передана ссылка OneNote (onenote://), откроется окно OneNote для соответствующего расположения в OneNote.</span><span class="sxs-lookup"><span data-stu-id="079e9-192">If passed a OneNote link (onenote://), opens the OneNote window to the corresponding location in OneNote.</span></span> <span data-ttu-id="079e9-193">Однако если ссылка является внешней ссылкой, такой как https://или file://, появится диалоговое окно безопасности.</span><span class="sxs-lookup"><span data-stu-id="079e9-193">However, if the link is an external link, such as https:// or file://, a security dialog box will appear.</span></span> <span data-ttu-id="079e9-194">После увольнения OneNote пытается открыть ссылку, и возвращается ошибка HResult. Хробжектдоеснотексист.</span><span class="sxs-lookup"><span data-stu-id="079e9-194">Upon dismissal, OneNote attempts to open up the link and an HResult.hrObjectDoesNotExist error is returned.</span></span>  <br/> |
|<span data-ttu-id="079e9-195">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="079e9-195">**Syntax**</span></span> <br/> | <span data-ttu-id="079e9-196">`HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); `</span><span class="sxs-lookup"><span data-stu-id="079e9-196">`HRESULT NavigateToUrl (`           ` [in]BSTR bstrUrl); `</span></span> <br/> |
|<span data-ttu-id="079e9-197">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="079e9-197">**Parameters**</span></span> <br/> | <span data-ttu-id="079e9-198">_бструрл_— URL-адрес для перехода.</span><span class="sxs-lookup"><span data-stu-id="079e9-198">_bstrUrl_—The URL to navigate to.</span></span>  <br/> |
   
<span data-ttu-id="079e9-199">**сетдоккедлокатион**</span><span class="sxs-lookup"><span data-stu-id="079e9-199">**SetDockedLocation**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="079e9-200">**Описание**</span><span class="sxs-lookup"><span data-stu-id="079e9-200">**Description**</span></span> <br/> |<span data-ttu-id="079e9-201">Закрепляет окно в расположении, указанном в **докклокатион** , и на мониторе по адресу **птмонитор**.</span><span class="sxs-lookup"><span data-stu-id="079e9-201">Docks the window to the location specified by **dockLocation** and the monitor at **ptMonitor**.</span></span>  <br/> |
|<span data-ttu-id="079e9-202">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="079e9-202">**Syntax**</span></span> <br/> | <span data-ttu-id="079e9-203">`HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);`</span><span class="sxs-lookup"><span data-stu-id="079e9-203">`HRESULT SetDockedLocation`(           `[in] DockLocation dockLocation,`           `[in] POINT ptMonitor);`</span></span> <br/> |
|<span data-ttu-id="079e9-204">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="079e9-204">**Parameters**</span></span> <br/> | <span data-ttu-id="079e9-205">_докклокатион_ — указывает закрепленное расположение окна OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="079e9-205">_dockLocation_ - Indicates the docked location of a OneNote 2013 window.</span></span>  <br/>  <span data-ttu-id="079e9-206">_птмонитор_ — (необязательно) указывает x, y – координаты, на которые должен закрепляться окно.</span><span class="sxs-lookup"><span data-stu-id="079e9-206">_ptMonitor_ - (Optional) Indicates in x,y co-ordinates which monitor the window should be docked to.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="079e9-207">Пример</span><span class="sxs-lookup"><span data-stu-id="079e9-207">Example</span></span>

<span data-ttu-id="079e9-208">Следующий код выполняет итерацию окон OneNote для поиска закрепленного окна.</span><span class="sxs-lookup"><span data-stu-id="079e9-208">The following code iterates through the OneNote windows to find a docked window.</span></span> <span data-ttu-id="079e9-209">Если закрепленного окна нет, в примере закрепляется активное окно.</span><span class="sxs-lookup"><span data-stu-id="079e9-209">If no docked window exists, the example docks the active window.</span></span> <span data-ttu-id="079e9-210">Если активное окно не существует, код создает новое закрепленное окно.</span><span class="sxs-lookup"><span data-stu-id="079e9-210">If no active window exists, the code creates a new docked window.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="079e9-211">См. также</span><span class="sxs-lookup"><span data-stu-id="079e9-211">See also</span></span>

- [<span data-ttu-id="079e9-212">Справочник разработчика для OneNote</span><span class="sxs-lookup"><span data-stu-id="079e9-212">OneNote developer reference</span></span>](onenote-developer-reference.md)

