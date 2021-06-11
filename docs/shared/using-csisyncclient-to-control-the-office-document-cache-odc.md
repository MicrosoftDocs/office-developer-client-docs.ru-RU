---
title: Использование CSISyncClient для управления кэшом Office документов (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Узнайте, как использовать CSISyncClient для управления кэшом Office документов (ODC).
ms.openlocfilehash: ce33063f88492bcd6f9682a4a6431fb36f138d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346258"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a><span data-ttu-id="beed3-103">Использование CSISyncClient для управления кэшом Office документов (ODC)</span><span class="sxs-lookup"><span data-stu-id="beed3-103">Using CSISyncClient to control the Office Document Cache (ODC)</span></span>

<span data-ttu-id="beed3-104">Узнайте, как использовать CSISyncClient для управления кэшом Office документов (ODC).</span><span class="sxs-lookup"><span data-stu-id="beed3-104">Learn how to use CSISyncClient to control the Office Document Cache (ODC).</span></span>
  
<span data-ttu-id="beed3-105">CSISyncClient — это сервер com(CsiSyncClient.exe), который позволяет Microsoft OneDrive управлять поведением кэша документов Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="beed3-105">CSISyncClient is an out-of-proc COM server (CsiSyncClient.exe) that allows Microsoft OneDrive to control the behavior of the Office Document Cache (ODC).</span></span> <span data-ttu-id="beed3-106">Например, OneDrive может вызвать ODC через CSISyncClient для загрузки файлов в конечные точки с включенной поддержкой MS-FSSHTTP и из нее.</span><span class="sxs-lookup"><span data-stu-id="beed3-106">For example, OneDrive may call upon the ODC via CSISyncClient to upload and download files to and from MS-FSSHTTP enabled endpoints.</span></span> <span data-ttu-id="beed3-107">Это позволяет использовать расширенные функции, Office службы, такие как совместное авторство и бесшовные переходы из автономного в online.</span><span class="sxs-lookup"><span data-stu-id="beed3-107">This enables advanced service-backed features in Office, such as co-authoring and seamless transitions from offline to online.</span></span>
  
<span data-ttu-id="beed3-108">CsiSyncClient доступен в Office Desktop (как x86, так и x64).</span><span class="sxs-lookup"><span data-stu-id="beed3-108">CsiSyncClient is available in Office Desktop (both x86 and x64).</span></span> <span data-ttu-id="beed3-109">Примечание. Хотя более новые версии Office могут быть отгрузка с CsiSyncClient, этот процесс будет использоваться только для обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="beed3-109">Note: While newer versions of Office may ship with CsiSyncClient, the process will be used for backward compatibility only.</span></span> <span data-ttu-id="beed3-110">Интерфейс CsiSyncClient и методология управления ODC изменятся в будущих версиях Office.</span><span class="sxs-lookup"><span data-stu-id="beed3-110">The CsiSyncClient interface and the methodology of controlling the ODC will change in future versions of Office.</span></span>
  
<span data-ttu-id="beed3-111">В настоящее время ID класса должен отвечать только на OneDrive.</span><span class="sxs-lookup"><span data-stu-id="beed3-111">The class ID is currently set to respond only to OneDrive.</span></span>
  
<span data-ttu-id="beed3-112">Объект COM может быть угодным в качестве неугодного com-сервера и выполняется в CsiSyncClient.exe.</span><span class="sxs-lookup"><span data-stu-id="beed3-112">The COM object is usable as an out-of-proc COM server and runs in CsiSyncClient.exe.</span></span> <span data-ttu-id="beed3-113">Из-за ограничений с Access (который использует ODC), он поставляется с типом бита, который Office входит, поэтому x64 Office означает объект x64 COM, или x86 Office означает объект x86 COM.</span><span class="sxs-lookup"><span data-stu-id="beed3-113">Due to limitations with Access (which the ODC uses), it ships with the bit type that Office comes in, so x64 Office means an x64 COM object, or x86 Office means an x86 COM object.</span></span> <span data-ttu-id="beed3-114">Чтобы обойти это ограничение, укажите CLSCTX_LOCAL_SERVER в качестве части CoCreateInstance будет иметь объект COM, который будет иметь возможность использовать com-сервер, который не является профессиональным com-сервером, что обеспечивает совместимость между битами.</span><span class="sxs-lookup"><span data-stu-id="beed3-114">To get around this limitation, specifying CLSCTX_LOCAL_SERVER as part of the CoCreateInstance will have the COM object be hosted as an out-of-proc COM server, allowing cross-bitness compatibility.</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="beed3-115">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="beed3-115">Interfaces</span></span>

<span data-ttu-id="beed3-116">CSISyncClient использует следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="beed3-116">CSISyncClient uses the following interfaces.</span></span>
  
### <a name="interface-ilsclocalsyncclient"></a><span data-ttu-id="beed3-117">Интерфейс ILSCLocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="beed3-117">Interface ILSCLocalSyncClient</span></span>

<span data-ttu-id="beed3-118">Это основной интерфейс, используемый для синхронизации файлов в Office.</span><span class="sxs-lookup"><span data-stu-id="beed3-118">This is the primary interface used to synchronize files in Office.</span></span>
  
- <span data-ttu-id="beed3-119">ProgID: Office. LocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="beed3-119">ProgID: Office.LocalSyncClient</span></span>
- <span data-ttu-id="beed3-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span><span class="sxs-lookup"><span data-stu-id="beed3-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span></span>
- <span data-ttu-id="beed3-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span><span class="sxs-lookup"><span data-stu-id="beed3-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span></span>
   
<span data-ttu-id="beed3-122">Объект COM, который подвергается воздействию, используется в качестве неавтономного сервера.</span><span class="sxs-lookup"><span data-stu-id="beed3-122">The COM object that is exposed is used as an out-of-proc server.</span></span> <span data-ttu-id="beed3-123">Указание CLSCTX_LOCAL_SERVER в составе CoCreateInstance позволяет совмесить между процессами 64bit и 32bit.</span><span class="sxs-lookup"><span data-stu-id="beed3-123">Specifying CLSCTX_LOCAL_SERVER as part of CoCreateInstance allows compatability between 64bit and 32bit processes.</span></span>
  
<span data-ttu-id="beed3-124">После совместной создания объекта COM необходимо сначала вызвать [ILSCLocalSyncClient::Initialize.](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)</span><span class="sxs-lookup"><span data-stu-id="beed3-124">Once you've co-created the COM object, you MUST call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) first.</span></span> <span data-ttu-id="beed3-125">После успешного завершения [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) любой API можно вызывать так часто, как вы хотите и в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="beed3-125">Once [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has completed successfully, you may call any API as often as you wish and in any order.</span></span> <span data-ttu-id="beed3-126">Вы также можете вызвать [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) на уже инициализированном объекте, но это ничего не делает.</span><span class="sxs-lookup"><span data-stu-id="beed3-126">You may also call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) on an already initialized object, but this does nothing.</span></span> 
  
<span data-ttu-id="beed3-127">Исключения из предыдущего абзаца: [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) и [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="beed3-127">The exceptions to the previous paragraph are [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) and [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="beed3-128">После вызова [ОБЪЕКТА ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) на объекте COM необходимо уничтожить этот объект и создать новый.</span><span class="sxs-lookup"><span data-stu-id="beed3-128">After you call [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) on the COM object, you MUST destroy that object and create a new one.</span></span> <span data-ttu-id="beed3-129">[ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) удаляет подкаченик, удаляет все связанные сведения о файле в кэше, но оставляет документы на диске.</span><span class="sxs-lookup"><span data-stu-id="beed3-129">[ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) will delete your subcache, delete all associated file information in the cache, but leave the documents on disk.</span></span> <span data-ttu-id="beed3-130">Он также оставляет состояние нетронутым для связи с кэшом.</span><span class="sxs-lookup"><span data-stu-id="beed3-130">It also leaves the state intact for communicating with the cache.</span></span> <span data-ttu-id="beed3-131">Это позволяет вызвать [ILSCLocalSyncClient:::Initialize, ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) чтобы создать новый кэш без необходимости уничтожения и воссоздания объекта COM.</span><span class="sxs-lookup"><span data-stu-id="beed3-131">This allows you to call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) again to create a new cache without having to destroy and recreate the COM object.</span></span> 
  
<span data-ttu-id="beed3-132">**Функции общедоступных членов**</span><span class="sxs-lookup"><span data-stu-id="beed3-132">**Public member functions**</span></span>

#### <a name="ilsclocalsyncclientdeletefile"></a><span data-ttu-id="beed3-133">ILSCLocalSyncClient::D eleteFile</span><span class="sxs-lookup"><span data-stu-id="beed3-133">ILSCLocalSyncClient::DeleteFile</span></span>

<span data-ttu-id="beed3-134">DeleteFile используется для удаления данных файлов из кэша.</span><span class="sxs-lookup"><span data-stu-id="beed3-134">DeleteFile is used to remove the file information from the cache.</span></span> <span data-ttu-id="beed3-135">Однако этот метод оставит связанный файл на диске и на сервере.</span><span class="sxs-lookup"><span data-stu-id="beed3-135">However, this method will leave the associated file on disk and on the server.</span></span>
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="beed3-136">Parameters</span><span class="sxs-lookup"><span data-stu-id="beed3-136">Parameters</span></span>

 <span data-ttu-id="beed3-137">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="beed3-137">_bstrResourceID_</span></span>
  
<span data-ttu-id="beed3-138">Строка, определяемая ResourceID файла.</span><span class="sxs-lookup"><span data-stu-id="beed3-138">The string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="beed3-139">Это значение должно быть непустым с максимальным значением 128 символов.</span><span class="sxs-lookup"><span data-stu-id="beed3-139">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="beed3-140">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-140">Return values</span></span>

|<span data-ttu-id="beed3-141">Значение</span><span class="sxs-lookup"><span data-stu-id="beed3-141">Value</span></span>|<span data-ttu-id="beed3-142">Описание</span><span class="sxs-lookup"><span data-stu-id="beed3-142">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="beed3-143">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="beed3-143">E_FAIL</span></span>  <br/> |<span data-ttu-id="beed3-144">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="beed3-144">The call failed.</span></span>  <br/> |
|<span data-ttu-id="beed3-145">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="beed3-145">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="beed3-146">Один или несколько параметров являются недействительными.</span><span class="sxs-lookup"><span data-stu-id="beed3-146">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="beed3-147">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="beed3-147">E_FAIL</span></span>  <br/> |<span data-ttu-id="beed3-148">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="beed3-148">The call failed.</span></span>  <br/> |
|<span data-ttu-id="beed3-149">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="beed3-149">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="beed3-150">Данный ResourceID не находится в кэше.</span><span class="sxs-lookup"><span data-stu-id="beed3-150">The given ResourceID is not in the cache.</span></span>  <br/> |
|<span data-ttu-id="beed3-151">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="beed3-151">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="beed3-152">Initialize не была успешно вызвана в прошлом.</span><span class="sxs-lookup"><span data-stu-id="beed3-152">Initialize has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="beed3-153">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="beed3-153">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="beed3-154">В настоящее время файл синхронизируется или открыт и не может быть удален.</span><span class="sxs-lookup"><span data-stu-id="beed3-154">The file is currently synchronizing or open and cannot be deleted.</span></span>  <br/> |
|<span data-ttu-id="beed3-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="beed3-155">S_OK</span></span>  <br/> |<span data-ttu-id="beed3-156">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="beed3-156">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a><span data-ttu-id="beed3-157">ILSCLocalSyncClient::GetChanges</span><span class="sxs-lookup"><span data-stu-id="beed3-157">ILSCLocalSyncClient::GetChanges</span></span>
<span data-ttu-id="beed3-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span><span class="sxs-lookup"><span data-stu-id="beed3-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span></span>

<span data-ttu-id="beed3-159">GetChanges возвращает объекты ILSCEvent, а также возвращает маркер, который будет передан следующему вызову в GetChanges, если предположить, что потребитель обработал предыдущий набор событий.</span><span class="sxs-lookup"><span data-stu-id="beed3-159">GetChanges returns an enumerator of ILSCEvent objects, and also returns a token that is given to the next call to GetChanges, assuming the consumer has processed the previous set of events.</span></span> <span data-ttu-id="beed3-160">События перед  _указанным nPreviousChangesToken_ будут удалены и недоступны.</span><span class="sxs-lookup"><span data-stu-id="beed3-160">Events before the  _nPreviousChangesToken_ specified will be deleted and unavailable.</span></span> <span data-ttu-id="beed3-161">Если события не будут обработаны,  _pnCurrentChangesToken_ должен иметь то же значение, что  _и nPreviousChangesToken,_ но  _ppiEvents_ все равно будет задат.</span><span class="sxs-lookup"><span data-stu-id="beed3-161">If there are no events to be processed,  _pnCurrentChangesToken_ should be the same value as  _nPreviousChangesToken_, but  _ppiEvents_ will still be set.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a><span data-ttu-id="beed3-162">Parameters</span><span class="sxs-lookup"><span data-stu-id="beed3-162">Parameters</span></span>

 <span data-ttu-id="beed3-163">_nPreviousChangesToken_</span><span class="sxs-lookup"><span data-stu-id="beed3-163">_nPreviousChangesToken_</span></span>
  
<span data-ttu-id="beed3-164">Определяет, какое событие в последний раз обрабатывалось потребителем.</span><span class="sxs-lookup"><span data-stu-id="beed3-164">Identifies which event was last processed by the consumer.</span></span> 
  
 <span data-ttu-id="beed3-165">_pnCurrentChangesToken_</span><span class="sxs-lookup"><span data-stu-id="beed3-165">_pnCurrentChangesToken_</span></span>
  
<span data-ttu-id="beed3-166">Определяет последнее событие, переданное потребителю.</span><span class="sxs-lookup"><span data-stu-id="beed3-166">Identifies the most recent event being handed to the consumer.</span></span> <span data-ttu-id="beed3-167">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="beed3-167">Must not be null.</span></span>
  
 <span data-ttu-id="beed3-168">_ppiEvents_</span><span class="sxs-lookup"><span data-stu-id="beed3-168">_ppiEvents_</span></span>
  
<span data-ttu-id="beed3-169">Переумывчик событий, переданных потребителю.</span><span class="sxs-lookup"><span data-stu-id="beed3-169">An enumerator for the events handed to the consumer.</span></span> <span data-ttu-id="beed3-170">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="beed3-170">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="beed3-171">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-171">Return values</span></span>

|<span data-ttu-id="beed3-172">Значение</span><span class="sxs-lookup"><span data-stu-id="beed3-172">Value</span></span>|<span data-ttu-id="beed3-173">Описание</span><span class="sxs-lookup"><span data-stu-id="beed3-173">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="beed3-174">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="beed3-174">E_FAIL</span></span>  <br/> |<span data-ttu-id="beed3-175">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="beed3-175">The call failed.</span></span>  <br/> |
|<span data-ttu-id="beed3-176">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="beed3-176">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="beed3-177">Один или несколько параметров являются недействительными.</span><span class="sxs-lookup"><span data-stu-id="beed3-177">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="beed3-178">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="beed3-178">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="beed3-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="beed3-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="beed3-180">S_OK</span><span class="sxs-lookup"><span data-stu-id="beed3-180">S_OK</span></span>  <br/> |<span data-ttu-id="beed3-181">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="beed3-181">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a><span data-ttu-id="beed3-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="beed3-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span></span>

<span data-ttu-id="beed3-183">GetClientNetworkSyncPermission используется для запроса, Office ли Office синхронизации с сетевыми затратами и использованием электроэнергии.</span><span class="sxs-lookup"><span data-stu-id="beed3-183">GetClientNetworkSyncPermission is used to query whether Office's synchronizing heuristics for network cost and power usage are overridden.</span></span> <span data-ttu-id="beed3-184">При работе с 3G или другой дорогостояной сетью или при работе с аккумулятором в сравнении с подключением Office может заблокировать сетевой трафик до более подходящих периодов времени.</span><span class="sxs-lookup"><span data-stu-id="beed3-184">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span>
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a><span data-ttu-id="beed3-185">Parameters</span><span class="sxs-lookup"><span data-stu-id="beed3-185">Parameters</span></span>

 <span data-ttu-id="beed3-186">_nspType_</span><span class="sxs-lookup"><span data-stu-id="beed3-186">_nspType_</span></span>
  
<span data-ttu-id="beed3-187">Флаг, определяющий, какие затраты на запрос.</span><span class="sxs-lookup"><span data-stu-id="beed3-187">A flag which defines which cost heuristic to query.</span></span> <span data-ttu-id="beed3-188">См. [enum LSCNetworkSyncPermissionType.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType)</span><span class="sxs-lookup"><span data-stu-id="beed3-188">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span> 
  
 <span data-ttu-id="beed3-189">_pfSyncEnabled_</span><span class="sxs-lookup"><span data-stu-id="beed3-189">_pfSyncEnabled_</span></span>
  
<span data-ttu-id="beed3-190">Указывает, переопределена ли в настоящее время запрашиваемая еуристическая стоимость.</span><span class="sxs-lookup"><span data-stu-id="beed3-190">Specifies whether the requested cost heuristic is currently overridden or not.</span></span> <span data-ttu-id="beed3-191">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="beed3-191">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="beed3-192">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-192">Return values</span></span>

|<span data-ttu-id="beed3-193">Значение</span><span class="sxs-lookup"><span data-stu-id="beed3-193">Value</span></span>|<span data-ttu-id="beed3-194">Описание</span><span class="sxs-lookup"><span data-stu-id="beed3-194">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="beed3-195">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="beed3-195">E_FAIL</span></span>  <br/> |<span data-ttu-id="beed3-196">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="beed3-196">The call failed.</span></span>  <br/> |
|<span data-ttu-id="beed3-197">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="beed3-197">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="beed3-198">Один или несколько параметров являются недействительными.</span><span class="sxs-lookup"><span data-stu-id="beed3-198">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="beed3-199">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="beed3-199">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="beed3-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="beed3-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="beed3-201">S_OK</span><span class="sxs-lookup"><span data-stu-id="beed3-201">S_OK</span></span>  <br/> |<span data-ttu-id="beed3-202">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="beed3-202">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a><span data-ttu-id="beed3-203">ILSCLocalSyncClient::GetFileStatus</span><span class="sxs-lookup"><span data-stu-id="beed3-203">ILSCLocalSyncClient::GetFileStatus</span></span>

<span data-ttu-id="beed3-204">GetFileStatus используется для сбора сведений для определенного файла: существует ли он в кэше, имеет ли он ожидающих связи с копией сервера и если Office 2013 г. имеет самые последние данные из локальной копии.</span><span class="sxs-lookup"><span data-stu-id="beed3-204">GetFileStatus is used to gather information for a specific file: whether it exists in the cache, if it has pending communication with the server copy, and if Office 2013 has the most up to date data from the local copy.</span></span> <span data-ttu-id="beed3-205">Для определения того, для каких сведений запрашивается объект CsiSyncClient COM, требуется флаг [Enum LSCStatusFlag.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag)</span><span class="sxs-lookup"><span data-stu-id="beed3-205">It requires a bitwise flag of [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) values to determine what information the CsiSyncClient COM object is to query for.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a><span data-ttu-id="beed3-206">Parameters</span><span class="sxs-lookup"><span data-stu-id="beed3-206">Parameters</span></span>

 <span data-ttu-id="beed3-207">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="beed3-207">_bstrResourceID_</span></span>
  
<span data-ttu-id="beed3-208">Строка, определяемая файлом клиента.</span><span class="sxs-lookup"><span data-stu-id="beed3-208">The string which identifies the file on the client.</span></span> <span data-ttu-id="beed3-209">Это значение должно быть не пустым, а не более 128 символов.</span><span class="sxs-lookup"><span data-stu-id="beed3-209">This value must be non-empty, with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="beed3-210">_sfRequestedStatus_</span><span class="sxs-lookup"><span data-stu-id="beed3-210">_sfRequestedStatus_</span></span>
  
<span data-ttu-id="beed3-211">Флаг, который определяет, какие сведения нужно возвращать.</span><span class="sxs-lookup"><span data-stu-id="beed3-211">A flag which defines what information to return.</span></span> <span data-ttu-id="beed3-212">См. [enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="beed3-212">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
 <span data-ttu-id="beed3-213">_pbstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="beed3-213">_pbstrFileSystemPath_</span></span>
  
<span data-ttu-id="beed3-214">Строка, которая определяет расположение файла, определяемого  _bstrResourceID_ на клиенте.</span><span class="sxs-lookup"><span data-stu-id="beed3-214">The string which identifies the location of the file identified by  _bstrResourceID_ on the client.</span></span> <span data-ttu-id="beed3-215">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="beed3-215">Must not be null.</span></span> 
  
 <span data-ttu-id="beed3-216">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="beed3-216">_pbstrETag_</span></span>
  
<span data-ttu-id="beed3-217">Строка, которая будет содержать eTag для файла, идентифицированного _bstrResourceID._</span><span class="sxs-lookup"><span data-stu-id="beed3-217">A string which will contain the eTag for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="beed3-218">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="beed3-218">Must not be null.</span></span> 
  
 <span data-ttu-id="beed3-219">_psfFileStatus_</span><span class="sxs-lookup"><span data-stu-id="beed3-219">_psfFileStatus_</span></span>
  
<span data-ttu-id="beed3-220">Флаг, который будет содержать состояние, запрашиваемого _с помощью sfRequestedStatus_ для файла, идентифицированного _bstrResourceID._</span><span class="sxs-lookup"><span data-stu-id="beed3-220">A flag which will contain the status requested via  _sfRequestedStatus_ for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="beed3-221">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="beed3-221">Must not be null.</span></span> <span data-ttu-id="beed3-222">См. [enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="beed3-222">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="beed3-223">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-223">Return values</span></span>

|<span data-ttu-id="beed3-224">Значение</span><span class="sxs-lookup"><span data-stu-id="beed3-224">Value</span></span>|<span data-ttu-id="beed3-225">Описание</span><span class="sxs-lookup"><span data-stu-id="beed3-225">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="beed3-226">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="beed3-226">E_FAIL</span></span>  <br/> |<span data-ttu-id="beed3-227">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="beed3-227">The call failed.</span></span>  <br/> |
|<span data-ttu-id="beed3-228">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="beed3-228">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="beed3-229">Один или несколько параметров являются недействительными.</span><span class="sxs-lookup"><span data-stu-id="beed3-229">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="beed3-230">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="beed3-230">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="beed3-231">Сведения о файлах, указанные  _bstrResourceID,_ не существуют в кэше.</span><span class="sxs-lookup"><span data-stu-id="beed3-231">The file information specified by  _bstrResourceID_ does not exist in the cache.</span></span>  <br/> |
|<span data-ttu-id="beed3-232">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="beed3-232">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="beed3-233">LSCStatusFlag_LocalFileUnchanged запросили или файл, указанный  _bstrResourceID,_ заблокирован или отсутствует.</span><span class="sxs-lookup"><span data-stu-id="beed3-233">LSCStatusFlag_LocalFileUnchanged was requested or the file specified by  _bstrResourceID_ is locked or missing.</span></span>  <br/> |
|<span data-ttu-id="beed3-234">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="beed3-234">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="beed3-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="beed3-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="beed3-236">S_OK</span><span class="sxs-lookup"><span data-stu-id="beed3-236">S_OK</span></span>  <br/> |<span data-ttu-id="beed3-237">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="beed3-237">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a><span data-ttu-id="beed3-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="beed3-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span></span>
<span data-ttu-id="beed3-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span><span class="sxs-lookup"><span data-stu-id="beed3-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span></span>

<span data-ttu-id="beed3-240">GetSupportedFileExtensions возвращает список расширений файлов, которые в настоящее время поддерживаются объектом CsiSyncClient COM.</span><span class="sxs-lookup"><span data-stu-id="beed3-240">GetSupportedFileExtensions returns a list of pipe-delimited file extensions which are currently supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="beed3-241">Обратите внимание, что этот список может измениться, и потребитель будет уведомлен об изменении с помощью объекта IPartnerActivityCallback, предоставленного в [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (см. eventOccured).</span><span class="sxs-lookup"><span data-stu-id="beed3-241">Note that this list may change, and the consumer will be notified of a change via the IPartnerActivityCallback object provided on [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (See EventOccured).</span></span> 
  
<span data-ttu-id="beed3-242">Пример возвращаемой строки: "|docx|docm|pptx|"</span><span class="sxs-lookup"><span data-stu-id="beed3-242">An example of the string returned is as follows: "|docx|docm|pptx|"</span></span>
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a><span data-ttu-id="beed3-243">Parameters</span><span class="sxs-lookup"><span data-stu-id="beed3-243">Parameters</span></span>

 <span data-ttu-id="beed3-244">_pbstrSupportedFileExtensions_</span><span class="sxs-lookup"><span data-stu-id="beed3-244">_pbstrSupportedFileExtensions_</span></span>
  
<span data-ttu-id="beed3-245">Строка, которая должна быть установлена с набором расширений файлов, поддерживаемых объектом CsiSyncClient COM.</span><span class="sxs-lookup"><span data-stu-id="beed3-245">A string to be set with a pipe-delimited set of file extensions supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="beed3-246">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="beed3-246">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="beed3-247">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-247">Return values</span></span>

|<span data-ttu-id="beed3-248">Значение</span><span class="sxs-lookup"><span data-stu-id="beed3-248">Value</span></span>|<span data-ttu-id="beed3-249">Описание</span><span class="sxs-lookup"><span data-stu-id="beed3-249">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="beed3-250">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="beed3-250">E_FAIL</span></span>  <br/> |<span data-ttu-id="beed3-251">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="beed3-251">The call failed.</span></span>  <br/> |
|<span data-ttu-id="beed3-252">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="beed3-252">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="beed3-253">Один или несколько параметров являются недействительными.</span><span class="sxs-lookup"><span data-stu-id="beed3-253">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="beed3-254">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="beed3-254">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="beed3-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="beed3-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="beed3-256">S_OK</span><span class="sxs-lookup"><span data-stu-id="beed3-256">S_OK</span></span>  <br/> |<span data-ttu-id="beed3-257">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="beed3-257">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a><span data-ttu-id="beed3-258">ILSCLocalSyncClient::Initialize</span><span class="sxs-lookup"><span data-stu-id="beed3-258">ILSCLocalSyncClient::Initialize</span></span>
<span data-ttu-id="beed3-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span><span class="sxs-lookup"><span data-stu-id="beed3-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span></span>

<span data-ttu-id="beed3-260">Инициализация должна быть первым вызванным методом.</span><span class="sxs-lookup"><span data-stu-id="beed3-260">Initialize must be the first method called.</span></span> <span data-ttu-id="beed3-261">В противном случае все другие API возвращаются E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="beed3-261">Otherwise, all other APIs will return E_LSC_NOTINITIALIZED.</span></span> <span data-ttu-id="beed3-262">Вызов Initialize на уже инициализированном объекте возвращает S_OK и ничего не делает.</span><span class="sxs-lookup"><span data-stu-id="beed3-262">Calling Initialize on an already initialized object returns S_OK and does nothing.</span></span> <span data-ttu-id="beed3-263">Если E_LSC_CACHEMISMATCH возвращается, вызываемая может вызвать [ILSCLocalSyncClient::ResetCache, ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) чтобы удалить кэш, связанный с данным SuppliedID.</span><span class="sxs-lookup"><span data-stu-id="beed3-263">If E_LSC_CACHEMISMATCH is returned, the caller may call [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) to delete the cache associated with the given SuppliedID.</span></span> <span data-ttu-id="beed3-264">Однако в этом случае другие API все равно будут возвращать E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="beed3-264">However, in this case other APIs will still return E_LSC_NOTINITIALIZED.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a><span data-ttu-id="beed3-265">Parameters</span><span class="sxs-lookup"><span data-stu-id="beed3-265">Parameters</span></span>

 <span data-ttu-id="beed3-266">_bstrSuppliedID_</span><span class="sxs-lookup"><span data-stu-id="beed3-266">_bstrSuppliedID_</span></span>
  
<span data-ttu-id="beed3-267">Определяет потребителя и какой кэш использовать.</span><span class="sxs-lookup"><span data-stu-id="beed3-267">Identifies the consumer and which cache to use.</span></span> <span data-ttu-id="beed3-268">Должно быть непустым с максимальной 32 символами.</span><span class="sxs-lookup"><span data-stu-id="beed3-268">Must be non-empty with a maximum of 32 characters.</span></span> 
  
 <span data-ttu-id="beed3-269">_bstrProgID_</span><span class="sxs-lookup"><span data-stu-id="beed3-269">_bstrProgID_</span></span>
  
<span data-ttu-id="beed3-270">Определяет объект COM потребителя для двуна пути связи.</span><span class="sxs-lookup"><span data-stu-id="beed3-270">Identifies the consumer's COM object for two-way communication.</span></span> <span data-ttu-id="beed3-271">Должно быть непустым с максимумом 39 символов.</span><span class="sxs-lookup"><span data-stu-id="beed3-271">Must be non-empty with a maximum of 39 characters.</span></span> <span data-ttu-id="beed3-272">Дополнительные сведения о progID-данных см. в [ \< \> progID-ключе.](https://docs.microsoft.com/windows/desktop/com/-progid--key)</span><span class="sxs-lookup"><span data-stu-id="beed3-272">See [\<ProgID\> Key](https://docs.microsoft.com/windows/desktop/com/-progid--key) for more information about ProgIDs.</span></span> 
  
 <span data-ttu-id="beed3-273">_bstrFileSystemDirectoryHint_</span><span class="sxs-lookup"><span data-stu-id="beed3-273">_bstrFileSystemDirectoryHint_</span></span>
  
<span data-ttu-id="beed3-274">Определяет корень каталога, в котором будут храниться локальные файлы.</span><span class="sxs-lookup"><span data-stu-id="beed3-274">Identifies the directory root in which local files will be stored.</span></span> <span data-ttu-id="beed3-275">Должно быть непустым с максимальным значением 256 символов.</span><span class="sxs-lookup"><span data-stu-id="beed3-275">Must be non-empty with a maximum of 256 characters.</span></span> <span data-ttu-id="beed3-276">Каталог уже должен существовать.</span><span class="sxs-lookup"><span data-stu-id="beed3-276">The directory must already exist.</span></span> 
  
 <span data-ttu-id="beed3-277">_pEventCallback_</span><span class="sxs-lookup"><span data-stu-id="beed3-277">_pEventCallback_</span></span>
  
<span data-ttu-id="beed3-278">Интерфейс вызова, который CsiSyncClient уведомит об изменениях.</span><span class="sxs-lookup"><span data-stu-id="beed3-278">The callback interface which CsiSyncClient will notify on changes.</span></span> <span data-ttu-id="beed3-279">См. iPartnerActivityCallback::EventOccurred.</span><span class="sxs-lookup"><span data-stu-id="beed3-279">See IPartnerActivityCallback::EventOccurred.</span></span> <span data-ttu-id="beed3-280">Это значение не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="beed3-280">This value must not be null.</span></span> 
  
 <span data-ttu-id="beed3-281">_pfCreatedNewCache_</span><span class="sxs-lookup"><span data-stu-id="beed3-281">_pfCreatedNewCache_</span></span>
  
<span data-ttu-id="beed3-282">Возвращает, был ли создан новый кэш.</span><span class="sxs-lookup"><span data-stu-id="beed3-282">Returns whether a new cache was created.</span></span> <span data-ttu-id="beed3-283">Если кэш не связан с SuppliedID, он будет создан.</span><span class="sxs-lookup"><span data-stu-id="beed3-283">If no cache is associated with the SuppliedID, one will be created.</span></span> <span data-ttu-id="beed3-284">Это значение не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="beed3-284">This value must not be null.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="beed3-285">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-285">Return values</span></span>

|<span data-ttu-id="beed3-286">Значение</span><span class="sxs-lookup"><span data-stu-id="beed3-286">Value</span></span>|<span data-ttu-id="beed3-287">Описание</span><span class="sxs-lookup"><span data-stu-id="beed3-287">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="beed3-288">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="beed3-288">E_FAIL</span></span>  <br/> |<span data-ttu-id="beed3-289">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="beed3-289">The call failed.</span></span>  <br/> |
|<span data-ttu-id="beed3-290">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="beed3-290">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="beed3-291">Один или несколько параметров являются недействительными.</span><span class="sxs-lookup"><span data-stu-id="beed3-291">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="beed3-292">E_LSC_CACHEMISMATCH</span><span class="sxs-lookup"><span data-stu-id="beed3-292">E_LSC_CACHEMISMATCH</span></span>  <br/> |<span data-ttu-id="beed3-293">В SuppliedID уже есть кэш, связанный с ним, но он отличается от предоставляемых ProgId или FileSystemDirectoryHint.</span><span class="sxs-lookup"><span data-stu-id="beed3-293">A SuppliedID already has a cache associated with it, but has a different ProgId or FileSystemDirectoryHint than the ones provided.</span></span>  <br/> |
|<span data-ttu-id="beed3-294">E_LSC_DIRECTORYHINTCONFLICT</span><span class="sxs-lookup"><span data-stu-id="beed3-294">E_LSC_DIRECTORYHINTCONFLICT</span></span>  <br/> |<span data-ttu-id="beed3-295">Файл FileSystemDirectoryHint (или поддвектор) уже существует в другом кэше.</span><span class="sxs-lookup"><span data-stu-id="beed3-295">The FileSystemDirectoryHint (or a subfolder) already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="beed3-296">E_LAC_PROGIDCONFLICT</span><span class="sxs-lookup"><span data-stu-id="beed3-296">E_LAC_PROGIDCONFLICT</span></span>  <br/> |<span data-ttu-id="beed3-297">ProgID уже существует в другом кэше.</span><span class="sxs-lookup"><span data-stu-id="beed3-297">The ProgID already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="beed3-298">S_OK</span><span class="sxs-lookup"><span data-stu-id="beed3-298">S_OK</span></span>  <br/> |<span data-ttu-id="beed3-299">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="beed3-299">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a><span data-ttu-id="beed3-300">ILSCLocalSyncClient::LocalFileChange</span><span class="sxs-lookup"><span data-stu-id="beed3-300">ILSCLocalSyncClient::LocalFileChange</span></span>
<span data-ttu-id="beed3-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="beed3-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span></span>

<span data-ttu-id="beed3-302">LocalFileChange используется для отправки указанного файла в объект CsiSyncClient COM.</span><span class="sxs-lookup"><span data-stu-id="beed3-302">LocalFileChange is used to tell the CsiSyncClient COM object to attempt to upload the specified file.</span></span> <span data-ttu-id="beed3-303">Метод подготовит файл к отправке, включая чтение текущего содержимого файла.</span><span class="sxs-lookup"><span data-stu-id="beed3-303">The method will prepare the file for upload, including reading the file's current contents.</span></span> <span data-ttu-id="beed3-304">Если отправка уже не завершена, предыдущая загрузка будет отброшена и новое содержимое будет подготовлено к отправке.</span><span class="sxs-lookup"><span data-stu-id="beed3-304">If an upload is already pending, the previous upload will be discarded and the new contents prepared for upload.</span></span> <span data-ttu-id="beed3-305">Если файл открыт для редактирования в приложении, этот метод возвращается S_OK без подготовки файла к отправке (приложение уже должно сделать этот шаг, если есть изменения).</span><span class="sxs-lookup"><span data-stu-id="beed3-305">If the file is open for editing in an application, this method will return S_OK without preparing the file for upload (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="beed3-306">Этот метод позволит загружать, если он был отмечен как заблокированные ранее загрузки (см. [ilSCLocalSyncClient::RenameFile). ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)</span><span class="sxs-lookup"><span data-stu-id="beed3-306">This method will allow uploads if it was marked as uploads blocked previously (see [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span></span>
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="beed3-307">Parameters</span><span class="sxs-lookup"><span data-stu-id="beed3-307">Parameters</span></span>

 <span data-ttu-id="beed3-308">_bstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="beed3-308">_bstrFileSystemPath_</span></span>
  
<span data-ttu-id="beed3-309">Строка, идентифицируемая с файлом клиента.</span><span class="sxs-lookup"><span data-stu-id="beed3-309">A string which identifies the file on the client.</span></span> <span data-ttu-id="beed3-310">Это значение должно быть непустым локальным путем с максимальным значением 256 символов.</span><span class="sxs-lookup"><span data-stu-id="beed3-310">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="beed3-311">Этот путь должен быть в дереве каталога, указанном FileSystemDirectoryHint при вызове [в ILSCLocalSyncClient::Initialize.](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize)</span><span class="sxs-lookup"><span data-stu-id="beed3-311">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was made.</span></span> 
  
 <span data-ttu-id="beed3-312">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="beed3-312">_bstrResourceID_</span></span>
  
<span data-ttu-id="beed3-313">Строка, определяемая ResourceID файла.</span><span class="sxs-lookup"><span data-stu-id="beed3-313">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="beed3-314">Это значение должно быть непустым с максимальным значением 128 символов.</span><span class="sxs-lookup"><span data-stu-id="beed3-314">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="beed3-315">_bstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="beed3-315">_bstrWebPath_</span></span>
  
<span data-ttu-id="beed3-316">Строка, идентифицирует файл на сервере.</span><span class="sxs-lookup"><span data-stu-id="beed3-316">A string which identifies the file on the server.</span></span> <span data-ttu-id="beed3-317">Это значение должно быть непустым, допустимым URL-адресом, но не более INTERNET_MAX_URL_LENGTH, как определено https://support.microsoft.com/kb/208427 .</span><span class="sxs-lookup"><span data-stu-id="beed3-317">This value must be non-empty, valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="beed3-318">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-318">Return values</span></span>

|<span data-ttu-id="beed3-319">Значение</span><span class="sxs-lookup"><span data-stu-id="beed3-319">Value</span></span>|<span data-ttu-id="beed3-320">Описание</span><span class="sxs-lookup"><span data-stu-id="beed3-320">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="beed3-321">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="beed3-321">E_FAIL</span></span>  <br/> |<span data-ttu-id="beed3-322">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="beed3-322">The call failed.</span></span>  <br/> |
|<span data-ttu-id="beed3-323">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="beed3-323">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="beed3-324">Один или несколько параметров являются недействительными.</span><span class="sxs-lookup"><span data-stu-id="beed3-324">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="beed3-325">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="beed3-325">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="beed3-326">Файл, указанный  _bstrFileSystemPath,_ имеет другой ResourceID, чем указанный.</span><span class="sxs-lookup"><span data-stu-id="beed3-326">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span> <span data-ttu-id="beed3-327">Событие типа LSCEventType_OnFilePathConflict при возвращении этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="beed3-327">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="beed3-328">См. [ilSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="beed3-328">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="beed3-329">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="beed3-329">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="beed3-330">Файл был удален в середине операции.</span><span class="sxs-lookup"><span data-stu-id="beed3-330">The file was deleted mid-operation.</span></span>  <br/> |
|<span data-ttu-id="beed3-331">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="beed3-331">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="beed3-332">Заданное расширение файла не поддерживается объектом CsiSyncClient COM.</span><span class="sxs-lookup"><span data-stu-id="beed3-332">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="beed3-333">См. [ilSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span><span class="sxs-lookup"><span data-stu-id="beed3-333">See [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span></span>  <br/> |
|<span data-ttu-id="beed3-334">E_LSC_FILEUPTODATE</span><span class="sxs-lookup"><span data-stu-id="beed3-334">E_LSC_FILEUPTODATE</span></span>  <br/> |<span data-ttu-id="beed3-335">Объект COM не запланировать отправку, так как в файле кэша произошли самые последние изменения с диска.</span><span class="sxs-lookup"><span data-stu-id="beed3-335">The COM object did not schedule an upload because the file in the cache had the most recent changes from the disk.</span></span>  <br/> |
|<span data-ttu-id="beed3-336">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="beed3-336">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="beed3-337">Файл, указанный  _bstrFileSystemPath,_ отсутствует или заблокирован.</span><span class="sxs-lookup"><span data-stu-id="beed3-337">The file specified by  _bstrFileSystemPath_ is missing or locked.</span></span>  <br/> |
|<span data-ttu-id="beed3-338">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="beed3-338">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="beed3-339">Данный FileSystemPath не находится под корнем каталога, заданным FileSystemDirectoryHint при вызове инициализации.</span><span class="sxs-lookup"><span data-stu-id="beed3-339">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="beed3-340">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="beed3-340">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="beed3-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="beed3-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="beed3-342">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="beed3-342">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="beed3-343">Файл, указанный  _bstrResourceID,_ отличается от указанного файла FileSystemPath.</span><span class="sxs-lookup"><span data-stu-id="beed3-343">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="beed3-344">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="beed3-344">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="beed3-345">Указанный файл уже имеет ожидающих изменений в другом кэше и пока не может быть связан с кэшом потребителя.</span><span class="sxs-lookup"><span data-stu-id="beed3-345">The file specified already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="beed3-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="beed3-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="beed3-347">Предоставляемый ВебПат попадает под другой кэш.</span><span class="sxs-lookup"><span data-stu-id="beed3-347">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="beed3-348">S_OK</span><span class="sxs-lookup"><span data-stu-id="beed3-348">S_OK</span></span>  <br/> |<span data-ttu-id="beed3-349">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="beed3-349">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a><span data-ttu-id="beed3-350">ILSCLocalSyncClient::RenameFile</span><span class="sxs-lookup"><span data-stu-id="beed3-350">ILSCLocalSyncClient::RenameFile</span></span>
<span data-ttu-id="beed3-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span><span class="sxs-lookup"><span data-stu-id="beed3-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span></span>

<span data-ttu-id="beed3-352">RenameFile будет связывать новый URL-адрес и локальный путь для данного ResourceID.</span><span class="sxs-lookup"><span data-stu-id="beed3-352">RenameFile will associate a new URL and local path for a given ResourceID.</span></span> <span data-ttu-id="beed3-353">Если файл, указанный ResourceID, еще не существует в кэше, будет предпринята попытка создать его и пометить его для скачивания.</span><span class="sxs-lookup"><span data-stu-id="beed3-353">If the file specified by the ResourceID doesn't already exist in the cache, an attempt will be made to create it and mark it for download.</span></span>
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a><span data-ttu-id="beed3-354">Parameters</span><span class="sxs-lookup"><span data-stu-id="beed3-354">Parameters</span></span>

 <span data-ttu-id="beed3-355">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="beed3-355">_bstrResourceID_</span></span>
  
<span data-ttu-id="beed3-356">Строка, определяемая ResourceID файла.</span><span class="sxs-lookup"><span data-stu-id="beed3-356">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="beed3-357">Это значение должно быть непустым с максимальным значением 128 символов.</span><span class="sxs-lookup"><span data-stu-id="beed3-357">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="beed3-358">_bstrNewFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="beed3-358">_bstrNewFileSystemPath_</span></span>
  
<span data-ttu-id="beed3-359">Строка, которая указывает новый локальный путь для файла.</span><span class="sxs-lookup"><span data-stu-id="beed3-359">A string which specifies the new local path for the file.</span></span> <span data-ttu-id="beed3-360">Это значение должно быть непустым локальным путем с максимальным значением 256 символов.</span><span class="sxs-lookup"><span data-stu-id="beed3-360">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="beed3-361">Этот путь должен быть в дереве каталога, указанном FileSystemDirectoryHint при вызове инициализации.</span><span class="sxs-lookup"><span data-stu-id="beed3-361">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span> 
  
 <span data-ttu-id="beed3-362">_bstrNewWebPath_</span><span class="sxs-lookup"><span data-stu-id="beed3-362">_bstrNewWebPath_</span></span>
  
<span data-ttu-id="beed3-363">Строка, которая указывает новый URL-адрес файла.</span><span class="sxs-lookup"><span data-stu-id="beed3-363">A string which specifies the new URL for the file.</span></span> <span data-ttu-id="beed3-364">Это значение должно быть непустым допустимым URL-адресом, но не более INTERNET_MAX_URL_LENGTH, как определено https://support.microsoft.com/kb/208427 .</span><span class="sxs-lookup"><span data-stu-id="beed3-364">This value must be non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
 <span data-ttu-id="beed3-365">_fBlockUploads_</span><span class="sxs-lookup"><span data-stu-id="beed3-365">_fBlockUploads_</span></span>
  
<span data-ttu-id="beed3-366">Указывает, разрешены ли в настоящее время загрузки в новое расположение.</span><span class="sxs-lookup"><span data-stu-id="beed3-366">Specifies whether uploads to the new location are allowed currently.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="beed3-367">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-367">Return values</span></span>

|<span data-ttu-id="beed3-368">Значение</span><span class="sxs-lookup"><span data-stu-id="beed3-368">Value</span></span>|<span data-ttu-id="beed3-369">Описание</span><span class="sxs-lookup"><span data-stu-id="beed3-369">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="beed3-370">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="beed3-370">E_FAIL</span></span>  <br/> |<span data-ttu-id="beed3-371">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="beed3-371">The call failed.</span></span>  <br/> |
|<span data-ttu-id="beed3-372">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="beed3-372">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="beed3-373">Один или несколько параметров являются недействительными.</span><span class="sxs-lookup"><span data-stu-id="beed3-373">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="beed3-374">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="beed3-374">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="beed3-375">_BstrNewFileSystemPath_ или _bstrNewWebPath_ уже существуют в другом файле в любом кэше.</span><span class="sxs-lookup"><span data-stu-id="beed3-375">The  _bstrNewFileSystemPath_ or  _bstrNewWebPath_ already exist on another file in any cache.</span></span> <span data-ttu-id="beed3-376">Событие типа LSCEventType_OnFilePathConflict при возвращении этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="beed3-376">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="beed3-377">См. [ilSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="beed3-377">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="beed3-378">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="beed3-378">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="beed3-379">Сведения о файле были удалены из кэша во время работы этого метода.</span><span class="sxs-lookup"><span data-stu-id="beed3-379">The file information was deleted from the cache while this method was running.</span></span>  <br/> |
|<span data-ttu-id="beed3-380">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="beed3-380">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="beed3-381">Данный FileSystemPath не находится под корнем каталога, заданным FileSystemDirectoryHint при вызове инициализации.</span><span class="sxs-lookup"><span data-stu-id="beed3-381">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="beed3-382">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="beed3-382">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="beed3-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="beed3-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="beed3-384">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="beed3-384">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="beed3-385">Указанный файл в настоящее время синхронизируется в Office приложении.</span><span class="sxs-lookup"><span data-stu-id="beed3-385">The file specified is currently synchronizing in an Office application.</span></span>  <br/> |
|<span data-ttu-id="beed3-386">S_OK</span><span class="sxs-lookup"><span data-stu-id="beed3-386">S_OK</span></span>  <br/> |<span data-ttu-id="beed3-387">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="beed3-387">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a><span data-ttu-id="beed3-388">ILSCLocalSyncClient::ResetCache</span><span class="sxs-lookup"><span data-stu-id="beed3-388">ILSCLocalSyncClient::ResetCache</span></span>
<span data-ttu-id="beed3-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span><span class="sxs-lookup"><span data-stu-id="beed3-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span></span>

<span data-ttu-id="beed3-390">ResetCache удаляет кэш, связанный с SuppliedID, который был предоставлен в Initialize.</span><span class="sxs-lookup"><span data-stu-id="beed3-390">ResetCache will delete the cache associated with the SuppliedID that was provided on Initialize.</span></span> <span data-ttu-id="beed3-391">Это включает всю информацию о файлах, но оставляет файлы как на клиенте, так и на сервере.</span><span class="sxs-lookup"><span data-stu-id="beed3-391">This includes all of the file information, but will leave the files on both the client and the server.</span></span> <span data-ttu-id="beed3-392">Этот метод также оставляет объект в частично ненициализованном состоянии.</span><span class="sxs-lookup"><span data-stu-id="beed3-392">This method also leaves the object in a partially uninitialized state.</span></span> <span data-ttu-id="beed3-393">Единственными допустимыми вызовами после этого являются [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) или [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="beed3-393">The only valid calls after this are [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) or [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="beed3-394">Этот метод может вызываться, если Initialize не удается и возвращает E_LSC_CACHEMISMATCH, и удаляет кэш, связанный с SuppliedID, который был предоставлен с ошибкой вызова.</span><span class="sxs-lookup"><span data-stu-id="beed3-394">This method MAY be called if Initialize fails and returns E_LSC_CACHEMISMATCH, and will delete the cache associated with the SuppliedID that was provided with the failing call.</span></span>
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a><span data-ttu-id="beed3-395">Параметры</span><span class="sxs-lookup"><span data-stu-id="beed3-395">Parameters</span></span>

<span data-ttu-id="beed3-396">Нет</span><span class="sxs-lookup"><span data-stu-id="beed3-396">None</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="beed3-397">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-397">Return values</span></span>

|<span data-ttu-id="beed3-398">Значение</span><span class="sxs-lookup"><span data-stu-id="beed3-398">Value</span></span>|<span data-ttu-id="beed3-399">Описание</span><span class="sxs-lookup"><span data-stu-id="beed3-399">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="beed3-400">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="beed3-400">E_FAIL</span></span>  <br/> |<span data-ttu-id="beed3-401">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="beed3-401">The call failed.</span></span>  <br/> |
|<span data-ttu-id="beed3-402">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="beed3-402">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="beed3-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="beed3-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was not successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="beed3-404">S_OK</span><span class="sxs-lookup"><span data-stu-id="beed3-404">S_OK</span></span>  <br/> |<span data-ttu-id="beed3-405">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="beed3-405">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a><span data-ttu-id="beed3-406">ILSCLocalSyncClient::ServerFileChange</span><span class="sxs-lookup"><span data-stu-id="beed3-406">ILSCLocalSyncClient::ServerFileChange</span></span>
<span data-ttu-id="beed3-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="beed3-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="beed3-408">ServerFileChange сообщает объекту CsiSyncClient COM пометить указанный файл для скачивания.</span><span class="sxs-lookup"><span data-stu-id="beed3-408">ServerFileChange tells the CsiSyncClient COM object to mark the specified file for download.</span></span> <span data-ttu-id="beed3-409">Если файл открыт в приложении Office для редактирования, этот метод возвращается S_OK без маркировки файла для скачивания (приложение уже должно сделать этот шаг, если есть изменения).</span><span class="sxs-lookup"><span data-stu-id="beed3-409">If the file is open in an Office application for edit, this method will return S_OK without marking the file for download (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="beed3-410">Этот метод позволит скачивать, если он был отмечен как заблокированные ранее загрузки (см. в нем RenameFile).</span><span class="sxs-lookup"><span data-stu-id="beed3-410">This method will allow downloads if it was marked as downloads blocked previously (see RenameFile).</span></span>
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="beed3-411">Параметры</span><span class="sxs-lookup"><span data-stu-id="beed3-411">Parameters</span></span>

|<span data-ttu-id="beed3-412">Параметр</span><span class="sxs-lookup"><span data-stu-id="beed3-412">Parameter</span></span>|<span data-ttu-id="beed3-413">Описание</span><span class="sxs-lookup"><span data-stu-id="beed3-413">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="beed3-414">bstrFileSystemPath</span><span class="sxs-lookup"><span data-stu-id="beed3-414">bstrFileSystemPath</span></span>  <br/> |<span data-ttu-id="beed3-415">Строка, идентифицируемая с файлом клиента.</span><span class="sxs-lookup"><span data-stu-id="beed3-415">A string which identifies the file on the client.</span></span> <span data-ttu-id="beed3-416">Это значение должно быть непустым локальным путем с максимальным значением 256 символов.</span><span class="sxs-lookup"><span data-stu-id="beed3-416">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="beed3-417">Этот путь должен быть в дереве каталога, указанном FileSystemDirectoryHint при вызове инициализации.</span><span class="sxs-lookup"><span data-stu-id="beed3-417">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="beed3-418">bstrResourceID</span><span class="sxs-lookup"><span data-stu-id="beed3-418">bstrResourceID</span></span>  <br/> |<span data-ttu-id="beed3-419">Строка, определяемая ResourceID файла.</span><span class="sxs-lookup"><span data-stu-id="beed3-419">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="beed3-420">Это значение должно быть непустым с максимальным значением 128 символов.</span><span class="sxs-lookup"><span data-stu-id="beed3-420">This value must be non-empty with a maximum of 128 characters.</span></span>  <br/> |
|<span data-ttu-id="beed3-421">bstrWebPath</span><span class="sxs-lookup"><span data-stu-id="beed3-421">bstrWebPath</span></span>  <br/> |<span data-ttu-id="beed3-422">Строка, идентифицирует файл на сервере.</span><span class="sxs-lookup"><span data-stu-id="beed3-422">A string which identifies the file on the server.</span></span> <span data-ttu-id="beed3-423">Это значение должно быть непустым допустимым URL-адресом, но не более INTERNET_MAX_URL_LENGTH, как определено https://support.microsoft.com/kb/208427 .</span><span class="sxs-lookup"><span data-stu-id="beed3-423">This value must be a non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span>  <br/> |
   
##### <a name="return-values"></a><span data-ttu-id="beed3-424">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-424">Return values</span></span>

|<span data-ttu-id="beed3-425">Значение</span><span class="sxs-lookup"><span data-stu-id="beed3-425">Value</span></span>|<span data-ttu-id="beed3-426">Описание</span><span class="sxs-lookup"><span data-stu-id="beed3-426">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="beed3-427">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="beed3-427">E_FAIL</span></span>  <br/> |<span data-ttu-id="beed3-428">Невозможность установить состояние подключения кэша.</span><span class="sxs-lookup"><span data-stu-id="beed3-428">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="beed3-429">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="beed3-429">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="beed3-430">Файл, указанный  _bstrFileSystemPath,_ имеет другой ResourceID, чем указанный.</span><span class="sxs-lookup"><span data-stu-id="beed3-430">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span>  <br/> |
|<span data-ttu-id="beed3-431">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="beed3-431">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="beed3-432">Заданное расширение файла не поддерживается объектом CsiSyncClient COM.</span><span class="sxs-lookup"><span data-stu-id="beed3-432">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="beed3-433">См. в рублях GetSupportedFileExtensions.</span><span class="sxs-lookup"><span data-stu-id="beed3-433">See GetSupportedFileExtensions.</span></span>  <br/> |
|<span data-ttu-id="beed3-434">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="beed3-434">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="beed3-435">Файл был удален в середине операции.</span><span class="sxs-lookup"><span data-stu-id="beed3-435">The file was deleted in mid-operation.</span></span>  <br/> |
|<span data-ttu-id="beed3-436">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="beed3-436">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="beed3-437">Один или несколько параметров являются недействительными.</span><span class="sxs-lookup"><span data-stu-id="beed3-437">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="beed3-438">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="beed3-438">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="beed3-439">Данный FileSystemPath не находится под корнем каталога, заданным FileSystemDirectoryHint при вызове инициализации.</span><span class="sxs-lookup"><span data-stu-id="beed3-439">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="beed3-440">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="beed3-440">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="beed3-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="beed3-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="beed3-442">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="beed3-442">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="beed3-443">Файл, указанный  _bstrResourceID,_ отличается от указанного файла FileSystemPath.</span><span class="sxs-lookup"><span data-stu-id="beed3-443">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="beed3-444">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="beed3-444">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="beed3-445">Указанный файл уже имеет ожидающих изменений в другом кэше и пока не может быть связан с кэшом потребителя.</span><span class="sxs-lookup"><span data-stu-id="beed3-445">The specified file already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="beed3-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="beed3-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="beed3-447">Предоставляемый ВебПат попадает под другой кэш.</span><span class="sxs-lookup"><span data-stu-id="beed3-447">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="beed3-448">S_OK</span><span class="sxs-lookup"><span data-stu-id="beed3-448">S_OK</span></span>  <br/> |<span data-ttu-id="beed3-449">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="beed3-449">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a><span data-ttu-id="beed3-450">ILSCLocalSyncClient::SetClientConnectivityState</span><span class="sxs-lookup"><span data-stu-id="beed3-450">ILSCLocalSyncClient::SetClientConnectivityState</span></span>
<span data-ttu-id="beed3-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="beed3-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="beed3-452">Задает кэш в состояние online или автономное.</span><span class="sxs-lookup"><span data-stu-id="beed3-452">Sets the cache into an online or offline state.</span></span> <span data-ttu-id="beed3-453">В автономном режиме Office не будет пытаться связываться с сервером для любых файлов в этом кэше, независимо от параметра _fBlockUploads_ каждого отдельного файла.</span><span class="sxs-lookup"><span data-stu-id="beed3-453">If offline, Office will not attempt to communicate with the server for any files in that cache, regardless of each individual file's  _fBlockUploads_ setting.</span></span> 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a><span data-ttu-id="beed3-454">Parameters</span><span class="sxs-lookup"><span data-stu-id="beed3-454">Parameters</span></span>

 <span data-ttu-id="beed3-455">_fIsOnline_</span><span class="sxs-lookup"><span data-stu-id="beed3-455">_fIsOnline_</span></span>
  
<span data-ttu-id="beed3-456">A boolean determining the connectivity state of the cache.</span><span class="sxs-lookup"><span data-stu-id="beed3-456">A boolean determining the connectivity state of the cache.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="beed3-457">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-457">Return values</span></span>

|<span data-ttu-id="beed3-458">Значение</span><span class="sxs-lookup"><span data-stu-id="beed3-458">Value</span></span>|<span data-ttu-id="beed3-459">Описание</span><span class="sxs-lookup"><span data-stu-id="beed3-459">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="beed3-460">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="beed3-460">E_FAIL</span></span>  <br/> |<span data-ttu-id="beed3-461">Невозможность установить состояние подключения кэша.</span><span class="sxs-lookup"><span data-stu-id="beed3-461">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="beed3-462">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="beed3-462">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="beed3-463">Один или несколько параметров являются недействительными.</span><span class="sxs-lookup"><span data-stu-id="beed3-463">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="beed3-464">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="beed3-464">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="beed3-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="beed3-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="beed3-466">S_OK</span><span class="sxs-lookup"><span data-stu-id="beed3-466">S_OK</span></span>  <br/> |<span data-ttu-id="beed3-467">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="beed3-467">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a><span data-ttu-id="beed3-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="beed3-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span></span>
<span data-ttu-id="beed3-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="beed3-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="beed3-470">SetClientNetworkSyncPermission используется для переопределения или восстановления синхронизации heuristicsOffice для затрат сети и использования электроэнергии.</span><span class="sxs-lookup"><span data-stu-id="beed3-470">SetClientNetworkSyncPermission is used to either override or restoreOffice's synchronizing heuristics for network cost and power usage.</span></span> <span data-ttu-id="beed3-471">При работе с 3G или другой дорогостояной сетью или при работе с аккумулятором в сравнении с подключением Office может заблокировать сетевой трафик до более подходящих периодов времени.</span><span class="sxs-lookup"><span data-stu-id="beed3-471">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span> <span data-ttu-id="beed3-472">Потребитель этого API может использовать его для переопределения Office и принудительной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="beed3-472">The consumer of this API can use it to override Office's heuristics and force synchronizing to occur.</span></span>
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a><span data-ttu-id="beed3-473">Parameters</span><span class="sxs-lookup"><span data-stu-id="beed3-473">Parameters</span></span>

 <span data-ttu-id="beed3-474">_nspType_</span><span class="sxs-lookup"><span data-stu-id="beed3-474">_nspType_</span></span>
  
<span data-ttu-id="beed3-475">Флаг, который определяет, какие затраты переопределять.</span><span class="sxs-lookup"><span data-stu-id="beed3-475">A flag which defines which cost heuristic to override.</span></span> <span data-ttu-id="beed3-476">См. [enum LSCNetworkSyncPermissionType.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType)</span><span class="sxs-lookup"><span data-stu-id="beed3-476">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span>
  
 <span data-ttu-id="beed3-477">_fEnableSync_</span><span class="sxs-lookup"><span data-stu-id="beed3-477">_fEnableSync_</span></span>
  
<span data-ttu-id="beed3-478">Указывает, следует ли принудить к синхронизации, переопределив таким образом эту стоимость, или больше не переопределять ее.</span><span class="sxs-lookup"><span data-stu-id="beed3-478">Specifies whether to force synchronizing on, thus overriding that cost heuristic, or to no longer override it.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="beed3-479">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-479">Return values</span></span>

|<span data-ttu-id="beed3-480">Значение</span><span class="sxs-lookup"><span data-stu-id="beed3-480">Value</span></span>|<span data-ttu-id="beed3-481">Описание</span><span class="sxs-lookup"><span data-stu-id="beed3-481">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="beed3-482">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="beed3-482">E_FAIL</span></span>  <br/> |<span data-ttu-id="beed3-483">Невыполнение переопределения синхронизации с юристией.</span><span class="sxs-lookup"><span data-stu-id="beed3-483">Failure to override synchronizing heuristics.</span></span>  <br/> |
|<span data-ttu-id="beed3-484">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="beed3-484">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="beed3-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="beed3-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="beed3-486">S_OK</span><span class="sxs-lookup"><span data-stu-id="beed3-486">S_OK</span></span>  <br/> |<span data-ttu-id="beed3-487">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="beed3-487">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a><span data-ttu-id="beed3-488">ILSCLocalSyncClient::Uninitialize</span><span class="sxs-lookup"><span data-stu-id="beed3-488">ILSCLocalSyncClient::Uninitialize</span></span>
<span data-ttu-id="beed3-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span><span class="sxs-lookup"><span data-stu-id="beed3-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span></span>

<span data-ttu-id="beed3-490">Выгружает кэш из объекта COM и выполняет операции закрытия.</span><span class="sxs-lookup"><span data-stu-id="beed3-490">Unloads the cache from the COM object and perform closing operations.</span></span> <span data-ttu-id="beed3-491">[ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) Необходимо вызволить объект COM перед уничтожением.</span><span class="sxs-lookup"><span data-stu-id="beed3-491">[ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUST be called before destroying the COM object.</span></span> <span data-ttu-id="beed3-492">После призыва никакие другие API не могут быть вызваны, объект COM должен быть уничтожен и создан новый, если вы хотите продолжить операции.</span><span class="sxs-lookup"><span data-stu-id="beed3-492">Once called, no other APIs can be called, the COM object MUST be destroyed and a new one created if you wish to continue operations.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a><span data-ttu-id="beed3-493">Параметры</span><span class="sxs-lookup"><span data-stu-id="beed3-493">Parameters</span></span>

<span data-ttu-id="beed3-494">Нет.</span><span class="sxs-lookup"><span data-stu-id="beed3-494">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="beed3-495">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-495">Return values</span></span>

|<span data-ttu-id="beed3-496">Значение</span><span class="sxs-lookup"><span data-stu-id="beed3-496">Value</span></span>|<span data-ttu-id="beed3-497">Описание</span><span class="sxs-lookup"><span data-stu-id="beed3-497">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="beed3-498">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="beed3-498">E_FAIL</span></span>  <br/> |<span data-ttu-id="beed3-499">Неунинициализация.</span><span class="sxs-lookup"><span data-stu-id="beed3-499">Failure to uninitialize.</span></span>  <br/> |
|<span data-ttu-id="beed3-500">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="beed3-500">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="beed3-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не был успешно вызван в прошлом.</span><span class="sxs-lookup"><span data-stu-id="beed3-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="beed3-502">S_OK</span><span class="sxs-lookup"><span data-stu-id="beed3-502">S_OK</span></span>  <br/> |<span data-ttu-id="beed3-503">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="beed3-503">The call succeeded.</span></span>  <br/> |
   
### <a name="interface-ienumlscevent"></a><span data-ttu-id="beed3-504">Интерфейс IEnumLSCEvent</span><span class="sxs-lookup"><span data-stu-id="beed3-504">Interface IEnumLSCEvent</span></span>

<span data-ttu-id="beed3-505">Этот интерфейс представляет список событий ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="beed3-505">This interface represents a list of ILSCEvent events.</span></span>
  
<span data-ttu-id="beed3-506">**Функции общедоступных членов**</span><span class="sxs-lookup"><span data-stu-id="beed3-506">**Public member functions**</span></span>

#### <a name="ienumlsceventfnext"></a><span data-ttu-id="beed3-507">IEnumLSCEvent::FNext</span><span class="sxs-lookup"><span data-stu-id="beed3-507">IEnumLSCEvent::FNext</span></span>

<span data-ttu-id="beed3-508">Извлекает следующее событие из списка событий.</span><span class="sxs-lookup"><span data-stu-id="beed3-508">Retrieves the next event from the list of events.</span></span>
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a><span data-ttu-id="beed3-509">Parameters</span><span class="sxs-lookup"><span data-stu-id="beed3-509">Parameters</span></span>

 <span data-ttu-id="beed3-510">_ppiLSCEvent_</span><span class="sxs-lookup"><span data-stu-id="beed3-510">_ppiLSCEvent_</span></span>
  
<span data-ttu-id="beed3-511">Указатель на интерфейс ILSCEvent.</span><span class="sxs-lookup"><span data-stu-id="beed3-511">A pointer to an ILSCEvent interface.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="beed3-512">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-512">Return values</span></span>

|<span data-ttu-id="beed3-513">Значение</span><span class="sxs-lookup"><span data-stu-id="beed3-513">Value</span></span>|<span data-ttu-id="beed3-514">Описание</span><span class="sxs-lookup"><span data-stu-id="beed3-514">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="beed3-515">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="beed3-515">E_FAIL</span></span>  <br/> |<span data-ttu-id="beed3-516">Больше нет событий.</span><span class="sxs-lookup"><span data-stu-id="beed3-516">There are no more events.</span></span>  <br/> |
|<span data-ttu-id="beed3-517">S_OK</span><span class="sxs-lookup"><span data-stu-id="beed3-517">S_OK</span></span>  <br/> |<span data-ttu-id="beed3-518">Вызов был успешным.</span><span class="sxs-lookup"><span data-stu-id="beed3-518">The call was successful.</span></span>  <br/> |
   
#### <a name="ienumlsceventreset"></a><span data-ttu-id="beed3-519">IEnumLSCEvent::Reset</span><span class="sxs-lookup"><span data-stu-id="beed3-519">IEnumLSCEvent::Reset</span></span>

<span data-ttu-id="beed3-520">Сбрасывает переустановку в первое событие.</span><span class="sxs-lookup"><span data-stu-id="beed3-520">Resets the enumerator to the first event.</span></span>
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a><span data-ttu-id="beed3-521">Параметры</span><span class="sxs-lookup"><span data-stu-id="beed3-521">Parameters</span></span>

<span data-ttu-id="beed3-522">Нет.</span><span class="sxs-lookup"><span data-stu-id="beed3-522">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="beed3-523">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-523">Return values</span></span>

<span data-ttu-id="beed3-524">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="beed3-524">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent"></a><span data-ttu-id="beed3-525">Интерфейс ILSCEvent</span><span class="sxs-lookup"><span data-stu-id="beed3-525">Interface ILSCEvent</span></span>

<span data-ttu-id="beed3-526">Этот интерфейс представляет событие синхронизации.</span><span class="sxs-lookup"><span data-stu-id="beed3-526">This interface represents a synchronizing event.</span></span> <span data-ttu-id="beed3-527">Вся информация о событии может быть извлечена из интерфейса.</span><span class="sxs-lookup"><span data-stu-id="beed3-527">All information about the event can be retrieved from the interface.</span></span>
  
<span data-ttu-id="beed3-528">**Функции общедоступных членов**</span><span class="sxs-lookup"><span data-stu-id="beed3-528">**Public member functions**</span></span>

#### <a name="ilsceventgetconflictstatus"></a><span data-ttu-id="beed3-529">ILSCEvent::GetConflictStatus</span><span class="sxs-lookup"><span data-stu-id="beed3-529">ILSCEvent::GetConflictStatus</span></span>

<span data-ttu-id="beed3-530">Обратите внимание, что это значение заполняется при назвав [ILSCLocalSyncClient::GetChanges, ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) а не в момент создания события, поэтому при смене состояния конфликта у вас будет только текущий статус файла, а не состояние файла.</span><span class="sxs-lookup"><span data-stu-id="beed3-530">Note that this value is populated when [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) is called, not when the event was created, so you will only have the current status of the file, not the status of the file when the conflict status changed.</span></span> 
  
<span data-ttu-id="beed3-531">Это значение заполняется только в том случае, если [значение Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnLocalConflictStateChanged.</span><span class="sxs-lookup"><span data-stu-id="beed3-531">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnLocalConflictStateChanged.</span></span> 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a><span data-ttu-id="beed3-532">Parameters</span><span class="sxs-lookup"><span data-stu-id="beed3-532">Parameters</span></span>

 <span data-ttu-id="beed3-533">_pfIsInConflict_</span><span class="sxs-lookup"><span data-stu-id="beed3-533">_pfIsInConflict_</span></span>
  
<span data-ttu-id="beed3-534">Текущее состояние конфликта файла, связанного с событием.</span><span class="sxs-lookup"><span data-stu-id="beed3-534">The current conflict status of the file associated with the event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="beed3-535">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-535">Return values</span></span>

<span data-ttu-id="beed3-536">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="beed3-536">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeterror"></a><span data-ttu-id="beed3-537">ILSCEvent::GetError</span><span class="sxs-lookup"><span data-stu-id="beed3-537">ILSCEvent::GetError</span></span>

<span data-ttu-id="beed3-538">Это значение заполняется только в том случае, если значение [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="beed3-538">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a><span data-ttu-id="beed3-539">Parameters</span><span class="sxs-lookup"><span data-stu-id="beed3-539">Parameters</span></span>

 <span data-ttu-id="beed3-540">_pnError_</span><span class="sxs-lookup"><span data-stu-id="beed3-540">_pnError_</span></span>
  
<span data-ttu-id="beed3-541">Ошибка, связанная с этим событием.</span><span class="sxs-lookup"><span data-stu-id="beed3-541">The error associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="beed3-542">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-542">Return values</span></span>

<span data-ttu-id="beed3-543">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="beed3-543">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetetag"></a><span data-ttu-id="beed3-544">ILSCEvent::GetETag</span><span class="sxs-lookup"><span data-stu-id="beed3-544">ILSCEvent::GetETag</span></span>

<span data-ttu-id="beed3-545">Это значение заполняется только в том случае, если значение [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="beed3-545">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a><span data-ttu-id="beed3-546">Parameters</span><span class="sxs-lookup"><span data-stu-id="beed3-546">Parameters</span></span>

 <span data-ttu-id="beed3-547">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="beed3-547">_pbstrETag_</span></span>
  
<span data-ttu-id="beed3-548">ETag, связанный с этим событием</span><span class="sxs-lookup"><span data-stu-id="beed3-548">The ETag associated with this event</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="beed3-549">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-549">Return values</span></span>

<span data-ttu-id="beed3-550">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="beed3-550">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeteventtype"></a><span data-ttu-id="beed3-551">ILSCEvent::GetEventType</span><span class="sxs-lookup"><span data-stu-id="beed3-551">ILSCEvent::GetEventType</span></span>

<span data-ttu-id="beed3-552">Получает тип для этого события.</span><span class="sxs-lookup"><span data-stu-id="beed3-552">Gets the type for this event.</span></span>
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a><span data-ttu-id="beed3-553">Parameters</span><span class="sxs-lookup"><span data-stu-id="beed3-553">Parameters</span></span>

 <span data-ttu-id="beed3-554">_pnEventType_</span><span class="sxs-lookup"><span data-stu-id="beed3-554">_pnEventType_</span></span>
  
<span data-ttu-id="beed3-555">Тип события этого события.</span><span class="sxs-lookup"><span data-stu-id="beed3-555">The event type of this event.</span></span> <span data-ttu-id="beed3-556">Для действительных значений см. в [enum LSCEventType.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType)</span><span class="sxs-lookup"><span data-stu-id="beed3-556">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for valid values.</span></span> <span data-ttu-id="beed3-557">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="beed3-557">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="beed3-558">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-558">Return values</span></span>

|<span data-ttu-id="beed3-559">Значение</span><span class="sxs-lookup"><span data-stu-id="beed3-559">Value</span></span>|<span data-ttu-id="beed3-560">Описание</span><span class="sxs-lookup"><span data-stu-id="beed3-560">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="beed3-561">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="beed3-561">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="beed3-562">Один или несколько параметров являются недействительными.</span><span class="sxs-lookup"><span data-stu-id="beed3-562">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="beed3-563">S_OK</span><span class="sxs-lookup"><span data-stu-id="beed3-563">S_OK</span></span>  <br/> |<span data-ttu-id="beed3-564">Вызов был успешным.</span><span class="sxs-lookup"><span data-stu-id="beed3-564">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a><span data-ttu-id="beed3-565">ILSCEvent::GetLocalWorkingPath</span><span class="sxs-lookup"><span data-stu-id="beed3-565">ILSCEvent::GetLocalWorkingPath</span></span>

<span data-ttu-id="beed3-566">Получает локальный рабочий путь для этого события.</span><span class="sxs-lookup"><span data-stu-id="beed3-566">Gets the local working path for this event.</span></span>
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a><span data-ttu-id="beed3-567">Parameters</span><span class="sxs-lookup"><span data-stu-id="beed3-567">Parameters</span></span>

 <span data-ttu-id="beed3-568">_pbstrLocalWorkingPath_</span><span class="sxs-lookup"><span data-stu-id="beed3-568">_pbstrLocalWorkingPath_</span></span>
  
<span data-ttu-id="beed3-569">Локальный путь файла, к которому относится это событие.</span><span class="sxs-lookup"><span data-stu-id="beed3-569">The local path of the file to which this event pertains.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="beed3-570">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-570">Return values</span></span>

<span data-ttu-id="beed3-571">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="beed3-571">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceid"></a><span data-ttu-id="beed3-572">ILSCEvent::GetResourceID</span><span class="sxs-lookup"><span data-stu-id="beed3-572">ILSCEvent::GetResourceID</span></span>

<span data-ttu-id="beed3-573">Получает ИД ресурса для события.</span><span class="sxs-lookup"><span data-stu-id="beed3-573">Gets the resource ID for the event.</span></span>
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="beed3-574">Parameters</span><span class="sxs-lookup"><span data-stu-id="beed3-574">Parameters</span></span>

 <span data-ttu-id="beed3-575">_pbstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="beed3-575">_pbstrResourceID_</span></span>
  
<span data-ttu-id="beed3-576">ResourceID файла, связанного с этим событием.</span><span class="sxs-lookup"><span data-stu-id="beed3-576">The ResourceID of the file associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="beed3-577">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-577">Return values</span></span>

<span data-ttu-id="beed3-578">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="beed3-578">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceidattempted"></a><span data-ttu-id="beed3-579">ILSCEvent::GetResourceIDAttempted</span><span class="sxs-lookup"><span data-stu-id="beed3-579">ILSCEvent::GetResourceIDAttempted</span></span>

<span data-ttu-id="beed3-580">Это значение заполняется только в том случае, если [значение Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="beed3-580">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> <span data-ttu-id="beed3-581">При вызове [в ILSCLocalSyncClient::LocalFileChange, ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange) [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)или [ILSCLocalSyncClient::RenameFi Office le](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) создается это событие.</span><span class="sxs-lookup"><span data-stu-id="beed3-581">When a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) would cause a Web Path or Local Path collision with another file in the Office file cache, this event is generated.</span></span> 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a><span data-ttu-id="beed3-582">Parameters</span><span class="sxs-lookup"><span data-stu-id="beed3-582">Parameters</span></span>

 <span data-ttu-id="beed3-583">_pbstrResourceIDAttempted_</span><span class="sxs-lookup"><span data-stu-id="beed3-583">_pbstrResourceIDAttempted_</span></span>
  
<span data-ttu-id="beed3-584">ResourceID, из-за чего произошло это событие.</span><span class="sxs-lookup"><span data-stu-id="beed3-584">The ResourceID that caused this event to get generated.</span></span> <span data-ttu-id="beed3-585">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="beed3-585">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="beed3-586">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-586">Return values</span></span>

<span data-ttu-id="beed3-587">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="beed3-587">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetsyncerrortype"></a><span data-ttu-id="beed3-588">ILSCEvent::GetSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="beed3-588">ILSCEvent::GetSyncErrorType</span></span>

<span data-ttu-id="beed3-589">Это значение заполняется только в том случае, если значение [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="beed3-589">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a><span data-ttu-id="beed3-590">Parameters</span><span class="sxs-lookup"><span data-stu-id="beed3-590">Parameters</span></span>

 <span data-ttu-id="beed3-591">_pnSyncErrorType_</span><span class="sxs-lookup"><span data-stu-id="beed3-591">_pnSyncErrorType_</span></span>
  
<span data-ttu-id="beed3-592">Тип ошибки, связанный с этим событием.</span><span class="sxs-lookup"><span data-stu-id="beed3-592">The error type associated with this event.</span></span> <span data-ttu-id="beed3-593">Потенциальные значения см. в [enum LSCEventType.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType)</span><span class="sxs-lookup"><span data-stu-id="beed3-593">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for potential values.</span></span> <span data-ttu-id="beed3-594">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="beed3-594">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="beed3-595">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-595">Return values</span></span>

|<span data-ttu-id="beed3-596">Значение</span><span class="sxs-lookup"><span data-stu-id="beed3-596">Value</span></span>|<span data-ttu-id="beed3-597">Описание</span><span class="sxs-lookup"><span data-stu-id="beed3-597">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="beed3-598">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="beed3-598">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="beed3-599">Один или несколько параметров являются недействительными.</span><span class="sxs-lookup"><span data-stu-id="beed3-599">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="beed3-600">S_OK</span><span class="sxs-lookup"><span data-stu-id="beed3-600">S_OK</span></span>  <br/> |<span data-ttu-id="beed3-601">Вызов был успешным.</span><span class="sxs-lookup"><span data-stu-id="beed3-601">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetwebpath"></a><span data-ttu-id="beed3-602">ILSCEvent::GetWebPath</span><span class="sxs-lookup"><span data-stu-id="beed3-602">ILSCEvent::GetWebPath</span></span>

<span data-ttu-id="beed3-603">Это значение заполняется только в том случае, если [значение Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="beed3-603">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a><span data-ttu-id="beed3-604">Parameters</span><span class="sxs-lookup"><span data-stu-id="beed3-604">Parameters</span></span>

 <span data-ttu-id="beed3-605">_pbstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="beed3-605">_pbstrWebPath_</span></span>
  
<span data-ttu-id="beed3-606">Указывает веб-путь, связанный с этим событием.</span><span class="sxs-lookup"><span data-stu-id="beed3-606">Specifies the Web Path associated with this event.</span></span> <span data-ttu-id="beed3-607">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="beed3-607">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="beed3-608">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-608">Return values</span></span>

<span data-ttu-id="beed3-609">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="beed3-609">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent2"></a><span data-ttu-id="beed3-610">Интерфейс ILSCEvent2</span><span class="sxs-lookup"><span data-stu-id="beed3-610">Interface ILSCEvent2</span></span>

<span data-ttu-id="beed3-611">Этот интерфейс содержит дополнительные сведения о событии синхронизации.</span><span class="sxs-lookup"><span data-stu-id="beed3-611">This interface holds additional information about a synchronizing event.</span></span>
  
<span data-ttu-id="beed3-612">**Функции общедоступных членов**</span><span class="sxs-lookup"><span data-stu-id="beed3-612">**Public member functions**</span></span>

#### <a name="ilscevent2geterrorchain"></a><span data-ttu-id="beed3-613">ILSCEvent2::GetErrorChain</span><span class="sxs-lookup"><span data-stu-id="beed3-613">ILSCEvent2::GetErrorChain</span></span>

<span data-ttu-id="beed3-614">Получает сведения о цепочке ошибок о событии синхронизации.</span><span class="sxs-lookup"><span data-stu-id="beed3-614">Gets the error chain information about a synchronizing event.</span></span>
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a><span data-ttu-id="beed3-615">Parameters</span><span class="sxs-lookup"><span data-stu-id="beed3-615">Parameters</span></span>

 <span data-ttu-id="beed3-616">_pbstrErrorChain_</span><span class="sxs-lookup"><span data-stu-id="beed3-616">_pbstrErrorChain_</span></span>
  
<span data-ttu-id="beed3-617">Строка для удержания сведений о цепочке ошибок.</span><span class="sxs-lookup"><span data-stu-id="beed3-617">A string to hold the error chain information.</span></span> <span data-ttu-id="beed3-618">Не должно быть null.</span><span class="sxs-lookup"><span data-stu-id="beed3-618">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="beed3-619">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-619">Return values</span></span>

|<span data-ttu-id="beed3-620">Значение</span><span class="sxs-lookup"><span data-stu-id="beed3-620">Value</span></span>|<span data-ttu-id="beed3-621">Описание</span><span class="sxs-lookup"><span data-stu-id="beed3-621">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="beed3-622">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="beed3-622">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="beed3-623">Установленная версия Office не поддерживает этот интерфейс</span><span class="sxs-lookup"><span data-stu-id="beed3-623">The installed version of Office does not support this interface</span></span>  <br/> |
|<span data-ttu-id="beed3-624">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="beed3-624">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="beed3-625">Одно или несколько значений параметров являются недействительными.</span><span class="sxs-lookup"><span data-stu-id="beed3-625">One or more of the parameter values are invalid.</span></span>  <br/> |
|<span data-ttu-id="beed3-626">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="beed3-626">E_FAIL</span></span>  <br/> |<span data-ttu-id="beed3-627">Сведения о цепочке ошибок недоступны.</span><span class="sxs-lookup"><span data-stu-id="beed3-627">The error chain information is not available.</span></span>  <br/> |
|<span data-ttu-id="beed3-628">S_OK</span><span class="sxs-lookup"><span data-stu-id="beed3-628">S_OK</span></span>  <br/> |<span data-ttu-id="beed3-629">Вызов был успешным.</span><span class="sxs-lookup"><span data-stu-id="beed3-629">The call was successful.</span></span>  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a><span data-ttu-id="beed3-630">Интерфейс IPartnerActivityCallback</span><span class="sxs-lookup"><span data-stu-id="beed3-630">Interface IPartnerActivityCallback</span></span>

<span data-ttu-id="beed3-631">Этот интерфейс предоставляет функцию вызова для объекта CSISyncClient COM.</span><span class="sxs-lookup"><span data-stu-id="beed3-631">This interface provides a callback function to the CSISyncClient COM object.</span></span>
  
<span data-ttu-id="beed3-632">**Функции общедоступных членов**</span><span class="sxs-lookup"><span data-stu-id="beed3-632">**Public member functions**</span></span>

#### <a name="ipartneractivitycallbackeventoccurred"></a><span data-ttu-id="beed3-633">IPartnerActivityCallback::EventOccurred</span><span class="sxs-lookup"><span data-stu-id="beed3-633">IPartnerActivityCallback::EventOccurred</span></span>

<span data-ttu-id="beed3-634">Это функция вызова на объекте, предоставленном объекту CsiSyncClient COM.</span><span class="sxs-lookup"><span data-stu-id="beed3-634">This is a callback function on the object given to the CsiSyncClient COM object.</span></span> <span data-ttu-id="beed3-635">Ожидается, что при событии (см. [enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) для допустимых типов событий) объект CsiSyncClient COM будет вызывать этот метод, сигнализая потребителю.</span><span class="sxs-lookup"><span data-stu-id="beed3-635">It's expected that when an Event occurs (see [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid event types), the CsiSyncClient COM object will call this method, signalling the consumer.</span></span> 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a><span data-ttu-id="beed3-636">Parameters</span><span class="sxs-lookup"><span data-stu-id="beed3-636">Parameters</span></span>

 <span data-ttu-id="beed3-637">_eEventTypeOccurred_</span><span class="sxs-lookup"><span data-stu-id="beed3-637">_eEventTypeOccurred_</span></span>
  
<span data-ttu-id="beed3-638">Тип события этого события.</span><span class="sxs-lookup"><span data-stu-id="beed3-638">The event type of this event.</span></span> <span data-ttu-id="beed3-639">Дополнительные значения см. в [enum LSCEventTypeOccurred.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred)</span><span class="sxs-lookup"><span data-stu-id="beed3-639">See [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid values.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="beed3-640">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="beed3-640">Return values</span></span>

<span data-ttu-id="beed3-641">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="beed3-641">Always returns S_OK.</span></span>
  
## <a name="enumerations"></a><span data-ttu-id="beed3-642">Перечисления</span><span class="sxs-lookup"><span data-stu-id="beed3-642">Enumerations</span></span>

<span data-ttu-id="beed3-643">CSISyncClient использует следующие переумерия.</span><span class="sxs-lookup"><span data-stu-id="beed3-643">CSISyncClient uses the following enumerations.</span></span>
  
### <a name="enum-lsceventsyncerrortype"></a><span data-ttu-id="beed3-644">Enum LSCEventSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="beed3-644">Enum LSCEventSyncErrorType</span></span>
<span data-ttu-id="beed3-645"><a name="Enum_LSCEventSyncErrorType"> </a></span><span class="sxs-lookup"><span data-stu-id="beed3-645"><a name="Enum_LSCEventSyncErrorType"> </a></span></span>

<span data-ttu-id="beed3-646">В этом переумехе указаны категории ошибок, которые могут возникать при синхронизации файла.</span><span class="sxs-lookup"><span data-stu-id="beed3-646">This enumeration specifies the categories of errors that can occur while synchronizing a file.</span></span>
  
|<span data-ttu-id="beed3-647">Enumerator</span><span class="sxs-lookup"><span data-stu-id="beed3-647">Enumerator</span></span>|<span data-ttu-id="beed3-648">Описание</span><span class="sxs-lookup"><span data-stu-id="beed3-648">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="beed3-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span><span class="sxs-lookup"><span data-stu-id="beed3-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span></span>  <br/> |<span data-ttu-id="beed3-650">Ошибка синхронизации этого события была неожиданной и может потребовать особого рассмотрения.</span><span class="sxs-lookup"><span data-stu-id="beed3-650">The synchronizing error of this event was unexpected, and may require special consideration.</span></span> <span data-ttu-id="beed3-651">По умолчанию пользователю может потребоваться вмешательство.</span><span class="sxs-lookup"><span data-stu-id="beed3-651">By default, the user may have to intervene.</span></span>  <br/> |
|<span data-ttu-id="beed3-652">LSCEventSyncErrorType_NoInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="beed3-652">LSCEventSyncErrorType_NoInterventionRequired</span></span>  <br/> |<span data-ttu-id="beed3-653">Ошибка синхронизации этого события не требует особого внимания.</span><span class="sxs-lookup"><span data-stu-id="beed3-653">The synchronizing error of this event does not need special consideration.</span></span> <span data-ttu-id="beed3-654">Office будет обрабатываться автоматически.</span><span class="sxs-lookup"><span data-stu-id="beed3-654">Office will handle it automatically.</span></span>  <br/> |
|<span data-ttu-id="beed3-655">LSCEventSyncErrorType_UserInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="beed3-655">LSCEventSyncErrorType_UserInterventionRequired</span></span>  <br/> |<span data-ttu-id="beed3-656">Ошибка синхронизации этого события требует от пользователя его устранения.</span><span class="sxs-lookup"><span data-stu-id="beed3-656">The synchronizing error of this event requires a user to resolve it.</span></span> <span data-ttu-id="beed3-657">Например, ошибка слияния конфликтов требует, чтобы пользователь открыл документ и слил его.</span><span class="sxs-lookup"><span data-stu-id="beed3-657">For example, merge conflict error requires a user to open the document and merge it.</span></span>  <br/> |
|<span data-ttu-id="beed3-658">LSCEventSyncErrorType_WaitingOnClient</span><span class="sxs-lookup"><span data-stu-id="beed3-658">LSCEventSyncErrorType_WaitingOnClient</span></span>  <br/> |<span data-ttu-id="beed3-659">Ошибка синхронизации этого события требует вмешательства пользователя, но не требует особого рассмотрения пользователем.</span><span class="sxs-lookup"><span data-stu-id="beed3-659">The synchronizing error of this event requires the consumer to intervene, but should not require special consideration by the user.</span></span>  <br/> |
|<span data-ttu-id="beed3-660">LSCEventSyncErrorType_ClientInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="beed3-660">LSCEventSyncErrorType_ClientInterventionRequired</span></span>  <br/> |<span data-ttu-id="beed3-661">Ошибка синхронизации этого события требует от потребителя вмешательства в качестве особого случая.</span><span class="sxs-lookup"><span data-stu-id="beed3-661">The synchronizing error of this event requires the consumer to intervene as a special case.</span></span>  <br/> |
|<span data-ttu-id="beed3-662">LSCEventSyncErrorType_Max</span><span class="sxs-lookup"><span data-stu-id="beed3-662">LSCEventSyncErrorType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtype"></a><span data-ttu-id="beed3-663">Enum LSCEventType</span><span class="sxs-lookup"><span data-stu-id="beed3-663">Enum LSCEventType</span></span>
<span data-ttu-id="beed3-664"><a name="Enum_LSCEventType"> </a></span><span class="sxs-lookup"><span data-stu-id="beed3-664"><a name="Enum_LSCEventType"> </a></span></span>

<span data-ttu-id="beed3-665">В этом переумехе указывается тип событий, которые могут произойти для конкретного файла.</span><span class="sxs-lookup"><span data-stu-id="beed3-665">This enumeration specifies the type of events that can occur for a particular file.</span></span>
  
|<span data-ttu-id="beed3-666">Enumerator</span><span class="sxs-lookup"><span data-stu-id="beed3-666">Enumerator</span></span>|<span data-ttu-id="beed3-667">Описание</span><span class="sxs-lookup"><span data-stu-id="beed3-667">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="beed3-668">LSCEventType_None</span><span class="sxs-lookup"><span data-stu-id="beed3-668">LSCEventType_None</span></span>  <br/> ||
|<span data-ttu-id="beed3-669">LSCEventType_OnLocalChanges</span><span class="sxs-lookup"><span data-stu-id="beed3-669">LSCEventType_OnLocalChanges</span></span>  <br/> |<span data-ttu-id="beed3-670">Изменения были внесены в локальный файл.</span><span class="sxs-lookup"><span data-stu-id="beed3-670">Changes were made to a local file.</span></span>  <br/> |
|<span data-ttu-id="beed3-671">LSCEventType_OnOpenedByUser</span><span class="sxs-lookup"><span data-stu-id="beed3-671">LSCEventType_OnOpenedByUser</span></span>  <br/> |<span data-ttu-id="beed3-672">Пользователь открыл файл.</span><span class="sxs-lookup"><span data-stu-id="beed3-672">A user opened a file.</span></span>  <br/> |
|<span data-ttu-id="beed3-673">LSCEventType_OnServerChangesDownloaded</span><span class="sxs-lookup"><span data-stu-id="beed3-673">LSCEventType_OnServerChangesDownloaded</span></span>  <br/> |<span data-ttu-id="beed3-674">Законченная загрузка файлов изменяется с сервера.</span><span class="sxs-lookup"><span data-stu-id="beed3-674">Finished downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="beed3-675">LSCEventType_OnLocalChangesUploaded</span><span class="sxs-lookup"><span data-stu-id="beed3-675">LSCEventType_OnLocalChangesUploaded</span></span>  <br/> |<span data-ttu-id="beed3-676">Законченная загрузка изменений файла на сервер.</span><span class="sxs-lookup"><span data-stu-id="beed3-676">Finished uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="beed3-677">LSCEventType_OnLocalConflictStateChanged</span><span class="sxs-lookup"><span data-stu-id="beed3-677">LSCEventType_OnLocalConflictStateChanged</span></span>  <br/> |<span data-ttu-id="beed3-678">Изменилось состояние конфликта слияния файла.</span><span class="sxs-lookup"><span data-stu-id="beed3-678">The merge conflict state of a file has changed.</span></span>  <br/> |
|<span data-ttu-id="beed3-679">LSCEventType_OnFileAdded</span><span class="sxs-lookup"><span data-stu-id="beed3-679">LSCEventType_OnFileAdded</span></span>  <br/> |<span data-ttu-id="beed3-680">Добавлен файл.</span><span class="sxs-lookup"><span data-stu-id="beed3-680">A file was added.</span></span>  <br/> |
|<span data-ttu-id="beed3-681">LSCEventType_OnFileDeleted</span><span class="sxs-lookup"><span data-stu-id="beed3-681">LSCEventType_OnFileDeleted</span></span>  <br/> |<span data-ttu-id="beed3-682">Файл был удален.</span><span class="sxs-lookup"><span data-stu-id="beed3-682">A file was deleted.</span></span>  <br/> |
|<span data-ttu-id="beed3-683">LSCEventType_OnSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="beed3-683">LSCEventType_OnSyncEnabled</span></span>  <br/> |<span data-ttu-id="beed3-684">Для файлов пользователя включена синхронизация.</span><span class="sxs-lookup"><span data-stu-id="beed3-684">Synchronizing was enabled for a user's files.</span></span>  <br/> |
|<span data-ttu-id="beed3-685">LSCEventType_OnServerChangesDownloadStarted</span><span class="sxs-lookup"><span data-stu-id="beed3-685">LSCEventType_OnServerChangesDownloadStarted</span></span>  <br/> |<span data-ttu-id="beed3-686">Начался скачивание изменений файла с сервера.</span><span class="sxs-lookup"><span data-stu-id="beed3-686">Started downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="beed3-687">LSCEventType_OnLocalChangesUploadStarted</span><span class="sxs-lookup"><span data-stu-id="beed3-687">LSCEventType_OnLocalChangesUploadStarted</span></span>  <br/> |<span data-ttu-id="beed3-688">Начался процесс загрузки изменений файла на сервер.</span><span class="sxs-lookup"><span data-stu-id="beed3-688">Started uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="beed3-689">LSCEventType_OnFilePathConflict</span><span class="sxs-lookup"><span data-stu-id="beed3-689">LSCEventType_OnFilePathConflict</span></span>  <br/> |<span data-ttu-id="beed3-690">Это событие создается при вызове [в ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)или [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) вызывает столкновение веб-пути или локального пути с другим файлом в кэше Office файла.</span><span class="sxs-lookup"><span data-stu-id="beed3-690">This event is generated when a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) causes a Web Path or Local Path collision with another file in the Office file cache.</span></span>  <br/> |
|<span data-ttu-id="beed3-691">LSCEventType_OnFileForked</span><span class="sxs-lookup"><span data-stu-id="beed3-691">LSCEventType_OnFileForked</span></span>  <br/> ||
|<span data-ttu-id="beed3-692">LSCEventType_Max</span><span class="sxs-lookup"><span data-stu-id="beed3-692">LSCEventType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a><span data-ttu-id="beed3-693">Enum LSCEventTypeOccurred</span><span class="sxs-lookup"><span data-stu-id="beed3-693">Enum LSCEventTypeOccurred</span></span>
<span data-ttu-id="beed3-694"><a name="Enum_LSCEventTypeOccurred"> </a></span><span class="sxs-lookup"><span data-stu-id="beed3-694"><a name="Enum_LSCEventTypeOccurred"> </a></span></span>

<span data-ttu-id="beed3-695">В этом переумехе указывается тип событий, которые могут произойти.</span><span class="sxs-lookup"><span data-stu-id="beed3-695">This enumeration specifies the type of events that can occur.</span></span> <span data-ttu-id="beed3-696">Потребителю необходимо вызвать определенные функции ILSCLocalSyncClient в зависимости от типа события.</span><span class="sxs-lookup"><span data-stu-id="beed3-696">The consumer needs to call specific ILSCLocalSyncClient functions based on the event type.</span></span>
  
|<span data-ttu-id="beed3-697">Enumerator</span><span class="sxs-lookup"><span data-stu-id="beed3-697">Enumerator</span></span>|<span data-ttu-id="beed3-698">Описание</span><span class="sxs-lookup"><span data-stu-id="beed3-698">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="beed3-699">LSCEventTypeOccurred_GetChanges</span><span class="sxs-lookup"><span data-stu-id="beed3-699">LSCEventTypeOccurred_GetChanges</span></span>  <br/> |<span data-ttu-id="beed3-700">Произошел ilSCEvent.</span><span class="sxs-lookup"><span data-stu-id="beed3-700">An ILSCEvent has occurred.</span></span> <span data-ttu-id="beed3-701">Чтобы получить данные, потребитель должен вызвать [ILSCLocalSyncClient::GetChanges.](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges)</span><span class="sxs-lookup"><span data-stu-id="beed3-701">The consumer should call [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) to retrieve the data.</span></span>  <br/> |
|<span data-ttu-id="beed3-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="beed3-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span></span>  <br/> |<span data-ttu-id="beed3-703">Изменены поддерживаемые расширения файлов.</span><span class="sxs-lookup"><span data-stu-id="beed3-703">The supported file extensions have changed.</span></span> <span data-ttu-id="beed3-704">Чтобы получить новый список поддерживаемых расширений, потребитель должен вызвать [ILSCLocalSyncClient::GetSupportedFileExtensions.](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions)</span><span class="sxs-lookup"><span data-stu-id="beed3-704">The consumer should call [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) to retrieve the new list of supported extensions.</span></span>  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a><span data-ttu-id="beed3-705">Enum LSCNetworkSyncPermissionType</span><span class="sxs-lookup"><span data-stu-id="beed3-705">Enum LSCNetworkSyncPermissionType</span></span>
<span data-ttu-id="beed3-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span><span class="sxs-lookup"><span data-stu-id="beed3-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span></span>

<span data-ttu-id="beed3-707">В этом переумечении указаны флаги, используемые для использования в сети.</span><span class="sxs-lookup"><span data-stu-id="beed3-707">This enumeration specifies the flags used for a network cost heuristic.</span></span> 

|<span data-ttu-id="beed3-708">Enumerator</span><span class="sxs-lookup"><span data-stu-id="beed3-708">Enumerator</span></span>|<span data-ttu-id="beed3-709">Описание</span><span class="sxs-lookup"><span data-stu-id="beed3-709">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="beed3-710">LSCNetworkSyncPermissionType_HighCost</span><span class="sxs-lookup"><span data-stu-id="beed3-710">LSCNetworkSyncPermissionType_HighCost</span></span>  <br/> |<span data-ttu-id="beed3-711">True, если переопределена стоимость для дорогих сетей (например, 3G).</span><span class="sxs-lookup"><span data-stu-id="beed3-711">True if the cost heuristic for expensive networks (such as 3G) is overridden.</span></span>  <br/> |
|<span data-ttu-id="beed3-712">LSCNetworkSyncPermissionType_HighPowerUsage</span><span class="sxs-lookup"><span data-stu-id="beed3-712">LSCNetworkSyncPermissionType_HighPowerUsage</span></span>  <br/> |<span data-ttu-id="beed3-713">True, если переопределена стоимость использования электроэнергии (например, аккумулятора).</span><span class="sxs-lookup"><span data-stu-id="beed3-713">True if the cost heuristic for power usage (such as a battery) is overridden.</span></span>  <br/> |
   
### <a name="enum-lscstatusflag"></a><span data-ttu-id="beed3-714">Enum LSCStatusFlag</span><span class="sxs-lookup"><span data-stu-id="beed3-714">Enum LSCStatusFlag</span></span>
<span data-ttu-id="beed3-715"><a name="Enum_LSCStatusFlag"> </a></span><span class="sxs-lookup"><span data-stu-id="beed3-715"><a name="Enum_LSCStatusFlag"> </a></span></span>

<span data-ttu-id="beed3-716">Это переумежение используется для представления состояния синхронизации файла.</span><span class="sxs-lookup"><span data-stu-id="beed3-716">This enumeration is used to represent the synchronize status of a file.</span></span> 
  
|<span data-ttu-id="beed3-717">Enumerator</span><span class="sxs-lookup"><span data-stu-id="beed3-717">Enumerator</span></span>|<span data-ttu-id="beed3-718">Описание</span><span class="sxs-lookup"><span data-stu-id="beed3-718">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="beed3-719">LCSStatusFlag_None</span><span class="sxs-lookup"><span data-stu-id="beed3-719">LCSStatusFlag_None</span></span>  <br/> ||
|<span data-ttu-id="beed3-720">LSCStatusFlag_UploadPending</span><span class="sxs-lookup"><span data-stu-id="beed3-720">LSCStatusFlag_UploadPending</span></span>  <br/> |<span data-ttu-id="beed3-721">True, если в файл сервера отправляются отложенные данные.</span><span class="sxs-lookup"><span data-stu-id="beed3-721">True if there is pending data to send to the server file.</span></span>  <br/> |
|<span data-ttu-id="beed3-722">LSCStatusFlag_DownloadPending</span><span class="sxs-lookup"><span data-stu-id="beed3-722">LSCStatusFlag_DownloadPending</span></span>  <br/> |<span data-ttu-id="beed3-723">True, если есть ожидаемые данные для скачивания из файла сервера.</span><span class="sxs-lookup"><span data-stu-id="beed3-723">True if there is pending data to download from the server file.</span></span>  <br/> |
|<span data-ttu-id="beed3-724">LSCStatusFlag_LocalFileUnchanged</span><span class="sxs-lookup"><span data-stu-id="beed3-724">LSCStatusFlag_LocalFileUnchanged</span></span>  <br/> |<span data-ttu-id="beed3-725">True, если Office на файле в кэше — это самая недавняя копия данных на диске.</span><span class="sxs-lookup"><span data-stu-id="beed3-725">True if the data Office has on the file in its cache is the most recent copy of the data on disk.</span></span>  <br/> |
   

