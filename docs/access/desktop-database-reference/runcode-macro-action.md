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
# <a name="runcode-macro-action"></a><span data-ttu-id="d92ba-102">Макрокоманда RunCode</span><span class="sxs-lookup"><span data-stu-id="d92ba-102">RunCode macro action</span></span>

<span data-ttu-id="d92ba-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d92ba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d92ba-104">Вы можете использовать макрокоманду **ЗапускПрограммы (RunCode** ) для вызова функции Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="d92ba-104">You can use the **RunCode** action to call a Visual Basic for Applications (VBA) Function procedure.</span></span>

## <a name="setting"></a><span data-ttu-id="d92ba-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="d92ba-105">Setting</span></span>

<span data-ttu-id="d92ba-106">Макрокоманда **ЗапускПрограммы** имеет следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="d92ba-106">The **RunCode** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d92ba-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="d92ba-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d92ba-108">Описание</span><span class="sxs-lookup"><span data-stu-id="d92ba-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d92ba-109"><strong>Имя функции</strong></span><span class="sxs-lookup"><span data-stu-id="d92ba-109"><strong>Function Name</strong></span></span></p></td>
<td><p><span data-ttu-id="d92ba-110">Имя вызываемой процедуры функции VBA.</span><span class="sxs-lookup"><span data-stu-id="d92ba-110">The name of the VBA Function procedure to call.</span></span> <span data-ttu-id="d92ba-111">Заключите все аргументы функции в круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="d92ba-111">Enclose any function arguments in parentheses.</span></span> <span data-ttu-id="d92ba-112">Введите имя функции в поле <strong>имя функции</strong> в разделе <strong>аргументы макрокоманды</strong> в области построителя макросов.</span><span class="sxs-lookup"><span data-stu-id="d92ba-112">Enter the function name in the <strong>Function Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="d92ba-113">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="d92ba-113">This is a required argument.</span></span></p><p><span data-ttu-id="d92ba-114"><strong>Примечание</strong>: в базе данных Access (MDB или ACCDB) нажмите кнопку <strong>построить</strong> , чтобы использовать построитель выражений для выбора функции для этого аргумента.</span><span class="sxs-lookup"><span data-stu-id="d92ba-114"><strong>NOTE</strong>: In an Access database (.mdb or .accdb), click the <strong>Build</strong> button to use the Expression Builder to select a function for this argument.</span></span> <span data-ttu-id="d92ba-115">Выберите нужную функцию в списке в поСтроителе выражений.</span><span class="sxs-lookup"><span data-stu-id="d92ba-115">Click the desired function in the list in the Expression Builder.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d92ba-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="d92ba-116">Remarks</span></span>

<span data-ttu-id="d92ba-117">Процедуры пользовательской функции хранятся в модулях Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="d92ba-117">The user-defined Function procedures are stored in Microsoft Access modules.</span></span>

<span data-ttu-id="d92ba-118">Необходимо включить круглые скобки, даже если процедура Function не содержит аргументов, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="d92ba-118">You must include parentheses, even if the Function procedure doesn't have any arguments, as in the following example:</span></span>

`TestFunction()`

<span data-ttu-id="d92ba-119">В отличие от имен пользовательских функций, используемых для параметров свойств событий, имя функции в аргументе **имя функции** не начинается со знака равенства (**=**).</span><span class="sxs-lookup"><span data-stu-id="d92ba-119">Unlike user-defined function names used for event property settings, the function name in the **Function Name** argument doesn't begin with an equal sign (**=**).</span></span>

<span data-ttu-id="d92ba-120">Access игнорирует возвращаемое значение функции.</span><span class="sxs-lookup"><span data-stu-id="d92ba-120">Access ignores the return value of the function.</span></span>

> [!NOTE]
> <span data-ttu-id="d92ba-121">Невозможно вызвать процедуру Function из макроса, если имя функции совпадает с именем модуля.</span><span class="sxs-lookup"><span data-stu-id="d92ba-121">You can't call a Function procedure from a macro if the function name is the same as the module name.</span></span>

> [!TIP]
> <span data-ttu-id="d92ba-122">Чтобы выполнить подпроцедуру или процедуру обработки события, написанную на языке Visual Basic, создайте процедуру Function, которая вызывает процедуру Sub или процедуру обработки события.</span><span class="sxs-lookup"><span data-stu-id="d92ba-122">To run a Sub procedure or event procedure written in Visual Basic, create a Function procedure that calls the Sub procedure or event procedure.</span></span> <span data-ttu-id="d92ba-123">Затем используйте макрокоманду **ЗапускПрограммы (RunCode** ) для выполнения процедуры Function.</span><span class="sxs-lookup"><span data-stu-id="d92ba-123">Then use the **RunCode** action to run the Function procedure.</span></span>

<span data-ttu-id="d92ba-124">Если для вызова функции используется Макрокоманда **ЗапускПрограммы** , Access ищет функцию с именем, указанным аргументом **имени функции** в стандартных модулях базы данных.</span><span class="sxs-lookup"><span data-stu-id="d92ba-124">If you use the **RunCode** action to call a function, Access looks for the function with the name specified by the **Function Name** argument in the standard modules for the database.</span></span> <span data-ttu-id="d92ba-125">Однако если это действие выполняется в ответ на команду в форме или отчете или в ответ на событие в форме или отчете, Access сначала выполняет поиск функции в модуле класса формы или отчета, а затем в стандартных модулях.</span><span class="sxs-lookup"><span data-stu-id="d92ba-125">However, when this action runs in response to clicking a menu command on a form or report or in response to an event on a form or report, Access first looks for the function in the form's or report's class module and then in the standard modules.</span></span> <span data-ttu-id="d92ba-126">Access не выполняет поиск в модулях класса, которые отображаются в области **модулей** области навигации для функции, указанной аргументом " **имя функции** ".</span><span class="sxs-lookup"><span data-stu-id="d92ba-126">Access doesn't search the class modules that appear in the **Modules** area of the Navigation Pane for the function specified by the **Function Name** argument.</span></span>

<span data-ttu-id="d92ba-127">Это действие недоступно в модуле VBA.</span><span class="sxs-lookup"><span data-stu-id="d92ba-127">This action isn't available in a VBA module.</span></span> <span data-ttu-id="d92ba-128">Вместо этого запустите нужную процедуру непосредственно в VBA.</span><span class="sxs-lookup"><span data-stu-id="d92ba-128">Instead, run the desired Function procedure directly in VBA.</span></span>

