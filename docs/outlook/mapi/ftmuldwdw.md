---
title: FtMulDwDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDwDw
api_type:
- COM
ms.assetid: 8c1a342c-d7ae-4e26-b327-a63cdd3c3ee6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 16dca82b94225afc88bcb6c4e698a50565d6b088
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808517"
---
# <a name="ftmuldwdw"></a><span data-ttu-id="09515-103">FtMulDwDw</span><span class="sxs-lookup"><span data-stu-id="09515-103">FtMulDwDw</span></span>

  
  
<span data-ttu-id="09515-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="09515-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="09515-105">Умножает один целых 32-разрядная версия на другой.</span><span class="sxs-lookup"><span data-stu-id="09515-105">Multiplies one unsigned 32-bit integer by another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="09515-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="09515-106">Header file:</span></span>  <br/> |<span data-ttu-id="09515-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="09515-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="09515-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="09515-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="09515-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="09515-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="09515-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="09515-110">Called by:</span></span>  <br/> |<span data-ttu-id="09515-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="09515-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a><span data-ttu-id="09515-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="09515-112">Parameters</span></span>

 <span data-ttu-id="09515-113">_Множитель_</span><span class="sxs-lookup"><span data-stu-id="09515-113">_Multiplicand_</span></span>
  
> <span data-ttu-id="09515-114">[in] Двойное слово, содержащий целых 32-разрядная версия умножается на значение параметра _Множитель_ .</span><span class="sxs-lookup"><span data-stu-id="09515-114">[in] A double word that contains the unsigned 32-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
 <span data-ttu-id="09515-115">_Множитель_</span><span class="sxs-lookup"><span data-stu-id="09515-115">_Multiplier_</span></span>
  
> <span data-ttu-id="09515-116">[in] Двойное слово, содержащий множитель неподписанных 32-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="09515-116">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="09515-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7">Return value</span></span>

<span data-ttu-id="09515-118">Функция **FtMulDwDw** возвращает структуру [FILETIME](filetime.md) , содержащую произведение двух целых чисел.</span><span class="sxs-lookup"><span data-stu-id="09515-118">The **FtMulDwDw** function returns a [FILETIME](filetime.md) structure that contains the product of the two integers.</span></span> <span data-ttu-id="09515-119">Два входных параметра не изменяются.</span><span class="sxs-lookup"><span data-stu-id="09515-119">The two input parameters remain unchanged.</span></span> 
  

