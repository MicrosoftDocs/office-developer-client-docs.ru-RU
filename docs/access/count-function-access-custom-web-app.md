---
title: Функция счёт (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: Возвращает количество записей в запросе или таблице.
ms.openlocfilehash: 98dbed393bf2f6dc401119f6c5dc7ab6b5ff7864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282238"
---
# <a name="count-function-access-custom-web-app"></a><span data-ttu-id="200ff-103">Функция счёт (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="200ff-103">Count function (Access custom web app)</span></span>

<span data-ttu-id="200ff-104">Возвращает количество записей в запросе или таблице.</span><span class="sxs-lookup"><span data-stu-id="200ff-104">Returns the number of records in a query or table.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="200ff-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="200ff-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="200ff-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="200ff-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="200ff-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="200ff-107">Syntax</span></span>

<span data-ttu-id="200ff-108">**Count (количество** ) (*Expression*)</span><span class="sxs-lookup"><span data-stu-id="200ff-108">**Count** (*Expression*)</span></span> 
  
<span data-ttu-id="200ff-109">Функция **Count** содержит следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="200ff-109">The **Count** function contains the following argument.</span></span> 
  
|<span data-ttu-id="200ff-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="200ff-110">**Argument name**</span></span>|<span data-ttu-id="200ff-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="200ff-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="200ff-112">*Expression*</span><span class="sxs-lookup"><span data-stu-id="200ff-112">*Expression*</span></span>  <br/> |<span data-ttu-id="200ff-113">Строковое выражение, определяющее поле, содержащее данные, которые необходимо подсчитать, или выражение, которое выполняет вычисления с использованием данных в поле.</span><span class="sxs-lookup"><span data-stu-id="200ff-113">A string expression identifying the field that contains the data you want to count or an expression that performs a calculation using the data in the field.</span></span> <span data-ttu-id="200ff-114">Операнды в *выражении* могут включать имя поля или функции таблицы (как встроенные, так и пользовательские, но не другие статистические функции SQL).</span><span class="sxs-lookup"><span data-stu-id="200ff-114">Operands in  *Expression*  can include the name of a table field or function (which can be either intrinsic or user-defined but not other SQL aggregate functions).</span></span> <span data-ttu-id="200ff-115">Можно вычислять любой тип данных, включая текст.</span><span class="sxs-lookup"><span data-stu-id="200ff-115">You can count any kind of data, including text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="200ff-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="200ff-116">Remarks</span></span>

<span data-ttu-id="200ff-117">Чтобы вычислить количество записей в базовом запросе, можно использовать функцию Count.</span><span class="sxs-lookup"><span data-stu-id="200ff-117">You can use Count to count the number of records in an underlying query.</span></span> <span data-ttu-id="200ff-118">Например, можно использовать функцию Count для вычисления количества заказов, отправленных в определенную страну или регион.</span><span class="sxs-lookup"><span data-stu-id="200ff-118">For example, you could use Count to count the number of orders shipped to a particular country or region.</span></span>
  
<span data-ttu-id="200ff-119">**Count (количество** ) (\*) возвращает количество элементов в группе.</span><span class="sxs-lookup"><span data-stu-id="200ff-119">**Count** (\*) returns the number of items in a group.</span></span> <span data-ttu-id="200ff-120">Сюда входят значения NULL и дубликаты.</span><span class="sxs-lookup"><span data-stu-id="200ff-120">This includes NULL values and duplicates.</span></span> 
  

