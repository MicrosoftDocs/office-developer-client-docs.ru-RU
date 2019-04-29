---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: Переменная этого типа данных содержит значение свойства, которое относится к типу данных Variant.
ms.openlocfilehash: 124cfaef40e63d60e2e9c6681884bfb57a043dde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424401"
---
# <a name="acctvariant"></a><span data-ttu-id="5d857-103">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="5d857-103">ACCT_VARIANT</span></span>

<span data-ttu-id="5d857-104">Переменная этого типа данных содержит значение свойства, которое относится к типу данных Variant.</span><span class="sxs-lookup"><span data-stu-id="5d857-104">A variable of this data type holds the value of a property, which is of a variant data type.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5d857-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="5d857-105">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="5d857-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="5d857-106">Members</span></span>

<span data-ttu-id="5d857-107">_Двтипе_</span><span class="sxs-lookup"><span data-stu-id="5d857-107">_dwType_</span></span>
  
> <span data-ttu-id="5d857-108">Тип варианта:</span><span class="sxs-lookup"><span data-stu-id="5d857-108">Type of variant:</span></span>
    
    - <span data-ttu-id="5d857-109">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5d857-109">PT_LONG</span></span>
    
    - <span data-ttu-id="5d857-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5d857-110">PT_UNICODE</span></span>
    
    - <span data-ttu-id="5d857-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5d857-111">PT_BINARY</span></span>
    
<span data-ttu-id="5d857-112">_хранилищ_</span><span class="sxs-lookup"><span data-stu-id="5d857-112">_dw_</span></span>
  
> <span data-ttu-id="5d857-113">Значение Variant типа DWORD.</span><span class="sxs-lookup"><span data-stu-id="5d857-113">DWORD value of variant.</span></span>
    
<span data-ttu-id="5d857-114">_пвсз_</span><span class="sxs-lookup"><span data-stu-id="5d857-114">_pwsz_</span></span>
  
> <span data-ttu-id="5d857-115">Строковое значение Variant.</span><span class="sxs-lookup"><span data-stu-id="5d857-115">String value of variant.</span></span>
    
<span data-ttu-id="5d857-116">_bin_</span><span class="sxs-lookup"><span data-stu-id="5d857-116">_bin_</span></span>
  
> <span data-ttu-id="5d857-117">Двоичное значение Variant.</span><span class="sxs-lookup"><span data-stu-id="5d857-117">Binary value of the variant.</span></span>
    

