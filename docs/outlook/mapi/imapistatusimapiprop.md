---
title: IMAPIStatus IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus
api_type:
- COM
ms.assetid: 17b2aa43-0267-45b6-8c57-11b7a5c67333
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f90cf661c069ecd476bd02c5719147633a8392e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408301"
---
# <a name="imapistatus--imapiprop"></a><span data-ttu-id="95edd-103">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="95edd-103">IMAPIStatus : IMAPIProp</span></span>

  
  
<span data-ttu-id="95edd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95edd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95edd-105">Предоставляет сведения о состоянии подсистемы MAPI, интегрированной адресной книги и шпалере MAPI.</span><span class="sxs-lookup"><span data-stu-id="95edd-105">Provides status information about the MAPI subsystem, the integrated address book, and the MAPI spooler.</span></span> <span data-ttu-id="95edd-106">Поставщик услуг реализует **IMAPIStatus,** чтобы предоставить сведения о своем собственном состоянии.</span><span class="sxs-lookup"><span data-stu-id="95edd-106">A service provider implements **IMAPIStatus** to supply information about its own status.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95edd-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="95edd-107">Header file:</span></span>  <br/> |<span data-ttu-id="95edd-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="95edd-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="95edd-109">Подвергается:</span><span class="sxs-lookup"><span data-stu-id="95edd-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="95edd-110">Объекты состояний</span><span class="sxs-lookup"><span data-stu-id="95edd-110">Status objects</span></span>  <br/> |
|<span data-ttu-id="95edd-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="95edd-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="95edd-112">Поставщики услуг и MAPI</span><span class="sxs-lookup"><span data-stu-id="95edd-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="95edd-113">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="95edd-113">Called by:</span></span>  <br/> |<span data-ttu-id="95edd-114">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="95edd-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="95edd-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="95edd-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="95edd-116">IID_IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="95edd-116">IID_IMAPIStatus</span></span>  <br/> |
|<span data-ttu-id="95edd-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="95edd-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="95edd-118">LPMAPISTATUS</span><span class="sxs-lookup"><span data-stu-id="95edd-118">LPMAPISTATUS</span></span>  <br/> |
|<span data-ttu-id="95edd-119">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="95edd-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="95edd-120">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="95edd-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="95edd-121">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="95edd-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="95edd-122">ValidateState</span><span class="sxs-lookup"><span data-stu-id="95edd-122">ValidateState</span></span>](imapistatus-validatestate.md) <br/> |<span data-ttu-id="95edd-123">Подтверждает сведения о внешнем состоянии, доступные для ресурса MAPI или поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="95edd-123">Confirms the external status information available for the MAPI resource or the service provider.</span></span>  <br/> |
|[<span data-ttu-id="95edd-124">SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="95edd-124">SettingsDialog</span></span>](imapistatus-settingsdialog.md) <br/> |<span data-ttu-id="95edd-125">Отображает лист свойств, который позволяет пользователю изменять конфигурацию поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="95edd-125">Displays a property sheet that enables the user to change a service provider's configuration.</span></span>  <br/> |
|[<span data-ttu-id="95edd-126">ChangePassword</span><span class="sxs-lookup"><span data-stu-id="95edd-126">ChangePassword</span></span>](imapistatus-changepassword.md) <br/> |<span data-ttu-id="95edd-127">Изменяет пароль поставщика услуг без отображения пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="95edd-127">Modifies a service provider's password without displaying a user interface.</span></span>  <br/> |
|[<span data-ttu-id="95edd-128">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="95edd-128">FlushQueues</span></span>](imapistatus-flushqueues.md) <br/> |<span data-ttu-id="95edd-129">Заставляет все сообщения, ожидаемые для отправки или отправки, немедленно загружаться или загружаться.</span><span class="sxs-lookup"><span data-stu-id="95edd-129">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span>  <br/> |
   
|<span data-ttu-id="95edd-130">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="95edd-130">**Required properties**</span></span>|<span data-ttu-id="95edd-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="95edd-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="95edd-132">**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="95edd-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="95edd-133">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="95edd-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="95edd-134">**PR_PROVIDER_DISPLAY** [(PidTagProviderDisplay)](pidtagproviderdisplay-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="95edd-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="95edd-135">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="95edd-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="95edd-136">**PR_PROVIDER_DLL_NAME** [(PidTagProviderDllName)](pidtagproviderdllname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="95edd-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="95edd-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="95edd-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="95edd-138">**PR_RESOURCE_FLAGS** [(PidTagResourceFlags)](pidtagresourceflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="95edd-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="95edd-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="95edd-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="95edd-140">**PR_RESOURCE_METHODS** [(PidTagResourceMethods)](pidtagresourcemethods-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="95edd-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="95edd-141">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="95edd-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="95edd-142">**PR_RESOURCE_TYPE** [(PidTagResourceType)](pidtagresourcetype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="95edd-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="95edd-143">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="95edd-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="95edd-144">**PR_STATUS_CODE** [(PidTagStatusCode)](pidtagstatuscode-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="95edd-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="95edd-145">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="95edd-145">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95edd-146">Примечания</span><span class="sxs-lookup"><span data-stu-id="95edd-146">Remarks</span></span>

<span data-ttu-id="95edd-147">Объекты состояния, реализуемые MAPI, поддерживают следующие методы:</span><span class="sxs-lookup"><span data-stu-id="95edd-147">The status objects that MAPI implements support the following methods:</span></span>
  
|<span data-ttu-id="95edd-148">**Объект Status**</span><span class="sxs-lookup"><span data-stu-id="95edd-148">**Status object**</span></span>|<span data-ttu-id="95edd-149">**Поддерживаемые методы**</span><span class="sxs-lookup"><span data-stu-id="95edd-149">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="95edd-150">Подсистема MAPI</span><span class="sxs-lookup"><span data-stu-id="95edd-150">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="95edd-151">**Только ValidateState**</span><span class="sxs-lookup"><span data-stu-id="95edd-151">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="95edd-152">Адресная книга MAPI</span><span class="sxs-lookup"><span data-stu-id="95edd-152">MAPI address book</span></span>  <br/> |<span data-ttu-id="95edd-153">**Только ValidateState**</span><span class="sxs-lookup"><span data-stu-id="95edd-153">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="95edd-154">Шпалер MAPI</span><span class="sxs-lookup"><span data-stu-id="95edd-154">MAPI spooler</span></span>  <br/> |<span data-ttu-id="95edd-155">**ValidateState** и **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="95edd-155">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="95edd-156">Объекты состояния, реализуемые MAPI, должны иметь только для чтения версию методов интерфейса [IMAPIProp](imapipropiunknown.md) и поддерживать метод **ValidateState.**</span><span class="sxs-lookup"><span data-stu-id="95edd-156">The status objects that MAPI implements are required to have a read-only version of the methods of the [IMAPIProp](imapipropiunknown.md) interface and to support the **ValidateState** method.</span></span> <span data-ttu-id="95edd-157">Поставщики транспорта также должны поддерживать **flushQueues.**</span><span class="sxs-lookup"><span data-stu-id="95edd-157">Transport providers should also support **FlushQueues**.</span></span> <span data-ttu-id="95edd-158">Все поставщики должны поддерживать **SettingsDialog;** поддержка **ChangePassword** необязательна.</span><span class="sxs-lookup"><span data-stu-id="95edd-158">All providers should support **SettingsDialog**; support for **ChangePassword** is optional.</span></span> 
  
<span data-ttu-id="95edd-159">Клиенты используют объекты состояния для выполнения конфигурации и для того, чтобы узнать о состоянии сеанса.</span><span class="sxs-lookup"><span data-stu-id="95edd-159">Clients use status objects to perform configuration and to learn about the state of the session.</span></span> <span data-ttu-id="95edd-160">Они получают доступ к объекту состояния, позвонив **методу OpenStatusEntry** объекта logon поставщика услуг или [методу IMAPISession::GetStatusTable](imapisession-getstatustable.md) для получения объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="95edd-160">They access a status object by calling the **OpenStatusEntry** method of a service provider logon object or the [IMAPISession::GetStatusTable](imapisession-getstatustable.md) method to retrieve the status object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="95edd-161">См. также</span><span class="sxs-lookup"><span data-stu-id="95edd-161">See also</span></span>



[<span data-ttu-id="95edd-162">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="95edd-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

