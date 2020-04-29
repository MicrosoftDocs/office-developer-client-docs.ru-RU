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
ms.openlocfilehash: cb20469adec938817fedf1b00789304625b388c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404766"
---
# <a name="ftaddft"></a><span data-ttu-id="d7793-103">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="d7793-103">FtAddFt</span></span>

  
  
<span data-ttu-id="d7793-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7793-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7793-105">Добавляет одно целое число без знака 64 в другое.</span><span class="sxs-lookup"><span data-stu-id="d7793-105">Adds one unsigned 64-bit integer to another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d7793-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d7793-106">Header file:</span></span>  <br/> |<span data-ttu-id="d7793-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="d7793-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d7793-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="d7793-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d7793-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d7793-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d7793-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="d7793-110">Called by:</span></span>  <br/> |<span data-ttu-id="d7793-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="d7793-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a><span data-ttu-id="d7793-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7793-112">Parameters</span></span>

 <span data-ttu-id="d7793-113">_Addend1_</span><span class="sxs-lookup"><span data-stu-id="d7793-113">_Addend1_</span></span>
  
> <span data-ttu-id="d7793-114">возврата Структура [fileTime](filetime.md) , содержащая первое 64 – разрядное целое число, которое требуется добавить.</span><span class="sxs-lookup"><span data-stu-id="d7793-114">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="d7793-115">_Addend2_</span><span class="sxs-lookup"><span data-stu-id="d7793-115">_Addend2_</span></span>
  
> <span data-ttu-id="d7793-116">возврата Структура **fileTime** , содержащая второе 64 – разрядное целое число, которое требуется добавить.</span><span class="sxs-lookup"><span data-stu-id="d7793-116">[in] A **FILETIME** structure that contains the second unsigned 64-bit integer to be added.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d7793-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7793-117">Return value</span></span>

<span data-ttu-id="d7793-118">Функция **фтаддфт** возвращает структуру **fileTime** , которая содержит сумму двух целых чисел.</span><span class="sxs-lookup"><span data-stu-id="d7793-118">The **FtAddFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="d7793-119">Два входных параметра остаются неизменными.</span><span class="sxs-lookup"><span data-stu-id="d7793-119">The two input parameters remain unchanged.</span></span> 
  

