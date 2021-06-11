---
title: IFolderSupport IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport
api_type:
- COM
ms.assetid: a4b03a66-cf6d-cd20-f1df-b247d3ee87aa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: da186e6804fc3d3c820551fee66519a2ff76f0db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415777"
---
# <a name="ifoldersupport--iunknown"></a><span data-ttu-id="58671-103">IFolderSupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="58671-103">IFolderSupport : IUnknown</span></span>

  
  
<span data-ttu-id="58671-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58671-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58671-105">Предоставляет сведения о поддержке папки для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="58671-105">Provides information about a folder's support for sharing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="58671-106">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="58671-106">Provided by:</span></span>  <br/> |<span data-ttu-id="58671-107">Поставщик магазина сообщений</span><span class="sxs-lookup"><span data-stu-id="58671-107">Message store provider</span></span>  <br/> |
|<span data-ttu-id="58671-108">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="58671-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="58671-109">IID_IFolderSupport</span><span class="sxs-lookup"><span data-stu-id="58671-109">IID_IFolderSupport</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="58671-110">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="58671-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58671-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="58671-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span></span> <br/> |<span data-ttu-id="58671-112">Получает сведения о поддержке папки для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="58671-112">Gets information about a folder's support for sharing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58671-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="58671-113">Remarks</span></span>

<span data-ttu-id="58671-114">Как правило, Microsoft Office Outlook поставщик магазина MAPI должен реализовать этот интерфейс, если поставщик хочет поделиться папкой.</span><span class="sxs-lookup"><span data-stu-id="58671-114">Generally, Microsoft Office Outlook requires a MAPI store provider to implement this interface if the provider wants to share a folder.</span></span> <span data-ttu-id="58671-115">Исключением является поставщик Exchange Server, который может обмениваться папками без реализации этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="58671-115">The exception is the Exchange Server store provider, which can share folders without implementing this interface.</span></span>
  
<span data-ttu-id="58671-116">Клиент может запрашивать **[IMAPIFolder](imapifolderimapicontainer.md)** для **IFolderSupport**.</span><span class="sxs-lookup"><span data-stu-id="58671-116">A client can query an **[IMAPIFolder](imapifolderimapicontainer.md)** for **IFolderSupport**.</span></span> <span data-ttu-id="58671-117">Если это удастся, **позвоните** **в IFolderSupport::GetSupportMask** и проверьте, FS_SUPPORTS_SHARING необходимо установить бит.</span><span class="sxs-lookup"><span data-stu-id="58671-117">If that succeeds, call **IFolderSupport::GetSupportMask** and check for the **FS_SUPPORTS_SHARING** bit to be set.</span></span> 
  

