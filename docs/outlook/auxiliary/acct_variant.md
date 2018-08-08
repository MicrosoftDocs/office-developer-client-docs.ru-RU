---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: Переменная этого типа данных содержит значение свойства, которое имеет тип данных variant.
ms.openlocfilehash: c85af4bd4fefffb4fadf671bb7cf5b7f072d5e95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807680"
---
# <a name="acctvariant"></a><span data-ttu-id="75057-103">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="75057-103">ACCT_VARIANT</span></span>

<span data-ttu-id="75057-104">Переменная этого типа данных содержит значение свойства, которое имеет тип данных variant.</span><span class="sxs-lookup"><span data-stu-id="75057-104">A variable of this data type holds the value of a property, which is of a variant data type.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="75057-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="75057-105">Quick info</span></span>

```cpp
typedef struct 
    { 
        DWORD dwType; 
        union  
            { 
            DWORD dw; 
            WCHAR *pwsz; 
            ACCT_BIN bin; 
            } Val; 
    } ACCT_VARIANT; 

```

## <a name="members"></a><span data-ttu-id="75057-106">Members</span><span class="sxs-lookup"><span data-stu-id="75057-106">Members</span></span>

<span data-ttu-id="75057-107">_dwType_</span><span class="sxs-lookup"><span data-stu-id="75057-107">_dwType_</span></span>
  
> <span data-ttu-id="75057-108">Тип variant:</span><span class="sxs-lookup"><span data-stu-id="75057-108">Type of variant:</span></span>
    
    - <span data-ttu-id="75057-109">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="75057-109">PT_LONG</span></span>
    
    - <span data-ttu-id="75057-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="75057-110">PT_UNICODE</span></span>
    
    - <span data-ttu-id="75057-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="75057-111">PT_BINARY</span></span>
    
<span data-ttu-id="75057-112">_DW_</span><span class="sxs-lookup"><span data-stu-id="75057-112">_dw_</span></span>
  
> <span data-ttu-id="75057-113">Значение DWORD значение типа variant.</span><span class="sxs-lookup"><span data-stu-id="75057-113">DWORD value of variant.</span></span>
    
<span data-ttu-id="75057-114">_pwsz_</span><span class="sxs-lookup"><span data-stu-id="75057-114">_pwsz_</span></span>
  
> <span data-ttu-id="75057-115">Строковое значение типа variant.</span><span class="sxs-lookup"><span data-stu-id="75057-115">String value of variant.</span></span>
    
<span data-ttu-id="75057-116">_корзины_</span><span class="sxs-lookup"><span data-stu-id="75057-116">_bin_</span></span>
  
> <span data-ttu-id="75057-117">Двоичное значение типа variant.</span><span class="sxs-lookup"><span data-stu-id="75057-117">Binary value of the variant.</span></span>
    

