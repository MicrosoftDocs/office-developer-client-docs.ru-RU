---
title: FtAddFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtAddFt
api_type:
- COM
ms.assetid: 341ad06b-1caa-49bb-b859-cb512f6fb55d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4b02fc316001ae11d64988cc29d0e62e9adde55e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585586"
---
# <a name="ftaddft"></a><span data-ttu-id="47da7-103">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="47da7-103">FtAddFt</span></span>

  
  
<span data-ttu-id="47da7-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47da7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47da7-105">Добавление одного целых 64-разрядная версия на другой.</span><span class="sxs-lookup"><span data-stu-id="47da7-105">Adds one unsigned 64-bit integer to another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="47da7-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="47da7-106">Header file:</span></span>  <br/> |<span data-ttu-id="47da7-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="47da7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="47da7-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="47da7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="47da7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="47da7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="47da7-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="47da7-110">Called by:</span></span>  <br/> |<span data-ttu-id="47da7-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="47da7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a><span data-ttu-id="47da7-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="47da7-112">Parameters</span></span>

 <span data-ttu-id="47da7-113">_Addend1_</span><span class="sxs-lookup"><span data-stu-id="47da7-113">_Addend1_</span></span>
  
> <span data-ttu-id="47da7-114">[in] Структура [FILETIME](filetime.md) , содержащую первого целого числа без знака 64-разрядная версия будет добавлена.</span><span class="sxs-lookup"><span data-stu-id="47da7-114">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="47da7-115">_Addend2_</span><span class="sxs-lookup"><span data-stu-id="47da7-115">_Addend2_</span></span>
  
> <span data-ttu-id="47da7-116">[in] Структура **FILETIME** , содержащий второй целого числа без знака 64-разрядная версия будет добавлена.</span><span class="sxs-lookup"><span data-stu-id="47da7-116">[in] A **FILETIME** structure that contains the second unsigned 64-bit integer to be added.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="47da7-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="47da7-117">Return value</span></span>

<span data-ttu-id="47da7-118">Функция **FtAddFt** возвращает структуру **FILETIME** , содержащую сумма двух целых чисел.</span><span class="sxs-lookup"><span data-stu-id="47da7-118">The **FtAddFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="47da7-119">Два входных параметра не изменяются.</span><span class="sxs-lookup"><span data-stu-id="47da7-119">The two input parameters remain unchanged.</span></span> 
  

