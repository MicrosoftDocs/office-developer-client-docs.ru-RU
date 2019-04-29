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
ms.openlocfilehash: 353bc574ca5987d71faf4841744de30a3d6c3f19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435413"
---
# <a name="smapiformpropenumval"></a><span data-ttu-id="d4da1-103">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="d4da1-103">SMAPIFormPropEnumVal</span></span>

  
  
<span data-ttu-id="d4da1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4da1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4da1-105">Сопоставляет перечисленное целое число с отображаемым именем для этого значения.</span><span class="sxs-lookup"><span data-stu-id="d4da1-105">Maps an enumerated integer value to a display name for that value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d4da1-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d4da1-106">Header file:</span></span>  <br/> |<span data-ttu-id="d4da1-107">Мапиформ. h</span><span class="sxs-lookup"><span data-stu-id="d4da1-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a><span data-ttu-id="d4da1-108">Members</span><span class="sxs-lookup"><span data-stu-id="d4da1-108">Members</span></span>

 <span data-ttu-id="d4da1-109">**Псздисплайнаме**</span><span class="sxs-lookup"><span data-stu-id="d4da1-109">**pszDisplayName**</span></span>
  
> <span data-ttu-id="d4da1-110">Строка, содержащая отображаемое имя для значения, указанного в элементе **нвал** .</span><span class="sxs-lookup"><span data-stu-id="d4da1-110">String that contains the display name for the value specified in the **nVal** member.</span></span> 
    
 <span data-ttu-id="d4da1-111">**Нвал**</span><span class="sxs-lookup"><span data-stu-id="d4da1-111">**nVal**</span></span>
  
> <span data-ttu-id="d4da1-112">Значение перечисления для отображаемого имени, на которое указывает элемент **псздисплайнаме** .</span><span class="sxs-lookup"><span data-stu-id="d4da1-112">An enumeration value for the display name pointed to by the **pszDisplayName** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d4da1-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="d4da1-113">Remarks</span></span>

<span data-ttu-id="d4da1-114">Когда пользователь выбирает отображаемое имя из формы, соответствующее значение перечисления сохраняется с использованием реализации интерфейса [IMAPIProp](imapipropiunknown.md) , связанной с формой.</span><span class="sxs-lookup"><span data-stu-id="d4da1-114">When a user selects a display name from a form, the name's corresponding enumeration value is stored by using the [IMAPIProp](imapipropiunknown.md) interface implementation that is associated with the form.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d4da1-115">См. также</span><span class="sxs-lookup"><span data-stu-id="d4da1-115">See also</span></span>



[<span data-ttu-id="d4da1-116">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="d4da1-116">SMAPIFormProp</span></span>](smapiformprop.md)
  
[<span data-ttu-id="d4da1-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d4da1-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="d4da1-118">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="d4da1-118">MAPI Structures</span></span>](mapi-structures.md)

