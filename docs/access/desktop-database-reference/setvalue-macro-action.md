---
title: Макрокоманда SetValue
TOCTitle: SetValue macro action
ms:assetid: a08be0c1-a053-45f9-b4ae-709fedc58e8b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820771(v=office.15)
ms:contentKeyID: 48546712
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 6b6f16c22e9265159c73279cfa1b2644adbc0277
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722692"
---
# <a name="setvalue-macro-action"></a><span data-ttu-id="ae4b1-102">Макрокоманда SetValue</span><span class="sxs-lookup"><span data-stu-id="ae4b1-102">SetValue macro action</span></span>

<span data-ttu-id="ae4b1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae4b1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ae4b1-104">Действие **SetValue** можно использовать для установки значения поля Microsoft Access, элемента управления или свойства на форме, форма таблицы или отчета.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-104">You can use the **SetValue** action to set the value of a Microsoft Access field, control, or property on a form, a form datasheet, or a report.</span></span>

> [!NOTE]
> - <span data-ttu-id="ae4b1-105">**Макрокоманды** нельзя использовать для задания значения свойства Access, которое возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-105">You cannot use the **SetValue** action to set the value of an Access property that returns an object.</span></span>
> - <span data-ttu-id="ae4b1-106">Это действие не разрешено, если база данных не является доверенной.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="ae4b1-107">Setting</span><span class="sxs-lookup"><span data-stu-id="ae4b1-107">Setting</span></span>

<span data-ttu-id="ae4b1-108">Действие **SetValue** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-108">The **SetValue** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae4b1-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="ae4b1-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="ae4b1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ae4b1-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae4b1-111"><strong>Элемент</strong></span><span class="sxs-lookup"><span data-stu-id="ae4b1-111"><strong>Item</strong></span></span></p></td>
<td><p><span data-ttu-id="ae4b1-112">Имя поля, элемента управления или свойства, значение которого требуется установить.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-112">The name of the field, control, or property whose value you want to set.</span></span> <span data-ttu-id="ae4b1-113">Введите имя поля, элемента управления или свойства в поле <strong>элемента</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-113">Enter the field, control, or property name in the <strong>Item</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="ae4b1-114">Необходимо использовать полный синтаксис для ссылки на элемент, например <em>ИмяЭлементаУправления</em> (для элемента управления в форму или отчет, из которого был вызван макрос) или <strong>форм</strong>! <em>имя_формы</em>! <em>ИмяЭлементаУправления</em>.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-114">You must use the full syntax to refer to this item, such as <em>controlname</em> (for a control on the form or report from which the macro was called) or <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>.</span></span> <span data-ttu-id="ae4b1-115">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-115">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae4b1-116"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="ae4b1-116"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="ae4b1-117">Выражение, которое доступа используется для задания значения для этого элемента.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-117">The expression Access uses to set the value for this item.</span></span> <span data-ttu-id="ae4b1-118">Всегда необходимо использовать полный синтаксис для ссылки на любые объекты в выражении.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-118">You must always use the full syntax to refer to any objects in the expression.</span></span> <span data-ttu-id="ae4b1-119">Например чтобы увеличить значение в элементе управления заработной платы в форме сотрудников на 10 процентов, используйте форм! Сотрудники! Заработной платы \* 1.1.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-119">For example, to increase the value in a Salary control on an Employees form by 10 percent, use Forms!Employees!Salary\*1.1.</span></span> <span data-ttu-id="ae4b1-120">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-120">This is a required argument.</span></span></p><p><span data-ttu-id="ae4b1-121"><strong>Примечание</strong>: в этом аргумент не следует использовать знак равенства (=) перед выражением.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-121"><strong>NOTE</strong>: You shouldn't use an equal sign (=) before the expression in this argument.</span></span> <span data-ttu-id="ae4b1-122">В противном случае Access применяет выражение, а затем использует это значение как выражение в этом аргументе.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-122">If you do, Access evaluates the expression and then uses this value as the expression in this argument.</span></span> <span data-ttu-id="ae4b1-123">Это может привести к непредсказуемым последствиям, если выражение — это строка.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-123">This can produce unexpected results if the expression is a string.</span></span></p>
<p><span data-ttu-id="ae4b1-124">Например, если ввести <strong> = &quot;String1&quot; </strong> для этого аргумента доступа сначала применяет выражение как String1.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-124">For example, if you type <strong>=&quot;String1&quot;</strong> for this argument, Access first evaluates the expression as String1.</span></span> <span data-ttu-id="ae4b1-125">Затем String1 используется как выражение в этом аргументе, чтобы найти элемент управления или свойство с именем String1 в форму или отчет, который называется макрос.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-125">Then it uses String1 as the expression in this argument, expecting to find a control or property named String1 on the form or report that called the macro.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="ae4b1-126">В базе данных Microsoft Access (MDB- или .accdb) нажмите кнопку **Построить** использовать построитель выражений для создания выражения для любого из этих аргументов.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-126">In an Access database (.mdb or .accdb), click the **Build** button to use the Expression Builder to create an expression for either of these arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae4b1-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="ae4b1-127">Remarks</span></span>

<span data-ttu-id="ae4b1-128">Это действие можно использовать для задания значения для поля или элемента управления на форме, форма таблицы или отчета.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-128">You can use this action to set a value for a field or control on a form, a form datasheet, or a report.</span></span> <span data-ttu-id="ae4b1-129">Также можно задать значение для практически во всех элемента управления, формы и свойства отчета в любом представлении.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-129">You can also set the value for almost all control, form, and report properties in any view.</span></span> <span data-ttu-id="ae4b1-130">Чтобы узнать, совместимо ли конкретному свойству можно задать с помощью макросов и представлений, к которым может быть задано, обратитесь к разделу справки для этого свойства в редакторе Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-130">To find out whether a particular property can be set by using a macro and which views it can be set in, see the Help topic for that property in the Visual Basic Editor.</span></span>

<span data-ttu-id="ae4b1-131">Также можно задать значение для поля в базовой таблице формы даже в том случае, если форма не содержит элемент управления, связанный с полем.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-131">You can also set the value for a field in a form's underlying table even if the form doesn't contain a control bound to the field.</span></span> <span data-ttu-id="ae4b1-132">Используйте синтаксис **форм**\!*имя_формы*\!*fieldname* в поле **элемента** , чтобы задать значение для такого поля.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-132">Use the syntax **Forms**\!*formname*\!*fieldname* in the **Item** box to set the value for such a field.</span></span> <span data-ttu-id="ae4b1-133">Можно найти на поле в базовой таблице отчета с помощью синтаксиса **отчеты**\!*имя_отчета*\!*fieldname*, но должен быть элемент управления для отчета, связанного с данным полем или поле должно быть описано в вычисляемый элемент управления в отчете.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-133">You can also refer to a field in a report's underlying table by using the syntax **Reports**\!*reportname*\!*fieldname*, but there must be a control on the report bound to this field, or the field must be referred to in a calculated control on the report.</span></span>

<span data-ttu-id="ae4b1-134">Если значение элемента управления в форме **ЗадатьЗначение** не приводит к возникновению правил проверки на уровне формы элемента управления, но его выдача правил проверки на уровне таблицы базового поля, если элемент управления связанный элемент управления.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-134">If you set the value of a control on a form, the **SetValue** action doesn't trigger the control's form-level validation rules, but it does trigger the underlying field's table-level validation rules if the control is a bound control.</span></span> <span data-ttu-id="ae4b1-135">Проверка условий **ЗадатьЗначение** , но пересчет может произойти не сразу.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-135">The **SetValue** action also triggers recalculation, but the recalculation may not happen immediately.</span></span> <span data-ttu-id="ae4b1-136">Для запуска немедленное обновление и принудительного повторного до завершения, используйте **ОбновитьОбъект** .</span><span class="sxs-lookup"><span data-stu-id="ae4b1-136">To trigger immediate repainting and force the recalculation to completion, use the **RepaintObject** action.</span></span> <span data-ttu-id="ae4b1-137">Значение, заданное в элементе управления с помощью **макрокоманды** не также влияет маски ввода в элемент управления или базовым **Маска** поля.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-137">The value you set in a control by using the **SetValue** action is also not affected by an input mask set in the control's or underlying field's **InputMask** property.</span></span>

<span data-ttu-id="ae4b1-138">Чтобы изменить значение элемента управления, можно использовать **макрокоманды** в макросе, указанном свойством события **AfterUpdate** элемента управления.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-138">To change the value of a control, you can use the **SetValue** action in a macro specified by the control's **AfterUpdate** event property.</span></span> <span data-ttu-id="ae4b1-139">Тем не менее нельзя использовать **макрокоманды** в макросе, указанном свойством событие **BeforeUpdate** элемента управления для изменения значения элемента управления (хотя **ЗадатьЗначение** можно использовать для изменения значения других элементов управления).</span><span class="sxs-lookup"><span data-stu-id="ae4b1-139">However, you can't use the **SetValue** action in a macro specified by a control's **BeforeUpdate** event property to change the value of the control (although you can use the **SetValue** action to change the value of other controls).</span></span> <span data-ttu-id="ae4b1-140">Можно также использовать **макрокоманды** в макросе, указанном свойством **до обновления** или **после обновления** формы для изменения значения всех элементов управления в текущей записи.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-140">You can also use the **SetValue** action in a macro specified by the **BeforeUpdate** or **AfterUpdate** property of a form to change the value of any controls in the current record.</span></span>

> [!NOTE]
> <span data-ttu-id="ae4b1-141">**Макрокоманды** нельзя использовать для задания значения следующих элементов управления:</span><span class="sxs-lookup"><span data-stu-id="ae4b1-141">You can't use the **SetValue** action to set the value of the following controls:</span></span>
> - <span data-ttu-id="ae4b1-142">Привязки элементов управления и вычисляемые элементы управления в отчетах.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-142">Bound controls and calculated controls on reports.</span></span>
> - <span data-ttu-id="ae4b1-143">Вычисляемые элементы управления в формах.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-143">Calculated controls on forms.</span></span>

> [!TIP]
> <span data-ttu-id="ae4b1-144">Чтобы скрыть или отобразить форму в представлении формы можно использовать **макрокоманды** .</span><span class="sxs-lookup"><span data-stu-id="ae4b1-144">You can use the **SetValue** action to hide or show a form in Form view.</span></span> <span data-ttu-id="ae4b1-145">Введите **форм**! \*имя_формы \***. Отображается** в поле **элемента** и **No** или **Да** в поле **выражение** .</span><span class="sxs-lookup"><span data-stu-id="ae4b1-145">Enter **Forms**!*formname\*\*\*.Visible*\* in the **Item** box, and **No** or **Yes** in the **Expression** box.</span></span> <span data-ttu-id="ae4b1-146">Установка для свойства **Visible** модальную форму **No** скрывает форму и делает ее немодальной.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-146">Setting a modal form's **Visible** property to **No** hides the form and makes it modeless.</span></span> <span data-ttu-id="ae4b1-147">Для свойства значение **Да** отображает форму и снова делает ее модальной.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-147">Setting the property to **Yes** displays the form and makes it modal again.</span></span>

<span data-ttu-id="ae4b1-148">При изменении значения или добавление новых данных в элементе управления с помощью **макрокоманды** в макросе не приводит к возникновению событиями, например **до обновления**, **до вставки**или **изменения** , возникающие при изменении или ввести данные в этих элементах управления в пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-148">Changing the value of or adding new data in a control by using the **SetValue** action in a macro doesn't trigger events such as **BeforeUpdate**, **BeforeInsert**, or **Change** that occur when you change or enter data in these controls in the user interface.</span></span> <span data-ttu-id="ae4b1-149">Эти события также не возникают при установке значения элемента управления с помощью Visual Basic для приложений (VBA) модуля.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-149">These events also don't occur if you set the value of the control by using a Visual Basic for Applications (VBA) module.</span></span>

<span data-ttu-id="ae4b1-150">Это действие недоступно в модуле VBA.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-150">This action isn't available in a VBA module.</span></span> <span data-ttu-id="ae4b1-151">Задайте значение непосредственно в VBA.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-151">Set the value directly in VBA.</span></span>

## <a name="example"></a><span data-ttu-id="ae4b1-152">Пример</span><span class="sxs-lookup"><span data-stu-id="ae4b1-152">Example</span></span>

<span data-ttu-id="ae4b1-153">**Задайте значение элемента управления с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="ae4b1-153">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="ae4b1-154">Следующий макрос открывает форму добавления продуктов с помощью кнопки на форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-154">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="ae4b1-155">Демонстрируется использование **эхо**, **CloseWindow**, **ОткрытьФорму**, **SetValue**и **КЭлементуУправления** действий.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-155">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="ae4b1-156">Действие **SetValue** задает КодПоставщика управления на форме продуктов для текущего поставщика в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-156">The **SetValue** action sets the SupplierID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="ae4b1-157">**Затем КЭлементуУправления** перемещает фокус в поле Идентификатор категории, где можно вводить данные для нового продукта.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-157">The **GoToControl** action then moves the focus to the CategoryID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="ae4b1-158">Этот макрос должен быть связан с кнопкой Добавить продукты в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-158">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae4b1-159">Action</span><span class="sxs-lookup"><span data-stu-id="ae4b1-159">Action</span></span></p></th>
<th><p><span data-ttu-id="ae4b1-160">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="ae4b1-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="ae4b1-161">Comment</span><span class="sxs-lookup"><span data-stu-id="ae4b1-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae4b1-162"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="ae4b1-162"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="ae4b1-163"><strong>Вывод на экран</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="ae4b1-163"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="ae4b1-164">Остановите обновление экрана в процессе выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-164">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae4b1-165"><strong>CloseWindow</strong></span><span class="sxs-lookup"><span data-stu-id="ae4b1-165"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="ae4b1-166"><strong>Тип объекта</strong>: <strong>FormObject имя</strong>: продукт списка <strong>Сохранить</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="ae4b1-166"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="ae4b1-167">Закройте форму списка продуктов.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-167">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae4b1-168"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="ae4b1-168"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="ae4b1-169"><strong>Имя формы</strong>: продуктов <strong>представления</strong>: <strong>FormData режима</strong>: <strong>Режим AddWindow</strong>: <strong>Обычный</strong></span><span class="sxs-lookup"><span data-stu-id="ae4b1-169"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="ae4b1-170">Откройте форму продуктов.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-170">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae4b1-171"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="ae4b1-171"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="ae4b1-172"><strong>Элемент</strong>: [формы]! [Товары]! [Код поставщика] <strong>Выражение</strong>: КодПоставщика</span><span class="sxs-lookup"><span data-stu-id="ae4b1-172"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="ae4b1-173">Значение элемента управления КодПоставщика текущего поставщика в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-173">Set the SupplierID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae4b1-174"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="ae4b1-174"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="ae4b1-175"><strong>Имя элемента управления</strong>: идентификатор категории</span><span class="sxs-lookup"><span data-stu-id="ae4b1-175"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="ae4b1-176">Перейдите к элементу управления идентификатор категории.</span><span class="sxs-lookup"><span data-stu-id="ae4b1-176">Go to the CategoryID control.</span></span></p></td>
</tr>
</tbody>
</table>

