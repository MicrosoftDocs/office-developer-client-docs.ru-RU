---
title: If... Then... Else Macro Block (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 18d28dc1-c41f-47c6-b5c7-258d5f877d01
description: Можно использовать блок макросов if для условного выполнения группы действий в зависимости от значения выражения.
ms.openlocfilehash: 6fe82e2c42f8e5d93cdc26798e7572e32d6cdc7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304265"
---
# <a name="ifthenelse-macro-block-access-custom-web-app"></a><span data-ttu-id="9fb93-103">If... Then... Else Macro Block (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="9fb93-103">If...Then...Else Macro Block (Access custom web app)</span></span>

<span data-ttu-id="9fb93-104">Можно использовать блок макросов **If** для условного выполнения группы действий в зависимости от значения выражения.</span><span class="sxs-lookup"><span data-stu-id="9fb93-104">You can use the **If** macro block to conditionally execute a group of actions, depending on the value of an expression.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="9fb93-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="9fb93-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="9fb93-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="9fb93-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9fb93-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9fb93-107">Syntax</span></span>

```vb
IfexpressionThen 
 Insert macro actions here ... 
Else Ifexpression  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

## <a name="setting"></a><span data-ttu-id="9fb93-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="9fb93-108">Setting</span></span>

<span data-ttu-id="9fb93-109">Для **If** и \* \* Else If \* \* необходимо указать следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="9fb93-109">For both **If** and \*\* Else If \*\*, the following arguments are required.</span></span> 
  
|<span data-ttu-id="9fb93-110">**Аргумент макрокоманды**</span><span class="sxs-lookup"><span data-stu-id="9fb93-110">**Action argument**</span></span>|<span data-ttu-id="9fb93-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9fb93-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9fb93-112">**Expression**</span><span class="sxs-lookup"><span data-stu-id="9fb93-112">**Expression**</span></span> <br/> |<span data-ttu-id="9fb93-113">Условие, которое вы хотите проверить.</span><span class="sxs-lookup"><span data-stu-id="9fb93-113">The condition that you wish to test.</span></span> <span data-ttu-id="9fb93-114">Это должно быть выражение, вычисление которого дает значение true или false.</span><span class="sxs-lookup"><span data-stu-id="9fb93-114">It must be an expression that evaluates to True or False.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9fb93-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="9fb93-115">Remarks</span></span>

<span data-ttu-id="9fb93-116">Когда вы выбираете блок макроса **If** , появляется текстовое поле, в котором можно ввести выражение, представляющее условие, которое необходимо протестировать.</span><span class="sxs-lookup"><span data-stu-id="9fb93-116">When you select the **If** macro block, a textbox appears so that you can enter an expression that represents the condition you wish to test.</span></span> <span data-ttu-id="9fb93-117">Кроме того, отображается поле со списком, в котором можно вставить макрокоманду, расположенную под текстом "End If", которое автоматически отображается.</span><span class="sxs-lookup"><span data-stu-id="9fb93-117">In addition, a combo box appears where you can insert a macro action, below which the text "End If" automatically displays.</span></span> <span data-ttu-id="9fb93-118">If и End, если квадратная скобка область, в которой можно ввести группу или заблокировать действия.</span><span class="sxs-lookup"><span data-stu-id="9fb93-118">The If and the End If bracket an area in which you can enter a group, or block, of actions.</span></span> <span data-ttu-id="9fb93-119">Блок выполняется только в том случае, если введенное выражение имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="9fb93-119">The block executes only if the expression that you enter is True.</span></span> 
  
<span data-ttu-id="9fb93-120">Чтобы оценить другое выражение, если первое выражение имеет значение false, можно нажать кнопку **Добавить Else, если** нужно вставить необязательный блок **Else If** .</span><span class="sxs-lookup"><span data-stu-id="9fb93-120">To evaluate a different expression when the first expression is false, you can click **Add Else If** to insert an optional **Else If** block.</span></span> <span data-ttu-id="9fb93-121">Необходимо ввести выражение, которое оценивается как true или false.</span><span class="sxs-lookup"><span data-stu-id="9fb93-121">You must enter an expression that evaluates to True or False.</span></span> <span data-ttu-id="9fb93-122">В этом случае блок выполняется только в том случае, если выражение имеет значение true, а первое выражение имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="9fb93-122">In this case, the block executes only if the expression is True and the first expression is False.</span></span> 
  
<span data-ttu-id="9fb93-123">Вы можете добавить любое количество **else, если** вы хотите блоку if.</span><span class="sxs-lookup"><span data-stu-id="9fb93-123">You can add as many **Else If** blocks as you like to an If block.</span></span> 
  
<span data-ttu-id="9fb93-124">Вы можете нажать кнопку **Добавить еще** , чтобы вставить необязательный блок **else** .</span><span class="sxs-lookup"><span data-stu-id="9fb93-124">You can click **Add Else** to insert an optional **Else** block.</span></span> <span data-ttu-id="9fb93-125">В этом случае действия, которые вы вставляете под **другим** разделом, заменяют блок **else** , который выполняется, только если не выполняются действия, указанные выше.</span><span class="sxs-lookup"><span data-stu-id="9fb93-125">In this case, the actions that you insert below the **Else** form the **Else** block, which executes only when the actions above do not.</span></span> <span data-ttu-id="9fb93-126">Вы можете добавить один блок **else** в блок **If** .</span><span class="sxs-lookup"><span data-stu-id="9fb93-126">You can add a single **Else** block to an **If** block.</span></span> 
  
<span data-ttu-id="9fb93-127">В следующем примере кода макрокоманды в первом блоке выполняются, если значение [Status] больше 0.</span><span class="sxs-lookup"><span data-stu-id="9fb93-127">In the following code example, the macro actions in the first block execute if the value of [Status] is greater than 0.</span></span> <span data-ttu-id="9fb93-128">Если значение [Status] не больше 0, вычисляется выражение, следующее за знаком **Else If** .</span><span class="sxs-lookup"><span data-stu-id="9fb93-128">If the value of [Status] is not greater than 0, the expression that follows the **Else If** is evaluated.</span></span> <span data-ttu-id="9fb93-129">Макрокоманды в блоке **Else If** выполняются, если значение параметра [Status] равно 0.</span><span class="sxs-lookup"><span data-stu-id="9fb93-129">The macro actions in the **Else If** block execute if the value of [Status] is equal to 0.</span></span> <span data-ttu-id="9fb93-130">Наконец, если не выполняется ни первый блок, ни второй блок Execute, действия в блоке **else** выполняются.</span><span class="sxs-lookup"><span data-stu-id="9fb93-130">Finally, if neither the first block nor the second block execute, the actions in the **Else** block execute.</span></span> 
  
```vb
If[Status] > 0Then 
 Insert macro actions here ... 
Else If[Status] = 0  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

<span data-ttu-id="9fb93-131">Вы можете вложить блоки **If** .</span><span class="sxs-lookup"><span data-stu-id="9fb93-131">You can nest **If** blocks.</span></span> <span data-ttu-id="9fb93-132">Следует рассмотреть вложение блока **If** в блоке **If** , если необходимо оценить второе выражение, если первое выражение имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="9fb93-132">You should consider nesting an **If** block within an **If** block if you want to evaluate a second expression when the first expression is True.</span></span> <span data-ttu-id="9fb93-133">В приведенном ниже примере кода внутренний блок **If** выполняется только в том случае, если значение [Status] больше 0 *и* больше 100.</span><span class="sxs-lookup"><span data-stu-id="9fb93-133">In the following code example, the inner **If** block only executes when the value of [Status] is both greater than 0  *and*  greater than 100.</span></span> 
  

