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
ms.openlocfilehash: aaa1adaa170349c3df3a2256802a502cb2512b20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810024"
---
# <a name="msgcallrelease"></a><span data-ttu-id="d58ab-103">MSGCALLRELEASE</span><span class="sxs-lookup"><span data-stu-id="d58ab-103">MSGCALLRELEASE</span></span>

  
  
<span data-ttu-id="d58ab-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d58ab-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d58ab-105">Определяет функцию обратного вызова, можно освободить интерфейс **IStorage** после окончательной версии объекта **IMessage** , построенных на основе его с помощью функции [OpenIMsgOnIStg](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="d58ab-105">Defines a callback function that can free an **IStorage** interface after the final release of an **IMessage** object built on top of it with the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d58ab-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d58ab-106">Header file:</span></span>  <br/> |<span data-ttu-id="d58ab-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="d58ab-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="d58ab-108">Функция реализован:</span><span class="sxs-lookup"><span data-stu-id="d58ab-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="d58ab-109">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="d58ab-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="d58ab-110">Вызывается функция:</span><span class="sxs-lookup"><span data-stu-id="d58ab-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="d58ab-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="d58ab-111">MAPI</span></span>  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a><span data-ttu-id="d58ab-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d58ab-112">Parameters</span></span>

 <span data-ttu-id="d58ab-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="d58ab-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="d58ab-114">[in] Содержит вызывающего приложения сведения об интерфейсе **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="d58ab-114">[in] Contains calling application information about the **IMessage** interface.</span></span> 
    
 <span data-ttu-id="d58ab-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="d58ab-115">_lpMessage_</span></span>
  
> <span data-ttu-id="d58ab-116">[in] Указатель на верхнего уровня сообщений и вложений, которые были выпущены.</span><span class="sxs-lookup"><span data-stu-id="d58ab-116">[in] Pointer to the top-level message and attachments that have been released.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d58ab-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d58ab-117">Return value</span></span>

<span data-ttu-id="d58ab-118">Нет.</span><span class="sxs-lookup"><span data-stu-id="d58ab-118">None.</span></span>
  

