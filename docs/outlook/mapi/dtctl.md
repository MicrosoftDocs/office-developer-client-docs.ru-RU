---
title: DTCTL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTCTL
api_type:
- COM
ms.assetid: 6d1589e9-b171-427a-9a3e-b4154ee8ceb6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2a2ca1fba5dceb45b41c2f25a96e163f02c41440
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421503"
---
# <a name="dtctl"></a><span data-ttu-id="cca35-103">DTCTL</span><span class="sxs-lookup"><span data-stu-id="cca35-103">DTCTL</span></span>

<span data-ttu-id="cca35-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cca35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cca35-105">Описывает элемент управления, который будет использоваться в диалоговом окне, созданном из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="cca35-105">Describes a control that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cca35-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="cca35-106">Header file:</span></span>  <br/> |<span data-ttu-id="cca35-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="cca35-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulCtlType;
  ULONG ulCtlFlags;
  LPBYTE lpbNotif;
  ULONG cbNotif;
  LPSTR lpszFilter;
  ULONG ulItemID;
  union
  {
    LPVOID lpv;
    LPDTBLLABEL lplabel;
    LPDTBLEDIT lpedit;
    LPDTBLLBX lplbx;
    LPDTBLCOMBOBOX lpcombobox;
    LPDTBLDDLBX lpddlbx;
    LPDTBLCHECKBOX lpcheckbox;
    LPDTBLGROUPBOX lpgroupbox;
    LPDTBLBUTTON lpbutton;
    LPDTBLRADIOBUTTON lpradiobutton;
    LPDTBLMVLISTBOX lpmvlbx;
    LPDTBLMVDDLBX lpmvddlbx;
    LPDTBLPAGE lppage;
  } ctl;
} DTCTL, FAR *LPDTCTL;

```

## <a name="members"></a><span data-ttu-id="cca35-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="cca35-108">Members</span></span>

<span data-ttu-id="cca35-109">**улктлтипе**</span><span class="sxs-lookup"><span data-stu-id="cca35-109">**ulCtlType**</span></span>
  
> <span data-ttu-id="cca35-110">Тип элемента управления, включенный в элемент **CTL** и соответствующий свойству **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) элемента управления.</span><span class="sxs-lookup"><span data-stu-id="cca35-110">Type of control that is included in the **ctl** member and corresponds to the control's **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) property.</span></span> <span data-ttu-id="cca35-111">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="cca35-111">Possible values are as follows:</span></span>
    
<span data-ttu-id="cca35-112">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="cca35-112">DTCT_LABEL</span></span> 
  
> <span data-ttu-id="cca35-113">Элемент управления Label.</span><span class="sxs-lookup"><span data-stu-id="cca35-113">Label control.</span></span>
    
<span data-ttu-id="cca35-114">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="cca35-114">DTCT_EDIT</span></span> 
  
> <span data-ttu-id="cca35-115">Элемент управления Edit.</span><span class="sxs-lookup"><span data-stu-id="cca35-115">Edit control.</span></span>
    
<span data-ttu-id="cca35-116">DTCT_LBX</span><span class="sxs-lookup"><span data-stu-id="cca35-116">DTCT_LBX</span></span> 
  
> <span data-ttu-id="cca35-117">Элемент управления "список".</span><span class="sxs-lookup"><span data-stu-id="cca35-117">List box control.</span></span>
    
<span data-ttu-id="cca35-118">DTCT_COMBOBOX</span><span class="sxs-lookup"><span data-stu-id="cca35-118">DTCT_COMBOBOX</span></span> 
  
> <span data-ttu-id="cca35-119">Элемент управления "поле со списком".</span><span class="sxs-lookup"><span data-stu-id="cca35-119">Combo box control.</span></span>
    
<span data-ttu-id="cca35-120">DTCT_DDLBX</span><span class="sxs-lookup"><span data-stu-id="cca35-120">DTCT_DDLBX</span></span> 
  
> <span data-ttu-id="cca35-121">Элемент управления "раскрывающийся список".</span><span class="sxs-lookup"><span data-stu-id="cca35-121">Drop-down list control.</span></span>
    
<span data-ttu-id="cca35-122">DTCT_CHECKBOX</span><span class="sxs-lookup"><span data-stu-id="cca35-122">DTCT_CHECKBOX</span></span> 
  
> <span data-ttu-id="cca35-123">Элемент управления "флажок".</span><span class="sxs-lookup"><span data-stu-id="cca35-123">Check box control.</span></span>
    
<span data-ttu-id="cca35-124">DTCT_GROUPBOX</span><span class="sxs-lookup"><span data-stu-id="cca35-124">DTCT_GROUPBOX</span></span> 
  
> <span data-ttu-id="cca35-125">Элемент управления "Группа".</span><span class="sxs-lookup"><span data-stu-id="cca35-125">Group box control.</span></span>
    
<span data-ttu-id="cca35-126">DTCT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="cca35-126">DTCT_BUTTON</span></span> 
  
> <span data-ttu-id="cca35-127">Элемент управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="cca35-127">Button control.</span></span>
    
<span data-ttu-id="cca35-128">DTCT_PAGE</span><span class="sxs-lookup"><span data-stu-id="cca35-128">DTCT_PAGE</span></span> 
  
> <span data-ttu-id="cca35-129">Элемент управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="cca35-129">Tabbed page control.</span></span>
    
<span data-ttu-id="cca35-130">DTCT_RADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="cca35-130">DTCT_RADIOBUTTON</span></span> 
  
> <span data-ttu-id="cca35-131">Элемент управления "переключатель".</span><span class="sxs-lookup"><span data-stu-id="cca35-131">Radio button control.</span></span>
    
<span data-ttu-id="cca35-132">DTCT_MVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="cca35-132">DTCT_MVLISTBOX</span></span> 
  
> <span data-ttu-id="cca35-133">Многозначный список элементов управления.</span><span class="sxs-lookup"><span data-stu-id="cca35-133">Multi-valued list control.</span></span>
    
<span data-ttu-id="cca35-134">DTCT_MVDDLBX</span><span class="sxs-lookup"><span data-stu-id="cca35-134">DTCT_MVDDLBX</span></span> 
  
> <span data-ttu-id="cca35-135">Элемент управления раскрывающегося списка с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="cca35-135">Multi-valued drop-down list control.</span></span>
    
<span data-ttu-id="cca35-136">**улктлфлагс**</span><span class="sxs-lookup"><span data-stu-id="cca35-136">**ulCtlFlags**</span></span>
  
> <span data-ttu-id="cca35-137">Битовая маска флагов, описывающих компоненты элемента управления и соответствующих свойству **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) элемента управления.</span><span class="sxs-lookup"><span data-stu-id="cca35-137">Bitmask of flags that describes the control's features and corresponds to the control's **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="cca35-138">Эти флажки можно устанавливать только для флажков, полей со списками, списков и элементов управления редактирования.</span><span class="sxs-lookup"><span data-stu-id="cca35-138">These flags can be set for check boxes, combo boxes, list boxes, and edit controls only.</span></span> <span data-ttu-id="cca35-139">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="cca35-139">Possible values are as follows:</span></span>
    
<span data-ttu-id="cca35-140">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="cca35-140">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="cca35-141">Принимается формат ANSI или DBCS.</span><span class="sxs-lookup"><span data-stu-id="cca35-141">Either the ANSI or DBCS format is accepted.</span></span> <span data-ttu-id="cca35-142">Этот флаг действителен только для элементов управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="cca35-142">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="cca35-143">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="cca35-143">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="cca35-144">Пользователь может изменять текст в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="cca35-144">A user can modify the text in the control.</span></span> 
    
<span data-ttu-id="cca35-145">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="cca35-145">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="cca35-146">Элемент управления может содержать несколько строк текста.</span><span class="sxs-lookup"><span data-stu-id="cca35-146">The control can contain multiple text lines.</span></span> <span data-ttu-id="cca35-147">Этот флаг действителен только для элементов управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="cca35-147">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="cca35-148">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="cca35-148">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="cca35-149">Элемент управления содержит пароль; Поэтому содержимое элемента управления не должно отображаться для пользователя.</span><span class="sxs-lookup"><span data-stu-id="cca35-149">The control contains a password; therefore, the contents of the control should not be displayed to the user.</span></span> <span data-ttu-id="cca35-150">Этот флаг действителен только для элементов управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="cca35-150">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="cca35-151">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="cca35-151">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="cca35-152">Элемент управления "диалоговое окно" является обязательным.</span><span class="sxs-lookup"><span data-stu-id="cca35-152">The dialog box control is required.</span></span> <span data-ttu-id="cca35-153">Этот флаг действителен только для элементов управления "поле ввода" и "поле со списком".</span><span class="sxs-lookup"><span data-stu-id="cca35-153">This flag is valid only for edit and combo box controls.</span></span>
    
<span data-ttu-id="cca35-154">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="cca35-154">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="cca35-155">Включает немедленный вывод значения при изменении элемента управления.</span><span class="sxs-lookup"><span data-stu-id="cca35-155">Enables immediate output of a value upon a change in the control.</span></span> <span data-ttu-id="cca35-156">Это позволяет установить отношение зависимости между двумя элементами управления.</span><span class="sxs-lookup"><span data-stu-id="cca35-156">This allows a dependency relationship to be established between two controls.</span></span> 
    
<span data-ttu-id="cca35-157">**лпбнотиф**</span><span class="sxs-lookup"><span data-stu-id="cca35-157">**lpbNotif**</span></span>
  
> <span data-ttu-id="cca35-158">Указатель на структуру, состоящую из структуры [GUID](guid.md) , которая представляет поставщика услуг и идентификатор элемента управления.</span><span class="sxs-lookup"><span data-stu-id="cca35-158">Pointer to a structure that consists of a [GUID](guid.md) structure, to represent the service provider and an identifier for the control.</span></span> <span data-ttu-id="cca35-159">Члены **лпбнотиф** и **кбнотиф** соответствуют свойству **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) элемента управления и используются для уведомления пользовательского интерфейса о необходимости обновления элемента управления.</span><span class="sxs-lookup"><span data-stu-id="cca35-159">The **lpbNotif** and **cbNotif** members correspond to the control's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property and are used to notify the user interface when the control has to be updated.</span></span>
    
<span data-ttu-id="cca35-160">**кбнотиф**</span><span class="sxs-lookup"><span data-stu-id="cca35-160">**cbNotif**</span></span>
  
> <span data-ttu-id="cca35-161">Количество байтов в структуре, на которую указывает элемент **лпбнотиф** .</span><span class="sxs-lookup"><span data-stu-id="cca35-161">Count of bytes in the structure pointed to by the **lpbNotif** member.</span></span> 
    
<span data-ttu-id="cca35-162">**лпсзфилтер**</span><span class="sxs-lookup"><span data-stu-id="cca35-162">**lpszFilter**</span></span>
  
> <span data-ttu-id="cca35-163">Указатель на строку символов, описывающую символы, которые можно ввести в элемент управления "поле ввода" или "поле со списком".</span><span class="sxs-lookup"><span data-stu-id="cca35-163">Pointer to a character string that describes which characters can be entered into an edit or combo box control.</span></span> <span data-ttu-id="cca35-164">Для других типов элементов управления элемент **лпсзфилтер** может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="cca35-164">For other types of controls, the **lpszFilter** member can be NULL.</span></span> <span data-ttu-id="cca35-165">Для элементов управления "поле со списком" и "поле со списком" это должно быть регулярное выражение, которое применяется к отдельному символу за раз.</span><span class="sxs-lookup"><span data-stu-id="cca35-165">For edit and combo box controls, it should be a regular expression that applies to a single character at a time.</span></span> <span data-ttu-id="cca35-166">Один и тот же фильтр применяется ко всем символам в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="cca35-166">The same filter is applied to all characters in the control.</span></span> <span data-ttu-id="cca35-167">Строка фильтра имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="cca35-167">The format of the filter string is as follows:</span></span> 
    
|<span data-ttu-id="cca35-168">**Символ**</span><span class="sxs-lookup"><span data-stu-id="cca35-168">**Character**</span></span>|<span data-ttu-id="cca35-169">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cca35-169">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> | <span data-ttu-id="cca35-170">Разрешен любой символ (например, `"*"`).</span><span class="sxs-lookup"><span data-stu-id="cca35-170">Any character is allowed (for example, `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="cca35-171">Определяет набор символов (например, `"[0123456789]"`.).</span><span class="sxs-lookup"><span data-stu-id="cca35-171">Defines a set of characters (for example, `"[0123456789]"`.)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="cca35-172">Указывает диапазон символов (например, `"[a-z]"`).</span><span class="sxs-lookup"><span data-stu-id="cca35-172">Indicates a range of characters (for example, `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="cca35-173">Указывает, что эти символы не разрешены (например, `"[~0-9]")`.</span><span class="sxs-lookup"><span data-stu-id="cca35-173">Indicates that these characters are not allowed (for example, `"[~0-9]")`.</span></span> <br/>|   
| `\` <br/> |<span data-ttu-id="cca35-174">Используется для заключения в кавычки любого из предыдущих символов (например `"[\-\\\[\]]"` , допустимые \, символы-, [, и]).</span><span class="sxs-lookup"><span data-stu-id="cca35-174">Used to quote any of the previous symbols (for example, `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
<span data-ttu-id="cca35-175">**улитемид**</span><span class="sxs-lookup"><span data-stu-id="cca35-175">**ulItemID**</span></span>
  
> <span data-ttu-id="cca35-176">Значение, идентифицирующее элемент управления в ресурсе диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="cca35-176">Value that identifies the control in the dialog box resource.</span></span> <span data-ttu-id="cca35-177">Для элементов управления страниц с вкладками типа DTCT_PAGE элемент **улитемид** (необязательно) используется для загрузки имени компонента страницы из строкового ресурса.</span><span class="sxs-lookup"><span data-stu-id="cca35-177">For tabbed pages controls of type DTCT_PAGE the **ulItemID** member is optionally used to load the component name for the page from a string resource.</span></span> <span data-ttu-id="cca35-178">Сведения о положении и метке считываются из диалогового окна ресурс.</span><span class="sxs-lookup"><span data-stu-id="cca35-178">Position and label information are read from the dialog box resource.</span></span> 
    
<span data-ttu-id="cca35-179">**доверен**</span><span class="sxs-lookup"><span data-stu-id="cca35-179">**ctl**</span></span>
  
> <span data-ttu-id="cca35-180">Структура, содержащая данные для элемента управления и соответствующая свойству **PR_CONTROL_STRUCTURE** элемента управления ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cca35-180">A structure that holds the data for the control and corresponds to the control's **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) property.</span></span> <span data-ttu-id="cca35-181">Каждый тип элемента управления имеет разную структуру.</span><span class="sxs-lookup"><span data-stu-id="cca35-181">Each type of control has a different structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cca35-182">Примечания</span><span class="sxs-lookup"><span data-stu-id="cca35-182">Remarks</span></span>

<span data-ttu-id="cca35-183">Структура **дтктл** описывает один элемент управления любого типа.</span><span class="sxs-lookup"><span data-stu-id="cca35-183">The **DTCTL** structure describes one control of any type.</span></span> <span data-ttu-id="cca35-184">Большинство его членов используются для задания свойств элемента управления.</span><span class="sxs-lookup"><span data-stu-id="cca35-184">Most of its members are used to set properties on the control.</span></span> 
  
<span data-ttu-id="cca35-185">Элемент **CTL** является объединением структур, которые относятся к определенному типу элементов управления.</span><span class="sxs-lookup"><span data-stu-id="cca35-185">The **ctl** member is a union of structures that relate to a particular type of control.</span></span> <span data-ttu-id="cca35-186">Если структура **дтктл** описывает элемент управления для редактирования, например, элемент **CTL** будет указывает на структуру [дтбледит](dtbledit.md) .</span><span class="sxs-lookup"><span data-stu-id="cca35-186">If the **DTCTL** structure is describing an edit control, for example, the **ctl** member will point to a [DTBLEDIT](dtbledit.md) structure.</span></span> <span data-ttu-id="cca35-187">Эта структура соответствует свойству **PR_CONTROL_STRUCTURE** элемента управления.</span><span class="sxs-lookup"><span data-stu-id="cca35-187">This structure corresponds to the control's **PR_CONTROL_STRUCTURE** property.</span></span> <span data-ttu-id="cca35-188">Union имеет в качестве первого члена переменную типа ЛПВОИД, чтобы разрешить инициализацию времени компиляции структуры **дтктл** .</span><span class="sxs-lookup"><span data-stu-id="cca35-188">The union has as its first member a variable of type LPVOID to allow compile time initialization of the **DTCTL** structure.</span></span> 
  
<span data-ttu-id="cca35-189">Несмотря на то, что функция [буилддисплайтабле](builddisplaytable.md) использует структуру **дтктл** для создания таблицы отображения из ресурсов управления, структура **дтктл** никогда не отображается в самой таблице.</span><span class="sxs-lookup"><span data-stu-id="cca35-189">Although the [BuildDisplayTable](builddisplaytable.md) function uses the **DTCTL** structure for building the display table from control resources, the **DTCTL** structure never appears in the display table itself.</span></span> <span data-ttu-id="cca35-190">Эта структура просто предоставляет информацию в **буилддисплайтабле**.</span><span class="sxs-lookup"><span data-stu-id="cca35-190">This structure just supplies information to **BuildDisplayTable**.</span></span>
  
<span data-ttu-id="cca35-191">В элементе **улктлфлагс** четыре флажка DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT влияют только на элементы управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="cca35-191">In the **ulCtlFlags** member, four flags DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT affect edit controls only.</span></span> <span data-ttu-id="cca35-192">Два других DT_REQUIRED и DT_SET_IMMEDIATE влияют на любой редактируемый элемент управления.</span><span class="sxs-lookup"><span data-stu-id="cca35-192">Two others DT_REQUIRED and DT_SET_IMMEDIATE affect any editable control.</span></span> 
  
<span data-ttu-id="cca35-193">Элементы управления, доступные для диалогового окна: Label, текстовое поле, текстовое поле с поддержкой рукописного ввода, список, раскрывающийся список, поле со списком, флажок, группа, кнопка, переключатель и страница с вкладками.</span><span class="sxs-lookup"><span data-stu-id="cca35-193">The controls available for a dialog box are label, text box, ink-aware text box, list, drop-down list, combo box, check box, group box, button, radio button, and tabbed page.</span></span>
  
<span data-ttu-id="cca35-194">Общие сведения о отображаемых таблицах приведены в разделе [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="cca35-194">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="cca35-195">Сведения о том, как реализовать таблицу отображения, можно найти [в статье реализация таблицы отображения](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="cca35-195">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cca35-196">См. также</span><span class="sxs-lookup"><span data-stu-id="cca35-196">See also</span></span>

- [<span data-ttu-id="cca35-197">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="cca35-197">BuildDisplayTable</span></span>](builddisplaytable.md)
- [<span data-ttu-id="cca35-198">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="cca35-198">DTBLBUTTON</span></span>](dtblbutton.md)
- [<span data-ttu-id="cca35-199">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="cca35-199">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="cca35-200">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="cca35-200">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="cca35-201">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="cca35-201">DTBLDDLBX</span></span>](dtblddlbx.md)
- [<span data-ttu-id="cca35-202">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="cca35-202">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="cca35-203">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="cca35-203">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="cca35-204">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="cca35-204">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="cca35-205">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="cca35-205">DTBLLBX</span></span>](dtbllbx.md)
- [<span data-ttu-id="cca35-206">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="cca35-206">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md)
- [<span data-ttu-id="cca35-207">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="cca35-207">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md)
- [<span data-ttu-id="cca35-208">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="cca35-208">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="cca35-209">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="cca35-209">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md)
- [<span data-ttu-id="cca35-210">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="cca35-210">MAPI Structures</span></span>](mapi-structures.md)

