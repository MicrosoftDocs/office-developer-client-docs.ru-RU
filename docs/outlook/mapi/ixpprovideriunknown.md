---
title: IXPProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider
api_type:
- COM
ms.assetid: d5507785-c924-4981-ae80-19709ceb054d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 49cb500279540317059cde2d9baba28fcbf06165
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574113"
---
# <a name="ixpprovider--iunknown"></a><span data-ttu-id="0e264-103">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0e264-103">IXPProvider : IUnknown</span></span>

  
  
<span data-ttu-id="0e264-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e264-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e264-105">Инициализирует объект поставщика транспорта и завершает работу объекта, если они больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="0e264-105">Initializes a transport provider object and shuts down the object when it is no longer needed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0e264-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="0e264-106">Header file:</span></span>  <br/> |<span data-ttu-id="0e264-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="0e264-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="0e264-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="0e264-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="0e264-109">Объекты поставщика транспорта</span><span class="sxs-lookup"><span data-stu-id="0e264-109">Transport provider objects</span></span>  <br/> |
|<span data-ttu-id="0e264-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="0e264-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="0e264-111">Поставщиками транспорта</span><span class="sxs-lookup"><span data-stu-id="0e264-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="0e264-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="0e264-112">Called by:</span></span>  <br/> |<span data-ttu-id="0e264-113">Диспетчер очереди MAPI</span><span class="sxs-lookup"><span data-stu-id="0e264-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="0e264-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="0e264-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0e264-115">IID_IXPProvider</span><span class="sxs-lookup"><span data-stu-id="0e264-115">IID_IXPProvider</span></span>  <br/> |
|<span data-ttu-id="0e264-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="0e264-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="0e264-117">LPXPROVIDER</span><span class="sxs-lookup"><span data-stu-id="0e264-117">LPXPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0e264-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="0e264-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="0e264-119">Shutdown</span><span class="sxs-lookup"><span data-stu-id="0e264-119">Shutdown</span></span>](ixpprovider-shutdown.md) <br/> |<span data-ttu-id="0e264-120">Закрывает вниз поставщика транспорта определенным образом.</span><span class="sxs-lookup"><span data-stu-id="0e264-120">Closes down a transport provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="0e264-121">TransportLogon</span><span class="sxs-lookup"><span data-stu-id="0e264-121">TransportLogon</span></span>](ixpprovider-transportlogon.md) <br/> |<span data-ttu-id="0e264-122">Устанавливает сеанс, в котором клиентское приложение входит в систему поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="0e264-122">Establishes a session in which a client application logs on to a transport provider.</span></span>  <br/> |
   

