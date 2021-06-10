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
# <a name="gotopage-macro-action"></a><span data-ttu-id="b3f50-102">Макрокоманда GoToPage</span><span class="sxs-lookup"><span data-stu-id="b3f50-102">GoToPage macro action</span></span>

<span data-ttu-id="b3f50-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3f50-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b3f50-104">Вы можете использовать **действие GoToPage,** чтобы переместить фокус в активной форме на первый контроль на указанной странице.</span><span class="sxs-lookup"><span data-stu-id="b3f50-104">You can use the **GoToPage** action to move the focus in the active form to the first control on a specified page.</span></span> <span data-ttu-id="b3f50-105">Вы можете использовать это действие, если вы создали форму с разрывами страниц, которая содержит группы связанных сведений.</span><span class="sxs-lookup"><span data-stu-id="b3f50-105">You can use this action if you have created a form with page breaks that contains groups of related information.</span></span> <span data-ttu-id="b3f50-106">Например, на одной странице может быть форма Сотрудников с персональными данными, сведения об офисе на другой странице и сведения о продажах на третьей странице.</span><span class="sxs-lookup"><span data-stu-id="b3f50-106">For example, you might have an Employees form with personal information on one page, office information on another page, and sales information on a third page.</span></span> <span data-ttu-id="b3f50-107">Вы можете использовать **действие GoToPage** для перемещения на нужную страницу.</span><span class="sxs-lookup"><span data-stu-id="b3f50-107">You can use the **GoToPage** action to move to the desired page.</span></span> <span data-ttu-id="b3f50-108">Вы также можете представить несколько страниц информации в одной форме с помощью элементов управления вкладками.</span><span class="sxs-lookup"><span data-stu-id="b3f50-108">You can also present multiple pages of information on a single form by using tab controls.</span></span>

## <a name="setting"></a><span data-ttu-id="b3f50-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="b3f50-109">Setting</span></span>

<span data-ttu-id="b3f50-110">Действие **GoToPage** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="b3f50-110">The **GoToPage** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b3f50-111">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="b3f50-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b3f50-112">Описание</span><span class="sxs-lookup"><span data-stu-id="b3f50-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b3f50-113"><strong>Номер страницы</strong></span><span class="sxs-lookup"><span data-stu-id="b3f50-113"><strong>Page Number</strong></span></span></p></td>
<td><p><span data-ttu-id="b3f50-114">Число страницы, на которую необходимо переместить фокус.</span><span class="sxs-lookup"><span data-stu-id="b3f50-114">The number of the page to which you want to move the focus.</span></span> <span data-ttu-id="b3f50-115">Введите номер страницы в поле <strong>Номер страницы</strong> в разделе <strong>Аргументы</strong> действий в области Macro Builder.</span><span class="sxs-lookup"><span data-stu-id="b3f50-115">Enter the page number in the <strong>Page Number</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="b3f50-116">Если оставить этот аргумент пустым, фокус остается на текущей странице.</span><span class="sxs-lookup"><span data-stu-id="b3f50-116">If you leave this argument blank, the focus stays on the current page.</span></span> <span data-ttu-id="b3f50-117">Для отображения <strong></strong> нужной <strong></strong> части страницы можно использовать аргументы "Право и вниз".</span><span class="sxs-lookup"><span data-stu-id="b3f50-117">You can use the <strong>Right</strong> and <strong>Down</strong> arguments to display the part of the page you want to see.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3f50-118"><strong>Right</strong></span><span class="sxs-lookup"><span data-stu-id="b3f50-118"><strong>Right</strong></span></span></p></td>
<td><p><span data-ttu-id="b3f50-119">Горизонтальное положение пятна на странице, измеряемое с левого края его содержащего окна, которое должно отображаться на левом краю окна.</span><span class="sxs-lookup"><span data-stu-id="b3f50-119">The horizontal position of the spot on the page, measured from the left edge of its containing window, that is to appear at the left edge of the window.</span></span> <span data-ttu-id="b3f50-120">Это необходимо, если указать аргумент <strong>Down.</strong></span><span class="sxs-lookup"><span data-stu-id="b3f50-120">This is required if you specify a <strong>Down</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3f50-121"><strong>Down</strong></span><span class="sxs-lookup"><span data-stu-id="b3f50-121"><strong>Down</strong></span></span></p></td>
<td><p><span data-ttu-id="b3f50-122">Вертикальное положение пятна на странице, измеряемое с верхнего края его содержащего окна, которое должно отображаться на верхнем краю окна.</span><span class="sxs-lookup"><span data-stu-id="b3f50-122">The vertical position of the spot on the page, measured from the top edge of its containing window, that is to appear at the top edge of the window.</span></span> <span data-ttu-id="b3f50-123">Это необходимо, если указать правильный <strong>аргумент.</strong></span><span class="sxs-lookup"><span data-stu-id="b3f50-123">This is required if you specify a <strong>Right</strong> argument.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="b3f50-124">Аргументы **Right** и **Down** измеряются в дюймах или сантиметрах в зависимости от региональных параметров Windows панели управления.</span><span class="sxs-lookup"><span data-stu-id="b3f50-124">The **Right** and **Down** arguments are measured in inches or centimeters, depending on the regional settings in Windows Control Panel.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3f50-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="b3f50-125">Remarks</span></span>

<span data-ttu-id="b3f50-126">Это действие можно использовать для выбора первого управления (как определено порядком вкладки формы) на указанной странице.</span><span class="sxs-lookup"><span data-stu-id="b3f50-126">You can use this action to select the first control (as defined by the form's tab order) on the specified page.</span></span> <span data-ttu-id="b3f50-127">Чтобы перейти к определенному контролю формы, используйте действие **GoToControl.**</span><span class="sxs-lookup"><span data-stu-id="b3f50-127">Use the **GoToControl** action to move to a particular control on the form.</span></span>

<span data-ttu-id="b3f50-128">Аргументы **"Право** и **вниз"** можно использовать для форм со страницами, размером больше, чем окно Access.</span><span class="sxs-lookup"><span data-stu-id="b3f50-128">You can use the **Right** and **Down** arguments for forms with pages larger than the Access window.</span></span> <span data-ttu-id="b3f50-129">Используйте аргумент **Номер страницы,** чтобы перейти на нужную  страницу, а затем используйте аргументы **"Право"** и "Вниз", чтобы отобразить нужную часть страницы.</span><span class="sxs-lookup"><span data-stu-id="b3f50-129">Use the **Page Number** argument to move to the desired page, and then use the **Right** and **Down** arguments to display the part of the page you want to see.</span></span> <span data-ttu-id="b3f50-130">Доступ отображает часть страницы, верхний левый угол которой смещен заданным расстоянием от верхнего левого угла страницы.</span><span class="sxs-lookup"><span data-stu-id="b3f50-130">Access displays the part of the page whose upper-left corner is offset the specified distance from the upper-left corner of the page.</span></span>

<span data-ttu-id="b3f50-131">Действие **GoToPage** нельзя использовать в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="b3f50-131">You can't use the **GoToPage** action in the following cases:</span></span>

- <span data-ttu-id="b3f50-132">Перемещение фокуса на страницу в скрытой форме.</span><span class="sxs-lookup"><span data-stu-id="b3f50-132">To move the focus to a page on a hidden form.</span></span>

- <span data-ttu-id="b3f50-133">Перемещение фокуса с одной страницы на другую в области управления вкладками.</span><span class="sxs-lookup"><span data-stu-id="b3f50-133">To move the focus from one page to another within the tab control.</span></span>

<span data-ttu-id="b3f50-134">Чтобы выполнить **действие GoToPage** в Visual Basic для приложений (VBA), используйте метод **GoToPage** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="b3f50-134">To run the **GoToPage** action in a Visual Basic for Applications (VBA) module, use the **GoToPage** method of the **DoCmd** object.</span></span>

