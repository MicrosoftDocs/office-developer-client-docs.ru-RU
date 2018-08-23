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
ms.openlocfilehash: 23663cea49c50f3f584d6b06e331545320e8283b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565384"
---
# <a name="imapistatus--imapiprop"></a><span data-ttu-id="89c46-103">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="89c46-103">IMAPIStatus : IMAPIProp</span></span>

  
  
<span data-ttu-id="89c46-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89c46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89c46-105">Предоставляет сведения о состоянии о подсистемы MAPI, встроенная адресной книги и диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="89c46-105">Provides status information about the MAPI subsystem, the integrated address book, and the MAPI spooler.</span></span> <span data-ttu-id="89c46-106">Поставщик службы реализует **IMAPIStatus** для предоставления сведений о своем состоянии.</span><span class="sxs-lookup"><span data-stu-id="89c46-106">A service provider implements **IMAPIStatus** to supply information about its own status.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="89c46-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="89c46-107">Header file:</span></span>  <br/> |<span data-ttu-id="89c46-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="89c46-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="89c46-109">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="89c46-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="89c46-110">Объекты состояния</span><span class="sxs-lookup"><span data-stu-id="89c46-110">Status objects</span></span>  <br/> |
|<span data-ttu-id="89c46-111">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="89c46-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="89c46-112">Поставщиков услуг и MAPI</span><span class="sxs-lookup"><span data-stu-id="89c46-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="89c46-113">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="89c46-113">Called by:</span></span>  <br/> |<span data-ttu-id="89c46-114">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="89c46-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="89c46-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="89c46-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="89c46-116">IID_IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="89c46-116">IID_IMAPIStatus</span></span>  <br/> |
|<span data-ttu-id="89c46-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="89c46-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="89c46-118">LPMAPISTATUS</span><span class="sxs-lookup"><span data-stu-id="89c46-118">LPMAPISTATUS</span></span>  <br/> |
|<span data-ttu-id="89c46-119">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="89c46-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="89c46-120">Не входящих в транзакции</span><span class="sxs-lookup"><span data-stu-id="89c46-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="89c46-121">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="89c46-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="89c46-122">ValidateState</span><span class="sxs-lookup"><span data-stu-id="89c46-122">ValidateState</span></span>](imapistatus-validatestate.md) <br/> |<span data-ttu-id="89c46-123">Проверяет состояние внешних информация, доступная для ресурсов MAPI или поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="89c46-123">Confirms the external status information available for the MAPI resource or the service provider.</span></span>  <br/> |
|[<span data-ttu-id="89c46-124">SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="89c46-124">SettingsDialog</span></span>](imapistatus-settingsdialog.md) <br/> |<span data-ttu-id="89c46-125">Отображает страницу свойств, который позволяет пользователю изменять конфигурации поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="89c46-125">Displays a property sheet that enables the user to change a service provider's configuration.</span></span>  <br/> |
|[<span data-ttu-id="89c46-126">Изменение пароля</span><span class="sxs-lookup"><span data-stu-id="89c46-126">ChangePassword</span></span>](imapistatus-changepassword.md) <br/> |<span data-ttu-id="89c46-127">Изменение пароля поставщика услуг без отображения пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="89c46-127">Modifies a service provider's password without displaying a user interface.</span></span>  <br/> |
|[<span data-ttu-id="89c46-128">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="89c46-128">FlushQueues</span></span>](imapistatus-flushqueues.md) <br/> |<span data-ttu-id="89c46-129">Выполняет принудительное все сообщения, ожидающие отправку и получение для сразу же отправки или загрузки.</span><span class="sxs-lookup"><span data-stu-id="89c46-129">Forces all messages waiting to be sent or received to be immediately uploaded or downloaded.</span></span>  <br/> |
   
|<span data-ttu-id="89c46-130">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="89c46-130">**Required properties**</span></span>|<span data-ttu-id="89c46-131">**Access**</span><span class="sxs-lookup"><span data-stu-id="89c46-131">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="89c46-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="89c46-132">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="89c46-133">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="89c46-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="89c46-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="89c46-134">**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="89c46-135">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="89c46-135">Read/write</span></span>  <br/> |
|<span data-ttu-id="89c46-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="89c46-136">**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="89c46-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c46-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="89c46-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="89c46-138">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="89c46-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c46-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="89c46-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="89c46-140">**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="89c46-141">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c46-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="89c46-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="89c46-142">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="89c46-143">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c46-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="89c46-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="89c46-144">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="89c46-145">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="89c46-145">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89c46-146">Замечания</span><span class="sxs-lookup"><span data-stu-id="89c46-146">Remarks</span></span>

<span data-ttu-id="89c46-147">Состояние объекты, внедряемые MAPI поддерживают следующие методы:</span><span class="sxs-lookup"><span data-stu-id="89c46-147">The status objects that MAPI implements support the following methods:</span></span>
  
|<span data-ttu-id="89c46-148">**Состояние объекта**</span><span class="sxs-lookup"><span data-stu-id="89c46-148">**Status object**</span></span>|<span data-ttu-id="89c46-149">**Поддерживаемые методы**</span><span class="sxs-lookup"><span data-stu-id="89c46-149">**Supported methods**</span></span>|
|:-----|:-----|
|<span data-ttu-id="89c46-150">Подсистема MAPI</span><span class="sxs-lookup"><span data-stu-id="89c46-150">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="89c46-151">Только **ValidateState**</span><span class="sxs-lookup"><span data-stu-id="89c46-151">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="89c46-152">Адресная книга MAPI</span><span class="sxs-lookup"><span data-stu-id="89c46-152">MAPI address book</span></span>  <br/> |<span data-ttu-id="89c46-153">Только **ValidateState**</span><span class="sxs-lookup"><span data-stu-id="89c46-153">**ValidateState** only</span></span>  <br/> |
|<span data-ttu-id="89c46-154">Диспетчер очереди MAPI</span><span class="sxs-lookup"><span data-stu-id="89c46-154">MAPI spooler</span></span>  <br/> |<span data-ttu-id="89c46-155">**ValidateState** и **FlushQueues**</span><span class="sxs-lookup"><span data-stu-id="89c46-155">**ValidateState** and **FlushQueues**</span></span> <br/> |
   
<span data-ttu-id="89c46-156">Состояние объекты, внедряемые MAPI должны иметь только для чтения версии методов интерфейса [IMAPIProp](imapipropiunknown.md) и поддерживает метод **ValidateState** .</span><span class="sxs-lookup"><span data-stu-id="89c46-156">The status objects that MAPI implements are required to have a read-only version of the methods of the [IMAPIProp](imapipropiunknown.md) interface and to support the **ValidateState** method.</span></span> <span data-ttu-id="89c46-157">Поставщики транспорта, также должны поддерживать **FlushQueues**.</span><span class="sxs-lookup"><span data-stu-id="89c46-157">Transport providers should also support **FlushQueues**.</span></span> <span data-ttu-id="89c46-158">Все поставщики должны поддерживать **SettingsDialog**; Поддержка **Изменение пароля** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="89c46-158">All providers should support **SettingsDialog**; support for **ChangePassword** is optional.</span></span> 
  
<span data-ttu-id="89c46-159">Клиенты используют объекты состояние для выполнения настройки, а также информацию о состоянии сеанса.</span><span class="sxs-lookup"><span data-stu-id="89c46-159">Clients use status objects to perform configuration and to learn about the state of the session.</span></span> <span data-ttu-id="89c46-160">Они доступ к объекту состояния путем вызова метода **OpenStatusEntry** объекта службы поставщика входа в систему или метод [IMAPISession::GetStatusTable](imapisession-getstatustable.md) для извлечения объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="89c46-160">They access a status object by calling the **OpenStatusEntry** method of a service provider logon object or the [IMAPISession::GetStatusTable](imapisession-getstatustable.md) method to retrieve the status object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="89c46-161">См. также</span><span class="sxs-lookup"><span data-stu-id="89c46-161">See also</span></span>



[<span data-ttu-id="89c46-162">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="89c46-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

