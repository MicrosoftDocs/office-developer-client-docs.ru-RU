---
title: Функция count (Доступ к настраиваемой веб-приложении)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: Возвращает количество записей в запросе или таблице.
ms.openlocfilehash: 98dbed393bf2f6dc401119f6c5dc7ab6b5ff7864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419144"
---
# <a name="count-function-access-custom-web-app"></a><span data-ttu-id="bb184-103">Функция count (Доступ к настраиваемой веб-приложении)</span><span class="sxs-lookup"><span data-stu-id="bb184-103">Count function (Access custom web app)</span></span>

<span data-ttu-id="bb184-104">Возвращает количество записей в запросе или таблице.</span><span class="sxs-lookup"><span data-stu-id="bb184-104">Returns the number of records in a query or table.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="bb184-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="bb184-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="bb184-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="bb184-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="bb184-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb184-107">Syntax</span></span>

<span data-ttu-id="bb184-108">**Count** *(Expression)*</span><span class="sxs-lookup"><span data-stu-id="bb184-108">**Count** (*Expression*)</span></span> 
  
<span data-ttu-id="bb184-109">Функция **Count** содержит следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="bb184-109">The **Count** function contains the following argument.</span></span> 
  
|<span data-ttu-id="bb184-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="bb184-110">**Argument name**</span></span>|<span data-ttu-id="bb184-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bb184-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="bb184-112">*Expression*</span><span class="sxs-lookup"><span data-stu-id="bb184-112">*Expression*</span></span>  <br/> |<span data-ttu-id="bb184-113">Строковая экспрессия, определяемая поле, содержаще данные, которые необходимо считать, или выражение, которое выполняет вычисление с помощью данных в поле.</span><span class="sxs-lookup"><span data-stu-id="bb184-113">A string expression identifying the field that contains the data you want to count or an expression that performs a calculation using the data in the field.</span></span> <span data-ttu-id="bb184-114">Operands в *Expression* может включать имя настольного поля или функции (которые могут быть внутренними или пользовательскими, но не другими SQL совокупными функциями).</span><span class="sxs-lookup"><span data-stu-id="bb184-114">Operands in  *Expression*  can include the name of a table field or function (which can be either intrinsic or user-defined but not other SQL aggregate functions).</span></span> <span data-ttu-id="bb184-115">Можно вычислять любой тип данных, включая текст.</span><span class="sxs-lookup"><span data-stu-id="bb184-115">You can count any kind of data, including text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb184-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="bb184-116">Remarks</span></span>

<span data-ttu-id="bb184-117">Чтобы вычислить количество записей в базовом запросе, можно использовать функцию Count.</span><span class="sxs-lookup"><span data-stu-id="bb184-117">You can use Count to count the number of records in an underlying query.</span></span> <span data-ttu-id="bb184-118">Например, можно использовать функцию Count для вычисления количества заказов, отправленных в определенную страну или регион.</span><span class="sxs-lookup"><span data-stu-id="bb184-118">For example, you could use Count to count the number of orders shipped to a particular country or region.</span></span>
  
<span data-ttu-id="bb184-119">**Count** \* () возвращает количество элементов в группе.</span><span class="sxs-lookup"><span data-stu-id="bb184-119">**Count** (\*) returns the number of items in a group.</span></span> <span data-ttu-id="bb184-120">Это включает значения nULL и дубликаты.</span><span class="sxs-lookup"><span data-stu-id="bb184-120">This includes NULL values and duplicates.</span></span> 
  

