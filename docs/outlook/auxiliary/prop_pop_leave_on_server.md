---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Указывает, что копия сообщения на сервере остается на сервере для учетной записи POP.
ms.openlocfilehash: e1bbddea0f10c07d630676960d1b330f6055e137
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326490"
---
# <a name="proppopleaveonserver"></a><span data-ttu-id="479ed-103">PROP_POP_LEAVE_ON_SERVER</span><span class="sxs-lookup"><span data-stu-id="479ed-103">PROP_POP_LEAVE_ON_SERVER</span></span>

<span data-ttu-id="479ed-104">Указывает, что копия сообщения на сервере остается на сервере для учетной записи POP.</span><span class="sxs-lookup"><span data-stu-id="479ed-104">Specifies leaving a copy of a message on the server for a POP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="479ed-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="479ed-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="479ed-106">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="479ed-106">Identifier:</span></span>  <br/> |<span data-ttu-id="479ed-107">0x1000</span><span class="sxs-lookup"><span data-stu-id="479ed-107">0x1000</span></span>  <br/> |
|<span data-ttu-id="479ed-108">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="479ed-108">Property type:</span></span>  <br/> |<span data-ttu-id="479ed-109">ПТ_ДВОРД</span><span class="sxs-lookup"><span data-stu-id="479ed-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="479ed-110">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="479ed-110">Property tag:</span></span>  <br/> |<span data-ttu-id="479ed-111">0x10000003</span><span class="sxs-lookup"><span data-stu-id="479ed-111">0x10000003</span></span>  <br/> |
|<span data-ttu-id="479ed-112">Обращения</span><span class="sxs-lookup"><span data-stu-id="479ed-112">Access:</span></span>  <br/> |<span data-ttu-id="479ed-113">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="479ed-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="479ed-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="479ed-114">Remarks</span></span>

<span data-ttu-id="479ed-115">В приведенной ниже таблице перечислены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="479ed-115">The following table lists the possible values.</span></span> <span data-ttu-id="479ed-116">Для [](constants-account-management-api.md) получения дополнительных сведений о константах см.</span><span class="sxs-lookup"><span data-stu-id="479ed-116">See [Constants (Account management API)](constants-account-management-api.md) for more information on the constants.</span></span> 
  
|<span data-ttu-id="479ed-117">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="479ed-117">**Possible values**</span></span>|<span data-ttu-id="479ed-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="479ed-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="479ed-119">**ЛЕАВЕ_ОН_СЕРВЕР**</span><span class="sxs-lookup"><span data-stu-id="479ed-119">**LEAVE_ON_SERVER**</span></span> <br/> |<span data-ttu-id="479ed-120">Оставляет копию сообщения на сервере POP после загрузки сообщения на устройство.</span><span class="sxs-lookup"><span data-stu-id="479ed-120">Leaves a copy of the message on the POP server after downloading the message to a device.</span></span>  <br/> |
|<span data-ttu-id="479ed-121">**РЕМОВЕ_АФТЕР**</span><span class="sxs-lookup"><span data-stu-id="479ed-121">**REMOVE_AFTER**</span></span> <br/> |<span data-ttu-id="479ed-122">Удаляет сообщение с сервера POP после его загрузки на устройство.</span><span class="sxs-lookup"><span data-stu-id="479ed-122">Removes the message from the POP server after downloading it to a device.</span></span>  <br/> |
|<span data-ttu-id="479ed-123">**РЕМОВЕ_ОН_НУКЕ**</span><span class="sxs-lookup"><span data-stu-id="479ed-123">**REMOVE_ON_NUKE**</span></span> <br/> |<span data-ttu-id="479ed-124">Удаляет сообщение с сервера POP только после того, как пользователь удалит сообщение из папки "Удаленные".</span><span class="sxs-lookup"><span data-stu-id="479ed-124">Removes the message from the POP server only after the user deletes the message from the Deleted Items folder.</span></span>  <br/> |
|<span data-ttu-id="479ed-125">**Жет_ремове_афтер_дайс** ( _UL_)</span><span class="sxs-lookup"><span data-stu-id="479ed-125">**GET_REMOVE_AFTER_DAYS**( _ul_)</span></span>  <br/> |<span data-ttu-id="479ed-126">Возвращает количество дней, по истечении которого сообщение будет удалено с сервера POP.</span><span class="sxs-lookup"><span data-stu-id="479ed-126">Gets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
|<span data-ttu-id="479ed-127">**Сет_ремове_афтер_дайс** ( _дней_)</span><span class="sxs-lookup"><span data-stu-id="479ed-127">**SET_REMOVE_AFTER_DAYS**( _days_)</span></span>  <br/> |<span data-ttu-id="479ed-128">Задает число дней, по истечении которого сообщение будет удалено с сервера POP.</span><span class="sxs-lookup"><span data-stu-id="479ed-128">Sets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="479ed-129">См. также</span><span class="sxs-lookup"><span data-stu-id="479ed-129">See also</span></span>

- [<span data-ttu-id="479ed-130">Управление скачиванием сообщений для учетных записей POP3</span><span class="sxs-lookup"><span data-stu-id="479ed-130">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="479ed-131">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="479ed-131">Constants (Account management API)</span></span>](constants-account-management-api.md)

