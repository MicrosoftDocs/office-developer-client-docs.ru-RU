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
# <a name="openfunction-macro-action"></a><span data-ttu-id="6f924-102">Макрокоманда OpenFunction</span><span class="sxs-lookup"><span data-stu-id="6f924-102">OpenFunction macro action</span></span>

<span data-ttu-id="6f924-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f924-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6f924-104">В проекте Access можно использовать действие **OpenFunction** для открытия пользовательской функции в представлении таблицы, в представлении конструктора функций, в представлении конструктора функций SQL текстового редактора (для скалярной или табулярной пользовательской функции) или предварительного просмотра печати.</span><span class="sxs-lookup"><span data-stu-id="6f924-104">In an Access project, you can use the **OpenFunction** action to open a user-defined function in Datasheet view, inline function Design view, SQL Text Editor view (for a scalar or table user-defined function), or Print Preview.</span></span> <span data-ttu-id="6f924-105">Это действие запускает пользовательской функции при запуске в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="6f924-105">This action runs the user-defined function when opened in Datasheet view.</span></span> <span data-ttu-id="6f924-106">Можно также выбрать режим ввода данных для пользовательской функции и ограничить отображаемую пользователем запись.</span><span class="sxs-lookup"><span data-stu-id="6f924-106">You can also select the data entry mode for the user-defined function and restrict the records that the user-defined function displays.</span></span>

> [!NOTE]
> <span data-ttu-id="6f924-107">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="6f924-107">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="6f924-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="6f924-108">Setting</span></span>

<span data-ttu-id="6f924-109">Действие **OpenFunction** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="6f924-109">The **OpenFunction** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6f924-110">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="6f924-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="6f924-111">Описание</span><span class="sxs-lookup"><span data-stu-id="6f924-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f924-112"><strong>Имя функции</strong></span><span class="sxs-lookup"><span data-stu-id="6f924-112"><strong>Function Name</strong></span></span></p></td>
<td><p><span data-ttu-id="6f924-113">Имя пользовательской функции, которая требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="6f924-113">The name of the user-defined function to open.</span></span> <span data-ttu-id="6f924-114">В <strong>поле "Имя функции"</strong> в разделе <strong>"Аргументы</strong> действий" области построитель макроса показаны все пользовательские функции в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="6f924-114">The <strong>Function Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all user-defined functions in the current database.</span></span> <span data-ttu-id="6f924-115">Это необходимый аргумент. При запуске макроса, содержащего действие <strong>Функции</strong> в базе данных библиотеки, Microsoft Access сначала ищет функцию с этим именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="6f924-115">This is a required argument.If you run a macro containing the <strong>Function</strong> action in a library database, Microsoft Access first looks for the function with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f924-116"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="6f924-116"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="6f924-117">Представление, в котором откроется определяемая пользователем функция.</span><span class="sxs-lookup"><span data-stu-id="6f924-117">The view in which the user-defined function will open.</span></span> <span data-ttu-id="6f924-118">Щелкните <strong></strong> <strong>"Таблица</strong> <strong>данных", "Конструктор",</strong>"Предварительный <strong>просмотр",</strong> <strong>"Сводная диаграмма</strong> в поле <strong>"Вид".</strong></span><span class="sxs-lookup"><span data-stu-id="6f924-118">Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="6f924-119">Значение по умолчанию <strong>— Таблица.</strong></span><span class="sxs-lookup"><span data-stu-id="6f924-119">The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f924-120"><strong>Режим данных</strong></span><span class="sxs-lookup"><span data-stu-id="6f924-120"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="6f924-121">Режим ввода данных для пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="6f924-121">The data entry mode for the user-defined function.</span></span> <span data-ttu-id="6f924-122">Это относится только к пользовательским функциям, открытым в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="6f924-122">This applies only to user-defined functions opened in Datasheet view.</span></span> <span data-ttu-id="6f924-123">Нажмите <strong></strong> кнопку "Добавить" (пользователь может добавлять новые записи, но не может просматривать или редактировать существующие <strong>записи),</strong> изменять (пользователь может просматривать или редактировать существующие записи и добавлять новые записи) или только для чтения <strong>(пользователь</strong> может просматривать только записи).</span><span class="sxs-lookup"><span data-stu-id="6f924-123">Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="6f924-124">Значение по умолчанию <strong>— Edit</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f924-124">The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6f924-125">Заметки</span><span class="sxs-lookup"><span data-stu-id="6f924-125">Remarks</span></span>

<span data-ttu-id="6f924-126">Это действие аналогично двойному щелчку пользовательской функции в области навигации или щелчку правой кнопкой мыши функции в области навигации и выбору представления.</span><span class="sxs-lookup"><span data-stu-id="6f924-126">This action is similar to double-clicking a user-defined function in the Navigation Pane, or right-clicking the function in the Navigation Pane and selecting a view.</span></span>

<span data-ttu-id="6f924-127">При переключении в режим конструктора во время открытия  пользовательской функции удаляется параметр аргумента режима данных для пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="6f924-127">Switching to Design view while the user-defined function is open removes the **Data Mode** argument setting for the user-defined function.</span></span> <span data-ttu-id="6f924-128">Этот параметр не действует, даже если пользователь возвращается в представление таблицы.</span><span class="sxs-lookup"><span data-stu-id="6f924-128">This setting is not in effect, even if the user returns to Datasheet view.</span></span>

> [!TIP]
> - <span data-ttu-id="6f924-129">Вы можете выбрать определяемую пользователем функцию в области навигации и перетащить ее в строку макроса.</span><span class="sxs-lookup"><span data-stu-id="6f924-129">You can select a user-defined function in the Navigation Pane and drag it to a macro action row.</span></span> <span data-ttu-id="6f924-130">При этом автоматически создается действие **OpenFunction,** которое открывает пользовательская функция в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="6f924-130">This automatically creates an **OpenFunction** action that opens the user-defined function in Datasheet view.</span></span>
> - <span data-ttu-id="6f924-131">Если вы не хотите отображать системные сообщения, которые обычно отображаются при запуске пользовательской функции (указывая, что это пользовательская функция и показывает, сколько записей будет затронуто), можно использовать действие **SetWarning,** чтобы запретить отображение этих сообщений.</span><span class="sxs-lookup"><span data-stu-id="6f924-131">If you don't want to display the system messages that normally appear when a user-defined function is run (indicating it is a user-defined function and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="6f924-132">Чтобы запустить действие **OpenFunction** в модуле Visual Basic для приложений VBA, используйте метод **OpenFunction** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="6f924-132">To run the **OpenFunction** action in a Visual Basic for Applications (VBA) module, use the **OpenFunction** method of the **DoCmd** object.</span></span>

