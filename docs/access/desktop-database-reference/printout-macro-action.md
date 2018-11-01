---
title: Макрос макрокоманду
TOCTitle: PrintOut Macro Action
ms:assetid: 13688158-1cf1-4b2e-d90a-271c8890e413
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845432(v=office.15)
ms:contentKeyID: 48543368
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm1697
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6a0aa0ae6d992410d5bed6126bfe49d7e84e9135
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878733"
---
# <a name="printout-macro-action"></a><span data-ttu-id="dfcb0-102">Макрос макрокоманду</span><span class="sxs-lookup"><span data-stu-id="dfcb0-102">PrintOut Macro Action</span></span>


<span data-ttu-id="dfcb0-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dfcb0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dfcb0-104">**Макрокоманду** можно использовать для печати активного объекта в открытой базы данных.</span><span class="sxs-lookup"><span data-stu-id="dfcb0-104">You can use the **PrintOut** action to print the active object in the open database.</span></span> <span data-ttu-id="dfcb0-105">Можно распечатать таблицы данных, отчеты, формы, страницы доступа к данным и модули.</span><span class="sxs-lookup"><span data-stu-id="dfcb0-105">You can print datasheets, reports, forms, data access pages, and modules.</span></span>


> [!NOTE]
> <P><span data-ttu-id="dfcb0-p102">
		Эта действие не разрешено, если база данных не является доверенной. Дополнительные сведения о включении макросов см. по ссылкам в разделе See Also этой статьи.
</span><span class="sxs-lookup"><span data-stu-id="dfcb0-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="dfcb0-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="dfcb0-108">Setting</span></span>

<span data-ttu-id="dfcb0-109">**Макрокоманду** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="dfcb0-109">The **PrintOut** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dfcb0-110">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="dfcb0-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="dfcb0-111">Описание</span><span class="sxs-lookup"><span data-stu-id="dfcb0-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dfcb0-112"><strong>Диапазон печати</strong></span><span class="sxs-lookup"><span data-stu-id="dfcb0-112"><strong>Print Range</strong></span></span></p></td>
<td><p><span data-ttu-id="dfcb0-113">Диапазон для печати.</span><span class="sxs-lookup"><span data-stu-id="dfcb0-113">The range to print.</span></span> <span data-ttu-id="dfcb0-114">Выберите пункт <strong>все</strong> (пользователя можно распечатать все объекта), <strong>выбора</strong> (печатается часть выбранного объекта) или <strong>страниц</strong> (пользователь может указать диапазон страниц <strong>Из страницы</strong> и <strong>Страницы для</strong> аргументов) в <strong> Диапазон печати</strong> флажок в разделе <strong>Действие аргументы</strong> области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="dfcb0-114">Click <strong>All</strong> (the user can print all of the object), <strong>Selection</strong> (the user can print the part of the object that's selected), or <strong>Pages</strong> (the user can specify a range of pages in the <strong>Page From</strong> and <strong>Page To</strong> arguments) in the <strong>Print Range</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="dfcb0-115">Значение по умолчанию — <strong>все</strong>.</span><span class="sxs-lookup"><span data-stu-id="dfcb0-115">The default is <strong>All</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dfcb0-116"><strong>Страница с</strong></span><span class="sxs-lookup"><span data-stu-id="dfcb0-116"><strong>Page From</strong></span></span></p></td>
<td><p><span data-ttu-id="dfcb0-117">Первая страница для печати.</span><span class="sxs-lookup"><span data-stu-id="dfcb0-117">The first page to print.</span></span> <span data-ttu-id="dfcb0-118">Печать начинается в верхней части на этой странице.</span><span class="sxs-lookup"><span data-stu-id="dfcb0-118">Printing starts at the top of this page.</span></span> <span data-ttu-id="dfcb0-119">Этот аргумент является обязательным, если элемент <strong>страницы</strong> в поле <strong>Диапазон печати</strong> .</span><span class="sxs-lookup"><span data-stu-id="dfcb0-119">This argument is required if you select <strong>Pages</strong> in the <strong>Print Range</strong> box.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dfcb0-120"><strong>Страницы, чтобы</strong></span><span class="sxs-lookup"><span data-stu-id="dfcb0-120"><strong>Page To</strong></span></span></p></td>
<td><p><span data-ttu-id="dfcb0-121">Последняя страница для печати.</span><span class="sxs-lookup"><span data-stu-id="dfcb0-121">The last page to print.</span></span> <span data-ttu-id="dfcb0-122">Печать заканчивается в нижней части страницы.</span><span class="sxs-lookup"><span data-stu-id="dfcb0-122">Printing stops at the bottom of this page.</span></span> <span data-ttu-id="dfcb0-123">Этот аргумент является обязательным, если элемент <strong>страницы</strong> в поле <strong>Диапазон печати</strong> .</span><span class="sxs-lookup"><span data-stu-id="dfcb0-123">This argument is required if you select <strong>Pages</strong> in the <strong>Print Range</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dfcb0-124"><strong>Качество печати</strong></span><span class="sxs-lookup"><span data-stu-id="dfcb0-124"><strong>Print Quality</strong></span></span></p></td>
<td><p><span data-ttu-id="dfcb0-125">Качество печати.</span><span class="sxs-lookup"><span data-stu-id="dfcb0-125">The print quality.</span></span> <span data-ttu-id="dfcb0-126">Щелкните <strong>высокой</strong>, <strong>Medium</strong>, <strong>Low</strong>или <strong>черновиков</strong>.</span><span class="sxs-lookup"><span data-stu-id="dfcb0-126">Click <strong>High</strong>, <strong>Medium</strong>, <strong>Low</strong>, or <strong>Draft</strong>.</span></span> <span data-ttu-id="dfcb0-127">Чем ниже качество, скорость печатает.</span><span class="sxs-lookup"><span data-stu-id="dfcb0-127">The lower the quality, the faster the object prints.</span></span> <span data-ttu-id="dfcb0-128">Значение по умолчанию — <strong>высокий</strong>.</span><span class="sxs-lookup"><span data-stu-id="dfcb0-128">The default is <strong>High</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dfcb0-129"><strong>Копий</strong></span><span class="sxs-lookup"><span data-stu-id="dfcb0-129"><strong>Copies</strong></span></span></p></td>
<td><p><span data-ttu-id="dfcb0-130">Число копий для печати.</span><span class="sxs-lookup"><span data-stu-id="dfcb0-130">The number of copies to print.</span></span> <span data-ttu-id="dfcb0-131">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="dfcb0-131">The default is 1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dfcb0-132"><strong>Копиям</strong></span><span class="sxs-lookup"><span data-stu-id="dfcb0-132"><strong>Collate Copies</strong></span></span></p></td>
<td><p><span data-ttu-id="dfcb0-133">Нажмите кнопку <strong>Да</strong> (копиям распечатанных) или <strong>Нет</strong> (не копиям).</span><span class="sxs-lookup"><span data-stu-id="dfcb0-133">Click <strong>Yes</strong> (collate the printed copies) or <strong>No</strong> (do not collate copies).</span></span> <span data-ttu-id="dfcb0-134">Печать объекта может производиться быстрее, если этот аргумент задано значение <strong>No</strong>.</span><span class="sxs-lookup"><span data-stu-id="dfcb0-134">The object may print faster if this argument is set to <strong>No</strong>.</span></span> <span data-ttu-id="dfcb0-135">По умолчанию используется значение <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="dfcb0-135">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="dfcb0-136">Замечания</span><span class="sxs-lookup"><span data-stu-id="dfcb0-136">Remarks</span></span>

<span data-ttu-id="dfcb0-137">Это действие аналогично при выборе объекта, щелкнув вкладку **файл** и затем выбрав команду **Печать**.</span><span class="sxs-lookup"><span data-stu-id="dfcb0-137">This action is similar to selecting an object, clicking the **File** tab and then clicking **Print**.</span></span> <span data-ttu-id="dfcb0-138">С помощью этого действия тем не менее, не **Print** откроется диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="dfcb0-138">With this action, however, no **Print** dialog box appears.</span></span>


> [!TIP]
> <P><span data-ttu-id="dfcb0-139">При наличии определенного параметры печати часто используемых создайте макрос, содержащий <STRONG>макрокоманду с этими параметрами аргументов</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="dfcb0-139">If you have particular print settings you use frequently, create a macro containing a <STRONG>PrintOut</STRONG> action with these settings in its arguments.</span></span></P>



<span data-ttu-id="dfcb0-140">Аргументы для этого действия соответствующие параметры в диалоговом окне " **Печать** ".</span><span class="sxs-lookup"><span data-stu-id="dfcb0-140">The arguments for this action correspond to options in the **Print** dialog box.</span></span> <span data-ttu-id="dfcb0-141">Тем не менее в отличие от **НайтиЗапись** и диалоговое окно **Найти и заменить** параметры аргумент не предоставлен параметры диалогового окна **Печать** .</span><span class="sxs-lookup"><span data-stu-id="dfcb0-141">However, unlike the **FindRecord** action and **Find and Replace** dialog box, the argument settings aren't shared with the **Print** dialog box options.</span></span>

<span data-ttu-id="dfcb0-142">Чтобы запустить **макрокоманду** в Visual Basic для приложений (VBA) модуль, используйте метод **PrintOut** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="dfcb0-142">To run the **PrintOut** action in a Visual Basic for Applications (VBA) module, use the **PrintOut** method of the **DoCmd** object.</span></span>

