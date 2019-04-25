---
title: Макроблок Если... То... Иначе
TOCTitle: If...Then...Else macro block
ms:assetid: 0c4a4b7a-4fdb-9dbc-a94e-939a2ff1c0e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845158(v=office.15)
ms:contentKeyID: 48543188
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: fb6cbd6cc925a3e4841d9e7d6d77332cc36c7a03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291896"
---
# <a name="ifthenelse-macro-block"></a><span data-ttu-id="2fb11-102">Макроблок Если... То... Иначе</span><span class="sxs-lookup"><span data-stu-id="2fb11-102">If...Then...Else macro block</span></span>


<span data-ttu-id="2fb11-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2fb11-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2fb11-104">Вы можете использовать макроблок **Если**, чтобы выполнять группы макрокоманд в зависимости от значения выражения.</span><span class="sxs-lookup"><span data-stu-id="2fb11-104">You can use the **If** macro block to conditionally execute a group of actions, depending on the value of an expression.</span></span>

```vb
    If expression Then 
     Insert macro actions here ... 
    Else If expression 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

## <a name="setting"></a><span data-ttu-id="2fb11-105">Настройка</span><span class="sxs-lookup"><span data-stu-id="2fb11-105">Setting</span></span>

<span data-ttu-id="2fb11-106">Как для макроблока **Если**, так и для макроблока **Иначе если** необходимо задать следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="2fb11-106">For both **If** and **Else If**, the following arguments are required.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2fb11-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="2fb11-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="2fb11-108">Описание</span><span class="sxs-lookup"><span data-stu-id="2fb11-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2fb11-109"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="2fb11-109"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="2fb11-110">Условие, истинность которого должна проверяться.</span><span class="sxs-lookup"><span data-stu-id="2fb11-110">The condition that you wish to test.</span></span> <span data-ttu-id="2fb11-111">Принимает значение ИСТИНА или ЛОЖЬ.</span><span class="sxs-lookup"><span data-stu-id="2fb11-111">It must be an expression that evaluates to True or False.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2fb11-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="2fb11-112">Remarks</span></span>

<span data-ttu-id="2fb11-113">При выборе макроблока **Если** появляется поле для ввода выражения, представляющего собой условие, истинность которого будет в дальнейшем проверяться.</span><span class="sxs-lookup"><span data-stu-id="2fb11-113">When you select the **If** macro block, a textbox appears so that you can enter an expression that represents the condition you wish to test.</span></span> <span data-ttu-id="2fb11-114">Кроме того, доступно поле со списком, в которое можно добавить макрокоманду. Под ним автоматически отображается текст "Конец блока "Если"</span><span class="sxs-lookup"><span data-stu-id="2fb11-114">In addition, a combo box appears where you can insert a macro action, below which the text "End If" automatically displays.</span></span> <span data-ttu-id="2fb11-115">Поля "Если" и "Конец блока "Если" ограничивают область, в которую можно добавить группу (блок) макрокоманд.</span><span class="sxs-lookup"><span data-stu-id="2fb11-115">The If and the End If bracket an area in which you can enter a group, or block, of actions.</span></span> <span data-ttu-id="2fb11-116">Макрокоманды блока будут выполнены лишь в случае, если введенное выражение примет значение ИСТИНА.</span><span class="sxs-lookup"><span data-stu-id="2fb11-116">The block executes only if the expression that you enter is True.</span></span>

<span data-ttu-id="2fb11-117">Для проверки истинности другого выражения в случае ложности первого вы можете выбрать команду **Добавить блок "Иначе если"**, чтобы вставить необязательный блок **Иначе если**.</span><span class="sxs-lookup"><span data-stu-id="2fb11-117">To evaluate a different expression when the first expression is false, you can click **Add Else If** to insert an optional **Else If** block.</span></span> <span data-ttu-id="2fb11-118">Необходимо ввести выражение, принимающее значение ИСТИНА или ЛОЖЬ.</span><span class="sxs-lookup"><span data-stu-id="2fb11-118">You must enter an expression that evaluates to True or False.</span></span> <span data-ttu-id="2fb11-119">Добавленный блок будет выполнен только в случае истинности этого выражения и ложности первого.</span><span class="sxs-lookup"><span data-stu-id="2fb11-119">In this case, the block executes only if the expression is True and the first expression is False.</span></span>

<span data-ttu-id="2fb11-120">К блоку "Если" можно добавить любое число блоков **Иначе если**.</span><span class="sxs-lookup"><span data-stu-id="2fb11-120">You can add as many **Else If** blocks as you like to an If block.</span></span>

<span data-ttu-id="2fb11-121">Вы можете выбрать команду **Добавить блок "Иначе"**, чтобы вставить необязательный блок **Иначе**.</span><span class="sxs-lookup"><span data-stu-id="2fb11-121">You can click **Add Else** to insert an optional **Else** block.</span></span> <span data-ttu-id="2fb11-122">В этом случае макрокоманды, добавленные под формой **Иначе**, сформируют блок **Иначе**, который будет выполнен только в случае ложности выражений в блоках "Если" и "Иначе если".</span><span class="sxs-lookup"><span data-stu-id="2fb11-122">In this case, the actions that you insert below the **Else** form the **Else** block, which executes only when the actions above do not.</span></span> <span data-ttu-id="2fb11-123">К каждому блоку **Если** можно добавить один блок **Иначе**.</span><span class="sxs-lookup"><span data-stu-id="2fb11-123">You can add a single **Else** block to an **If** block.</span></span>

<span data-ttu-id="2fb11-124">В представленном ниже примере кода макрокоманды первого блока выполняются, если параметр \[Status\] принимает положительное значение.</span><span class="sxs-lookup"><span data-stu-id="2fb11-124">In the following code example, the macro actions in the first block execute if the value of \[Status\] is greater than 0.</span></span> <span data-ttu-id="2fb11-125">Если значение параметра \[Status\] отрицательно или равно нулю, оценивается истинность выражения в блоке **Иначе если**.</span><span class="sxs-lookup"><span data-stu-id="2fb11-125">If the value of \[Status\] is not greater than 0, the expression that follows the **Else If** is evaluated.</span></span> <span data-ttu-id="2fb11-126">Макрокоманды блока **Иначе если** выполняются, если параметр \[Status\] равен нулю.</span><span class="sxs-lookup"><span data-stu-id="2fb11-126">The macro actions in the **Else If** block execute if the value of \[Status\] is equal to 0.</span></span> <span data-ttu-id="2fb11-127">Наконец, если ложны выражения как в первом, так и во втором блоке, выполняются макрокоманды блока **Иначе**.</span><span class="sxs-lookup"><span data-stu-id="2fb11-127">Finally, if neither the first block nor the second block execute, the actions in the **Else** block execute.</span></span>

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
    Else If [Status] = 0 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

<span data-ttu-id="2fb11-128">Вы можете вкладывать блоки **Если** друг в друга.</span><span class="sxs-lookup"><span data-stu-id="2fb11-128">You can nest **If** blocks.</span></span> <span data-ttu-id="2fb11-129">Один блок **Если** можно вложить в другой, если в случае истинности первого выражения нужно оценить второе.</span><span class="sxs-lookup"><span data-stu-id="2fb11-129">You should consider nesting an **If** block within an **If** block if you want to evaluate a second expression when the first expression is True.</span></span> <span data-ttu-id="2fb11-130">В представленном ниже примере кода внутренний блок **Если** выполняется только если значение параметра \[Status\] положительно *и* больше 100.</span><span class="sxs-lookup"><span data-stu-id="2fb11-130">In the following code example, the inner **If** block only executes when the value of \[Status\] is both greater than 0 *and* greater than 100.</span></span>

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
     If [Status] > 100 
     Insert macro actions here ... 
     EndifEnd If
```
