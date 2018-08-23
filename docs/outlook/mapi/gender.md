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
ms.openlocfilehash: a74a6639023ae6ffddeabd03970b609e7b7babe1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588456"
---
# <a name="gender"></a><span data-ttu-id="d891d-103">Gender</span><span class="sxs-lookup"><span data-stu-id="d891d-103">Gender</span></span>

  
  
<span data-ttu-id="d891d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d891d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d891d-105">Задает возможные значения для Пол обмена сообщениями пользователя.</span><span class="sxs-lookup"><span data-stu-id="d891d-105">Specifies the possible values for the gender of a messaging user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d891d-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="d891d-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="d891d-107">Members</span><span class="sxs-lookup"><span data-stu-id="d891d-107">Members</span></span>

 <span data-ttu-id="d891d-108">_genderMin_</span><span class="sxs-lookup"><span data-stu-id="d891d-108">_genderMin_</span></span>
  
> <span data-ttu-id="d891d-109">Минимальное количество различные значения, поддерживаемые для Пол.</span><span class="sxs-lookup"><span data-stu-id="d891d-109">The minimum number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="d891d-110">_genderUnspecified_</span><span class="sxs-lookup"><span data-stu-id="d891d-110">_genderUnspecified_</span></span>
  
> <span data-ttu-id="d891d-111">Пол не задан для обмена сообщениями пользователя.</span><span class="sxs-lookup"><span data-stu-id="d891d-111">The gender is not specified for the messaging user.</span></span>
    
 <span data-ttu-id="d891d-112">_genderFemale_</span><span class="sxs-lookup"><span data-stu-id="d891d-112">_genderFemale_</span></span>
  
> <span data-ttu-id="d891d-113">Пользователь, обмена мгновенными сообщениями, гнездо.</span><span class="sxs-lookup"><span data-stu-id="d891d-113">The messaging user is female.</span></span>
    
 <span data-ttu-id="d891d-114">_genderMale_</span><span class="sxs-lookup"><span data-stu-id="d891d-114">_genderMale_</span></span>
  
> <span data-ttu-id="d891d-115">Пользователь, обмена мгновенными сообщениями, штекер.</span><span class="sxs-lookup"><span data-stu-id="d891d-115">The messaging user is male.</span></span>
    
 <span data-ttu-id="d891d-116">_genderCount_</span><span class="sxs-lookup"><span data-stu-id="d891d-116">_genderCount_</span></span>
  
> <span data-ttu-id="d891d-117">Число различных значений, поддерживаемые для Пол.</span><span class="sxs-lookup"><span data-stu-id="d891d-117">The number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="d891d-118">_genderMax_</span><span class="sxs-lookup"><span data-stu-id="d891d-118">_genderMax_</span></span>
  
> <span data-ttu-id="d891d-119">Максимальное число различные значения, поддерживаемые для Пол.</span><span class="sxs-lookup"><span data-stu-id="d891d-119">The maximum number of different values supported for the gender.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d891d-120">См. также</span><span class="sxs-lookup"><span data-stu-id="d891d-120">See also</span></span>



[<span data-ttu-id="d891d-121">Каноническое свойство PidTagGender</span><span class="sxs-lookup"><span data-stu-id="d891d-121">PidTagGender Canonical Property</span></span>](pidtaggender-canonical-property.md)

