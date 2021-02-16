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
# <a name="dtctl"></a><span data-ttu-id="dc8b8-103">DTCTL</span><span class="sxs-lookup"><span data-stu-id="dc8b8-103">DTCTL</span></span>

<span data-ttu-id="dc8b8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc8b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc8b8-105">Описывается управление, которое будет использоваться в диалоговом окне, построенного из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-105">Describes a control that will be used in a dialog box built from a display table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dc8b8-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="dc8b8-106">Header file:</span></span>  <br/> |<span data-ttu-id="dc8b8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dc8b8-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="dc8b8-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="dc8b8-108">Members</span></span>

<span data-ttu-id="dc8b8-109">**ulCtlType**</span><span class="sxs-lookup"><span data-stu-id="dc8b8-109">**ulCtlType**</span></span>
  
> <span data-ttu-id="dc8b8-110">Тип управления, включенный в член **ctl** и соответствующий  свойству PR_CONTROL_TYPE [(PidTagControlType).](pidtagcontroltype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="dc8b8-110">Type of control that is included in the **ctl** member and corresponds to the control's **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) property.</span></span> <span data-ttu-id="dc8b8-111">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="dc8b8-111">Possible values are as follows:</span></span>
    
<span data-ttu-id="dc8b8-112">DTCT_LABEL</span><span class="sxs-lookup"><span data-stu-id="dc8b8-112">DTCT_LABEL</span></span> 
  
> <span data-ttu-id="dc8b8-113">Управление меткой.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-113">Label control.</span></span>
    
<span data-ttu-id="dc8b8-114">DTCT_EDIT</span><span class="sxs-lookup"><span data-stu-id="dc8b8-114">DTCT_EDIT</span></span> 
  
> <span data-ttu-id="dc8b8-115">Изменение управления.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-115">Edit control.</span></span>
    
<span data-ttu-id="dc8b8-116">DTCT_LBX</span><span class="sxs-lookup"><span data-stu-id="dc8b8-116">DTCT_LBX</span></span> 
  
> <span data-ttu-id="dc8b8-117">Управление списком.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-117">List box control.</span></span>
    
<span data-ttu-id="dc8b8-118">DTCT_COMBOBOX</span><span class="sxs-lookup"><span data-stu-id="dc8b8-118">DTCT_COMBOBOX</span></span> 
  
> <span data-ttu-id="dc8b8-119">Управление полем со combo.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-119">Combo box control.</span></span>
    
<span data-ttu-id="dc8b8-120">DTCT_DDLBX</span><span class="sxs-lookup"><span data-stu-id="dc8b8-120">DTCT_DDLBX</span></span> 
  
> <span data-ttu-id="dc8b8-121">Drop-down list control.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-121">Drop-down list control.</span></span>
    
<span data-ttu-id="dc8b8-122">DTCT_CHECKBOX</span><span class="sxs-lookup"><span data-stu-id="dc8b8-122">DTCT_CHECKBOX</span></span> 
  
> <span data-ttu-id="dc8b8-123">Контрольный окне.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-123">Check box control.</span></span>
    
<span data-ttu-id="dc8b8-124">DTCT_GROUPBOX</span><span class="sxs-lookup"><span data-stu-id="dc8b8-124">DTCT_GROUPBOX</span></span> 
  
> <span data-ttu-id="dc8b8-125">Групповое поле.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-125">Group box control.</span></span>
    
<span data-ttu-id="dc8b8-126">DTCT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="dc8b8-126">DTCT_BUTTON</span></span> 
  
> <span data-ttu-id="dc8b8-127">Кнопка управления.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-127">Button control.</span></span>
    
<span data-ttu-id="dc8b8-128">DTCT_PAGE</span><span class="sxs-lookup"><span data-stu-id="dc8b8-128">DTCT_PAGE</span></span> 
  
> <span data-ttu-id="dc8b8-129">Tabbed page control.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-129">Tabbed page control.</span></span>
    
<span data-ttu-id="dc8b8-130">DTCT_RADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="dc8b8-130">DTCT_RADIOBUTTON</span></span> 
  
> <span data-ttu-id="dc8b8-131">Управление кнопками.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-131">Radio button control.</span></span>
    
<span data-ttu-id="dc8b8-132">DTCT_MVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="dc8b8-132">DTCT_MVLISTBOX</span></span> 
  
> <span data-ttu-id="dc8b8-133">Много значений для управления списком.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-133">Multi-valued list control.</span></span>
    
<span data-ttu-id="dc8b8-134">DTCT_MVDDLBX</span><span class="sxs-lookup"><span data-stu-id="dc8b8-134">DTCT_MVDDLBX</span></span> 
  
> <span data-ttu-id="dc8b8-135">Много значений для выпадаемого списка.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-135">Multi-valued drop-down list control.</span></span>
    
<span data-ttu-id="dc8b8-136">**ulCtlFlags**</span><span class="sxs-lookup"><span data-stu-id="dc8b8-136">**ulCtlFlags**</span></span>
  
> <span data-ttu-id="dc8b8-137">Битовая маской флагов, которая описывает функции управления и соответствует свойству **PR_CONTROL_FLAGS** ([PidTagControlFlags).](pidtagcontrolflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="dc8b8-137">Bitmask of flags that describes the control's features and corresponds to the control's **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) property.</span></span> <span data-ttu-id="dc8b8-138">Эти флаги можно установить только для флажков, полей со списком, списков и элементов управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-138">These flags can be set for check boxes, combo boxes, list boxes, and edit controls only.</span></span> <span data-ttu-id="dc8b8-139">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="dc8b8-139">Possible values are as follows:</span></span>
    
<span data-ttu-id="dc8b8-140">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="dc8b8-140">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="dc8b8-141">Принимается формат ANSI или DBCS.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-141">Either the ANSI or DBCS format is accepted.</span></span> <span data-ttu-id="dc8b8-142">Этот флаг действителен только для элементов управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-142">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="dc8b8-143">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="dc8b8-143">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="dc8b8-144">Пользователь может изменить текст в окнах.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-144">A user can modify the text in the control.</span></span> 
    
<span data-ttu-id="dc8b8-145">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="dc8b8-145">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="dc8b8-146">Этот контроль может содержать несколько текстовых строк.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-146">The control can contain multiple text lines.</span></span> <span data-ttu-id="dc8b8-147">Этот флаг действителен только для элементов управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-147">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="dc8b8-148">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="dc8b8-148">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="dc8b8-149">Этот контроль содержит пароль; Следовательно, содержимое этого управления не должно отображаться для пользователя.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-149">The control contains a password; therefore, the contents of the control should not be displayed to the user.</span></span> <span data-ttu-id="dc8b8-150">Этот флаг действителен только для элементов управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-150">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="dc8b8-151">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="dc8b8-151">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="dc8b8-152">Необходимое поле управления диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-152">The dialog box control is required.</span></span> <span data-ttu-id="dc8b8-153">Этот флаг действителен только для элементов управления "Изменить" и "Поле со combo".</span><span class="sxs-lookup"><span data-stu-id="dc8b8-153">This flag is valid only for edit and combo box controls.</span></span>
    
<span data-ttu-id="dc8b8-154">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="dc8b8-154">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="dc8b8-155">Включает немедленные выходные данные значения при изменении в контроле.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-155">Enables immediate output of a value upon a change in the control.</span></span> <span data-ttu-id="dc8b8-156">Это позволяет установить отношение зависимостей между двумя средствами управления.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-156">This allows a dependency relationship to be established between two controls.</span></span> 
    
<span data-ttu-id="dc8b8-157">**lpbNotif**</span><span class="sxs-lookup"><span data-stu-id="dc8b8-157">**lpbNotif**</span></span>
  
> <span data-ttu-id="dc8b8-158">Указатель на структуру, состоящую из [структуры GUID,](guid.md) которая представляет поставщика услуг и идентификатор для управления.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-158">Pointer to a structure that consists of a [GUID](guid.md) structure, to represent the service provider and an identifier for the control.</span></span> <span data-ttu-id="dc8b8-159">Члены **lpbNotif** и **cbNotif** соответствуют свойству **PR_CONTROL_ID** [(PidTagControlId)](pidtagcontrolid-canonical-property.md)и используются для уведомления пользовательского интерфейса о том, что необходимо обновить этот объект.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-159">The **lpbNotif** and **cbNotif** members correspond to the control's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property and are used to notify the user interface when the control has to be updated.</span></span>
    
<span data-ttu-id="dc8b8-160">**cbNotif**</span><span class="sxs-lookup"><span data-stu-id="dc8b8-160">**cbNotif**</span></span>
  
> <span data-ttu-id="dc8b8-161">Количествобайтов в структуре, на который указывает **член lpbNotif.**</span><span class="sxs-lookup"><span data-stu-id="dc8b8-161">Count of bytes in the structure pointed to by the **lpbNotif** member.</span></span> 
    
<span data-ttu-id="dc8b8-162">**lpszFilter**</span><span class="sxs-lookup"><span data-stu-id="dc8b8-162">**lpszFilter**</span></span>
  
> <span data-ttu-id="dc8b8-163">Указатель на строку символов, описываемую, какие символы можно вказать в поле редактирования или со полем со combo.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-163">Pointer to a character string that describes which characters can be entered into an edit or combo box control.</span></span> <span data-ttu-id="dc8b8-164">Для других типов элементов управления элемент **lpszFilter** может иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-164">For other types of controls, the **lpszFilter** member can be NULL.</span></span> <span data-ttu-id="dc8b8-165">Для элементов управления полем редактирования и сомеда это должно быть регулярное выражение, которое применяется к отдельному символу за раз.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-165">For edit and combo box controls, it should be a regular expression that applies to a single character at a time.</span></span> <span data-ttu-id="dc8b8-166">Один и тот же фильтр применяется к всем символам в этом контроле.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-166">The same filter is applied to all characters in the control.</span></span> <span data-ttu-id="dc8b8-167">Формат строки фильтра:</span><span class="sxs-lookup"><span data-stu-id="dc8b8-167">The format of the filter string is as follows:</span></span> 
    
|<span data-ttu-id="dc8b8-168">**Символ**</span><span class="sxs-lookup"><span data-stu-id="dc8b8-168">**Character**</span></span>|<span data-ttu-id="dc8b8-169">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dc8b8-169">**Description**</span></span>|
|:-----|:-----|
| `*` <br/> | <span data-ttu-id="dc8b8-170">Любой символ разрешен (например, `"*"` ).</span><span class="sxs-lookup"><span data-stu-id="dc8b8-170">Any character is allowed (for example, `"*"`).</span></span>  <br/> |
| `[ ]` <br/> |<span data-ttu-id="dc8b8-171">Определяет набор символов (например, `"[0123456789]"` .)</span><span class="sxs-lookup"><span data-stu-id="dc8b8-171">Defines a set of characters (for example, `"[0123456789]"`.)</span></span>  <br/> |
| `-` <br/> |<span data-ttu-id="dc8b8-172">Указывает диапазон символов (например, `"[a-z]"` ).</span><span class="sxs-lookup"><span data-stu-id="dc8b8-172">Indicates a range of characters (for example, `"[a-z]"`).</span></span>  <br/> |
| `~` <br/> |<span data-ttu-id="dc8b8-173">Указывает, что эти символы не разрешены (например, `"[~0-9]")` .</span><span class="sxs-lookup"><span data-stu-id="dc8b8-173">Indicates that these characters are not allowed (for example, `"[~0-9]")`.</span></span> <br/>|   
| `\` <br/> |<span data-ttu-id="dc8b8-174">Используется для кавычка любых из предыдущих символов (например, `"[\-\\\[\]]"` знаки -, \, [и ] разрешены).</span><span class="sxs-lookup"><span data-stu-id="dc8b8-174">Used to quote any of the previous symbols (for example, `"[\-\\\[\]]"` means -, \, [, and ] characters are allowed).</span></span>  <br/> |
   
<span data-ttu-id="dc8b8-175">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="dc8b8-175">**ulItemID**</span></span>
  
> <span data-ttu-id="dc8b8-176">Значение, определя которое определяет управление в ресурсе диалоговых окно.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-176">Value that identifies the control in the dialog box resource.</span></span> <span data-ttu-id="dc8b8-177">Для страниц вкладок элементы управления типа DTCT_PAGE **элемент ulItemID** при желании используется для загрузки имени компонента страницы из строки ресурса.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-177">For tabbed pages controls of type DTCT_PAGE the **ulItemID** member is optionally used to load the component name for the page from a string resource.</span></span> <span data-ttu-id="dc8b8-178">Сведения о положении и метке считыются из ресурса диалоговых окно.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-178">Position and label information are read from the dialog box resource.</span></span> 
    
<span data-ttu-id="dc8b8-179">**ctl**</span><span class="sxs-lookup"><span data-stu-id="dc8b8-179">**ctl**</span></span>
  
> <span data-ttu-id="dc8b8-180">Структура, которая содержит данные для управления и соответствует свойству **PR_CONTROL_STRUCTURE** [(PidTagControlStructure).](pidtagcontrolstructure-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="dc8b8-180">A structure that holds the data for the control and corresponds to the control's **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) property.</span></span> <span data-ttu-id="dc8b8-181">Каждый тип управления имеет разную структуру.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-181">Each type of control has a different structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dc8b8-182">Примечания</span><span class="sxs-lookup"><span data-stu-id="dc8b8-182">Remarks</span></span>

<span data-ttu-id="dc8b8-183">Структура **DTCTL** описывает один из типов.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-183">The **DTCTL** structure describes one control of any type.</span></span> <span data-ttu-id="dc8b8-184">Большинство его членов используются для того, чтобы установить свойства в этом объекте управления.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-184">Most of its members are used to set properties on the control.</span></span> 
  
<span data-ttu-id="dc8b8-185">Член **ctl** — это объединение структур, которые связаны с определенным типом управления.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-185">The **ctl** member is a union of structures that relate to a particular type of control.</span></span> <span data-ttu-id="dc8b8-186">Если структура **DTCTL** описывает, например, изменение, член **ctl** будет указать на [структуру DTBLEDIT.](dtbledit.md)</span><span class="sxs-lookup"><span data-stu-id="dc8b8-186">If the **DTCTL** structure is describing an edit control, for example, the **ctl** member will point to a [DTBLEDIT](dtbledit.md) structure.</span></span> <span data-ttu-id="dc8b8-187">Эта структура соответствует свойству PR_CONTROL_STRUCTURE **управления.**</span><span class="sxs-lookup"><span data-stu-id="dc8b8-187">This structure corresponds to the control's **PR_CONTROL_STRUCTURE** property.</span></span> <span data-ttu-id="dc8b8-188">В качестве первого члена объединения имеется переменная типа LPVOID, позволяющая инициализации времени компиляции **структуры DTCTL.**</span><span class="sxs-lookup"><span data-stu-id="dc8b8-188">The union has as its first member a variable of type LPVOID to allow compile time initialization of the **DTCTL** structure.</span></span> 
  
<span data-ttu-id="dc8b8-189">Хотя функция [BuildDisplayTable](builddisplaytable.md) использует структуру **DTCTL** для построения таблицы отображения из ресурсов управления, **структура DTCTL** никогда не отображается в самой таблице отображения.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-189">Although the [BuildDisplayTable](builddisplaytable.md) function uses the **DTCTL** structure for building the display table from control resources, the **DTCTL** structure never appears in the display table itself.</span></span> <span data-ttu-id="dc8b8-190">Эта структура просто сообщает сведения **в BuildDisplayTable.**</span><span class="sxs-lookup"><span data-stu-id="dc8b8-190">This structure just supplies information to **BuildDisplayTable**.</span></span>
  
<span data-ttu-id="dc8b8-191">В **элементе ulCtlFlags** четыре флага DT_ACCEPT_DBCS, DT_EDITABLE и DT_MULTILINE_and DT_PASSWORD_EDIT только на элементы управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-191">In the **ulCtlFlags** member, four flags DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT affect edit controls only.</span></span> <span data-ttu-id="dc8b8-192">Два других DT_REQUIRED и DT_SET_IMMEDIATE любого редактируемого управления.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-192">Two others DT_REQUIRED and DT_SET_IMMEDIATE affect any editable control.</span></span> 
  
<span data-ttu-id="dc8b8-193">Элементы управления, доступные для диалогового окна: метка, текстовое поле, список, выпадаичный список, поле со списком, поле со списком, поле группы, кнопка, кнопка, кнопка и страница вкладок.</span><span class="sxs-lookup"><span data-stu-id="dc8b8-193">The controls available for a dialog box are label, text box, ink-aware text box, list, drop-down list, combo box, check box, group box, button, radio button, and tabbed page.</span></span>
  
<span data-ttu-id="dc8b8-194">Обзор таблиц отображения см. в [таблице отображения.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="dc8b8-194">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="dc8b8-195">Сведения о реализации таблицы отображения см. в таблице ["Реализация таблицы отображения".](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="dc8b8-195">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dc8b8-196">См. также</span><span class="sxs-lookup"><span data-stu-id="dc8b8-196">See also</span></span>

- [<span data-ttu-id="dc8b8-197">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="dc8b8-197">BuildDisplayTable</span></span>](builddisplaytable.md)
- [<span data-ttu-id="dc8b8-198">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="dc8b8-198">DTBLBUTTON</span></span>](dtblbutton.md)
- [<span data-ttu-id="dc8b8-199">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="dc8b8-199">DTBLCHECKBOX</span></span>](dtblcheckbox.md)
- [<span data-ttu-id="dc8b8-200">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="dc8b8-200">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="dc8b8-201">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="dc8b8-201">DTBLDDLBX</span></span>](dtblddlbx.md)
- [<span data-ttu-id="dc8b8-202">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="dc8b8-202">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="dc8b8-203">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="dc8b8-203">DTBLGROUPBOX</span></span>](dtblgroupbox.md)
- [<span data-ttu-id="dc8b8-204">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="dc8b8-204">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="dc8b8-205">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="dc8b8-205">DTBLLBX</span></span>](dtbllbx.md)
- [<span data-ttu-id="dc8b8-206">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="dc8b8-206">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md)
- [<span data-ttu-id="dc8b8-207">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="dc8b8-207">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md)
- [<span data-ttu-id="dc8b8-208">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="dc8b8-208">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="dc8b8-209">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="dc8b8-209">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md)
- [<span data-ttu-id="dc8b8-210">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="dc8b8-210">MAPI Structures</span></span>](mapi-structures.md)

