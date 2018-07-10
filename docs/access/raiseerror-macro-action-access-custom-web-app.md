---
title: Действия макроса RaiseError (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5e29bf64-300a-4094-82ff-664e79782d86
description: Действие RaiseError Отображает всплывающее окно, содержащий указанное сообщение об ошибке.
ms.openlocfilehash: 1176804106c5cfd9d4bd30f79f47975593089dbc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807098"
---
# <a name="raiseerror-macro-action-access-custom-web-app"></a><span data-ttu-id="9f7cf-103">Действия макроса RaiseError (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="9f7cf-103">RaiseError Macro Action (Access custom web app)</span></span>

<span data-ttu-id="9f7cf-104">Действие **RaiseError** Отображает всплывающее окно, содержащий указанное сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9f7cf-104">The **RaiseError** action displays a popup window that contains a specified error message.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="9f7cf-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="9f7cf-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="9f7cf-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="9f7cf-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9f7cf-107">Действие **RaiseError** доступна только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="9f7cf-107">The **RaiseError** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="9f7cf-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="9f7cf-108">Setting</span></span>

<span data-ttu-id="9f7cf-109">Действие **RaiseError** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="9f7cf-109">The **RaiseError** action has the following argument.</span></span> 
  
|<span data-ttu-id="9f7cf-110">**Аргумент**</span><span class="sxs-lookup"><span data-stu-id="9f7cf-110">**Argument**</span></span>|<span data-ttu-id="9f7cf-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9f7cf-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="9f7cf-112">_Описание ошибки_</span><span class="sxs-lookup"><span data-stu-id="9f7cf-112">_Error Description_</span></span> <br/> |<span data-ttu-id="9f7cf-113">Строковое выражение, описывающее ошибку.</span><span class="sxs-lookup"><span data-stu-id="9f7cf-113">A string expression that describes the error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f7cf-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="9f7cf-114">Remarks</span></span>

<span data-ttu-id="9f7cf-115">При вызове действие **RaiseError** все операции в текущей операции будет выполнен откат.</span><span class="sxs-lookup"><span data-stu-id="9f7cf-115">When the **RaiseError** action is called, all of the operations in the current transaction are rolled back.</span></span> 
  

