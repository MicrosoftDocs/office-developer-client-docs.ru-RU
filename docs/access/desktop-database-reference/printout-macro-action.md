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
ms.openlocfilehash: c2e5b3e2cdfb743df8a098d3978ccd3d6eb66d90
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999031"
---
# <a name="printout-macro-action"></a><span data-ttu-id="435d4-102">Макрокоманда PrintOut</span><span class="sxs-lookup"><span data-stu-id="435d4-102">PrintOut macro action</span></span>

<span data-ttu-id="435d4-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="435d4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="435d4-104">**Макрокоманду** можно использовать для печати активного объекта в открытой базы данных.</span><span class="sxs-lookup"><span data-stu-id="435d4-104">You can use the **PrintOut** action to print the active object in the open database.</span></span> <span data-ttu-id="435d4-105">Можно распечатать таблицы данных, отчеты, формы, страницы доступа к данным и модули.</span><span class="sxs-lookup"><span data-stu-id="435d4-105">You can print datasheets, reports, forms, data access pages, and modules.</span></span>

> [!NOTE]
> <span data-ttu-id="435d4-106">Это действие не разрешено, если база данных не является доверенной.</span><span class="sxs-lookup"><span data-stu-id="435d4-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="435d4-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="435d4-107">Setting</span></span>

<span data-ttu-id="435d4-108">**Макрокоманду** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="435d4-108">The **PrintOut** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="435d4-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="435d4-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="435d4-110">Описание</span><span class="sxs-lookup"><span data-stu-id="435d4-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="435d4-111"><strong>Диапазон печати</strong></span><span class="sxs-lookup"><span data-stu-id="435d4-111"><strong>Print Range</strong></span></span></p></td>
<td><p><span data-ttu-id="435d4-112">Диапазон для печати.</span><span class="sxs-lookup"><span data-stu-id="435d4-112">The range to print.</span></span> <span data-ttu-id="435d4-113">Выберите пункт <strong>все</strong> (пользователя можно распечатать все объекта), <strong>выбора</strong> (печатается часть выбранного объекта) или <strong>страниц</strong> (пользователь может указать диапазон страниц <strong>Из страницы</strong> и <strong>Страницы для</strong> аргументов) в <strong> Диапазон печати</strong> флажок в разделе <strong>Действие аргументы</strong> области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="435d4-113">Click <strong>All</strong> (the user can print all of the object), <strong>Selection</strong> (the user can print the part of the object that's selected), or <strong>Pages</strong> (the user can specify a range of pages in the <strong>Page From</strong> and <strong>Page To</strong> arguments) in the <strong>Print Range</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="435d4-114">Значение по умолчанию — <strong>все</strong>.</span><span class="sxs-lookup"><span data-stu-id="435d4-114">The default is <strong>All</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="435d4-115"><strong>Страница с</strong></span><span class="sxs-lookup"><span data-stu-id="435d4-115"><strong>Page From</strong></span></span></p></td>
<td><p><span data-ttu-id="435d4-116">Первая страница для печати.</span><span class="sxs-lookup"><span data-stu-id="435d4-116">The first page to print.</span></span> <span data-ttu-id="435d4-117">Печать начинается в верхней части на этой странице.</span><span class="sxs-lookup"><span data-stu-id="435d4-117">Printing starts at the top of this page.</span></span> <span data-ttu-id="435d4-118">Этот аргумент является обязательным, если элемент <strong>страницы</strong> в поле <strong>Диапазон печати</strong> .</span><span class="sxs-lookup"><span data-stu-id="435d4-118">This argument is required if you select <strong>Pages</strong> in the <strong>Print Range</strong> box.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="435d4-119"><strong>Страницы, чтобы</strong></span><span class="sxs-lookup"><span data-stu-id="435d4-119"><strong>Page To</strong></span></span></p></td>
<td><p><span data-ttu-id="435d4-120">Последняя страница для печати.</span><span class="sxs-lookup"><span data-stu-id="435d4-120">The last page to print.</span></span> <span data-ttu-id="435d4-121">Печать заканчивается в нижней части страницы.</span><span class="sxs-lookup"><span data-stu-id="435d4-121">Printing stops at the bottom of this page.</span></span> <span data-ttu-id="435d4-122">Этот аргумент является обязательным, если элемент <strong>страницы</strong> в поле <strong>Диапазон печати</strong> .</span><span class="sxs-lookup"><span data-stu-id="435d4-122">This argument is required if you select <strong>Pages</strong> in the <strong>Print Range</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="435d4-123"><strong>Качество печати</strong></span><span class="sxs-lookup"><span data-stu-id="435d4-123"><strong>Print Quality</strong></span></span></p></td>
<td><p><span data-ttu-id="435d4-124">Качество печати.</span><span class="sxs-lookup"><span data-stu-id="435d4-124">The print quality.</span></span> <span data-ttu-id="435d4-125">Щелкните <strong>высокой</strong>, <strong>Medium</strong>, <strong>Low</strong>или <strong>черновиков</strong>.</span><span class="sxs-lookup"><span data-stu-id="435d4-125">Click <strong>High</strong>, <strong>Medium</strong>, <strong>Low</strong>, or <strong>Draft</strong>.</span></span> <span data-ttu-id="435d4-126">Чем ниже качество, скорость печатает.</span><span class="sxs-lookup"><span data-stu-id="435d4-126">The lower the quality, the faster the object prints.</span></span> <span data-ttu-id="435d4-127">Значение по умолчанию — <strong>высокий</strong>.</span><span class="sxs-lookup"><span data-stu-id="435d4-127">The default is <strong>High</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="435d4-128"><strong>Копий</strong></span><span class="sxs-lookup"><span data-stu-id="435d4-128"><strong>Copies</strong></span></span></p></td>
<td><p><span data-ttu-id="435d4-129">Число копий для печати.</span><span class="sxs-lookup"><span data-stu-id="435d4-129">The number of copies to print.</span></span> <span data-ttu-id="435d4-130">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="435d4-130">The default is 1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="435d4-131"><strong>Копиям</strong></span><span class="sxs-lookup"><span data-stu-id="435d4-131"><strong>Collate Copies</strong></span></span></p></td>
<td><p><span data-ttu-id="435d4-132">Нажмите кнопку <strong>Да</strong> (копиям распечатанных) или <strong>Нет</strong> (не копиям).</span><span class="sxs-lookup"><span data-stu-id="435d4-132">Click <strong>Yes</strong> (collate the printed copies) or <strong>No</strong> (do not collate copies).</span></span> <span data-ttu-id="435d4-133">Печать объекта может производиться быстрее, если этот аргумент задано значение <strong>No</strong>.</span><span class="sxs-lookup"><span data-stu-id="435d4-133">The object may print faster if this argument is set to <strong>No</strong>.</span></span> <span data-ttu-id="435d4-134">По умолчанию используется значение <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="435d4-134">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="435d4-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="435d4-135">Remarks</span></span>

<span data-ttu-id="435d4-136">Это действие аналогично при выборе объекта, щелкнув вкладку **файл** и затем выбрав команду **Печать**.</span><span class="sxs-lookup"><span data-stu-id="435d4-136">This action is similar to selecting an object, clicking the **File** tab and then clicking **Print**.</span></span> <span data-ttu-id="435d4-137">С помощью этого действия тем не менее, не **Print** откроется диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="435d4-137">With this action, however, no **Print** dialog box appears.</span></span>

> [!TIP]
> <span data-ttu-id="435d4-138">При наличии определенного параметры печати часто используемых создайте макрос, содержащий **макрокоманду с этими параметрами аргументов** .</span><span class="sxs-lookup"><span data-stu-id="435d4-138">If you have particular print settings you use frequently, create a macro containing a **PrintOut** action with these settings in its arguments.</span></span>

<span data-ttu-id="435d4-139">Аргументы для этого действия соответствующие параметры в диалоговом окне " **Печать** ".</span><span class="sxs-lookup"><span data-stu-id="435d4-139">The arguments for this action correspond to options in the **Print** dialog box.</span></span> <span data-ttu-id="435d4-140">Тем не менее в отличие от **НайтиЗапись** и диалоговое окно **Найти и заменить** параметры аргумент не предоставлен параметры диалогового окна **Печать** .</span><span class="sxs-lookup"><span data-stu-id="435d4-140">However, unlike the **FindRecord** action and **Find and Replace** dialog box, the argument settings aren't shared with the **Print** dialog box options.</span></span>

<span data-ttu-id="435d4-141">Чтобы запустить **макрокоманду** в Visual Basic для приложений (VBA) модуль, используйте метод **PrintOut** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="435d4-141">To run the **PrintOut** action in a Visual Basic for Applications (VBA) module, use the **PrintOut** method of the **DoCmd** object.</span></span>

