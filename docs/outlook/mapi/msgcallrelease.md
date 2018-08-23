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
ms.openlocfilehash: e9a1c416cbf992c9cbcfb5de42d302ff16e7f521
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573189"
---
# <a name="msgcallrelease"></a><span data-ttu-id="5bb30-103">MSGCALLRELEASE</span><span class="sxs-lookup"><span data-stu-id="5bb30-103">MSGCALLRELEASE</span></span>

  
  
<span data-ttu-id="5bb30-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5bb30-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5bb30-105">Определяет функцию обратного вызова, можно освободить интерфейс **IStorage** после окончательной версии объекта **IMessage** , построенных на основе его с помощью функции [OpenIMsgOnIStg](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="5bb30-105">Defines a callback function that can free an **IStorage** interface after the final release of an **IMessage** object built on top of it with the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5bb30-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5bb30-106">Header file:</span></span>  <br/> |<span data-ttu-id="5bb30-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="5bb30-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="5bb30-108">Функция реализован:</span><span class="sxs-lookup"><span data-stu-id="5bb30-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="5bb30-109">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="5bb30-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="5bb30-110">Вызывается функция:</span><span class="sxs-lookup"><span data-stu-id="5bb30-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="5bb30-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="5bb30-111">MAPI</span></span>  <br/> |
   
```cpp
typedef void (STDAPICALLTYPE MSGCALLRELEASE)(
  ULONG  ulCallerData,
  LPMESSAGE  lpMessage );
```

## <a name="parameters"></a><span data-ttu-id="5bb30-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="5bb30-112">Parameters</span></span>

 <span data-ttu-id="5bb30-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="5bb30-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="5bb30-114">[in] Содержит вызывающего приложения сведения об интерфейсе **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="5bb30-114">[in] Contains calling application information about the **IMessage** interface.</span></span> 
    
 <span data-ttu-id="5bb30-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="5bb30-115">_lpMessage_</span></span>
  
> <span data-ttu-id="5bb30-116">[in] Указатель на верхнего уровня сообщений и вложений, которые были выпущены.</span><span class="sxs-lookup"><span data-stu-id="5bb30-116">[in] Pointer to the top-level message and attachments that have been released.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5bb30-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5bb30-117">Return value</span></span>

<span data-ttu-id="5bb30-118">Нет.</span><span class="sxs-lookup"><span data-stu-id="5bb30-118">None.</span></span>
  

