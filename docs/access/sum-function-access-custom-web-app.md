---
title: Функция Sum (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: Возвращает сумму всех значений в выражении.
ms.openlocfilehash: b0fed86469b32ddcc7f60a388f5d42c7bbd48b6c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427103"
---
# <a name="sum-function-access-custom-web-app"></a><span data-ttu-id="414db-103">Функция Sum (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="414db-103">Sum Function (Access custom web app)</span></span>

<span data-ttu-id="414db-104">Возвращает сумму всех значений в выражении.</span><span class="sxs-lookup"><span data-stu-id="414db-104">Returns the sum of all the values in the expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="414db-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="414db-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="414db-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="414db-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="414db-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="414db-107">Syntax</span></span>

 <span data-ttu-id="414db-108">**Sum (сумма** ) (*Нумерицекспрессион*)</span><span class="sxs-lookup"><span data-stu-id="414db-108">**Sum** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="414db-109">Функция **Sum** содержит следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="414db-109">The **Sum** function contains the following argument.</span></span> 
  
|<span data-ttu-id="414db-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="414db-110">**Argument name**</span></span>|<span data-ttu-id="414db-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="414db-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="414db-112">*Нумерицекспрессион*</span><span class="sxs-lookup"><span data-stu-id="414db-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="414db-113">Выражение, определяющее поле, содержащее числовые данные, которые требуется добавить, или выражение, которое выполняет вычисления с использованием данных в этом поле.</span><span class="sxs-lookup"><span data-stu-id="414db-113">An expression identifying the field that contains the numeric data you want to add or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="414db-114">Операнды в *нумерицекспрессион* могут включать имя поля таблицы, константу или функцию (либо встроенную, либо определяемую пользователем, но не одну из других статистических функций SQL).</span><span class="sxs-lookup"><span data-stu-id="414db-114">Operands in  *NumericExpression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="414db-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="414db-115">Remarks</span></span>

<span data-ttu-id="414db-116">Функция **Sum** игнорирует записи, содержащие значения NULL.</span><span class="sxs-lookup"><span data-stu-id="414db-116">The **Sum** function ignores records that contain Null values.</span></span> 
  
<span data-ttu-id="414db-117">Функцию **Sum** можно использовать только с числовыми столбцами.</span><span class="sxs-lookup"><span data-stu-id="414db-117">The **Sum** function can only be used with numeric columns.</span></span> 
  

