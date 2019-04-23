---
title: Макрокоманда MoveAndSizeWindow
TOCTitle: MoveAndSizeWindow macro action
ms:assetid: 86bcf45f-90ce-4ca2-a7fb-efbe5347d137
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197001(v=office.15)
ms:contentKeyID: 48546090
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c1b127995a2f9a0af7da80e9df862259b570870e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288808"
---
# <a name="moveandsizewindow-macro-action"></a><span data-ttu-id="66872-102">Макрокоманда MoveAndSizeWindow</span><span class="sxs-lookup"><span data-stu-id="66872-102">MoveAndSizeWindow macro action</span></span>

<span data-ttu-id="66872-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="66872-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="66872-104">Если вы настроили параметры окна документа на использование перекрывающихся окон, а не документов с вкладками, можно использовать действие **мовеандсизевиндов** для перемещения или изменения размеров активного окна.</span><span class="sxs-lookup"><span data-stu-id="66872-104">If you have set your document window options to use overlapping windows instead of tabbed documents, you can use the **MoveAndSizeWindow** action to move or resize the active window.</span></span> <span data-ttu-id="66872-105">Сведения о том, как задать параметры окна документа, представлены в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="66872-105">For information on how to set document window options, see the Remarks section.</span></span>

## <a name="setting"></a><span data-ttu-id="66872-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="66872-106">Setting</span></span>

<span data-ttu-id="66872-107">Макрокоманда **мовеандсизевиндов** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="66872-107">The **MoveAndSizeWindow** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="66872-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="66872-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="66872-109">Описание</span><span class="sxs-lookup"><span data-stu-id="66872-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="66872-110"><strong>Right</strong></span><span class="sxs-lookup"><span data-stu-id="66872-110"><strong>Right</strong></span></span></p></td>
<td><p><span data-ttu-id="66872-111">Новая горизонтальная позиция верхнего левого угла окна, измеряемая от левого края содержащего его окна.</span><span class="sxs-lookup"><span data-stu-id="66872-111">The new horizontal position of the window's upper-left corner, measured from the left edge of its containing window.</span></span> <span data-ttu-id="66872-112">Введите позицию в <strong>правом</strong> поле в разделе <strong>аргументы макрокоманды</strong> в области построителя макросов.</span><span class="sxs-lookup"><span data-stu-id="66872-112">Enter the position in the <strong>Right</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66872-113"><strong>Понижен</strong></span><span class="sxs-lookup"><span data-stu-id="66872-113"><strong>Down</strong></span></span></p></td>
<td><p><span data-ttu-id="66872-114">Новая вертикальная позиция верхнего левого угла окна, измеряемая от верхнего края содержащего его окна.</span><span class="sxs-lookup"><span data-stu-id="66872-114">The new vertical position of the window's upper-left corner, measured from the top edge of its containing window.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="66872-115"><strong>Width</strong></span><span class="sxs-lookup"><span data-stu-id="66872-115"><strong>Width</strong></span></span></p></td>
<td><p><span data-ttu-id="66872-116">Новая ширина окна.</span><span class="sxs-lookup"><span data-stu-id="66872-116">The window's new width.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66872-117"><strong>Height</strong></span><span class="sxs-lookup"><span data-stu-id="66872-117"><strong>Height</strong></span></span></p></td>
<td><p><span data-ttu-id="66872-118">Новая высота окна.</span><span class="sxs-lookup"><span data-stu-id="66872-118">The window's new height.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="66872-119">Если оставить аргумент пустым, Microsoft Access будет использовать текущие параметры окна.</span><span class="sxs-lookup"><span data-stu-id="66872-119">If you leave an argument blank, Microsoft Access uses the window's current setting.</span></span>

<span data-ttu-id="66872-120">Необходимо ввести значение по крайней мере для одного аргумента.</span><span class="sxs-lookup"><span data-stu-id="66872-120">You must enter a value for at least one argument.</span></span>

> [!NOTE]
> <span data-ttu-id="66872-121">Каждое измерение находится в дюймах или сантиметрах в зависимости от региональных параметров в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="66872-121">Each measurement is in inches or centimeters, depending on the regional settings in Windows Control Panel.</span></span>

## <a name="remarks"></a><span data-ttu-id="66872-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="66872-122">Remarks</span></span>

<span data-ttu-id="66872-123">Чтобы настроить приложение для использования перекрывающихся окон вместо документов с вкладками, выполните следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="66872-123">To set up an application to use overlapping windows instead of tabbed documents, use the following procedure:</span></span>

1.  <span data-ttu-id="66872-124">Нажмите кнопку **Параметры**</span><span class="sxs-lookup"><span data-stu-id="66872-124">Click **Options**</span></span>

2.  <span data-ttu-id="66872-125">Щелкните **Текущая база данных**.</span><span class="sxs-lookup"><span data-stu-id="66872-125">Click **Current Database**.</span></span>

3.  <span data-ttu-id="66872-126">В разделе Параметры **приложения** в разделе **Параметры окна документа**щелкните перекрывающиеся **окна**.</span><span class="sxs-lookup"><span data-stu-id="66872-126">In the **Application Options** section, under **Document Window Options**, click **Overlapping Windows**.</span></span>

4.  <span data-ttu-id="66872-127">Нажмите кнопку **ОК**, а затем закройте и снова откройте базу данных.</span><span class="sxs-lookup"><span data-stu-id="66872-127">Click **OK**, and then close and reopen the database.</span></span>

<span data-ttu-id="66872-128">Это действие аналогично нажатию кнопки **переместить** или **изменить** в меню оконного \*\*\*\* меню.</span><span class="sxs-lookup"><span data-stu-id="66872-128">This action is similar to clicking **Move** or **Size** on the window's **Control** menu.</span></span> <span data-ttu-id="66872-129">С помощью команд меню вы можете переместить или изменить размер окна с помощью клавиш со стрелками на клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="66872-129">With the menu commands, you use the keyboard's arrow keys to move or resize the window.</span></span> <span data-ttu-id="66872-130">С помощью действия **мовеандсизевиндов** вы вводите положение и размер измерений напрямую.</span><span class="sxs-lookup"><span data-stu-id="66872-130">With the **MoveAndSizeWindow** action, you enter the position and size measurements directly.</span></span> <span data-ttu-id="66872-131">Вы также можете использовать мышь для перемещения и изменения размеров окон.</span><span class="sxs-lookup"><span data-stu-id="66872-131">You can also use the mouse to move and size windows.</span></span>

<span data-ttu-id="66872-132">Вы можете использовать это действие для любого окна в любом представлении.</span><span class="sxs-lookup"><span data-stu-id="66872-132">You can use this action on any window, in any view.</span></span>

> [!TIP]
> - <span data-ttu-id="66872-133">Чтобы переместить окно без изменения его размера, введите значения для аргументов **right** и **Down** , но не заполняйте аргументы **Width** и **Height** .</span><span class="sxs-lookup"><span data-stu-id="66872-133">To move a window without resizing it, enter values for the **Right** and **Down** arguments but leave the **Width** and **Height** arguments blank.</span></span>
> - <span data-ttu-id="66872-134">Чтобы изменить размер окна без его перемещения, введите значения для аргументов **Width** и **Height** , но не вводите аргументы **справа** и **вниз** .</span><span class="sxs-lookup"><span data-stu-id="66872-134">To resize a window without moving it, enter values for the **Width** and **Height** arguments but leave the **Right** and **Down** arguments blank.</span></span>

<span data-ttu-id="66872-135">Чтобы запустить действие **мовеандсизевиндов** в модуле Visual Basic для приложений (VBA), используйте метод **мовесизе** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="66872-135">To run the **MoveAndSizeWindow** action in a Visual Basic for Applications (VBA) module, use the **MoveSize** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="66872-136">Пример</span><span class="sxs-lookup"><span data-stu-id="66872-136">Example</span></span>

<span data-ttu-id="66872-137">**Синхронизация форм с помощью макроса**</span><span class="sxs-lookup"><span data-stu-id="66872-137">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="66872-138">Следующий макрос открывает форму списка товаров в правом нижнем углу формы поставщики, в которой отображаются продукты текущего поставщика.</span><span class="sxs-lookup"><span data-stu-id="66872-138">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="66872-139">В нем показано использование действий **echo**, **MessageBox**, **КЭлементуУправления**, **Макрокоманда StopMacro**, **OpenForm**и **мовеандсизевиндов** .</span><span class="sxs-lookup"><span data-stu-id="66872-139">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="66872-140">В нем также показано использование условного выражения с действиями **MessageBox**, **КЭлементуУправления**и **Макрокоманда StopMacro** .</span><span class="sxs-lookup"><span data-stu-id="66872-140">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="66872-141">Этот макрос необходимо прикрепить к кнопке "проверить продукты" в форме "поставщики".</span><span class="sxs-lookup"><span data-stu-id="66872-141">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="66872-142">Условие</span><span class="sxs-lookup"><span data-stu-id="66872-142">Condition</span></span></p></th>
<th><p><span data-ttu-id="66872-143">Действие</span><span class="sxs-lookup"><span data-stu-id="66872-143">Action</span></span></p></th>
<th><p><span data-ttu-id="66872-144">Аргументы: Настройка</span><span class="sxs-lookup"><span data-stu-id="66872-144">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="66872-145">Комментарий</span><span class="sxs-lookup"><span data-stu-id="66872-145">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="66872-146"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="66872-146"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="66872-147"><strong>Echo on</strong>: <strong>нет</strong></span><span class="sxs-lookup"><span data-stu-id="66872-147"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="66872-148">Остановить обновление экрана во время выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="66872-148">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66872-149">IsNull ([идентификатор поставщика])</span><span class="sxs-lookup"><span data-stu-id="66872-149">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="66872-150"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="66872-150"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="66872-151"><strong>Сообщение</strong>: перейдите к записи поставщика, продукты которой вы хотите просмотреть, а затем снова нажмите кнопку Просмотр продуктов.</span><span class="sxs-lookup"><span data-stu-id="66872-151"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="66872-152"><strong>Beep</strong>: <strong>естипе</strong>: <strong>нонетитле</strong>: выберите поставщика</span><span class="sxs-lookup"><span data-stu-id="66872-152"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="66872-153">Если в форме Поставщики нет текущего поставщика, отобразите сообщение.</span><span class="sxs-lookup"><span data-stu-id="66872-153">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="66872-154"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="66872-154"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="66872-155"><strong>Имя элемента управления</strong>: CompanyName</span><span class="sxs-lookup"><span data-stu-id="66872-155"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="66872-156">Перемещение фокуса на элемент управления CompanyName.</span><span class="sxs-lookup"><span data-stu-id="66872-156">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="66872-157">...</span><span class="sxs-lookup"><span data-stu-id="66872-157"></span></span></p></td>
<td><p><span data-ttu-id="66872-158"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="66872-158"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="66872-159">Остановка макроса.</span><span class="sxs-lookup"><span data-stu-id="66872-159">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="66872-160"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="66872-160"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="66872-161"><strong>Имя формы</strong>: <strong>представление</strong>списка продуктов: <strong>даташитфилтер Name</strong>: <strong>WHERE Condition</strong>: [ID поставщика] = [Forms]! [Поставщики]! Ключев <strong>Режим данных</strong>: <strong>режим чтения онливиндов</strong>: <strong>обычный</strong></span><span class="sxs-lookup"><span data-stu-id="66872-161"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="66872-162">Откройте форму Список продуктов и отобразите текущие продукты поставщика.</span><span class="sxs-lookup"><span data-stu-id="66872-162">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="66872-163"><strong>Мовеандсизевиндов</strong></span><span class="sxs-lookup"><span data-stu-id="66872-163"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="66872-164"><strong>Right</strong>: 0,7799&quot; <strong>вниз</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="66872-164"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="66872-165">РасПоложите форму списка товаров в правом нижнем углу формы Поставщики.</span><span class="sxs-lookup"><span data-stu-id="66872-165">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

