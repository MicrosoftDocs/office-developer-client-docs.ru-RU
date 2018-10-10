---
title: If...Then...Else Macro Block
TOCTitle: If...Then...Else Macro Block
ms:assetid: 0c4a4b7a-4fdb-9dbc-a94e-939a2ff1c0e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845158(v=office.15)
ms:contentKeyID: 48543188
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 79e5379ad2c50eff3ddf12b597defc7b85cefb39
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483179"
---
# <a name="ifthenelse-macro-block"></a><span data-ttu-id="9bf28-102">If...Then...Else Macro Block</span><span class="sxs-lookup"><span data-stu-id="9bf28-102">If...Then...Else Macro Block</span></span>


<span data-ttu-id="9bf28-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9bf28-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9bf28-104">Можно использовать макрос блок **If** позволяет выполнять группу действия в зависимости от значения выражения.</span><span class="sxs-lookup"><span data-stu-id="9bf28-104">You can use the **If** macro block to conditionally execute a group of actions, depending on the value of an expression.</span></span>

```vb
    If expression Then 
     Insert macro actions here ... 
    Else If expression 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

## <a name="setting"></a><span data-ttu-id="9bf28-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="9bf28-105">Setting</span></span>

<span data-ttu-id="9bf28-106">**Если** и **Else If**требуются следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="9bf28-106">For both **If** and **Else If**, the following arguments are required.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9bf28-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="9bf28-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="9bf28-108">Описание</span><span class="sxs-lookup"><span data-stu-id="9bf28-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9bf28-109"><strong>Выражение</strong></span><span class="sxs-lookup"><span data-stu-id="9bf28-109"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="9bf28-110">Условие, которое требуется проверить.</span><span class="sxs-lookup"><span data-stu-id="9bf28-110">The condition that you wish to test.</span></span> <span data-ttu-id="9bf28-111">Это должно быть выражение, которое оценивается как True или False.</span><span class="sxs-lookup"><span data-stu-id="9bf28-111">It must be an expression that evaluates to True or False.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9bf28-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="9bf28-112">Remarks</span></span>

<span data-ttu-id="9bf28-113">При выборе макрос блок **If** текстовое поле отображается таким образом, можно ввести выражение, представляющее условие, которую вы хотите проверить.</span><span class="sxs-lookup"><span data-stu-id="9bf28-113">When you select the **If** macro block, a textbox appears so that you can enter an expression that represents the condition you wish to test.</span></span> <span data-ttu-id="9bf28-114">Кроме того поле со списком отображается, где можно вставить действия макроса, под которой автоматически отображается текст «End If».</span><span class="sxs-lookup"><span data-stu-id="9bf28-114">In addition, a combo box appears where you can insert a macro action, below which the text "End If" automatically displays.</span></span> <span data-ttu-id="9bf28-115">If и End If квадратная скобка область, в котором можно ввести группу или блок действия.</span><span class="sxs-lookup"><span data-stu-id="9bf28-115">The If and the End If bracket an area in which you can enter a group, or block, of actions.</span></span> <span data-ttu-id="9bf28-116">Блок выполняется только в том случае, если выражение, которое вводится имеет значение True.</span><span class="sxs-lookup"><span data-stu-id="9bf28-116">The block executes only if the expression that you enter is True.</span></span>

<span data-ttu-id="9bf28-117">Чтобы оценить различные выражения, если первое выражение имеет значение false, щелкните **Добавить Else If** для вставки необязательно блок **Else If** .</span><span class="sxs-lookup"><span data-stu-id="9bf28-117">To evaluate a different expression when the first expression is false, you can click **Add Else If** to insert an optional **Else If** block.</span></span> <span data-ttu-id="9bf28-118">Необходимо ввести выражение, которое оценивается как True или False.</span><span class="sxs-lookup"><span data-stu-id="9bf28-118">You must enter an expression that evaluates to True or False.</span></span> <span data-ttu-id="9bf28-119">В этом случае блок выполняется только в том случае, если выражение имеет значение True и первое выражение имеет значение False.</span><span class="sxs-lookup"><span data-stu-id="9bf28-119">In this case, the block executes only if the expression is True and the first expression is False.</span></span>

<span data-ttu-id="9bf28-120">Как вы, как в том случае, если блокировка можно добавить столько блоки **Else If** .</span><span class="sxs-lookup"><span data-stu-id="9bf28-120">You can add as many **Else If** blocks as you like to an If block.</span></span>

<span data-ttu-id="9bf28-121">Щелкните **Добавить Else** для вставки блок **Else** необязательно.</span><span class="sxs-lookup"><span data-stu-id="9bf28-121">You can click **Add Else** to insert an optional **Else** block.</span></span> <span data-ttu-id="9bf28-122">В этом случае действия, которые можно вставить **Else** форм блок **Else** , который выполняет только в том случае, когда не следует действий, описанных выше.</span><span class="sxs-lookup"><span data-stu-id="9bf28-122">In this case, the actions that you insert below the **Else** form the **Else** block, which executes only when the actions above do not.</span></span> <span data-ttu-id="9bf28-123">**Если** блок можно добавить один блок **Else** .</span><span class="sxs-lookup"><span data-stu-id="9bf28-123">You can add a single **Else** block to an **If** block.</span></span>

<span data-ttu-id="9bf28-124">В следующем примере кода макрокоманд в первый блок выполняется, если значение \[состояние\] больше 0.</span><span class="sxs-lookup"><span data-stu-id="9bf28-124">In the following code example, the macro actions in the first block execute if the value of \[Status\] is greater than 0.</span></span> <span data-ttu-id="9bf28-125">Если значение \[состояние\] не больше 0, исходя из **Else If** выражение.</span><span class="sxs-lookup"><span data-stu-id="9bf28-125">If the value of \[Status\] is not greater than 0, the expression that follows the **Else If** is evaluated.</span></span> <span data-ttu-id="9bf28-126">Действия макроса в блоке **Else If** выполняется, если значение \[состояние\] равно 0.</span><span class="sxs-lookup"><span data-stu-id="9bf28-126">The macro actions in the **Else If** block execute if the value of \[Status\] is equal to 0.</span></span> <span data-ttu-id="9bf28-127">И, наконец Если первый блок ни второй блок выполнение, выполните действия в блоке **Else** .</span><span class="sxs-lookup"><span data-stu-id="9bf28-127">Finally, if neither the first block nor the second block execute, the actions in the **Else** block execute.</span></span>

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
    Else If [Status] = 0 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

<span data-ttu-id="9bf28-128">**Если** блоки можно вкладывать.</span><span class="sxs-lookup"><span data-stu-id="9bf28-128">You can nest **If** blocks.</span></span> <span data-ttu-id="9bf28-129">Необходимо учитывать вложением блока **Если** блока **если** , чтобы оценить второго выражения, если первое выражение имеет значение True.</span><span class="sxs-lookup"><span data-stu-id="9bf28-129">You should consider nesting an **If** block within an **If** block if you want to evaluate a second expression when the first expression is True.</span></span> <span data-ttu-id="9bf28-130">В следующем примере кода внутреннего блока **If** выполняется только если значение \[состояние\] оба больше 0 *и* больше 100.</span><span class="sxs-lookup"><span data-stu-id="9bf28-130">In the following code example, the inner **If** block only executes when the value of \[Status\] is both greater than 0 *and* greater than 100.</span></span>

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
     If [Status] > 100 
     Insert macro actions here ... 
     EndifEnd If
```
