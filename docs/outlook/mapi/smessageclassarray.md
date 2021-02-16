---
title: SMessageClassArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMessageClassArray
api_type:
- COM
ms.assetid: 05f8c191-db2b-4174-8b3c-a9fdabfe6ac8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 01b42c04244d35d72dd856222b4bab543b84db45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412697"
---
# <a name="smessageclassarray"></a><span data-ttu-id="d6bcb-103">SMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="d6bcb-103">SMessageClassArray</span></span>

  
  
<span data-ttu-id="d6bcb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6bcb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6bcb-105">Содержит массив указателей на строки класса сообщения.</span><span class="sxs-lookup"><span data-stu-id="d6bcb-105">Contains an array of pointers to message class strings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d6bcb-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d6bcb-106">Header file:</span></span>  <br/> |<span data-ttu-id="d6bcb-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="d6bcb-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="d6bcb-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="d6bcb-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="d6bcb-109">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="d6bcb-109">CbMessageClassArray</span></span>](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a><span data-ttu-id="d6bcb-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="d6bcb-110">Members</span></span>

 <span data-ttu-id="d6bcb-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="d6bcb-111">**cValues**</span></span>
  
> <span data-ttu-id="d6bcb-112">Количество указателей строки класса сообщений в массиве.</span><span class="sxs-lookup"><span data-stu-id="d6bcb-112">Count of message class string pointers in the array.</span></span>
    
 <span data-ttu-id="d6bcb-113">**aMessageClass**</span><span class="sxs-lookup"><span data-stu-id="d6bcb-113">**aMessageClass**</span></span>
  
> <span data-ttu-id="d6bcb-114">Массив указателей на строки класса сообщения.</span><span class="sxs-lookup"><span data-stu-id="d6bcb-114">Array of pointers to message class strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d6bcb-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="d6bcb-115">Remarks</span></span>

<span data-ttu-id="d6bcb-116">Структура **SMessageClassArray** передается в качестве параметра в следующих методах:</span><span class="sxs-lookup"><span data-stu-id="d6bcb-116">The **SMessageClassArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="d6bcb-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="d6bcb-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="d6bcb-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="d6bcb-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="d6bcb-119">См. также</span><span class="sxs-lookup"><span data-stu-id="d6bcb-119">See also</span></span>



[<span data-ttu-id="d6bcb-120">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="d6bcb-120">MAPI Structures</span></span>](mapi-structures.md)

