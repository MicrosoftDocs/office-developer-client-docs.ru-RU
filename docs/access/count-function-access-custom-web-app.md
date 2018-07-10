---
title: Функция Count (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: Возвращает число записей в запросе или в таблице.
ms.openlocfilehash: 300fcbfd2aa927dd19516355ae28eec2adadf521
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806966"
---
# <a name="count-function-access-custom-web-app"></a><span data-ttu-id="4e7c9-103">Функция Count (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="4e7c9-103">Count function (Access custom web app)</span></span>

<span data-ttu-id="4e7c9-104">Возвращает число записей в запросе или в таблице.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-104">Returns the number of records in a query or table.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="4e7c9-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="4e7c9-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4e7c9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e7c9-107">Syntax</span></span>

<span data-ttu-id="4e7c9-108">**Count** (*Выражение*)</span><span class="sxs-lookup"><span data-stu-id="4e7c9-108">**Count** (*Expression*)</span></span> 
  
<span data-ttu-id="4e7c9-109">Функция **Count** содержит следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-109">The **Count** function contains the following argument.</span></span> 
  
|<span data-ttu-id="4e7c9-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="4e7c9-110">**Argument name**</span></span>|<span data-ttu-id="4e7c9-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4e7c9-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="4e7c9-112">*Выражение*</span><span class="sxs-lookup"><span data-stu-id="4e7c9-112">*Expression*</span></span>  <br/> |<span data-ttu-id="4e7c9-113">Строковое выражение, определяющее поле, содержащее данные необходимо число или выражение, которое выполняет вычисления с использованием данных в поле.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-113">A string expression identifying the field that contains the data you want to count or an expression that performs a calculation using the data in the field.</span></span> <span data-ttu-id="4e7c9-114">Операнды в *выражении* может включать имя поля в таблице или функция (это может быть встроенным или определяемым пользователем, но не другие SQL статистические функции).</span><span class="sxs-lookup"><span data-stu-id="4e7c9-114">Operands in  *Expression*  can include the name of a table field or function (which can be either intrinsic or user-defined but not other SQL aggregate functions).</span></span> <span data-ttu-id="4e7c9-115">Можно подсчитать любой тип данных, включая текст.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-115">You can count any kind of data, including text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e7c9-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="4e7c9-116">Remarks</span></span>

<span data-ttu-id="4e7c9-117">Count можно использовать для определения числа записей в запросе.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-117">You can use Count to count the number of records in an underlying query.</span></span> <span data-ttu-id="4e7c9-118">Count можно использовать, например, чтобы подсчитать количество заказов, отправленных в определенной стране или регионе.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-118">For example, you could use Count to count the number of orders shipped to a particular country or region.</span></span>
  
<span data-ttu-id="4e7c9-119">**Count** (\*) возвращает число элементов в группе.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-119">**Count** (\*) returns the number of items in a group.</span></span> <span data-ttu-id="4e7c9-120">Этот компонент включает значения NULL и повторяющиеся.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-120">This includes NULL values and duplicates.</span></span> 
  

