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
ms.openlocfilehash: 3ef284a2c036abb9eac10ecf33de4adbf61f3c54
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410961"
---
# <a name="smapiverb"></a><span data-ttu-id="ce680-103">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="ce680-103">SMAPIVerb</span></span>

  
  
<span data-ttu-id="ce680-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce680-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce680-105">Описывает глагол MAPI.</span><span class="sxs-lookup"><span data-stu-id="ce680-105">Describes a MAPI verb.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ce680-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ce680-106">Header file:</span></span>  <br/> |<span data-ttu-id="ce680-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="ce680-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="ce680-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="ce680-108">Members</span></span>

 <span data-ttu-id="ce680-109">**lVerb**</span><span class="sxs-lookup"><span data-stu-id="ce680-109">**lVerb**</span></span>
  
> <span data-ttu-id="ce680-110">Код, представляющий глагол, который передается [IMAPIForm::D oVerb](imapiform-doverb.md).</span><span class="sxs-lookup"><span data-stu-id="ce680-110">Code representing the verb that is passed to [IMAPIForm::DoVerb](imapiform-doverb.md).</span></span> <span data-ttu-id="ce680-111">Стандартные глаголы определяются в файле загона Exchform.h.</span><span class="sxs-lookup"><span data-stu-id="ce680-111">Standard verbs are defined in the header file Exchform.h.</span></span>
    
 <span data-ttu-id="ce680-112">**szVerbname**</span><span class="sxs-lookup"><span data-stu-id="ce680-112">**szVerbname**</span></span>
  
> <span data-ttu-id="ce680-113">Отображение имени глагола по мере его отображения в меню формы.</span><span class="sxs-lookup"><span data-stu-id="ce680-113">Display name of the verb as it appears on the form menu.</span></span>
    
 <span data-ttu-id="ce680-114">**fuFlags**</span><span class="sxs-lookup"><span data-stu-id="ce680-114">**fuFlags**</span></span>
  
> <span data-ttu-id="ce680-115">Флаги для глагола.</span><span class="sxs-lookup"><span data-stu-id="ce680-115">Flags for the verb.</span></span>
    
 <span data-ttu-id="ce680-116">**grfAttribs**</span><span class="sxs-lookup"><span data-stu-id="ce680-116">**grfAttribs**</span></span>
  
> <span data-ttu-id="ce680-117">Атрибуты глагола.</span><span class="sxs-lookup"><span data-stu-id="ce680-117">Attributes of the verb.</span></span> 
    
 <span data-ttu-id="ce680-118">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="ce680-118">**ulFlags**</span></span>
  
> <span data-ttu-id="ce680-119">Флаг с указанием формата отображаемого имени глагола.</span><span class="sxs-lookup"><span data-stu-id="ce680-119">Flag indicating the format of the verb's display name.</span></span> <span data-ttu-id="ce680-120">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="ce680-120">The following flag can be set:</span></span>
    
<span data-ttu-id="ce680-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ce680-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ce680-122">Имя дисплея находится в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="ce680-122">The display name is in Unicode format.</span></span> <span data-ttu-id="ce680-123">Если флаг MAPI_UNICODE не установлен, имя отображения находится в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="ce680-123">If the MAPI_UNICODE flag is not set, the display name is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ce680-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="ce680-124">Remarks</span></span>

<span data-ttu-id="ce680-125">Структура **SMAPIVerb** передается в качестве параметра в следующих методах:</span><span class="sxs-lookup"><span data-stu-id="ce680-125">The **SMAPIVerb** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="ce680-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="ce680-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="ce680-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="ce680-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="ce680-128">См. также</span><span class="sxs-lookup"><span data-stu-id="ce680-128">See also</span></span>



[<span data-ttu-id="ce680-129">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="ce680-129">CbMessageClassArray</span></span>](cbmessageclassarray.md)


[<span data-ttu-id="ce680-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="ce680-130">MAPI Structures</span></span>](mapi-structures.md)

