---
title: Gender
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7abc62938b3c33e42adedfe8ccd66e072314e333
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808531"
---
# <a name="gender"></a><span data-ttu-id="244e5-103">Gender</span><span class="sxs-lookup"><span data-stu-id="244e5-103">Gender</span></span>

  
  
<span data-ttu-id="244e5-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="244e5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="244e5-105">Задает возможные значения для Пол обмена сообщениями пользователя.</span><span class="sxs-lookup"><span data-stu-id="244e5-105">Specifies the possible values for the gender of a messaging user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="244e5-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="244e5-106">Quick info</span></span>

```cpp
enum Gender { 
    genderMin = 0, 
    genderUnspecified = genderMin, 
    genderFemale, 
    genderMale, 
    genderCount, 
    genderMax = genderCount - 1 
}; 

```

## <a name="members"></a><span data-ttu-id="244e5-107">Members</span><span class="sxs-lookup"><span data-stu-id="244e5-107">Members</span></span>

 <span data-ttu-id="244e5-108">_genderMin_</span><span class="sxs-lookup"><span data-stu-id="244e5-108">_genderMin_</span></span>
  
> <span data-ttu-id="244e5-109">Минимальное количество различные значения, поддерживаемые для Пол.</span><span class="sxs-lookup"><span data-stu-id="244e5-109">The minimum number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="244e5-110">_genderUnspecified_</span><span class="sxs-lookup"><span data-stu-id="244e5-110">_genderUnspecified_</span></span>
  
> <span data-ttu-id="244e5-111">Пол не задан для обмена сообщениями пользователя.</span><span class="sxs-lookup"><span data-stu-id="244e5-111">The gender is not specified for the messaging user.</span></span>
    
 <span data-ttu-id="244e5-112">_genderFemale_</span><span class="sxs-lookup"><span data-stu-id="244e5-112">_genderFemale_</span></span>
  
> <span data-ttu-id="244e5-113">Пользователь, обмена мгновенными сообщениями, гнездо.</span><span class="sxs-lookup"><span data-stu-id="244e5-113">The messaging user is female.</span></span>
    
 <span data-ttu-id="244e5-114">_genderMale_</span><span class="sxs-lookup"><span data-stu-id="244e5-114">_genderMale_</span></span>
  
> <span data-ttu-id="244e5-115">Пользователь, обмена мгновенными сообщениями, штекер.</span><span class="sxs-lookup"><span data-stu-id="244e5-115">The messaging user is male.</span></span>
    
 <span data-ttu-id="244e5-116">_genderCount_</span><span class="sxs-lookup"><span data-stu-id="244e5-116">_genderCount_</span></span>
  
> <span data-ttu-id="244e5-117">Число различных значений, поддерживаемые для Пол.</span><span class="sxs-lookup"><span data-stu-id="244e5-117">The number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="244e5-118">_genderMax_</span><span class="sxs-lookup"><span data-stu-id="244e5-118">_genderMax_</span></span>
  
> <span data-ttu-id="244e5-119">Максимальное число различные значения, поддерживаемые для Пол.</span><span class="sxs-lookup"><span data-stu-id="244e5-119">The maximum number of different values supported for the gender.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="244e5-120">См. также</span><span class="sxs-lookup"><span data-stu-id="244e5-120">See also</span></span>



[<span data-ttu-id="244e5-121">Каноническое свойство PidTagGender</span><span class="sxs-lookup"><span data-stu-id="244e5-121">PidTagGender Canonical Property</span></span>](pidtaggender-canonical-property.md)

