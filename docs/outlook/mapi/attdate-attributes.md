---
title: Атрибуты Аттдате
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b7c1ce8d0338a2bda63a276628bdd6e8be3b8eb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318069"
---
# <a name="attdate-attributes"></a><span data-ttu-id="18704-103">Атрибуты Аттдате</span><span class="sxs-lookup"><span data-stu-id="18704-103">attDate Attributes</span></span>

  
  
<span data-ttu-id="18704-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18704-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18704-105">Все свойства MAPI, относящиеся к датам и времени, сопоставляются с атрибутами TNEF, имеющими префикс **аттдате** .</span><span class="sxs-lookup"><span data-stu-id="18704-105">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="18704-106">Все они кодируются как структуры **DTR** .</span><span class="sxs-lookup"><span data-stu-id="18704-106">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="18704-107">Даты и время для атрибутов вложений кодируются как структуры **DTR** .</span><span class="sxs-lookup"><span data-stu-id="18704-107">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="18704-108">Все свойства MAPI, относящиеся к датам и времени, сопоставляются с атрибутами TNEF, имеющими префикс **аттдате** .</span><span class="sxs-lookup"><span data-stu-id="18704-108">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="18704-109">Все они кодируются как структуры **DTR** .</span><span class="sxs-lookup"><span data-stu-id="18704-109">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="18704-110">Даты и время для атрибутов вложений кодируются как структуры **DTR** .</span><span class="sxs-lookup"><span data-stu-id="18704-110">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="18704-111">**DTR** -структура очень похожа на структуру **SYSTEMTIME** , определенную в файлах заголовков Win32.</span><span class="sxs-lookup"><span data-stu-id="18704-111">A **DTR** structure is very similar to the **SYSTEMTIME** structure defined in the Win32 header files.</span></span> <span data-ttu-id="18704-112">В потоке TNEF структура **DTR** кодируется в байтах типа **sizeof (DTR)** , начиная с первого члена структуры.</span><span class="sxs-lookup"><span data-stu-id="18704-112">The **DTR** structure is encoded in the TNEF stream as **sizeof(DTR)** bytes starting with the first member of the structure.</span></span> <span data-ttu-id="18704-113">Структура **DTR** определена в формате TNEF. H файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="18704-113">The **DTR** structure is defined in the TNEF.H header file.</span></span> 
  

