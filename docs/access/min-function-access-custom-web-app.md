---
title: Функция мин (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 930c906d-d6f0-49ad-8ed7-336e7833d672
description: Возвращает минимальное значение в выражении запроса или в таблице.
ms.openlocfilehash: c1543ed87a13bf7e35bda7feae214674e79d188c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807086"
---
# <a name="min-function-access-custom-web-app"></a><span data-ttu-id="5cdb6-103">Функция мин (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="5cdb6-103">Min Function (Access custom web app)</span></span>

<span data-ttu-id="5cdb6-104">Возвращает минимальное значение в выражении запроса или в таблице.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-104">Returns the minimum value in the expression in a query or table.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="5cdb6-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="5cdb6-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5cdb6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5cdb6-107">Syntax</span></span>

 <span data-ttu-id="5cdb6-108">**Мин.** (*Выражение*)</span><span class="sxs-lookup"><span data-stu-id="5cdb6-108">**Min** (*Expression*)</span></span> 
  
<span data-ttu-id="5cdb6-109">Функция **Min** содержит следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-109">The **Min** function contains the following argument.</span></span> 
  
|<span data-ttu-id="5cdb6-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="5cdb6-110">**Argument name**</span></span>|<span data-ttu-id="5cdb6-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5cdb6-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5cdb6-112">*Выражение*</span><span class="sxs-lookup"><span data-stu-id="5cdb6-112">*Expression*</span></span>  <br/> |<span data-ttu-id="5cdb6-113">Строковое выражение, определяющее поле, содержащее данные, которые требуется вычислить или выражение, которое выполняет вычисления с использованием данных для этого поля.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-113">A string expression identifying the field that contains the data you want to evaluate or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="5cdb6-114">Операнды в *выражении* может включать имя поля в таблице, константа или функция (это может быть встроенным или определяемым пользователем, но не в одной из других статистические функции SQL).</span><span class="sxs-lookup"><span data-stu-id="5cdb6-114">Operands in  *Expression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   

