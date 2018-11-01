---
title: Действия OpenView макроса
TOCTitle: OpenView Macro Action
ms:assetid: 4d3b7e6d-4b81-4fbe-7222-24d745350321
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193569(v=office.15)
ms:contentKeyID: 48544726
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50135
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ee0a46e909c86534693638de98f42980bccfebba
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870172"
---
# <a name="openview-macro-action"></a><span data-ttu-id="1045a-102">Действия OpenView макроса</span><span class="sxs-lookup"><span data-stu-id="1045a-102">OpenView Macro Action</span></span>


<span data-ttu-id="1045a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1045a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1045a-104">В проекте Microsoft Access можно использовать **ОткрытьПредставление** , чтобы открыть представление в режиме таблицы, конструктора или просмотра.</span><span class="sxs-lookup"><span data-stu-id="1045a-104">In an Access project, you can use the **OpenView** action to open a view in Datasheet view, Design view, or Print Preview.</span></span> <span data-ttu-id="1045a-105">Это действие выполняется именованные представления при открытии в представлении таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="1045a-105">This action runs the named view when opened in Datasheet view.</span></span> <span data-ttu-id="1045a-106">Можно выбрать ввода данных для представления и ограничить записи, которые отображаются в представлении.</span><span class="sxs-lookup"><span data-stu-id="1045a-106">You can select data entry for the view and restrict the records that the view displays.</span></span>


> [!NOTE]
> <P><span data-ttu-id="1045a-p102">
		Эта действие не разрешено, если база данных не является доверенной. Дополнительные сведения о включении макросов см. по ссылкам в разделе See Also этой статьи.
</span><span class="sxs-lookup"><span data-stu-id="1045a-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="1045a-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="1045a-109">Setting</span></span>

<span data-ttu-id="1045a-110">**ОткрытьПредставление** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="1045a-110">The **OpenView** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1045a-111">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="1045a-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="1045a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="1045a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1045a-113"><strong>Имя представления</strong></span><span class="sxs-lookup"><span data-stu-id="1045a-113"><strong>View Name</strong></span></span></p></td>
<td><p><span data-ttu-id="1045a-114">Имя представления, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="1045a-114">The name of the view to open.</span></span> <span data-ttu-id="1045a-115">В поле <strong>Имя представления</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов содержит все представления в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="1045a-115">The <strong>View Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all views in the current database.</span></span> <span data-ttu-id="1045a-116">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="1045a-116">This is a required argument.</span></span> <span data-ttu-id="1045a-117">Если макрос, содержащий <strong>ОткрытьПредставление в базе данных библиотеки</strong> , Microsoft Access сначала выполняет поиск представления с этим именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="1045a-117">If you run a macro containing the <strong>OpenView</strong> action in a library database, Microsoft Access first looks for the view with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1045a-118"><strong>Просмотр</strong></span><span class="sxs-lookup"><span data-stu-id="1045a-118"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="1045a-119">Представление, в котором откроется представление.</span><span class="sxs-lookup"><span data-stu-id="1045a-119">The view in which the view will open.</span></span> <span data-ttu-id="1045a-120">Выберите <strong>таблицы</strong>, <strong>разработки</strong>, <strong>Режим предварительного просмотра</strong>, <strong>сводной таблицы</strong>или <strong>сводной диаграммы</strong> в поле <strong>View</strong> .</span><span class="sxs-lookup"><span data-stu-id="1045a-120">Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="1045a-121">Значение по умолчанию — <strong>таблицы данных</strong>.</span><span class="sxs-lookup"><span data-stu-id="1045a-121">The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1045a-122"><strong>Режим данных</strong></span><span class="sxs-lookup"><span data-stu-id="1045a-122"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="1045a-123">Режим ввода данных для представления.</span><span class="sxs-lookup"><span data-stu-id="1045a-123">The data entry mode for the view.</span></span> <span data-ttu-id="1045a-124">Это относится только к представлений, открытых в режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="1045a-124">This applies only to views opened in Datasheet view.</span></span> <span data-ttu-id="1045a-125">Нажмите кнопку <strong>Add</strong> (пользователь может добавлять новые записи, но не могут просматривать и изменять существующие записи), <strong>Изменение</strong> (пользователь может просматривать или изменять существующие записи и добавление новых записей) или <strong>Только для чтения</strong> (пользователь может только просматривать записи).</span><span class="sxs-lookup"><span data-stu-id="1045a-125">Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="1045a-126">Значение по умолчанию — <strong>Изменить</strong>.</span><span class="sxs-lookup"><span data-stu-id="1045a-126">The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1045a-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="1045a-127">Remarks</span></span>

<span data-ttu-id="1045a-128">Это действие аналогично дважды щелкнув представления в области переходов или щелкнув правой кнопкой мыши представления в области переходов и затем выбрав команду.</span><span class="sxs-lookup"><span data-stu-id="1045a-128">This action is similar to double-clicking a view in the Navigation Pane, or right-clicking the view in the Navigation Pane and then clicking the command you want.</span></span>

<span data-ttu-id="1045a-129">\*\*Советы \*\*</span><span class="sxs-lookup"><span data-stu-id="1045a-129">**Tips**</span></span>

  - <span data-ttu-id="1045a-130">Представления можно перетаскивать из области переходов в строку действие в макросе.</span><span class="sxs-lookup"><span data-stu-id="1045a-130">You can drag a view from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="1045a-131">Это автоматически создает **OpenView** действие, которое открывается представление в режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="1045a-131">This automatically creates an **OpenView** action that opens the view in Datasheet view.</span></span>

  - <span data-ttu-id="1045a-132">Если не требуется отображать системные сообщения, которые появляются при запуске представления (это представление и показывают количество записей, которые будут затронуты), можно использовать действие **УстановитьСообщения** отображение этих сообщений.</span><span class="sxs-lookup"><span data-stu-id="1045a-132">If you don't want to display the system messages that normally appear when a view is run (indicating it is a view and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="1045a-133">Чтобы запустить **ОткрытьПредставление** в Visual Basic для приложений (VBA) модуль, используйте метод **OpenView** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="1045a-133">To run the **OpenView** action in a Visual Basic for Applications (VBA) module, use the **OpenView** method of the **DoCmd** object.</span></span>

