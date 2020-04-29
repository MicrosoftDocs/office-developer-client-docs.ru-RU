---
title: Макрокоманда SetReturnVar (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: Действие SetReturnVar создает переменную возврата и присваивает ей определенное значение.
ms.openlocfilehash: 29445f5021bed99fe45cee1d34457f1f91ca417d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409596"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a><span data-ttu-id="4176d-103">Макрокоманда SetReturnVar (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="4176d-103">SetReturnVar Macro action (Access custom web app)</span></span>

<span data-ttu-id="4176d-104">Действие **SetReturnVar** создает переменную возврата и присваивает ей определенное значение.</span><span class="sxs-lookup"><span data-stu-id="4176d-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="4176d-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4176d-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="4176d-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="4176d-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4176d-107">Действие **SetReturnVar** доступно только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="4176d-107">The **SetReturnVar** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="4176d-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="4176d-108">Setting</span></span>

<span data-ttu-id="4176d-109">Макрокоманда **SetReturnVar** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="4176d-109">The **SetReturnVar** action has the following arguments.</span></span> 
  
|<span data-ttu-id="4176d-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="4176d-110">**Argument name**</span></span>|<span data-ttu-id="4176d-111">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="4176d-111">**Required**</span></span>|<span data-ttu-id="4176d-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="4176d-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="4176d-113">_Name_</span><span class="sxs-lookup"><span data-stu-id="4176d-113">_Name_</span></span> <br/> |<span data-ttu-id="4176d-114">Да</span><span class="sxs-lookup"><span data-stu-id="4176d-114">Yes</span></span>  <br/> |<span data-ttu-id="4176d-115">Строка, определяющая имя переменной.</span><span class="sxs-lookup"><span data-stu-id="4176d-115">A string that specifies the name of the variable.</span></span>  <br/> |
| <span data-ttu-id="4176d-116">_Expression_</span><span class="sxs-lookup"><span data-stu-id="4176d-116">_Expression_</span></span> <br/> |<span data-ttu-id="4176d-117">Да</span><span class="sxs-lookup"><span data-stu-id="4176d-117">Yes</span></span>  <br/> |<span data-ttu-id="4176d-118">Выражение, которое будет использоваться для задания значений для данной временной переменной.</span><span class="sxs-lookup"><span data-stu-id="4176d-118">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="4176d-119">Не ставьте перед выражением знак равенства (=).</span><span class="sxs-lookup"><span data-stu-id="4176d-119">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="4176d-120">Вы можете нажать кнопку **Build**, чтобы использовать **Создатель выражений** для установки данного аргумента.</span><span class="sxs-lookup"><span data-stu-id="4176d-120">You can click the **Build** button to use the **Expression Builder** to set this argument.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4176d-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4176d-121">Remarks</span></span>

<span data-ttu-id="4176d-122">Действие **SetReturnVar** используется для создания **ReturnVar**, который представляет собой переменную, которая может использоваться макросами, вызывающими макросы данных с помощью действия **RunDataMacro** .</span><span class="sxs-lookup"><span data-stu-id="4176d-122">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span> 
  
<span data-ttu-id="4176d-123">После создания **ReturnVar** действием **SetReturnVar** вызывающий макрос может использовать его в выражении.</span><span class="sxs-lookup"><span data-stu-id="4176d-123">After a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression.</span></span> <span data-ttu-id="4176d-124">Например, если вы создали **ReturnVar** с именем **упдатесукцесс**, вы можете использовать переменную с помощью следующего синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="4176d-124">For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>
  
`=[ReturnVars]![UpdateSuccess]`

<span data-ttu-id="4176d-125">Действие **SetReturnVar** можно использовать только в именованных макросах данных.</span><span class="sxs-lookup"><span data-stu-id="4176d-125">The **SetReturnVar** action can be used only in named data macros.</span></span> <span data-ttu-id="4176d-126">Она недоступна в макросах данных, вложенных в событие макросов данных.</span><span class="sxs-lookup"><span data-stu-id="4176d-126">It is not available in data macros that are attached to a data macro event.</span></span> 
  

