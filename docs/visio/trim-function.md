---
title: Функция TRIM
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027318
localization_priority: Normal
ms.assetid: 6f2d84fd-27eb-4c2f-a2e1-43d20e0c78be
description: Удаляет все пробелы из текста, за исключением одиночных пробелов между словами.
ms.openlocfilehash: b947c9500012d0ceefe3e8044be387f7b810dda9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435721"
---
# <a name="trim-function"></a><span data-ttu-id="ceb00-103">Функция TRIM</span><span class="sxs-lookup"><span data-stu-id="ceb00-103">TRIM Function</span></span>

<span data-ttu-id="ceb00-104">Удаляет все пробелы из текста, за исключением одиночных пробелов между словами.</span><span class="sxs-lookup"><span data-stu-id="ceb00-104">Removes all space from text, except for single spaces between words.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ceb00-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ceb00-105">Syntax</span></span>

<span data-ttu-id="ceb00-106">TRIM (\* \* *Text* \* \*)</span><span class="sxs-lookup"><span data-stu-id="ceb00-106">TRIM (\*\* *text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ceb00-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ceb00-107">Parameters</span></span>

|<span data-ttu-id="ceb00-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="ceb00-108">**Name**</span></span>|<span data-ttu-id="ceb00-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="ceb00-109">**Required/Optional**</span></span>|<span data-ttu-id="ceb00-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="ceb00-110">**Data Type**</span></span>|<span data-ttu-id="ceb00-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ceb00-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ceb00-112">_text_</span><span class="sxs-lookup"><span data-stu-id="ceb00-112">_text_</span></span> <br/> |<span data-ttu-id="ceb00-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ceb00-113">Required</span></span>  <br/> |<span data-ttu-id="ceb00-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ceb00-114">**String**</span></span> <br/> |<span data-ttu-id="ceb00-115">Текст, из которого требуется удалить пробелы.</span><span class="sxs-lookup"><span data-stu-id="ceb00-115">The text from which you want to remove spaces.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ceb00-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ceb00-116">Return value</span></span>

<span data-ttu-id="ceb00-117">String</span><span class="sxs-lookup"><span data-stu-id="ceb00-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ceb00-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="ceb00-118">Remarks</span></span>

<span data-ttu-id="ceb00-119">Функцию TRIM можно использовать для текста, полученного из другого приложения с неравномерными интервалами.</span><span class="sxs-lookup"><span data-stu-id="ceb00-119">You can use the TRIM function on text that you have received from another application that may have irregular spacing.</span></span>
  
## <a name="example"></a><span data-ttu-id="ceb00-120">Пример</span><span class="sxs-lookup"><span data-stu-id="ceb00-120">Example</span></span>

<span data-ttu-id="ceb00-121">TRIM ("1 января 2003")</span><span class="sxs-lookup"><span data-stu-id="ceb00-121">TRIM ("January 1, 2003 ")</span></span> 
  
<span data-ttu-id="ceb00-122">Возвращает значение "1 января 2003".</span><span class="sxs-lookup"><span data-stu-id="ceb00-122">Returns "January 1, 2003".</span></span> 
  

