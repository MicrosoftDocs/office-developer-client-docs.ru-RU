---
title: Функция EVALTEXT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251422
localization_priority: Normal
ms.assetid: c9b5b96c-d8c8-6119-e3f1-a2ce9d7c043e
description: Оценивает текст в шапенаме как формулу и возвращает результат.
ms.openlocfilehash: 6600d9d6ddaf630a93fdb5c37639ce50a21a4307
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438360"
---
# <a name="evaltext-function"></a><span data-ttu-id="5ef4d-103">Функция EVALTEXT</span><span class="sxs-lookup"><span data-stu-id="5ef4d-103">EVALTEXT Function</span></span>

<span data-ttu-id="5ef4d-104">Оценивает текст в _шапенаме_ как формулу и возвращает результат.</span><span class="sxs-lookup"><span data-stu-id="5ef4d-104">Evaluates the text in  _shapename_ as if it were a formula and returns the result.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5ef4d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ef4d-105">Syntax</span></span>

<span data-ttu-id="5ef4d-106">EVALTEXT (\* \* *шапенаме! theText* \* \*)</span><span class="sxs-lookup"><span data-stu-id="5ef4d-106">EVALTEXT(\*\* *shapename!theText* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5ef4d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ef4d-107">Parameters</span></span>

|<span data-ttu-id="5ef4d-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="5ef4d-108">**Name**</span></span>|<span data-ttu-id="5ef4d-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="5ef4d-109">**Required/Optional**</span></span>|<span data-ttu-id="5ef4d-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="5ef4d-110">**Data Type**</span></span>|<span data-ttu-id="5ef4d-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5ef4d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5ef4d-112">_шапенаме! theText_</span><span class="sxs-lookup"><span data-stu-id="5ef4d-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="5ef4d-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5ef4d-113">Required</span></span>  <br/> |<span data-ttu-id="5ef4d-114">**String**</span><span class="sxs-lookup"><span data-stu-id="5ef4d-114">**String**</span></span> <br/> |<span data-ttu-id="5ef4d-115">Ячейка, вызываемая при изменении композиции текста связанной фигуры.</span><span class="sxs-lookup"><span data-stu-id="5ef4d-115">A cell that is triggered when the associated shape's text composition changes.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5ef4d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ef4d-116">Return value</span></span>

<span data-ttu-id="5ef4d-117">String</span><span class="sxs-lookup"><span data-stu-id="5ef4d-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5ef4d-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="5ef4d-118">Remarks</span></span>

 <span data-ttu-id="5ef4d-119">_шапенаме_ можно использовать для ссылки на текст фигуры, отличной от текущей фигуры.</span><span class="sxs-lookup"><span data-stu-id="5ef4d-119">_shapename_ can be used to refer to the text of a shape other than the current shape.</span></span> 
  
<span data-ttu-id="5ef4d-120">Если текст отсутствует, результат равен нулю.</span><span class="sxs-lookup"><span data-stu-id="5ef4d-120">If there is no text, the result is zero.</span></span> <span data-ttu-id="5ef4d-121">Если текст не может быть оценен, функция возвращает сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="5ef4d-121">If the text cannot be evaluated, the function returns an error.</span></span>
  
## <a name="example"></a><span data-ttu-id="5ef4d-122">Пример</span><span class="sxs-lookup"><span data-stu-id="5ef4d-122">Example</span></span>

<span data-ttu-id="5ef4d-123">EVALTEXT (line. 2! theText)</span><span class="sxs-lookup"><span data-stu-id="5ef4d-123">EVALTEXT(Line.2!theText)</span></span> 
  
<span data-ttu-id="5ef4d-124">Оценивает текст, содержащийся в линии фигуры. 2.</span><span class="sxs-lookup"><span data-stu-id="5ef4d-124">Evaluates the text contained in the shape Line.2.</span></span> <span data-ttu-id="5ef4d-125">Например, если строка. 2 содержит "4 ФТ + 0,5 ФТ", возвращает значение 4,5 ФТ.</span><span class="sxs-lookup"><span data-stu-id="5ef4d-125">For example, if Line.2 contains "4 ft + 0.5 ft", returns the value 4.5 ft.</span></span> 
  

