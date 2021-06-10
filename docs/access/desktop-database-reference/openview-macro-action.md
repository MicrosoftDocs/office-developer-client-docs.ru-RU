---
title: Макрокоманда OpenView
TOCTitle: OpenView macro action
ms:assetid: 4d3b7e6d-4b81-4fbe-7222-24d745350321
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193569(v=office.15)
ms:contentKeyID: 48544726
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50135
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 88bebab46cd6b76fb101c86c4fe33c5ab86a3e70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288303"
---
# <a name="openview-macro-action"></a><span data-ttu-id="8114d-102">Макрокоманда OpenView</span><span class="sxs-lookup"><span data-stu-id="8114d-102">OpenView macro action</span></span>

<span data-ttu-id="8114d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8114d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8114d-104">В проекте Access можно использовать действие **OpenView** для открытия представления в представлении таблицы данных, представлении дизайна или предварительном просмотре печати.</span><span class="sxs-lookup"><span data-stu-id="8114d-104">In an Access project, you can use the **OpenView** action to open a view in Datasheet view, Design view, or Print Preview.</span></span> <span data-ttu-id="8114d-105">Это действие выполняет именуемую точку представления при открываемом представлении Таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="8114d-105">This action runs the named view when opened in Datasheet view.</span></span> <span data-ttu-id="8114d-106">Вы можете выбрать запись данных для представления и ограничить записи, отображаемые в представлении.</span><span class="sxs-lookup"><span data-stu-id="8114d-106">You can select data entry for the view and restrict the records that the view displays.</span></span>

> [!NOTE]
> <span data-ttu-id="8114d-107">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="8114d-107">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="8114d-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="8114d-108">Setting</span></span>

<span data-ttu-id="8114d-109">Действие **OpenView** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="8114d-109">The **OpenView** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8114d-110">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="8114d-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="8114d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="8114d-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8114d-112"><strong>Просмотр имени</strong></span><span class="sxs-lookup"><span data-stu-id="8114d-112"><strong>View Name</strong></span></span></p></td>
<td><p><span data-ttu-id="8114d-113">Имя открываемого представления.</span><span class="sxs-lookup"><span data-stu-id="8114d-113">The name of the view to open.</span></span> <span data-ttu-id="8114d-114">Поле <strong>Имя представления</strong> в разделе <strong>Аргументы</strong> действий в области Macro Builder отображает все представления в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="8114d-114">The <strong>View Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all views in the current database.</span></span> <span data-ttu-id="8114d-115">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="8114d-115">This is a required argument.</span></span> <span data-ttu-id="8114d-116">Если вы запустите макрос, содержащий действие <strong>OpenView</strong> в базе данных библиотеки, Microsoft Access сначала ищет представление с этим именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="8114d-116">If you run a macro containing the <strong>OpenView</strong> action in a library database, Microsoft Access first looks for the view with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8114d-117"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="8114d-117"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="8114d-118">Представление, в котором откроется представление.</span><span class="sxs-lookup"><span data-stu-id="8114d-118">The view in which the view will open.</span></span> <span data-ttu-id="8114d-119">Щелкните <strong>таблицу</strong>данных, <strong>дизайн,</strong> <strong>предварительный</strong>просмотр печати, <strong>pivotTable</strong>или сводная диаграмма в <strong>поле Просмотр.</strong> <strong></strong></span><span class="sxs-lookup"><span data-stu-id="8114d-119">Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="8114d-120">По умолчанию — <strong>таблица данных.</strong></span><span class="sxs-lookup"><span data-stu-id="8114d-120">The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8114d-121"><strong>Режим данных</strong></span><span class="sxs-lookup"><span data-stu-id="8114d-121"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="8114d-122">Режим ввода данных для представления.</span><span class="sxs-lookup"><span data-stu-id="8114d-122">The data entry mode for the view.</span></span> <span data-ttu-id="8114d-123">Это касается только представлений, открытых в представлении Datasheet.</span><span class="sxs-lookup"><span data-stu-id="8114d-123">This applies only to views opened in Datasheet view.</span></span> <span data-ttu-id="8114d-124">Щелкните Добавить (пользователь может добавлять новые записи, но не может просматривать или изменять существующие записи), изменить (пользователь может просматривать или изменять существующие записи и добавлять новые записи) или Только для чтения <strong>(пользователь</strong> может просматривать только записи). <strong></strong> <strong></strong></span><span class="sxs-lookup"><span data-stu-id="8114d-124">Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="8114d-125">По умолчанию <strong>изменить</strong>.</span><span class="sxs-lookup"><span data-stu-id="8114d-125">The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8114d-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="8114d-126">Remarks</span></span>

<span data-ttu-id="8114d-127">Это действие аналогично дважды щелкнув представление в области навигации или щелкнув правой кнопкой мыши представление в области навигации, а затем щелкнув команду, которая вам нужна.</span><span class="sxs-lookup"><span data-stu-id="8114d-127">This action is similar to double-clicking a view in the Navigation Pane, or right-clicking the view in the Navigation Pane and then clicking the command you want.</span></span>

> [!TIP]
> - <span data-ttu-id="8114d-128">Можно перетаскивать представление из области навигации в строку действий макроса.</span><span class="sxs-lookup"><span data-stu-id="8114d-128">You can drag a view from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="8114d-129">Это автоматически создает действие **OpenView,** которое открывает представление в представлении Datasheet.</span><span class="sxs-lookup"><span data-stu-id="8114d-129">This automatically creates an **OpenView** action that opens the view in Datasheet view.</span></span>
> - <span data-ttu-id="8114d-130">Если вы не хотите отображать системные сообщения, которые обычно отображаются при запуске представления (указывающее представление и показывая, сколько записей будет затронуто), вы можете использовать действие **SetWarning** для подавления отображения этих сообщений.</span><span class="sxs-lookup"><span data-stu-id="8114d-130">If you don't want to display the system messages that normally appear when a view is run (indicating it is a view and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="8114d-131">Чтобы выполнить **действие OpenView** в Visual Basic для приложений (VBA), используйте метод **OpenView** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="8114d-131">To run the **OpenView** action in a Visual Basic for Applications (VBA) module, use the **OpenView** method of the **DoCmd** object.</span></span>

