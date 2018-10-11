---
title: AddMenu Macro Action
TOCTitle: AddMenu Macro Action
ms:assetid: 4eb2afa0-ed1f-41b1-d27f-b3ce7a73d2bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193760(v=office.15)
ms:contentKeyID: 48544762
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm37891
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 984b10638ab7f01aeb4dc9656bc70aa1e44d56a7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482075"
---
# <a name="addmenu-macro-action"></a><span data-ttu-id="350f9-102">AddMenu Macro Action</span><span class="sxs-lookup"><span data-stu-id="350f9-102">AddMenu Macro Action</span></span>


<span data-ttu-id="350f9-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="350f9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="350f9-104">В этой статье описываются основные операции **макрокоманды макрос** .</span><span class="sxs-lookup"><span data-stu-id="350f9-104">This article describes the basic operation of the **AddMenu** macro action.</span></span>

<span data-ttu-id="350f9-105">**Макрокоманды** можно использовать для создания:</span><span class="sxs-lookup"><span data-stu-id="350f9-105">You can use the **AddMenu** action to create:</span></span>

- <span data-ttu-id="350f9-106">Настраиваемые меню на вкладке **Надстройки** для определенного форму или отчет.</span><span class="sxs-lookup"><span data-stu-id="350f9-106">Custom menus on the **Add-Ins** tab for a particular form or report.</span></span>

- <span data-ttu-id="350f9-107">Настраиваемые контекстное меню для формы, отчета или элемента управления.</span><span class="sxs-lookup"><span data-stu-id="350f9-107">A custom shortcut menu for a form, report, or control.</span></span> <span data-ttu-id="350f9-108">Настраиваемого контекстного меню заменяет встроенное контекстное меню для формы, отчета или элемента управления.</span><span class="sxs-lookup"><span data-stu-id="350f9-108">The custom shortcut menu replaces the built-in shortcut menu for the form, report, or control.</span></span>

- <span data-ttu-id="350f9-109">Глобальное контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="350f9-109">A global shortcut menu.</span></span> <span data-ttu-id="350f9-110">Глобальное контекстное меню заменяет встроенное контекстное меню для полей в таблице и технические описания запросов, форм и отчетов, за исключением которые пользователь добавил настраиваемого контекстного меню для формы, отчета или элемента управления.</span><span class="sxs-lookup"><span data-stu-id="350f9-110">The global shortcut menu replaces the built-in shortcut menu for fields in table and query datasheets, forms, and reports, except where you've added a custom shortcut menu for a form, report, or control.</span></span>

## <a name="setting"></a><span data-ttu-id="350f9-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="350f9-111">Setting</span></span>

<span data-ttu-id="350f9-112">**ДобавитьМеню** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="350f9-112">The **AddMenu** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="350f9-113">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="350f9-113">Action argument</span></span></p></th>
<th><p><span data-ttu-id="350f9-114">Описание</span><span class="sxs-lookup"><span data-stu-id="350f9-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="350f9-115"><strong>Имя меню</strong></span><span class="sxs-lookup"><span data-stu-id="350f9-115"><strong>Menu Name</strong></span></span></p></td>
<td><p><span data-ttu-id="350f9-116">Имя меню, например, &quot;команды отчета&quot; или &quot;средств&quot;.</span><span class="sxs-lookup"><span data-stu-id="350f9-116">The name of the menu, for example, &quot;Report Commands&quot; or &quot;Tools&quot;.</span></span> <span data-ttu-id="350f9-117">Чтобы создать ключ доступа, чтобы выбрать в меню можно использовать клавиатуру, введите амперсанд (<strong>&amp;</strong>) перед буквой, нужно быть ключом доступа.</span><span class="sxs-lookup"><span data-stu-id="350f9-117">To create an access key so that you can use the keyboard to choose the menu, type an ampersand (<strong>&amp;</strong>) before the letter you want to be the access key.</span></span> <span data-ttu-id="350f9-118">В этом буква будет подчеркнуто в поле имя меню на вкладке <strong>Надстройки</strong> .</span><span class="sxs-lookup"><span data-stu-id="350f9-118">This letter will be underlined in the menu name on the <strong>Add-Ins</strong> tab.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="350f9-119"><strong>Имя макроса</strong></span><span class="sxs-lookup"><span data-stu-id="350f9-119"><strong>Menu Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="350f9-120">Имя группы макросов, содержащий макросы для команды меню.</span><span class="sxs-lookup"><span data-stu-id="350f9-120">The name of the macro group that contains the macros for the menu's commands.</span></span> <span data-ttu-id="350f9-121">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="350f9-121">This is a required argument.</span></span></p>

> [!NOTE]
> <span data-ttu-id="350f9-122">Если макрос, содержащий **макрокоманды в базе данных библиотеки** , Microsoft Office Access 2007 выполняет поиск группы макросов с этим именем только текущей базы данных.</span><span class="sxs-lookup"><span data-stu-id="350f9-122">If you run a macro containing the **AddMenu** action in a library database, Microsoft Office Access 2007 looks for the macro group with this name in the current database only.</span></span>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="350f9-123"><strong>Текст в строке состояния</strong></span><span class="sxs-lookup"><span data-stu-id="350f9-123"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="350f9-124">Текст, отображаемый в строке состояния при выборе меню.</span><span class="sxs-lookup"><span data-stu-id="350f9-124">The text to display in the status bar when the menu is selected.</span></span> <span data-ttu-id="350f9-125">Этот аргумент игнорируется для контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="350f9-125">This argument is ignored for shortcut menus.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="350f9-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="350f9-126">Remarks</span></span>

<span data-ttu-id="350f9-127">Для запуска **макрокоманды** в Visual Basic для приложений (VBA) модуль, используйте метод **ДобавитьМеню** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="350f9-127">To run the **AddMenu** action in a Visual Basic for Applications (VBA) module, use the **AddMenu** method of the **DoCmd** object.</span></span> <span data-ttu-id="350f9-128">Также можно задать свойство **строки меню** или **ShortcutMenuBar** в VBA для создания настраиваемого меню на вкладке **Надстройки** , чтобы присоединить настраиваемого контекстного меню для формы, отчета или элемента управления.</span><span class="sxs-lookup"><span data-stu-id="350f9-128">You can also set the **MenuBar** or **ShortcutMenuBar** property in VBA to create a custom menu on the **Add-Ins** tab or to attach a custom shortcut menu to a form, report, or control.</span></span> <span data-ttu-id="350f9-129">Можно задать свойство **ShortcutMenuBar** объекта **приложения** для создания глобального контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="350f9-129">You can set the **ShortcutMenuBar** property of the **Application** object to create a global shortcut menu.</span></span>

