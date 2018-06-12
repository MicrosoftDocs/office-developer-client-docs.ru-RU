---
title: Использование CSISyncClient для управления кэша документов Office (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Узнайте, как использовать CSISyncClient для управления кэша документов Office (ODC).
ms.openlocfilehash: adaa56bf040889bd8220506bcfab8fdb0b7ab6c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813109"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a><span data-ttu-id="60027-103">Использование CSISyncClient для управления кэша документов Office (ODC)</span><span class="sxs-lookup"><span data-stu-id="60027-103">Using CSISyncClient to control the Office Document Cache (ODC)</span></span>

<span data-ttu-id="60027-104">Узнайте, как использовать CSISyncClient для управления кэша документов Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="60027-104">Learn how to use CSISyncClient to control the Office Document Cache (ODC).</span></span>
  
<span data-ttu-id="60027-105">CSISyncClient является сервером COM ожидания proc (CsiSyncClient.exe), который позволяет Microsoft OneDrive для управления поведением кэша документов Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="60027-105">CSISyncClient is an out-of-proc COM server (CsiSyncClient.exe) that allows Microsoft OneDrive to control the behavior of the Office Document Cache (ODC).</span></span> <span data-ttu-id="60027-106">Например OneDrive могут вызывать ODC через CSISyncClient для загрузки файлов в и из конечных точек MS-FSSHTTP включено.</span><span class="sxs-lookup"><span data-stu-id="60027-106">For example, OneDrive may call upon the ODC via CSISyncClient to upload and download files to and from MS-FSSHTTP enabled endpoints.</span></span> <span data-ttu-id="60027-107">Это позволяет расширенных функций резервные службы, в Office, такие как переходы совместного редактирования и полностью из автономного режима для сети.</span><span class="sxs-lookup"><span data-stu-id="60027-107">This enables advanced service-backed features in Office, such as co-authoring and seamless transitions from offline to online.</span></span>
  
<span data-ttu-id="60027-108">CsiSyncClient доступна в Office Desktop (x86 и x64).</span><span class="sxs-lookup"><span data-stu-id="60027-108">CsiSyncClient is available in Office Desktop (both x86 and x64).</span></span> <span data-ttu-id="60027-109">Примечание: Во время новых версиях Office может имеющимся в CsiSyncClient, процесс будет использоваться для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="60027-109">Note: While newer versions of Office may ship with CsiSyncClient, the process will be used for backward compatibility only.</span></span> <span data-ttu-id="60027-110">Методика управления ODC и интерфейса CsiSyncClient изменится в будущих версиях Office.</span><span class="sxs-lookup"><span data-stu-id="60027-110">The CsiSyncClient interface and the methodology of controlling the ODC will change in future versions of Office.</span></span>
  
<span data-ttu-id="60027-111">Идентификатор класса в настоящее время имеет значение только ответить на OneDrive.</span><span class="sxs-lookup"><span data-stu-id="60027-111">The class ID is currently set to respond only to OneDrive.</span></span>
  
<span data-ttu-id="60027-112">Можно использовать как сервер ожидания proc COM и выполняется в CsiSyncClient.exe COM-объектов.</span><span class="sxs-lookup"><span data-stu-id="60027-112">The COM object is usable as an out-of-proc COM server and runs in CsiSyncClient.exe.</span></span> <span data-ttu-id="60027-113">Из-за ограничения доступа (которая использует ODC) поставляется с типа bit, поступающих Office, поэтому x64 Office означает, что x64 COM-объектом или x86 Office означает, что x86 COM-объектом.</span><span class="sxs-lookup"><span data-stu-id="60027-113">Due to limitations with Access (which the ODC uses), it ships with the bit type that Office comes in, so x64 Office means an x64 COM object, or x86 Office means an x86 COM object.</span></span> <span data-ttu-id="60027-114">Чтобы обойти данное ограничение, определяющее CLSCTX_LOCAL_SERVER как часть CoCreateInstance будет иметь размещаться как сервер COM ожидания proc, позволяя совместимости различной разрядности COM-объектом.</span><span class="sxs-lookup"><span data-stu-id="60027-114">To get around this limitation, specifying CLSCTX_LOCAL_SERVER as part of the CoCreateInstance will have the COM object be hosted as an out-of-proc COM server, allowing cross-bitness compatibility.</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="60027-115">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="60027-115">Interfaces</span></span>

<span data-ttu-id="60027-116">CSISyncClient использует следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="60027-116">CSISyncClient uses the following interfaces.</span></span>
  
### <a name="interface-ilsclocalsyncclient"></a><span data-ttu-id="60027-117">Интерфейс ILSCLocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="60027-117">Interface ILSCLocalSyncClient</span></span>

<span data-ttu-id="60027-118">Это основной интерфейс, используемый для синхронизации файлов в Office.</span><span class="sxs-lookup"><span data-stu-id="60027-118">This is the primary interface used to synchronize files in Office.</span></span>
  
- <span data-ttu-id="60027-119">ProgID: Office.LocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="60027-119">ProgID: Office.LocalSyncClient</span></span>
- <span data-ttu-id="60027-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span><span class="sxs-lookup"><span data-stu-id="60027-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span></span>
- <span data-ttu-id="60027-121">Библиотека типов: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span><span class="sxs-lookup"><span data-stu-id="60027-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span></span>
   
<span data-ttu-id="60027-122">COM-объектом, который предоставляется используется как сервер вне процесса.</span><span class="sxs-lookup"><span data-stu-id="60027-122">The COM object that is exposed is used as an out-of-proc server.</span></span> <span data-ttu-id="60027-123">Указание CLSCTX_LOCAL_SERVER как часть CoCreateInstance позволяет совместимости между процессов 32-разрядная и 64-разрядный выпуск.</span><span class="sxs-lookup"><span data-stu-id="60027-123">Specifying CLSCTX_LOCAL_SERVER as part of CoCreateInstance allows compatability between 64bit and 32bit processes.</span></span>
  
<span data-ttu-id="60027-124">После создания совместного COM-объектом, сначала необходимо вызвать [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) .</span><span class="sxs-lookup"><span data-stu-id="60027-124">Once you've co-created the COM object, you MUST call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) first.</span></span> <span data-ttu-id="60027-125">После успешного завершения [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) может вызвать любой API часто требуется и в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="60027-125">Once [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has completed successfully, you may call any API as often as you wish and in any order.</span></span> <span data-ttu-id="60027-126">Можно также вызвать [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) на уже инициализированный объект, но не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="60027-126">You may also call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) on an already initialized object, but this does nothing.</span></span> 
  
<span data-ttu-id="60027-127">Исключения в предыдущем параграфе, [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) и [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="60027-127">The exceptions to the previous paragraph are [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) and [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="60027-128">После вызова [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) на COM-объектом, необходимо удалить этот объект и создать новую.</span><span class="sxs-lookup"><span data-stu-id="60027-128">After you call [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) on the COM object, you MUST destroy that object and create a new one.</span></span> <span data-ttu-id="60027-129">[ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) удаление вашей subcache, удалите все сведения о связанных файлов в кэше, но оставить документы на диске.</span><span class="sxs-lookup"><span data-stu-id="60027-129">[ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) will delete your subcache, delete all associated file information in the cache, but leave the documents on disk.</span></span> <span data-ttu-id="60027-130">Он также затрагивает состояние для общения с кэшем.</span><span class="sxs-lookup"><span data-stu-id="60027-130">It also leaves the state intact for communicating with the cache.</span></span> <span data-ttu-id="60027-131">Это позволяет вызывать [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) еще раз, чтобы создать новый кэш без необходимости удалить и повторно создать COM-объектом.</span><span class="sxs-lookup"><span data-stu-id="60027-131">This allows you to call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) again to create a new cache without having to destroy and recreate the COM object.</span></span> 
  
<span data-ttu-id="60027-132">**Функции общих элементов**</span><span class="sxs-lookup"><span data-stu-id="60027-132">**Public member functions**</span></span>

#### <a name="ilsclocalsyncclientdeletefile"></a><span data-ttu-id="60027-133">ILSCLocalSyncClient::DeleteFile</span><span class="sxs-lookup"><span data-stu-id="60027-133">ILSCLocalSyncClient::DeleteFile</span></span>

<span data-ttu-id="60027-134">DeleteFile используется для удаления файла данных из кэша.</span><span class="sxs-lookup"><span data-stu-id="60027-134">DeleteFile is used to remove the file information from the cache.</span></span> <span data-ttu-id="60027-135">Тем не менее этот метод будет закрыто соответствующий файл на диске и на сервере.</span><span class="sxs-lookup"><span data-stu-id="60027-135">However, this method will leave the associated file on disk and on the server.</span></span>
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="60027-136">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-136">Parameters</span></span>

 <span data-ttu-id="60027-137">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="60027-137">_bstrResourceID_</span></span>
  
<span data-ttu-id="60027-138">Строка, которая идентифицирует Ид_ресурса файла.</span><span class="sxs-lookup"><span data-stu-id="60027-138">The string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="60027-139">Это значение должно быть пустым длиной 128 символов.</span><span class="sxs-lookup"><span data-stu-id="60027-139">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="60027-140">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-140">Return values</span></span>

|<span data-ttu-id="60027-141">Значение</span><span class="sxs-lookup"><span data-stu-id="60027-141">Value</span></span>|<span data-ttu-id="60027-142">Описание</span><span class="sxs-lookup"><span data-stu-id="60027-142">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="60027-143">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="60027-143">E_FAIL</span></span>  <br/> |<span data-ttu-id="60027-144">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="60027-144">The call failed.</span></span>  <br/> |
|<span data-ttu-id="60027-145">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="60027-145">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="60027-146">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="60027-146">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="60027-147">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="60027-147">E_FAIL</span></span>  <br/> |<span data-ttu-id="60027-148">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="60027-148">The call failed.</span></span>  <br/> |
|<span data-ttu-id="60027-149">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="60027-149">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="60027-150">Заданным Ид_ресурса не находится в кэше.</span><span class="sxs-lookup"><span data-stu-id="60027-150">The given ResourceID is not in the cache.</span></span>  <br/> |
|<span data-ttu-id="60027-151">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="60027-151">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="60027-152">Initialize не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="60027-152">Initialize has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="60027-153">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="60027-153">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="60027-154">Файл в настоящее время синхронизации или открыть и не может быть удалена.</span><span class="sxs-lookup"><span data-stu-id="60027-154">The file is currently synchronizing or open and cannot be deleted.</span></span>  <br/> |
|<span data-ttu-id="60027-155">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="60027-155">S_OK</span></span>  <br/> |<span data-ttu-id="60027-156">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="60027-156">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a><span data-ttu-id="60027-157">ILSCLocalSyncClient::GetChanges</span><span class="sxs-lookup"><span data-stu-id="60027-157">ILSCLocalSyncClient::GetChanges</span></span>
<span data-ttu-id="60027-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span><span class="sxs-lookup"><span data-stu-id="60027-158"></span></span>

<span data-ttu-id="60027-159">GetChanges Возвращает перечислитель ILSCEvent объекты, а также возвращает маркер, которое задано в следующем вызове GetChanges, при условии, что получатель обработал предыдущей набор событий.</span><span class="sxs-lookup"><span data-stu-id="60027-159">GetChanges returns an enumerator of ILSCEvent objects, and also returns a token that is given to the next call to GetChanges, assuming the consumer has processed the previous set of events.</span></span> <span data-ttu-id="60027-160">События, прежде чем _nPreviousChangesToken_ указан, будут удаленного и недоступен.</span><span class="sxs-lookup"><span data-stu-id="60027-160">Events before the  _nPreviousChangesToken_ specified will be deleted and unavailable.</span></span> <span data-ttu-id="60027-161">Если нет событий для обработки, _pnCurrentChangesToken_ должны быть равны значениям _nPreviousChangesToken_, но по-прежнему устанавливающей _ppiEvents_ .</span><span class="sxs-lookup"><span data-stu-id="60027-161">If there are no events to be processed,  _pnCurrentChangesToken_ should be the same value as  _nPreviousChangesToken_, but  _ppiEvents_ will still be set.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a><span data-ttu-id="60027-162">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-162">Parameters</span></span>

 <span data-ttu-id="60027-163">_nPreviousChangesToken_</span><span class="sxs-lookup"><span data-stu-id="60027-163">_nPreviousChangesToken_</span></span>
  
<span data-ttu-id="60027-164">Определяет, какие события последней обработки потребителем.</span><span class="sxs-lookup"><span data-stu-id="60027-164">Identifies which event was last processed by the consumer.</span></span> 
  
 <span data-ttu-id="60027-165">_pnCurrentChangesToken_</span><span class="sxs-lookup"><span data-stu-id="60027-165">_pnCurrentChangesToken_</span></span>
  
<span data-ttu-id="60027-166">Идентифицирует самых последних событий затем передаются получателю.</span><span class="sxs-lookup"><span data-stu-id="60027-166">Identifies the most recent event being handed to the consumer.</span></span> <span data-ttu-id="60027-167">Не должно быть значение null.</span><span class="sxs-lookup"><span data-stu-id="60027-167">Must not be null.</span></span>
  
 <span data-ttu-id="60027-168">_ppiEvents_</span><span class="sxs-lookup"><span data-stu-id="60027-168">_ppiEvents_</span></span>
  
<span data-ttu-id="60027-169">Перечислитель для событий передачи получателю.</span><span class="sxs-lookup"><span data-stu-id="60027-169">An enumerator for the events handed to the consumer.</span></span> <span data-ttu-id="60027-170">Не должно быть значение null.</span><span class="sxs-lookup"><span data-stu-id="60027-170">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="60027-171">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-171">Return values</span></span>

|<span data-ttu-id="60027-172">Значение</span><span class="sxs-lookup"><span data-stu-id="60027-172">Value</span></span>|<span data-ttu-id="60027-173">Описание</span><span class="sxs-lookup"><span data-stu-id="60027-173">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="60027-174">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="60027-174">E_FAIL</span></span>  <br/> |<span data-ttu-id="60027-175">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="60027-175">The call failed.</span></span>  <br/> |
|<span data-ttu-id="60027-176">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="60027-176">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="60027-177">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="60027-177">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="60027-178">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="60027-178">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="60027-179">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="60027-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="60027-180">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="60027-180">S_OK</span></span>  <br/> |<span data-ttu-id="60027-181">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="60027-181">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a><span data-ttu-id="60027-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="60027-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span></span>

<span data-ttu-id="60027-183">GetClientNetworkSyncPermission используется для запросов ли Office синхронизации эвристику для сети затрат и энергии переопределяются.</span><span class="sxs-lookup"><span data-stu-id="60027-183">GetClientNetworkSyncPermission is used to query whether Office's synchronizing heuristics for network cost and power usage are overridden.</span></span> <span data-ttu-id="60027-184">На 3G или другую сеть высокая стоимость или при их запуске на батарей сравнение подключен, Office следующим шагом нужно заблокировать сетевого трафика до более opportune времени.</span><span class="sxs-lookup"><span data-stu-id="60027-184">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span>
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a><span data-ttu-id="60027-185">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-185">Parameters</span></span>

 <span data-ttu-id="60027-186">_nspType_</span><span class="sxs-lookup"><span data-stu-id="60027-186">_nspType_</span></span>
  
<span data-ttu-id="60027-187">Флаг, который определяет какие совет стоимость запроса.</span><span class="sxs-lookup"><span data-stu-id="60027-187">A flag which defines which cost heuristic to query.</span></span> <span data-ttu-id="60027-188">В разделе [LSCNetworkSyncPermissionType перечисления](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="60027-188">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span> 
  
 <span data-ttu-id="60027-189">_pfSyncEnabled_</span><span class="sxs-lookup"><span data-stu-id="60027-189">_pfSyncEnabled_</span></span>
  
<span data-ttu-id="60027-190">Указывает, в настоящее время переопределен совет запрошенные затраты или нет.</span><span class="sxs-lookup"><span data-stu-id="60027-190">Specifies whether the requested cost heuristic is currently overridden or not.</span></span> <span data-ttu-id="60027-191">Не должно быть значение null.</span><span class="sxs-lookup"><span data-stu-id="60027-191">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="60027-192">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-192">Return values</span></span>

|<span data-ttu-id="60027-193">Значение</span><span class="sxs-lookup"><span data-stu-id="60027-193">Value</span></span>|<span data-ttu-id="60027-194">Описание</span><span class="sxs-lookup"><span data-stu-id="60027-194">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="60027-195">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="60027-195">E_FAIL</span></span>  <br/> |<span data-ttu-id="60027-196">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="60027-196">The call failed.</span></span>  <br/> |
|<span data-ttu-id="60027-197">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="60027-197">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="60027-198">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="60027-198">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="60027-199">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="60027-199">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="60027-200">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="60027-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="60027-201">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="60027-201">S_OK</span></span>  <br/> |<span data-ttu-id="60027-202">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="60027-202">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a><span data-ttu-id="60027-203">ILSCLocalSyncClient::GetFileStatus</span><span class="sxs-lookup"><span data-stu-id="60027-203">ILSCLocalSyncClient::GetFileStatus</span></span>

<span data-ttu-id="60027-204">GetFileStatus используется для сбора данных для конкретного файла: является ли он существует в кэше, если у него есть ожидающие обмена данными с копией на сервере, и, если Office 2013 имеет самые даты данных из локальной копии.</span><span class="sxs-lookup"><span data-stu-id="60027-204">GetFileStatus is used to gather information for a specific file: whether it exists in the cache, if it has pending communication with the server copy, and if Office 2013 has the most up to date data from the local copy.</span></span> <span data-ttu-id="60027-205">Требует побитовое флаг [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) значений, чтобы определить, какая информация CsiSyncClient COM-объектом, чтобы запрашивать.</span><span class="sxs-lookup"><span data-stu-id="60027-205">It requires a bitwise flag of [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) values to determine what information the CsiSyncClient COM object is to query for.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a><span data-ttu-id="60027-206">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-206">Parameters</span></span>

 <span data-ttu-id="60027-207">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="60027-207">_bstrResourceID_</span></span>
  
<span data-ttu-id="60027-208">Строка, которая определяет файл на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="60027-208">The string which identifies the file on the client.</span></span> <span data-ttu-id="60027-209">Это значение должно быть пустым, длиной 128 символов.</span><span class="sxs-lookup"><span data-stu-id="60027-209">This value must be non-empty, with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="60027-210">_sfRequestedStatus_</span><span class="sxs-lookup"><span data-stu-id="60027-210">_sfRequestedStatus_</span></span>
  
<span data-ttu-id="60027-211">Флаг, который определяет, какие сведения для возврата.</span><span class="sxs-lookup"><span data-stu-id="60027-211">A flag which defines what information to return.</span></span> <span data-ttu-id="60027-212">В разделе [LSCStatusFlag перечисления](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="60027-212">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
 <span data-ttu-id="60027-213">_pbstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="60027-213">_pbstrFileSystemPath_</span></span>
  
<span data-ttu-id="60027-214">Строка, которая определяет расположение файла, определенного _bstrResourceID_ на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="60027-214">The string which identifies the location of the file identified by  _bstrResourceID_ on the client.</span></span> <span data-ttu-id="60027-215">Не должно быть значение null.</span><span class="sxs-lookup"><span data-stu-id="60027-215">Must not be null.</span></span> 
  
 <span data-ttu-id="60027-216">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="60027-216">_pbstrETag_</span></span>
  
<span data-ttu-id="60027-217">Строка, которая будет содержать eTag для файл, указанный параметром _bstrResourceID_.</span><span class="sxs-lookup"><span data-stu-id="60027-217">A string which will contain the eTag for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="60027-218">Не должно быть значение null.</span><span class="sxs-lookup"><span data-stu-id="60027-218">Must not be null.</span></span> 
  
 <span data-ttu-id="60027-219">_psfFileStatus_</span><span class="sxs-lookup"><span data-stu-id="60027-219">_psfFileStatus_</span></span>
  
<span data-ttu-id="60027-220">Флаг, который будет содержать состояние, при использовании _sfRequestedStatus_ для файл, указанный параметром _bstrResourceID_.</span><span class="sxs-lookup"><span data-stu-id="60027-220">A flag which will contain the status requested via  _sfRequestedStatus_ for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="60027-221">Не должно быть значение null.</span><span class="sxs-lookup"><span data-stu-id="60027-221">Must not be null.</span></span> <span data-ttu-id="60027-222">В разделе [LSCStatusFlag перечисления](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="60027-222">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="60027-223">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-223">Return values</span></span>

|<span data-ttu-id="60027-224">Значение</span><span class="sxs-lookup"><span data-stu-id="60027-224">Value</span></span>|<span data-ttu-id="60027-225">Описание</span><span class="sxs-lookup"><span data-stu-id="60027-225">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="60027-226">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="60027-226">E_FAIL</span></span>  <br/> |<span data-ttu-id="60027-227">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="60027-227">The call failed.</span></span>  <br/> |
|<span data-ttu-id="60027-228">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="60027-228">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="60027-229">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="60027-229">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="60027-230">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="60027-230">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="60027-231">Сведения о файле, указанного идентификатором _bstrResourceID_ не существует в кэше.</span><span class="sxs-lookup"><span data-stu-id="60027-231">The file information specified by  _bstrResourceID_ does not exist in the cache.</span></span>  <br/> |
|<span data-ttu-id="60027-232">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="60027-232">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="60027-233">Был запрошен LSCStatusFlag_LocalFileUnchanged или файл, указанный в _bstrResourceID_ заблокированы или отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="60027-233">LSCStatusFlag_LocalFileUnchanged was requested or the file specified by  _bstrResourceID_ is locked or missing.</span></span>  <br/> |
|<span data-ttu-id="60027-234">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="60027-234">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="60027-235">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="60027-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="60027-236">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="60027-236">S_OK</span></span>  <br/> |<span data-ttu-id="60027-237">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="60027-237">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a><span data-ttu-id="60027-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="60027-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span></span>
<span data-ttu-id="60027-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span><span class="sxs-lookup"><span data-stu-id="60027-239"></span></span>

<span data-ttu-id="60027-240">GetSupportedFileExtensions возвращает список расширений имени файла с разделителями канала, которые в настоящее время поддерживаются в CsiSyncClient COM-объектом.</span><span class="sxs-lookup"><span data-stu-id="60027-240">GetSupportedFileExtensions returns a list of pipe-delimited file extensions which are currently supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="60027-241">Обратите внимание на то, что этот список может меняться, и потребитель будет оповещать об изменении с помощью объекта IPartnerActivityCallback, содержащимся на [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (EventOccured см).</span><span class="sxs-lookup"><span data-stu-id="60027-241">Note that this list may change, and the consumer will be notified of a change via the IPartnerActivityCallback object provided on [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (See EventOccured).</span></span> 
  
<span data-ttu-id="60027-242">Пример строки, возвращаемой выглядит следующим образом: «| docx | docm | pptx |»</span><span class="sxs-lookup"><span data-stu-id="60027-242">An example of the string returned is as follows: "|docx|docm|pptx|"</span></span>
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a><span data-ttu-id="60027-243">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-243">Parameters</span></span>

 <span data-ttu-id="60027-244">_pbstrSupportedFileExtensions_</span><span class="sxs-lookup"><span data-stu-id="60027-244">_pbstrSupportedFileExtensions_</span></span>
  
<span data-ttu-id="60027-245">Строка, должно быть задано набор разделенных вертикальная черта расширения имен файлов, поддерживаемые CsiSyncClient COM-объектом.</span><span class="sxs-lookup"><span data-stu-id="60027-245">A string to be set with a pipe-delimited set of file extensions supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="60027-246">Не должно быть значение null.</span><span class="sxs-lookup"><span data-stu-id="60027-246">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="60027-247">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-247">Return values</span></span>

|<span data-ttu-id="60027-248">Значение</span><span class="sxs-lookup"><span data-stu-id="60027-248">Value</span></span>|<span data-ttu-id="60027-249">Описание</span><span class="sxs-lookup"><span data-stu-id="60027-249">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="60027-250">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="60027-250">E_FAIL</span></span>  <br/> |<span data-ttu-id="60027-251">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="60027-251">The call failed.</span></span>  <br/> |
|<span data-ttu-id="60027-252">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="60027-252">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="60027-253">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="60027-253">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="60027-254">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="60027-254">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="60027-255">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="60027-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="60027-256">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="60027-256">S_OK</span></span>  <br/> |<span data-ttu-id="60027-257">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="60027-257">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a><span data-ttu-id="60027-258">ILSCLocalSyncClient::Initialize</span><span class="sxs-lookup"><span data-stu-id="60027-258">ILSCLocalSyncClient::Initialize</span></span>
<span data-ttu-id="60027-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span><span class="sxs-lookup"><span data-stu-id="60027-259"></span></span>

<span data-ttu-id="60027-260">Initialize должен быть метод вызывается первым.</span><span class="sxs-lookup"><span data-stu-id="60027-260">Initialize must be the first method called.</span></span> <span data-ttu-id="60027-261">В противном случае возвращает E_LSC_NOTINITIALIZED другим API.</span><span class="sxs-lookup"><span data-stu-id="60027-261">Otherwise, all other APIs will return E_LSC_NOTINITIALIZED.</span></span> <span data-ttu-id="60027-262">Вызов метода Initialize для уже инициализированный объект возвращает значение S_OK и не имеет никакого эффекта.</span><span class="sxs-lookup"><span data-stu-id="60027-262">Calling Initialize on an already initialized object returns S_OK and does nothing.</span></span> <span data-ttu-id="60027-263">Если возвращаются E_LSC_CACHEMISMATCH Звонящий может вызвать [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) удаление кэша, связанного с заданным SuppliedID.</span><span class="sxs-lookup"><span data-stu-id="60027-263">If E_LSC_CACHEMISMATCH is returned, the caller may call [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) to delete the cache associated with the given SuppliedID.</span></span> <span data-ttu-id="60027-264">Тем не менее в данном случае другие API-интерфейсы по-прежнему возвращает E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="60027-264">However, in this case other APIs will still return E_LSC_NOTINITIALIZED.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a><span data-ttu-id="60027-265">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-265">Parameters</span></span>

 <span data-ttu-id="60027-266">_bstrSuppliedID_</span><span class="sxs-lookup"><span data-stu-id="60027-266">_bstrSuppliedID_</span></span>
  
<span data-ttu-id="60027-267">Определяет потребитель и, для кэширования для использования.</span><span class="sxs-lookup"><span data-stu-id="60027-267">Identifies the consumer and which cache to use.</span></span> <span data-ttu-id="60027-268">Должен быть пустым с 32 знаков.</span><span class="sxs-lookup"><span data-stu-id="60027-268">Must be non-empty with a maximum of 32 characters.</span></span> 
  
 <span data-ttu-id="60027-269">_bstrProgID_</span><span class="sxs-lookup"><span data-stu-id="60027-269">_bstrProgID_</span></span>
  
<span data-ttu-id="60027-270">Определяет COM-объект получателя для двусторонней связи.</span><span class="sxs-lookup"><span data-stu-id="60027-270">Identifies the consumer's COM object for two-way communication.</span></span> <span data-ttu-id="60027-271">Должен быть пустым с 39 знаков.</span><span class="sxs-lookup"><span data-stu-id="60027-271">Must be non-empty with a maximum of 39 characters.</span></span> <span data-ttu-id="60027-272">Просмотреть \< для получения дополнительных сведений о коды ProgID.</span><span class="sxs-lookup"><span data-stu-id="60027-272">See [\<ProgID\> Key](http://msdn.microsoft.com/en-us/library/ms690196.aspx.aspx) for more information on ProgIDs.</span></span> 
  
 <span data-ttu-id="60027-273">_bstrFileSystemDirectoryHint_</span><span class="sxs-lookup"><span data-stu-id="60027-273">_bstrFileSystemDirectoryHint_</span></span>
  
<span data-ttu-id="60027-274">Определяет корневой каталог, в котором будут храниться локальные файлы.</span><span class="sxs-lookup"><span data-stu-id="60027-274">Identifies the directory root in which local files will be stored.</span></span> <span data-ttu-id="60027-275">Должен быть пустым с 256 знаков.</span><span class="sxs-lookup"><span data-stu-id="60027-275">Must be non-empty with a maximum of 256 characters.</span></span> <span data-ttu-id="60027-276">Каталог уже должен существовать.</span><span class="sxs-lookup"><span data-stu-id="60027-276">The directory must already exist.</span></span> 
  
 <span data-ttu-id="60027-277">_pEventCallback_</span><span class="sxs-lookup"><span data-stu-id="60027-277">_pEventCallback_</span></span>
  
<span data-ttu-id="60027-278">Интерфейс обратного вызова, который CsiSyncClient будет уведомление об изменениях.</span><span class="sxs-lookup"><span data-stu-id="60027-278">The callback interface which CsiSyncClient will notify on changes.</span></span> <span data-ttu-id="60027-279">В разделе IPartnerActivityCallback::EventOccurred.</span><span class="sxs-lookup"><span data-stu-id="60027-279">See IPartnerActivityCallback::EventOccurred.</span></span> <span data-ttu-id="60027-280">Это значение не может быть null.</span><span class="sxs-lookup"><span data-stu-id="60027-280">This value must not be null.</span></span> 
  
 <span data-ttu-id="60027-281">_pfCreatedNewCache_</span><span class="sxs-lookup"><span data-stu-id="60027-281">_pfCreatedNewCache_</span></span>
  
<span data-ttu-id="60027-282">Возвращает, был ли создан новый кэш.</span><span class="sxs-lookup"><span data-stu-id="60027-282">Returns whether a new cache was created.</span></span> <span data-ttu-id="60027-283">Если кэширование отключено связан с SuppliedID, он будет создан.</span><span class="sxs-lookup"><span data-stu-id="60027-283">If no cache is associated with the SuppliedID, one will be created.</span></span> <span data-ttu-id="60027-284">Это значение не может быть null.</span><span class="sxs-lookup"><span data-stu-id="60027-284">This value must not be null.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="60027-285">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-285">Return values</span></span>

|<span data-ttu-id="60027-286">Значение</span><span class="sxs-lookup"><span data-stu-id="60027-286">Value</span></span>|<span data-ttu-id="60027-287">Описание</span><span class="sxs-lookup"><span data-stu-id="60027-287">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="60027-288">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="60027-288">E_FAIL</span></span>  <br/> |<span data-ttu-id="60027-289">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="60027-289">The call failed.</span></span>  <br/> |
|<span data-ttu-id="60027-290">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="60027-290">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="60027-291">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="60027-291">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="60027-292">E_LSC_CACHEMISMATCH</span><span class="sxs-lookup"><span data-stu-id="60027-292">E_LSC_CACHEMISMATCH</span></span>  <br/> |<span data-ttu-id="60027-293">SuppliedID уже имеет кэша, связанных с ним, но имеет разные ProgId или FileSystemDirectoryHint отличный от предоставляемых.</span><span class="sxs-lookup"><span data-stu-id="60027-293">A SuppliedID already has a cache associated with it, but has a different ProgId or FileSystemDirectoryHint than the ones provided.</span></span>  <br/> |
|<span data-ttu-id="60027-294">E_LSC_DIRECTORYHINTCONFLICT</span><span class="sxs-lookup"><span data-stu-id="60027-294">E_LSC_DIRECTORYHINTCONFLICT</span></span>  <br/> |<span data-ttu-id="60027-295">FileSystemDirectoryHint (или вложенной папке) уже присутствует в разных кэша.</span><span class="sxs-lookup"><span data-stu-id="60027-295">The FileSystemDirectoryHint (or a subfolder) already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="60027-296">E_LAC_PROGIDCONFLICT</span><span class="sxs-lookup"><span data-stu-id="60027-296">E_LAC_PROGIDCONFLICT</span></span>  <br/> |<span data-ttu-id="60027-297">Программный идентификатор уже присутствует в разных кэша.</span><span class="sxs-lookup"><span data-stu-id="60027-297">The ProgID already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="60027-298">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="60027-298">S_OK</span></span>  <br/> |<span data-ttu-id="60027-299">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="60027-299">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a><span data-ttu-id="60027-300">ILSCLocalSyncClient::LocalFileChange</span><span class="sxs-lookup"><span data-stu-id="60027-300">ILSCLocalSyncClient::LocalFileChange</span></span>
<span data-ttu-id="60027-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="60027-301"></span></span>

<span data-ttu-id="60027-302">LocalFileChange используется CsiSyncClient COM-объектом, чтобы попытаться загрузить указанный файл.</span><span class="sxs-lookup"><span data-stu-id="60027-302">LocalFileChange is used to tell the CsiSyncClient COM object to attempt to upload the specified file.</span></span> <span data-ttu-id="60027-303">Метод подготовить файл для загрузки, включая чтение текущее содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="60027-303">The method will prepare the file for upload, including reading the file's current contents.</span></span> <span data-ttu-id="60027-304">Если передаваемых ожидающих установки, предыдущей загрузки будут отменены и отправьте подготовлено для нового содержимого.</span><span class="sxs-lookup"><span data-stu-id="60027-304">If an upload is already pending, the previous upload will be discarded and the new contents prepared for upload.</span></span> <span data-ttu-id="60027-305">Если файл открыт для редактирования в приложении, этот метод возвращает значение S_OK без подготовки файл для загрузки (приложение уже делать это действие при наличии изменений).</span><span class="sxs-lookup"><span data-stu-id="60027-305">If the file is open for editing in an application, this method will return S_OK without preparing the file for upload (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="60027-306">Этот метод позволяет передача если помечено как отправляет заблокированных ранее ( [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)см).</span><span class="sxs-lookup"><span data-stu-id="60027-306">This method will allow uploads if it was marked as uploads blocked previously (see [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span></span>
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="60027-307">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-307">Parameters</span></span>

 <span data-ttu-id="60027-308">_bstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="60027-308">_bstrFileSystemPath_</span></span>
  
<span data-ttu-id="60027-309">Строка, которая определяет файл на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="60027-309">A string which identifies the file on the client.</span></span> <span data-ttu-id="60027-310">Это значение должно быть пустым локальный путь с 256 знаков.</span><span class="sxs-lookup"><span data-stu-id="60027-310">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="60027-311">Этот путь должен быть в дереве каталогов, назначаемое FileSystemDirectoryHint при вызове [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) .</span><span class="sxs-lookup"><span data-stu-id="60027-311">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was made.</span></span> 
  
 <span data-ttu-id="60027-312">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="60027-312">_bstrResourceID_</span></span>
  
<span data-ttu-id="60027-313">Строка, которая идентифицирует Ид_ресурса файла.</span><span class="sxs-lookup"><span data-stu-id="60027-313">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="60027-314">Это значение должно быть пустым длиной 128 символов.</span><span class="sxs-lookup"><span data-stu-id="60027-314">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="60027-315">_bstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="60027-315">_bstrWebPath_</span></span>
  
<span data-ttu-id="60027-316">Строка, которая определяет файл на сервере.</span><span class="sxs-lookup"><span data-stu-id="60027-316">A string which identifies the file on the server.</span></span> <span data-ttu-id="60027-317">Это значение должно быть пустым, допустимый URL-адрес, но не более INTERNET_MAX_URL_LENGTH, в соответствии с определением http://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="60027-317">This value must be non-empty, valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by http://support.microsoft.com/kb/208427.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="60027-318">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-318">Return values</span></span>

|<span data-ttu-id="60027-319">Значение</span><span class="sxs-lookup"><span data-stu-id="60027-319">Value</span></span>|<span data-ttu-id="60027-320">Описание</span><span class="sxs-lookup"><span data-stu-id="60027-320">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="60027-321">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="60027-321">E_FAIL</span></span>  <br/> |<span data-ttu-id="60027-322">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="60027-322">The call failed.</span></span>  <br/> |
|<span data-ttu-id="60027-323">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="60027-323">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="60027-324">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="60027-324">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="60027-325">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="60027-325">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="60027-326">Файл, указанный в _bstrFileSystemPath_ имеет разные Ид_ресурса не указан.</span><span class="sxs-lookup"><span data-stu-id="60027-326">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span> <span data-ttu-id="60027-327">Событие типа LSCEventType_OnFilePathConflict сообщения при этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="60027-327">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="60027-328">В разделе [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="60027-328">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="60027-329">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="60027-329">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="60027-330">Файл был удаленных Среднеатлантическое операции.</span><span class="sxs-lookup"><span data-stu-id="60027-330">The file was deleted mid-operation.</span></span>  <br/> |
|<span data-ttu-id="60027-331">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="60027-331">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="60027-332">Расширение указанного файла не поддерживается объектом CsiSyncClient COM.</span><span class="sxs-lookup"><span data-stu-id="60027-332">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="60027-333">В разделе [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span><span class="sxs-lookup"><span data-stu-id="60027-333">See [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span></span>  <br/> |
|<span data-ttu-id="60027-334">E_LSC_FILEUPTODATE</span><span class="sxs-lookup"><span data-stu-id="60027-334">E_LSC_FILEUPTODATE</span></span>  <br/> |<span data-ttu-id="60027-335">COM-объектом собрания не выбрано передаваемых из-за последних изменений с диска файла в кэше.</span><span class="sxs-lookup"><span data-stu-id="60027-335">The COM object did not schedule an upload because the file in the cache had the most recent changes from the disk.</span></span>  <br/> |
|<span data-ttu-id="60027-336">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="60027-336">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="60027-337">Файл, указанный в _bstrFileSystemPath_ отсутствует или заблокирован.</span><span class="sxs-lookup"><span data-stu-id="60027-337">The file specified by  _bstrFileSystemPath_ is missing or locked.</span></span>  <br/> |
|<span data-ttu-id="60027-338">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="60027-338">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="60027-339">Заданным FileSystemPath не в корневом каталоге, указанный с FileSystemDirectoryHint, когда вызов для инициализации.</span><span class="sxs-lookup"><span data-stu-id="60027-339">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="60027-340">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="60027-340">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="60027-341">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="60027-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="60027-342">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="60027-342">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="60027-343">Файл, указанный в _bstrResourceID_ имеет разные FileSystemPath не указан.</span><span class="sxs-lookup"><span data-stu-id="60027-343">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="60027-344">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="60027-344">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="60027-345">Указанный файл уже имеет ожидающих изменений в различных кэша и еще не могут быть связаны с кэшем получателя.</span><span class="sxs-lookup"><span data-stu-id="60027-345">The file specified already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="60027-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="60027-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="60027-347">WebPath предоставляются попадает в разных кэша.</span><span class="sxs-lookup"><span data-stu-id="60027-347">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="60027-348">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="60027-348">S_OK</span></span>  <br/> |<span data-ttu-id="60027-349">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="60027-349">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a><span data-ttu-id="60027-350">ILSCLocalSyncClient::RenameFile</span><span class="sxs-lookup"><span data-stu-id="60027-350">ILSCLocalSyncClient::RenameFile</span></span>
<span data-ttu-id="60027-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span><span class="sxs-lookup"><span data-stu-id="60027-351"></span></span>

<span data-ttu-id="60027-352">RenameFile будет сопоставьте новый URL-адрес и локальный путь для указанного Ид_ресурса.</span><span class="sxs-lookup"><span data-stu-id="60027-352">RenameFile will associate a new URL and local path for a given ResourceID.</span></span> <span data-ttu-id="60027-353">Если файл, указанный в Ид_ресурса еще не существует в кэше, будет предпринята попытка создать его и отметить для загрузки.</span><span class="sxs-lookup"><span data-stu-id="60027-353">If the file specified by the ResourceID doesn't already exist in the cache, an attempt will be made to create it and mark it for download.</span></span>
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a><span data-ttu-id="60027-354">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-354">Parameters</span></span>

 <span data-ttu-id="60027-355">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="60027-355">_bstrResourceID_</span></span>
  
<span data-ttu-id="60027-356">Строка, которая идентифицирует Ид_ресурса файла.</span><span class="sxs-lookup"><span data-stu-id="60027-356">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="60027-357">Это значение должно быть пустым длиной 128 символов.</span><span class="sxs-lookup"><span data-stu-id="60027-357">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="60027-358">_bstrNewFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="60027-358">_bstrNewFileSystemPath_</span></span>
  
<span data-ttu-id="60027-359">Строка, которая задает новый локальный путь для файла.</span><span class="sxs-lookup"><span data-stu-id="60027-359">A string which specifies the new local path for the file.</span></span> <span data-ttu-id="60027-360">Это значение должно быть пустым локальный путь с 256 знаков.</span><span class="sxs-lookup"><span data-stu-id="60027-360">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="60027-361">Этот путь должен быть в дереве каталогов, указанный с FileSystemDirectoryHint, когда вызов для инициализации.</span><span class="sxs-lookup"><span data-stu-id="60027-361">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span> 
  
 <span data-ttu-id="60027-362">_bstrNewWebPath_</span><span class="sxs-lookup"><span data-stu-id="60027-362">_bstrNewWebPath_</span></span>
  
<span data-ttu-id="60027-363">Строка, которая задает новый URL-адрес для файла.</span><span class="sxs-lookup"><span data-stu-id="60027-363">A string which specifies the new URL for the file.</span></span> <span data-ttu-id="60027-364">Это значение должно быть пустым допустимый URL-адрес, но не более INTERNET_MAX_URL_LENGTH, в соответствии с определением http://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="60027-364">This value must be non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by http://support.microsoft.com/kb/208427.</span></span> 
  
 <span data-ttu-id="60027-365">_fBlockUploads_</span><span class="sxs-lookup"><span data-stu-id="60027-365">_fBlockUploads_</span></span>
  
<span data-ttu-id="60027-366">Указывает, разрешены ли в настоящее время отправки в новом месте.</span><span class="sxs-lookup"><span data-stu-id="60027-366">Specifies whether uploads to the new location are allowed currently.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="60027-367">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-367">Return values</span></span>

|<span data-ttu-id="60027-368">Значение</span><span class="sxs-lookup"><span data-stu-id="60027-368">Value</span></span>|<span data-ttu-id="60027-369">Описание</span><span class="sxs-lookup"><span data-stu-id="60027-369">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="60027-370">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="60027-370">E_FAIL</span></span>  <br/> |<span data-ttu-id="60027-371">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="60027-371">The call failed.</span></span>  <br/> |
|<span data-ttu-id="60027-372">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="60027-372">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="60027-373">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="60027-373">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="60027-374">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="60027-374">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="60027-375">_BstrNewFileSystemPath_ или _bstrNewWebPath_ уже существует на другой файл в любой кэш.</span><span class="sxs-lookup"><span data-stu-id="60027-375">The  _bstrNewFileSystemPath_ or  _bstrNewWebPath_ already exist on another file in any cache.</span></span> <span data-ttu-id="60027-376">Событие типа LSCEventType_OnFilePathConflict сообщения при этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="60027-376">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="60027-377">В разделе [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="60027-377">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="60027-378">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="60027-378">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="60027-379">Сведения о файле был удален из кэша во время выполнения этого метода.</span><span class="sxs-lookup"><span data-stu-id="60027-379">The file information was deleted from the cache while this method was running.</span></span>  <br/> |
|<span data-ttu-id="60027-380">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="60027-380">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="60027-381">Заданным FileSystemPath не в корневом каталоге, указанный с FileSystemDirectoryHint, когда вызов для инициализации.</span><span class="sxs-lookup"><span data-stu-id="60027-381">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="60027-382">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="60027-382">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="60027-383">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="60027-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="60027-384">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="60027-384">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="60027-385">Файл, указанный в настоящее время синхронизации в приложении Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="60027-385">The file specified is currently synchronizing in an Office application.</span></span>  <br/> |
|<span data-ttu-id="60027-386">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="60027-386">S_OK</span></span>  <br/> |<span data-ttu-id="60027-387">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="60027-387">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a><span data-ttu-id="60027-388">ILSCLocalSyncClient::ResetCache</span><span class="sxs-lookup"><span data-stu-id="60027-388">ILSCLocalSyncClient::ResetCache</span></span>
<span data-ttu-id="60027-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span><span class="sxs-lookup"><span data-stu-id="60027-389"></span></span>

<span data-ttu-id="60027-390">ResetCache приведет к удалению кэша, связанного с SuppliedID, которое было указано на Initialize.</span><span class="sxs-lookup"><span data-stu-id="60027-390">ResetCache will delete the cache associated with the SuppliedID that was provided on Initialize.</span></span> <span data-ttu-id="60027-391">Это включает в себя все сведения о файле, но останется файлов на клиенте и на сервере.</span><span class="sxs-lookup"><span data-stu-id="60027-391">This includes all of the file information, but will leave the files on both the client and the server.</span></span> <span data-ttu-id="60027-392">Этот метод также оставляет объект в частично не инициализированный состоянии.</span><span class="sxs-lookup"><span data-stu-id="60027-392">This method also leaves the object in a partially uninitialized state.</span></span> <span data-ttu-id="60027-393">Вызовы допустимо только после этого — это [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) или [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="60027-393">The only valid calls after this are [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) or [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="60027-394">Этот метод может вызываться при инициализации, возникает ошибка и возвращает E_LSC_CACHEMISMATCH и приведет к удалению кэша, связанного с SuppliedID, которое было указано при вызове со сбоями.</span><span class="sxs-lookup"><span data-stu-id="60027-394">This method MAY be called if Initialize fails and returns E_LSC_CACHEMISMATCH, and will delete the cache associated with the SuppliedID that was provided with the failing call.</span></span>
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a><span data-ttu-id="60027-395">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-395">Parameters</span></span>

<span data-ttu-id="60027-396">Нет</span><span class="sxs-lookup"><span data-stu-id="60027-396">None</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="60027-397">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-397">Return values</span></span>

|<span data-ttu-id="60027-398">Значение</span><span class="sxs-lookup"><span data-stu-id="60027-398">Value</span></span>|<span data-ttu-id="60027-399">Описание</span><span class="sxs-lookup"><span data-stu-id="60027-399">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="60027-400">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="60027-400">E_FAIL</span></span>  <br/> |<span data-ttu-id="60027-401">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="60027-401">The call failed.</span></span>  <br/> |
|<span data-ttu-id="60027-402">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="60027-402">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="60027-403">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызывается в прошлом.</span><span class="sxs-lookup"><span data-stu-id="60027-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was not successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="60027-404">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="60027-404">S_OK</span></span>  <br/> |<span data-ttu-id="60027-405">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="60027-405">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a><span data-ttu-id="60027-406">ILSCLocalSyncClient::ServerFileChange</span><span class="sxs-lookup"><span data-stu-id="60027-406">ILSCLocalSyncClient::ServerFileChange</span></span>
<span data-ttu-id="60027-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="60027-407"></span></span>

<span data-ttu-id="60027-408">ServerFileChange указывает CsiSyncClient COM-объектом, чтобы пометить указанный файл для загрузки.</span><span class="sxs-lookup"><span data-stu-id="60027-408">ServerFileChange tells the CsiSyncClient COM object to mark the specified file for download.</span></span> <span data-ttu-id="60027-409">Если файл открыт в приложении Microsoft Office для изменения, этот метод возвращает значение S_OK не помечая файл для загрузки (приложение уже делать это действие при наличии изменений).</span><span class="sxs-lookup"><span data-stu-id="60027-409">If the file is open in an Office application for edit, this method will return S_OK without marking the file for download (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="60027-410">Этот метод позволяет загрузки если помечено как файлы для загрузки заблокированных ранее (RenameFile см).</span><span class="sxs-lookup"><span data-stu-id="60027-410">This method will allow downloads if it was marked as downloads blocked previously (see RenameFile).</span></span>
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="60027-411">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-411">Parameters</span></span>

|<span data-ttu-id="60027-412">Параметр</span><span class="sxs-lookup"><span data-stu-id="60027-412">Parameter</span></span>|<span data-ttu-id="60027-413">Описание</span><span class="sxs-lookup"><span data-stu-id="60027-413">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="60027-414">bstrFileSystemPath</span><span class="sxs-lookup"><span data-stu-id="60027-414">bstrFileSystemPath</span></span>  <br/> |<span data-ttu-id="60027-415">Строка, которая определяет файл на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="60027-415">A string which identifies the file on the client.</span></span> <span data-ttu-id="60027-416">Это значение должно быть пустым локальный путь с 256 знаков.</span><span class="sxs-lookup"><span data-stu-id="60027-416">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="60027-417">Этот путь должен быть в дереве каталогов, указанный с FileSystemDirectoryHint, когда вызов для инициализации.</span><span class="sxs-lookup"><span data-stu-id="60027-417">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="60027-418">bstrResourceID</span><span class="sxs-lookup"><span data-stu-id="60027-418">bstrResourceID</span></span>  <br/> |<span data-ttu-id="60027-419">Строка, которая идентифицирует Ид_ресурса файла.</span><span class="sxs-lookup"><span data-stu-id="60027-419">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="60027-420">Это значение должно быть пустым длиной 128 символов.</span><span class="sxs-lookup"><span data-stu-id="60027-420">This value must be non-empty with a maximum of 128 characters.</span></span>  <br/> |
|<span data-ttu-id="60027-421">bstrWebPath</span><span class="sxs-lookup"><span data-stu-id="60027-421">bstrWebPath</span></span>  <br/> |<span data-ttu-id="60027-422">Строка, которая определяет файл на сервере.</span><span class="sxs-lookup"><span data-stu-id="60027-422">A string which identifies the file on the server.</span></span> <span data-ttu-id="60027-423">Это значение должно быть пустым допустимый URL-адрес, но не более INTERNET_MAX_URL_LENGTH, в соответствии с определением http://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="60027-423">This value must be a non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by http://support.microsoft.com/kb/208427.</span></span>  <br/> |
   
##### <a name="return-values"></a><span data-ttu-id="60027-424">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-424">Return values</span></span>

|<span data-ttu-id="60027-425">Значение</span><span class="sxs-lookup"><span data-stu-id="60027-425">Value</span></span>|<span data-ttu-id="60027-426">Описание</span><span class="sxs-lookup"><span data-stu-id="60027-426">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="60027-427">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="60027-427">E_FAIL</span></span>  <br/> |<span data-ttu-id="60027-428">Сбой при попытке подключения к состояние кэша.</span><span class="sxs-lookup"><span data-stu-id="60027-428">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="60027-429">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="60027-429">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="60027-430">Файл, указанный в _bstrFileSystemPath_ имеет разные Ид_ресурса не указан.</span><span class="sxs-lookup"><span data-stu-id="60027-430">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span>  <br/> |
|<span data-ttu-id="60027-431">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="60027-431">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="60027-432">Расширение указанного файла не поддерживается объектом CsiSyncClient COM.</span><span class="sxs-lookup"><span data-stu-id="60027-432">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="60027-433">В разделе GetSupportedFileExtensions.</span><span class="sxs-lookup"><span data-stu-id="60027-433">See GetSupportedFileExtensions.</span></span>  <br/> |
|<span data-ttu-id="60027-434">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="60027-434">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="60027-435">Файл был удален в середине операции.</span><span class="sxs-lookup"><span data-stu-id="60027-435">The file was deleted in mid-operation.</span></span>  <br/> |
|<span data-ttu-id="60027-436">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="60027-436">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="60027-437">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="60027-437">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="60027-438">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="60027-438">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="60027-439">Заданным FileSystemPath не в корневом каталоге, указанный с FileSystemDirectoryHint, когда вызов для инициализации.</span><span class="sxs-lookup"><span data-stu-id="60027-439">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="60027-440">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="60027-440">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="60027-441">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="60027-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="60027-442">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="60027-442">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="60027-443">Файл, указанный в _bstrResourceID_ имеет разные FileSystemPath не указан.</span><span class="sxs-lookup"><span data-stu-id="60027-443">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="60027-444">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="60027-444">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="60027-445">Указанный файл уже имеет ожидающих изменений в различных кэша и еще не могут быть связаны с кэшем получателя.</span><span class="sxs-lookup"><span data-stu-id="60027-445">The specified file already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="60027-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="60027-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="60027-447">WebPath предоставляются попадает в разных кэша.</span><span class="sxs-lookup"><span data-stu-id="60027-447">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="60027-448">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="60027-448">S_OK</span></span>  <br/> |<span data-ttu-id="60027-449">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="60027-449">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a><span data-ttu-id="60027-450">ILSCLocalSyncClient::SetClientConnectivityState</span><span class="sxs-lookup"><span data-stu-id="60027-450">ILSCLocalSyncClient::SetClientConnectivityState</span></span>
<span data-ttu-id="60027-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="60027-451"></span></span>

<span data-ttu-id="60027-452">Задает кэш в автономном и интерактивном состояние.</span><span class="sxs-lookup"><span data-stu-id="60027-452">Sets the cache into an online or offline state.</span></span> <span data-ttu-id="60027-453">Если в автономном режиме, Office не будет пытаться связаться с сервером для всех файлов в этом кэше, независимо от настройки _fBlockUploads_ каждого отдельного файла.</span><span class="sxs-lookup"><span data-stu-id="60027-453">If offline, Office will not attempt to communicate with the server for any files in that cache, regardless of each individual file's  _fBlockUploads_ setting.</span></span> 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a><span data-ttu-id="60027-454">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-454">Parameters</span></span>

 <span data-ttu-id="60027-455">_fIsOnline_</span><span class="sxs-lookup"><span data-stu-id="60027-455">_fIsOnline_</span></span>
  
<span data-ttu-id="60027-456">Логическое значение, определение состояния подключения кэша.</span><span class="sxs-lookup"><span data-stu-id="60027-456">A boolean determining the connectivity state of the cache.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="60027-457">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-457">Return values</span></span>

|<span data-ttu-id="60027-458">Значение</span><span class="sxs-lookup"><span data-stu-id="60027-458">Value</span></span>|<span data-ttu-id="60027-459">Описание</span><span class="sxs-lookup"><span data-stu-id="60027-459">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="60027-460">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="60027-460">E_FAIL</span></span>  <br/> |<span data-ttu-id="60027-461">Сбой при попытке подключения к состояние кэша.</span><span class="sxs-lookup"><span data-stu-id="60027-461">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="60027-462">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="60027-462">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="60027-463">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="60027-463">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="60027-464">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="60027-464">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="60027-465">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="60027-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="60027-466">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="60027-466">S_OK</span></span>  <br/> |<span data-ttu-id="60027-467">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="60027-467">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a><span data-ttu-id="60027-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="60027-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span></span>
<span data-ttu-id="60027-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="60027-469"></span></span>

<span data-ttu-id="60027-470">SetClientNetworkSyncPermission используется для переопределять или restoreOffice's синхронизации эвристику для сети затрат и power об использовании.</span><span class="sxs-lookup"><span data-stu-id="60027-470">SetClientNetworkSyncPermission is used to either override or restoreOffice's synchronizing heuristics for network cost and power usage.</span></span> <span data-ttu-id="60027-471">На 3G или другую сеть высокая стоимость или при их запуске на батарей сравнение подключен, Office следующим шагом нужно заблокировать сетевого трафика до более opportune времени.</span><span class="sxs-lookup"><span data-stu-id="60027-471">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span> <span data-ttu-id="60027-472">Потребитель этот интерфейс API можно использовать для переопределения эвристику Office и Принудительная синхронизация будет выполнена.</span><span class="sxs-lookup"><span data-stu-id="60027-472">The consumer of this API can use it to override Office's heuristics and force synchronizing to occur.</span></span>
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a><span data-ttu-id="60027-473">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-473">Parameters</span></span>

 <span data-ttu-id="60027-474">_nspType_</span><span class="sxs-lookup"><span data-stu-id="60027-474">_nspType_</span></span>
  
<span data-ttu-id="60027-475">Флаг, который определяет, какие расходы Совет для переопределения.</span><span class="sxs-lookup"><span data-stu-id="60027-475">A flag which defines which cost heuristic to override.</span></span> <span data-ttu-id="60027-476">В разделе [LSCNetworkSyncPermissionType перечисления](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="60027-476">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span>
  
 <span data-ttu-id="60027-477">_fEnableSync_</span><span class="sxs-lookup"><span data-stu-id="60027-477">_fEnableSync_</span></span>
  
<span data-ttu-id="60027-478">Указывает, следует ли для принудительной синхронизации на таким образом переопределение этот совет затраты или больше не переопределить его.</span><span class="sxs-lookup"><span data-stu-id="60027-478">Specifies whether to force synchronizing on, thus overriding that cost heuristic, or to no longer override it.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="60027-479">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-479">Return values</span></span>

|<span data-ttu-id="60027-480">Значение</span><span class="sxs-lookup"><span data-stu-id="60027-480">Value</span></span>|<span data-ttu-id="60027-481">Описание</span><span class="sxs-lookup"><span data-stu-id="60027-481">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="60027-482">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="60027-482">E_FAIL</span></span>  <br/> |<span data-ttu-id="60027-483">Сбой, связанный с переопределить синхронизации эвристику.</span><span class="sxs-lookup"><span data-stu-id="60027-483">Failure to override synchronizing heuristics.</span></span>  <br/> |
|<span data-ttu-id="60027-484">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="60027-484">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="60027-485">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="60027-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="60027-486">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="60027-486">S_OK</span></span>  <br/> |<span data-ttu-id="60027-487">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="60027-487">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a><span data-ttu-id="60027-488">ILSCLocalSyncClient::Uninitialize</span><span class="sxs-lookup"><span data-stu-id="60027-488">ILSCLocalSyncClient::Uninitialize</span></span>
<span data-ttu-id="60027-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span><span class="sxs-lookup"><span data-stu-id="60027-489"></span></span>

<span data-ttu-id="60027-490">Выгрузка кэша из объекта COM и выполнять операции закрытия.</span><span class="sxs-lookup"><span data-stu-id="60027-490">Unloads the cache from the COM object and perform closing operations.</span></span> <span data-ttu-id="60027-491">[ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) НЕОБХОДИМО вызывать перед удалением COM-объектом.</span><span class="sxs-lookup"><span data-stu-id="60027-491">[ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUST be called before destroying the COM object.</span></span> <span data-ttu-id="60027-492">После вызова можно вызвать другие интерфейсы API, должен быть потеряны COM-объектом и создан новый, если продолжить выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="60027-492">Once called, no other APIs can be called, the COM object MUST be destroyed and a new one created if you wish to continue operations.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a><span data-ttu-id="60027-493">Параметры</span><span class="sxs-lookup"><span data-stu-id="60027-493">Parameters</span></span>

<span data-ttu-id="60027-494">Нет.</span><span class="sxs-lookup"><span data-stu-id="60027-494">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="60027-495">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-495">Return values</span></span>

|<span data-ttu-id="60027-496">Значение</span><span class="sxs-lookup"><span data-stu-id="60027-496">Value</span></span>|<span data-ttu-id="60027-497">Описание</span><span class="sxs-lookup"><span data-stu-id="60027-497">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="60027-498">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="60027-498">E_FAIL</span></span>  <br/> |<span data-ttu-id="60027-499">Сбой при выполнении отмены инициализации.</span><span class="sxs-lookup"><span data-stu-id="60027-499">Failure to uninitialize.</span></span>  <br/> |
|<span data-ttu-id="60027-500">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="60027-500">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="60027-501">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="60027-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="60027-502">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="60027-502">S_OK</span></span>  <br/> |<span data-ttu-id="60027-503">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="60027-503">The call succeeded.</span></span>  <br/> |
   
### <a name="interface-ienumlscevent"></a><span data-ttu-id="60027-504">Интерфейс IEnumLSCEvent</span><span class="sxs-lookup"><span data-stu-id="60027-504">Interface IEnumLSCEvent</span></span>

<span data-ttu-id="60027-505">Этот интерфейс представляет список событий ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="60027-505">This interface represents a list of ILSCEvent events.</span></span>
  
<span data-ttu-id="60027-506">**Функции общих элементов**</span><span class="sxs-lookup"><span data-stu-id="60027-506">**Public member functions**</span></span>

#### <a name="ienumlsceventfnext"></a><span data-ttu-id="60027-507">IEnumLSCEvent::FNext</span><span class="sxs-lookup"><span data-stu-id="60027-507">IEnumLSCEvent::FNext</span></span>

<span data-ttu-id="60027-508">Возвращает следующее событие из списка событий.</span><span class="sxs-lookup"><span data-stu-id="60027-508">Retrieves the next event from the list of events.</span></span>
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a><span data-ttu-id="60027-509">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-509">Parameters</span></span>

 <span data-ttu-id="60027-510">_ppiLSCEvent_</span><span class="sxs-lookup"><span data-stu-id="60027-510">_ppiLSCEvent_</span></span>
  
<span data-ttu-id="60027-511">Указатель на интерфейс ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="60027-511">A pointer to an ILSCEvent interface.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="60027-512">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-512">Return values</span></span>

|<span data-ttu-id="60027-513">Значение</span><span class="sxs-lookup"><span data-stu-id="60027-513">Value</span></span>|<span data-ttu-id="60027-514">Описание</span><span class="sxs-lookup"><span data-stu-id="60027-514">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="60027-515">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="60027-515">E_FAIL</span></span>  <br/> |<span data-ttu-id="60027-516">Нет дополнительных событий.</span><span class="sxs-lookup"><span data-stu-id="60027-516">There are no more events.</span></span>  <br/> |
|<span data-ttu-id="60027-517">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="60027-517">S_OK</span></span>  <br/> |<span data-ttu-id="60027-518">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="60027-518">The call was successful.</span></span>  <br/> |
   
#### <a name="ienumlsceventreset"></a><span data-ttu-id="60027-519">IEnumLSCEvent::Reset</span><span class="sxs-lookup"><span data-stu-id="60027-519">IEnumLSCEvent::Reset</span></span>

<span data-ttu-id="60027-520">Сбрасывает перечислитель для первого события.</span><span class="sxs-lookup"><span data-stu-id="60027-520">Resets the enumerator to the first event.</span></span>
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a><span data-ttu-id="60027-521">Параметры</span><span class="sxs-lookup"><span data-stu-id="60027-521">Parameters</span></span>

<span data-ttu-id="60027-522">Нет.</span><span class="sxs-lookup"><span data-stu-id="60027-522">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="60027-523">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-523">Return values</span></span>

<span data-ttu-id="60027-524">Всегда возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="60027-524">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent"></a><span data-ttu-id="60027-525">Интерфейс ILSCEvent</span><span class="sxs-lookup"><span data-stu-id="60027-525">Interface ILSCEvent</span></span>

<span data-ttu-id="60027-526">Этот интерфейс представляет событие синхронизации.</span><span class="sxs-lookup"><span data-stu-id="60027-526">This interface represents a synchronizing event.</span></span> <span data-ttu-id="60027-527">Все сведения о событии могут быть получены из интерфейса.</span><span class="sxs-lookup"><span data-stu-id="60027-527">All information about the event can be retrieved from the interface.</span></span>
  
<span data-ttu-id="60027-528">**Функции общих элементов**</span><span class="sxs-lookup"><span data-stu-id="60027-528">**Public member functions**</span></span>

#### <a name="ilsceventgetconflictstatus"></a><span data-ttu-id="60027-529">ILSCEvent::GetConflictStatus</span><span class="sxs-lookup"><span data-stu-id="60027-529">ILSCEvent::GetConflictStatus</span></span>

<span data-ttu-id="60027-530">Обратите внимание на то, что это значение заполняется при [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) вызывается, не в том случае, когда событие был создан, поэтому будут иметь только текущее состояние файла не состояние файла при изменении состояния конфликта.</span><span class="sxs-lookup"><span data-stu-id="60027-530">Note that this value is populated when [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) is called, not when the event was created, so you will only have the current status of the file, not the status of the file when the conflict status changed.</span></span> 
  
<span data-ttu-id="60027-531">Это значение заполняется только в том случае, когда [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnLocalConflictStateChanged.</span><span class="sxs-lookup"><span data-stu-id="60027-531">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnLocalConflictStateChanged.</span></span> 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a><span data-ttu-id="60027-532">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-532">Parameters</span></span>

 <span data-ttu-id="60027-533">_pfIsInConflict_</span><span class="sxs-lookup"><span data-stu-id="60027-533">_pfIsInConflict_</span></span>
  
<span data-ttu-id="60027-534">Текущее состояние конфликта файла, связанный с событием.</span><span class="sxs-lookup"><span data-stu-id="60027-534">The current conflict status of the file associated with the event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="60027-535">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-535">Return values</span></span>

<span data-ttu-id="60027-536">Всегда возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="60027-536">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeterror"></a><span data-ttu-id="60027-537">ILSCEvent::GetError</span><span class="sxs-lookup"><span data-stu-id="60027-537">ILSCEvent::GetError</span></span>

<span data-ttu-id="60027-538">Это значение заполняется только в том случае, когда [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="60027-538">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a><span data-ttu-id="60027-539">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-539">Parameters</span></span>

 <span data-ttu-id="60027-540">_pnError_</span><span class="sxs-lookup"><span data-stu-id="60027-540">_pnError_</span></span>
  
<span data-ttu-id="60027-541">Ошибка, связанный с данным событием.</span><span class="sxs-lookup"><span data-stu-id="60027-541">The error associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="60027-542">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-542">Return values</span></span>

<span data-ttu-id="60027-543">Всегда возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="60027-543">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetetag"></a><span data-ttu-id="60027-544">ILSCEvent::GetETag</span><span class="sxs-lookup"><span data-stu-id="60027-544">ILSCEvent::GetETag</span></span>

<span data-ttu-id="60027-545">Это значение заполняется только в том случае, когда [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="60027-545">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a><span data-ttu-id="60027-546">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-546">Parameters</span></span>

 <span data-ttu-id="60027-547">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="60027-547">_pbstrETag_</span></span>
  
<span data-ttu-id="60027-548">ETag, связанный с данным событием</span><span class="sxs-lookup"><span data-stu-id="60027-548">The ETag associated with this event</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="60027-549">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-549">Return values</span></span>

<span data-ttu-id="60027-550">Всегда возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="60027-550">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeteventtype"></a><span data-ttu-id="60027-551">ILSCEvent::GetEventType</span><span class="sxs-lookup"><span data-stu-id="60027-551">ILSCEvent::GetEventType</span></span>

<span data-ttu-id="60027-552">Получает тип для этого события.</span><span class="sxs-lookup"><span data-stu-id="60027-552">Gets the type for this event.</span></span>
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a><span data-ttu-id="60027-553">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-553">Parameters</span></span>

 <span data-ttu-id="60027-554">_pnEventType_</span><span class="sxs-lookup"><span data-stu-id="60027-554">_pnEventType_</span></span>
  
<span data-ttu-id="60027-555">Тип события это событие.</span><span class="sxs-lookup"><span data-stu-id="60027-555">The event type of this event.</span></span> <span data-ttu-id="60027-556">В разделе [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="60027-556">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for valid values.</span></span> <span data-ttu-id="60027-557">Не должно быть значение null.</span><span class="sxs-lookup"><span data-stu-id="60027-557">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="60027-558">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-558">Return values</span></span>

|<span data-ttu-id="60027-559">Значение</span><span class="sxs-lookup"><span data-stu-id="60027-559">Value</span></span>|<span data-ttu-id="60027-560">Описание</span><span class="sxs-lookup"><span data-stu-id="60027-560">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="60027-561">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="60027-561">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="60027-562">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="60027-562">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="60027-563">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="60027-563">S_OK</span></span>  <br/> |<span data-ttu-id="60027-564">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="60027-564">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a><span data-ttu-id="60027-565">ILSCEvent::GetLocalWorkingPath</span><span class="sxs-lookup"><span data-stu-id="60027-565">ILSCEvent::GetLocalWorkingPath</span></span>

<span data-ttu-id="60027-566">Возвращает локальный путь рабочее для этого события.</span><span class="sxs-lookup"><span data-stu-id="60027-566">Gets the local working path for this event.</span></span>
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a><span data-ttu-id="60027-567">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-567">Parameters</span></span>

 <span data-ttu-id="60027-568">_pbstrLocalWorkingPath_</span><span class="sxs-lookup"><span data-stu-id="60027-568">_pbstrLocalWorkingPath_</span></span>
  
<span data-ttu-id="60027-569">Локальный путь к файлу, к которому относится это событие.</span><span class="sxs-lookup"><span data-stu-id="60027-569">The local path of the file to which this event pertains.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="60027-570">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-570">Return values</span></span>

<span data-ttu-id="60027-571">Всегда возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="60027-571">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceid"></a><span data-ttu-id="60027-572">ILSCEvent::GetResourceID</span><span class="sxs-lookup"><span data-stu-id="60027-572">ILSCEvent::GetResourceID</span></span>

<span data-ttu-id="60027-573">Получает идентификатор ресурсов для события.</span><span class="sxs-lookup"><span data-stu-id="60027-573">Gets the resource ID for the event.</span></span>
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="60027-574">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-574">Parameters</span></span>

 <span data-ttu-id="60027-575">_pbstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="60027-575">_pbstrResourceID_</span></span>
  
<span data-ttu-id="60027-576">Ид_ресурса файла, связанного с данным событием.</span><span class="sxs-lookup"><span data-stu-id="60027-576">The ResourceID of the file associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="60027-577">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-577">Return values</span></span>

<span data-ttu-id="60027-578">Всегда возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="60027-578">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceidattempted"></a><span data-ttu-id="60027-579">ILSCEvent::GetResourceIDAttempted</span><span class="sxs-lookup"><span data-stu-id="60027-579">ILSCEvent::GetResourceIDAttempted</span></span>

<span data-ttu-id="60027-580">Это значение заполняется только в том случае, когда [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="60027-580">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> <span data-ttu-id="60027-581">Когда вызов [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)или [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) вызовет конфликт Web или локальный путь с другой файл кэша файлов Office, это генерируется событие.</span><span class="sxs-lookup"><span data-stu-id="60027-581">When a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) would cause a Web Path or Local Path collision with another file in the Office file cache, this event is generated.</span></span> 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a><span data-ttu-id="60027-582">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-582">Parameters</span></span>

 <span data-ttu-id="60027-583">_pbstrResourceIDAttempted_</span><span class="sxs-lookup"><span data-stu-id="60027-583">_pbstrResourceIDAttempted_</span></span>
  
<span data-ttu-id="60027-584">Ид_ресурса, вызвавшего это событие, чтобы получить созданные.</span><span class="sxs-lookup"><span data-stu-id="60027-584">The ResourceID that caused this event to get generated.</span></span> <span data-ttu-id="60027-585">Не должно быть значение null.</span><span class="sxs-lookup"><span data-stu-id="60027-585">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="60027-586">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-586">Return values</span></span>

<span data-ttu-id="60027-587">Всегда возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="60027-587">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetsyncerrortype"></a><span data-ttu-id="60027-588">ILSCEvent::GetSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="60027-588">ILSCEvent::GetSyncErrorType</span></span>

<span data-ttu-id="60027-589">Это значение заполняется только в том случае, когда [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="60027-589">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a><span data-ttu-id="60027-590">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-590">Parameters</span></span>

 <span data-ttu-id="60027-591">_pnSyncErrorType_</span><span class="sxs-lookup"><span data-stu-id="60027-591">_pnSyncErrorType_</span></span>
  
<span data-ttu-id="60027-592">Тип ошибки, связанный с данным событием.</span><span class="sxs-lookup"><span data-stu-id="60027-592">The error type associated with this event.</span></span> <span data-ttu-id="60027-593">В разделе [LSCEventType перечисление](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) возможных значений.</span><span class="sxs-lookup"><span data-stu-id="60027-593">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for potential values.</span></span> <span data-ttu-id="60027-594">Не должно быть значение null.</span><span class="sxs-lookup"><span data-stu-id="60027-594">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="60027-595">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-595">Return values</span></span>

|<span data-ttu-id="60027-596">Значение</span><span class="sxs-lookup"><span data-stu-id="60027-596">Value</span></span>|<span data-ttu-id="60027-597">Описание</span><span class="sxs-lookup"><span data-stu-id="60027-597">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="60027-598">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="60027-598">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="60027-599">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="60027-599">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="60027-600">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="60027-600">S_OK</span></span>  <br/> |<span data-ttu-id="60027-601">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="60027-601">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetwebpath"></a><span data-ttu-id="60027-602">ILSCEvent::GetWebPath</span><span class="sxs-lookup"><span data-stu-id="60027-602">ILSCEvent::GetWebPath</span></span>

<span data-ttu-id="60027-603">Это значение заполняется только в том случае, когда [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="60027-603">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a><span data-ttu-id="60027-604">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-604">Parameters</span></span>

 <span data-ttu-id="60027-605">_pbstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="60027-605">_pbstrWebPath_</span></span>
  
<span data-ttu-id="60027-606">Указывает веб-путь, связанный с данным событием.</span><span class="sxs-lookup"><span data-stu-id="60027-606">Specifies the Web Path associated with this event.</span></span> <span data-ttu-id="60027-607">Не должно быть значение null.</span><span class="sxs-lookup"><span data-stu-id="60027-607">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="60027-608">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-608">Return values</span></span>

<span data-ttu-id="60027-609">Всегда возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="60027-609">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent2"></a><span data-ttu-id="60027-610">Интерфейс ILSCEvent2</span><span class="sxs-lookup"><span data-stu-id="60027-610">Interface ILSCEvent2</span></span>

<span data-ttu-id="60027-611">Этот интерфейс содержит дополнительные сведения о синхронизации событий.</span><span class="sxs-lookup"><span data-stu-id="60027-611">This interface holds additional information about a synchronizing event.</span></span>
  
<span data-ttu-id="60027-612">**Функции общих элементов**</span><span class="sxs-lookup"><span data-stu-id="60027-612">**Public member functions**</span></span>

#### <a name="ilscevent2geterrorchain"></a><span data-ttu-id="60027-613">ILSCEvent2::GetErrorChain</span><span class="sxs-lookup"><span data-stu-id="60027-613">ILSCEvent2::GetErrorChain</span></span>

<span data-ttu-id="60027-614">Получает сведения об ошибке цепочки о синхронизации событий.</span><span class="sxs-lookup"><span data-stu-id="60027-614">Gets the error chain information about a synchronizing event.</span></span>
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a><span data-ttu-id="60027-615">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-615">Parameters</span></span>

 <span data-ttu-id="60027-616">_pbstrErrorChain_</span><span class="sxs-lookup"><span data-stu-id="60027-616">_pbstrErrorChain_</span></span>
  
<span data-ttu-id="60027-617">Строка для хранения цепочки сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="60027-617">A string to hold the error chain information.</span></span> <span data-ttu-id="60027-618">Не должно быть значение null.</span><span class="sxs-lookup"><span data-stu-id="60027-618">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="60027-619">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-619">Return values</span></span>

|<span data-ttu-id="60027-620">Значение</span><span class="sxs-lookup"><span data-stu-id="60027-620">Value</span></span>|<span data-ttu-id="60027-621">Описание</span><span class="sxs-lookup"><span data-stu-id="60027-621">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="60027-622">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="60027-622">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="60027-623">Установленная версия Office не поддерживает этот интерфейс</span><span class="sxs-lookup"><span data-stu-id="60027-623">The installed version of Office does not support this interface</span></span>  <br/> |
|<span data-ttu-id="60027-624">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="60027-624">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="60027-625">Одно или несколько значений параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="60027-625">One or more of the parameter values are invalid.</span></span>  <br/> |
|<span data-ttu-id="60027-626">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="60027-626">E_FAIL</span></span>  <br/> |<span data-ttu-id="60027-627">Сведения об ошибке цепочки недоступен.</span><span class="sxs-lookup"><span data-stu-id="60027-627">The error chain information is not available.</span></span>  <br/> |
|<span data-ttu-id="60027-628">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="60027-628">S_OK</span></span>  <br/> |<span data-ttu-id="60027-629">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="60027-629">The call was successful.</span></span>  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a><span data-ttu-id="60027-630">Интерфейс IPartnerActivityCallback</span><span class="sxs-lookup"><span data-stu-id="60027-630">Interface IPartnerActivityCallback</span></span>

<span data-ttu-id="60027-631">Этот интерфейс предоставляет функцию обратного вызова для CSISyncClient COM-объектом.</span><span class="sxs-lookup"><span data-stu-id="60027-631">This interface provides a callback function to the CSISyncClient COM object.</span></span>
  
<span data-ttu-id="60027-632">**Функции общих элементов**</span><span class="sxs-lookup"><span data-stu-id="60027-632">**Public member functions**</span></span>

#### <a name="ipartneractivitycallbackeventoccurred"></a><span data-ttu-id="60027-633">IPartnerActivityCallback::EventOccurred</span><span class="sxs-lookup"><span data-stu-id="60027-633">IPartnerActivityCallback::EventOccurred</span></span>

<span data-ttu-id="60027-634">Это функции обратного вызова на объект, заданный для CsiSyncClient COM-объектом.</span><span class="sxs-lookup"><span data-stu-id="60027-634">This is a callback function on the object given to the CsiSyncClient COM object.</span></span> <span data-ttu-id="60027-635">Предполагается, что при возникновении события (разделе [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) допустимых типов событий), CsiSyncClient COM-объектом будут вызывать этот метод, сигналов потребителем.</span><span class="sxs-lookup"><span data-stu-id="60027-635">It's expected that when an Event occurs (see [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid event types), the CsiSyncClient COM object will call this method, signalling the consumer.</span></span> 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a><span data-ttu-id="60027-636">Parameters</span><span class="sxs-lookup"><span data-stu-id="60027-636">Parameters</span></span>

 <span data-ttu-id="60027-637">_eEventTypeOccurred_</span><span class="sxs-lookup"><span data-stu-id="60027-637">_eEventTypeOccurred_</span></span>
  
<span data-ttu-id="60027-638">Тип события это событие.</span><span class="sxs-lookup"><span data-stu-id="60027-638">The event type of this event.</span></span> <span data-ttu-id="60027-639">В разделе [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="60027-639">See [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid values.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="60027-640">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="60027-640">Return values</span></span>

<span data-ttu-id="60027-641">Всегда возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="60027-641">Always returns S_OK.</span></span>
  
## <a name="enumerations"></a><span data-ttu-id="60027-642">Перечисления</span><span class="sxs-lookup"><span data-stu-id="60027-642">Enumerations</span></span>

<span data-ttu-id="60027-643">CSISyncClient использует следующие перечисления.</span><span class="sxs-lookup"><span data-stu-id="60027-643">CSISyncClient uses the following enumerations.</span></span>
  
### <a name="enum-lsceventsyncerrortype"></a><span data-ttu-id="60027-644">Enum LSCEventSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="60027-644">Enum LSCEventSyncErrorType</span></span>
<span data-ttu-id="60027-645"><a name="Enum_LSCEventSyncErrorType"> </a></span><span class="sxs-lookup"><span data-stu-id="60027-645"></span></span>

<span data-ttu-id="60027-646">Это перечисление определяет категории ошибок, которые могут возникнуть во время синхронизации в файл.</span><span class="sxs-lookup"><span data-stu-id="60027-646">This enumeration specifies the categories of errors that can occur while synchronizing a file.</span></span>
  
|<span data-ttu-id="60027-647">Перечислитель</span><span class="sxs-lookup"><span data-stu-id="60027-647">Enumerator</span></span>|<span data-ttu-id="60027-648">Описание</span><span class="sxs-lookup"><span data-stu-id="60027-648">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="60027-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span><span class="sxs-lookup"><span data-stu-id="60027-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span></span>  <br/> |<span data-ttu-id="60027-650">Ошибка синхронизации для этого события непредвиденное и может потребоваться особое внимание.</span><span class="sxs-lookup"><span data-stu-id="60027-650">The synchronizing error of this event was unexpected, and may require special consideration.</span></span> <span data-ttu-id="60027-651">По умолчанию пользователь может иметь предотвратить.</span><span class="sxs-lookup"><span data-stu-id="60027-651">By default, the user may have to intervene.</span></span>  <br/> |
|<span data-ttu-id="60027-652">LSCEventSyncErrorType_NoInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="60027-652">LSCEventSyncErrorType_NoInterventionRequired</span></span>  <br/> |<span data-ttu-id="60027-653">Ошибка синхронизации для этого события не обязательно особое внимание.</span><span class="sxs-lookup"><span data-stu-id="60027-653">The synchronizing error of this event does not need special consideration.</span></span> <span data-ttu-id="60027-654">Office будет обрабатывать его автоматически.</span><span class="sxs-lookup"><span data-stu-id="60027-654">Office will handle it automatically.</span></span>  <br/> |
|<span data-ttu-id="60027-655">LSCEventSyncErrorType_UserInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="60027-655">LSCEventSyncErrorType_UserInterventionRequired</span></span>  <br/> |<span data-ttu-id="60027-656">Ошибка синхронизации для этого события требуется пользователя ее решения.</span><span class="sxs-lookup"><span data-stu-id="60027-656">The synchronizing error of this event requires a user to resolve it.</span></span> <span data-ttu-id="60027-657">Ошибка конфликта объединения требуется пользователя для открытия документа и слияние его.</span><span class="sxs-lookup"><span data-stu-id="60027-657">For example, merge conflict error requires a user to open the document and merge it.</span></span>  <br/> |
|<span data-ttu-id="60027-658">LSCEventSyncErrorType_WaitingOnClient</span><span class="sxs-lookup"><span data-stu-id="60027-658">LSCEventSyncErrorType_WaitingOnClient</span></span>  <br/> |<span data-ttu-id="60027-659">Потребитель предотвратить, требует синхронизации ошибки это событие, но не требуют особое внимание пользователем.</span><span class="sxs-lookup"><span data-stu-id="60027-659">The synchronizing error of this event requires the consumer to intervene, but should not require special consideration by the user.</span></span>  <br/> |
|<span data-ttu-id="60027-660">LSCEventSyncErrorType_ClientInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="60027-660">LSCEventSyncErrorType_ClientInterventionRequired</span></span>  <br/> |<span data-ttu-id="60027-661">Ошибка синхронизации для этого события требуется потребитель предотвратить как особый случай.</span><span class="sxs-lookup"><span data-stu-id="60027-661">The synchronizing error of this event requires the consumer to intervene as a special case.</span></span>  <br/> |
|<span data-ttu-id="60027-662">LSCEventSyncErrorType_Max</span><span class="sxs-lookup"><span data-stu-id="60027-662">LSCEventSyncErrorType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtype"></a><span data-ttu-id="60027-663">Enum LSCEventType</span><span class="sxs-lookup"><span data-stu-id="60027-663">Enum LSCEventType</span></span>
<span data-ttu-id="60027-664"><a name="Enum_LSCEventType"> </a></span><span class="sxs-lookup"><span data-stu-id="60027-664"></span></span>

<span data-ttu-id="60027-665">Это перечисление указывает тип события, которые могут возникнуть для определенного файла.</span><span class="sxs-lookup"><span data-stu-id="60027-665">This enumeration specifies the type of events that can occur for a particular file.</span></span>
  
|<span data-ttu-id="60027-666">Перечислитель</span><span class="sxs-lookup"><span data-stu-id="60027-666">Enumerator</span></span>|<span data-ttu-id="60027-667">Описание</span><span class="sxs-lookup"><span data-stu-id="60027-667">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="60027-668">LSCEventType_None</span><span class="sxs-lookup"><span data-stu-id="60027-668">LSCEventType_None</span></span>  <br/> ||
|<span data-ttu-id="60027-669">LSCEventType_OnLocalChanges</span><span class="sxs-lookup"><span data-stu-id="60027-669">LSCEventType_OnLocalChanges</span></span>  <br/> |<span data-ttu-id="60027-670">Изменения были внесены в локальный файл.</span><span class="sxs-lookup"><span data-stu-id="60027-670">Changes were made to a local file.</span></span>  <br/> |
|<span data-ttu-id="60027-671">LSCEventType_OnOpenedByUser</span><span class="sxs-lookup"><span data-stu-id="60027-671">LSCEventType_OnOpenedByUser</span></span>  <br/> |<span data-ttu-id="60027-672">Пользователь может открыть файл.</span><span class="sxs-lookup"><span data-stu-id="60027-672">A user opened a file.</span></span>  <br/> |
|<span data-ttu-id="60027-673">LSCEventType_OnServerChangesDownloaded</span><span class="sxs-lookup"><span data-stu-id="60027-673">LSCEventType_OnServerChangesDownloaded</span></span>  <br/> |<span data-ttu-id="60027-674">Завершения загрузки изменений в файле с сервера.</span><span class="sxs-lookup"><span data-stu-id="60027-674">Finished downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="60027-675">LSCEventType_OnLocalChangesUploaded</span><span class="sxs-lookup"><span data-stu-id="60027-675">LSCEventType_OnLocalChangesUploaded</span></span>  <br/> |<span data-ttu-id="60027-676">Отправка изменений в файле на сервере завершена.</span><span class="sxs-lookup"><span data-stu-id="60027-676">Finished uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="60027-677">LSCEventType_OnLocalConflictStateChanged</span><span class="sxs-lookup"><span data-stu-id="60027-677">LSCEventType_OnLocalConflictStateChanged</span></span>  <br/> |<span data-ttu-id="60027-678">Состояние конфликта объединения файла был изменен.</span><span class="sxs-lookup"><span data-stu-id="60027-678">The merge conflict state of a file has changed.</span></span>  <br/> |
|<span data-ttu-id="60027-679">LSCEventType_OnFileAdded</span><span class="sxs-lookup"><span data-stu-id="60027-679">LSCEventType_OnFileAdded</span></span>  <br/> |<span data-ttu-id="60027-680">Файл был добавлен.</span><span class="sxs-lookup"><span data-stu-id="60027-680">A file was added.</span></span>  <br/> |
|<span data-ttu-id="60027-681">LSCEventType_OnFileDeleted</span><span class="sxs-lookup"><span data-stu-id="60027-681">LSCEventType_OnFileDeleted</span></span>  <br/> |<span data-ttu-id="60027-682">Файл был удален.</span><span class="sxs-lookup"><span data-stu-id="60027-682">A file was deleted.</span></span>  <br/> |
|<span data-ttu-id="60027-683">LSCEventType_OnSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="60027-683">LSCEventType_OnSyncEnabled</span></span>  <br/> |<span data-ttu-id="60027-684">Синхронизация была включена поддержка файлы пользователя.</span><span class="sxs-lookup"><span data-stu-id="60027-684">Synchronizing was enabled for a user's files.</span></span>  <br/> |
|<span data-ttu-id="60027-685">LSCEventType_OnServerChangesDownloadStarted</span><span class="sxs-lookup"><span data-stu-id="60027-685">LSCEventType_OnServerChangesDownloadStarted</span></span>  <br/> |<span data-ttu-id="60027-686">Начало загрузку изменений в файле с сервера.</span><span class="sxs-lookup"><span data-stu-id="60027-686">Started downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="60027-687">LSCEventType_OnLocalChangesUploadStarted</span><span class="sxs-lookup"><span data-stu-id="60027-687">LSCEventType_OnLocalChangesUploadStarted</span></span>  <br/> |<span data-ttu-id="60027-688">Первые шаги в отправке изменений в файле на сервер.</span><span class="sxs-lookup"><span data-stu-id="60027-688">Started uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="60027-689">LSCEventType_OnFilePathConflict</span><span class="sxs-lookup"><span data-stu-id="60027-689">LSCEventType_OnFilePathConflict</span></span>  <br/> |<span data-ttu-id="60027-690">Это событие создается при вызове [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)или [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) приводит к возникновению конфликта Web или локальный путь с другой файл в Кэш файлов Office.</span><span class="sxs-lookup"><span data-stu-id="60027-690">This event is generated when a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) causes a Web Path or Local Path collision with another file in the Office file cache.</span></span>  <br/> |
|<span data-ttu-id="60027-691">LSCEventType_OnFileForked</span><span class="sxs-lookup"><span data-stu-id="60027-691">LSCEventType_OnFileForked</span></span>  <br/> ||
|<span data-ttu-id="60027-692">LSCEventType_Max</span><span class="sxs-lookup"><span data-stu-id="60027-692">LSCEventType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a><span data-ttu-id="60027-693">Enum LSCEventTypeOccurred</span><span class="sxs-lookup"><span data-stu-id="60027-693">Enum LSCEventTypeOccurred</span></span>
<span data-ttu-id="60027-694"><a name="Enum_LSCEventTypeOccurred"> </a></span><span class="sxs-lookup"><span data-stu-id="60027-694"></span></span>

<span data-ttu-id="60027-695">Это перечисление указывает тип события, которые могут возникнуть.</span><span class="sxs-lookup"><span data-stu-id="60027-695">This enumeration specifies the type of events that can occur.</span></span> <span data-ttu-id="60027-696">Он должен вызова определенных функций ILSCLocalSyncClient на основе типа события.</span><span class="sxs-lookup"><span data-stu-id="60027-696">The consumer needs to call specific ILSCLocalSyncClient functions based on the event type.</span></span>
  
|<span data-ttu-id="60027-697">Перечислитель</span><span class="sxs-lookup"><span data-stu-id="60027-697">Enumerator</span></span>|<span data-ttu-id="60027-698">Описание</span><span class="sxs-lookup"><span data-stu-id="60027-698">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="60027-699">LSCEventTypeOccurred_GetChanges</span><span class="sxs-lookup"><span data-stu-id="60027-699">LSCEventTypeOccurred_GetChanges</span></span>  <br/> |<span data-ttu-id="60027-700">Произошла ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="60027-700">An ILSCEvent has occurred.</span></span> <span data-ttu-id="60027-701">Пользователь должен вызвать [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) для извлечения данных.</span><span class="sxs-lookup"><span data-stu-id="60027-701">The consumer should call [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) to retrieve the data.</span></span>  <br/> |
|<span data-ttu-id="60027-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="60027-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span></span>  <br/> |<span data-ttu-id="60027-703">Расширения имен файлов, поддерживаемые были изменены.</span><span class="sxs-lookup"><span data-stu-id="60027-703">The supported file extensions have changed.</span></span> <span data-ttu-id="60027-704">Пользователь должен вызвать [ILSCLocalSyncClient::GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) получить новый список поддерживаемых расширений.</span><span class="sxs-lookup"><span data-stu-id="60027-704">The consumer should call [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) to retrieve the new list of supported extensions.</span></span>  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a><span data-ttu-id="60027-705">Enum LSCNetworkSyncPermissionType</span><span class="sxs-lookup"><span data-stu-id="60027-705">Enum LSCNetworkSyncPermissionType</span></span>
<span data-ttu-id="60027-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span><span class="sxs-lookup"><span data-stu-id="60027-706"></span></span>

<span data-ttu-id="60027-707">Это перечисление указывает флаги, используемые для совет стоимость сети.</span><span class="sxs-lookup"><span data-stu-id="60027-707">This enumeration specifies the flags used for a network cost heuristic.</span></span> 

|<span data-ttu-id="60027-708">Перечислитель</span><span class="sxs-lookup"><span data-stu-id="60027-708">Enumerator</span></span>|<span data-ttu-id="60027-709">Описание</span><span class="sxs-lookup"><span data-stu-id="60027-709">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="60027-710">LSCNetworkSyncPermissionType_HighCost</span><span class="sxs-lookup"><span data-stu-id="60027-710">LSCNetworkSyncPermissionType_HighCost</span></span>  <br/> |<span data-ttu-id="60027-711">Значение true, если совет стоимость дорогостоящих сетей (например, 3 G) имеет преимущество.</span><span class="sxs-lookup"><span data-stu-id="60027-711">True if the cost heuristic for expensive networks (such as 3G) is overridden.</span></span>  <br/> |
|<span data-ttu-id="60027-712">LSCNetworkSyncPermissionType_HighPowerUsage</span><span class="sxs-lookup"><span data-stu-id="60027-712">LSCNetworkSyncPermissionType_HighPowerUsage</span></span>  <br/> |<span data-ttu-id="60027-713">Значение true, если совет затрат для использования power (например, батарей) имеет преимущество.</span><span class="sxs-lookup"><span data-stu-id="60027-713">True if the cost heuristic for power usage (such as a battery) is overridden.</span></span>  <br/> |
   
### <a name="enum-lscstatusflag"></a><span data-ttu-id="60027-714">Enum LSCStatusFlag</span><span class="sxs-lookup"><span data-stu-id="60027-714">Enum LSCStatusFlag</span></span>
<span data-ttu-id="60027-715"><a name="Enum_LSCStatusFlag"> </a></span><span class="sxs-lookup"><span data-stu-id="60027-715"></span></span>

<span data-ttu-id="60027-716">Это перечисление используется для представления состояния синхронизации файла.</span><span class="sxs-lookup"><span data-stu-id="60027-716">This enumeration is used to represent the synchronize status of a file.</span></span> 
  
|<span data-ttu-id="60027-717">Перечислитель</span><span class="sxs-lookup"><span data-stu-id="60027-717">Enumerator</span></span>|<span data-ttu-id="60027-718">Описание</span><span class="sxs-lookup"><span data-stu-id="60027-718">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="60027-719">LCSStatusFlag_None</span><span class="sxs-lookup"><span data-stu-id="60027-719">LCSStatusFlag_None</span></span>  <br/> ||
|<span data-ttu-id="60027-720">LSCStatusFlag_UploadPending</span><span class="sxs-lookup"><span data-stu-id="60027-720">LSCStatusFlag_UploadPending</span></span>  <br/> |<span data-ttu-id="60027-721">Значение true, если ожидает данных для отправки в файл сервера.</span><span class="sxs-lookup"><span data-stu-id="60027-721">True if there is pending data to send to the server file.</span></span>  <br/> |
|<span data-ttu-id="60027-722">LSCStatusFlag_DownloadPending</span><span class="sxs-lookup"><span data-stu-id="60027-722">LSCStatusFlag_DownloadPending</span></span>  <br/> |<span data-ttu-id="60027-723">Значение true, если ожидает данных для загрузки из файла сервера.</span><span class="sxs-lookup"><span data-stu-id="60027-723">True if there is pending data to download from the server file.</span></span>  <br/> |
|<span data-ttu-id="60027-724">LSCStatusFlag_LocalFileUnchanged</span><span class="sxs-lookup"><span data-stu-id="60027-724">LSCStatusFlag_LocalFileUnchanged</span></span>  <br/> |<span data-ttu-id="60027-725">Значение true, если данные Office на файл в кэш последнюю копию данных на диске.</span><span class="sxs-lookup"><span data-stu-id="60027-725">True if the data Office has on the file in its cache is the most recent copy of the data on disk.</span></span>  <br/> |
   

