---
title: MSGCALLRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MSGCALLRELEASE
api_type:
- COM
ms.assetid: 23c08597-41f0-4f48-a63e-79962fa812bc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9ffaab1e9cc381be2abfb389f4b72067dca2438b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405914"
---
# <a name="msgcallrelease"></a><span data-ttu-id="893f8-103">MSGCALLRELEASE</span><span class="sxs-lookup"><span data-stu-id="893f8-103">MSGCALLRELEASE</span></span>

  
  
<span data-ttu-id="893f8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="893f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="893f8-105">Определяет функцию вызова, которая может освободить **интерфейс IStorage** после окончательного выпуска объекта **IMessage,** построенного поверх него с помощью функции [OpenIMsgOnIStg.](openimsgonistg.md)</span><span class="sxs-lookup"><span data-stu-id="893f8-105">Defines a callback function that can free an **IStorage** interface after the final release of an **IMessage** object built on top of it with the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="893f8-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="893f8-106">Header file:</span></span>  <br/> |<span data-ttu-id="893f8-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="893f8-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="893f8-108">Определенные функции, реализованные в:</span><span class="sxs-lookup"><span data-stu-id="893f8-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="893f8-109">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="893f8-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="893f8-110">Определенная функция, вызванная:</span><span class="sxs-lookup"><span data-stu-id="893f8-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="893f8-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="893f8-111">MAPI</span></span>  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a><span data-ttu-id="893f8-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="893f8-112">Parameters</span></span>

 <span data-ttu-id="893f8-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="893f8-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="893f8-114">[in] Содержит сведения о вызываемом приложении **об интерфейсе IMessage.**</span><span class="sxs-lookup"><span data-stu-id="893f8-114">[in] Contains calling application information about the **IMessage** interface.</span></span> 
    
 <span data-ttu-id="893f8-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="893f8-115">_lpMessage_</span></span>
  
> <span data-ttu-id="893f8-116">[in] Указатель на выпущенное сообщение верхнего уровня и вложения.</span><span class="sxs-lookup"><span data-stu-id="893f8-116">[in] Pointer to the top-level message and attachments that have been released.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="893f8-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="893f8-117">Return value</span></span>

<span data-ttu-id="893f8-118">Нет.</span><span class="sxs-lookup"><span data-stu-id="893f8-118">None.</span></span>
  

