---
title: Иксппровидер IUnknown
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
ms.openlocfilehash: 0aa77ced9d0c242dcafb84ca1e1a60d02db9504a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404696"
---
# <a name="ixpprovider--iunknown"></a><span data-ttu-id="b8b4b-103">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b8b4b-103">IXPProvider : IUnknown</span></span>

  
  
<span data-ttu-id="b8b4b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8b4b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8b4b-105">Инициализирует объект поставщика транспорта и завершает объект, когда он больше не нужен.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-105">Initializes a transport provider object and shuts down the object when it is no longer needed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b8b4b-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b8b4b-106">Header file:</span></span>  <br/> |<span data-ttu-id="b8b4b-107">Маписпи. h</span><span class="sxs-lookup"><span data-stu-id="b8b4b-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="b8b4b-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="b8b4b-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="b8b4b-109">Объекты поставщиков транспорта</span><span class="sxs-lookup"><span data-stu-id="b8b4b-109">Transport provider objects</span></span>  <br/> |
|<span data-ttu-id="b8b4b-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="b8b4b-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="b8b4b-111">Поставщики транспорта</span><span class="sxs-lookup"><span data-stu-id="b8b4b-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="b8b4b-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="b8b4b-112">Called by:</span></span>  <br/> |<span data-ttu-id="b8b4b-113">Диспетчер очереди MAPI</span><span class="sxs-lookup"><span data-stu-id="b8b4b-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="b8b4b-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="b8b4b-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b8b4b-115">IID_IXPProvider</span><span class="sxs-lookup"><span data-stu-id="b8b4b-115">IID_IXPProvider</span></span>  <br/> |
|<span data-ttu-id="b8b4b-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="b8b4b-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="b8b4b-117">лпкспровидер</span><span class="sxs-lookup"><span data-stu-id="b8b4b-117">LPXPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b8b4b-118">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="b8b4b-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b8b4b-119">Shutdown</span><span class="sxs-lookup"><span data-stu-id="b8b4b-119">Shutdown</span></span>](ixpprovider-shutdown.md) <br/> |<span data-ttu-id="b8b4b-120">Закрывает поставщик транспорта в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-120">Closes down a transport provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="b8b4b-121">транспортлогон</span><span class="sxs-lookup"><span data-stu-id="b8b4b-121">TransportLogon</span></span>](ixpprovider-transportlogon.md) <br/> |<span data-ttu-id="b8b4b-122">Устанавливает сеанс, в котором клиентское приложение выполняет вход в поставщик транспорта.</span><span class="sxs-lookup"><span data-stu-id="b8b4b-122">Establishes a session in which a client application logs on to a transport provider.</span></span>  <br/> |
   

