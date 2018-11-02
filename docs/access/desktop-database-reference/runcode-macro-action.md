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
ms.openlocfilehash: acf8ed2bd10efd55436b8933a862833b8e49c5f0
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926691"
---
# <a name="runcode-macro-action"></a><span data-ttu-id="ff767-102">Макрокоманда RunCode</span><span class="sxs-lookup"><span data-stu-id="ff767-102">RunCode macro action</span></span>


<span data-ttu-id="ff767-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff767-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ff767-104">Действием **RunCode** можно использовать для вызова Visual Basic для приложений (VBA) функция процедуры.</span><span class="sxs-lookup"><span data-stu-id="ff767-104">You can use the **RunCode** action to call a Visual Basic for Applications (VBA) Function procedure.</span></span>

## <a name="setting"></a><span data-ttu-id="ff767-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="ff767-105">Setting</span></span>

<span data-ttu-id="ff767-106">Действие **ЗапускПрограммы** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="ff767-106">The **RunCode** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ff767-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="ff767-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="ff767-108">Описание</span><span class="sxs-lookup"><span data-stu-id="ff767-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ff767-109"><strong>Имя функции</strong></span><span class="sxs-lookup"><span data-stu-id="ff767-109"><strong>Function Name</strong></span></span></p></td>
<td><p><span data-ttu-id="ff767-110">Имя процедуры функцию VBA для вызова.</span><span class="sxs-lookup"><span data-stu-id="ff767-110">The name of the VBA Function procedure to call.</span></span> <span data-ttu-id="ff767-111">Необходимые аргументы заключите в круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="ff767-111">Enclose any function arguments in parentheses.</span></span> <span data-ttu-id="ff767-112">Введите имя функции в поле <strong>Имя функции</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="ff767-112">Enter the function name in the <strong>Function Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="ff767-113">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="ff767-113">This is a required argument.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="ff767-114">В базе данных Microsoft Access (MDB- или .accdb) нажмите кнопку <STRONG>Построить</STRONG> использовать построитель выражений для выбора функции для этого аргумента.</span><span class="sxs-lookup"><span data-stu-id="ff767-114">In an Access database (.mdb or .accdb), click the <STRONG>Build</STRONG> button to use the Expression Builder to select a function for this argument.</span></span> <span data-ttu-id="ff767-115">Выберите нужную функцию в списке в построителе выражений.</span><span class="sxs-lookup"><span data-stu-id="ff767-115">Click the desired function in the list in the Expression Builder.</span></span></P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ff767-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="ff767-116">Remarks</span></span>

<span data-ttu-id="ff767-117">Процедуры пользовательских функций, хранятся в модулях Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="ff767-117">The user-defined Function procedures are stored in Microsoft Access modules.</span></span>

<span data-ttu-id="ff767-118">Необходимо включить скобки, даже если процедуру Function не требует аргументов, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="ff767-118">You must include parentheses, even if the Function procedure doesn't have any arguments, as in the following example:</span></span>

`TestFunction()`

<span data-ttu-id="ff767-119">В отличие от пользовательских функций, используемых для свойств событий, имя функции в качестве аргумента **Имя функции** не начинается со знака равенства (**=**).</span><span class="sxs-lookup"><span data-stu-id="ff767-119">Unlike user-defined function names used for event property settings, the function name in the **Function Name** argument doesn't begin with an equal sign (**=**).</span></span>

<span data-ttu-id="ff767-120">Access игнорирует возвращаемое значение функции.</span><span class="sxs-lookup"><span data-stu-id="ff767-120">Access ignores the return value of the function.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ff767-121">Не удается вызвать процедуру Function в макросе, если имя функции совпадает с именем модуля.</span><span class="sxs-lookup"><span data-stu-id="ff767-121">You can't call a Function procedure from a macro if the function name is the same as the module name.</span></span></P>




> [!TIP]
> <P><span data-ttu-id="ff767-122">Для выполнения процедуры Sub или процедуру события, написанных на языке Visual Basic, создайте Function, которая вызывает процедуру Sub или процедуру события.</span><span class="sxs-lookup"><span data-stu-id="ff767-122">To run a Sub procedure or event procedure written in Visual Basic, create a Function procedure that calls the Sub procedure or event procedure.</span></span> <span data-ttu-id="ff767-123">Затем используйте действием <STRONG>RunCode</STRONG> для запуска процедуру Function.</span><span class="sxs-lookup"><span data-stu-id="ff767-123">Then use the <STRONG>RunCode</STRONG> action to run the Function procedure.</span></span></P>



<span data-ttu-id="ff767-124">Если вы используете действие **ЗапускПрограммы** для вызова функции, поиск функцию с именем, указанным в аргументе **Имя функции** в стандартных модулях базы данных.</span><span class="sxs-lookup"><span data-stu-id="ff767-124">If you use the **RunCode** action to call a function, Access looks for the function with the name specified by the **Function Name** argument in the standard modules for the database.</span></span> <span data-ttu-id="ff767-125">Тем не менее если это действие выполняется в ответ на нажатие команды меню в форму или отчет или в ответ на события на форму или отчет, сначала поиск функции в модуле класса формы или отчета, а затем в стандартных модулях.</span><span class="sxs-lookup"><span data-stu-id="ff767-125">However, when this action runs in response to clicking a menu command on a form or report or in response to an event on a form or report, Access first looks for the function in the form's or report's class module and then in the standard modules.</span></span> <span data-ttu-id="ff767-126">Access не поиска модулей класса, которые отображаются в области **модулей** области переходов для функции, указанный в аргументе **Имя функции** .</span><span class="sxs-lookup"><span data-stu-id="ff767-126">Access doesn't search the class modules that appear in the **Modules** area of the Navigation Pane for the function specified by the **Function Name** argument.</span></span>

<span data-ttu-id="ff767-127">Это действие недоступно в модуле VBA.</span><span class="sxs-lookup"><span data-stu-id="ff767-127">This action isn't available in a VBA module.</span></span> <span data-ttu-id="ff767-128">Вместо этого запустите нужную процедуру Function непосредственно в VBA.</span><span class="sxs-lookup"><span data-stu-id="ff767-128">Instead, run the desired Function procedure directly in VBA.</span></span>

