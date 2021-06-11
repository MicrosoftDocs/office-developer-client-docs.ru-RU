---
title: SetLocalVar Macro Action (Доступ к настраиваемой веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 12444313-1cfa-49ff-89da-3030fe75c13e
description: Действие SetLocalVar создает временную переменную и присваивает ей определенное значение.
ms.openlocfilehash: 2493bc5c908c551e171a8fa7d9eaeea699a04f72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428118"
---
# <a name="setlocalvar-macro-action-access-custom-web-app"></a><span data-ttu-id="5002d-103">SetLocalVar Macro Action (Доступ к настраиваемой веб-приложению)</span><span class="sxs-lookup"><span data-stu-id="5002d-103">SetLocalVar Macro Action (Access custom web app)</span></span>

<span data-ttu-id="5002d-104">Действие **SetLocalVar** создает временную переменную и присваивает ей определенное значение.</span><span class="sxs-lookup"><span data-stu-id="5002d-104">The **SetLocalVar** action creates a temporary variable and set it to a specific value.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="5002d-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5002d-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="5002d-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="5002d-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5002d-107">Действие **SetLocalVar** доступно только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="5002d-107">The **SetLocalVar** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="5002d-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="5002d-108">Setting</span></span>

<span data-ttu-id="5002d-109">Действие **GoToControl** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="5002d-109">The **SetLocalVar** action has the following arguments.</span></span> 
  
|<span data-ttu-id="5002d-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="5002d-110">**Argument name**</span></span>|<span data-ttu-id="5002d-111">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="5002d-111">**Required**</span></span>|<span data-ttu-id="5002d-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="5002d-112">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5002d-113">**Name**</span><span class="sxs-lookup"><span data-stu-id="5002d-113">**Name**</span></span> <br/> |<span data-ttu-id="5002d-114">Да</span><span class="sxs-lookup"><span data-stu-id="5002d-114">Yes</span></span>  <br/> |<span data-ttu-id="5002d-115">Строка, определяющая имя переменной.</span><span class="sxs-lookup"><span data-stu-id="5002d-115">A string that specifies the name of the variable.</span></span>  <br/> |
|<span data-ttu-id="5002d-116">**Expression**</span><span class="sxs-lookup"><span data-stu-id="5002d-116">**Expression**</span></span> <br/> |<span data-ttu-id="5002d-117">Да</span><span class="sxs-lookup"><span data-stu-id="5002d-117">Yes</span></span>  <br/> |<span data-ttu-id="5002d-118">Выражение, которое будет использоваться для задания значений для данной временной переменной.</span><span class="sxs-lookup"><span data-stu-id="5002d-118">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="5002d-119">Не ставьте перед выражением знак равенства (=).</span><span class="sxs-lookup"><span data-stu-id="5002d-119">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="5002d-120">Вы можете нажать кнопку **Build**, чтобы использовать **Создатель выражений** для установки данного аргумента.</span><span class="sxs-lookup"><span data-stu-id="5002d-120">You can click the **Build** button to use the **Expression Builder** to set this argument.</span></span>  <br/> |
   

