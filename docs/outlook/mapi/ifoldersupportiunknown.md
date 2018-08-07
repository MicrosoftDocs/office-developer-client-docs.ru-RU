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
ms.openlocfilehash: a4a1c78e65d9a515b2b42d7e0a2bc3a8b4bd8869
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808843"
---
# <a name="ifoldersupport--iunknown"></a><span data-ttu-id="0cfde-103">IFolderSupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0cfde-103">IFolderSupport : IUnknown</span></span>

  
  
<span data-ttu-id="0cfde-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0cfde-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0cfde-105">Предоставляет сведения о поддержке папки для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="0cfde-105">Provides information about a folder's support for sharing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0cfde-106">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="0cfde-106">Provided by:</span></span>  <br/> |<span data-ttu-id="0cfde-107">Поставщик хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="0cfde-107">Message store provider</span></span>  <br/> |
|<span data-ttu-id="0cfde-108">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="0cfde-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0cfde-109">IID_IFolderSupport</span><span class="sxs-lookup"><span data-stu-id="0cfde-109">IID_IFolderSupport</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0cfde-110">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="0cfde-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0cfde-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="0cfde-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span></span> <br/> |<span data-ttu-id="0cfde-112">Получает сведения о поддержке папки для совместного доступа.</span><span class="sxs-lookup"><span data-stu-id="0cfde-112">Gets information about a folder's support for sharing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0cfde-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="0cfde-113">Remarks</span></span>

<span data-ttu-id="0cfde-114">Как правило Microsoft Office Outlook требуется поставщик, чтобы реализовать интерфейс, если поставщик хочет общей папки хранилища MAPI.</span><span class="sxs-lookup"><span data-stu-id="0cfde-114">Generally, Microsoft Office Outlook requires a MAPI store provider to implement this interface if the provider wants to share a folder.</span></span> <span data-ttu-id="0cfde-115">Исключение поставщика хранилища Exchange Server, который можно совместно использовать папки не реализации этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0cfde-115">The exception is the Exchange Server store provider, which can share folders without implementing this interface.</span></span>
  
<span data-ttu-id="0cfde-116">Клиент может запросить **[IMAPIFolder](imapifolderimapicontainer.md)** **IFolderSupport**.</span><span class="sxs-lookup"><span data-stu-id="0cfde-116">A client can query an **[IMAPIFolder](imapifolderimapicontainer.md)** for **IFolderSupport**.</span></span> <span data-ttu-id="0cfde-117">В случае успеха вызвать **IFolderSupport::GetSupportMask** и проверить наличие бит **FS_SUPPORTS_SHARING** должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="0cfde-117">If that succeeds, call **IFolderSupport::GetSupportMask** and check for the **FS_SUPPORTS_SHARING** bit to be set.</span></span> 
  

