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
ms.openlocfilehash: 8002698b1644fb63292b4242d4fb3d784a99a03f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592026"
---
# <a name="ftmuldwdw"></a><span data-ttu-id="8c7e1-103">FtMulDwDw</span><span class="sxs-lookup"><span data-stu-id="8c7e1-103">FtMulDwDw</span></span>

  
  
<span data-ttu-id="8c7e1-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c7e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c7e1-105">Умножает один целых 32-разрядная версия на другой.</span><span class="sxs-lookup"><span data-stu-id="8c7e1-105">Multiplies one unsigned 32-bit integer by another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8c7e1-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8c7e1-106">Header file:</span></span>  <br/> |<span data-ttu-id="8c7e1-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="8c7e1-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="8c7e1-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="8c7e1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8c7e1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8c7e1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8c7e1-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="8c7e1-110">Called by:</span></span>  <br/> |<span data-ttu-id="8c7e1-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="8c7e1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a><span data-ttu-id="8c7e1-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c7e1-112">Parameters</span></span>

 <span data-ttu-id="8c7e1-113">_Множитель_</span><span class="sxs-lookup"><span data-stu-id="8c7e1-113">_Multiplicand_</span></span>
  
> <span data-ttu-id="8c7e1-114">[in] Двойное слово, содержащий целых 32-разрядная версия умножается на значение параметра _Множитель_ .</span><span class="sxs-lookup"><span data-stu-id="8c7e1-114">[in] A double word that contains the unsigned 32-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
 <span data-ttu-id="8c7e1-115">_Множитель_</span><span class="sxs-lookup"><span data-stu-id="8c7e1-115">_Multiplier_</span></span>
  
> <span data-ttu-id="8c7e1-116">[in] Двойное слово, содержащий множитель неподписанных 32-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="8c7e1-116">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8c7e1-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="8c7e1-117">Return value</span></span>

<span data-ttu-id="8c7e1-118">Функция **FtMulDwDw** возвращает структуру [FILETIME](filetime.md) , содержащую произведение двух целых чисел.</span><span class="sxs-lookup"><span data-stu-id="8c7e1-118">The **FtMulDwDw** function returns a [FILETIME](filetime.md) structure that contains the product of the two integers.</span></span> <span data-ttu-id="8c7e1-119">Два входных параметра не изменяются.</span><span class="sxs-lookup"><span data-stu-id="8c7e1-119">The two input parameters remain unchanged.</span></span> 
  

