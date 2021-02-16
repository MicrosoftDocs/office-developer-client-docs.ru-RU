---
title: Функция LISTSHEETREF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ddbc35-8577-0a96-20b8-aa7734764c5b
description: Возвращает ссылку листа на фигуру контейнера списка, содержаную фигуру.
ms.openlocfilehash: 748a248f68345e97e97ca90a4603b6e164a551c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429553"
---
# <a name="listsheetref-function"></a><span data-ttu-id="fb6c6-103">Функция LISTSHEETREF</span><span class="sxs-lookup"><span data-stu-id="fb6c6-103">LISTSHEETREF Function</span></span>

<span data-ttu-id="fb6c6-104">Возвращает ссылку листа на фигуру контейнера списка, содержаную фигуру.</span><span class="sxs-lookup"><span data-stu-id="fb6c6-104">Returns a sheet reference to the list container shape that contains the shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="fb6c6-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="fb6c6-105">Version Information</span></span>

<span data-ttu-id="fb6c6-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="fb6c6-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fb6c6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb6c6-107">Syntax</span></span>

<span data-ttu-id="fb6c6-108">LISTMEMBERCOUNT()</span><span class="sxs-lookup"><span data-stu-id="fb6c6-108">LISTMEMBERCOUNT()</span></span>
  
### <a name="return-value"></a><span data-ttu-id="fb6c6-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb6c6-109">Return value</span></span>

<span data-ttu-id="fb6c6-110">Справка по shapeSheet</span><span class="sxs-lookup"><span data-stu-id="fb6c6-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fb6c6-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="fb6c6-111">Remarks</span></span>

<span data-ttu-id="fb6c6-112">Если фигура не является членом списка, функция LISTSHEETREF возвращает #REF!.</span><span class="sxs-lookup"><span data-stu-id="fb6c6-112">If the shape is not a list member, the LISTSHEETREF function returns #REF!.</span></span>
  
## <a name="example"></a><span data-ttu-id="fb6c6-113">Пример</span><span class="sxs-lookup"><span data-stu-id="fb6c6-113">Example</span></span>

<span data-ttu-id="fb6c6-114">LISTSHEETREF(1)! Height</span><span class="sxs-lookup"><span data-stu-id="fb6c6-114">LISTSHEETREF(1)!Height</span></span> 
  
<span data-ttu-id="fb6c6-115">Возвращает значение в ячейке Height фигуры контейнера списка, которая содержит фигуру.</span><span class="sxs-lookup"><span data-stu-id="fb6c6-115">Returns the value in the Height cell of the list container shape that contains the shape.</span></span> 
  

