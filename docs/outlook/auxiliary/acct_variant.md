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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316921"
---
# <a name="acctvariant"></a><span data-ttu-id="b805b-103">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="b805b-103">ACCT_VARIANT</span></span>

<span data-ttu-id="b805b-104">Переменная этого типа данных содержит значение свойства, которое относится к типу данных Variant.</span><span class="sxs-lookup"><span data-stu-id="b805b-104">A variable of this data type holds the value of a property, which is of a variant data type.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b805b-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="b805b-105">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="b805b-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="b805b-106">Members</span></span>

<span data-ttu-id="b805b-107">_Двтипе_</span><span class="sxs-lookup"><span data-stu-id="b805b-107">_dwType_</span></span>
  
> <span data-ttu-id="b805b-108">Тип варианта:</span><span class="sxs-lookup"><span data-stu-id="b805b-108">Type of variant:</span></span>
    
    - <span data-ttu-id="b805b-109">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b805b-109">PT_LONG</span></span>
    
    - <span data-ttu-id="b805b-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b805b-110">PT_UNICODE</span></span>
    
    - <span data-ttu-id="b805b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b805b-111">PT_BINARY</span></span>
    
<span data-ttu-id="b805b-112">_хранилищ_</span><span class="sxs-lookup"><span data-stu-id="b805b-112">_dw_</span></span>
  
> <span data-ttu-id="b805b-113">Значение Variant типа DWORD.</span><span class="sxs-lookup"><span data-stu-id="b805b-113">DWORD value of variant.</span></span>
    
<span data-ttu-id="b805b-114">_пвсз_</span><span class="sxs-lookup"><span data-stu-id="b805b-114">_pwsz_</span></span>
  
> <span data-ttu-id="b805b-115">Строковое значение Variant.</span><span class="sxs-lookup"><span data-stu-id="b805b-115">String value of variant.</span></span>
    
<span data-ttu-id="b805b-116">_bin_</span><span class="sxs-lookup"><span data-stu-id="b805b-116">_bin_</span></span>
  
> <span data-ttu-id="b805b-117">Двоичное значение Variant.</span><span class="sxs-lookup"><span data-stu-id="b805b-117">Binary value of the variant.</span></span>
    

