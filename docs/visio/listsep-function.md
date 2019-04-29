---
title: Функция LISTSEP
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251882
localization_priority: Normal
ms.assetid: 73dc5981-2c8c-e76e-e4bd-e65a7c8db242
description: Возвращает строку с разделителем списков для текущего языкового стандарта пользователя.
ms.openlocfilehash: 901442a3c2af8509855b8b038057e7f813634ea1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431409"
---
# <a name="listsep-function"></a><span data-ttu-id="05ac8-103">Функция LISTSEP</span><span class="sxs-lookup"><span data-stu-id="05ac8-103">LISTSEP Function</span></span>

<span data-ttu-id="05ac8-104">Возвращает строку с разделителем списков для текущего языкового стандарта пользователя.</span><span class="sxs-lookup"><span data-stu-id="05ac8-104">Returns the list-separator string for the current user locale.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="05ac8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05ac8-105">Syntax</span></span>

<span data-ttu-id="05ac8-106">LISTSEP ()</span><span class="sxs-lookup"><span data-stu-id="05ac8-106">LISTSEP ()</span></span>
  
### <a name="return-value"></a><span data-ttu-id="05ac8-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05ac8-107">Return value</span></span>

<span data-ttu-id="05ac8-108">String</span><span class="sxs-lookup"><span data-stu-id="05ac8-108">String</span></span>
  
## <a name="example"></a><span data-ttu-id="05ac8-109">Пример</span><span class="sxs-lookup"><span data-stu-id="05ac8-109">Example</span></span>

<span data-ttu-id="05ac8-110">SETF (GETREF (User. экстент), "MAX (ширина" &amp; ListSep () &amp; "высота)")</span><span class="sxs-lookup"><span data-stu-id="05ac8-110">SETF(GETREF(user.extent), "MAX(Width" &amp; ListSep() &amp; "Height)")</span></span> 
  

