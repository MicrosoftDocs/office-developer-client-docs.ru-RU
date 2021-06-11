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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435175"
---
# <a name="mtsid"></a><span data-ttu-id="675e4-103">MTSID</span><span class="sxs-lookup"><span data-stu-id="675e4-103">MTSID</span></span>

  
  
<span data-ttu-id="675e4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="675e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="675e4-105">Содержит идентификатор входа транспортной системы сообщений X.400 (MTS).</span><span class="sxs-lookup"><span data-stu-id="675e4-105">Contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="675e4-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="675e4-106">Header file:</span></span>  <br/> |<span data-ttu-id="675e4-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="675e4-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="675e4-108">Связанные макрос:</span><span class="sxs-lookup"><span data-stu-id="675e4-108">Related macros:</span></span>  <br/> |<span data-ttu-id="675e4-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span><span class="sxs-lookup"><span data-stu-id="675e4-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a><span data-ttu-id="675e4-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="675e4-110">Members</span></span>

 <span data-ttu-id="675e4-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="675e4-111">**cb**</span></span>
  
> <span data-ttu-id="675e4-112">Количество bytes в массиве, описанного **участником abEntry.**</span><span class="sxs-lookup"><span data-stu-id="675e4-112">Count of bytes in the array described by the **abEntry** member.</span></span> 
    
 <span data-ttu-id="675e4-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="675e4-113">**abEntry**</span></span>
  
> <span data-ttu-id="675e4-114">Массив Byte, содержащий данные идентификатора входа в МТС.</span><span class="sxs-lookup"><span data-stu-id="675e4-114">Byte array that contains the MTS entry identifier data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="675e4-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="675e4-115">Remarks</span></span>

<span data-ttu-id="675e4-116">Структура **MTSID** используется только для сопоставлений X.400 идентификаторов записей MAPI.</span><span class="sxs-lookup"><span data-stu-id="675e4-116">The **MTSID** structure is used only for X.400 mappings of MAPI entry identifiers.</span></span> <span data-ttu-id="675e4-117">Он соответствует структуре [FLATENTRY](flatentry.md) MAPI.</span><span class="sxs-lookup"><span data-stu-id="675e4-117">It corresponds to the MAPI [FLATENTRY](flatentry.md) structure.</span></span> 
  
<span data-ttu-id="675e4-118">Идентификатор МТС имеет тот же формат, что и идентификатор входа MAPI или двоичное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="675e4-118">An MTS identifier has the same format as a MAPI entry identifier or a binary property value.</span></span> <span data-ttu-id="675e4-119">Идентификаторы МТС могут быть особенно полезны для отмены отложенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="675e4-119">MTS identifiers can be particularly useful for canceling deferred messages.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="675e4-120">См. также</span><span class="sxs-lookup"><span data-stu-id="675e4-120">See also</span></span>



[<span data-ttu-id="675e4-121">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="675e4-121">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="675e4-122">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="675e4-122">FLATMTSIDLIST</span></span>](flatmtsidlist.md)


[<span data-ttu-id="675e4-123">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="675e4-123">MAPI Structures</span></span>](mapi-structures.md)

