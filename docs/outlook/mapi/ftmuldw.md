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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 861a48464193f357224e33eb0348bc7d5372aa10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808513"
---
# <a name="ftmuldw"></a><span data-ttu-id="0fc18-103">FtMulDw</span><span class="sxs-lookup"><span data-stu-id="0fc18-103">FtMulDw</span></span>

  
  
<span data-ttu-id="0fc18-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0fc18-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0fc18-105">Умножает целых 64-разрядная версия с 32-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="0fc18-105">Multiplies an unsigned 64-bit integer by an unsigned 32-bit integer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0fc18-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="0fc18-106">Header file:</span></span>  <br/> |<span data-ttu-id="0fc18-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0fc18-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0fc18-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="0fc18-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0fc18-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0fc18-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0fc18-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="0fc18-110">Called by:</span></span>  <br/> |<span data-ttu-id="0fc18-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="0fc18-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a><span data-ttu-id="0fc18-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="0fc18-112">Parameters</span></span>

 <span data-ttu-id="0fc18-113">_Множитель_</span><span class="sxs-lookup"><span data-stu-id="0fc18-113">_Multiplier_</span></span>
  
> <span data-ttu-id="0fc18-114">[in] Двойное слово, содержащий множитель неподписанных 32-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="0fc18-114">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span> 
    
 <span data-ttu-id="0fc18-115">_Множитель_</span><span class="sxs-lookup"><span data-stu-id="0fc18-115">_Multiplicand_</span></span>
  
> <span data-ttu-id="0fc18-116">[in] Структура [FILETIME](filetime.md) , содержащую целых 64-разрядная версия умножается на значение параметра _Множитель_ .</span><span class="sxs-lookup"><span data-stu-id="0fc18-116">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0fc18-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="0fc18-117">Return value</span></span>

<span data-ttu-id="0fc18-118">Функция **FtMulDw** возвращает структуру **FILETIME** , содержащую произведение двух целых чисел.</span><span class="sxs-lookup"><span data-stu-id="0fc18-118">The **FtMulDw** function returns a **FILETIME** structure that contains the product of the two integers.</span></span> <span data-ttu-id="0fc18-119">Два входных параметра не изменяются.</span><span class="sxs-lookup"><span data-stu-id="0fc18-119">The two input parameters remain unchanged.</span></span> 
  

