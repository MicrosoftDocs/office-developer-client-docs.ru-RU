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
description: Возвращает строку разделителя элементов списка для текущей операционной системы.
ms.openlocfilehash: 77610b2cf3cc515fb5d3e8b4c6c48de98ab4acc2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814100"
---
# <a name="listsep-function"></a><span data-ttu-id="b9d29-103">Функция LISTSEP</span><span class="sxs-lookup"><span data-stu-id="b9d29-103">LISTSEP Function</span></span>

<span data-ttu-id="b9d29-104">Возвращает строку разделителя элементов списка для текущей операционной системы.</span><span class="sxs-lookup"><span data-stu-id="b9d29-104">Returns the list-separator string for the current user locale.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b9d29-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9d29-105">Syntax</span></span>

<span data-ttu-id="b9d29-106">(LISTSEP)</span><span class="sxs-lookup"><span data-stu-id="b9d29-106">LISTSEP ()</span></span>
  
### <a name="return-value"></a><span data-ttu-id="b9d29-107">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="b9d29-107">Return value</span></span>

<span data-ttu-id="b9d29-108">String</span><span class="sxs-lookup"><span data-stu-id="b9d29-108">String</span></span>
  
## <a name="example"></a><span data-ttu-id="b9d29-109">Пример</span><span class="sxs-lookup"><span data-stu-id="b9d29-109">Example</span></span>

<span data-ttu-id="b9d29-110">SETF(GETREF(User.Extent) «MAX (ширина» &amp; ListSep() &amp; «Высота»))</span><span class="sxs-lookup"><span data-stu-id="b9d29-110">SETF(GETREF(user.extent), "MAX(Width" &amp; ListSep() &amp; "Height)")</span></span> 
  

