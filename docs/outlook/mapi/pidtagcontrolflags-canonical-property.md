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
ms.openlocfilehash: 099f08876eadc83ebb66b9e4226eeeee6277bf01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430884"
---
# <a name="pidtagcontrolflags-canonical-property"></a><span data-ttu-id="e1df1-103">Каноническое свойство PidTagControlFlags</span><span class="sxs-lookup"><span data-stu-id="e1df1-103">PidTagControlFlags Canonical Property</span></span>

  
  
<span data-ttu-id="e1df1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1df1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1df1-105">Содержит битовую маску флагов, определяющих поведение элемента управления, используемого в диалоговом окне, созданном из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="e1df1-105">Contains a bitmask of flags governing the behavior of a control used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e1df1-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e1df1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e1df1-107">ПР_КОНТРОЛ_ФЛАГС</span><span class="sxs-lookup"><span data-stu-id="e1df1-107">PR_CONTROL_FLAGS</span></span>  <br/> |
|<span data-ttu-id="e1df1-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e1df1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e1df1-109">0x3F00</span><span class="sxs-lookup"><span data-stu-id="e1df1-109">0x3F00</span></span>  <br/> |
|<span data-ttu-id="e1df1-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e1df1-110">Data type:</span></span>  <br/> |<span data-ttu-id="e1df1-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e1df1-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e1df1-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e1df1-112">Area:</span></span>  <br/> |<span data-ttu-id="e1df1-113">Таблица отображения MAPI</span><span class="sxs-lookup"><span data-stu-id="e1df1-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1df1-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e1df1-114">Remarks</span></span>

<span data-ttu-id="e1df1-115">Для этого свойства можно задать один или несколько из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="e1df1-115">One or more of the following flags can be set for this property:</span></span>
  
<span data-ttu-id="e1df1-116">ДТ_АКЦЕПТ_ДБКС</span><span class="sxs-lookup"><span data-stu-id="e1df1-116">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="e1df1-117">Элемент управления может иметь в нем символы набора двухбайтовых символов (DBCS).</span><span class="sxs-lookup"><span data-stu-id="e1df1-117">The control can have Double-Byte Character Set (DBCS) characters in it.</span></span> <span data-ttu-id="e1df1-118">Этот флаг используется с элементами управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="e1df1-118">This flag is used with edit controls.</span></span> <span data-ttu-id="e1df1-119">Допускается множество многобайтовых кодировок.</span><span class="sxs-lookup"><span data-stu-id="e1df1-119">It allows multiple-byte character sets.</span></span>
    
<span data-ttu-id="e1df1-120">ДТ_ЕДИТАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="e1df1-120">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="e1df1-121">Элемент управления можно редактировать; можно изменить значение, связанное с элементом управления.</span><span class="sxs-lookup"><span data-stu-id="e1df1-121">The control can be edited; the value associated with the control can be changed.</span></span> <span data-ttu-id="e1df1-122">Если этот флаг не установлен, элемент управления доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e1df1-122">When this flag is not set, the control is read-only.</span></span> <span data-ttu-id="e1df1-123">Это значение игнорируется в элементах управления "подпись", "Группа", "Стандартная кнопка", "многозначный" раскрывающийся список и элемент управления "список".</span><span class="sxs-lookup"><span data-stu-id="e1df1-123">This value is ignored on label, group box, standard push button, multivalued drop down list box and list box controls.</span></span>
    
<span data-ttu-id="e1df1-124">ДТ_МУЛТИЛИНЕ</span><span class="sxs-lookup"><span data-stu-id="e1df1-124">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="e1df1-125">Элемент управления "поле ввода" может содержать несколько строк.</span><span class="sxs-lookup"><span data-stu-id="e1df1-125">The edit control can contain multiple lines.</span></span> <span data-ttu-id="e1df1-126">Это означает, что возвращаемый символ можно ввести в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="e1df1-126">This means a return character can be entered within the control.</span></span> <span data-ttu-id="e1df1-127">Этот флаг действителен только для элементов управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="e1df1-127">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="e1df1-128">ДТ_ПАССВОРД_ЕДИТ</span><span class="sxs-lookup"><span data-stu-id="e1df1-128">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="e1df1-129">Применяется к элементам управления для редактирования.</span><span class="sxs-lookup"><span data-stu-id="e1df1-129">Applies to edit controls.</span></span> <span data-ttu-id="e1df1-130">Элемент управления редактированием рассматривается как пароль.</span><span class="sxs-lookup"><span data-stu-id="e1df1-130">The edit control is treated like a password.</span></span> <span data-ttu-id="e1df1-131">Значение отображается с использованием звездочек вместо того, чтобы отображать введенные фактические символы.</span><span class="sxs-lookup"><span data-stu-id="e1df1-131">The value is displayed using asterisks instead of echoing the actual characters entered.</span></span>
    
<span data-ttu-id="e1df1-132">ДТ_РЕКУИРЕД</span><span class="sxs-lookup"><span data-stu-id="e1df1-132">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="e1df1-133">Если элемент управления допускает изменения (ДТ_ЕДИТАБЛЕ), он должен иметь значение до [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="e1df1-133">If the control allows changes (DT_EDITABLE), it must have a value before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
    
<span data-ttu-id="e1df1-134">ДТ_СЕТ_ИММЕДИАТЕ</span><span class="sxs-lookup"><span data-stu-id="e1df1-134">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="e1df1-135">Включает немедленный параметр значения; как только значение в элементе управления изменится, MAPI вызывает метод **SetProps** для свойства, связанного с этим элементом управления.</span><span class="sxs-lookup"><span data-stu-id="e1df1-135">Enables immediate setting of a value; as soon as a value in the control changes, MAPI calls the **SetProps** method for the property associated with that control.</span></span> <span data-ttu-id="e1df1-136">Если этот флаг не задан, значения задаются при закрытии диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="e1df1-136">When this flag is not set, the values are set when the dialog box is dismissed.</span></span> 
    
<span data-ttu-id="e1df1-137">ДТ_СЕТ_СЕЛЕКТИОН</span><span class="sxs-lookup"><span data-stu-id="e1df1-137">DT_SET_SELECTION</span></span> 
  
> <span data-ttu-id="e1df1-138">Если в списке сделан выбор, в качестве значения свойства используется столбец индекс этого списка.</span><span class="sxs-lookup"><span data-stu-id="e1df1-138">When a selection is made within the list box, the index column of that list box is set as a property.</span></span> <span data-ttu-id="e1df1-139">Всегда используется с ДТ_СЕТ_ИММЕДИАТЕ.</span><span class="sxs-lookup"><span data-stu-id="e1df1-139">Always used with DT_SET_IMMEDIATE.</span></span>
    
<span data-ttu-id="e1df1-140">Это свойство хранится в элементе Улктлфлагс структуры [дтктл](dtctl.md) элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e1df1-140">This property is stored in the ulCtlFlags member of a control's [DTCTL](dtctl.md) structure.</span></span> <span data-ttu-id="e1df1-141">Большинство флагов элемента управления применяются ко всем элементам управления, которые позволяют вводить данные пользователем; несколько относятся только к элементу управления редактирования.</span><span class="sxs-lookup"><span data-stu-id="e1df1-141">Most of the control flags apply to all of the controls that allow user input; a few apply only to the edit control.</span></span> <span data-ttu-id="e1df1-142">Элементы управления, которые не допускают ввод пользователем (например, кнопку или метку), задают значение 0 для своих флагов управления.</span><span class="sxs-lookup"><span data-stu-id="e1df1-142">Controls that do not allow user input, such as a button or a label, set 0 for their control flags.</span></span> 
  
<span data-ttu-id="e1df1-143">Многие из значений флагов понятны ясно.</span><span class="sxs-lookup"><span data-stu-id="e1df1-143">Many of the flag values are self-explanatory.</span></span> <span data-ttu-id="e1df1-144">Например, если для элемента управления задано значение ДТ_РЕКУИРЕД, оно должно содержать значение, прежде чем разрешить отправку этого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="e1df1-144">For example, when DT_REQUIRED is set for a control, it must contain a value before the dialog box is allowed to be dismissed.</span></span> <span data-ttu-id="e1df1-145">Поставщик услуг может предоставить значение с помощью своей реализации **IMAPIProp** или ввести один из пользователей.</span><span class="sxs-lookup"><span data-stu-id="e1df1-145">Either the service provider can supply a value through its **IMAPIProp** implementation or the user can enter one.</span></span> <span data-ttu-id="e1df1-146">ДТ_ЕДИТАБЛЕ указывает, что значение для элемента управления можно изменить.</span><span class="sxs-lookup"><span data-stu-id="e1df1-146">DT_EDITABLE indicates that the value for the control can be modified.</span></span> <span data-ttu-id="e1df1-147">ДТ_МУЛТИЛИНЕ позволяет значению элемента управления "поле ввода" занимать несколько строк.</span><span class="sxs-lookup"><span data-stu-id="e1df1-147">DT_MULTILINE allows the value for an edit control to span multiple lines.</span></span> 
  
<span data-ttu-id="e1df1-148">Некоторые флаги элементов управления не настолько очевидны.</span><span class="sxs-lookup"><span data-stu-id="e1df1-148">Some control flags are not so obvious in their meaning.</span></span> <span data-ttu-id="e1df1-149">Когда элемент управления устанавливает флаг ДТ_СЕТ_ИММЕДИАТЕ, любые изменения его значения вступают в силу сразу после того, как пользователь перемещается на новый элемент управления.</span><span class="sxs-lookup"><span data-stu-id="e1df1-149">When a control sets the DT_SET_IMMEDIATE flag, any changes to its value take affect as soon as the user moves to a new control.</span></span> <span data-ttu-id="e1df1-150">MAPI создает один вызов метода свойства [IMAPIProp:: SetProps](imapiprop-setprops.md) для свойства элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e1df1-150">MAPI makes a single call to the property interface's [IMAPIProp::SetProps](imapiprop-setprops.md) method for the control's property.</span></span> <span data-ttu-id="e1df1-151">Это отличается от поведения по умолчанию, которое откладывается на то, что изменения значений элементов управления вступают в силу до тех пор, пока пользователь не нажимает кнопку **ОК** или не закрывает диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="e1df1-151">This is different from the default behavior, which is to postpone having changes to control values take effect until after the user selects the **OK** button or dismisses the dialog box.</span></span> <span data-ttu-id="e1df1-152">Флаг ДТ_СЕТ_ИММЕДИАТЕ часто используется в сочетании с уведомлениями в таблице отображения.</span><span class="sxs-lookup"><span data-stu-id="e1df1-152">The DT_SET_IMMEDIATE flag is often used in combination with display table notifications.</span></span> 
  
<span data-ttu-id="e1df1-153">В следующей таблице перечислены типы элементов управления и все значения флагов, которые можно задать для каждого типа.</span><span class="sxs-lookup"><span data-stu-id="e1df1-153">The following table lists the types of controls and all of the flag values that can be set for each type.</span></span>
  
|<span data-ttu-id="e1df1-154">**Control**</span><span class="sxs-lookup"><span data-stu-id="e1df1-154">**Control**</span></span>|<span data-ttu-id="e1df1-155">**Допустимые значения для этого свойства**</span><span class="sxs-lookup"><span data-stu-id="e1df1-155">**Valid values for this property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e1df1-156">Кнопка</span><span class="sxs-lookup"><span data-stu-id="e1df1-156">Button</span></span>  <br/> |<span data-ttu-id="e1df1-157">Должно быть равно нулю</span><span class="sxs-lookup"><span data-stu-id="e1df1-157">Must be zero</span></span>  <br/> |
|<span data-ttu-id="e1df1-158">Флажок</span><span class="sxs-lookup"><span data-stu-id="e1df1-158">Check box</span></span>  <br/> |<span data-ttu-id="e1df1-159">ДТ_ЕДИТАБЛЕ, ДТ_СЕТ_ИММЕДИАТЕ</span><span class="sxs-lookup"><span data-stu-id="e1df1-159">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="e1df1-160">Поле со списком</span><span class="sxs-lookup"><span data-stu-id="e1df1-160">Combo box</span></span>  <br/> |<span data-ttu-id="e1df1-161">ДТ_ЕДИТАБЛЕ, ДТ_РЕКУИРЕД, ДТ_СЕТ_ИММЕДИАТЕ</span><span class="sxs-lookup"><span data-stu-id="e1df1-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="e1df1-162">Раскрывающийся список</span><span class="sxs-lookup"><span data-stu-id="e1df1-162">Drop-down list box</span></span>  <br/> |<span data-ttu-id="e1df1-163">ДТ_ЕДИТАБЛЕ, ДТ_СЕТ_ИММЕДИАТЕ</span><span class="sxs-lookup"><span data-stu-id="e1df1-163">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="e1df1-164">Edit</span><span class="sxs-lookup"><span data-stu-id="e1df1-164">Edit</span></span>  <br/> |<span data-ttu-id="e1df1-165">ДТ_АКЦЕПТ_ДБКС, ДТ_МУЛТИЛИНЕ, ДТ_ЕДИТАБЛЕ, ДТ_ПАССВОРД_ЕДИТ, ДТ_РЕКУИРЕД, ДТ_СЕТ_ИММЕДИАТЕ</span><span class="sxs-lookup"><span data-stu-id="e1df1-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="e1df1-166">Поле группы</span><span class="sxs-lookup"><span data-stu-id="e1df1-166">Group box</span></span>  <br/> |<span data-ttu-id="e1df1-167">Должно быть равно нулю</span><span class="sxs-lookup"><span data-stu-id="e1df1-167">Must be zero</span></span>  <br/> |
|<span data-ttu-id="e1df1-168">Метка</span><span class="sxs-lookup"><span data-stu-id="e1df1-168">Label</span></span>  <br/> |<span data-ttu-id="e1df1-169">Должно быть равно нулю</span><span class="sxs-lookup"><span data-stu-id="e1df1-169">Must be zero</span></span>  <br/> |
|<span data-ttu-id="e1df1-170">Поле со списком</span><span class="sxs-lookup"><span data-stu-id="e1df1-170">List box</span></span>  <br/> |<span data-ttu-id="e1df1-171">Должно быть равно нулю</span><span class="sxs-lookup"><span data-stu-id="e1df1-171">Must be zero</span></span>  <br/> |
|<span data-ttu-id="e1df1-172">Раскрывающийся список с несколькими значениями</span><span class="sxs-lookup"><span data-stu-id="e1df1-172">Multivalue drop-down list box</span></span>  <br/> |<span data-ttu-id="e1df1-173">Должно быть равно нулю</span><span class="sxs-lookup"><span data-stu-id="e1df1-173">Must be zero</span></span>  <br/> |
|<span data-ttu-id="e1df1-174">МногоЗначный список</span><span class="sxs-lookup"><span data-stu-id="e1df1-174">Multivalue list box</span></span>  <br/> |<span data-ttu-id="e1df1-175">Должно быть равно нулю</span><span class="sxs-lookup"><span data-stu-id="e1df1-175">Must be zero</span></span>  <br/> |
|<span data-ttu-id="e1df1-176">Страница с вкладками</span><span class="sxs-lookup"><span data-stu-id="e1df1-176">Tabbed page</span></span>  <br/> |<span data-ttu-id="e1df1-177">Должно быть равно нулю</span><span class="sxs-lookup"><span data-stu-id="e1df1-177">Must be zero</span></span>  <br/> |
|<span data-ttu-id="e1df1-178">Переключатель</span><span class="sxs-lookup"><span data-stu-id="e1df1-178">Radio button</span></span>  <br/> |<span data-ttu-id="e1df1-179">Должно быть равно нулю</span><span class="sxs-lookup"><span data-stu-id="e1df1-179">Must be zero</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e1df1-180">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e1df1-180">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e1df1-181">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="e1df1-181">Header files</span></span>

<span data-ttu-id="e1df1-182">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="e1df1-182">Mapidefs.h</span></span>
  
> <span data-ttu-id="e1df1-183">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e1df1-183">Provides data type definitions.</span></span>
    
<span data-ttu-id="e1df1-184">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="e1df1-184">Mapitags.h</span></span>
  
> <span data-ttu-id="e1df1-185">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="e1df1-185">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1df1-186">См. также</span><span class="sxs-lookup"><span data-stu-id="e1df1-186">See also</span></span>



[<span data-ttu-id="e1df1-187">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e1df1-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e1df1-188">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="e1df1-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e1df1-189">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e1df1-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e1df1-190">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e1df1-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

