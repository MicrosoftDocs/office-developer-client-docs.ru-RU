---
title: If... Then... Else Macro Block (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 18d28dc1-c41f-47c6-b5c7-258d5f877d01
description: Вы можете использовать макроблок Если, чтобы выполнять группы макрокоманд в зависимости от значения выражения.
ms.openlocfilehash: 6fe82e2c42f8e5d93cdc26798e7572e32d6cdc7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434496"
---
# <a name="ifthenelse-macro-block-access-custom-web-app"></a><span data-ttu-id="77b6a-103">If... Then... Else Macro Block (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="77b6a-103">If...Then...Else Macro Block (Access custom web app)</span></span>

<span data-ttu-id="77b6a-104">Вы можете использовать макроблок **Если**, чтобы выполнять группы макрокоманд в зависимости от значения выражения.</span><span class="sxs-lookup"><span data-stu-id="77b6a-104">You can use the **If** macro block to conditionally execute a group of actions, depending on the value of an expression.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="77b6a-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="77b6a-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="77b6a-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="77b6a-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="77b6a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77b6a-107">Syntax</span></span>

```vb
IfexpressionThen 
 Insert macro actions here ... 
Else Ifexpression  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

## <a name="setting"></a><span data-ttu-id="77b6a-108">Setting</span><span class="sxs-lookup"><span data-stu-id="77b6a-108">Setting</span></span>

<span data-ttu-id="77b6a-109">Для **If** и \* \* Else If \* \* необходимо указать следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="77b6a-109">For both **If** and \*\* Else If \*\*, the following arguments are required.</span></span> 
  
|<span data-ttu-id="77b6a-110">**Аргумент макрокоманды**</span><span class="sxs-lookup"><span data-stu-id="77b6a-110">**Action argument**</span></span>|<span data-ttu-id="77b6a-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="77b6a-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="77b6a-112">**Expression**</span><span class="sxs-lookup"><span data-stu-id="77b6a-112">**Expression**</span></span> <br/> |<span data-ttu-id="77b6a-113">Условие, истинность которого должна проверяться.</span><span class="sxs-lookup"><span data-stu-id="77b6a-113">The condition that you wish to test.</span></span> <span data-ttu-id="77b6a-114">Принимает значение ИСТИНА или ЛОЖЬ.</span><span class="sxs-lookup"><span data-stu-id="77b6a-114">It must be an expression that evaluates to True or False.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77b6a-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="77b6a-115">Remarks</span></span>

<span data-ttu-id="77b6a-116">При выборе макроблока **Если** появляется поле для ввода выражения, представляющего собой условие, истинность которого будет в дальнейшем проверяться.</span><span class="sxs-lookup"><span data-stu-id="77b6a-116">When you select the **If** macro block, a textbox appears so that you can enter an expression that represents the condition you wish to test.</span></span> <span data-ttu-id="77b6a-117">Кроме того, доступно поле со списком, в которое можно добавить макрокоманду. Под ним автоматически отображается текст "Конец блока "Если"</span><span class="sxs-lookup"><span data-stu-id="77b6a-117">In addition, a combo box appears where you can insert a macro action, below which the text "End If" automatically displays.</span></span> <span data-ttu-id="77b6a-118">Поля "Если" и "Конец блока "Если" ограничивают область, в которую можно добавить группу (блок) макрокоманд.</span><span class="sxs-lookup"><span data-stu-id="77b6a-118">The If and the End If bracket an area in which you can enter a group, or block, of actions.</span></span> <span data-ttu-id="77b6a-119">Макрокоманды блока будут выполнены лишь в случае, если введенное выражение примет значение ИСТИНА.</span><span class="sxs-lookup"><span data-stu-id="77b6a-119">The block executes only if the expression that you enter is True.</span></span> 
  
<span data-ttu-id="77b6a-120">Для проверки истинности другого выражения в случае ложности первого вы можете выбрать команду **Добавить блок "Иначе если"**, чтобы вставить необязательный блок **Иначе если**.</span><span class="sxs-lookup"><span data-stu-id="77b6a-120">To evaluate a different expression when the first expression is false, you can click **Add Else If** to insert an optional **Else If** block.</span></span> <span data-ttu-id="77b6a-121">Необходимо ввести выражение, принимающее значение ИСТИНА или ЛОЖЬ.</span><span class="sxs-lookup"><span data-stu-id="77b6a-121">You must enter an expression that evaluates to True or False.</span></span> <span data-ttu-id="77b6a-122">Добавленный блок будет выполнен только в случае истинности этого выражения и ложности первого.</span><span class="sxs-lookup"><span data-stu-id="77b6a-122">In this case, the block executes only if the expression is True and the first expression is False.</span></span> 
  
<span data-ttu-id="77b6a-123">К блоку "Если" можно добавить любое число блоков **Иначе если**.</span><span class="sxs-lookup"><span data-stu-id="77b6a-123">You can add as many **Else If** blocks as you like to an If block.</span></span> 
  
<span data-ttu-id="77b6a-124">Вы можете выбрать команду **Добавить блок "Иначе"**, чтобы вставить необязательный блок **Иначе**.</span><span class="sxs-lookup"><span data-stu-id="77b6a-124">You can click **Add Else** to insert an optional **Else** block.</span></span> <span data-ttu-id="77b6a-125">В этом случае макрокоманды, добавленные под формой **Иначе**, сформируют блок **Иначе**, который будет выполнен только в случае ложности выражений в блоках "Если" и "Иначе если".</span><span class="sxs-lookup"><span data-stu-id="77b6a-125">In this case, the actions that you insert below the **Else** form the **Else** block, which executes only when the actions above do not.</span></span> <span data-ttu-id="77b6a-126">К каждому блоку **Если** можно добавить один блок **Иначе**.</span><span class="sxs-lookup"><span data-stu-id="77b6a-126">You can add a single **Else** block to an **If** block.</span></span> 
  
<span data-ttu-id="77b6a-127">В следующем примере кода макрокоманды в первом блоке выполняются, если значение [Status] больше 0.</span><span class="sxs-lookup"><span data-stu-id="77b6a-127">In the following code example, the macro actions in the first block execute if the value of [Status] is greater than 0.</span></span> <span data-ttu-id="77b6a-128">Если значение [Status] не больше 0, вычисляется выражение, следующее за знаком **Else If** .</span><span class="sxs-lookup"><span data-stu-id="77b6a-128">If the value of [Status] is not greater than 0, the expression that follows the **Else If** is evaluated.</span></span> <span data-ttu-id="77b6a-129">Макрокоманды в блоке **Else If** выполняются, если значение параметра [Status] равно 0.</span><span class="sxs-lookup"><span data-stu-id="77b6a-129">The macro actions in the **Else If** block execute if the value of [Status] is equal to 0.</span></span> <span data-ttu-id="77b6a-130">Наконец, если ложны выражения как в первом, так и во втором блоке, выполняются макрокоманды блока **Иначе**.</span><span class="sxs-lookup"><span data-stu-id="77b6a-130">Finally, if neither the first block nor the second block execute, the actions in the **Else** block execute.</span></span> 
  
```vb
If[Status] > 0Then 
 Insert macro actions here ... 
Else If[Status] = 0  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

<span data-ttu-id="77b6a-131">Вы можете вкладывать блоки **Если** друг в друга.</span><span class="sxs-lookup"><span data-stu-id="77b6a-131">You can nest **If** blocks.</span></span> <span data-ttu-id="77b6a-132">Один блок **Если** можно вложить в другой, если в случае истинности первого выражения нужно оценить второе.</span><span class="sxs-lookup"><span data-stu-id="77b6a-132">You should consider nesting an **If** block within an **If** block if you want to evaluate a second expression when the first expression is True.</span></span> <span data-ttu-id="77b6a-133">В приведенном ниже примере кода внутренний блок **If** выполняется только в том случае, если значение [Status] больше 0 *и* больше 100.</span><span class="sxs-lookup"><span data-stu-id="77b6a-133">In the following code example, the inner **If** block only executes when the value of [Status] is both greater than 0  *and*  greater than 100.</span></span> 
  

