---
title: Имаписуппортневуид
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330200"
---
# <a name="imapisupportnewuid"></a><span data-ttu-id="f1b33-103">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="f1b33-103">IMAPISupport::NewUID</span></span>

  
  
<span data-ttu-id="f1b33-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1b33-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1b33-105">Создает новую структуру [мапиуид](mapiuid.md) , которая будет использоваться в качестве уникального идентификатора.</span><span class="sxs-lookup"><span data-stu-id="f1b33-105">Creates a new [MAPIUID](mapiuid.md) structure to be used as a unique identifier.</span></span> 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a><span data-ttu-id="f1b33-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1b33-106">Parameters</span></span>

 <span data-ttu-id="f1b33-107">_Лпмуид_</span><span class="sxs-lookup"><span data-stu-id="f1b33-107">_lpMuid_</span></span>
  
> <span data-ttu-id="f1b33-108">Указатель на новую структуру **мапиуид** .</span><span class="sxs-lookup"><span data-stu-id="f1b33-108">A pointer to the new **MAPIUID** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f1b33-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1b33-109">Return value</span></span>

<span data-ttu-id="f1b33-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="f1b33-110">S_OK</span></span> 
  
> <span data-ttu-id="f1b33-111">Создана новая структура **мапиуид** .</span><span class="sxs-lookup"><span data-stu-id="f1b33-111">The new **MAPIUID** structure was created.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f1b33-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1b33-112">Remarks</span></span>

<span data-ttu-id="f1b33-113">Метод **имаписуппорт:: невуид** реализован для всех объектов поддержки.</span><span class="sxs-lookup"><span data-stu-id="f1b33-113">The **IMAPISupport::NewUID** method is implemented for all support objects.</span></span> <span data-ttu-id="f1b33-114">Поставщики услуг и службы сообщений вызывайте **невуид** , когда им нужно создать долгосрочный уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="f1b33-114">Service providers and message services call **NewUID** whenever they need to generate a long-term unique identifier.</span></span> <span data-ttu-id="f1b33-115">Например, поставщик хранилища сообщений может вызвать **невуид** , чтобы получить **мапиуид** , которое будет размещено в свойстве **пр_сеарч_кэй** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) только что созданного сообщения.</span><span class="sxs-lookup"><span data-stu-id="f1b33-115">A message store provider, for example, might call **NewUID** to obtain a **MAPIUID** to put in the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of a newly created message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="f1b33-116">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="f1b33-116">Notes to callers</span></span>

<span data-ttu-id="f1b33-117">Не путайте структуру **мапиуид** , которую вы регистрируете во время входа в структуры **мапиуид** , создаваемые методом **невуид** .</span><span class="sxs-lookup"><span data-stu-id="f1b33-117">Do not confuse the **MAPIUID** structure that you register at logon time with the **MAPIUID** structures that the **NewUID** method creates.</span></span> <span data-ttu-id="f1b33-118">Структура **мапиуид** , регистрируемая при вызове метода [Имаписуппорт:: сетпровидеруид](imapisupport-setprovideruid.md) , представляет адресную книгу или поставщика хранилища сообщений для MAPI и используется для различения идентификаторов записей, создаваемых различными поставщиками.</span><span class="sxs-lookup"><span data-stu-id="f1b33-118">The **MAPIUID** structure that you register when you call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method represents your address book or message store provider to MAPI and is used to distinguish entry identifiers that different providers create.</span></span> <span data-ttu-id="f1b33-119">Эта структура **мапиуид** должна быть жестко запрограммирована и не была получена через вызов **невуид**.</span><span class="sxs-lookup"><span data-stu-id="f1b33-119">This **MAPIUID** structure should be hard-coded and not obtained through a call to **NewUID**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f1b33-120">См. также</span><span class="sxs-lookup"><span data-stu-id="f1b33-120">See also</span></span>



[<span data-ttu-id="f1b33-121">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="f1b33-121">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="f1b33-122">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f1b33-122">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

