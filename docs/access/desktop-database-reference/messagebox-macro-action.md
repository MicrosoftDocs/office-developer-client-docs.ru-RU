---
title: Действия макроса MessageBox
TOCTitle: MessageBox Macro Action
ms:assetid: 326a0e68-38fb-4f81-b319-5a70caa5aec4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192304(v=office.15)
ms:contentKeyID: 48544077
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6654d2994b472ff2d495b60fffd5fcdbd6e58089
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885236"
---
# <a name="messagebox-macro-action"></a><span data-ttu-id="e7bae-102">Действия макроса MessageBox</span><span class="sxs-lookup"><span data-stu-id="e7bae-102">MessageBox Macro Action</span></span>


<span data-ttu-id="e7bae-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e7bae-103">**Applies to**: Access 2013, Office 2013</span></span>




<span data-ttu-id="e7bae-104">Действие **MessageBox** можно использовать для отображения окна сообщения, содержащее предупреждение или информационное сообщение.</span><span class="sxs-lookup"><span data-stu-id="e7bae-104">You can use the **MessageBox** action to display a message box containing a warning or an informational message.</span></span> <span data-ttu-id="e7bae-105">Например можно использовать действие **MessageBox** с макросами проверки.</span><span class="sxs-lookup"><span data-stu-id="e7bae-105">For example, you can use the **MessageBox** action with validation macros.</span></span> <span data-ttu-id="e7bae-106">Элемент управления или запись не условие в макросе, прошедших окно сообщения можно отображать сообщение об ошибке и приведены инструкции по тип данных, который должен быть введен.</span><span class="sxs-lookup"><span data-stu-id="e7bae-106">When a control or record fails a validation condition in the macro, a message box can display an error message and provide instructions about the kind of data that should be entered.</span></span>

## <a name="setting"></a><span data-ttu-id="e7bae-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="e7bae-107">Setting</span></span>

<span data-ttu-id="e7bae-108">Действие **MessageBox** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="e7bae-108">The **MessageBox** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e7bae-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="e7bae-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="e7bae-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e7bae-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7bae-111"><strong>Сообщение</strong></span><span class="sxs-lookup"><span data-stu-id="e7bae-111"><strong>Message</strong></span></span></p></td>
<td><p><span data-ttu-id="e7bae-112">Текст в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="e7bae-112">The text in the message box.</span></span> <span data-ttu-id="e7bae-113">Введите текст сообщения в окне <strong>сообщения</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="e7bae-113">Enter the message text in the <strong>Message</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="e7bae-114">Можно ввести до 255 знаков или введите выражение (стоять знак равенства).</span><span class="sxs-lookup"><span data-stu-id="e7bae-114">You can type up to 255 characters or enter an expression (preceded by an equal sign).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bae-115"><strong>Beep</strong></span><span class="sxs-lookup"><span data-stu-id="e7bae-115"><strong>Beep</strong></span></span></p></td>
<td><p><span data-ttu-id="e7bae-116">Указывает ли ваше звукового сигнала при выводе сообщения.</span><span class="sxs-lookup"><span data-stu-id="e7bae-116">Specifies whether your computer's speaker sounds a beep tone when the message displays.</span></span> <span data-ttu-id="e7bae-117">Нажмите кнопку <strong>Да</strong> (звук сигнала) или <strong>Нет</strong> (не звук сигнала).</span><span class="sxs-lookup"><span data-stu-id="e7bae-117">Click <strong>Yes</strong> (sound the beep tone) or <strong>No</strong> (don't sound the beep tone).</span></span> <span data-ttu-id="e7bae-118">По умолчанию используется значение <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="e7bae-118">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bae-119"><strong>Тип</strong></span><span class="sxs-lookup"><span data-stu-id="e7bae-119"><strong>Type</strong></span></span></p></td>
<td><p><span data-ttu-id="e7bae-120">Тип окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="e7bae-120">The type of message box.</span></span> <span data-ttu-id="e7bae-121">Каждый тип имеет другой значок.</span><span class="sxs-lookup"><span data-stu-id="e7bae-121">Each type has a different icon.</span></span> <span data-ttu-id="e7bae-122">Нажмите кнопку <strong>Нет</strong>, <strong>важных</strong>, <strong>Предупреждение?</strong>, <strong>Предупреждение!</strong>, или <strong>сведения</strong>.</span><span class="sxs-lookup"><span data-stu-id="e7bae-122">Click <strong>None</strong>, <strong>Critical</strong>, <strong>Warning?</strong>, <strong>Warning!</strong>, or <strong>Information</strong>.</span></span> <span data-ttu-id="e7bae-123">Значение по умолчанию — <strong>None</strong>.</span><span class="sxs-lookup"><span data-stu-id="e7bae-123">The default is <strong>None</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bae-124"><strong>Название</strong></span><span class="sxs-lookup"><span data-stu-id="e7bae-124"><strong>Title</strong></span></span></p></td>
<td><p><span data-ttu-id="e7bae-125">Текст, отображаемый в строке заголовка окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="e7bae-125">The text displayed in the message box title bar.</span></span> <span data-ttu-id="e7bae-126">Например имеется отображения панели заголовка &quot;проверка кода клиента&quot;.</span><span class="sxs-lookup"><span data-stu-id="e7bae-126">For example, you can have the title bar display &quot;Customer ID Validation&quot;.</span></span> <span data-ttu-id="e7bae-127">Если оставить этот аргумент пустым, &quot;Microsoft Access&quot; отображается.</span><span class="sxs-lookup"><span data-stu-id="e7bae-127">If you leave this argument blank, &quot;Microsoft Access&quot; is displayed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e7bae-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="e7bae-128">Remarks</span></span>

<span data-ttu-id="e7bae-129">Действие **MessageBox** можно использовать для создания форматированное сообщение об ошибке, аналогичное встроенным сообщениям об ошибках в Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="e7bae-129">You can use the **MessageBox** action to create a formatted error message similar to built-in error messages displayed by Microsoft Access.</span></span> <span data-ttu-id="e7bae-130">Действие **MessageBox** позволяет ввести сообщение из трех разделов для аргумента сообщения.</span><span class="sxs-lookup"><span data-stu-id="e7bae-130">The **MessageBox** action permits you to supply a message in three sections for the Message argument.</span></span> <span data-ttu-id="e7bae-131">Разделите разделы с «@» символов.</span><span class="sxs-lookup"><span data-stu-id="e7bae-131">You separate the sections with the "@" character.</span></span>

<span data-ttu-id="e7bae-132">Следующий пример отображает окно с форматированным сообщением.</span><span class="sxs-lookup"><span data-stu-id="e7bae-132">The following example displays a formatted message box with a sectioned message.</span></span> <span data-ttu-id="e7bae-133">В первом разделе текста в сообщении отображается как заголовок полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="e7bae-133">The first section of text in the message is displayed as a bold heading.</span></span> <span data-ttu-id="e7bae-134">Во втором разделе отображается в виде обычного текста под заголовком.</span><span class="sxs-lookup"><span data-stu-id="e7bae-134">The second section is displayed as plain text beneath that heading.</span></span> <span data-ttu-id="e7bae-135">Третий раздел отображается в виде обычного текста под во втором разделе с пустой строки между ними.</span><span class="sxs-lookup"><span data-stu-id="e7bae-135">The third section is displayed as plain text beneath the second section, with a blank line between them.</span></span>

<span data-ttu-id="e7bae-136">Введите следующую строку в аргументе **сообщения** :</span><span class="sxs-lookup"><span data-stu-id="e7bae-136">Type the following string in the **Message** argument:</span></span>

<span data-ttu-id="e7bae-137">**Неверный кнопка\!@This кнопка не Work.@Try другую.**</span><span class="sxs-lookup"><span data-stu-id="e7bae-137">**Wrong button\!@This button doesn't work.@Try another.**</span></span>

<span data-ttu-id="e7bae-138">Не удается выполнить действие **MessageBox** в Visual Basic для приложений (VBA) модуля.</span><span class="sxs-lookup"><span data-stu-id="e7bae-138">You can't run the **MessageBox** action in a Visual Basic for Applications (VBA) module.</span></span> <span data-ttu-id="e7bae-139">Вместо этого используйте функции **MsgBox** .</span><span class="sxs-lookup"><span data-stu-id="e7bae-139">Use the **MsgBox** function instead.</span></span>

## <a name="examples"></a><span data-ttu-id="e7bae-140">Примеры</span><span class="sxs-lookup"><span data-stu-id="e7bae-140">Examples</span></span>

<span data-ttu-id="e7bae-141">**Синхронизация форм с помощью макроса (en)**</span><span class="sxs-lookup"><span data-stu-id="e7bae-141">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="e7bae-142">Следующий макрос открывает форму списка продуктов в правом нижнем углу формы Поставщики, отображение текущего поставщика продуктов.</span><span class="sxs-lookup"><span data-stu-id="e7bae-142">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="e7bae-143">Демонстрируется использование **эхо**, **MessageBox**, **КЭлементуУправления**, **ОстановитьМакрос**, **ОткрытьФорму**и **MoveAndSizeWindow** действий.</span><span class="sxs-lookup"><span data-stu-id="e7bae-143">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="e7bae-144">Также показано использование условного выражения с **MessageBox**, **КЭлементуУправления**« **Поставщики** ».</span><span class="sxs-lookup"><span data-stu-id="e7bae-144">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="e7bae-145">Этот макрос должен быть связан с кнопкой Обзор продуктов в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="e7bae-145">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e7bae-146">Condition</span><span class="sxs-lookup"><span data-stu-id="e7bae-146">Condition</span></span></p></th>
<th><p><span data-ttu-id="e7bae-147">Действие</span><span class="sxs-lookup"><span data-stu-id="e7bae-147">Action</span></span></p></th>
<th><p><span data-ttu-id="e7bae-148">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="e7bae-148">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="e7bae-149">Comment</span><span class="sxs-lookup"><span data-stu-id="e7bae-149">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="e7bae-150"><strong>Эхо</strong></span><span class="sxs-lookup"><span data-stu-id="e7bae-150"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="e7bae-151"><strong>Вывод на экран</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="e7bae-151"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="e7bae-152">Остановите обновление экрана в процессе выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="e7bae-152">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bae-153">IsNull([SupplierID])</span><span class="sxs-lookup"><span data-stu-id="e7bae-153">IsNull([SupplierID])</span></span></p></td>
<td><p><span data-ttu-id="e7bae-154"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="e7bae-154"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="e7bae-155"><strong>Сообщение</strong>: перемещение на запись поставщика, продукты, чтобы увидеть, затем нажмите кнопку Предварительный просмотр еще раз.</span><span class="sxs-lookup"><span data-stu-id="e7bae-155"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="e7bae-156"><strong>Звуковые сигналы</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Выбор поставщика</span><span class="sxs-lookup"><span data-stu-id="e7bae-156"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="e7bae-157">При отсутствии никто из современных поставщиков в форме Поставщики, отображается сообщение.</span><span class="sxs-lookup"><span data-stu-id="e7bae-157">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bae-158">...</span><span class="sxs-lookup"><span data-stu-id="e7bae-158"></span></span></p></td>
<td><p><span data-ttu-id="e7bae-159"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="e7bae-159"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="e7bae-160"><strong>Имя элемента управления</strong>: CompanyName</span><span class="sxs-lookup"><span data-stu-id="e7bae-160"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="e7bae-161">Перемещение фокуса на элемент управления CompanyName.</span><span class="sxs-lookup"><span data-stu-id="e7bae-161">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bae-162">...</span><span class="sxs-lookup"><span data-stu-id="e7bae-162"></span></span></p></td>
<td><p><span data-ttu-id="e7bae-163"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="e7bae-163"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e7bae-164">Остановка макроса.</span><span class="sxs-lookup"><span data-stu-id="e7bae-164">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="e7bae-165"><strong>ОткрытьФорму</strong></span><span class="sxs-lookup"><span data-stu-id="e7bae-165"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="e7bae-166"><strong>Имя формы</strong>: список продуктов <strong>представления</strong>: <strong>Имя DatasheetFilter</strong>: <strong>условие отбора</strong>: [код поставщика] = [Forms]! [Поставщики]! [Код поставщика] <strong>Режим данных</strong>: <strong>Режим чтения OnlyWindow</strong>: <strong>Обычный</strong></span><span class="sxs-lookup"><span data-stu-id="e7bae-166"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [SupplierID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="e7bae-167">Откройте форму списка продуктов и отображение текущего поставщика продуктов.</span><span class="sxs-lookup"><span data-stu-id="e7bae-167">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="e7bae-168"><strong>MoveAndSizeWindow</strong></span><span class="sxs-lookup"><span data-stu-id="e7bae-168"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="e7bae-169"><strong>Право</strong>: 0,7799&quot; <strong>вниз</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="e7bae-169"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="e7bae-170">Положение формы списка продуктов в нижней правой части формы Поставщики.</span><span class="sxs-lookup"><span data-stu-id="e7bae-170">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e7bae-171">**Проверка данных с помощью макроса (en)**</span><span class="sxs-lookup"><span data-stu-id="e7bae-171">**Validate data by using a macro**</span></span>

<span data-ttu-id="e7bae-172">Следующий макрос для проверки проверяет почтовые индексы, введенные в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="e7bae-172">The following validation macro checks the postal codes entered in a Suppliers form.</span></span> <span data-ttu-id="e7bae-173">Демонстрируется использование **ОстановитьМакрос**, **MessageBox**, **ОтменитьСобытие**и **КЭлементуУправления** действия.</span><span class="sxs-lookup"><span data-stu-id="e7bae-173">It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions.</span></span> <span data-ttu-id="e7bae-174">Условным выражением проверяет страны или региона и почтового индекса в записи на форме.</span><span class="sxs-lookup"><span data-stu-id="e7bae-174">A conditional expression checks the country/region and postal code entered in a record on the form.</span></span> <span data-ttu-id="e7bae-175">Если почтовый индекс не находится в нужном формате для страны или региона, макрос отображается окно сообщения и показано, как отменить сохранение записи.</span><span class="sxs-lookup"><span data-stu-id="e7bae-175">If the postal code isn't in the right format for the country/region, the macro displays a message box and cancels saving the record.</span></span> <span data-ttu-id="e7bae-176">Оно будет снова к элементу управления PostalCode для исправления ошибки.</span><span class="sxs-lookup"><span data-stu-id="e7bae-176">It then returns you to the PostalCode control, where you can correct the error.</span></span> <span data-ttu-id="e7bae-177">Этот макрос должен быть связан свойством **BeforeUpdate** формы Поставщики.</span><span class="sxs-lookup"><span data-stu-id="e7bae-177">This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e7bae-178">Condition</span><span class="sxs-lookup"><span data-stu-id="e7bae-178">Condition</span></span></p></th>
<th><p><span data-ttu-id="e7bae-179">Действие</span><span class="sxs-lookup"><span data-stu-id="e7bae-179">Action</span></span></p></th>
<th><p><span data-ttu-id="e7bae-180">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="e7bae-180">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="e7bae-181">Comment</span><span class="sxs-lookup"><span data-stu-id="e7bae-181">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7bae-182">IsNull([CountryRegion])</span><span class="sxs-lookup"><span data-stu-id="e7bae-182">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="e7bae-183"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="e7bae-183"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e7bae-184">Если Страна имеет <strong>значение Null</strong>, почтовый индекс не может быть проверен.</span><span class="sxs-lookup"><span data-stu-id="e7bae-184">If CountryRegion is <strong>Null</strong>, the postal code can't be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bae-185">[Страна] В (&quot;Франции&quot;,&quot;Италия&quot;,&quot;Испания&quot;) и Len([PostalCode]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="e7bae-185">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([PostalCode]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="e7bae-186"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="e7bae-186"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="e7bae-187"><strong>Сообщение</strong>: почтовый индекс должен состоять из 5 знаков.</span><span class="sxs-lookup"><span data-stu-id="e7bae-187"><strong>Message</strong>: The postal code must be 5 characters.</span></span> <span data-ttu-id="e7bae-188"><strong>Звуковые сигналы</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: ошибка почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="e7bae-188"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="e7bae-189">Если почтовый индекс не 5 знаков, отобразите сообщение.</span><span class="sxs-lookup"><span data-stu-id="e7bae-189">If the postal code isn't 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bae-190">...</span><span class="sxs-lookup"><span data-stu-id="e7bae-190"></span></span></p></td>
<td><p><span data-ttu-id="e7bae-191"><strong>ОтменитьСобытие</strong></span><span class="sxs-lookup"><span data-stu-id="e7bae-191"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e7bae-192">Отмените событие.</span><span class="sxs-lookup"><span data-stu-id="e7bae-192">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="e7bae-193"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="e7bae-193"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="e7bae-194"><strong>Имя элемента управления</strong>: PostalCode</span><span class="sxs-lookup"><span data-stu-id="e7bae-194"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bae-195">[Страна] В (&quot;Австралия&quot;,&quot;Сингапур&quot;) и Len([PostalCode]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="e7bae-195">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([PostalCode]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="e7bae-196"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="e7bae-196"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="e7bae-197"><strong>Сообщение</strong>: почтовый индекс должен быть 4 символов.</span><span class="sxs-lookup"><span data-stu-id="e7bae-197"><strong>Message</strong>: The postal code must be 4 characters.</span></span> <span data-ttu-id="e7bae-198"><strong>Звуковые сигналы</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: ошибка почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="e7bae-198"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="e7bae-199">Если почтовый индекс не 4 символа, отобразите сообщение.</span><span class="sxs-lookup"><span data-stu-id="e7bae-199">If the postal code isn't 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bae-200">...</span><span class="sxs-lookup"><span data-stu-id="e7bae-200"></span></span></p></td>
<td><p><span data-ttu-id="e7bae-201"><strong>ОтменитьСобытие</strong></span><span class="sxs-lookup"><span data-stu-id="e7bae-201"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e7bae-202">Отмените событие.</span><span class="sxs-lookup"><span data-stu-id="e7bae-202">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="e7bae-203"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="e7bae-203"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="e7bae-204"><strong>Имя элемента управления</strong>: PostalCode</span><span class="sxs-lookup"><span data-stu-id="e7bae-204"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bae-205">([Страна] = &quot;Канада&quot;) И ([PostalCode] не нравится&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</span><span class="sxs-lookup"><span data-stu-id="e7bae-205">([CountryRegion] = &quot;Canada&quot;) And ([PostalCode] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="e7bae-206"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="e7bae-206"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="e7bae-207"><strong>Сообщение</strong>: почтовый индекс является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="e7bae-207"><strong>Message</strong>: The postal code is not valid.</span></span> <span data-ttu-id="e7bae-208">Пример кода, английский (Канада): H1J 1 c 3 <strong>звуковые сигналы</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: почтовый код ошибки</span><span class="sxs-lookup"><span data-stu-id="e7bae-208">Example of Canadian code: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="e7bae-209">Если почтовый индекс не соответствует формату для Канады, отобразите сообщение.</span><span class="sxs-lookup"><span data-stu-id="e7bae-209">If the postal code isn't correct for Canada, display a message.</span></span> <span data-ttu-id="e7bae-210">(Пример кода, английский (Канада): H1J 1 c 3)</span><span class="sxs-lookup"><span data-stu-id="e7bae-210">(Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bae-211">...</span><span class="sxs-lookup"><span data-stu-id="e7bae-211"></span></span></p></td>
<td><p><span data-ttu-id="e7bae-212"><strong>ОтменитьСобытие</strong></span><span class="sxs-lookup"><span data-stu-id="e7bae-212"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e7bae-213">Отмените событие.</span><span class="sxs-lookup"><span data-stu-id="e7bae-213">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

