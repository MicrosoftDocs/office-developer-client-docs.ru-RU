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
# <a name="openfunction-macro-action"></a><span data-ttu-id="3f463-102">Макрокоманда OpenFunction</span><span class="sxs-lookup"><span data-stu-id="3f463-102">OpenFunction macro action</span></span>

<span data-ttu-id="3f463-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f463-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3f463-104">В проекте Access вы можете использовать действие **OpenFunction** для открытия функции, определяемой пользователем, в представлении Datasheet, представлении дизайна функции inline, SQL представлении редактора текста (для функции масштабирования или таблицы, определенной пользователем) или предварительного просмотра печати.</span><span class="sxs-lookup"><span data-stu-id="3f463-104">In an Access project, you can use the **OpenFunction** action to open a user-defined function in Datasheet view, inline function Design view, SQL Text Editor view (for a scalar or table user-defined function), or Print Preview.</span></span> <span data-ttu-id="3f463-105">Это действие выполняет функцию, определяемую пользователем, при открываемом в представлении Datasheet.</span><span class="sxs-lookup"><span data-stu-id="3f463-105">This action runs the user-defined function when opened in Datasheet view.</span></span> <span data-ttu-id="3f463-106">Вы также можете выбрать режим ввода данных для определенной пользователем функции и ограничить записи, отображаемые функцией, определяемой пользователем.</span><span class="sxs-lookup"><span data-stu-id="3f463-106">You can also select the data entry mode for the user-defined function and restrict the records that the user-defined function displays.</span></span>

> [!NOTE]
> <span data-ttu-id="3f463-107">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="3f463-107">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="3f463-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="3f463-108">Setting</span></span>

<span data-ttu-id="3f463-109">Действие **OpenFunction** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="3f463-109">The **OpenFunction** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3f463-110">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="3f463-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="3f463-111">Описание</span><span class="sxs-lookup"><span data-stu-id="3f463-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f463-112"><strong>Имя функции</strong></span><span class="sxs-lookup"><span data-stu-id="3f463-112"><strong>Function Name</strong></span></span></p></td>
<td><p><span data-ttu-id="3f463-113">Имя открываемой функции, определяемой пользователем.</span><span class="sxs-lookup"><span data-stu-id="3f463-113">The name of the user-defined function to open.</span></span> <span data-ttu-id="3f463-114">Поле <strong>Имя функции</strong> в разделе <strong>Аргументы</strong> действий в области Macro Builder отображает все функции, определенные пользователем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="3f463-114">The <strong>Function Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all user-defined functions in the current database.</span></span> <span data-ttu-id="3f463-115">Это необходимый аргумент. Если вы запустите макрос, содержащий действие <strong>Function</strong> в базе данных библиотеки, Microsoft Access сначала ищет функцию с этим именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="3f463-115">This is a required argument.If you run a macro containing the <strong>Function</strong> action in a library database, Microsoft Access first looks for the function with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f463-116"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="3f463-116"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="3f463-117">Представление, в котором откроется функция, определяемая пользователем.</span><span class="sxs-lookup"><span data-stu-id="3f463-117">The view in which the user-defined function will open.</span></span> <span data-ttu-id="3f463-118">Щелкните <strong>таблицу</strong>данных, <strong>дизайн,</strong> <strong>предварительный</strong>просмотр печати, <strong>pivotTable</strong>или сводная диаграмма в <strong>поле Просмотр.</strong> <strong></strong></span><span class="sxs-lookup"><span data-stu-id="3f463-118">Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="3f463-119">По умолчанию — <strong>таблица данных.</strong></span><span class="sxs-lookup"><span data-stu-id="3f463-119">The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f463-120"><strong>Режим данных</strong></span><span class="sxs-lookup"><span data-stu-id="3f463-120"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="3f463-121">Режим ввода данных для определенной пользователем функции.</span><span class="sxs-lookup"><span data-stu-id="3f463-121">The data entry mode for the user-defined function.</span></span> <span data-ttu-id="3f463-122">Это касается только определенных пользователем функций, открытых в представлении Datasheet.</span><span class="sxs-lookup"><span data-stu-id="3f463-122">This applies only to user-defined functions opened in Datasheet view.</span></span> <span data-ttu-id="3f463-123">Щелкните Добавить (пользователь может добавлять новые записи, но не может просматривать или изменять существующие записи), изменить (пользователь может просматривать или изменять существующие записи и добавлять новые записи) или Только для чтения <strong>(пользователь</strong> может просматривать только записи). <strong></strong> <strong></strong></span><span class="sxs-lookup"><span data-stu-id="3f463-123">Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="3f463-124">По умолчанию <strong>изменить</strong>.</span><span class="sxs-lookup"><span data-stu-id="3f463-124">The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3f463-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="3f463-125">Remarks</span></span>

<span data-ttu-id="3f463-126">Это действие аналогично двойному нажатию функции, определенной пользователем в области навигации, или правой щелкнув функцию в области навигации и выбрав представление.</span><span class="sxs-lookup"><span data-stu-id="3f463-126">This action is similar to double-clicking a user-defined function in the Navigation Pane, or right-clicking the function in the Navigation Pane and selecting a view.</span></span>

<span data-ttu-id="3f463-127">Переход на представление "Дизайн" при открытой функции, определяемой пользователем, удаляет параметр аргумента **"Режим** данных" для определенной пользователем функции.</span><span class="sxs-lookup"><span data-stu-id="3f463-127">Switching to Design view while the user-defined function is open removes the **Data Mode** argument setting for the user-defined function.</span></span> <span data-ttu-id="3f463-128">Этот параметр не действует, даже если пользователь возвращается в представление Таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="3f463-128">This setting is not in effect, even if the user returns to Datasheet view.</span></span>

> [!TIP]
> - <span data-ttu-id="3f463-129">В области навигации можно выбрать функцию, определяемую пользователем, и перетаскивать ее в строку действия макроса.</span><span class="sxs-lookup"><span data-stu-id="3f463-129">You can select a user-defined function in the Navigation Pane and drag it to a macro action row.</span></span> <span data-ttu-id="3f463-130">Это автоматически создает действие **OpenFunction,** которое открывает функцию, определяемую пользователем, в представлении Datasheet.</span><span class="sxs-lookup"><span data-stu-id="3f463-130">This automatically creates an **OpenFunction** action that opens the user-defined function in Datasheet view.</span></span>
> - <span data-ttu-id="3f463-131">Если вы не хотите отображать системные сообщения, которые обычно отображаются при запуске определенной пользователем функции (указывающее, что это функция, определяемая пользователем, и показывая, сколько записей будет затронуто), вы можете использовать действие **SetWarning** для подавления отображения этих сообщений.</span><span class="sxs-lookup"><span data-stu-id="3f463-131">If you don't want to display the system messages that normally appear when a user-defined function is run (indicating it is a user-defined function and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="3f463-132">Чтобы выполнить **действие OpenFunction** в модуле Visual Basic для приложений (VBA), используйте метод **OpenFunction** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="3f463-132">To run the **OpenFunction** action in a Visual Basic for Applications (VBA) module, use the **OpenFunction** method of the **DoCmd** object.</span></span>

