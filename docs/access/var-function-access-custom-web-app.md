---
title: Функция ДИСП (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: Возвращает статистическую дисперсию для примера Генеральной совокупности, представленную в виде набора значений, содержащегося в указанном поле запроса.
ms.openlocfilehash: 80cea512b0386d9b0461c927675ae51be3e0dcda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437758"
---
# <a name="var-function-access-custom-web-app"></a><span data-ttu-id="2667d-103">Функция ДИСП (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="2667d-103">Var Function (Access custom web app)</span></span>

<span data-ttu-id="2667d-104">Возвращает статистическую дисперсию для примера Генеральной совокупности, представленную в виде набора значений, содержащегося в указанном поле запроса.</span><span class="sxs-lookup"><span data-stu-id="2667d-104">Returns the statistical variance for a population sample represented as a set of values contained in a specified field in a query.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="2667d-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="2667d-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="2667d-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="2667d-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2667d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2667d-107">Syntax</span></span>

 <span data-ttu-id="2667d-108">**Var** (*нумерицекспрессион*)</span><span class="sxs-lookup"><span data-stu-id="2667d-108">**Var** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="2667d-109">Функция **ДИСП** содержит следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="2667d-109">The **Var** function contains the following argument.</span></span> 
  
|<span data-ttu-id="2667d-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="2667d-110">**Argument name**</span></span>|<span data-ttu-id="2667d-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2667d-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2667d-112">*нумерицекспрессион*</span><span class="sxs-lookup"><span data-stu-id="2667d-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="2667d-113">Текстовое выражение, определяющее поле, содержащее числовые данные, которые необходимо оценить, или выражение, которое выполняет вычисления с использованием данных в этом поле.</span><span class="sxs-lookup"><span data-stu-id="2667d-113">A text expression identifying the field that contains the numeric data you want to evaluate or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="2667d-114">Операнды в *нумерицекспрессион* могут включать имя поля таблицы, константу или функцию (либо встроенную, либо определяемую пользователем, но не одну из других статистических функций SQL).</span><span class="sxs-lookup"><span data-stu-id="2667d-114">Operands in  *NumericExpression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2667d-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="2667d-115">Remarks</span></span>

 <span data-ttu-id="2667d-116">**Var** можно использовать только с числовыми столбцами.</span><span class="sxs-lookup"><span data-stu-id="2667d-116">**Var** can be used with numeric columns only.</span></span> <span data-ttu-id="2667d-117">Значения NULL игнорируются.</span><span class="sxs-lookup"><span data-stu-id="2667d-117">Null values are ignored.</span></span> 
  

