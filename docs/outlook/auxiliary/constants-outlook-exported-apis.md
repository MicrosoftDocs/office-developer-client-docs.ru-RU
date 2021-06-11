---
title: Constants (Outlook exported APIs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: В этом разделе содержатся постоянные определения API, Outlook экспорта.
ms.openlocfilehash: 65181932b858da1b32c3fbe5fd0bd7e92ca8dc9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319875"
---
# <a name="constants-outlook-exported-apis"></a><span data-ttu-id="27d09-103">Constants (Outlook exported APIs)</span><span class="sxs-lookup"><span data-stu-id="27d09-103">Constants (Outlook exported APIs)</span></span>

<span data-ttu-id="27d09-104">В этом разделе содержатся постоянные определения API, Outlook экспорта.</span><span class="sxs-lookup"><span data-stu-id="27d09-104">This topic contains constant definitions for APIs that Outlook exports.</span></span>
  
## <a name="definitions-for-time-zone-support"></a><span data-ttu-id="27d09-105">Определения для поддержки часовой зоны</span><span class="sxs-lookup"><span data-stu-id="27d09-105">Definitions for Time Zone support</span></span>

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a><span data-ttu-id="27d09-106">Определения поддержки категорий</span><span class="sxs-lookup"><span data-stu-id="27d09-106">Definitions for Category support</span></span>

|<span data-ttu-id="27d09-107">**Константа**</span><span class="sxs-lookup"><span data-stu-id="27d09-107">**Constant**</span></span>|<span data-ttu-id="27d09-108">**Определение**</span><span class="sxs-lookup"><span data-stu-id="27d09-108">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="27d09-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="27d09-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="27d09-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="27d09-110">0x00000001</span></span>  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a><span data-ttu-id="27d09-111">Разные идентификаторы отправки</span><span class="sxs-lookup"><span data-stu-id="27d09-111">Miscellaneous dispatch identifiers</span></span>

<span data-ttu-id="27d09-112">Outlook предоставляет следующие идентификаторы отправки (отчаялись), чтобы разработчики могли использовать [IDispatch::Invoke,](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) чтобы получить доступ к соответствующему свойству или методу или прослушать соответствующее событие.</span><span class="sxs-lookup"><span data-stu-id="27d09-112">Outlook exposes the following dispatch identifiers (dispids) so that developers can use [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) to access the corresponding property or method, or listen to the corresponding event.</span></span> 
  
|<span data-ttu-id="27d09-113">**Связанная константа**</span><span class="sxs-lookup"><span data-stu-id="27d09-113">**Associated constant**</span></span>|<span data-ttu-id="27d09-114">**Неописуемая величина**</span><span class="sxs-lookup"><span data-stu-id="27d09-114">**Dispid value**</span></span>|<span data-ttu-id="27d09-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="27d09-115">**Description**</span></span>|<span data-ttu-id="27d09-116">**Применимый интерфейс**</span><span class="sxs-lookup"><span data-stu-id="27d09-116">**Applicable interface**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="27d09-117">**dispidFDirty**</span><span class="sxs-lookup"><span data-stu-id="27d09-117">**dispidFDirty**</span></span> <br/> |<span data-ttu-id="27d09-118">0xF024</span><span class="sxs-lookup"><span data-stu-id="27d09-118">0xF024</span></span>  <br/> |<span data-ttu-id="27d09-119">Используется для вызова соответствующего свойства элемента для проверки того, был ли элемент изменен, но не сохранен.</span><span class="sxs-lookup"><span data-stu-id="27d09-119">Used to invoke the corresponding property on an item to verify whether the item has been modified but has not been saved.</span></span>  <br/> |<span data-ttu-id="27d09-120">Объекты уровня элемента</span><span class="sxs-lookup"><span data-stu-id="27d09-120">Item-level objects</span></span>  <br/> |
|<span data-ttu-id="27d09-121">**dispidShowSenderPhoto**</span><span class="sxs-lookup"><span data-stu-id="27d09-121">**dispidShowSenderPhoto**</span></span> <br/> |<span data-ttu-id="27d09-122">0xF0D0</span><span class="sxs-lookup"><span data-stu-id="27d09-122">0xF0D0</span></span>  <br/> |<span data-ttu-id="27d09-123">Используется для вызова соответствующего метода в проводнике или инспекторе, чтобы указать, следует ли отображать изображение контакта на основе заданного аргумента.</span><span class="sxs-lookup"><span data-stu-id="27d09-123">Used to invoke the corresponding method on the explorer or inspector to specify whether to display a contact's picture, based on a given argument.</span></span>  <br/> |<span data-ttu-id="27d09-124">Обозреватель или инспектор</span><span class="sxs-lookup"><span data-stu-id="27d09-124">Explorer or inspector</span></span>  <br/> |
|<span data-ttu-id="27d09-125">**dispidBeforePrint**</span><span class="sxs-lookup"><span data-stu-id="27d09-125">**dispidBeforePrint**</span></span> <br/> |<span data-ttu-id="27d09-126">0xFC8E</span><span class="sxs-lookup"><span data-stu-id="27d09-126">0xFC8E</span></span>  <br/> |<span data-ttu-id="27d09-127">Используется для обработки события из **функции IDispatch::Invoke,** которая загорелась перед операцией печати.</span><span class="sxs-lookup"><span data-stu-id="27d09-127">Used to handle the event from the **IDispatch::Invoke** function that fires before a printing operation.</span></span>  <br/> |<span data-ttu-id="27d09-128">Приложение</span><span class="sxs-lookup"><span data-stu-id="27d09-128">Application</span></span>  <br/> |
|<span data-ttu-id="27d09-129">**dispidEventReadComplete**</span><span class="sxs-lookup"><span data-stu-id="27d09-129">**dispidEventReadComplete**</span></span> <br/> |<span data-ttu-id="27d09-130">0xFC8F</span><span class="sxs-lookup"><span data-stu-id="27d09-130">0xFC8F</span></span>  <br/> |<span data-ttu-id="27d09-131">Используется для обработки события из функции **IDispatch::Invoke,** которая Outlook после завершения чтения свойств элемента.</span><span class="sxs-lookup"><span data-stu-id="27d09-131">Used to handle the event from the **IDispatch::Invoke** function that fires when Outlook has completed reading the properties of the item.</span></span>  <br/> |<span data-ttu-id="27d09-132">Объекты уровня элемента</span><span class="sxs-lookup"><span data-stu-id="27d09-132">Item-level objects</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="27d09-133">См. также</span><span class="sxs-lookup"><span data-stu-id="27d09-133">See also</span></span>

- [<span data-ttu-id="27d09-134">Экспортированные API Outlook</span><span class="sxs-lookup"><span data-stu-id="27d09-134">Outlook exported APIs</span></span>](outlook-exported-apis.md)
- [<span data-ttu-id="27d09-135">Сведения об интерфейсах API, экспортируемых Outlook</span><span class="sxs-lookup"><span data-stu-id="27d09-135">About APIs exported by Outlook</span></span>](about-apis-exported-by-outlook.md)
- <span data-ttu-id="27d09-136">[Определение того, был ли элемент Outlook изменен, но не сохранен (Вспомогательная справка по Outlook)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)  </span><span class="sxs-lookup"><span data-stu-id="27d09-136">[Determine whether an Outlook item has been modified but not saved (Outlook Auxiliary Reference)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)</span></span>
- [<span data-ttu-id="27d09-137">Указание на необходимость отображать изображение контакта в Outlook (Дополнительная справка по Outlook)</span><span class="sxs-lookup"><span data-stu-id="27d09-137">Specify whether to display a contact's picture in Outlook (Outlook Auxiliary Reference)</span></span>](https://msdn.microsoft.com/library/office/gg262879.aspx)
- [<span data-ttu-id="27d09-138">Доступные события и их удлиняется (Outlook экспортируются API)</span><span class="sxs-lookup"><span data-stu-id="27d09-138">Available events and their dispids (Outlook exported APIs)</span></span>](available-events-and-their-dispids-outlook-exported-apis.md)

