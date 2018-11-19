---
title: Макрокоманда GoToPage
TOCTitle: GoToPage macro action
ms:assetid: 611aadff-83b7-e74d-4093-93fb5ce6e3ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194858(v=office.15)
ms:contentKeyID: 48545199
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm129285
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 179ee840370cef98c70e947cef555401408bbe12
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026227"
---
# <a name="gotopage-macro-action"></a><span data-ttu-id="c0e18-102">Макрокоманда GoToPage</span><span class="sxs-lookup"><span data-stu-id="c0e18-102">GoToPage macro action</span></span>

<span data-ttu-id="c0e18-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c0e18-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c0e18-104">Действие **НаСтраницу** можно использовать для перемещения фокуса в активной форме на первый элемент управления на указанной странице.</span><span class="sxs-lookup"><span data-stu-id="c0e18-104">You can use the **GoToPage** action to move the focus in the active form to the first control on a specified page.</span></span> <span data-ttu-id="c0e18-105">Это действие можно использовать при создании формы с разрывов страниц, которые содержит группы связанные сведения.</span><span class="sxs-lookup"><span data-stu-id="c0e18-105">You can use this action if you have created a form with page breaks that contains groups of related information.</span></span> <span data-ttu-id="c0e18-106">К примеру может иметь форму сотрудников с персональными данными на одну страницу, сведения о office на другую страницу и сведения о продажах на третьей страницы.</span><span class="sxs-lookup"><span data-stu-id="c0e18-106">For example, you might have an Employees form with personal information on one page, office information on another page, and sales information on a third page.</span></span> <span data-ttu-id="c0e18-107">Действие **НаСтраницу** можно использовать для перемещения на нужную страницу.</span><span class="sxs-lookup"><span data-stu-id="c0e18-107">You can use the **GoToPage** action to move to the desired page.</span></span> <span data-ttu-id="c0e18-108">Также можно представить несколько страниц сведения для одной формы с помощью элементов управления вкладки.</span><span class="sxs-lookup"><span data-stu-id="c0e18-108">You can also present multiple pages of information on a single form by using tab controls.</span></span>

## <a name="setting"></a><span data-ttu-id="c0e18-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="c0e18-109">Setting</span></span>

<span data-ttu-id="c0e18-110">Действие **НаСтраницу** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="c0e18-110">The **GoToPage** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c0e18-111">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="c0e18-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="c0e18-112">Описание</span><span class="sxs-lookup"><span data-stu-id="c0e18-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0e18-113"><strong>Номер страницы</strong></span><span class="sxs-lookup"><span data-stu-id="c0e18-113"><strong>Page Number</strong></span></span></p></td>
<td><p><span data-ttu-id="c0e18-114">Номер страницы, на который необходимо переместить фокус.</span><span class="sxs-lookup"><span data-stu-id="c0e18-114">The number of the page to which you want to move the focus.</span></span> <span data-ttu-id="c0e18-115">Введите номер в поле <strong>Номер страницы</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="c0e18-115">Enter the page number in the <strong>Page Number</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="c0e18-116">Если оставить это аргумент, фокус остается на текущей странице.</span><span class="sxs-lookup"><span data-stu-id="c0e18-116">If you leave this argument blank, the focus stays on the current page.</span></span> <span data-ttu-id="c0e18-117">Аргументы <strong>вправо</strong> и <strong>вниз</strong> можно использовать для отображения части страницы, которую необходимо просмотреть.</span><span class="sxs-lookup"><span data-stu-id="c0e18-117">You can use the <strong>Right</strong> and <strong>Down</strong> arguments to display the part of the page you want to see.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0e18-118"><strong>Right</strong></span><span class="sxs-lookup"><span data-stu-id="c0e18-118"><strong>Right</strong></span></span></p></td>
<td><p><span data-ttu-id="c0e18-119">Горизонтальную позицию точки на странице относительно левого края содержащего его окна, который будет отображаться в левой части окна.</span><span class="sxs-lookup"><span data-stu-id="c0e18-119">The horizontal position of the spot on the page, measured from the left edge of its containing window, that is to appear at the left edge of the window.</span></span> <span data-ttu-id="c0e18-120">Это является обязательным, если указан аргумент <strong>вниз</strong> .</span><span class="sxs-lookup"><span data-stu-id="c0e18-120">This is required if you specify a <strong>Down</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0e18-121"><strong>Вниз</strong></span><span class="sxs-lookup"><span data-stu-id="c0e18-121"><strong>Down</strong></span></span></p></td>
<td><p><span data-ttu-id="c0e18-122">Вертикальное положение место на странице относительно верхнего края содержащего его окна, который будет отображаться в верхней границы окна.</span><span class="sxs-lookup"><span data-stu-id="c0e18-122">The vertical position of the spot on the page, measured from the top edge of its containing window, that is to appear at the top edge of the window.</span></span> <span data-ttu-id="c0e18-123">Это является обязательным, если указан аргумент <strong>вправо</strong> .</span><span class="sxs-lookup"><span data-stu-id="c0e18-123">This is required if you specify a <strong>Right</strong> argument.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="c0e18-124">Аргументы **вправо** и **вниз** заданная в дюймах или сантиметрах, в зависимости от региональных параметров в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="c0e18-124">The **Right** and **Down** arguments are measured in inches or centimeters, depending on the regional settings in Windows Control Panel.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0e18-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="c0e18-125">Remarks</span></span>

<span data-ttu-id="c0e18-126">Это действие можно использовать для выбора первый элемент управления (как определено в последовательности табуляции формы) на указанной странице.</span><span class="sxs-lookup"><span data-stu-id="c0e18-126">You can use this action to select the first control (as defined by the form's tab order) on the specified page.</span></span> <span data-ttu-id="c0e18-127">Используйте **КЭлементуУправления** для перемещения для определенного элемента управления в форме.</span><span class="sxs-lookup"><span data-stu-id="c0e18-127">Use the **GoToControl** action to move to a particular control on the form.</span></span>

<span data-ttu-id="c0e18-128">Аргументы **вправо** и **вниз** для форм можно использовать со страницы, размер которых превышает окна клиента.</span><span class="sxs-lookup"><span data-stu-id="c0e18-128">You can use the **Right** and **Down** arguments for forms with pages larger than the Access window.</span></span> <span data-ttu-id="c0e18-129">Использовать аргумент **Номер страницы** для перехода на нужную страницу, а затем аргументы **вправо** и **вниз** для отображения части страницы, которую необходимо просмотреть.</span><span class="sxs-lookup"><span data-stu-id="c0e18-129">Use the **Page Number** argument to move to the desired page, and then use the **Right** and **Down** arguments to display the part of the page you want to see.</span></span> <span data-ttu-id="c0e18-130">Access отображает часть страницы, верхний левый угол смещения на определенное расстояние от левом верхнем углу страницы.</span><span class="sxs-lookup"><span data-stu-id="c0e18-130">Access displays the part of the page whose upper-left corner is offset the specified distance from the upper-left corner of the page.</span></span>

<span data-ttu-id="c0e18-131">Действие **НаСтраницу** нельзя использовать в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="c0e18-131">You can't use the **GoToPage** action in the following cases:</span></span>

- <span data-ttu-id="c0e18-132">Для перемещения фокуса на страницу в скрытой форме.</span><span class="sxs-lookup"><span data-stu-id="c0e18-132">To move the focus to a page on a hidden form.</span></span>

- <span data-ttu-id="c0e18-133">Для перемещения фокуса с одной страницы на другой в пределах вкладок.</span><span class="sxs-lookup"><span data-stu-id="c0e18-133">To move the focus from one page to another within the tab control.</span></span>

<span data-ttu-id="c0e18-134">Чтобы выполнить действие **НаСтраницу** в Visual Basic для приложений (VBA) модуль, используйте метод **НаСтраницу** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="c0e18-134">To run the **GoToPage** action in a Visual Basic for Applications (VBA) module, use the **GoToPage** method of the **DoCmd** object.</span></span>

