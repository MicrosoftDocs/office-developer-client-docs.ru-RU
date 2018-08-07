---
title: Каноническое свойство PidTagControlFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlFlags
api_type:
- HeaderDef
ms.assetid: b97a9e72-fbb7-49ab-a19d-5e9bd1b8a80d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f6947efe1aa6866efb7a5a3d96262d021c68013f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811015"
---
# <a name="pidtagcontrolflags-canonical-property"></a><span data-ttu-id="c88d3-103">Каноническое свойство PidTagControlFlags</span><span class="sxs-lookup"><span data-stu-id="c88d3-103">PidTagControlFlags Canonical Property</span></span>

  
  
<span data-ttu-id="c88d3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c88d3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c88d3-105">Содержит битовую маску флагов регулирующих поведение элемента управления, используемые в диалоговое окно, построенная на основе таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="c88d3-105">Contains a bitmask of flags governing the behavior of a control used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c88d3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c88d3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c88d3-107">PR_CONTROL_FLAGS</span><span class="sxs-lookup"><span data-stu-id="c88d3-107">PR_CONTROL_FLAGS</span></span>  <br/> |
|<span data-ttu-id="c88d3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c88d3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c88d3-109">0x3F00</span><span class="sxs-lookup"><span data-stu-id="c88d3-109">0x3F00</span></span>  <br/> |
|<span data-ttu-id="c88d3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c88d3-110">Data type:</span></span>  <br/> |<span data-ttu-id="c88d3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c88d3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c88d3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c88d3-112">Area:</span></span>  <br/> |<span data-ttu-id="c88d3-113">Таблица отображения MAPI</span><span class="sxs-lookup"><span data-stu-id="c88d3-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c88d3-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c88d3-114">Remarks</span></span>

<span data-ttu-id="c88d3-115">Для этого свойства может быть установлено одно или несколько из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="c88d3-115">One or more of the following flags can be set for this property:</span></span>
  
<span data-ttu-id="c88d3-116">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="c88d3-116">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="c88d3-117">Элемент управления может иметь значение двухбайтовых знаков (DBCS) символов в нем.</span><span class="sxs-lookup"><span data-stu-id="c88d3-117">The control can have Double-Byte Character Set (DBCS) characters in it.</span></span> <span data-ttu-id="c88d3-118">Этот флаг используется с элементами управления Правка.</span><span class="sxs-lookup"><span data-stu-id="c88d3-118">This flag is used with edit controls.</span></span> <span data-ttu-id="c88d3-119">Он обеспечивает наборы символов несколько байтов.</span><span class="sxs-lookup"><span data-stu-id="c88d3-119">It allows multiple-byte character sets.</span></span>
    
<span data-ttu-id="c88d3-120">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="c88d3-120">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="c88d3-121">Элемент управления можно редактировать; можно изменить значение, связанное с элементом управления.</span><span class="sxs-lookup"><span data-stu-id="c88d3-121">The control can be edited; the value associated with the control can be changed.</span></span> <span data-ttu-id="c88d3-122">Если этот флаг не задан, элемент управления доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c88d3-122">When this flag is not set, the control is read-only.</span></span> <span data-ttu-id="c88d3-123">Это значение игнорируется на метку, группа, стандартной кнопки, многозначных раскрывающегося списка и элемента управления списка полей.</span><span class="sxs-lookup"><span data-stu-id="c88d3-123">This value is ignored on label, group box, standard push button, multivalued drop down list box and list box controls.</span></span>
    
<span data-ttu-id="c88d3-124">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="c88d3-124">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="c88d3-125">Элемент управления для редактирования может содержать несколько строк.</span><span class="sxs-lookup"><span data-stu-id="c88d3-125">The edit control can contain multiple lines.</span></span> <span data-ttu-id="c88d3-126">Это означает, что возвращаемый символ можно ввести в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="c88d3-126">This means a return character can be entered within the control.</span></span> <span data-ttu-id="c88d3-127">Этот флаг является допустимым редактирования только для элементов управления.</span><span class="sxs-lookup"><span data-stu-id="c88d3-127">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="c88d3-128">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="c88d3-128">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="c88d3-129">Применяется для редактирования элементов управления.</span><span class="sxs-lookup"><span data-stu-id="c88d3-129">Applies to edit controls.</span></span> <span data-ttu-id="c88d3-130">Элемент управления для редактирования рассматривается как пароль.</span><span class="sxs-lookup"><span data-stu-id="c88d3-130">The edit control is treated like a password.</span></span> <span data-ttu-id="c88d3-131">Значение отображается с помощью звездочки вместо вывода вводимых символов.</span><span class="sxs-lookup"><span data-stu-id="c88d3-131">The value is displayed using asterisks instead of echoing the actual characters entered.</span></span>
    
<span data-ttu-id="c88d3-132">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="c88d3-132">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="c88d3-133">Если элемент управления позволяет изменения (DT_EDITABLE), он должен иметь значение до вызова [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="c88d3-133">If the control allows changes (DT_EDITABLE), it must have a value before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
    
<span data-ttu-id="c88d3-134">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="c88d3-134">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="c88d3-135">Позволяет интерпретации параметр значение; как только изменяет значение в элементе управления MAPI вызывает метод **SetProps** для свойства, связанного с этим элементом управления.</span><span class="sxs-lookup"><span data-stu-id="c88d3-135">Enables immediate setting of a value; as soon as a value in the control changes, MAPI calls the **SetProps** method for the property associated with that control.</span></span> <span data-ttu-id="c88d3-136">Если этот флаг не задан, значения устанавливаются при диалоговое окно закрывается.</span><span class="sxs-lookup"><span data-stu-id="c88d3-136">When this flag is not set, the values are set when the dialog box is dismissed.</span></span> 
    
<span data-ttu-id="c88d3-137">DT_SET_SELECTION</span><span class="sxs-lookup"><span data-stu-id="c88d3-137">DT_SET_SELECTION</span></span> 
  
> <span data-ttu-id="c88d3-138">При выбора в поле списка в столбце индекса из этого списка устанавливается как свойство.</span><span class="sxs-lookup"><span data-stu-id="c88d3-138">When a selection is made within the list box, the index column of that list box is set as a property.</span></span> <span data-ttu-id="c88d3-139">Всегда использовать совместно с DT_SET_IMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="c88d3-139">Always used with DT_SET_IMMEDIATE.</span></span>
    
<span data-ttu-id="c88d3-140">Это свойство хранится в член ulCtlFlags структуры [DTCTL](dtctl.md) элемента управления.</span><span class="sxs-lookup"><span data-stu-id="c88d3-140">This property is stored in the ulCtlFlags member of a control's [DTCTL](dtctl.md) structure.</span></span> <span data-ttu-id="c88d3-141">Большая часть флаги управления применяются ко всем элементам управления, которые позволяют пользователям вводить данные; несколько применяются только к элемент управления для редактирования.</span><span class="sxs-lookup"><span data-stu-id="c88d3-141">Most of the control flags apply to all of the controls that allow user input; a few apply only to the edit control.</span></span> <span data-ttu-id="c88d3-142">Элементы управления, которые не позволяют пользователям вводить данные, такие как кнопки или метки, задайте 0 для их флаги элемента управления.</span><span class="sxs-lookup"><span data-stu-id="c88d3-142">Controls that do not allow user input, such as a button or a label, set 0 for their control flags.</span></span> 
  
<span data-ttu-id="c88d3-143">Многие из значений флаг очевидны.</span><span class="sxs-lookup"><span data-stu-id="c88d3-143">Many of the flag values are self-explanatory.</span></span> <span data-ttu-id="c88d3-144">Например когда DT_REQUIRED для элемента управления, он должен содержать значение перед диалоговое окно может быть закрыт.</span><span class="sxs-lookup"><span data-stu-id="c88d3-144">For example, when DT_REQUIRED is set for a control, it must contain a value before the dialog box is allowed to be dismissed.</span></span> <span data-ttu-id="c88d3-145">Поставщик услуг можно указать значение его реализации **IMAPIProp** либо пользователь может ввести один.</span><span class="sxs-lookup"><span data-stu-id="c88d3-145">Either the service provider can supply a value through its **IMAPIProp** implementation or the user can enter one.</span></span> <span data-ttu-id="c88d3-146">DT_EDITABLE указывает, что значение для элемента управления может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="c88d3-146">DT_EDITABLE indicates that the value for the control can be modified.</span></span> <span data-ttu-id="c88d3-147">DT_MULTILINE позволяет значение для ввода нескольких строк.</span><span class="sxs-lookup"><span data-stu-id="c88d3-147">DT_MULTILINE allows the value for an edit control to span multiple lines.</span></span> 
  
<span data-ttu-id="c88d3-148">Некоторые флаги управления не столь очевидно в их значения.</span><span class="sxs-lookup"><span data-stu-id="c88d3-148">Some control flags are not so obvious in their meaning.</span></span> <span data-ttu-id="c88d3-149">Когда элемент управления устанавливает флаг DT_SET_IMMEDIATE, все изменения, необходимо выполнить его значение влияет на сразу же пользователь перемещается на новый элемент управления.</span><span class="sxs-lookup"><span data-stu-id="c88d3-149">When a control sets the DT_SET_IMMEDIATE flag, any changes to its value take affect as soon as the user moves to a new control.</span></span> <span data-ttu-id="c88d3-150">MAPI делает один вызов метода [IMAPIProp::SetProps](imapiprop-setprops.md) интерфейса свойств для свойства элемента управления.</span><span class="sxs-lookup"><span data-stu-id="c88d3-150">MAPI makes a single call to the property interface's [IMAPIProp::SetProps](imapiprop-setprops.md) method for the control's property.</span></span> <span data-ttu-id="c88d3-151">Это отличается от поведения по умолчанию, являющийся откладывать необходимости изменения значения элемента управления вступают в силу только после пользователь выбирает кнопку **ОК** или закрывает диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="c88d3-151">This is different from the default behavior, which is to postpone having changes to control values take effect until after the user selects the **OK** button or dismisses the dialog box.</span></span> <span data-ttu-id="c88d3-152">Флаг DT_SET_IMMEDIATE часто используется в сочетании с отображения таблицы уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c88d3-152">The DT_SET_IMMEDIATE flag is often used in combination with display table notifications.</span></span> 
  
<span data-ttu-id="c88d3-153">В следующей таблице перечислены типы элементов управления и всех флаг значения, которые можно задать для каждого типа.</span><span class="sxs-lookup"><span data-stu-id="c88d3-153">The following table lists the types of controls and all of the flag values that can be set for each type.</span></span>
  
|<span data-ttu-id="c88d3-154">**Control**</span><span class="sxs-lookup"><span data-stu-id="c88d3-154">**Control**</span></span>|<span data-ttu-id="c88d3-155">**Допустимые значения для этого свойства**</span><span class="sxs-lookup"><span data-stu-id="c88d3-155">**Valid values for this property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c88d3-156">Кнопка</span><span class="sxs-lookup"><span data-stu-id="c88d3-156">Button</span></span>  <br/> |<span data-ttu-id="c88d3-157">Должно быть равно нулю</span><span class="sxs-lookup"><span data-stu-id="c88d3-157">Must be zero</span></span>  <br/> |
|<span data-ttu-id="c88d3-158">Флажок</span><span class="sxs-lookup"><span data-stu-id="c88d3-158">Check box</span></span>  <br/> |<span data-ttu-id="c88d3-159">DT_EDITABLE DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="c88d3-159">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="c88d3-160">Поле со списком</span><span class="sxs-lookup"><span data-stu-id="c88d3-160">Combo box</span></span>  <br/> |<span data-ttu-id="c88d3-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="c88d3-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="c88d3-162">Поле раскрывающегося списка</span><span class="sxs-lookup"><span data-stu-id="c88d3-162">Drop-down list box</span></span>  <br/> |<span data-ttu-id="c88d3-163">DT_EDITABLE DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="c88d3-163">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="c88d3-164">Изменить</span><span class="sxs-lookup"><span data-stu-id="c88d3-164">Edit</span></span>  <br/> |<span data-ttu-id="c88d3-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="c88d3-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="c88d3-166">Группа</span><span class="sxs-lookup"><span data-stu-id="c88d3-166">Group box</span></span>  <br/> |<span data-ttu-id="c88d3-167">Должно быть равно нулю</span><span class="sxs-lookup"><span data-stu-id="c88d3-167">Must be zero</span></span>  <br/> |
|<span data-ttu-id="c88d3-168">Метка</span><span class="sxs-lookup"><span data-stu-id="c88d3-168">Label</span></span>  <br/> |<span data-ttu-id="c88d3-169">Должно быть равно нулю</span><span class="sxs-lookup"><span data-stu-id="c88d3-169">Must be zero</span></span>  <br/> |
|<span data-ttu-id="c88d3-170">Список</span><span class="sxs-lookup"><span data-stu-id="c88d3-170">List box</span></span>  <br/> |<span data-ttu-id="c88d3-171">Должно быть равно нулю</span><span class="sxs-lookup"><span data-stu-id="c88d3-171">Must be zero</span></span>  <br/> |
|<span data-ttu-id="c88d3-172">Для нескольких значений раскрывающегося списка</span><span class="sxs-lookup"><span data-stu-id="c88d3-172">Multivalue drop-down list box</span></span>  <br/> |<span data-ttu-id="c88d3-173">Должно быть равно нулю</span><span class="sxs-lookup"><span data-stu-id="c88d3-173">Must be zero</span></span>  <br/> |
|<span data-ttu-id="c88d3-174">Поле список с несколькими значениями</span><span class="sxs-lookup"><span data-stu-id="c88d3-174">Multivalue list box</span></span>  <br/> |<span data-ttu-id="c88d3-175">Должно быть равно нулю</span><span class="sxs-lookup"><span data-stu-id="c88d3-175">Must be zero</span></span>  <br/> |
|<span data-ttu-id="c88d3-176">Страницы с вкладками</span><span class="sxs-lookup"><span data-stu-id="c88d3-176">Tabbed page</span></span>  <br/> |<span data-ttu-id="c88d3-177">Должно быть равно нулю</span><span class="sxs-lookup"><span data-stu-id="c88d3-177">Must be zero</span></span>  <br/> |
|<span data-ttu-id="c88d3-178">Переключатель</span><span class="sxs-lookup"><span data-stu-id="c88d3-178">Radio button</span></span>  <br/> |<span data-ttu-id="c88d3-179">Должно быть равно нулю</span><span class="sxs-lookup"><span data-stu-id="c88d3-179">Must be zero</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c88d3-180">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c88d3-180">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c88d3-181">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c88d3-181">Header files</span></span>

<span data-ttu-id="c88d3-182">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c88d3-182">Mapidefs.h</span></span>
  
> <span data-ttu-id="c88d3-183">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c88d3-183">Provides data type definitions.</span></span>
    
<span data-ttu-id="c88d3-184">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c88d3-184">Mapitags.h</span></span>
  
> <span data-ttu-id="c88d3-185">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="c88d3-185">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c88d3-186">См. также</span><span class="sxs-lookup"><span data-stu-id="c88d3-186">See also</span></span>



[<span data-ttu-id="c88d3-187">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c88d3-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c88d3-188">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c88d3-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c88d3-189">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c88d3-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c88d3-190">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c88d3-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

