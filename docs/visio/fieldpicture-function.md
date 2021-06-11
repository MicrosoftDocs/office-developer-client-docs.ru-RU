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
description: Возвращает строку формат-картинка, которая соответствует коду формата microsoft Visio текстового поля.
ms.openlocfilehash: 1ab24c602c7975cf6be22a564a8b9ee9aa0d6f46
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431458"
---
# <a name="fieldpicture-function"></a><span data-ttu-id="83b8d-103">Функция FIELDPICTURE</span><span class="sxs-lookup"><span data-stu-id="83b8d-103">FIELDPICTURE Function</span></span>

<span data-ttu-id="83b8d-104">Возвращает строку формат-картинка, которая соответствует коду формата microsoft Visio текстового поля.</span><span class="sxs-lookup"><span data-stu-id="83b8d-104">Returns a format-picture string that matches the Microsoft Visio internal text field format code.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="83b8d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83b8d-105">Syntax</span></span>

<span data-ttu-id="83b8d-106">FIELDPICTURE(\*\* *code* \*\* )</span><span class="sxs-lookup"><span data-stu-id="83b8d-106">FIELDPICTURE(\*\* *code* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="83b8d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="83b8d-107">Parameters</span></span>

|<span data-ttu-id="83b8d-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="83b8d-108">**Name**</span></span>|<span data-ttu-id="83b8d-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="83b8d-109">**Required/Optional**</span></span>|<span data-ttu-id="83b8d-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="83b8d-110">**Data Type**</span></span>|<span data-ttu-id="83b8d-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="83b8d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="83b8d-112">_code_</span><span class="sxs-lookup"><span data-stu-id="83b8d-112">_code_</span></span> <br/> |<span data-ttu-id="83b8d-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="83b8d-113">Required</span></span>  <br/> |<span data-ttu-id="83b8d-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="83b8d-114">**Number**</span></span> <br/> | <span data-ttu-id="83b8d-115">Код формата текстового поля.</span><span class="sxs-lookup"><span data-stu-id="83b8d-115">A text field format code.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="83b8d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83b8d-116">Return value</span></span>

<span data-ttu-id="83b8d-117">String</span><span class="sxs-lookup"><span data-stu-id="83b8d-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="83b8d-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="83b8d-118">Remarks</span></span>

<span data-ttu-id="83b8d-119">Строки изображений формата используются в функции FORMAT для определения расширения значений до дат, времен, чисел и меток единиц.</span><span class="sxs-lookup"><span data-stu-id="83b8d-119">Format picture strings are used in the FORMAT function to define the expansion of values to dates, times, numbers, and unit labels.</span></span>
  
## <a name="example"></a><span data-ttu-id="83b8d-120">Пример</span><span class="sxs-lookup"><span data-stu-id="83b8d-120">Example</span></span>

<span data-ttu-id="83b8d-121">FIELDPICTURE(0)</span><span class="sxs-lookup"><span data-stu-id="83b8d-121">FIELDPICTURE(0)</span></span> 
  
<span data-ttu-id="83b8d-122">Возвращает строку изображения формата "esc(0)", которая указывает номер, который имеет одно десятичной номер и описание блока нижнего регистра при работе с функцией FORMAT.</span><span class="sxs-lookup"><span data-stu-id="83b8d-122">Returns the format picture string "esc(0)", which specifies a number that has one decimal place and a lowercase unit description when used in the FORMAT function.</span></span> 
  

