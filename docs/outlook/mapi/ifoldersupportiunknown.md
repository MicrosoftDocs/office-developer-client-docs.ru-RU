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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351389"
---
# <a name="ifoldersupport--iunknown"></a><span data-ttu-id="612d9-103">IFolderSupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="612d9-103">IFolderSupport : IUnknown</span></span>

  
  
<span data-ttu-id="612d9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="612d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="612d9-105">Предоставляет сведения о поддержке общего доступа к папке.</span><span class="sxs-lookup"><span data-stu-id="612d9-105">Provides information about a folder's support for sharing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="612d9-106">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="612d9-106">Provided by:</span></span>  <br/> |<span data-ttu-id="612d9-107">Поставщик хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="612d9-107">Message store provider</span></span>  <br/> |
|<span data-ttu-id="612d9-108">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="612d9-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="612d9-109">Иид_ифолдерсуппорт</span><span class="sxs-lookup"><span data-stu-id="612d9-109">IID_IFolderSupport</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="612d9-110">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="612d9-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="612d9-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="612d9-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span></span> <br/> |<span data-ttu-id="612d9-112">Получает сведения о поддержке папки для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="612d9-112">Gets information about a folder's support for sharing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="612d9-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="612d9-113">Remarks</span></span>

<span data-ttu-id="612d9-114">Как правило, для реализации этого интерфейса в Microsoft Office Outlook требуется поставщик хранилища MAPI, если поставщику требуется предоставить общий доступ к папке.</span><span class="sxs-lookup"><span data-stu-id="612d9-114">Generally, Microsoft Office Outlook requires a MAPI store provider to implement this interface if the provider wants to share a folder.</span></span> <span data-ttu-id="612d9-115">Исключением является поставщик хранилища Exchange Server, который может предоставлять общий доступ к папкам без реализации этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="612d9-115">The exception is the Exchange Server store provider, which can share folders without implementing this interface.</span></span>
  
<span data-ttu-id="612d9-116">Клиент может запросить **[IMAPIFolder](imapifolderimapicontainer.md)** для **IFolderSupport**.</span><span class="sxs-lookup"><span data-stu-id="612d9-116">A client can query an **[IMAPIFolder](imapifolderimapicontainer.md)** for **IFolderSupport**.</span></span> <span data-ttu-id="612d9-117">В случае успеха вызовите метод **IFolderSupport:: GetSupportMask** и проверьте, установлен ли бит **фс_суппортс_шаринг** .</span><span class="sxs-lookup"><span data-stu-id="612d9-117">If that succeeds, call **IFolderSupport::GetSupportMask** and check for the **FS_SUPPORTS_SHARING** bit to be set.</span></span> 
  

