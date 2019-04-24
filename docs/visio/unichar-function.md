---
title: Функция UNICHAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60117
localization_priority: Normal
ms.assetid: 371a475d-50f7-6b4c-4b47-581cd778dcba
description: Возвращает символ Юникода из числа.
ms.openlocfilehash: 81e76b72da35f79dee9ad6afbde51bc2e228483c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327351"
---
# <a name="unichar-function"></a><span data-ttu-id="341c6-103">Функция UNICHAR</span><span class="sxs-lookup"><span data-stu-id="341c6-103">UNICHAR Function</span></span>

<span data-ttu-id="341c6-104">Возвращает символ Юникода из числа.</span><span class="sxs-lookup"><span data-stu-id="341c6-104">Returns the Unicode character from a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="341c6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="341c6-105">Syntax</span></span>

<span data-ttu-id="341c6-106">ЮНИСИМВ (\* \* *Number* \* \*)</span><span class="sxs-lookup"><span data-stu-id="341c6-106">UNICHAR (\*\* *number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="341c6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="341c6-107">Parameters</span></span>

|<span data-ttu-id="341c6-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="341c6-108">**Name**</span></span>|<span data-ttu-id="341c6-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="341c6-109">**Required/Optional**</span></span>|<span data-ttu-id="341c6-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="341c6-110">**Data Type**</span></span>|<span data-ttu-id="341c6-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="341c6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="341c6-112">_число_</span><span class="sxs-lookup"><span data-stu-id="341c6-112">_number_</span></span> <br/> |<span data-ttu-id="341c6-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="341c6-113">Required</span></span>  <br/> |<span data-ttu-id="341c6-114">**Integer**</span><span class="sxs-lookup"><span data-stu-id="341c6-114">**Integer**</span></span> <br/> |<span data-ttu-id="341c6-115">Целое число от 1 до 65 535 (включительно), или функция возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="341c6-115">An integer between 1 and 65,535 (inclusive), or the function returns an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="341c6-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="341c6-116">Remarks</span></span>

<span data-ttu-id="341c6-117">Результирующая строка — это один символ Юникода (два символа) в длину.</span><span class="sxs-lookup"><span data-stu-id="341c6-117">The resulting string is one Unicode character (two characters) in length.</span></span> 
  
## <a name="example"></a><span data-ttu-id="341c6-118">Пример</span><span class="sxs-lookup"><span data-stu-id="341c6-118">Example</span></span>

<span data-ttu-id="341c6-119">ЮНИСИМВ (65)</span><span class="sxs-lookup"><span data-stu-id="341c6-119">UNICHAR(65)</span></span> 
  
<span data-ttu-id="341c6-120">Возвращает (прописная латинская буква A)</span><span class="sxs-lookup"><span data-stu-id="341c6-120">Returns A (Latin Capital Letter A)</span></span> 
  

