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
ms.openlocfilehash: b2caa70600bd32234e38420f274bcd5c46ffb070
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578159"
---
# <a name="smessageclassarray"></a><span data-ttu-id="b0ae6-103">SMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="b0ae6-103">SMessageClassArray</span></span>

  
  
<span data-ttu-id="b0ae6-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0ae6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0ae6-105">Содержит массив указатели на строки класс сообщения.</span><span class="sxs-lookup"><span data-stu-id="b0ae6-105">Contains an array of pointers to message class strings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b0ae6-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b0ae6-106">Header file:</span></span>  <br/> |<span data-ttu-id="b0ae6-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="b0ae6-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="b0ae6-108">Связанные макрос:</span><span class="sxs-lookup"><span data-stu-id="b0ae6-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="b0ae6-109">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="b0ae6-109">CbMessageClassArray</span></span>](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a><span data-ttu-id="b0ae6-110">Members</span><span class="sxs-lookup"><span data-stu-id="b0ae6-110">Members</span></span>

 <span data-ttu-id="b0ae6-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="b0ae6-111">**cValues**</span></span>
  
> <span data-ttu-id="b0ae6-112">Число указатели строка класс сообщения в массиве.</span><span class="sxs-lookup"><span data-stu-id="b0ae6-112">Count of message class string pointers in the array.</span></span>
    
 <span data-ttu-id="b0ae6-113">**aMessageClass**</span><span class="sxs-lookup"><span data-stu-id="b0ae6-113">**aMessageClass**</span></span>
  
> <span data-ttu-id="b0ae6-114">Массив, содержащий указатели на строки класс сообщения.</span><span class="sxs-lookup"><span data-stu-id="b0ae6-114">Array of pointers to message class strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b0ae6-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="b0ae6-115">Remarks</span></span>

<span data-ttu-id="b0ae6-116">Структура **SMessageClassArray** передается как параметр в следующих методов:</span><span class="sxs-lookup"><span data-stu-id="b0ae6-116">The **SMessageClassArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="b0ae6-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="b0ae6-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="b0ae6-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="b0ae6-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="b0ae6-119">См. также</span><span class="sxs-lookup"><span data-stu-id="b0ae6-119">See also</span></span>



[<span data-ttu-id="b0ae6-120">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="b0ae6-120">MAPI Structures</span></span>](mapi-structures.md)

