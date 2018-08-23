---
title: attDate Attributes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ff0cc6b1c17b2ed83d7b0ec0921904763da8624b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567015"
---
# <a name="attdate-attributes"></a><span data-ttu-id="00e1c-103">attDate Attributes</span><span class="sxs-lookup"><span data-stu-id="00e1c-103">attDate Attributes</span></span>

  
  
<span data-ttu-id="00e1c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00e1c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00e1c-105">Все свойства MAPI, относящиеся к значения даты и времени, сопоставляются с TNEF атрибутов, начинающиеся с префикса **attDate** .</span><span class="sxs-lookup"><span data-stu-id="00e1c-105">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="00e1c-106">Все эти кодируются как **DTR** структуры.</span><span class="sxs-lookup"><span data-stu-id="00e1c-106">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="00e1c-107">Дата и время для атрибутов вложения, помеченные как также **DTR** структуры.</span><span class="sxs-lookup"><span data-stu-id="00e1c-107">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="00e1c-108">Все свойства MAPI, относящиеся к значения даты и времени, сопоставляются с TNEF атрибутов, начинающиеся с префикса **attDate** .</span><span class="sxs-lookup"><span data-stu-id="00e1c-108">All MAPI properties relating to dates and times are mapped to TNEF attributes that have the **attDate** prefix.</span></span> <span data-ttu-id="00e1c-109">Все эти кодируются как **DTR** структуры.</span><span class="sxs-lookup"><span data-stu-id="00e1c-109">These are all encoded as **DTR** structures.</span></span> <span data-ttu-id="00e1c-110">Дата и время для атрибутов вложения, помеченные как также **DTR** структуры.</span><span class="sxs-lookup"><span data-stu-id="00e1c-110">The dates and times for attachment attributes are encoded as **DTR** structures as well.</span></span> 
  
<span data-ttu-id="00e1c-111">Структура **DTR** является очень похож на структуру **SYSTEMTIME** , определенных в файлы заголовков Win32.</span><span class="sxs-lookup"><span data-stu-id="00e1c-111">A **DTR** structure is very similar to the **SYSTEMTIME** structure defined in the Win32 header files.</span></span> <span data-ttu-id="00e1c-112">Структура **DTR** закодирован в потоке TNEF **sizeof(DTR)** байт, начиная с первого элемента структуры.</span><span class="sxs-lookup"><span data-stu-id="00e1c-112">The **DTR** structure is encoded in the TNEF stream as **sizeof(DTR)** bytes starting with the first member of the structure.</span></span> <span data-ttu-id="00e1c-113">Структура **DTR** определен в формате TNEF. Файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="00e1c-113">The **DTR** structure is defined in the TNEF.H header file.</span></span> 
  

