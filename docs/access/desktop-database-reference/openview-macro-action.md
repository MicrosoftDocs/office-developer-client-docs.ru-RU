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
# <a name="openview-macro-action"></a><span data-ttu-id="13adc-102">Макрокоманда OpenView</span><span class="sxs-lookup"><span data-stu-id="13adc-102">OpenView macro action</span></span>

<span data-ttu-id="13adc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="13adc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="13adc-104">В проекте Access можно использовать действие **опенвиев** для открытия представления в режиме таблицы, конструктора или предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="13adc-104">In an Access project, you can use the **OpenView** action to open a view in Datasheet view, Design view, or Print Preview.</span></span> <span data-ttu-id="13adc-105">Это действие запускает именованное представление при открытии в представлении таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="13adc-105">This action runs the named view when opened in Datasheet view.</span></span> <span data-ttu-id="13adc-106">Вы можете выбрать запись данных для представления и ограничить записи, отображаемые в представлении.</span><span class="sxs-lookup"><span data-stu-id="13adc-106">You can select data entry for the view and restrict the records that the view displays.</span></span>

> [!NOTE]
> <span data-ttu-id="13adc-107">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="13adc-107">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="13adc-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="13adc-108">Setting</span></span>

<span data-ttu-id="13adc-109">Макрокоманда **опенвиев** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="13adc-109">The **OpenView** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="13adc-110">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="13adc-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="13adc-111">Описание</span><span class="sxs-lookup"><span data-stu-id="13adc-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13adc-112"><strong>Имя представления</strong></span><span class="sxs-lookup"><span data-stu-id="13adc-112"><strong>View Name</strong></span></span></p></td>
<td><p><span data-ttu-id="13adc-113">Имя представления, которое требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="13adc-113">The name of the view to open.</span></span> <span data-ttu-id="13adc-114">В поле <strong>имя представления</strong> в разделе <strong>аргументы макрокоманды</strong> области построителя макросов отображаются все представления текущей базы данных.</span><span class="sxs-lookup"><span data-stu-id="13adc-114">The <strong>View Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all views in the current database.</span></span> <span data-ttu-id="13adc-115">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="13adc-115">This is a required argument.</span></span> <span data-ttu-id="13adc-116">При запуске макроса, содержащего действие <strong>опенвиев</strong> , в библиотечной базе данных Microsoft Access сначала ищет представление с этим именем в библиотечной базе данных, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="13adc-116">If you run a macro containing the <strong>OpenView</strong> action in a library database, Microsoft Access first looks for the view with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13adc-117"><strong>Просмотр</strong></span><span class="sxs-lookup"><span data-stu-id="13adc-117"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="13adc-118">Представление, в котором откроется представление.</span><span class="sxs-lookup"><span data-stu-id="13adc-118">The view in which the view will open.</span></span> <span data-ttu-id="13adc-119">В поле <strong>вид</strong> щелкните <strong>Таблица</strong>, <strong>Макет</strong>, <strong>Предварительный просмотр</strong>, <strong>Сводная таблица</strong>или <strong>Сводная диаграмма</strong> .</span><span class="sxs-lookup"><span data-stu-id="13adc-119">Click <strong>Datasheet</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box.</span></span> <span data-ttu-id="13adc-120">Значение по умолчанию — <strong>Таблица</strong>.</span><span class="sxs-lookup"><span data-stu-id="13adc-120">The default is <strong>Datasheet</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13adc-121"><strong>Режим данных</strong></span><span class="sxs-lookup"><span data-stu-id="13adc-121"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="13adc-122">Режим ввода данных для представления.</span><span class="sxs-lookup"><span data-stu-id="13adc-122">The data entry mode for the view.</span></span> <span data-ttu-id="13adc-123">Это относится только к представлениям, открываемым в режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="13adc-123">This applies only to views opened in Datasheet view.</span></span> <span data-ttu-id="13adc-124">Нажмите кнопку <strong>Добавить</strong> (пользователь может добавлять новые записи, но не может просматривать или изменять существующие), <strong>изменять</strong> (пользователь может просматривать или редактировать существующие записи и добавлять новые записи) или <strong>только для чтения</strong> (пользователи могут только просматривать записи).</span><span class="sxs-lookup"><span data-stu-id="13adc-124">Click <strong>Add</strong> (the user can add new records but can't view or edit existing records), <strong>Edit</strong> (the user can view or edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="13adc-125">Значение по умолчанию — <strong>Edit</strong>.</span><span class="sxs-lookup"><span data-stu-id="13adc-125">The default is <strong>Edit</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="13adc-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="13adc-126">Remarks</span></span>

<span data-ttu-id="13adc-127">Это действие аналогично двойному щелчку представления в области навигации или щелчком правой кнопкой мыши представления в области навигации и выбора нужной команды.</span><span class="sxs-lookup"><span data-stu-id="13adc-127">This action is similar to double-clicking a view in the Navigation Pane, or right-clicking the view in the Navigation Pane and then clicking the command you want.</span></span>

> [!TIP]
> - <span data-ttu-id="13adc-128">Вы можете перетащить представление из области навигации в строку макрокоманды.</span><span class="sxs-lookup"><span data-stu-id="13adc-128">You can drag a view from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="13adc-129">При этом автоматически создается действие **опенвиев** , которое открывает представление в режиме таблицы.</span><span class="sxs-lookup"><span data-stu-id="13adc-129">This automatically creates an **OpenView** action that opens the view in Datasheet view.</span></span>
> - <span data-ttu-id="13adc-130">Если вы не хотите отображать системные сообщения, которые обычно отображаются при запуске представления (указывает, что это представление и показывает, сколько записей будет затронуто), можно использовать действие **сетварнинг** , чтобы отключить отображение этих сообщений.</span><span class="sxs-lookup"><span data-stu-id="13adc-130">If you don't want to display the system messages that normally appear when a view is run (indicating it is a view and showing how many records will be affected), you can use the **SetWarning** action to suppress the display of these messages.</span></span>

<span data-ttu-id="13adc-131">Чтобы запустить действие **опенвиев** в модуле Visual Basic для приложений (VBA), используйте метод **опенвиев** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="13adc-131">To run the **OpenView** action in a Visual Basic for Applications (VBA) module, use the **OpenView** method of the **DoCmd** object.</span></span>

