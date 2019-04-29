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
# <a name="smapiverb"></a><span data-ttu-id="db694-103">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="db694-103">SMAPIVerb</span></span>

  
  
<span data-ttu-id="db694-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db694-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db694-105">Описывает команду MAPI.</span><span class="sxs-lookup"><span data-stu-id="db694-105">Describes a MAPI verb.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="db694-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="db694-106">Header file:</span></span>  <br/> |<span data-ttu-id="db694-107">Мапиформ. h</span><span class="sxs-lookup"><span data-stu-id="db694-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="db694-108">Members</span><span class="sxs-lookup"><span data-stu-id="db694-108">Members</span></span>

 <span data-ttu-id="db694-109">**Лверб**</span><span class="sxs-lookup"><span data-stu-id="db694-109">**lVerb**</span></span>
  
> <span data-ttu-id="db694-110">Код, представляющий команду, которая передается в [имапиформ::D оверб](imapiform-doverb.md).</span><span class="sxs-lookup"><span data-stu-id="db694-110">Code representing the verb that is passed to [IMAPIForm::DoVerb](imapiform-doverb.md).</span></span> <span data-ttu-id="db694-111">Стандартные команды определяются в файле заголовка Ексчформ. h.</span><span class="sxs-lookup"><span data-stu-id="db694-111">Standard verbs are defined in the header file Exchform.h.</span></span>
    
 <span data-ttu-id="db694-112">**Сзвербнаме**</span><span class="sxs-lookup"><span data-stu-id="db694-112">**szVerbname**</span></span>
  
> <span data-ttu-id="db694-113">Отображаемое имя команды в том виде, в котором оно отображается в меню формы.</span><span class="sxs-lookup"><span data-stu-id="db694-113">Display name of the verb as it appears on the form menu.</span></span>
    
 <span data-ttu-id="db694-114">**Фуфлагс**</span><span class="sxs-lookup"><span data-stu-id="db694-114">**fuFlags**</span></span>
  
> <span data-ttu-id="db694-115">Флаги для команды.</span><span class="sxs-lookup"><span data-stu-id="db694-115">Flags for the verb.</span></span>
    
 <span data-ttu-id="db694-116">**Грфаттрибс**</span><span class="sxs-lookup"><span data-stu-id="db694-116">**grfAttribs**</span></span>
  
> <span data-ttu-id="db694-117">Атрибуты команды.</span><span class="sxs-lookup"><span data-stu-id="db694-117">Attributes of the verb.</span></span> 
    
 <span data-ttu-id="db694-118">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="db694-118">**ulFlags**</span></span>
  
> <span data-ttu-id="db694-119">Флаг, указывающий формат отображаемого имени команды.</span><span class="sxs-lookup"><span data-stu-id="db694-119">Flag indicating the format of the verb's display name.</span></span> <span data-ttu-id="db694-120">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="db694-120">The following flag can be set:</span></span>
    
<span data-ttu-id="db694-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="db694-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="db694-122">Отображаемое имя в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="db694-122">The display name is in Unicode format.</span></span> <span data-ttu-id="db694-123">Если флаг МАПИ_УНИКОДЕ не установлен, отображаемое имя отображается в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="db694-123">If the MAPI_UNICODE flag is not set, the display name is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="db694-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="db694-124">Remarks</span></span>

<span data-ttu-id="db694-125">Структура **смапиверб** передается в качестве параметра в следующих методах:</span><span class="sxs-lookup"><span data-stu-id="db694-125">The **SMAPIVerb** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="db694-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="db694-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="db694-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="db694-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="db694-128">См. также</span><span class="sxs-lookup"><span data-stu-id="db694-128">See also</span></span>



[<span data-ttu-id="db694-129">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="db694-129">CbMessageClassArray</span></span>](cbmessageclassarray.md)


[<span data-ttu-id="db694-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="db694-130">MAPI Structures</span></span>](mapi-structures.md)

