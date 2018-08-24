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
ms.openlocfilehash: 2c49a17389a9bfc998f892e0becf96dca4cd773f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578719"
---
# <a name="smapiformpropenumval"></a><span data-ttu-id="1f09d-103">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="1f09d-103">SMAPIFormPropEnumVal</span></span>

  
  
<span data-ttu-id="1f09d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f09d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f09d-105">Сопоставляет перечисляемые целое значение отображаемое имя для этого значения.</span><span class="sxs-lookup"><span data-stu-id="1f09d-105">Maps an enumerated integer value to a display name for that value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1f09d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1f09d-106">Header file:</span></span>  <br/> |<span data-ttu-id="1f09d-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="1f09d-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a><span data-ttu-id="1f09d-108">Members</span><span class="sxs-lookup"><span data-stu-id="1f09d-108">Members</span></span>

 <span data-ttu-id="1f09d-109">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="1f09d-109">**pszDisplayName**</span></span>
  
> <span data-ttu-id="1f09d-110">Строка, содержащая отображаемое имя для значения, указанного в элементе **nVal** .</span><span class="sxs-lookup"><span data-stu-id="1f09d-110">String that contains the display name for the value specified in the **nVal** member.</span></span> 
    
 <span data-ttu-id="1f09d-111">**nVal**</span><span class="sxs-lookup"><span data-stu-id="1f09d-111">**nVal**</span></span>
  
> <span data-ttu-id="1f09d-112">Значение перечисления в поле отображаемое имя, на который указывает член **pszDisplayName** .</span><span class="sxs-lookup"><span data-stu-id="1f09d-112">An enumeration value for the display name pointed to by the **pszDisplayName** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1f09d-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="1f09d-113">Remarks</span></span>

<span data-ttu-id="1f09d-114">Когда пользователь выбирает отображаемое имя из формы, соответствующее значение перечисления имя хранится с помощью реализации интерфейса [IMAPIProp](imapipropiunknown.md) , связанный с формой.</span><span class="sxs-lookup"><span data-stu-id="1f09d-114">When a user selects a display name from a form, the name's corresponding enumeration value is stored by using the [IMAPIProp](imapipropiunknown.md) interface implementation that is associated with the form.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1f09d-115">См. также</span><span class="sxs-lookup"><span data-stu-id="1f09d-115">See also</span></span>



[<span data-ttu-id="1f09d-116">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="1f09d-116">SMAPIFormProp</span></span>](smapiformprop.md)
  
[<span data-ttu-id="1f09d-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="1f09d-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="1f09d-118">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="1f09d-118">MAPI Structures</span></span>](mapi-structures.md)

