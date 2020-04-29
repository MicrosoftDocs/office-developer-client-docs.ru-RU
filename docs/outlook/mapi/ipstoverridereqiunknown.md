---
title: ИПСТОВЕРРИДЕРЕК IUnknown
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
# <a name="ipstoverridereq--iunknown"></a><span data-ttu-id="d5dbe-103">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d5dbe-103">IPSTOVERRIDEREQ : IUnknown</span></span>

  
  
<span data-ttu-id="d5dbe-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5dbe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5dbe-105">Получает доступ к ресурсам поставщика хранилища файлов личных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="d5dbe-105">Accesses resources of a Personal Folders file (PST) store provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d5dbe-106">Наследование от:</span><span class="sxs-lookup"><span data-stu-id="d5dbe-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="d5dbe-107">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="d5dbe-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="d5dbe-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="d5dbe-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d5dbe-109">Поставщик хранилища PST</span><span class="sxs-lookup"><span data-stu-id="d5dbe-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="d5dbe-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="d5dbe-110">Called by:</span></span>  <br/> |<span data-ttu-id="d5dbe-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="d5dbe-111">Client applications</span></span>  <br/> |
|<span data-ttu-id="d5dbe-112">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="d5dbe-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="d5dbe-113">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="d5dbe-113">IID_IPSTOVERRIDEREQ</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="d5dbe-114">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="d5dbe-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="d5dbe-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="d5dbe-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |<span data-ttu-id="d5dbe-116">Инициирует процедуру разблокировки для файла личных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="d5dbe-116">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5dbe-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="d5dbe-117">Remarks</span></span>

<span data-ttu-id="d5dbe-118">Идентификаторы интерфейса обработчика переопределения PST-файлов могут быть не определены в текущем загружаемом файле заголовков, в этом случае вы найдете их в разделе [константы MAPI](mapi-constants.md) и можете скопировать их в свой код.</span><span class="sxs-lookup"><span data-stu-id="d5dbe-118">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="d5dbe-119">Используйте макрос DEFINE_GUID, определенный в файле заголовка пакета средств разработки программного обеспечения (SDK) для Microsoft Windows (SDK) guiddef. h, для сопоставления псевдонимов глобального уникального идентификатора (GUID) с их значениями.</span><span class="sxs-lookup"><span data-stu-id="d5dbe-119">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="d5dbe-120">Для получения дополнительных сведений Узнайте, [как реализовать обработчик переопределения PST-файлов, чтобы обойти политику пстдисаблегров в Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="d5dbe-120">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d5dbe-121">См. также</span><span class="sxs-lookup"><span data-stu-id="d5dbe-121">See also</span></span>



[<span data-ttu-id="d5dbe-122">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d5dbe-122">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)

