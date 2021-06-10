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
# <a name="gotocontrol-macro-action"></a><span data-ttu-id="b9b27-102">Макрокоманда GoToControl</span><span class="sxs-lookup"><span data-stu-id="b9b27-102">GoToControl macro action</span></span>

<span data-ttu-id="b9b27-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b9b27-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b9b27-104">Действие **GoToControl** можно использовать для перемещения фокуса в указанное поле или управление в текущей записи открытой формы, таблицы данных форм, таблицы данных или таблицы данных запросов.</span><span class="sxs-lookup"><span data-stu-id="b9b27-104">You can use the **GoToControl** action to move the focus to the specified field or control in the current record of the open form, form datasheet, table datasheet, or query datasheet.</span></span> <span data-ttu-id="b9b27-105">Эта макрокоманда позволяет переместить фокус на определенное поле или на другой элемент управления.</span><span class="sxs-lookup"><span data-stu-id="b9b27-105">You can use this action when you want a particular field or control to have the focus.</span></span> <span data-ttu-id="b9b27-106">Затем это поле или управление можно использовать для сопоставлений или **действий FindRecord.**</span><span class="sxs-lookup"><span data-stu-id="b9b27-106">This field or control can then be used for comparisons or **FindRecord** actions.</span></span> <span data-ttu-id="b9b27-107">Кроме того, можно использовать эту макрокоманду для навигации в форме в соответствии с определенными условиями.</span><span class="sxs-lookup"><span data-stu-id="b9b27-107">You can also use this action to navigate in a form according to certain conditions.</span></span> <span data-ttu-id="b9b27-108">Например, если пользователь введет "Нет" в элементе управления "Брак" формы медицинского страхования, фокус может сразу автоматически переместиться на элемент управления, следующий за элементом управления "Имя партнера".</span><span class="sxs-lookup"><span data-stu-id="b9b27-108">For example, if the user enters No in a Married control on a health insurance form, the focus can automatically skip the Spouse/partner Name control and move to the next control.</span></span>

## <a name="setting"></a><span data-ttu-id="b9b27-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="b9b27-109">Setting</span></span>

> [!NOTE]
> <span data-ttu-id="b9b27-110">Это действие не доступно для использования со страницами доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="b9b27-110">This action is not available for use with data access pages.</span></span>

<span data-ttu-id="b9b27-111">Макрокоманда **GoToControl** имеет указанный ниже аргумент.</span><span class="sxs-lookup"><span data-stu-id="b9b27-111">The **GoToControl** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b9b27-112">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="b9b27-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b9b27-113">Описание</span><span class="sxs-lookup"><span data-stu-id="b9b27-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9b27-114"><strong>Имя элемента управления</strong></span><span class="sxs-lookup"><span data-stu-id="b9b27-114"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b27-115">Имя поля или элемента управления, куда необходимо переместить фокус.</span><span class="sxs-lookup"><span data-stu-id="b9b27-115">The name of the field or control where you want the focus.</span></span> <span data-ttu-id="b9b27-116">Введите поле или имя управления в поле <strong>Имя</strong> управления в разделе <strong>Аргументы</strong> действий области Macro Builder.</span><span class="sxs-lookup"><span data-stu-id="b9b27-116">Enter the field or control name in the <strong>Control Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="b9b27-117">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="b9b27-117">This is a required argument.</span></span></p>
<p><span data-ttu-id="b9b27-118"><strong>ПРИМЕЧАНИЕ.</strong>Введите только имя поля или управления в <strong>аргументе Имя</strong> управления, а не полностью квалифицированный идентификатор, например Forms! Продукты! [ID продукта].</span><span class="sxs-lookup"><span data-stu-id="b9b27-118"><strong>NOTE</strong>: Enter only the name of the field or control in the <strong>Control Name</strong> argument, not the fully qualified identifier, such as Forms!Products![Product ID].</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b9b27-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="b9b27-119">Remarks</span></span>

<span data-ttu-id="b9b27-120">Действие **GoToControl** нельзя использовать для перемещения фокуса на управление скрытой формой.</span><span class="sxs-lookup"><span data-stu-id="b9b27-120">You cannot use the **GoToControl** action to move the focus to a control on a hidden form.</span></span>

> [!TIP]
> <span data-ttu-id="b9b27-121">Действие **GoToControl** можно использовать для перемещения в подформу, которая является типом управления.</span><span class="sxs-lookup"><span data-stu-id="b9b27-121">You can use the **GoToControl** action to move to a subform, which is a type of control.</span></span> <span data-ttu-id="b9b27-122">Затем можно использовать **действие GoToRecord** для перемещения к определенной записи в подформе.</span><span class="sxs-lookup"><span data-stu-id="b9b27-122">You can then use the **GoToRecord** action to move to a particular record in the subform.</span></span> <span data-ttu-id="b9b27-123">Вы также можете перейти на управление в подформе с помощью действия **GoToControl** для перемещения сначала в подформу, а затем в управление в подформе.</span><span class="sxs-lookup"><span data-stu-id="b9b27-123">You can also move to a control on a subform by using the **GoToControl** action to move first to the subform and then to the control on the subform.</span></span>

<span data-ttu-id="b9b27-124">Чтобы выполнить **действие GoToControl** в модуле Visual Basic для приложений (VBA), используйте метод **GoToControl** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="b9b27-124">To run the **GoToControl** action in a Visual Basic for Applications (VBA) module, use the **GoToControl** method of the **DoCmd** object.</span></span> <span data-ttu-id="b9b27-125">Вы также можете использовать метод **SetFocus,** чтобы переместить фокус на управление на форму или любую из ее подформ или в поле в открытой таблице, запросе или таблице данных форм.</span><span class="sxs-lookup"><span data-stu-id="b9b27-125">You can also use the **SetFocus** method to move the focus to a control on a form or any of its subforms, or to a field in an open table, query, or form datasheet.</span></span>

## <a name="examples"></a><span data-ttu-id="b9b27-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="b9b27-126">Examples</span></span>

<span data-ttu-id="b9b27-127">**Установка значения элемента управления с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="b9b27-127">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="b9b27-128">Следующий макрос открывает форму "Добавить товары" с помощью кнопки в форме "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="b9b27-128">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="b9b27-129">Он демонстрирует применение макрокоманд **ВыводНаЭкран**, **ЗакрытьОкно**, **ОткрытьФорму**, **ЗадатьЗначение** и **КЭлементуУправления**.</span><span class="sxs-lookup"><span data-stu-id="b9b27-129">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="b9b27-130">Действие **SetValue задает** контроль поставщика в форме Продуктов текущему поставщику в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="b9b27-130">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="b9b27-131">Затем **действие GoToControl** перемещает фокус в поле Category ID, где можно начать ввод данных для нового продукта.</span><span class="sxs-lookup"><span data-stu-id="b9b27-131">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="b9b27-132">Этот макрос должен быть привязан к кнопке "Добавить товары" в форме "Поставщики".</span><span class="sxs-lookup"><span data-stu-id="b9b27-132">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b9b27-133">Макрокоманда</span><span class="sxs-lookup"><span data-stu-id="b9b27-133">Action</span></span></p></th>
<th><p><span data-ttu-id="b9b27-134">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="b9b27-134">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="b9b27-135">Примечание</span><span class="sxs-lookup"><span data-stu-id="b9b27-135">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9b27-136"><strong>ВыводНаЭкран</strong></span><span class="sxs-lookup"><span data-stu-id="b9b27-136"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b27-137"><strong>Включить вывод</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="b9b27-137"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b27-138">Приостанавливает обновление экрана, пока выполняется макрос.</span><span class="sxs-lookup"><span data-stu-id="b9b27-138">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b27-139"><strong>ЗакрытьОкно</strong></span><span class="sxs-lookup"><span data-stu-id="b9b27-139"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b27-140"><strong>Тип объекта</strong>: <strong>FormObject Имя</strong>: Список товаров <strong>Сохранить</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="b9b27-140"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b27-141">Закрыть форму списка продуктов.</span><span class="sxs-lookup"><span data-stu-id="b9b27-141">Close Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b27-142"><strong>ОткрытьФорму</strong></span><span class="sxs-lookup"><span data-stu-id="b9b27-142"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b27-143"><strong>Имя формы</strong>: Товары <strong>Представление</strong>: <strong>FormData Режим</strong>: <strong>AddWindow Режим</strong>: <strong>Обычный</strong></span><span class="sxs-lookup"><span data-stu-id="b9b27-143"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b27-144">Открывает форму "Товары".</span><span class="sxs-lookup"><span data-stu-id="b9b27-144">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b27-145"><strong>ЗадатьЗначение</strong></span><span class="sxs-lookup"><span data-stu-id="b9b27-145"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b27-146"><strong>Элемент</strong>: [Forms]![Товары]![КодПоставщика] <strong>Выражение</strong>: КодПоставщика</span><span class="sxs-lookup"><span data-stu-id="b9b27-146"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="b9b27-147">Установите контроль поставщика для текущего поставщика в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="b9b27-147">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b27-148"><strong>КЭлементуУправления</strong></span><span class="sxs-lookup"><span data-stu-id="b9b27-148"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b27-149"><strong>Имя элемента управления</strong>: КодКатегории</span><span class="sxs-lookup"><span data-stu-id="b9b27-149"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="b9b27-150">Перейдите к контролю category ID.</span><span class="sxs-lookup"><span data-stu-id="b9b27-150">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b9b27-151">**Проверка данных с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="b9b27-151">**Validate data by using a macro**</span></span>

<span data-ttu-id="b9b27-152">Следующий макрос проверки проверяет почтовые коды, вступив в форму Поставщики.</span><span class="sxs-lookup"><span data-stu-id="b9b27-152">The following validation macro checks the postal codes entered in a Suppliers form.</span></span> <span data-ttu-id="b9b27-153">В нем показано использование действий **StopMacro,** **MessageBox,** **CancelEvent** и **GoToControl.**</span><span class="sxs-lookup"><span data-stu-id="b9b27-153">It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions.</span></span> <span data-ttu-id="b9b27-154">Условное выражение проверяет страну/регион и почтовый код, вписаный в запись в форме.</span><span class="sxs-lookup"><span data-stu-id="b9b27-154">A conditional expression checks the country/region and postal code entered in a record on the form.</span></span> <span data-ttu-id="b9b27-155">Если почтовый код не находится в нужном формате для страны или региона, макрос отображает окно сообщений и отменяет сохранение записи.</span><span class="sxs-lookup"><span data-stu-id="b9b27-155">If the postal code is not in the right format for the country/region, the macro displays a message box and cancels saving the record.</span></span> <span data-ttu-id="b9b27-156">Затем макрос возвращает вас в пункт управления почтовым кодом, где можно исправить ошибку.</span><span class="sxs-lookup"><span data-stu-id="b9b27-156">The macro then returns you to the Postal Code control, where you can correct the error.</span></span> <span data-ttu-id="b9b27-157">Этот макрос должен быть присоединен к свойству **BeforeUpdate** формы Поставщики.</span><span class="sxs-lookup"><span data-stu-id="b9b27-157">This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b9b27-158">Условие</span><span class="sxs-lookup"><span data-stu-id="b9b27-158">Condition</span></span></p></th>
<th><p><span data-ttu-id="b9b27-159">Макрокоманда</span><span class="sxs-lookup"><span data-stu-id="b9b27-159">Action</span></span></p></th>
<th><p><span data-ttu-id="b9b27-160">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="b9b27-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="b9b27-161">Примечание</span><span class="sxs-lookup"><span data-stu-id="b9b27-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9b27-162">IsNull([CountryRegion])</span><span class="sxs-lookup"><span data-stu-id="b9b27-162">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="b9b27-163"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="b9b27-163"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b9b27-164">Если CountryRegion <strong>является Null,</strong>почтовый код не может быть проверен.</span><span class="sxs-lookup"><span data-stu-id="b9b27-164">If CountryRegion is <strong>Null</strong>, postal code cannot be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b27-165">[CountryRegion] В ( &quot; &quot; Франция, &quot; &quot; Италия, &quot; Испания &quot; ) и Len ([Почтовый код]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="b9b27-165">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([Postal Code]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="b9b27-166"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="b9b27-166"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b27-167"><strong>Сообщение.</strong>Почтовый код должен быть 5 символов.</span><span class="sxs-lookup"><span data-stu-id="b9b27-167"><strong>Message</strong>: The postal code must be 5 characters.</span></span> <span data-ttu-id="b9b27-168"><strong>Звуковой сигнал</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Ошибка почтового кода</span><span class="sxs-lookup"><span data-stu-id="b9b27-168"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="b9b27-169">Если почтовый код не 5 символов, отобразить сообщение.</span><span class="sxs-lookup"><span data-stu-id="b9b27-169">If the postal code is not 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b27-170">...</span><span class="sxs-lookup"><span data-stu-id="b9b27-170">...</span></span></p></td>
<td><p><span data-ttu-id="b9b27-171"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="b9b27-171"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b9b27-172">Отмена события.</span><span class="sxs-lookup"><span data-stu-id="b9b27-172">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="b9b27-173"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="b9b27-173"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b27-174"><strong>Имя управления:</strong>PostalCode</span><span class="sxs-lookup"><span data-stu-id="b9b27-174"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b27-175">[CountryRegion] В ( &quot; Австралия , Сингапур ) и &quot; &quot; &quot; Len ([Почтовый код]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="b9b27-175">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([Postal Code]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="b9b27-176"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="b9b27-176"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b27-177">Сообщение. Почтовый код должен быть 4 символа.</span><span class="sxs-lookup"><span data-stu-id="b9b27-177">Message: The postal code must be 4 characters.</span></span> <span data-ttu-id="b9b27-178"><strong>Звуковой сигнал</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Ошибка почтового кода</span><span class="sxs-lookup"><span data-stu-id="b9b27-178"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="b9b27-179">Если почтовый код не 4 символа, отобразить сообщение.</span><span class="sxs-lookup"><span data-stu-id="b9b27-179">If the postal code is not 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b27-180">...</span><span class="sxs-lookup"><span data-stu-id="b9b27-180">...</span></span></p></td>
<td><p><span data-ttu-id="b9b27-181"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="b9b27-181"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b9b27-182">Отмена события.</span><span class="sxs-lookup"><span data-stu-id="b9b27-182">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="b9b27-183"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="b9b27-183"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b27-184"><strong>Имя управления:</strong>PostalCode</span><span class="sxs-lookup"><span data-stu-id="b9b27-184"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b27-185">([CountryRegion] = &quot; Канада ) и &quot; ([Почтовый код] Не нравится &quot; [A-Z][0-9][A-Z] [0-9][A-Z][0-9] &quot; )</span><span class="sxs-lookup"><span data-stu-id="b9b27-185">([CountryRegion] = &quot;Canada&quot;) And ([Postal Code] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="b9b27-186"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="b9b27-186"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b27-187"><strong>Сообщение.</strong>Почтовый код не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="b9b27-187"><strong>Message</strong>: The postal code is not valid.</span></span> <span data-ttu-id="b9b27-188">Пример канадского кода: сигнал H1J 1C3 <strong></strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Ошибка почтового кода</span><span class="sxs-lookup"><span data-stu-id="b9b27-188">Example of Canadian code: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="b9b27-189">Если почтовый код не является правильным для Канады, отобразить сообщение.</span><span class="sxs-lookup"><span data-stu-id="b9b27-189">If the postal code is not correct for Canada, display a message.</span></span> <span data-ttu-id="b9b27-190">(Пример канадского кода: H1J 1C3)</span><span class="sxs-lookup"><span data-stu-id="b9b27-190">(Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b27-191">...</span><span class="sxs-lookup"><span data-stu-id="b9b27-191">...</span></span></p></td>
<td><p><span data-ttu-id="b9b27-192"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="b9b27-192"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b9b27-193">Отмена события.</span><span class="sxs-lookup"><span data-stu-id="b9b27-193">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

