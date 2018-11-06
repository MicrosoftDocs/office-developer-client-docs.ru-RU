---
title: Действия макроса эхо (Справочник по для настольных баз данных Access)
TOCTitle: Echo macro action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 03eeab3884e093b7c22f8fd23d5471d1dc620bc8
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997457"
---
# <a name="echo-macro-action"></a><span data-ttu-id="79e48-102">Макрокоманда Echo</span><span class="sxs-lookup"><span data-stu-id="79e48-102">Echo macro action</span></span>

<span data-ttu-id="79e48-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="79e48-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="79e48-104">Действие **эхо** можно использовать для определения, включено ли эхо.</span><span class="sxs-lookup"><span data-stu-id="79e48-104">You can use the **Echo** action to specify whether echo is turned on.</span></span> <span data-ttu-id="79e48-105">Например можно использовать это действие скрытие или отображение результатов макроса во время его выполнения.</span><span class="sxs-lookup"><span data-stu-id="79e48-105">For example, you can use this action to hide or show the results of a macro while it runs.</span></span>

## <a name="setting"></a><span data-ttu-id="79e48-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="79e48-106">Setting</span></span>

> [!NOTE]
> <span data-ttu-id="79e48-107">Это действие не разрешено, если база данных не является доверенной.</span><span class="sxs-lookup"><span data-stu-id="79e48-107">This action will not be allowed if the database is not trusted.</span></span>

<span data-ttu-id="79e48-108">Действие **эхо** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="79e48-108">The **Echo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="79e48-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="79e48-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="79e48-110">Описание</span><span class="sxs-lookup"><span data-stu-id="79e48-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="79e48-111"><strong>Включить вывод</strong></span><span class="sxs-lookup"><span data-stu-id="79e48-111"><strong>Echo On</strong></span></span></p></td>
<td><p><span data-ttu-id="79e48-112">Нажмите кнопку <strong>Да</strong> (включает вывод на экран) или <strong>Нет</strong> (отключает вывод) в <strong>Эхо на</strong> поле в разделе <strong>Действие аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="79e48-112">Click <strong>Yes</strong> (turn echo on) or <strong>No</strong> (turn echo off) in the <strong>Echo On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="79e48-113">По умолчанию используется значение <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="79e48-113">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79e48-114"><strong>Текст в строке состояния</strong></span><span class="sxs-lookup"><span data-stu-id="79e48-114"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="79e48-115">Текст, отображаемый в строке когда выключена эхо состояния.</span><span class="sxs-lookup"><span data-stu-id="79e48-115">The text to display in the status bar when echo is turned off.</span></span> <span data-ttu-id="79e48-116">Например, при отключении эхо в строке состояния может отображаться &quot;выполнение макроса.&quot;</span><span class="sxs-lookup"><span data-stu-id="79e48-116">For example, when echo is turned off, the status bar can display &quot;The macro is running.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="79e48-117">После запуска макроса обновление экрана часто отображается информация, без необходимые для функционирования макрос.</span><span class="sxs-lookup"><span data-stu-id="79e48-117">When a macro runs, screen updating often shows information not essential to the functioning of the macro.</span></span> <span data-ttu-id="79e48-118">Если аргумент **Эхо на** значение **No**, макрос выполняется без обновления экрана.</span><span class="sxs-lookup"><span data-stu-id="79e48-118">When you set the **Echo On** argument to **No**, the macro runs without updating the screen.</span></span> <span data-ttu-id="79e48-119">После завершения макроса доступа автоматически включает эхо и обновляет окна.</span><span class="sxs-lookup"><span data-stu-id="79e48-119">When the macro finishes, Access automatically turns echo back on and repaints the window.</span></span> <span data-ttu-id="79e48-120">**No** для аргумента **Эхо на** не влияет на функциональность макроса или его результаты.</span><span class="sxs-lookup"><span data-stu-id="79e48-120">The **No** setting for the **Echo On** argument doesn't affect the functionality of the macro or its results.</span></span>

<span data-ttu-id="79e48-121">Действие **эхо** не отображение без модальных диалоговых окон, например, сообщений об ошибках или всплывающих форм, таких как страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="79e48-121">The **Echo** action doesn't suppress the display of modal dialog boxes, such as error messages, or pop-up forms, such as property sheets.</span></span> <span data-ttu-id="79e48-122">Диалоговые окна и всплывающие формы для сбора и отображения данных, можно использовать даже в том случае, если отключено эхо.</span><span class="sxs-lookup"><span data-stu-id="79e48-122">You can use dialog boxes and pop-up forms to gather or display information, even if echo is turned off.</span></span> <span data-ttu-id="79e48-123">Чтобы запретить все сообщения и диалоговых окон за исключением окна сообщений об ошибках и диалоговых окон, которые требуют пользователю требуется ввести сведения, используйте действие **УстановитьСообщения** .</span><span class="sxs-lookup"><span data-stu-id="79e48-123">To suppress all message or dialog boxes except error message boxes and dialog boxes that require the user to enter information, use the **SetWarnings** action.</span></span>

<span data-ttu-id="79e48-124">**Эхо** действие можно выполнить более одного раза в макросе.</span><span class="sxs-lookup"><span data-stu-id="79e48-124">You can run the **Echo** action more than once in a macro.</span></span> <span data-ttu-id="79e48-125">Это позволяет изменить текст в строке состояния во время выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="79e48-125">This allows you to change the status bar text while the macro runs.</span></span>

<span data-ttu-id="79e48-126">При выключении эхо, можно использовать действие **DisplayHourglassPointer** изменение указатель мыши на значок песочными часами (или любое значок указателя мыши, заданные для «Занят») для предоставления визуальный индикатор, на котором выполняется макрос.</span><span class="sxs-lookup"><span data-stu-id="79e48-126">If you turn echo off, you can use the **DisplayHourglassPointer** action to change the mouse pointer into an hourglass icon (or whatever mouse pointer icon you've set for "Busy") to provide a visual indication that the macro is running.</span></span>

<span data-ttu-id="79e48-127">Чтобы выполнить действие **эхо** в Visual Basic для приложений (VBA) модуль, используйте метод **эхо** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="79e48-127">To run the **Echo** action in a Visual Basic for Applications (VBA) module, use the **Echo** method of the **DoCmd** object.</span></span>

## <a name="examples"></a><span data-ttu-id="79e48-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="79e48-128">Examples</span></span>

### <a name="set-the-value-of-a-control-by-using-a-macro"></a><span data-ttu-id="79e48-129">Задайте значение элемента управления с помощью макроса</span><span class="sxs-lookup"><span data-stu-id="79e48-129">Set the value of a control by using a macro</span></span>

<span data-ttu-id="79e48-130">Следующий макрос открывает форму добавления продуктов с помощью кнопки на форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="79e48-130">The following macro opens the Add Products form from a button on the Suppliers form.</span></span> <span data-ttu-id="79e48-131">Демонстрируется использование **эхо**, **CloseWindow**, **ОткрытьФорму**, **SetValue**и **КЭлементуУправления** действий.</span><span class="sxs-lookup"><span data-stu-id="79e48-131">It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions.</span></span> <span data-ttu-id="79e48-132">Действие **SetValue** задает код поставщика управления на форме продуктов для текущего поставщика в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="79e48-132">The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form.</span></span> <span data-ttu-id="79e48-133">**Затем КЭлементуУправления** перемещает фокус в поле Идентификатор категории, где можно вводить данные для нового продукта.</span><span class="sxs-lookup"><span data-stu-id="79e48-133">The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product.</span></span> <span data-ttu-id="79e48-134">Этот макрос должен быть связан с кнопкой Добавить продукты в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="79e48-134">This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="79e48-135">Действие</span><span class="sxs-lookup"><span data-stu-id="79e48-135">Action</span></span></p></th>
<th><p><span data-ttu-id="79e48-136">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="79e48-136">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="79e48-137">Comment</span><span class="sxs-lookup"><span data-stu-id="79e48-137">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="79e48-138"><strong>Эхо</strong></span><span class="sxs-lookup"><span data-stu-id="79e48-138"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="79e48-139"><strong>Вывод на экран</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="79e48-139"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="79e48-140">Остановите обновление экрана в процессе выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="79e48-140">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79e48-141"><strong>CloseWindow</strong></span><span class="sxs-lookup"><span data-stu-id="79e48-141"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="79e48-142"><strong>Тип объекта</strong>: <strong>FormObject имя</strong>: продукт списка <strong>Сохранить</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="79e48-142"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="79e48-143">Закройте форму списка продуктов.</span><span class="sxs-lookup"><span data-stu-id="79e48-143">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79e48-144"><strong>ОткрытьФорму</strong></span><span class="sxs-lookup"><span data-stu-id="79e48-144"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="79e48-145"><strong>Имя формы</strong>: продуктов <strong>представления</strong>: <strong>FormData режима</strong>: <strong>Режим AddWindow</strong>: <strong>Обычный</strong></span><span class="sxs-lookup"><span data-stu-id="79e48-145"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="79e48-146">Откройте форму продуктов.</span><span class="sxs-lookup"><span data-stu-id="79e48-146">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79e48-147"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="79e48-147"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="79e48-148"><strong>Элемент</strong>: [формы]! [Товары]! [Код поставщика] <strong>Выражение</strong>: КодПоставщика</span><span class="sxs-lookup"><span data-stu-id="79e48-148"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="79e48-149">Значение текущего поставщика управления код поставщика в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="79e48-149">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79e48-150"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="79e48-150"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="79e48-151"><strong>Имя элемента управления</strong>: идентификатор категории</span><span class="sxs-lookup"><span data-stu-id="79e48-151"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="79e48-152">Перейдите к элементу управления идентификатор категории.</span><span class="sxs-lookup"><span data-stu-id="79e48-152">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="synchronize-forms-by-using-a-macro"></a><span data-ttu-id="79e48-153">Синхронизация форм с помощью макроса (en)</span><span class="sxs-lookup"><span data-stu-id="79e48-153">Synchronize forms by using a macro</span></span>

<span data-ttu-id="79e48-154">Следующий макрос открывает форму списка продуктов в правом нижнем углу формы Поставщики, отображение текущего поставщика продуктов.</span><span class="sxs-lookup"><span data-stu-id="79e48-154">The following macro opens the Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="79e48-155">Демонстрируется использование **эхо**, **MessageBox**, **КЭлементуУправления**, **ОстановитьМакрос**, **ОткрытьФорму**и **MoveAndSizeWindow** действий.</span><span class="sxs-lookup"><span data-stu-id="79e48-155">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="79e48-156">Также показано использование условного выражения с **MessageBox**, **КЭлементуУправления**« **Поставщики** ».</span><span class="sxs-lookup"><span data-stu-id="79e48-156">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="79e48-157">Этот макрос должен быть связан с кнопкой Обзор продуктов в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="79e48-157">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="79e48-158">Condition</span><span class="sxs-lookup"><span data-stu-id="79e48-158">Condition</span></span></p></th>
<th><p><span data-ttu-id="79e48-159">Действие</span><span class="sxs-lookup"><span data-stu-id="79e48-159">Action</span></span></p></th>
<th><p><span data-ttu-id="79e48-160">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="79e48-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="79e48-161">Comment</span><span class="sxs-lookup"><span data-stu-id="79e48-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="79e48-162"><strong>Эхо</strong></span><span class="sxs-lookup"><span data-stu-id="79e48-162"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="79e48-163"><strong>Вывод на экран</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="79e48-163"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="79e48-164">Остановите обновление экрана в процессе выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="79e48-164">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79e48-165">Функция IsNull ([код поставщика])</span><span class="sxs-lookup"><span data-stu-id="79e48-165">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="79e48-166"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="79e48-166"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="79e48-167"><strong>Сообщение</strong>: перемещение на запись поставщика, продукты, чтобы увидеть, затем нажмите кнопку Предварительный просмотр еще раз.</span><span class="sxs-lookup"><span data-stu-id="79e48-167"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="79e48-168"><strong>Звуковые сигналы</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Выбор поставщика</span><span class="sxs-lookup"><span data-stu-id="79e48-168"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="79e48-169">При отсутствии никто из современных поставщиков в форме Поставщики, отображается сообщение.</span><span class="sxs-lookup"><span data-stu-id="79e48-169">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79e48-170">...</span><span class="sxs-lookup"><span data-stu-id="79e48-170"></span></span></p></td>
<td><p><span data-ttu-id="79e48-171"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="79e48-171"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="79e48-172"><strong>Имя элемента управления</strong>: CompanyName</span><span class="sxs-lookup"><span data-stu-id="79e48-172"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="79e48-173">Перемещение фокуса на элемент управления CompanyName.</span><span class="sxs-lookup"><span data-stu-id="79e48-173">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79e48-174">...</span><span class="sxs-lookup"><span data-stu-id="79e48-174"></span></span></p></td>
<td><p><span data-ttu-id="79e48-175"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="79e48-175"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="79e48-176">Остановка макроса.</span><span class="sxs-lookup"><span data-stu-id="79e48-176">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="79e48-177"><strong>ОткрытьФорму</strong></span><span class="sxs-lookup"><span data-stu-id="79e48-177"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="79e48-178"><strong>Имя формы</strong>: список продуктов <strong>представления</strong>: <strong>Имя DatasheetFilter</strong>: <strong>условие отбора</strong>: [код поставщика] = [Forms]! [Поставщики]! [Код поставщика] <strong>Режим данных</strong>: <strong>Режим чтения OnlyWindow</strong>: <strong>Обычный</strong></span><span class="sxs-lookup"><span data-stu-id="79e48-178"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="79e48-179">Откройте форму списка продуктов и отображение текущего поставщика продуктов.</span><span class="sxs-lookup"><span data-stu-id="79e48-179">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="79e48-180"><strong>MoveAndSizeWindow</strong></span><span class="sxs-lookup"><span data-stu-id="79e48-180"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="79e48-181"><strong>Право</strong>: 0,7799&quot; <strong>вниз</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="79e48-181"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="79e48-182">Положение формы списка продуктов в нижней правой части формы Поставщики.</span><span class="sxs-lookup"><span data-stu-id="79e48-182">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

