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
# <a name="dtctl"></a><span data-ttu-id="df7f4-103">DTCTL</span><span class="sxs-lookup"><span data-stu-id="df7f4-103">DTCTL</span></span>

<span data-ttu-id="df7f4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df7f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df7f4-105">Описывает управление, которое будет использоваться в диалоговом окне, построенной из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="df7f4-105">Describes a control that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="df7f4-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="df7f4-106">Header file:</span></span>  <br/> |<span data-ttu-id="df7f4-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="df7f4-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="df7f4-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="df7f4-108">Members</span></span>

<span data-ttu-id="df7f4-109">**ulCtlType**</span><span class="sxs-lookup"><span data-stu-id="df7f4-109">**ulCtlType**</span></span>
  
> <span data-ttu-id="df7f4-110">Тип управления, который входит в состав **ctl** и соответствует свойству **PR_CONTROL_TYPE** [(PidTagControlType).](pidtagcontroltype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="df7f4-110">Type of control that is included in the **ctl** member and corresponds to the control's **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) property.</span></span> <span data-ttu-id="df7f4-111">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="df7f4-111">Possible values are as follows:</span></span>
    
<span data-ttu-id="df7f4-112">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="df7f4-112">DTCT_LABEL</span></span> 
  
> <span data-ttu-id="df7f4-113">Управление меткой.</span><span class="sxs-lookup"><span data-stu-id="df7f4-113">Label control.</span></span>
    
<span data-ttu-id="df7f4-114">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="df7f4-114">DTCT_EDIT</span></span> 
  
> <span data-ttu-id="df7f4-115">Изменение управления.</span><span class="sxs-lookup"><span data-stu-id="df7f4-115">Edit control.</span></span>
    
<span data-ttu-id="df7f4-116">DTCT_LBX</span><span class="sxs-lookup"><span data-stu-id="df7f4-116">DTCT_LBX</span></span> 
  
> <span data-ttu-id="df7f4-117">Управление полем списка.</span><span class="sxs-lookup"><span data-stu-id="df7f4-117">List box control.</span></span>
    
<span data-ttu-id="df7f4-118">DTCT_COMBOBOX</span><span class="sxs-lookup"><span data-stu-id="df7f4-118">DTCT_COMBOBOX</span></span> 
  
> <span data-ttu-id="df7f4-119">Управление полем combo.</span><span class="sxs-lookup"><span data-stu-id="df7f4-119">Combo box control.</span></span>
    
<span data-ttu-id="df7f4-120">DTCT_DDLBX</span><span class="sxs-lookup"><span data-stu-id="df7f4-120">DTCT_DDLBX</span></span> 
  
> <span data-ttu-id="df7f4-121">Drop-down list control.</span><span class="sxs-lookup"><span data-stu-id="df7f4-121">Drop-down list control.</span></span>
    
<span data-ttu-id="df7f4-122">DTCT_CHECKBOX</span><span class="sxs-lookup"><span data-stu-id="df7f4-122">DTCT_CHECKBOX</span></span> 
  
> <span data-ttu-id="df7f4-123">Управление полем проверки.</span><span class="sxs-lookup"><span data-stu-id="df7f4-123">Check box control.</span></span>
    
<span data-ttu-id="df7f4-124">DTCT_GROUPBOX</span><span class="sxs-lookup"><span data-stu-id="df7f4-124">DTCT_GROUPBOX</span></span> 
  
> <span data-ttu-id="df7f4-125">Управление групповой коробкой.</span><span class="sxs-lookup"><span data-stu-id="df7f4-125">Group box control.</span></span>
    
<span data-ttu-id="df7f4-126">DTCT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="df7f4-126">DTCT_BUTTON</span></span> 
  
> <span data-ttu-id="df7f4-127">Управление кнопками.</span><span class="sxs-lookup"><span data-stu-id="df7f4-127">Button control.</span></span>
    
<span data-ttu-id="df7f4-128">DTCT_PAGE</span><span class="sxs-lookup"><span data-stu-id="df7f4-128">DTCT_PAGE</span></span> 
  
> <span data-ttu-id="df7f4-129">Управление страницей с вкладками.</span><span class="sxs-lookup"><span data-stu-id="df7f4-129">Tabbed page control.</span></span>
    
<span data-ttu-id="df7f4-130">DTCT_RADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="df7f4-130">DTCT_RADIOBUTTON</span></span> 
  
> <span data-ttu-id="df7f4-131">Управление кнопкой радио.</span><span class="sxs-lookup"><span data-stu-id="df7f4-131">Radio button control.</span></span>
    
<span data-ttu-id="df7f4-132">DTCT_MVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="df7f4-132">DTCT_MVLISTBOX</span></span> 
  
> <span data-ttu-id="df7f4-133">Управление списком с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="df7f4-133">Multi-valued list control.</span></span>
    
<span data-ttu-id="df7f4-134">DTCT_MVDDLBX</span><span class="sxs-lookup"><span data-stu-id="df7f4-134">DTCT_MVDDLBX</span></span> 
  
> <span data-ttu-id="df7f4-135">Управление списком с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="df7f4-135">Multi-valued drop-down list control.</span></span>
    
<span data-ttu-id="df7f4-136">**ulCtlFlags**</span><span class="sxs-lookup"><span data-stu-id="df7f4-136">**ulCtlFlags**</span></span>
  
> <span data-ttu-id="df7f4-137">Битмаски флагов, описывая функции управления и соответствующие свойству PR_CONTROL_FLAGS[(PidTagControlFlags).](pidtagcontrolflags-canonical-property.md) </span><span class="sxs-lookup"><span data-stu-id="df7f4-137">Bitmask of flags that describes the control's features and corresponds to the control's **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="df7f4-138">Эти флаги можно установить только для флажков, комбо-полей, списков и элементов управления.</span><span class="sxs-lookup"><span data-stu-id="df7f4-138">These flags can be set for check boxes, combo boxes, list boxes, and edit controls only.</span></span> <span data-ttu-id="df7f4-139">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="df7f4-139">Possible values are as follows:</span></span>
    
<span data-ttu-id="df7f4-140">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="df7f4-140">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="df7f4-141">Принимается формат ANSI или DBCS.</span><span class="sxs-lookup"><span data-stu-id="df7f4-141">Either the ANSI or DBCS format is accepted.</span></span> <span data-ttu-id="df7f4-142">Этот флаг действителен только для редактирования элементов управления.</span><span class="sxs-lookup"><span data-stu-id="df7f4-142">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="df7f4-143">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="df7f4-143">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="df7f4-144">Пользователь может изменить текст в области управления.</span><span class="sxs-lookup"><span data-stu-id="df7f4-144">A user can modify the text in the control.</span></span> 
    
<span data-ttu-id="df7f4-145">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="df7f4-145">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="df7f4-146">Управление может содержать несколько строк текста.</span><span class="sxs-lookup"><span data-stu-id="df7f4-146">The control can contain multiple text lines.</span></span> <span data-ttu-id="df7f4-147">Этот флаг действителен только для редактирования элементов управления.</span><span class="sxs-lookup"><span data-stu-id="df7f4-147">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="df7f4-148">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="df7f4-148">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="df7f4-149">Управление содержит пароль; поэтому содержимое управления не должно отображаться пользователю.</span><span class="sxs-lookup"><span data-stu-id="df7f4-149">The control contains a password; therefore, the contents of the control should not be displayed to the user.</span></span> <span data-ttu-id="df7f4-150">Этот флаг действителен только для редактирования элементов управления.</span><span class="sxs-lookup"><span data-stu-id="df7f4-150">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="df7f4-151">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="df7f4-151">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="df7f4-152">Требуется управление диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="df7f4-152">The dialog box control is required.</span></span> <span data-ttu-id="df7f4-153">Этот флаг действителен только для элементов управления полем редактирования и комбо.</span><span class="sxs-lookup"><span data-stu-id="df7f4-153">This flag is valid only for edit and combo box controls.</span></span>
    
<span data-ttu-id="df7f4-154">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="df7f4-154">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="df7f4-155">Включает немедленный выход значения при изменении управления.</span><span class="sxs-lookup"><span data-stu-id="df7f4-155">Enables immediate output of a value upon a change in the control.</span></span> <span data-ttu-id="df7f4-156">Это позволяет установить связь зависимости между двумя средствами управления.</span><span class="sxs-lookup"><span data-stu-id="df7f4-156">This allows a dependency relationship to be established between two controls.</span></span> 
    
<span data-ttu-id="df7f4-157">**lpbNotif**</span><span class="sxs-lookup"><span data-stu-id="df7f4-157">**lpbNotif**</span></span>
  
> <span data-ttu-id="df7f4-158">Указатель на структуру, состоящую из [структуры GUID,](guid.md) для представления поставщика услуг и идентификатора для управления.</span><span class="sxs-lookup"><span data-stu-id="df7f4-158">Pointer to a structure that consists of a [GUID](guid.md) structure, to represent the service provider and an identifier for the control.</span></span> <span data-ttu-id="df7f4-159">Члены **lpbNotif** и **cbNotif** соответствуют свойству PR_CONTROL_ID [(PidTagControlId)](pidtagcontrolid-canonical-property.md)и используются для уведомления пользовательского интерфейса при обновлении управления. </span><span class="sxs-lookup"><span data-stu-id="df7f4-159">The **lpbNotif** and **cbNotif** members correspond to the control's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property and are used to notify the user interface when the control has to be updated.</span></span>
    
<span data-ttu-id="df7f4-160">**cbNotif**</span><span class="sxs-lookup"><span data-stu-id="df7f4-160">**cbNotif**</span></span>
  
> <span data-ttu-id="df7f4-161">Количество bytes в структуре, на который указывает член **lpbNotif.**</span><span class="sxs-lookup"><span data-stu-id="df7f4-161">Count of bytes in the structure pointed to by the **lpbNotif** member.</span></span> 
    
<span data-ttu-id="df7f4-162">**lpszFilter**</span><span class="sxs-lookup"><span data-stu-id="df7f4-162">**lpszFilter**</span></span>
  
> <span data-ttu-id="df7f4-163">Указатель на строку символов, которая описывает, какие символы можно вправить или комбо-поле управления.</span><span class="sxs-lookup"><span data-stu-id="df7f4-163">Pointer to a character string that describes which characters can be entered into an edit or combo box control.</span></span> <span data-ttu-id="df7f4-164">Для других типов элементов управления **член lpszFilter** может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="df7f4-164">For other types of controls, the **lpszFilter** member can be NULL.</span></span> <span data-ttu-id="df7f4-165">Для элементов управления полем редактирования и комбо оно должно быть регулярным выражением, которое применяется к одному символу одновременно.</span><span class="sxs-lookup"><span data-stu-id="df7f4-165">For edit and combo box controls, it should be a regular expression that applies to a single character at a time.</span></span> <span data-ttu-id="df7f4-166">Один и тот же фильтр применяется к всем символам управления.</span><span class="sxs-lookup"><span data-stu-id="df7f4-166">The same filter is applied to all characters in the control.</span></span> <span data-ttu-id="df7f4-167">Формат строки фильтра следующим образом:</span><span class="sxs-lookup"><span data-stu-id="df7f4-167">The format of the filter string is as follows:</span></span> 
    
|<span data-ttu-id="df7f4-168">**Символ**</span><span class="sxs-lookup"><span data-stu-id="df7f4-168">**Character**</span></span>|<span data-ttu-id="df7f4-169">**Описание**</span><span class="sxs-lookup"><span data-stu-id="df7f4-169">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> | <span data-ttu-id="df7f4-170">Разрешен любой символ (например, `"*"` ).</span><span class="sxs-lookup"><span data-stu-id="df7f4-170">Any character is allowed (for example, `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="df7f4-171">Определяет набор символов (например, `"[0123456789]"` .)</span><span class="sxs-lookup"><span data-stu-id="df7f4-171">Defines a set of characters (for example, `"[0123456789]"`.)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="df7f4-172">Указывает диапазон символов (например, `"[a-z]"` ).</span><span class="sxs-lookup"><span data-stu-id="df7f4-172">Indicates a range of characters (for example, `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="df7f4-173">Указывает, что эти символы не разрешены (например, `"[~0-9]")` .</span><span class="sxs-lookup"><span data-stu-id="df7f4-173">Indicates that these characters are not allowed (for example, `"[~0-9]")`.</span></span> <br/>|   
| `\` <br/> |<span data-ttu-id="df7f4-174">Используется для цитаты любого из предыдущих символов (например, разрешены знаки `"[\-\\\[\]]"` -, \, [и ]).</span><span class="sxs-lookup"><span data-stu-id="df7f4-174">Used to quote any of the previous symbols (for example, `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
<span data-ttu-id="df7f4-175">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="df7f4-175">**ulItemID**</span></span>
  
> <span data-ttu-id="df7f4-176">Значение, определяее управление в диалоговом окне ресурса.</span><span class="sxs-lookup"><span data-stu-id="df7f4-176">Value that identifies the control in the dialog box resource.</span></span> <span data-ttu-id="df7f4-177">Для элементов управления страницами типа DTCT_PAGE **элемент ulItemID** необязательно используется для загрузки имени компонента для страницы из строки ресурса.</span><span class="sxs-lookup"><span data-stu-id="df7f4-177">For tabbed pages controls of type DTCT_PAGE the **ulItemID** member is optionally used to load the component name for the page from a string resource.</span></span> <span data-ttu-id="df7f4-178">Сведения о позиции и метке считыются из ресурса диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="df7f4-178">Position and label information are read from the dialog box resource.</span></span> 
    
<span data-ttu-id="df7f4-179">**ctl**</span><span class="sxs-lookup"><span data-stu-id="df7f4-179">**ctl**</span></span>
  
> <span data-ttu-id="df7f4-180">Структура, которая содержит данные для управления и соответствует свойству **PR_CONTROL_STRUCTURE** [(PidTagControlStructure).](pidtagcontrolstructure-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="df7f4-180">A structure that holds the data for the control and corresponds to the control's **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) property.</span></span> <span data-ttu-id="df7f4-181">Каждый тип управления имеет другую структуру.</span><span class="sxs-lookup"><span data-stu-id="df7f4-181">Each type of control has a different structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="df7f4-182">Примечания</span><span class="sxs-lookup"><span data-stu-id="df7f4-182">Remarks</span></span>

<span data-ttu-id="df7f4-183">Структура **DTCTL** описывает один контроль любого типа.</span><span class="sxs-lookup"><span data-stu-id="df7f4-183">The **DTCTL** structure describes one control of any type.</span></span> <span data-ttu-id="df7f4-184">Большинство его членов используются для набора свойств на пульте управления.</span><span class="sxs-lookup"><span data-stu-id="df7f4-184">Most of its members are used to set properties on the control.</span></span> 
  
<span data-ttu-id="df7f4-185">Член **ctl** — это объединение структур, которые относятся к определенному типу управления.</span><span class="sxs-lookup"><span data-stu-id="df7f4-185">The **ctl** member is a union of structures that relate to a particular type of control.</span></span> <span data-ttu-id="df7f4-186">Если в **структуре DTCTL** описывается управление изменением, например, участник **ctl** будет указать на [структуру DTBLEDIT.](dtbledit.md)</span><span class="sxs-lookup"><span data-stu-id="df7f4-186">If the **DTCTL** structure is describing an edit control, for example, the **ctl** member will point to a [DTBLEDIT](dtbledit.md) structure.</span></span> <span data-ttu-id="df7f4-187">Эта структура соответствует свойству PR_CONTROL_STRUCTURE **управления.**</span><span class="sxs-lookup"><span data-stu-id="df7f4-187">This structure corresponds to the control's **PR_CONTROL_STRUCTURE** property.</span></span> <span data-ttu-id="df7f4-188">Профсоюз имеет в качестве первого члена переменную типа LPVOID, позволяющую инициализации времени компилировать **структуру DTCTL.**</span><span class="sxs-lookup"><span data-stu-id="df7f4-188">The union has as its first member a variable of type LPVOID to allow compile time initialization of the **DTCTL** structure.</span></span> 
  
<span data-ttu-id="df7f4-189">Хотя функция [BuildDisplayTable](builddisplaytable.md) использует структуру **DTCTL** для построения таблицы отображения из ресурсов управления, структура **DTCTL** никогда не отображается в самой таблице отображения.</span><span class="sxs-lookup"><span data-stu-id="df7f4-189">Although the [BuildDisplayTable](builddisplaytable.md) function uses the **DTCTL** structure for building the display table from control resources, the **DTCTL** structure never appears in the display table itself.</span></span> <span data-ttu-id="df7f4-190">Эта структура просто поставляет сведения **в BuildDisplayTable**.</span><span class="sxs-lookup"><span data-stu-id="df7f4-190">This structure just supplies information to **BuildDisplayTable**.</span></span>
  
<span data-ttu-id="df7f4-191">В **члене ulCtlFlags** четыре флага DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT влияют только на элементы управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="df7f4-191">In the **ulCtlFlags** member, four flags DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT affect edit controls only.</span></span> <span data-ttu-id="df7f4-192">Два других DT_REQUIRED и DT_SET_IMMEDIATE могут повлиять на любой редактурируемый контроль.</span><span class="sxs-lookup"><span data-stu-id="df7f4-192">Two others DT_REQUIRED and DT_SET_IMMEDIATE affect any editable control.</span></span> 
  
<span data-ttu-id="df7f4-193">Элементы управления, доступные для диалогового окна: метка, текстовое поле, список, комбо-поле, контрольное окно, групповое поле, кнопка, кнопка, кнопка радио и страница вкладки.</span><span class="sxs-lookup"><span data-stu-id="df7f4-193">The controls available for a dialog box are label, text box, ink-aware text box, list, drop-down list, combo box, check box, group box, button, radio button, and tabbed page.</span></span>
  
<span data-ttu-id="df7f4-194">Обзор таблиц отображения см. в таблице [Display Tables.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="df7f4-194">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="df7f4-195">Сведения о реализации таблицы отображения см. в таблице [Implementing a Display Table.](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="df7f4-195">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="df7f4-196">См. также</span><span class="sxs-lookup"><span data-stu-id="df7f4-196">See also</span></span>

- [<span data-ttu-id="df7f4-197">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="df7f4-197">BuildDisplayTable</span></span>](builddisplaytable.md)
- [<span data-ttu-id="df7f4-198">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="df7f4-198">DTBLBUTTON</span></span>](dtblbutton.md)
- [<span data-ttu-id="df7f4-199">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="df7f4-199">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="df7f4-200">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="df7f4-200">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="df7f4-201">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="df7f4-201">DTBLDDLBX</span></span>](dtblddlbx.md)
- [<span data-ttu-id="df7f4-202">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="df7f4-202">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="df7f4-203">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="df7f4-203">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="df7f4-204">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="df7f4-204">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="df7f4-205">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="df7f4-205">DTBLLBX</span></span>](dtbllbx.md)
- [<span data-ttu-id="df7f4-206">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="df7f4-206">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md)
- [<span data-ttu-id="df7f4-207">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="df7f4-207">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md)
- [<span data-ttu-id="df7f4-208">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="df7f4-208">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="df7f4-209">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="df7f4-209">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md)
- [<span data-ttu-id="df7f4-210">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="df7f4-210">MAPI Structures</span></span>](mapi-structures.md)

