---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Указывает оставить копию сообщения на сервере для учетной записи POP.
ms.openlocfilehash: e1bbddea0f10c07d630676960d1b330f6055e137
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410947"
---
# <a name="prop_pop_leave_on_server"></a><span data-ttu-id="ab5ab-103">PROP_POP_LEAVE_ON_SERVER</span><span class="sxs-lookup"><span data-stu-id="ab5ab-103">PROP_POP_LEAVE_ON_SERVER</span></span>

<span data-ttu-id="ab5ab-104">Указывает оставить копию сообщения на сервере для учетной записи POP.</span><span class="sxs-lookup"><span data-stu-id="ab5ab-104">Specifies leaving a copy of a message on the server for a POP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ab5ab-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="ab5ab-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab5ab-106">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ab5ab-106">Identifier:</span></span>  <br/> |<span data-ttu-id="ab5ab-107">0x1000</span><span class="sxs-lookup"><span data-stu-id="ab5ab-107">0x1000</span></span>  <br/> |
|<span data-ttu-id="ab5ab-108">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="ab5ab-108">Property type:</span></span>  <br/> |<span data-ttu-id="ab5ab-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="ab5ab-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="ab5ab-110">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="ab5ab-110">Property tag:</span></span>  <br/> |<span data-ttu-id="ab5ab-111">0x10000003</span><span class="sxs-lookup"><span data-stu-id="ab5ab-111">0x10000003</span></span>  <br/> |
|<span data-ttu-id="ab5ab-112">Доступ:</span><span class="sxs-lookup"><span data-stu-id="ab5ab-112">Access:</span></span>  <br/> |<span data-ttu-id="ab5ab-113">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab5ab-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab5ab-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="ab5ab-114">Remarks</span></span>

<span data-ttu-id="ab5ab-115">В следующей таблице перечислены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="ab5ab-115">The following table lists the possible values.</span></span> <span data-ttu-id="ab5ab-116">Дополнительные сведения о константах см. в руководстве Constants [(API](constants-account-management-api.md) управления учетной записью).</span><span class="sxs-lookup"><span data-stu-id="ab5ab-116">See [Constants (Account management API)](constants-account-management-api.md) for more information on the constants.</span></span> 
  
|<span data-ttu-id="ab5ab-117">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="ab5ab-117">**Possible values**</span></span>|<span data-ttu-id="ab5ab-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ab5ab-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ab5ab-119">**LEAVE_ON_SERVER**</span><span class="sxs-lookup"><span data-stu-id="ab5ab-119">**LEAVE_ON_SERVER**</span></span> <br/> |<span data-ttu-id="ab5ab-120">Оставляет копию сообщения на сервере POP после загрузки сообщения на устройство.</span><span class="sxs-lookup"><span data-stu-id="ab5ab-120">Leaves a copy of the message on the POP server after downloading the message to a device.</span></span>  <br/> |
|<span data-ttu-id="ab5ab-121">**REMOVE_AFTER**</span><span class="sxs-lookup"><span data-stu-id="ab5ab-121">**REMOVE_AFTER**</span></span> <br/> |<span data-ttu-id="ab5ab-122">Удаляет сообщение с pop-сервера после его загрузки на устройство.</span><span class="sxs-lookup"><span data-stu-id="ab5ab-122">Removes the message from the POP server after downloading it to a device.</span></span>  <br/> |
|<span data-ttu-id="ab5ab-123">**REMOVE_ON_NUKE**</span><span class="sxs-lookup"><span data-stu-id="ab5ab-123">**REMOVE_ON_NUKE**</span></span> <br/> |<span data-ttu-id="ab5ab-124">Удаляет сообщение с pop-сервера только после удаления сообщения из папки "Удаленные элементы".</span><span class="sxs-lookup"><span data-stu-id="ab5ab-124">Removes the message from the POP server only after the user deletes the message from the Deleted Items folder.</span></span>  <br/> |
|<span data-ttu-id="ab5ab-125">**GET_REMOVE_AFTER_DAYS** _(ul)_</span><span class="sxs-lookup"><span data-stu-id="ab5ab-125">**GET_REMOVE_AFTER_DAYS**( _ul_)</span></span>  <br/> |<span data-ttu-id="ab5ab-126">Получает количество дней, после которых сообщение будет удалено с pop-сервера.</span><span class="sxs-lookup"><span data-stu-id="ab5ab-126">Gets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
|<span data-ttu-id="ab5ab-127">**SET_REMOVE_AFTER_DAYS** _(дней)_</span><span class="sxs-lookup"><span data-stu-id="ab5ab-127">**SET_REMOVE_AFTER_DAYS**( _days_)</span></span>  <br/> |<span data-ttu-id="ab5ab-128">Задает количество дней, после которых сообщение будет удалено с pop-сервера.</span><span class="sxs-lookup"><span data-stu-id="ab5ab-128">Sets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ab5ab-129">См. также</span><span class="sxs-lookup"><span data-stu-id="ab5ab-129">See also</span></span>

- [<span data-ttu-id="ab5ab-130">Управление скачиванием сообщений для учетных записей POP3</span><span class="sxs-lookup"><span data-stu-id="ab5ab-130">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="ab5ab-131">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="ab5ab-131">Constants (Account management API)</span></span>](constants-account-management-api.md)

