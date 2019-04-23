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
# <a name="messagebox-macro-action"></a><span data-ttu-id="adeee-102">Макрокоманда MessageBox</span><span class="sxs-lookup"><span data-stu-id="adeee-102">MessageBox macro action</span></span>

<span data-ttu-id="adeee-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="adeee-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="adeee-104">С помощью макрокоманды **MessageBox** можно отобразить окно сообщения с предупреждением или информационным сообщением.</span><span class="sxs-lookup"><span data-stu-id="adeee-104">You can use the **MessageBox** action to display a message box containing a warning or an informational message.</span></span> <span data-ttu-id="adeee-105">Например, вы можете использовать действие **MessageBox** с макросами проверки.</span><span class="sxs-lookup"><span data-stu-id="adeee-105">For example, you can use the **MessageBox** action with validation macros.</span></span> <span data-ttu-id="adeee-106">Когда элемент управления или запись не проходит условие проверки в макросе, в окне сообщения отображается сообщение об ошибке и предоставляются инструкции о типе вводимых данных.</span><span class="sxs-lookup"><span data-stu-id="adeee-106">When a control or record fails a validation condition in the macro, a message box can display an error message and provide instructions about the kind of data that should be entered.</span></span>

## <a name="setting"></a><span data-ttu-id="adeee-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="adeee-107">Setting</span></span>

<span data-ttu-id="adeee-108">Действие **MessageBox** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="adeee-108">The **MessageBox** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="adeee-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="adeee-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="adeee-110">Описание</span><span class="sxs-lookup"><span data-stu-id="adeee-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adeee-111"><strong>Message</strong></span><span class="sxs-lookup"><span data-stu-id="adeee-111"><strong>Message</strong></span></span></p></td>
<td><p><span data-ttu-id="adeee-112">Текст в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="adeee-112">The text in the message box.</span></span> <span data-ttu-id="adeee-113">Введите текст сообщения в поле <strong>сообщение</strong> в разделе <strong>аргументы макрокоманды</strong> в панели построителя макросов.</span><span class="sxs-lookup"><span data-stu-id="adeee-113">Enter the message text in the <strong>Message</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="adeee-114">Можно ввести до 255 символов или ввести выражение (перед ним должен стоять знак равенства).</span><span class="sxs-lookup"><span data-stu-id="adeee-114">You can type up to 255 characters or enter an expression (preceded by an equal sign).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adeee-115"><strong>Beep</strong></span><span class="sxs-lookup"><span data-stu-id="adeee-115"><strong>Beep</strong></span></span></p></td>
<td><p><span data-ttu-id="adeee-116">Указывает, будет ли динамик компьютера звуковым сигналом при отображении сообщения.</span><span class="sxs-lookup"><span data-stu-id="adeee-116">Specifies whether your computer's speaker sounds a beep tone when the message displays.</span></span> <span data-ttu-id="adeee-117">Нажмите кнопку <strong>Да</strong> (звук гудка гудка) или <strong>нет</strong> (не выдавать звуковой сигнал гудка).</span><span class="sxs-lookup"><span data-stu-id="adeee-117">Click <strong>Yes</strong> (sound the beep tone) or <strong>No</strong> (don't sound the beep tone).</span></span> <span data-ttu-id="adeee-118">Значение по умолчанию — <strong>Yes</strong>.</span><span class="sxs-lookup"><span data-stu-id="adeee-118">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adeee-119"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="adeee-119"><strong>Type</strong></span></span></p></td>
<td><p><span data-ttu-id="adeee-120">Тип окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="adeee-120">The type of message box.</span></span> <span data-ttu-id="adeee-121">Каждый тип имеет свой значок.</span><span class="sxs-lookup"><span data-stu-id="adeee-121">Each type has a different icon.</span></span> <span data-ttu-id="adeee-122">Выберите <strong>None (нет</strong>), <strong>Critical</strong>( <strong>предупреждение</strong>), Warning ( <strong>предупреждение</strong>)) или <strong>Information (сведения</strong>).</span><span class="sxs-lookup"><span data-stu-id="adeee-122">Click <strong>None</strong>, <strong>Critical</strong>, <strong>Warning?</strong>, <strong>Warning!</strong>, or <strong>Information</strong>.</span></span> <span data-ttu-id="adeee-123">Значение по умолчанию — <strong>None</strong>.</span><span class="sxs-lookup"><span data-stu-id="adeee-123">The default is <strong>None</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adeee-124"><strong>Title</strong></span><span class="sxs-lookup"><span data-stu-id="adeee-124"><strong>Title</strong></span></span></p></td>
<td><p><span data-ttu-id="adeee-125">Текст, отображаемый в строке заголовка окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="adeee-125">The text displayed in the message box title bar.</span></span> <span data-ttu-id="adeee-126">Например, можно отобразить &quot;для строки заголовка проверку&quot;кода клиента.</span><span class="sxs-lookup"><span data-stu-id="adeee-126">For example, you can have the title bar display &quot;Customer ID Validation&quot;.</span></span> <span data-ttu-id="adeee-127">Если оставить этот аргумент пустым, &quot;будет выведено&quot; приложение Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="adeee-127">If you leave this argument blank, &quot;Microsoft Access&quot; is displayed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="adeee-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="adeee-128">Remarks</span></span>

<span data-ttu-id="adeee-129">С помощью макрокоманды **MessageBox** можно создавать отформатированные сообщения об ошибках, аналогичные встроенным сообщениям об ошибках, отображаемЫм в Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="adeee-129">You can use the **MessageBox** action to create a formatted error message similar to built-in error messages displayed by Microsoft Access.</span></span> <span data-ttu-id="adeee-130">Действие **MessageBox** позволяет указать сообщение в трех разделах для аргумента Message.</span><span class="sxs-lookup"><span data-stu-id="adeee-130">The **MessageBox** action permits you to supply a message in three sections for the Message argument.</span></span> <span data-ttu-id="adeee-131">Вы разделяете разделы символом "@".</span><span class="sxs-lookup"><span data-stu-id="adeee-131">You separate the sections with the "@" character.</span></span>

<span data-ttu-id="adeee-132">В следующем примере отображается форматированное окно с сообщением с поразделным сообщением.</span><span class="sxs-lookup"><span data-stu-id="adeee-132">The following example displays a formatted message box with a sectioned message.</span></span> <span data-ttu-id="adeee-133">Первый раздел текста сообщения отображается в виде полужирного начертания.</span><span class="sxs-lookup"><span data-stu-id="adeee-133">The first section of text in the message is displayed as a bold heading.</span></span> <span data-ttu-id="adeee-134">Второй раздел отображается в виде обычного текста под заголовком.</span><span class="sxs-lookup"><span data-stu-id="adeee-134">The second section is displayed as plain text beneath that heading.</span></span> <span data-ttu-id="adeee-135">Третий раздел отображается как обычный текст под вторым разделом с пустой строкой между ними.</span><span class="sxs-lookup"><span data-stu-id="adeee-135">The third section is displayed as plain text beneath the second section, with a blank line between them.</span></span>

<span data-ttu-id="adeee-136">Введите в аргументе **Message** следующую строку:</span><span class="sxs-lookup"><span data-stu-id="adeee-136">Type the following string in the **Message** argument:</span></span>

<span data-ttu-id="adeee-137">**НеПравильное Нажатие\!кнопки @This кнопка не работает. @Try другой.**</span><span class="sxs-lookup"><span data-stu-id="adeee-137">**Wrong button\!@This button doesn't work.@Try another.**</span></span>

<span data-ttu-id="adeee-138">Действие **MessageBox** невозможно выполнить в модуле Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="adeee-138">You can't run the **MessageBox** action in a Visual Basic for Applications (VBA) module.</span></span> <span data-ttu-id="adeee-139">Вместо этого используйте функцию **MsgBox** .</span><span class="sxs-lookup"><span data-stu-id="adeee-139">Use the **MsgBox** function instead.</span></span>

## <a name="examples"></a><span data-ttu-id="adeee-140">Примеры</span><span class="sxs-lookup"><span data-stu-id="adeee-140">Examples</span></span>

<span data-ttu-id="adeee-141">**Синхронизация форм с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="adeee-141">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="adeee-142">Следующий макрос открывает форму списка товаров в правом нижнем углу формы поставщики, в которой отображаются продукты текущего поставщика.</span><span class="sxs-lookup"><span data-stu-id="adeee-142">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="adeee-143">В нем показано использование действий **echo**, **MessageBox**, **КЭлементуУправления**, **Макрокоманда StopMacro**, **OpenForm**и **мовеандсизевиндов** .</span><span class="sxs-lookup"><span data-stu-id="adeee-143">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="adeee-144">В нем также показано использование условного выражения с действиями **MessageBox**, **КЭлементуУправления**и **Макрокоманда StopMacro** .</span><span class="sxs-lookup"><span data-stu-id="adeee-144">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="adeee-145">Этот макрос необходимо прикрепить к кнопке "проверить продукты" в форме "поставщики".</span><span class="sxs-lookup"><span data-stu-id="adeee-145">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="adeee-146">Условие</span><span class="sxs-lookup"><span data-stu-id="adeee-146">Condition</span></span></p></th>
<th><p><span data-ttu-id="adeee-147">Действие</span><span class="sxs-lookup"><span data-stu-id="adeee-147">Action</span></span></p></th>
<th><p><span data-ttu-id="adeee-148">Аргументы: Настройка</span><span class="sxs-lookup"><span data-stu-id="adeee-148">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="adeee-149">Комментарий</span><span class="sxs-lookup"><span data-stu-id="adeee-149">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="adeee-150"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="adeee-150"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="adeee-151"><strong>Echo on</strong>: <strong>нет</strong></span><span class="sxs-lookup"><span data-stu-id="adeee-151"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="adeee-152">Остановить обновление экрана во время выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="adeee-152">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adeee-153">IsNull ([КодПоставщика])</span><span class="sxs-lookup"><span data-stu-id="adeee-153">IsNull([SupplierID])</span></span></p></td>
<td><p><span data-ttu-id="adeee-154"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="adeee-154"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="adeee-155"><strong>Сообщение</strong>: перейдите к записи поставщика, продукты которой вы хотите просмотреть, а затем снова нажмите кнопку Просмотр продуктов.</span><span class="sxs-lookup"><span data-stu-id="adeee-155"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="adeee-156"><strong>Beep</strong>: <strong>естипе</strong>: <strong>нонетитле</strong>: выберите поставщика</span><span class="sxs-lookup"><span data-stu-id="adeee-156"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="adeee-157">Если в форме Поставщики нет текущего поставщика, отобразите сообщение.</span><span class="sxs-lookup"><span data-stu-id="adeee-157">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adeee-158">...</span><span class="sxs-lookup"><span data-stu-id="adeee-158"></span></span></p></td>
<td><p><span data-ttu-id="adeee-159"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="adeee-159"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="adeee-160"><strong>Имя элемента управления</strong>: CompanyName</span><span class="sxs-lookup"><span data-stu-id="adeee-160"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="adeee-161">Перемещение фокуса на элемент управления CompanyName.</span><span class="sxs-lookup"><span data-stu-id="adeee-161">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adeee-162">...</span><span class="sxs-lookup"><span data-stu-id="adeee-162"></span></span></p></td>
<td><p><span data-ttu-id="adeee-163"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="adeee-163"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="adeee-164">Остановка макроса.</span><span class="sxs-lookup"><span data-stu-id="adeee-164">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="adeee-165"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="adeee-165"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="adeee-166"><strong>Имя формы</strong>: <strong>представление</strong>списка продуктов: <strong>даташитфилтер Name</strong>: <strong>WHERE Condition</strong>: [КодПоставщика] = [Forms]! [Поставщики]! Ключев <strong>Режим данных</strong>: <strong>режим чтения онливиндов</strong>: <strong>обычный</strong></span><span class="sxs-lookup"><span data-stu-id="adeee-166"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [SupplierID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="adeee-167">Откройте форму Список продуктов и отобразите текущие продукты поставщика.</span><span class="sxs-lookup"><span data-stu-id="adeee-167">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="adeee-168"><strong>Мовеандсизевиндов</strong></span><span class="sxs-lookup"><span data-stu-id="adeee-168"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="adeee-169"><strong>Right</strong>: 0,7799&quot; <strong>вниз</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="adeee-169"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="adeee-170">РасПоложите форму списка товаров в правом нижнем углу формы Поставщики.</span><span class="sxs-lookup"><span data-stu-id="adeee-170">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="adeee-171">**Проверка данных с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="adeee-171">**Validate data by using a macro**</span></span>

<span data-ttu-id="adeee-172">Следующий макрос проверки проверяет почтовые индексы, введенные в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="adeee-172">The following validation macro checks the postal codes entered in a Suppliers form.</span></span> <span data-ttu-id="adeee-173">В нем показано использование действий **Макрокоманда StopMacro**, **MessageBox**, **Макрокоманда CancelEvent**и **КЭлементуУправления** .</span><span class="sxs-lookup"><span data-stu-id="adeee-173">It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions.</span></span> <span data-ttu-id="adeee-174">Условное выражение проверяет страну, регион и почтовый индекс, введенные в записи в форме.</span><span class="sxs-lookup"><span data-stu-id="adeee-174">A conditional expression checks the country/region and postal code entered in a record on the form.</span></span> <span data-ttu-id="adeee-175">Если почтовый индекс находится в неправильном формате для страны или региона, макрос выводит окно сообщения и отменяет сохранение записи.</span><span class="sxs-lookup"><span data-stu-id="adeee-175">If the postal code isn't in the right format for the country/region, the macro displays a message box and cancels saving the record.</span></span> <span data-ttu-id="adeee-176">Затем выполняется возврат к элементу управления PostalCode, в котором можно исправить ошибку.</span><span class="sxs-lookup"><span data-stu-id="adeee-176">It then returns you to the PostalCode control, where you can correct the error.</span></span> <span data-ttu-id="adeee-177">Этот макрос необходимо вложить в свойство **BeforeUpdate** формы "поставщики".</span><span class="sxs-lookup"><span data-stu-id="adeee-177">This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="adeee-178">Условие</span><span class="sxs-lookup"><span data-stu-id="adeee-178">Condition</span></span></p></th>
<th><p><span data-ttu-id="adeee-179">Действие</span><span class="sxs-lookup"><span data-stu-id="adeee-179">Action</span></span></p></th>
<th><p><span data-ttu-id="adeee-180">Аргументы: Настройка</span><span class="sxs-lookup"><span data-stu-id="adeee-180">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="adeee-181">Комментарий</span><span class="sxs-lookup"><span data-stu-id="adeee-181">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adeee-182">IsNull ([страна])</span><span class="sxs-lookup"><span data-stu-id="adeee-182">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="adeee-183"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="adeee-183"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="adeee-184">Если параметру страна не присвоено <strong>значение NULL</strong>, почтовый индекс не может быть проверен.</span><span class="sxs-lookup"><span data-stu-id="adeee-184">If CountryRegion is <strong>Null</strong>, the postal code can't be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adeee-185">Ватикан В (&quot;Франция&quot;,&quot;Италия&quot;,&quot;Испания&quot;) и len ([PostalCode]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="adeee-185">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([PostalCode]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="adeee-186"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="adeee-186"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="adeee-187"><strong>Сообщение</strong>: длина почтового индекса не должна превышать 5 символов.</span><span class="sxs-lookup"><span data-stu-id="adeee-187"><strong>Message</strong>: The postal code must be 5 characters.</span></span> <span data-ttu-id="adeee-188"><strong>Гудок</strong>: <strong>естипе</strong>: <strong>Информатионтитле</strong>: ошибка почтового кода</span><span class="sxs-lookup"><span data-stu-id="adeee-188"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="adeee-189">Если почтовый индекс не имеет 5 символов, отобразится сообщение.</span><span class="sxs-lookup"><span data-stu-id="adeee-189">If the postal code isn't 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adeee-190">...</span><span class="sxs-lookup"><span data-stu-id="adeee-190"></span></span></p></td>
<td><p><span data-ttu-id="adeee-191"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="adeee-191"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="adeee-192">Отмена события.</span><span class="sxs-lookup"><span data-stu-id="adeee-192">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="adeee-193"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="adeee-193"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="adeee-194"><strong>Имя элемента управления</strong>: PostalCode</span><span class="sxs-lookup"><span data-stu-id="adeee-194"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adeee-195">Ватикан В (&quot;Австралия&quot;,&quot;Сингапур&quot;) и len ([PostalCode]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="adeee-195">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([PostalCode]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="adeee-196"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="adeee-196"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="adeee-197"><strong>Сообщение</strong>: почтовый индекс должен иметь 4 символа.</span><span class="sxs-lookup"><span data-stu-id="adeee-197"><strong>Message</strong>: The postal code must be 4 characters.</span></span> <span data-ttu-id="adeee-198"><strong>Гудок</strong>: <strong>естипе</strong>: <strong>Информатионтитле</strong>: ошибка почтового кода</span><span class="sxs-lookup"><span data-stu-id="adeee-198"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="adeee-199">Если почтовый индекс не имеет 4 символов, отобразится сообщение.</span><span class="sxs-lookup"><span data-stu-id="adeee-199">If the postal code isn't 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adeee-200">...</span><span class="sxs-lookup"><span data-stu-id="adeee-200"></span></span></p></td>
<td><p><span data-ttu-id="adeee-201"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="adeee-201"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="adeee-202">Отмена события.</span><span class="sxs-lookup"><span data-stu-id="adeee-202">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="adeee-203"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="adeee-203"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="adeee-204"><strong>Имя элемента управления</strong>: PostalCode</span><span class="sxs-lookup"><span data-stu-id="adeee-204"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adeee-205">([Страна] = &quot;Канада&quot;) And ([PostalCode], не&quot;например [A-z] [0-9] [A-z] [0-9] [A-z] [0-9&quot;])</span><span class="sxs-lookup"><span data-stu-id="adeee-205">([CountryRegion] = &quot;Canada&quot;) And ([PostalCode] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="adeee-206"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="adeee-206"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="adeee-207"><strong>Сообщение</strong>: недопустимый почтовый индекс.</span><span class="sxs-lookup"><span data-stu-id="adeee-207"><strong>Message</strong>: The postal code is not valid.</span></span> <span data-ttu-id="adeee-208">Пример кода канадского канадского: H1J 1C3 <strong>Beep</strong>: <strong>естипе</strong>: <strong>Информатионтитле</strong>: ошибка почтового кода</span><span class="sxs-lookup"><span data-stu-id="adeee-208">Example of Canadian code: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="adeee-209">Если почтовый индекс не подходит для Канады, отобразите сообщение.</span><span class="sxs-lookup"><span data-stu-id="adeee-209">If the postal code isn't correct for Canada, display a message.</span></span> <span data-ttu-id="adeee-210">(Пример канадского кода: H1J 1C3)</span><span class="sxs-lookup"><span data-stu-id="adeee-210">(Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adeee-211">...</span><span class="sxs-lookup"><span data-stu-id="adeee-211"></span></span></p></td>
<td><p><span data-ttu-id="adeee-212"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="adeee-212"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="adeee-213">Отмена события.</span><span class="sxs-lookup"><span data-stu-id="adeee-213">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

