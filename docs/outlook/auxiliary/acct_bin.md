---
title: ACCT_BIN
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5b57296c-61d7-e517-7ab7-44a9cc1f7ffc
description: Переменная этого типа данных имеет двоичное значение.
ms.openlocfilehash: 8299230a30b65ef8fb7856dc74618dd15ae218ac
ms.sourcegitcommit: 66e74e39f44dca8c41f97f05528b8f9eb1aaed87
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "52061337"
---
# <a name="acct_bin"></a><span data-ttu-id="8d5d6-103">ACCT_BIN</span><span class="sxs-lookup"><span data-stu-id="8d5d6-103">ACCT_BIN</span></span>

<span data-ttu-id="8d5d6-104">Переменная этого типа данных имеет двоичное значение.</span><span class="sxs-lookup"><span data-stu-id="8d5d6-104">A variable of this data type holds a binary value.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8d5d6-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="8d5d6-105">Quick info</span></span>

```cpp
typedef struct { 
    DWORD cb; 
    BYTE * pb; 
} ACCT_BIN; 

```

## <a name="members"></a><span data-ttu-id="8d5d6-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="8d5d6-106">Members</span></span>

<span data-ttu-id="8d5d6-107">_cb_</span><span class="sxs-lookup"><span data-stu-id="8d5d6-107">_cb_</span></span>
  
> <span data-ttu-id="8d5d6-108">Количество bytes, на которое _указывает pb._</span><span class="sxs-lookup"><span data-stu-id="8d5d6-108">Number of bytes that  _pb_ points to.</span></span> 
    
<span data-ttu-id="8d5d6-109">_pb_</span><span class="sxs-lookup"><span data-stu-id="8d5d6-109">_pb_</span></span>
  
> <span data-ttu-id="8d5d6-110">Указатель на двоичные сведения.</span><span class="sxs-lookup"><span data-stu-id="8d5d6-110">Pointer to binary information.</span></span>
    

