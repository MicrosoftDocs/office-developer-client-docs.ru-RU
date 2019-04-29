---
title: Иконтабадминремовесторе
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IContabAdmin.RemoveStore
api_type:
- COM
ms.assetid: 2a5fcf5c-8a5a-4774-b8c9-1ac1ff27947d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4865c1c867dd73514ab22ac4e8da628caf154ee7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435420"
---
# <a name="icontabadminremovestore"></a><span data-ttu-id="6cdec-103">IContabAdmin::RemoveStore</span><span class="sxs-lookup"><span data-stu-id="6cdec-103">IContabAdmin::RemoveStore</span></span>

  
  
<span data-ttu-id="6cdec-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6cdec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6cdec-105">Удаляет адресную книгу контакта (CAB-файл), указанную указанным ИДЕНТИФИКАТОРом записи, из иерархии адресной книги.</span><span class="sxs-lookup"><span data-stu-id="6cdec-105">Removes the Contact Address Book (CAB) specified by the given entry ID from the address book hierarchy.</span></span>
  
```cpp
HRESULT RemoveStore(
ULONG cbEntryID, 
LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="6cdec-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6cdec-106">Parameters</span></span>

 <span data-ttu-id="6cdec-107">_Кбентрид_</span><span class="sxs-lookup"><span data-stu-id="6cdec-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="6cdec-108">возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="6cdec-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="6cdec-109">_Лпентрид_</span><span class="sxs-lookup"><span data-stu-id="6cdec-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="6cdec-110">возврата Указатель на идентификатор записи объекта, который требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="6cdec-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    

