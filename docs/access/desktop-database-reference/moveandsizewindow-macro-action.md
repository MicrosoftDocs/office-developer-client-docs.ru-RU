---
title: MoveAndSizeWindow Macro Action
TOCTitle: MoveAndSizeWindow Macro Action
ms:assetid: 86bcf45f-90ce-4ca2-a7fb-efbe5347d137
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197001(v=office.15)
ms:contentKeyID: 48546090
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d423668f5ef53abf4216fa8f976c674474a752ed
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481730"
---
# <a name="moveandsizewindow-macro-action"></a><span data-ttu-id="352c2-102">MoveAndSizeWindow Macro Action</span><span class="sxs-lookup"><span data-stu-id="352c2-102">MoveAndSizeWindow Macro Action</span></span>


<span data-ttu-id="352c2-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="352c2-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="352c2-104">Если документ окно Параметры настроены для использования перекрывающиеся windows вместо вкладками, можно использовать действие **MoveAndSizeWindow** переместить или изменить размер активного окна.</span><span class="sxs-lookup"><span data-stu-id="352c2-104">If you have set your document window options to use overlapping windows instead of tabbed documents, you can use the **MoveAndSizeWindow** action to move or resize the active window.</span></span> <span data-ttu-id="352c2-105">Сведения о том, как задать параметры окна документа см.</span><span class="sxs-lookup"><span data-stu-id="352c2-105">For information on how to set document window options, see the Remarks section.</span></span>

## <a name="setting"></a><span data-ttu-id="352c2-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="352c2-106">Setting</span></span>

<span data-ttu-id="352c2-107">Действие **MoveAndSizeWindow** состоит из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="352c2-107">The **MoveAndSizeWindow** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="352c2-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="352c2-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="352c2-109">Описание</span><span class="sxs-lookup"><span data-stu-id="352c2-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="352c2-110"><strong>Right</strong></span><span class="sxs-lookup"><span data-stu-id="352c2-110"><strong>Right</strong></span></span></p></td>
<td><p><span data-ttu-id="352c2-111">Новые горизонтальную позицию левом верхнем углу окна, измеряемую от левого края содержащего его окна.</span><span class="sxs-lookup"><span data-stu-id="352c2-111">The new horizontal position of the window's upper-left corner, measured from the left edge of its containing window.</span></span> <span data-ttu-id="352c2-112">Введите позицию в <strong>правом</strong> поле в разделе <strong>Действие аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="352c2-112">Enter the position in the <strong>Right</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352c2-113"><strong>Вниз</strong></span><span class="sxs-lookup"><span data-stu-id="352c2-113"><strong>Down</strong></span></span></p></td>
<td><p><span data-ttu-id="352c2-114">Новые вертикальную позицию левом верхнем углу окна, измеряемую от верхней границы активного.</span><span class="sxs-lookup"><span data-stu-id="352c2-114">The new vertical position of the window's upper-left corner, measured from the top edge of its containing window.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="352c2-115"><strong>Ширина</strong></span><span class="sxs-lookup"><span data-stu-id="352c2-115"><strong>Width</strong></span></span></p></td>
<td><p><span data-ttu-id="352c2-116">Новая ширина окна.</span><span class="sxs-lookup"><span data-stu-id="352c2-116">The window's new width.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352c2-117"><strong>Высота</strong></span><span class="sxs-lookup"><span data-stu-id="352c2-117"><strong>Height</strong></span></span></p></td>
<td><p><span data-ttu-id="352c2-118">Новая высота окна.</span><span class="sxs-lookup"><span data-stu-id="352c2-118">The window's new height.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="352c2-119">Если аргумент оставить пустым, Microsoft Access использует текущее значение окна.</span><span class="sxs-lookup"><span data-stu-id="352c2-119">If you leave an argument blank, Microsoft Access uses the window's current setting.</span></span>

<span data-ttu-id="352c2-120">Необходимо ввести значение для по крайней мере один из аргументов.</span><span class="sxs-lookup"><span data-stu-id="352c2-120">You must enter a value for at least one argument.</span></span>


> [!NOTE]
> <P><span data-ttu-id="352c2-121">Измерения — в дюймах или сантиметрах, в зависимости от региональных параметров в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="352c2-121">Each measurement is in inches or centimeters, depending on the regional settings in Windows Control Panel.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="352c2-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="352c2-122">Remarks</span></span>

<span data-ttu-id="352c2-123">Чтобы настроить приложение для использования перекрывающиеся windows вместо вкладками, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="352c2-123">To set up an application to use overlapping windows instead of tabbed documents, use the following procedure:</span></span>

1.  <span data-ttu-id="352c2-124">Выберите пункт **Свойства**</span><span class="sxs-lookup"><span data-stu-id="352c2-124">and then click **Options**</span></span>

2.  <span data-ttu-id="352c2-125">Нажмите кнопку **текущей базы данных**.</span><span class="sxs-lookup"><span data-stu-id="352c2-125">Click **Current Database**.</span></span>

3.  <span data-ttu-id="352c2-126">В разделе **Параметры приложения** в разделе **Параметры окна документа**нажмите кнопку **Перекрывающиеся Windows**.</span><span class="sxs-lookup"><span data-stu-id="352c2-126">In the **Application Options** section, under **Document Window Options**, click **Overlapping Windows**.</span></span>

4.  <span data-ttu-id="352c2-127">Нажмите кнопку **ОК**и закройте и снова откройте базу данных.</span><span class="sxs-lookup"><span data-stu-id="352c2-127">Click **OK**, and then close and reopen the database.</span></span>

<span data-ttu-id="352c2-128">Это действие аналогично меню **переместить** или **размер** окна **элемента управления** .</span><span class="sxs-lookup"><span data-stu-id="352c2-128">This action is similar to clicking **Move** or **Size** on the window's **Control** menu.</span></span> <span data-ttu-id="352c2-129">С помощью команды меню используйте клавиши со стрелками для перемещения или изменить размеры этого окна.</span><span class="sxs-lookup"><span data-stu-id="352c2-129">With the menu commands, you use the keyboard's arrow keys to move or resize the window.</span></span> <span data-ttu-id="352c2-130">С действием **MoveAndSizeWindow** введите его положение и размер значения напрямую.</span><span class="sxs-lookup"><span data-stu-id="352c2-130">With the **MoveAndSizeWindow** action, you enter the position and size measurements directly.</span></span> <span data-ttu-id="352c2-131">Можно также использовать мышь в перемещение и размер windows.</span><span class="sxs-lookup"><span data-stu-id="352c2-131">You can also use the mouse to move and size windows.</span></span>

<span data-ttu-id="352c2-132">Это действие можно использовать для любого окна в любом представлении.</span><span class="sxs-lookup"><span data-stu-id="352c2-132">You can use this action on any window, in any view.</span></span>

<span data-ttu-id="352c2-133">\*\*Советы \*\*</span><span class="sxs-lookup"><span data-stu-id="352c2-133">**Tips**</span></span>

  - <span data-ttu-id="352c2-134">Переместить окно без его размера, введите значения для **вправо** и **вниз** аргументов, но оставить пустым аргументы **ширины** и **высоты** .</span><span class="sxs-lookup"><span data-stu-id="352c2-134">To move a window without resizing it, enter values for the **Right** and **Down** arguments but leave the **Width** and **Height** arguments blank.</span></span>

  - <span data-ttu-id="352c2-135">Чтобы изменить размер окна без перемещения, введите значения для **ширины** и **высоты** аргументов, но оставить пустым аргументы **вправо** и **вниз** .</span><span class="sxs-lookup"><span data-stu-id="352c2-135">To resize a window without moving it, enter values for the **Width** and **Height** arguments but leave the **Right** and **Down** arguments blank.</span></span>

<span data-ttu-id="352c2-136">Чтобы выполнить действие **MoveAndSizeWindow** в Visual Basic для приложений (VBA) модуль, используйте метод **СдвигРазмер** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="352c2-136">To run the **MoveAndSizeWindow** action in a Visual Basic for Applications (VBA) module, use the **MoveSize** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="352c2-137">Пример</span><span class="sxs-lookup"><span data-stu-id="352c2-137">Example</span></span>

<span data-ttu-id="352c2-138">**Синхронизация форм с помощью макроса (en)**</span><span class="sxs-lookup"><span data-stu-id="352c2-138">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="352c2-139">Следующий макрос открывает форму списка продуктов в правом нижнем углу формы Поставщики, отображение текущего поставщика продуктов.</span><span class="sxs-lookup"><span data-stu-id="352c2-139">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="352c2-140">Демонстрируется использование **эхо**, **MessageBox**, **КЭлементуУправления**, **ОстановитьМакрос**, **ОткрытьФорму**и **MoveAndSizeWindow** действий.</span><span class="sxs-lookup"><span data-stu-id="352c2-140">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="352c2-141">Также показано использование условного выражения с **MessageBox**, **КЭлементуУправления**« **Поставщики** ».</span><span class="sxs-lookup"><span data-stu-id="352c2-141">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="352c2-142">Этот макрос должен быть связан с кнопкой Обзор продуктов в форме Поставщики.</span><span class="sxs-lookup"><span data-stu-id="352c2-142">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="352c2-143">Condition</span><span class="sxs-lookup"><span data-stu-id="352c2-143">Condition</span></span></p></th>
<th><p><span data-ttu-id="352c2-144">Действие</span><span class="sxs-lookup"><span data-stu-id="352c2-144">Action</span></span></p></th>
<th><p><span data-ttu-id="352c2-145">Аргументы: параметр</span><span class="sxs-lookup"><span data-stu-id="352c2-145">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="352c2-146">Comment</span><span class="sxs-lookup"><span data-stu-id="352c2-146">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="352c2-147"><strong>Эхо</strong></span><span class="sxs-lookup"><span data-stu-id="352c2-147"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="352c2-148"><strong>Вывод на экран</strong>: <strong>Нет</strong></span><span class="sxs-lookup"><span data-stu-id="352c2-148"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="352c2-149">Остановите обновление экрана в процессе выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="352c2-149">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352c2-150">Функция IsNull ([код поставщика])</span><span class="sxs-lookup"><span data-stu-id="352c2-150">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="352c2-151"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="352c2-151"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="352c2-152"><strong>Сообщение</strong>: перемещение на запись поставщика, продукты, чтобы увидеть, затем нажмите кнопку Предварительный просмотр еще раз.</span><span class="sxs-lookup"><span data-stu-id="352c2-152"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="352c2-153"><strong>Звуковые сигналы</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Выбор поставщика</span><span class="sxs-lookup"><span data-stu-id="352c2-153"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="352c2-154">При отсутствии никто из современных поставщиков в форме Поставщики, отображается сообщение.</span><span class="sxs-lookup"><span data-stu-id="352c2-154">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="352c2-155"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="352c2-155"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="352c2-156"><strong>Имя элемента управления</strong>: CompanyName</span><span class="sxs-lookup"><span data-stu-id="352c2-156"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="352c2-157">Перемещение фокуса на элемент управления CompanyName.</span><span class="sxs-lookup"><span data-stu-id="352c2-157">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="352c2-158">...</span><span class="sxs-lookup"><span data-stu-id="352c2-158"></span></span></p></td>
<td><p><span data-ttu-id="352c2-159"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="352c2-159"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="352c2-160">Остановка макроса.</span><span class="sxs-lookup"><span data-stu-id="352c2-160">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="352c2-161"><strong>ОткрытьФорму</strong></span><span class="sxs-lookup"><span data-stu-id="352c2-161"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="352c2-162"><strong>Имя формы</strong>: список продуктов <strong>представления</strong>: <strong>Имя DatasheetFilter</strong>: <strong>условие отбора</strong>: [код поставщика] = [Forms]! [Поставщики]! [Код поставщика] <strong>Режим данных</strong>: <strong>Режим чтения OnlyWindow</strong>: <strong>Обычный</strong></span><span class="sxs-lookup"><span data-stu-id="352c2-162"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="352c2-163">Откройте форму списка продуктов и отображение текущего поставщика продуктов.</span><span class="sxs-lookup"><span data-stu-id="352c2-163">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="352c2-164"><strong>MoveAndSizeWindow</strong></span><span class="sxs-lookup"><span data-stu-id="352c2-164"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="352c2-165"><strong>Право</strong>: 0,7799&quot; <strong>вниз</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="352c2-165"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="352c2-166">Положение формы списка продуктов в нижней правой части формы Поставщики.</span><span class="sxs-lookup"><span data-stu-id="352c2-166">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

