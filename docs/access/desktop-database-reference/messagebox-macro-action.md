---
title: Макрокоманда MessageBox
TOCTitle: MessageBox macro action
ms:assetid: 326a0e68-38fb-4f81-b319-5a70caa5aec4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192304(v=office.15)
ms:contentKeyID: 48544077
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1175e3903e54fd3420be43dfd9e3652d9990468b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289158"
---
# <a name="messagebox-macro-action"></a><span data-ttu-id="5698d-102">Макрокоманда MessageBox</span><span class="sxs-lookup"><span data-stu-id="5698d-102">MessageBox macro action</span></span>

<span data-ttu-id="5698d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5698d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5698d-104">С помощью действия **MessageBox** можно отобразить окно сообщения, содержащее предупреждение или информационное сообщение.</span><span class="sxs-lookup"><span data-stu-id="5698d-104">You can use the **MessageBox** action to display a message box containing a warning or an informational message.</span></span> <span data-ttu-id="5698d-105">Например, вы можете использовать действие **MessageBox** с макросами проверки.</span><span class="sxs-lookup"><span data-stu-id="5698d-105">For example, you can use the **MessageBox** action with validation macros.</span></span> <span data-ttu-id="5698d-106">Если в макросе не удается найти условие проверки для какого-либо из них, в окне сообщения может отображаться сообщение об ошибке и указаны инструкции по типу данных, которые необходимо в введены.</span><span class="sxs-lookup"><span data-stu-id="5698d-106">When a control or record fails a validation condition in the macro, a message box can display an error message and provide instructions about the kind of data that should be entered.</span></span>

## <a name="setting"></a><span data-ttu-id="5698d-107">Setting</span><span class="sxs-lookup"><span data-stu-id="5698d-107">Setting</span></span>

<span data-ttu-id="5698d-108">Действие **MessageBox** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="5698d-108">The **MessageBox** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5698d-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="5698d-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="5698d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="5698d-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5698d-111"><strong>Message</strong></span><span class="sxs-lookup"><span data-stu-id="5698d-111"><strong>Message</strong></span></span></p></td>
<td><p><span data-ttu-id="5698d-112">Текст в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="5698d-112">The text in the message box.</span></span> <span data-ttu-id="5698d-113">Введите текст сообщения в поле <strong>"Сообщение"</strong> в разделе <strong>"Аргументы действий"</strong> области построитель макроса.</span><span class="sxs-lookup"><span data-stu-id="5698d-113">Enter the message text in the <strong>Message</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="5698d-114">Можно ввести до 255 символов или ввести выражение (предшествует знаку "равно").</span><span class="sxs-lookup"><span data-stu-id="5698d-114">You can type up to 255 characters or enter an expression (preceded by an equal sign).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5698d-115"><strong>Beep</strong></span><span class="sxs-lookup"><span data-stu-id="5698d-115"><strong>Beep</strong></span></span></p></td>
<td><p><span data-ttu-id="5698d-116">Указывает, звучит ли звуковой сигнал динамика компьютера при отображе сообщения.</span><span class="sxs-lookup"><span data-stu-id="5698d-116">Specifies whether your computer's speaker sounds a beep tone when the message displays.</span></span> <span data-ttu-id="5698d-117">Нажмите <strong>кнопку "Да"</strong> (звук звукового сигнала) или <strong>"Нет"</strong> (не звучайте звуковой сигнал).</span><span class="sxs-lookup"><span data-stu-id="5698d-117">Click <strong>Yes</strong> (sound the beep tone) or <strong>No</strong> (don't sound the beep tone).</span></span> <span data-ttu-id="5698d-118">Значение по умолчанию <strong>— Да.</strong></span><span class="sxs-lookup"><span data-stu-id="5698d-118">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5698d-119"><strong>Тип</strong></span><span class="sxs-lookup"><span data-stu-id="5698d-119"><strong>Type</strong></span></span></p></td>
<td><p><span data-ttu-id="5698d-120">Тип окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="5698d-120">The type of message box.</span></span> <span data-ttu-id="5698d-121">Каждый тип имеет разные значки.</span><span class="sxs-lookup"><span data-stu-id="5698d-121">Each type has a different icon.</span></span> <span data-ttu-id="5698d-122">Щелкните <strong>"Нет",</strong> <strong>"Критическое",</strong> <strong>"Предупреждение?",</strong> <strong>"Предупреждение!"</strong>или <strong>"Сведения".</strong></span><span class="sxs-lookup"><span data-stu-id="5698d-122">Click <strong>None</strong>, <strong>Critical</strong>, <strong>Warning?</strong>, <strong>Warning!</strong>, or <strong>Information</strong>.</span></span> <span data-ttu-id="5698d-123">Значение по умолчанию <strong>— None</strong>.</span><span class="sxs-lookup"><span data-stu-id="5698d-123">The default is <strong>None</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5698d-124"><strong>Title</strong></span><span class="sxs-lookup"><span data-stu-id="5698d-124"><strong>Title</strong></span></span></p></td>
<td><p><span data-ttu-id="5698d-125">Текст, отображаемой в заголовке окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="5698d-125">The text displayed in the message box title bar.</span></span> <span data-ttu-id="5698d-126">Например, в заголовке заголовка может &quot; отображаться проверка кодов &quot; клиентов.</span><span class="sxs-lookup"><span data-stu-id="5698d-126">For example, you can have the title bar display &quot;Customer ID Validation&quot;.</span></span> <span data-ttu-id="5698d-127">Если оставить этот аргумент пустым, &quot; будет отображаться Microsoft &quot; Access.</span><span class="sxs-lookup"><span data-stu-id="5698d-127">If you leave this argument blank, &quot;Microsoft Access&quot; is displayed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5698d-128">Заметки</span><span class="sxs-lookup"><span data-stu-id="5698d-128">Remarks</span></span>

<span data-ttu-id="5698d-129">С помощью действия **MessageBox** можно создать отформатированные сообщения об ошибке, аналогичные встроенным сообщениям об ошибках, отображаемой Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="5698d-129">You can use the **MessageBox** action to create a formatted error message similar to built-in error messages displayed by Microsoft Access.</span></span> <span data-ttu-id="5698d-130">Действие **MessageBox** позволяет предоставить сообщение в трех разделах для аргумента Message.</span><span class="sxs-lookup"><span data-stu-id="5698d-130">The **MessageBox** action permits you to supply a message in three sections for the Message argument.</span></span> <span data-ttu-id="5698d-131">Разделы разделов разделяют символами "@".</span><span class="sxs-lookup"><span data-stu-id="5698d-131">You separate the sections with the "@" character.</span></span>

<span data-ttu-id="5698d-132">В следующем примере отображается отформатированные сообщения с раздельным сообщением.</span><span class="sxs-lookup"><span data-stu-id="5698d-132">The following example displays a formatted message box with a sectioned message.</span></span> <span data-ttu-id="5698d-133">Первый раздел текста в сообщении отображается полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="5698d-133">The first section of text in the message is displayed as a bold heading.</span></span> <span data-ttu-id="5698d-134">Второй раздел отображается в виде обычного текста под этим заголовком.</span><span class="sxs-lookup"><span data-stu-id="5698d-134">The second section is displayed as plain text beneath that heading.</span></span> <span data-ttu-id="5698d-135">Третий раздел отображается в виде обычного текста под вторым разделом с пустой строкой между ними.</span><span class="sxs-lookup"><span data-stu-id="5698d-135">The third section is displayed as plain text beneath the second section, with a blank line between them.</span></span>

<span data-ttu-id="5698d-136">Введите в **аргументе Message** следующую строку:</span><span class="sxs-lookup"><span data-stu-id="5698d-136">Type the following string in the **Message** argument:</span></span>

<span data-ttu-id="5698d-137">**\!Неправильная @This кнопка не work.@Try другой.**</span><span class="sxs-lookup"><span data-stu-id="5698d-137">**Wrong button\!@This button doesn't work.@Try another.**</span></span>

<span data-ttu-id="5698d-138">Действие **MessageBox** нельзя запустить в модуле Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="5698d-138">You can't run the **MessageBox** action in a Visual Basic for Applications (VBA) module.</span></span> <span data-ttu-id="5698d-139">Вместо этого **используйте функцию MsgBox.**</span><span class="sxs-lookup"><span data-stu-id="5698d-139">Use the **MsgBox** function instead.</span></span>

## <a name="examples"></a><span data-ttu-id="5698d-140">Примеры</span><span class="sxs-lookup"><span data-stu-id="5698d-140">Examples</span></span>

<span data-ttu-id="5698d-141">**Синхронизация форм с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="5698d-141">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="5698d-142">Следующий макрос открывает форму "Список продуктов" в правом нижнем углу формы "Поставщики", отображая продукты текущего поставщика.</span><span class="sxs-lookup"><span data-stu-id="5698d-142">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="5698d-143">Здесь показано использование действий **Echo,** **MessageBox,** **GoToControl,** **StopMacro,** **OpenForm** и **MoveAndSizeWindow.**</span><span class="sxs-lookup"><span data-stu-id="5698d-143">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="5698d-144">Здесь также показано использование условного выражения с действиями **MessageBox,** **GoToControl** и **StopMacro.**</span><span class="sxs-lookup"><span data-stu-id="5698d-144">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="5698d-145">Этот макрос следует прикрепить к кнопке "Обзор продуктов" в форме "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="5698d-145">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5698d-146">Condition</span><span class="sxs-lookup"><span data-stu-id="5698d-146">Condition</span></span></p></th>
<th><p><span data-ttu-id="5698d-147">Макрокоманда</span><span class="sxs-lookup"><span data-stu-id="5698d-147">Action</span></span></p></th>
<th><p><span data-ttu-id="5698d-148">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="5698d-148">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="5698d-149">Примечание</span><span class="sxs-lookup"><span data-stu-id="5698d-149">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="5698d-150"><strong>ВыводНаЭкран</strong></span><span class="sxs-lookup"><span data-stu-id="5698d-150"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="5698d-151"><strong>Включить вывод</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="5698d-151"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="5698d-152">Приостанавливает обновление экрана, пока выполняется макрос.</span><span class="sxs-lookup"><span data-stu-id="5698d-152">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5698d-153">IsNull([SupplierID])</span><span class="sxs-lookup"><span data-stu-id="5698d-153">IsNull([SupplierID])</span></span></p></td>
<td><p><span data-ttu-id="5698d-154"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="5698d-154"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="5698d-155"><strong>Сообщение:</strong>перейдите к записи поставщика, продукты которой вы хотите просмотреть, а затем снова нажмите кнопку "Просмотреть продукты".</span><span class="sxs-lookup"><span data-stu-id="5698d-155"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="5698d-156"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span><span class="sxs-lookup"><span data-stu-id="5698d-156"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="5698d-157">Если в форме "Поставщики" нет текущего поставщика, отобразить сообщение.</span><span class="sxs-lookup"><span data-stu-id="5698d-157">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5698d-158">...</span><span class="sxs-lookup"><span data-stu-id="5698d-158">...</span></span></p></td>
<td><p><span data-ttu-id="5698d-159"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="5698d-159"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="5698d-160"><strong>Имя управления</strong>: CompanyName</span><span class="sxs-lookup"><span data-stu-id="5698d-160"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="5698d-161">Переместите фокус на управление CompanyName.</span><span class="sxs-lookup"><span data-stu-id="5698d-161">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5698d-162">...</span><span class="sxs-lookup"><span data-stu-id="5698d-162">...</span></span></p></td>
<td><p><span data-ttu-id="5698d-163"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="5698d-163"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5698d-164">Остановите макрос.</span><span class="sxs-lookup"><span data-stu-id="5698d-164">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="5698d-165"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="5698d-165"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="5698d-166"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [SupplierID] = [Forms]! [Поставщики]! [SupplierID] <strong>Режим данных:</strong> <strong>режим только чтенияWindow</strong>: <strong>обычный</strong></span><span class="sxs-lookup"><span data-stu-id="5698d-166"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [SupplierID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="5698d-167">Откройте форму "Список продуктов" и откажите продукты текущего поставщика.</span><span class="sxs-lookup"><span data-stu-id="5698d-167">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="5698d-168"><strong>MoveAndSizeWindow</strong></span><span class="sxs-lookup"><span data-stu-id="5698d-168"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="5698d-169"><strong>Right</strong>: 0.7799 &quot; <strong>Down</strong>: 1.8&quot;</span><span class="sxs-lookup"><span data-stu-id="5698d-169"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="5698d-170">Расположить форму "Список продуктов" в правом нижнем правом месте формы "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="5698d-170">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5698d-171">**Проверка данных с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="5698d-171">**Validate data by using a macro**</span></span>

<span data-ttu-id="5698d-172">Следующий макрос проверки проверяет почтовые коды, вступив в форму "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="5698d-172">The following validation macro checks the postal codes entered in a Suppliers form.</span></span> <span data-ttu-id="5698d-173">Здесь показано использование действий **StopMacro,** **MessageBox,** **CancelEvent** и **GoToControl.**</span><span class="sxs-lookup"><span data-stu-id="5698d-173">It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions.</span></span> <span data-ttu-id="5698d-174">Условное выражение проверяет страну или регион и почтовый код, внося в запись в форме.</span><span class="sxs-lookup"><span data-stu-id="5698d-174">A conditional expression checks the country/region and postal code entered in a record on the form.</span></span> <span data-ttu-id="5698d-175">Если почтовый код не имеет правильного формата для страны или региона, макрос отображает окно сообщения и отменяет сохранение записи.</span><span class="sxs-lookup"><span data-stu-id="5698d-175">If the postal code isn't in the right format for the country/region, the macro displays a message box and cancels saving the record.</span></span> <span data-ttu-id="5698d-176">Затем он возвращает вас в пункт управления PostalCode, где можно исправить ошибку.</span><span class="sxs-lookup"><span data-stu-id="5698d-176">It then returns you to the PostalCode control, where you can correct the error.</span></span> <span data-ttu-id="5698d-177">Этот макрос следует присоединить к свойству **BeforeUpdate** формы "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="5698d-177">This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5698d-178">Condition</span><span class="sxs-lookup"><span data-stu-id="5698d-178">Condition</span></span></p></th>
<th><p><span data-ttu-id="5698d-179">Макрокоманда</span><span class="sxs-lookup"><span data-stu-id="5698d-179">Action</span></span></p></th>
<th><p><span data-ttu-id="5698d-180">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="5698d-180">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="5698d-181">Примечание</span><span class="sxs-lookup"><span data-stu-id="5698d-181">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5698d-182">IsNull([CountryRegion])</span><span class="sxs-lookup"><span data-stu-id="5698d-182">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="5698d-183"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="5698d-183"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5698d-184">Если countryRegion <strong>имеет null,</strong>почтовый код не может быть проверен.</span><span class="sxs-lookup"><span data-stu-id="5698d-184">If CountryRegion is <strong>Null</strong>, the postal code can't be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5698d-185">[CountryRegion] In &quot; &quot; (Франция, &quot; &quot; Италия, &quot; &quot; Испания) и Len([PostalCode]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="5698d-185">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([PostalCode]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="5698d-186"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="5698d-186"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="5698d-187"><strong>Сообщение:</strong>почтовый индекс должен иметь 5 символов.</span><span class="sxs-lookup"><span data-stu-id="5698d-187"><strong>Message</strong>: The postal code must be 5 characters.</span></span> <span data-ttu-id="5698d-188"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span><span class="sxs-lookup"><span data-stu-id="5698d-188"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="5698d-189">Если почтовый индекс не имеет 5 символов, отобразить сообщение.</span><span class="sxs-lookup"><span data-stu-id="5698d-189">If the postal code isn't 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5698d-190">...</span><span class="sxs-lookup"><span data-stu-id="5698d-190">...</span></span></p></td>
<td><p><span data-ttu-id="5698d-191"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="5698d-191"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5698d-192">Отмените событие.</span><span class="sxs-lookup"><span data-stu-id="5698d-192">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="5698d-193"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="5698d-193"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="5698d-194"><strong>Имя управления</strong>: PostalCode</span><span class="sxs-lookup"><span data-stu-id="5698d-194"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5698d-195">[CountryRegion] In &quot; &quot; (Australia, &quot; &quot; Singapore) and Len([PostalCode]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="5698d-195">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([PostalCode]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="5698d-196"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="5698d-196"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="5698d-197"><strong>Сообщение:</strong>почтовый индекс должен иметь 4 символа.</span><span class="sxs-lookup"><span data-stu-id="5698d-197"><strong>Message</strong>: The postal code must be 4 characters.</span></span> <span data-ttu-id="5698d-198"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span><span class="sxs-lookup"><span data-stu-id="5698d-198"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="5698d-199">Если почтовый индекс не имеет 4 символов, отобразить сообщение.</span><span class="sxs-lookup"><span data-stu-id="5698d-199">If the postal code isn't 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5698d-200">...</span><span class="sxs-lookup"><span data-stu-id="5698d-200">...</span></span></p></td>
<td><p><span data-ttu-id="5698d-201"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="5698d-201"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5698d-202">Отмените событие.</span><span class="sxs-lookup"><span data-stu-id="5698d-202">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="5698d-203"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="5698d-203"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="5698d-204"><strong>Имя управления</strong>: PostalCode</span><span class="sxs-lookup"><span data-stu-id="5698d-204"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5698d-205">([CountryRegion] = &quot; Канада) и &quot; ([PostalCode] не нравится &quot; [A-Z][0-9][A-Z] [0-9][A-Z][0-9] &quot; )</span><span class="sxs-lookup"><span data-stu-id="5698d-205">([CountryRegion] = &quot;Canada&quot;) And ([PostalCode] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="5698d-206"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="5698d-206"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="5698d-207"><strong>Сообщение:</strong>почтовый индекс не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="5698d-207"><strong>Message</strong>: The postal code is not valid.</span></span> <span data-ttu-id="5698d-208">Пример кода для Канады: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span><span class="sxs-lookup"><span data-stu-id="5698d-208">Example of Canadian code: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="5698d-209">Если почтовый индекс неправиа для Канады, отобразить сообщение.</span><span class="sxs-lookup"><span data-stu-id="5698d-209">If the postal code isn't correct for Canada, display a message.</span></span> <span data-ttu-id="5698d-210">(Пример кода для Канады: H1J 1C3)</span><span class="sxs-lookup"><span data-stu-id="5698d-210">(Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5698d-211">...</span><span class="sxs-lookup"><span data-stu-id="5698d-211">...</span></span></p></td>
<td><p><span data-ttu-id="5698d-212"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="5698d-212"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="5698d-213">Отмените событие.</span><span class="sxs-lookup"><span data-stu-id="5698d-213">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

