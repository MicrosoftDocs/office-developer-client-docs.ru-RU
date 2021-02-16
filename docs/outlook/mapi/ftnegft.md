---
title: FtNegFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtNegFt
api_type:
- COM
ms.assetid: 639a408c-aed1-456b-9f75-9d6fb8dcb33b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: db208dad8697060e394b3ee037ea658cefbab669
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423386"
---
# <a name="ftnegft"></a><span data-ttu-id="55fc3-103">FtNegFt</span><span class="sxs-lookup"><span data-stu-id="55fc3-103">FtNegFt</span></span>

  
  
<span data-ttu-id="55fc3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55fc3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55fc3-105">Вычисляет два дополнения 64-битного 64-битного 64-битного.</span><span class="sxs-lookup"><span data-stu-id="55fc3-105">Computes the two's complement of an unsigned 64-bit integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="55fc3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="55fc3-106">Header file:</span></span>  <br/> |<span data-ttu-id="55fc3-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="55fc3-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="55fc3-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="55fc3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="55fc3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="55fc3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="55fc3-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="55fc3-110">Called by:</span></span>  <br/> |<span data-ttu-id="55fc3-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="55fc3-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a><span data-ttu-id="55fc3-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="55fc3-112">Parameters</span></span>

 <span data-ttu-id="55fc3-113">_ft_</span><span class="sxs-lookup"><span data-stu-id="55fc3-113">_ft_</span></span>
  
> <span data-ttu-id="55fc3-114">[in] Структура [FILETIME,](filetime.md) которая содержит неподписаное 64-битное 64-битное количество, для которого вычисляется дополнение этих двух файлов.</span><span class="sxs-lookup"><span data-stu-id="55fc3-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer for which to compute the two's complement.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="55fc3-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55fc3-115">Return value</span></span>

<span data-ttu-id="55fc3-116">Функция **FtNegFt** возвращает структуру **FILETIME,** которая содержит два дополнения для всего.</span><span class="sxs-lookup"><span data-stu-id="55fc3-116">The **FtNegFt** function returns a **FILETIME** structure that contains the two's complement of the integer.</span></span> <span data-ttu-id="55fc3-117">Входной параметр остается без изменений.</span><span class="sxs-lookup"><span data-stu-id="55fc3-117">The input parameter remains unchanged.</span></span> 
  

