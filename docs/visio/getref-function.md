---
title: Функция GETREF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251884
localization_priority: Normal
ms.assetid: 25c9f817-d22b-28c9-1339-dc9f27d0dd41
description: Ссылается на ячейку и не пересчитывает формулу при изменении ячейки, на которую указывает ссылка.
ms.openlocfilehash: 38f3c8b4f34ed2b3d3711be5faed6b0d317e907a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424331"
---
# <a name="getref-function"></a><span data-ttu-id="056f0-103">Функция GETREF</span><span class="sxs-lookup"><span data-stu-id="056f0-103">GETREF Function</span></span>

<span data-ttu-id="056f0-104">Ссылается на ячейку и не пересчитывает формулу при изменении ячейки, на которую указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="056f0-104">References a cell and doesn't recalculate the formula when the referenced cell changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="056f0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="056f0-105">Syntax</span></span>

<span data-ttu-id="056f0-106">GETREF (\* \* *целлнаме* \* \*)</span><span class="sxs-lookup"><span data-stu-id="056f0-106">GETREF(\*\* *cellname* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="056f0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="056f0-107">Parameters</span></span>

|<span data-ttu-id="056f0-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="056f0-108">**Name**</span></span>|<span data-ttu-id="056f0-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="056f0-109">**Required/Optional**</span></span>|<span data-ttu-id="056f0-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="056f0-110">**Data Type**</span></span>|<span data-ttu-id="056f0-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="056f0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="056f0-112">_целлнаме_</span><span class="sxs-lookup"><span data-stu-id="056f0-112">_cellname_</span></span> <br/> |<span data-ttu-id="056f0-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="056f0-113">Required</span></span>  <br/> |<span data-ttu-id="056f0-114">**String**</span><span class="sxs-lookup"><span data-stu-id="056f0-114">**String**</span></span> <br/> |<span data-ttu-id="056f0-115">Имя ячейки, к которой требуется получить ссылку.</span><span class="sxs-lookup"><span data-stu-id="056f0-115">The name of the cell to get a reference to.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="056f0-116">Пример</span><span class="sxs-lookup"><span data-stu-id="056f0-116">Example</span></span>

<span data-ttu-id="056f0-117">SETF (GETREF (PinX), 5.1)</span><span class="sxs-lookup"><span data-stu-id="056f0-117">SETF(GETREF(PinX),5.1)</span></span> 
  
<span data-ttu-id="056f0-118">Задает формулу ячейки PinX равным 5,1.</span><span class="sxs-lookup"><span data-stu-id="056f0-118">Sets the formula of the PinX cell to 5.1.</span></span> 
  

