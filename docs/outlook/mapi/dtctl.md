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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 68c621f5f73073ed127767cc1db189769dab227d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808389"
---
# <a name="dtctl"></a><span data-ttu-id="f2e5f-103">DTCTL</span><span class="sxs-lookup"><span data-stu-id="f2e5f-103">DTCTL</span></span>

<span data-ttu-id="f2e5f-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f2e5f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f2e5f-105">Описывает элемент управления, который будет использоваться в диалоговое окно, построенная на основе таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-105">Describes a control that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f2e5f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f2e5f-106">Header file:</span></span>  <br/> |<span data-ttu-id="f2e5f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f2e5f-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="f2e5f-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="f2e5f-108">Members</span></span>

<span data-ttu-id="f2e5f-109">**ulCtlType**</span><span class="sxs-lookup"><span data-stu-id="f2e5f-109">**ulCtlType**</span></span>
  
> <span data-ttu-id="f2e5f-110">Тип элемента управления, который включен в **список доверия сертификатов** член и соответствует свойству **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) элемента управления.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-110">Type of control that is included in the **ctl** member and corresponds to the control's **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) property.</span></span> <span data-ttu-id="f2e5f-111">Ниже приведены возможные значения:</span><span class="sxs-lookup"><span data-stu-id="f2e5f-111">Possible values are as follows:</span></span>
    
<span data-ttu-id="f2e5f-112">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="f2e5f-112">DTCT_LABEL</span></span> 
  
> <span data-ttu-id="f2e5f-113">Элемент управления Label.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-113">Label control.</span></span>
    
<span data-ttu-id="f2e5f-114">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="f2e5f-114">DTCT_EDIT</span></span> 
  
> <span data-ttu-id="f2e5f-115">Изменение элемента управления.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-115">Edit control.</span></span>
    
<span data-ttu-id="f2e5f-116">DTCT_LBX</span><span class="sxs-lookup"><span data-stu-id="f2e5f-116">DTCT_LBX</span></span> 
  
> <span data-ttu-id="f2e5f-117">Окно списка.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-117">List box control.</span></span>
    
<span data-ttu-id="f2e5f-118">DTCT_COMBOBOX</span><span class="sxs-lookup"><span data-stu-id="f2e5f-118">DTCT_COMBOBOX</span></span> 
  
> <span data-ttu-id="f2e5f-119">Элемент управления ComboBox.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-119">Combo box control.</span></span>
    
<span data-ttu-id="f2e5f-120">DTCT_DDLBX</span><span class="sxs-lookup"><span data-stu-id="f2e5f-120">DTCT_DDLBX</span></span> 
  
> <span data-ttu-id="f2e5f-121">Элемент управления раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-121">Drop-down list control.</span></span>
    
<span data-ttu-id="f2e5f-122">DTCT_CHECKBOX</span><span class="sxs-lookup"><span data-stu-id="f2e5f-122">DTCT_CHECKBOX</span></span> 
  
> <span data-ttu-id="f2e5f-123">Элемент управления "флажок".</span><span class="sxs-lookup"><span data-stu-id="f2e5f-123">Check box control.</span></span>
    
<span data-ttu-id="f2e5f-124">DTCT_GROUPBOX</span><span class="sxs-lookup"><span data-stu-id="f2e5f-124">DTCT_GROUPBOX</span></span> 
  
> <span data-ttu-id="f2e5f-125">Элемент управления поля группы.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-125">Group box control.</span></span>
    
<span data-ttu-id="f2e5f-126">DTCT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="f2e5f-126">DTCT_BUTTON</span></span> 
  
> <span data-ttu-id="f2e5f-127">Элемент управления Button.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-127">Button control.</span></span>
    
<span data-ttu-id="f2e5f-128">DTCT_PAGE</span><span class="sxs-lookup"><span data-stu-id="f2e5f-128">DTCT_PAGE</span></span> 
  
> <span data-ttu-id="f2e5f-129">Элемент управления страницы с вкладками.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-129">Tabbed page control.</span></span>
    
<span data-ttu-id="f2e5f-130">DTCT_RADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="f2e5f-130">DTCT_RADIOBUTTON</span></span> 
  
> <span data-ttu-id="f2e5f-131">Управления "переключатель".</span><span class="sxs-lookup"><span data-stu-id="f2e5f-131">Radio button control.</span></span>
    
<span data-ttu-id="f2e5f-132">DTCT_MVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="f2e5f-132">DTCT_MVLISTBOX</span></span> 
  
> <span data-ttu-id="f2e5f-133">Элемент управления, поддерживающий несколько значений списка.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-133">Multi-valued list control.</span></span>
    
<span data-ttu-id="f2e5f-134">DTCT_MVDDLBX</span><span class="sxs-lookup"><span data-stu-id="f2e5f-134">DTCT_MVDDLBX</span></span> 
  
> <span data-ttu-id="f2e5f-135">Элемент управления, поддерживающий несколько значений раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-135">Multi-valued drop-down list control.</span></span>
    
<span data-ttu-id="f2e5f-136">**ulCtlFlags**</span><span class="sxs-lookup"><span data-stu-id="f2e5f-136">**ulCtlFlags**</span></span>
  
> <span data-ttu-id="f2e5f-137">Битовая маска флаги с описанием функций элемента управления и соответствует свойству **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) элемента управления.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-137">Bitmask of flags that describes the control's features and corresponds to the control's **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="f2e5f-138">Эти флаги можно задать для флажки, поля со списками, списков и изменить только элементы управления.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-138">These flags can be set for check boxes, combo boxes, list boxes, and edit controls only.</span></span> <span data-ttu-id="f2e5f-139">Ниже приведены возможные значения:</span><span class="sxs-lookup"><span data-stu-id="f2e5f-139">Possible values are as follows:</span></span>
    
<span data-ttu-id="f2e5f-140">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="f2e5f-140">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="f2e5f-141">Допускается формата ANSI или DBCS.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-141">Either the ANSI or DBCS format is accepted.</span></span> <span data-ttu-id="f2e5f-142">Этот флаг является допустимым редактирования только для элементов управления.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-142">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="f2e5f-143">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="f2e5f-143">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="f2e5f-144">Пользователь может изменить текст в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-144">A user can modify the text in the control.</span></span> 
    
<span data-ttu-id="f2e5f-145">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="f2e5f-145">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="f2e5f-146">Элемент управления может содержать несколько строк текста.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-146">The control can contain multiple text lines.</span></span> <span data-ttu-id="f2e5f-147">Этот флаг является допустимым редактирования только для элементов управления.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-147">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="f2e5f-148">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="f2e5f-148">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="f2e5f-149">Элемент управления содержит пароль; Таким образом содержимое элемента управления не должен отображаться для пользователя.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-149">The control contains a password; therefore, the contents of the control should not be displayed to the user.</span></span> <span data-ttu-id="f2e5f-150">Этот флаг является допустимым редактирования только для элементов управления.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-150">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="f2e5f-151">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="f2e5f-151">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="f2e5f-152">Элемент управления полем диалоговое окно является обязательным.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-152">The dialog box control is required.</span></span> <span data-ttu-id="f2e5f-153">Этот флаг является допустимым только для элементов управления редактирования и поля со списком.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-153">This flag is valid only for edit and combo box controls.</span></span>
    
<span data-ttu-id="f2e5f-154">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="f2e5f-154">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="f2e5f-155">Включение Интерпретация выходных данных, значение при изменении в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-155">Enables immediate output of a value upon a change in the control.</span></span> <span data-ttu-id="f2e5f-156">Это позволяет отношения зависимости соединения между двумя элементами управления.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-156">This allows a dependency relationship to be established between two controls.</span></span> 
    
<span data-ttu-id="f2e5f-157">**lpbNotif**</span><span class="sxs-lookup"><span data-stu-id="f2e5f-157">**lpbNotif**</span></span>
  
> <span data-ttu-id="f2e5f-158">Указатель на структуру, которая состоит из структуру [идентификатор GUID](guid.md) для представления поставщика услуг и идентификатор для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-158">Pointer to a structure that consists of a [GUID](guid.md) structure, to represent the service provider and an identifier for the control.</span></span> <span data-ttu-id="f2e5f-159">Члены **lpbNotif** и **cbNotif** соответствуют свойства **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) и использовать для уведомления пользовательского интерфейса, когда элемент управления имеет должны обновляться.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-159">The **lpbNotif** and **cbNotif** members correspond to the control's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property and are used to notify the user interface when the control has to be updated.</span></span>
    
<span data-ttu-id="f2e5f-160">**cbNotif**</span><span class="sxs-lookup"><span data-stu-id="f2e5f-160">**cbNotif**</span></span>
  
> <span data-ttu-id="f2e5f-161">Число байт в структуре, на который указывает член **lpbNotif** .</span><span class="sxs-lookup"><span data-stu-id="f2e5f-161">Count of bytes in the structure pointed to by the **lpbNotif** member.</span></span> 
    
<span data-ttu-id="f2e5f-162">**lpszFilter**</span><span class="sxs-lookup"><span data-stu-id="f2e5f-162">**lpszFilter**</span></span>
  
> <span data-ttu-id="f2e5f-163">Указатель на строку символов, которая описывается, какие символы можно ввести в элемент управления поля со списком или изменить.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-163">Pointer to a character string that describes which characters can be entered into an edit or combo box control.</span></span> <span data-ttu-id="f2e5f-164">Для других типов элементов управления **lpszFilter** участник может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-164">For other types of controls, the **lpszFilter** member can be NULL.</span></span> <span data-ttu-id="f2e5f-165">Для редактирования и поля со списком элементов управления следует регулярное выражение, которое применяется к один символ за раз.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-165">For edit and combo box controls, it should be a regular expression that applies to a single character at a time.</span></span> <span data-ttu-id="f2e5f-166">Тот же фильтр будет применяться ко всем символов в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-166">The same filter is applied to all characters in the control.</span></span> <span data-ttu-id="f2e5f-167">Формат строки фильтра выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f2e5f-167">The format of the filter string is as follows:</span></span> 
    
|<span data-ttu-id="f2e5f-168">**Символ**</span><span class="sxs-lookup"><span data-stu-id="f2e5f-168">**Character**</span></span>|<span data-ttu-id="f2e5f-169">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f2e5f-169">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> | <span data-ttu-id="f2e5f-170">Допускается любой символ (например, `"*"`).</span><span class="sxs-lookup"><span data-stu-id="f2e5f-170">Any character is allowed (for example, `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="f2e5f-171">Определяет набор символов (например, `"[0123456789]"`.)</span><span class="sxs-lookup"><span data-stu-id="f2e5f-171">Defines a set of characters (for example, `"[0123456789]"`.)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="f2e5f-172">Указывает диапазон символов (например, `"[a-z]"`).</span><span class="sxs-lookup"><span data-stu-id="f2e5f-172">Indicates a range of characters (for example, `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="f2e5f-173">Указывает, что эти символы не разрешены (например, `"[~0-9]")`.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-173">Indicates that these characters are not allowed (for example, `"[~0-9]")`.</span></span> <br/>|   
| `\` <br/> |<span data-ttu-id="f2e5f-174">Используется для любой из предыдущих символы кавычек (например, `"[\-\\\[\]]"` означает, что-, \, [, и] могут знаков).</span><span class="sxs-lookup"><span data-stu-id="f2e5f-174">Used to quote any of the previous symbols (for example, `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
<span data-ttu-id="f2e5f-175">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="f2e5f-175">**ulItemID**</span></span>
  
> <span data-ttu-id="f2e5f-176">Значение, идентифицирующее элемент управления в ресурс диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-176">Value that identifies the control in the dialog box resource.</span></span> <span data-ttu-id="f2e5f-177">Для элементов управления страниц с вкладками типа DTCT_PAGE **ulItemID** член при необходимости используется для загрузки имя компонента страницы из строки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-177">For tabbed pages controls of type DTCT_PAGE the **ulItemID** member is optionally used to load the component name for the page from a string resource.</span></span> <span data-ttu-id="f2e5f-178">Положение и сведения о метке считываются из ресурс диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-178">Position and label information are read from the dialog box resource.</span></span> 
    
<span data-ttu-id="f2e5f-179">**список доверия сертификатов**</span><span class="sxs-lookup"><span data-stu-id="f2e5f-179">**ctl**</span></span>
  
> <span data-ttu-id="f2e5f-180">Структура, которая содержит данные для элемента управления и соответствует свойству **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) элемента управления.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-180">A structure that holds the data for the control and corresponds to the control's **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) property.</span></span> <span data-ttu-id="f2e5f-181">Каждый тип элемента управления имеет другую структуру.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-181">Each type of control has a different structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f2e5f-182">Замечания</span><span class="sxs-lookup"><span data-stu-id="f2e5f-182">Remarks</span></span>

<span data-ttu-id="f2e5f-183">Структура **DTCTL** описывает один элемент управления любого типа.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-183">The **DTCTL** structure describes one control of any type.</span></span> <span data-ttu-id="f2e5f-184">Большая часть его члены используются для задания свойств элемента управления.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-184">Most of its members are used to set properties on the control.</span></span> 
  
<span data-ttu-id="f2e5f-185">Член **список доверия сертификатов** — это объединение структуры, относящиеся к определенным типом элемента управления.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-185">The **ctl** member is a union of structures that relate to a particular type of control.</span></span> <span data-ttu-id="f2e5f-186">Если структура **DTCTL** — это описания элемента управления, например, член **список доверия сертификатов** будет наведите указатель мыши [DTBLEDIT](dtbledit.md) структуры.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-186">If the **DTCTL** structure is describing an edit control, for example, the **ctl** member will point to a [DTBLEDIT](dtbledit.md) structure.</span></span> <span data-ttu-id="f2e5f-187">Эта структура соответствует свойству **PR_CONTROL_STRUCTURE** элемента управления.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-187">This structure corresponds to the control's **PR_CONTROL_STRUCTURE** property.</span></span> <span data-ttu-id="f2e5f-188">Объединение имеет его, входящей в первой переменной типа LPVOID, чтобы разрешить инициализацию времени компиляции **DTCTL** структуры.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-188">The union has as its first member a variable of type LPVOID to allow compile time initialization of the **DTCTL** structure.</span></span> 
  
<span data-ttu-id="f2e5f-189">Несмотря на то, что функция [BuildDisplayTable](builddisplaytable.md) использует структуру **DTCTL** для построения в таблице отображения из элемента управления ресурсами, структура **DTCTL** никогда не отображается в самой таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-189">Although the [BuildDisplayTable](builddisplaytable.md) function uses the **DTCTL** structure for building the display table from control resources, the **DTCTL** structure never appears in the display table itself.</span></span> <span data-ttu-id="f2e5f-190">Эта структура только что предоставляет сведения о **BuildDisplayTable**.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-190">This structure just supplies information to **BuildDisplayTable**.</span></span>
  
<span data-ttu-id="f2e5f-191">Элемент **ulCtlFlags** четыре флаги DT_ACCEPT_DBCS, DT_EDITABLE, влияющие на DT_MULTILINE_and DT_PASSWORD_EDIT изменить только элементы управления.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-191">In the **ulCtlFlags** member, four flags DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT affect edit controls only.</span></span> <span data-ttu-id="f2e5f-192">Два других пользователей DT_REQUIRED и DT_SET_IMMEDIATE влияет на любой редактируемом элементе управления.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-192">Two others DT_REQUIRED and DT_SET_IMMEDIATE affect any editable control.</span></span> 
  
<span data-ttu-id="f2e5f-193">Элементы управления, доступные для диалогового окна, метки, текстовое поле, принять во внимание рукописного ввода текстовое поле, список, раскрывающегося списка, поля со списком, флажок, поле группы, кнопка, переключатель и страницы с вкладками.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-193">The controls available for a dialog box are label, text box, ink-aware text box, list, drop-down list, combo box, check box, group box, button, radio button, and tabbed page.</span></span>
  
<span data-ttu-id="f2e5f-194">Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f2e5f-194">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="f2e5f-195">Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.</span><span class="sxs-lookup"><span data-stu-id="f2e5f-195">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f2e5f-196">См. также</span><span class="sxs-lookup"><span data-stu-id="f2e5f-196">See also</span></span>

- [<span data-ttu-id="f2e5f-197">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="f2e5f-197">BuildDisplayTable</span></span>](builddisplaytable.md)
- [<span data-ttu-id="f2e5f-198">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="f2e5f-198">DTBLBUTTON</span></span>](dtblbutton.md)
- [<span data-ttu-id="f2e5f-199">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="f2e5f-199">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="f2e5f-200">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="f2e5f-200">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="f2e5f-201">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="f2e5f-201">DTBLDDLBX</span></span>](dtblddlbx.md)
- [<span data-ttu-id="f2e5f-202">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="f2e5f-202">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="f2e5f-203">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="f2e5f-203">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="f2e5f-204">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="f2e5f-204">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="f2e5f-205">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="f2e5f-205">DTBLLBX</span></span>](dtbllbx.md)
- [<span data-ttu-id="f2e5f-206">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="f2e5f-206">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md)
- [<span data-ttu-id="f2e5f-207">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="f2e5f-207">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md)
- [<span data-ttu-id="f2e5f-208">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="f2e5f-208">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="f2e5f-209">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="f2e5f-209">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md)
- [<span data-ttu-id="f2e5f-210">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="f2e5f-210">MAPI Structures</span></span>](mapi-structures.md)

