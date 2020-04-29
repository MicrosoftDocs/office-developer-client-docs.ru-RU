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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410947"
---
# <a name="prop_pop_leave_on_server"></a><span data-ttu-id="f06e5-103">PROP_POP_LEAVE_ON_SERVER</span><span class="sxs-lookup"><span data-stu-id="f06e5-103">PROP_POP_LEAVE_ON_SERVER</span></span>

<span data-ttu-id="f06e5-104">Указывает, что копия сообщения на сервере остается на сервере для учетной записи POP.</span><span class="sxs-lookup"><span data-stu-id="f06e5-104">Specifies leaving a copy of a message on the server for a POP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f06e5-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="f06e5-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f06e5-106">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f06e5-106">Identifier:</span></span>  <br/> |<span data-ttu-id="f06e5-107">0x1000</span><span class="sxs-lookup"><span data-stu-id="f06e5-107">0x1000</span></span>  <br/> |
|<span data-ttu-id="f06e5-108">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="f06e5-108">Property type:</span></span>  <br/> |<span data-ttu-id="f06e5-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="f06e5-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="f06e5-110">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="f06e5-110">Property tag:</span></span>  <br/> |<span data-ttu-id="f06e5-111">0x10000003</span><span class="sxs-lookup"><span data-stu-id="f06e5-111">0x10000003</span></span>  <br/> |
|<span data-ttu-id="f06e5-112">Обращения</span><span class="sxs-lookup"><span data-stu-id="f06e5-112">Access:</span></span>  <br/> |<span data-ttu-id="f06e5-113">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f06e5-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f06e5-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f06e5-114">Remarks</span></span>

<span data-ttu-id="f06e5-115">В приведенной ниже таблице перечислены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="f06e5-115">The following table lists the possible values.</span></span> <span data-ttu-id="f06e5-116">Для получения дополнительных сведений [о константах см.](constants-account-management-api.md)</span><span class="sxs-lookup"><span data-stu-id="f06e5-116">See [Constants (Account management API)](constants-account-management-api.md) for more information on the constants.</span></span> 
  
|<span data-ttu-id="f06e5-117">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="f06e5-117">**Possible values**</span></span>|<span data-ttu-id="f06e5-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f06e5-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f06e5-119">**LEAVE_ON_SERVER**</span><span class="sxs-lookup"><span data-stu-id="f06e5-119">**LEAVE_ON_SERVER**</span></span> <br/> |<span data-ttu-id="f06e5-120">Оставляет копию сообщения на сервере POP после загрузки сообщения на устройство.</span><span class="sxs-lookup"><span data-stu-id="f06e5-120">Leaves a copy of the message on the POP server after downloading the message to a device.</span></span>  <br/> |
|<span data-ttu-id="f06e5-121">**REMOVE_AFTER**</span><span class="sxs-lookup"><span data-stu-id="f06e5-121">**REMOVE_AFTER**</span></span> <br/> |<span data-ttu-id="f06e5-122">Удаляет сообщение с сервера POP после его загрузки на устройство.</span><span class="sxs-lookup"><span data-stu-id="f06e5-122">Removes the message from the POP server after downloading it to a device.</span></span>  <br/> |
|<span data-ttu-id="f06e5-123">**REMOVE_ON_NUKE**</span><span class="sxs-lookup"><span data-stu-id="f06e5-123">**REMOVE_ON_NUKE**</span></span> <br/> |<span data-ttu-id="f06e5-124">Удаляет сообщение с сервера POP только после того, как пользователь удалит сообщение из папки "Удаленные".</span><span class="sxs-lookup"><span data-stu-id="f06e5-124">Removes the message from the POP server only after the user deletes the message from the Deleted Items folder.</span></span>  <br/> |
|<span data-ttu-id="f06e5-125">**GET_REMOVE_AFTER_DAYS**( _UL_)</span><span class="sxs-lookup"><span data-stu-id="f06e5-125">**GET_REMOVE_AFTER_DAYS**( _ul_)</span></span>  <br/> |<span data-ttu-id="f06e5-126">Возвращает количество дней, по истечении которого сообщение будет удалено с сервера POP.</span><span class="sxs-lookup"><span data-stu-id="f06e5-126">Gets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
|<span data-ttu-id="f06e5-127">**SET_REMOVE_AFTER_DAYS**( _дней_)</span><span class="sxs-lookup"><span data-stu-id="f06e5-127">**SET_REMOVE_AFTER_DAYS**( _days_)</span></span>  <br/> |<span data-ttu-id="f06e5-128">Задает число дней, по истечении которого сообщение будет удалено с сервера POP.</span><span class="sxs-lookup"><span data-stu-id="f06e5-128">Sets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f06e5-129">См. также</span><span class="sxs-lookup"><span data-stu-id="f06e5-129">See also</span></span>

- [<span data-ttu-id="f06e5-130">Управление скачиванием сообщений для учетных записей POP3</span><span class="sxs-lookup"><span data-stu-id="f06e5-130">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="f06e5-131">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="f06e5-131">Constants (Account management API)</span></span>](constants-account-management-api.md)

