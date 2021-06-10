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
# <a name="openform-macro-action"></a><span data-ttu-id="fd079-102">Макрокоманда OpenForm</span><span class="sxs-lookup"><span data-stu-id="fd079-102">OpenForm macro action</span></span>

<span data-ttu-id="fd079-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fd079-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fd079-104">Вы можете использовать действие **OpenForm** для открытия формы в представлении формы, представлении дизайна, предварительной печати или представлении таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="fd079-104">You can use the **OpenForm** action to open a form in Form view, Design view, Print Preview, or Datasheet view.</span></span> <span data-ttu-id="fd079-105">Он позволяет выбирать режим ввода данных и режим окна для формы, а также ограничивать количество записей, отображаемых в форме.</span><span class="sxs-lookup"><span data-stu-id="fd079-105">You can select data entry and window modes for the form and restrict the records that the form displays.</span></span>

## <a name="setting"></a><span data-ttu-id="fd079-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="fd079-106">Setting</span></span>

<span data-ttu-id="fd079-107">Действие **OpenForm** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="fd079-107">The **OpenForm** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fd079-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="fd079-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="fd079-109">Описание</span><span class="sxs-lookup"><span data-stu-id="fd079-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd079-110"><strong>Имя формы</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-110"><strong>Form Name</strong></span></span></p></td>
<td><p><span data-ttu-id="fd079-111">Имя формы для открытия.</span><span class="sxs-lookup"><span data-stu-id="fd079-111">The name of the form to open.</span></span> <span data-ttu-id="fd079-112">Поле <strong>Имя формы</strong> в разделе <strong>Аргументы</strong> действий в области Macro Builder отображает все формы в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="fd079-112">The <strong>Form Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all forms in the current database.</span></span> <span data-ttu-id="fd079-113">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="fd079-113">This is a required argument.</span></span> <span data-ttu-id="fd079-114">Если вы запустите макрос, содержащий действие <strong>OpenForm</strong> в базе данных библиотеки, Microsoft Access сначала ищет форму с этим именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="fd079-114">If you run a macro containing the <strong>OpenForm</strong> action in a library database, Microsoft Access first looks for the form with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd079-115"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-115"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="fd079-116">Представление, в котором откроется форма.</span><span class="sxs-lookup"><span data-stu-id="fd079-116">The view in which the form will open.</span></span> <span data-ttu-id="fd079-117">Щелкните <strong>форму,</strong> <strong>дизайн,</strong> <strong>предварительный</strong>просмотр <strong>печати,</strong>таблицу <strong></strong> данных, таблицу <strong>pivotTable</strong>или сводная диаграмма в <strong>поле Просмотр.</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-117">Click <strong>Form</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>Datasheet</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="fd079-118">По умолчанию является <strong>Form</strong>.</span><span class="sxs-lookup"><span data-stu-id="fd079-118">The default is <strong>Form</strong>.</span></span></p><p><span data-ttu-id="fd079-119"><strong>ПРИМЕЧАНИЕ.</strong> <STRONG>Параметр аргумента View</STRONG> переопределяет параметры свойств <STRONG>DefaultView</STRONG> формы и <STRONG>ViewsAllowed.</STRONG></span><span class="sxs-lookup"><span data-stu-id="fd079-119"><strong>NOTE</strong>: The <STRONG>View</STRONG> argument setting overrides the settings of the form's <STRONG>DefaultView</STRONG> and <STRONG>ViewsAllowed</STRONG> properties.</span></span> <span data-ttu-id="fd079-120">Например, если свойство <STRONG>ViewsAllowed</STRONG> формы настроено на <STRONG>таблицу Datasheet,</STRONG>можно использовать действие <STRONG>OpenForm</STRONG> для открытия формы в представлении Формы.</span><span class="sxs-lookup"><span data-stu-id="fd079-120">For example, if a form's <STRONG>ViewsAllowed</STRONG> property is set to <STRONG>Datasheet</STRONG>, you can still use the <STRONG>OpenForm</STRONG> action to open the form in Form view.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd079-121"><strong>Имя фильтра</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-121"><strong>Filter Name</strong></span></span></p></td>
<td><p><span data-ttu-id="fd079-122">Фильтр, который ограничивает или сортит записи формы.</span><span class="sxs-lookup"><span data-stu-id="fd079-122">A filter that restricts or sorts the form's records.</span></span> <span data-ttu-id="fd079-123">Можно ввести имя существующего запроса или фильтра, сохраненного в качестве запроса.</span><span class="sxs-lookup"><span data-stu-id="fd079-123">You can enter the name of either an existing query or a filter that was saved as a query.</span></span> <span data-ttu-id="fd079-124">Однако запрос должен включать все поля в открываемой форме или иметь свойство <strong>OutputAllFields,</strong> за набором <strong>да.</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-124">However, the query must include all the fields in the form you are opening or have its <strong>OutputAllFields</strong> property set to <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd079-125"><strong>Где состояние</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-125"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="fd079-126">Допустимый SQL where (без слова WHERE) или выражение, которое Access использует для выбора записей из таблицы или запроса формы.</span><span class="sxs-lookup"><span data-stu-id="fd079-126">A valid SQL WHERE clause (without the word WHERE) or expression that Access uses to select records from the form's underlying table or query.</span></span> <span data-ttu-id="fd079-127">Если выбрать фильтр с аргументом <strong>Имя фильтра,</strong> Access применяет этот пункт WHERE к результатам фильтра.</span><span class="sxs-lookup"><span data-stu-id="fd079-127">If you select a filter with the <strong>Filter Name</strong> argument, Access applies this WHERE clause to the results of the filter.</span></span> <span data-ttu-id="fd079-128">Чтобы открыть форму и ограничить ее записи теми, которые указаны значением управления в другой форме, используйте следующее выражение: <strong>[</strong><em>имя</em>поля ]<strong>= Forms![</strong> <em>formname</em><strong>]! [</strong><em>имя управления в</em>другой <em></em> <strong>форме] Замените</strong> имя поля на имя поля в таблице или запросе формы, которая должна открыться.</span><span class="sxs-lookup"><span data-stu-id="fd079-128">To open a form and restrict its records to those specified by the value of a control on another form, use the following expression: <strong>[</strong><em>fieldname</em><strong>] = Forms![</strong><em>formname</em><strong>]![</strong><em>controlname on other form</em><strong>]</strong> Replace <em>fieldname</em> with the name of a field in the underlying table or query of the form you want to open.</span></span> <span data-ttu-id="fd079-129"><em>Замените</em> имя <em></em> формы и имя управления в другой форме с именем другой формы и управлением в другой форме, которая содержит необходимое значение записей в первой форме для совпадения.</span><span class="sxs-lookup"><span data-stu-id="fd079-129">Replace <em>formname</em> and <em>controlname on other form</em> with the name of the other form and the control on the other form that contains the value you want records in the first form to match.</span></span></p><p><span data-ttu-id="fd079-130"><strong>ПРИМЕЧАНИЕ.</strong>Максимальная длина аргумента <STRONG>Where Condition</STRONG> — 255 символов.</span><span class="sxs-lookup"><span data-stu-id="fd079-130"><strong>NOTE</strong>: The maximum length of the <STRONG>Where Condition</STRONG> argument is 255 characters.</span></span> <span data-ttu-id="fd079-131">Если требуется ввести более сложный пункт SQL WHERE дольше, используйте метод <STRONG>OpenForm</STRONG> объекта <STRONG>DoCmd</STRONG> в модуле Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="fd079-131">If you need to enter a more complex SQL WHERE clause longer than this, use the <STRONG>OpenForm</STRONG> method of the <STRONG>DoCmd</STRONG> object in a Visual Basic for Applications (VBA) module instead.</span></span> <span data-ttu-id="fd079-132">Вы можете ввести SQL, где в VBA можно ввести утверждения о клаузулах до 32 768 знаков.</span><span class="sxs-lookup"><span data-stu-id="fd079-132">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd079-133"><strong>Режим данных</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-133"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="fd079-134">Режим ввода данных для формы.</span><span class="sxs-lookup"><span data-stu-id="fd079-134">The data entry mode for the form.</span></span> <span data-ttu-id="fd079-135">Это относится только к формам, открываемым в режиме формы или режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="fd079-135">This applies only to forms opened in Form view or Datasheet view.</span></span> <span data-ttu-id="fd079-136">Щелкните <strong>Добавить</strong> (пользователь может добавлять новые записи, но не может изменять существующие записи), <strong></strong> изменить (пользователь может изменять существующие записи и добавлять новые записи) или <strong>Только</strong> для чтения (пользователь может просматривать только записи).</span><span class="sxs-lookup"><span data-stu-id="fd079-136">Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="fd079-137">По умолчанию <strong>изменить</strong>.</span><span class="sxs-lookup"><span data-stu-id="fd079-137">The default is <strong>Edit</strong>.</span></span> <span data-ttu-id="fd079-138"><strong>Примечания</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-138"><strong>Notes</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="fd079-139">Параметр <strong>аргумента Режим</strong> данных переопределяет параметры свойств <strong>AllowEdits</strong>формы, <strong>AllowDeletions,</strong> <strong>AllowAdditions</strong>и <strong>DataEntry.</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-139">The <strong>Data Mode</strong> argument setting overrides the settings of the form's <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>, and <strong>DataEntry</strong> properties.</span></span> <span data-ttu-id="fd079-140">Например, если свойство <strong>AllowEdits</strong> формы настроено на <strong>"Нет",</strong>можно использовать действие <strong>OpenForm</strong> для открытия формы в режиме Редактирования.</span><span class="sxs-lookup"><span data-stu-id="fd079-140">For example, if a form's <strong>AllowEdits</strong> property is set to <strong>No</strong>, you can still use the <strong>OpenForm</strong> action to open the form in Edit mode.</span></span></p></li>
<li><p><span data-ttu-id="fd079-141">Если оставить этот аргумент пустым, Access открывает форму в режиме ввода данных, заданной свойствами <strong>AllowEdits,</strong> <strong>AllowDeletions,</strong> <strong>AllowAdditions</strong>и <strong>DataEntry.</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-141">If you leave this argument blank, Access opens the form in the data entry mode set by the form's <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>, and <strong>DataEntry</strong> properties.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd079-142"><strong>Режим окна</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-142"><strong>Window Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="fd079-143">Режим окна, в котором открывается форма.</span><span class="sxs-lookup"><span data-stu-id="fd079-143">The window mode in which the form opens.</span></span> <span data-ttu-id="fd079-144">Щелкните <strong>Normal</strong> (форма открывается в режиме, задаваемом его свойствами), <strong>Hidden</strong> (форма скрыта), <strong>Icon</strong> (форма открывается свести к минимуму как небольшая строка заголовка в нижней части экрана) или <strong>Диалоговое</strong> окно (свойства <strong>Modal</strong> и <strong>PopUp</strong> формы задаваются <strong>да).</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-144">Click <strong>Normal</strong> (the form opens in the mode set by its properties), <strong>Hidden</strong> (the form is hidden), <strong>Icon</strong> (the form opens minimized as a small title bar at the bottom of the screen), or <strong>Dialog</strong> (the form's <strong>Modal</strong> and <strong>PopUp</strong> properties are set to <strong>Yes</strong>).</span></span> <span data-ttu-id="fd079-145">По умолчанию является <strong>нормальным</strong>.</span><span class="sxs-lookup"><span data-stu-id="fd079-145">The default is <strong>Normal</strong>.</span></span></p><p><span data-ttu-id="fd079-146"><strong>ПРИМЕЧАНИЕ.</strong>Некоторые <STRONG>параметры аргумента в</STRONG> режиме окна не применяются при использовании документов на вкладке.</span><span class="sxs-lookup"><span data-stu-id="fd079-146"><strong>NOTE</strong>: Some <STRONG>Window Mode</STRONG> argument settings do not apply when using tabbed documents.</span></span> <span data-ttu-id="fd079-147">Чтобы перейти на перекрывающиеся окна:</span><span class="sxs-lookup"><span data-stu-id="fd079-147">To switch to overlapping windows:</span></span></p>
<ol>
<li><p><span data-ttu-id="fd079-148">Щелкните вкладку File и нажмите кнопку <strong>Параметры</strong>.</span><span class="sxs-lookup"><span data-stu-id="fd079-148">Click the File tab and then click <strong>Options</strong>.</span></span></p></li>
<li><p><span data-ttu-id="fd079-149">В <strong>диалоговом окне Параметры</strong> доступа щелкните <strong>Текущая база данных</strong>.</span><span class="sxs-lookup"><span data-stu-id="fd079-149">In the <strong>Access Options</strong> dialog box, click <strong>Current Database</strong>.</span></span></p></li>
<li><p><span data-ttu-id="fd079-150">В разделе <strong>Параметры приложений</strong>в <strong>разделе Параметры окна документов</strong>нажмите <strong>кнопку Перекрытие Windows</strong>.</span><span class="sxs-lookup"><span data-stu-id="fd079-150">In the <strong>Application Options</strong>section, under <strong>Document Window Options</strong>, click <strong>Overlapping Windows</strong>.</span></span></p></li>
<li><p><span data-ttu-id="fd079-151">Нажмите <strong>кнопку ОК,</strong>затем закроем и снова откроете базу данных.</span><span class="sxs-lookup"><span data-stu-id="fd079-151">Click <strong>OK</strong>, then close and reopen the database.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fd079-152">Примечания</span><span class="sxs-lookup"><span data-stu-id="fd079-152">Remarks</span></span>

<span data-ttu-id="fd079-153">Это действие аналогично дважды щелкнуть форму в области навигации или щелкнуть правой кнопкой мыши форму в области навигации, а затем выбрать представление.</span><span class="sxs-lookup"><span data-stu-id="fd079-153">This action is similar to double-clicking a form in the Navigation Pane, or right-clicking the form in the Navigation Pane and then selecting a view.</span></span>

<span data-ttu-id="fd079-154">Форма может быть модальной (она должна быть закрыта или скрыта перед выполнением пользователем любых других действий) или без режима (пользователь может перейти в другие окна, пока форма открыта).</span><span class="sxs-lookup"><span data-stu-id="fd079-154">A form can be modal (it must be closed or hidden before the user can perform any other action) or modeless (the user can move to other windows while the form is open).</span></span> <span data-ttu-id="fd079-155">Это может быть всплывающее окно (форма, используемая для сбора или отображения информации, которая остается на верхней части всех остальных окон Access).</span><span class="sxs-lookup"><span data-stu-id="fd079-155">It can also be a pop-up form (a form used to collect or display information that remains on top of all other Access windows).</span></span> <span data-ttu-id="fd079-156">При разработке формы вы задали свойства **Modal** и **PopUp.**</span><span class="sxs-lookup"><span data-stu-id="fd079-156">You set the **Modal** and **PopUp** properties when you design the form.</span></span> <span data-ttu-id="fd079-157">Если используется **аргумент Normal** для **аргумента Window Mode,** форма открывается в режиме, заданном этими настройками свойств.</span><span class="sxs-lookup"><span data-stu-id="fd079-157">If you use **Normal** for the **Window Mode** argument, the form opens in the mode specified by these property settings.</span></span> <span data-ttu-id="fd079-158">Если вы используете **диалоговое окно** для **аргумента Режим окна,** эти свойства за набором **да**.</span><span class="sxs-lookup"><span data-stu-id="fd079-158">If you use **Dialog** for the **Window Mode** argument, these properties are both set to **Yes**.</span></span> <span data-ttu-id="fd079-159">Форма, открытая как скрытая или как значок, возвращается в режим, заданный его настройками свойств при показе или восстановлении.</span><span class="sxs-lookup"><span data-stu-id="fd079-159">A form opened as hidden or as an icon returns to the mode specified by its property settings when you show or restore it.</span></span>

<span data-ttu-id="fd079-160">Когда вы открываете форму с аргументом **Window Mode** set to **Dialog,** Access приостанавливать макрос, пока форма не будет закрыта или скрыта.</span><span class="sxs-lookup"><span data-stu-id="fd079-160">When you open a form with the **Window Mode** argument set to **Dialog**, Access suspends the macro until the form is closed or hidden.</span></span> <span data-ttu-id="fd079-161">Вы можете скрыть форму, установив **ее** видимое свойство **"Нет",** используя **действие SetValue.**</span><span class="sxs-lookup"><span data-stu-id="fd079-161">You can hide a form by setting its **Visible** property to **No** by using the **SetValue** action.</span></span>

> [!TIP]
> <span data-ttu-id="fd079-162">Вы можете выбрать форму в области навигации и перетаскивать ее в строку действий макроса.</span><span class="sxs-lookup"><span data-stu-id="fd079-162">You can select a form in the Navigation Pane and drag it to a macro action row.</span></span> <span data-ttu-id="fd079-163">Это автоматически создает действие **OpenForm,** которое открывает форму в представлении Формы.</span><span class="sxs-lookup"><span data-stu-id="fd079-163">This automatically creates an **OpenForm** action that opens the form in Form view.</span></span>

<span data-ttu-id="fd079-164">Фильтр и условия WHERE, которые вы применяли, становятся параметром свойства **Фильтр формы.**</span><span class="sxs-lookup"><span data-stu-id="fd079-164">The filter and WHERE condition you apply become the setting of the form's **Filter** property.</span></span>

## <a name="examples"></a><span data-ttu-id="fd079-165">Примеры</span><span class="sxs-lookup"><span data-stu-id="fd079-165">Examples</span></span>

<span data-ttu-id="fd079-166">**Установка значения элемента управления с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="fd079-166">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="fd079-167">Следующий макрос открывает форму "Добавить товары" с помощью кнопки в форме "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="fd079-167">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="fd079-168">Он демонстрирует применение макрокоманд **ВыводНаЭкран**, **ЗакрытьОкно**, **ОткрытьФорму**, **ЗадатьЗначение** и **КЭлементуУправления**.</span><span class="sxs-lookup"><span data-stu-id="fd079-168">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="fd079-169">Действие **SetValue задает** контроль поставщика в форме Продуктов текущему поставщику в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="fd079-169">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="fd079-170">Затем **действие GoToControl** перемещает фокус в поле Category ID, где можно начать ввод данных для нового продукта.</span><span class="sxs-lookup"><span data-stu-id="fd079-170">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="fd079-171">Этот макрос должен быть привязан к кнопке "Добавить товары" в форме "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="fd079-171">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fd079-172">Макрокоманда</span><span class="sxs-lookup"><span data-stu-id="fd079-172">Action</span></span></p></th>
<th><p><span data-ttu-id="fd079-173">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="fd079-173">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="fd079-174">Примечание</span><span class="sxs-lookup"><span data-stu-id="fd079-174">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd079-175"><strong>ВыводНаЭкран</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-175"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="fd079-176"><strong>Включить вывод</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-176"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="fd079-177">Приостанавливает обновление экрана, пока выполняется макрос.</span><span class="sxs-lookup"><span data-stu-id="fd079-177">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd079-178"><strong>ЗакрытьОкно</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-178"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="fd079-179"><strong>Тип объекта</strong>: <strong>FormObject Имя</strong>: Список товаров <strong>Сохранить</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-179"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="fd079-180">Закрывает форму "Список товаров".</span><span class="sxs-lookup"><span data-stu-id="fd079-180">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd079-181"><strong>ОткрытьФорму</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-181"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="fd079-182"><strong>Имя формы</strong>: Товары <strong>Представление</strong>: <strong>FormData Режим</strong>: <strong>AddWindow Режим</strong>: <strong>Обычный</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-182"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="fd079-183">Открывает форму "Товары".</span><span class="sxs-lookup"><span data-stu-id="fd079-183">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd079-184"><strong>ЗадатьЗначение</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-184"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="fd079-185"><strong>Элемент</strong>: [Forms]![Товары]![КодПоставщика] <strong>Выражение</strong>: КодПоставщика</span><span class="sxs-lookup"><span data-stu-id="fd079-185"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="fd079-186">Установите контроль поставщика для текущего поставщика в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="fd079-186">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd079-187"><strong>КЭлементуУправления</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-187"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="fd079-188"><strong>Имя элемента управления</strong>: КодКатегории</span><span class="sxs-lookup"><span data-stu-id="fd079-188"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="fd079-189">Перейдите к контролю category ID.</span><span class="sxs-lookup"><span data-stu-id="fd079-189">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fd079-190">Следующий макрос открывает форму Списка продуктов в нижнем правом углу формы Поставщики, отображая продукты текущего поставщика.</span><span class="sxs-lookup"><span data-stu-id="fd079-190">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="fd079-191">В нем показано использование действий **Echo,** **MessageBox,** **GoToControl,** **StopMacro,** **OpenForm** и **MoveAndSizeWindow.**</span><span class="sxs-lookup"><span data-stu-id="fd079-191">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="fd079-192">В нем также показано использование условного выражения с **действиями MessageBox,** **GoToControl** и **StopMacro.**</span><span class="sxs-lookup"><span data-stu-id="fd079-192">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="fd079-193">Этот макрос следует прикрепить к кнопке Review Products в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="fd079-193">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<span data-ttu-id="fd079-194">**Синхронизация форм с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="fd079-194">**Synchronize forms by using a macro**</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fd079-195">Условие</span><span class="sxs-lookup"><span data-stu-id="fd079-195">Condition</span></span></p></th>
<th><p><span data-ttu-id="fd079-196">Макрокоманда</span><span class="sxs-lookup"><span data-stu-id="fd079-196">Action</span></span></p></th>
<th><p><span data-ttu-id="fd079-197">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="fd079-197">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="fd079-198">Примечание</span><span class="sxs-lookup"><span data-stu-id="fd079-198">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="fd079-199"><strong>ВыводНаЭкран</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-199"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="fd079-200"><strong>Включить вывод</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-200"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="fd079-201">Приостанавливает обновление экрана, пока выполняется макрос.</span><span class="sxs-lookup"><span data-stu-id="fd079-201">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd079-202">IsNull([SupplierID])</span><span class="sxs-lookup"><span data-stu-id="fd079-202">IsNull([SupplierID])</span></span></p></td>
<td><p><span data-ttu-id="fd079-203"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-203"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="fd079-204"><strong>Сообщение.</strong>Перейдите к записи поставщика, продукты которого вы хотите видеть, а затем нажмите кнопку Обзор продуктов снова.</span><span class="sxs-lookup"><span data-stu-id="fd079-204"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="fd079-205"><strong>Звуковой сигнал</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Выберите поставщика</span><span class="sxs-lookup"><span data-stu-id="fd079-205"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="fd079-206">Если в форме Поставщики нет текущего поставщика, отобразить сообщение.</span><span class="sxs-lookup"><span data-stu-id="fd079-206">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd079-207">...</span><span class="sxs-lookup"><span data-stu-id="fd079-207">...</span></span></p></td>
<td><p><span data-ttu-id="fd079-208"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-208"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="fd079-209"><strong>Имя управления:</strong>CompanyName</span><span class="sxs-lookup"><span data-stu-id="fd079-209"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="fd079-210">Переместите фокус на управление CompanyName.</span><span class="sxs-lookup"><span data-stu-id="fd079-210">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd079-211">...</span><span class="sxs-lookup"><span data-stu-id="fd079-211">...</span></span></p></td>
<td><p><span data-ttu-id="fd079-212"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-212"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fd079-213">Остановите макрос.</span><span class="sxs-lookup"><span data-stu-id="fd079-213">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="fd079-214"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-214"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="fd079-215"><strong>Имя формы</strong>: Представление списка <strong>продуктов:</strong> <strong>Имя DatasheetFilter</strong>: Where <strong>Condition</strong>: [SupplierID] = [Forms]! [Поставщики]! [SupplierID] <strong>Режим данных:</strong> <strong>Режим чтения OnlyWindow</strong>: <strong>Нормальный</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-215"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [SupplierID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="fd079-216">Откройте форму списка продуктов и покажите продукты текущего поставщика.</span><span class="sxs-lookup"><span data-stu-id="fd079-216">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="fd079-217"><strong>MoveAndSizeWindow</strong></span><span class="sxs-lookup"><span data-stu-id="fd079-217"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="fd079-218"><strong>Справа</strong>: 0.7799 &quot; <strong>Вниз</strong>: 1.8&quot;</span><span class="sxs-lookup"><span data-stu-id="fd079-218"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="fd079-219">Расположить форму списка продуктов в нижнем праве формы Поставщики.</span><span class="sxs-lookup"><span data-stu-id="fd079-219">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

