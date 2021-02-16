---
title: IPSTOVERRIDEREQ IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ
api_type:
- COM
ms.assetid: 22f497de-4afe-4433-965d-c3b5a66b05da
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7f3f6ae2b9849710bf44d3635fc7bb9a62016f48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356982"
---
# <a name="ipstoverridereq--iunknown"></a><span data-ttu-id="e0bb5-103">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e0bb5-103">IPSTOVERRIDEREQ : IUnknown</span></span>

  
  
<span data-ttu-id="e0bb5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0bb5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0bb5-105">Доступ к ресурсам поставщика файлов личных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="e0bb5-105">Accesses resources of a Personal Folders file (PST) store provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e0bb5-106">Наследуется от:</span><span class="sxs-lookup"><span data-stu-id="e0bb5-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="e0bb5-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="e0bb5-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="e0bb5-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="e0bb5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e0bb5-109">Поставщик PST-магазина</span><span class="sxs-lookup"><span data-stu-id="e0bb5-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="e0bb5-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="e0bb5-110">Called by:</span></span>  <br/> |<span data-ttu-id="e0bb5-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="e0bb5-111">Client applications</span></span>  <br/> |
|<span data-ttu-id="e0bb5-112">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="e0bb5-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e0bb5-113">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="e0bb5-113">IID_IPSTOVERRIDEREQ</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e0bb5-114">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="e0bb5-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e0bb5-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="e0bb5-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |<span data-ttu-id="e0bb5-116">Инициирует процедуру разблокировки для файла личных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="e0bb5-116">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0bb5-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="e0bb5-117">Remarks</span></span>

<span data-ttu-id="e0bb5-118">Идентификаторы интерфейса обработчиков переопределения PST-файлов могут быть не определены в загружаемом файле заголовщика, который вы найдете в разделе "Константы [MAPI"](mapi-constants.md) и сможете копировать и добавлять их в код.</span><span class="sxs-lookup"><span data-stu-id="e0bb5-118">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="e0bb5-119">Используйте макрос DEFINE_GUID, определенный в файле guiddef.h файла загона SDK, чтобы связать символьные имена глобального уникального идентификатора (GUID) с их значениями.</span><span class="sxs-lookup"><span data-stu-id="e0bb5-119">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="e0bb5-120">Дополнительные сведения см. в реализации обработора переопределения PST-данных для обхода [политики PSTDisableGrow в Outlook 2007.](https://support.microsoft.com/kb/956070)</span><span class="sxs-lookup"><span data-stu-id="e0bb5-120">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e0bb5-121">См. также</span><span class="sxs-lookup"><span data-stu-id="e0bb5-121">See also</span></span>



[<span data-ttu-id="e0bb5-122">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e0bb5-122">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)

