---
title: Интерфейсы диалоговых окон быстрого хранения (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d83e39f0-b259-4c33-8f3e-e03e94c2403d
description: В этом разделе описываются интерфейсы, которые можно использовать для программного настройки диалогового окна быстрого хранения в OneNote 2013.
ms.openlocfilehash: dd6b28ae6cb2acb007bae26ea661facaf1f8d4be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317102"
---
# <a name="quick-filing-dialog-box-interfaces-onenote"></a><span data-ttu-id="b7f3d-103">Интерфейсы диалоговых окон быстрого хранения (OneNote)</span><span class="sxs-lookup"><span data-stu-id="b7f3d-103">Quick Filing dialog box interfaces (OneNote)</span></span>

<span data-ttu-id="b7f3d-104">В этом разделе описываются интерфейсы, которые можно использовать для программного настройки диалогового окна быстрого хранения в OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-104">This topic describes the interfaces that you can use to programmatically customize the Quick Filing dialog box in OneNote 2013.</span></span>
  
## <a name="quick-filing-dialog-box"></a><span data-ttu-id="b7f3d-105">Диалоговое окно "быстрое сохранение"</span><span class="sxs-lookup"><span data-stu-id="b7f3d-105">Quick Filing dialog box</span></span>

<span data-ttu-id="b7f3d-106">Диалоговое окно "быстрое сохранение" в OneNote 2013 является настраиваемым диалоговым окном, которое позволяет пользователям выбрать расположение в структуре иерархии OneNote.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-106">The Quick Filing dialog box in OneNote 2013 is a customizable dialog box that allows users to select a location within the OneNote hierarchy structure.</span></span> <span data-ttu-id="b7f3d-107">Выбираемые расположения включают записные книжки, группы разделов, разделы, страницы и вложенные страницы.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-107">Selectable locations include notebooks, section groups, sections, pages, and subpages.</span></span> <span data-ttu-id="b7f3d-108">Диалоговое окно используется как в приложении OneNote, так и во внешних приложениях с помощью API OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-108">The dialog box is used both within the OneNote application and by external applications through the OneNote 2013 API.</span></span> <span data-ttu-id="b7f3d-109">На рисунке 1 показано диалоговое окно быстрого хранения в состоянии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-109">Figure 1 shows the Quick Filing dialog box in its default state.</span></span>
  
<span data-ttu-id="b7f3d-110">**Рис. 1. Диалоговое окно "быстрое сохранение" без настроек**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-110">**Figure 1. Quick Filing dialog box without customizations**</span></span>

<span data-ttu-id="b7f3d-111">![Диалоговое окно "быстрое сохранение" без настроек] (media/ON15Con_quick_filing_dialog.jpg "Диалоговое окно \"быстрое сохранение\" без настроек")</span><span class="sxs-lookup"><span data-stu-id="b7f3d-111">![Quick Filing dialog box without customizations](media/ON15Con_quick_filing_dialog.jpg "Quick Filing dialog box without customizations")</span></span>
  
<span data-ttu-id="b7f3d-112">В диалоговом окне пользователи могут перейти в иерархию "все записные книжки", чтобы найти определенные расположения, или выполнить поиск по древовидной структуре OneNote, введя текст в текстовое поле.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-112">Within the dialog box, users can navigate the All Notebooks hierarchy to look for specific locations or search the OneNote tree structure by typing into the text box.</span></span> <span data-ttu-id="b7f3d-113">Параметры диалогового окна, которое можно изменить, включают название, описание, список недавних результатов, текст флажка и состояние, глубину дерева, кнопки и доступные для выбора типы расположения.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-113">Aspects of the dialog box that can be customized include the title, description, recent results list, check box text and state, tree depth, buttons, and selectable location types.</span></span>

<span data-ttu-id="b7f3d-114">Вы можете получить доступ к функциям диалогового окна "быстрое сохранение" через два интерфейса OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-114">You can access the Quick Filing dialog box functionality through two OneNote 2013 interfaces.</span></span> <span data-ttu-id="b7f3d-115">Интерфейс **икуиккфилингдиалог** позволяет пользователям создавать экземпляры, настраивать и запускать диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-115">The **IQuickFilingDialog** interface allows users to instantiate, set up, and run the dialog box.</span></span> <span data-ttu-id="b7f3d-116">Интерфейс **икуиккфилингдиалогкаллбакк** вызывается после закрытия диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-116">The **IQuickFilingDialogCallback** interface is called after the dialog box is closed.</span></span> <span data-ttu-id="b7f3d-117">Диалоговое окно запускается в процессе OneNote, поэтому необходим механизм, позволяющий обеспечить выполнение потока диалогового окна, а затем записывать выбор пользователя и состояние диалогового окна при его закрытии.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-117">The dialog box is run in the OneNote process, so a mechanism is needed to keep the dialog box's thread running and then to capture the user's selection and the state of the dialog box when it is closed.</span></span> 
  
## <a name="iquickfilingdialog-interface"></a><span data-ttu-id="b7f3d-118">Интерфейс Икуиккфилингдиалог</span><span class="sxs-lookup"><span data-stu-id="b7f3d-118">IQuickFilingDialog interface</span></span>
<span data-ttu-id="b7f3d-119"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="b7f3d-119"></span></span>

<span data-ttu-id="b7f3d-120">Этот интерфейс позволяет пользователю настраивать и запускать диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-120">This interface allows the user to customize and run the dialog box.</span></span> <span data-ttu-id="b7f3d-121">Пользователь может создать экземпляр диалогового окна с помощью класса **Application** с помощью метода **Application. куиккфилингдиалог** .</span><span class="sxs-lookup"><span data-stu-id="b7f3d-121">The user can instantiate a dialog box through the **Application** class by using the **Application.QuickFilingDialog** method.</span></span> <span data-ttu-id="b7f3d-122">Метод возвращает экземпляр диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-122">The method returns an instance of the dialog box.</span></span> <span data-ttu-id="b7f3d-123">После задания свойств диалогового окна метод **икуиккфилингдиалог. Run** используется для запуска диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-123">Once the properties of the dialog box are set, the **IQuickFilingDialog.Run** method is used to run the dialog box.</span></span> <span data-ttu-id="b7f3d-124">Этот метод запускает диалоговое окно в новом потоке.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-124">This method runs the dialog box on a new thread.</span></span> 
  
<span data-ttu-id="b7f3d-125">**Свойства**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-125">**Properties**</span></span>

|<span data-ttu-id="b7f3d-126">**Name**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-126">**Name**</span></span>|<span data-ttu-id="b7f3d-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-127">**Type**</span></span>|<span data-ttu-id="b7f3d-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-128">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b7f3d-129">**Title**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-129">**Title**</span></span> <br/> |<span data-ttu-id="b7f3d-130">строка</span><span class="sxs-lookup"><span data-stu-id="b7f3d-130">string</span></span>  <br/> |<span data-ttu-id="b7f3d-131">Получает или задает текст заголовка, который отображается в строке заголовка окна диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-131">Gets or sets the title text that appears in the title bar of the dialog box window.</span></span>  <br/> |
|<span data-ttu-id="b7f3d-132">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-132">**Description**</span></span> <br/> |<span data-ttu-id="b7f3d-133">строка</span><span class="sxs-lookup"><span data-stu-id="b7f3d-133">string</span></span>  <br/> |<span data-ttu-id="b7f3d-134">Получает или задает текстовое описание, указывающее пользователю, что нужно выбрать.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-134">Gets or sets the text description to instruct the user about what to select.</span></span> <span data-ttu-id="b7f3d-135">Это значение может быть многострочным текстом.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-135">This value can be multiple-line text.</span></span>  <br/> |
|<span data-ttu-id="b7f3d-136">**Чеккбокстекст**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-136">**CheckboxText**</span></span> <br/> |<span data-ttu-id="b7f3d-137">строка</span><span class="sxs-lookup"><span data-stu-id="b7f3d-137">string</span></span>  <br/> |<span data-ttu-id="b7f3d-138">Получает или задает текст, который следует за флажком.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-138">Gets or sets the text that follows the check box.</span></span> <span data-ttu-id="b7f3d-139">Если для этого параметра задана непустая строка, в диалоговом окне отображается флажок.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-139">If this value is set to a non-empty string, a check box appears in the dialog box.</span></span> <span data-ttu-id="b7f3d-140">Если значением является пустая строка, флажок не отображается.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-140">If the value is an empty string, no check box appears.</span></span>  <br/> |
|<span data-ttu-id="b7f3d-141">**Чеккбоксстате**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-141">**CheckboxState**</span></span> <br/> |<span data-ttu-id="b7f3d-142">bool</span><span class="sxs-lookup"><span data-stu-id="b7f3d-142">bool</span></span>  <br/> |<span data-ttu-id="b7f3d-143">Получает или задает состояние флажка.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-143">Gets or sets the state of the check box.</span></span> <span data-ttu-id="b7f3d-144">Если параметру присвоено значение **false**, то при запуске диалогового окна флажок снимается.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-144">If value is set to **false**, the check box is cleared when the dialog box is started.</span></span> <span data-ttu-id="b7f3d-145">Если для этого параметра установлено значение **true**, то при запуске диалогового окна устанавливается флажок, если **чеккбокстекст** не является пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-145">If the value is set to **true**, the check box is selected when the dialog box is started as long as **CheckboxText** is a non-empty string.</span></span>  <br/> |
|<span data-ttu-id="b7f3d-146">**Виндовхандле**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-146">**WindowHandle**</span></span> <br/> |<span data-ttu-id="b7f3d-147">ulong</span><span class="sxs-lookup"><span data-stu-id="b7f3d-147">ulong</span></span>  <br/> |<span data-ttu-id="b7f3d-148">Получает идентификатор дескриптора для окна диалогового окна быстрого хранения.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-148">Gets the handle ID of the Quick Filing dialog box window.</span></span>  <br/> |
|<span data-ttu-id="b7f3d-149">**Тридепс**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-149">**TreeDepth**</span></span> <br/> |<span data-ttu-id="b7f3d-150">**Хиерарчелемент**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-150">**HierarchyElement**</span></span> <br/> |<span data-ttu-id="b7f3d-151">Получает или задает значение, указывающее, как глубокое дерево OneNote должно отображаться в разделе Все записные книжки.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-151">Gets or sets how deep the OneNote tree should be displayed in the All Notebooks section.</span></span> <span data-ttu-id="b7f3d-152">По умолчанию дерево отображается в соответствии с разделами.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-152">By default, the tree is displayed up to the sections.</span></span> <span data-ttu-id="b7f3d-153">Это свойство не влияет на тип элементов, которые можно выбрать.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-153">This property does not affect what type of elements can be selected.</span></span>  <br/> <span data-ttu-id="b7f3d-154">Если для **тридепс** задан элемент, расположенный ниже в иерархии OneNote, чем можно выбрать с помощью любой из кнопок, отображаемая глубина дерева будет наименьшим возможным выбираемым элементом.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-154">If **TreeDepth** is set to an element lower in the OneNote hierarchy than can be selected by any of the buttons, the displayed tree depth will be the lowest possible selectable element.</span></span> <span data-ttu-id="b7f3d-155">То есть, если глубина дерева настроена на отображение страниц, но самый маленький элемент является разделом, дерево отображается в разделах.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-155">That is, if tree depth is set to display down to pages, but the lowest selectable element is a section, the tree is displayed down to sections.</span></span>  <br/> |
|<span data-ttu-id="b7f3d-156">**Парентвиндовхандле**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-156">**ParentWindowHandle**</span></span> <br/> |<span data-ttu-id="b7f3d-157">ulong</span><span class="sxs-lookup"><span data-stu-id="b7f3d-157">ulong</span></span>  <br/> |<span data-ttu-id="b7f3d-158">Получает или задает идентификатор дескриптора родительского окна диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-158">Gets or sets the handle ID of the parent window of the dialog box.</span></span> <span data-ttu-id="b7f3d-159">Если это свойство задано, диалоговое окно быстрого хранения будет модальным для назначенного родительского окна при открытии диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-159">If this property is set, the Quick Filing dialog box will be modal to the assigned parent window when the dialog box opens.</span></span> <span data-ttu-id="b7f3d-160">Таким образом, пользователь не сможет получить доступ к родительскому окну до тех пор, пока не будет закрыто диалоговое окно "быстрое Архивация".</span><span class="sxs-lookup"><span data-stu-id="b7f3d-160">That is, a user will not be able to access the parent window until the Quick Filing dialog box is closed.</span></span>  <br/> |
|<span data-ttu-id="b7f3d-161">**Position**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-161">**Position**</span></span> <br/> |<span data-ttu-id="b7f3d-162">Тагпоинт</span><span class="sxs-lookup"><span data-stu-id="b7f3d-162">tagPOINT</span></span>  <br/> |<span data-ttu-id="b7f3d-163">Получает или задает положение окна по отношению к экрану.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-163">Gets or sets the position of the window in relation to the screen.</span></span> <span data-ttu-id="b7f3d-164">По умолчанию диалоговое окно отображается в середине родительского окна или рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-164">By default, the dialog box appears in the middle of the parent window or the desktop.</span></span>  <br/> |
|<span data-ttu-id="b7f3d-165">**SelectedItem**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-165">**SelectedItem**</span></span> <br/> |<span data-ttu-id="b7f3d-166">строка</span><span class="sxs-lookup"><span data-stu-id="b7f3d-166">string</span></span>  <br/> |<span data-ttu-id="b7f3d-167">Получает идентификатор объекта расположения OneNote, выбранного пользователем при закрытии диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-167">Gets the object ID of the OneNote location selected by the user when the dialog box is closed.</span></span> <span data-ttu-id="b7f3d-168">Если пользователь нажимает кнопку **Cancel (Отмена** ), для объекта устанавливается значение null.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-168">If the user clicks the **Cancel** button, the object is set to null.</span></span>  <br/> |
|<span data-ttu-id="b7f3d-169">**Пресседбуттон**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-169">**PressedButton**</span></span> <br/> |<span data-ttu-id="b7f3d-170">ulong</span><span class="sxs-lookup"><span data-stu-id="b7f3d-170">ulong</span></span>  <br/> |<span data-ttu-id="b7f3d-171">Получает значение, по которому была нажата кнопка при закрытии диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-171">Gets which button was clicked when the dialog box was closed.</span></span> <span data-ttu-id="b7f3d-172">Если была нажата кнопка **Cancel (Отмена** ), это свойство возвращает значение – 1.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-172">If the **Cancel** button was clicked, this property returns a value of -1.</span></span> <span data-ttu-id="b7f3d-173">Всем остальным кнопкам присваиваются целочисленные значения от 0, что увеличивается на 1 для каждой кнопки, добавленной в диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-173">All other buttons are assigned integer values from 0, incremented by 1 for each button added to the dialog box.</span></span> <span data-ttu-id="b7f3d-174">Целочисленное значение кнопки **ОК** по умолчанию равно 0.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-174">The integer value of the default **OK** button is 0.</span></span>  <br/> |
   
### <a name="methods"></a><span data-ttu-id="b7f3d-175">Методы</span><span class="sxs-lookup"><span data-stu-id="b7f3d-175">Methods</span></span>

<span data-ttu-id="b7f3d-176">**Сетрецентресултс**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-176">**SetRecentResults**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7f3d-177">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-177">**Description**</span></span> <br/> |<span data-ttu-id="b7f3d-178">Задает, какой список последних результатов будет отображаться в диалоговом окне "быстрое сохранение", и указывает, следует ли включить в список некоторые специальные места хранения.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-178">Sets what recent result list will be displayed in the Quick Filing dialog box, and indicates whether to include some special filing locations in the list.</span></span> <span data-ttu-id="b7f3d-179">Пользователи могут выбрать последний список результатов из перечисления [рецентресулттипе](enumerations-onenote-developer-reference.md#odc_RecentResultType) .</span><span class="sxs-lookup"><span data-stu-id="b7f3d-179">Users can select a recent result list from the [RecentResultType](enumerations-onenote-developer-reference.md#odc_RecentResultType) enumeration.</span></span> <span data-ttu-id="b7f3d-180">Кроме того, пользователи могут добавлять в список следующие параметры: текущий раздел, текущая страница или unfile Notes.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-180">Users can also choose to add the following options to the list: Current Section, Current Page, or Unfiled Notes.</span></span> <span data-ttu-id="b7f3d-181">Если выбрано **рецентресулттипе. рртноне** , список последних результатов не отображается.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-181">If **RecentResultType.rrtNone** is selected, no recent result list is shown.</span></span>  <br/> |
|<span data-ttu-id="b7f3d-182">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-182">**Syntax**</span></span> <br/> | `HRESULT SetRecentResults (`<br/>`[in]RecentResultType recentResults,`<br/>`[in]VARIANT_BOOL fShowCurrentSection,`<br/>`[in]VARIANT_BOOL fShowCurrentPage,`<br/>`[in]VARIANT_BOOL fShowUnfiledNotes);` <br/> |
|<span data-ttu-id="b7f3d-183">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-183">**Parameters**</span></span> <br/> | <span data-ttu-id="b7f3d-184">_рецентресултс_ &ndash; Объект типа **рецентресулттипе** , указывающий, какой список последних результатов (при его наличии) должен отображаться.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-184">_recentResults_ &ndash; An object of type **RecentResultType** that indicates which recent result list, if any, should appear.</span></span> <span data-ttu-id="b7f3d-185">Если выбрано значение **рртноне** , в диалоговом окне не отображается ни одного списка результатов.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-185">If **rrtNone** is selected, no recent result list appears in the dialog box.</span></span><br/><br/>  <span data-ttu-id="b7f3d-186">_фшовкуррентсектион_ &ndash; Логическое значение, которое указывает, следует ли включить текущий раздел в список последних результатов.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-186">_fShowCurrentSection_ &ndash; A Boolean value that indicates whether the current section should be included in the recent result list.</span></span><br/><br/>  <span data-ttu-id="b7f3d-187">_фшовкуррентпаже_ &ndash; Логическое значение, которое указывает, следует ли включить текущую страницу в список последних результатов.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-187">_fShowCurrentPage_ &ndash; A Boolean value that indicates whether the current page should be included in the recent result list.</span></span><br/><br/>  <span data-ttu-id="b7f3d-188">_фшовунфиледнотес_ &ndash; Логическое значение, которое указывает, следует ли включать раздел "невыполненные заметки" в список последних результатов.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-188">_fShowUnfiledNotes_ &ndash; A Boolean value that indicates whether the Unfiled Notes section should be included in the recent result list.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="b7f3d-189">Если специальное расположение для хранения не может быть выбрано с помощью каких-либо кнопок в диалоговом окне, оно не отображается в списке.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-189">If a special filing location cannot be selected by using any of the buttons in the dialog box, it is not shown in the list.</span></span> <span data-ttu-id="b7f3d-190">Если в списке "Недавние результаты" нет выбираемого элемента, список последних результатов не отображается.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-190">If no selectable item in the recent results list is found, no recent result list is displayed.</span></span> 
  
<span data-ttu-id="b7f3d-191">В следующем примере используется метод **сетрецентресултс** для отображения текущего раздела, текущей страницы и раздела unfile Notes в списке последних результатов.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-191">The following example uses the **SetRecentResults** method to display the current section, current page, and the Unfiled Notes section in the recent result list.</span></span> 
  
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

<span data-ttu-id="b7f3d-192">**Аддбуттон**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-192">**AddButton**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7f3d-193">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-193">**Description**</span></span> <br/> |<span data-ttu-id="b7f3d-194">Позволяет пользователям добавлять и настраивать кнопки в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-194">Allows users to add and customize buttons in the dialog box.</span></span> <span data-ttu-id="b7f3d-195">Пользователи могут указать текст на кнопках и элементы иерархии OneNote, которые могут быть выбраны каждой кнопкой.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-195">Users can specify the text on the buttons and what elements of the OneNote hierarchy can be selected by each button.</span></span>  <br/> |
|<span data-ttu-id="b7f3d-196">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-196">**Syntax**</span></span> <br/> | `HRESULT AddButton (`<br/>`[in]BSTR bstrText,`<br/>`[in]HierarchyElement allowedElements,`<br/>`[in]HierarchyElement allowedReadOnlyElements,`<br/>`[in]VARIANT_BOOL fDefault);` <br/> |
|<span data-ttu-id="b7f3d-197">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-197">**Parameters**</span></span> <br/> | <span data-ttu-id="b7f3d-198">_бстртекст_ &ndash; Строка, указывающая текст, который будет отображаться на кнопке.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-198">_bstrText_ &ndash; A string that specifies the text to appear on the button.</span></span> <span data-ttu-id="b7f3d-199">Чтобы настроить кнопку " **ОК** " по умолчанию, передайте значение NULL в качестве **бстртекст**.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-199">To customize the default **OK** button, pass in a null value as **bstrText**.</span></span>  <br/><br/><span data-ttu-id="b7f3d-200">_алловеделементс_ &ndash; Объект **хиерарчелемент** , указывающий, какие элементы иерархии OneNote, не предназначенные только для чтения, разрешено выбирать пользователю с помощью кнопки.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-200">_allowedElements_ &ndash; A **HierarchyElement** that indicates what non-read-only OneNote hierarchy elements a user is allowed to select by using the button.</span></span> <span data-ttu-id="b7f3d-201">Для выбора нескольких элементов пользователь должен передать оператор **or** для всех эквивалентных значений типа uint, допустимых в виде \*\*\*\* **хиерарчелемент**.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-201">For selecting multiple items, the user should pass in the **OR** operator for all the uint equivalent values of the **HierarchyElement** types allowed as a **HierarchyElement**.</span></span><br/><br/>  <span data-ttu-id="b7f3d-202">_алловедреадонлелементс_ &ndash; Объект **хиерарчелемент** , указывающий элементы иерархии OneNote, доступные только для чтения, которые пользователь может выбрать с помощью кнопки.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-202">_allowedReadOnlyElements_ &ndash; A **HierarchyElement** that indicates what OneNote read-only hierarchy elements a user is allowed to select by using the button.</span></span> <span data-ttu-id="b7f3d-203">Чтобы выбрать несколько элементов, пользователь должен передать оператору **or** все значения **uint** , эквивалентные типам **хиерарчелемент** , разрешенные в виде **хиерарчелемент**.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-203">For selecting multiple items, the user should pass in the **OR** operator for all the **uint** equivalents values of the **HierarchyElement** types allowed as a **HierarchyElement**.</span></span><br/><br/>  <span data-ttu-id="b7f3d-204">_фдефаулт_ &ndash; Логическое значение, которое указывает, должна ли эта кнопка быть кнопкой по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-204">_fDefault_ &ndash; A Boolean value that specifies whether this button should be the default button.</span></span> <span data-ttu-id="b7f3d-205">Если для нескольких кнопок задано значение по умолчанию, Последняя указанная кнопка становится кнопкой по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-205">If multiple buttons are set as default, the last specified button becomes the default button.</span></span>  <br/> |
   
<span data-ttu-id="b7f3d-206">В приведенном ниже примере в диалоговое окно "быстрое хранение" добавляются три кнопки.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-206">The following example adds three buttons to the Quick Filing dialog box.</span></span> <span data-ttu-id="b7f3d-207">Первый из них может \*\*\*\* быть выбран всеми элементами в дереве иерархии OneNote.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-207">The first one, **All**, can be selected by all elements in the OneNote hierarchy tree.</span></span> <span data-ttu-id="b7f3d-208">Остальные, **записНые книжки** и **страницы**можно выбирать только в том случае, если выбраны соответствующие элементы, записные книжки и страницы.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-208">The others, **Notebooks** and **Pages**, can be selected only if their corresponding elements, Notebooks and Pages, are selected.</span></span>
  
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

<span data-ttu-id="b7f3d-209">**Run**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-209">**Run**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7f3d-210">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-210">**Description**</span></span> <br/> |<span data-ttu-id="b7f3d-211">Отображает диалоговое окно "быстрое сохранение в новом потоке".</span><span class="sxs-lookup"><span data-stu-id="b7f3d-211">Displays the Quick Filing dialog box from a new thread.</span></span> <span data-ttu-id="b7f3d-212">Он принимает ссылку на интерфейс **икуиккфилингдиалогкаллбакк** , метод **ондиалогклосед** которого будет вызываться после закрытия диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-212">It takes a reference to the **IQuickFilingDialogCallback** interface, whose **OnDialogClosed** method will be called once the dialog box closes.</span></span>  <br/> |
|<span data-ttu-id="b7f3d-213">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-213">**Syntax**</span></span> <br/> | `HRESULT Run (`<br/>`[in]IQuickFilingDialogCallback piCallback);` <br/> |
|<span data-ttu-id="b7f3d-214">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-214">**Parameters**</span></span> <br/> | <span data-ttu-id="b7f3d-215">_пикаллбакк_ &ndash; Ссылка на интерфейс **икуиккфилингдиалогкаллбакк** , который будет создаваться после закрытия диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-215">_piCallback_ &ndash; A reference to the **IQuickFilingDialogCallback** interface that will be instantiated once the dialog box closes.</span></span>  <br/> |
   
<span data-ttu-id="b7f3d-216">В следующем примере используется метод **Run** для отображения диалогового окна быстрого хранения из нового потока.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-216">The following example uses the **Run** method to display the Quick Filing dialog box from a new thread.</span></span> 
  
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

<span data-ttu-id="b7f3d-217">**Триколлапседстате**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-217">**TreeCollapsedState**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7f3d-218">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-218">**Description**</span></span> <br/> |<span data-ttu-id="b7f3d-219">Указывает, должно ли дерево иерархии разворачиваться или сворачиваться.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-219">Indicates whether the hierarchy tree should be expanded or collapsed.</span></span>  <br/> |
|<span data-ttu-id="b7f3d-220">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-220">**Syntax**</span></span> <br/> | `HRESULT TreeCollapsedState(`<br/>`[in] TreeCollapsedStateType tcs);` <br/> |
|<span data-ttu-id="b7f3d-221">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-221">**Parameters**</span></span> <br/> | <span data-ttu-id="b7f3d-222">_служб TCS_ — указывает, развернут или свернут дерево.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-222">_tcs_ - Specifies whether the tree is expanded or collapsed.</span></span>  <br/> |
   
<span data-ttu-id="b7f3d-223">**Нотебукфилтераут**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-223">**NotebookFilterOut**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7f3d-224">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-224">**Description**</span></span> <br/> |<span data-ttu-id="b7f3d-225">Фильтрует список записных книжек, отображаемых по типу.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-225">Filters the list of notebooks shown by type.</span></span>  <br/> |
|<span data-ttu-id="b7f3d-226">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-226">**Syntax**</span></span> <br/> | `HRESULT NotebookFilterOut(`<br/>`[in] NotebookFilterOutType nfo);` <br/> |
|<span data-ttu-id="b7f3d-227">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-227">**Parameters**</span></span> <br/> | <span data-ttu-id="b7f3d-228">_NFO_ — задает набор записных книжек, которые будут отфильтровываться из списка.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-228">_nfo_ - Specifies the set of notebooks that are to be filtered out of the list</span></span>  <br/> |
   
<span data-ttu-id="b7f3d-229">**Шовкреатеневнотебук**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-229">**ShowCreateNewNotebook**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7f3d-230">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-230">**Description**</span></span> <br/> |<span data-ttu-id="b7f3d-231">Отображает параметр создать новую записную книжку в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-231">Displays the create new notebook option in the dialog.</span></span>  <br/> |
|<span data-ttu-id="b7f3d-232">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-232">**Syntax**</span></span> <br/> | `HRESULT ShowCreateNewNotebook ();` <br/> |
|<span data-ttu-id="b7f3d-233">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-233">**Parameters**</span></span> <br/> |<span data-ttu-id="b7f3d-234">Нет</span><span class="sxs-lookup"><span data-stu-id="b7f3d-234">None</span></span>  <br/> |
   
<span data-ttu-id="b7f3d-235">**Аддинитиаледитор**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-235">**AddInitialEditor**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7f3d-236">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-236">**Description**</span></span> <br/> |<span data-ttu-id="b7f3d-237">Добавляет пользователя в качестве исходного редактора в записную книжку в диалоговом окне "быстрое хранение".</span><span class="sxs-lookup"><span data-stu-id="b7f3d-237">Adds a user as an initial editor to a notebook in the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="b7f3d-238">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-238">**Syntax**</span></span> <br/> | `HRESULT AddInitialEditor (BSTR initialEditor);` <br/> |
|<span data-ttu-id="b7f3d-239">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-239">**Parameters**</span></span> <br/> | <span data-ttu-id="b7f3d-240">_инитиаледитор_ — адрес электронной почты пользователя, который вы хотите добавить в качестве редактора записной книжки.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-240">_initialEditor_ - The email address of the user you wish to add as an editor to the notebook.</span></span> <span data-ttu-id="b7f3d-241">Когда Записная книжка создается с помощью диалогового окна "быстрое Архивация", она автоматически становится общей для всех начальных редакторов.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-241">When the notebook is created via the Quick Filing dialog box, it is automatically shared with all Initial Editors.</span></span>  <br/> |
   
<span data-ttu-id="b7f3d-242">**Клеаринитиаледиторс**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-242">**ClearInitialEditors**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7f3d-243">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-243">**Description**</span></span> <br/> |<span data-ttu-id="b7f3d-244">Удаляет все начальные редакторы из диалогового окна "быстрое сохранение".</span><span class="sxs-lookup"><span data-stu-id="b7f3d-244">Removes all initial editors from the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="b7f3d-245">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-245">**Syntax**</span></span> <br/> | `HRESULT ClearInitialEditors ();` <br/> |
|<span data-ttu-id="b7f3d-246">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-246">**Parameters**</span></span> <br/> |<span data-ttu-id="b7f3d-247">Нет</span><span class="sxs-lookup"><span data-stu-id="b7f3d-247">None</span></span>  <br/> |
   
<span data-ttu-id="b7f3d-248">**Шовшарингхиперлинк**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-248">**ShowSharingHyperlink**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7f3d-249">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-249">**Description**</span></span> <br/> |<span data-ttu-id="b7f3d-250">Отображает ссылку на раздел справки "общий доступ" в диалоговом окне "быстрое Архивация".</span><span class="sxs-lookup"><span data-stu-id="b7f3d-250">Displays the Sharing Help Topic Hyperlink in the Quick Filing dialog box.</span></span>  <br/> |
|<span data-ttu-id="b7f3d-251">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-251">**Syntax**</span></span> <br/> | `HRESULT ShowSharingHyperlink();` <br/> |
|<span data-ttu-id="b7f3d-252">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-252">**Parameters**</span></span> <br/> |<span data-ttu-id="b7f3d-253">Нет</span><span class="sxs-lookup"><span data-stu-id="b7f3d-253">None</span></span>  <br/> |
   
## <a name="iquickfilingdialogcallback-interface"></a><span data-ttu-id="b7f3d-254">Интерфейс Икуиккфилингдиалогкаллбакк</span><span class="sxs-lookup"><span data-stu-id="b7f3d-254">IQuickFilingDialogCallback interface</span></span>
<span data-ttu-id="b7f3d-255"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="b7f3d-255"></span></span>

<span data-ttu-id="b7f3d-256">Этот интерфейс позволяет пользователю получить доступ к свойствам диалогового окна после закрытия диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-256">This interface allows the user to access the dialog box properties after the dialog box closes.</span></span> <span data-ttu-id="b7f3d-257">Когда диалоговое окно закроется, OneNote 2013 вызывает метод **икуиккфилингдиалогкаллбакк. ондиалогклосе** в этом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-257">Once the dialog box closes, OneNote 2013 calls the **IQuickFilingDialogCallback.OnDialogClose** method in this interface.</span></span> 
  
<span data-ttu-id="b7f3d-258">Необходимо определить класс, наследуемый этим интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-258">A class that inherits this interface has to be defined.</span></span>
  
### <a name="methods"></a><span data-ttu-id="b7f3d-259">Методы</span><span class="sxs-lookup"><span data-stu-id="b7f3d-259">Methods</span></span>

<span data-ttu-id="b7f3d-260">В следующем разделе описаны методы, связанные с интерфейсами, описанными выше.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-260">The following section describes the methods associated with the interfaces detailed previously.</span></span>
  
<span data-ttu-id="b7f3d-261">**Ондиалогклосед**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-261">**OnDialogClosed**</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7f3d-262">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-262">**Description**</span></span> <br/> |<span data-ttu-id="b7f3d-263">Позволяет пользователям добавлять функции для захвата и использования выбора пользователя в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-263">Enables users to add functionality to capture and use the user selection from the dialog box.</span></span> <span data-ttu-id="b7f3d-264">Этот метод вызывается после закрытия диалогового окна "быстрое Архивация".</span><span class="sxs-lookup"><span data-stu-id="b7f3d-264">This method is called after the Quick Filing dialog box is closed.</span></span> <span data-ttu-id="b7f3d-265">Этот метод является функцией, которую необходимо определить для интерфейсов **икуиккфилингдиалогкаллбакк** .</span><span class="sxs-lookup"><span data-stu-id="b7f3d-265">This method is a function that **IQuickFilingDialogCallback** interfaces have to define.</span></span>  <br/> |
|<span data-ttu-id="b7f3d-266">**Синтаксис**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-266">**Syntax**</span></span> <br/> | `HRESULT OnDialogClosed (`<br/>`[in]IQuickFilingDialog dialog);` <br/> |
|<span data-ttu-id="b7f3d-267">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="b7f3d-267">**Parameters**</span></span> <br/> | <span data-ttu-id="b7f3d-268">_диалоговое окно_ &ndash; Объект **икуиккфилингдиалог** , который вызвал метод **ондиалогклосе** .</span><span class="sxs-lookup"><span data-stu-id="b7f3d-268">_dialog_ &ndash; The **IQuickFilingDialog** object that called the **OnDialogClose** method.</span></span>  <br/> |
   
<span data-ttu-id="b7f3d-269">Ниже приведен пример интерфейса **икуиккфилингдиалогкаллбакк** .</span><span class="sxs-lookup"><span data-stu-id="b7f3d-269">The following example is a sample **IQuickFilingDialogCallback** interface.</span></span> <span data-ttu-id="b7f3d-270">Метод **ондиалогклосе** выводит выбранные пользователем элементы из диалогового окна быстрого хранения в консоль.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-270">The **OnDialogClose** method prints the user's selection from the Quick Filing dialog box to the console.</span></span> 
  
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

## <a name="example"></a><span data-ttu-id="b7f3d-271">Пример</span><span class="sxs-lookup"><span data-stu-id="b7f3d-271">Example</span></span>
<span data-ttu-id="b7f3d-272"><a name="odc_IQuickFilingDialog"> </a></span><span class="sxs-lookup"><span data-stu-id="b7f3d-272"></span></span>

<span data-ttu-id="b7f3d-273">В следующем примере кода открывается диалоговое окно быстрого хранения с настроенным названием, описанием, списком последних результатов, глубиной дерева, флажком и кнопками.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-273">The following code example opens a Quick Filing dialog box that has a customized title, description, recent result list, tree depth, check box, and buttons.</span></span> <span data-ttu-id="b7f3d-274">Выбранный пользователем элемент, нажатая кнопка и состояние флажка будут отображаться в окне консоли при закрытии диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-274">The user's selected item, pressed button, and check-box state will be displayed in a console window when the dialog box is closed.</span></span> <span data-ttu-id="b7f3d-275">Чтобы увидеть, включена ли кнопка страницы, пользователь должен выполнить поиск страницы и выбрать ее, так как глубина дерева устанавливается на разделы.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-275">To see the page button enabled, the user will have to search for a page and select it, because the tree depth is set down to sections.</span></span> <span data-ttu-id="b7f3d-276">Диалоговое окно не является дочерним по отношению к какому-либо окну.</span><span class="sxs-lookup"><span data-stu-id="b7f3d-276">The dialog box is not a child of any window.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="b7f3d-277">См. также</span><span class="sxs-lookup"><span data-stu-id="b7f3d-277">See also</span></span>

- [<span data-ttu-id="b7f3d-278">Справочник разработчика для OneNote</span><span class="sxs-lookup"><span data-stu-id="b7f3d-278">OneNote developer reference</span></span>](onenote-developer-reference.md)

