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
ms.openlocfilehash: e12f69e3486e5eeb9087b30753735f7f910dc6f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809657"
---
# <a name="ixpprovider--iunknown"></a><span data-ttu-id="76566-103">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="76566-103">IXPProvider : IUnknown</span></span>

  
  
<span data-ttu-id="76566-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="76566-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="76566-105">Инициализирует объект поставщика транспорта и завершает работу объекта, если они больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="76566-105">Initializes a transport provider object and shuts down the object when it is no longer needed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="76566-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="76566-106">Header file:</span></span>  <br/> |<span data-ttu-id="76566-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="76566-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="76566-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="76566-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="76566-109">Объекты поставщика транспорта</span><span class="sxs-lookup"><span data-stu-id="76566-109">Transport provider objects</span></span>  <br/> |
|<span data-ttu-id="76566-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="76566-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="76566-111">Поставщиками транспорта</span><span class="sxs-lookup"><span data-stu-id="76566-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="76566-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="76566-112">Called by:</span></span>  <br/> |<span data-ttu-id="76566-113">Диспетчер очереди MAPI</span><span class="sxs-lookup"><span data-stu-id="76566-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="76566-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="76566-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="76566-115">IID_IXPProvider</span><span class="sxs-lookup"><span data-stu-id="76566-115">IID_IXPProvider</span></span>  <br/> |
|<span data-ttu-id="76566-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="76566-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="76566-117">LPXPROVIDER</span><span class="sxs-lookup"><span data-stu-id="76566-117">LPXPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="76566-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="76566-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="76566-119">Shutdown</span><span class="sxs-lookup"><span data-stu-id="76566-119">Shutdown</span></span>](ixpprovider-shutdown.md) <br/> |<span data-ttu-id="76566-120">Закрывает вниз поставщика транспорта определенным образом.</span><span class="sxs-lookup"><span data-stu-id="76566-120">Closes down a transport provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="76566-121">TransportLogon</span><span class="sxs-lookup"><span data-stu-id="76566-121">TransportLogon</span></span>](ixpprovider-transportlogon.md) <br/> |<span data-ttu-id="76566-122">Устанавливает сеанс, в котором клиентское приложение входит в систему поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="76566-122">Establishes a session in which a client application logs on to a transport provider.</span></span>  <br/> |
   

