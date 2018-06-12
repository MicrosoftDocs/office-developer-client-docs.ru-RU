---
title: Функция рэнд (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6390b325-025e-4546-bb19-1cd1c45ceb5a
description: Возвращает псевдослучайное число от 0 до 1.
ms.openlocfilehash: ed0f9991b2b1d9553d6d45524d6b1e4e5321ea7e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807095"
---
# <a name="rand-function-access-custom-web-app"></a><span data-ttu-id="ad905-103">Функция рэнд (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="ad905-103">Rand Function (Access custom web app)</span></span>

<span data-ttu-id="ad905-104">Возвращает псевдослучайное число от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="ad905-104">Returns a pseudo-random number between 0 and 1.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ad905-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ad905-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="ad905-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="ad905-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ad905-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad905-107">Syntax</span></span>

 <span data-ttu-id="ad905-108">**Рэнд** ([ *Начального значения* ])</span><span class="sxs-lookup"><span data-stu-id="ad905-108">**Rand** ( [  *Seed*  ])</span></span> 
  
<span data-ttu-id="ad905-109">Функция **рэнд** содержит следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="ad905-109">The **Rand** function contains the following argument.</span></span> 
  
|<span data-ttu-id="ad905-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="ad905-110">**Argument name**</span></span>|<span data-ttu-id="ad905-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ad905-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ad905-112">*Seed*</span><span class="sxs-lookup"><span data-stu-id="ad905-112">*Seed*</span></span>  <br/> |<span data-ttu-id="ad905-113">Целочисленное выражение, которое задает начальное значение.</span><span class="sxs-lookup"><span data-stu-id="ad905-113">An integer expression that gives the seed value.</span></span> <span data-ttu-id="ad905-114">Если *Начальное* значение не указано, начальное значение назначается в произвольном порядке.</span><span class="sxs-lookup"><span data-stu-id="ad905-114">If  *Seed*  is not specified, a seed value is assigned at random.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad905-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="ad905-115">Remarks</span></span>

<span data-ttu-id="ad905-116">Повторные вызовы функции **рэнд** с того же начального значения возвращает одинаковые результаты.</span><span class="sxs-lookup"><span data-stu-id="ad905-116">Repetitive calls of the **Rand** function with the same seed return the same results.</span></span> 
  

