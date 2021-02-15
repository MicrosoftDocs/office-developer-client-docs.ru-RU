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
localization_priority: Normal
ms.openlocfilehash: 10d55b435a59594eaf3e8380b6690ebbda63a258
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292162"
---
# <a name="gotopage-macro-action"></a><span data-ttu-id="7cd4a-102">Макрокоманда GoToPage</span><span class="sxs-lookup"><span data-stu-id="7cd4a-102">GoToPage macro action</span></span>

<span data-ttu-id="7cd4a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7cd4a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7cd4a-104">Вы можете использовать действие **GoToPage,** чтобы переместить фокус в активной форме на первый контроль на указанной странице.</span><span class="sxs-lookup"><span data-stu-id="7cd4a-104">You can use the **GoToPage** action to move the focus in the active form to the first control on a specified page.</span></span> <span data-ttu-id="7cd4a-105">Это действие можно использовать, если создана форма с разрывами страниц, которая содержит группы связанных сведений.</span><span class="sxs-lookup"><span data-stu-id="7cd4a-105">You can use this action if you have created a form with page breaks that contains groups of related information.</span></span> <span data-ttu-id="7cd4a-106">Например, у вас может быть форма "Сотрудники" с личной информацией на одной странице, сведения об office на другой странице и сведения о продажах на третьей странице.</span><span class="sxs-lookup"><span data-stu-id="7cd4a-106">For example, you might have an Employees form with personal information on one page, office information on another page, and sales information on a third page.</span></span> <span data-ttu-id="7cd4a-107">Для перемещения на нужную страницу можно использовать действие **GoToPage.**</span><span class="sxs-lookup"><span data-stu-id="7cd4a-107">You can use the **GoToPage** action to move to the desired page.</span></span> <span data-ttu-id="7cd4a-108">Вы также можете представить несколько страниц сведений в одной форме с помощью элементов управления вкладками.</span><span class="sxs-lookup"><span data-stu-id="7cd4a-108">You can also present multiple pages of information on a single form by using tab controls.</span></span>

## <a name="setting"></a><span data-ttu-id="7cd4a-109">Setting</span><span class="sxs-lookup"><span data-stu-id="7cd4a-109">Setting</span></span>

<span data-ttu-id="7cd4a-110">Действие **GoToPage** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="7cd4a-110">The **GoToPage** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7cd4a-111">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="7cd4a-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="7cd4a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="7cd4a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7cd4a-113"><strong>Номер страницы</strong></span><span class="sxs-lookup"><span data-stu-id="7cd4a-113"><strong>Page Number</strong></span></span></p></td>
<td><p><span data-ttu-id="7cd4a-114">Номер страницы, на которую нужно переместить фокус.</span><span class="sxs-lookup"><span data-stu-id="7cd4a-114">The number of the page to which you want to move the focus.</span></span> <span data-ttu-id="7cd4a-115">Введите номер страницы в поле <strong>"Номер</strong> страницы" в разделе <strong>"Аргументы действий"</strong> области построитель макроса.</span><span class="sxs-lookup"><span data-stu-id="7cd4a-115">Enter the page number in the <strong>Page Number</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="7cd4a-116">Если оставить этот аргумент пустым, фокус останется на текущей странице.</span><span class="sxs-lookup"><span data-stu-id="7cd4a-116">If you leave this argument blank, the focus stays on the current page.</span></span> <span data-ttu-id="7cd4a-117">Вы можете использовать <strong></strong> <strong>аргументы "Право"</strong> и "Вниз", чтобы отобразить часть нужной страницы.</span><span class="sxs-lookup"><span data-stu-id="7cd4a-117">You can use the <strong>Right</strong> and <strong>Down</strong> arguments to display the part of the page you want to see.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cd4a-118"><strong>Right</strong></span><span class="sxs-lookup"><span data-stu-id="7cd4a-118"><strong>Right</strong></span></span></p></td>
<td><p><span data-ttu-id="7cd4a-119">Горизонтальное положение места на странице, измеряемое от левого края окна, которое должно отображаться на левом краю окна.</span><span class="sxs-lookup"><span data-stu-id="7cd4a-119">The horizontal position of the spot on the page, measured from the left edge of its containing window, that is to appear at the left edge of the window.</span></span> <span data-ttu-id="7cd4a-120">Это необходимо при указании аргумента <strong>"Вниз".</strong></span><span class="sxs-lookup"><span data-stu-id="7cd4a-120">This is required if you specify a <strong>Down</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cd4a-121"><strong>Вниз</strong></span><span class="sxs-lookup"><span data-stu-id="7cd4a-121"><strong>Down</strong></span></span></p></td>
<td><p><span data-ttu-id="7cd4a-122">Вертикальное положение места на странице, измеряемое от верхнего края окна, которое должно отображаться в верхней части окна.</span><span class="sxs-lookup"><span data-stu-id="7cd4a-122">The vertical position of the spot on the page, measured from the top edge of its containing window, that is to appear at the top edge of the window.</span></span> <span data-ttu-id="7cd4a-123">Это необходимо, если указать правильный <strong>аргумент.</strong></span><span class="sxs-lookup"><span data-stu-id="7cd4a-123">This is required if you specify a <strong>Right</strong> argument.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="7cd4a-124">Аргументы **Right** и **Down** измеряются в дюймах или см в зависимости от региональных параметров в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="7cd4a-124">The **Right** and **Down** arguments are measured in inches or centimeters, depending on the regional settings in Windows Control Panel.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cd4a-125">Заметки</span><span class="sxs-lookup"><span data-stu-id="7cd4a-125">Remarks</span></span>

<span data-ttu-id="7cd4a-126">Это действие можно использовать для выбора первого (определенного по порядку табуляц формы) на указанной странице.</span><span class="sxs-lookup"><span data-stu-id="7cd4a-126">You can use this action to select the first control (as defined by the form's tab order) on the specified page.</span></span> <span data-ttu-id="7cd4a-127">Используйте действие **GoToControl для** перемещения в определенный контроль формы.</span><span class="sxs-lookup"><span data-stu-id="7cd4a-127">Use the **GoToControl** action to move to a particular control on the form.</span></span>

<span data-ttu-id="7cd4a-128">Вы можете использовать аргументы **"Право"** и **"Вниз"** для форм со страницами, размером больше, чем окно Access.</span><span class="sxs-lookup"><span data-stu-id="7cd4a-128">You can use the **Right** and **Down** arguments for forms with pages larger than the Access window.</span></span> <span data-ttu-id="7cd4a-129">Используйте аргумент **"Номер** страницы", чтобы перейти на нужную страницу, а затем используйте аргументы **"Право"** и "Вниз", чтобы отобразить нужную часть страницы. </span><span class="sxs-lookup"><span data-stu-id="7cd4a-129">Use the **Page Number** argument to move to the desired page, and then use the **Right** and **Down** arguments to display the part of the page you want to see.</span></span> <span data-ttu-id="7cd4a-130">Access отображает часть страницы, верхний левый угол которой смещен на указанное расстояние от левого верхнего угла страницы.</span><span class="sxs-lookup"><span data-stu-id="7cd4a-130">Access displays the part of the page whose upper-left corner is offset the specified distance from the upper-left corner of the page.</span></span>

<span data-ttu-id="7cd4a-131">Действие **GoToPage** нельзя использовать в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="7cd4a-131">You can't use the **GoToPage** action in the following cases:</span></span>

- <span data-ttu-id="7cd4a-132">Перемещение фокуса на страницу скрытой формы.</span><span class="sxs-lookup"><span data-stu-id="7cd4a-132">To move the focus to a page on a hidden form.</span></span>

- <span data-ttu-id="7cd4a-133">Перемещение фокуса с одной страницы на другую в пределах управления вкладками.</span><span class="sxs-lookup"><span data-stu-id="7cd4a-133">To move the focus from one page to another within the tab control.</span></span>

<span data-ttu-id="7cd4a-134">Чтобы запустить действие **GoToPage** в модуле Visual Basic для приложений (VBA), используйте метод **GoToPage** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="7cd4a-134">To run the **GoToPage** action in a Visual Basic for Applications (VBA) module, use the **GoToPage** method of the **DoCmd** object.</span></span>

