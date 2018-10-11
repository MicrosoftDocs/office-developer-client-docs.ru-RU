---
title: SetMenuItem Macro Action
TOCTitle: SetMenuItem Macro Action
ms:assetid: 503b3635-e721-1b99-3249-626e5dccdb8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193803(v=office.15)
ms:contentKeyID: 48544789
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm16614
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d6b5a91e9aa2f0c729a7fce221c859eb0cecc290
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480303"
---
# <a name="setmenuitem-macro-action"></a><span data-ttu-id="facb4-102">SetMenuItem Macro Action</span><span class="sxs-lookup"><span data-stu-id="facb4-102">SetMenuItem Macro Action</span></span>


<span data-ttu-id="facb4-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="facb4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="facb4-104">**Макрокоманды** можно использовать для задания состояния пунктов меню (включены или отключены, выбранные или не выбран) на пользовательских и глобальных меню на вкладке **Надстройки** .</span><span class="sxs-lookup"><span data-stu-id="facb4-104">You can use the **SetMenuItem** action to set the state of menu items (enabled or disabled, selected or unselected) on custom or global menus on the **Add-Ins** tab.</span></span>


> [!NOTE]
> <P><span data-ttu-id="facb4-105"><STRONG>Макрокоманды</STRONG> работает только с пользовательских и глобальных меню, созданные с помощью макросов меню.</span><span class="sxs-lookup"><span data-stu-id="facb4-105">The <STRONG>SetMenuItem</STRONG> action works only with custom and global menus created by using menu macros.</span></span> <span data-ttu-id="facb4-106"><STRONG>Макрокоманды</STRONG> включен в Microsoft Access только для совместимости с предыдущими версиями.</span><span class="sxs-lookup"><span data-stu-id="facb4-106">The <STRONG>SetMenuItem</STRONG> action is included in Microsoft Access only for compatibility with previous versions.</span></span> <span data-ttu-id="facb4-107">Он не работает с функциональных возможностях панели команд.</span><span class="sxs-lookup"><span data-stu-id="facb4-107">It does not work with the command bar functionality.</span></span> <span data-ttu-id="facb4-108">Тем не менее можно использовать свойства <STRONG>Enabled</STRONG> и <STRONG>состояния</STRONG> в Visual Basic для приложений (VBA) модуль отключение или включение и выберите или отмените выбор настройки элементов контекстных меню или настраиваемые или глобального меню.</span><span class="sxs-lookup"><span data-stu-id="facb4-108">However, you can use the <STRONG>Enabled</STRONG> and <STRONG>State</STRONG> properties in a Visual Basic for Applications (VBA) module to disable or enable and select or unselect items on shortcut menus or custom or global menus.</span></span></P>



## <a name="setting"></a><span data-ttu-id="facb4-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="facb4-109">Setting</span></span>

<span data-ttu-id="facb4-110">**Макрокоманды** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="facb4-110">The **SetMenuItem** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="facb4-111">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="facb4-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="facb4-112">Описание</span><span class="sxs-lookup"><span data-stu-id="facb4-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="facb4-113"><strong>Индекс меню</strong></span><span class="sxs-lookup"><span data-stu-id="facb4-113"><strong>Menu Index</strong></span></span></p></td>
<td><p><span data-ttu-id="facb4-114">Индекс меню, которое содержит команды, для которого требуется задать состояние.</span><span class="sxs-lookup"><span data-stu-id="facb4-114">The index of the menu that contains the command for which you want to set the state.</span></span> <span data-ttu-id="facb4-115">Введите значение типа integer, начиная с 0 для индекса нужного меню в меню настраиваемых или глобального.</span><span class="sxs-lookup"><span data-stu-id="facb4-115">Enter an integer value, starting from 0, for the index of the desired menu in the custom or global menu.</span></span> <span data-ttu-id="facb4-116">Введите значение индекса в поле <strong>Индекс меню</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="facb4-116">Enter the index value in the <strong>Menu Index</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="facb4-117">Индекс связан с позицией меню в макросе меню для настраиваемого или глобального меню (позиция <strong>в этом меню макрокоманды в макросе меню, начиная с 0</strong> ).</span><span class="sxs-lookup"><span data-stu-id="facb4-117">The index is relative to the menu's position in the menu macro for the custom or global menu (the position of this menu's <strong>AddMenu</strong> action in the menu macro, counting from 0).</span></span> <span data-ttu-id="facb4-118">Отображение меню возможно несколько различных условного выражения можно использовать в макросе меню скрытие и отображение нестандартных пунктов меню.</span><span class="sxs-lookup"><span data-stu-id="facb4-118">The menu's display may be somewhat different, because you can use conditional expressions in the menu macro to hide or display custom menu items.</span></span> <span data-ttu-id="facb4-119">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="facb4-119">This is a required argument.</span></span> <span data-ttu-id="facb4-120">Если выбрать меню с данным аргументом и оставить пустым аргументы <strong>Командной индексов</strong> и <strong>Команды</strong> можно включить или отключить само имя меню.</span><span class="sxs-lookup"><span data-stu-id="facb4-120">If you select a menu with this argument and leave the <strong>Command Index</strong> and <strong>Subcommand Index</strong> arguments blank, you can enable or disable the menu name itself.</span></span> <span data-ttu-id="facb4-121">Тем не менее, невозможно установите или снимите флажок имя меню (Access игнорирует параметры <strong>проверки</strong> и <strong>снимите флажок</strong> для аргумента <strong>флаг</strong> для имена меню).</span><span class="sxs-lookup"><span data-stu-id="facb4-121">You cannot, however, select or unselect a menu name (Access ignores the <strong>Check</strong> and <strong>Uncheck</strong> settings for the <strong>Flag</strong> argument for menu names).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="facb4-122"><strong>Индекс команды</strong></span><span class="sxs-lookup"><span data-stu-id="facb4-122"><strong>Command Index</strong></span></span></p></td>
<td><p><span data-ttu-id="facb4-123">Индекс команды, для которого требуется задать состояние.</span><span class="sxs-lookup"><span data-stu-id="facb4-123">The index of the command for which you want to set the state.</span></span> <span data-ttu-id="facb4-124">Введите значение типа integer, начиная с 0 для индекса нужную команду меню, указанному в аргументе <strong>Индекс меню</strong> .</span><span class="sxs-lookup"><span data-stu-id="facb4-124">Enter an integer value, starting from 0, for the index of the desired command in the menu selected by the <strong>Menu Index</strong> argument.</span></span> <span data-ttu-id="facb4-125">Индекс связан команды позицию в группе макросов, которая определяет выбранный меню для настраиваемого или глобального меню (позиция эта команда макроса в группе макросов, начиная с 0).</span><span class="sxs-lookup"><span data-stu-id="facb4-125">The index is relative to the command's position in the macro group that defines the selected menu for the custom or global menu (the position of this command's macro in the macro group, counting from 0).</span></span> <span data-ttu-id="facb4-126">Отображение меню может быть немного отличаются, так как можно использовать условного выражения в группы макросов, чтобы скрыть или отобразить настраиваемые команды меню.</span><span class="sxs-lookup"><span data-stu-id="facb4-126">The menu's display may be somewhat different, because you can use conditional expressions in the menu's macro group to hide or display custom menu commands.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="facb4-127"><strong>Индекс подкоманды</strong></span><span class="sxs-lookup"><span data-stu-id="facb4-127"><strong>Subcommand Index</strong></span></span></p></td>
<td><p><span data-ttu-id="facb4-128">Индекс команды, для которого требуется задать состояние.</span><span class="sxs-lookup"><span data-stu-id="facb4-128">The index of the subcommand for which you want to set the state.</span></span> <span data-ttu-id="facb4-129">Применяется только в том случае, если нужная команда имеет подменю.</span><span class="sxs-lookup"><span data-stu-id="facb4-129">This applies only if the desired command has a submenu.</span></span> <span data-ttu-id="facb4-130">Введите значение типа integer, начиная с 0 для индекса нужной подменю, указанному в аргументе <strong>Индекс команды</strong> .</span><span class="sxs-lookup"><span data-stu-id="facb4-130">Enter an integer value, starting from 0, for the index of the desired subcommand in the submenu selected by the <strong>Command Index</strong> argument.</span></span> <span data-ttu-id="facb4-131">Индекс связан положение команды в группе макросов, определяющий выбранного подменю для настраиваемого или глобального меню (позиция макроса этой команды в группе макросов, начиная с 0).</span><span class="sxs-lookup"><span data-stu-id="facb4-131">The index is relative to the subcommand's position in the macro group that defines the selected submenu for the custom or global menu (the position of this subcommand's macro in the macro group, counting from 0).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="facb4-132"><strong>Flag</strong></span><span class="sxs-lookup"><span data-stu-id="facb4-132"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="facb4-133">Состояние, которой требуется присвоить команда или команды для.</span><span class="sxs-lookup"><span data-stu-id="facb4-133">The state you want to set the command or subcommand to.</span></span> <span data-ttu-id="facb4-134">Щелкните <strong>серый цвет</strong> (отключить команды — эта кнопка недоступна), <strong>включен</strong> (для поддержки этих), <strong>Проверьте</strong> (установите с помощью команды, как правило, указывающее, был выбран или переключить), или <strong>Снять пометку</strong> (чтобы снять флажок).</span><span class="sxs-lookup"><span data-stu-id="facb4-134">Click <strong>Gray</strong> (to disable the command — it appears dimmed), <strong>Ungray</strong> (to enable it), <strong>Check</strong> (to place a check by the command — typically indicating it has been selected or toggled), or <strong>Uncheck</strong> (to remove the check).</span></span> <span data-ttu-id="facb4-135">Значение по умолчанию — <strong>включен</strong>.</span><span class="sxs-lookup"><span data-stu-id="facb4-135">The default is <strong>Ungray</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="facb4-136">Замечания</span><span class="sxs-lookup"><span data-stu-id="facb4-136">Remarks</span></span>

<span data-ttu-id="facb4-137">**Макрокоманды** работает только в пользовательских или глобального меню.</span><span class="sxs-lookup"><span data-stu-id="facb4-137">The **SetMenuItem** action works only on a custom or global menu.</span></span> <span data-ttu-id="facb4-138">Если активного окна не имеет настраиваемых или глобального меню, макрос, содержащий **макрокоманды** вызывает ошибку времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="facb4-138">If the active window does not have a custom or global menu, running a macro containing the **SetMenuItem** action causes a run-time error.</span></span>

<span data-ttu-id="facb4-139">Это действие можно использовать для установки состояния команды меню и команд, но не команд подменю следующих уровней.</span><span class="sxs-lookup"><span data-stu-id="facb4-139">You can use this action to set the state of menu commands and subcommands, but not subcommands of subcommands.</span></span>

<span data-ttu-id="facb4-140">Для запуска **макрокоманды** в Visual Basic для приложений (VBA) модуль, используйте метод **ЗадатьКомандуМеню** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="facb4-140">To run the **SetMenuItem** action in a Visual Basic for Applications (VBA) module, use the **SetMenuItem** method of the **DoCmd** object.</span></span>

