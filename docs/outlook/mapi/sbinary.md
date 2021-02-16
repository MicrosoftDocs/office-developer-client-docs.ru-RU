---
title: SBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinary
api_type:
- COM
ms.assetid: f21b5e6c-7a63-46bf-acbf-0e042e3519f7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 38263f46ccb50e1836f31d457f54f52abca7ce9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407846"
---
# <a name="sbinary"></a><span data-ttu-id="8ae63-103">SBinary</span><span class="sxs-lookup"><span data-stu-id="8ae63-103">SBinary</span></span>

  
  
<span data-ttu-id="8ae63-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ae63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ae63-105">Описывает свойство типа PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="8ae63-105">Describes a property of type PT_BINARY.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8ae63-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8ae63-106">Header file:</span></span>  <br/> |<span data-ttu-id="8ae63-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8ae63-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a><span data-ttu-id="8ae63-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="8ae63-108">Members</span></span>

 <span data-ttu-id="8ae63-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="8ae63-109">**cb**</span></span>
  
> <span data-ttu-id="8ae63-110">Количество в **lpb-члене.**</span><span class="sxs-lookup"><span data-stu-id="8ae63-110">Count of bytes in the **lpb** member.</span></span> 
    
 <span data-ttu-id="8ae63-111">**lpb**</span><span class="sxs-lookup"><span data-stu-id="8ae63-111">**lpb**</span></span>
  
> <span data-ttu-id="8ae63-112">Указатель на PT_BINARY свойства.</span><span class="sxs-lookup"><span data-stu-id="8ae63-112">Pointer to the PT_BINARY property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8ae63-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ae63-113">Remarks</span></span>

<span data-ttu-id="8ae63-114">Сведения о типах свойств см. в обзоре [типов свойств MAPI.](mapi-property-type-overview.md)</span><span class="sxs-lookup"><span data-stu-id="8ae63-114">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8ae63-115">См. также</span><span class="sxs-lookup"><span data-stu-id="8ae63-115">See also</span></span>



[<span data-ttu-id="8ae63-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8ae63-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="8ae63-117">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="8ae63-117">MAPI Structures</span></span>](mapi-structures.md)

