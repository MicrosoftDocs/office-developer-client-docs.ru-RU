---
title: Макрокоманда "ЗадатьЗначение"
TOCTitle: SetValue macro action
ms:assetid: a08be0c1-a053-45f9-b4ae-709fedc58e8b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820771(v=office.15)
ms:contentKeyID: 48546712
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 6b6f16c22e9265159c73279cfa1b2644adbc0277
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306820"
---
# <a name="setvalue-macro-action"></a><span data-ttu-id="dc3a0-102">Макрокоманда "ЗадатьЗначение"</span><span class="sxs-lookup"><span data-stu-id="dc3a0-102">SetValue macro action</span></span>

<span data-ttu-id="dc3a0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc3a0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dc3a0-104">С помощью макрокоманды **ЗадатьЗначение** можно задать значение для поля, элемента управления или свойства в форме (в режиме формы или таблицы) или в отчете Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-104">You can use the **SetValue** action to set the value of a Microsoft Access field, control, or property on a form, a form datasheet, or a report.</span></span>

> [!NOTE]
> - <span data-ttu-id="dc3a0-105">Чтобы задать значение свойства Access, которое возвращает объект, нельзя использовать макрокоманду **ЗадатьЗначение**.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-105">You cannot use the **SetValue** action to set the value of an Access property that returns an object.</span></span>
> - <span data-ttu-id="dc3a0-106">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="dc3a0-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="dc3a0-107">Setting</span></span>

<span data-ttu-id="dc3a0-108">Макрокоманда **ЗадатьЗначение** имеет следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="dc3a0-108">The **SetLocalVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc3a0-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="dc3a0-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="dc3a0-110">Описание</span><span class="sxs-lookup"><span data-stu-id="dc3a0-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc3a0-111"><strong>Элемент</strong></span><span class="sxs-lookup"><span data-stu-id="dc3a0-111"><strong>Item</strong></span></span></p></td>
<td><p><span data-ttu-id="dc3a0-112">Имя поля, элемента управления или свойства, значение которого вы хотите задать.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-112">The name of the field, control, or property whose value you want to set.</span></span> <span data-ttu-id="dc3a0-113">Введите имя поля, элемента управления или свойства в поле <strong>Элемент</strong> в разделе <strong>Аргументы макрокоманды</strong> области построителя макросов.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-113">Enter the field, control, or property name in the <strong>Item</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="dc3a0-114">Следует использовать полный синтаксис в ссылке на этот элемент, например, <em>имя_элемента_управления</em> (для элемента управления в форме или отчете, из которого вызывается макрос) или <strong>Forms</strong>!<em>имя_формы</em>!<em>имя_элемента_управления</em>.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-114">You must use the full syntax to refer to this item, such as <em>controlname</em> (for a control on the form or report from which the macro was called) or <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>.</span></span> <span data-ttu-id="dc3a0-115">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-115">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc3a0-116"><strong>Выражение</strong></span><span class="sxs-lookup"><span data-stu-id="dc3a0-116"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="dc3a0-117">Выражение, которое Access использует, чтобы задать значение для указанного элемента.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-117">The expression Access uses to set the value for this item.</span></span> <span data-ttu-id="dc3a0-118">Следует всегда использовать полный синтаксис для ссылки на любой объект в выражении.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-118">You must always use the full syntax to refer to any objects in the expression.</span></span> <span data-ttu-id="dc3a0-119">Например, чтобы увеличить значение элемента управления "Зарплата" в форме "Сотрудники" на 10 процентов, следует использовать синтаксис Forms!Сотрудники!Зарплата\*1.1.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-119">For example, to increase the value in a Salary control on an Employees form by 10 percent, use Forms!Employees!Salary\*1.1.</span></span> <span data-ttu-id="dc3a0-120">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-120">This is a required argument.</span></span></p><p><span data-ttu-id="dc3a0-121"><strong>ПРИМЕЧАНИЕ</strong>. В этом аргументе не следует использовать знак равенства (=) перед выражением.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-121"><strong>NOTE</strong>: You shouldn't use an equal sign (=) before the expression in this argument.</span></span> <span data-ttu-id="dc3a0-122">В противном случае Access вычисляет выражение и затем использует полученное значение для этого аргумента.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-122">If you do, Access evaluates the expression and then uses this value as the expression in this argument.</span></span> <span data-ttu-id="dc3a0-123">Это может привести к непредвиденным результатам, если выражение является строкой.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-123">This can produce unexpected results if the expression is a string.</span></span></p>
<p><span data-ttu-id="dc3a0-124">Например, если ввести <strong>=&quot;Строка1&quot;</strong> для этого аргумента, Access сначала вычислит выражение как "Строка1".</span><span class="sxs-lookup"><span data-stu-id="dc3a0-124">For example, if you type <strong>=&quot;String1&quot;</strong> for this argument, Access first evaluates the expression as String1.</span></span> <span data-ttu-id="dc3a0-125">Затем Access будет использовать "Строка1" как выражение в этом аргументе и попытается найти элемент управления или свойство с именем "Строка1" в форме или отчете, из которого вызывался макрос.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-125">Then it uses String1 as the expression in this argument, expecting to find a control or property named String1 on the form or report that called the macro.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="dc3a0-126">В базе данных Access (MDB или ACCDB) нажмите кнопку **Построить**, чтобы создать выражение для любого из этих аргументов с помощью построителя выражений.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-126">In an Access database (.mdb or .accdb), click the **Build** button to use the Expression Builder to create an expression for either of these arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc3a0-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="dc3a0-127">Remarks</span></span>

<span data-ttu-id="dc3a0-128">Данную макрокоманду можно использовать, чтобы задать значение для поля или элемента управления в форме (в режиме формы или в режиме таблицы) или в отчете.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-128">You can use this action to set a value for a field or control on a form, a form datasheet, or a report.</span></span> <span data-ttu-id="dc3a0-129">Вы также можете задать значения практически для любого свойства элемента управления, формы или отчета в любом режиме.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-129">You can also set the value for almost all control, form, and report properties in any view.</span></span> <span data-ttu-id="dc3a0-130">Чтобы определить, можно ли задать значение конкретного свойства с помощью макроса и в каких режимах это сделать, см. раздел для этого свойства в справке редактора Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-130">To find out whether a particular property can be set by using a macro and which views it can be set in, see the Help topic for that property in the Visual Basic Editor.</span></span>

<span data-ttu-id="dc3a0-131">Можно также задать значение для поля в базовой таблице формы, даже если форма не содержит элемент управления, привязанный к полю.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-131">You can also set the value for a field in a form's underlying table even if the form doesn't contain a control bound to the field.</span></span> <span data-ttu-id="dc3a0-132">Используйте для этого синтаксис **Forms**\!*имя_формы*\!*имя_поля* в поле **Элемент**.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-132">Use the syntax **Forms**\!*formname*\!*fieldname* in the **Item** box to set the value for such a field.</span></span> <span data-ttu-id="dc3a0-133">Вы также можете указать поле в базовой таблице отчета, используя синтаксис **Reports**\!*имя_отчета*\!*имя_поля*, но в отчете должен быть элемент управления, привязанный к этому полю, или на поле должен ссылаться вычисляемый элемент управления в отчете.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-133">You can also refer to a field in a report's underlying table by using the syntax **Reports**\!*reportname*\!*fieldname*, but there must be a control on the report bound to this field, or the field must be referred to in a calculated control on the report.</span></span>

<span data-ttu-id="dc3a0-134">Если задать значение элемента управления в форме, макрокоманда **ЗадатьЗначение** не будет запускать для него правила проверки на уровне формы, но если элемент управления является связанным, запускаются правила проверки на уровне таблицы для соответствующего поля.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-134">If you set the value of a control on a form, the **SetValue** action doesn't trigger the control's form-level validation rules, but it does trigger the underlying field's table-level validation rules if the control is a bound control.</span></span> <span data-ttu-id="dc3a0-135">Макрокоманда **ЗадатьЗначение** также вызывает пересчет, который может выполняться не сразу.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-135">The **SetValue** action also triggers recalculation, but the recalculation may not happen immediately.</span></span> <span data-ttu-id="dc3a0-136">Чтобы запустить немедленное обновление и принудительно выполнить пересчет, используйте макрокоманду **ОбновитьОбъект**.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-136">To trigger immediate repainting and force the recalculation to completion, use the **RepaintObject** action.</span></span> <span data-ttu-id="dc3a0-137">На значение, заданное в элементе управления с помощью макрокоманды **ЗадатьЗначение**, также не влияет маска ввода, заданная в свойстве **InputMask** элемента управления или соответствующего ему поля.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-137">The value you set in a control by using the **SetValue** action is also not affected by an input mask set in the control's or underlying field's **InputMask** property.</span></span>

<span data-ttu-id="dc3a0-138">Изменить значение элемента управления можно с помощью макрокоманды **ЗадатьЗначение** в макросе, который указан в свойстве события **После обновления** элемента управления.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-138">To change the value of a control, you can use the **SetValue** action in a macro specified by the control's **AfterUpdate** event property.</span></span> <span data-ttu-id="dc3a0-139">Однако с помощью макрокоманды **ЗадатьЗначение** в макросе, указанном в свойстве события **До обновления** элемента управления, невозможно изменить значение для этого элемента управления (хотя с помощью макрокоманды **ЗадатьЗначение** можно изменять значения других элементов управления).</span><span class="sxs-lookup"><span data-stu-id="dc3a0-139">However, you can't use the **SetValue** action in a macro specified by a control's **BeforeUpdate** event property to change the value of the control (although you can use the **SetValue** action to change the value of other controls).</span></span> <span data-ttu-id="dc3a0-140">Макрокоманду **ЗадатьЗначение** в макросе, который указан в свойствах событий **До обновления** или **После обновления** формы, можно также использовать для изменения значений любых элементов управления в текущей записи.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-140">You can also use the **SetValue** action in a macro specified by the **BeforeUpdate** or **AfterUpdate** property of a form to change the value of any controls in the current record.</span></span>

> [!NOTE]
> <span data-ttu-id="dc3a0-141">С помощью макрокоманды **ЗадатьЗначение** невозможно задать значение для следующих элементов управления:</span><span class="sxs-lookup"><span data-stu-id="dc3a0-141">You can't use the **SetValue** action to set the value of the following controls:</span></span>
> - <span data-ttu-id="dc3a0-142">связанных и вычисляемых элементов управления в отчетах;</span><span class="sxs-lookup"><span data-stu-id="dc3a0-142">Bound controls and calculated controls on reports.</span></span>
> - <span data-ttu-id="dc3a0-143">вычисляемых элементов управления в формах.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-143">Calculated controls on forms.</span></span>

> [!TIP]
> <span data-ttu-id="dc3a0-144">С помощью макрокоманды **ЗадатьЗначение** можно скрыть или отобразить форму в режиме формы.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-144">You can use the **SetValue** action to hide or show a form in Form view.</span></span> <span data-ttu-id="dc3a0-145">Введите **Forms**!*имя_формы\*\*\*.Visible*\* в поле **Элемент** и **Нет** или **Да** в поле **Выражение**.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-145">Enter **Forms**!*formname\*\*\*.Visible*\* in the **Item** box, and **No** or **Yes** in the **Expression** box.</span></span> <span data-ttu-id="dc3a0-146">Если для свойства **Visible** модальной формы задано значение **Нет**, форма скрывается и становится немодальной.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-146">Setting a modal form's **Visible** property to **No** hides the form and makes it modeless.</span></span> <span data-ttu-id="dc3a0-147">Чтобы отобразить форму и снова сделать ее модальной, выберите значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-147">Setting the property to **Yes** displays the form and makes it modal again.</span></span>

<span data-ttu-id="dc3a0-148">При изменении значения или добавления новых данных в элемент управления с помощью макрокоманды **ЗадатьЗначение** в макросе не запускаются такие события, как **До обновления**, **До вставки** или **Изменение**, которые происходят при изменении или вводе данных в эти элементы управления через пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-148">Changing the value of or adding new data in a control by using the **SetValue** action in a macro doesn't trigger events such as **BeforeUpdate**, **BeforeInsert**, or **Change** that occur when you change or enter data in these controls in the user interface.</span></span> <span data-ttu-id="dc3a0-149">Эти события также не происходят, если задать значение элемента управления в модуле Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="dc3a0-149">These events also don't occur if you set the value of the control by using a Visual Basic for Applications (VBA) module.</span></span>

<span data-ttu-id="dc3a0-150">Эта макрокоманда недоступна в модуле VBA. </span><span class="sxs-lookup"><span data-stu-id="dc3a0-150">This action isn't available in a VBA module.</span></span> <span data-ttu-id="dc3a0-151">Нужное значение следует задавать непосредственно в VBA.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-151">Set the value directly in Visual Basic.</span></span>

## <a name="example"></a><span data-ttu-id="dc3a0-152">Пример</span><span class="sxs-lookup"><span data-stu-id="dc3a0-152">Example</span></span>

<span data-ttu-id="dc3a0-153">**Установка значения элемента управления с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="dc3a0-153">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="dc3a0-154">Следующий макрос открывает форму "Добавить товары" с помощью кнопки в форме "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="dc3a0-154">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="dc3a0-155">Он демонстрирует применение макрокоманд **ВыводНаЭкран**, **ЗакрытьОкно**, **ОткрытьФорму**, **ЗадатьЗначение** и **КЭлементуУправления**.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-155">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="dc3a0-156">Макрокоманда **ЗадатьЗначение** задает в качестве значения элемента управления "Код поставщика" в форме "Товары" текущего поставщика в форме "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="dc3a0-156">The **SetValue** action sets the SupplierID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="dc3a0-157">После этого макрокоманда **КЭлементуУправления** перемещает фокус на поле "Код категории", с которого начинается ввод данных для нового товара.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-157">The **GoToControl** action then moves the focus to the CategoryID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="dc3a0-158">Этот макрос должен быть привязан к кнопке "Добавить товары" в форме "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="dc3a0-158">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc3a0-159">Макрокоманда</span><span class="sxs-lookup"><span data-stu-id="dc3a0-159">Action</span></span></p></th>
<th><p><span data-ttu-id="dc3a0-160">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="dc3a0-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="dc3a0-161">Примечание</span><span class="sxs-lookup"><span data-stu-id="dc3a0-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc3a0-162"><strong>ВыводНаЭкран</strong></span><span class="sxs-lookup"><span data-stu-id="dc3a0-162"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="dc3a0-163"><strong>Включить вывод</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="dc3a0-163"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="dc3a0-164">Приостанавливает обновление экрана, пока выполняется макрос.</span><span class="sxs-lookup"><span data-stu-id="dc3a0-164">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc3a0-165"><strong>ЗакрытьОкно</strong></span><span class="sxs-lookup"><span data-stu-id="dc3a0-165"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="dc3a0-166"><strong>Тип объекта</strong>: <strong>FormObject Имя</strong>: Список товаров <strong>Сохранить</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="dc3a0-166"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="dc3a0-167">Закрывает форму "Список товаров".</span><span class="sxs-lookup"><span data-stu-id="dc3a0-167">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc3a0-168"><strong>ОткрытьФорму</strong></span><span class="sxs-lookup"><span data-stu-id="dc3a0-168"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="dc3a0-169"><strong>Имя формы</strong>: Товары <strong>Представление</strong>: <strong>FormData Режим</strong>: <strong>AddWindow Режим</strong>: <strong>Обычный</strong></span><span class="sxs-lookup"><span data-stu-id="dc3a0-169"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="dc3a0-170">Открывает форму "Товары".</span><span class="sxs-lookup"><span data-stu-id="dc3a0-170">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc3a0-171"><strong>ЗадатьЗначение</strong></span><span class="sxs-lookup"><span data-stu-id="dc3a0-171"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="dc3a0-172"><strong>Элемент</strong>: [Forms]![Товары]![КодПоставщика] <strong>Выражение</strong>: КодПоставщика</span><span class="sxs-lookup"><span data-stu-id="dc3a0-172"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="dc3a0-173">Задает в качестве значения элемента управления "КодПоставщика" текущего поставщика в форме "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="dc3a0-173">Set the SupplierID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc3a0-174"><strong>КЭлементуУправления</strong></span><span class="sxs-lookup"><span data-stu-id="dc3a0-174"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="dc3a0-175"><strong>Имя элемента управления</strong>: КодКатегории</span><span class="sxs-lookup"><span data-stu-id="dc3a0-175"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="dc3a0-176">Выполняет переход к элементу управления "КодКатегории".</span><span class="sxs-lookup"><span data-stu-id="dc3a0-176">Go to the CategoryID control.</span></span></p></td>
</tr>
</tbody>
</table>

