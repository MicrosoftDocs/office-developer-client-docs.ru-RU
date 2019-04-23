---
title: Макрокоманда OpenForm
TOCTitle: OpenForm macro action
ms:assetid: c519a9d7-99d4-4765-ad96-59c3fe1be9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823095(v=office.15)
ms:contentKeyID: 48547604
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf89b61a65c11f09d5a07e52caeee5ad416c118a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288373"
---
# <a name="openform-macro-action"></a><span data-ttu-id="6be84-102">Макрокоманда OpenForm</span><span class="sxs-lookup"><span data-stu-id="6be84-102">OpenForm macro action</span></span>

<span data-ttu-id="6be84-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6be84-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6be84-104">Макрокоманда «ОткрытьФорму» ( **OpenForm** ) позволяет открыть форму в режиме формы, конструктора, просмотра или таблицы.</span><span class="sxs-lookup"><span data-stu-id="6be84-104">You can use the **OpenForm** action to open a form in Form view, Design view, Print Preview, or Datasheet view.</span></span> <span data-ttu-id="6be84-105">Он позволяет выбирать режим ввода данных и режим окна для формы, а также ограничивать количество записей, отображаемых в форме.</span><span class="sxs-lookup"><span data-stu-id="6be84-105">You can select data entry and window modes for the form and restrict the records that the form displays.</span></span>

## <a name="setting"></a><span data-ttu-id="6be84-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="6be84-106">Setting</span></span>

<span data-ttu-id="6be84-107">Макрокоманда «ОткрытьФорму» ( **OpenForm** ) использует следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="6be84-107">The **OpenForm** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6be84-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="6be84-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="6be84-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6be84-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6be84-110"><strong>Имя формы</strong></span><span class="sxs-lookup"><span data-stu-id="6be84-110"><strong>Form Name</strong></span></span></p></td>
<td><p><span data-ttu-id="6be84-111">Имя открываемой формы.</span><span class="sxs-lookup"><span data-stu-id="6be84-111">The name of the form to open.</span></span> <span data-ttu-id="6be84-112">В поле <strong>имя формы</strong> в разделе <strong>аргументы макрокоманды</strong> области построителя макросов отображаются все формы в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="6be84-112">The <strong>Form Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all forms in the current database.</span></span> <span data-ttu-id="6be84-113">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="6be84-113">This is a required argument.</span></span> <span data-ttu-id="6be84-114">При запуске макроса, содержащего макрокоманду "ОткрытьФорму" ( <strong>OpenForm</strong> ), в библиотечной базе данных Microsoft Access сначала ищет форму с этим именем в библиотечной базе данных, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="6be84-114">If you run a macro containing the <strong>OpenForm</strong> action in a library database, Microsoft Access first looks for the form with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6be84-115"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="6be84-115"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="6be84-116">Представление, в котором будет открыта форма.</span><span class="sxs-lookup"><span data-stu-id="6be84-116">The view in which the form will open.</span></span> <span data-ttu-id="6be84-117">В поле <strong>вид</strong> выберите <strong>форма</strong>, <strong>Макет</strong>, <strong></strong> <strong>Предварительный просмотр</strong>, таблица, <strong>Сводная таблица</strong>или <strong>Сводная диаграмма</strong> .</span><span class="sxs-lookup"><span data-stu-id="6be84-117">Click <strong>Form</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>Datasheet</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="6be84-118">По умолчанию используется <strong>форма</strong>.</span><span class="sxs-lookup"><span data-stu-id="6be84-118">The default is <strong>Form</strong>.</span></span></p><p><span data-ttu-id="6be84-119"><strong>Note</strong>: значение аргумента <STRONG>View</STRONG> переопределяет параметры свойства <STRONG>DefaultView</STRONG> формы и свойства <STRONG>виевсалловед</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="6be84-119"><strong>NOTE</strong>: The <STRONG>View</STRONG> argument setting overrides the settings of the form's <STRONG>DefaultView</STRONG> and <STRONG>ViewsAllowed</STRONG> properties.</span></span> <span data-ttu-id="6be84-120">Например, если для свойства формы <STRONG>виевсалловед</STRONG> задано значение <STRONG>Таблица</STRONG>, по-прежнему можно использовать макрокоманду "ОткрытьФорму" ( <STRONG>OpenForm</STRONG> ), чтобы открыть форму в представлении формы.</span><span class="sxs-lookup"><span data-stu-id="6be84-120">For example, if a form's <STRONG>ViewsAllowed</STRONG> property is set to <STRONG>Datasheet</STRONG>, you can still use the <STRONG>OpenForm</STRONG> action to open the form in Form view.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6be84-121"><strong>Имя фильтра</strong></span><span class="sxs-lookup"><span data-stu-id="6be84-121"><strong>Filter Name</strong></span></span></p></td>
<td><p><span data-ttu-id="6be84-122">Фильтр, который запрещает или сортирует записи формы.</span><span class="sxs-lookup"><span data-stu-id="6be84-122">A filter that restricts or sorts the form's records.</span></span> <span data-ttu-id="6be84-123">Можно ввести имя существующего запроса или фильтра, сохраненного в виде запроса.</span><span class="sxs-lookup"><span data-stu-id="6be84-123">You can enter the name of either an existing query or a filter that was saved as a query.</span></span> <span data-ttu-id="6be84-124">Однако запрос должен включать все поля в форме, которые вы открываете, или задать для свойства <strong>OutputAllFields</strong> значение <strong>"Да"</strong>.</span><span class="sxs-lookup"><span data-stu-id="6be84-124">However, the query must include all the fields in the form you are opening or have its <strong>OutputAllFields</strong> property set to <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6be84-125"><strong>Условие отбора</strong></span><span class="sxs-lookup"><span data-stu-id="6be84-125"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="6be84-126">Допустимое предложение WHERE (без слова WHERE) или выражение, которое Access использует для выбора записей из базовой таблицы или запроса формы.</span><span class="sxs-lookup"><span data-stu-id="6be84-126">A valid SQL WHERE clause (without the word WHERE) or expression that Access uses to select records from the form's underlying table or query.</span></span> <span data-ttu-id="6be84-127">Если выбран фильтр с аргументом <strong>имя фильтра</strong> , Access применяет это предложение WHERE к результатам фильтра.</span><span class="sxs-lookup"><span data-stu-id="6be84-127">If you select a filter with the <strong>Filter Name</strong> argument, Access applies this WHERE clause to the results of the filter.</span></span> <span data-ttu-id="6be84-128">Чтобы открыть форму и ограничить записи записями, указанными в значении элемента управления в другой форме, используйте следующее выражение: <strong>[</strong><em>fieldname</em><strong>] = Forms! [</strong> <em>FormName</em> <strong>]! [</strong><em>контролнаме в другой форме</em><strong>]</strong> замените <em>fieldname</em> именем поля в базовой таблице или запросе формы, которую нужно открыть.</span><span class="sxs-lookup"><span data-stu-id="6be84-128">To open a form and restrict its records to those specified by the value of a control on another form, use the following expression: <strong>[</strong><em>fieldname</em><strong>] = Forms![</strong><em>formname</em><strong>]![</strong><em>controlname on other form</em><strong>]</strong> Replace <em>fieldname</em> with the name of a field in the underlying table or query of the form you want to open.</span></span> <span data-ttu-id="6be84-129">Замените <em>FormName</em> и <em>контролнаме в другой форме</em> , указав имя другой формы и элемент управления в другой форме, который содержит значение, в котором будут сопоставлены записи в первой форме.</span><span class="sxs-lookup"><span data-stu-id="6be84-129">Replace <em>formname</em> and <em>controlname on other form</em> with the name of the other form and the control on the other form that contains the value you want records in the first form to match.</span></span></p><p><span data-ttu-id="6be84-130"><strong>Note</strong>: максимальная длина аргумента <STRONG>условия WHERE</STRONG> — 255 символов.</span><span class="sxs-lookup"><span data-stu-id="6be84-130"><strong>NOTE</strong>: The maximum length of the <STRONG>Where Condition</STRONG> argument is 255 characters.</span></span> <span data-ttu-id="6be84-131">Если необходимо ввести более сложное предложение WHERE SQL, более длинное, используйте метод <STRONG>OpenForm</STRONG> объекта DoCmd в <STRONG></STRONG> модуле Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="6be84-131">If you need to enter a more complex SQL WHERE clause longer than this, use the <STRONG>OpenForm</STRONG> method of the <STRONG>DoCmd</STRONG> object in a Visual Basic for Applications (VBA) module instead.</span></span> <span data-ttu-id="6be84-132">Вы можете ввести инструкции SQL WHERE, содержащие до 32 768 символов в VBA.</span><span class="sxs-lookup"><span data-stu-id="6be84-132">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6be84-133"><strong>Режим данных</strong></span><span class="sxs-lookup"><span data-stu-id="6be84-133"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="6be84-134">Режим ввода данных для формы.</span><span class="sxs-lookup"><span data-stu-id="6be84-134">The data entry mode for the form.</span></span> <span data-ttu-id="6be84-135">Это относится только к формам, открываемым в режиме формы или режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="6be84-135">This applies only to forms opened in Form view or Datasheet view.</span></span> <span data-ttu-id="6be84-136">Нажмите кнопку <strong>Добавить</strong> (пользователь может добавлять новые записи, но не может изменять существующие), <strong>изменять</strong> (пользователь может изменять существующие записи и добавлять новые записи) или <strong>только для чтения</strong> (пользователи могут только просматривать записи).</span><span class="sxs-lookup"><span data-stu-id="6be84-136">Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="6be84-137">Значение по умолчанию — <strong>Edit</strong>.</span><span class="sxs-lookup"><span data-stu-id="6be84-137">The default is <strong>Edit</strong>.</span></span> <span data-ttu-id="6be84-138"><strong>Notes</strong></span><span class="sxs-lookup"><span data-stu-id="6be84-138"><strong>Notes</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="6be84-139">Параметр <strong>режим данных</strong> в аргументе переопределяет параметры свойств <strong>AllowEdits</strong>, <strong>алловделетионс</strong>, <strong>алловаддитионс</strong>и <strong>DataEntry</strong> формы.</span><span class="sxs-lookup"><span data-stu-id="6be84-139">The <strong>Data Mode</strong> argument setting overrides the settings of the form's <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>, and <strong>DataEntry</strong> properties.</span></span> <span data-ttu-id="6be84-140">Например, если свойству <strong>AllowEdits</strong> формы присвоено значение <strong>нет</strong>, вы по-прежнему можете открыть форму в режиме редактирования с помощью макрокоманды "ОткрытьФорму" ( <strong>OpenForm</strong> ).</span><span class="sxs-lookup"><span data-stu-id="6be84-140">For example, if a form's <strong>AllowEdits</strong> property is set to <strong>No</strong>, you can still use the <strong>OpenForm</strong> action to open the form in Edit mode.</span></span></p></li>
<li><p><span data-ttu-id="6be84-141">Если оставить этот аргумент пустым, Access открывает форму в режиме ввода данных, заданном в свойствах <strong>AllowEdits</strong>, <strong>алловделетионс</strong>, <strong>алловаддитионс</strong>и <strong>DataEntry</strong> формы.</span><span class="sxs-lookup"><span data-stu-id="6be84-141">If you leave this argument blank, Access opens the form in the data entry mode set by the form's <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>, and <strong>DataEntry</strong> properties.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6be84-142"><strong>Режим окна</strong></span><span class="sxs-lookup"><span data-stu-id="6be84-142"><strong>Window Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="6be84-143">Режим окна, в котором открывается форма.</span><span class="sxs-lookup"><span data-stu-id="6be84-143">The window mode in which the form opens.</span></span> <span data-ttu-id="6be84-144">Нажмите кнопку <strong>обычный</strong> (форма открывается в режиме, заданном его свойствами), <strong>скрыто</strong> (форма скрыта), <strong>значок</strong> (форма открывается в свернутом виде в нижней части экрана) или диалоговое <strong>окно</strong> ( <strong>модальное</strong> и всплывающее окно формы <strong> </strong>для свойств задано значение <strong>"Да"</strong>).</span><span class="sxs-lookup"><span data-stu-id="6be84-144">Click <strong>Normal</strong> (the form opens in the mode set by its properties), <strong>Hidden</strong> (the form is hidden), <strong>Icon</strong> (the form opens minimized as a small title bar at the bottom of the screen), or <strong>Dialog</strong> (the form's <strong>Modal</strong> and <strong>PopUp</strong> properties are set to <strong>Yes</strong>).</span></span> <span data-ttu-id="6be84-145">Значение по умолчанию — <strong>Normal</strong>.</span><span class="sxs-lookup"><span data-stu-id="6be84-145">The default is <strong>Normal</strong>.</span></span></p><p><span data-ttu-id="6be84-146"><strong>Note</strong>: некоторые параметры аргументов <STRONG>режима окна</STRONG> не применяются при использовании документов с вкладками.</span><span class="sxs-lookup"><span data-stu-id="6be84-146"><strong>NOTE</strong>: Some <STRONG>Window Mode</STRONG> argument settings do not apply when using tabbed documents.</span></span> <span data-ttu-id="6be84-147">Чтобы переключиться на перекрывающиеся окна:</span><span class="sxs-lookup"><span data-stu-id="6be84-147">To switch to overlapping windows:</span></span></p>
<ol>
<li><p><span data-ttu-id="6be84-148">Перейдите на вкладку файл и нажмите кнопку <strong>Параметры</strong>.</span><span class="sxs-lookup"><span data-stu-id="6be84-148">Click the File tab and then click <strong>Options</strong>.</span></span></p></li>
<li><p><span data-ttu-id="6be84-149">В диалоговом окне " <strong>Параметры Access</strong> " щелкните <strong>Текущая база данных</strong>.</span><span class="sxs-lookup"><span data-stu-id="6be84-149">In the <strong>Access Options</strong> dialog box, click <strong>Current Database</strong>.</span></span></p></li>
<li><p><span data-ttu-id="6be84-150">В разделе Параметры <strong>приложения</strong>в разделе <strong>Параметры окна документа</strong>щелкните перекрывающиеся <strong>окна</strong>.</span><span class="sxs-lookup"><span data-stu-id="6be84-150">In the <strong>Application Options</strong>section, under <strong>Document Window Options</strong>, click <strong>Overlapping Windows</strong>.</span></span></p></li>
<li><p><span data-ttu-id="6be84-151">Нажмите кнопку <strong>ОК</strong>, а затем закройте и снова откройте базу данных.</span><span class="sxs-lookup"><span data-stu-id="6be84-151">Click <strong>OK</strong>, then close and reopen the database.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6be84-152">Замечания</span><span class="sxs-lookup"><span data-stu-id="6be84-152">Remarks</span></span>

<span data-ttu-id="6be84-153">Это действие аналогично двойному щелчку формы в области навигации или щелчку правой кнопкой мыши формы в области навигации и последующему выбору представления.</span><span class="sxs-lookup"><span data-stu-id="6be84-153">This action is similar to double-clicking a form in the Navigation Pane, or right-clicking the form in the Navigation Pane and then selecting a view.</span></span>

<span data-ttu-id="6be84-154">Форма может быть модальной (ее необходимо закрыть или скрыть до того, как пользователь сможет выполнять какие-либо другие действия) или немодальные (пользователь может перемещаться в другие окна, пока форма открыта).</span><span class="sxs-lookup"><span data-stu-id="6be84-154">A form can be modal (it must be closed or hidden before the user can perform any other action) or modeless (the user can move to other windows while the form is open).</span></span> <span data-ttu-id="6be84-155">Это также может быть всплывающая форма (форма, используемая для сбора и отображения информации, которая остается в верхней части всех остальных окон Access).</span><span class="sxs-lookup"><span data-stu-id="6be84-155">It can also be a pop-up form (a form used to collect or display information that remains on top of all other Access windows).</span></span> <span data-ttu-id="6be84-156">Свойства модальных \*\*\*\* и **всплывающих окон** задаются при разработке формы.</span><span class="sxs-lookup"><span data-stu-id="6be84-156">You set the **Modal** and **PopUp** properties when you design the form.</span></span> <span data-ttu-id="6be84-157">Если вы используете параметр **Normal** для аргумента **Window Mode** , форма откроется в режиме, определяемом параметрами этих свойств.</span><span class="sxs-lookup"><span data-stu-id="6be84-157">If you use **Normal** for the **Window Mode** argument, the form opens in the mode specified by these property settings.</span></span> <span data-ttu-id="6be84-158">Если вы используете **диалоговОе окно** для аргумента **mode Window** , для обоих свойств устанавливается значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="6be84-158">If you use **Dialog** for the **Window Mode** argument, these properties are both set to **Yes**.</span></span> <span data-ttu-id="6be84-159">Форма, открытая как скрытая или как значок, возвращается в режим, заданный параметрами его свойства при его отображении или восстановлении.</span><span class="sxs-lookup"><span data-stu-id="6be84-159">A form opened as hidden or as an icon returns to the mode specified by its property settings when you show or restore it.</span></span>

<span data-ttu-id="6be84-160">Когда вы открываете форму с диалоговым окном аргумента \*\*\*\* **режим окна** , Access приостанавливает макрос до тех пор, пока форма не будет закрыта или скрыта.</span><span class="sxs-lookup"><span data-stu-id="6be84-160">When you open a form with the **Window Mode** argument set to **Dialog**, Access suspends the macro until the form is closed or hidden.</span></span> <span data-ttu-id="6be84-161">Вы можете скрыть форму, задав для ее свойства **Visible** значение **нет** , используя действие **SetValue** .</span><span class="sxs-lookup"><span data-stu-id="6be84-161">You can hide a form by setting its **Visible** property to **No** by using the **SetValue** action.</span></span>

> [!TIP]
> <span data-ttu-id="6be84-162">Вы можете выбрать форму в области навигации и перетащить ее в строку макрокоманды.</span><span class="sxs-lookup"><span data-stu-id="6be84-162">You can select a form in the Navigation Pane and drag it to a macro action row.</span></span> <span data-ttu-id="6be84-163">При этом автоматически создается макрокоманда "ОткрытьФорму" ( **OpenForm** ), которая открывает форму в режиме формы.</span><span class="sxs-lookup"><span data-stu-id="6be84-163">This automatically creates an **OpenForm** action that opens the form in Form view.</span></span>

<span data-ttu-id="6be84-164">Фильтр и условие, где вы хотите применить, становятся значением свойства **Filter** формы.</span><span class="sxs-lookup"><span data-stu-id="6be84-164">The filter and WHERE condition you apply become the setting of the form's **Filter** property.</span></span>

## <a name="examples"></a><span data-ttu-id="6be84-165">Примеры</span><span class="sxs-lookup"><span data-stu-id="6be84-165">Examples</span></span>

<span data-ttu-id="6be84-166">**Задание значения элемента управления с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="6be84-166">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="6be84-167">Следующий макрос открывает форму "Добавление продуктов" на кнопке в форме "поставщики".</span><span class="sxs-lookup"><span data-stu-id="6be84-167">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="6be84-168">В нем показано использование действий **echo**, **клосевиндов**, **OpenForm**, **SetValue**и **КЭлементуУправления** .</span><span class="sxs-lookup"><span data-stu-id="6be84-168">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="6be84-169">Действие **SetValue** устанавливает для элемента управления "идентификатор поставщика" в форме "продукты" текущего поставщика в форме "поставщики".</span><span class="sxs-lookup"><span data-stu-id="6be84-169">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="6be84-170">После этого действие " **КЭлементуУправления** " переместит фокус на поле "идентификатор категории", в котором можно начать ввод данных для нового продукта.</span><span class="sxs-lookup"><span data-stu-id="6be84-170">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="6be84-171">Этот макрос должен быть присоединен к кнопке "добавить продукты" в форме "поставщики".</span><span class="sxs-lookup"><span data-stu-id="6be84-171">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6be84-172">Действие</span><span class="sxs-lookup"><span data-stu-id="6be84-172">Action</span></span></p></th>
<th><p><span data-ttu-id="6be84-173">Аргументы: Настройка</span><span class="sxs-lookup"><span data-stu-id="6be84-173">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="6be84-174">Комментарий</span><span class="sxs-lookup"><span data-stu-id="6be84-174">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6be84-175"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="6be84-175"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="6be84-176"><strong>Echo on</strong>: <strong>нет</strong></span><span class="sxs-lookup"><span data-stu-id="6be84-176"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="6be84-177">Остановить обновление экрана во время выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="6be84-177">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6be84-178"><strong>Клосевиндов</strong></span><span class="sxs-lookup"><span data-stu-id="6be84-178"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="6be84-179"><strong>Тип объекта</strong>: <strong>Формобжект Name</strong>: List Product <strong>Save</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="6be84-179"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="6be84-180">Закройте форму "список товаров".</span><span class="sxs-lookup"><span data-stu-id="6be84-180">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6be84-181"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="6be84-181"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="6be84-182"><strong>Имя формы</strong>: " <strong>Просмотр</strong>продуктов: <strong>режим формдата</strong>: режим <strong>аддвиндов</strong>: <strong>обычный</strong> "</span><span class="sxs-lookup"><span data-stu-id="6be84-182"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="6be84-183">Откройте форму продукты.</span><span class="sxs-lookup"><span data-stu-id="6be84-183">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6be84-184"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="6be84-184"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="6be84-185"><strong>Элемент</strong>: [Forms]! [Products]! Ключев <strong>Выражение</strong>: КодПоставщика</span><span class="sxs-lookup"><span data-stu-id="6be84-185"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="6be84-186">В форме Поставщики задайте для элемента управления "идентификатор поставщика" текущего поставщика.</span><span class="sxs-lookup"><span data-stu-id="6be84-186">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6be84-187"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="6be84-187"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="6be84-188"><strong>Имя элемента управления</strong>: КодТипа</span><span class="sxs-lookup"><span data-stu-id="6be84-188"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="6be84-189">Перейдите к элементу управления ИДЕНТИФИКАТОРом категории.</span><span class="sxs-lookup"><span data-stu-id="6be84-189">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6be84-190">Следующий макрос открывает форму списка товаров в правом нижнем углу формы поставщики, в которой отображаются продукты текущего поставщика.</span><span class="sxs-lookup"><span data-stu-id="6be84-190">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="6be84-191">В нем показано использование действий **echo**, **MessageBox**, **КЭлементуУправления**, **Макрокоманда StopMacro**, **OpenForm**и **мовеандсизевиндов** .</span><span class="sxs-lookup"><span data-stu-id="6be84-191">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="6be84-192">В нем также показано использование условного выражения с действиями **MessageBox**, **КЭлементуУправления**и **Макрокоманда StopMacro** .</span><span class="sxs-lookup"><span data-stu-id="6be84-192">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="6be84-193">Этот макрос необходимо прикрепить к кнопке "проверить продукты" в форме "поставщики".</span><span class="sxs-lookup"><span data-stu-id="6be84-193">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<span data-ttu-id="6be84-194">**Синхронизация форм с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="6be84-194">**Synchronize forms by using a macro**</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6be84-195">Условие</span><span class="sxs-lookup"><span data-stu-id="6be84-195">Condition</span></span></p></th>
<th><p><span data-ttu-id="6be84-196">Действие</span><span class="sxs-lookup"><span data-stu-id="6be84-196">Action</span></span></p></th>
<th><p><span data-ttu-id="6be84-197">Аргументы: Настройка</span><span class="sxs-lookup"><span data-stu-id="6be84-197">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="6be84-198">Комментарий</span><span class="sxs-lookup"><span data-stu-id="6be84-198">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="6be84-199"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="6be84-199"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="6be84-200"><strong>Echo on</strong>: <strong>нет</strong></span><span class="sxs-lookup"><span data-stu-id="6be84-200"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="6be84-201">Остановить обновление экрана во время выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="6be84-201">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6be84-202">IsNull ([КодПоставщика])</span><span class="sxs-lookup"><span data-stu-id="6be84-202">IsNull([SupplierID])</span></span></p></td>
<td><p><span data-ttu-id="6be84-203"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="6be84-203"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="6be84-204"><strong>Сообщение</strong>: перейдите к записи поставщика, продукты которой вы хотите просмотреть, а затем снова нажмите кнопку Просмотр продуктов.</span><span class="sxs-lookup"><span data-stu-id="6be84-204"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="6be84-205"><strong>Beep</strong>: <strong>естипе</strong>: <strong>нонетитле</strong>: выберите поставщика</span><span class="sxs-lookup"><span data-stu-id="6be84-205"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="6be84-206">Если в форме Поставщики нет текущего поставщика, отобразите сообщение.</span><span class="sxs-lookup"><span data-stu-id="6be84-206">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6be84-207">...</span><span class="sxs-lookup"><span data-stu-id="6be84-207"></span></span></p></td>
<td><p><span data-ttu-id="6be84-208"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="6be84-208"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="6be84-209"><strong>Имя элемента управления</strong>: CompanyName</span><span class="sxs-lookup"><span data-stu-id="6be84-209"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="6be84-210">Перемещение фокуса на элемент управления CompanyName.</span><span class="sxs-lookup"><span data-stu-id="6be84-210">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6be84-211">...</span><span class="sxs-lookup"><span data-stu-id="6be84-211"></span></span></p></td>
<td><p><span data-ttu-id="6be84-212"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="6be84-212"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6be84-213">Остановка макроса.</span><span class="sxs-lookup"><span data-stu-id="6be84-213">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="6be84-214"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="6be84-214"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="6be84-215"><strong>Имя формы</strong>: <strong>представление</strong>списка продуктов: <strong>даташитфилтер Name</strong>: <strong>WHERE Condition</strong>: [КодПоставщика] = [Forms]! [Поставщики]! Ключев <strong>Режим данных</strong>: <strong>режим чтения онливиндов</strong>: <strong>обычный</strong></span><span class="sxs-lookup"><span data-stu-id="6be84-215"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [SupplierID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="6be84-216">Откройте форму Список продуктов и отобразите текущие продукты поставщика.</span><span class="sxs-lookup"><span data-stu-id="6be84-216">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="6be84-217"><strong>Мовеандсизевиндов</strong></span><span class="sxs-lookup"><span data-stu-id="6be84-217"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="6be84-218"><strong>Right</strong>: 0,7799&quot; <strong>вниз</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="6be84-218"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="6be84-219">РасПоложите форму списка товаров в правом нижнем углу формы Поставщики.</span><span class="sxs-lookup"><span data-stu-id="6be84-219">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

