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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338565"
---
# <a name="msgcallrelease"></a><span data-ttu-id="a5f70-103">MSGCALLRELEASE</span><span class="sxs-lookup"><span data-stu-id="a5f70-103">MSGCALLRELEASE</span></span>

  
  
<span data-ttu-id="a5f70-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5f70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5f70-105">Определяет функцию обратного вызова, которая может освобождать интерфейс **IStorage** после окончательного выпуска объекта **iMessage** , построенного на основе функции [опенимсгонистг](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f70-105">Defines a callback function that can free an **IStorage** interface after the final release of an **IMessage** object built on top of it with the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a5f70-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a5f70-106">Header file:</span></span>  <br/> |<span data-ttu-id="a5f70-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="a5f70-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="a5f70-108">Определенная функция реализована следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a5f70-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="a5f70-109">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="a5f70-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="a5f70-110">Определенная функция, вызываемая:</span><span class="sxs-lookup"><span data-stu-id="a5f70-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="a5f70-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="a5f70-111">MAPI</span></span>  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a><span data-ttu-id="a5f70-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5f70-112">Parameters</span></span>

 <span data-ttu-id="a5f70-113">_Улкаллердата_</span><span class="sxs-lookup"><span data-stu-id="a5f70-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="a5f70-114">возврата Содержит сведения о вызывающем приложении для интерфейса **iMessage** .</span><span class="sxs-lookup"><span data-stu-id="a5f70-114">[in] Contains calling application information about the **IMessage** interface.</span></span> 
    
 <span data-ttu-id="a5f70-115">_Лпмессаже_</span><span class="sxs-lookup"><span data-stu-id="a5f70-115">_lpMessage_</span></span>
  
> <span data-ttu-id="a5f70-116">возврата Указатель на сообщение верхнего уровня и вложения, которые были выпущены.</span><span class="sxs-lookup"><span data-stu-id="a5f70-116">[in] Pointer to the top-level message and attachments that have been released.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a5f70-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5f70-117">Return value</span></span>

<span data-ttu-id="a5f70-118">Нет.</span><span class="sxs-lookup"><span data-stu-id="a5f70-118">None.</span></span>
  

