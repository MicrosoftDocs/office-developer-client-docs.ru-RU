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
ms.openlocfilehash: 0aa77ced9d0c242dcafb84ca1e1a60d02db9504a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404696"
---
# <a name="ixpprovider--iunknown"></a><span data-ttu-id="4d637-103">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4d637-103">IXPProvider : IUnknown</span></span>

  
  
<span data-ttu-id="4d637-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d637-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d637-105">Инициализирует объект поставщика транспорта и закрывает объект, когда он больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="4d637-105">Initializes a transport provider object and shuts down the object when it is no longer needed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4d637-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="4d637-106">Header file:</span></span>  <br/> |<span data-ttu-id="4d637-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="4d637-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="4d637-108">Подвергается:</span><span class="sxs-lookup"><span data-stu-id="4d637-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="4d637-109">Объекты поставщиков транспорта</span><span class="sxs-lookup"><span data-stu-id="4d637-109">Transport provider objects</span></span>  <br/> |
|<span data-ttu-id="4d637-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="4d637-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="4d637-111">Поставщики транспорта</span><span class="sxs-lookup"><span data-stu-id="4d637-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="4d637-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="4d637-112">Called by:</span></span>  <br/> |<span data-ttu-id="4d637-113">Шпалер MAPI</span><span class="sxs-lookup"><span data-stu-id="4d637-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="4d637-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="4d637-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4d637-115">IID_IXPProvider</span><span class="sxs-lookup"><span data-stu-id="4d637-115">IID_IXPProvider</span></span>  <br/> |
|<span data-ttu-id="4d637-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="4d637-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="4d637-117">LPXPROVIDER</span><span class="sxs-lookup"><span data-stu-id="4d637-117">LPXPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4d637-118">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="4d637-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4d637-119">Shutdown</span><span class="sxs-lookup"><span data-stu-id="4d637-119">Shutdown</span></span>](ixpprovider-shutdown.md) <br/> |<span data-ttu-id="4d637-120">Упорядоченно закрывает поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="4d637-120">Closes down a transport provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="4d637-121">TransportLogon</span><span class="sxs-lookup"><span data-stu-id="4d637-121">TransportLogon</span></span>](ixpprovider-transportlogon.md) <br/> |<span data-ttu-id="4d637-122">Создает сеанс, в котором клиентская заявка входит в систему поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="4d637-122">Establishes a session in which a client application logs on to a transport provider.</span></span>  <br/> |
   

