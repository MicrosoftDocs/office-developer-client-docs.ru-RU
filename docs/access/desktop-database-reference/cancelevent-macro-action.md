---
title: Макрокоманда CancelEvent
TOCTitle: CancelEvent macro action
ms:assetid: d9d3ea99-c9fb-2524-c570-e3ee6d20af98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835110(v=office.15)
ms:contentKeyID: 48548066
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm78430
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b55fc51f70bcc2c9d2f7e93cf9c79228cd2fe440
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296635"
---
# <a name="cancelevent-macro-action"></a><span data-ttu-id="57fbb-102">Макрокоманда CancelEvent</span><span class="sxs-lookup"><span data-stu-id="57fbb-102">CancelEvent macro action</span></span>

<span data-ttu-id="57fbb-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="57fbb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="57fbb-104">Действие **CancelEvent** можно использовать для отмены события, из-за чего Access запускал макрос, содержащий это действие.</span><span class="sxs-lookup"><span data-stu-id="57fbb-104">You can use the **CancelEvent** action to cancel the event that caused Access to run the macro containing this action.</span></span> <span data-ttu-id="57fbb-105">Имя макроса — это параметр свойства события, например **BeforeUpdate,** **OnOpen,** **OnUnload** или **OnPrint.**</span><span class="sxs-lookup"><span data-stu-id="57fbb-105">The macro name is the setting of an event property such as **BeforeUpdate**, **OnOpen**, **OnUnload**, or **OnPrint**.</span></span>

## <a name="setting"></a><span data-ttu-id="57fbb-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="57fbb-106">Setting</span></span>

<span data-ttu-id="57fbb-107">Действие **CancelEvent** не имеет аргументов.</span><span class="sxs-lookup"><span data-stu-id="57fbb-107">The **CancelEvent** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="57fbb-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="57fbb-108">Remarks</span></span>

<span data-ttu-id="57fbb-109">В форме обычно используется действие **CancelEvent** в макрос проверки с свойством **событий BeforeUpdate.**</span><span class="sxs-lookup"><span data-stu-id="57fbb-109">In a form, you typically use the **CancelEvent** action in a validation macro with the **BeforeUpdate** event property.</span></span> <span data-ttu-id="57fbb-110">Когда пользователь вводит данные в управление или запись, Access запускает макрос перед добавлением данных в базу данных.</span><span class="sxs-lookup"><span data-stu-id="57fbb-110">When a user enters data in a control or record, Access runs the macro before adding the data to the database.</span></span> <span data-ttu-id="57fbb-111">Если данные не справят условия проверки в макрос, действие **CancelEvent** отменяет процесс обновления перед его началом.</span><span class="sxs-lookup"><span data-stu-id="57fbb-111">If the data fails the validation conditions in the macro, the **CancelEvent** action cancels the update process before it starts.</span></span>

<span data-ttu-id="57fbb-112">Часто вы используете это действие с действием **MessageBox,** чтобы указать, что данные не удалось с условиями проверки, и предоставить полезную информацию о том, какие данные должны быть введены.</span><span class="sxs-lookup"><span data-stu-id="57fbb-112">Often, you use this action with the **MessageBox** action to indicate that the data has failed the validation conditions and to provide helpful information about the kind of data that should be entered.</span></span>

<span data-ttu-id="57fbb-113">Следующие события могут быть отменены **действием CancelEvent.**</span><span class="sxs-lookup"><span data-stu-id="57fbb-113">The following events can be canceled by the **CancelEvent** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57fbb-114"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="57fbb-114"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="57fbb-115"><strong>Dirty</strong></span><span class="sxs-lookup"><span data-stu-id="57fbb-115"><strong>Dirty</strong></span></span></p></td>
<td><p><span data-ttu-id="57fbb-116"><strong>MouseDown</strong></span><span class="sxs-lookup"><span data-stu-id="57fbb-116"><strong>MouseDown</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57fbb-117"><strong>BeforeDelConfirm</strong></span><span class="sxs-lookup"><span data-stu-id="57fbb-117"><strong>BeforeDelConfirm</strong></span></span></p></td>
<td><p><span data-ttu-id="57fbb-118"><strong>Exit</strong></span><span class="sxs-lookup"><span data-stu-id="57fbb-118"><strong>Exit</strong></span></span></p></td>
<td><p><span data-ttu-id="57fbb-119"><strong>NoData</strong></span><span class="sxs-lookup"><span data-stu-id="57fbb-119"><strong>NoData</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57fbb-120"><strong>BeforeInsert</strong></span><span class="sxs-lookup"><span data-stu-id="57fbb-120"><strong>BeforeInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="57fbb-121"><strong>Filter</strong></span><span class="sxs-lookup"><span data-stu-id="57fbb-121"><strong>Filter</strong></span></span></p></td>
<td><p><span data-ttu-id="57fbb-122"><strong>Open</strong></span><span class="sxs-lookup"><span data-stu-id="57fbb-122"><strong>Open</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57fbb-123"><strong>BeforeUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="57fbb-123"><strong>BeforeUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="57fbb-124"><strong>Format</strong></span><span class="sxs-lookup"><span data-stu-id="57fbb-124"><strong>Format</strong></span></span></p></td>
<td><p><span data-ttu-id="57fbb-125"><strong>Print</strong></span><span class="sxs-lookup"><span data-stu-id="57fbb-125"><strong>Print</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57fbb-126"><strong>DblClick</strong></span><span class="sxs-lookup"><span data-stu-id="57fbb-126"><strong>DblClick</strong></span></span></p></td>
<td><p><span data-ttu-id="57fbb-127"><strong>KeyPress</strong></span><span class="sxs-lookup"><span data-stu-id="57fbb-127"><strong>KeyPress</strong></span></span></p></td>
<td><p><span data-ttu-id="57fbb-128"><strong>Unload</strong></span><span class="sxs-lookup"><span data-stu-id="57fbb-128"><strong>Unload</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57fbb-129"><strong>Delete</strong></span><span class="sxs-lookup"><span data-stu-id="57fbb-129"><strong>Delete</strong></span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="57fbb-130">Вы можете использовать **действие CancelEvent** с событием **MouseDown** только для отмены события, которое происходит при правой кнопке мыши объекта.</span><span class="sxs-lookup"><span data-stu-id="57fbb-130">You can use the **CancelEvent** action with the **MouseDown** event only to cancel the event that occurs when you right-click an object.</span></span>

<span data-ttu-id="57fbb-131">Если параметр свойства **событий OnDblClick** управления указывает макрос, содержащий действие **CancelEvent,** действие отменяет **событие DblClick.**</span><span class="sxs-lookup"><span data-stu-id="57fbb-131">If a control's **OnDblClick** event property setting specifies a macro containing the **CancelEvent** action, the action cancels the **DblClick** event.</span></span>

<span data-ttu-id="57fbb-132">Для событий, которые можно отменить, поведение по умолчанию для события (то есть то, что access обычно делает при событии) возникает после того, как выполняется макрос для события.</span><span class="sxs-lookup"><span data-stu-id="57fbb-132">For events that can be canceled, the default behavior for the event (that is, what Access typically does when the event occurs) occurs after the macro for the event runs.</span></span> <span data-ttu-id="57fbb-133">Это позволяет отменить поведение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="57fbb-133">This enables you to cancel the default behavior.</span></span> <span data-ttu-id="57fbb-134">Например, если дважды щелкнуть слово, на которое включена точка вставки в текстовом окне, Access обычно выбирает слово.</span><span class="sxs-lookup"><span data-stu-id="57fbb-134">For example, when you double-click a word that the insertion point is on in a text box, Access normally selects the word.</span></span> <span data-ttu-id="57fbb-135">Вы можете отменить это поведение по умолчанию в макрос для **события DblClick** и выполнить некоторые другие действия, например открытие формы, содержащей сведения о данных в текстовом окне.</span><span class="sxs-lookup"><span data-stu-id="57fbb-135">You can cancel this default behavior in the macro for the **DblClick** event and perform some other action, such as opening a form containing information about the data in the text box.</span></span> <span data-ttu-id="57fbb-136">Для событий, которые нельзя отменить, поведение по умолчанию происходит перед запуском макроса.</span><span class="sxs-lookup"><span data-stu-id="57fbb-136">For events that can't be canceled, the default behavior occurs before the macro runs.</span></span>

> [!NOTE]
> <span data-ttu-id="57fbb-137">Если свойство события **OnUnload** формы указывает макрос, который выполняет действие **CancelEvent,** вы не сможете закрыть форму.</span><span class="sxs-lookup"><span data-stu-id="57fbb-137">If a form's **OnUnload** event property specifies a macro that carries out a **CancelEvent** action, you won't be able to close the form.</span></span> <span data-ttu-id="57fbb-138">Необходимо либо исправить условие, из-за чего было выполнено действие **CancelEvent,** либо открыть макрос и удалить **действие CancelEvent.**</span><span class="sxs-lookup"><span data-stu-id="57fbb-138">You must either correct the condition that caused the **CancelEvent** action to be carried out or open the macro and delete the **CancelEvent** action.</span></span> <span data-ttu-id="57fbb-139">Если форма является модальной формой, вы не сможете открыть макрос.</span><span class="sxs-lookup"><span data-stu-id="57fbb-139">If the form is a modal form, you won't be able to open the macro.</span></span>

<span data-ttu-id="57fbb-140">Чтобы выполнить действие **CancelEvent** в модуле Visual Basic для приложений (VBA), используйте метод **CancelEvent** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="57fbb-140">To carry out the **CancelEvent** action in a Visual Basic for Applications (VBA) module, use the **CancelEvent** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="57fbb-141">Пример</span><span class="sxs-lookup"><span data-stu-id="57fbb-141">Example</span></span>

<span data-ttu-id="57fbb-142">Проверка данных с помощью макроса</span><span class="sxs-lookup"><span data-stu-id="57fbb-142">Validate data by using a macro</span></span>

<span data-ttu-id="57fbb-143">Следующий макрос проверки проверяет почтовые коды, вступив в форму Поставщики.</span><span class="sxs-lookup"><span data-stu-id="57fbb-143">The following validation macro checks the postal codes entered in a Suppliers form.</span></span> <span data-ttu-id="57fbb-144">В нем показано использование действий **StopMacro,** **MessageBox,** **CancelEvent** и **GoToControl.**</span><span class="sxs-lookup"><span data-stu-id="57fbb-144">It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions.</span></span> <span data-ttu-id="57fbb-145">Условное выражение проверяет страну/регион и почтовый код, вписаный в запись в форме.</span><span class="sxs-lookup"><span data-stu-id="57fbb-145">A conditional expression checks the country/region and postal code entered in a record on the form.</span></span> <span data-ttu-id="57fbb-146">Если почтовый код не находится в нужном формате для страны или региона, макрос отображает окно сообщений и отменяет сохранение записи.</span><span class="sxs-lookup"><span data-stu-id="57fbb-146">If the postal code is not in the right format for the country/region, the macro displays a message box and cancels saving the record.</span></span> <span data-ttu-id="57fbb-147">Затем возвращается управление почтовым кодом, где можно исправить ошибку.</span><span class="sxs-lookup"><span data-stu-id="57fbb-147">It then returns you to the Postal Code control, where you can correct the error.</span></span> <span data-ttu-id="57fbb-148">Этот макрос должен быть присоединен к свойству **BeforeUpdate** формы Поставщики.</span><span class="sxs-lookup"><span data-stu-id="57fbb-148">This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="57fbb-149">Условие</span><span class="sxs-lookup"><span data-stu-id="57fbb-149">Condition</span></span></p></th>
<th><p><span data-ttu-id="57fbb-150">Макрокоманда</span><span class="sxs-lookup"><span data-stu-id="57fbb-150">Action</span></span></p></th>
<th><p><span data-ttu-id="57fbb-151">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="57fbb-151">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="57fbb-152">Примечание</span><span class="sxs-lookup"><span data-stu-id="57fbb-152">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57fbb-153">IsNull([CountryRegion])</span><span class="sxs-lookup"><span data-stu-id="57fbb-153">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="57fbb-154">StopMacro</span><span class="sxs-lookup"><span data-stu-id="57fbb-154">StopMacro</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="57fbb-155">Если CountryRegion <strong>является Null,</strong>почтовый код не может быть проверен.</span><span class="sxs-lookup"><span data-stu-id="57fbb-155">If CountryRegion is <strong>Null</strong>, postal code can't be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57fbb-156">[CountryRegion] В ( &quot; &quot; Франция, &quot; &quot; Италия, &quot; Испания &quot; ) и Len ([Почтовый код]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="57fbb-156">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([Postal Code]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="57fbb-157">MessageBox</span><span class="sxs-lookup"><span data-stu-id="57fbb-157">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="57fbb-158">Сообщение. Почтовый код должен быть 5 символов.</span><span class="sxs-lookup"><span data-stu-id="57fbb-158">Message: The postal code must be 5 characters.</span></span> <span data-ttu-id="57fbb-159">Звуковой сигнал: <strong>Да</strong> тип: <strong>название</strong> информации: ошибка почтового кода</span><span class="sxs-lookup"><span data-stu-id="57fbb-159">Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="57fbb-160">Если почтовый код не имеет 5 символов, отобразить сообщение.</span><span class="sxs-lookup"><span data-stu-id="57fbb-160">If the postal code isn't 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57fbb-161">...</span><span class="sxs-lookup"><span data-stu-id="57fbb-161">...</span></span></p></td>
<td><p><span data-ttu-id="57fbb-162">ОтменитьСобытие</span><span class="sxs-lookup"><span data-stu-id="57fbb-162">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="57fbb-163">Отмена события.</span><span class="sxs-lookup"><span data-stu-id="57fbb-163">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="57fbb-164">GoToControl</span><span class="sxs-lookup"><span data-stu-id="57fbb-164">GoToControl</span></span></p></td>
<td><p><span data-ttu-id="57fbb-165">Имя управления: PostalCode</span><span class="sxs-lookup"><span data-stu-id="57fbb-165">Control Name: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57fbb-166">[CountryRegion] В ( &quot; Австралия , Сингапур ) и &quot; &quot; &quot; Len ([Почтовый код]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="57fbb-166">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([Postal Code]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="57fbb-167">MessageBox</span><span class="sxs-lookup"><span data-stu-id="57fbb-167">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="57fbb-168">Сообщение. Почтовый код должен быть 4 символа.</span><span class="sxs-lookup"><span data-stu-id="57fbb-168">Message: The postal code must be 4 characters.</span></span> <span data-ttu-id="57fbb-169">Звуковой сигнал: <strong>Да</strong> тип: <strong>название</strong> информации: ошибка почтового кода</span><span class="sxs-lookup"><span data-stu-id="57fbb-169">Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="57fbb-170">Если почтовый код не 4 символа, отобразить сообщение.</span><span class="sxs-lookup"><span data-stu-id="57fbb-170">If the postal code isn't 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57fbb-171">...</span><span class="sxs-lookup"><span data-stu-id="57fbb-171">...</span></span></p></td>
<td><p><span data-ttu-id="57fbb-172">ОтменитьСобытие</span><span class="sxs-lookup"><span data-stu-id="57fbb-172">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="57fbb-173">Отмена события.</span><span class="sxs-lookup"><span data-stu-id="57fbb-173">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="57fbb-174">GoToControl</span><span class="sxs-lookup"><span data-stu-id="57fbb-174">GoToControl</span></span></p></td>
<td><p><span data-ttu-id="57fbb-175">Имя управления: PostalCode</span><span class="sxs-lookup"><span data-stu-id="57fbb-175">Control Name: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57fbb-176">([CountryRegion] = &quot; Канада ) и &quot; ([Почтовый код] Не нравится &quot; [A-Z][0-9][A-Z] [0-9][A-Z][0-9] &quot; )</span><span class="sxs-lookup"><span data-stu-id="57fbb-176">([CountryRegion] = &quot;Canada&quot;) And ([Postal Code] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="57fbb-177">MessageBox</span><span class="sxs-lookup"><span data-stu-id="57fbb-177">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="57fbb-178">Сообщение. Почтовый код не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="57fbb-178">Message: The postal code is not valid.</span></span> <span data-ttu-id="57fbb-179">Пример канадского кода: звуковой сигнал H1J 1C3: <strong>Да</strong> <strong>тип:</strong> название информации: ошибка почтового кода</span><span class="sxs-lookup"><span data-stu-id="57fbb-179">Example of Canadian code: H1J 1C3 Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="57fbb-180">Если почтовый код не является правильным для Канады, отобразить сообщение.</span><span class="sxs-lookup"><span data-stu-id="57fbb-180">If the postal code isn't correct for Canada, display a message.</span></span> <span data-ttu-id="57fbb-181">(Пример канадского кода: H1J 1C3)</span><span class="sxs-lookup"><span data-stu-id="57fbb-181">(Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57fbb-182">...</span><span class="sxs-lookup"><span data-stu-id="57fbb-182">...</span></span></p></td>
<td><p><span data-ttu-id="57fbb-183">ОтменитьСобытие</span><span class="sxs-lookup"><span data-stu-id="57fbb-183">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="57fbb-184">Отмена события.</span><span class="sxs-lookup"><span data-stu-id="57fbb-184">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

