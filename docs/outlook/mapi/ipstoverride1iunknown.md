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
ms.openlocfilehash: e73115811fe0009769826e0f6a011c489772f770
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569850"
---
# <a name="ipstoverride1--iunknown"></a><span data-ttu-id="9a773-103">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9a773-103">IPSTOVERRIDE1 : IUnknown</span></span>

  
  
<span data-ttu-id="9a773-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a773-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a773-105">Позволяет поставщику хранилища файлов (PST) личных папок для переопределения политики PSTDisableGrow.</span><span class="sxs-lookup"><span data-stu-id="9a773-105">Allows a Personal Folders file (PST) store provider to override the PSTDisableGrow policy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9a773-106">Наследует от:</span><span class="sxs-lookup"><span data-stu-id="9a773-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="9a773-107">Интерфейс IUnknown</span><span class="sxs-lookup"><span data-stu-id="9a773-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="9a773-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="9a773-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9a773-109">Поставщик хранения PST-файлов</span><span class="sxs-lookup"><span data-stu-id="9a773-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="9a773-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="9a773-110">Called by:</span></span>  <br/> |<span data-ttu-id="9a773-111">Клиент</span><span class="sxs-lookup"><span data-stu-id="9a773-111">Client</span></span>  <br/> |
|<span data-ttu-id="9a773-112">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="9a773-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9a773-113">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="9a773-113">IID_IPSTOVERRIDE1</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9a773-114">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="9a773-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9a773-115">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="9a773-115">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>](ipstoverride1-getpersistedregistrations.md) <br/> |<span data-ttu-id="9a773-116">Получение списка регистраций для файл личных папок (PST).</span><span class="sxs-lookup"><span data-stu-id="9a773-116">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>  <br/> |
|[<span data-ttu-id="9a773-117">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="9a773-117">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>](ipstoverride1-setpersistedregistrations.md) <br/> |<span data-ttu-id="9a773-118">Регистрирует файлы личных папок для автоматического разблокирование Предотвращение дальнейшие вызовы HrTrustedPSTOverrideHandlerCallback.</span><span class="sxs-lookup"><span data-stu-id="9a773-118">Registers Personal Folders files for automatic unlocking, avoiding further calls to HrTrustedPSTOverrideHandlerCallback.</span></span>  <br/> |
|[<span data-ttu-id="9a773-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span><span class="sxs-lookup"><span data-stu-id="9a773-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span></span>](ipstoverride1-overridepstdisablegrow.md) <br/> |<span data-ttu-id="9a773-120">Разблокирует файл личных папок для роста.</span><span class="sxs-lookup"><span data-stu-id="9a773-120">Unlocks a Personal Folders file for growth.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9a773-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="9a773-121">Remarks</span></span>

<span data-ttu-id="9a773-122">Идентификаторы интерфейса обработчик переопределить PST-файлов не могут быть определены в файле загружаемых заголовка, которое имеется в настоящее время, в этом случае будет получить в разделе [Константы MAPI](mapi-constants.md) и можно скопировать и добавьте их в коде.</span><span class="sxs-lookup"><span data-stu-id="9a773-122">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="9a773-123">Используйте макрос DEFINE_GUID определенные в guiddef.h файл заголовка Microsoft Windows Software Development Kit (SDK) для сопоставления имен символьной глобальный уникальный идентификатор (GUID) с их значениями.</span><span class="sxs-lookup"><span data-stu-id="9a773-123">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="9a773-124">Дополнительные сведения см в [реализации обработчика переопределение PST-файлов для обхода политики PSTDisableGrow в Outlook 2007](http://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="9a773-124">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](http://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9a773-125">См. также</span><span class="sxs-lookup"><span data-stu-id="9a773-125">See also</span></span>



[<span data-ttu-id="9a773-126">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9a773-126">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

