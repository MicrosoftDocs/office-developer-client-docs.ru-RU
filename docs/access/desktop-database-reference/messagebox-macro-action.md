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
# <a name="messagebox-macro-action"></a><span data-ttu-id="05d2f-102">Макрокоманда MessageBox</span><span class="sxs-lookup"><span data-stu-id="05d2f-102">MessageBox macro action</span></span>

<span data-ttu-id="05d2f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="05d2f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="05d2f-104">Вы можете использовать **действие MessageBox** для отображения окна сообщений, содержащего предупреждение или информационное сообщение.</span><span class="sxs-lookup"><span data-stu-id="05d2f-104">You can use the **MessageBox** action to display a message box containing a warning or an informational message.</span></span> <span data-ttu-id="05d2f-105">Например, можно использовать действие **MessageBox** с макросами проверки.</span><span class="sxs-lookup"><span data-stu-id="05d2f-105">For example, you can use the **MessageBox** action with validation macros.</span></span> <span data-ttu-id="05d2f-106">Если в макросе у управления или записи не получается условие проверки, окно сообщений может отображать сообщение об ошибке и давать инструкции о том, какие данные следует в них вписать.</span><span class="sxs-lookup"><span data-stu-id="05d2f-106">When a control or record fails a validation condition in the macro, a message box can display an error message and provide instructions about the kind of data that should be entered.</span></span>

## <a name="setting"></a><span data-ttu-id="05d2f-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="05d2f-107">Setting</span></span>

<span data-ttu-id="05d2f-108">В **действии MessageBox** есть следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="05d2f-108">The **MessageBox** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05d2f-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="05d2f-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="05d2f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="05d2f-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05d2f-111"><strong>Message</strong></span><span class="sxs-lookup"><span data-stu-id="05d2f-111"><strong>Message</strong></span></span></p></td>
<td><p><span data-ttu-id="05d2f-112">Текст в поле сообщений.</span><span class="sxs-lookup"><span data-stu-id="05d2f-112">The text in the message box.</span></span> <span data-ttu-id="05d2f-113">Введите текст сообщения в поле <strong>Сообщение</strong> в разделе <strong>Аргументы</strong> действий в области Macro Builder.</span><span class="sxs-lookup"><span data-stu-id="05d2f-113">Enter the message text in the <strong>Message</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="05d2f-114">Можно ввести до 255 символов или ввести выражение (предшествующего равному знаку).</span><span class="sxs-lookup"><span data-stu-id="05d2f-114">You can type up to 255 characters or enter an expression (preceded by an equal sign).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05d2f-115"><strong>Beep</strong></span><span class="sxs-lookup"><span data-stu-id="05d2f-115"><strong>Beep</strong></span></span></p></td>
<td><p><span data-ttu-id="05d2f-116">Указывает, звучит ли звуковой сигнал в динамике компьютера при показе сообщения.</span><span class="sxs-lookup"><span data-stu-id="05d2f-116">Specifies whether your computer's speaker sounds a beep tone when the message displays.</span></span> <span data-ttu-id="05d2f-117">Щелкните <strong>Да</strong> (звук звукового сигнала) или <strong>Нет</strong> (не звучайте звуковой сигнал).</span><span class="sxs-lookup"><span data-stu-id="05d2f-117">Click <strong>Yes</strong> (sound the beep tone) or <strong>No</strong> (don't sound the beep tone).</span></span> <span data-ttu-id="05d2f-118">По умолчанию — <strong>Да.</strong></span><span class="sxs-lookup"><span data-stu-id="05d2f-118">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05d2f-119"><strong>Тип</strong></span><span class="sxs-lookup"><span data-stu-id="05d2f-119"><strong>Type</strong></span></span></p></td>
<td><p><span data-ttu-id="05d2f-120">Тип окна сообщений.</span><span class="sxs-lookup"><span data-stu-id="05d2f-120">The type of message box.</span></span> <span data-ttu-id="05d2f-121">Каждый тип имеет другой значок.</span><span class="sxs-lookup"><span data-stu-id="05d2f-121">Each type has a different icon.</span></span> <span data-ttu-id="05d2f-122">Щелкните <strong>Нет,</strong> <strong>Критический</strong>, <strong>Предупреждение?</strong>, <strong>Предупреждение!</strong>, или <strong>сведения</strong>.</span><span class="sxs-lookup"><span data-stu-id="05d2f-122">Click <strong>None</strong>, <strong>Critical</strong>, <strong>Warning?</strong>, <strong>Warning!</strong>, or <strong>Information</strong>.</span></span> <span data-ttu-id="05d2f-123">По умолчанию <strong>нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="05d2f-123">The default is <strong>None</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05d2f-124"><strong>Title</strong></span><span class="sxs-lookup"><span data-stu-id="05d2f-124"><strong>Title</strong></span></span></p></td>
<td><p><span data-ttu-id="05d2f-125">Текст, отображаемый в панели заголовка окна сообщений.</span><span class="sxs-lookup"><span data-stu-id="05d2f-125">The text displayed in the message box title bar.</span></span> <span data-ttu-id="05d2f-126">Например, в панели заголовков может &quot; отображаться проверка удостоверения &quot; клиента.</span><span class="sxs-lookup"><span data-stu-id="05d2f-126">For example, you can have the title bar display &quot;Customer ID Validation&quot;.</span></span> <span data-ttu-id="05d2f-127">Если оставить этот аргумент пустым, &quot; отображается Microsoft &quot; Access.</span><span class="sxs-lookup"><span data-stu-id="05d2f-127">If you leave this argument blank, &quot;Microsoft Access&quot; is displayed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="05d2f-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="05d2f-128">Remarks</span></span>

<span data-ttu-id="05d2f-129">Вы можете использовать **действие MessageBox** для создания форматного сообщения об ошибке, аналогичного встроенным сообщениям об ошибках, отображаемой Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="05d2f-129">You can use the **MessageBox** action to create a formatted error message similar to built-in error messages displayed by Microsoft Access.</span></span> <span data-ttu-id="05d2f-130">Действие **MessageBox** позволяет отправлять сообщение в трех разделах для аргумента Сообщение.</span><span class="sxs-lookup"><span data-stu-id="05d2f-130">The **MessageBox** action permits you to supply a message in three sections for the Message argument.</span></span> <span data-ttu-id="05d2f-131">Разделы разделов разделяют с помощью символа "@".</span><span class="sxs-lookup"><span data-stu-id="05d2f-131">You separate the sections with the "@" character.</span></span>

<span data-ttu-id="05d2f-132">В следующем примере отображается форматированный ящик сообщений с раздельным сообщением.</span><span class="sxs-lookup"><span data-stu-id="05d2f-132">The following example displays a formatted message box with a sectioned message.</span></span> <span data-ttu-id="05d2f-133">Первый раздел текста в сообщении отображается в виде смелого заголовка.</span><span class="sxs-lookup"><span data-stu-id="05d2f-133">The first section of text in the message is displayed as a bold heading.</span></span> <span data-ttu-id="05d2f-134">Второй раздел отображается в виде простого текста под этим заголовком.</span><span class="sxs-lookup"><span data-stu-id="05d2f-134">The second section is displayed as plain text beneath that heading.</span></span> <span data-ttu-id="05d2f-135">Третий раздел отображается в виде простого текста под вторым разделом с пустой линией между ними.</span><span class="sxs-lookup"><span data-stu-id="05d2f-135">The third section is displayed as plain text beneath the second section, with a blank line between them.</span></span>

<span data-ttu-id="05d2f-136">Введите следующую строку в **аргументе Сообщение:**</span><span class="sxs-lookup"><span data-stu-id="05d2f-136">Type the following string in the **Message** argument:</span></span>

<span data-ttu-id="05d2f-137">**\!Неправильная @This кнопка не work.@Try другой.**</span><span class="sxs-lookup"><span data-stu-id="05d2f-137">**Wrong button\!@This button doesn't work.@Try another.**</span></span>

<span data-ttu-id="05d2f-138">Вы не можете запустить действие **MessageBox** в модуле Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="05d2f-138">You can't run the **MessageBox** action in a Visual Basic for Applications (VBA) module.</span></span> <span data-ttu-id="05d2f-139">Вместо этого используйте **функцию MsgBox.**</span><span class="sxs-lookup"><span data-stu-id="05d2f-139">Use the **MsgBox** function instead.</span></span>

## <a name="examples"></a><span data-ttu-id="05d2f-140">Примеры</span><span class="sxs-lookup"><span data-stu-id="05d2f-140">Examples</span></span>

<span data-ttu-id="05d2f-141">**Синхронизация форм с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="05d2f-141">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="05d2f-142">Следующий макрос открывает форму Списка продуктов в нижнем правом углу формы Поставщики, отображая продукты текущего поставщика.</span><span class="sxs-lookup"><span data-stu-id="05d2f-142">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="05d2f-143">В нем показано использование действий **Echo,** **MessageBox,** **GoToControl,** **StopMacro,** **OpenForm** и **MoveAndSizeWindow.**</span><span class="sxs-lookup"><span data-stu-id="05d2f-143">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="05d2f-144">В нем также показано использование условного выражения с **действиями MessageBox,** **GoToControl** и **StopMacro.**</span><span class="sxs-lookup"><span data-stu-id="05d2f-144">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="05d2f-145">Этот макрос следует прикрепить к кнопке Review Products в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="05d2f-145">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05d2f-146">Условие</span><span class="sxs-lookup"><span data-stu-id="05d2f-146">Condition</span></span></p></th>
<th><p><span data-ttu-id="05d2f-147">Макрокоманда</span><span class="sxs-lookup"><span data-stu-id="05d2f-147">Action</span></span></p></th>
<th><p><span data-ttu-id="05d2f-148">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="05d2f-148">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="05d2f-149">Примечание</span><span class="sxs-lookup"><span data-stu-id="05d2f-149">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="05d2f-150"><strong>ВыводНаЭкран</strong></span><span class="sxs-lookup"><span data-stu-id="05d2f-150"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="05d2f-151"><strong>Включить вывод</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="05d2f-151"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="05d2f-152">Приостанавливает обновление экрана, пока выполняется макрос.</span><span class="sxs-lookup"><span data-stu-id="05d2f-152">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05d2f-153">IsNull([SupplierID])</span><span class="sxs-lookup"><span data-stu-id="05d2f-153">IsNull([SupplierID])</span></span></p></td>
<td><p><span data-ttu-id="05d2f-154"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="05d2f-154"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="05d2f-155"><strong>Сообщение.</strong>Перейдите к записи поставщика, продукты которого вы хотите видеть, а затем нажмите кнопку Обзор продуктов снова.</span><span class="sxs-lookup"><span data-stu-id="05d2f-155"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="05d2f-156"><strong>Звуковой сигнал</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Выберите поставщика</span><span class="sxs-lookup"><span data-stu-id="05d2f-156"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="05d2f-157">Если в форме Поставщики нет текущего поставщика, отобразить сообщение.</span><span class="sxs-lookup"><span data-stu-id="05d2f-157">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05d2f-158">...</span><span class="sxs-lookup"><span data-stu-id="05d2f-158">...</span></span></p></td>
<td><p><span data-ttu-id="05d2f-159"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="05d2f-159"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="05d2f-160"><strong>Имя управления:</strong>CompanyName</span><span class="sxs-lookup"><span data-stu-id="05d2f-160"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="05d2f-161">Переместите фокус на управление CompanyName.</span><span class="sxs-lookup"><span data-stu-id="05d2f-161">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05d2f-162">...</span><span class="sxs-lookup"><span data-stu-id="05d2f-162">...</span></span></p></td>
<td><p><span data-ttu-id="05d2f-163"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="05d2f-163"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="05d2f-164">Остановите макрос.</span><span class="sxs-lookup"><span data-stu-id="05d2f-164">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="05d2f-165"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="05d2f-165"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="05d2f-166"><strong>Имя формы</strong>: Представление списка <strong>продуктов:</strong> <strong>Имя DatasheetFilter</strong>: Where <strong>Condition</strong>: [SupplierID] = [Forms]! [Поставщики]! [SupplierID] <strong>Режим данных:</strong> <strong>Режим чтения OnlyWindow</strong>: <strong>Нормальный</strong></span><span class="sxs-lookup"><span data-stu-id="05d2f-166"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [SupplierID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="05d2f-167">Откройте форму списка продуктов и покажите продукты текущего поставщика.</span><span class="sxs-lookup"><span data-stu-id="05d2f-167">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="05d2f-168"><strong>MoveAndSizeWindow</strong></span><span class="sxs-lookup"><span data-stu-id="05d2f-168"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="05d2f-169"><strong>Справа</strong>: 0.7799 &quot; <strong>Вниз</strong>: 1.8&quot;</span><span class="sxs-lookup"><span data-stu-id="05d2f-169"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="05d2f-170">Расположить форму списка продуктов в нижнем праве формы Поставщики.</span><span class="sxs-lookup"><span data-stu-id="05d2f-170">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="05d2f-171">**Проверка данных с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="05d2f-171">**Validate data by using a macro**</span></span>

<span data-ttu-id="05d2f-172">Следующий макрос проверки проверяет почтовые коды, вступив в форму Поставщики.</span><span class="sxs-lookup"><span data-stu-id="05d2f-172">The following validation macro checks the postal codes entered in a Suppliers form.</span></span> <span data-ttu-id="05d2f-173">В нем показано использование действий **StopMacro,** **MessageBox,** **CancelEvent** и **GoToControl.**</span><span class="sxs-lookup"><span data-stu-id="05d2f-173">It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions.</span></span> <span data-ttu-id="05d2f-174">Условное выражение проверяет страну/регион и почтовый код, вписаный в запись в форме.</span><span class="sxs-lookup"><span data-stu-id="05d2f-174">A conditional expression checks the country/region and postal code entered in a record on the form.</span></span> <span data-ttu-id="05d2f-175">Если почтовый код не в нужном формате для страны или региона, макрос отображает окно сообщений и отменяет сохранение записи.</span><span class="sxs-lookup"><span data-stu-id="05d2f-175">If the postal code isn't in the right format for the country/region, the macro displays a message box and cancels saving the record.</span></span> <span data-ttu-id="05d2f-176">Затем он возвращает вас в пункт управления почтовым кодом, где можно исправить ошибку.</span><span class="sxs-lookup"><span data-stu-id="05d2f-176">It then returns you to the PostalCode control, where you can correct the error.</span></span> <span data-ttu-id="05d2f-177">Этот макрос должен быть присоединен к свойству **BeforeUpdate** формы Поставщики.</span><span class="sxs-lookup"><span data-stu-id="05d2f-177">This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05d2f-178">Условие</span><span class="sxs-lookup"><span data-stu-id="05d2f-178">Condition</span></span></p></th>
<th><p><span data-ttu-id="05d2f-179">Макрокоманда</span><span class="sxs-lookup"><span data-stu-id="05d2f-179">Action</span></span></p></th>
<th><p><span data-ttu-id="05d2f-180">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="05d2f-180">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="05d2f-181">Примечание</span><span class="sxs-lookup"><span data-stu-id="05d2f-181">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05d2f-182">IsNull([CountryRegion])</span><span class="sxs-lookup"><span data-stu-id="05d2f-182">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="05d2f-183"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="05d2f-183"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="05d2f-184">Если CountryRegion <strong>является Null,</strong>почтовый код не может быть проверен.</span><span class="sxs-lookup"><span data-stu-id="05d2f-184">If CountryRegion is <strong>Null</strong>, the postal code can't be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05d2f-185">[CountryRegion] В ( &quot; &quot; Франция, &quot; &quot; Италия, &quot; Испания &quot; ) и Len ([Почтовый индекс]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="05d2f-185">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([PostalCode]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="05d2f-186"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="05d2f-186"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="05d2f-187"><strong>Сообщение.</strong>Почтовый код должен быть 5 символов.</span><span class="sxs-lookup"><span data-stu-id="05d2f-187"><strong>Message</strong>: The postal code must be 5 characters.</span></span> <span data-ttu-id="05d2f-188"><strong>Звуковой сигнал</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Ошибка почтового кода</span><span class="sxs-lookup"><span data-stu-id="05d2f-188"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="05d2f-189">Если почтовый код не имеет 5 символов, отобразить сообщение.</span><span class="sxs-lookup"><span data-stu-id="05d2f-189">If the postal code isn't 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05d2f-190">...</span><span class="sxs-lookup"><span data-stu-id="05d2f-190">...</span></span></p></td>
<td><p><span data-ttu-id="05d2f-191"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="05d2f-191"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="05d2f-192">Отмена события.</span><span class="sxs-lookup"><span data-stu-id="05d2f-192">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="05d2f-193"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="05d2f-193"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="05d2f-194"><strong>Имя управления:</strong>PostalCode</span><span class="sxs-lookup"><span data-stu-id="05d2f-194"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05d2f-195">[CountryRegion] В ( &quot; Австралия , Сингапур ) и &quot; &quot; &quot; Len ([Почтовый индекс]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="05d2f-195">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([PostalCode]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="05d2f-196"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="05d2f-196"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="05d2f-197"><strong>Сообщение.</strong>Почтовый код должен быть 4 символа.</span><span class="sxs-lookup"><span data-stu-id="05d2f-197"><strong>Message</strong>: The postal code must be 4 characters.</span></span> <span data-ttu-id="05d2f-198"><strong>Звуковой сигнал</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Ошибка почтового кода</span><span class="sxs-lookup"><span data-stu-id="05d2f-198"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="05d2f-199">Если почтовый код не 4 символа, отобразить сообщение.</span><span class="sxs-lookup"><span data-stu-id="05d2f-199">If the postal code isn't 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05d2f-200">...</span><span class="sxs-lookup"><span data-stu-id="05d2f-200">...</span></span></p></td>
<td><p><span data-ttu-id="05d2f-201"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="05d2f-201"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="05d2f-202">Отмена события.</span><span class="sxs-lookup"><span data-stu-id="05d2f-202">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="05d2f-203"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="05d2f-203"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="05d2f-204"><strong>Имя управления:</strong>PostalCode</span><span class="sxs-lookup"><span data-stu-id="05d2f-204"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05d2f-205">([CountryRegion] = &quot; Канада ) и &quot; ([Почтовый индекс] Не нравится &quot; [A-Z][0-9][A-Z] [0-9][A-Z][0-9] &quot; )</span><span class="sxs-lookup"><span data-stu-id="05d2f-205">([CountryRegion] = &quot;Canada&quot;) And ([PostalCode] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="05d2f-206"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="05d2f-206"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="05d2f-207"><strong>Сообщение.</strong>Почтовый код не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="05d2f-207"><strong>Message</strong>: The postal code is not valid.</span></span> <span data-ttu-id="05d2f-208">Пример канадского кода: сигнал H1J 1C3 <strong></strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Ошибка почтового кода</span><span class="sxs-lookup"><span data-stu-id="05d2f-208">Example of Canadian code: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="05d2f-209">Если почтовый код не является правильным для Канады, отобразить сообщение.</span><span class="sxs-lookup"><span data-stu-id="05d2f-209">If the postal code isn't correct for Canada, display a message.</span></span> <span data-ttu-id="05d2f-210">(Пример канадского кода: H1J 1C3)</span><span class="sxs-lookup"><span data-stu-id="05d2f-210">(Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05d2f-211">...</span><span class="sxs-lookup"><span data-stu-id="05d2f-211">...</span></span></p></td>
<td><p><span data-ttu-id="05d2f-212"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="05d2f-212"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="05d2f-213">Отмена события.</span><span class="sxs-lookup"><span data-stu-id="05d2f-213">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

