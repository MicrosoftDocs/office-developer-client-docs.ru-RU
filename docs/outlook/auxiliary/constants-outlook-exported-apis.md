---
title: Constants (Outlook exported APIs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: В этом разделе содержатся определения констант для API, которые экспортируются Outlook.
ms.openlocfilehash: 65181932b858da1b32c3fbe5fd0bd7e92ca8dc9f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386077"
---
# <a name="constants-outlook-exported-apis"></a><span data-ttu-id="d0a6d-103">Constants (Outlook exported APIs)</span><span class="sxs-lookup"><span data-stu-id="d0a6d-103">Constants (Outlook exported APIs)</span></span>

<span data-ttu-id="d0a6d-104">В этом разделе содержатся определения констант для API, которые экспортируются Outlook.</span><span class="sxs-lookup"><span data-stu-id="d0a6d-104">This topic contains constant definitions for APIs that Outlook exports.</span></span>
  
## <a name="definitions-for-time-zone-support"></a><span data-ttu-id="d0a6d-105">Поддерживает определения для часового пояса</span><span class="sxs-lookup"><span data-stu-id="d0a6d-105">Definitions for Time Zone support</span></span>

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a><span data-ttu-id="d0a6d-106">Поддерживает определения для категории</span><span class="sxs-lookup"><span data-stu-id="d0a6d-106">Definitions for Category support</span></span>

|<span data-ttu-id="d0a6d-107">**Constant**</span><span class="sxs-lookup"><span data-stu-id="d0a6d-107">**Constant**</span></span>|<span data-ttu-id="d0a6d-108">**Определение**</span><span class="sxs-lookup"><span data-stu-id="d0a6d-108">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d0a6d-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="d0a6d-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="d0a6d-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d0a6d-110">0x00000001</span></span>  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a><span data-ttu-id="d0a6d-111">Идентификаторы прочие диспетчера</span><span class="sxs-lookup"><span data-stu-id="d0a6d-111">Miscellaneous dispatch identifiers</span></span>

<span data-ttu-id="d0a6d-112">Outlook предоставляет следующие идентификаторов отправки (DISPID), чтобы [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) могут использоваться разработчиками для доступа к соответствующее свойство или метод или прослушивание для соответствующих событий.</span><span class="sxs-lookup"><span data-stu-id="d0a6d-112">Outlook exposes the following dispatch identifiers (dispids) so that developers can use [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) to access the corresponding property or method, or listen to the corresponding event.</span></span> 
  
|<span data-ttu-id="d0a6d-113">**Связанные константа**</span><span class="sxs-lookup"><span data-stu-id="d0a6d-113">**Associated constant**</span></span>|<span data-ttu-id="d0a6d-114">**Значение DispId**</span><span class="sxs-lookup"><span data-stu-id="d0a6d-114">**Dispid value**</span></span>|<span data-ttu-id="d0a6d-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d0a6d-115">**Description**</span></span>|<span data-ttu-id="d0a6d-116">**Доступный интерфейс**</span><span class="sxs-lookup"><span data-stu-id="d0a6d-116">**Applicable interface**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d0a6d-117">**dispidFDirty**</span><span class="sxs-lookup"><span data-stu-id="d0a6d-117">**dispidFDirty**</span></span> <br/> |<span data-ttu-id="d0a6d-118">0xF024</span><span class="sxs-lookup"><span data-stu-id="d0a6d-118">0xF024</span></span>  <br/> |<span data-ttu-id="d0a6d-119">Используется для вызова соответствующее свойство элемента для проверки, является ли элемент был изменен, но не был сохранен.</span><span class="sxs-lookup"><span data-stu-id="d0a6d-119">Used to invoke the corresponding property on an item to verify whether the item has been modified but has not been saved.</span></span>  <br/> |<span data-ttu-id="d0a6d-120">Объекты на уровне элементов</span><span class="sxs-lookup"><span data-stu-id="d0a6d-120">Item-level objects</span></span>  <br/> |
|<span data-ttu-id="d0a6d-121">**dispidShowSenderPhoto**</span><span class="sxs-lookup"><span data-stu-id="d0a6d-121">**dispidShowSenderPhoto**</span></span> <br/> |<span data-ttu-id="d0a6d-122">0xF0D0</span><span class="sxs-lookup"><span data-stu-id="d0a6d-122">0xF0D0</span></span>  <br/> |<span data-ttu-id="d0a6d-123">Используется для вызова на проводника или инспектора, укажите, нужно ли отображать фотографии контакта, на основании данный аргумент через соответствующий метод.</span><span class="sxs-lookup"><span data-stu-id="d0a6d-123">Used to invoke the corresponding method on the explorer or inspector to specify whether to display a contact's picture, based on a given argument.</span></span>  <br/> |<span data-ttu-id="d0a6d-124">Проводника или инспектора</span><span class="sxs-lookup"><span data-stu-id="d0a6d-124">Explorer or inspector</span></span>  <br/> |
|<span data-ttu-id="d0a6d-125">**dispidBeforePrint**</span><span class="sxs-lookup"><span data-stu-id="d0a6d-125">**dispidBeforePrint**</span></span> <br/> |<span data-ttu-id="d0a6d-126">0xFC8E</span><span class="sxs-lookup"><span data-stu-id="d0a6d-126">0xFC8E</span></span>  <br/> |<span data-ttu-id="d0a6d-127">Используется для обработки событий из функции **IDispatch::Invoke** , которое вызывается перед операцией печати.</span><span class="sxs-lookup"><span data-stu-id="d0a6d-127">Used to handle the event from the **IDispatch::Invoke** function that fires before a printing operation.</span></span>  <br/> |<span data-ttu-id="d0a6d-128">Для приложения</span><span class="sxs-lookup"><span data-stu-id="d0a6d-128">Application</span></span>  <br/> |
|<span data-ttu-id="d0a6d-129">**dispidEventReadComplete**</span><span class="sxs-lookup"><span data-stu-id="d0a6d-129">**dispidEventReadComplete**</span></span> <br/> |<span data-ttu-id="d0a6d-130">0xFC8F</span><span class="sxs-lookup"><span data-stu-id="d0a6d-130">0xFC8F</span></span>  <br/> |<span data-ttu-id="d0a6d-131">Используется для обработки событий из функции **IDispatch::Invoke** , которое вызывается после завершения чтение свойств элемента Outlook.</span><span class="sxs-lookup"><span data-stu-id="d0a6d-131">Used to handle the event from the **IDispatch::Invoke** function that fires when Outlook has completed reading the properties of the item.</span></span>  <br/> |<span data-ttu-id="d0a6d-132">Объекты на уровне элементов</span><span class="sxs-lookup"><span data-stu-id="d0a6d-132">Item-level objects</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0a6d-133">См. также</span><span class="sxs-lookup"><span data-stu-id="d0a6d-133">See also</span></span>

- [<span data-ttu-id="d0a6d-134">Экспортированные API Outlook</span><span class="sxs-lookup"><span data-stu-id="d0a6d-134">Outlook exported APIs</span></span>](outlook-exported-apis.md)
- [<span data-ttu-id="d0a6d-135">Сведения об интерфейсах API, экспортируемых Outlook</span><span class="sxs-lookup"><span data-stu-id="d0a6d-135">About APIs exported by Outlook</span></span>](about-apis-exported-by-outlook.md)
- [<span data-ttu-id="d0a6d-136">Определить, является ли элемент Outlook был изменен, но не сохраняются (Outlook дополнительные справочные материалы по)</span><span class="sxs-lookup"><span data-stu-id="d0a6d-136">Determine whether an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [<span data-ttu-id="d0a6d-137">Укажите, нужно ли отображать фотографии контакта в Outlook (Outlook дополнительные справочные материалы по)</span><span class="sxs-lookup"><span data-stu-id="d0a6d-137">Specify whether to display a contact's picture in Outlook (Outlook Auxiliary Reference)</span></span>](https://msdn.microsoft.com/library/office/gg262879.aspx)
- [<span data-ttu-id="d0a6d-138">Доступные события и их идентификаторы DISPID (Outlook экспортировать API-интерфейсы)</span><span class="sxs-lookup"><span data-stu-id="d0a6d-138">Available events and their dispids (Outlook exported APIs)</span></span>](available-events-and-their-dispids-outlook-exported-apis.md)

