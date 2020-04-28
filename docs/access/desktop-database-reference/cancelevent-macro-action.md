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
# <a name="cancelevent-macro-action"></a><span data-ttu-id="7e1d9-102">Макрокоманда CancelEvent</span><span class="sxs-lookup"><span data-stu-id="7e1d9-102">CancelEvent macro action</span></span>

<span data-ttu-id="7e1d9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e1d9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7e1d9-104">Вы можете использовать действие **Макрокоманда CancelEvent** , чтобы отменить событие, которое привело к запуску макроса, содержащего это действие.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-104">You can use the **CancelEvent** action to cancel the event that caused Access to run the macro containing this action.</span></span> <span data-ttu-id="7e1d9-105">Имя макроса — это значение свойства события, например " **до обновления**", " **OnOpen**", " **OnOpen**" или " **OnOpen**".</span><span class="sxs-lookup"><span data-stu-id="7e1d9-105">The macro name is the setting of an event property such as **BeforeUpdate**, **OnOpen**, **OnUnload**, or **OnPrint**.</span></span>

## <a name="setting"></a><span data-ttu-id="7e1d9-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="7e1d9-106">Setting</span></span>

<span data-ttu-id="7e1d9-107">Макрокоманда **Макрокоманда CancelEvent** не содержит аргументов.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-107">The **CancelEvent** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e1d9-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="7e1d9-108">Remarks</span></span>

<span data-ttu-id="7e1d9-109">В форме, как правило, используется действие **Макрокоманда CancelEvent** в макросе проверки с свойством **до обновления** события.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-109">In a form, you typically use the **CancelEvent** action in a validation macro with the **BeforeUpdate** event property.</span></span> <span data-ttu-id="7e1d9-110">Когда пользователь вводит данные в элемент управления или запись, Access выполняет макрос перед добавлением данных в базу данных.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-110">When a user enters data in a control or record, Access runs the macro before adding the data to the database.</span></span> <span data-ttu-id="7e1d9-111">Если данные не прошли условия проверки в макросе, действие **Макрокоманда CancelEvent** отменяет процесс обновления перед запуском.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-111">If the data fails the validation conditions in the macro, the **CancelEvent** action cancels the update process before it starts.</span></span>

<span data-ttu-id="7e1d9-112">Часто вы используете это действие с действием **MessageBox** , чтобы указать, что данные не прошли условия проверки и содержат полезную информацию о типе вводимых данных.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-112">Often, you use this action with the **MessageBox** action to indicate that the data has failed the validation conditions and to provide helpful information about the kind of data that should be entered.</span></span>

<span data-ttu-id="7e1d9-113">Действие **Макрокоманда CancelEvent** может отменять следующие события.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-113">The following events can be canceled by the **CancelEvent** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e1d9-114"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="7e1d9-114"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="7e1d9-115"><strong>Dirty</strong></span><span class="sxs-lookup"><span data-stu-id="7e1d9-115"><strong>Dirty</strong></span></span></p></td>
<td><p><span data-ttu-id="7e1d9-116"><strong>MouseDown</strong></span><span class="sxs-lookup"><span data-stu-id="7e1d9-116"><strong>MouseDown</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e1d9-117"><strong>BeforeDelConfirm</strong></span><span class="sxs-lookup"><span data-stu-id="7e1d9-117"><strong>BeforeDelConfirm</strong></span></span></p></td>
<td><p><span data-ttu-id="7e1d9-118"><strong>Exit</strong></span><span class="sxs-lookup"><span data-stu-id="7e1d9-118"><strong>Exit</strong></span></span></p></td>
<td><p><span data-ttu-id="7e1d9-119"><strong>NoData</strong></span><span class="sxs-lookup"><span data-stu-id="7e1d9-119"><strong>NoData</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e1d9-120"><strong>BeforeInsert</strong></span><span class="sxs-lookup"><span data-stu-id="7e1d9-120"><strong>BeforeInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="7e1d9-121"><strong>Filter</strong></span><span class="sxs-lookup"><span data-stu-id="7e1d9-121"><strong>Filter</strong></span></span></p></td>
<td><p><span data-ttu-id="7e1d9-122"><strong>Open</strong></span><span class="sxs-lookup"><span data-stu-id="7e1d9-122"><strong>Open</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e1d9-123"><strong>BeforeUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="7e1d9-123"><strong>BeforeUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="7e1d9-124"><strong>Формат</strong></span><span class="sxs-lookup"><span data-stu-id="7e1d9-124"><strong>Format</strong></span></span></p></td>
<td><p><span data-ttu-id="7e1d9-125"><strong>Print</strong></span><span class="sxs-lookup"><span data-stu-id="7e1d9-125"><strong>Print</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e1d9-126"><strong>DblClick</strong></span><span class="sxs-lookup"><span data-stu-id="7e1d9-126"><strong>DblClick</strong></span></span></p></td>
<td><p><span data-ttu-id="7e1d9-127"><strong>KeyPress</strong></span><span class="sxs-lookup"><span data-stu-id="7e1d9-127"><strong>KeyPress</strong></span></span></p></td>
<td><p><span data-ttu-id="7e1d9-128"><strong>Unload</strong></span><span class="sxs-lookup"><span data-stu-id="7e1d9-128"><strong>Unload</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e1d9-129"><strong>удаление</strong>;</span><span class="sxs-lookup"><span data-stu-id="7e1d9-129"><strong>Delete</strong></span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="7e1d9-130">Вы можете использовать действие **Макрокоманда CancelEvent** с событием **MouseDown** только для отмены события, которое возникает при щелчке объекта правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-130">You can use the **CancelEvent** action with the **MouseDown** event only to cancel the event that occurs when you right-click an object.</span></span>

<span data-ttu-id="7e1d9-131">Если параметр свойства события **ондблкликк** элемента управления указывает макрос, содержащий действие **Макрокоманда CancelEvent** , действие отменяет событие **DblClick** .</span><span class="sxs-lookup"><span data-stu-id="7e1d9-131">If a control's **OnDblClick** event property setting specifies a macro containing the **CancelEvent** action, the action cancels the **DblClick** event.</span></span>

<span data-ttu-id="7e1d9-132">Для событий, которые можно отменять, поведение по умолчанию для события (то есть, как правило, обычно выполняется при возникновении события) возникает после запуска макроса для события.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-132">For events that can be canceled, the default behavior for the event (that is, what Access typically does when the event occurs) occurs after the macro for the event runs.</span></span> <span data-ttu-id="7e1d9-133">Это позволяет отменить поведение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-133">This enables you to cancel the default behavior.</span></span> <span data-ttu-id="7e1d9-134">Например, если дважды щелкнуть слово, в текстовом поле которого находится точка вставки, Access обычно выделяет это слово.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-134">For example, when you double-click a word that the insertion point is on in a text box, Access normally selects the word.</span></span> <span data-ttu-id="7e1d9-135">Вы можете отменить это поведение по умолчанию в макросе для события **DblClick** и выполнить другие действия, такие как открытие формы, содержащей сведения о данных в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-135">You can cancel this default behavior in the macro for the **DblClick** event and perform some other action, such as opening a form containing information about the data in the text box.</span></span> <span data-ttu-id="7e1d9-136">Для событий, которые не могут быть отменены, поведение по умолчанию возникает перед запуском макроса.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-136">For events that can't be canceled, the default behavior occurs before the macro runs.</span></span>

> [!NOTE]
> <span data-ttu-id="7e1d9-137">Если свойство события **OnUnload** формы указывает макрос, который выполняет действие **Макрокоманда CancelEvent** , вы не сможете закрыть форму.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-137">If a form's **OnUnload** event property specifies a macro that carries out a **CancelEvent** action, you won't be able to close the form.</span></span> <span data-ttu-id="7e1d9-138">Необходимо либо исправить условие, вызвавшее действие **Макрокоманда CancelEvent** , либо открыть макрос и удалить действие **Макрокоманда CancelEvent** .</span><span class="sxs-lookup"><span data-stu-id="7e1d9-138">You must either correct the condition that caused the **CancelEvent** action to be carried out or open the macro and delete the **CancelEvent** action.</span></span> <span data-ttu-id="7e1d9-139">Если форма является модальной, открыть макрос будет невозможно.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-139">If the form is a modal form, you won't be able to open the macro.</span></span>

<span data-ttu-id="7e1d9-140">Чтобы выполнить действие **Макрокоманда CancelEvent** в модуле Visual Basic для приложений (VBA), используйте метод **Макрокоманда CancelEvent** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="7e1d9-140">To carry out the **CancelEvent** action in a Visual Basic for Applications (VBA) module, use the **CancelEvent** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="7e1d9-141">Пример</span><span class="sxs-lookup"><span data-stu-id="7e1d9-141">Example</span></span>

<span data-ttu-id="7e1d9-142">Проверка данных с помощью макроса</span><span class="sxs-lookup"><span data-stu-id="7e1d9-142">Validate data by using a macro</span></span>

<span data-ttu-id="7e1d9-143">Следующий макрос проверки проверяет почтовые индексы, введенные в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-143">The following validation macro checks the postal codes entered in a Suppliers form.</span></span> <span data-ttu-id="7e1d9-144">В нем показано использование действий **Макрокоманда StopMacro**, **MessageBox**, **Макрокоманда CancelEvent**и **КЭлементуУправления** .</span><span class="sxs-lookup"><span data-stu-id="7e1d9-144">It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions.</span></span> <span data-ttu-id="7e1d9-145">Условное выражение проверяет страну, регион и почтовый индекс, введенные в записи в форме.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-145">A conditional expression checks the country/region and postal code entered in a record on the form.</span></span> <span data-ttu-id="7e1d9-146">Если почтовый индекс находится в неправильном формате для страны или региона, макрос выводит окно сообщения и отменяет сохранение записи.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-146">If the postal code is not in the right format for the country/region, the macro displays a message box and cancels saving the record.</span></span> <span data-ttu-id="7e1d9-147">Затем выполняется возврат к элементу управления "почтовый индекс", в котором можно исправить ошибку.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-147">It then returns you to the Postal Code control, where you can correct the error.</span></span> <span data-ttu-id="7e1d9-148">Этот макрос необходимо вложить в свойство **BeforeUpdate** формы "поставщики".</span><span class="sxs-lookup"><span data-stu-id="7e1d9-148">This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e1d9-149">Условие</span><span class="sxs-lookup"><span data-stu-id="7e1d9-149">Condition</span></span></p></th>
<th><p><span data-ttu-id="7e1d9-150">Макрокоманда</span><span class="sxs-lookup"><span data-stu-id="7e1d9-150">Action</span></span></p></th>
<th><p><span data-ttu-id="7e1d9-151">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="7e1d9-151">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="7e1d9-152">Примечание</span><span class="sxs-lookup"><span data-stu-id="7e1d9-152">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e1d9-153">IsNull ([страна])</span><span class="sxs-lookup"><span data-stu-id="7e1d9-153">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="7e1d9-154">StopMacro</span><span class="sxs-lookup"><span data-stu-id="7e1d9-154">StopMacro</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7e1d9-155">Если страна имеет <strong>значение NULL</strong>, почтовый индекс не может быть проверен.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-155">If CountryRegion is <strong>Null</strong>, postal code can't be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e1d9-156">Ватикан В (&quot;Франция&quot;,&quot;Италия&quot;,&quot;Испания&quot;) и len ([почтовый индекс]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="7e1d9-156">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([Postal Code]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="7e1d9-157">MessageBox</span><span class="sxs-lookup"><span data-stu-id="7e1d9-157">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="7e1d9-158">Сообщение: длина почтового индекса не должна превышать 5 символов.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-158">Message: The postal code must be 5 characters.</span></span> <span data-ttu-id="7e1d9-159">Гудок: тип <strong>Да</strong> : <strong>сведения</strong> : ошибка почтового индекса</span><span class="sxs-lookup"><span data-stu-id="7e1d9-159">Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="7e1d9-160">Если почтовый индекс не имеет 5 символов, отобразится сообщение.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-160">If the postal code isn't 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e1d9-161">...</span><span class="sxs-lookup"><span data-stu-id="7e1d9-161">...</span></span></p></td>
<td><p><span data-ttu-id="7e1d9-162">ОтменитьСобытие</span><span class="sxs-lookup"><span data-stu-id="7e1d9-162">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7e1d9-163">Отмена события.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-163">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="7e1d9-164">GoToControl</span><span class="sxs-lookup"><span data-stu-id="7e1d9-164">GoToControl</span></span></p></td>
<td><p><span data-ttu-id="7e1d9-165">Имя элемента управления: PostalCode</span><span class="sxs-lookup"><span data-stu-id="7e1d9-165">Control Name: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e1d9-166">Ватикан В (&quot;Австралия&quot;,&quot;Сингапур&quot;) и len ([почтовый индекс]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="7e1d9-166">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([Postal Code]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="7e1d9-167">MessageBox</span><span class="sxs-lookup"><span data-stu-id="7e1d9-167">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="7e1d9-168">Сообщение: почтовый индекс должен иметь 4 символа.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-168">Message: The postal code must be 4 characters.</span></span> <span data-ttu-id="7e1d9-169">Гудок: тип <strong>Да</strong> : <strong>сведения</strong> : ошибка почтового индекса</span><span class="sxs-lookup"><span data-stu-id="7e1d9-169">Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="7e1d9-170">Если почтовый индекс не имеет 4 символов, отобразится сообщение.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-170">If the postal code isn't 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e1d9-171">...</span><span class="sxs-lookup"><span data-stu-id="7e1d9-171">...</span></span></p></td>
<td><p><span data-ttu-id="7e1d9-172">ОтменитьСобытие</span><span class="sxs-lookup"><span data-stu-id="7e1d9-172">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7e1d9-173">Отмена события.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-173">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="7e1d9-174">GoToControl</span><span class="sxs-lookup"><span data-stu-id="7e1d9-174">GoToControl</span></span></p></td>
<td><p><span data-ttu-id="7e1d9-175">Имя элемента управления: PostalCode</span><span class="sxs-lookup"><span data-stu-id="7e1d9-175">Control Name: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e1d9-176">([Страна] = &quot;Канада&quot;) And ([почтовый индекс] не похоже&quot;на [a-z] [0-9] [a-z] [0-9] [a-z] [0-9&quot;])</span><span class="sxs-lookup"><span data-stu-id="7e1d9-176">([CountryRegion] = &quot;Canada&quot;) And ([Postal Code] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="7e1d9-177">MessageBox</span><span class="sxs-lookup"><span data-stu-id="7e1d9-177">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="7e1d9-178">Сообщение: недопустимый почтовый индекс.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-178">Message: The postal code is not valid.</span></span> <span data-ttu-id="7e1d9-179">Пример кода канадского канадского: H1J 1C3 beep: тип <strong>Да</strong> : <strong>сведения</strong> : ошибка почтового индекса</span><span class="sxs-lookup"><span data-stu-id="7e1d9-179">Example of Canadian code: H1J 1C3 Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="7e1d9-180">Если почтовый индекс не подходит для Канады, отобразите сообщение.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-180">If the postal code isn't correct for Canada, display a message.</span></span> <span data-ttu-id="7e1d9-181">(Пример канадского кода: H1J 1C3)</span><span class="sxs-lookup"><span data-stu-id="7e1d9-181">(Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e1d9-182">...</span><span class="sxs-lookup"><span data-stu-id="7e1d9-182">...</span></span></p></td>
<td><p><span data-ttu-id="7e1d9-183">ОтменитьСобытие</span><span class="sxs-lookup"><span data-stu-id="7e1d9-183">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7e1d9-184">Отмена события.</span><span class="sxs-lookup"><span data-stu-id="7e1d9-184">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

