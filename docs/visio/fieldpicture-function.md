---
title: Функция FIELDPICTURE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251592
localization_priority: Normal
ms.assetid: df88c55f-c098-dd4c-bf53-c7d7b60cf719
description: Возвращает строку формата изображения, которая соответствует коду внутреннего текстового формата поля Microsoft Visio.
ms.openlocfilehash: 1ab24c602c7975cf6be22a564a8b9ee9aa0d6f46
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322549"
---
# <a name="fieldpicture-function"></a><span data-ttu-id="590d9-103">Функция FIELDPICTURE</span><span class="sxs-lookup"><span data-stu-id="590d9-103">FIELDPICTURE Function</span></span>

<span data-ttu-id="590d9-104">Возвращает строку формата изображения, которая соответствует коду внутреннего текстового формата поля Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="590d9-104">Returns a format-picture string that matches the Microsoft Visio internal text field format code.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="590d9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="590d9-105">Syntax</span></span>

<span data-ttu-id="590d9-106">FIELDPICTURE (\* \* *Code* \* \*)</span><span class="sxs-lookup"><span data-stu-id="590d9-106">FIELDPICTURE(\*\* *code* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="590d9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="590d9-107">Parameters</span></span>

|<span data-ttu-id="590d9-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="590d9-108">**Name**</span></span>|<span data-ttu-id="590d9-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="590d9-109">**Required/Optional**</span></span>|<span data-ttu-id="590d9-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="590d9-110">**Data Type**</span></span>|<span data-ttu-id="590d9-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="590d9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="590d9-112">_code_</span><span class="sxs-lookup"><span data-stu-id="590d9-112">_code_</span></span> <br/> |<span data-ttu-id="590d9-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="590d9-113">Required</span></span>  <br/> |<span data-ttu-id="590d9-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="590d9-114">**Number**</span></span> <br/> | <span data-ttu-id="590d9-115">Код формата текстового поля.</span><span class="sxs-lookup"><span data-stu-id="590d9-115">A text field format code.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="590d9-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="590d9-116">Return value</span></span>

<span data-ttu-id="590d9-117">Строка</span><span class="sxs-lookup"><span data-stu-id="590d9-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="590d9-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="590d9-118">Remarks</span></span>

<span data-ttu-id="590d9-119">Format строки изображений используются в функции FORMAT для определения расширения значений дат, времени, чисел и меток единиц.</span><span class="sxs-lookup"><span data-stu-id="590d9-119">Format picture strings are used in the FORMAT function to define the expansion of values to dates, times, numbers, and unit labels.</span></span>
  
## <a name="example"></a><span data-ttu-id="590d9-120">Пример</span><span class="sxs-lookup"><span data-stu-id="590d9-120">Example</span></span>

<span data-ttu-id="590d9-121">FIELDPICTURE (0)</span><span class="sxs-lookup"><span data-stu-id="590d9-121">FIELDPICTURE(0)</span></span> 
  
<span data-ttu-id="590d9-122">Возвращает строку изображения "ESC (0)", которая указывает число с одним десятичным разрядом и описанием в нижнем регистре при использовании в функции FORMAT.</span><span class="sxs-lookup"><span data-stu-id="590d9-122">Returns the format picture string "esc(0)", which specifies a number that has one decimal place and a lowercase unit description when used in the FORMAT function.</span></span> 
  

