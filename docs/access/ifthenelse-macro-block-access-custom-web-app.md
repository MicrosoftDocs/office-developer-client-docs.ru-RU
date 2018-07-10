---
title: If... Затем... Блок else макросов (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 18d28dc1-c41f-47c6-b5c7-258d5f877d01
description: Можно использовать функции Если макрос блока, который позволяет выполнять группу действия в зависимости от значения выражения.
ms.openlocfilehash: 8ac78ff0eaf22c1d821e306654ebfa8fac4ed34a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806965"
---
# <a name="ifthenelse-macro-block-access-custom-web-app"></a><span data-ttu-id="f196a-103">If... Затем... Блок else макросов (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="f196a-103">If...Then...Else Macro Block (Access custom web app)</span></span>

<span data-ttu-id="f196a-104">Можно использовать макрос блок **If** позволяет выполнять группу действия в зависимости от значения выражения.</span><span class="sxs-lookup"><span data-stu-id="f196a-104">You can use the **If** macro block to conditionally execute a group of actions, depending on the value of an expression.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="f196a-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f196a-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="f196a-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="f196a-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f196a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f196a-107">Syntax</span></span>

```vb
IfexpressionThen 
 Insert macro actions here ... 
Else Ifexpression  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

## <a name="setting"></a><span data-ttu-id="f196a-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="f196a-108">Setting</span></span>

<span data-ttu-id="f196a-109">Для обоих **Если** и ** Else If **, необходимы следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="f196a-109">For both **If** and ** Else If **, the following arguments are required.</span></span> 
  
|<span data-ttu-id="f196a-110">**Аргумент действия**</span><span class="sxs-lookup"><span data-stu-id="f196a-110">**Action argument**</span></span>|<span data-ttu-id="f196a-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f196a-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f196a-112">**Выражение**</span><span class="sxs-lookup"><span data-stu-id="f196a-112">**Expression**</span></span> <br/> |<span data-ttu-id="f196a-113">Условие, которое требуется проверить.</span><span class="sxs-lookup"><span data-stu-id="f196a-113">The condition that you wish to test.</span></span> <span data-ttu-id="f196a-114">Это должно быть выражение, которое оценивается как True или False.</span><span class="sxs-lookup"><span data-stu-id="f196a-114">It must be an expression that evaluates to True or False.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f196a-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="f196a-115">Remarks</span></span>

<span data-ttu-id="f196a-116">При выборе макрос блок **If** текстовое поле отображается таким образом, можно ввести выражение, представляющее условие, которую вы хотите проверить.</span><span class="sxs-lookup"><span data-stu-id="f196a-116">When you select the **If** macro block, a textbox appears so that you can enter an expression that represents the condition you wish to test.</span></span> <span data-ttu-id="f196a-117">Кроме того поле со списком отображается, где можно вставить действия макроса, под которой автоматически отображается текст «End If».</span><span class="sxs-lookup"><span data-stu-id="f196a-117">In addition, a combo box appears where you can insert a macro action, below which the text "End If" automatically displays.</span></span> <span data-ttu-id="f196a-118">If и End If квадратная скобка область, в котором можно ввести группу или блок действия.</span><span class="sxs-lookup"><span data-stu-id="f196a-118">The If and the End If bracket an area in which you can enter a group, or block, of actions.</span></span> <span data-ttu-id="f196a-119">Блок выполняется только в том случае, если выражение, которое вводится имеет значение True.</span><span class="sxs-lookup"><span data-stu-id="f196a-119">The block executes only if the expression that you enter is True.</span></span> 
  
<span data-ttu-id="f196a-120">Чтобы оценить различные выражения, если первое выражение имеет значение false, щелкните **Добавить Else If** для вставки необязательно блок **Else If** .</span><span class="sxs-lookup"><span data-stu-id="f196a-120">To evaluate a different expression when the first expression is false, you can click **Add Else If** to insert an optional **Else If** block.</span></span> <span data-ttu-id="f196a-121">Необходимо ввести выражение, которое оценивается как True или False.</span><span class="sxs-lookup"><span data-stu-id="f196a-121">You must enter an expression that evaluates to True or False.</span></span> <span data-ttu-id="f196a-122">В этом случае блок выполняется только в том случае, если выражение имеет значение True и первое выражение имеет значение False.</span><span class="sxs-lookup"><span data-stu-id="f196a-122">In this case, the block executes only if the expression is True and the first expression is False.</span></span> 
  
<span data-ttu-id="f196a-123">Как вы, как в том случае, если блокировка можно добавить столько блоки **Else If** .</span><span class="sxs-lookup"><span data-stu-id="f196a-123">You can add as many **Else If** blocks as you like to an If block.</span></span> 
  
<span data-ttu-id="f196a-124">Щелкните **Добавить Else** для вставки блок **Else** необязательно.</span><span class="sxs-lookup"><span data-stu-id="f196a-124">You can click **Add Else** to insert an optional **Else** block.</span></span> <span data-ttu-id="f196a-125">В этом случае действия, которые можно вставить **Else** форм блок **Else** , который выполняет только в том случае, когда не следует действий, описанных выше.</span><span class="sxs-lookup"><span data-stu-id="f196a-125">In this case, the actions that you insert below the **Else** form the **Else** block, which executes only when the actions above do not.</span></span> <span data-ttu-id="f196a-126">**Если** блок можно добавить один блок **Else** .</span><span class="sxs-lookup"><span data-stu-id="f196a-126">You can add a single **Else** block to an **If** block.</span></span> 
  
<span data-ttu-id="f196a-127">В следующем примере кода макрокоманд в первый блок выполняется, если значение [Состояние] больше 0.</span><span class="sxs-lookup"><span data-stu-id="f196a-127">In the following code example, the macro actions in the first block execute if the value of [Status] is greater than 0.</span></span> <span data-ttu-id="f196a-128">Если значение [Состояние] не больше 0, исходя из **Else If** выражение.</span><span class="sxs-lookup"><span data-stu-id="f196a-128">If the value of [Status] is not greater than 0, the expression that follows the **Else If** is evaluated.</span></span> <span data-ttu-id="f196a-129">Действия макроса в блоке **Else If** выполняется, если значение [Состояние] равно 0.</span><span class="sxs-lookup"><span data-stu-id="f196a-129">The macro actions in the **Else If** block execute if the value of [Status] is equal to 0.</span></span> <span data-ttu-id="f196a-130">И, наконец Если первый блок ни второй блок выполнение, выполните действия в блоке **Else** .</span><span class="sxs-lookup"><span data-stu-id="f196a-130">Finally, if neither the first block nor the second block execute, the actions in the **Else** block execute.</span></span> 
  
```vb
If[Status] > 0Then 
 Insert macro actions here ... 
Else If[Status] = 0  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

<span data-ttu-id="f196a-131">**Если** блоки можно вкладывать.</span><span class="sxs-lookup"><span data-stu-id="f196a-131">You can nest **If** blocks.</span></span> <span data-ttu-id="f196a-132">Необходимо учитывать вложением блока **Если** блока **если** , чтобы оценить второго выражения, если первое выражение имеет значение True.</span><span class="sxs-lookup"><span data-stu-id="f196a-132">You should consider nesting an **If** block within an **If** block if you want to evaluate a second expression when the first expression is True.</span></span> <span data-ttu-id="f196a-133">В следующем примере кода внутреннего блока **If** выполняется, только когда значение [Состояние] больше 0 *и* больше 100.</span><span class="sxs-lookup"><span data-stu-id="f196a-133">In the following code example, the inner **If** block only executes when the value of [Status] is both greater than 0  *and*  greater than 100.</span></span> 
  

