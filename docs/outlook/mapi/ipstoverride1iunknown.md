---
title: IPSTOVERRIDE1 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1
api_type:
- COM
ms.assetid: d26cee81-45ea-4fd3-8a54-5f35264b5d6a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: db2853080b1fc2ff3a346dcfb8d112237b7f3459
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809567"
---
# <a name="ipstoverride1--iunknown"></a><span data-ttu-id="16a82-103">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="16a82-103">IPSTOVERRIDE1 : IUnknown</span></span>

  
  
<span data-ttu-id="16a82-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="16a82-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="16a82-105">Позволяет поставщику хранилища файлов (PST) личных папок для переопределения политики PSTDisableGrow.</span><span class="sxs-lookup"><span data-stu-id="16a82-105">Allows a Personal Folders file (PST) store provider to override the PSTDisableGrow policy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="16a82-106">Наследует от:</span><span class="sxs-lookup"><span data-stu-id="16a82-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="16a82-107">Интерфейс IUnknown</span><span class="sxs-lookup"><span data-stu-id="16a82-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="16a82-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="16a82-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="16a82-109">Поставщик хранения PST-файлов</span><span class="sxs-lookup"><span data-stu-id="16a82-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="16a82-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="16a82-110">Called by:</span></span>  <br/> |<span data-ttu-id="16a82-111">Клиент</span><span class="sxs-lookup"><span data-stu-id="16a82-111">Client</span></span>  <br/> |
|<span data-ttu-id="16a82-112">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="16a82-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="16a82-113">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="16a82-113">IID_IPSTOVERRIDE1</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="16a82-114">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="16a82-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="16a82-115">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="16a82-115">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>](ipstoverride1-getpersistedregistrations.md) <br/> |<span data-ttu-id="16a82-116">Получение списка регистраций для файл личных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="16a82-116">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>  <br/> |
|[<span data-ttu-id="16a82-117">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="16a82-117">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>](ipstoverride1-setpersistedregistrations.md) <br/> |<span data-ttu-id="16a82-118">Регистрирует файлы личных папок для автоматического разблокирование Предотвращение дальнейшие вызовы HrTrustedPSTOverrideHandlerCallback.</span><span class="sxs-lookup"><span data-stu-id="16a82-118">Registers Personal Folders files for automatic unlocking, avoiding further calls to HrTrustedPSTOverrideHandlerCallback.</span></span>  <br/> |
|[<span data-ttu-id="16a82-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span><span class="sxs-lookup"><span data-stu-id="16a82-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span></span>](ipstoverride1-overridepstdisablegrow.md) <br/> |<span data-ttu-id="16a82-120">Разблокирует файл личных папок для роста.</span><span class="sxs-lookup"><span data-stu-id="16a82-120">Unlocks a Personal Folders file for growth.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16a82-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="16a82-121">Remarks</span></span>

<span data-ttu-id="16a82-122">Идентификаторы интерфейса обработчик переопределить PST-файлов не могут быть определены в файле загружаемых заголовка, которое имеется в настоящее время, в этом случае будет получить в разделе [Константы MAPI](mapi-constants.md) и можно скопировать и добавьте их в коде.</span><span class="sxs-lookup"><span data-stu-id="16a82-122">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="16a82-123">Используйте макрос DEFINE_GUID определенные в guiddef.h файл заголовка Microsoft Windows Software Development Kit (SDK) для сопоставления имен символьной глобальный уникальный идентификатор (GUID) с их значениями.</span><span class="sxs-lookup"><span data-stu-id="16a82-123">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="16a82-124">Дополнительные сведения см в [реализации обработчика переопределение PST-файлов для обхода политики PSTDisableGrow в Outlook 2007](http://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="16a82-124">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](http://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="16a82-125">См. также</span><span class="sxs-lookup"><span data-stu-id="16a82-125">See also</span></span>



[<span data-ttu-id="16a82-126">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="16a82-126">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

