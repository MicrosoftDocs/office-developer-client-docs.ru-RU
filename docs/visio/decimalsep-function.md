---
title: Функция DECIMALSEP
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251883
localization_priority: Normal
ms.assetid: 091fe401-05b2-464f-9333-7bb7118cd7cd
description: Возвращает строку разделителя целой и дробной части для текущей операционной системы.
ms.openlocfilehash: a47bc20702262ab7d4a072694c36e424e6949919
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813573"
---
# <a name="decimalsep-function"></a><span data-ttu-id="64aee-103">Функция DECIMALSEP</span><span class="sxs-lookup"><span data-stu-id="64aee-103">DECIMALSEP Function</span></span>

<span data-ttu-id="64aee-104">Возвращает строку разделителя целой и дробной части для текущей операционной системы.</span><span class="sxs-lookup"><span data-stu-id="64aee-104">Returns the decimal separator string for the current user locale.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="64aee-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64aee-105">Syntax</span></span>

<span data-ttu-id="64aee-106">(DECIMALSEP)</span><span class="sxs-lookup"><span data-stu-id="64aee-106">DECIMALSEP( )</span></span>
  
## <a name="example"></a><span data-ttu-id="64aee-107">Пример</span><span class="sxs-lookup"><span data-stu-id="64aee-107">Example</span></span>

<span data-ttu-id="64aee-108">SETF(GETREF(User.Size), user.wholePart &amp; DECIMALSEP() &amp; user.fracPart)</span><span class="sxs-lookup"><span data-stu-id="64aee-108">SETF(GETREF(user.size), user.wholePart &amp; DECIMALSEP() &amp; user.fracPart)</span></span> 
  

