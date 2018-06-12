---
title: Функция var (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: Возвращает дисперсию для совокупности, представленные в виде набор значений, содержащихся в указанном поле в запросе.
ms.openlocfilehash: 9937f1985c0a7df5eb06977333ab889947891380
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807139"
---
# <a name="var-function-access-custom-web-app"></a><span data-ttu-id="2f958-103">Функция var (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="2f958-103">Var Function (Access custom web app)</span></span>

<span data-ttu-id="2f958-104">Возвращает дисперсию для совокупности, представленные в виде набор значений, содержащихся в указанном поле в запросе.</span><span class="sxs-lookup"><span data-stu-id="2f958-104">Returns the statistical variance for a population sample represented as a set of values contained in a specified field in a query.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="2f958-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="2f958-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="2f958-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="2f958-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2f958-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f958-107">Syntax</span></span>

 <span data-ttu-id="2f958-108">**Var** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="2f958-108">**Var** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="2f958-109">Функция **Var** содержит следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="2f958-109">The **Var** function contains the following argument.</span></span> 
  
|<span data-ttu-id="2f958-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="2f958-110">**Argument name**</span></span>|<span data-ttu-id="2f958-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2f958-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2f958-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="2f958-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="2f958-113">Текст выражение, определяющее поле, содержащее числовые данные, которые необходимо оценить или выражение, которое выполняет вычисления с использованием данных для этого поля.</span><span class="sxs-lookup"><span data-stu-id="2f958-113">A text expression identifying the field that contains the numeric data you want to evaluate or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="2f958-114">Операнды в *NumericExpression* может включать имя поля в таблице, константа или функция (это может быть встроенным или определяемым пользователем, но не в одной из других статистические функции SQL).</span><span class="sxs-lookup"><span data-stu-id="2f958-114">Operands in  *NumericExpression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f958-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="2f958-115">Remarks</span></span>

 <span data-ttu-id="2f958-116">**Var** можно использовать только для числовых столбцов.</span><span class="sxs-lookup"><span data-stu-id="2f958-116">**Var** can be used with numeric columns only.</span></span> <span data-ttu-id="2f958-117">Пустые значения игнорируются.</span><span class="sxs-lookup"><span data-stu-id="2f958-117">Null values are ignored.</span></span> 
  

