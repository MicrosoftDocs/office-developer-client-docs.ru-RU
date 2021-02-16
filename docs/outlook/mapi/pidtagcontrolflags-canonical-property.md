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
# <a name="pidtagcontrolflags-canonical-property"></a><span data-ttu-id="15802-103">Каноническое свойство PidTagControlFlags</span><span class="sxs-lookup"><span data-stu-id="15802-103">PidTagControlFlags Canonical Property</span></span>

  
  
<span data-ttu-id="15802-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15802-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15802-105">Содержит битовуюmass флагов, управляющих поведением управления, используемого в диалоговом окне, построенного из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="15802-105">Contains a bitmask of flags governing the behavior of a control used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="15802-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="15802-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="15802-107">PR_CONTROL_FLAGS</span><span class="sxs-lookup"><span data-stu-id="15802-107">PR_CONTROL_FLAGS</span></span>  <br/> |
|<span data-ttu-id="15802-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="15802-108">Identifier:</span></span>  <br/> |<span data-ttu-id="15802-109">0x3F00</span><span class="sxs-lookup"><span data-stu-id="15802-109">0x3F00</span></span>  <br/> |
|<span data-ttu-id="15802-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="15802-110">Data type:</span></span>  <br/> |<span data-ttu-id="15802-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="15802-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="15802-112">Область:</span><span class="sxs-lookup"><span data-stu-id="15802-112">Area:</span></span>  <br/> |<span data-ttu-id="15802-113">Таблица отображения MAPI</span><span class="sxs-lookup"><span data-stu-id="15802-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15802-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="15802-114">Remarks</span></span>

<span data-ttu-id="15802-115">Для этого свойства можно установить один или несколько из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="15802-115">One or more of the following flags can be set for this property:</span></span>
  
<span data-ttu-id="15802-116">DT_ACCEPT_DBCS</span><span class="sxs-lookup"><span data-stu-id="15802-116">DT_ACCEPT_DBCS</span></span> 
  
> <span data-ttu-id="15802-117">В нем может Double-Byte символы набора символов (DBCS).</span><span class="sxs-lookup"><span data-stu-id="15802-117">The control can have Double-Byte Character Set (DBCS) characters in it.</span></span> <span data-ttu-id="15802-118">Этот флаг используется с элементом управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="15802-118">This flag is used with edit controls.</span></span> <span data-ttu-id="15802-119">Он позволяет использовать много byte character sets.</span><span class="sxs-lookup"><span data-stu-id="15802-119">It allows multiple-byte character sets.</span></span>
    
<span data-ttu-id="15802-120">DT_EDITABLE</span><span class="sxs-lookup"><span data-stu-id="15802-120">DT_EDITABLE</span></span> 
  
> <span data-ttu-id="15802-121">Можно редактировать этот контроль; Значение, связанное с управлением, можно изменить.</span><span class="sxs-lookup"><span data-stu-id="15802-121">The control can be edited; the value associated with the control can be changed.</span></span> <span data-ttu-id="15802-122">Если этот флаг не установлен, то этот флажок будет только для чтения.</span><span class="sxs-lookup"><span data-stu-id="15802-122">When this flag is not set, the control is read-only.</span></span> <span data-ttu-id="15802-123">Это значение игнорируется для элементов управления меткой, полем группы, стандартной кнопкой push-кнопки, многоценным списком и списком.</span><span class="sxs-lookup"><span data-stu-id="15802-123">This value is ignored on label, group box, standard push button, multivalued drop down list box and list box controls.</span></span>
    
<span data-ttu-id="15802-124">DT_MULTILINE</span><span class="sxs-lookup"><span data-stu-id="15802-124">DT_MULTILINE</span></span> 
  
> <span data-ttu-id="15802-125">Редактируемая строка может содержать несколько строк.</span><span class="sxs-lookup"><span data-stu-id="15802-125">The edit control can contain multiple lines.</span></span> <span data-ttu-id="15802-126">Это означает, что в этом средстве управления может быть введен возвращаемый символ.</span><span class="sxs-lookup"><span data-stu-id="15802-126">This means a return character can be entered within the control.</span></span> <span data-ttu-id="15802-127">Этот флаг действителен только для элементов управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="15802-127">This flag is valid for edit controls only.</span></span>
    
<span data-ttu-id="15802-128">DT_PASSWORD_EDIT</span><span class="sxs-lookup"><span data-stu-id="15802-128">DT_PASSWORD_EDIT</span></span> 
  
> <span data-ttu-id="15802-129">Применяется к элементу управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="15802-129">Applies to edit controls.</span></span> <span data-ttu-id="15802-130">Управление редактированием рассматривается как пароль.</span><span class="sxs-lookup"><span data-stu-id="15802-130">The edit control is treated like a password.</span></span> <span data-ttu-id="15802-131">Значение отображается с помощью звездочек вместо того, чтобы в него ввели фактические символы.</span><span class="sxs-lookup"><span data-stu-id="15802-131">The value is displayed using asterisks instead of echoing the actual characters entered.</span></span>
    
<span data-ttu-id="15802-132">DT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="15802-132">DT_REQUIRED</span></span> 
  
> <span data-ttu-id="15802-133">Если перед тем как будет вызван [IMAPIProp::SaveChanges,](imapiprop-savechanges.md) у этого DT_EDITABLE должно быть значение.</span><span class="sxs-lookup"><span data-stu-id="15802-133">If the control allows changes (DT_EDITABLE), it must have a value before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
    
<span data-ttu-id="15802-134">DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="15802-134">DT_SET_IMMEDIATE</span></span> 
  
> <span data-ttu-id="15802-135">Включает немедленную настройку значения; Как только значение в этом объекте изменяется, MAPI вызывает метод **SetProps** для свойства, связанного с этим управлением.</span><span class="sxs-lookup"><span data-stu-id="15802-135">Enables immediate setting of a value; as soon as a value in the control changes, MAPI calls the **SetProps** method for the property associated with that control.</span></span> <span data-ttu-id="15802-136">Если этот флаг не установлен, значения устанавливаются при отклоне диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="15802-136">When this flag is not set, the values are set when the dialog box is dismissed.</span></span> 
    
<span data-ttu-id="15802-137">DT_SET_SELECTION</span><span class="sxs-lookup"><span data-stu-id="15802-137">DT_SET_SELECTION</span></span> 
  
> <span data-ttu-id="15802-138">При выборе в списке столбец индекса этого списка устанавливается как свойство.</span><span class="sxs-lookup"><span data-stu-id="15802-138">When a selection is made within the list box, the index column of that list box is set as a property.</span></span> <span data-ttu-id="15802-139">Всегда используется с DT_SET_IMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="15802-139">Always used with DT_SET_IMMEDIATE.</span></span>
    
<span data-ttu-id="15802-140">Это свойство хранится в члене ulCtlFlags структуры [DTCTL](dtctl.md) для управления.</span><span class="sxs-lookup"><span data-stu-id="15802-140">This property is stored in the ulCtlFlags member of a control's [DTCTL](dtctl.md) structure.</span></span> <span data-ttu-id="15802-141">Большинство флагов элементов управления применяются к всем средствам управления, которые позволяют вводить данные пользователем; Некоторые из них применяются только к редактированию.</span><span class="sxs-lookup"><span data-stu-id="15802-141">Most of the control flags apply to all of the controls that allow user input; a few apply only to the edit control.</span></span> <span data-ttu-id="15802-142">Элементы управления, которые не позволяют пользователю вводить данные, такие как кнопка или метка, устанавливают 0 для своих флагов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="15802-142">Controls that do not allow user input, such as a button or a label, set 0 for their control flags.</span></span> 
  
<span data-ttu-id="15802-143">Многие значения флагов не пояснительные.</span><span class="sxs-lookup"><span data-stu-id="15802-143">Many of the flag values are self-explanatory.</span></span> <span data-ttu-id="15802-144">Например, если DT_REQUIRED для управления, он должен содержать значение, прежде чем диалоговое окно будет разрешено отклонять.</span><span class="sxs-lookup"><span data-stu-id="15802-144">For example, when DT_REQUIRED is set for a control, it must contain a value before the dialog box is allowed to be dismissed.</span></span> <span data-ttu-id="15802-145">Либо поставщик услуг может предоставить значение через реализацию **IMAPIProp,** либо пользователь может ввести его.</span><span class="sxs-lookup"><span data-stu-id="15802-145">Either the service provider can supply a value through its **IMAPIProp** implementation or the user can enter one.</span></span> <span data-ttu-id="15802-146">DT_EDITABLE указывает, что значение для этого управления можно изменить.</span><span class="sxs-lookup"><span data-stu-id="15802-146">DT_EDITABLE indicates that the value for the control can be modified.</span></span> <span data-ttu-id="15802-147">DT_MULTILINE позволяет значению для управления редактированием охватывать несколько строк.</span><span class="sxs-lookup"><span data-stu-id="15802-147">DT_MULTILINE allows the value for an edit control to span multiple lines.</span></span> 
  
<span data-ttu-id="15802-148">Некоторые флаги управления не так очевидны в их значении.</span><span class="sxs-lookup"><span data-stu-id="15802-148">Some control flags are not so obvious in their meaning.</span></span> <span data-ttu-id="15802-149">Когда этот флажок DT_SET_IMMEDIATE, все изменения его значения влияют, как только пользователь переходит на новый.</span><span class="sxs-lookup"><span data-stu-id="15802-149">When a control sets the DT_SET_IMMEDIATE flag, any changes to its value take affect as soon as the user moves to a new control.</span></span> <span data-ttu-id="15802-150">MAPI совершает один вызов метода [IMAPIProp::SetProps](imapiprop-setprops.md) интерфейса свойства для свойства этого управления.</span><span class="sxs-lookup"><span data-stu-id="15802-150">MAPI makes a single call to the property interface's [IMAPIProp::SetProps](imapiprop-setprops.md) method for the control's property.</span></span> <span data-ttu-id="15802-151">Это отличается от поведения по умолчанию, которое состоит в отложении внесения изменений  в значения управления до тех пор, пока пользователь не нажмет кнопку "ОК" или не заберет диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="15802-151">This is different from the default behavior, which is to postpone having changes to control values take effect until after the user selects the **OK** button or dismisses the dialog box.</span></span> <span data-ttu-id="15802-152">Флаг DT_SET_IMMEDIATE часто используется в сочетании с уведомлениями таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="15802-152">The DT_SET_IMMEDIATE flag is often used in combination with display table notifications.</span></span> 
  
<span data-ttu-id="15802-153">В следующей таблице перечислены типы элементов управления и все значения флагов, которые можно установить для каждого типа.</span><span class="sxs-lookup"><span data-stu-id="15802-153">The following table lists the types of controls and all of the flag values that can be set for each type.</span></span>
  
|<span data-ttu-id="15802-154">**Control**</span><span class="sxs-lookup"><span data-stu-id="15802-154">**Control**</span></span>|<span data-ttu-id="15802-155">**Допустимые значения для этого свойства**</span><span class="sxs-lookup"><span data-stu-id="15802-155">**Valid values for this property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="15802-156">Кнопка</span><span class="sxs-lookup"><span data-stu-id="15802-156">Button</span></span>  <br/> |<span data-ttu-id="15802-157">Должно быть нулем</span><span class="sxs-lookup"><span data-stu-id="15802-157">Must be zero</span></span>  <br/> |
|<span data-ttu-id="15802-158">Флажок</span><span class="sxs-lookup"><span data-stu-id="15802-158">Check box</span></span>  <br/> |<span data-ttu-id="15802-159">DT_EDITABLE, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="15802-159">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="15802-160">Поле со списком</span><span class="sxs-lookup"><span data-stu-id="15802-160">Combo box</span></span>  <br/> |<span data-ttu-id="15802-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="15802-161">DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="15802-162">Поле "Список в выпадаемом списке"</span><span class="sxs-lookup"><span data-stu-id="15802-162">Drop-down list box</span></span>  <br/> |<span data-ttu-id="15802-163">DT_EDITABLE, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="15802-163">DT_EDITABLE, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="15802-164">Редактирование</span><span class="sxs-lookup"><span data-stu-id="15802-164">Edit</span></span>  <br/> |<span data-ttu-id="15802-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="15802-165">DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE</span></span>  <br/> |
|<span data-ttu-id="15802-166">Поле группы</span><span class="sxs-lookup"><span data-stu-id="15802-166">Group box</span></span>  <br/> |<span data-ttu-id="15802-167">Должно быть нулем</span><span class="sxs-lookup"><span data-stu-id="15802-167">Must be zero</span></span>  <br/> |
|<span data-ttu-id="15802-168">Метка</span><span class="sxs-lookup"><span data-stu-id="15802-168">Label</span></span>  <br/> |<span data-ttu-id="15802-169">Должно быть нулем</span><span class="sxs-lookup"><span data-stu-id="15802-169">Must be zero</span></span>  <br/> |
|<span data-ttu-id="15802-170">Поле со списком</span><span class="sxs-lookup"><span data-stu-id="15802-170">List box</span></span>  <br/> |<span data-ttu-id="15802-171">Должно быть нулем</span><span class="sxs-lookup"><span data-stu-id="15802-171">Must be zero</span></span>  <br/> |
|<span data-ttu-id="15802-172">Поле "Многоценный" в выпадаемом списке</span><span class="sxs-lookup"><span data-stu-id="15802-172">Multivalue drop-down list box</span></span>  <br/> |<span data-ttu-id="15802-173">Должно быть нулем</span><span class="sxs-lookup"><span data-stu-id="15802-173">Must be zero</span></span>  <br/> |
|<span data-ttu-id="15802-174">Поле со списком с несколькими наценами</span><span class="sxs-lookup"><span data-stu-id="15802-174">Multivalue list box</span></span>  <br/> |<span data-ttu-id="15802-175">Должно быть нулем</span><span class="sxs-lookup"><span data-stu-id="15802-175">Must be zero</span></span>  <br/> |
|<span data-ttu-id="15802-176">Вкладка страницы</span><span class="sxs-lookup"><span data-stu-id="15802-176">Tabbed page</span></span>  <br/> |<span data-ttu-id="15802-177">Должно быть нулем</span><span class="sxs-lookup"><span data-stu-id="15802-177">Must be zero</span></span>  <br/> |
|<span data-ttu-id="15802-178">Кнопка "Радио"</span><span class="sxs-lookup"><span data-stu-id="15802-178">Radio button</span></span>  <br/> |<span data-ttu-id="15802-179">Должно быть нулем</span><span class="sxs-lookup"><span data-stu-id="15802-179">Must be zero</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="15802-180">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="15802-180">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="15802-181">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="15802-181">Header files</span></span>

<span data-ttu-id="15802-182">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="15802-182">Mapidefs.h</span></span>
  
> <span data-ttu-id="15802-183">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="15802-183">Provides data type definitions.</span></span>
    
<span data-ttu-id="15802-184">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="15802-184">Mapitags.h</span></span>
  
> <span data-ttu-id="15802-185">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="15802-185">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="15802-186">См. также</span><span class="sxs-lookup"><span data-stu-id="15802-186">See also</span></span>



[<span data-ttu-id="15802-187">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="15802-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="15802-188">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="15802-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="15802-189">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="15802-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="15802-190">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="15802-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

