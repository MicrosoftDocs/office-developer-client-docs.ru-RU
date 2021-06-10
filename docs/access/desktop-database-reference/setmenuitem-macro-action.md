---
title: Макрокоманда SetMenuItem
TOCTitle: SetMenuItem macro action
ms:assetid: 503b3635-e721-1b99-3249-626e5dccdb8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193803(v=office.15)
ms:contentKeyID: 48544789
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm16614
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fe61a3368813ba3420920909f818beee2029d993
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308682"
---
# <a name="setmenuitem-macro-action"></a><span data-ttu-id="fb459-102">Макрокоманда SetMenuItem</span><span class="sxs-lookup"><span data-stu-id="fb459-102">SetMenuItem macro action</span></span>

<span data-ttu-id="fb459-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fb459-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fb459-104">Действие **SetMenuItem** можно использовать для настройки состояния элементов меню (включено или отключено, выбрано или невыбрано) в настраиваемом или глобальном меню на вкладке Надстройки. </span><span class="sxs-lookup"><span data-stu-id="fb459-104">You can use the **SetMenuItem** action to set the state of menu items (enabled or disabled, selected or unselected) on custom or global menus on the **Add-Ins** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="fb459-105">Действие **SetMenuItem** работает только с пользовательскими и глобальными меню, созданными с помощью макрос меню.</span><span class="sxs-lookup"><span data-stu-id="fb459-105">The **SetMenuItem** action works only with custom and global menus created by using menu macros.</span></span> <span data-ttu-id="fb459-106">Действие **SetMenuItem** включено в Microsoft Access только для совместимости с предыдущими версиями.</span><span class="sxs-lookup"><span data-stu-id="fb459-106">The **SetMenuItem** action is included in Microsoft Access only for compatibility with previous versions.</span></span> <span data-ttu-id="fb459-107">Он не работает с функцией панели команд.</span><span class="sxs-lookup"><span data-stu-id="fb459-107">It does not work with the command bar functionality.</span></span> <span data-ttu-id="fb459-108">Однако в модуле  Visual Basic для приложений  (VBA) можно использовать свойства включено и состояние для отключения или включения и выбора элементов в меню ярлыка или настраиваемом или глобальном меню.</span><span class="sxs-lookup"><span data-stu-id="fb459-108">However, you can use the **Enabled** and **State** properties in a Visual Basic for Applications (VBA) module to disable or enable and select or unselect items on shortcut menus or custom or global menus.</span></span>

## <a name="setting"></a><span data-ttu-id="fb459-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="fb459-109">Setting</span></span>

<span data-ttu-id="fb459-110">Действие **SetMenuItem имеет** следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="fb459-110">The **SetMenuItem** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fb459-111">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="fb459-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="fb459-112">Описание</span><span class="sxs-lookup"><span data-stu-id="fb459-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb459-113"><strong>Индекс меню</strong></span><span class="sxs-lookup"><span data-stu-id="fb459-113"><strong>Menu Index</strong></span></span></p></td>
<td><p><span data-ttu-id="fb459-114">Индекс меню, в котором содержится команда, для которой необходимо установить состояние.</span><span class="sxs-lookup"><span data-stu-id="fb459-114">The index of the menu that contains the command for which you want to set the state.</span></span> <span data-ttu-id="fb459-115">Введите значение integer, начиная с 0, для индекса нужного меню в настраиваемом или глобальном меню.</span><span class="sxs-lookup"><span data-stu-id="fb459-115">Enter an integer value, starting from 0, for the index of the desired menu in the custom or global menu.</span></span> <span data-ttu-id="fb459-116">Введите значение индекса в <strong>поле Индекс меню</strong> в разделе <strong>Аргументы</strong> действий в области Macro Builder.</span><span class="sxs-lookup"><span data-stu-id="fb459-116">Enter the index value in the <strong>Menu Index</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="fb459-117">Индекс относительно позиции меню в макрос меню для настраиваемого или глобального меню (положение действия <strong>AddMenu</strong> этого меню в макрос меню, считая от 0).</span><span class="sxs-lookup"><span data-stu-id="fb459-117">The index is relative to the menu's position in the menu macro for the custom or global menu (the position of this menu's <strong>AddMenu</strong> action in the menu macro, counting from 0).</span></span> <span data-ttu-id="fb459-118">Отображение меню может быть несколько иным, так как можно использовать условные выражения в макрос меню, чтобы скрыть или отобразить настраиваемые элементы меню.</span><span class="sxs-lookup"><span data-stu-id="fb459-118">The menu's display may be somewhat different, because you can use conditional expressions in the menu macro to hide or display custom menu items.</span></span> <span data-ttu-id="fb459-119">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="fb459-119">This is a required argument.</span></span> <span data-ttu-id="fb459-120">Если выбрать меню с этим аргументом и <strong></strong> оставить аргументы <strong>Индекс</strong> команд и Подкоманда пустыми, можно включить или отключить само имя меню.</span><span class="sxs-lookup"><span data-stu-id="fb459-120">If you select a menu with this argument and leave the <strong>Command Index</strong> and <strong>Subcommand Index</strong> arguments blank, you can enable or disable the menu name itself.</span></span> <span data-ttu-id="fb459-121">Однако нельзя выбрать или отобрать имя меню (Access игнорирует параметры <strong>Check</strong> и <strong>Uncheck</strong> для аргумента <strong>Флаг</strong> для имен меню).</span><span class="sxs-lookup"><span data-stu-id="fb459-121">You cannot, however, select or unselect a menu name (Access ignores the <strong>Check</strong> and <strong>Uncheck</strong> settings for the <strong>Flag</strong> argument for menu names).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb459-122"><strong>Индекс команд</strong></span><span class="sxs-lookup"><span data-stu-id="fb459-122"><strong>Command Index</strong></span></span></p></td>
<td><p><span data-ttu-id="fb459-123">Индекс команды, для которой нужно установить состояние.</span><span class="sxs-lookup"><span data-stu-id="fb459-123">The index of the command for which you want to set the state.</span></span> <span data-ttu-id="fb459-124">Введите значение integer, начиная с 0, для индекса нужной команды в меню, выбранном <strong>аргументом Индекс меню.</strong></span><span class="sxs-lookup"><span data-stu-id="fb459-124">Enter an integer value, starting from 0, for the index of the desired command in the menu selected by the <strong>Menu Index</strong> argument.</span></span> <span data-ttu-id="fb459-125">Индекс относительно позиции команды в макрогруппе, определяемой выбранным меню для настраиваемого или глобального меню (положение макроса этой команды в макрогруппе, считая от 0).</span><span class="sxs-lookup"><span data-stu-id="fb459-125">The index is relative to the command's position in the macro group that defines the selected menu for the custom or global menu (the position of this command's macro in the macro group, counting from 0).</span></span> <span data-ttu-id="fb459-126">Отображение меню может быть несколько иным, так как можно использовать условные выражения в макрогруппе меню, чтобы скрыть или отобразить настраиваемые команды меню.</span><span class="sxs-lookup"><span data-stu-id="fb459-126">The menu's display may be somewhat different, because you can use conditional expressions in the menu's macro group to hide or display custom menu commands.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb459-127"><strong>Индекс subcommand</strong></span><span class="sxs-lookup"><span data-stu-id="fb459-127"><strong>Subcommand Index</strong></span></span></p></td>
<td><p><span data-ttu-id="fb459-128">Индекс подкомитета, для которого необходимо установить состояние.</span><span class="sxs-lookup"><span data-stu-id="fb459-128">The index of the subcommand for which you want to set the state.</span></span> <span data-ttu-id="fb459-129">Это применяется только в том случае, если в нужной команде есть подмену.</span><span class="sxs-lookup"><span data-stu-id="fb459-129">This applies only if the desired command has a submenu.</span></span> <span data-ttu-id="fb459-130">Введите значение integer, начиная с 0, для индекса нужного подкомитета в submenu, выбранном аргументом <strong>Command Index.</strong></span><span class="sxs-lookup"><span data-stu-id="fb459-130">Enter an integer value, starting from 0, for the index of the desired subcommand in the submenu selected by the <strong>Command Index</strong> argument.</span></span> <span data-ttu-id="fb459-131">Индекс относительно позиции подкомитета в макрогруппе, определяемой выбранным подмену для настраиваемого или глобального меню (позиция макроса этого подкомитета в макрогруппе, считая от 0).</span><span class="sxs-lookup"><span data-stu-id="fb459-131">The index is relative to the subcommand's position in the macro group that defines the selected submenu for the custom or global menu (the position of this subcommand's macro in the macro group, counting from 0).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb459-132"><strong>Флаг</strong></span><span class="sxs-lookup"><span data-stu-id="fb459-132"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="fb459-133">Состояние, в который необходимо настроить команду или подкомитет.</span><span class="sxs-lookup"><span data-stu-id="fb459-133">The state you want to set the command or subcommand to.</span></span> <span data-ttu-id="fb459-134">Щелкните <strong>Серый</strong> цвет (чтобы отключить команду — она отображается потусклой), <strong>Ungray</strong> (чтобы включить <strong>ее),</strong> Проверьте (чтобы сделать проверку командой — как правило, указывающее, что она выбрана или переключена) или <strong>Uncheck</strong> (чтобы удалить проверку).</span><span class="sxs-lookup"><span data-stu-id="fb459-134">Click <strong>Gray</strong> (to disable the command — it appears dimmed), <strong>Ungray</strong> (to enable it), <strong>Check</strong> (to place a check by the command — typically indicating it has been selected or toggled), or <strong>Uncheck</strong> (to remove the check).</span></span> <span data-ttu-id="fb459-135">По умолчанию является <strong>неграйным</strong>.</span><span class="sxs-lookup"><span data-stu-id="fb459-135">The default is <strong>Ungray</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fb459-136">Примечания</span><span class="sxs-lookup"><span data-stu-id="fb459-136">Remarks</span></span>

<span data-ttu-id="fb459-137">Действие **SetMenuItem** работает только в настраиваемом или глобальном меню.</span><span class="sxs-lookup"><span data-stu-id="fb459-137">The **SetMenuItem** action works only on a custom or global menu.</span></span> <span data-ttu-id="fb459-138">Если в активном окне нет настраиваемого или глобального меню, запуск макроса, содержащего действие **SetMenuItem,** вызывает ошибку во времени запуска.</span><span class="sxs-lookup"><span data-stu-id="fb459-138">If the active window does not have a custom or global menu, running a macro containing the **SetMenuItem** action causes a run-time error.</span></span>

<span data-ttu-id="fb459-139">Это действие можно использовать для настройки состояния команд меню и подкоммандатов, но не подкомкомитетов подкомитетов.</span><span class="sxs-lookup"><span data-stu-id="fb459-139">You can use this action to set the state of menu commands and subcommands, but not subcommands of subcommands.</span></span>

<span data-ttu-id="fb459-140">Чтобы выполнить **действие SetMenuItem** в модуле Visual Basic для приложений (VBA), используйте метод **SetMenuItem** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="fb459-140">To run the **SetMenuItem** action in a Visual Basic for Applications (VBA) module, use the **SetMenuItem** method of the **DoCmd** object.</span></span>

