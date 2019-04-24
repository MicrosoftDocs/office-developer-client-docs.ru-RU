---
title: Макрокоманда SetLocalVar (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 12444313-1cfa-49ff-89da-3030fe75c13e
description: Действие SetLocalVar создает временную переменную и присваивает ей определенное значение.
ms.openlocfilehash: 2493bc5c908c551e171a8fa7d9eaeea699a04f72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310947"
---
# <a name="setlocalvar-macro-action-access-custom-web-app"></a><span data-ttu-id="001ca-103">Макрокоманда SetLocalVar (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="001ca-103">SetLocalVar Macro Action (Access custom web app)</span></span>

<span data-ttu-id="001ca-104">Действие **SetLocalVar** создает временную переменную и присваивает ей определенное значение.</span><span class="sxs-lookup"><span data-stu-id="001ca-104">The **SetLocalVar** action creates a temporary variable and set it to a specific value.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="001ca-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="001ca-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="001ca-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="001ca-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="001ca-107">Действие **SetLocalVar** доступно только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="001ca-107">The **SetLocalVar** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="001ca-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="001ca-108">Setting</span></span>

<span data-ttu-id="001ca-109">Действие **GoToControl** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="001ca-109">The **SetLocalVar** action has the following arguments.</span></span> 
  
|<span data-ttu-id="001ca-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="001ca-110">**Argument name**</span></span>|<span data-ttu-id="001ca-111">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="001ca-111">**Required**</span></span>|<span data-ttu-id="001ca-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="001ca-112">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="001ca-113">**Name**</span><span class="sxs-lookup"><span data-stu-id="001ca-113">**Name**</span></span> <br/> |<span data-ttu-id="001ca-114">Да</span><span class="sxs-lookup"><span data-stu-id="001ca-114">Yes</span></span>  <br/> |<span data-ttu-id="001ca-115">Строка, определяющая имя переменной.</span><span class="sxs-lookup"><span data-stu-id="001ca-115">A string that specifies the name of the variable.</span></span>  <br/> |
|<span data-ttu-id="001ca-116">**Expression**</span><span class="sxs-lookup"><span data-stu-id="001ca-116">**Expression**</span></span> <br/> |<span data-ttu-id="001ca-117">Да</span><span class="sxs-lookup"><span data-stu-id="001ca-117">Yes</span></span>  <br/> |<span data-ttu-id="001ca-118">Выражение, которое будет использоваться для задания значений для данной временной переменной.</span><span class="sxs-lookup"><span data-stu-id="001ca-118">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="001ca-119">Не ставьте перед выражением знак равенства (=).</span><span class="sxs-lookup"><span data-stu-id="001ca-119">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="001ca-120">Вы можете нажать кнопку **Build**, чтобы использовать **Создатель выражений** для установки данного аргумента.</span><span class="sxs-lookup"><span data-stu-id="001ca-120">You can click the **Build** button to use the **Expression Builder** to set this argument.</span></span>  <br/> |
   

