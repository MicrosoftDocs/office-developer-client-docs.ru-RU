---
title: SMAPIFormPropEnumVal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropEnumVal
api_type:
- COM
ms.assetid: 694d40e9-cff2-435e-ad90-446044c306d2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bae750e7e940bc1417b3d225c9c81129e9da77b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812331"
---
# <a name="smapiformpropenumval"></a><span data-ttu-id="0f6cd-103">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="0f6cd-103">SMAPIFormPropEnumVal</span></span>

  
  
<span data-ttu-id="0f6cd-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0f6cd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0f6cd-105">Сопоставляет перечисляемые целое значение отображаемое имя для этого значения.</span><span class="sxs-lookup"><span data-stu-id="0f6cd-105">Maps an enumerated integer value to a display name for that value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0f6cd-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="0f6cd-106">Header file:</span></span>  <br/> |<span data-ttu-id="0f6cd-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="0f6cd-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a><span data-ttu-id="0f6cd-108">Members</span><span class="sxs-lookup"><span data-stu-id="0f6cd-108">Members</span></span>

 <span data-ttu-id="0f6cd-109">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="0f6cd-109">**pszDisplayName**</span></span>
  
> <span data-ttu-id="0f6cd-110">Строка, содержащая отображаемое имя для значения, указанного в элементе **nVal** .</span><span class="sxs-lookup"><span data-stu-id="0f6cd-110">String that contains the display name for the value specified in the **nVal** member.</span></span> 
    
 <span data-ttu-id="0f6cd-111">**nVal**</span><span class="sxs-lookup"><span data-stu-id="0f6cd-111">**nVal**</span></span>
  
> <span data-ttu-id="0f6cd-112">Значение перечисления в поле отображаемое имя, на который указывает член **pszDisplayName** .</span><span class="sxs-lookup"><span data-stu-id="0f6cd-112">An enumeration value for the display name pointed to by the **pszDisplayName** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0f6cd-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="0f6cd-113">Remarks</span></span>

<span data-ttu-id="0f6cd-114">Когда пользователь выбирает отображаемое имя из формы, соответствующее значение перечисления имя хранится с помощью реализации интерфейса [IMAPIProp](imapipropiunknown.md) , связанный с формой.</span><span class="sxs-lookup"><span data-stu-id="0f6cd-114">When a user selects a display name from a form, the name's corresponding enumeration value is stored by using the [IMAPIProp](imapipropiunknown.md) interface implementation that is associated with the form.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0f6cd-115">См. также</span><span class="sxs-lookup"><span data-stu-id="0f6cd-115">See also</span></span>



[<span data-ttu-id="0f6cd-116">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="0f6cd-116">SMAPIFormProp</span></span>](smapiformprop.md)
  
[<span data-ttu-id="0f6cd-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="0f6cd-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="0f6cd-118">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="0f6cd-118">MAPI Structures</span></span>](mapi-structures.md)

