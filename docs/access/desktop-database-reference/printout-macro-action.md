---
title: Макрокоманда PrintOut
TOCTitle: PrintOut macro action
ms:assetid: 13688158-1cf1-4b2e-d90a-271c8890e413
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845432(v=office.15)
ms:contentKeyID: 48543368
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm1697
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 04212a8bf63d5039c6548463612f006f0d116229
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301409"
---
# <a name="printout-macro-action"></a><span data-ttu-id="925f6-102">Макрокоманда PrintOut</span><span class="sxs-lookup"><span data-stu-id="925f6-102">PrintOut macro action</span></span>

<span data-ttu-id="925f6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="925f6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="925f6-104">Вы можете использовать действие **Печать** для печати активного объекта в открытой базе данных.</span><span class="sxs-lookup"><span data-stu-id="925f6-104">You can use the **PrintOut** action to print the active object in the open database.</span></span> <span data-ttu-id="925f6-105">Можно распечатать таблицы, отчеты, формы, страницы доступа к данным и модули.</span><span class="sxs-lookup"><span data-stu-id="925f6-105">You can print datasheets, reports, forms, data access pages, and modules.</span></span>

> [!NOTE]
> <span data-ttu-id="925f6-106">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="925f6-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="925f6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="925f6-107">Setting</span></span>

<span data-ttu-id="925f6-108">Макрокоманда " **Печать** " имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="925f6-108">The **PrintOut** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="925f6-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="925f6-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="925f6-110">Описание</span><span class="sxs-lookup"><span data-stu-id="925f6-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="925f6-111"><strong>Диапазон печати</strong></span><span class="sxs-lookup"><span data-stu-id="925f6-111"><strong>Print Range</strong></span></span></p></td>
<td><p><span data-ttu-id="925f6-112">Диапазон для печати.</span><span class="sxs-lookup"><span data-stu-id="925f6-112">The range to print.</span></span> <span data-ttu-id="925f6-113">Нажмите кнопку <strong>все</strong> (пользователь может напечатать весь объект), выделенный <strong>фрагмент</strong> (пользователь может напечатать часть выбранного объекта) или <strong>страницы</strong> (пользователь может указать диапазон страниц на <strong>странице с</strong> и аргументы <strong>на странице</strong> ) в <strong> Поле диапазона печати</strong> в разделе <strong>аргументы макрокоманды</strong> в панели построителя макросов.</span><span class="sxs-lookup"><span data-stu-id="925f6-113">Click <strong>All</strong> (the user can print all of the object), <strong>Selection</strong> (the user can print the part of the object that's selected), or <strong>Pages</strong> (the user can specify a range of pages in the <strong>Page From</strong> and <strong>Page To</strong> arguments) in the <strong>Print Range</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="925f6-114">Значение по умолчанию — <strong>ALL</strong>.</span><span class="sxs-lookup"><span data-stu-id="925f6-114">The default is <strong>All</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="925f6-115"><strong>Страница из</strong></span><span class="sxs-lookup"><span data-stu-id="925f6-115"><strong>Page From</strong></span></span></p></td>
<td><p><span data-ttu-id="925f6-116">Первая страница, которую необходимо напечатать.</span><span class="sxs-lookup"><span data-stu-id="925f6-116">The first page to print.</span></span> <span data-ttu-id="925f6-117">Печать начинается в начале этой страницы.</span><span class="sxs-lookup"><span data-stu-id="925f6-117">Printing starts at the top of this page.</span></span> <span data-ttu-id="925f6-118">Этот аргумент является обязательным, если выбрать <strong>страницы</strong> в поле <strong>диапазон печати</strong> .</span><span class="sxs-lookup"><span data-stu-id="925f6-118">This argument is required if you select <strong>Pages</strong> in the <strong>Print Range</strong> box.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="925f6-119"><strong>Страницу, чтобы</strong></span><span class="sxs-lookup"><span data-stu-id="925f6-119"><strong>Page To</strong></span></span></p></td>
<td><p><span data-ttu-id="925f6-120">Последняя страница, которую необходимо напечатать.</span><span class="sxs-lookup"><span data-stu-id="925f6-120">The last page to print.</span></span> <span data-ttu-id="925f6-121">В нижней части этой страницы печать завершается.</span><span class="sxs-lookup"><span data-stu-id="925f6-121">Printing stops at the bottom of this page.</span></span> <span data-ttu-id="925f6-122">Этот аргумент является обязательным, если выбрать <strong>страницы</strong> в поле <strong>диапазон печати</strong> .</span><span class="sxs-lookup"><span data-stu-id="925f6-122">This argument is required if you select <strong>Pages</strong> in the <strong>Print Range</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="925f6-123"><strong>Качество печати</strong></span><span class="sxs-lookup"><span data-stu-id="925f6-123"><strong>Print Quality</strong></span></span></p></td>
<td><p><span data-ttu-id="925f6-124">Качество печати.</span><span class="sxs-lookup"><span data-stu-id="925f6-124">The print quality.</span></span> <span data-ttu-id="925f6-125">Выберите <strong>Высокая</strong>, <strong>Средняя</strong>, <strong>Минимальная</strong>или <strong>черновик</strong>.</span><span class="sxs-lookup"><span data-stu-id="925f6-125">Click <strong>High</strong>, <strong>Medium</strong>, <strong>Low</strong>, or <strong>Draft</strong>.</span></span> <span data-ttu-id="925f6-126">Чем ниже качество, тем быстрее печатается объект.</span><span class="sxs-lookup"><span data-stu-id="925f6-126">The lower the quality, the faster the object prints.</span></span> <span data-ttu-id="925f6-127">Значение по умолчанию — <strong>High</strong>.</span><span class="sxs-lookup"><span data-stu-id="925f6-127">The default is <strong>High</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="925f6-128"><strong>Copies</strong></span><span class="sxs-lookup"><span data-stu-id="925f6-128"><strong>Copies</strong></span></span></p></td>
<td><p><span data-ttu-id="925f6-129">Число копий для печати.</span><span class="sxs-lookup"><span data-stu-id="925f6-129">The number of copies to print.</span></span> <span data-ttu-id="925f6-130">По умолчанию используется значение 1.</span><span class="sxs-lookup"><span data-stu-id="925f6-130">The default is 1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="925f6-131"><strong>Разбор по копиям</strong></span><span class="sxs-lookup"><span data-stu-id="925f6-131"><strong>Collate Copies</strong></span></span></p></td>
<td><p><span data-ttu-id="925f6-132">Нажмите кнопку <strong>Да</strong> (разобрание распечатанных копий) или <strong>нет</strong> (не разбирать по копиям).</span><span class="sxs-lookup"><span data-stu-id="925f6-132">Click <strong>Yes</strong> (collate the printed copies) or <strong>No</strong> (do not collate copies).</span></span> <span data-ttu-id="925f6-133">Объект может печататься быстрее, если для этого аргумента задано значение <strong>нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="925f6-133">The object may print faster if this argument is set to <strong>No</strong>.</span></span> <span data-ttu-id="925f6-134">Значение по умолчанию — <strong>Yes</strong>.</span><span class="sxs-lookup"><span data-stu-id="925f6-134">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="925f6-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="925f6-135">Remarks</span></span>

<span data-ttu-id="925f6-136">Это действие аналогично выбору объекта, щелчком на вкладке **файл** и нажатием кнопки **Печать**.</span><span class="sxs-lookup"><span data-stu-id="925f6-136">This action is similar to selecting an object, clicking the **File** tab and then clicking **Print**.</span></span> <span data-ttu-id="925f6-137">Однако это действие не появление диалогового окна " **Печать** ".</span><span class="sxs-lookup"><span data-stu-id="925f6-137">With this action, however, no **Print** dialog box appears.</span></span>

> [!TIP]
> <span data-ttu-id="925f6-138">Если вы часто используете конкретные параметры печати, создайте макрос, содержащий действие расПечатки, с помощью этих параметров в аргументах. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="925f6-138">If you have particular print settings you use frequently, create a macro containing a **PrintOut** action with these settings in its arguments.</span></span>

<span data-ttu-id="925f6-139">Аргументы этого действия соответствуют параметрам в диалоговом окне " **Печать** ".</span><span class="sxs-lookup"><span data-stu-id="925f6-139">The arguments for this action correspond to options in the **Print** dialog box.</span></span> <span data-ttu-id="925f6-140">Однако в отличие от диалогового окна "Макрокоманда" **найти и заменить** "Параметры аргумента не являются общими с параметрами диалогового окна" \*\*\*\* **Печать** ".</span><span class="sxs-lookup"><span data-stu-id="925f6-140">However, unlike the **FindRecord** action and **Find and Replace** dialog box, the argument settings aren't shared with the **Print** dialog box options.</span></span>

<span data-ttu-id="925f6-141">Чтобы выполнить действие \*\*\*\* по распечатке в модуле Visual Basic для приложений (VBA), используйте метод **PrintOut** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="925f6-141">To run the **PrintOut** action in a Visual Basic for Applications (VBA) module, use the **PrintOut** method of the **DoCmd** object.</span></span>

