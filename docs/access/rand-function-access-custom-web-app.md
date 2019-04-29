---
title: Функция RAND (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6390b325-025e-4546-bb19-1cd1c45ceb5a
description: Возвращает псевдо — случайное число от 0 до 1.
ms.openlocfilehash: 02d914de9d74083a6ebf76f6d0e556fe51954a24
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416610"
---
# <a name="rand-function-access-custom-web-app"></a><span data-ttu-id="4c70d-103">Функция RAND (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="4c70d-103">Rand Function (Access custom web app)</span></span>

<span data-ttu-id="4c70d-104">Возвращает псевдо — случайное число от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="4c70d-104">Returns a pseudo-random number between 0 and 1.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="4c70d-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4c70d-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="4c70d-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="4c70d-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4c70d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c70d-107">Syntax</span></span>

 <span data-ttu-id="4c70d-108">**СЛЧИС** ([ *SEED* ])</span><span class="sxs-lookup"><span data-stu-id="4c70d-108">**Rand** ( [  *Seed*  ])</span></span> 
  
<span data-ttu-id="4c70d-109">Функция **Rand** содержит следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="4c70d-109">The **Rand** function contains the following argument.</span></span> 
  
|<span data-ttu-id="4c70d-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="4c70d-110">**Argument name**</span></span>|<span data-ttu-id="4c70d-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4c70d-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="4c70d-112">*Seed*</span><span class="sxs-lookup"><span data-stu-id="4c70d-112">*Seed*</span></span>  <br/> |<span data-ttu-id="4c70d-113">Целочисленное выражение, задающее начальное значение.</span><span class="sxs-lookup"><span data-stu-id="4c70d-113">An integer expression that gives the seed value.</span></span> <span data-ttu-id="4c70d-114">Если параметр *SEED* не указан, начальное значение присваивается случайным образом.</span><span class="sxs-lookup"><span data-stu-id="4c70d-114">If  *Seed*  is not specified, a seed value is assigned at random.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c70d-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="4c70d-115">Remarks</span></span>

<span data-ttu-id="4c70d-116">Повторные вызовы функции **СЛЧИС** с одинаковым начальным значением возвращают одни и те же результаты.</span><span class="sxs-lookup"><span data-stu-id="4c70d-116">Repetitive calls of the **Rand** function with the same seed return the same results.</span></span> 
  

