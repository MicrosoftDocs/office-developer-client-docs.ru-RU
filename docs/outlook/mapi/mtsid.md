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
ms.openlocfilehash: 59e9cf23aed2a389384318468c3853cd41c9ec1e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585684"
---
# <a name="mtsid"></a><span data-ttu-id="6e1f9-103">MTSID</span><span class="sxs-lookup"><span data-stu-id="6e1f9-103">MTSID</span></span>

  
  
<span data-ttu-id="6e1f9-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e1f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e1f9-105">Содержит идентификатор записи система X.400 сообщения транспорта.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-105">Contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e1f9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6e1f9-106">Header file:</span></span>  <br/> |<span data-ttu-id="6e1f9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6e1f9-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6e1f9-108">Связанные макросы:</span><span class="sxs-lookup"><span data-stu-id="6e1f9-108">Related macros:</span></span>  <br/> |<span data-ttu-id="6e1f9-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span><span class="sxs-lookup"><span data-stu-id="6e1f9-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a><span data-ttu-id="6e1f9-110">Members</span><span class="sxs-lookup"><span data-stu-id="6e1f9-110">Members</span></span>

 <span data-ttu-id="6e1f9-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="6e1f9-111">**cb**</span></span>
  
> <span data-ttu-id="6e1f9-112">Число байт в массиве описано участником **abEntry** .</span><span class="sxs-lookup"><span data-stu-id="6e1f9-112">Count of bytes in the array described by the **abEntry** member.</span></span> 
    
 <span data-ttu-id="6e1f9-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="6e1f9-113">**abEntry**</span></span>
  
> <span data-ttu-id="6e1f9-114">Массив байтов, который содержит данные идентификатор MTS запись.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-114">Byte array that contains the MTS entry identifier data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6e1f9-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="6e1f9-115">Remarks</span></span>

<span data-ttu-id="6e1f9-116">Структура **MTSID** используется только для сопоставления X.400 идентификаторов запись MAPI.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-116">The **MTSID** structure is used only for X.400 mappings of MAPI entry identifiers.</span></span> <span data-ttu-id="6e1f9-117">Оно соответствует MAPI [FLATENTRY](flatentry.md) структуры.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-117">It corresponds to the MAPI [FLATENTRY](flatentry.md) structure.</span></span> 
  
<span data-ttu-id="6e1f9-118">Идентификатор MTS имеет тот же формат как идентификатор записи MAPI или двоичного свойства значение.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-118">An MTS identifier has the same format as a MAPI entry identifier or a binary property value.</span></span> <span data-ttu-id="6e1f9-119">Идентификаторы MTS может быть полезно для отмены отложенные сообщения.</span><span class="sxs-lookup"><span data-stu-id="6e1f9-119">MTS identifiers can be particularly useful for canceling deferred messages.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6e1f9-120">См. также</span><span class="sxs-lookup"><span data-stu-id="6e1f9-120">See also</span></span>



[<span data-ttu-id="6e1f9-121">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="6e1f9-121">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="6e1f9-122">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="6e1f9-122">FLATMTSIDLIST</span></span>](flatmtsidlist.md)


[<span data-ttu-id="6e1f9-123">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="6e1f9-123">MAPI Structures</span></span>](mapi-structures.md)

