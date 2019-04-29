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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408245"
---
# <a name="raiseerror-macro-action-access-custom-web-app"></a><span data-ttu-id="b6b88-103">Макрокоманда Раисиррор (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="b6b88-103">RaiseError Macro Action (Access custom web app)</span></span>

<span data-ttu-id="b6b88-104">Действие **раисиррор** отображает всплывающее окно, содержащее указанное сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="b6b88-104">The **RaiseError** action displays a popup window that contains a specified error message.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="b6b88-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="b6b88-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="b6b88-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="b6b88-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b6b88-107">Действие **раисиррор** доступно только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="b6b88-107">The **RaiseError** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="b6b88-108">Setting</span><span class="sxs-lookup"><span data-stu-id="b6b88-108">Setting</span></span>

<span data-ttu-id="b6b88-109">Действие **раисиррор** имеет следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="b6b88-109">The **RaiseError** action has the following argument.</span></span> 
  
|<span data-ttu-id="b6b88-110">**Аргумент**</span><span class="sxs-lookup"><span data-stu-id="b6b88-110">**Argument**</span></span>|<span data-ttu-id="b6b88-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b6b88-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b6b88-112">_Описание ошибки_</span><span class="sxs-lookup"><span data-stu-id="b6b88-112">_Error Description_</span></span> <br/> |<span data-ttu-id="b6b88-113">Строковое выражение, описывающее ошибку.</span><span class="sxs-lookup"><span data-stu-id="b6b88-113">A string expression that describes the error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6b88-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="b6b88-114">Remarks</span></span>

<span data-ttu-id="b6b88-115">При вызове действия **раисиррор** выполняется откат всех операций в текущей транзакции.</span><span class="sxs-lookup"><span data-stu-id="b6b88-115">When the **RaiseError** action is called, all of the operations in the current transaction are rolled back.</span></span> 
  

