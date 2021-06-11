---
title: Функция sum (Доступ к настраиваемой веб-приложению)
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
# <a name="sum-function-access-custom-web-app"></a><span data-ttu-id="eac1b-103">Функция sum (Доступ к настраиваемой веб-приложению)</span><span class="sxs-lookup"><span data-stu-id="eac1b-103">Sum Function (Access custom web app)</span></span>

<span data-ttu-id="eac1b-104">Возвращает сумму всех значений в выражении.</span><span class="sxs-lookup"><span data-stu-id="eac1b-104">Returns the sum of all the values in the expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="eac1b-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="eac1b-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="eac1b-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="eac1b-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="eac1b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eac1b-107">Syntax</span></span>

 <span data-ttu-id="eac1b-108">**Sum** *(NumericExpression)*</span><span class="sxs-lookup"><span data-stu-id="eac1b-108">**Sum** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="eac1b-109">Функция **Sum** содержит следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="eac1b-109">The **Sum** function contains the following argument.</span></span> 
  
|<span data-ttu-id="eac1b-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="eac1b-110">**Argument name**</span></span>|<span data-ttu-id="eac1b-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="eac1b-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="eac1b-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="eac1b-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="eac1b-113">Выражение, определяющие поле, содержаще числимые данные, которые необходимо добавить, или выражение, которое выполняет вычисление с помощью данных в этом поле.</span><span class="sxs-lookup"><span data-stu-id="eac1b-113">An expression identifying the field that contains the numeric data you want to add or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="eac1b-114">Operands в *NumericExpression* может включать имя настольного поля, константы или функции (которая может быть внутренней или пользовательской, но не одной из других SQL совокупных функций).</span><span class="sxs-lookup"><span data-stu-id="eac1b-114">Operands in  *NumericExpression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eac1b-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="eac1b-115">Remarks</span></span>

<span data-ttu-id="eac1b-116">Функция **Sum** игнорирует записи, содержащие значения Null.</span><span class="sxs-lookup"><span data-stu-id="eac1b-116">The **Sum** function ignores records that contain Null values.</span></span> 
  
<span data-ttu-id="eac1b-117">Функцию **Sum** можно использовать только с числными столбцами.</span><span class="sxs-lookup"><span data-stu-id="eac1b-117">The **Sum** function can only be used with numeric columns.</span></span> 
  

