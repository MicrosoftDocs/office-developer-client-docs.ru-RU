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
ms.openlocfilehash: 6ee4524d08e334df858c2f035f1b21bd2b0a1c8b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809560"
---
# <a name="ipstoverridereq--iunknown"></a><span data-ttu-id="68044-103">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="68044-103">IPSTOVERRIDEREQ : IUnknown</span></span>

  
  
<span data-ttu-id="68044-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="68044-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="68044-105">Поставщик хранилища доступ к ресурсам файл личных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="68044-105">Accesses resources of a Personal Folders file (PST) store provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="68044-106">Наследует от:</span><span class="sxs-lookup"><span data-stu-id="68044-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="68044-107">Интерфейс IUnknown</span><span class="sxs-lookup"><span data-stu-id="68044-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="68044-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="68044-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="68044-109">Поставщик хранения PST-файлов</span><span class="sxs-lookup"><span data-stu-id="68044-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="68044-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="68044-110">Called by:</span></span>  <br/> |<span data-ttu-id="68044-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="68044-111">Client applications</span></span>  <br/> |
|<span data-ttu-id="68044-112">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="68044-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="68044-113">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="68044-113">IID_IPSTOVERRIDEREQ</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="68044-114">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="68044-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="68044-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="68044-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |<span data-ttu-id="68044-116">Инициирует разблокировка процедура файл личных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="68044-116">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68044-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="68044-117">Remarks</span></span>

<span data-ttu-id="68044-118">Идентификаторы интерфейса обработчик переопределить PST-файлов не могут быть определены в файле загружаемых заголовка, которое имеется в настоящее время, в этом случае будет получить в разделе [Константы MAPI](mapi-constants.md) и можно скопировать и добавьте их в коде.</span><span class="sxs-lookup"><span data-stu-id="68044-118">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="68044-119">Используйте макрос DEFINE_GUID определенные в guiddef.h файл заголовка Microsoft Windows Software Development Kit (SDK) для сопоставления имен символьной глобальный уникальный идентификатор (GUID) с их значениями.</span><span class="sxs-lookup"><span data-stu-id="68044-119">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="68044-120">Дополнительные сведения см в [реализации обработчика переопределение PST-файлов для обхода политики PSTDisableGrow в Outlook 2007](http://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="68044-120">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](http://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="68044-121">См. также</span><span class="sxs-lookup"><span data-stu-id="68044-121">See also</span></span>



[<span data-ttu-id="68044-122">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="68044-122">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)

