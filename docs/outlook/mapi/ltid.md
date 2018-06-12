---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 4a60e2fe3a58e1d696ae9645e03ce8dde5340d9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809663"
---
# <a name="ltid"></a><span data-ttu-id="42cf4-103">LTID</span><span class="sxs-lookup"><span data-stu-id="42cf4-103">LTID</span></span>

  
  
<span data-ttu-id="42cf4-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="42cf4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="42cf4-105">Универсальный длинный идентификатор термина объекта в хранилище Outlook.</span><span class="sxs-lookup"><span data-stu-id="42cf4-105">Generic Long Term ID of an object in an Outlook store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="42cf4-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="42cf4-106">Quick info</span></span>

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a><span data-ttu-id="42cf4-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="42cf4-107">Members</span></span>

 <span data-ttu-id="42cf4-108">_Идентификатор GUID_</span><span class="sxs-lookup"><span data-stu-id="42cf4-108">_guid_</span></span>
  
- <span data-ttu-id="42cf4-109">[out] Идентификатор GUID сервера, создавшее этот объект.</span><span class="sxs-lookup"><span data-stu-id="42cf4-109">[out] The GUID of the server that created the object.</span></span>
    
 <span data-ttu-id="42cf4-110">_globcnt_</span><span class="sxs-lookup"><span data-stu-id="42cf4-110">_globcnt_</span></span>
  
- <span data-ttu-id="42cf4-111">[out] 6-байтовое уникальный номер, идентифицирующий объекта в хранилище Outlook.</span><span class="sxs-lookup"><span data-stu-id="42cf4-111">[out] A 6-byte unique number that identifies the object within the Outlook store.</span></span>
    
 <span data-ttu-id="42cf4-112">_wLevel_</span><span class="sxs-lookup"><span data-stu-id="42cf4-112">_wLevel_</span></span>
  
- <span data-ttu-id="42cf4-113">[out] Уровень иерархии идентификатор записи для Exchange избранные общей папки.</span><span class="sxs-lookup"><span data-stu-id="42cf4-113">[out] The hierarchy level of the entry ID for an Exchange Favorite Public folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="42cf4-114">См. также</span><span class="sxs-lookup"><span data-stu-id="42cf4-114">See also</span></span>



[<span data-ttu-id="42cf4-115">О репликации API</span><span class="sxs-lookup"><span data-stu-id="42cf4-115">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="42cf4-116">О репликации конечного автомата</span><span class="sxs-lookup"><span data-stu-id="42cf4-116">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="42cf4-117">FEID</span><span class="sxs-lookup"><span data-stu-id="42cf4-117">FEID</span></span>](feid.md)

