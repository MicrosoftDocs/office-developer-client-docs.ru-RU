---
title: SMAPIVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerb
api_type:
- COM
ms.assetid: 45066528-2447-4178-aaa3-7513ed0b3ba4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4d060d62deb685b4691846c2b8e48a82ae3195ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812353"
---
# <a name="smapiverb"></a><span data-ttu-id="a43fa-103">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="a43fa-103">SMAPIVerb</span></span>

  
  
<span data-ttu-id="a43fa-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a43fa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a43fa-105">Описываются команды MAPI.</span><span class="sxs-lookup"><span data-stu-id="a43fa-105">Describes a MAPI verb.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a43fa-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a43fa-106">Header file:</span></span>  <br/> |<span data-ttu-id="a43fa-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="a43fa-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG lVerb;
  LPSTR szVerbname;
  DWORD fuFlags;
  DWORD grfAttribs;
  ULONG ulFlags; /* Either 0 or MAPI_UNICODE */
} SMAPIVerb, FAR * LPMAPIVERB;

```

## <a name="members"></a><span data-ttu-id="a43fa-108">Members</span><span class="sxs-lookup"><span data-stu-id="a43fa-108">Members</span></span>

 <span data-ttu-id="a43fa-109">**lVerb**</span><span class="sxs-lookup"><span data-stu-id="a43fa-109">**lVerb**</span></span>
  
> <span data-ttu-id="a43fa-110">Код, который представляет команду, которая передается [IMAPIForm::DoVerb](imapiform-doverb.md).</span><span class="sxs-lookup"><span data-stu-id="a43fa-110">Code representing the verb that is passed to [IMAPIForm::DoVerb](imapiform-doverb.md).</span></span> <span data-ttu-id="a43fa-111">Стандартные команды определены в файле заголовка Exchform.h.</span><span class="sxs-lookup"><span data-stu-id="a43fa-111">Standard verbs are defined in the header file Exchform.h.</span></span>
    
 <span data-ttu-id="a43fa-112">**szVerbname**</span><span class="sxs-lookup"><span data-stu-id="a43fa-112">**szVerbname**</span></span>
  
> <span data-ttu-id="a43fa-113">Отображаемое имя команды, как оно отображается в виде меню.</span><span class="sxs-lookup"><span data-stu-id="a43fa-113">Display name of the verb as it appears on the form menu.</span></span>
    
 <span data-ttu-id="a43fa-114">**fuFlags**</span><span class="sxs-lookup"><span data-stu-id="a43fa-114">**fuFlags**</span></span>
  
> <span data-ttu-id="a43fa-115">Флаги для команды.</span><span class="sxs-lookup"><span data-stu-id="a43fa-115">Flags for the verb.</span></span>
    
 <span data-ttu-id="a43fa-116">**grfAttribs**</span><span class="sxs-lookup"><span data-stu-id="a43fa-116">**grfAttribs**</span></span>
  
> <span data-ttu-id="a43fa-117">Атрибуты команды.</span><span class="sxs-lookup"><span data-stu-id="a43fa-117">Attributes of the verb.</span></span> 
    
 <span data-ttu-id="a43fa-118">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="a43fa-118">**ulFlags**</span></span>
  
> <span data-ttu-id="a43fa-119">Флаг, указывающий формат команды отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="a43fa-119">Flag indicating the format of the verb's display name.</span></span> <span data-ttu-id="a43fa-120">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="a43fa-120">The following flag can be set:</span></span>
    
<span data-ttu-id="a43fa-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a43fa-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a43fa-122">Отображаемое имя — в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="a43fa-122">The display name is in Unicode format.</span></span> <span data-ttu-id="a43fa-123">Если флаг MAPI_UNICODE не установлен, отображаемое имя — в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="a43fa-123">If the MAPI_UNICODE flag is not set, the display name is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a43fa-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="a43fa-124">Remarks</span></span>

<span data-ttu-id="a43fa-125">Структура **SMAPIVerb** передается как параметр в следующих методов:</span><span class="sxs-lookup"><span data-stu-id="a43fa-125">The **SMAPIVerb** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="a43fa-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="a43fa-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="a43fa-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="a43fa-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="a43fa-128">См. также</span><span class="sxs-lookup"><span data-stu-id="a43fa-128">See also</span></span>



[<span data-ttu-id="a43fa-129">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="a43fa-129">CbMessageClassArray</span></span>](cbmessageclassarray.md)


[<span data-ttu-id="a43fa-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="a43fa-130">MAPI Structures</span></span>](mapi-structures.md)

