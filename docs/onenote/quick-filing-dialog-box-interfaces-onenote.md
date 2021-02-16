---
title: Интерфейсы диалоговых окне "Быстрая подача данных" (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d83e39f0-b259-4c33-8f3e-e03e94c2403d
description: В этом разделе описываются интерфейсы, которые можно использовать для программной настройки диалоговых окна "Быстрая подача данных" в OneNote 2013.
ms.openlocfilehash: dd6b28ae6cb2acb007bae26ea661facaf1f8d4be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425339"
---
# <a name="quick-filing-dialog-box-interfaces-onenote"></a><span data-ttu-id="ea54e-103">Интерфейсы диалоговых окне "Быстрая подача данных" (OneNote)</span><span class="sxs-lookup"><span data-stu-id="ea54e-103">Quick Filing dialog box interfaces (OneNote)</span></span>

<span data-ttu-id="ea54e-104">В этом разделе описываются интерфейсы, которые можно использовать для программной настройки диалоговых окна "Быстрая подача данных" в OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="ea54e-104">This topic describes the interfaces that you can use to programmatically customize the Quick Filing dialog box in OneNote 2013.</span></span>
  
## <a name="quick-filing-dialog-box"></a><span data-ttu-id="ea54e-105">Диалоговое окно "Быстрая подача документов"</span><span class="sxs-lookup"><span data-stu-id="ea54e-105">Quick Filing dialog box</span></span>

<span data-ttu-id="ea54e-106">Диалоговое окно "Быстрая подача данных" в OneNote 2013 — это настраиваемое диалоговое окно, которое позволяет пользователям выбирать расположение в структуре иерархии OneNote.</span><span class="sxs-lookup"><span data-stu-id="ea54e-106">The Quick Filing dialog box in OneNote 2013 is a customizable dialog box that allows users to select a location within the OneNote hierarchy structure.</span></span> <span data-ttu-id="ea54e-107">К выбранным расположениям относятся записные книжки, группы разделов, разделы, страницы и подпапки.</span><span class="sxs-lookup"><span data-stu-id="ea54e-107">Selectable locations include notebooks, section groups, sections, pages, and subpages.</span></span> <span data-ttu-id="ea54e-108">Диалоговое окно используется как в приложении OneNote, так и во внешних приложениях с помощью API OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="ea54e-108">The dialog box is used both within the OneNote application and by external applications through the OneNote 2013 API.</span></span> <span data-ttu-id="ea54e-109">На рисунке 1 показано диалоговое окно "Быстрая подача" в состоянии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ea54e-109">Figure 1 shows the Quick Filing dialog box in its default state.</span></span>
  
<span data-ttu-id="ea54e-110">**Рисунок 1. Диалоговое окно "Быстрая подача документов" без настроек**</span><span class="sxs-lookup"><span data-stu-id="ea54e-110">**Figure 1. Quick Filing dialog box without customizations**</span></span>

<span data-ttu-id="ea54e-111">![Диалоговое окно "Быстрая подача документов"]без настройки диалоговое окно "Быстрая подача(media/ON15Con_quick_filing_dialog.jpg "документов\" без настроек")</span><span class="sxs-lookup"><span data-stu-id="ea54e-111">![Quick Filing dialog box without customizations](media/ON15Con_quick_filing_dialog.jpg "Quick Filing dialog box without customizations")</span></span>
  
<span data-ttu-id="ea54e-112">В диалоговом окне пользователи могут перейти по иерархии "Все записные книжки", чтобы найти определенные расположения, или найти структуру дерева OneNote, введя текстовое поле.</span><span class="sxs-lookup"><span data-stu-id="ea54e-112">Within the dialog box, users can navigate the All Notebooks hierarchy to look for specific locations or search the OneNote tree structure by typing into the text box.</span></span> <span data-ttu-id="ea54e-113">Параметры диалогового окна, которые можно настроить, включают название, описание, список последних результатов, текст и состояние в поле, глубину дерева, кнопки и типы выбора расположения.</span><span class="sxs-lookup"><span data-stu-id="ea54e-113">Aspects of the dialog box that can be customized include the title, description, recent results list, check box text and state, tree depth, buttons, and selectable location types.</span></span>

<span data-ttu-id="ea54e-114">Доступ к диалоговом окну "Быстрая подача данных" можно получить с помощью двух интерфейсов OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="ea54e-114">You can access the Quick Filing dialog box functionality through two OneNote 2013 interfaces.</span></span> <span data-ttu-id="ea54e-115">Интерфейс **IQuickFilingDialog** позволяет пользователям создать, настроить и запустить диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="ea54e-115">The **IQuickFilingDialog** interface allows users to instantiate, set up, and run the dialog box.</span></span> <span data-ttu-id="ea54e-116">Интерфейс **IQuickFilingDialogCallback** будет вызван после закрытия диалоговых окно.</span><span class="sxs-lookup"><span data-stu-id="ea54e-116">The **IQuickFilingDialogCallback** interface is called after the dialog box is closed.</span></span> <span data-ttu-id="ea54e-117">Диалоговое окно запущено в процессе OneNote, поэтому требуется механизм для поддержания потока диалоговых окна, а затем для записи выбора пользователя и состояния диалоговое окно при закрытии.</span><span class="sxs-lookup"><span data-stu-id="ea54e-117">The dialog box is run in the OneNote process, so a mechanism is needed to keep the dialog box's thread running and then to capture the user's selection and the state of the dialog box when it is closed.</span></span> 
  
## <a name="iquickfilingdialog-interface"></a><span data-ttu-id="ea54e-118">Интерфейс IQuickFilingDialog</span><span class="sxs-lookup"><span data-stu-id="ea54e-118">IQuickFilingDialog interface</span></span>
<span data-ttu-id="ea54e-119"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="ea54e-119"><a name="odc_IQuickFilingDialog"> </a></span></span>

<span data-ttu-id="ea54e-120">Этот интерфейс позволяет пользователю настраивать и запускать диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="ea54e-120">This interface allows the user to customize and run the dialog box.</span></span> <span data-ttu-id="ea54e-121">Пользователь может с помощью метода **Application.QuickFilingDialog** сделать диалоговое окно с помощью класса Application. </span><span class="sxs-lookup"><span data-stu-id="ea54e-121">The user can instantiate a dialog box through the **Application** class by using the **Application.QuickFilingDialog** method.</span></span> <span data-ttu-id="ea54e-122">Метод возвращает экземпляр диалоговых окно.</span><span class="sxs-lookup"><span data-stu-id="ea54e-122">The method returns an instance of the dialog box.</span></span> <span data-ttu-id="ea54e-123">После того как свойства диалоговых окна задаются, для запуска диалоговых окно используется метод **IQuickFilingDialog.Run.**</span><span class="sxs-lookup"><span data-stu-id="ea54e-123">Once the properties of the dialog box are set, the **IQuickFilingDialog.Run** method is used to run the dialog box.</span></span> <span data-ttu-id="ea54e-124">Этот метод запускает диалоговое окно в новом потоке.</span><span class="sxs-lookup"><span data-stu-id="ea54e-124">This method runs the dialog box on a new thread.</span></span> 
  
<span data-ttu-id="ea54e-125">**Свойства**</span><span class="sxs-lookup"><span data-stu-id="ea54e-125">**Properties**</span></span>

|<span data-ttu-id="ea54e-126">**Имя**</span><span class="sxs-lookup"><span data-stu-id="ea54e-126">**Name**</span></span>|<span data-ttu-id="ea54e-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ea54e-127">**Type**</span></span>|<span data-ttu-id="ea54e-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ea54e-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ea54e-129">**Title**</span><span class="sxs-lookup"><span data-stu-id="ea54e-129">**Title**</span></span> <br/> |<span data-ttu-id="ea54e-130">string</span><span class="sxs-lookup"><span data-stu-id="ea54e-130">string</span></span>  <br/> |<span data-ttu-id="ea54e-131">Получает или задает текст заголовка, который отображается в заголовке окна диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="ea54e-131">Gets or sets the title text that appears in the title bar of the dialog box window.</span></span>  <br/> |
|<span data-ttu-id="ea54e-132">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ea54e-132">**Description**</span></span> <br/> |<span data-ttu-id="ea54e-133">string</span><span class="sxs-lookup"><span data-stu-id="ea54e-133">string</span></span>  <br/> |<span data-ttu-id="ea54e-134">Получает или задает текстовое описание, указывав пользователю, что выбрать.</span><span class="sxs-lookup"><span data-stu-id="ea54e-134">Gets or sets the text description to instruct the user about what to select.</span></span> <span data-ttu-id="ea54e-135">Это значение может быть многострочная строка текста.</span><span class="sxs-lookup"><span data-stu-id="ea54e-135">This value can be multiple-line text.</span></span>  <br/> |
|<span data-ttu-id="ea54e-136">**CheckboxText**</span><span class="sxs-lookup"><span data-stu-id="ea54e-136">**CheckboxText**</span></span> <br/> |<span data-ttu-id="ea54e-137">string</span><span class="sxs-lookup"><span data-stu-id="ea54e-137">string</span></span>  <br/> |<span data-ttu-id="ea54e-138">Получает или задает текст, который следует за этим полем.</span><span class="sxs-lookup"><span data-stu-id="ea54e-138">Gets or sets the text that follows the check box.</span></span> <span data-ttu-id="ea54e-139">Если для этого значения установлена непустая строка, в диалоговом окне появится этот диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="ea54e-139">If this value is set to a non-empty string, a check box appears in the dialog box.</span></span> <span data-ttu-id="ea54e-140">Если значением является пустая строка, никакие из них не появляются.</span><span class="sxs-lookup"><span data-stu-id="ea54e-140">If the value is an empty string, no check box appears.</span></span>  <br/> |
|<span data-ttu-id="ea54e-141">**CheckboxState**</span><span class="sxs-lookup"><span data-stu-id="ea54e-141">**CheckboxState**</span></span> <br/> |<span data-ttu-id="ea54e-142">bool</span><span class="sxs-lookup"><span data-stu-id="ea54e-142">bool</span></span>  <br/> |<span data-ttu-id="ea54e-143">Возвращает или задает состояние этого контрольного окна.</span><span class="sxs-lookup"><span data-stu-id="ea54e-143">Gets or sets the state of the check box.</span></span> <span data-ttu-id="ea54e-144">Если за установлено значение **false,** то при нарабатыии диалоговом окне этот установлен.</span><span class="sxs-lookup"><span data-stu-id="ea54e-144">If value is set to **false**, the check box is cleared when the dialog box is started.</span></span> <span data-ttu-id="ea54e-145">Если установлено значение **true,** то при входящих в диалоговое окно диалоговых окнах устанавливается непустая строка **checkboxText.**</span><span class="sxs-lookup"><span data-stu-id="ea54e-145">If the value is set to **true**, the check box is selected when the dialog box is started as long as **CheckboxText** is a non-empty string.</span></span>  <br/> |
|<span data-ttu-id="ea54e-146">**WindowHandle**</span><span class="sxs-lookup"><span data-stu-id="ea54e-146">**WindowHandle**</span></span> <br/> |<span data-ttu-id="ea54e-147">ulong</span><span class="sxs-lookup"><span data-stu-id="ea54e-147">ulong</span></span>  <br/> |<span data-ttu-id="ea54e-148">Получает ИД работки диалогового окна "Быстрая подача документов".</span><span class="sxs-lookup"><span data-stu-id="ea54e-148">Gets the handle ID of the Quick Filing dialog box window.</span></span>  <br/> |
|<span data-ttu-id="ea54e-149">**TreeDepth**</span><span class="sxs-lookup"><span data-stu-id="ea54e-149">**TreeDepth**</span></span> <br/> |<span data-ttu-id="ea54e-150">**HierarchyElement**</span><span class="sxs-lookup"><span data-stu-id="ea54e-150">**HierarchyElement**</span></span> <br/> |<span data-ttu-id="ea54e-151">Получает или задает глубину отображения дерева OneNote в разделе "Все записные книжки".</span><span class="sxs-lookup"><span data-stu-id="ea54e-151">Gets or sets how deep the OneNote tree should be displayed in the All Notebooks section.</span></span> <span data-ttu-id="ea54e-152">По умолчанию дерево отображается до разделов.</span><span class="sxs-lookup"><span data-stu-id="ea54e-152">By default, the tree is displayed up to the sections.</span></span> <span data-ttu-id="ea54e-153">Это свойство не влияет на тип элементов, которые можно выбрать.</span><span class="sxs-lookup"><span data-stu-id="ea54e-153">This property does not affect what type of elements can be selected.</span></span>  <br/> <span data-ttu-id="ea54e-154">Если в иерархии OneNote установлен элемент **TreeDepth,** который находится ниже, чем может быть выбран любой из кнопок, отображаемая глубина дерева будет самым низким из возможных элементов, которые можно выбрать.</span><span class="sxs-lookup"><span data-stu-id="ea54e-154">If **TreeDepth** is set to an element lower in the OneNote hierarchy than can be selected by any of the buttons, the displayed tree depth will be the lowest possible selectable element.</span></span> <span data-ttu-id="ea54e-155">То есть, если глубина дерева настроена на отображение вниз по страницам, но самый низкий из выбираемых элементов — это раздел, дерево отображается вниз до разделов.</span><span class="sxs-lookup"><span data-stu-id="ea54e-155">That is, if tree depth is set to display down to pages, but the lowest selectable element is a section, the tree is displayed down to sections.</span></span>  <br/> |
|<span data-ttu-id="ea54e-156">**ParentWindowHandle**</span><span class="sxs-lookup"><span data-stu-id="ea54e-156">**ParentWindowHandle**</span></span> <br/> |<span data-ttu-id="ea54e-157">ulong</span><span class="sxs-lookup"><span data-stu-id="ea54e-157">ulong</span></span>  <br/> |<span data-ttu-id="ea54e-158">Получает или задает ИД работки родительского окна диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="ea54e-158">Gets or sets the handle ID of the parent window of the dialog box.</span></span> <span data-ttu-id="ea54e-159">Если это свойство установлено, диалоговое окно "Быстрая подача документов" будет модальным для назначенного родительского окна, когда откроется диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="ea54e-159">If this property is set, the Quick Filing dialog box will be modal to the assigned parent window when the dialog box opens.</span></span> <span data-ttu-id="ea54e-160">То есть пользователь не сможет получить доступ к родительскому окну, пока диалоговое окно "Быстрая подача данных" не будет закрыто.</span><span class="sxs-lookup"><span data-stu-id="ea54e-160">That is, a user will not be able to access the parent window until the Quick Filing dialog box is closed.</span></span>  <br/> |
|<span data-ttu-id="ea54e-161">**Position**</span><span class="sxs-lookup"><span data-stu-id="ea54e-161">**Position**</span></span> <br/> |<span data-ttu-id="ea54e-162">tagPOINT</span><span class="sxs-lookup"><span data-stu-id="ea54e-162">tagPOINT</span></span>  <br/> |<span data-ttu-id="ea54e-163">Получает или задает положение окна относительно экрана.</span><span class="sxs-lookup"><span data-stu-id="ea54e-163">Gets or sets the position of the window in relation to the screen.</span></span> <span data-ttu-id="ea54e-164">По умолчанию диалоговое окно отображается в центре родительского окна или рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="ea54e-164">By default, the dialog box appears in the middle of the parent window or the desktop.</span></span>  <br/> |
|<span data-ttu-id="ea54e-165">**SelectedItem**</span><span class="sxs-lookup"><span data-stu-id="ea54e-165">**SelectedItem**</span></span> <br/> |<span data-ttu-id="ea54e-166">string</span><span class="sxs-lookup"><span data-stu-id="ea54e-166">string</span></span>  <br/> |<span data-ttu-id="ea54e-167">Получает ИД объекта расположения OneNote, выбранного пользователем при закрытии диалоговых окно.</span><span class="sxs-lookup"><span data-stu-id="ea54e-167">Gets the object ID of the OneNote location selected by the user when the dialog box is closed.</span></span> <span data-ttu-id="ea54e-168">Если пользователь нажимает кнопку **"Отмена",** для объекта устанавливается null.</span><span class="sxs-lookup"><span data-stu-id="ea54e-168">If the user clicks the **Cancel** button, the object is set to null.</span></span>  <br/> |
|<span data-ttu-id="ea54e-169">**PressedButton**</span><span class="sxs-lookup"><span data-stu-id="ea54e-169">**PressedButton**</span></span> <br/> |<span data-ttu-id="ea54e-170">ulong</span><span class="sxs-lookup"><span data-stu-id="ea54e-170">ulong</span></span>  <br/> |<span data-ttu-id="ea54e-171">Получает, какая кнопка была нажата при закрытии диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="ea54e-171">Gets which button was clicked when the dialog box was closed.</span></span> <span data-ttu-id="ea54e-172">Если **кнопка** "Отмена" была нажата, это свойство возвращает значение -1.</span><span class="sxs-lookup"><span data-stu-id="ea54e-172">If the **Cancel** button was clicked, this property returns a value of -1.</span></span> <span data-ttu-id="ea54e-173">Всем другим кнопкам назначены значения от 0 до 1 для каждой кнопки, добавленной в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="ea54e-173">All other buttons are assigned integer values from 0, incremented by 1 for each button added to the dialog box.</span></span> <span data-ttu-id="ea54e-174">Для кнопки "ОК"  по умолчанию имеется значение 0.</span><span class="sxs-lookup"><span data-stu-id="ea54e-174">The integer value of the default **OK** button is 0.</span></span>  <br/> |
   
### <a name="methods"></a><span data-ttu-id="ea54e-175">Methods</span><span class="sxs-lookup"><span data-stu-id="ea54e-175">Methods</span></span>

<span data-ttu-id="ea54e-176">**SetRecentResults**</span><span class="sxs-lookup"><span data-stu-id="ea54e-176">**SetRecentResults**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ea54e-177">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ea54e-177">**Description**</span></span> <br/> |<span data-ttu-id="ea54e-178">Задает список последних результатов, который будет отображаться в диалоговом окне "Быстрая подача документов", и указывает, следует ли включить в список некоторые специальные расположения для хранения.</span><span class="sxs-lookup"><span data-stu-id="ea54e-178">Sets what recent result list will be displayed in the Quick Filing dialog box, and indicates whether to include some special filing locations in the list.</span></span> <span data-ttu-id="ea54e-179">Пользователи могут выбрать список последних результатов из списка [RecentResultType.](enumerations-onenote-developer-reference.md#odc_RecentResultType)</span><span class="sxs-lookup"><span data-stu-id="ea54e-179">Users can select a recent result list from the [RecentResultType](enumerations-onenote-developer-reference.md#odc_RecentResultType) enumeration.</span></span> <span data-ttu-id="ea54e-180">Пользователи также могут добавить в список следующие параметры: "Текущий раздел", "Текущая страница" или "Невыверченные заметки".</span><span class="sxs-lookup"><span data-stu-id="ea54e-180">Users can also choose to add the following options to the list: Current Section, Current Page, or Unfiled Notes.</span></span> <span data-ttu-id="ea54e-181">Если **выбран RecentResultType.rrtNone,** список последних результатов не отображается.</span><span class="sxs-lookup"><span data-stu-id="ea54e-181">If **RecentResultType.rrtNone** is selected, no recent result list is shown.</span></span>  <br/> |
|<span data-ttu-id="ea54e-182">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="ea54e-182">**Syntax**</span></span> <br/> | `HRESULT SetRecentResults (`<br/>`[in]RecentResultType recentResults,`<br/>`[in]VARIANT_BOOL fShowCurrentSection,`<br/>`[in]VARIANT_BOOL fShowCurrentPage,`<br/>`[in]VARIANT_BOOL fShowUnfiledNotes);` <br/> |
|<span data-ttu-id="ea54e-183">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="ea54e-183">**Parameters**</span></span> <br/> | <span data-ttu-id="ea54e-184">_recentResults_ &ndash; Объект типа **RecentResultType,** который указывает, какой последний список результатов должен отображаться, если таковый имеется.</span><span class="sxs-lookup"><span data-stu-id="ea54e-184">_recentResults_ &ndash; An object of type **RecentResultType** that indicates which recent result list, if any, should appear.</span></span> <span data-ttu-id="ea54e-185">Если **выбрано rrtNone,** в диалоговом окне не отображается список последних результатов.</span><span class="sxs-lookup"><span data-stu-id="ea54e-185">If **rrtNone** is selected, no recent result list appears in the dialog box.</span></span><br/><br/>  <span data-ttu-id="ea54e-186">_fShowCurrentSection_ &ndash; Boolean value that indicates whether the current section should be included in the recent result list.</span><span class="sxs-lookup"><span data-stu-id="ea54e-186">_fShowCurrentSection_ &ndash; A Boolean value that indicates whether the current section should be included in the recent result list.</span></span><br/><br/>  <span data-ttu-id="ea54e-187">_fShowCurrentPage_ &ndash; Boolean value that indicates whether the current page should be included in the recent result list.</span><span class="sxs-lookup"><span data-stu-id="ea54e-187">_fShowCurrentPage_ &ndash; A Boolean value that indicates whether the current page should be included in the recent result list.</span></span><br/><br/>  <span data-ttu-id="ea54e-188">_fShowUnfiledNotes_ &ndash; Boolean value that indicates whether the Unfiled Notes section should be included in the recent result list.</span><span class="sxs-lookup"><span data-stu-id="ea54e-188">_fShowUnfiledNotes_ &ndash; A Boolean value that indicates whether the Unfiled Notes section should be included in the recent result list.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="ea54e-189">Если специальное расположение для хранения невозможно выбрать с помощью кнопок в диалоговом окне, оно не отображается в списке.</span><span class="sxs-lookup"><span data-stu-id="ea54e-189">If a special filing location cannot be selected by using any of the buttons in the dialog box, it is not shown in the list.</span></span> <span data-ttu-id="ea54e-190">Если в списке последних результатов не найдено ни элемента, ни один из последних результатов не отображается.</span><span class="sxs-lookup"><span data-stu-id="ea54e-190">If no selectable item in the recent results list is found, no recent result list is displayed.</span></span> 
  
<span data-ttu-id="ea54e-191">В следующем примере метод **SetRecentResults** используется для отображения текущего раздела, текущей страницы и раздела "Unfiled Notes" в списке последних результатов.</span><span class="sxs-lookup"><span data-stu-id="ea54e-191">The following example uses the **SetRecentResults** method to display the current section, current page, and the Unfiled Notes section in the recent result list.</span></span> 
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            ...
        }

```

<span data-ttu-id="ea54e-192">**AddButton**</span><span class="sxs-lookup"><span data-stu-id="ea54e-192">**AddButton**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ea54e-193">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ea54e-193">**Description**</span></span> <br/> |<span data-ttu-id="ea54e-194">Позволяет пользователям добавлять и настраивать кнопки в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="ea54e-194">Allows users to add and customize buttons in the dialog box.</span></span> <span data-ttu-id="ea54e-195">Пользователи могут указать текст на кнопках и элементы иерархии OneNote, которые могут быть выбраны каждой кнопкой.</span><span class="sxs-lookup"><span data-stu-id="ea54e-195">Users can specify the text on the buttons and what elements of the OneNote hierarchy can be selected by each button.</span></span>  <br/> |
|<span data-ttu-id="ea54e-196">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="ea54e-196">**Syntax**</span></span> <br/> | `HRESULT AddButton (`<br/>`[in]BSTR bstrText,`<br/>`[in]HierarchyElement allowedElements,`<br/>`[in]HierarchyElement allowedReadOnlyElements,`<br/>`[in]VARIANT_BOOL fDefault);` <br/> |
|<span data-ttu-id="ea54e-197">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="ea54e-197">**Parameters**</span></span> <br/> | <span data-ttu-id="ea54e-198">_bstrText_ &ndash; Строка, указывавая текст, который должен отображаться на кнопке.</span><span class="sxs-lookup"><span data-stu-id="ea54e-198">_bstrText_ &ndash; A string that specifies the text to appear on the button.</span></span> <span data-ttu-id="ea54e-199">Чтобы настроить кнопку **"ОК"** по умолчанию, передав значение null **в качестве bstrText.**</span><span class="sxs-lookup"><span data-stu-id="ea54e-199">To customize the default **OK** button, pass in a null value as **bstrText**.</span></span>  <br/><br/><span data-ttu-id="ea54e-200">_allowedElements_ &ndash; **Элемент HierarchyElement,** который указывает, какие элементы иерархии OneNote, не только для чтения, пользователь может выбрать с помощью кнопки.</span><span class="sxs-lookup"><span data-stu-id="ea54e-200">_allowedElements_ &ndash; A **HierarchyElement** that indicates what non-read-only OneNote hierarchy elements a user is allowed to select by using the button.</span></span> <span data-ttu-id="ea54e-201">При выборе нескольких элементов пользователь должен передать оператор **OR** для всех эквивалентных значений uint типов **HierarchyElement,** разрешенных в качестве **HierarchyElement.**</span><span class="sxs-lookup"><span data-stu-id="ea54e-201">For selecting multiple items, the user should pass in the **OR** operator for all the uint equivalent values of the **HierarchyElement** types allowed as a **HierarchyElement**.</span></span><br/><br/>  <span data-ttu-id="ea54e-202">_allowedReadOnlyElements_ &ndash; **Элемент HierarchyElement,** который указывает, какие элементы иерархии OneNote разрешено выбирать пользователю с помощью кнопки.</span><span class="sxs-lookup"><span data-stu-id="ea54e-202">_allowedReadOnlyElements_ &ndash; A **HierarchyElement** that indicates what OneNote read-only hierarchy elements a user is allowed to select by using the button.</span></span> <span data-ttu-id="ea54e-203">При выборе нескольких элементов пользователь должен передать оператор **OR** для всех значений **uint-эквивалентов** типов **HierarchyElement,** разрешенных в качестве **HierarchyElement.**</span><span class="sxs-lookup"><span data-stu-id="ea54e-203">For selecting multiple items, the user should pass in the **OR** operator for all the **uint** equivalents values of the **HierarchyElement** types allowed as a **HierarchyElement**.</span></span><br/><br/>  <span data-ttu-id="ea54e-204">_fDefault_ &ndash; Boolean value that specifies whether this button should be the default button.</span><span class="sxs-lookup"><span data-stu-id="ea54e-204">_fDefault_ &ndash; A Boolean value that specifies whether this button should be the default button.</span></span> <span data-ttu-id="ea54e-205">Если несколько кнопок заданы по умолчанию, последняя указанная кнопка становится кнопкой по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ea54e-205">If multiple buttons are set as default, the last specified button becomes the default button.</span></span>  <br/> |
   
<span data-ttu-id="ea54e-206">В следующем примере в диалоговое окно "Быстрая подача документов" добавляются три кнопки.</span><span class="sxs-lookup"><span data-stu-id="ea54e-206">The following example adds three buttons to the Quick Filing dialog box.</span></span> <span data-ttu-id="ea54e-207">Первый элемент( **All)** может быть выбран всеми элементами в дереве иерархии OneNote.</span><span class="sxs-lookup"><span data-stu-id="ea54e-207">The first one, **All**, can be selected by all elements in the OneNote hierarchy tree.</span></span> <span data-ttu-id="ea54e-208">Остальные **записные книжки** и страницы можно выбрать, только если выбраны соответствующие элементы, записные книжки и страницы. </span><span class="sxs-lookup"><span data-stu-id="ea54e-208">The others, **Notebooks** and **Pages**, can be selected only if their corresponding elements, Notebooks and Pages, are selected.</span></span>
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            ... 
        }

```

<span data-ttu-id="ea54e-209">**Run**</span><span class="sxs-lookup"><span data-stu-id="ea54e-209">**Run**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ea54e-210">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ea54e-210">**Description**</span></span> <br/> |<span data-ttu-id="ea54e-211">Отображает диалоговое окно "Быстрая подача документов" из нового потока.</span><span class="sxs-lookup"><span data-stu-id="ea54e-211">Displays the Quick Filing dialog box from a new thread.</span></span> <span data-ttu-id="ea54e-212">Он принимает ссылку на интерфейс **IQuickFilingDialogCallback,** метод **OnDialogClosed** которого будет вызван после закрытия диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="ea54e-212">It takes a reference to the **IQuickFilingDialogCallback** interface, whose **OnDialogClosed** method will be called once the dialog box closes.</span></span>  <br/> |
|<span data-ttu-id="ea54e-213">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="ea54e-213">**Syntax**</span></span> <br/> | `HRESULT Run (`<br/>`[in]IQuickFilingDialogCallback piCallback);` <br/> |
|<span data-ttu-id="ea54e-214">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="ea54e-214">**Parameters**</span></span> <br/> | <span data-ttu-id="ea54e-215">_piCallback_ &ndash; Ссылка на интерфейс **IQuickFilingDialogCallback,** который будет созважен после закрытия диалоговых окном.</span><span class="sxs-lookup"><span data-stu-id="ea54e-215">_piCallback_ &ndash; A reference to the **IQuickFilingDialogCallback** interface that will be instantiated once the dialog box closes.</span></span>  <br/> |
   
<span data-ttu-id="ea54e-216">В следующем примере метод **Run** используется для отображения диалоговых окна "Быстрая подача" из нового потока.</span><span class="sxs-lookup"><span data-stu-id="ea54e-216">The following example uses the **Run** method to display the Quick Filing dialog box from a new thread.</span></span> 
  
```cs
    class OpenQuickFilingDialog
    {
            ... 
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            ... 
        }
    }

```

<span data-ttu-id="ea54e-217">**TreeCollapsedState**</span><span class="sxs-lookup"><span data-stu-id="ea54e-217">**TreeCollapsedState**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ea54e-218">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ea54e-218">**Description**</span></span> <br/> |<span data-ttu-id="ea54e-219">Указывает, следует ли развернуть или свернуть дерево иерархии.</span><span class="sxs-lookup"><span data-stu-id="ea54e-219">Indicates whether the hierarchy tree should be expanded or collapsed.</span></span>  <br/> |
|<span data-ttu-id="ea54e-220">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="ea54e-220">**Syntax**</span></span> <br/> | `HRESULT TreeCollapsedState(`<br/>`[in] TreeCollapsedStateType tcs);` <br/> |
|<span data-ttu-id="ea54e-221">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="ea54e-221">**Parameters**</span></span> <br/> | <span data-ttu-id="ea54e-222">_tcs_ — указывает, будет ли дерево расширено или свернуто.</span><span class="sxs-lookup"><span data-stu-id="ea54e-222">_tcs_ - Specifies whether the tree is expanded or collapsed.</span></span>  <br/> |
   
<span data-ttu-id="ea54e-223">**NotebookFilterOut**</span><span class="sxs-lookup"><span data-stu-id="ea54e-223">**NotebookFilterOut**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ea54e-224">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ea54e-224">**Description**</span></span> <br/> |<span data-ttu-id="ea54e-225">Фильтрует список записных книжок, показанных по типу.</span><span class="sxs-lookup"><span data-stu-id="ea54e-225">Filters the list of notebooks shown by type.</span></span>  <br/> |
|<span data-ttu-id="ea54e-226">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="ea54e-226">**Syntax**</span></span> <br/> | `HRESULT NotebookFilterOut(`<br/>`[in] NotebookFilterOutType nfo);` <br/> |
|<span data-ttu-id="ea54e-227">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="ea54e-227">**Parameters**</span></span> <br/> | <span data-ttu-id="ea54e-228">_nfo_ — указывает набор записных книзок, которые необходимо отфильтровать из списка</span><span class="sxs-lookup"><span data-stu-id="ea54e-228">_nfo_ - Specifies the set of notebooks that are to be filtered out of the list</span></span>  <br/> |
   
<span data-ttu-id="ea54e-229">**ShowCreateNewNotebook**</span><span class="sxs-lookup"><span data-stu-id="ea54e-229">**ShowCreateNewNotebook**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ea54e-230">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ea54e-230">**Description**</span></span> <br/> |<span data-ttu-id="ea54e-231">Отображает параметр создания записной книжки в диалоговом оке.</span><span class="sxs-lookup"><span data-stu-id="ea54e-231">Displays the create new notebook option in the dialog.</span></span>  <br/> |
|<span data-ttu-id="ea54e-232">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="ea54e-232">**Syntax**</span></span> <br/> | `HRESULT ShowCreateNewNotebook ();` <br/> |
|<span data-ttu-id="ea54e-233">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="ea54e-233">**Parameters**</span></span> <br/> |<span data-ttu-id="ea54e-234">Нет</span><span class="sxs-lookup"><span data-stu-id="ea54e-234">None</span></span>  <br/> |
   
<span data-ttu-id="ea54e-235">**AddInitialEditor**</span><span class="sxs-lookup"><span data-stu-id="ea54e-235">**AddInitialEditor**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ea54e-236">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ea54e-236">**Description**</span></span> <br/> |<span data-ttu-id="ea54e-237">Добавляет пользователя в качестве начального редактора в записную книжку в диалоговом окне "Быстрая подача данных".</span><span class="sxs-lookup"><span data-stu-id="ea54e-237">Adds a user as an initial editor to a notebook in the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="ea54e-238">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="ea54e-238">**Syntax**</span></span> <br/> | `HRESULT AddInitialEditor (BSTR initialEditor);` <br/> |
|<span data-ttu-id="ea54e-239">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="ea54e-239">**Parameters**</span></span> <br/> | <span data-ttu-id="ea54e-240">_initialEditor_ — адрес электронной почты пользователя, который вы хотите добавить в записную книжку в качестве редактора.</span><span class="sxs-lookup"><span data-stu-id="ea54e-240">_initialEditor_ - The email address of the user you wish to add as an editor to the notebook.</span></span> <span data-ttu-id="ea54e-241">Когда записная книжка создается в диалоговом окне "Быстрая подача документов", она автоматически передается всем начальным редакторам.</span><span class="sxs-lookup"><span data-stu-id="ea54e-241">When the notebook is created via the Quick Filing dialog box, it is automatically shared with all Initial Editors.</span></span>  <br/> |
   
<span data-ttu-id="ea54e-242">**ClearInitialEditors**</span><span class="sxs-lookup"><span data-stu-id="ea54e-242">**ClearInitialEditors**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ea54e-243">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ea54e-243">**Description**</span></span> <br/> |<span data-ttu-id="ea54e-244">Удаляет все начальные редакторы из диалогового окна "Быстрая подача документов".</span><span class="sxs-lookup"><span data-stu-id="ea54e-244">Removes all initial editors from the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="ea54e-245">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="ea54e-245">**Syntax**</span></span> <br/> | `HRESULT ClearInitialEditors ();` <br/> |
|<span data-ttu-id="ea54e-246">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="ea54e-246">**Parameters**</span></span> <br/> |<span data-ttu-id="ea54e-247">Нет</span><span class="sxs-lookup"><span data-stu-id="ea54e-247">None</span></span>  <br/> |
   
<span data-ttu-id="ea54e-248">**ShowSharingHyperlink**</span><span class="sxs-lookup"><span data-stu-id="ea54e-248">**ShowSharingHyperlink**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ea54e-249">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ea54e-249">**Description**</span></span> <br/> |<span data-ttu-id="ea54e-250">Отображает гиперссылку раздела справки по совместному доступу в диалоговом окне "Быстрая подача документов".</span><span class="sxs-lookup"><span data-stu-id="ea54e-250">Displays the Sharing Help Topic Hyperlink in the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="ea54e-251">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="ea54e-251">**Syntax**</span></span> <br/> | `HRESULT ShowSharingHyperlink();` <br/> |
|<span data-ttu-id="ea54e-252">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="ea54e-252">**Parameters**</span></span> <br/> |<span data-ttu-id="ea54e-253">Нет</span><span class="sxs-lookup"><span data-stu-id="ea54e-253">None</span></span>  <br/> |
   
## <a name="iquickfilingdialogcallback-interface"></a><span data-ttu-id="ea54e-254">Интерфейс IQuickFilingDialogCallback</span><span class="sxs-lookup"><span data-stu-id="ea54e-254">IQuickFilingDialogCallback interface</span></span>
<span data-ttu-id="ea54e-255"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="ea54e-255"><a name="odc_IQuickFilingDialog"> </a></span></span>

<span data-ttu-id="ea54e-256">Этот интерфейс позволяет пользователю получать доступ к свойствам диалоговых окно после закрытия диалоговых окно.</span><span class="sxs-lookup"><span data-stu-id="ea54e-256">This interface allows the user to access the dialog box properties after the dialog box closes.</span></span> <span data-ttu-id="ea54e-257">После закрытия диалоговое окно OneNote 2013 вызывает метод **IQuickFilingDialogCallback.OnDialogClose** в этом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="ea54e-257">Once the dialog box closes, OneNote 2013 calls the **IQuickFilingDialogCallback.OnDialogClose** method in this interface.</span></span> 
  
<span data-ttu-id="ea54e-258">Необходимо определить класс, наследуемый этим интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="ea54e-258">A class that inherits this interface has to be defined.</span></span>
  
### <a name="methods"></a><span data-ttu-id="ea54e-259">Methods</span><span class="sxs-lookup"><span data-stu-id="ea54e-259">Methods</span></span>

<span data-ttu-id="ea54e-260">В следующем разделе описаны методы, связанные с интерфейсами, которые были подробно описаны ранее.</span><span class="sxs-lookup"><span data-stu-id="ea54e-260">The following section describes the methods associated with the interfaces detailed previously.</span></span>
  
<span data-ttu-id="ea54e-261">**OnDialogClosed**</span><span class="sxs-lookup"><span data-stu-id="ea54e-261">**OnDialogClosed**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ea54e-262">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ea54e-262">**Description**</span></span> <br/> |<span data-ttu-id="ea54e-263">Позволяет пользователям добавлять функции для захвата и использования выбора пользователя в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="ea54e-263">Enables users to add functionality to capture and use the user selection from the dialog box.</span></span> <span data-ttu-id="ea54e-264">Этот метод будет вызван после закрытия диалоговых окна "Быстрая подача документов".</span><span class="sxs-lookup"><span data-stu-id="ea54e-264">This method is called after the Quick Filing dialog box is closed.</span></span> <span data-ttu-id="ea54e-265">Этот метод является функцией, которую должны определять интерфейсы **IQuickFilingDialogCallback.**</span><span class="sxs-lookup"><span data-stu-id="ea54e-265">This method is a function that **IQuickFilingDialogCallback** interfaces have to define.</span></span>  <br/> |
|<span data-ttu-id="ea54e-266">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="ea54e-266">**Syntax**</span></span> <br/> | `HRESULT OnDialogClosed (`<br/>`[in]IQuickFilingDialog dialog);` <br/> |
|<span data-ttu-id="ea54e-267">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="ea54e-267">**Parameters**</span></span> <br/> | <span data-ttu-id="ea54e-268">_диалоговое окно_ &ndash; Объект **IQuickFilingDialog,** который вызвал **метод OnDialogClose.**</span><span class="sxs-lookup"><span data-stu-id="ea54e-268">_dialog_ &ndash; The **IQuickFilingDialog** object that called the **OnDialogClose** method.</span></span>  <br/> |
   
<span data-ttu-id="ea54e-269">Ниже приводится пример интерфейса **IQuickFilingDialogCallback.**</span><span class="sxs-lookup"><span data-stu-id="ea54e-269">The following example is a sample **IQuickFilingDialogCallback** interface.</span></span> <span data-ttu-id="ea54e-270">Метод **OnDialogClose** печатает выбор пользователя в диалоговом окне "Быстрая подача данных" на консоль.</span><span class="sxs-lookup"><span data-stu-id="ea54e-270">The **OnDialogClose** method prints the user's selection from the Quick Filing dialog box to the console.</span></span> 
  
```cs
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }

```

## <a name="example"></a><span data-ttu-id="ea54e-271">Пример</span><span class="sxs-lookup"><span data-stu-id="ea54e-271">Example</span></span>
<span data-ttu-id="ea54e-272"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="ea54e-272"><a name="odc_IQuickFilingDialog"> </a></span></span>

<span data-ttu-id="ea54e-273">В следующем примере кода открывается диалоговое окно "Быстрая подача" с настроенным заголовком, описанием, недавним списком результатов, глубиной дерева, полем и кнопками.</span><span class="sxs-lookup"><span data-stu-id="ea54e-273">The following code example opens a Quick Filing dialog box that has a customized title, description, recent result list, tree depth, check box, and buttons.</span></span> <span data-ttu-id="ea54e-274">Выбранный пользователем элемент, нажатая кнопка и состояние проверки будут отображаться в окне консоли при закрытии диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="ea54e-274">The user's selected item, pressed button, and check-box state will be displayed in a console window when the dialog box is closed.</span></span> <span data-ttu-id="ea54e-275">Чтобы увидеть, что кнопка страницы включена, пользователю необходимо будет найти страницу и выбрать ее, так как глубина дерева настроена на разделы.</span><span class="sxs-lookup"><span data-stu-id="ea54e-275">To see the page button enabled, the user will have to search for a page and select it, because the tree depth is set down to sections.</span></span> <span data-ttu-id="ea54e-276">Диалоговое окно не является относячным к любому окну.</span><span class="sxs-lookup"><span data-stu-id="ea54e-276">The dialog box is not a child of any window.</span></span>
  
```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading;
using Microsoft.Office.Interop.OneNote;
namespace SampleQFD
{
    class OpenQuickFilingDialog
    {
        private static EventWaitHandle wh = new AutoResetEvent(false);
        private static IQuickFilingDialog qfDialog;
        private static String strTitle = "Sample Title";
        private static String strDescription = "Sample Description";
        private static String strCheckboxText = "Sample Checkbox";
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            // Instantiate Quick Filing UI
            qfDialog = app.QuickFiling();
            #region//SET API PARAMETERS
            // TITLE
            qfDialog.Title = strTitle;
            // DESCRIPTION
            qfDialog.Description = strDescription;
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            // TREE DEPTH
            qfDialog.TreeDepth = HierarchyElement.heSections;
            // CHECKBOX
            qfDialog.CheckboxText = strCheckboxText;
            qfDialog.CheckboxState = false;
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            // PARENTWINDOW
            #endregion
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            // Clean up and Wait so console window does not close
            qfDialog = null;
            wh.WaitOne();
        }
    }
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }
}

```

## <a name="see-also"></a><span data-ttu-id="ea54e-277">См. также</span><span class="sxs-lookup"><span data-stu-id="ea54e-277">See also</span></span>

- [<span data-ttu-id="ea54e-278">Справочник разработчика для OneNote</span><span class="sxs-lookup"><span data-stu-id="ea54e-278">OneNote developer reference</span></span>](onenote-developer-reference.md)

