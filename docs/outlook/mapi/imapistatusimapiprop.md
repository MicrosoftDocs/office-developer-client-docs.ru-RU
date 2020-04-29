---
title: Имапистатус IMAPIProp
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
# <a name="imapistatus--imapiprop"></a><span data-ttu-id="9a19d-103">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9a19d-103">IMAPIStatus : IMAPIProp</span></span>

  
  
<span data-ttu-id="9a19d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a19d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a19d-105">Предоставляет сведения о состоянии подсистемы MAPI, интегрированной адресной книги и диспетчере очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="9a19d-105">Provides status information about the MAPI subsystem, the integrated address book, and the MAPI spooler.</span></span> <span data-ttu-id="9a19d-106">Поставщик услуг реализует **имапистатус** для предоставления сведений о своем состоянии.</span><span class="sxs-lookup"><span data-stu-id="9a19d-106">A service provider implements **IMAPIStatus** to supply information about its own status.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9a19d-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9a19d-107">Header file:</span></span>  <br/> |<span data-ttu-id="9a19d-108">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="9a19d-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9a19d-109">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="9a19d-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="9a19d-110">Объекты состояний</span><span class="sxs-lookup"><span data-stu-id="9a19d-110">Status objects</span></span>  <br/> |
|<span data-ttu-id="9a19d-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="9a19d-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="9a19d-112">Поставщики услуг и MAPI</span><span class="sxs-lookup"><span data-stu-id="9a19d-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="9a19d-113">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="9a19d-113">Called by:</span></span>  <br/> |<span data-ttu-id="9a19d-114">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="9a19d-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="9a19d-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="9a19d-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9a19d-116">IID_IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="9a19d-116">IID_IMAPIStatus</span></span>  <br/> |
|<span data-ttu-id="9a19d-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="9a19d-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="9a19d-118">лпмапистатус</span><span class="sxs-lookup"><span data-stu-id="9a19d-118">LPMAPISTATUS</span></span>  <br/> |
|<span data-ttu-id="9a19d-119">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="9a19d-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="9a19d-120">Не transactd</span><span class="sxs-lookup"><span data-stu-id="9a19d-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9a19d-121">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="9a19d-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9a19d-122">валидатестате</span><span class="sxs-lookup"><span data-stu-id="9a19d-122">ValidateState</span></span>](imapistatus-validatestate.md) <br/> |<span data-ttu-id="9a19d-123">Проверяет внешние сведения о состоянии, доступные для ресурса MAPI или поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="9a19d-123">Confirms the external status information available for the MAPI resource or the service provider.</span></span>  <br/> |
|[<span data-ttu-id="9a19d-124">сеттингсдиалог</span><span class="sxs-lookup"><span data-stu-id="9a19d-124">SettingsDialog</span></span>](imapistatus-settingsdialog.md) <br/> |<span data-ttu-id="9a19d-125">Отображает страницу свойств, позволяющую пользователю изменить конфигурацию поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="9a19d-125">Displays a property sheet that enables the user to change a service provider's configuration.</span></span>  <br/> |
|[<span data-ttu-id="9a19d-126">ChangePassword</span><span class="sxs-lookup"><span data-stu-id="9a19d-126">ChangePassword</span></span>](imapistatus-changepassword.md) <br/> |<span data-ttu-id="9a19d-127">Изменяет пароль поставщика услуг без отображения пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9a19d-127">Modifies a service provider's password without displaying a user interface.</span></span>  <br/> |
|[<span data-ttu-id="9a19d-128">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="9a19d-128">FlushQueues</span></span>](imapistatus-flushqueues.md) <br/> |<span data-ttu-id="9a19d-129">Принудительно отправляет или загружает все сообщения, ожидающие отправки или получения.</span><span class="sxs-lookup"><span data-stu-id="9a19d-129">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span>  <br/> |
   
|<span data-ttu-id="9a19d-130">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="9a19d-130">**Required properties**</span></span>|<span data-ttu-id="9a19d-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="9a19d-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9a19d-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a19d-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9a19d-133">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9a19d-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="9a19d-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a19d-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9a19d-135">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9a19d-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="9a19d-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a19d-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9a19d-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a19d-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="9a19d-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a19d-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9a19d-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a19d-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="9a19d-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a19d-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9a19d-141">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a19d-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="9a19d-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a19d-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9a19d-143">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a19d-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="9a19d-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="9a19d-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="9a19d-145">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9a19d-145">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9a19d-146">Примечания</span><span class="sxs-lookup"><span data-stu-id="9a19d-146">Remarks</span></span>

<span data-ttu-id="9a19d-147">Объекты состояния, реализованные в MAPI, поддерживают следующие методы:</span><span class="sxs-lookup"><span data-stu-id="9a19d-147">The status objects that MAPI implements support the following methods:</span></span>
  
|<span data-ttu-id="9a19d-148">**Объект Status**</span><span class="sxs-lookup"><span data-stu-id="9a19d-148">**Status object**</span></span>|<span data-ttu-id="9a19d-149">**Поддерживаемые методы**</span><span class="sxs-lookup"><span data-stu-id="9a19d-149">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9a19d-150">Подсистема MAPI</span><span class="sxs-lookup"><span data-stu-id="9a19d-150">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="9a19d-151">Только **валидатестате**</span><span class="sxs-lookup"><span data-stu-id="9a19d-151">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="9a19d-152">Адресная книга MAPI</span><span class="sxs-lookup"><span data-stu-id="9a19d-152">MAPI address book</span></span>  <br/> |<span data-ttu-id="9a19d-153">Только **валидатестате**</span><span class="sxs-lookup"><span data-stu-id="9a19d-153">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="9a19d-154">Диспетчер очереди MAPI</span><span class="sxs-lookup"><span data-stu-id="9a19d-154">MAPI spooler</span></span>  <br/> |<span data-ttu-id="9a19d-155">**Валидатестате** и **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="9a19d-155">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="9a19d-156">Для объектов status, реализованных в MAPI, необходима доступная только для чтения версия методов интерфейса [IMAPIProp](imapipropiunknown.md) и поддержка метода **валидатестате** .</span><span class="sxs-lookup"><span data-stu-id="9a19d-156">The status objects that MAPI implements are required to have a read-only version of the methods of the [IMAPIProp](imapipropiunknown.md) interface and to support the **ValidateState** method.</span></span> <span data-ttu-id="9a19d-157">Поставщики транспорта также должны поддерживать **FlushQueues**.</span><span class="sxs-lookup"><span data-stu-id="9a19d-157">Transport providers should also support **FlushQueues**.</span></span> <span data-ttu-id="9a19d-158">Все поставщики должны поддерживать **сеттингсдиалог**; поддержка **ChangePassword** является необязательной.</span><span class="sxs-lookup"><span data-stu-id="9a19d-158">All providers should support **SettingsDialog**; support for **ChangePassword** is optional.</span></span> 
  
<span data-ttu-id="9a19d-159">Клиенты используют объекты состояния для выполнения настройки и получения сведений о состоянии сеанса.</span><span class="sxs-lookup"><span data-stu-id="9a19d-159">Clients use status objects to perform configuration and to learn about the state of the session.</span></span> <span data-ttu-id="9a19d-160">Они обращаются к объекту status, вызывая метод **опенстатусентри** объекта входа поставщика услуг или метод [IMAPISession:: жетстатустабле](imapisession-getstatustable.md) для получения объекта Status.</span><span class="sxs-lookup"><span data-stu-id="9a19d-160">They access a status object by calling the **OpenStatusEntry** method of a service provider logon object or the [IMAPISession::GetStatusTable](imapisession-getstatustable.md) method to retrieve the status object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9a19d-161">См. также</span><span class="sxs-lookup"><span data-stu-id="9a19d-161">See also</span></span>



[<span data-ttu-id="9a19d-162">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="9a19d-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

