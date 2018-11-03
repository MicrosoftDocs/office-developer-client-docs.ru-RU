---
title: Макрокоманда OpenFunction
TOCTitle: OpenFunction macro action
ms:assetid: 0446dbb9-c342-9225-27ba-b8a6892030e1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844833(v=office.15)
ms:contentKeyID: 48543005
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89179
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2a9a96b22669889cf4dc51984fc3d3c9f7623428
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930226"
---
# <a name="openfunction-macro-action"></a><span data-ttu-id="5c2d5-102">Макрокоманда OpenFunction</span><span class="sxs-lookup"><span data-stu-id="5c2d5-102">OpenFunction macro action</span></span>


<span data-ttu-id="5c2d5-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5c2d5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5c2d5-104">В проекте Microsoft Access можно использовать действие **ОткрытьФункцию** Открытие пользовательской функции в представлении таблицы данных, представление конструктора встроенные функции, представления SQL, текстовый редактор (для скалярные или таблице пользовательских функций), или режим предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-104">In an Access project, you can use the **OpenFunction** action to open a user-defined function in Datasheet view, inline function Design view, SQL Text Editor view (for a scalar or table user-defined function), or Print Preview.</span></span> <span data-ttu-id="5c2d5-105">Это действие выполняется пользовательской функции при открытии в представлении таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-105">This action runs the user-defined function when opened in Datasheet view.</span></span> <span data-ttu-id="5c2d5-106">Также можно выбрать режим ввода данных для пользовательских функций и ограничить записи, которые отображаются пользовательских функций.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-106">You can also select the data entry mode for the user-defined function and restrict the records that the user-defined function displays.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5c2d5-p102">
		Эта действие не разрешено, если база данных не является доверенной. Дополнительные сведения о включении макросов см. по ссылкам в разделе See Also этой статьи.
</span><span class="sxs-lookup"><span data-stu-id="5c2d5-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="5c2d5-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="5c2d5-109">Setting</span></span>

<span data-ttu-id="5c2d5-110">Действие **ОткрытьФункцию** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-110">The **OpenFunction** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5c2d5-111">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="5c2d5-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="5c2d5-112">Описание</span><span class="sxs-lookup"><span data-stu-id="5c2d5-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c2d5-113"><strong>Имя функции</strong></span><span class="sxs-lookup"><span data-stu-id="5c2d5-113"><strong>Function Name</strong></span></span></p></td>
<td><p><span data-ttu-id="5c2d5-114">Имя функции, определенной пользователем, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-114">The name of the user-defined function to open.</span></span> <span data-ttu-id="5c2d5-115">В поле <strong>Имя функции</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов показаны все пользовательские функции в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-115">The <strong>Function Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all user-defined functions in the current database.</span></span> <span data-ttu-id="5c2d5-116">Этот параметр является обязательным. Если макрос, содержащий действие <strong>функции</strong> в базе данных библиотеки, Microsoft Access сначала выполняет поиск функции с указанным именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-116">This is a required argument.If you run a macro containing the <strong>Function</strong> action in a library database, Microsoft Access first looks for the function with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c2d5-117"><strong>Просмотр</strong></span><span class="sxs-lookup"><span data-stu-id="5c2d5-117"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="5c2d5-118">Представление, в котором будут открываться пользовательских функций.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-118">The view in which the user-defined function will open.</span></span> <span data-ttu-id="5c2d5-119">Выберите <strong>таблицы</strong>, <strong>разработки</strong>, <strong>Режим предварительного просмотра</strong>, <strong>сводной таблицы</strong>или <strong>сводной диаграммы</strong> в поле <strong>View</strong> .</span><span class="sxs-lookup"><span data-stu-id="5c2d5-119">Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="5c2d5-120">Значение по умолчанию — <strong>таблицы данных</strong>.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-120">The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c2d5-121"><strong>Режим данных</strong></span><span class="sxs-lookup"><span data-stu-id="5c2d5-121"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="5c2d5-122">Режим ввода данных для пользовательских функций.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-122">The data entry mode for the user-defined function.</span></span> <span data-ttu-id="5c2d5-123">Это относится только к пользовательских функций, открытых в режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-123">This applies only to user-defined functions opened in Datasheet view.</span></span> <span data-ttu-id="5c2d5-124">Нажмите кнопку <strong>Add</strong> (пользователь может добавлять новые записи, но не могут просматривать и изменять существующие записи), <strong>Изменение</strong> (пользователь может просматривать или изменять существующие записи и добавление новых записей) или <strong>Только для чтения</strong> (пользователь может только просматривать записи).</span><span class="sxs-lookup"><span data-stu-id="5c2d5-124">Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="5c2d5-125">Значение по умолчанию — <strong>Изменить</strong>.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-125">The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5c2d5-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="5c2d5-126">Remarks</span></span>

<span data-ttu-id="5c2d5-127">Это действие аналогично дважды щелкнув пользовательской функции в области навигации или щелкнув правой кнопкой мыши функцию на левой панели навигации и выбрав представления.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-127">This action is similar to double-clicking a user-defined function in the Navigation Pane, or right-clicking the function in the Navigation Pane and selecting a view.</span></span>

<span data-ttu-id="5c2d5-128">Переключение в режим конструктора при открытом пользовательской функции удаляется значение аргумента **Режим данных** для пользовательских функций.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-128">Switching to Design view while the user-defined function is open removes the **Data Mode** argument setting for the user-defined function.</span></span> <span data-ttu-id="5c2d5-129">Этот параметр не действует, даже в том случае, если пользователь возвращается в режим таблицы.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-129">This setting is not in effect, even if the user returns to Datasheet view.</span></span>

<span data-ttu-id="5c2d5-130">\*\*Советы \*\*</span><span class="sxs-lookup"><span data-stu-id="5c2d5-130">**Tips**</span></span>

  - <span data-ttu-id="5c2d5-131">Можно выбрать пользовательской функции в области навигации и перетащите его в строку действие в макросе.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-131">You can select a user-defined function in the Navigation Pane and drag it to a macro action row.</span></span> <span data-ttu-id="5c2d5-132">Это автоматически создает **ОткрытьФункцию** действие, которое открывается пользовательских функций в представлении таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-132">This automatically creates an **OpenFunction** action that opens the user-defined function in Datasheet view.</span></span>

  - <span data-ttu-id="5c2d5-133">Если вы не хотите отобразить системные сообщения, которые появляются при выполнении функции, определенной пользователем (является пользовательской функции и показывают количество записей, которые будут затронуты), чтобы отключить отображение можно использовать действие **УстановитьСообщения** Эти сообщения.</span><span class="sxs-lookup"><span data-stu-id="5c2d5-133">If you don't want to display the system messages that normally appear when a user-defined function is run (indicating it is a user-defined function and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="5c2d5-134">Чтобы выполнить действие **ОткрытьФункцию** в Visual Basic для приложений (VBA) модуль, используйте метод **ОткрытьФункцию** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="5c2d5-134">To run the **OpenFunction** action in a Visual Basic for Applications (VBA) module, use the **OpenFunction** method of the **DoCmd** object.</span></span>

