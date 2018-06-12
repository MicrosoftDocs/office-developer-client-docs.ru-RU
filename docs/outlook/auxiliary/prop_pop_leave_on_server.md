---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Указывает, сохранение копий сообщений на сервере для учетной записи POP.
ms.openlocfilehash: 9f986ff60a5824ece0a8bb91619323b58ec8b87a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807947"
---
# <a name="proppopleaveonserver"></a><span data-ttu-id="78ac7-103">PROP_POP_LEAVE_ON_SERVER</span><span class="sxs-lookup"><span data-stu-id="78ac7-103">PROP_POP_LEAVE_ON_SERVER</span></span>

<span data-ttu-id="78ac7-104">Указывает, сохранение копий сообщений на сервере для учетной записи POP.</span><span class="sxs-lookup"><span data-stu-id="78ac7-104">Specifies leaving a copy of a message on the server for a POP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="78ac7-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="78ac7-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="78ac7-106">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="78ac7-106">Identifier:</span></span>  <br/> |<span data-ttu-id="78ac7-107">0x1000</span><span class="sxs-lookup"><span data-stu-id="78ac7-107">0x1000</span></span>  <br/> |
|<span data-ttu-id="78ac7-108">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="78ac7-108">Property type:</span></span>  <br/> |<span data-ttu-id="78ac7-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="78ac7-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="78ac7-110">Свойство tag:</span><span class="sxs-lookup"><span data-stu-id="78ac7-110">Property tag:</span></span>  <br/> |<span data-ttu-id="78ac7-111">0x10000003</span><span class="sxs-lookup"><span data-stu-id="78ac7-111">0x10000003</span></span>  <br/> |
|<span data-ttu-id="78ac7-112">Access:</span><span class="sxs-lookup"><span data-stu-id="78ac7-112">Access:</span></span>  <br/> |<span data-ttu-id="78ac7-113">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="78ac7-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78ac7-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="78ac7-114">Remarks</span></span>

<span data-ttu-id="78ac7-115">В следующей таблице приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="78ac7-115">The following table lists the possible values.</span></span> <span data-ttu-id="78ac7-116">Для получения дополнительных сведений о константы видеть [константы (Управление учетными записями API)](constants-account-management-api.md) .</span><span class="sxs-lookup"><span data-stu-id="78ac7-116">See [Constants (Account management API)](constants-account-management-api.md) for more information on the constants.</span></span> 
  
|<span data-ttu-id="78ac7-117">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="78ac7-117">**Possible values**</span></span>|<span data-ttu-id="78ac7-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="78ac7-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="78ac7-119">**LEAVE_ON_SERVER**</span><span class="sxs-lookup"><span data-stu-id="78ac7-119">**LEAVE_ON_SERVER**</span></span> <br/> |<span data-ttu-id="78ac7-120">Покидает копии сообщения на POP-сервер после загрузки сообщения с устройством.</span><span class="sxs-lookup"><span data-stu-id="78ac7-120">Leaves a copy of the message on the POP server after downloading the message to a device.</span></span>  <br/> |
|<span data-ttu-id="78ac7-121">**REMOVE_AFTER**</span><span class="sxs-lookup"><span data-stu-id="78ac7-121">**REMOVE_AFTER**</span></span> <br/> |<span data-ttu-id="78ac7-122">Удаляет сообщение с POP-сервера после загрузки на устройство.</span><span class="sxs-lookup"><span data-stu-id="78ac7-122">Removes the message from the POP server after downloading it to a device.</span></span>  <br/> |
|<span data-ttu-id="78ac7-123">**REMOVE_ON_NUKE**</span><span class="sxs-lookup"><span data-stu-id="78ac7-123">**REMOVE_ON_NUKE**</span></span> <br/> |<span data-ttu-id="78ac7-124">Удаляет сообщение из POP-сервер только после пользователь удаляет сообщение из папки «Удаленные».</span><span class="sxs-lookup"><span data-stu-id="78ac7-124">Removes the message from the POP server only after the user deletes the message from the Deleted Items folder.</span></span>  <br/> |
|<span data-ttu-id="78ac7-125">**GET_REMOVE_AFTER_DAYS** ( _ul_)</span><span class="sxs-lookup"><span data-stu-id="78ac7-125">**GET_REMOVE_AFTER_DAYS**( _ul_)</span></span>  <br/> |<span data-ttu-id="78ac7-126">Получает количество дней, после которого сообщение будет удален из POP-сервера.</span><span class="sxs-lookup"><span data-stu-id="78ac7-126">Gets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
|<span data-ttu-id="78ac7-127">**SET_REMOVE_AFTER_DAYS** ( _дней_)</span><span class="sxs-lookup"><span data-stu-id="78ac7-127">**SET_REMOVE_AFTER_DAYS**( _days_)</span></span>  <br/> |<span data-ttu-id="78ac7-128">Задает число дней, после которого сообщение будет удален из POP-сервера.</span><span class="sxs-lookup"><span data-stu-id="78ac7-128">Sets the number of days after which the message will be removed from the POP server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78ac7-129">См. также</span><span class="sxs-lookup"><span data-stu-id="78ac7-129">See also</span></span>

- [<span data-ttu-id="78ac7-130">Загружаемые файлы для управления сообщения для учетных записей POP3</span><span class="sxs-lookup"><span data-stu-id="78ac7-130">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="78ac7-131">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="78ac7-131">Constants (Account management API)</span></span>](constants-account-management-api.md)

