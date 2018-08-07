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
description: Возвращает символ Unicode из числа.
ms.openlocfilehash: 06f97717ee4d5965253b0da7cfd5c35faf0ca2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815104"
---
# <a name="unichar-function"></a><span data-ttu-id="9faf3-103">Функция UNICHAR</span><span class="sxs-lookup"><span data-stu-id="9faf3-103">UNICHAR Function</span></span>

<span data-ttu-id="9faf3-104">Возвращает символ Unicode из числа.</span><span class="sxs-lookup"><span data-stu-id="9faf3-104">Returns the Unicode character from a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9faf3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9faf3-105">Syntax</span></span>

<span data-ttu-id="9faf3-106">UNICHAR (** *номер* **)</span><span class="sxs-lookup"><span data-stu-id="9faf3-106">UNICHAR (** *number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9faf3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9faf3-107">Parameters</span></span>

|<span data-ttu-id="9faf3-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="9faf3-108">**Name**</span></span>|<span data-ttu-id="9faf3-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="9faf3-109">**Required/Optional**</span></span>|<span data-ttu-id="9faf3-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="9faf3-110">**Data Type**</span></span>|<span data-ttu-id="9faf3-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9faf3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9faf3-112">_number_</span><span class="sxs-lookup"><span data-stu-id="9faf3-112">_number_</span></span> <br/> |<span data-ttu-id="9faf3-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9faf3-113">Required</span></span>  <br/> |<span data-ttu-id="9faf3-114">**Integer**</span><span class="sxs-lookup"><span data-stu-id="9faf3-114">**Integer**</span></span> <br/> |<span data-ttu-id="9faf3-115">Целое число от 1 до 65 535 (включительно) или функцию возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="9faf3-115">An integer between 1 and 65,535 (inclusive), or the function returns an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9faf3-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="9faf3-116">Remarks</span></span>

<span data-ttu-id="9faf3-117">Результирующую строку — один символ Unicode (двух знаков) в длину.</span><span class="sxs-lookup"><span data-stu-id="9faf3-117">The resulting string is one Unicode character (two characters) in length.</span></span> 
  
## <a name="example"></a><span data-ttu-id="9faf3-118">Пример</span><span class="sxs-lookup"><span data-stu-id="9faf3-118">Example</span></span>

<span data-ttu-id="9faf3-119">UNICHAR(65)</span><span class="sxs-lookup"><span data-stu-id="9faf3-119">UNICHAR(65)</span></span> 
  
<span data-ttu-id="9faf3-120">Возвращает (прописная латинская буква A)</span><span class="sxs-lookup"><span data-stu-id="9faf3-120">Returns A (Latin Capital Letter A)</span></span> 
  

