---
title: RaiseError Macro Action (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5e29bf64-300a-4094-82ff-664e79782d86
description: Действие RaiseError отображает всплывающее окно с указанным сообщением об ошибке.
ms.openlocfilehash: 49e544d2234759709c19052b5540d42e88070849
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408245"
---
# <a name="raiseerror-macro-action-access-custom-web-app"></a><span data-ttu-id="73b62-103">RaiseError Macro Action (пользовательское веб-приложение Access)</span><span class="sxs-lookup"><span data-stu-id="73b62-103">RaiseError Macro Action (Access custom web app)</span></span>

<span data-ttu-id="73b62-104">Действие **RaiseError** отображает всплывающее окно с указанным сообщением об ошибке.</span><span class="sxs-lookup"><span data-stu-id="73b62-104">The **RaiseError** action displays a popup window that contains a specified error message.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="73b62-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="73b62-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="73b62-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="73b62-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="73b62-107">Действие **RaiseError** доступно только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="73b62-107">The **RaiseError** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="73b62-108">Setting</span><span class="sxs-lookup"><span data-stu-id="73b62-108">Setting</span></span>

<span data-ttu-id="73b62-109">Действие **RaiseError** имеет следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="73b62-109">The **RaiseError** action has the following argument.</span></span> 
  
|<span data-ttu-id="73b62-110">**Аргумент**</span><span class="sxs-lookup"><span data-stu-id="73b62-110">**Argument**</span></span>|<span data-ttu-id="73b62-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="73b62-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="73b62-112">_Описание ошибки_</span><span class="sxs-lookup"><span data-stu-id="73b62-112">_Error Description_</span></span> <br/> |<span data-ttu-id="73b62-113">Строка выражения, описываемая ошибку.</span><span class="sxs-lookup"><span data-stu-id="73b62-113">A string expression that describes the error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73b62-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="73b62-114">Remarks</span></span>

<span data-ttu-id="73b62-115">При **вызывается действие RaiseError,** все операции в текущей транзакции откатываются.</span><span class="sxs-lookup"><span data-stu-id="73b62-115">When the **RaiseError** action is called, all of the operations in the current transaction are rolled back.</span></span> 
  

