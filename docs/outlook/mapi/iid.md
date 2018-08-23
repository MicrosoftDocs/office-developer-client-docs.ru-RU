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
ms.openlocfilehash: 00c7560427ece58026030ce6895d60aec7cc5a2e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570943"
---
# <a name="iid"></a><span data-ttu-id="bf324-103">IID</span><span class="sxs-lookup"><span data-stu-id="bf324-103">IID</span></span>

  
  
<span data-ttu-id="bf324-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf324-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf324-105">Описывает структуру [идентификатор GUID](guid.md) , используемый для описания идентификатор для интерфейса MAPI.</span><span class="sxs-lookup"><span data-stu-id="bf324-105">Describes a [GUID](guid.md) structure used to describe an identifier for a MAPI interface.</span></span> 
  
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="bf324-106">Members</span><span class="sxs-lookup"><span data-stu-id="bf324-106">Members</span></span>

<span data-ttu-id="bf324-107">Просмотр структуры **GUID** .</span><span class="sxs-lookup"><span data-stu-id="bf324-107">See the **GUID** structure.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bf324-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="bf324-108">Remarks</span></span>

<span data-ttu-id="bf324-109">**ИД интерфейса** структура используется для уникальной идентификации интерфейса MAPI и связывание определенного интерфейса с помощью объекта.</span><span class="sxs-lookup"><span data-stu-id="bf324-109">An **IID** structure is used to uniquely identify a MAPI interface and to associate a particular interface with an object.</span></span> <span data-ttu-id="bf324-110">Например при вызовах клиента [IMAPISession::OpenEntry](imapisession-openentry.md) чтобы открыть папку, клиент задается параметр _lpInterface_ для указания на **ИД интерфейса** представляющее интерфейс [IMAPIFolder](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="bf324-110">For example, when a client calls [IMAPISession::OpenEntry](imapisession-openentry.md) to open a folder, the client sets the  _lpInterface_ parameter to point to an **IID** representing the [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> <span data-ttu-id="bf324-111">MAPI определяет **IMAPIFolderIID** быть IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="bf324-111">MAPI defines the **IMAPIFolderIID** to be IID_IMAPIFolder.</span></span> <span data-ttu-id="bf324-112">**ИД интерфейса** структуры также используются для уникальной идентификации интерфейсов OLE.</span><span class="sxs-lookup"><span data-stu-id="bf324-112">**IID** structures are also used to uniquely identify OLE interfaces.</span></span> 
  
<span data-ttu-id="bf324-113">Все определенные структуры **ИД интерфейса** MAPI интерфейсов определены в файле заголовка Mapiguid.h.</span><span class="sxs-lookup"><span data-stu-id="bf324-113">All of the specific **IID** structures for the MAPI interfaces are defined in the Mapiguid.h header file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bf324-114">См. также</span><span class="sxs-lookup"><span data-stu-id="bf324-114">See also</span></span>



[<span data-ttu-id="bf324-115">ИДЕНТИФИКАТОР GUID</span><span class="sxs-lookup"><span data-stu-id="bf324-115">GUID</span></span>](guid.md)


[<span data-ttu-id="bf324-116">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="bf324-116">MAPI Structures</span></span>](mapi-structures.md)

