---
title: Макрокоманда Раисиррор (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5e29bf64-300a-4094-82ff-664e79782d86
description: Действие Раисиррор отображает всплывающее окно, содержащее указанное сообщение об ошибке.
ms.openlocfilehash: 49e544d2234759709c19052b5540d42e88070849
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308017"
---
# <a name="raiseerror-macro-action-access-custom-web-app"></a><span data-ttu-id="711a9-103">Макрокоманда Раисиррор (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="711a9-103">RaiseError Macro Action (Access custom web app)</span></span>

<span data-ttu-id="711a9-104">Действие **раисиррор** отображает всплывающее окно, содержащее указанное сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="711a9-104">The **RaiseError** action displays a popup window that contains a specified error message.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="711a9-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="711a9-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="711a9-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="711a9-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="711a9-107">Действие **раисиррор** доступно только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="711a9-107">The **RaiseError** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="711a9-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="711a9-108">Setting</span></span>

<span data-ttu-id="711a9-109">Действие **раисиррор** имеет следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="711a9-109">The **RaiseError** action has the following argument.</span></span> 
  
|<span data-ttu-id="711a9-110">**Аргумент**</span><span class="sxs-lookup"><span data-stu-id="711a9-110">**Argument**</span></span>|<span data-ttu-id="711a9-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="711a9-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="711a9-112">_Описание ошибки_</span><span class="sxs-lookup"><span data-stu-id="711a9-112">_Error Description_</span></span> <br/> |<span data-ttu-id="711a9-113">Строковое выражение, описывающее ошибку.</span><span class="sxs-lookup"><span data-stu-id="711a9-113">A string expression that describes the error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="711a9-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="711a9-114">Remarks</span></span>

<span data-ttu-id="711a9-115">При вызове действия **раисиррор** выполняется откат всех операций в текущей транзакции.</span><span class="sxs-lookup"><span data-stu-id="711a9-115">When the **RaiseError** action is called, all of the operations in the current transaction are rolled back.</span></span> 
  

