---
title: Макрокоманда AddMenu
TOCTitle: AddMenu macro action
ms:assetid: 4eb2afa0-ed1f-41b1-d27f-b3ce7a73d2bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193760(v=office.15)
ms:contentKeyID: 48544762
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm37891
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 119e824cae71d54bb398aa68f476a667f14a6888
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280275"
---
# <a name="addmenu-macro-action"></a><span data-ttu-id="2b0ad-102">Макрокоманда AddMenu</span><span class="sxs-lookup"><span data-stu-id="2b0ad-102">AddMenu macro action</span></span>


<span data-ttu-id="2b0ad-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b0ad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2b0ad-104">В этой статье описывается базовая операция **макроса AddMenu.**</span><span class="sxs-lookup"><span data-stu-id="2b0ad-104">This article describes the basic operation of the **AddMenu** macro action.</span></span>

<span data-ttu-id="2b0ad-105">Действие **AddMenu** можно использовать для создания:</span><span class="sxs-lookup"><span data-stu-id="2b0ad-105">You can use the **AddMenu** action to create:</span></span>

- <span data-ttu-id="2b0ad-106">Настраиваемые меню на **вкладке "Надстройки"** для определенной формы или отчета.</span><span class="sxs-lookup"><span data-stu-id="2b0ad-106">Custom menus on the **Add-Ins** tab for a particular form or report.</span></span>

- <span data-ttu-id="2b0ad-107">Настраиваемое меню ярлыка для формы, отчета или управления.</span><span class="sxs-lookup"><span data-stu-id="2b0ad-107">A custom shortcut menu for a form, report, or control.</span></span> <span data-ttu-id="2b0ad-108">Настраиваемые ярлыки заменяют встроенное меню для формы, отчета или управления.</span><span class="sxs-lookup"><span data-stu-id="2b0ad-108">The custom shortcut menu replaces the built-in shortcut menu for the form, report, or control.</span></span>

- <span data-ttu-id="2b0ad-109">Глобальное меню ярлыка.</span><span class="sxs-lookup"><span data-stu-id="2b0ad-109">A global shortcut menu.</span></span> <span data-ttu-id="2b0ad-110">Глобальное меню заменяет встроенное ярлыкное меню для полей в таблицах и таблицах данных запросов, формах и отчетах, за исключением случаев, когда добавлено настраиваемое меню для формы, отчета или управления.</span><span class="sxs-lookup"><span data-stu-id="2b0ad-110">The global shortcut menu replaces the built-in shortcut menu for fields in table and query datasheets, forms, and reports, except where you've added a custom shortcut menu for a form, report, or control.</span></span>

## <a name="setting"></a><span data-ttu-id="2b0ad-111">Setting</span><span class="sxs-lookup"><span data-stu-id="2b0ad-111">Setting</span></span>

<span data-ttu-id="2b0ad-112">Действие **AddMenu** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="2b0ad-112">The **AddMenu** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2b0ad-113">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="2b0ad-113">Action argument</span></span></p></th>
<th><p><span data-ttu-id="2b0ad-114">Описание</span><span class="sxs-lookup"><span data-stu-id="2b0ad-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b0ad-115"><strong>Имя меню</strong></span><span class="sxs-lookup"><span data-stu-id="2b0ad-115"><strong>Menu Name</strong></span></span></p></td>
<td><p><span data-ttu-id="2b0ad-116">Имя меню, например "Команды &quot; отчета" &quot; или &quot; "Инструменты". &quot;</span><span class="sxs-lookup"><span data-stu-id="2b0ad-116">The name of the menu, for example, &quot;Report Commands&quot; or &quot;Tools&quot;.</span></span> <span data-ttu-id="2b0ad-117">Чтобы создать клавишу доступа для выбора меню с помощью клавиатуры, введите амперанд () перед буквой, которая должна быть <strong>&amp;</strong> клавишей доступа.</span><span class="sxs-lookup"><span data-stu-id="2b0ad-117">To create an access key so that you can use the keyboard to choose the menu, type an ampersand (<strong>&amp;</strong>) before the letter you want to be the access key.</span></span> <span data-ttu-id="2b0ad-118">Эта буква будет подчеркивается в имени меню на вкладке <strong>"Надстройки".</strong></span><span class="sxs-lookup"><span data-stu-id="2b0ad-118">This letter will be underlined in the menu name on the <strong>Add-Ins</strong> tab.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b0ad-119"><strong>Имя макроса меню</strong></span><span class="sxs-lookup"><span data-stu-id="2b0ad-119"><strong>Menu Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="2b0ad-120">Имя группы макроса, которая содержит макрос для команд меню.</span><span class="sxs-lookup"><span data-stu-id="2b0ad-120">The name of the macro group that contains the macros for the menu's commands.</span></span> <span data-ttu-id="2b0ad-121">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="2b0ad-121">This is a required argument.</span></span></p>
<p><span data-ttu-id="2b0ad-122"><strong>ПРИМЕЧАНИЕ.</strong>При запуске макроса, содержащего действие <strong>AddMenu</strong> в базе данных библиотеки, Microsoft Office Access 2007 ищет группу макроса с этим именем только в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="2b0ad-122"><strong>NOTE</strong>: If you run a macro containing the <strong>AddMenu</strong> action in a library database, Microsoft Office Access 2007 looks for the macro group with this name in the current database only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b0ad-123"><strong>Текст в панели состояния</strong></span><span class="sxs-lookup"><span data-stu-id="2b0ad-123"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="2b0ad-124">Текст, который будет отображаться в панели состояния при выборе меню.</span><span class="sxs-lookup"><span data-stu-id="2b0ad-124">The text to display in the status bar when the menu is selected.</span></span> <span data-ttu-id="2b0ad-125">Этот аргумент игнорируется для ярлыков меню.</span><span class="sxs-lookup"><span data-stu-id="2b0ad-125">This argument is ignored for shortcut menus.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2b0ad-126">Заметки</span><span class="sxs-lookup"><span data-stu-id="2b0ad-126">Remarks</span></span>

<span data-ttu-id="2b0ad-127">Чтобы запустить **действие AddMenu** в модуле Visual Basic для приложений (VBA), используйте метод **AddMenu** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="2b0ad-127">To run the **AddMenu** action in a Visual Basic for Applications (VBA) module, use the **AddMenu** method of the **DoCmd** object.</span></span> <span data-ttu-id="2b0ad-128">Вы также можете настроить свойство **MenuBar** или **ShortcutMenuBar** в VBA, чтобы создать настраиваемые меню на вкладке "Надстройки" или прикрепить настраиваемые ярлыки к форме, отчету или управления. </span><span class="sxs-lookup"><span data-stu-id="2b0ad-128">You can also set the **MenuBar** or **ShortcutMenuBar** property in VBA to create a custom menu on the **Add-Ins** tab or to attach a custom shortcut menu to a form, report, or control.</span></span> <span data-ttu-id="2b0ad-129">Вы можете настроить свойство **ShortcutMenuBar** объекта **Application,** чтобы создать глобальное меню.</span><span class="sxs-lookup"><span data-stu-id="2b0ad-129">You can set the **ShortcutMenuBar** property of the **Application** object to create a global shortcut menu.</span></span>

