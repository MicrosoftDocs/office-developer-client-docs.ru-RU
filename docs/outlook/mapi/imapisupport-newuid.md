---
title: имаписуппортневуид
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.NewUID
api_type:
- COM
ms.assetid: 7994477d-5207-4335-b538-69c98782d52d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a38f7ea475f8a5cbad4f1cc295c3e2550ea8cd66
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406999"
---
# <a name="imapisupportnewuid"></a><span data-ttu-id="82510-103">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="82510-103">IMAPISupport::NewUID</span></span>

  
  
<span data-ttu-id="82510-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82510-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82510-105">Создает новую структуру [мапиуид](mapiuid.md) , которая будет использоваться в качестве уникального идентификатора.</span><span class="sxs-lookup"><span data-stu-id="82510-105">Creates a new [MAPIUID](mapiuid.md) structure to be used as a unique identifier.</span></span> 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a><span data-ttu-id="82510-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="82510-106">Parameters</span></span>

 <span data-ttu-id="82510-107">_лпмуид_</span><span class="sxs-lookup"><span data-stu-id="82510-107">_lpMuid_</span></span>
  
> <span data-ttu-id="82510-108">Указатель на новую структуру **мапиуид** .</span><span class="sxs-lookup"><span data-stu-id="82510-108">A pointer to the new **MAPIUID** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="82510-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82510-109">Return value</span></span>

<span data-ttu-id="82510-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="82510-110">S_OK</span></span> 
  
> <span data-ttu-id="82510-111">Создана новая структура **мапиуид** .</span><span class="sxs-lookup"><span data-stu-id="82510-111">The new **MAPIUID** structure was created.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="82510-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="82510-112">Remarks</span></span>

<span data-ttu-id="82510-113">Метод **имаписуппорт:: невуид** реализован для всех объектов поддержки.</span><span class="sxs-lookup"><span data-stu-id="82510-113">The **IMAPISupport::NewUID** method is implemented for all support objects.</span></span> <span data-ttu-id="82510-114">Поставщики услуг и службы сообщений вызывайте **невуид** , когда им нужно создать долгосрочный уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="82510-114">Service providers and message services call **NewUID** whenever they need to generate a long-term unique identifier.</span></span> <span data-ttu-id="82510-115">Поставщик хранилища сообщений, например, может вызывать **невуид** для получения **мапиуид** , помещаемого в свойство **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) только что созданного сообщения.</span><span class="sxs-lookup"><span data-stu-id="82510-115">A message store provider, for example, might call **NewUID** to obtain a **MAPIUID** to put in the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of a newly created message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="82510-116">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="82510-116">Notes to callers</span></span>

<span data-ttu-id="82510-117">Не путайте структуру **мапиуид** , которую вы регистрируете во время входа в структуры **мапиуид** , создаваемые методом **невуид** .</span><span class="sxs-lookup"><span data-stu-id="82510-117">Do not confuse the **MAPIUID** structure that you register at logon time with the **MAPIUID** structures that the **NewUID** method creates.</span></span> <span data-ttu-id="82510-118">Структура **мапиуид** , регистрируемая при вызове метода [Имаписуппорт:: сетпровидеруид](imapisupport-setprovideruid.md) , представляет адресную книгу или поставщика хранилища сообщений для MAPI и используется для различения идентификаторов записей, создаваемых различными поставщиками.</span><span class="sxs-lookup"><span data-stu-id="82510-118">The **MAPIUID** structure that you register when you call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method represents your address book or message store provider to MAPI and is used to distinguish entry identifiers that different providers create.</span></span> <span data-ttu-id="82510-119">Эта структура **мапиуид** должна быть жестко запрограммирована и не была получена через вызов **невуид**.</span><span class="sxs-lookup"><span data-stu-id="82510-119">This **MAPIUID** structure should be hard-coded and not obtained through a call to **NewUID**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="82510-120">См. также</span><span class="sxs-lookup"><span data-stu-id="82510-120">See also</span></span>



[<span data-ttu-id="82510-121">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="82510-121">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="82510-122">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="82510-122">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

