---
title: FtMulDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDw
api_type:
- COM
ms.assetid: e135ba67-97be-4ce0-a72e-93c49ed7d6e2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c823a4e3d08d9082a3b5ac5c4bd8169612caa16e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583997"
---
# <a name="ftmuldw"></a><span data-ttu-id="0d31a-103">FtMulDw</span><span class="sxs-lookup"><span data-stu-id="0d31a-103">FtMulDw</span></span>

  
  
<span data-ttu-id="0d31a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d31a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d31a-105">Умножает целых 64-разрядная версия с 32-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="0d31a-105">Multiplies an unsigned 64-bit integer by an unsigned 32-bit integer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0d31a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="0d31a-106">Header file:</span></span>  <br/> |<span data-ttu-id="0d31a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0d31a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0d31a-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="0d31a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0d31a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0d31a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0d31a-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="0d31a-110">Called by:</span></span>  <br/> |<span data-ttu-id="0d31a-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="0d31a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a><span data-ttu-id="0d31a-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d31a-112">Parameters</span></span>

 <span data-ttu-id="0d31a-113">_Множитель_</span><span class="sxs-lookup"><span data-stu-id="0d31a-113">_Multiplier_</span></span>
  
> <span data-ttu-id="0d31a-114">[in] Двойное слово, содержащий множитель неподписанных 32-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="0d31a-114">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span> 
    
 <span data-ttu-id="0d31a-115">_Множитель_</span><span class="sxs-lookup"><span data-stu-id="0d31a-115">_Multiplicand_</span></span>
  
> <span data-ttu-id="0d31a-116">[in] Структура [FILETIME](filetime.md) , содержащую целых 64-разрядная версия умножается на значение параметра _Множитель_ .</span><span class="sxs-lookup"><span data-stu-id="0d31a-116">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0d31a-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="0d31a-117">Return value</span></span>

<span data-ttu-id="0d31a-118">Функция **FtMulDw** возвращает структуру **FILETIME** , содержащую произведение двух целых чисел.</span><span class="sxs-lookup"><span data-stu-id="0d31a-118">The **FtMulDw** function returns a **FILETIME** structure that contains the product of the two integers.</span></span> <span data-ttu-id="0d31a-119">Два входных параметра не изменяются.</span><span class="sxs-lookup"><span data-stu-id="0d31a-119">The two input parameters remain unchanged.</span></span> 
  

