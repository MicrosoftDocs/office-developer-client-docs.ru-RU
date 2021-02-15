---
title: Макрокоманда RunCode
TOCTitle: RunCode macro action
ms:assetid: cb0625be-4b5d-4927-9b0e-59a6e411b5bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834373(v=office.15)
ms:contentKeyID: 48547706
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98700
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 646c1393cc798c1f827e6ceaebf46bfe7c87bcbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306834"
---
# <a name="runcode-macro-action"></a><span data-ttu-id="41fd4-102">Макрокоманда RunCode</span><span class="sxs-lookup"><span data-stu-id="41fd4-102">RunCode macro action</span></span>

<span data-ttu-id="41fd4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="41fd4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="41fd4-104">С помощью действия **RunCode** можно вызвать процедуру Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="41fd4-104">You can use the **RunCode** action to call a Visual Basic for Applications (VBA) Function procedure.</span></span>

## <a name="setting"></a><span data-ttu-id="41fd4-105">Setting</span><span class="sxs-lookup"><span data-stu-id="41fd4-105">Setting</span></span>

<span data-ttu-id="41fd4-106">Действие **RunCode** имеет следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="41fd4-106">The **RunCode** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="41fd4-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="41fd4-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="41fd4-108">Описание</span><span class="sxs-lookup"><span data-stu-id="41fd4-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41fd4-109"><strong>Имя функции</strong></span><span class="sxs-lookup"><span data-stu-id="41fd4-109"><strong>Function Name</strong></span></span></p></td>
<td><p><span data-ttu-id="41fd4-110">Имя вызываемой процедуры функции VBA.</span><span class="sxs-lookup"><span data-stu-id="41fd4-110">The name of the VBA Function procedure to call.</span></span> <span data-ttu-id="41fd4-111">Заключите все аргументы функции в скобки.</span><span class="sxs-lookup"><span data-stu-id="41fd4-111">Enclose any function arguments in parentheses.</span></span> <span data-ttu-id="41fd4-112">Введите имя функции в поле <strong>"Имя функции"</strong> в разделе <strong>"Аргументы действий"</strong> области построитель макроса.</span><span class="sxs-lookup"><span data-stu-id="41fd4-112">Enter the function name in the <strong>Function Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="41fd4-113">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="41fd4-113">This is a required argument.</span></span></p><p><span data-ttu-id="41fd4-114"><strong>ПРИМЕЧАНИЕ.</strong>В базе данных Access (MDB или <strong></strong> ACCDB) нажмите кнопку "Построение", чтобы использовать построитель выражений для выбора функции для этого аргумента.</span><span class="sxs-lookup"><span data-stu-id="41fd4-114"><strong>NOTE</strong>: In an Access database (.mdb or .accdb), click the <strong>Build</strong> button to use the Expression Builder to select a function for this argument.</span></span> <span data-ttu-id="41fd4-115">Щелкните нужную функцию в списке в построителье выражений.</span><span class="sxs-lookup"><span data-stu-id="41fd4-115">Click the desired function in the list in the Expression Builder.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="41fd4-116">Заметки</span><span class="sxs-lookup"><span data-stu-id="41fd4-116">Remarks</span></span>

<span data-ttu-id="41fd4-117">Пользовательские процедуры функций хранятся в модулях Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="41fd4-117">The user-defined Function procedures are stored in Microsoft Access modules.</span></span>

<span data-ttu-id="41fd4-118">Необходимо включить скобки, даже если в процедуре Function нет аргументов, как в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="41fd4-118">You must include parentheses, even if the Function procedure doesn't have any arguments, as in the following example:</span></span>

`TestFunction()`

<span data-ttu-id="41fd4-119">В отличие от имен пользовательских функций, используемых для параметров свойства события, имя функции в аргументе **имени** функции не начинается со знака равного **=** ().</span><span class="sxs-lookup"><span data-stu-id="41fd4-119">Unlike user-defined function names used for event property settings, the function name in the **Function Name** argument doesn't begin with an equal sign (**=**).</span></span>

<span data-ttu-id="41fd4-120">Access игнорирует возвращаемую функцию.</span><span class="sxs-lookup"><span data-stu-id="41fd4-120">Access ignores the return value of the function.</span></span>

> [!NOTE]
> <span data-ttu-id="41fd4-121">Процедуру Функции нельзя вызвать из макроса, если имя функции такое же, как имя модуля.</span><span class="sxs-lookup"><span data-stu-id="41fd4-121">You can't call a Function procedure from a macro if the function name is the same as the module name.</span></span>

> [!TIP]
> <span data-ttu-id="41fd4-122">Чтобы запустить процедуру sub или события, написанную на Visual Basic, создайте процедуру function, которая вызывает процедуру Sub или процедуру события.</span><span class="sxs-lookup"><span data-stu-id="41fd4-122">To run a Sub procedure or event procedure written in Visual Basic, create a Function procedure that calls the Sub procedure or event procedure.</span></span> <span data-ttu-id="41fd4-123">Затем используйте действие **RunCode** для запуска процедуры Function.</span><span class="sxs-lookup"><span data-stu-id="41fd4-123">Then use the **RunCode** action to run the Function procedure.</span></span>

<span data-ttu-id="41fd4-124">Если для вызова функции используется действие **RunCode,** Access ищет функцию с именем, указанным аргументом **Имени** функции в стандартных модулях базы данных.</span><span class="sxs-lookup"><span data-stu-id="41fd4-124">If you use the **RunCode** action to call a function, Access looks for the function with the name specified by the **Function Name** argument in the standard modules for the database.</span></span> <span data-ttu-id="41fd4-125">Однако если это действие выполняется в ответ на нажатие команды меню в форме или отчете или в ответ на событие в форме или отчете, Access сначала ищет функцию в модуле класса формы или отчета, а затем в стандартных модулях.</span><span class="sxs-lookup"><span data-stu-id="41fd4-125">However, when this action runs in response to clicking a menu command on a form or report or in response to an event on a form or report, Access first looks for the function in the form's or report's class module and then in the standard modules.</span></span> <span data-ttu-id="41fd4-126">Access не позволяет искать функцию, указанную в аргументе **Имени** функции, в модулях области навигации. </span><span class="sxs-lookup"><span data-stu-id="41fd4-126">Access doesn't search the class modules that appear in the **Modules** area of the Navigation Pane for the function specified by the **Function Name** argument.</span></span>

<span data-ttu-id="41fd4-127">Эта макрокоманда недоступна в модуле VBA. </span><span class="sxs-lookup"><span data-stu-id="41fd4-127">This action isn't available in a VBA module.</span></span> <span data-ttu-id="41fd4-128">Вместо этого запустите нужную процедуру функции непосредственно в VBA.</span><span class="sxs-lookup"><span data-stu-id="41fd4-128">Instead, run the desired Function procedure directly in VBA.</span></span>

