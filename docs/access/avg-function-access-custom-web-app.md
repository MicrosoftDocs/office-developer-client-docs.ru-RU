---
title: Функция AVG (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: Вычисляет геометрического набор значений, содержащихся в указанном поле.
ms.openlocfilehash: afe832a51fc9cd3b224087a0b06fe539f6a7004b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806946"
---
# <a name="avg-function-access-custom-web-app"></a><span data-ttu-id="19448-103">Функция AVG (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="19448-103">Avg Function (Access custom web app)</span></span>

<span data-ttu-id="19448-104">Вычисляет геометрического набор значений, содержащихся в указанном поле.</span><span class="sxs-lookup"><span data-stu-id="19448-104">Calculates the arithmetic mean of a set of values contained in a specified field.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="19448-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="19448-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="19448-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="19448-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="19448-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19448-107">Syntax</span></span>

 <span data-ttu-id="19448-108">**Avg** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="19448-108">**Avg** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="19448-109">Функция **Avg** содержит следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="19448-109">The **Avg** function contains the following argument.</span></span> 
  
|<span data-ttu-id="19448-110">**Аргумент**</span><span class="sxs-lookup"><span data-stu-id="19448-110">**Argument**</span></span>|<span data-ttu-id="19448-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="19448-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="19448-112">NumericExpression</span><span class="sxs-lookup"><span data-stu-id="19448-112">NumericExpression</span></span>  <br/> |<span data-ttu-id="19448-113">Строковое выражение, определяющее поле, которое содержит числовые данные необходимо среднее число или выражение, которое выполняет вычисления с использованием данных для этого поля.</span><span class="sxs-lookup"><span data-stu-id="19448-113">A string expression identifying the field that contains the numeric data you want to average or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="19448-114">Операнды в *NumericExpression* может включать имя поля в таблице, переменной или функция (это может быть встроенным или определяемым пользователем, но не в одной из других статистические функции SQL).</span><span class="sxs-lookup"><span data-stu-id="19448-114">Operands in  *NumericExpression*  can include the name of a table field, a variable, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19448-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="19448-115">Remarks</span></span>

<span data-ttu-id="19448-116">Среднее значение, полученное с **Avg** — это геометрического (суммарный размер значения, разделенная на число значений).</span><span class="sxs-lookup"><span data-stu-id="19448-116">The average calculated by **Avg** is the arithmetic mean (the sum of the values divided by the number of values).</span></span> <span data-ttu-id="19448-117">**Avg**, например, можно использовать для вычисления себестоимости среднее доставки.</span><span class="sxs-lookup"><span data-stu-id="19448-117">You could use **Avg**, for example, to calculate average freight cost.</span></span> 
  
<span data-ttu-id="19448-118">Функция **Avg** не включает все **пустые** значения в расчет.</span><span class="sxs-lookup"><span data-stu-id="19448-118">The **Avg** function does not include any **Null** values in the calculation.</span></span> 
  

