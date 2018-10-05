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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389108"
---
# <a name="ipstoverridereq--iunknown"></a><span data-ttu-id="18817-103">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="18817-103">IPSTOVERRIDEREQ : IUnknown</span></span>

  
  
<span data-ttu-id="18817-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18817-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18817-105">Поставщик хранилища доступ к ресурсам файл личных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="18817-105">Accesses resources of a Personal Folders file (PST) store provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="18817-106">Наследует от:</span><span class="sxs-lookup"><span data-stu-id="18817-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="18817-107">Интерфейс IUnknown</span><span class="sxs-lookup"><span data-stu-id="18817-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="18817-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="18817-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="18817-109">Поставщик хранения PST-файлов</span><span class="sxs-lookup"><span data-stu-id="18817-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="18817-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="18817-110">Called by:</span></span>  <br/> |<span data-ttu-id="18817-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="18817-111">Client applications</span></span>  <br/> |
|<span data-ttu-id="18817-112">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="18817-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="18817-113">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="18817-113">IID_IPSTOVERRIDEREQ</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="18817-114">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="18817-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="18817-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="18817-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |<span data-ttu-id="18817-116">Инициирует разблокировка процедура файл личных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="18817-116">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18817-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="18817-117">Remarks</span></span>

<span data-ttu-id="18817-118">Идентификаторы интерфейса обработчик переопределить PST-файлов не могут быть определены в файле загружаемых заголовка, которое имеется в настоящее время, в этом случае будет получить в разделе [Константы MAPI](mapi-constants.md) и можно скопировать и добавьте их в коде.</span><span class="sxs-lookup"><span data-stu-id="18817-118">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="18817-119">Используйте макрос DEFINE_GUID определенные в guiddef.h файл заголовка Microsoft Windows Software Development Kit (SDK) для сопоставления имен символьной глобальный уникальный идентификатор (GUID) с их значениями.</span><span class="sxs-lookup"><span data-stu-id="18817-119">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="18817-120">Дополнительные сведения см в [реализации обработчика переопределение PST-файлов для обхода политики PSTDisableGrow в Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="18817-120">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="18817-121">См. также</span><span class="sxs-lookup"><span data-stu-id="18817-121">See also</span></span>



[<span data-ttu-id="18817-122">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="18817-122">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)

