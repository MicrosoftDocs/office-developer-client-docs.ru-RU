---
title: Макрокоманда GoToControl
TOCTitle: GoToControl macro action
ms:assetid: caff76dc-7ca8-4f87-8144-89445ed4600d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834370(v=office.15)
ms:contentKeyID: 48547705
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c056f2b0922402ea7cde7cf767969b73f912f572
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292169"
---
# <a name="gotocontrol-macro-action"></a><span data-ttu-id="b466b-102">Макрокоманда GoToControl</span><span class="sxs-lookup"><span data-stu-id="b466b-102">GoToControl macro action</span></span>

<span data-ttu-id="b466b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b466b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b466b-104">Чтобы переместить фокус на указанное поле или элемент управления в текущей записи открытой формы, таблицы формы, таблицы или запроса в режиме таблицы, можно использовать макрокоманду **КЭлементуУправления (КЭлементуУправления** ).</span><span class="sxs-lookup"><span data-stu-id="b466b-104">You can use the **GoToControl** action to move the focus to the specified field or control in the current record of the open form, form datasheet, table datasheet, or query datasheet.</span></span> <span data-ttu-id="b466b-105">Эта макрокоманда позволяет переместить фокус на определенное поле или на другой элемент управления.</span><span class="sxs-lookup"><span data-stu-id="b466b-105">You can use this action when you want a particular field or control to have the focus.</span></span> <span data-ttu-id="b466b-106">Затем это поле или элемент управления можно использовать для сравнения или макрокоманд **НайтиЗапись** .</span><span class="sxs-lookup"><span data-stu-id="b466b-106">This field or control can then be used for comparisons or **FindRecord** actions.</span></span> <span data-ttu-id="b466b-107">Кроме того, можно использовать эту макрокоманду для навигации в форме в соответствии с определенными условиями.</span><span class="sxs-lookup"><span data-stu-id="b466b-107">You can also use this action to navigate in a form according to certain conditions.</span></span> <span data-ttu-id="b466b-108">Например, если пользователь введет "Нет" в элементе управления "Брак" формы медицинского страхования, фокус может сразу автоматически переместиться на элемент управления, следующий за элементом управления "Имя партнера".</span><span class="sxs-lookup"><span data-stu-id="b466b-108">For example, if the user enters No in a Married control on a health insurance form, the focus can automatically skip the Spouse/partner Name control and move to the next control.</span></span>

## <a name="setting"></a><span data-ttu-id="b466b-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="b466b-109">Setting</span></span>

> [!NOTE]
> <span data-ttu-id="b466b-110">Это действие недоступно для использования со страницами доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="b466b-110">This action is not available for use with data access pages.</span></span>

<span data-ttu-id="b466b-111">Макрокоманда **GoToControl** имеет указанный ниже аргумент.</span><span class="sxs-lookup"><span data-stu-id="b466b-111">The **GoToControl** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b466b-112">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="b466b-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b466b-113">Описание</span><span class="sxs-lookup"><span data-stu-id="b466b-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b466b-114"><strong>Имя элемента управления</strong></span><span class="sxs-lookup"><span data-stu-id="b466b-114"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="b466b-115">Имя поля или элемента управления, куда необходимо переместить фокус.</span><span class="sxs-lookup"><span data-stu-id="b466b-115">The name of the field or control where you want the focus.</span></span> <span data-ttu-id="b466b-116">Введите имя поля или элемента управления в поле <strong>имя элемента</strong> управления в разделе <strong>аргументы макрокоманды</strong> в области построителя макросов.</span><span class="sxs-lookup"><span data-stu-id="b466b-116">Enter the field or control name in the <strong>Control Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="b466b-117">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="b466b-117">This is a required argument.</span></span></p>
<p><span data-ttu-id="b466b-118"><strong>Note</strong>: введите только имя поля или элемента управления в аргументе <strong>имя элемента управления</strong> , а не полный идентификатор, например Forms! Продуктов! [Product ID].</span><span class="sxs-lookup"><span data-stu-id="b466b-118"><strong>NOTE</strong>: Enter only the name of the field or control in the <strong>Control Name</strong> argument, not the fully qualified identifier, such as Forms!Products![Product ID].</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b466b-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="b466b-119">Remarks</span></span>

<span data-ttu-id="b466b-120">Нельзя использовать макрокоманду **КЭлементуУправления** для перемещения фокуса на элемент управления в скрытой форме.</span><span class="sxs-lookup"><span data-stu-id="b466b-120">You cannot use the **GoToControl** action to move the focus to a control on a hidden form.</span></span>

> [!TIP]
> <span data-ttu-id="b466b-121">С помощью макрокоманды **КЭлементуУправления** можно перейти к подчиненной форме, которая представляет собой тип элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b466b-121">You can use the **GoToControl** action to move to a subform, which is a type of control.</span></span> <span data-ttu-id="b466b-122">Затем можно использовать макрокоманду **GoToRecord (GoToRecord** ) для перехода к определенной записи в подчиненной форме.</span><span class="sxs-lookup"><span data-stu-id="b466b-122">You can then use the **GoToRecord** action to move to a particular record in the subform.</span></span> <span data-ttu-id="b466b-123">Вы также можете перейти к элементу управления в подчиненной форме, используя макрокоманду **КЭлементуУправления (КЭлементуУправления** ), чтобы перейти к подчиненной форме, а затем к элементу управления в подчиненной форме.</span><span class="sxs-lookup"><span data-stu-id="b466b-123">You can also move to a control on a subform by using the **GoToControl** action to move first to the subform and then to the control on the subform.</span></span>

<span data-ttu-id="b466b-124">Чтобы выполнить макрокоманду **КЭлементуУправления** в модуле Visual Basic для приложений (VBA), используйте метод **КЭлементуУправления** объекта DoCmd. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="b466b-124">To run the **GoToControl** action in a Visual Basic for Applications (VBA) module, use the **GoToControl** method of the **DoCmd** object.</span></span> <span data-ttu-id="b466b-125">Кроме того, можно использовать метод **SetFocus** для перемещения фокуса на элемент управления в форме или любой из его подчиненных форм или в поле в таблице в режиме таблицы, запросе или форме.</span><span class="sxs-lookup"><span data-stu-id="b466b-125">You can also use the **SetFocus** method to move the focus to a control on a form or any of its subforms, or to a field in an open table, query, or form datasheet.</span></span>

## <a name="examples"></a><span data-ttu-id="b466b-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="b466b-126">Examples</span></span>

<span data-ttu-id="b466b-127">**Задание значения элемента управления с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="b466b-127">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="b466b-128">Следующий макрос открывает форму "Добавление продуктов" на кнопке в форме "поставщики".</span><span class="sxs-lookup"><span data-stu-id="b466b-128">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="b466b-129">В нем показано использование действий **echo**, **клосевиндов**, **OpenForm**, **SetValue**и **КЭлементуУправления** .</span><span class="sxs-lookup"><span data-stu-id="b466b-129">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="b466b-130">Действие **SetValue** устанавливает для элемента управления "идентификатор поставщика" в форме "продукты" текущего поставщика в форме "поставщики".</span><span class="sxs-lookup"><span data-stu-id="b466b-130">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="b466b-131">После этого действие " **КЭлементуУправления** " переместит фокус на поле "идентификатор категории", в котором можно начать ввод данных для нового продукта.</span><span class="sxs-lookup"><span data-stu-id="b466b-131">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="b466b-132">Этот макрос должен быть присоединен к кнопке "добавить продукты" в форме "поставщики".</span><span class="sxs-lookup"><span data-stu-id="b466b-132">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b466b-133">Действие</span><span class="sxs-lookup"><span data-stu-id="b466b-133">Action</span></span></p></th>
<th><p><span data-ttu-id="b466b-134">Аргументы: Настройка</span><span class="sxs-lookup"><span data-stu-id="b466b-134">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="b466b-135">Комментарий</span><span class="sxs-lookup"><span data-stu-id="b466b-135">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b466b-136"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="b466b-136"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="b466b-137"><strong>Echo on</strong>: <strong>нет</strong></span><span class="sxs-lookup"><span data-stu-id="b466b-137"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="b466b-138">Остановить обновление экрана во время выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="b466b-138">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b466b-139"><strong>Клосевиндов</strong></span><span class="sxs-lookup"><span data-stu-id="b466b-139"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="b466b-140"><strong>Тип объекта</strong>: <strong>Формобжект Name</strong>: List Product <strong>Save</strong>: <strong>No</strong></span><span class="sxs-lookup"><span data-stu-id="b466b-140"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="b466b-141">Закройте форму "список товаров".</span><span class="sxs-lookup"><span data-stu-id="b466b-141">Close Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b466b-142"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="b466b-142"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="b466b-143"><strong>Имя формы</strong>: " <strong>Просмотр</strong>продуктов: <strong>режим формдата</strong>: режим <strong>аддвиндов</strong>: <strong>обычный</strong> "</span><span class="sxs-lookup"><span data-stu-id="b466b-143"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="b466b-144">Откройте форму продукты.</span><span class="sxs-lookup"><span data-stu-id="b466b-144">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b466b-145"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="b466b-145"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="b466b-146"><strong>Элемент</strong>: [Forms]! [Products]! Ключев <strong>Выражение</strong>: КодПоставщика</span><span class="sxs-lookup"><span data-stu-id="b466b-146"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="b466b-147">В форме Поставщики задайте для элемента управления "идентификатор поставщика" текущего поставщика.</span><span class="sxs-lookup"><span data-stu-id="b466b-147">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b466b-148"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="b466b-148"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="b466b-149"><strong>Имя элемента управления</strong>: КодТипа</span><span class="sxs-lookup"><span data-stu-id="b466b-149"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="b466b-150">Перейдите к элементу управления ИДЕНТИФИКАТОРом категории.</span><span class="sxs-lookup"><span data-stu-id="b466b-150">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b466b-151">**Проверка данных с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="b466b-151">**Validate data by using a macro**</span></span>

<span data-ttu-id="b466b-152">Следующий макрос проверки проверяет почтовые индексы, введенные в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="b466b-152">The following validation macro checks the postal codes entered in a Suppliers form.</span></span> <span data-ttu-id="b466b-153">В нем показано использование действий **Макрокоманда StopMacro**, **MessageBox**, **Макрокоманда CancelEvent**и **КЭлементуУправления** .</span><span class="sxs-lookup"><span data-stu-id="b466b-153">It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions.</span></span> <span data-ttu-id="b466b-154">Условное выражение проверяет страну, регион и почтовый индекс, введенные в записи в форме.</span><span class="sxs-lookup"><span data-stu-id="b466b-154">A conditional expression checks the country/region and postal code entered in a record on the form.</span></span> <span data-ttu-id="b466b-155">Если почтовый индекс находится в неправильном формате для страны или региона, макрос выводит окно сообщения и отменяет сохранение записи.</span><span class="sxs-lookup"><span data-stu-id="b466b-155">If the postal code is not in the right format for the country/region, the macro displays a message box and cancels saving the record.</span></span> <span data-ttu-id="b466b-156">После этого макрос вернется к элементу управления почтового кода, где можно исправить ошибку.</span><span class="sxs-lookup"><span data-stu-id="b466b-156">The macro then returns you to the Postal Code control, where you can correct the error.</span></span> <span data-ttu-id="b466b-157">Этот макрос необходимо вложить в свойство **BeforeUpdate** формы "поставщики".</span><span class="sxs-lookup"><span data-stu-id="b466b-157">This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b466b-158">Условие</span><span class="sxs-lookup"><span data-stu-id="b466b-158">Condition</span></span></p></th>
<th><p><span data-ttu-id="b466b-159">Действие</span><span class="sxs-lookup"><span data-stu-id="b466b-159">Action</span></span></p></th>
<th><p><span data-ttu-id="b466b-160">Аргументы: Настройка</span><span class="sxs-lookup"><span data-stu-id="b466b-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="b466b-161">Комментарий</span><span class="sxs-lookup"><span data-stu-id="b466b-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b466b-162">IsNull ([страна])</span><span class="sxs-lookup"><span data-stu-id="b466b-162">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="b466b-163"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="b466b-163"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b466b-164">Если страна имеет <strong>значение NULL</strong>, почтовый индекс не может быть проверен.</span><span class="sxs-lookup"><span data-stu-id="b466b-164">If CountryRegion is <strong>Null</strong>, postal code cannot be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b466b-165">Ватикан В (&quot;Франция&quot;,&quot;Италия&quot;,&quot;Испания&quot;) и len ([почтовый индекс]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="b466b-165">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([Postal Code]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="b466b-166"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="b466b-166"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="b466b-167"><strong>Сообщение</strong>: длина почтового индекса не должна превышать 5 символов.</span><span class="sxs-lookup"><span data-stu-id="b466b-167"><strong>Message</strong>: The postal code must be 5 characters.</span></span> <span data-ttu-id="b466b-168"><strong>Гудок</strong>: <strong>естипе</strong>: <strong>Информатионтитле</strong>: ошибка почтового кода</span><span class="sxs-lookup"><span data-stu-id="b466b-168"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="b466b-169">Если почтовый индекс не состоит из 5 символов, отобразится сообщение.</span><span class="sxs-lookup"><span data-stu-id="b466b-169">If the postal code is not 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b466b-170">...</span><span class="sxs-lookup"><span data-stu-id="b466b-170"></span></span></p></td>
<td><p><span data-ttu-id="b466b-171"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="b466b-171"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b466b-172">Отмена события.</span><span class="sxs-lookup"><span data-stu-id="b466b-172">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="b466b-173"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="b466b-173"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="b466b-174"><strong>Имя элемента управления</strong>: PostalCode</span><span class="sxs-lookup"><span data-stu-id="b466b-174"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b466b-175">Ватикан В (&quot;Австралия&quot;,&quot;Сингапур&quot;) и len ([почтовый индекс]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="b466b-175">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([Postal Code]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="b466b-176"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="b466b-176"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="b466b-177">Сообщение: почтовый индекс должен иметь 4 символа.</span><span class="sxs-lookup"><span data-stu-id="b466b-177">Message: The postal code must be 4 characters.</span></span> <span data-ttu-id="b466b-178"><strong>Гудок</strong>: <strong>естипе</strong>: <strong>Информатионтитле</strong>: ошибка почтового кода</span><span class="sxs-lookup"><span data-stu-id="b466b-178"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="b466b-179">Если почтовый индекс не состоит из 4 символов, отобразится сообщение.</span><span class="sxs-lookup"><span data-stu-id="b466b-179">If the postal code is not 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b466b-180">...</span><span class="sxs-lookup"><span data-stu-id="b466b-180"></span></span></p></td>
<td><p><span data-ttu-id="b466b-181"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="b466b-181"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b466b-182">Отмена события.</span><span class="sxs-lookup"><span data-stu-id="b466b-182">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="b466b-183"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="b466b-183"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="b466b-184"><strong>Имя элемента управления</strong>: PostalCode</span><span class="sxs-lookup"><span data-stu-id="b466b-184"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b466b-185">([Страна] = &quot;Канада&quot;) And ([почтовый индекс] не похоже&quot;на [A-z] [0-9] [A-z] [0-9] [A-z] [0-9&quot;])</span><span class="sxs-lookup"><span data-stu-id="b466b-185">([CountryRegion] = &quot;Canada&quot;) And ([Postal Code] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="b466b-186"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="b466b-186"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="b466b-187"><strong>Сообщение</strong>: недопустимый почтовый индекс.</span><span class="sxs-lookup"><span data-stu-id="b466b-187"><strong>Message</strong>: The postal code is not valid.</span></span> <span data-ttu-id="b466b-188">Пример кода канадского канадского: H1J 1C3 <strong>Beep</strong>: <strong>естипе</strong>: <strong>Информатионтитле</strong>: ошибка почтового кода</span><span class="sxs-lookup"><span data-stu-id="b466b-188">Example of Canadian code: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="b466b-189">Если почтовый индекс неправилен для Канады, отобразите сообщение.</span><span class="sxs-lookup"><span data-stu-id="b466b-189">If the postal code is not correct for Canada, display a message.</span></span> <span data-ttu-id="b466b-190">(Пример канадского кода: H1J 1C3)</span><span class="sxs-lookup"><span data-stu-id="b466b-190">(Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b466b-191">...</span><span class="sxs-lookup"><span data-stu-id="b466b-191"></span></span></p></td>
<td><p><span data-ttu-id="b466b-192"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="b466b-192"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b466b-193">Отмена события.</span><span class="sxs-lookup"><span data-stu-id="b466b-193">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

