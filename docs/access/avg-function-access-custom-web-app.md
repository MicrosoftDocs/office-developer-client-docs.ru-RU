---
title: Avg Function (Доступ к настраиваемой веб-приложению)
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
# <a name="avg-function-access-custom-web-app"></a><span data-ttu-id="188f0-103">Avg Function (Доступ к настраиваемой веб-приложению)</span><span class="sxs-lookup"><span data-stu-id="188f0-103">Avg Function (Access custom web app)</span></span>

<span data-ttu-id="188f0-104">Вычисляет арифметическое значение набора значений, содержащихся в указанном поле.</span><span class="sxs-lookup"><span data-stu-id="188f0-104">Calculates the arithmetic mean of a set of values contained in a specified field.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="188f0-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="188f0-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="188f0-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="188f0-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="188f0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="188f0-107">Syntax</span></span>

 <span data-ttu-id="188f0-108">**Avg** *(NumericExpression)*</span><span class="sxs-lookup"><span data-stu-id="188f0-108">**Avg** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="188f0-109">Функция **Avg** содержит следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="188f0-109">The **Avg** function contains the following argument.</span></span> 
  
|<span data-ttu-id="188f0-110">**Аргумент**</span><span class="sxs-lookup"><span data-stu-id="188f0-110">**Argument**</span></span>|<span data-ttu-id="188f0-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="188f0-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="188f0-112">NumericExpression</span><span class="sxs-lookup"><span data-stu-id="188f0-112">NumericExpression</span></span>  <br/> |<span data-ttu-id="188f0-113">Строковая экспрессия, определяемая поле, содержаще числимые данные, которые необходимо усреднить, или выражение, которое выполняет вычисление с помощью данных в этом поле.</span><span class="sxs-lookup"><span data-stu-id="188f0-113">A string expression identifying the field that contains the numeric data you want to average or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="188f0-114">Operands в *NumericExpression* может включать имя настольного поля, переменной или функции (которая может быть внутренней или пользовательской, но не одной из других SQL совокупных функций).</span><span class="sxs-lookup"><span data-stu-id="188f0-114">Operands in  *NumericExpression*  can include the name of a table field, a variable, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="188f0-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="188f0-115">Remarks</span></span>

<span data-ttu-id="188f0-116">Среднее значение, рассчитанное **Avg,** — это арифметическое значение (сумма значений, разделенных на количество значений).</span><span class="sxs-lookup"><span data-stu-id="188f0-116">The average calculated by **Avg** is the arithmetic mean (the sum of the values divided by the number of values).</span></span> <span data-ttu-id="188f0-117">Например, можно использовать **Avg** для расчета средней стоимости груза.</span><span class="sxs-lookup"><span data-stu-id="188f0-117">You could use **Avg**, for example, to calculate average freight cost.</span></span> 
  
<span data-ttu-id="188f0-118">Функция **Avg** не включает в расчет значения **Null.**</span><span class="sxs-lookup"><span data-stu-id="188f0-118">The **Avg** function does not include any **Null** values in the calculation.</span></span> 
  

