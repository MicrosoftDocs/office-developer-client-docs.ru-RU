---
title: Функция СУММ (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: Возвращает сумму всех значений в выражении.
ms.openlocfilehash: 98531a0487505c24ed62034b7c283b9765a3e7a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807127"
---
# <a name="sum-function-access-custom-web-app"></a><span data-ttu-id="a3eeb-103">Функция СУММ (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="a3eeb-103">Sum Function (Access custom web app)</span></span>

<span data-ttu-id="a3eeb-104">Возвращает сумму всех значений в выражении.</span><span class="sxs-lookup"><span data-stu-id="a3eeb-104">Returns the sum of all the values in the expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a3eeb-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a3eeb-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="a3eeb-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="a3eeb-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a3eeb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3eeb-107">Syntax</span></span>

 <span data-ttu-id="a3eeb-108">**Сумма** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="a3eeb-108">**Sum** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="a3eeb-109">Функция **сумм** содержит следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="a3eeb-109">The **Sum** function contains the following argument.</span></span> 
  
|<span data-ttu-id="a3eeb-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="a3eeb-110">**Argument name**</span></span>|<span data-ttu-id="a3eeb-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a3eeb-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a3eeb-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="a3eeb-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="a3eeb-113">Выражение, определяющее поле, содержащее числовые данные, которые необходимо добавить или выражение, которое выполняет вычисления с использованием данных для этого поля.</span><span class="sxs-lookup"><span data-stu-id="a3eeb-113">An expression identifying the field that contains the numeric data you want to add or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="a3eeb-114">Операнды в *NumericExpression* может включать имя поля в таблице, константа или функция (это может быть встроенным или определяемым пользователем, но не в одной из других статистические функции SQL).</span><span class="sxs-lookup"><span data-stu-id="a3eeb-114">Operands in  *NumericExpression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3eeb-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="a3eeb-115">Remarks</span></span>

<span data-ttu-id="a3eeb-116">Функция **сумм** игнорирует записи, содержащие значения Null.</span><span class="sxs-lookup"><span data-stu-id="a3eeb-116">The **Sum** function ignores records that contain Null values.</span></span> 
  
<span data-ttu-id="a3eeb-117">Функция **сумм** может использоваться только для числовых столбцов.</span><span class="sxs-lookup"><span data-stu-id="a3eeb-117">The **Sum** function can only be used with numeric columns.</span></span> 
  

