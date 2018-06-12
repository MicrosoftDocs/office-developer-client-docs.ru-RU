---
title: Атрибуты attDate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: f3319c9ae49fa97a6179b0ee800bd5dd594aefab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808087"
---
# <a name="attdate-attributes"></a><span data-ttu-id="e915e-103">Атрибуты attDate</span><span class="sxs-lookup"><span data-stu-id="e915e-103">attDate Attributes</span></span>

  
  
<span data-ttu-id="e915e-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e915e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e915e-105">Все свойства MAPI, относящиеся к значения даты и времени, сопоставляются с TNEF атрибутов, начинающиеся с префикса **attDate** .</span><span class="sxs-lookup"><span data-stu-id="e915e-105">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="e915e-106">Все эти кодируются как **DTR** структуры.</span><span class="sxs-lookup"><span data-stu-id="e915e-106">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="e915e-107">Дата и время для атрибутов вложения, помеченные как также **DTR** структуры.</span><span class="sxs-lookup"><span data-stu-id="e915e-107">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="e915e-108">Все свойства MAPI, относящиеся к значения даты и времени, сопоставляются с TNEF атрибутов, начинающиеся с префикса **attDate** .</span><span class="sxs-lookup"><span data-stu-id="e915e-108">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="e915e-109">Все эти кодируются как **DTR** структуры.</span><span class="sxs-lookup"><span data-stu-id="e915e-109">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="e915e-110">Дата и время для атрибутов вложения, помеченные как также **DTR** структуры.</span><span class="sxs-lookup"><span data-stu-id="e915e-110">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="e915e-111">Структура **DTR** является очень похож на структуру **SYSTEMTIME** , определенных в файлы заголовков Win32.</span><span class="sxs-lookup"><span data-stu-id="e915e-111">A **DTR** structure is very similar to the **SYSTEMTIME** structure defined in the Win32 header files.</span></span> <span data-ttu-id="e915e-112">Структура **DTR** закодирован в потоке TNEF **sizeof(DTR)** байт, начиная с первого элемента структуры.</span><span class="sxs-lookup"><span data-stu-id="e915e-112">The **DTR** structure is encoded in the TNEF stream as **sizeof(DTR)** bytes starting with the first member of the structure.</span></span> <span data-ttu-id="e915e-113">Структура **DTR** определен в формате TNEF. Файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="e915e-113">The **DTR** structure is defined in the TNEF.H header file.</span></span> 
  

