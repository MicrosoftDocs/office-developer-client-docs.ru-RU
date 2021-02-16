---
title: Использование CSISyncClient для управления кэшом документов Office (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Узнайте, как использовать CSISyncClient для управления кэшом документов Office (ODC).
ms.openlocfilehash: ce33063f88492bcd6f9682a4a6431fb36f138d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346258"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a><span data-ttu-id="effc8-103">Использование CSISyncClient для управления кэшом документов Office (ODC)</span><span class="sxs-lookup"><span data-stu-id="effc8-103">Using CSISyncClient to control the Office Document Cache (ODC)</span></span>

<span data-ttu-id="effc8-104">Узнайте, как использовать CSISyncClient для управления кэшом документов Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="effc8-104">Learn how to use CSISyncClient to control the Office Document Cache (ODC).</span></span>
  
<span data-ttu-id="effc8-105">CSISyncClient — это сервер COM, который не является прокси-сервером (CsiSyncClient.exe), который позволяет Microsoft OneDrive управлять поведением кэша документов Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="effc8-105">CSISyncClient is an out-of-proc COM server (CsiSyncClient.exe) that allows Microsoft OneDrive to control the behavior of the Office Document Cache (ODC).</span></span> <span data-ttu-id="effc8-106">Например, OneDrive может вызвать ODC через CSISyncClient для отправки и загрузки файлов в конечные точки с поддержкой MS-FSSHTTP и из них.</span><span class="sxs-lookup"><span data-stu-id="effc8-106">For example, OneDrive may call upon the ODC via CSISyncClient to upload and download files to and from MS-FSSHTTP enabled endpoints.</span></span> <span data-ttu-id="effc8-107">Это позволяет использовать расширенные функции Office с помощью службы, такие как совместное авторство и плавный переход от автономного к сетевому.</span><span class="sxs-lookup"><span data-stu-id="effc8-107">This enables advanced service-backed features in Office, such as co-authoring and seamless transitions from offline to online.</span></span>
  
<span data-ttu-id="effc8-108">CsiSyncClient доступен в Office Desktop (x86 и x64).</span><span class="sxs-lookup"><span data-stu-id="effc8-108">CsiSyncClient is available in Office Desktop (both x86 and x64).</span></span> <span data-ttu-id="effc8-109">Примечание. Хотя более новые версии Office могут быть погрузки с помощью CsiSyncClient, этот процесс будет использоваться только для обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="effc8-109">Note: While newer versions of Office may ship with CsiSyncClient, the process will be used for backward compatibility only.</span></span> <span data-ttu-id="effc8-110">Интерфейс CsiSyncClient и методология управления ODC изменятся в будущих версиях Office.</span><span class="sxs-lookup"><span data-stu-id="effc8-110">The CsiSyncClient interface and the methodology of controlling the ODC will change in future versions of Office.</span></span>
  
<span data-ttu-id="effc8-111">В настоящее время этот ИД класса настроен для ответа только на OneDrive.</span><span class="sxs-lookup"><span data-stu-id="effc8-111">The class ID is currently set to respond only to OneDrive.</span></span>
  
<span data-ttu-id="effc8-112">Com-объект может быть заархивируемым com-сервером и работает в CsiSyncClient.exe.</span><span class="sxs-lookup"><span data-stu-id="effc8-112">The COM object is usable as an out-of-proc COM server and runs in CsiSyncClient.exe.</span></span> <span data-ttu-id="effc8-113">Из-за ограничений Access (который использует ODC), он поставляется с типом бита, в который входит Office, поэтому x64 Office означает объект x64 COM, а x86 Office — объект COM x86.</span><span class="sxs-lookup"><span data-stu-id="effc8-113">Due to limitations with Access (which the ODC uses), it ships with the bit type that Office comes in, so x64 Office means an x64 COM object, or x86 Office means an x86 COM object.</span></span> <span data-ttu-id="effc8-114">Чтобы обойти это ограничение, при указании CLSCTX_LOCAL_SERVER как части CoCreateInstance com-объект будет иметь место как сервер COM, который не является сервером COM, что обеспечивает совместимость между битами.</span><span class="sxs-lookup"><span data-stu-id="effc8-114">To get around this limitation, specifying CLSCTX_LOCAL_SERVER as part of the CoCreateInstance will have the COM object be hosted as an out-of-proc COM server, allowing cross-bitness compatibility.</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="effc8-115">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="effc8-115">Interfaces</span></span>

<span data-ttu-id="effc8-116">CSISyncClient использует следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="effc8-116">CSISyncClient uses the following interfaces.</span></span>
  
### <a name="interface-ilsclocalsyncclient"></a><span data-ttu-id="effc8-117">Интерфейс ILSCLocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="effc8-117">Interface ILSCLocalSyncClient</span></span>

<span data-ttu-id="effc8-118">Это основной интерфейс, используемый для синхронизации файлов в Office.</span><span class="sxs-lookup"><span data-stu-id="effc8-118">This is the primary interface used to synchronize files in Office.</span></span>
  
- <span data-ttu-id="effc8-119">ProgID: Office.LocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="effc8-119">ProgID: Office.LocalSyncClient</span></span>
- <span data-ttu-id="effc8-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span><span class="sxs-lookup"><span data-stu-id="effc8-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span></span>
- <span data-ttu-id="effc8-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span><span class="sxs-lookup"><span data-stu-id="effc8-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span></span>
   
<span data-ttu-id="effc8-122">Объект COM, который выставит, используется в качестве вне proc-сервера.</span><span class="sxs-lookup"><span data-stu-id="effc8-122">The COM object that is exposed is used as an out-of-proc server.</span></span> <span data-ttu-id="effc8-123">Указание CLSCTX_LOCAL_SERVER как части CoCreateInstance позволяет совместить процессы от 64 до 32 раз.</span><span class="sxs-lookup"><span data-stu-id="effc8-123">Specifying CLSCTX_LOCAL_SERVER as part of CoCreateInstance allows compatability between 64bit and 32bit processes.</span></span>
  
<span data-ttu-id="effc8-124">После создания объекта COM необходимо сначала вызвать [ILSCLocalSyncClient::Initialize.](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)</span><span class="sxs-lookup"><span data-stu-id="effc8-124">Once you've co-created the COM object, you MUST call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) first.</span></span> <span data-ttu-id="effc8-125">После [успешного завершения ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) любой API можно вызывать как можно чаще и в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="effc8-125">Once [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has completed successfully, you may call any API as often as you wish and in any order.</span></span> <span data-ttu-id="effc8-126">Также можно вызвать [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) для уже инициализированного объекта, но это ничего не делает.</span><span class="sxs-lookup"><span data-stu-id="effc8-126">You may also call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) on an already initialized object, but this does nothing.</span></span> 
  
<span data-ttu-id="effc8-127">Исключениями из предыдущего абзаца являются [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) и [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="effc8-127">The exceptions to the previous paragraph are [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) and [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="effc8-128">После вызова [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) объекта COM необходимо уничтожать этот объект и создавать новый.</span><span class="sxs-lookup"><span data-stu-id="effc8-128">After you call [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) on the COM object, you MUST destroy that object and create a new one.</span></span> <span data-ttu-id="effc8-129">[ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) удалит ваш подкаш, удалит все связанные сведения о файле в кэше, но оставляет документы на диске.</span><span class="sxs-lookup"><span data-stu-id="effc8-129">[ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) will delete your subcache, delete all associated file information in the cache, but leave the documents on disk.</span></span> <span data-ttu-id="effc8-130">Оно также оставляет состояние без изменений для связи с кэшом.</span><span class="sxs-lookup"><span data-stu-id="effc8-130">It also leaves the state intact for communicating with the cache.</span></span> <span data-ttu-id="effc8-131">Это позволяет вызвать [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) еще раз, чтобы создать кэш без необходимости уничтожения и воссоздания com-объекта.</span><span class="sxs-lookup"><span data-stu-id="effc8-131">This allows you to call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) again to create a new cache without having to destroy and recreate the COM object.</span></span> 
  
<span data-ttu-id="effc8-132">**Функции открытых членов**</span><span class="sxs-lookup"><span data-stu-id="effc8-132">**Public member functions**</span></span>

#### <a name="ilsclocalsyncclientdeletefile"></a><span data-ttu-id="effc8-133">ILSCLocalSyncClient::D eleteFile</span><span class="sxs-lookup"><span data-stu-id="effc8-133">ILSCLocalSyncClient::DeleteFile</span></span>

<span data-ttu-id="effc8-134">DeleteFile используется для удаления сведений о файле из кэша.</span><span class="sxs-lookup"><span data-stu-id="effc8-134">DeleteFile is used to remove the file information from the cache.</span></span> <span data-ttu-id="effc8-135">Однако этот метод оставляет связанный файл на диске и на сервере.</span><span class="sxs-lookup"><span data-stu-id="effc8-135">However, this method will leave the associated file on disk and on the server.</span></span>
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="effc8-136">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-136">Parameters</span></span>

 <span data-ttu-id="effc8-137">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="effc8-137">_bstrResourceID_</span></span>
  
<span data-ttu-id="effc8-138">Строка, идентифицирует ResourceID файла.</span><span class="sxs-lookup"><span data-stu-id="effc8-138">The string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="effc8-139">Это значение должно быть непустым и иметь не более 128 символов.</span><span class="sxs-lookup"><span data-stu-id="effc8-139">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="effc8-140">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-140">Return values</span></span>

|<span data-ttu-id="effc8-141">Значение</span><span class="sxs-lookup"><span data-stu-id="effc8-141">Value</span></span>|<span data-ttu-id="effc8-142">Описание</span><span class="sxs-lookup"><span data-stu-id="effc8-142">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="effc8-143">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="effc8-143">E_FAIL</span></span>  <br/> |<span data-ttu-id="effc8-144">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="effc8-144">The call failed.</span></span>  <br/> |
|<span data-ttu-id="effc8-145">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="effc8-145">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="effc8-146">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="effc8-146">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="effc8-147">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="effc8-147">E_FAIL</span></span>  <br/> |<span data-ttu-id="effc8-148">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="effc8-148">The call failed.</span></span>  <br/> |
|<span data-ttu-id="effc8-149">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="effc8-149">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="effc8-150">Заданный ResourceID не находится в кэше.</span><span class="sxs-lookup"><span data-stu-id="effc8-150">The given ResourceID is not in the cache.</span></span>  <br/> |
|<span data-ttu-id="effc8-151">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="effc8-151">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="effc8-152">Инициализация не была успешно вызвана в прошлом.</span><span class="sxs-lookup"><span data-stu-id="effc8-152">Initialize has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="effc8-153">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="effc8-153">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="effc8-154">В настоящее время файл синхронизируется или открывается и не может быть удален.</span><span class="sxs-lookup"><span data-stu-id="effc8-154">The file is currently synchronizing or open and cannot be deleted.</span></span>  <br/> |
|<span data-ttu-id="effc8-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="effc8-155">S_OK</span></span>  <br/> |<span data-ttu-id="effc8-156">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="effc8-156">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a><span data-ttu-id="effc8-157">ILSCLocalSyncClient::GetChanges</span><span class="sxs-lookup"><span data-stu-id="effc8-157">ILSCLocalSyncClient::GetChanges</span></span>
<span data-ttu-id="effc8-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span><span class="sxs-lookup"><span data-stu-id="effc8-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span></span>

<span data-ttu-id="effc8-159">GetChanges возвращает enumerator объектов ILSCEvent, а также возвращает маркер, который передается следующему вызову GetChanges, если потребитель обработал предыдущий набор событий.</span><span class="sxs-lookup"><span data-stu-id="effc8-159">GetChanges returns an enumerator of ILSCEvent objects, and also returns a token that is given to the next call to GetChanges, assuming the consumer has processed the previous set of events.</span></span> <span data-ttu-id="effc8-160">События перед  _указанным nPreviousChangesToken_ будут удалены и недоступны.</span><span class="sxs-lookup"><span data-stu-id="effc8-160">Events before the  _nPreviousChangesToken_ specified will be deleted and unavailable.</span></span> <span data-ttu-id="effc8-161">Если обработка событий не происходит,  _pnCurrentChangesToken_ должен иметь то же значение, что  _и nPreviousChangesToken,_ но  _ppiEvents_ все равно будет установлен.</span><span class="sxs-lookup"><span data-stu-id="effc8-161">If there are no events to be processed,  _pnCurrentChangesToken_ should be the same value as  _nPreviousChangesToken_, but  _ppiEvents_ will still be set.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a><span data-ttu-id="effc8-162">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-162">Parameters</span></span>

 <span data-ttu-id="effc8-163">_nPreviousChangesToken_</span><span class="sxs-lookup"><span data-stu-id="effc8-163">_nPreviousChangesToken_</span></span>
  
<span data-ttu-id="effc8-164">Определяет, какое событие было обработано потребителем в последний раз.</span><span class="sxs-lookup"><span data-stu-id="effc8-164">Identifies which event was last processed by the consumer.</span></span> 
  
 <span data-ttu-id="effc8-165">_pnCurrentChangesToken_</span><span class="sxs-lookup"><span data-stu-id="effc8-165">_pnCurrentChangesToken_</span></span>
  
<span data-ttu-id="effc8-166">Определяет последнее событие, которое передается потребителю.</span><span class="sxs-lookup"><span data-stu-id="effc8-166">Identifies the most recent event being handed to the consumer.</span></span> <span data-ttu-id="effc8-167">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="effc8-167">Must not be null.</span></span>
  
 <span data-ttu-id="effc8-168">_ppiEvents_</span><span class="sxs-lookup"><span data-stu-id="effc8-168">_ppiEvents_</span></span>
  
<span data-ttu-id="effc8-169">Enumerator для событий, переданных потребителю.</span><span class="sxs-lookup"><span data-stu-id="effc8-169">An enumerator for the events handed to the consumer.</span></span> <span data-ttu-id="effc8-170">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="effc8-170">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="effc8-171">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-171">Return values</span></span>

|<span data-ttu-id="effc8-172">Значение</span><span class="sxs-lookup"><span data-stu-id="effc8-172">Value</span></span>|<span data-ttu-id="effc8-173">Описание</span><span class="sxs-lookup"><span data-stu-id="effc8-173">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="effc8-174">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="effc8-174">E_FAIL</span></span>  <br/> |<span data-ttu-id="effc8-175">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="effc8-175">The call failed.</span></span>  <br/> |
|<span data-ttu-id="effc8-176">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="effc8-176">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="effc8-177">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="effc8-177">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="effc8-178">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="effc8-178">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="effc8-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="effc8-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="effc8-180">S_OK</span><span class="sxs-lookup"><span data-stu-id="effc8-180">S_OK</span></span>  <br/> |<span data-ttu-id="effc8-181">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="effc8-181">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a><span data-ttu-id="effc8-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="effc8-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span></span>

<span data-ttu-id="effc8-183">GetClientNetworkSyncPermission используется для запроса на необходимость переопределения синхронизации office с использованием сетевой стоимости и энергопотребления.</span><span class="sxs-lookup"><span data-stu-id="effc8-183">GetClientNetworkSyncPermission is used to query whether Office's synchronizing heuristics for network cost and power usage are overridden.</span></span> <span data-ttu-id="effc8-184">Если в сети с высокой стоимостью 3G или в сети с высокой стоимостью либо при работе от аккумулятора или при подключении к сети, Office может заблокировать сетевой трафик до более непрозраченного времени.</span><span class="sxs-lookup"><span data-stu-id="effc8-184">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span>
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a><span data-ttu-id="effc8-185">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-185">Parameters</span></span>

 <span data-ttu-id="effc8-186">_nspType_</span><span class="sxs-lookup"><span data-stu-id="effc8-186">_nspType_</span></span>
  
<span data-ttu-id="effc8-187">Флаг, определяющий, какие затраты необходимо запросить.</span><span class="sxs-lookup"><span data-stu-id="effc8-187">A flag which defines which cost heuristic to query.</span></span> <span data-ttu-id="effc8-188">См. [enum LSCNetworkSyncPermissionType.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType)</span><span class="sxs-lookup"><span data-stu-id="effc8-188">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span> 
  
 <span data-ttu-id="effc8-189">_pfSyncEnabled_</span><span class="sxs-lookup"><span data-stu-id="effc8-189">_pfSyncEnabled_</span></span>
  
<span data-ttu-id="effc8-190">Указывает, переопределяется ли в настоящее время запросивая авристическая стоимость.</span><span class="sxs-lookup"><span data-stu-id="effc8-190">Specifies whether the requested cost heuristic is currently overridden or not.</span></span> <span data-ttu-id="effc8-191">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="effc8-191">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="effc8-192">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-192">Return values</span></span>

|<span data-ttu-id="effc8-193">Значение</span><span class="sxs-lookup"><span data-stu-id="effc8-193">Value</span></span>|<span data-ttu-id="effc8-194">Описание</span><span class="sxs-lookup"><span data-stu-id="effc8-194">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="effc8-195">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="effc8-195">E_FAIL</span></span>  <br/> |<span data-ttu-id="effc8-196">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="effc8-196">The call failed.</span></span>  <br/> |
|<span data-ttu-id="effc8-197">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="effc8-197">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="effc8-198">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="effc8-198">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="effc8-199">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="effc8-199">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="effc8-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="effc8-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="effc8-201">S_OK</span><span class="sxs-lookup"><span data-stu-id="effc8-201">S_OK</span></span>  <br/> |<span data-ttu-id="effc8-202">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="effc8-202">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a><span data-ttu-id="effc8-203">ILSCLocalSyncClient::GetFileStatus</span><span class="sxs-lookup"><span data-stu-id="effc8-203">ILSCLocalSyncClient::GetFileStatus</span></span>

<span data-ttu-id="effc8-204">GetFileStatus используется для сбора сведений об определенном файле: существует ли он в кэше, находится ли в состоянии ожидания связь с копией сервера и есть ли в Office 2013 самые последние данные из локальной копии.</span><span class="sxs-lookup"><span data-stu-id="effc8-204">GetFileStatus is used to gather information for a specific file: whether it exists in the cache, if it has pending communication with the server copy, and if Office 2013 has the most up to date data from the local copy.</span></span> <span data-ttu-id="effc8-205">Для определения сведений, запрашиваемой COM-объектом CsiSyncClient, требуется битовая пометка значений [Enum LSCStatusFlag.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag)</span><span class="sxs-lookup"><span data-stu-id="effc8-205">It requires a bitwise flag of [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) values to determine what information the CsiSyncClient COM object is to query for.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a><span data-ttu-id="effc8-206">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-206">Parameters</span></span>

 <span data-ttu-id="effc8-207">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="effc8-207">_bstrResourceID_</span></span>
  
<span data-ttu-id="effc8-208">Строка, идентифицирует файл в клиенте.</span><span class="sxs-lookup"><span data-stu-id="effc8-208">The string which identifies the file on the client.</span></span> <span data-ttu-id="effc8-209">Это значение должно быть непустым и иметь не более 128 символов.</span><span class="sxs-lookup"><span data-stu-id="effc8-209">This value must be non-empty, with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="effc8-210">_sfRequestedStatus_</span><span class="sxs-lookup"><span data-stu-id="effc8-210">_sfRequestedStatus_</span></span>
  
<span data-ttu-id="effc8-211">Флаг, который определяет возвращаемую информацию.</span><span class="sxs-lookup"><span data-stu-id="effc8-211">A flag which defines what information to return.</span></span> <span data-ttu-id="effc8-212">См. [enum LSCStatusFlag.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag)</span><span class="sxs-lookup"><span data-stu-id="effc8-212">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
 <span data-ttu-id="effc8-213">_pbstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="effc8-213">_pbstrFileSystemPath_</span></span>
  
<span data-ttu-id="effc8-214">Строка, которая определяет расположение файла, определяемого  _bstrResourceID_ в клиенте.</span><span class="sxs-lookup"><span data-stu-id="effc8-214">The string which identifies the location of the file identified by  _bstrResourceID_ on the client.</span></span> <span data-ttu-id="effc8-215">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="effc8-215">Must not be null.</span></span> 
  
 <span data-ttu-id="effc8-216">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="effc8-216">_pbstrETag_</span></span>
  
<span data-ttu-id="effc8-217">Строка, которая будет содержать eTag для файла, заданного _bstrResourceID._</span><span class="sxs-lookup"><span data-stu-id="effc8-217">A string which will contain the eTag for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="effc8-218">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="effc8-218">Must not be null.</span></span> 
  
 <span data-ttu-id="effc8-219">_psfFileStatus_</span><span class="sxs-lookup"><span data-stu-id="effc8-219">_psfFileStatus_</span></span>
  
<span data-ttu-id="effc8-220">Флаг, который будет содержать состояние, запрашиваемого  _с помощью sfRequestedStatus_ для файла, заданного  _bstrResourceID_.</span><span class="sxs-lookup"><span data-stu-id="effc8-220">A flag which will contain the status requested via  _sfRequestedStatus_ for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="effc8-221">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="effc8-221">Must not be null.</span></span> <span data-ttu-id="effc8-222">См. [enum LSCStatusFlag.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag)</span><span class="sxs-lookup"><span data-stu-id="effc8-222">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="effc8-223">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-223">Return values</span></span>

|<span data-ttu-id="effc8-224">Значение</span><span class="sxs-lookup"><span data-stu-id="effc8-224">Value</span></span>|<span data-ttu-id="effc8-225">Описание</span><span class="sxs-lookup"><span data-stu-id="effc8-225">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="effc8-226">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="effc8-226">E_FAIL</span></span>  <br/> |<span data-ttu-id="effc8-227">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="effc8-227">The call failed.</span></span>  <br/> |
|<span data-ttu-id="effc8-228">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="effc8-228">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="effc8-229">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="effc8-229">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="effc8-230">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="effc8-230">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="effc8-231">Сведения о файле, указанные  _bstrResourceID,_ не существуют в кэше.</span><span class="sxs-lookup"><span data-stu-id="effc8-231">The file information specified by  _bstrResourceID_ does not exist in the cache.</span></span>  <br/> |
|<span data-ttu-id="effc8-232">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="effc8-232">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="effc8-233">LSCStatusFlag_LocalFileUnchanged запроса или файл, указанный  _bstrResourceID,_ заблокирован или отсутствует.</span><span class="sxs-lookup"><span data-stu-id="effc8-233">LSCStatusFlag_LocalFileUnchanged was requested or the file specified by  _bstrResourceID_ is locked or missing.</span></span>  <br/> |
|<span data-ttu-id="effc8-234">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="effc8-234">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="effc8-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="effc8-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="effc8-236">S_OK</span><span class="sxs-lookup"><span data-stu-id="effc8-236">S_OK</span></span>  <br/> |<span data-ttu-id="effc8-237">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="effc8-237">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a><span data-ttu-id="effc8-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="effc8-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span></span>
<span data-ttu-id="effc8-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span><span class="sxs-lookup"><span data-stu-id="effc8-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span></span>

<span data-ttu-id="effc8-240">GetSupportedFileExtensions возвращает список расширений файлов, которые в настоящее время поддерживаются com-объектом CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="effc8-240">GetSupportedFileExtensions returns a list of pipe-delimited file extensions which are currently supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="effc8-241">Обратите внимание, что этот список может измениться, и потребитель получит уведомление об изменении с помощью объекта IPartnerActivityCallback, предоставленного в [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (См. EventOccured).</span><span class="sxs-lookup"><span data-stu-id="effc8-241">Note that this list may change, and the consumer will be notified of a change via the IPartnerActivityCallback object provided on [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (See EventOccured).</span></span> 
  
<span data-ttu-id="effc8-242">Пример возвращаемой строки: "|docx|docm|pptx|"</span><span class="sxs-lookup"><span data-stu-id="effc8-242">An example of the string returned is as follows: "|docx|docm|pptx|"</span></span>
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a><span data-ttu-id="effc8-243">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-243">Parameters</span></span>

 <span data-ttu-id="effc8-244">_pbstrSupportedFileExtensions_</span><span class="sxs-lookup"><span data-stu-id="effc8-244">_pbstrSupportedFileExtensions_</span></span>
  
<span data-ttu-id="effc8-245">Строка, устанавливаемая с помощью набора расширений файлов, которые поддерживаются com-объектом CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="effc8-245">A string to be set with a pipe-delimited set of file extensions supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="effc8-246">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="effc8-246">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="effc8-247">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-247">Return values</span></span>

|<span data-ttu-id="effc8-248">Значение</span><span class="sxs-lookup"><span data-stu-id="effc8-248">Value</span></span>|<span data-ttu-id="effc8-249">Описание</span><span class="sxs-lookup"><span data-stu-id="effc8-249">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="effc8-250">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="effc8-250">E_FAIL</span></span>  <br/> |<span data-ttu-id="effc8-251">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="effc8-251">The call failed.</span></span>  <br/> |
|<span data-ttu-id="effc8-252">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="effc8-252">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="effc8-253">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="effc8-253">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="effc8-254">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="effc8-254">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="effc8-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="effc8-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="effc8-256">S_OK</span><span class="sxs-lookup"><span data-stu-id="effc8-256">S_OK</span></span>  <br/> |<span data-ttu-id="effc8-257">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="effc8-257">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a><span data-ttu-id="effc8-258">ILSCLocalSyncClient::Initialize</span><span class="sxs-lookup"><span data-stu-id="effc8-258">ILSCLocalSyncClient::Initialize</span></span>
<span data-ttu-id="effc8-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span><span class="sxs-lookup"><span data-stu-id="effc8-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span></span>

<span data-ttu-id="effc8-260">Инициализация должна быть первым вызванным методом.</span><span class="sxs-lookup"><span data-stu-id="effc8-260">Initialize must be the first method called.</span></span> <span data-ttu-id="effc8-261">В противном случае все остальные API будут возвращать E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="effc8-261">Otherwise, all other APIs will return E_LSC_NOTINITIALIZED.</span></span> <span data-ttu-id="effc8-262">Вызов инициализации для уже инициализированного объекта S_OK и ничего не делает.</span><span class="sxs-lookup"><span data-stu-id="effc8-262">Calling Initialize on an already initialized object returns S_OK and does nothing.</span></span> <span data-ttu-id="effc8-263">Если E_LSC_CACHEMISMATCH возвращается, вызываемая может вызвать [ILSCLocalSyncClient::ResetCache, ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) чтобы удалить кэш, связанный с данным SuppliedID.</span><span class="sxs-lookup"><span data-stu-id="effc8-263">If E_LSC_CACHEMISMATCH is returned, the caller may call [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) to delete the cache associated with the given SuppliedID.</span></span> <span data-ttu-id="effc8-264">Однако в этом случае другие API по-прежнему будут возвращать E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="effc8-264">However, in this case other APIs will still return E_LSC_NOTINITIALIZED.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a><span data-ttu-id="effc8-265">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-265">Parameters</span></span>

 <span data-ttu-id="effc8-266">_bstrSuppliedID_</span><span class="sxs-lookup"><span data-stu-id="effc8-266">_bstrSuppliedID_</span></span>
  
<span data-ttu-id="effc8-267">Определяет потребителя и кэш для использования.</span><span class="sxs-lookup"><span data-stu-id="effc8-267">Identifies the consumer and which cache to use.</span></span> <span data-ttu-id="effc8-268">Должен быть непустым и иметь не более 32 символов.</span><span class="sxs-lookup"><span data-stu-id="effc8-268">Must be non-empty with a maximum of 32 characters.</span></span> 
  
 <span data-ttu-id="effc8-269">_bstrProgID_</span><span class="sxs-lookup"><span data-stu-id="effc8-269">_bstrProgID_</span></span>
  
<span data-ttu-id="effc8-270">Определяет COM-объект потребителя для двунабной связи.</span><span class="sxs-lookup"><span data-stu-id="effc8-270">Identifies the consumer's COM object for two-way communication.</span></span> <span data-ttu-id="effc8-271">Должен быть непустым и иметь не более 39 символов.</span><span class="sxs-lookup"><span data-stu-id="effc8-271">Must be non-empty with a maximum of 39 characters.</span></span> <span data-ttu-id="effc8-272">Дополнительные [ \< сведения \> о progID](https://docs.microsoft.com/windows/desktop/com/-progid--key) см. в ключе ProgID.</span><span class="sxs-lookup"><span data-stu-id="effc8-272">See [\<ProgID\> Key](https://docs.microsoft.com/windows/desktop/com/-progid--key) for more information about ProgIDs.</span></span> 
  
 <span data-ttu-id="effc8-273">_bstrFileSystemDirectoryHint_</span><span class="sxs-lookup"><span data-stu-id="effc8-273">_bstrFileSystemDirectoryHint_</span></span>
  
<span data-ttu-id="effc8-274">Определяет корневой каталог, в котором будут храниться локальные файлы.</span><span class="sxs-lookup"><span data-stu-id="effc8-274">Identifies the directory root in which local files will be stored.</span></span> <span data-ttu-id="effc8-275">Должен быть непустым и иметь не более 256 символов.</span><span class="sxs-lookup"><span data-stu-id="effc8-275">Must be non-empty with a maximum of 256 characters.</span></span> <span data-ttu-id="effc8-276">Каталог должен уже существовать.</span><span class="sxs-lookup"><span data-stu-id="effc8-276">The directory must already exist.</span></span> 
  
 <span data-ttu-id="effc8-277">_pEventCallback_</span><span class="sxs-lookup"><span data-stu-id="effc8-277">_pEventCallback_</span></span>
  
<span data-ttu-id="effc8-278">Интерфейс callback, который CsiSyncClient будет уведомлять об изменениях.</span><span class="sxs-lookup"><span data-stu-id="effc8-278">The callback interface which CsiSyncClient will notify on changes.</span></span> <span data-ttu-id="effc8-279">См. IPartnerActivityCallback::EventOccurred.</span><span class="sxs-lookup"><span data-stu-id="effc8-279">See IPartnerActivityCallback::EventOccurred.</span></span> <span data-ttu-id="effc8-280">Это значение не должно иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="effc8-280">This value must not be null.</span></span> 
  
 <span data-ttu-id="effc8-281">_pfCreatedNewCache_</span><span class="sxs-lookup"><span data-stu-id="effc8-281">_pfCreatedNewCache_</span></span>
  
<span data-ttu-id="effc8-282">Возвращает, был ли создан новый кэш.</span><span class="sxs-lookup"><span data-stu-id="effc8-282">Returns whether a new cache was created.</span></span> <span data-ttu-id="effc8-283">Если с SuppliedID кэш не связан, он будет создан.</span><span class="sxs-lookup"><span data-stu-id="effc8-283">If no cache is associated with the SuppliedID, one will be created.</span></span> <span data-ttu-id="effc8-284">Это значение не должно иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="effc8-284">This value must not be null.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="effc8-285">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-285">Return values</span></span>

|<span data-ttu-id="effc8-286">Значение</span><span class="sxs-lookup"><span data-stu-id="effc8-286">Value</span></span>|<span data-ttu-id="effc8-287">Описание</span><span class="sxs-lookup"><span data-stu-id="effc8-287">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="effc8-288">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="effc8-288">E_FAIL</span></span>  <br/> |<span data-ttu-id="effc8-289">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="effc8-289">The call failed.</span></span>  <br/> |
|<span data-ttu-id="effc8-290">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="effc8-290">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="effc8-291">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="effc8-291">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="effc8-292">E_LSC_CACHEMISMATCH</span><span class="sxs-lookup"><span data-stu-id="effc8-292">E_LSC_CACHEMISMATCH</span></span>  <br/> |<span data-ttu-id="effc8-293">С ним уже связан кэш SuppliedID, но он отличается от предоставленного progId или FileSystemDirectoryHint.</span><span class="sxs-lookup"><span data-stu-id="effc8-293">A SuppliedID already has a cache associated with it, but has a different ProgId or FileSystemDirectoryHint than the ones provided.</span></span>  <br/> |
|<span data-ttu-id="effc8-294">E_LSC_DIRECTORYHINTCONFLICT</span><span class="sxs-lookup"><span data-stu-id="effc8-294">E_LSC_DIRECTORYHINTCONFLICT</span></span>  <br/> |<span data-ttu-id="effc8-295">FileSystemDirectoryHint (или вузаная папка) уже существует в другом кэше.</span><span class="sxs-lookup"><span data-stu-id="effc8-295">The FileSystemDirectoryHint (or a subfolder) already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="effc8-296">E_LAC_PROGIDCONFLICT</span><span class="sxs-lookup"><span data-stu-id="effc8-296">E_LAC_PROGIDCONFLICT</span></span>  <br/> |<span data-ttu-id="effc8-297">ProgID уже существует в другом кэше.</span><span class="sxs-lookup"><span data-stu-id="effc8-297">The ProgID already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="effc8-298">S_OK</span><span class="sxs-lookup"><span data-stu-id="effc8-298">S_OK</span></span>  <br/> |<span data-ttu-id="effc8-299">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="effc8-299">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a><span data-ttu-id="effc8-300">ILSCLocalSyncClient::LocalFileChange</span><span class="sxs-lookup"><span data-stu-id="effc8-300">ILSCLocalSyncClient::LocalFileChange</span></span>
<span data-ttu-id="effc8-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="effc8-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span></span>

<span data-ttu-id="effc8-302">LocalFileChange используется для отправки указанного файла объекту COM CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="effc8-302">LocalFileChange is used to tell the CsiSyncClient COM object to attempt to upload the specified file.</span></span> <span data-ttu-id="effc8-303">Метод подготовит файл к отправке, включая чтение текущего содержимого файла.</span><span class="sxs-lookup"><span data-stu-id="effc8-303">The method will prepare the file for upload, including reading the file's current contents.</span></span> <span data-ttu-id="effc8-304">Если отправка уже ожидает отправки, предыдущая отправка будет отклонена, а новое содержимое будет подготовлено к отправке.</span><span class="sxs-lookup"><span data-stu-id="effc8-304">If an upload is already pending, the previous upload will be discarded and the new contents prepared for upload.</span></span> <span data-ttu-id="effc8-305">Если файл открыт для редактирования в приложении, этот метод возвращает S_OK без подготовки файла к отправке (приложение должно уже сделать это при внесении изменений).</span><span class="sxs-lookup"><span data-stu-id="effc8-305">If the file is open for editing in an application, this method will return S_OK without preparing the file for upload (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="effc8-306">Этот метод разрешает отправку, если он был помечен как ранее заблокированный (см. [ILSCLocalSyncClient::RenameFile). ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)</span><span class="sxs-lookup"><span data-stu-id="effc8-306">This method will allow uploads if it was marked as uploads blocked previously (see [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span></span>
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="effc8-307">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-307">Parameters</span></span>

 <span data-ttu-id="effc8-308">_bstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="effc8-308">_bstrFileSystemPath_</span></span>
  
<span data-ttu-id="effc8-309">Строка, идентифицирует файл в клиенте.</span><span class="sxs-lookup"><span data-stu-id="effc8-309">A string which identifies the file on the client.</span></span> <span data-ttu-id="effc8-310">Это значение должно быть непустым локальным путем не более 256 символов.</span><span class="sxs-lookup"><span data-stu-id="effc8-310">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="effc8-311">Этот путь должен быть в дереве каталогов, заданном FileSystemDirectoryHint при вызове [ILSCLocalSyncClient::Initialize.](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)</span><span class="sxs-lookup"><span data-stu-id="effc8-311">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was made.</span></span> 
  
 <span data-ttu-id="effc8-312">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="effc8-312">_bstrResourceID_</span></span>
  
<span data-ttu-id="effc8-313">Строка, идентифицирует ResourceID файла.</span><span class="sxs-lookup"><span data-stu-id="effc8-313">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="effc8-314">Это значение должно быть непустым и иметь не более 128 символов.</span><span class="sxs-lookup"><span data-stu-id="effc8-314">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="effc8-315">_bstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="effc8-315">_bstrWebPath_</span></span>
  
<span data-ttu-id="effc8-316">Строка, идентифицирует файл на сервере.</span><span class="sxs-lookup"><span data-stu-id="effc8-316">A string which identifies the file on the server.</span></span> <span data-ttu-id="effc8-317">Это значение должно быть непустым, допустимым URL-адресом, но не более INTERNET_MAX_URL_LENGTH, как определено https://support.microsoft.com/kb/208427 .</span><span class="sxs-lookup"><span data-stu-id="effc8-317">This value must be non-empty, valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="effc8-318">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-318">Return values</span></span>

|<span data-ttu-id="effc8-319">Значение</span><span class="sxs-lookup"><span data-stu-id="effc8-319">Value</span></span>|<span data-ttu-id="effc8-320">Описание</span><span class="sxs-lookup"><span data-stu-id="effc8-320">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="effc8-321">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="effc8-321">E_FAIL</span></span>  <br/> |<span data-ttu-id="effc8-322">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="effc8-322">The call failed.</span></span>  <br/> |
|<span data-ttu-id="effc8-323">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="effc8-323">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="effc8-324">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="effc8-324">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="effc8-325">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="effc8-325">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="effc8-326">Файл, указанный  _bstrFileSystemPath,_ имеет другой ResourceID, чем указано.</span><span class="sxs-lookup"><span data-stu-id="effc8-326">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span> <span data-ttu-id="effc8-327">Событие типа LSCEventType_OnFilePathConflict при возвращении этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="effc8-327">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="effc8-328">См. [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="effc8-328">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="effc8-329">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="effc8-329">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="effc8-330">Файл был удален в середине операции.</span><span class="sxs-lookup"><span data-stu-id="effc8-330">The file was deleted mid-operation.</span></span>  <br/> |
|<span data-ttu-id="effc8-331">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="effc8-331">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="effc8-332">Заданное расширение файла не поддерживается com-объектом CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="effc8-332">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="effc8-333">См. [ILSCLocalSyncClient::GetSupportedFileExtensions. ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions)</span><span class="sxs-lookup"><span data-stu-id="effc8-333">See [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span></span>  <br/> |
|<span data-ttu-id="effc8-334">E_LSC_FILEUPTODATE</span><span class="sxs-lookup"><span data-stu-id="effc8-334">E_LSC_FILEUPTODATE</span></span>  <br/> |<span data-ttu-id="effc8-335">Com-объект не запланил отправку, так как файл в кэше имел последние изменения с диска.</span><span class="sxs-lookup"><span data-stu-id="effc8-335">The COM object did not schedule an upload because the file in the cache had the most recent changes from the disk.</span></span>  <br/> |
|<span data-ttu-id="effc8-336">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="effc8-336">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="effc8-337">Файл, указанный  _bstrFileSystemPath,_ отсутствует или заблокирован.</span><span class="sxs-lookup"><span data-stu-id="effc8-337">The file specified by  _bstrFileSystemPath_ is missing or locked.</span></span>  <br/> |
|<span data-ttu-id="effc8-338">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="effc8-338">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="effc8-339">Данный fileSystemPath не находится в корне каталога, указанном FileSystemDirectoryHint при вызове инициализации.</span><span class="sxs-lookup"><span data-stu-id="effc8-339">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="effc8-340">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="effc8-340">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="effc8-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="effc8-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="effc8-342">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="effc8-342">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="effc8-343">Файл, указанный  _bstrResourceID,_ имеет файл FileSystemPath, который отличается от указанного.</span><span class="sxs-lookup"><span data-stu-id="effc8-343">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="effc8-344">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="effc8-344">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="effc8-345">Указанный файл уже имеет ожидающих изменений в другом кэше и еще не может быть связан с кэшом потребителя.</span><span class="sxs-lookup"><span data-stu-id="effc8-345">The file specified already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="effc8-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="effc8-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="effc8-347">Предоставленный WebPath попадает в другой кэш.</span><span class="sxs-lookup"><span data-stu-id="effc8-347">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="effc8-348">S_OK</span><span class="sxs-lookup"><span data-stu-id="effc8-348">S_OK</span></span>  <br/> |<span data-ttu-id="effc8-349">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="effc8-349">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a><span data-ttu-id="effc8-350">ILSCLocalSyncClient::RenameFile</span><span class="sxs-lookup"><span data-stu-id="effc8-350">ILSCLocalSyncClient::RenameFile</span></span>
<span data-ttu-id="effc8-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span><span class="sxs-lookup"><span data-stu-id="effc8-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span></span>

<span data-ttu-id="effc8-352">RenameFile связывает новый URL-адрес и локальный путь для заданного ResourceID.</span><span class="sxs-lookup"><span data-stu-id="effc8-352">RenameFile will associate a new URL and local path for a given ResourceID.</span></span> <span data-ttu-id="effc8-353">Если файл, указанный с помощью ResourceID, еще не существует в кэше, будет предпринята попытка создать его и пометить для скачивания.</span><span class="sxs-lookup"><span data-stu-id="effc8-353">If the file specified by the ResourceID doesn't already exist in the cache, an attempt will be made to create it and mark it for download.</span></span>
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a><span data-ttu-id="effc8-354">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-354">Parameters</span></span>

 <span data-ttu-id="effc8-355">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="effc8-355">_bstrResourceID_</span></span>
  
<span data-ttu-id="effc8-356">Строка, идентифицирует ResourceID файла.</span><span class="sxs-lookup"><span data-stu-id="effc8-356">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="effc8-357">Это значение должно быть непустым и иметь не более 128 символов.</span><span class="sxs-lookup"><span data-stu-id="effc8-357">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="effc8-358">_bstrNewFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="effc8-358">_bstrNewFileSystemPath_</span></span>
  
<span data-ttu-id="effc8-359">Строка, которая указывает новый локальный путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="effc8-359">A string which specifies the new local path for the file.</span></span> <span data-ttu-id="effc8-360">Это значение должно быть непустым локальным путем не более 256 символов.</span><span class="sxs-lookup"><span data-stu-id="effc8-360">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="effc8-361">Этот путь должен быть указан в дереве каталогов, указанном FileSystemDirectoryHint при вызове инициализации.</span><span class="sxs-lookup"><span data-stu-id="effc8-361">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span> 
  
 <span data-ttu-id="effc8-362">_bstrNewWebPath_</span><span class="sxs-lookup"><span data-stu-id="effc8-362">_bstrNewWebPath_</span></span>
  
<span data-ttu-id="effc8-363">Строка, которая указывает новый URL-адрес файла.</span><span class="sxs-lookup"><span data-stu-id="effc8-363">A string which specifies the new URL for the file.</span></span> <span data-ttu-id="effc8-364">Это значение должно быть непустым допустимым URL-адресом, но не более INTERNET_MAX_URL_LENGTH, как определено https://support.microsoft.com/kb/208427 .</span><span class="sxs-lookup"><span data-stu-id="effc8-364">This value must be non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
 <span data-ttu-id="effc8-365">_fBlockUploads_</span><span class="sxs-lookup"><span data-stu-id="effc8-365">_fBlockUploads_</span></span>
  
<span data-ttu-id="effc8-366">Указывает, разрешены ли в данный момент отправки в новое расположение.</span><span class="sxs-lookup"><span data-stu-id="effc8-366">Specifies whether uploads to the new location are allowed currently.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="effc8-367">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-367">Return values</span></span>

|<span data-ttu-id="effc8-368">Значение</span><span class="sxs-lookup"><span data-stu-id="effc8-368">Value</span></span>|<span data-ttu-id="effc8-369">Описание</span><span class="sxs-lookup"><span data-stu-id="effc8-369">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="effc8-370">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="effc8-370">E_FAIL</span></span>  <br/> |<span data-ttu-id="effc8-371">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="effc8-371">The call failed.</span></span>  <br/> |
|<span data-ttu-id="effc8-372">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="effc8-372">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="effc8-373">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="effc8-373">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="effc8-374">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="effc8-374">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="effc8-375">_BstrNewFileSystemPath_ или _bstrNewWebPath уже_ существуют в другом файле в любом кэше.</span><span class="sxs-lookup"><span data-stu-id="effc8-375">The  _bstrNewFileSystemPath_ or  _bstrNewWebPath_ already exist on another file in any cache.</span></span> <span data-ttu-id="effc8-376">Событие типа LSCEventType_OnFilePathConflict при возвращении этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="effc8-376">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="effc8-377">См. [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="effc8-377">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="effc8-378">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="effc8-378">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="effc8-379">Сведения о файле были удалены из кэша во время работы этого метода.</span><span class="sxs-lookup"><span data-stu-id="effc8-379">The file information was deleted from the cache while this method was running.</span></span>  <br/> |
|<span data-ttu-id="effc8-380">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="effc8-380">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="effc8-381">Данный fileSystemPath не находится в корне каталога, указанном FileSystemDirectoryHint при вызове инициализации.</span><span class="sxs-lookup"><span data-stu-id="effc8-381">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="effc8-382">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="effc8-382">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="effc8-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="effc8-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="effc8-384">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="effc8-384">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="effc8-385">Указанный файл в настоящее время синхронизируется в приложении Office.</span><span class="sxs-lookup"><span data-stu-id="effc8-385">The file specified is currently synchronizing in an Office application.</span></span>  <br/> |
|<span data-ttu-id="effc8-386">S_OK</span><span class="sxs-lookup"><span data-stu-id="effc8-386">S_OK</span></span>  <br/> |<span data-ttu-id="effc8-387">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="effc8-387">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a><span data-ttu-id="effc8-388">ILSCLocalSyncClient::ResetCache</span><span class="sxs-lookup"><span data-stu-id="effc8-388">ILSCLocalSyncClient::ResetCache</span></span>
<span data-ttu-id="effc8-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span><span class="sxs-lookup"><span data-stu-id="effc8-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span></span>

<span data-ttu-id="effc8-390">ResetCache удалит кэш, связанный с SuppliedID, предоставленным при инициализации.</span><span class="sxs-lookup"><span data-stu-id="effc8-390">ResetCache will delete the cache associated with the SuppliedID that was provided on Initialize.</span></span> <span data-ttu-id="effc8-391">К ним относятся все сведения о файле, но файлы будут оставляться как на клиенте, так и на сервере.</span><span class="sxs-lookup"><span data-stu-id="effc8-391">This includes all of the file information, but will leave the files on both the client and the server.</span></span> <span data-ttu-id="effc8-392">Этот метод также оставляет объект в частично неинициализированном состоянии.</span><span class="sxs-lookup"><span data-stu-id="effc8-392">This method also leaves the object in a partially uninitialized state.</span></span> <span data-ttu-id="effc8-393">После этого единственными допустимыми вызовами [являются ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) или [ILSCLocalSyncClient::Uninitialize. ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize)</span><span class="sxs-lookup"><span data-stu-id="effc8-393">The only valid calls after this are [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) or [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="effc8-394">Этот метод МОЖЕТ вызываться, если инициализация не удалась и возвращает E_LSC_CACHEMISMATCH и удаляет кэш, связанный с SuppliedID, который был предоставлен при сбое вызова.</span><span class="sxs-lookup"><span data-stu-id="effc8-394">This method MAY be called if Initialize fails and returns E_LSC_CACHEMISMATCH, and will delete the cache associated with the SuppliedID that was provided with the failing call.</span></span>
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a><span data-ttu-id="effc8-395">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-395">Parameters</span></span>

<span data-ttu-id="effc8-396">Нет</span><span class="sxs-lookup"><span data-stu-id="effc8-396">None</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="effc8-397">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-397">Return values</span></span>

|<span data-ttu-id="effc8-398">Значение</span><span class="sxs-lookup"><span data-stu-id="effc8-398">Value</span></span>|<span data-ttu-id="effc8-399">Описание</span><span class="sxs-lookup"><span data-stu-id="effc8-399">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="effc8-400">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="effc8-400">E_FAIL</span></span>  <br/> |<span data-ttu-id="effc8-401">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="effc8-401">The call failed.</span></span>  <br/> |
|<span data-ttu-id="effc8-402">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="effc8-402">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="effc8-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="effc8-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was not successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="effc8-404">S_OK</span><span class="sxs-lookup"><span data-stu-id="effc8-404">S_OK</span></span>  <br/> |<span data-ttu-id="effc8-405">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="effc8-405">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a><span data-ttu-id="effc8-406">ILSCLocalSyncClient::ServerFileChange</span><span class="sxs-lookup"><span data-stu-id="effc8-406">ILSCLocalSyncClient::ServerFileChange</span></span>
<span data-ttu-id="effc8-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="effc8-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="effc8-408">ServerFileChange сообщает COM-объекту CsiSyncClient пометить указанный файл для скачивания.</span><span class="sxs-lookup"><span data-stu-id="effc8-408">ServerFileChange tells the CsiSyncClient COM object to mark the specified file for download.</span></span> <span data-ttu-id="effc8-409">Если файл открыт в приложении Office для редактирования, этот метод возвращает S_OK без пометки файла для скачивания (приложение должно уже сделать это при внесении изменений).</span><span class="sxs-lookup"><span data-stu-id="effc8-409">If the file is open in an Office application for edit, this method will return S_OK without marking the file for download (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="effc8-410">Этот метод разрешает скачивание, если он был помечен как скачиваемые ранее заблокированные (см. renameFile).</span><span class="sxs-lookup"><span data-stu-id="effc8-410">This method will allow downloads if it was marked as downloads blocked previously (see RenameFile).</span></span>
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="effc8-411">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-411">Parameters</span></span>

|<span data-ttu-id="effc8-412">Параметр</span><span class="sxs-lookup"><span data-stu-id="effc8-412">Parameter</span></span>|<span data-ttu-id="effc8-413">Описание</span><span class="sxs-lookup"><span data-stu-id="effc8-413">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="effc8-414">bstrFileSystemPath</span><span class="sxs-lookup"><span data-stu-id="effc8-414">bstrFileSystemPath</span></span>  <br/> |<span data-ttu-id="effc8-415">Строка, идентифицирует файл в клиенте.</span><span class="sxs-lookup"><span data-stu-id="effc8-415">A string which identifies the file on the client.</span></span> <span data-ttu-id="effc8-416">Это значение должно быть непустым локальным путем не более 256 символов.</span><span class="sxs-lookup"><span data-stu-id="effc8-416">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="effc8-417">Этот путь должен быть указан в дереве каталогов, указанном FileSystemDirectoryHint при вызове инициализации.</span><span class="sxs-lookup"><span data-stu-id="effc8-417">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="effc8-418">bstrResourceID</span><span class="sxs-lookup"><span data-stu-id="effc8-418">bstrResourceID</span></span>  <br/> |<span data-ttu-id="effc8-419">Строка, идентифицирует ResourceID файла.</span><span class="sxs-lookup"><span data-stu-id="effc8-419">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="effc8-420">Это значение должно быть непустым и иметь не более 128 символов.</span><span class="sxs-lookup"><span data-stu-id="effc8-420">This value must be non-empty with a maximum of 128 characters.</span></span>  <br/> |
|<span data-ttu-id="effc8-421">bstrWebPath</span><span class="sxs-lookup"><span data-stu-id="effc8-421">bstrWebPath</span></span>  <br/> |<span data-ttu-id="effc8-422">Строка, идентифицирует файл на сервере.</span><span class="sxs-lookup"><span data-stu-id="effc8-422">A string which identifies the file on the server.</span></span> <span data-ttu-id="effc8-423">Это значение должно быть непустым допустимым URL-адресом, но не более INTERNET_MAX_URL_LENGTH, как определено https://support.microsoft.com/kb/208427 .</span><span class="sxs-lookup"><span data-stu-id="effc8-423">This value must be a non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span>  <br/> |
   
##### <a name="return-values"></a><span data-ttu-id="effc8-424">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-424">Return values</span></span>

|<span data-ttu-id="effc8-425">Значение</span><span class="sxs-lookup"><span data-stu-id="effc8-425">Value</span></span>|<span data-ttu-id="effc8-426">Описание</span><span class="sxs-lookup"><span data-stu-id="effc8-426">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="effc8-427">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="effc8-427">E_FAIL</span></span>  <br/> |<span data-ttu-id="effc8-428">Сбой при настройках состояния подключения к кэше.</span><span class="sxs-lookup"><span data-stu-id="effc8-428">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="effc8-429">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="effc8-429">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="effc8-430">Файл, указанный  _bstrFileSystemPath,_ имеет другой ResourceID, чем указано.</span><span class="sxs-lookup"><span data-stu-id="effc8-430">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span>  <br/> |
|<span data-ttu-id="effc8-431">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="effc8-431">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="effc8-432">Заданное расширение файла не поддерживается com-объектом CsiSyncClient.</span><span class="sxs-lookup"><span data-stu-id="effc8-432">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="effc8-433">См. getSupportedFileExtensions.</span><span class="sxs-lookup"><span data-stu-id="effc8-433">See GetSupportedFileExtensions.</span></span>  <br/> |
|<span data-ttu-id="effc8-434">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="effc8-434">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="effc8-435">Файл был удален в середине операции.</span><span class="sxs-lookup"><span data-stu-id="effc8-435">The file was deleted in mid-operation.</span></span>  <br/> |
|<span data-ttu-id="effc8-436">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="effc8-436">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="effc8-437">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="effc8-437">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="effc8-438">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="effc8-438">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="effc8-439">Данный fileSystemPath не находится в корне каталога, указанном FileSystemDirectoryHint при вызове инициализации.</span><span class="sxs-lookup"><span data-stu-id="effc8-439">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="effc8-440">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="effc8-440">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="effc8-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="effc8-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="effc8-442">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="effc8-442">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="effc8-443">Файл, указанный  _bstrResourceID,_ имеет файл FileSystemPath, который отличается от указанного.</span><span class="sxs-lookup"><span data-stu-id="effc8-443">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="effc8-444">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="effc8-444">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="effc8-445">Указанный файл уже имеет ожидающих изменений в другом кэше и еще не может быть связан с кэшом потребителя.</span><span class="sxs-lookup"><span data-stu-id="effc8-445">The specified file already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="effc8-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="effc8-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="effc8-447">Предоставленный WebPath попадает в другой кэш.</span><span class="sxs-lookup"><span data-stu-id="effc8-447">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="effc8-448">S_OK</span><span class="sxs-lookup"><span data-stu-id="effc8-448">S_OK</span></span>  <br/> |<span data-ttu-id="effc8-449">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="effc8-449">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a><span data-ttu-id="effc8-450">ILSCLocalSyncClient::SetClientConnectivityState</span><span class="sxs-lookup"><span data-stu-id="effc8-450">ILSCLocalSyncClient::SetClientConnectivityState</span></span>
<span data-ttu-id="effc8-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="effc8-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="effc8-452">Устанавливает кэш в сетевое или автономное состояние.</span><span class="sxs-lookup"><span data-stu-id="effc8-452">Sets the cache into an online or offline state.</span></span> <span data-ttu-id="effc8-453">В автономном режиме Office не будет пытаться связаться с сервером для файлов в этом кэше, независимо от настроек  _fBlockUploads_ каждого отдельного файла.</span><span class="sxs-lookup"><span data-stu-id="effc8-453">If offline, Office will not attempt to communicate with the server for any files in that cache, regardless of each individual file's  _fBlockUploads_ setting.</span></span> 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a><span data-ttu-id="effc8-454">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-454">Parameters</span></span>

 <span data-ttu-id="effc8-455">_fIsOnline_</span><span class="sxs-lookup"><span data-stu-id="effc8-455">_fIsOnline_</span></span>
  
<span data-ttu-id="effc8-456">Boolean, определяющее состояние подключения кэша.</span><span class="sxs-lookup"><span data-stu-id="effc8-456">A boolean determining the connectivity state of the cache.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="effc8-457">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-457">Return values</span></span>

|<span data-ttu-id="effc8-458">Значение</span><span class="sxs-lookup"><span data-stu-id="effc8-458">Value</span></span>|<span data-ttu-id="effc8-459">Описание</span><span class="sxs-lookup"><span data-stu-id="effc8-459">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="effc8-460">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="effc8-460">E_FAIL</span></span>  <br/> |<span data-ttu-id="effc8-461">Сбой при настройках состояния подключения к кэше.</span><span class="sxs-lookup"><span data-stu-id="effc8-461">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="effc8-462">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="effc8-462">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="effc8-463">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="effc8-463">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="effc8-464">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="effc8-464">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="effc8-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="effc8-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="effc8-466">S_OK</span><span class="sxs-lookup"><span data-stu-id="effc8-466">S_OK</span></span>  <br/> |<span data-ttu-id="effc8-467">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="effc8-467">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a><span data-ttu-id="effc8-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="effc8-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span></span>
<span data-ttu-id="effc8-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="effc8-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="effc8-470">SetClientNetworkSyncPermission используется для переопределения или восстановления синхронизированной heuristicsOffice для затрат на сеть и использования питания.</span><span class="sxs-lookup"><span data-stu-id="effc8-470">SetClientNetworkSyncPermission is used to either override or restoreOffice's synchronizing heuristics for network cost and power usage.</span></span> <span data-ttu-id="effc8-471">Если в сети с высокой стоимостью 3G или в сети с высокой стоимостью либо при работе от аккумулятора или при подключении к сети, Office может заблокировать сетевой трафик до более непрозраченного времени.</span><span class="sxs-lookup"><span data-stu-id="effc8-471">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span> <span data-ttu-id="effc8-472">Потребитель этого API может использовать его для переопределения ауристических действий Office и принудительной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="effc8-472">The consumer of this API can use it to override Office's heuristics and force synchronizing to occur.</span></span>
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a><span data-ttu-id="effc8-473">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-473">Parameters</span></span>

 <span data-ttu-id="effc8-474">_nspType_</span><span class="sxs-lookup"><span data-stu-id="effc8-474">_nspType_</span></span>
  
<span data-ttu-id="effc8-475">Флаг, который определяет, какие затраты переопределять.</span><span class="sxs-lookup"><span data-stu-id="effc8-475">A flag which defines which cost heuristic to override.</span></span> <span data-ttu-id="effc8-476">См. [enum LSCNetworkSyncPermissionType.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType)</span><span class="sxs-lookup"><span data-stu-id="effc8-476">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span>
  
 <span data-ttu-id="effc8-477">_fEnableSync_</span><span class="sxs-lookup"><span data-stu-id="effc8-477">_fEnableSync_</span></span>
  
<span data-ttu-id="effc8-478">Указывает, следует ли принудительно синхронизироваться, переопределив эту ауристическую стоимость, или больше не переопределять ее.</span><span class="sxs-lookup"><span data-stu-id="effc8-478">Specifies whether to force synchronizing on, thus overriding that cost heuristic, or to no longer override it.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="effc8-479">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-479">Return values</span></span>

|<span data-ttu-id="effc8-480">Значение</span><span class="sxs-lookup"><span data-stu-id="effc8-480">Value</span></span>|<span data-ttu-id="effc8-481">Описание</span><span class="sxs-lookup"><span data-stu-id="effc8-481">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="effc8-482">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="effc8-482">E_FAIL</span></span>  <br/> |<span data-ttu-id="effc8-483">Невыполнение переопределения синхронизации с ауристией.</span><span class="sxs-lookup"><span data-stu-id="effc8-483">Failure to override synchronizing heuristics.</span></span>  <br/> |
|<span data-ttu-id="effc8-484">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="effc8-484">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="effc8-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="effc8-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="effc8-486">S_OK</span><span class="sxs-lookup"><span data-stu-id="effc8-486">S_OK</span></span>  <br/> |<span data-ttu-id="effc8-487">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="effc8-487">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a><span data-ttu-id="effc8-488">ILSCLocalSyncClient::Uninitialize</span><span class="sxs-lookup"><span data-stu-id="effc8-488">ILSCLocalSyncClient::Uninitialize</span></span>
<span data-ttu-id="effc8-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span><span class="sxs-lookup"><span data-stu-id="effc8-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span></span>

<span data-ttu-id="effc8-490">Выгружает кэш из объекта COM и выполняет операции закрытия.</span><span class="sxs-lookup"><span data-stu-id="effc8-490">Unloads the cache from the COM object and perform closing operations.</span></span> <span data-ttu-id="effc8-491">[ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) ДОЛЖЕН быть вызван перед уничтожением com-объекта.</span><span class="sxs-lookup"><span data-stu-id="effc8-491">[ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUST be called before destroying the COM object.</span></span> <span data-ttu-id="effc8-492">После этого никакие другие API не могут быть вызваны, com-объект ДОЛЖЕН быть уничтожен и создан новый, если вы хотите продолжить работу.</span><span class="sxs-lookup"><span data-stu-id="effc8-492">Once called, no other APIs can be called, the COM object MUST be destroyed and a new one created if you wish to continue operations.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a><span data-ttu-id="effc8-493">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-493">Parameters</span></span>

<span data-ttu-id="effc8-494">Нет.</span><span class="sxs-lookup"><span data-stu-id="effc8-494">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="effc8-495">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-495">Return values</span></span>

|<span data-ttu-id="effc8-496">Значение</span><span class="sxs-lookup"><span data-stu-id="effc8-496">Value</span></span>|<span data-ttu-id="effc8-497">Описание</span><span class="sxs-lookup"><span data-stu-id="effc8-497">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="effc8-498">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="effc8-498">E_FAIL</span></span>  <br/> |<span data-ttu-id="effc8-499">Сбой uninitialize.</span><span class="sxs-lookup"><span data-stu-id="effc8-499">Failure to uninitialize.</span></span>  <br/> |
|<span data-ttu-id="effc8-500">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="effc8-500">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="effc8-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="effc8-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="effc8-502">S_OK</span><span class="sxs-lookup"><span data-stu-id="effc8-502">S_OK</span></span>  <br/> |<span data-ttu-id="effc8-503">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="effc8-503">The call succeeded.</span></span>  <br/> |
   
### <a name="interface-ienumlscevent"></a><span data-ttu-id="effc8-504">Интерфейс IEnumLSCEvent</span><span class="sxs-lookup"><span data-stu-id="effc8-504">Interface IEnumLSCEvent</span></span>

<span data-ttu-id="effc8-505">Этот интерфейс представляет список событий ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="effc8-505">This interface represents a list of ILSCEvent events.</span></span>
  
<span data-ttu-id="effc8-506">**Функции открытых членов**</span><span class="sxs-lookup"><span data-stu-id="effc8-506">**Public member functions**</span></span>

#### <a name="ienumlsceventfnext"></a><span data-ttu-id="effc8-507">IEnumLSCEvent::FNext</span><span class="sxs-lookup"><span data-stu-id="effc8-507">IEnumLSCEvent::FNext</span></span>

<span data-ttu-id="effc8-508">Извлекает следующее событие из списка событий.</span><span class="sxs-lookup"><span data-stu-id="effc8-508">Retrieves the next event from the list of events.</span></span>
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a><span data-ttu-id="effc8-509">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-509">Parameters</span></span>

 <span data-ttu-id="effc8-510">_ppiLSCEvent_</span><span class="sxs-lookup"><span data-stu-id="effc8-510">_ppiLSCEvent_</span></span>
  
<span data-ttu-id="effc8-511">Указатель на интерфейс ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="effc8-511">A pointer to an ILSCEvent interface.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="effc8-512">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-512">Return values</span></span>

|<span data-ttu-id="effc8-513">Значение</span><span class="sxs-lookup"><span data-stu-id="effc8-513">Value</span></span>|<span data-ttu-id="effc8-514">Описание</span><span class="sxs-lookup"><span data-stu-id="effc8-514">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="effc8-515">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="effc8-515">E_FAIL</span></span>  <br/> |<span data-ttu-id="effc8-516">Больше нет событий.</span><span class="sxs-lookup"><span data-stu-id="effc8-516">There are no more events.</span></span>  <br/> |
|<span data-ttu-id="effc8-517">S_OK</span><span class="sxs-lookup"><span data-stu-id="effc8-517">S_OK</span></span>  <br/> |<span data-ttu-id="effc8-518">Вызов был успешным.</span><span class="sxs-lookup"><span data-stu-id="effc8-518">The call was successful.</span></span>  <br/> |
   
#### <a name="ienumlsceventreset"></a><span data-ttu-id="effc8-519">IEnumLSCEvent::Reset</span><span class="sxs-lookup"><span data-stu-id="effc8-519">IEnumLSCEvent::Reset</span></span>

<span data-ttu-id="effc8-520">Сбрасывает enumerator до первого события.</span><span class="sxs-lookup"><span data-stu-id="effc8-520">Resets the enumerator to the first event.</span></span>
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a><span data-ttu-id="effc8-521">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-521">Parameters</span></span>

<span data-ttu-id="effc8-522">Нет.</span><span class="sxs-lookup"><span data-stu-id="effc8-522">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="effc8-523">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-523">Return values</span></span>

<span data-ttu-id="effc8-524">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="effc8-524">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent"></a><span data-ttu-id="effc8-525">Интерфейс ILSCEvent</span><span class="sxs-lookup"><span data-stu-id="effc8-525">Interface ILSCEvent</span></span>

<span data-ttu-id="effc8-526">Этот интерфейс представляет событие синхронизации.</span><span class="sxs-lookup"><span data-stu-id="effc8-526">This interface represents a synchronizing event.</span></span> <span data-ttu-id="effc8-527">Все сведения о событии можно получить из интерфейса.</span><span class="sxs-lookup"><span data-stu-id="effc8-527">All information about the event can be retrieved from the interface.</span></span>
  
<span data-ttu-id="effc8-528">**Функции открытых членов**</span><span class="sxs-lookup"><span data-stu-id="effc8-528">**Public member functions**</span></span>

#### <a name="ilsceventgetconflictstatus"></a><span data-ttu-id="effc8-529">ILSCEvent::GetConflictStatus</span><span class="sxs-lookup"><span data-stu-id="effc8-529">ILSCEvent::GetConflictStatus</span></span>

<span data-ttu-id="effc8-530">Обратите внимание, что это значение заполняется при вызвании [ILSCLocalSyncClient::GetChanges, ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) а не при его добавлении, поэтому при смене состояния конфликта у вас будет только текущее состояние файла, а не его состояние.</span><span class="sxs-lookup"><span data-stu-id="effc8-530">Note that this value is populated when [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) is called, not when the event was created, so you will only have the current status of the file, not the status of the file when the conflict status changed.</span></span> 
  
<span data-ttu-id="effc8-531">Это значение заполняется, только если значение [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnLocalConflictStateChanged.</span><span class="sxs-lookup"><span data-stu-id="effc8-531">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnLocalConflictStateChanged.</span></span> 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a><span data-ttu-id="effc8-532">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-532">Parameters</span></span>

 <span data-ttu-id="effc8-533">_pfIsInConflict_</span><span class="sxs-lookup"><span data-stu-id="effc8-533">_pfIsInConflict_</span></span>
  
<span data-ttu-id="effc8-534">Текущее состояние конфликта файла, связанного с событием.</span><span class="sxs-lookup"><span data-stu-id="effc8-534">The current conflict status of the file associated with the event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="effc8-535">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-535">Return values</span></span>

<span data-ttu-id="effc8-536">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="effc8-536">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeterror"></a><span data-ttu-id="effc8-537">ILSCEvent::GetError</span><span class="sxs-lookup"><span data-stu-id="effc8-537">ILSCEvent::GetError</span></span>

<span data-ttu-id="effc8-538">Это значение заполняется, только если значение [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="effc8-538">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a><span data-ttu-id="effc8-539">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-539">Parameters</span></span>

 <span data-ttu-id="effc8-540">_pnError_</span><span class="sxs-lookup"><span data-stu-id="effc8-540">_pnError_</span></span>
  
<span data-ttu-id="effc8-541">Ошибка, связанная с этим событием.</span><span class="sxs-lookup"><span data-stu-id="effc8-541">The error associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="effc8-542">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-542">Return values</span></span>

<span data-ttu-id="effc8-543">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="effc8-543">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetetag"></a><span data-ttu-id="effc8-544">ILSCEvent::GetETag</span><span class="sxs-lookup"><span data-stu-id="effc8-544">ILSCEvent::GetETag</span></span>

<span data-ttu-id="effc8-545">Это значение заполняется, только если значение [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="effc8-545">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a><span data-ttu-id="effc8-546">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-546">Parameters</span></span>

 <span data-ttu-id="effc8-547">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="effc8-547">_pbstrETag_</span></span>
  
<span data-ttu-id="effc8-548">ETag, связанный с этим событием</span><span class="sxs-lookup"><span data-stu-id="effc8-548">The ETag associated with this event</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="effc8-549">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-549">Return values</span></span>

<span data-ttu-id="effc8-550">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="effc8-550">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeteventtype"></a><span data-ttu-id="effc8-551">ILSCEvent::GetEventType</span><span class="sxs-lookup"><span data-stu-id="effc8-551">ILSCEvent::GetEventType</span></span>

<span data-ttu-id="effc8-552">Получает тип для этого события.</span><span class="sxs-lookup"><span data-stu-id="effc8-552">Gets the type for this event.</span></span>
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a><span data-ttu-id="effc8-553">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-553">Parameters</span></span>

 <span data-ttu-id="effc8-554">_pnEventType_</span><span class="sxs-lookup"><span data-stu-id="effc8-554">_pnEventType_</span></span>
  
<span data-ttu-id="effc8-555">Тип события этого события.</span><span class="sxs-lookup"><span data-stu-id="effc8-555">The event type of this event.</span></span> <span data-ttu-id="effc8-556">Допустимые значения см. в [enum LSCEventType.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType)</span><span class="sxs-lookup"><span data-stu-id="effc8-556">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for valid values.</span></span> <span data-ttu-id="effc8-557">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="effc8-557">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="effc8-558">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-558">Return values</span></span>

|<span data-ttu-id="effc8-559">Значение</span><span class="sxs-lookup"><span data-stu-id="effc8-559">Value</span></span>|<span data-ttu-id="effc8-560">Описание</span><span class="sxs-lookup"><span data-stu-id="effc8-560">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="effc8-561">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="effc8-561">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="effc8-562">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="effc8-562">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="effc8-563">S_OK</span><span class="sxs-lookup"><span data-stu-id="effc8-563">S_OK</span></span>  <br/> |<span data-ttu-id="effc8-564">Вызов был успешным.</span><span class="sxs-lookup"><span data-stu-id="effc8-564">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a><span data-ttu-id="effc8-565">ILSCEvent::GetLocalWorkingPath</span><span class="sxs-lookup"><span data-stu-id="effc8-565">ILSCEvent::GetLocalWorkingPath</span></span>

<span data-ttu-id="effc8-566">Получает локальный рабочий путь для этого события.</span><span class="sxs-lookup"><span data-stu-id="effc8-566">Gets the local working path for this event.</span></span>
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a><span data-ttu-id="effc8-567">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-567">Parameters</span></span>

 <span data-ttu-id="effc8-568">_pbstrLocalWorkingPath_</span><span class="sxs-lookup"><span data-stu-id="effc8-568">_pbstrLocalWorkingPath_</span></span>
  
<span data-ttu-id="effc8-569">Локальный путь к файлу, к которому относится это событие.</span><span class="sxs-lookup"><span data-stu-id="effc8-569">The local path of the file to which this event pertains.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="effc8-570">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-570">Return values</span></span>

<span data-ttu-id="effc8-571">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="effc8-571">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceid"></a><span data-ttu-id="effc8-572">ILSCEvent::GetResourceID</span><span class="sxs-lookup"><span data-stu-id="effc8-572">ILSCEvent::GetResourceID</span></span>

<span data-ttu-id="effc8-573">Получает ИД ресурса для события.</span><span class="sxs-lookup"><span data-stu-id="effc8-573">Gets the resource ID for the event.</span></span>
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="effc8-574">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-574">Parameters</span></span>

 <span data-ttu-id="effc8-575">_pbstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="effc8-575">_pbstrResourceID_</span></span>
  
<span data-ttu-id="effc8-576">ResourceID файла, связанного с этим событием.</span><span class="sxs-lookup"><span data-stu-id="effc8-576">The ResourceID of the file associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="effc8-577">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-577">Return values</span></span>

<span data-ttu-id="effc8-578">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="effc8-578">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceidattempted"></a><span data-ttu-id="effc8-579">ILSCEvent::GetResourceIDAttempted</span><span class="sxs-lookup"><span data-stu-id="effc8-579">ILSCEvent::GetResourceIDAttempted</span></span>

<span data-ttu-id="effc8-580">Это значение заполняется, только если значение [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="effc8-580">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> <span data-ttu-id="effc8-581">Когда вызов [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)или [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) приведет к конфликту веб-пути или локального пути с другим файлом в кэше файлов Office, создается это событие.</span><span class="sxs-lookup"><span data-stu-id="effc8-581">When a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) would cause a Web Path or Local Path collision with another file in the Office file cache, this event is generated.</span></span> 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a><span data-ttu-id="effc8-582">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-582">Parameters</span></span>

 <span data-ttu-id="effc8-583">_pbstrResourceIDAttempted_</span><span class="sxs-lookup"><span data-stu-id="effc8-583">_pbstrResourceIDAttempted_</span></span>
  
<span data-ttu-id="effc8-584">ResourceID, который вызвал это событие для получения.</span><span class="sxs-lookup"><span data-stu-id="effc8-584">The ResourceID that caused this event to get generated.</span></span> <span data-ttu-id="effc8-585">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="effc8-585">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="effc8-586">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-586">Return values</span></span>

<span data-ttu-id="effc8-587">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="effc8-587">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetsyncerrortype"></a><span data-ttu-id="effc8-588">ILSCEvent::GetSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="effc8-588">ILSCEvent::GetSyncErrorType</span></span>

<span data-ttu-id="effc8-589">Это значение заполняется, только если значение [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="effc8-589">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a><span data-ttu-id="effc8-590">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-590">Parameters</span></span>

 <span data-ttu-id="effc8-591">_pnSyncErrorType_</span><span class="sxs-lookup"><span data-stu-id="effc8-591">_pnSyncErrorType_</span></span>
  
<span data-ttu-id="effc8-592">Тип ошибки, связанный с этим событием.</span><span class="sxs-lookup"><span data-stu-id="effc8-592">The error type associated with this event.</span></span> <span data-ttu-id="effc8-593">Возможные значения см. в [enum LSCEventType.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType)</span><span class="sxs-lookup"><span data-stu-id="effc8-593">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for potential values.</span></span> <span data-ttu-id="effc8-594">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="effc8-594">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="effc8-595">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-595">Return values</span></span>

|<span data-ttu-id="effc8-596">Значение</span><span class="sxs-lookup"><span data-stu-id="effc8-596">Value</span></span>|<span data-ttu-id="effc8-597">Описание</span><span class="sxs-lookup"><span data-stu-id="effc8-597">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="effc8-598">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="effc8-598">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="effc8-599">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="effc8-599">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="effc8-600">S_OK</span><span class="sxs-lookup"><span data-stu-id="effc8-600">S_OK</span></span>  <br/> |<span data-ttu-id="effc8-601">Вызов был успешным.</span><span class="sxs-lookup"><span data-stu-id="effc8-601">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetwebpath"></a><span data-ttu-id="effc8-602">ILSCEvent::GetWebPath</span><span class="sxs-lookup"><span data-stu-id="effc8-602">ILSCEvent::GetWebPath</span></span>

<span data-ttu-id="effc8-603">Это значение заполняется, только если значение [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="effc8-603">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a><span data-ttu-id="effc8-604">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-604">Parameters</span></span>

 <span data-ttu-id="effc8-605">_pbstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="effc8-605">_pbstrWebPath_</span></span>
  
<span data-ttu-id="effc8-606">Указывает веб-путь, связанный с этим событием.</span><span class="sxs-lookup"><span data-stu-id="effc8-606">Specifies the Web Path associated with this event.</span></span> <span data-ttu-id="effc8-607">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="effc8-607">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="effc8-608">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-608">Return values</span></span>

<span data-ttu-id="effc8-609">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="effc8-609">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent2"></a><span data-ttu-id="effc8-610">Интерфейс ILSCEvent2</span><span class="sxs-lookup"><span data-stu-id="effc8-610">Interface ILSCEvent2</span></span>

<span data-ttu-id="effc8-611">Этот интерфейс содержит дополнительные сведения о событии синхронизации.</span><span class="sxs-lookup"><span data-stu-id="effc8-611">This interface holds additional information about a synchronizing event.</span></span>
  
<span data-ttu-id="effc8-612">**Функции открытых членов**</span><span class="sxs-lookup"><span data-stu-id="effc8-612">**Public member functions**</span></span>

#### <a name="ilscevent2geterrorchain"></a><span data-ttu-id="effc8-613">ILSCEvent2::GetErrorChain</span><span class="sxs-lookup"><span data-stu-id="effc8-613">ILSCEvent2::GetErrorChain</span></span>

<span data-ttu-id="effc8-614">Получает сведения о цепочке ошибок о событии синхронизации.</span><span class="sxs-lookup"><span data-stu-id="effc8-614">Gets the error chain information about a synchronizing event.</span></span>
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a><span data-ttu-id="effc8-615">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-615">Parameters</span></span>

 <span data-ttu-id="effc8-616">_pbstrErrorChain_</span><span class="sxs-lookup"><span data-stu-id="effc8-616">_pbstrErrorChain_</span></span>
  
<span data-ttu-id="effc8-617">Строка для удержания сведений о цепочке ошибок.</span><span class="sxs-lookup"><span data-stu-id="effc8-617">A string to hold the error chain information.</span></span> <span data-ttu-id="effc8-618">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="effc8-618">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="effc8-619">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-619">Return values</span></span>

|<span data-ttu-id="effc8-620">Значение</span><span class="sxs-lookup"><span data-stu-id="effc8-620">Value</span></span>|<span data-ttu-id="effc8-621">Описание</span><span class="sxs-lookup"><span data-stu-id="effc8-621">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="effc8-622">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="effc8-622">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="effc8-623">Установленная версия Office не поддерживает этот интерфейс</span><span class="sxs-lookup"><span data-stu-id="effc8-623">The installed version of Office does not support this interface</span></span>  <br/> |
|<span data-ttu-id="effc8-624">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="effc8-624">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="effc8-625">Одно или несколько значений параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="effc8-625">One or more of the parameter values are invalid.</span></span>  <br/> |
|<span data-ttu-id="effc8-626">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="effc8-626">E_FAIL</span></span>  <br/> |<span data-ttu-id="effc8-627">Сведения о цепочке ошибок недоступны.</span><span class="sxs-lookup"><span data-stu-id="effc8-627">The error chain information is not available.</span></span>  <br/> |
|<span data-ttu-id="effc8-628">S_OK</span><span class="sxs-lookup"><span data-stu-id="effc8-628">S_OK</span></span>  <br/> |<span data-ttu-id="effc8-629">Вызов был успешным.</span><span class="sxs-lookup"><span data-stu-id="effc8-629">The call was successful.</span></span>  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a><span data-ttu-id="effc8-630">Интерфейс IPartnerActivityCallback</span><span class="sxs-lookup"><span data-stu-id="effc8-630">Interface IPartnerActivityCallback</span></span>

<span data-ttu-id="effc8-631">Этот интерфейс предоставляет функцию вызова объекту COM CSISyncClient.</span><span class="sxs-lookup"><span data-stu-id="effc8-631">This interface provides a callback function to the CSISyncClient COM object.</span></span>
  
<span data-ttu-id="effc8-632">**Функции открытых членов**</span><span class="sxs-lookup"><span data-stu-id="effc8-632">**Public member functions**</span></span>

#### <a name="ipartneractivitycallbackeventoccurred"></a><span data-ttu-id="effc8-633">IPartnerActivityCallback::EventOccurred</span><span class="sxs-lookup"><span data-stu-id="effc8-633">IPartnerActivityCallback::EventOccurred</span></span>

<span data-ttu-id="effc8-634">Это функция вызова для объекта, заданного объекту CsiSyncClient COM.</span><span class="sxs-lookup"><span data-stu-id="effc8-634">This is a callback function on the object given to the CsiSyncClient COM object.</span></span> <span data-ttu-id="effc8-635">Ожидается, что при событии (см. [enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) для допустимых типов событий) COM-объект CsiSyncClient будет вызывать этот метод, сигнализировать потребителя.</span><span class="sxs-lookup"><span data-stu-id="effc8-635">It's expected that when an Event occurs (see [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid event types), the CsiSyncClient COM object will call this method, signalling the consumer.</span></span> 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a><span data-ttu-id="effc8-636">Параметры</span><span class="sxs-lookup"><span data-stu-id="effc8-636">Parameters</span></span>

 <span data-ttu-id="effc8-637">_eEventTypeOccurred_</span><span class="sxs-lookup"><span data-stu-id="effc8-637">_eEventTypeOccurred_</span></span>
  
<span data-ttu-id="effc8-638">Тип события этого события.</span><span class="sxs-lookup"><span data-stu-id="effc8-638">The event type of this event.</span></span> <span data-ttu-id="effc8-639">Допустимые значения см. в [enum LSCEventTypeOccurred.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred)</span><span class="sxs-lookup"><span data-stu-id="effc8-639">See [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid values.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="effc8-640">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="effc8-640">Return values</span></span>

<span data-ttu-id="effc8-641">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="effc8-641">Always returns S_OK.</span></span>
  
## <a name="enumerations"></a><span data-ttu-id="effc8-642">Перечисления</span><span class="sxs-lookup"><span data-stu-id="effc8-642">Enumerations</span></span>

<span data-ttu-id="effc8-643">CSISyncClient использует следующие enumerations.</span><span class="sxs-lookup"><span data-stu-id="effc8-643">CSISyncClient uses the following enumerations.</span></span>
  
### <a name="enum-lsceventsyncerrortype"></a><span data-ttu-id="effc8-644">Enum LSCEventSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="effc8-644">Enum LSCEventSyncErrorType</span></span>
<span data-ttu-id="effc8-645"><a name="Enum_LSCEventSyncErrorType"> </a></span><span class="sxs-lookup"><span data-stu-id="effc8-645"><a name="Enum_LSCEventSyncErrorType"> </a></span></span>

<span data-ttu-id="effc8-646">Это enumeration указывает категории ошибок, которые могут возникнуть при синхронизации файла.</span><span class="sxs-lookup"><span data-stu-id="effc8-646">This enumeration specifies the categories of errors that can occur while synchronizing a file.</span></span>
  
|<span data-ttu-id="effc8-647">Enumerator</span><span class="sxs-lookup"><span data-stu-id="effc8-647">Enumerator</span></span>|<span data-ttu-id="effc8-648">Описание</span><span class="sxs-lookup"><span data-stu-id="effc8-648">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="effc8-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span><span class="sxs-lookup"><span data-stu-id="effc8-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span></span>  <br/> |<span data-ttu-id="effc8-650">Ошибка синхронизации этого события была непредвиденная и может потребовать особого внимания.</span><span class="sxs-lookup"><span data-stu-id="effc8-650">The synchronizing error of this event was unexpected, and may require special consideration.</span></span> <span data-ttu-id="effc8-651">По умолчанию пользователю может потребоваться вмешательство.</span><span class="sxs-lookup"><span data-stu-id="effc8-651">By default, the user may have to intervene.</span></span>  <br/> |
|<span data-ttu-id="effc8-652">LSCEventSyncErrorType_NoInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="effc8-652">LSCEventSyncErrorType_NoInterventionRequired</span></span>  <br/> |<span data-ttu-id="effc8-653">Ошибка синхронизации этого события не требует особого внимания.</span><span class="sxs-lookup"><span data-stu-id="effc8-653">The synchronizing error of this event does not need special consideration.</span></span> <span data-ttu-id="effc8-654">Office будет обрабатывать его автоматически.</span><span class="sxs-lookup"><span data-stu-id="effc8-654">Office will handle it automatically.</span></span>  <br/> |
|<span data-ttu-id="effc8-655">LSCEventSyncErrorType_UserInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="effc8-655">LSCEventSyncErrorType_UserInterventionRequired</span></span>  <br/> |<span data-ttu-id="effc8-656">Ошибка синхронизации этого события требует от пользователя ее устранения.</span><span class="sxs-lookup"><span data-stu-id="effc8-656">The synchronizing error of this event requires a user to resolve it.</span></span> <span data-ttu-id="effc8-657">Например, при объединении с конфликтом пользователь должен открыть документ и объединить его.</span><span class="sxs-lookup"><span data-stu-id="effc8-657">For example, merge conflict error requires a user to open the document and merge it.</span></span>  <br/> |
|<span data-ttu-id="effc8-658">LSCEventSyncErrorType_WaitingOnClient</span><span class="sxs-lookup"><span data-stu-id="effc8-658">LSCEventSyncErrorType_WaitingOnClient</span></span>  <br/> |<span data-ttu-id="effc8-659">Ошибка синхронизации этого события требует вмешательства потребителя, но не требует особого внимания пользователя.</span><span class="sxs-lookup"><span data-stu-id="effc8-659">The synchronizing error of this event requires the consumer to intervene, but should not require special consideration by the user.</span></span>  <br/> |
|<span data-ttu-id="effc8-660">LSCEventSyncErrorType_ClientInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="effc8-660">LSCEventSyncErrorType_ClientInterventionRequired</span></span>  <br/> |<span data-ttu-id="effc8-661">Ошибка синхронизации этого события требует, чтобы потребитель вступил в особый случай.</span><span class="sxs-lookup"><span data-stu-id="effc8-661">The synchronizing error of this event requires the consumer to intervene as a special case.</span></span>  <br/> |
|<span data-ttu-id="effc8-662">LSCEventSyncErrorType_Max</span><span class="sxs-lookup"><span data-stu-id="effc8-662">LSCEventSyncErrorType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtype"></a><span data-ttu-id="effc8-663">Enum LSCEventType</span><span class="sxs-lookup"><span data-stu-id="effc8-663">Enum LSCEventType</span></span>
<span data-ttu-id="effc8-664"><a name="Enum_LSCEventType"> </a></span><span class="sxs-lookup"><span data-stu-id="effc8-664"><a name="Enum_LSCEventType"> </a></span></span>

<span data-ttu-id="effc8-665">Это значение указывает тип событий, которые могут произойти для конкретного файла.</span><span class="sxs-lookup"><span data-stu-id="effc8-665">This enumeration specifies the type of events that can occur for a particular file.</span></span>
  
|<span data-ttu-id="effc8-666">Enumerator</span><span class="sxs-lookup"><span data-stu-id="effc8-666">Enumerator</span></span>|<span data-ttu-id="effc8-667">Описание</span><span class="sxs-lookup"><span data-stu-id="effc8-667">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="effc8-668">LSCEventType_None</span><span class="sxs-lookup"><span data-stu-id="effc8-668">LSCEventType_None</span></span>  <br/> ||
|<span data-ttu-id="effc8-669">LSCEventType_OnLocalChanges</span><span class="sxs-lookup"><span data-stu-id="effc8-669">LSCEventType_OnLocalChanges</span></span>  <br/> |<span data-ttu-id="effc8-670">В локальный файл были внесены изменения.</span><span class="sxs-lookup"><span data-stu-id="effc8-670">Changes were made to a local file.</span></span>  <br/> |
|<span data-ttu-id="effc8-671">LSCEventType_OnOpenedByUser</span><span class="sxs-lookup"><span data-stu-id="effc8-671">LSCEventType_OnOpenedByUser</span></span>  <br/> |<span data-ttu-id="effc8-672">Пользователь открыл файл.</span><span class="sxs-lookup"><span data-stu-id="effc8-672">A user opened a file.</span></span>  <br/> |
|<span data-ttu-id="effc8-673">LSCEventType_OnServerChangesDownloaded</span><span class="sxs-lookup"><span data-stu-id="effc8-673">LSCEventType_OnServerChangesDownloaded</span></span>  <br/> |<span data-ttu-id="effc8-674">Загрузка изменений файлов с сервера завершена.</span><span class="sxs-lookup"><span data-stu-id="effc8-674">Finished downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="effc8-675">LSCEventType_OnLocalChangesUploaded</span><span class="sxs-lookup"><span data-stu-id="effc8-675">LSCEventType_OnLocalChangesUploaded</span></span>  <br/> |<span data-ttu-id="effc8-676">Отправка изменений файлов на сервер завершена.</span><span class="sxs-lookup"><span data-stu-id="effc8-676">Finished uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="effc8-677">LSCEventType_OnLocalConflictStateChanged</span><span class="sxs-lookup"><span data-stu-id="effc8-677">LSCEventType_OnLocalConflictStateChanged</span></span>  <br/> |<span data-ttu-id="effc8-678">Состояние конфликта объединения файла изменилось.</span><span class="sxs-lookup"><span data-stu-id="effc8-678">The merge conflict state of a file has changed.</span></span>  <br/> |
|<span data-ttu-id="effc8-679">LSCEventType_OnFileAdded</span><span class="sxs-lookup"><span data-stu-id="effc8-679">LSCEventType_OnFileAdded</span></span>  <br/> |<span data-ttu-id="effc8-680">Добавлен файл.</span><span class="sxs-lookup"><span data-stu-id="effc8-680">A file was added.</span></span>  <br/> |
|<span data-ttu-id="effc8-681">LSCEventType_OnFileDeleted</span><span class="sxs-lookup"><span data-stu-id="effc8-681">LSCEventType_OnFileDeleted</span></span>  <br/> |<span data-ttu-id="effc8-682">Файл был удален.</span><span class="sxs-lookup"><span data-stu-id="effc8-682">A file was deleted.</span></span>  <br/> |
|<span data-ttu-id="effc8-683">LSCEventType_OnSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="effc8-683">LSCEventType_OnSyncEnabled</span></span>  <br/> |<span data-ttu-id="effc8-684">Синхронизация включена для файлов пользователя.</span><span class="sxs-lookup"><span data-stu-id="effc8-684">Synchronizing was enabled for a user's files.</span></span>  <br/> |
|<span data-ttu-id="effc8-685">LSCEventType_OnServerChangesDownloadStarted</span><span class="sxs-lookup"><span data-stu-id="effc8-685">LSCEventType_OnServerChangesDownloadStarted</span></span>  <br/> |<span data-ttu-id="effc8-686">Начал скачивать изменения файлов с сервера.</span><span class="sxs-lookup"><span data-stu-id="effc8-686">Started downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="effc8-687">LSCEventType_OnLocalChangesUploadStarted</span><span class="sxs-lookup"><span data-stu-id="effc8-687">LSCEventType_OnLocalChangesUploadStarted</span></span>  <br/> |<span data-ttu-id="effc8-688">Началась отправка изменений файлов на сервер.</span><span class="sxs-lookup"><span data-stu-id="effc8-688">Started uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="effc8-689">LSCEventType_OnFilePathConflict</span><span class="sxs-lookup"><span data-stu-id="effc8-689">LSCEventType_OnFilePathConflict</span></span>  <br/> |<span data-ttu-id="effc8-690">Это событие создается, когда вызов [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)или [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) вызывает конфликт веб-пути или локального пути с другим файлом в кэше файлов Office.</span><span class="sxs-lookup"><span data-stu-id="effc8-690">This event is generated when a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) causes a Web Path or Local Path collision with another file in the Office file cache.</span></span>  <br/> |
|<span data-ttu-id="effc8-691">LSCEventType_OnFileForked</span><span class="sxs-lookup"><span data-stu-id="effc8-691">LSCEventType_OnFileForked</span></span>  <br/> ||
|<span data-ttu-id="effc8-692">LSCEventType_Max</span><span class="sxs-lookup"><span data-stu-id="effc8-692">LSCEventType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a><span data-ttu-id="effc8-693">Enum LSCEventTypeOccurred</span><span class="sxs-lookup"><span data-stu-id="effc8-693">Enum LSCEventTypeOccurred</span></span>
<span data-ttu-id="effc8-694"><a name="Enum_LSCEventTypeOccurred"> </a></span><span class="sxs-lookup"><span data-stu-id="effc8-694"><a name="Enum_LSCEventTypeOccurred"> </a></span></span>

<span data-ttu-id="effc8-695">Это enumeration указывает тип событий, которые могут произойти.</span><span class="sxs-lookup"><span data-stu-id="effc8-695">This enumeration specifies the type of events that can occur.</span></span> <span data-ttu-id="effc8-696">Потребителю необходимо вызывать определенные функции ILSCLocalSyncClient в зависимости от типа события.</span><span class="sxs-lookup"><span data-stu-id="effc8-696">The consumer needs to call specific ILSCLocalSyncClient functions based on the event type.</span></span>
  
|<span data-ttu-id="effc8-697">Enumerator</span><span class="sxs-lookup"><span data-stu-id="effc8-697">Enumerator</span></span>|<span data-ttu-id="effc8-698">Описание</span><span class="sxs-lookup"><span data-stu-id="effc8-698">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="effc8-699">LSCEventTypeOccurred_GetChanges</span><span class="sxs-lookup"><span data-stu-id="effc8-699">LSCEventTypeOccurred_GetChanges</span></span>  <br/> |<span data-ttu-id="effc8-700">Произошел ilSCEvent.</span><span class="sxs-lookup"><span data-stu-id="effc8-700">An ILSCEvent has occurred.</span></span> <span data-ttu-id="effc8-701">Потребитель должен вызвать [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) для получения данных.</span><span class="sxs-lookup"><span data-stu-id="effc8-701">The consumer should call [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) to retrieve the data.</span></span>  <br/> |
|<span data-ttu-id="effc8-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="effc8-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span></span>  <br/> |<span data-ttu-id="effc8-703">Поддерживаемые расширения файлов изменились.</span><span class="sxs-lookup"><span data-stu-id="effc8-703">The supported file extensions have changed.</span></span> <span data-ttu-id="effc8-704">Потребитель должен вызвать [ILSCLocalSyncClient::GetSupportedFileExtensions, ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) чтобы получить новый список поддерживаемых расширений.</span><span class="sxs-lookup"><span data-stu-id="effc8-704">The consumer should call [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) to retrieve the new list of supported extensions.</span></span>  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a><span data-ttu-id="effc8-705">Enum LSCNetworkSyncPermissionType</span><span class="sxs-lookup"><span data-stu-id="effc8-705">Enum LSCNetworkSyncPermissionType</span></span>
<span data-ttu-id="effc8-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span><span class="sxs-lookup"><span data-stu-id="effc8-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span></span>

<span data-ttu-id="effc8-707">Это enumeration specifies the flags used for a network cost heuristic.</span><span class="sxs-lookup"><span data-stu-id="effc8-707">This enumeration specifies the flags used for a network cost heuristic.</span></span> 

|<span data-ttu-id="effc8-708">Enumerator</span><span class="sxs-lookup"><span data-stu-id="effc8-708">Enumerator</span></span>|<span data-ttu-id="effc8-709">Описание</span><span class="sxs-lookup"><span data-stu-id="effc8-709">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="effc8-710">LSCNetworkSyncPermissionType_HighCost</span><span class="sxs-lookup"><span data-stu-id="effc8-710">LSCNetworkSyncPermissionType_HighCost</span></span>  <br/> |<span data-ttu-id="effc8-711">Имеет true, если переопределяется дорожная выгружаемая стоимость для дорогостоящих сетей (например, 3G).</span><span class="sxs-lookup"><span data-stu-id="effc8-711">True if the cost heuristic for expensive networks (such as 3G) is overridden.</span></span>  <br/> |
|<span data-ttu-id="effc8-712">LSCNetworkSyncPermissionType_HighPowerUsage</span><span class="sxs-lookup"><span data-stu-id="effc8-712">LSCNetworkSyncPermissionType_HighPowerUsage</span></span>  <br/> |<span data-ttu-id="effc8-713">Имеет true, если переопределяется побороть затраты на использование питания (например, аккумулятор).</span><span class="sxs-lookup"><span data-stu-id="effc8-713">True if the cost heuristic for power usage (such as a battery) is overridden.</span></span>  <br/> |
   
### <a name="enum-lscstatusflag"></a><span data-ttu-id="effc8-714">Enum LSCStatusFlag</span><span class="sxs-lookup"><span data-stu-id="effc8-714">Enum LSCStatusFlag</span></span>
<span data-ttu-id="effc8-715"><a name="Enum_LSCStatusFlag"> </a></span><span class="sxs-lookup"><span data-stu-id="effc8-715"><a name="Enum_LSCStatusFlag"> </a></span></span>

<span data-ttu-id="effc8-716">Это enumeration используется для представления состояния синхронизации файла.</span><span class="sxs-lookup"><span data-stu-id="effc8-716">This enumeration is used to represent the synchronize status of a file.</span></span> 
  
|<span data-ttu-id="effc8-717">Enumerator</span><span class="sxs-lookup"><span data-stu-id="effc8-717">Enumerator</span></span>|<span data-ttu-id="effc8-718">Описание</span><span class="sxs-lookup"><span data-stu-id="effc8-718">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="effc8-719">LCSStatusFlag_None</span><span class="sxs-lookup"><span data-stu-id="effc8-719">LCSStatusFlag_None</span></span>  <br/> ||
|<span data-ttu-id="effc8-720">LSCStatusFlag_UploadPending</span><span class="sxs-lookup"><span data-stu-id="effc8-720">LSCStatusFlag_UploadPending</span></span>  <br/> |<span data-ttu-id="effc8-721">Имеет true, если в файле сервера есть ожидающих данных.</span><span class="sxs-lookup"><span data-stu-id="effc8-721">True if there is pending data to send to the server file.</span></span>  <br/> |
|<span data-ttu-id="effc8-722">LSCStatusFlag_DownloadPending</span><span class="sxs-lookup"><span data-stu-id="effc8-722">LSCStatusFlag_DownloadPending</span></span>  <br/> |<span data-ttu-id="effc8-723">Имеет true, если есть ожидающих загрузки данных из файла сервера.</span><span class="sxs-lookup"><span data-stu-id="effc8-723">True if there is pending data to download from the server file.</span></span>  <br/> |
|<span data-ttu-id="effc8-724">LSCStatusFlag_LocalFileUnchanged</span><span class="sxs-lookup"><span data-stu-id="effc8-724">LSCStatusFlag_LocalFileUnchanged</span></span>  <br/> |<span data-ttu-id="effc8-725">Имеет true, если данные, хранимые в файле в кэше Office, — это самая новейшая копия данных на диске.</span><span class="sxs-lookup"><span data-stu-id="effc8-725">True if the data Office has on the file in its cache is the most recent copy of the data on disk.</span></span>  <br/> |
   

