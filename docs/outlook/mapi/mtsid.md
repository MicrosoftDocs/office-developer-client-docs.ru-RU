---
title: MTSID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MTSID
api_type:
- COM
ms.assetid: 3d9bc643-332f-4c8e-83e6-ce9b15711945
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 96da91acec741322e6c07c64555171d35f0f7e00
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342772"
---
# <a name="mtsid"></a><span data-ttu-id="89926-103">MTSID</span><span class="sxs-lookup"><span data-stu-id="89926-103">MTSID</span></span>

  
  
<span data-ttu-id="89926-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89926-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89926-105">Содержит идентификатор записи системы передачи сообщений X. 400 (MTS).</span><span class="sxs-lookup"><span data-stu-id="89926-105">Contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="89926-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="89926-106">Header file:</span></span>  <br/> |<span data-ttu-id="89926-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="89926-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="89926-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="89926-108">Related macros:</span></span>  <br/> |<span data-ttu-id="89926-109">[Кбмтсид](cbmtsid.md), [кбневмтсид](cbnewmtsid.md)</span><span class="sxs-lookup"><span data-stu-id="89926-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a><span data-ttu-id="89926-110">Members</span><span class="sxs-lookup"><span data-stu-id="89926-110">Members</span></span>

 <span data-ttu-id="89926-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="89926-111">**cb**</span></span>
  
> <span data-ttu-id="89926-112">Количество байтов в массиве, описываемом элементом **абентри** .</span><span class="sxs-lookup"><span data-stu-id="89926-112">Count of bytes in the array described by the **abEntry** member.</span></span> 
    
 <span data-ttu-id="89926-113">**Абентри**</span><span class="sxs-lookup"><span data-stu-id="89926-113">**abEntry**</span></span>
  
> <span data-ttu-id="89926-114">Массив байтов, который содержит данные идентификатора записи MTS.</span><span class="sxs-lookup"><span data-stu-id="89926-114">Byte array that contains the MTS entry identifier data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="89926-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89926-115">Remarks</span></span>

<span data-ttu-id="89926-116">Структура **мтсид** используется только для сопоставлений X. 400 идентификаторов записей MAPI.</span><span class="sxs-lookup"><span data-stu-id="89926-116">The **MTSID** structure is used only for X.400 mappings of MAPI entry identifiers.</span></span> <span data-ttu-id="89926-117">Он соответствует структуре MAPI [флатентри](flatentry.md) .</span><span class="sxs-lookup"><span data-stu-id="89926-117">It corresponds to the MAPI [FLATENTRY](flatentry.md) structure.</span></span> 
  
<span data-ttu-id="89926-118">Идентификатор MTS имеет тот же формат, что и идентификатор записи MAPI, или двоичное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="89926-118">An MTS identifier has the same format as a MAPI entry identifier or a binary property value.</span></span> <span data-ttu-id="89926-119">Идентификаторы MTS могут быть особенно полезными для отмены отложенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="89926-119">MTS identifiers can be particularly useful for canceling deferred messages.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="89926-120">См. также</span><span class="sxs-lookup"><span data-stu-id="89926-120">See also</span></span>



[<span data-ttu-id="89926-121">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="89926-121">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="89926-122">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="89926-122">FLATMTSIDLIST</span></span>](flatmtsidlist.md)


[<span data-ttu-id="89926-123">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="89926-123">MAPI Structures</span></span>](mapi-structures.md)

