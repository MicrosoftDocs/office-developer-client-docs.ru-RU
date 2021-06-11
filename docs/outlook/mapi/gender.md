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
ms.openlocfilehash: 042216df309e98f35ed0ad71742e46300ebb06da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428650"
---
# <a name="gender"></a><span data-ttu-id="164df-103">Gender</span><span class="sxs-lookup"><span data-stu-id="164df-103">Gender</span></span>

  
  
<span data-ttu-id="164df-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="164df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="164df-105">Указывает возможные значения для пола пользователя обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="164df-105">Specifies the possible values for the gender of a messaging user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="164df-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="164df-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="164df-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="164df-107">Members</span></span>

 <span data-ttu-id="164df-108">_genderMin_</span><span class="sxs-lookup"><span data-stu-id="164df-108">_genderMin_</span></span>
  
> <span data-ttu-id="164df-109">Минимальное количество различных значений, поддерживаемых для пола.</span><span class="sxs-lookup"><span data-stu-id="164df-109">The minimum number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="164df-110">_genderUnspecified_</span><span class="sxs-lookup"><span data-stu-id="164df-110">_genderUnspecified_</span></span>
  
> <span data-ttu-id="164df-111">Пол пользователя обмена сообщениями не указывается.</span><span class="sxs-lookup"><span data-stu-id="164df-111">The gender is not specified for the messaging user.</span></span>
    
 <span data-ttu-id="164df-112">_genderFemale_</span><span class="sxs-lookup"><span data-stu-id="164df-112">_genderFemale_</span></span>
  
> <span data-ttu-id="164df-113">Пользователь обмена сообщениями — женщина.</span><span class="sxs-lookup"><span data-stu-id="164df-113">The messaging user is female.</span></span>
    
 <span data-ttu-id="164df-114">_genderMale_</span><span class="sxs-lookup"><span data-stu-id="164df-114">_genderMale_</span></span>
  
> <span data-ttu-id="164df-115">Пользователь обмена сообщениями — мужчина.</span><span class="sxs-lookup"><span data-stu-id="164df-115">The messaging user is male.</span></span>
    
 <span data-ttu-id="164df-116">_genderCount_</span><span class="sxs-lookup"><span data-stu-id="164df-116">_genderCount_</span></span>
  
> <span data-ttu-id="164df-117">Количество различных значений, поддерживаемых для пола.</span><span class="sxs-lookup"><span data-stu-id="164df-117">The number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="164df-118">_genderMax_</span><span class="sxs-lookup"><span data-stu-id="164df-118">_genderMax_</span></span>
  
> <span data-ttu-id="164df-119">Максимальное количество различных значений, поддерживаемых для пола.</span><span class="sxs-lookup"><span data-stu-id="164df-119">The maximum number of different values supported for the gender.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="164df-120">См. также</span><span class="sxs-lookup"><span data-stu-id="164df-120">See also</span></span>



[<span data-ttu-id="164df-121">Каноническое свойство PidTagGender</span><span class="sxs-lookup"><span data-stu-id="164df-121">PidTagGender Canonical Property</span></span>](pidtaggender-canonical-property.md)

