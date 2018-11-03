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
ms.openlocfilehash: b0b8d7cb1a224b7f9c4d587d5c8941977dab2f66
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937129"
---
# <a name="cancelevent-macro-action"></a><span data-ttu-id="b914a-102">Макрокоманда CancelEvent</span><span class="sxs-lookup"><span data-stu-id="b914a-102">CancelEvent macro action</span></span>

<span data-ttu-id="b914a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b914a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b914a-104">Действие **ОтменитьСобытие** можно использовать для отмены события, вызвавшего доступа для запуска макроса, содержащего эту операцию.</span><span class="sxs-lookup"><span data-stu-id="b914a-104">You can use the **CancelEvent** action to cancel the event that caused Access to run the macro containing this action.</span></span> <span data-ttu-id="b914a-105">Имя макроса задано для свойства события **BeforeUpdate**, **формы**, **OnUnload**или **OnPrint**.</span><span class="sxs-lookup"><span data-stu-id="b914a-105">The macro name is the setting of an event property such as **BeforeUpdate**, **OnOpen**, **OnUnload**, or **OnPrint**.</span></span>

## <a name="setting"></a><span data-ttu-id="b914a-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="b914a-106">Setting</span></span>

<span data-ttu-id="b914a-107">Действие **ОтменитьСобытие** не требует аргументов.</span><span class="sxs-lookup"><span data-stu-id="b914a-107">The **CancelEvent** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="b914a-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="b914a-108">Remarks</span></span>

<span data-ttu-id="b914a-109">В форме обычно используется **ОтменитьСобытие в макросе проверки** со свойством событие **BeforeUpdate** .</span><span class="sxs-lookup"><span data-stu-id="b914a-109">In a form, you typically use the **CancelEvent** action in a validation macro with the **BeforeUpdate** event property.</span></span> <span data-ttu-id="b914a-110">При вводе данных в элемент управления или запись Access запускает макрос перед добавлением данные в базу данных.</span><span class="sxs-lookup"><span data-stu-id="b914a-110">When a user enters data in a control or record, Access runs the macro before adding the data to the database.</span></span> <span data-ttu-id="b914a-111">В случае сбоя в макросе условиям проверки данных **ОтменитьСобытие** действие отменяет процесс обновления до его запуска.</span><span class="sxs-lookup"><span data-stu-id="b914a-111">If the data fails the validation conditions in the macro, the **CancelEvent** action cancels the update process before it starts.</span></span>

<span data-ttu-id="b914a-112">Часто используется это действие с действием **MessageBox** для указания, что данные не удалось выполнить проверку условий и предоставляются полезные сведения о типе данных, которые должны быть введены.</span><span class="sxs-lookup"><span data-stu-id="b914a-112">Often, you use this action with the **MessageBox** action to indicate that the data has failed the validation conditions and to provide helpful information about the kind of data that should be entered.</span></span>

<span data-ttu-id="b914a-113">Следующие события можно отменить с **ОтменитьСобытие** .</span><span class="sxs-lookup"><span data-stu-id="b914a-113">The following events can be canceled by the **CancelEvent** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b914a-114"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="b914a-114"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="b914a-115"><strong>Dirty</strong></span><span class="sxs-lookup"><span data-stu-id="b914a-115"><strong>Dirty</strong></span></span></p></td>
<td><p><span data-ttu-id="b914a-116"><strong>MouseDown</strong></span><span class="sxs-lookup"><span data-stu-id="b914a-116"><strong>MouseDown</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b914a-117"><strong>До подтверждения Del</strong></span><span class="sxs-lookup"><span data-stu-id="b914a-117"><strong>BeforeDelConfirm</strong></span></span></p></td>
<td><p><span data-ttu-id="b914a-118"><strong>Выход</strong></span><span class="sxs-lookup"><span data-stu-id="b914a-118"><strong>Exit</strong></span></span></p></td>
<td><p><span data-ttu-id="b914a-119"><strong>NoData</strong></span><span class="sxs-lookup"><span data-stu-id="b914a-119"><strong>NoData</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b914a-120"><strong>До вставки</strong></span><span class="sxs-lookup"><span data-stu-id="b914a-120"><strong>BeforeInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="b914a-121"><strong>Filter</strong></span><span class="sxs-lookup"><span data-stu-id="b914a-121"><strong>Filter</strong></span></span></p></td>
<td><p><span data-ttu-id="b914a-122"><strong>Открытие</strong></span><span class="sxs-lookup"><span data-stu-id="b914a-122"><strong>Open</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b914a-123"><strong>До обновления</strong></span><span class="sxs-lookup"><span data-stu-id="b914a-123"><strong>BeforeUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="b914a-124"><strong>Формат</strong></span><span class="sxs-lookup"><span data-stu-id="b914a-124"><strong>Format</strong></span></span></p></td>
<td><p><span data-ttu-id="b914a-125"><strong>Печать</strong></span><span class="sxs-lookup"><span data-stu-id="b914a-125"><strong>Print</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b914a-126"><strong>DblClick</strong></span><span class="sxs-lookup"><span data-stu-id="b914a-126"><strong>DblClick</strong></span></span></p></td>
<td><p><span data-ttu-id="b914a-127"><strong>Нажатие клавиши</strong></span><span class="sxs-lookup"><span data-stu-id="b914a-127"><strong>KeyPress</strong></span></span></p></td>
<td><p><span data-ttu-id="b914a-128"><strong>Unload</strong></span><span class="sxs-lookup"><span data-stu-id="b914a-128"><strong>Unload</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b914a-129"><strong>Delete</strong></span><span class="sxs-lookup"><span data-stu-id="b914a-129"><strong>Delete</strong></span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="b914a-130">Можно использовать действие **ОтменитьСобытие** с события **MouseDown** только, чтобы отменить событие, происходящее при щелчке правой кнопкой мыши объект.</span><span class="sxs-lookup"><span data-stu-id="b914a-130">You can use the **CancelEvent** action with the **MouseDown** event only to cancel the event that occurs when you right-click an object.</span></span>

<span data-ttu-id="b914a-131">Если значение свойства события элемента управления **OnDblClick** указывает макрос, содержащий **ОтменитьСобытие** , то действие отменяет событие **DblClick** .</span><span class="sxs-lookup"><span data-stu-id="b914a-131">If a control's **OnDblClick** event property setting specifies a macro containing the **CancelEvent** action, the action cancels the **DblClick** event.</span></span>

<span data-ttu-id="b914a-132">Для событий, которые можно отменить поведение по умолчанию для события (то есть, которое Access обычно выполняет при возникновении события) после выполнения макроса для события.</span><span class="sxs-lookup"><span data-stu-id="b914a-132">For events that can be canceled, the default behavior for the event (that is, what Access typically does when the event occurs) occurs after the macro for the event runs.</span></span> <span data-ttu-id="b914a-133">Это позволяет отменить поведение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b914a-133">This enables you to cancel the default behavior.</span></span> <span data-ttu-id="b914a-134">Например дважды щелкните слово, которое точка вставки находится на в текстовом поле, обычно выделяет слово.</span><span class="sxs-lookup"><span data-stu-id="b914a-134">For example, when you double-click a word that the insertion point is on in a text box, Access normally selects the word.</span></span> <span data-ttu-id="b914a-135">Можно отменить это поведение по умолчанию в макросе для события **DblClick** и выполнение некоторых действий, таких как Открытие формы, содержащей сведения о данных в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="b914a-135">You can cancel this default behavior in the macro for the **DblClick** event and perform some other action, such as opening a form containing information about the data in the text box.</span></span> <span data-ttu-id="b914a-136">Для событий, не может быть отменен поведение по умолчанию до выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="b914a-136">For events that can't be canceled, the default behavior occurs before the macro runs.</span></span>

> [!NOTE]
> <span data-ttu-id="b914a-137">Если свойство события **OnUnload** формы указывает макроса, выполняющего **ОтменитьСобытие** действие, не будут иметь возможность закрыть форму.</span><span class="sxs-lookup"><span data-stu-id="b914a-137">If a form's **OnUnload** event property specifies a macro that carries out a **CancelEvent** action, you won't be able to close the form.</span></span> <span data-ttu-id="b914a-138">Необходимо либо исправить условие, в которой обнаружен **ОтменитьСобытие осуществляться или откройте макрос и удаление **ОтменитьСобытие** действия** .</span><span class="sxs-lookup"><span data-stu-id="b914a-138">You must either correct the condition that caused the **CancelEvent** action to be carried out or open the macro and delete the **CancelEvent** action.</span></span> <span data-ttu-id="b914a-139">Если форма модальную форму, не будут иметь возможность открыть макрос.</span><span class="sxs-lookup"><span data-stu-id="b914a-139">If the form is a modal form, you won't be able to open the macro.</span></span>

<span data-ttu-id="b914a-140">Для выполнения **ОтменитьСобытие в Visual Basic для приложений (VBA) модуль** , используйте метод **ОтменитьСобытие** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="b914a-140">To carry out the **CancelEvent** action in a Visual Basic for Applications (VBA) module, use the **CancelEvent** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="b914a-141">Пример</span><span class="sxs-lookup"><span data-stu-id="b914a-141">Example</span></span>

<span data-ttu-id="b914a-142">Проверка данных с помощью макроса (en)</span><span class="sxs-lookup"><span data-stu-id="b914a-142">Validate data by using a macro</span></span>

<span data-ttu-id="b914a-143">Следующий макрос для проверки проверяет почтовые индексы, введенные в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="b914a-143">The following validation macro checks the postal codes entered in a Suppliers form.</span></span> <span data-ttu-id="b914a-144">Демонстрируется использование **ОстановитьМакрос**, **MessageBox**, **ОтменитьСобытие**и **КЭлементуУправления** действия.</span><span class="sxs-lookup"><span data-stu-id="b914a-144">It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions.</span></span> <span data-ttu-id="b914a-145">Условным выражением проверяет страны или региона и почтового индекса в записи на форме.</span><span class="sxs-lookup"><span data-stu-id="b914a-145">A conditional expression checks the country/region and postal code entered in a record on the form.</span></span> <span data-ttu-id="b914a-146">Если почтовый индекс не в нужном формате для страны или региона, макрос отображается окно сообщения и показано, как отменить сохранение записи.</span><span class="sxs-lookup"><span data-stu-id="b914a-146">If the postal code is not in the right format for the country/region, the macro displays a message box and cancels saving the record.</span></span> <span data-ttu-id="b914a-147">Оно будет снова к элементу управления почтовый индекс для исправления ошибки.</span><span class="sxs-lookup"><span data-stu-id="b914a-147">It then returns you to the Postal Code control, where you can correct the error.</span></span> <span data-ttu-id="b914a-148">Этот макрос должен быть связан свойством **BeforeUpdate** формы Поставщики.</span><span class="sxs-lookup"><span data-stu-id="b914a-148">This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b914a-149">Condition</span><span class="sxs-lookup"><span data-stu-id="b914a-149">Condition</span></span></p></th>
<th><p><span data-ttu-id="b914a-150">Действие</span><span class="sxs-lookup"><span data-stu-id="b914a-150">Action</span></span></p></th>
<th><p><span data-ttu-id="b914a-151">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="b914a-151">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="b914a-152">Comment</span><span class="sxs-lookup"><span data-stu-id="b914a-152">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b914a-153">IsNull([CountryRegion])</span><span class="sxs-lookup"><span data-stu-id="b914a-153">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="b914a-154">StopMacro</span><span class="sxs-lookup"><span data-stu-id="b914a-154">StopMacro</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b914a-155">Если Страна имеет <strong>значение Null</strong>, почтовый индекс не может быть проверен.</span><span class="sxs-lookup"><span data-stu-id="b914a-155">If CountryRegion is <strong>Null</strong>, postal code can't be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b914a-156">[Страна] В (&quot;Франции&quot;,&quot;Италия&quot;,&quot;Испания&quot;) и Len ([Почтовый индекс]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="b914a-156">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([Postal Code]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="b914a-157">MessageBox</span><span class="sxs-lookup"><span data-stu-id="b914a-157">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="b914a-158">Сообщение об ошибке: Почтовый индекс должен быть 5 символов.</span><span class="sxs-lookup"><span data-stu-id="b914a-158">Message: The postal code must be 5 characters.</span></span> <span data-ttu-id="b914a-159">Звуковые: <strong>Да</strong> тип: <strong>сведения о</strong> заголовок: ошибка почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="b914a-159">Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="b914a-160">Если почтовый индекс не 5 знаков, отобразите сообщение.</span><span class="sxs-lookup"><span data-stu-id="b914a-160">If the postal code isn't 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b914a-161">...</span><span class="sxs-lookup"><span data-stu-id="b914a-161"></span></span></p></td>
<td><p><span data-ttu-id="b914a-162">ОтменитьСобытие</span><span class="sxs-lookup"><span data-stu-id="b914a-162">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b914a-163">Отмените событие.</span><span class="sxs-lookup"><span data-stu-id="b914a-163">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="b914a-164">GoToControl</span><span class="sxs-lookup"><span data-stu-id="b914a-164">GoToControl</span></span></p></td>
<td><p><span data-ttu-id="b914a-165">Имя элемента управления: PostalCode</span><span class="sxs-lookup"><span data-stu-id="b914a-165">Control Name: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b914a-166">[Страна] В (&quot;Австралия&quot;,&quot;Сингапур&quot;) и Len ([Почтовый индекс]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="b914a-166">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([Postal Code]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="b914a-167">MessageBox</span><span class="sxs-lookup"><span data-stu-id="b914a-167">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="b914a-168">Сообщение об ошибке: Почтовый индекс должен быть 4 символов.</span><span class="sxs-lookup"><span data-stu-id="b914a-168">Message: The postal code must be 4 characters.</span></span> <span data-ttu-id="b914a-169">Звуковые: <strong>Да</strong> тип: <strong>сведения о</strong> заголовок: ошибка почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="b914a-169">Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="b914a-170">Если почтовый индекс не 4 символа, отобразите сообщение.</span><span class="sxs-lookup"><span data-stu-id="b914a-170">If the postal code isn't 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b914a-171">...</span><span class="sxs-lookup"><span data-stu-id="b914a-171"></span></span></p></td>
<td><p><span data-ttu-id="b914a-172">ОтменитьСобытие</span><span class="sxs-lookup"><span data-stu-id="b914a-172">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b914a-173">Отмените событие.</span><span class="sxs-lookup"><span data-stu-id="b914a-173">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="b914a-174">GoToControl</span><span class="sxs-lookup"><span data-stu-id="b914a-174">GoToControl</span></span></p></td>
<td><p><span data-ttu-id="b914a-175">Имя элемента управления: PostalCode</span><span class="sxs-lookup"><span data-stu-id="b914a-175">Control Name: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b914a-176">([Страна] = &quot;Канада&quot;) И ([Почтовый индекс] не нравится&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</span><span class="sxs-lookup"><span data-stu-id="b914a-176">([CountryRegion] = &quot;Canada&quot;) And ([Postal Code] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="b914a-177">MessageBox</span><span class="sxs-lookup"><span data-stu-id="b914a-177">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="b914a-178">Сообщение об ошибке: Почтовый индекс не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="b914a-178">Message: The postal code is not valid.</span></span> <span data-ttu-id="b914a-179">Пример кода, английский (Канада): H1J 1 c 3 звуковые сигналы: <strong>Да</strong> тип: <strong>данные</strong> заголовка: почтовый код ошибки</span><span class="sxs-lookup"><span data-stu-id="b914a-179">Example of Canadian code: H1J 1C3 Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="b914a-180">Если почтовый индекс не соответствует формату для Канады, отобразите сообщение.</span><span class="sxs-lookup"><span data-stu-id="b914a-180">If the postal code isn't correct for Canada, display a message.</span></span> <span data-ttu-id="b914a-181">(Пример кода, английский (Канада): H1J 1 c 3)</span><span class="sxs-lookup"><span data-stu-id="b914a-181">(Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b914a-182">...</span><span class="sxs-lookup"><span data-stu-id="b914a-182"></span></span></p></td>
<td><p><span data-ttu-id="b914a-183">ОтменитьСобытие</span><span class="sxs-lookup"><span data-stu-id="b914a-183">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b914a-184">Отмените событие.</span><span class="sxs-lookup"><span data-stu-id="b914a-184">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

