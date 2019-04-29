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
# <a name="smessageclassarray"></a><span data-ttu-id="1a604-103">SMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="1a604-103">SMessageClassArray</span></span>

  
  
<span data-ttu-id="1a604-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a604-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a604-105">Содержит массив указателей на строки класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="1a604-105">Contains an array of pointers to message class strings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1a604-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1a604-106">Header file:</span></span>  <br/> |<span data-ttu-id="1a604-107">Мапиформ. h</span><span class="sxs-lookup"><span data-stu-id="1a604-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="1a604-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="1a604-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="1a604-109">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="1a604-109">CbMessageClassArray</span></span>](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a><span data-ttu-id="1a604-110">Members</span><span class="sxs-lookup"><span data-stu-id="1a604-110">Members</span></span>

 <span data-ttu-id="1a604-111">**Квалуес**</span><span class="sxs-lookup"><span data-stu-id="1a604-111">**cValues**</span></span>
  
> <span data-ttu-id="1a604-112">Количество указателей по строкам в классе Message в массиве.</span><span class="sxs-lookup"><span data-stu-id="1a604-112">Count of message class string pointers in the array.</span></span>
    
 <span data-ttu-id="1a604-113">**Амессажекласс**</span><span class="sxs-lookup"><span data-stu-id="1a604-113">**aMessageClass**</span></span>
  
> <span data-ttu-id="1a604-114">Массив указателей на строки класса сообщений.</span><span class="sxs-lookup"><span data-stu-id="1a604-114">Array of pointers to message class strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1a604-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="1a604-115">Remarks</span></span>

<span data-ttu-id="1a604-116">Структура **смессажеклассаррай** передается в качестве параметра в следующих методах:</span><span class="sxs-lookup"><span data-stu-id="1a604-116">The **SMessageClassArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="1a604-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="1a604-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="1a604-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="1a604-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="1a604-119">См. также</span><span class="sxs-lookup"><span data-stu-id="1a604-119">See also</span></span>



[<span data-ttu-id="1a604-120">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="1a604-120">MAPI Structures</span></span>](mapi-structures.md)

