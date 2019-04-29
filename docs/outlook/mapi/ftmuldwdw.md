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
ms.openlocfilehash: 54561450e7d91d8a30695dacf508758623547e39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412914"
---
# <a name="ftmuldwdw"></a><span data-ttu-id="9b94d-103">FtMulDwDw</span><span class="sxs-lookup"><span data-stu-id="9b94d-103">FtMulDwDw</span></span>

  
  
<span data-ttu-id="9b94d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b94d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b94d-105">Умножает одно целое число без знака 32 на другое.</span><span class="sxs-lookup"><span data-stu-id="9b94d-105">Multiplies one unsigned 32-bit integer by another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9b94d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9b94d-106">Header file:</span></span>  <br/> |<span data-ttu-id="9b94d-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="9b94d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9b94d-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="9b94d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9b94d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9b94d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9b94d-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="9b94d-110">Called by:</span></span>  <br/> |<span data-ttu-id="9b94d-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="9b94d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a><span data-ttu-id="9b94d-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b94d-112">Parameters</span></span>

 <span data-ttu-id="9b94d-113">_Мултипликанд_</span><span class="sxs-lookup"><span data-stu-id="9b94d-113">_Multiplicand_</span></span>
  
> <span data-ttu-id="9b94d-114">возврата Двойное слово, содержащее Неподписанное 32 — разрядное целое число, умноженное на значение параметра множителя __ .</span><span class="sxs-lookup"><span data-stu-id="9b94d-114">[in] A double word that contains the unsigned 32-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
 <span data-ttu-id="9b94d-115">_Умножителя_</span><span class="sxs-lookup"><span data-stu-id="9b94d-115">_Multiplier_</span></span>
  
> <span data-ttu-id="9b94d-116">возврата Двойное слово, содержащее Неподписанное 32 — разрядное значение множителя.</span><span class="sxs-lookup"><span data-stu-id="9b94d-116">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9b94d-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b94d-117">Return value</span></span>

<span data-ttu-id="9b94d-118">Функция **фтмулдвдв** возвращает структуру [fileTime](filetime.md) , содержащую произведение двух целых чисел.</span><span class="sxs-lookup"><span data-stu-id="9b94d-118">The **FtMulDwDw** function returns a [FILETIME](filetime.md) structure that contains the product of the two integers.</span></span> <span data-ttu-id="9b94d-119">Два входных параметра остаются неизменными.</span><span class="sxs-lookup"><span data-stu-id="9b94d-119">The two input parameters remain unchanged.</span></span> 
  

