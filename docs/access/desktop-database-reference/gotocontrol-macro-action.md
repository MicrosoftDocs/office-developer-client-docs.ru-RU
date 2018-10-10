---
title: GoToControl Macro Action
TOCTitle: GoToControl Macro Action
ms:assetid: caff76dc-7ca8-4f87-8144-89445ed4600d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834370(v=office.15)
ms:contentKeyID: 48547705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2617544bf04aa0b26ccbb9d7ce8d7329d42ed1e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481286"
---
# <a name="gotocontrol-macro-action"></a><span data-ttu-id="ec06a-102">GoToControl Macro Action</span><span class="sxs-lookup"><span data-stu-id="ec06a-102">GoToControl Macro Action</span></span>


<span data-ttu-id="ec06a-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec06a-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="ec06a-104">Можно использовать **КЭлементуУправления** для перемещения фокуса указанного поля или элемента управления в записи текущей открытой формы, формы, таблицы или запроса таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="ec06a-104">You can use the **GoToControl** action to move the focus to the specified field or control in the current record of the open form, form datasheet, table datasheet, or query datasheet.</span></span> <span data-ttu-id="ec06a-105">Эта макрокоманда позволяет переместить фокус на определенное поле или на другой элемент управления.</span><span class="sxs-lookup"><span data-stu-id="ec06a-105">You can use this action when you want a particular field or control to have the focus.</span></span> <span data-ttu-id="ec06a-106">В этом поле или элемент управления затем используется для сравнения или **НайтиЗапись** действий.</span><span class="sxs-lookup"><span data-stu-id="ec06a-106">This field or control can then be used for comparisons or **FindRecord** actions.</span></span> <span data-ttu-id="ec06a-107">Кроме того, можно использовать эту макрокоманду для навигации в форме в соответствии с определенными условиями.</span><span class="sxs-lookup"><span data-stu-id="ec06a-107">You can also use this action to navigate in a form according to certain conditions.</span></span> <span data-ttu-id="ec06a-108">Например, если пользователь введет "Нет" в элементе управления "Брак" формы медицинского страхования, фокус может сразу автоматически переместиться на элемент управления, следующий за элементом управления "Имя партнера".</span><span class="sxs-lookup"><span data-stu-id="ec06a-108">For example, if the user enters No in a Married control on a health insurance form, the focus can automatically skip the Spouse/partner Name control and move to the next control.</span></span>

## <a name="setting"></a><span data-ttu-id="ec06a-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="ec06a-109">Setting</span></span>


> [!NOTE]
> <P><span data-ttu-id="ec06a-110">Это действие недоступно для использования с страницы доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="ec06a-110">This action is not available for use with data access pages.</span></span></P>



<span data-ttu-id="ec06a-111">Макрокоманда **GoToControl** имеет указанный ниже аргумент.</span><span class="sxs-lookup"><span data-stu-id="ec06a-111">The **GoToControl** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ec06a-112">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="ec06a-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="ec06a-113">Описание</span><span class="sxs-lookup"><span data-stu-id="ec06a-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec06a-114"><strong>Имя элемента управления</strong></span><span class="sxs-lookup"><span data-stu-id="ec06a-114"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="ec06a-115">Имя поля или элемента управления, куда необходимо переместить фокус.</span><span class="sxs-lookup"><span data-stu-id="ec06a-115">The name of the field or control where you want the focus.</span></span> <span data-ttu-id="ec06a-116">Введите имя элемента управления или поля в поле <strong>Имя элемента управления</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="ec06a-116">Enter the field or control name in the <strong>Control Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="ec06a-117">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="ec06a-117">This is a required argument.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="ec06a-118">Введите только имя поля или элемента управления в качестве аргумента <STRONG>Имя элемента управления</STRONG> , не полный идентификатор, такие как Forms! Продукты! [Код продукта].</span><span class="sxs-lookup"><span data-stu-id="ec06a-118">Enter only the name of the field or control in the <STRONG>Control Name</STRONG> argument, not the fully qualified identifier, such as Forms!Products![Product ID].</span></span></P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ec06a-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="ec06a-119">Remarks</span></span>

<span data-ttu-id="ec06a-120">**КЭлементуУправления** нельзя использовать для перемещения фокуса на элемент управления на форме скрытые.</span><span class="sxs-lookup"><span data-stu-id="ec06a-120">You cannot use the **GoToControl** action to move the focus to a control on a hidden form.</span></span>


> [!TIP]
> <P><span data-ttu-id="ec06a-121"><STRONG>КЭлементуУправления</STRONG> можно использовать для перемещения подчиненной формы, который является элементом управления.</span><span class="sxs-lookup"><span data-stu-id="ec06a-121">You can use the <STRONG>GoToControl</STRONG> action to move to a subform, which is a type of control.</span></span> <span data-ttu-id="ec06a-122">Затем можно использовать действие <STRONG>НаЗапись</STRONG> для перехода к конкретной записи подчиненной формы.</span><span class="sxs-lookup"><span data-stu-id="ec06a-122">You can then use the <STRONG>GoToRecord</STRONG> action to move to a particular record in the subform.</span></span> <span data-ttu-id="ec06a-123">Вы также можете переместить на элемент управления подчиненной формы с помощью <STRONG>КЭлементуУправления</STRONG> для перемещения сначала к подчиненной формы, а затем в элемент управления подчиненной формы.</span><span class="sxs-lookup"><span data-stu-id="ec06a-123">You can also move to a control on a subform by using the <STRONG>GoToControl</STRONG> action to move first to the subform and then to the control on the subform.</span></span></P>



<span data-ttu-id="ec06a-124">Чтобы запустить **КЭлементуУправления** в Visual Basic для приложений (VBA) модуль, используйте метод **КЭлементуУправления** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="ec06a-124">To run the **GoToControl** action in a Visual Basic for Applications (VBA) module, use the **GoToControl** method of the **DoCmd** object.</span></span> <span data-ttu-id="ec06a-125">Можно также использовать метод **SetFocus** для перемещения фокуса на элемент управления в форме или в подчиненной или к полю открыть таблицу, запроса или формы.</span><span class="sxs-lookup"><span data-stu-id="ec06a-125">You can also use the **SetFocus** method to move the focus to a control on a form or any of its subforms, or to a field in an open table, query, or form datasheet.</span></span>

## <a name="examples"></a><span data-ttu-id="ec06a-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="ec06a-126">Examples</span></span>

<span data-ttu-id="ec06a-127">**Задайте значение элемента управления с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="ec06a-127">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="ec06a-128">Следующий макрос открывает форму добавления продуктов с помощью кнопки на форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="ec06a-128">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="ec06a-129">Демонстрируется использование **эхо**, **CloseWindow**, **ОткрытьФорму**, **SetValue**и **КЭлементуУправления** действий.</span><span class="sxs-lookup"><span data-stu-id="ec06a-129">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="ec06a-130">Действие **SetValue** задает код поставщика управления на форме продуктов для текущего поставщика в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="ec06a-130">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="ec06a-131">**Затем КЭлементуУправления** перемещает фокус в поле Идентификатор категории, где можно вводить данные для нового продукта.</span><span class="sxs-lookup"><span data-stu-id="ec06a-131">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="ec06a-132">Этот макрос должен быть связан с кнопкой Добавить продукты в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="ec06a-132">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ec06a-133">Действие</span><span class="sxs-lookup"><span data-stu-id="ec06a-133">Action</span></span></p></th>
<th><p><span data-ttu-id="ec06a-134">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="ec06a-134">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="ec06a-135">Comment</span><span class="sxs-lookup"><span data-stu-id="ec06a-135">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec06a-136"><strong>Эхо</strong></span><span class="sxs-lookup"><span data-stu-id="ec06a-136"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="ec06a-137"><strong>Вывод на экран</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="ec06a-137"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="ec06a-138">Остановите обновление экрана в процессе выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="ec06a-138">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec06a-139"><strong>CloseWindow</strong></span><span class="sxs-lookup"><span data-stu-id="ec06a-139"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="ec06a-140"><strong>Тип объекта</strong>: <strong>FormObject имя</strong>: продукт списка <strong>Сохранить</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="ec06a-140"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="ec06a-141">Закрыть форму списка продуктов.</span><span class="sxs-lookup"><span data-stu-id="ec06a-141">Close Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec06a-142"><strong>ОткрытьФорму</strong></span><span class="sxs-lookup"><span data-stu-id="ec06a-142"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="ec06a-143"><strong>Имя формы</strong>: продуктов <strong>представления</strong>: <strong>FormData режима</strong>: <strong>Режим AddWindow</strong>: <strong>Обычный</strong></span><span class="sxs-lookup"><span data-stu-id="ec06a-143"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="ec06a-144">Откройте форму продуктов.</span><span class="sxs-lookup"><span data-stu-id="ec06a-144">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec06a-145"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="ec06a-145"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="ec06a-146"><strong>Элемент</strong>: [формы]! [Товары]! [Код поставщика] <strong>Выражение</strong>: КодПоставщика</span><span class="sxs-lookup"><span data-stu-id="ec06a-146"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="ec06a-147">Значение текущего поставщика управления код поставщика в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="ec06a-147">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec06a-148"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="ec06a-148"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="ec06a-149"><strong>Имя элемента управления</strong>: идентификатор категории</span><span class="sxs-lookup"><span data-stu-id="ec06a-149"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="ec06a-150">Перейдите к элементу управления идентификатор категории.</span><span class="sxs-lookup"><span data-stu-id="ec06a-150">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ec06a-151">**Проверка данных с помощью макроса (en)**</span><span class="sxs-lookup"><span data-stu-id="ec06a-151">**Validate data by using a macro**</span></span>

<span data-ttu-id="ec06a-152">Следующий макрос для проверки проверяет почтовые индексы, введенные в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="ec06a-152">The following validation macro checks the postal codes entered in a Suppliers form.</span></span> <span data-ttu-id="ec06a-153">Демонстрируется использование **ОстановитьМакрос**, **MessageBox**, **ОтменитьСобытие**и **КЭлементуУправления** действия.</span><span class="sxs-lookup"><span data-stu-id="ec06a-153">It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions.</span></span> <span data-ttu-id="ec06a-154">Условным выражением проверяет страны или региона и почтового индекса в записи на форме.</span><span class="sxs-lookup"><span data-stu-id="ec06a-154">A conditional expression checks the country/region and postal code entered in a record on the form.</span></span> <span data-ttu-id="ec06a-155">Если почтовый индекс не в нужном формате для страны или региона, макрос отображается окно сообщения и показано, как отменить сохранение записи.</span><span class="sxs-lookup"><span data-stu-id="ec06a-155">If the postal code is not in the right format for the country/region, the macro displays a message box and cancels saving the record.</span></span> <span data-ttu-id="ec06a-156">Макрос будет снова к элементу управления почтовый индекс для исправления ошибки.</span><span class="sxs-lookup"><span data-stu-id="ec06a-156">The macro then returns you to the Postal Code control, where you can correct the error.</span></span> <span data-ttu-id="ec06a-157">Этот макрос должен быть связан свойством **BeforeUpdate** формы Поставщики.</span><span class="sxs-lookup"><span data-stu-id="ec06a-157">This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ec06a-158">Condition</span><span class="sxs-lookup"><span data-stu-id="ec06a-158">Condition</span></span></p></th>
<th><p><span data-ttu-id="ec06a-159">Действие</span><span class="sxs-lookup"><span data-stu-id="ec06a-159">Action</span></span></p></th>
<th><p><span data-ttu-id="ec06a-160">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="ec06a-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="ec06a-161">Comment</span><span class="sxs-lookup"><span data-stu-id="ec06a-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec06a-162">IsNull([CountryRegion])</span><span class="sxs-lookup"><span data-stu-id="ec06a-162">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="ec06a-163"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="ec06a-163"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ec06a-164">Если Страна имеет <strong>значение Null</strong>, почтовый индекс не может быть проверен.</span><span class="sxs-lookup"><span data-stu-id="ec06a-164">If CountryRegion is <strong>Null</strong>, postal code cannot be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec06a-165">[Страна] В (&quot;Франции&quot;,&quot;Италия&quot;,&quot;Испания&quot;) и Len ([Почтовый индекс]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="ec06a-165">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([Postal Code]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="ec06a-166"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="ec06a-166"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="ec06a-167"><strong>Сообщение</strong>: почтовый индекс должен состоять из 5 знаков.</span><span class="sxs-lookup"><span data-stu-id="ec06a-167"><strong>Message</strong>: The postal code must be 5 characters.</span></span> <span data-ttu-id="ec06a-168"><strong>Звуковые сигналы</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: ошибка почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="ec06a-168"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="ec06a-169">Если почтовый индекс не 5 знаков, отображать сообщение.</span><span class="sxs-lookup"><span data-stu-id="ec06a-169">If the postal code is not 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec06a-170">...</span><span class="sxs-lookup"><span data-stu-id="ec06a-170"></span></span></p></td>
<td><p><span data-ttu-id="ec06a-171"><strong>ОтменитьСобытие</strong></span><span class="sxs-lookup"><span data-stu-id="ec06a-171"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ec06a-172">Отмените событие.</span><span class="sxs-lookup"><span data-stu-id="ec06a-172">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="ec06a-173"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="ec06a-173"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="ec06a-174"><strong>Имя элемента управления</strong>: PostalCode</span><span class="sxs-lookup"><span data-stu-id="ec06a-174"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec06a-175">[Страна] В (&quot;Австралия&quot;,&quot;Сингапур&quot;) и Len ([Почтовый индекс]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="ec06a-175">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([Postal Code]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="ec06a-176"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="ec06a-176"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="ec06a-177">Сообщение об ошибке: Почтовый индекс должен быть 4 символов.</span><span class="sxs-lookup"><span data-stu-id="ec06a-177">Message: The postal code must be 4 characters.</span></span> <span data-ttu-id="ec06a-178"><strong>Звуковые сигналы</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: ошибка почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="ec06a-178"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="ec06a-179">Если почтовый индекс не 4 символа, отображать сообщение.</span><span class="sxs-lookup"><span data-stu-id="ec06a-179">If the postal code is not 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec06a-180">...</span><span class="sxs-lookup"><span data-stu-id="ec06a-180"></span></span></p></td>
<td><p><span data-ttu-id="ec06a-181"><strong>ОтменитьСобытие</strong></span><span class="sxs-lookup"><span data-stu-id="ec06a-181"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ec06a-182">Отмените событие.</span><span class="sxs-lookup"><span data-stu-id="ec06a-182">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="ec06a-183"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="ec06a-183"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="ec06a-184"><strong>Имя элемента управления</strong>: PostalCode</span><span class="sxs-lookup"><span data-stu-id="ec06a-184"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec06a-185">([Страна] = &quot;Канада&quot;) И ([Почтовый индекс] не нравится&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</span><span class="sxs-lookup"><span data-stu-id="ec06a-185">([CountryRegion] = &quot;Canada&quot;) And ([Postal Code] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="ec06a-186"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="ec06a-186"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="ec06a-187"><strong>Сообщение</strong>: почтовый индекс является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="ec06a-187"><strong>Message</strong>: The postal code is not valid.</span></span> <span data-ttu-id="ec06a-188">Пример кода, английский (Канада): H1J 1 c 3 <strong>звуковые сигналы</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: почтовый код ошибки</span><span class="sxs-lookup"><span data-stu-id="ec06a-188">Example of Canadian code: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="ec06a-189">Если почтовый индекс не подходит для Канады, отображать сообщение.</span><span class="sxs-lookup"><span data-stu-id="ec06a-189">If the postal code is not correct for Canada, display a message.</span></span> <span data-ttu-id="ec06a-190">(Пример кода, английский (Канада): H1J 1 c 3)</span><span class="sxs-lookup"><span data-stu-id="ec06a-190">(Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec06a-191">...</span><span class="sxs-lookup"><span data-stu-id="ec06a-191"></span></span></p></td>
<td><p><span data-ttu-id="ec06a-192"><strong>ОтменитьСобытие</strong></span><span class="sxs-lookup"><span data-stu-id="ec06a-192"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="ec06a-193">Отмените событие.</span><span class="sxs-lookup"><span data-stu-id="ec06a-193">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

