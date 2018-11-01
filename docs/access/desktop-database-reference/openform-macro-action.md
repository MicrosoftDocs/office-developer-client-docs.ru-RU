---
title: Действия ОткрытьФорму макроса
TOCTitle: OpenForm Macro Action
ms:assetid: c519a9d7-99d4-4765-ad96-59c3fe1be9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823095(v=office.15)
ms:contentKeyID: 48547604
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 140ac927089a89fa5c77034c9e33d4cd1519e41c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870263"
---
# <a name="openform-macro-action"></a><span data-ttu-id="1220b-102">Действия ОткрытьФорму макроса</span><span class="sxs-lookup"><span data-stu-id="1220b-102">OpenForm Macro Action</span></span>


<span data-ttu-id="1220b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1220b-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="1220b-104">**ОткрытьФорму** можно использовать для открытия формы в режиме формы, режиме конструктора, предварительный или представление таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="1220b-104">You can use the **OpenForm** action to open a form in Form view, Design view, Print Preview, or Datasheet view.</span></span> <span data-ttu-id="1220b-105">Можно выбрать режимы запись и окно данных для формы и ограничить записи, которые отображаются в форме.</span><span class="sxs-lookup"><span data-stu-id="1220b-105">You can select data entry and window modes for the form and restrict the records that the form displays.</span></span>

## <a name="setting"></a><span data-ttu-id="1220b-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="1220b-106">Setting</span></span>

<span data-ttu-id="1220b-107">**ОткрытьФорму** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="1220b-107">The **OpenForm** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1220b-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="1220b-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="1220b-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1220b-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1220b-110"><strong>Имя формы</strong></span><span class="sxs-lookup"><span data-stu-id="1220b-110"><strong>Form Name</strong></span></span></p></td>
<td><p><span data-ttu-id="1220b-111">Имя формы для ее открытия.</span><span class="sxs-lookup"><span data-stu-id="1220b-111">The name of the form to open.</span></span> <span data-ttu-id="1220b-112">В поле <strong>Имя формы</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов показывает все формы в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="1220b-112">The <strong>Form Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all forms in the current database.</span></span> <span data-ttu-id="1220b-113">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="1220b-113">This is a required argument.</span></span> <span data-ttu-id="1220b-114">Если макрос, содержащий <strong>ОткрытьФорму в базе данных библиотеки</strong> , Microsoft Access сначала выполняет поиск формы с указанным именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="1220b-114">If you run a macro containing the <strong>OpenForm</strong> action in a library database, Microsoft Access first looks for the form with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1220b-115"><strong>Просмотр</strong></span><span class="sxs-lookup"><span data-stu-id="1220b-115"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="1220b-116">Представление, в котором будет открыта форма.</span><span class="sxs-lookup"><span data-stu-id="1220b-116">The view in which the form will open.</span></span> <span data-ttu-id="1220b-117">Выберите <strong>формы</strong>, <strong>разработки</strong>, <strong>Режим предварительного просмотра</strong>, <strong>таблицы</strong>, <strong>сводной таблицы</strong>или <strong>сводной диаграммы</strong> в поле <strong>View</strong> .</span><span class="sxs-lookup"><span data-stu-id="1220b-117">Click <strong>Form</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>Datasheet</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="1220b-118">Значение по умолчанию — <strong>формы</strong>.</span><span class="sxs-lookup"><span data-stu-id="1220b-118">The default is <strong>Form</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="1220b-119">Аргумент <STRONG>представления</STRONG> переопределяет параметры свойств <STRONG>режим по умолчанию</STRONG> и <STRONG>Допустимые режимы</STRONG> формы.</span><span class="sxs-lookup"><span data-stu-id="1220b-119">The <STRONG>View</STRONG> argument setting overrides the settings of the form's <STRONG>DefaultView</STRONG> and <STRONG>ViewsAllowed</STRONG> properties.</span></span> <span data-ttu-id="1220b-120">Например если свойство <STRONG>Допустимые режимы</STRONG> формы задано для <STRONG>таблицы данных</STRONG>, по-прежнему можно использовать <STRONG>ОткрытьФорму</STRONG> для открытия формы в режиме формы.</span><span class="sxs-lookup"><span data-stu-id="1220b-120">For example, if a form's <STRONG>ViewsAllowed</STRONG> property is set to <STRONG>Datasheet</STRONG>, you can still use the <STRONG>OpenForm</STRONG> action to open the form in Form view.</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1220b-121"><strong>Имя фильтра</strong></span><span class="sxs-lookup"><span data-stu-id="1220b-121"><strong>Filter Name</strong></span></span></p></td>
<td><p><span data-ttu-id="1220b-122">Фильтр, который ограничивает и сортировки записей формы.</span><span class="sxs-lookup"><span data-stu-id="1220b-122">A filter that restricts or sorts the form's records.</span></span> <span data-ttu-id="1220b-123">Можно ввести имя существующего запроса или фильтр, который был сохранен в виде запроса.</span><span class="sxs-lookup"><span data-stu-id="1220b-123">You can enter the name of either an existing query or a filter that was saved as a query.</span></span> <span data-ttu-id="1220b-124">Тем не менее запрос необходимо включить все поля в форме открытия или свойству <strong>Вывод всех полей</strong> , значение <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="1220b-124">However, the query must include all the fields in the form you are opening or have its <strong>OutputAllFields</strong> property set to <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1220b-125"><strong>Условие отбора</strong></span><span class="sxs-lookup"><span data-stu-id="1220b-125"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="1220b-126">Оператор SQL WHERE (без слова ГДЕ) или выражение, которое следует использовать для выбора записей из формы базовым таблицы или запроса.</span><span class="sxs-lookup"><span data-stu-id="1220b-126">A valid SQL WHERE clause (without the word WHERE) or expression that Access uses to select records from the form's underlying table or query.</span></span> <span data-ttu-id="1220b-127">Если выбран параметр аргумента <strong>Имя фильтра</strong> , доступа применяется это предложение WHERE к фильтру.</span><span class="sxs-lookup"><span data-stu-id="1220b-127">If you select a filter with the <strong>Filter Name</strong> argument, Access applies this WHERE clause to the results of the filter.</span></span> <span data-ttu-id="1220b-128">Для открытия формы и отобрать те указанное значение элемента управления на другой формы ее записи, используйте следующее выражение: <strong>[</strong><em>fieldname</em><strong>] = Forms! [</strong> <em>имя_формы</em> <strong>]! [</strong><em>имяЭлементаВДругойФорме</em><strong>]</strong> <em>fieldname</em> замените имя поля в базовой таблице или запросе формы, который необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="1220b-128">To open a form and restrict its records to those specified by the value of a control on another form, use the following expression: <strong>[</strong><em>fieldname</em><strong>] = Forms![</strong><em>formname</em><strong>]![</strong><em>controlname on other form</em><strong>]</strong> Replace <em>fieldname</em> with the name of a field in the underlying table or query of the form you want to open.</span></span> <span data-ttu-id="1220b-129">Замените имя другой формы и элемента управления в форме, которая содержит значение записей в первую форму в соответствии с <em>имя_формы</em> и <em>имяЭлементаВДругойФорме</em> .</span><span class="sxs-lookup"><span data-stu-id="1220b-129">Replace <em>formname</em> and <em>controlname on other form</em> with the name of the other form and the control on the other form that contains the value you want records in the first form to match.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="1220b-130">Максимальная длина аргумента <STRONG>Условие</STRONG> составляет 255 знаков.</span><span class="sxs-lookup"><span data-stu-id="1220b-130">The maximum length of the <STRONG>Where Condition</STRONG> argument is 255 characters.</span></span> <span data-ttu-id="1220b-131">Если необходимо ввести более сложных SQL предложение WHERE большее используйте метод <STRONG>ОткрытьФорму</STRONG> <STRONG>объекта</STRONG> в Visual Basic для приложений (VBA) модуля.</span><span class="sxs-lookup"><span data-stu-id="1220b-131">If you need to enter a more complex SQL WHERE clause longer than this, use the <STRONG>OpenForm</STRONG> method of the <STRONG>DoCmd</STRONG> object in a Visual Basic for Applications (VBA) module instead.</span></span> <span data-ttu-id="1220b-132">Можно ввести предложение инструкции SQL до 32 768 знаков в VBA.</span><span class="sxs-lookup"><span data-stu-id="1220b-132">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1220b-133"><strong>Режим данных</strong></span><span class="sxs-lookup"><span data-stu-id="1220b-133"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="1220b-134">Режим ввода данных для формы.</span><span class="sxs-lookup"><span data-stu-id="1220b-134">The data entry mode for the form.</span></span> <span data-ttu-id="1220b-135">Это относится только к формах, открытых в режиме формы или таблицы.</span><span class="sxs-lookup"><span data-stu-id="1220b-135">This applies only to forms opened in Form view or Datasheet view.</span></span> <span data-ttu-id="1220b-136">Нажмите кнопку <strong>Add</strong> (пользователь может добавлять новые записи, но не могут изменять существующие записи), <strong>Изменение</strong> (пользователь может изменять существующие записи и добавление новых записей), или <strong>Только для чтения</strong> (пользователь может только просматривать записи).</span><span class="sxs-lookup"><span data-stu-id="1220b-136">Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="1220b-137">Значение по умолчанию — <strong>Изменить</strong>.</span><span class="sxs-lookup"><span data-stu-id="1220b-137">The default is <strong>Edit</strong>.</span></span> <span data-ttu-id="1220b-138"><strong>Примечания</strong></span><span class="sxs-lookup"><span data-stu-id="1220b-138"><strong>Notes</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="1220b-139">Аргумент <strong>Режим данных</strong> переопределяет параметры свойств <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>и <strong>DataEntry</strong> формы.</span><span class="sxs-lookup"><span data-stu-id="1220b-139">The <strong>Data Mode</strong> argument setting overrides the settings of the form's <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>, and <strong>DataEntry</strong> properties.</span></span> <span data-ttu-id="1220b-140">Например если свойство <strong>AllowEdits</strong> формы задано значение <strong>No</strong>, по-прежнему можно использовать <strong>ОткрытьФорму</strong> для открытия формы в режиме редактирования.</span><span class="sxs-lookup"><span data-stu-id="1220b-140">For example, if a form's <strong>AllowEdits</strong> property is set to <strong>No</strong>, you can still use the <strong>OpenForm</strong> action to open the form in Edit mode.</span></span></p></li>
<li><p><span data-ttu-id="1220b-141">Если оставить этот аргумент пустым, форма будет открыта в режиме ввода данных, от <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>и <strong>DataEntry</strong> свойств формы.</span><span class="sxs-lookup"><span data-stu-id="1220b-141">If you leave this argument blank, Access opens the form in the data entry mode set by the form's <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>, and <strong>DataEntry</strong> properties.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1220b-142"><strong>Режим окна</strong></span><span class="sxs-lookup"><span data-stu-id="1220b-142"><strong>Window Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="1220b-143">Режим окна, в котором открывается форма.</span><span class="sxs-lookup"><span data-stu-id="1220b-143">The window mode in which the form opens.</span></span> <span data-ttu-id="1220b-144">Нажмите кнопку <strong>Normal</strong> (форма открывается в режиме, от его свойств), <strong>Hidden</strong> (форма скрыта), <strong>значок</strong> (свернутом виде малого заголовка в нижней части экрана откроется форма), или <strong>диалоговое окно</strong> ( <strong>модальные окна</strong> и формы <strong>контекстного меню </strong>задано значение <strong>Да</strong>).</span><span class="sxs-lookup"><span data-stu-id="1220b-144">Click <strong>Normal</strong> (the form opens in the mode set by its properties), <strong>Hidden</strong> (the form is hidden), <strong>Icon</strong> (the form opens minimized as a small title bar at the bottom of the screen), or <strong>Dialog</strong> (the form's <strong>Modal</strong> and <strong>PopUp</strong> properties are set to <strong>Yes</strong>).</span></span> <span data-ttu-id="1220b-145">Значение по умолчанию — <strong>Normal</strong>.</span><span class="sxs-lookup"><span data-stu-id="1220b-145">The default is <strong>Normal</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="1220b-146">Некоторые параметры аргумент <STRONG>Режим окна</STRONG> не применяются при использовании документов с вкладками.</span><span class="sxs-lookup"><span data-stu-id="1220b-146">Some <STRONG>Window Mode</STRONG> argument settings do not apply when using tabbed documents.</span></span> <span data-ttu-id="1220b-147">Чтобы переключиться на перекрывающиеся windows:</span><span class="sxs-lookup"><span data-stu-id="1220b-147">To switch to overlapping windows:</span></span></P>


<p></p>
<ol>
<li><p><span data-ttu-id="1220b-148">Перейдите на вкладку файл и нажмите кнопку <strong>Параметры</strong>.</span><span class="sxs-lookup"><span data-stu-id="1220b-148">Click the File tab and then click <strong>Options</strong>.</span></span></p></li>
<li><p><span data-ttu-id="1220b-149">В диалоговом окне <strong>Параметры доступа</strong> щелкните <strong>Текущей базы данных</strong>.</span><span class="sxs-lookup"><span data-stu-id="1220b-149">In the <strong>Access Options</strong> dialog box, click <strong>Current Database</strong>.</span></span></p></li>
<li><p><span data-ttu-id="1220b-150">В разделе <strong>Параметры приложения</strong>в разделе <strong>Параметры окна документа</strong>нажмите кнопку <strong>Перекрывающиеся Windows</strong>.</span><span class="sxs-lookup"><span data-stu-id="1220b-150">In the <strong>Application Options</strong>section, under <strong>Document Window Options</strong>, click <strong>Overlapping Windows</strong>.</span></span></p></li>
<li><p><span data-ttu-id="1220b-151">Нажмите кнопку <strong>ОК</strong>, а затем закройте и снова откройте базу данных.</span><span class="sxs-lookup"><span data-stu-id="1220b-151">Click <strong>OK</strong>, then close and reopen the database.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1220b-152">Замечания</span><span class="sxs-lookup"><span data-stu-id="1220b-152">Remarks</span></span>

<span data-ttu-id="1220b-153">Это действие аналогично дважды щелкнув формы в области навигации или щелкнув правой кнопкой мыши форму в области навигации, а затем выбрав представления.</span><span class="sxs-lookup"><span data-stu-id="1220b-153">This action is similar to double-clicking a form in the Navigation Pane, or right-clicking the form in the Navigation Pane and then selecting a view.</span></span>

<span data-ttu-id="1220b-154">Форма может быть модальные окна (его необходимо быть закрыт или скрытым, прежде чем пользователь может выполнять любые другие действия) или немодальной (пользователь может перейти в другое время, пока открыта форма).</span><span class="sxs-lookup"><span data-stu-id="1220b-154">A form can be modal (it must be closed or hidden before the user can perform any other action) or modeless (the user can move to other windows while the form is open).</span></span> <span data-ttu-id="1220b-155">Он также может быть как всплывающая форма (форма, используемая для сбора или отображение сведений остается поверх других окон Access).</span><span class="sxs-lookup"><span data-stu-id="1220b-155">It can also be a pop-up form (a form used to collect or display information that remains on top of all other Access windows).</span></span> <span data-ttu-id="1220b-156">**Модальное** **всплывающее** окно задать при разработке формы.</span><span class="sxs-lookup"><span data-stu-id="1220b-156">You set the **Modal** and **PopUp** properties when you design the form.</span></span> <span data-ttu-id="1220b-157">Если вы используете **Normal** для аргумента **Режим окна** , форма открывается в режиме, указанного идентификатором эти параметры свойств.</span><span class="sxs-lookup"><span data-stu-id="1220b-157">If you use **Normal** for the **Window Mode** argument, the form opens in the mode specified by these property settings.</span></span> <span data-ttu-id="1220b-158">Если вы используете **диалоговое окно** для аргумента **Режим окна** , эти свойства задаются значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="1220b-158">If you use **Dialog** for the **Window Mode** argument, these properties are both set to **Yes**.</span></span> <span data-ttu-id="1220b-159">Возвращает формы, открывается как скрытый или значка для режима, указанного с его параметры свойств, когда экран или восстановлении.</span><span class="sxs-lookup"><span data-stu-id="1220b-159">A form opened as hidden or as an icon returns to the mode specified by its property settings when you show or restore it.</span></span>

<span data-ttu-id="1220b-160">При открытии формы с аргументом **Режим окна** , задайте значение **диалоговое окно**макроса приостанавливается до закрытия формы или скрытым.</span><span class="sxs-lookup"><span data-stu-id="1220b-160">When you open a form with the **Window Mode** argument set to **Dialog**, Access suspends the macro until the form is closed or hidden.</span></span> <span data-ttu-id="1220b-161">Чтобы скрыть форму, значения свойства **Visible** **No** с помощью **макрокоманды** .</span><span class="sxs-lookup"><span data-stu-id="1220b-161">You can hide a form by setting its **Visible** property to **No** by using the **SetValue** action.</span></span>


> [!TIP]
> <P><span data-ttu-id="1220b-162">Можно выбрать форму в области навигации и перетащите его в строку действие в макросе.</span><span class="sxs-lookup"><span data-stu-id="1220b-162">You can select a form in the Navigation Pane and drag it to a macro action row.</span></span> <span data-ttu-id="1220b-163">Это автоматически создает <STRONG>ОткрытьФорму</STRONG> действие, которое открывается форма в представлении формы.</span><span class="sxs-lookup"><span data-stu-id="1220b-163">This automatically creates an <STRONG>OpenForm</STRONG> action that opens the form in Form view.</span></span></P>



<span data-ttu-id="1220b-164">Фильтр и условия WHERE, применяемые становятся значением свойства **фильтра** формы.</span><span class="sxs-lookup"><span data-stu-id="1220b-164">The filter and WHERE condition you apply become the setting of the form's **Filter** property.</span></span>

## <a name="examples"></a><span data-ttu-id="1220b-165">Примеры</span><span class="sxs-lookup"><span data-stu-id="1220b-165">Examples</span></span>

<span data-ttu-id="1220b-166">**Задайте значение элемента управления с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="1220b-166">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="1220b-167">Следующий макрос открывает форму добавления продуктов с помощью кнопки на форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="1220b-167">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="1220b-168">Демонстрируется использование **эхо**, **CloseWindow**, **ОткрытьФорму**, **SetValue**и **КЭлементуУправления** действий.</span><span class="sxs-lookup"><span data-stu-id="1220b-168">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="1220b-169">Действие **SetValue** задает код поставщика управления на форме продуктов для текущего поставщика в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="1220b-169">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="1220b-170">**Затем КЭлементуУправления** перемещает фокус в поле Идентификатор категории, где можно вводить данные для нового продукта.</span><span class="sxs-lookup"><span data-stu-id="1220b-170">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="1220b-171">Этот макрос должен быть связан с кнопкой Добавить продукты в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="1220b-171">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1220b-172">Действие</span><span class="sxs-lookup"><span data-stu-id="1220b-172">Action</span></span></p></th>
<th><p><span data-ttu-id="1220b-173">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="1220b-173">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="1220b-174">Comment</span><span class="sxs-lookup"><span data-stu-id="1220b-174">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1220b-175"><strong>Эхо</strong></span><span class="sxs-lookup"><span data-stu-id="1220b-175"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="1220b-176"><strong>Вывод на экран</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="1220b-176"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="1220b-177">Остановите обновление экрана в процессе выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="1220b-177">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1220b-178"><strong>CloseWindow</strong></span><span class="sxs-lookup"><span data-stu-id="1220b-178"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="1220b-179"><strong>Тип объекта</strong>: <strong>FormObject имя</strong>: продукт списка <strong>Сохранить</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="1220b-179"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="1220b-180">Закройте форму списка продуктов.</span><span class="sxs-lookup"><span data-stu-id="1220b-180">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1220b-181"><strong>ОткрытьФорму</strong></span><span class="sxs-lookup"><span data-stu-id="1220b-181"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="1220b-182"><strong>Имя формы</strong>: продуктов <strong>представления</strong>: <strong>FormData режима</strong>: <strong>Режим AddWindow</strong>: <strong>Обычный</strong></span><span class="sxs-lookup"><span data-stu-id="1220b-182"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="1220b-183">Откройте форму продуктов.</span><span class="sxs-lookup"><span data-stu-id="1220b-183">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1220b-184"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="1220b-184"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="1220b-185"><strong>Элемент</strong>: [формы]! [Товары]! [Код поставщика] <strong>Выражение</strong>: КодПоставщика</span><span class="sxs-lookup"><span data-stu-id="1220b-185"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="1220b-186">Значение текущего поставщика управления код поставщика в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="1220b-186">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1220b-187"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="1220b-187"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="1220b-188"><strong>Имя элемента управления</strong>: идентификатор категории</span><span class="sxs-lookup"><span data-stu-id="1220b-188"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="1220b-189">Перейдите к элементу управления идентификатор категории.</span><span class="sxs-lookup"><span data-stu-id="1220b-189">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1220b-190">Следующий макрос открывает форму списка продуктов в правом нижнем углу формы Поставщики, отображение текущего поставщика продуктов.</span><span class="sxs-lookup"><span data-stu-id="1220b-190">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="1220b-191">Демонстрируется использование **эхо**, **MessageBox**, **КЭлементуУправления**, **ОстановитьМакрос**, **ОткрытьФорму**и **MoveAndSizeWindow** действий.</span><span class="sxs-lookup"><span data-stu-id="1220b-191">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="1220b-192">Также показано использование условного выражения с **MessageBox**, **КЭлементуУправления**« **Поставщики** ».</span><span class="sxs-lookup"><span data-stu-id="1220b-192">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="1220b-193">Этот макрос должен быть связан с кнопкой Обзор продуктов в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="1220b-193">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<span data-ttu-id="1220b-194">**Синхронизация форм с помощью макроса (en)**</span><span class="sxs-lookup"><span data-stu-id="1220b-194">**Synchronize forms by using a macro**</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1220b-195">Condition</span><span class="sxs-lookup"><span data-stu-id="1220b-195">Condition</span></span></p></th>
<th><p><span data-ttu-id="1220b-196">Действие</span><span class="sxs-lookup"><span data-stu-id="1220b-196">Action</span></span></p></th>
<th><p><span data-ttu-id="1220b-197">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="1220b-197">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="1220b-198">Comment</span><span class="sxs-lookup"><span data-stu-id="1220b-198">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="1220b-199"><strong>Эхо</strong></span><span class="sxs-lookup"><span data-stu-id="1220b-199"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="1220b-200"><strong>Вывод на экран</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="1220b-200"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="1220b-201">Остановите обновление экрана в процессе выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="1220b-201">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1220b-202">IsNull([SupplierID])</span><span class="sxs-lookup"><span data-stu-id="1220b-202">IsNull([SupplierID])</span></span></p></td>
<td><p><span data-ttu-id="1220b-203"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="1220b-203"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="1220b-204"><strong>Сообщение</strong>: перемещение на запись поставщика, продукты, чтобы увидеть, затем нажмите кнопку Предварительный просмотр еще раз.</span><span class="sxs-lookup"><span data-stu-id="1220b-204"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="1220b-205"><strong>Звуковые сигналы</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Выбор поставщика</span><span class="sxs-lookup"><span data-stu-id="1220b-205"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="1220b-206">При отсутствии никто из современных поставщиков в форме Поставщики, отображается сообщение.</span><span class="sxs-lookup"><span data-stu-id="1220b-206">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1220b-207">...</span><span class="sxs-lookup"><span data-stu-id="1220b-207"></span></span></p></td>
<td><p><span data-ttu-id="1220b-208"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="1220b-208"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="1220b-209"><strong>Имя элемента управления</strong>: CompanyName</span><span class="sxs-lookup"><span data-stu-id="1220b-209"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="1220b-210">Перемещение фокуса на элемент управления CompanyName.</span><span class="sxs-lookup"><span data-stu-id="1220b-210">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1220b-211">...</span><span class="sxs-lookup"><span data-stu-id="1220b-211"></span></span></p></td>
<td><p><span data-ttu-id="1220b-212"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="1220b-212"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="1220b-213">Остановка макроса.</span><span class="sxs-lookup"><span data-stu-id="1220b-213">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="1220b-214"><strong>ОткрытьФорму</strong></span><span class="sxs-lookup"><span data-stu-id="1220b-214"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="1220b-215"><strong>Имя формы</strong>: список продуктов <strong>представления</strong>: <strong>Имя DatasheetFilter</strong>: <strong>условие отбора</strong>: [код поставщика] = [Forms]! [Поставщики]! [Код поставщика] <strong>Режим данных</strong>: <strong>Режим чтения OnlyWindow</strong>: <strong>Обычный</strong></span><span class="sxs-lookup"><span data-stu-id="1220b-215"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [SupplierID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="1220b-216">Откройте форму списка продуктов и отображение текущего поставщика продуктов.</span><span class="sxs-lookup"><span data-stu-id="1220b-216">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="1220b-217"><strong>MoveAndSizeWindow</strong></span><span class="sxs-lookup"><span data-stu-id="1220b-217"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="1220b-218"><strong>Право</strong>: 0,7799&quot; <strong>вниз</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="1220b-218"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="1220b-219">Положение формы списка продуктов в нижней правой части формы Поставщики.</span><span class="sxs-lookup"><span data-stu-id="1220b-219">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

