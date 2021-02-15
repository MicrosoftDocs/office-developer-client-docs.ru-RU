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
# <a name="cancelevent-macro-action"></a><span data-ttu-id="7b5cc-102">Макрокоманда CancelEvent</span><span class="sxs-lookup"><span data-stu-id="7b5cc-102">CancelEvent macro action</span></span>

<span data-ttu-id="7b5cc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7b5cc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7b5cc-104">Действие **CancelEvent** можно использовать для отмены события, которое вызвало запуск макроса, содержащего это действие, в Access.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-104">You can use the **CancelEvent** action to cancel the event that caused Access to run the macro containing this action.</span></span> <span data-ttu-id="7b5cc-105">Имя макроса — это параметр свойства события, например **BeforeUpdate,** **OnOpen,** **OnUnload** или **OnPrint.**</span><span class="sxs-lookup"><span data-stu-id="7b5cc-105">The macro name is the setting of an event property such as **BeforeUpdate**, **OnOpen**, **OnUnload**, or **OnPrint**.</span></span>

## <a name="setting"></a><span data-ttu-id="7b5cc-106">Setting</span><span class="sxs-lookup"><span data-stu-id="7b5cc-106">Setting</span></span>

<span data-ttu-id="7b5cc-107">Действие **CancelEvent** не имеет аргументов.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-107">The **CancelEvent** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b5cc-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="7b5cc-108">Remarks</span></span>

<span data-ttu-id="7b5cc-109">В форме обычно используется действие **CancelEvent** в макросах проверки со свойством события **BeforeUpdate.**</span><span class="sxs-lookup"><span data-stu-id="7b5cc-109">In a form, you typically use the **CancelEvent** action in a validation macro with the **BeforeUpdate** event property.</span></span> <span data-ttu-id="7b5cc-110">Когда пользователь вводит данные в control или запись, Access запускает макрос перед добавлением данных в базу данных.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-110">When a user enters data in a control or record, Access runs the macro before adding the data to the database.</span></span> <span data-ttu-id="7b5cc-111">Если данные не удается проверки условий макроса, действие **CancelEvent** отменяет процесс обновления перед его началом.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-111">If the data fails the validation conditions in the macro, the **CancelEvent** action cancels the update process before it starts.</span></span>

<span data-ttu-id="7b5cc-112">Часто это действие используется с действием **MessageBox,** чтобы указать, что данные не удалось проверки условий и предоставить полезную информацию о типе данных, которые должны быть введены.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-112">Often, you use this action with the **MessageBox** action to indicate that the data has failed the validation conditions and to provide helpful information about the kind of data that should be entered.</span></span>

<span data-ttu-id="7b5cc-113">Следующие события могут быть отменены **действием CancelEvent.**</span><span class="sxs-lookup"><span data-stu-id="7b5cc-113">The following events can be canceled by the **CancelEvent** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7b5cc-114"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="7b5cc-114"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="7b5cc-115"><strong>Dirty</strong></span><span class="sxs-lookup"><span data-stu-id="7b5cc-115"><strong>Dirty</strong></span></span></p></td>
<td><p><span data-ttu-id="7b5cc-116"><strong>MouseDown</strong></span><span class="sxs-lookup"><span data-stu-id="7b5cc-116"><strong>MouseDown</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b5cc-117"><strong>BeforeDelConfirm</strong></span><span class="sxs-lookup"><span data-stu-id="7b5cc-117"><strong>BeforeDelConfirm</strong></span></span></p></td>
<td><p><span data-ttu-id="7b5cc-118"><strong>Exit</strong></span><span class="sxs-lookup"><span data-stu-id="7b5cc-118"><strong>Exit</strong></span></span></p></td>
<td><p><span data-ttu-id="7b5cc-119"><strong>NoData</strong></span><span class="sxs-lookup"><span data-stu-id="7b5cc-119"><strong>NoData</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b5cc-120"><strong>BeforeInsert</strong></span><span class="sxs-lookup"><span data-stu-id="7b5cc-120"><strong>BeforeInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="7b5cc-121"><strong>Фильтр</strong></span><span class="sxs-lookup"><span data-stu-id="7b5cc-121"><strong>Filter</strong></span></span></p></td>
<td><p><span data-ttu-id="7b5cc-122"><strong>Open</strong></span><span class="sxs-lookup"><span data-stu-id="7b5cc-122"><strong>Open</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b5cc-123"><strong>BeforeUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="7b5cc-123"><strong>BeforeUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="7b5cc-124"><strong>Формат</strong></span><span class="sxs-lookup"><span data-stu-id="7b5cc-124"><strong>Format</strong></span></span></p></td>
<td><p><span data-ttu-id="7b5cc-125"><strong>Print</strong></span><span class="sxs-lookup"><span data-stu-id="7b5cc-125"><strong>Print</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b5cc-126"><strong>DblClick</strong></span><span class="sxs-lookup"><span data-stu-id="7b5cc-126"><strong>DblClick</strong></span></span></p></td>
<td><p><span data-ttu-id="7b5cc-127"><strong>KeyPress</strong></span><span class="sxs-lookup"><span data-stu-id="7b5cc-127"><strong>KeyPress</strong></span></span></p></td>
<td><p><span data-ttu-id="7b5cc-128"><strong>Unload</strong></span><span class="sxs-lookup"><span data-stu-id="7b5cc-128"><strong>Unload</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b5cc-129"><strong>удаление</strong>;</span><span class="sxs-lookup"><span data-stu-id="7b5cc-129"><strong>Delete</strong></span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="7b5cc-130">Действие **CancelEvent** с событием **MouseDown** можно использовать только для отмены события, которое происходит при щелчке правой кнопкой мыши по объекту.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-130">You can use the **CancelEvent** action with the **MouseDown** event only to cancel the event that occurs when you right-click an object.</span></span>

<span data-ttu-id="7b5cc-131">Если параметр свойства события **OnDblClick** для управления указывает макрос, содержащий действие **CancelEvent,** действие отменяет **событие DblClick.**</span><span class="sxs-lookup"><span data-stu-id="7b5cc-131">If a control's **OnDblClick** event property setting specifies a macro containing the **CancelEvent** action, the action cancels the **DblClick** event.</span></span>

<span data-ttu-id="7b5cc-132">Для событий, которые можно отменить, поведение по умолчанию для события (то есть, что Access обычно делает при событии) происходит после того, как выполняется макрос для события.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-132">For events that can be canceled, the default behavior for the event (that is, what Access typically does when the event occurs) occurs after the macro for the event runs.</span></span> <span data-ttu-id="7b5cc-133">Это позволяет отменить поведение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-133">This enables you to cancel the default behavior.</span></span> <span data-ttu-id="7b5cc-134">Например, если дважды щелкнуть слово, в которое включена точка вставки в текстовом поле, Access обычно выбирает это слово.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-134">For example, when you double-click a word that the insertion point is on in a text box, Access normally selects the word.</span></span> <span data-ttu-id="7b5cc-135">Можно отменить это поведение по умолчанию в макросах для события **DblClick** и выполнить какое-либо другое действие, например открытие формы, содержащей сведения о данных в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-135">You can cancel this default behavior in the macro for the **DblClick** event and perform some other action, such as opening a form containing information about the data in the text box.</span></span> <span data-ttu-id="7b5cc-136">Для событий, которые не могут быть отменены, поведение по умолчанию происходит перед запуском макроса.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-136">For events that can't be canceled, the default behavior occurs before the macro runs.</span></span>

> [!NOTE]
> <span data-ttu-id="7b5cc-137">Если свойство события **OnUnload** формы указывает макрос, который выполняет действие **CancelEvent,** закрыть форму будет нельзя.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-137">If a form's **OnUnload** event property specifies a macro that carries out a **CancelEvent** action, you won't be able to close the form.</span></span> <span data-ttu-id="7b5cc-138">Необходимо либо исправить условие, из-за чего было выполнено действие **CancelEvent,** либо открыть макрос и удалить действие **CancelEvent.**</span><span class="sxs-lookup"><span data-stu-id="7b5cc-138">You must either correct the condition that caused the **CancelEvent** action to be carried out or open the macro and delete the **CancelEvent** action.</span></span> <span data-ttu-id="7b5cc-139">Если форма является модальной, вы не сможете открыть макрос.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-139">If the form is a modal form, you won't be able to open the macro.</span></span>

<span data-ttu-id="7b5cc-140">Чтобы выполнить действие **CancelEvent** в модуле Visual Basic для приложений VBA, используйте метод **CancelEvent** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="7b5cc-140">To carry out the **CancelEvent** action in a Visual Basic for Applications (VBA) module, use the **CancelEvent** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="7b5cc-141">Пример</span><span class="sxs-lookup"><span data-stu-id="7b5cc-141">Example</span></span>

<span data-ttu-id="7b5cc-142">Проверка данных с помощью макроса</span><span class="sxs-lookup"><span data-stu-id="7b5cc-142">Validate data by using a macro</span></span>

<span data-ttu-id="7b5cc-143">Следующий макрос проверки проверяет почтовые коды, вступив в форму "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="7b5cc-143">The following validation macro checks the postal codes entered in a Suppliers form.</span></span> <span data-ttu-id="7b5cc-144">Здесь показано использование действий **StopMacro,** **MessageBox,** **CancelEvent** и **GoToControl.**</span><span class="sxs-lookup"><span data-stu-id="7b5cc-144">It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions.</span></span> <span data-ttu-id="7b5cc-145">Условное выражение проверяет страну или регион и почтовый код, внося в запись в форме.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-145">A conditional expression checks the country/region and postal code entered in a record on the form.</span></span> <span data-ttu-id="7b5cc-146">Если почтовый код не имеет нужного формата для страны или региона, макрос отображает окно сообщения и отменяет сохранение записи.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-146">If the postal code is not in the right format for the country/region, the macro displays a message box and cancels saving the record.</span></span> <span data-ttu-id="7b5cc-147">Затем он возвращает вас в почтовый индекс, где можно исправить ошибку.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-147">It then returns you to the Postal Code control, where you can correct the error.</span></span> <span data-ttu-id="7b5cc-148">Этот макрос должен быть присоединен к свойству **BeforeUpdate** формы "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="7b5cc-148">This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7b5cc-149">Condition</span><span class="sxs-lookup"><span data-stu-id="7b5cc-149">Condition</span></span></p></th>
<th><p><span data-ttu-id="7b5cc-150">Макрокоманда</span><span class="sxs-lookup"><span data-stu-id="7b5cc-150">Action</span></span></p></th>
<th><p><span data-ttu-id="7b5cc-151">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="7b5cc-151">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="7b5cc-152">Примечание</span><span class="sxs-lookup"><span data-stu-id="7b5cc-152">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7b5cc-153">IsNull([CountryRegion])</span><span class="sxs-lookup"><span data-stu-id="7b5cc-153">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="7b5cc-154">StopMacro</span><span class="sxs-lookup"><span data-stu-id="7b5cc-154">StopMacro</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7b5cc-155">Если countryRegion имеет <strong>null,</strong>почтовый код не может быть проверен.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-155">If CountryRegion is <strong>Null</strong>, postal code can't be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b5cc-156">[CountryRegion] In &quot; &quot; (Франция, &quot; &quot; Италия, &quot; &quot; Испания) и Len([Почтовый индекс]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="7b5cc-156">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([Postal Code]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="7b5cc-157">MessageBox</span><span class="sxs-lookup"><span data-stu-id="7b5cc-157">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="7b5cc-158">Сообщение: почтовый код должен иметь 5 символов.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-158">Message: The postal code must be 5 characters.</span></span> <span data-ttu-id="7b5cc-159">Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span><span class="sxs-lookup"><span data-stu-id="7b5cc-159">Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="7b5cc-160">Если почтовый индекс не имеет 5 символов, отобразить сообщение.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-160">If the postal code isn't 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b5cc-161">...</span><span class="sxs-lookup"><span data-stu-id="7b5cc-161">...</span></span></p></td>
<td><p><span data-ttu-id="7b5cc-162">ОтменитьСобытие</span><span class="sxs-lookup"><span data-stu-id="7b5cc-162">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7b5cc-163">Отмените событие.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-163">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="7b5cc-164">GoToControl</span><span class="sxs-lookup"><span data-stu-id="7b5cc-164">GoToControl</span></span></p></td>
<td><p><span data-ttu-id="7b5cc-165">Имя управления: PostalCode</span><span class="sxs-lookup"><span data-stu-id="7b5cc-165">Control Name: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b5cc-166">[CountryRegion] In &quot; &quot; (Australia, &quot; &quot; Singapore) and Len([Postal Code]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="7b5cc-166">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([Postal Code]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="7b5cc-167">MessageBox</span><span class="sxs-lookup"><span data-stu-id="7b5cc-167">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="7b5cc-168">Сообщение: почтовый индекс должен иметь 4 символа.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-168">Message: The postal code must be 4 characters.</span></span> <span data-ttu-id="7b5cc-169">Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span><span class="sxs-lookup"><span data-stu-id="7b5cc-169">Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="7b5cc-170">Если почтовый индекс не имеет 4 символов, отобразить сообщение.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-170">If the postal code isn't 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b5cc-171">...</span><span class="sxs-lookup"><span data-stu-id="7b5cc-171">...</span></span></p></td>
<td><p><span data-ttu-id="7b5cc-172">ОтменитьСобытие</span><span class="sxs-lookup"><span data-stu-id="7b5cc-172">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7b5cc-173">Отмените событие.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-173">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="7b5cc-174">GoToControl</span><span class="sxs-lookup"><span data-stu-id="7b5cc-174">GoToControl</span></span></p></td>
<td><p><span data-ttu-id="7b5cc-175">Имя управления: PostalCode</span><span class="sxs-lookup"><span data-stu-id="7b5cc-175">Control Name: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b5cc-176">([CountryRegion] = &quot; Канада) и ([Почтовый код] не нравится &quot; &quot; [A-Z][0-9][A-Z] [0-9][A-Z][0-9] &quot; )</span><span class="sxs-lookup"><span data-stu-id="7b5cc-176">([CountryRegion] = &quot;Canada&quot;) And ([Postal Code] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="7b5cc-177">MessageBox</span><span class="sxs-lookup"><span data-stu-id="7b5cc-177">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="7b5cc-178">Сообщение: почтовый индекс не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-178">Message: The postal code is not valid.</span></span> <span data-ttu-id="7b5cc-179">Пример кода для Канады: H1J 1C3 Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span><span class="sxs-lookup"><span data-stu-id="7b5cc-179">Example of Canadian code: H1J 1C3 Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="7b5cc-180">Если почтовый индекс неправиа для Канады, отобразить сообщение.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-180">If the postal code isn't correct for Canada, display a message.</span></span> <span data-ttu-id="7b5cc-181">(Пример кода для Канады: H1J 1C3)</span><span class="sxs-lookup"><span data-stu-id="7b5cc-181">(Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b5cc-182">...</span><span class="sxs-lookup"><span data-stu-id="7b5cc-182">...</span></span></p></td>
<td><p><span data-ttu-id="7b5cc-183">ОтменитьСобытие</span><span class="sxs-lookup"><span data-stu-id="7b5cc-183">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7b5cc-184">Отмените событие.</span><span class="sxs-lookup"><span data-stu-id="7b5cc-184">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

