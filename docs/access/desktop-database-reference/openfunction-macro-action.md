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
localization_priority: Normal
ms.openlocfilehash: b13d21ef1bd8a95587eb78cd448f19f9fd0c24c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288366"
---
# <a name="openfunction-macro-action"></a><span data-ttu-id="789d3-102">Макрокоманда OpenFunction</span><span class="sxs-lookup"><span data-stu-id="789d3-102">OpenFunction macro action</span></span>

<span data-ttu-id="789d3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="789d3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="789d3-104">В проекте Access вы можете использовать действие **опенфунктион** , чтобы открыть пользовательскую функцию в представлении таблицы данных, режиме конструктора для встроенной функции, в представлении "текстовый редактор SQL" (для скалярной или табличной пользовательской функции) или в режиме предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="789d3-104">In an Access project, you can use the **OpenFunction** action to open a user-defined function in Datasheet view, inline function Design view, SQL Text Editor view (for a scalar or table user-defined function), or Print Preview.</span></span> <span data-ttu-id="789d3-105">Это действие запускает пользовательскую функцию при открытии в режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="789d3-105">This action runs the user-defined function when opened in Datasheet view.</span></span> <span data-ttu-id="789d3-106">Вы также можете выбрать режим ввода данных для пользовательской функции и ограничить записи, которые отображаются в пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="789d3-106">You can also select the data entry mode for the user-defined function and restrict the records that the user-defined function displays.</span></span>

> [!NOTE]
> <span data-ttu-id="789d3-107">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="789d3-107">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="789d3-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="789d3-108">Setting</span></span>

<span data-ttu-id="789d3-109">Макрокоманда **опенфунктион** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="789d3-109">The **OpenFunction** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="789d3-110">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="789d3-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="789d3-111">Описание</span><span class="sxs-lookup"><span data-stu-id="789d3-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="789d3-112"><strong>Имя функции</strong></span><span class="sxs-lookup"><span data-stu-id="789d3-112"><strong>Function Name</strong></span></span></p></td>
<td><p><span data-ttu-id="789d3-113">Имя открываемой пользователем функции.</span><span class="sxs-lookup"><span data-stu-id="789d3-113">The name of the user-defined function to open.</span></span> <span data-ttu-id="789d3-114">В поле <strong>имя функции</strong> в разделе <strong>аргументы макрокоманды</strong> области построителя макросов отображаются все пользовательские функции в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="789d3-114">The <strong>Function Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all user-defined functions in the current database.</span></span> <span data-ttu-id="789d3-115">Это обязательный аргумент. При запуске макроса, содержащего действие <strong>Function</strong> , в библиотечной базе данных Microsoft Access сначала ищет функцию с этим именем в библиотечной базе данных, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="789d3-115">This is a required argument.If you run a macro containing the <strong>Function</strong> action in a library database, Microsoft Access first looks for the function with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="789d3-116"><strong>Просмотр</strong></span><span class="sxs-lookup"><span data-stu-id="789d3-116"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="789d3-117">Представление, в котором откроется пользовательская функция.</span><span class="sxs-lookup"><span data-stu-id="789d3-117">The view in which the user-defined function will open.</span></span> <span data-ttu-id="789d3-118">В поле <strong>вид</strong> щелкните <strong>Таблица</strong>, <strong>Макет</strong>, <strong>Предварительный просмотр</strong>, <strong>Сводная таблица</strong>или <strong>Сводная диаграмма</strong> .</span><span class="sxs-lookup"><span data-stu-id="789d3-118">Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="789d3-119">Значение по умолчанию — <strong>Таблица</strong>.</span><span class="sxs-lookup"><span data-stu-id="789d3-119">The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="789d3-120"><strong>Режим данных</strong></span><span class="sxs-lookup"><span data-stu-id="789d3-120"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="789d3-121">Режим ввода данных для пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="789d3-121">The data entry mode for the user-defined function.</span></span> <span data-ttu-id="789d3-122">Это относится только к пользовательским функциям, открываемым в представлении таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="789d3-122">This applies only to user-defined functions opened in Datasheet view.</span></span> <span data-ttu-id="789d3-123">Нажмите кнопку <strong>Добавить</strong> (пользователь может добавлять новые записи, но не может просматривать или изменять существующие), <strong>изменять</strong> (пользователь может просматривать или редактировать существующие записи и добавлять новые записи) или <strong>только для чтения</strong> (пользователи могут только просматривать записи).</span><span class="sxs-lookup"><span data-stu-id="789d3-123">Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="789d3-124">Значение по умолчанию — <strong>Edit</strong>.</span><span class="sxs-lookup"><span data-stu-id="789d3-124">The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="789d3-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="789d3-125">Remarks</span></span>

<span data-ttu-id="789d3-126">Это действие аналогично двойному щелчку пользовательской функции в области навигации или щелчке правой кнопкой мыши функции в области навигации и выбора представления.</span><span class="sxs-lookup"><span data-stu-id="789d3-126">This action is similar to double-clicking a user-defined function in the Navigation Pane, or right-clicking the function in the Navigation Pane and selecting a view.</span></span>

<span data-ttu-id="789d3-127">Переключение в режим конструктора в то время, когда пользовательская функция открыта, удаляет значение аргумента **режим данных** для пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="789d3-127">Switching to Design view while the user-defined function is open removes the **Data Mode** argument setting for the user-defined function.</span></span> <span data-ttu-id="789d3-128">Этот параметр не действует, даже если пользователь возвращается в режим таблицы.</span><span class="sxs-lookup"><span data-stu-id="789d3-128">This setting is not in effect, even if the user returns to Datasheet view.</span></span>

> [!TIP]
> - <span data-ttu-id="789d3-129">Вы можете выбрать пользовательскую функцию в области навигации и перетащить ее в строку макрокоманды.</span><span class="sxs-lookup"><span data-stu-id="789d3-129">You can select a user-defined function in the Navigation Pane and drag it to a macro action row.</span></span> <span data-ttu-id="789d3-130">При этом автоматически создается действие **опенфунктион** , которое открывает пользовательскую функцию в представлении таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="789d3-130">This automatically creates an **OpenFunction** action that opens the user-defined function in Datasheet view.</span></span>
> - <span data-ttu-id="789d3-131">Если вы не хотите отображать системные сообщения, которые обычно отображаются при запуске пользовательской функции (указывая, что это пользовательская функция, и показывает, сколько записей будет затронуто), можно использовать действие **сетварнинг** , чтобы отключить отображение этих сообщений.</span><span class="sxs-lookup"><span data-stu-id="789d3-131">If you don't want to display the system messages that normally appear when a user-defined function is run (indicating it is a user-defined function and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="789d3-132">Чтобы запустить действие **опенфунктион** в модуле Visual Basic для приложений (VBA), используйте метод **опенфунктион** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="789d3-132">To run the **OpenFunction** action in a Visual Basic for Applications (VBA) module, use the **OpenFunction** method of the **DoCmd** object.</span></span>

