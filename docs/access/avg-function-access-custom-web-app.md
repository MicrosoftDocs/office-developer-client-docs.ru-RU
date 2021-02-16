---
title: Avg Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: Вычисляет арифметическое значение набора значений, содержащихся в указанном поле.
ms.openlocfilehash: e67cde12e66f943d3b25fe9cb2fee4fe4aea760f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426725"
---
# <a name="avg-function-access-custom-web-app"></a><span data-ttu-id="25030-103">Avg Function (Access custom web app)</span><span class="sxs-lookup"><span data-stu-id="25030-103">Avg Function (Access custom web app)</span></span>

<span data-ttu-id="25030-104">Вычисляет арифметическое значение набора значений, содержащихся в указанном поле.</span><span class="sxs-lookup"><span data-stu-id="25030-104">Calculates the arithmetic mean of a set of values contained in a specified field.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="25030-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="25030-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="25030-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="25030-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="25030-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25030-107">Syntax</span></span>

 <span data-ttu-id="25030-108">**Avg** (*NumericExpression)*</span><span class="sxs-lookup"><span data-stu-id="25030-108">**Avg** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="25030-109">**Avg** function contains the following argument.</span><span class="sxs-lookup"><span data-stu-id="25030-109">The **Avg** function contains the following argument.</span></span> 
  
|<span data-ttu-id="25030-110">**Аргумент**</span><span class="sxs-lookup"><span data-stu-id="25030-110">**Argument**</span></span>|<span data-ttu-id="25030-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="25030-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="25030-112">NumericExpression</span><span class="sxs-lookup"><span data-stu-id="25030-112">NumericExpression</span></span>  <br/> |<span data-ttu-id="25030-113">Строковая выражение, определяющие поле, которое содержит числовую информацию, которую вы хотите усреднить, или выражение, которое выполняет вычисление с использованием данных в этом поле.</span><span class="sxs-lookup"><span data-stu-id="25030-113">A string expression identifying the field that contains the numeric data you want to average or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="25030-114">Операнды в  *NumericExpression*  могут включать имя поля таблицы, переменной или функции (которая может быть внутренней или определяемой пользователем, но не одной из других SQL агрегатных функций).</span><span class="sxs-lookup"><span data-stu-id="25030-114">Operands in  *NumericExpression*  can include the name of a table field, a variable, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25030-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="25030-115">Remarks</span></span>

<span data-ttu-id="25030-116">Среднее значение, вычисляемого **avg,** — это арифметическое среднее (сумма значений, разделенных на число значений).</span><span class="sxs-lookup"><span data-stu-id="25030-116">The average calculated by **Avg** is the arithmetic mean (the sum of the values divided by the number of values).</span></span> <span data-ttu-id="25030-117">Вы можете использовать **avg, например,** для расчета средней стоимости затрат на затраты.</span><span class="sxs-lookup"><span data-stu-id="25030-117">You could use **Avg**, for example, to calculate average freight cost.</span></span> 
  
<span data-ttu-id="25030-118">**Avg** function does not include any **Null** values in the calculation.</span><span class="sxs-lookup"><span data-stu-id="25030-118">The **Avg** function does not include any **Null** values in the calculation.</span></span> 
  

