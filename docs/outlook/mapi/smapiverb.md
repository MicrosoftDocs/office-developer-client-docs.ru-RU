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
ms.openlocfilehash: 11f11ae2d90a951a119895f3e0e3e3ca0dbc0fc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573700"
---
# <a name="smapiverb"></a><span data-ttu-id="47c0c-103">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="47c0c-103">SMAPIVerb</span></span>

  
  
<span data-ttu-id="47c0c-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47c0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47c0c-105">Описываются команды MAPI.</span><span class="sxs-lookup"><span data-stu-id="47c0c-105">Describes a MAPI verb.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="47c0c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="47c0c-106">Header file:</span></span>  <br/> |<span data-ttu-id="47c0c-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="47c0c-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="47c0c-108">Members</span><span class="sxs-lookup"><span data-stu-id="47c0c-108">Members</span></span>

 <span data-ttu-id="47c0c-109">**lVerb**</span><span class="sxs-lookup"><span data-stu-id="47c0c-109">**lVerb**</span></span>
  
> <span data-ttu-id="47c0c-110">Код, который представляет команду, которая передается [IMAPIForm::DoVerb](imapiform-doverb.md).</span><span class="sxs-lookup"><span data-stu-id="47c0c-110">Code representing the verb that is passed to [IMAPIForm::DoVerb](imapiform-doverb.md).</span></span> <span data-ttu-id="47c0c-111">Стандартные команды определены в файле заголовка Exchform.h.</span><span class="sxs-lookup"><span data-stu-id="47c0c-111">Standard verbs are defined in the header file Exchform.h.</span></span>
    
 <span data-ttu-id="47c0c-112">**szVerbname**</span><span class="sxs-lookup"><span data-stu-id="47c0c-112">**szVerbname**</span></span>
  
> <span data-ttu-id="47c0c-113">Отображаемое имя команды, как оно отображается в виде меню.</span><span class="sxs-lookup"><span data-stu-id="47c0c-113">Display name of the verb as it appears on the form menu.</span></span>
    
 <span data-ttu-id="47c0c-114">**fuFlags**</span><span class="sxs-lookup"><span data-stu-id="47c0c-114">**fuFlags**</span></span>
  
> <span data-ttu-id="47c0c-115">Флаги для команды.</span><span class="sxs-lookup"><span data-stu-id="47c0c-115">Flags for the verb.</span></span>
    
 <span data-ttu-id="47c0c-116">**grfAttribs**</span><span class="sxs-lookup"><span data-stu-id="47c0c-116">**grfAttribs**</span></span>
  
> <span data-ttu-id="47c0c-117">Атрибуты команды.</span><span class="sxs-lookup"><span data-stu-id="47c0c-117">Attributes of the verb.</span></span> 
    
 <span data-ttu-id="47c0c-118">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="47c0c-118">**ulFlags**</span></span>
  
> <span data-ttu-id="47c0c-119">Флаг, указывающий формат команды отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="47c0c-119">Flag indicating the format of the verb's display name.</span></span> <span data-ttu-id="47c0c-120">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="47c0c-120">The following flag can be set:</span></span>
    
<span data-ttu-id="47c0c-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="47c0c-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="47c0c-122">Отображаемое имя — в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="47c0c-122">The display name is in Unicode format.</span></span> <span data-ttu-id="47c0c-123">Если флаг MAPI_UNICODE не установлен, отображаемое имя — в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="47c0c-123">If the MAPI_UNICODE flag is not set, the display name is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="47c0c-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="47c0c-124">Remarks</span></span>

<span data-ttu-id="47c0c-125">Структура **SMAPIVerb** передается как параметр в следующих методов:</span><span class="sxs-lookup"><span data-stu-id="47c0c-125">The **SMAPIVerb** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="47c0c-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="47c0c-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="47c0c-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="47c0c-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="47c0c-128">См. также</span><span class="sxs-lookup"><span data-stu-id="47c0c-128">See also</span></span>



[<span data-ttu-id="47c0c-129">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="47c0c-129">CbMessageClassArray</span></span>](cbmessageclassarray.md)


[<span data-ttu-id="47c0c-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="47c0c-130">MAPI Structures</span></span>](mapi-structures.md)

