---
title: IID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IID
api_type:
- COM
ms.assetid: fa5498ab-2f8a-42f8-ba9d-1d555768594f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5605de7dbcc18197748713bcf909839690d7259f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411598"
---
# <a name="iid"></a><span data-ttu-id="36db7-103">IID</span><span class="sxs-lookup"><span data-stu-id="36db7-103">IID</span></span>

  
  
<span data-ttu-id="36db7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36db7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36db7-105">Описывает структуру [GUID](guid.md) , используемую для описания идентификатора интерфейса MAPI.</span><span class="sxs-lookup"><span data-stu-id="36db7-105">Describes a [GUID](guid.md) structure used to describe an identifier for a MAPI interface.</span></span> 
  
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="36db7-106">"Участники"</span><span class="sxs-lookup"><span data-stu-id="36db7-106">Members</span></span>

<span data-ttu-id="36db7-107">Просмотр структуры **GUID** .</span><span class="sxs-lookup"><span data-stu-id="36db7-107">See the **GUID** structure.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="36db7-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="36db7-108">Remarks</span></span>

<span data-ttu-id="36db7-109">Структура **IID** используется для уникальной идентификации интерфейса MAPI и связывания определенного интерфейса с объектом.</span><span class="sxs-lookup"><span data-stu-id="36db7-109">An **IID** structure is used to uniquely identify a MAPI interface and to associate a particular interface with an object.</span></span> <span data-ttu-id="36db7-110">Например, когда клиент вызывает [IMAPISession:: OpenEntry](imapisession-openentry.md) , чтобы открыть папку, клиент устанавливает параметр _лпинтерфаце_ , который указывает на **IID** , представляющий интерфейс [IMAPIFolder](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="36db7-110">For example, when a client calls [IMAPISession::OpenEntry](imapisession-openentry.md) to open a folder, the client sets the  _lpInterface_ parameter to point to an **IID** representing the [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> <span data-ttu-id="36db7-111">MAPI определяет **имапифолдериид** , который необходимо IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="36db7-111">MAPI defines the **IMAPIFolderIID** to be IID_IMAPIFolder.</span></span> <span data-ttu-id="36db7-112">Структуры **IID** также используются для уникальной идентификации интерфейсов OLE.</span><span class="sxs-lookup"><span data-stu-id="36db7-112">**IID** structures are also used to uniquely identify OLE interfaces.</span></span> 
  
<span data-ttu-id="36db7-113">Все конкретные структуры **IID** для интерфейсов MAPI определены в файле заголовка мапигуид. h.</span><span class="sxs-lookup"><span data-stu-id="36db7-113">All of the specific **IID** structures for the MAPI interfaces are defined in the Mapiguid.h header file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="36db7-114">См. также</span><span class="sxs-lookup"><span data-stu-id="36db7-114">See also</span></span>



[<span data-ttu-id="36db7-115">GUID</span><span class="sxs-lookup"><span data-stu-id="36db7-115">GUID</span></span>](guid.md)


[<span data-ttu-id="36db7-116">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="36db7-116">MAPI Structures</span></span>](mapi-structures.md)

