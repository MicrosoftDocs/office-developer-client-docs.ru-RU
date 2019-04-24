---
title: Функция AVG (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: Вычисляет среднее арифметическое набора значений, содержащегося в указанном поле.
ms.openlocfilehash: e67cde12e66f943d3b25fe9cb2fee4fe4aea760f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282336"
---
# <a name="avg-function-access-custom-web-app"></a><span data-ttu-id="dd92a-103">Функция AVG (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="dd92a-103">Avg Function (Access custom web app)</span></span>

<span data-ttu-id="dd92a-104">Вычисляет среднее арифметическое набора значений, содержащегося в указанном поле.</span><span class="sxs-lookup"><span data-stu-id="dd92a-104">Calculates the arithmetic mean of a set of values contained in a specified field.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="dd92a-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="dd92a-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="dd92a-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="dd92a-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="dd92a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd92a-107">Syntax</span></span>

 <span data-ttu-id="dd92a-108">**AVG** (*Нумерицекспрессион*)</span><span class="sxs-lookup"><span data-stu-id="dd92a-108">**Avg** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="dd92a-109">Функция **AVG** содержит следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="dd92a-109">The **Avg** function contains the following argument.</span></span> 
  
|<span data-ttu-id="dd92a-110">**Аргумент**</span><span class="sxs-lookup"><span data-stu-id="dd92a-110">**Argument**</span></span>|<span data-ttu-id="dd92a-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dd92a-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dd92a-112">Нумерицекспрессион</span><span class="sxs-lookup"><span data-stu-id="dd92a-112">NumericExpression</span></span>  <br/> |<span data-ttu-id="dd92a-113">Строковое выражение, определяющее поле, содержащее числовые данные, которые требуется усреднить, или выражение, которое выполняет вычисления с использованием данных в этом поле.</span><span class="sxs-lookup"><span data-stu-id="dd92a-113">A string expression identifying the field that contains the numeric data you want to average or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="dd92a-114">Операнды в *нумерицекспрессион* могут включать имя поля таблицы, переменной или функции (как встроенных, так и определенных пользователем, но не одной из других статистических функций SQL).</span><span class="sxs-lookup"><span data-stu-id="dd92a-114">Operands in  *NumericExpression*  can include the name of a table field, a variable, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd92a-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="dd92a-115">Remarks</span></span>

<span data-ttu-id="dd92a-116">Среднее арифметическое вычисление вычисляет среднее арифметическое значение (сумма значений, деленная на количество значений). \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="dd92a-116">The average calculated by **Avg** is the arithmetic mean (the sum of the values divided by the number of values).</span></span> <span data-ttu-id="dd92a-117">Можно использовать **AVG**, например, для вычисления средней стоимости доставки.</span><span class="sxs-lookup"><span data-stu-id="dd92a-117">You could use **Avg**, for example, to calculate average freight cost.</span></span> 
  
<span data-ttu-id="dd92a-118">Функция **AVG** не включает значения **null** в вычисление.</span><span class="sxs-lookup"><span data-stu-id="dd92a-118">The **Avg** function does not include any **Null** values in the calculation.</span></span> 
  

