---
title: Использование Ксисинкклиент для управления кэшем документов Office (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Узнайте, как использовать Ксисинкклиент для управления кэшем документов Office (ODC).
ms.openlocfilehash: ce33063f88492bcd6f9682a4a6431fb36f138d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346258"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a><span data-ttu-id="ae72e-103">Использование Ксисинкклиент для управления кэшем документов Office (ODC)</span><span class="sxs-lookup"><span data-stu-id="ae72e-103">Using CSISyncClient to control the Office Document Cache (ODC)</span></span>

<span data-ttu-id="ae72e-104">Узнайте, как использовать Ксисинкклиент для управления кэшем документов Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="ae72e-104">Learn how to use CSISyncClient to control the Office Document Cache (ODC).</span></span>
  
<span data-ttu-id="ae72e-105">Ксисинкклиент — это встроенный COM-сервер (Ксисинкклиент. exe), позволяющий Microsoft OneDrive управлять поведением кэша документов Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="ae72e-105">CSISyncClient is an out-of-proc COM server (CsiSyncClient.exe) that allows Microsoft OneDrive to control the behavior of the Office Document Cache (ODC).</span></span> <span data-ttu-id="ae72e-106">Например, OneDrive может позвонить на ODC через Ксисинкклиент для отправки и загрузки файлов в конечные точки с включенной поддержкой MS-FSSHTTP.</span><span class="sxs-lookup"><span data-stu-id="ae72e-106">For example, OneDrive may call upon the ODC via CSISyncClient to upload and download files to and from MS-FSSHTTP enabled endpoints.</span></span> <span data-ttu-id="ae72e-107">Это позволяет расширенным функциям, поддерживающим обслуживание, в Office, например, совместном редактировании и переходе из автономного режима в оперативный.</span><span class="sxs-lookup"><span data-stu-id="ae72e-107">This enables advanced service-backed features in Office, such as co-authoring and seamless transitions from offline to online.</span></span>
  
<span data-ttu-id="ae72e-108">Ксисинкклиент доступен на рабочем столе Office (x86 и x64).</span><span class="sxs-lookup"><span data-stu-id="ae72e-108">CsiSyncClient is available in Office Desktop (both x86 and x64).</span></span> <span data-ttu-id="ae72e-109">Примечание. в то время как новые версии Office могут поставляться с Ксисинкклиент, этот процесс будет использоваться только для обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="ae72e-109">Note: While newer versions of Office may ship with CsiSyncClient, the process will be used for backward compatibility only.</span></span> <span data-ttu-id="ae72e-110">Интерфейс Ксисинкклиент и методология управления ODC будут изменены в следующих версиях Office.</span><span class="sxs-lookup"><span data-stu-id="ae72e-110">The CsiSyncClient interface and the methodology of controlling the ODC will change in future versions of Office.</span></span>
  
<span data-ttu-id="ae72e-111">В настоящее время идентификатор класса имеет значение "ответить только на OneDrive".</span><span class="sxs-lookup"><span data-stu-id="ae72e-111">The class ID is currently set to respond only to OneDrive.</span></span>
  
<span data-ttu-id="ae72e-112">COM-объект можно использовать в качестве внепроцессных COM-серверов и работает в Ксисинкклиент. exe.</span><span class="sxs-lookup"><span data-stu-id="ae72e-112">The COM object is usable as an out-of-proc COM server and runs in CsiSyncClient.exe.</span></span> <span data-ttu-id="ae72e-113">В связи с ограничениями на доступ (используемая в ODC), она поставляется с типом бита, в котором находится Office, поэтому платформа x64 Office означает, что используется COM-объект на 64-разрядной версии, или x86 — COM-объект x86.</span><span class="sxs-lookup"><span data-stu-id="ae72e-113">Due to limitations with Access (which the ODC uses), it ships with the bit type that Office comes in, so x64 Office means an x64 COM object, or x86 Office means an x86 COM object.</span></span> <span data-ttu-id="ae72e-114">Чтобы обойти это ограничение, при указании CLSCTX_LOCAL_SERVER в составе компонента CoCreateInstance будет размещен COM-объект как внешний COM-сервер, что обеспечивает совместимость с несколькими разрядами.</span><span class="sxs-lookup"><span data-stu-id="ae72e-114">To get around this limitation, specifying CLSCTX_LOCAL_SERVER as part of the CoCreateInstance will have the COM object be hosted as an out-of-proc COM server, allowing cross-bitness compatibility.</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="ae72e-115">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="ae72e-115">Interfaces</span></span>

<span data-ttu-id="ae72e-116">В Ксисинкклиент используются следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="ae72e-116">CSISyncClient uses the following interfaces.</span></span>
  
### <a name="interface-ilsclocalsyncclient"></a><span data-ttu-id="ae72e-117">Интерфейс Илсклокалсинкклиент</span><span class="sxs-lookup"><span data-stu-id="ae72e-117">Interface ILSCLocalSyncClient</span></span>

<span data-ttu-id="ae72e-118">Это основной интерфейс, используемый для синхронизации файлов в Office.</span><span class="sxs-lookup"><span data-stu-id="ae72e-118">This is the primary interface used to synchronize files in Office.</span></span>
  
- <span data-ttu-id="ae72e-119">ProgID: Office. Локалсинкклиент</span><span class="sxs-lookup"><span data-stu-id="ae72e-119">ProgID: Office.LocalSyncClient</span></span>
- <span data-ttu-id="ae72e-120">CLSID: {14286318 – B6CF — 49a1 — 81FC. D74AD94902F9}</span><span class="sxs-lookup"><span data-stu-id="ae72e-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span></span>
- <span data-ttu-id="ae72e-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span><span class="sxs-lookup"><span data-stu-id="ae72e-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span></span>
   
<span data-ttu-id="ae72e-122">Предоставляемый COM-объект используется в качестве сервера вне процесса.</span><span class="sxs-lookup"><span data-stu-id="ae72e-122">The COM object that is exposed is used as an out-of-proc server.</span></span> <span data-ttu-id="ae72e-123">Указание CLSCTX_LOCAL_SERVER в составе компонента CoCreateInstance обеспечивает возможность совместимости между 64 64 и 32 – 32 процессами.</span><span class="sxs-lookup"><span data-stu-id="ae72e-123">Specifying CLSCTX_LOCAL_SERVER as part of CoCreateInstance allows compatability between 64bit and 32bit processes.</span></span>
  
<span data-ttu-id="ae72e-124">После создания объекта COM необходимо вызвать метод [илсклокалсинкклиент:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) First.</span><span class="sxs-lookup"><span data-stu-id="ae72e-124">Once you've co-created the COM object, you MUST call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) first.</span></span> <span data-ttu-id="ae72e-125">После [илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) успешно завершена, вы можете вызвать любой API так часто, как вы хотите и в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="ae72e-125">Once [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has completed successfully, you may call any API as often as you wish and in any order.</span></span> <span data-ttu-id="ae72e-126">Вы также можете вызвать метод [илсклокалсинкклиент:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) для уже инициализированного объекта, но при этом ничего не происходит.</span><span class="sxs-lookup"><span data-stu-id="ae72e-126">You may also call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) on an already initialized object, but this does nothing.</span></span> 
  
<span data-ttu-id="ae72e-127">Исключениями из предыдущего абзаца являются [илсклокалсинкклиент:: ресеткаче](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) и [илсклокалсинкклиент:: Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="ae72e-127">The exceptions to the previous paragraph are [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) and [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="ae72e-128">После вызова [илсклокалсинкклиент:: Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) для объекта COM необходимо удалить этот объект и создать новый.</span><span class="sxs-lookup"><span data-stu-id="ae72e-128">After you call [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) on the COM object, you MUST destroy that object and create a new one.</span></span> <span data-ttu-id="ae72e-129">[Илсклокалсинкклиент:: ресеткаче](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) удалит ваш подкэш, удалите все связанные сведения о файле в кэше, но оставьте документы на диске.</span><span class="sxs-lookup"><span data-stu-id="ae72e-129">[ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) will delete your subcache, delete all associated file information in the cache, but leave the documents on disk.</span></span> <span data-ttu-id="ae72e-130">Кроме того, он оставляет состояние неизменным для связи с кэшем.</span><span class="sxs-lookup"><span data-stu-id="ae72e-130">It also leaves the state intact for communicating with the cache.</span></span> <span data-ttu-id="ae72e-131">Это позволяет вызывать [илсклокалсинкклиент:: инициализировать](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) еще раз, чтобы создать новый кэш без необходимости уничтожения и повторного создания com-объекта.</span><span class="sxs-lookup"><span data-stu-id="ae72e-131">This allows you to call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) again to create a new cache without having to destroy and recreate the COM object.</span></span> 
  
<span data-ttu-id="ae72e-132">**Открытые функции элементов**</span><span class="sxs-lookup"><span data-stu-id="ae72e-132">**Public member functions**</span></span>

#### <a name="ilsclocalsyncclientdeletefile"></a><span data-ttu-id="ae72e-133">Илсклокалсинкклиент::D Елетефиле</span><span class="sxs-lookup"><span data-stu-id="ae72e-133">ILSCLocalSyncClient::DeleteFile</span></span>

<span data-ttu-id="ae72e-134">DeleteFile используется для удаления сведений о файле из кэша.</span><span class="sxs-lookup"><span data-stu-id="ae72e-134">DeleteFile is used to remove the file information from the cache.</span></span> <span data-ttu-id="ae72e-135">Тем не менее, этот метод оставляет связанный файл на диске и на сервере.</span><span class="sxs-lookup"><span data-stu-id="ae72e-135">However, this method will leave the associated file on disk and on the server.</span></span>
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="ae72e-136">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-136">Parameters</span></span>

 <span data-ttu-id="ae72e-137">_бстрресаурцеид_</span><span class="sxs-lookup"><span data-stu-id="ae72e-137">_bstrResourceID_</span></span>
  
<span data-ttu-id="ae72e-138">Строка, которая определяет значение ResourceID файла.</span><span class="sxs-lookup"><span data-stu-id="ae72e-138">The string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="ae72e-139">Это значение не должно быть пустым (не должно превышать 128 символов).</span><span class="sxs-lookup"><span data-stu-id="ae72e-139">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-140">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-140">Return values</span></span>

|<span data-ttu-id="ae72e-141">Значение</span><span class="sxs-lookup"><span data-stu-id="ae72e-141">Value</span></span>|<span data-ttu-id="ae72e-142">Описание</span><span class="sxs-lookup"><span data-stu-id="ae72e-142">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae72e-143">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae72e-143">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae72e-144">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ae72e-144">The call failed.</span></span>  <br/> |
|<span data-ttu-id="ae72e-145">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae72e-145">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae72e-146">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="ae72e-146">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae72e-147">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae72e-147">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae72e-148">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ae72e-148">The call failed.</span></span>  <br/> |
|<span data-ttu-id="ae72e-149">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="ae72e-149">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="ae72e-150">Данный ResourceID не находится в кэше.</span><span class="sxs-lookup"><span data-stu-id="ae72e-150">The given ResourceID is not in the cache.</span></span>  <br/> |
|<span data-ttu-id="ae72e-151">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae72e-151">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae72e-152">Инициализация не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="ae72e-152">Initialize has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae72e-153">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="ae72e-153">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="ae72e-154">Файл в настоящее время синхронизируется или открывается, и его невозможно удалить.</span><span class="sxs-lookup"><span data-stu-id="ae72e-154">The file is currently synchronizing or open and cannot be deleted.</span></span>  <br/> |
|<span data-ttu-id="ae72e-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae72e-155">S_OK</span></span>  <br/> |<span data-ttu-id="ae72e-156">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="ae72e-156">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a><span data-ttu-id="ae72e-157">Илсклокалсинкклиент:: Changes</span><span class="sxs-lookup"><span data-stu-id="ae72e-157">ILSCLocalSyncClient::GetChanges</span></span>
<span data-ttu-id="ae72e-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span><span class="sxs-lookup"><span data-stu-id="ae72e-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span></span>

<span data-ttu-id="ae72e-159">Метод GetNext возвращает перечислитель объектов Илсцевент, а также возвращает маркер, который передается следующему вызову метода GetNext, предполагая, что потребитель обработал предыдущий набор событий.</span><span class="sxs-lookup"><span data-stu-id="ae72e-159">GetChanges returns an enumerator of ILSCEvent objects, and also returns a token that is given to the next call to GetChanges, assuming the consumer has processed the previous set of events.</span></span> <span data-ttu-id="ae72e-160">События, предшествующие указанному _нпревиаусчанжестокен_ , будут удалены и недоступны.</span><span class="sxs-lookup"><span data-stu-id="ae72e-160">Events before the  _nPreviousChangesToken_ specified will be deleted and unavailable.</span></span> <span data-ttu-id="ae72e-161">Если события для обработки отсутствуют, _пнкуррентчанжестокен_ должно иметь то же значение, что и _Нпревиаусчанжестокен_, но _ппиевентс_ по-прежнему будет задано.</span><span class="sxs-lookup"><span data-stu-id="ae72e-161">If there are no events to be processed,  _pnCurrentChangesToken_ should be the same value as  _nPreviousChangesToken_, but  _ppiEvents_ will still be set.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a><span data-ttu-id="ae72e-162">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-162">Parameters</span></span>

 <span data-ttu-id="ae72e-163">_нпревиаусчанжестокен_</span><span class="sxs-lookup"><span data-stu-id="ae72e-163">_nPreviousChangesToken_</span></span>
  
<span data-ttu-id="ae72e-164">Определяет, какое событие было последний раз обработано потребителем.</span><span class="sxs-lookup"><span data-stu-id="ae72e-164">Identifies which event was last processed by the consumer.</span></span> 
  
 <span data-ttu-id="ae72e-165">_пнкуррентчанжестокен_</span><span class="sxs-lookup"><span data-stu-id="ae72e-165">_pnCurrentChangesToken_</span></span>
  
<span data-ttu-id="ae72e-166">Определяет Последнее событие, переданное потребителю.</span><span class="sxs-lookup"><span data-stu-id="ae72e-166">Identifies the most recent event being handed to the consumer.</span></span> <span data-ttu-id="ae72e-167">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="ae72e-167">Must not be null.</span></span>
  
 <span data-ttu-id="ae72e-168">_ппиевентс_</span><span class="sxs-lookup"><span data-stu-id="ae72e-168">_ppiEvents_</span></span>
  
<span data-ttu-id="ae72e-169">Перечислитель для событий, которые передаются потребителю.</span><span class="sxs-lookup"><span data-stu-id="ae72e-169">An enumerator for the events handed to the consumer.</span></span> <span data-ttu-id="ae72e-170">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="ae72e-170">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-171">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-171">Return values</span></span>

|<span data-ttu-id="ae72e-172">Значение</span><span class="sxs-lookup"><span data-stu-id="ae72e-172">Value</span></span>|<span data-ttu-id="ae72e-173">Описание</span><span class="sxs-lookup"><span data-stu-id="ae72e-173">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae72e-174">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae72e-174">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae72e-175">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ae72e-175">The call failed.</span></span>  <br/> |
|<span data-ttu-id="ae72e-176">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae72e-176">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae72e-177">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="ae72e-177">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae72e-178">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae72e-178">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae72e-179">[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="ae72e-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae72e-180">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae72e-180">S_OK</span></span>  <br/> |<span data-ttu-id="ae72e-181">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="ae72e-181">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a><span data-ttu-id="ae72e-182">Илсклокалсинкклиент:: Жетклиентнетворксинкпермиссион</span><span class="sxs-lookup"><span data-stu-id="ae72e-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span></span>

<span data-ttu-id="ae72e-183">Жетклиентнетворксинкпермиссион используется, чтобы запросить, переопределяются ли эвристика синхронизации Office для стоимости сети и энергопотребления.</span><span class="sxs-lookup"><span data-stu-id="ae72e-183">GetClientNetworkSyncPermission is used to query whether Office's synchronizing heuristics for network cost and power usage are overridden.</span></span> <span data-ttu-id="ae72e-184">При использовании сети 3G или другой сети с высоким уровнем затрат или при работе от батарей и до подключения к сети, Office может блокировать сетевой трафик до тех пор, пока не будет оппортуне время.</span><span class="sxs-lookup"><span data-stu-id="ae72e-184">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span>
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a><span data-ttu-id="ae72e-185">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-185">Parameters</span></span>

 <span data-ttu-id="ae72e-186">_нсптипе_</span><span class="sxs-lookup"><span data-stu-id="ae72e-186">_nspType_</span></span>
  
<span data-ttu-id="ae72e-187">Флаг, определяющий, какой эвристический объект затрат необходимо запросить.</span><span class="sxs-lookup"><span data-stu-id="ae72e-187">A flag which defines which cost heuristic to query.</span></span> <span data-ttu-id="ae72e-188">В разделе [enum лскнетворксинкпермиссионтипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="ae72e-188">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span> 
  
 <span data-ttu-id="ae72e-189">_пфсинценаблед_</span><span class="sxs-lookup"><span data-stu-id="ae72e-189">_pfSyncEnabled_</span></span>
  
<span data-ttu-id="ae72e-190">Указывает, является ли запрошенный эвристический алгоритм затрат в данный момент перегруженным или нет.</span><span class="sxs-lookup"><span data-stu-id="ae72e-190">Specifies whether the requested cost heuristic is currently overridden or not.</span></span> <span data-ttu-id="ae72e-191">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="ae72e-191">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-192">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-192">Return values</span></span>

|<span data-ttu-id="ae72e-193">Значение</span><span class="sxs-lookup"><span data-stu-id="ae72e-193">Value</span></span>|<span data-ttu-id="ae72e-194">Описание</span><span class="sxs-lookup"><span data-stu-id="ae72e-194">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae72e-195">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae72e-195">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae72e-196">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ae72e-196">The call failed.</span></span>  <br/> |
|<span data-ttu-id="ae72e-197">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae72e-197">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae72e-198">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="ae72e-198">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae72e-199">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae72e-199">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae72e-200">[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="ae72e-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae72e-201">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae72e-201">S_OK</span></span>  <br/> |<span data-ttu-id="ae72e-202">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="ae72e-202">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a><span data-ttu-id="ae72e-203">Илсклокалсинкклиент:: Жетфилестатус</span><span class="sxs-lookup"><span data-stu-id="ae72e-203">ILSCLocalSyncClient::GetFileStatus</span></span>

<span data-ttu-id="ae72e-204">Жетфилестатус используется для сбора сведений о конкретном файле: независимо от того, существует ли он в кэше, если у него есть ожидающая связь с копией на сервере, и если Office 2013 имеет самые актуальные данные из локальной копии.</span><span class="sxs-lookup"><span data-stu-id="ae72e-204">GetFileStatus is used to gather information for a specific file: whether it exists in the cache, if it has pending communication with the server copy, and if Office 2013 has the most up to date data from the local copy.</span></span> <span data-ttu-id="ae72e-205">Для определения сведений, к которым необходимо запросить COM-объект Ксисинкклиент, требуется битовый флаг значений [перечисления лскстатусфлаг](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) .</span><span class="sxs-lookup"><span data-stu-id="ae72e-205">It requires a bitwise flag of [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) values to determine what information the CsiSyncClient COM object is to query for.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a><span data-ttu-id="ae72e-206">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-206">Parameters</span></span>

 <span data-ttu-id="ae72e-207">_бстрресаурцеид_</span><span class="sxs-lookup"><span data-stu-id="ae72e-207">_bstrResourceID_</span></span>
  
<span data-ttu-id="ae72e-208">Строка, которая определяет файл на клиенте.</span><span class="sxs-lookup"><span data-stu-id="ae72e-208">The string which identifies the file on the client.</span></span> <span data-ttu-id="ae72e-209">Это значение не должно быть пустым, не более 128 символов.</span><span class="sxs-lookup"><span data-stu-id="ae72e-209">This value must be non-empty, with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="ae72e-210">_сфрекуестедстатус_</span><span class="sxs-lookup"><span data-stu-id="ae72e-210">_sfRequestedStatus_</span></span>
  
<span data-ttu-id="ae72e-211">Флаг, определяющий возвращаемую информацию.</span><span class="sxs-lookup"><span data-stu-id="ae72e-211">A flag which defines what information to return.</span></span> <span data-ttu-id="ae72e-212">В разделе [enum лскстатусфлаг](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="ae72e-212">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
 <span data-ttu-id="ae72e-213">_пбстрфилесистемпас_</span><span class="sxs-lookup"><span data-stu-id="ae72e-213">_pbstrFileSystemPath_</span></span>
  
<span data-ttu-id="ae72e-214">Строка, которая определяет расположение файла, определенного _бстрресаурцеид_ в клиенте.</span><span class="sxs-lookup"><span data-stu-id="ae72e-214">The string which identifies the location of the file identified by  _bstrResourceID_ on the client.</span></span> <span data-ttu-id="ae72e-215">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="ae72e-215">Must not be null.</span></span> 
  
 <span data-ttu-id="ae72e-216">_пбстретаг_</span><span class="sxs-lookup"><span data-stu-id="ae72e-216">_pbstrETag_</span></span>
  
<span data-ttu-id="ae72e-217">Строка, которая будет содержать тег eTag для файла, указанного с помощью _бстрресаурцеид_.</span><span class="sxs-lookup"><span data-stu-id="ae72e-217">A string which will contain the eTag for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="ae72e-218">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="ae72e-218">Must not be null.</span></span> 
  
 <span data-ttu-id="ae72e-219">_псффилестатус_</span><span class="sxs-lookup"><span data-stu-id="ae72e-219">_psfFileStatus_</span></span>
  
<span data-ttu-id="ae72e-220">Флаг, который будет содержать состояние, запрошенное через _сфрекуестедстатус_ , для файла, определенного _бстрресаурцеид_.</span><span class="sxs-lookup"><span data-stu-id="ae72e-220">A flag which will contain the status requested via  _sfRequestedStatus_ for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="ae72e-221">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="ae72e-221">Must not be null.</span></span> <span data-ttu-id="ae72e-222">В разделе [enum лскстатусфлаг](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="ae72e-222">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-223">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-223">Return values</span></span>

|<span data-ttu-id="ae72e-224">Значение</span><span class="sxs-lookup"><span data-stu-id="ae72e-224">Value</span></span>|<span data-ttu-id="ae72e-225">Описание</span><span class="sxs-lookup"><span data-stu-id="ae72e-225">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae72e-226">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae72e-226">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae72e-227">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ae72e-227">The call failed.</span></span>  <br/> |
|<span data-ttu-id="ae72e-228">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae72e-228">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae72e-229">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="ae72e-229">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae72e-230">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="ae72e-230">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="ae72e-231">Сведения о файле, указанные в _бстрресаурцеид_ , не существуют в кэше.</span><span class="sxs-lookup"><span data-stu-id="ae72e-231">The file information specified by  _bstrResourceID_ does not exist in the cache.</span></span>  <br/> |
|<span data-ttu-id="ae72e-232">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ae72e-232">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="ae72e-233">Запрошен LSCStatusFlag_LocalFileUnchanged или файл, указанный с помощью _бстрресаурцеид_ , заблокирован или отсутствует.</span><span class="sxs-lookup"><span data-stu-id="ae72e-233">LSCStatusFlag_LocalFileUnchanged was requested or the file specified by  _bstrResourceID_ is locked or missing.</span></span>  <br/> |
|<span data-ttu-id="ae72e-234">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae72e-234">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae72e-235">[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="ae72e-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae72e-236">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae72e-236">S_OK</span></span>  <br/> |<span data-ttu-id="ae72e-237">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="ae72e-237">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a><span data-ttu-id="ae72e-238">Илсклокалсинкклиент:: Жетсуппортедфиликстенсионс</span><span class="sxs-lookup"><span data-stu-id="ae72e-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span></span>
<span data-ttu-id="ae72e-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span><span class="sxs-lookup"><span data-stu-id="ae72e-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span></span>

<span data-ttu-id="ae72e-240">Жетсуппортедфиликстенсионс возвращает список расширений файлов с разделением каналов, которые в настоящее время поддерживаются объектом COM Ксисинкклиент.</span><span class="sxs-lookup"><span data-stu-id="ae72e-240">GetSupportedFileExtensions returns a list of pipe-delimited file extensions which are currently supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="ae72e-241">Обратите внимание, что этот список может измениться, а потребитель будет уведомлен об изменении с помощью объекта Ипартнерактивитикаллбакк, предоставленного в [илсклокалсинкклиент:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (см евентоккуред).</span><span class="sxs-lookup"><span data-stu-id="ae72e-241">Note that this list may change, and the consumer will be notified of a change via the IPartnerActivityCallback object provided on [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (See EventOccured).</span></span> 
  
<span data-ttu-id="ae72e-242">Ниже приведен пример возвращаемой строки: "| docx | DOCM | pptx |"</span><span class="sxs-lookup"><span data-stu-id="ae72e-242">An example of the string returned is as follows: "|docx|docm|pptx|"</span></span>
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a><span data-ttu-id="ae72e-243">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-243">Parameters</span></span>

 <span data-ttu-id="ae72e-244">_пбстрсуппортедфиликстенсионс_</span><span class="sxs-lookup"><span data-stu-id="ae72e-244">_pbstrSupportedFileExtensions_</span></span>
  
<span data-ttu-id="ae72e-245">Строка, для которой задается набор расширений файлов с разделителем каналов, поддерживаемый COM-объектом Ксисинкклиент.</span><span class="sxs-lookup"><span data-stu-id="ae72e-245">A string to be set with a pipe-delimited set of file extensions supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="ae72e-246">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="ae72e-246">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-247">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-247">Return values</span></span>

|<span data-ttu-id="ae72e-248">Значение</span><span class="sxs-lookup"><span data-stu-id="ae72e-248">Value</span></span>|<span data-ttu-id="ae72e-249">Описание</span><span class="sxs-lookup"><span data-stu-id="ae72e-249">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae72e-250">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae72e-250">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae72e-251">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ae72e-251">The call failed.</span></span>  <br/> |
|<span data-ttu-id="ae72e-252">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae72e-252">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae72e-253">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="ae72e-253">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae72e-254">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae72e-254">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae72e-255">[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="ae72e-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae72e-256">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae72e-256">S_OK</span></span>  <br/> |<span data-ttu-id="ae72e-257">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="ae72e-257">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a><span data-ttu-id="ae72e-258">Илсклокалсинкклиент:: Initialize</span><span class="sxs-lookup"><span data-stu-id="ae72e-258">ILSCLocalSyncClient::Initialize</span></span>
<span data-ttu-id="ae72e-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span><span class="sxs-lookup"><span data-stu-id="ae72e-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span></span>

<span data-ttu-id="ae72e-260">Инициализация должна быть первым вызываемым методом.</span><span class="sxs-lookup"><span data-stu-id="ae72e-260">Initialize must be the first method called.</span></span> <span data-ttu-id="ae72e-261">В противном случае все остальные API будут возвращать E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="ae72e-261">Otherwise, all other APIs will return E_LSC_NOTINITIALIZED.</span></span> <span data-ttu-id="ae72e-262">При вызове метода Initialize для уже инициализированного объекта возвращается S_OK и ничего не происходит.</span><span class="sxs-lookup"><span data-stu-id="ae72e-262">Calling Initialize on an already initialized object returns S_OK and does nothing.</span></span> <span data-ttu-id="ae72e-263">Если возвращается E_LSC_CACHEMISMATCH, вызывающий может вызвать [илсклокалсинкклиент:: ресеткаче](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) , чтобы удалить кэш, связанный с заданным супплиедид.</span><span class="sxs-lookup"><span data-stu-id="ae72e-263">If E_LSC_CACHEMISMATCH is returned, the caller may call [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) to delete the cache associated with the given SuppliedID.</span></span> <span data-ttu-id="ae72e-264">Тем не менее, в этом случае другие API будут возвращать E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="ae72e-264">However, in this case other APIs will still return E_LSC_NOTINITIALIZED.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a><span data-ttu-id="ae72e-265">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-265">Parameters</span></span>

 <span data-ttu-id="ae72e-266">_бстрсупплиедид_</span><span class="sxs-lookup"><span data-stu-id="ae72e-266">_bstrSuppliedID_</span></span>
  
<span data-ttu-id="ae72e-267">Идентифицирует объекта-получателя и используемого кэша.</span><span class="sxs-lookup"><span data-stu-id="ae72e-267">Identifies the consumer and which cache to use.</span></span> <span data-ttu-id="ae72e-268">Значение не должно быть пустым (не должно превышать 32 символов).</span><span class="sxs-lookup"><span data-stu-id="ae72e-268">Must be non-empty with a maximum of 32 characters.</span></span> 
  
 <span data-ttu-id="ae72e-269">_бстрпрогид_</span><span class="sxs-lookup"><span data-stu-id="ae72e-269">_bstrProgID_</span></span>
  
<span data-ttu-id="ae72e-270">Определяет COM-объект потребителя для двусторонней связи.</span><span class="sxs-lookup"><span data-stu-id="ae72e-270">Identifies the consumer's COM object for two-way communication.</span></span> <span data-ttu-id="ae72e-271">Значение не должно быть пустым (не должно превышать 39 символов).</span><span class="sxs-lookup"><span data-stu-id="ae72e-271">Must be non-empty with a maximum of 39 characters.</span></span> <span data-ttu-id="ae72e-272">Для получения дополнительных сведений об идентификаторах ProgID см. [ \<\> ](https://docs.microsoft.com/windows/desktop/com/-progid--key)</span><span class="sxs-lookup"><span data-stu-id="ae72e-272">See [\<ProgID\> Key](https://docs.microsoft.com/windows/desktop/com/-progid--key) for more information about ProgIDs.</span></span> 
  
 <span data-ttu-id="ae72e-273">_бстрфилесистемдиректорихинт_</span><span class="sxs-lookup"><span data-stu-id="ae72e-273">_bstrFileSystemDirectoryHint_</span></span>
  
<span data-ttu-id="ae72e-274">Определяет корневой каталог, в котором будут храниться локальные файлы.</span><span class="sxs-lookup"><span data-stu-id="ae72e-274">Identifies the directory root in which local files will be stored.</span></span> <span data-ttu-id="ae72e-275">Значение не должно быть пустым (не должно превышать 256 символов).</span><span class="sxs-lookup"><span data-stu-id="ae72e-275">Must be non-empty with a maximum of 256 characters.</span></span> <span data-ttu-id="ae72e-276">Каталог должен уже существовать.</span><span class="sxs-lookup"><span data-stu-id="ae72e-276">The directory must already exist.</span></span> 
  
 <span data-ttu-id="ae72e-277">_певенткаллбакк_</span><span class="sxs-lookup"><span data-stu-id="ae72e-277">_pEventCallback_</span></span>
  
<span data-ttu-id="ae72e-278">Интерфейс обратного вызова, который Ксисинкклиент будет уведомлять об изменениях.</span><span class="sxs-lookup"><span data-stu-id="ae72e-278">The callback interface which CsiSyncClient will notify on changes.</span></span> <span data-ttu-id="ae72e-279">См. Ипартнерактивитикаллбакк:: Евентоккурред.</span><span class="sxs-lookup"><span data-stu-id="ae72e-279">See IPartnerActivityCallback::EventOccurred.</span></span> <span data-ttu-id="ae72e-280">Это значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="ae72e-280">This value must not be null.</span></span> 
  
 <span data-ttu-id="ae72e-281">_пфкреатедневкаче_</span><span class="sxs-lookup"><span data-stu-id="ae72e-281">_pfCreatedNewCache_</span></span>
  
<span data-ttu-id="ae72e-282">Возвращает значение, указывающее, был ли создан новый кэш.</span><span class="sxs-lookup"><span data-stu-id="ae72e-282">Returns whether a new cache was created.</span></span> <span data-ttu-id="ae72e-283">Если с Супплиедид не связан ни один кэш, будет создан один из них.</span><span class="sxs-lookup"><span data-stu-id="ae72e-283">If no cache is associated with the SuppliedID, one will be created.</span></span> <span data-ttu-id="ae72e-284">Это значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="ae72e-284">This value must not be null.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-285">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-285">Return values</span></span>

|<span data-ttu-id="ae72e-286">Значение</span><span class="sxs-lookup"><span data-stu-id="ae72e-286">Value</span></span>|<span data-ttu-id="ae72e-287">Описание</span><span class="sxs-lookup"><span data-stu-id="ae72e-287">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae72e-288">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae72e-288">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae72e-289">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ae72e-289">The call failed.</span></span>  <br/> |
|<span data-ttu-id="ae72e-290">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae72e-290">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae72e-291">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="ae72e-291">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae72e-292">E_LSC_CACHEMISMATCH</span><span class="sxs-lookup"><span data-stu-id="ae72e-292">E_LSC_CACHEMISMATCH</span></span>  <br/> |<span data-ttu-id="ae72e-293">Супплиедид уже имеет связанный с ним кэш, но имеет другой ProgId или Филесистемдиректорихинт, чем предоставленные.</span><span class="sxs-lookup"><span data-stu-id="ae72e-293">A SuppliedID already has a cache associated with it, but has a different ProgId or FileSystemDirectoryHint than the ones provided.</span></span>  <br/> |
|<span data-ttu-id="ae72e-294">E_LSC_DIRECTORYHINTCONFLICT</span><span class="sxs-lookup"><span data-stu-id="ae72e-294">E_LSC_DIRECTORYHINTCONFLICT</span></span>  <br/> |<span data-ttu-id="ae72e-295">Филесистемдиректорихинт (или вложенная папка) уже существует в другом кэше.</span><span class="sxs-lookup"><span data-stu-id="ae72e-295">The FileSystemDirectoryHint (or a subfolder) already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="ae72e-296">E_LAC_PROGIDCONFLICT</span><span class="sxs-lookup"><span data-stu-id="ae72e-296">E_LAC_PROGIDCONFLICT</span></span>  <br/> |<span data-ttu-id="ae72e-297">ProgID уже существует в другом кэше.</span><span class="sxs-lookup"><span data-stu-id="ae72e-297">The ProgID already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="ae72e-298">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae72e-298">S_OK</span></span>  <br/> |<span data-ttu-id="ae72e-299">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="ae72e-299">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a><span data-ttu-id="ae72e-300">Илсклокалсинкклиент:: Локалфилечанже</span><span class="sxs-lookup"><span data-stu-id="ae72e-300">ILSCLocalSyncClient::LocalFileChange</span></span>
<span data-ttu-id="ae72e-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="ae72e-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span></span>

<span data-ttu-id="ae72e-302">Локалфилечанже используется, чтобы сообщить COM-объекту Ксисинкклиент попытаться отправить указанный файл.</span><span class="sxs-lookup"><span data-stu-id="ae72e-302">LocalFileChange is used to tell the CsiSyncClient COM object to attempt to upload the specified file.</span></span> <span data-ttu-id="ae72e-303">Метод подготовит файл для отправки, включая чтение текущего содержимого файла.</span><span class="sxs-lookup"><span data-stu-id="ae72e-303">The method will prepare the file for upload, including reading the file's current contents.</span></span> <span data-ttu-id="ae72e-304">Если отправка уже ожидается, Предыдущая отправка будет отменена и новое содержимое подготовлено к отправке.</span><span class="sxs-lookup"><span data-stu-id="ae72e-304">If an upload is already pending, the previous upload will be discarded and the new contents prepared for upload.</span></span> <span data-ttu-id="ae72e-305">Если файл открыт для редактирования в приложении, этот метод возвратит S_OK, не подготавливая файл для отправки (при наличии изменений приложение должно выполнить это действие).</span><span class="sxs-lookup"><span data-stu-id="ae72e-305">If the file is open for editing in an application, this method will return S_OK without preparing the file for upload (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="ae72e-306">Этот метод позволяет отправлять отправку, если он был помечен как отправленные ранее (см. [илсклокалсинкклиент:: ренамефиле ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span><span class="sxs-lookup"><span data-stu-id="ae72e-306">This method will allow uploads if it was marked as uploads blocked previously (see [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span></span>
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="ae72e-307">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-307">Parameters</span></span>

 <span data-ttu-id="ae72e-308">_бстрфилесистемпас_</span><span class="sxs-lookup"><span data-stu-id="ae72e-308">_bstrFileSystemPath_</span></span>
  
<span data-ttu-id="ae72e-309">Строка, которая определяет файл на клиенте.</span><span class="sxs-lookup"><span data-stu-id="ae72e-309">A string which identifies the file on the client.</span></span> <span data-ttu-id="ae72e-310">Это значение должно быть непустым локальным путем длиной не более 256 символов.</span><span class="sxs-lookup"><span data-stu-id="ae72e-310">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="ae72e-311">Этот путь должен находиться в дереве каталогов, указанном параметром Филесистемдиректорихинт при вызове [илсклокалсинкклиент:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) .</span><span class="sxs-lookup"><span data-stu-id="ae72e-311">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was made.</span></span> 
  
 <span data-ttu-id="ae72e-312">_бстрресаурцеид_</span><span class="sxs-lookup"><span data-stu-id="ae72e-312">_bstrResourceID_</span></span>
  
<span data-ttu-id="ae72e-313">Строка, определяющая значение ResourceID файла.</span><span class="sxs-lookup"><span data-stu-id="ae72e-313">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="ae72e-314">Это значение не должно быть пустым (не должно превышать 128 символов).</span><span class="sxs-lookup"><span data-stu-id="ae72e-314">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="ae72e-315">_бстрвебпас_</span><span class="sxs-lookup"><span data-stu-id="ae72e-315">_bstrWebPath_</span></span>
  
<span data-ttu-id="ae72e-316">Строка, которая определяет файл на сервере.</span><span class="sxs-lookup"><span data-stu-id="ae72e-316">A string which identifies the file on the server.</span></span> <span data-ttu-id="ae72e-317">Это значение должно быть непустым, допустимым URL-адресом, но не более чем INTERNET_MAX_URL_LENGTH, https://support.microsoft.com/kb/208427как определено.</span><span class="sxs-lookup"><span data-stu-id="ae72e-317">This value must be non-empty, valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-318">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-318">Return values</span></span>

|<span data-ttu-id="ae72e-319">Значение</span><span class="sxs-lookup"><span data-stu-id="ae72e-319">Value</span></span>|<span data-ttu-id="ae72e-320">Описание</span><span class="sxs-lookup"><span data-stu-id="ae72e-320">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae72e-321">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae72e-321">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae72e-322">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ae72e-322">The call failed.</span></span>  <br/> |
|<span data-ttu-id="ae72e-323">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae72e-323">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae72e-324">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="ae72e-324">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae72e-325">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="ae72e-325">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="ae72e-326">Значение ResourceID для файла, указанного в параметре _бстрфилесистемпас_ , отличается от указанного.</span><span class="sxs-lookup"><span data-stu-id="ae72e-326">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span> <span data-ttu-id="ae72e-327">При возвращении этой ошибки отправляется событие типа LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="ae72e-327">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="ae72e-328">См. [илсклокалсинкклиент:: Changes ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="ae72e-328">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="ae72e-329">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="ae72e-329">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="ae72e-330">Файл был удален средней операцией.</span><span class="sxs-lookup"><span data-stu-id="ae72e-330">The file was deleted mid-operation.</span></span>  <br/> |
|<span data-ttu-id="ae72e-331">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="ae72e-331">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="ae72e-332">Объект COM Ксисинкклиент не поддерживает заданное расширение файла.</span><span class="sxs-lookup"><span data-stu-id="ae72e-332">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="ae72e-333">См. [илсклокалсинкклиент:: жетсуппортедфиликстенсионс ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span><span class="sxs-lookup"><span data-stu-id="ae72e-333">See [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span></span>  <br/> |
|<span data-ttu-id="ae72e-334">E_LSC_FILEUPTODATE</span><span class="sxs-lookup"><span data-stu-id="ae72e-334">E_LSC_FILEUPTODATE</span></span>  <br/> |<span data-ttu-id="ae72e-335">COM-объект не запланировать отправку, так как файл в кэше содержал последние изменения с диска.</span><span class="sxs-lookup"><span data-stu-id="ae72e-335">The COM object did not schedule an upload because the file in the cache had the most recent changes from the disk.</span></span>  <br/> |
|<span data-ttu-id="ae72e-336">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="ae72e-336">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="ae72e-337">Файл, указанный в параметре _бстрфилесистемпас_ , отсутствует или заблокирован.</span><span class="sxs-lookup"><span data-stu-id="ae72e-337">The file specified by  _bstrFileSystemPath_ is missing or locked.</span></span>  <br/> |
|<span data-ttu-id="ae72e-338">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="ae72e-338">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="ae72e-339">Данный Филесистемпас не находится в корневом каталоге, заданном параметром Филесистемдиректорихинт при вызове метода Initialize.</span><span class="sxs-lookup"><span data-stu-id="ae72e-339">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="ae72e-340">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae72e-340">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae72e-341">[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="ae72e-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae72e-342">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="ae72e-342">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="ae72e-343">Файл, указанный в параметре _бстрресаурцеид_ , отличается от указанного в параметре филесистемпас.</span><span class="sxs-lookup"><span data-stu-id="ae72e-343">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="ae72e-344">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="ae72e-344">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="ae72e-345">Указанный файл уже содержит ожидающие изменения в другом кэше и еще не может быть связан с кэшем потребителя.</span><span class="sxs-lookup"><span data-stu-id="ae72e-345">The file specified already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="ae72e-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="ae72e-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="ae72e-347">Указанный путь находится в другом кэше.</span><span class="sxs-lookup"><span data-stu-id="ae72e-347">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="ae72e-348">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae72e-348">S_OK</span></span>  <br/> |<span data-ttu-id="ae72e-349">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="ae72e-349">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a><span data-ttu-id="ae72e-350">Илсклокалсинкклиент:: Ренамефиле</span><span class="sxs-lookup"><span data-stu-id="ae72e-350">ILSCLocalSyncClient::RenameFile</span></span>
<span data-ttu-id="ae72e-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span><span class="sxs-lookup"><span data-stu-id="ae72e-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span></span>

<span data-ttu-id="ae72e-352">Ренамефиле будет связывать новый URL-адрес и локальный путь для данного ResourceID.</span><span class="sxs-lookup"><span data-stu-id="ae72e-352">RenameFile will associate a new URL and local path for a given ResourceID.</span></span> <span data-ttu-id="ae72e-353">Если файл, указанный с помощью ResourceID, еще не существует в кэше, будет выполнена попытка создать его и пометить для скачивания.</span><span class="sxs-lookup"><span data-stu-id="ae72e-353">If the file specified by the ResourceID doesn't already exist in the cache, an attempt will be made to create it and mark it for download.</span></span>
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a><span data-ttu-id="ae72e-354">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-354">Parameters</span></span>

 <span data-ttu-id="ae72e-355">_бстрресаурцеид_</span><span class="sxs-lookup"><span data-stu-id="ae72e-355">_bstrResourceID_</span></span>
  
<span data-ttu-id="ae72e-356">Строка, определяющая значение ResourceID файла.</span><span class="sxs-lookup"><span data-stu-id="ae72e-356">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="ae72e-357">Это значение не должно быть пустым (не должно превышать 128 символов).</span><span class="sxs-lookup"><span data-stu-id="ae72e-357">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="ae72e-358">_бстрневфилесистемпас_</span><span class="sxs-lookup"><span data-stu-id="ae72e-358">_bstrNewFileSystemPath_</span></span>
  
<span data-ttu-id="ae72e-359">Строка, указывающая новый локальный путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="ae72e-359">A string which specifies the new local path for the file.</span></span> <span data-ttu-id="ae72e-360">Это значение должно быть непустым локальным путем длиной не более 256 символов.</span><span class="sxs-lookup"><span data-stu-id="ae72e-360">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="ae72e-361">Этот путь должен находиться в дереве каталогов, заданном параметром Филесистемдиректорихинт, при выполнении вызова метода Initialize.</span><span class="sxs-lookup"><span data-stu-id="ae72e-361">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span> 
  
 <span data-ttu-id="ae72e-362">_бстрневвебпас_</span><span class="sxs-lookup"><span data-stu-id="ae72e-362">_bstrNewWebPath_</span></span>
  
<span data-ttu-id="ae72e-363">Строка, указывающая новый URL-адрес файла.</span><span class="sxs-lookup"><span data-stu-id="ae72e-363">A string which specifies the new URL for the file.</span></span> <span data-ttu-id="ae72e-364">Это значение должно быть непустым допустимым URL-адресом, но не превышать INTERNET_MAX_URL_LENGTH, как https://support.microsoft.com/kb/208427определено.</span><span class="sxs-lookup"><span data-stu-id="ae72e-364">This value must be non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
 <span data-ttu-id="ae72e-365">_фблоккуплоадс_</span><span class="sxs-lookup"><span data-stu-id="ae72e-365">_fBlockUploads_</span></span>
  
<span data-ttu-id="ae72e-366">Указывает, разрешена ли в данный момент отправка в новое расположение.</span><span class="sxs-lookup"><span data-stu-id="ae72e-366">Specifies whether uploads to the new location are allowed currently.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-367">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-367">Return values</span></span>

|<span data-ttu-id="ae72e-368">Значение</span><span class="sxs-lookup"><span data-stu-id="ae72e-368">Value</span></span>|<span data-ttu-id="ae72e-369">Описание</span><span class="sxs-lookup"><span data-stu-id="ae72e-369">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae72e-370">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae72e-370">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae72e-371">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ae72e-371">The call failed.</span></span>  <br/> |
|<span data-ttu-id="ae72e-372">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae72e-372">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae72e-373">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="ae72e-373">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae72e-374">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="ae72e-374">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="ae72e-375">_Бстрневфилесистемпас_ или _бстрневвебпас_ уже существуют в другом файле в любом кэше.</span><span class="sxs-lookup"><span data-stu-id="ae72e-375">The  _bstrNewFileSystemPath_ or  _bstrNewWebPath_ already exist on another file in any cache.</span></span> <span data-ttu-id="ae72e-376">При возвращении этой ошибки отправляется событие типа LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="ae72e-376">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="ae72e-377">См. [илсклокалсинкклиент:: Changes ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="ae72e-377">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="ae72e-378">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="ae72e-378">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="ae72e-379">При выполнении этого метода сведения о файле были удалены из кэша.</span><span class="sxs-lookup"><span data-stu-id="ae72e-379">The file information was deleted from the cache while this method was running.</span></span>  <br/> |
|<span data-ttu-id="ae72e-380">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="ae72e-380">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="ae72e-381">Данный Филесистемпас не находится в корневом каталоге, заданном параметром Филесистемдиректорихинт при вызове метода Initialize.</span><span class="sxs-lookup"><span data-stu-id="ae72e-381">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="ae72e-382">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae72e-382">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae72e-383">[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="ae72e-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae72e-384">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="ae72e-384">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="ae72e-385">В настоящий момент указанный файл синхронизируется в приложении Office.</span><span class="sxs-lookup"><span data-stu-id="ae72e-385">The file specified is currently synchronizing in an Office application.</span></span>  <br/> |
|<span data-ttu-id="ae72e-386">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae72e-386">S_OK</span></span>  <br/> |<span data-ttu-id="ae72e-387">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="ae72e-387">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a><span data-ttu-id="ae72e-388">Илсклокалсинкклиент:: Ресеткаче</span><span class="sxs-lookup"><span data-stu-id="ae72e-388">ILSCLocalSyncClient::ResetCache</span></span>
<span data-ttu-id="ae72e-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span><span class="sxs-lookup"><span data-stu-id="ae72e-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span></span>

<span data-ttu-id="ae72e-390">Ресеткаче удалит кэш, связанный с Супплиедид, который был предоставлен при инициализации.</span><span class="sxs-lookup"><span data-stu-id="ae72e-390">ResetCache will delete the cache associated with the SuppliedID that was provided on Initialize.</span></span> <span data-ttu-id="ae72e-391">Сюда входят все сведения о файле, но файлы будут оставлены как на клиенте, так и на сервере.</span><span class="sxs-lookup"><span data-stu-id="ae72e-391">This includes all of the file information, but will leave the files on both the client and the server.</span></span> <span data-ttu-id="ae72e-392">Этот метод также оставляет объект в частично неинициализированном состоянии.</span><span class="sxs-lookup"><span data-stu-id="ae72e-392">This method also leaves the object in a partially uninitialized state.</span></span> <span data-ttu-id="ae72e-393">Единственные допустимые вызовы после этого [илсклокалсинкклиент:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) или [илсклокалсинкклиент:: Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="ae72e-393">The only valid calls after this are [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) or [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="ae72e-394">Этот метод можно вызвать, если происходит сбой инициализации и возвращается E_LSC_CACHEMISMATCH, и удаляется кэш, связанный с Супплиедид, который был предоставлен при сбое вызова.</span><span class="sxs-lookup"><span data-stu-id="ae72e-394">This method MAY be called if Initialize fails and returns E_LSC_CACHEMISMATCH, and will delete the cache associated with the SuppliedID that was provided with the failing call.</span></span>
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a><span data-ttu-id="ae72e-395">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-395">Parameters</span></span>

<span data-ttu-id="ae72e-396">Нет</span><span class="sxs-lookup"><span data-stu-id="ae72e-396">None</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-397">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-397">Return values</span></span>

|<span data-ttu-id="ae72e-398">Значение</span><span class="sxs-lookup"><span data-stu-id="ae72e-398">Value</span></span>|<span data-ttu-id="ae72e-399">Описание</span><span class="sxs-lookup"><span data-stu-id="ae72e-399">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae72e-400">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae72e-400">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae72e-401">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ae72e-401">The call failed.</span></span>  <br/> |
|<span data-ttu-id="ae72e-402">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae72e-402">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae72e-403">[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="ae72e-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was not successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae72e-404">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae72e-404">S_OK</span></span>  <br/> |<span data-ttu-id="ae72e-405">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="ae72e-405">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a><span data-ttu-id="ae72e-406">Илсклокалсинкклиент:: Серверфилечанже</span><span class="sxs-lookup"><span data-stu-id="ae72e-406">ILSCLocalSyncClient::ServerFileChange</span></span>
<span data-ttu-id="ae72e-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="ae72e-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="ae72e-408">Серверфилечанже указывает COM-объекту Ксисинкклиент пометить указанный файл для загрузки.</span><span class="sxs-lookup"><span data-stu-id="ae72e-408">ServerFileChange tells the CsiSyncClient COM object to mark the specified file for download.</span></span> <span data-ttu-id="ae72e-409">Если файл открыт в приложении Office для редактирования, этот метод возвратит S_OK, не помечая файл для загрузки (при наличии изменений приложение должно выполнить это действие).</span><span class="sxs-lookup"><span data-stu-id="ae72e-409">If the file is open in an Office application for edit, this method will return S_OK without marking the file for download (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="ae72e-410">Этот метод позволит загружать загружаемые файлы, если он был помечен как загруженные ранее (см. Ренамефиле).</span><span class="sxs-lookup"><span data-stu-id="ae72e-410">This method will allow downloads if it was marked as downloads blocked previously (see RenameFile).</span></span>
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="ae72e-411">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-411">Parameters</span></span>

|<span data-ttu-id="ae72e-412">Параметр</span><span class="sxs-lookup"><span data-stu-id="ae72e-412">Parameter</span></span>|<span data-ttu-id="ae72e-413">Описание</span><span class="sxs-lookup"><span data-stu-id="ae72e-413">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae72e-414">бстрфилесистемпас</span><span class="sxs-lookup"><span data-stu-id="ae72e-414">bstrFileSystemPath</span></span>  <br/> |<span data-ttu-id="ae72e-415">Строка, которая определяет файл на клиенте.</span><span class="sxs-lookup"><span data-stu-id="ae72e-415">A string which identifies the file on the client.</span></span> <span data-ttu-id="ae72e-416">Это значение должно быть непустым локальным путем длиной не более 256 символов.</span><span class="sxs-lookup"><span data-stu-id="ae72e-416">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="ae72e-417">Этот путь должен находиться в дереве каталогов, заданном параметром Филесистемдиректорихинт, при выполнении вызова метода Initialize.</span><span class="sxs-lookup"><span data-stu-id="ae72e-417">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="ae72e-418">бстрресаурцеид</span><span class="sxs-lookup"><span data-stu-id="ae72e-418">bstrResourceID</span></span>  <br/> |<span data-ttu-id="ae72e-419">Строка, определяющая значение ResourceID файла.</span><span class="sxs-lookup"><span data-stu-id="ae72e-419">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="ae72e-420">Это значение не должно быть пустым (не должно превышать 128 символов).</span><span class="sxs-lookup"><span data-stu-id="ae72e-420">This value must be non-empty with a maximum of 128 characters.</span></span>  <br/> |
|<span data-ttu-id="ae72e-421">бстрвебпас</span><span class="sxs-lookup"><span data-stu-id="ae72e-421">bstrWebPath</span></span>  <br/> |<span data-ttu-id="ae72e-422">Строка, которая определяет файл на сервере.</span><span class="sxs-lookup"><span data-stu-id="ae72e-422">A string which identifies the file on the server.</span></span> <span data-ttu-id="ae72e-423">Это значение должно быть непустым допустимым URL-адресом, но не превышать INTERNET_MAX_URL_LENGTH, как определено https://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="ae72e-423">This value must be a non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span>  <br/> |
   
##### <a name="return-values"></a><span data-ttu-id="ae72e-424">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-424">Return values</span></span>

|<span data-ttu-id="ae72e-425">Значение</span><span class="sxs-lookup"><span data-stu-id="ae72e-425">Value</span></span>|<span data-ttu-id="ae72e-426">Описание</span><span class="sxs-lookup"><span data-stu-id="ae72e-426">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae72e-427">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae72e-427">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae72e-428">Не удалось задать состояние подключения кэша.</span><span class="sxs-lookup"><span data-stu-id="ae72e-428">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="ae72e-429">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="ae72e-429">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="ae72e-430">Значение ResourceID для файла, указанного в параметре _бстрфилесистемпас_ , отличается от указанного.</span><span class="sxs-lookup"><span data-stu-id="ae72e-430">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span>  <br/> |
|<span data-ttu-id="ae72e-431">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="ae72e-431">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="ae72e-432">Объект COM Ксисинкклиент не поддерживает заданное расширение файла.</span><span class="sxs-lookup"><span data-stu-id="ae72e-432">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="ae72e-433">Обратитесь к разделу Жетсуппортедфиликстенсионс.</span><span class="sxs-lookup"><span data-stu-id="ae72e-433">See GetSupportedFileExtensions.</span></span>  <br/> |
|<span data-ttu-id="ae72e-434">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="ae72e-434">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="ae72e-435">Файл был удален в средней операции.</span><span class="sxs-lookup"><span data-stu-id="ae72e-435">The file was deleted in mid-operation.</span></span>  <br/> |
|<span data-ttu-id="ae72e-436">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae72e-436">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae72e-437">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="ae72e-437">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae72e-438">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="ae72e-438">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="ae72e-439">Данный Филесистемпас не находится в корневом каталоге, заданном параметром Филесистемдиректорихинт при вызове метода Initialize.</span><span class="sxs-lookup"><span data-stu-id="ae72e-439">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="ae72e-440">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae72e-440">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae72e-441">[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="ae72e-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae72e-442">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="ae72e-442">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="ae72e-443">Файл, указанный в параметре _бстрресаурцеид_ , отличается от указанного в параметре филесистемпас.</span><span class="sxs-lookup"><span data-stu-id="ae72e-443">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="ae72e-444">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="ae72e-444">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="ae72e-445">Указанный файл уже содержит ожидающие изменения в другом кэше и еще не может быть связан с кэшем потребителя.</span><span class="sxs-lookup"><span data-stu-id="ae72e-445">The specified file already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="ae72e-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="ae72e-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="ae72e-447">Указанный путь находится в другом кэше.</span><span class="sxs-lookup"><span data-stu-id="ae72e-447">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="ae72e-448">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae72e-448">S_OK</span></span>  <br/> |<span data-ttu-id="ae72e-449">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="ae72e-449">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a><span data-ttu-id="ae72e-450">Илсклокалсинкклиент:: Сетклиентконнективитистате</span><span class="sxs-lookup"><span data-stu-id="ae72e-450">ILSCLocalSyncClient::SetClientConnectivityState</span></span>
<span data-ttu-id="ae72e-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="ae72e-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="ae72e-452">Переводит кэш в оперативный или автономный режим.</span><span class="sxs-lookup"><span data-stu-id="ae72e-452">Sets the cache into an online or offline state.</span></span> <span data-ttu-id="ae72e-453">В автономном режиме Office не будет пытаться установить соединение с сервером для всех файлов в этом кэше, независимо от параметра _фблоккуплоадс_ каждого отдельного файла.</span><span class="sxs-lookup"><span data-stu-id="ae72e-453">If offline, Office will not attempt to communicate with the server for any files in that cache, regardless of each individual file's  _fBlockUploads_ setting.</span></span> 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a><span data-ttu-id="ae72e-454">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-454">Parameters</span></span>

 <span data-ttu-id="ae72e-455">_фисонлине_</span><span class="sxs-lookup"><span data-stu-id="ae72e-455">_fIsOnline_</span></span>
  
<span data-ttu-id="ae72e-456">Логическое значение, определяющее состояние подключения кэша.</span><span class="sxs-lookup"><span data-stu-id="ae72e-456">A boolean determining the connectivity state of the cache.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-457">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-457">Return values</span></span>

|<span data-ttu-id="ae72e-458">Значение</span><span class="sxs-lookup"><span data-stu-id="ae72e-458">Value</span></span>|<span data-ttu-id="ae72e-459">Описание</span><span class="sxs-lookup"><span data-stu-id="ae72e-459">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae72e-460">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae72e-460">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae72e-461">Не удалось задать состояние подключения кэша.</span><span class="sxs-lookup"><span data-stu-id="ae72e-461">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="ae72e-462">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae72e-462">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae72e-463">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="ae72e-463">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae72e-464">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae72e-464">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae72e-465">[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="ae72e-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae72e-466">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae72e-466">S_OK</span></span>  <br/> |<span data-ttu-id="ae72e-467">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="ae72e-467">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a><span data-ttu-id="ae72e-468">Илсклокалсинкклиент:: Сетклиентнетворксинкпермиссион</span><span class="sxs-lookup"><span data-stu-id="ae72e-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span></span>
<span data-ttu-id="ae72e-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="ae72e-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="ae72e-470">Сетклиентнетворксинкпермиссион используется для переопределения или Рестореоффице эвристических правил синхронизации для стоимости сети и потребления электроэнергии.</span><span class="sxs-lookup"><span data-stu-id="ae72e-470">SetClientNetworkSyncPermission is used to either override or restoreOffice's synchronizing heuristics for network cost and power usage.</span></span> <span data-ttu-id="ae72e-471">При использовании сети 3G или другой сети с высоким уровнем затрат или при работе от батарей и до подключения к сети, Office может блокировать сетевой трафик до тех пор, пока не будет оппортуне время.</span><span class="sxs-lookup"><span data-stu-id="ae72e-471">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span> <span data-ttu-id="ae72e-472">Потребитель этого API может использовать его для переопределения эвристики Office и принудительной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="ae72e-472">The consumer of this API can use it to override Office's heuristics and force synchronizing to occur.</span></span>
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a><span data-ttu-id="ae72e-473">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-473">Parameters</span></span>

 <span data-ttu-id="ae72e-474">_нсптипе_</span><span class="sxs-lookup"><span data-stu-id="ae72e-474">_nspType_</span></span>
  
<span data-ttu-id="ae72e-475">Флаг, определяющий, какой эвристикой затрат следует переопределить.</span><span class="sxs-lookup"><span data-stu-id="ae72e-475">A flag which defines which cost heuristic to override.</span></span> <span data-ttu-id="ae72e-476">В разделе [enum лскнетворксинкпермиссионтипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="ae72e-476">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span>
  
 <span data-ttu-id="ae72e-477">_фенаблесинк_</span><span class="sxs-lookup"><span data-stu-id="ae72e-477">_fEnableSync_</span></span>
  
<span data-ttu-id="ae72e-478">Указывает, следует ли принудительно выполнять синхронизацию, таким образом переопределяя более эвристику затрат или более не переопределять ее.</span><span class="sxs-lookup"><span data-stu-id="ae72e-478">Specifies whether to force synchronizing on, thus overriding that cost heuristic, or to no longer override it.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-479">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-479">Return values</span></span>

|<span data-ttu-id="ae72e-480">Значение</span><span class="sxs-lookup"><span data-stu-id="ae72e-480">Value</span></span>|<span data-ttu-id="ae72e-481">Описание</span><span class="sxs-lookup"><span data-stu-id="ae72e-481">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae72e-482">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae72e-482">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae72e-483">Не удалось переопределить эвристику синхронизации.</span><span class="sxs-lookup"><span data-stu-id="ae72e-483">Failure to override synchronizing heuristics.</span></span>  <br/> |
|<span data-ttu-id="ae72e-484">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae72e-484">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae72e-485">[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="ae72e-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae72e-486">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae72e-486">S_OK</span></span>  <br/> |<span data-ttu-id="ae72e-487">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="ae72e-487">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a><span data-ttu-id="ae72e-488">Илсклокалсинкклиент:: Uninitialize</span><span class="sxs-lookup"><span data-stu-id="ae72e-488">ILSCLocalSyncClient::Uninitialize</span></span>
<span data-ttu-id="ae72e-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span><span class="sxs-lookup"><span data-stu-id="ae72e-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span></span>

<span data-ttu-id="ae72e-490">Выгрузка кэша из COM-объекта и выполнение операций закрытия.</span><span class="sxs-lookup"><span data-stu-id="ae72e-490">Unloads the cache from the COM object and perform closing operations.</span></span> <span data-ttu-id="ae72e-491">[Илсклокалсинкклиент:: Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) Перед удалением COM-объекта необходимо вызвать метод.</span><span class="sxs-lookup"><span data-stu-id="ae72e-491">[ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUST be called before destroying the COM object.</span></span> <span data-ttu-id="ae72e-492">После вызова другие API не могут вызываться, COM-объект должен быть удален, а новый — создан, если вы хотите продолжить операции.</span><span class="sxs-lookup"><span data-stu-id="ae72e-492">Once called, no other APIs can be called, the COM object MUST be destroyed and a new one created if you wish to continue operations.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a><span data-ttu-id="ae72e-493">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-493">Parameters</span></span>

<span data-ttu-id="ae72e-494">Нет.</span><span class="sxs-lookup"><span data-stu-id="ae72e-494">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-495">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-495">Return values</span></span>

|<span data-ttu-id="ae72e-496">Значение</span><span class="sxs-lookup"><span data-stu-id="ae72e-496">Value</span></span>|<span data-ttu-id="ae72e-497">Описание</span><span class="sxs-lookup"><span data-stu-id="ae72e-497">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae72e-498">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae72e-498">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae72e-499">Сбой при невозможности инициализации.</span><span class="sxs-lookup"><span data-stu-id="ae72e-499">Failure to uninitialize.</span></span>  <br/> |
|<span data-ttu-id="ae72e-500">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ae72e-500">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="ae72e-501">[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="ae72e-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="ae72e-502">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae72e-502">S_OK</span></span>  <br/> |<span data-ttu-id="ae72e-503">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="ae72e-503">The call succeeded.</span></span>  <br/> |
   
### <a name="interface-ienumlscevent"></a><span data-ttu-id="ae72e-504">Интерфейс Иенумлсцевент</span><span class="sxs-lookup"><span data-stu-id="ae72e-504">Interface IEnumLSCEvent</span></span>

<span data-ttu-id="ae72e-505">Этот интерфейс представляет список событий Илсцевент.</span><span class="sxs-lookup"><span data-stu-id="ae72e-505">This interface represents a list of ILSCEvent events.</span></span>
  
<span data-ttu-id="ae72e-506">**Открытые функции элементов**</span><span class="sxs-lookup"><span data-stu-id="ae72e-506">**Public member functions**</span></span>

#### <a name="ienumlsceventfnext"></a><span data-ttu-id="ae72e-507">Иенумлсцевент:: Фнекст</span><span class="sxs-lookup"><span data-stu-id="ae72e-507">IEnumLSCEvent::FNext</span></span>

<span data-ttu-id="ae72e-508">Извлекает следующее событие из списка событий.</span><span class="sxs-lookup"><span data-stu-id="ae72e-508">Retrieves the next event from the list of events.</span></span>
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a><span data-ttu-id="ae72e-509">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-509">Parameters</span></span>

 <span data-ttu-id="ae72e-510">_ппилсцевент_</span><span class="sxs-lookup"><span data-stu-id="ae72e-510">_ppiLSCEvent_</span></span>
  
<span data-ttu-id="ae72e-511">Указатель на интерфейс Илсцевент.</span><span class="sxs-lookup"><span data-stu-id="ae72e-511">A pointer to an ILSCEvent interface.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-512">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-512">Return values</span></span>

|<span data-ttu-id="ae72e-513">Значение</span><span class="sxs-lookup"><span data-stu-id="ae72e-513">Value</span></span>|<span data-ttu-id="ae72e-514">Описание</span><span class="sxs-lookup"><span data-stu-id="ae72e-514">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae72e-515">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae72e-515">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae72e-516">Больше нет событий.</span><span class="sxs-lookup"><span data-stu-id="ae72e-516">There are no more events.</span></span>  <br/> |
|<span data-ttu-id="ae72e-517">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae72e-517">S_OK</span></span>  <br/> |<span data-ttu-id="ae72e-518">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="ae72e-518">The call was successful.</span></span>  <br/> |
   
#### <a name="ienumlsceventreset"></a><span data-ttu-id="ae72e-519">Иенумлсцевент:: Reset</span><span class="sxs-lookup"><span data-stu-id="ae72e-519">IEnumLSCEvent::Reset</span></span>

<span data-ttu-id="ae72e-520">Сбрасывает перечислитель к первому событию.</span><span class="sxs-lookup"><span data-stu-id="ae72e-520">Resets the enumerator to the first event.</span></span>
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a><span data-ttu-id="ae72e-521">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-521">Parameters</span></span>

<span data-ttu-id="ae72e-522">Нет.</span><span class="sxs-lookup"><span data-stu-id="ae72e-522">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-523">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-523">Return values</span></span>

<span data-ttu-id="ae72e-524">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="ae72e-524">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent"></a><span data-ttu-id="ae72e-525">Интерфейс Илсцевент</span><span class="sxs-lookup"><span data-stu-id="ae72e-525">Interface ILSCEvent</span></span>

<span data-ttu-id="ae72e-526">Этот интерфейс представляет событие синхронизации.</span><span class="sxs-lookup"><span data-stu-id="ae72e-526">This interface represents a synchronizing event.</span></span> <span data-ttu-id="ae72e-527">Все сведения о событии можно получить из интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ae72e-527">All information about the event can be retrieved from the interface.</span></span>
  
<span data-ttu-id="ae72e-528">**Открытые функции элементов**</span><span class="sxs-lookup"><span data-stu-id="ae72e-528">**Public member functions**</span></span>

#### <a name="ilsceventgetconflictstatus"></a><span data-ttu-id="ae72e-529">Илсцевент:: Жетконфликтстатус</span><span class="sxs-lookup"><span data-stu-id="ae72e-529">ILSCEvent::GetConflictStatus</span></span>

<span data-ttu-id="ae72e-530">Обратите внимание на то, что это значение заполняется при вызове метода [илсклокалсинкклиент::-Changes](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) , а не при создании события, поэтому отображается только текущее состояние файла, а не его состояние при изменении состояния конфликта.</span><span class="sxs-lookup"><span data-stu-id="ae72e-530">Note that this value is populated when [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) is called, not when the event was created, so you will only have the current status of the file, not the status of the file when the conflict status changed.</span></span> 
  
<span data-ttu-id="ae72e-531">Это значение заполняется только при LSCEventType_OnLocalConflictStateChanged [перечисления лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события.</span><span class="sxs-lookup"><span data-stu-id="ae72e-531">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnLocalConflictStateChanged.</span></span> 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a><span data-ttu-id="ae72e-532">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-532">Parameters</span></span>

 <span data-ttu-id="ae72e-533">_пфисинконфликт_</span><span class="sxs-lookup"><span data-stu-id="ae72e-533">_pfIsInConflict_</span></span>
  
<span data-ttu-id="ae72e-534">Текущее состояние конфликта файла, связанного с событием.</span><span class="sxs-lookup"><span data-stu-id="ae72e-534">The current conflict status of the file associated with the event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-535">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-535">Return values</span></span>

<span data-ttu-id="ae72e-536">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="ae72e-536">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeterror"></a><span data-ttu-id="ae72e-537">Илсцевент:: ошибка</span><span class="sxs-lookup"><span data-stu-id="ae72e-537">ILSCEvent::GetError</span></span>

<span data-ttu-id="ae72e-538">Это значение заполняется только в том случае, если [перечисление лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) для события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="ae72e-538">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a><span data-ttu-id="ae72e-539">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-539">Parameters</span></span>

 <span data-ttu-id="ae72e-540">_пнеррор_</span><span class="sxs-lookup"><span data-stu-id="ae72e-540">_pnError_</span></span>
  
<span data-ttu-id="ae72e-541">Ошибка, связанная с этим событием.</span><span class="sxs-lookup"><span data-stu-id="ae72e-541">The error associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-542">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-542">Return values</span></span>

<span data-ttu-id="ae72e-543">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="ae72e-543">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetetag"></a><span data-ttu-id="ae72e-544">Илсцевент::/ETag</span><span class="sxs-lookup"><span data-stu-id="ae72e-544">ILSCEvent::GetETag</span></span>

<span data-ttu-id="ae72e-545">Это значение заполняется только в том случае, если [перечисление лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) для события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="ae72e-545">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a><span data-ttu-id="ae72e-546">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-546">Parameters</span></span>

 <span data-ttu-id="ae72e-547">_пбстретаг_</span><span class="sxs-lookup"><span data-stu-id="ae72e-547">_pbstrETag_</span></span>
  
<span data-ttu-id="ae72e-548">ETag, связанный с этим событием</span><span class="sxs-lookup"><span data-stu-id="ae72e-548">The ETag associated with this event</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-549">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-549">Return values</span></span>

<span data-ttu-id="ae72e-550">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="ae72e-550">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeteventtype"></a><span data-ttu-id="ae72e-551">Илсцевент:: Жетевенттипе</span><span class="sxs-lookup"><span data-stu-id="ae72e-551">ILSCEvent::GetEventType</span></span>

<span data-ttu-id="ae72e-552">Получает тип данного события.</span><span class="sxs-lookup"><span data-stu-id="ae72e-552">Gets the type for this event.</span></span>
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a><span data-ttu-id="ae72e-553">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-553">Parameters</span></span>

 <span data-ttu-id="ae72e-554">_пневенттипе_</span><span class="sxs-lookup"><span data-stu-id="ae72e-554">_pnEventType_</span></span>
  
<span data-ttu-id="ae72e-555">Тип события для этого события.</span><span class="sxs-lookup"><span data-stu-id="ae72e-555">The event type of this event.</span></span> <span data-ttu-id="ae72e-556">Допустимые значения приведены в разделе [enum лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) .</span><span class="sxs-lookup"><span data-stu-id="ae72e-556">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for valid values.</span></span> <span data-ttu-id="ae72e-557">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="ae72e-557">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-558">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-558">Return values</span></span>

|<span data-ttu-id="ae72e-559">Значение</span><span class="sxs-lookup"><span data-stu-id="ae72e-559">Value</span></span>|<span data-ttu-id="ae72e-560">Описание</span><span class="sxs-lookup"><span data-stu-id="ae72e-560">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae72e-561">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae72e-561">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae72e-562">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="ae72e-562">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae72e-563">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae72e-563">S_OK</span></span>  <br/> |<span data-ttu-id="ae72e-564">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="ae72e-564">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a><span data-ttu-id="ae72e-565">Илсцевент:: Жетлокалворкингпас</span><span class="sxs-lookup"><span data-stu-id="ae72e-565">ILSCEvent::GetLocalWorkingPath</span></span>

<span data-ttu-id="ae72e-566">Получает путь к локальному рабочему пути для этого события.</span><span class="sxs-lookup"><span data-stu-id="ae72e-566">Gets the local working path for this event.</span></span>
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a><span data-ttu-id="ae72e-567">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-567">Parameters</span></span>

 <span data-ttu-id="ae72e-568">_пбстрлокалворкингпас_</span><span class="sxs-lookup"><span data-stu-id="ae72e-568">_pbstrLocalWorkingPath_</span></span>
  
<span data-ttu-id="ae72e-569">Локальный путь к файлу, к которому относится данное событие.</span><span class="sxs-lookup"><span data-stu-id="ae72e-569">The local path of the file to which this event pertains.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-570">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-570">Return values</span></span>

<span data-ttu-id="ae72e-571">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="ae72e-571">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceid"></a><span data-ttu-id="ae72e-572">Илсцевент:: Жетресаурцеид</span><span class="sxs-lookup"><span data-stu-id="ae72e-572">ILSCEvent::GetResourceID</span></span>

<span data-ttu-id="ae72e-573">Получает идентификатор ресурса для события.</span><span class="sxs-lookup"><span data-stu-id="ae72e-573">Gets the resource ID for the event.</span></span>
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="ae72e-574">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-574">Parameters</span></span>

 <span data-ttu-id="ae72e-575">_пбстрресаурцеид_</span><span class="sxs-lookup"><span data-stu-id="ae72e-575">_pbstrResourceID_</span></span>
  
<span data-ttu-id="ae72e-576">ResourceID файла, связанного с этим событием.</span><span class="sxs-lookup"><span data-stu-id="ae72e-576">The ResourceID of the file associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-577">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-577">Return values</span></span>

<span data-ttu-id="ae72e-578">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="ae72e-578">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceidattempted"></a><span data-ttu-id="ae72e-579">Илсцевент:: Жетресаурцеидаттемптед</span><span class="sxs-lookup"><span data-stu-id="ae72e-579">ILSCEvent::GetResourceIDAttempted</span></span>

<span data-ttu-id="ae72e-580">Это значение заполняется только при LSCEventType_OnFilePathConflict [перечисления лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события.</span><span class="sxs-lookup"><span data-stu-id="ae72e-580">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> <span data-ttu-id="ae72e-581">При вызове [илсклокалсинкклиент:: локалфилечанже ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [Илсклокалсинкклиент:: серверфилечанже ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)или [илсклокалсинкклиент:: RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) это приведет к созданию веб-пути или конфликта локального пути с другим файлом в кэше файлов Office.</span><span class="sxs-lookup"><span data-stu-id="ae72e-581">When a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) would cause a Web Path or Local Path collision with another file in the Office file cache, this event is generated.</span></span> 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a><span data-ttu-id="ae72e-582">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-582">Parameters</span></span>

 <span data-ttu-id="ae72e-583">_пбстрресаурцеидаттемптед_</span><span class="sxs-lookup"><span data-stu-id="ae72e-583">_pbstrResourceIDAttempted_</span></span>
  
<span data-ttu-id="ae72e-584">Значение ResourceID, которое вызвало создание события.</span><span class="sxs-lookup"><span data-stu-id="ae72e-584">The ResourceID that caused this event to get generated.</span></span> <span data-ttu-id="ae72e-585">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="ae72e-585">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-586">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-586">Return values</span></span>

<span data-ttu-id="ae72e-587">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="ae72e-587">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetsyncerrortype"></a><span data-ttu-id="ae72e-588">Илсцевент:: Жетсинцеррортипе</span><span class="sxs-lookup"><span data-stu-id="ae72e-588">ILSCEvent::GetSyncErrorType</span></span>

<span data-ttu-id="ae72e-589">Это значение заполняется только в том случае, если [перечисление лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) для события LSCEventType_OnServerChangesDownloaded или LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="ae72e-589">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a><span data-ttu-id="ae72e-590">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-590">Parameters</span></span>

 <span data-ttu-id="ae72e-591">_пнсинцеррортипе_</span><span class="sxs-lookup"><span data-stu-id="ae72e-591">_pnSyncErrorType_</span></span>
  
<span data-ttu-id="ae72e-592">Тип ошибки, связанный с этим событием.</span><span class="sxs-lookup"><span data-stu-id="ae72e-592">The error type associated with this event.</span></span> <span data-ttu-id="ae72e-593">Возможные значения приведены в разделе [enum лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) .</span><span class="sxs-lookup"><span data-stu-id="ae72e-593">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for potential values.</span></span> <span data-ttu-id="ae72e-594">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="ae72e-594">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-595">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-595">Return values</span></span>

|<span data-ttu-id="ae72e-596">Значение</span><span class="sxs-lookup"><span data-stu-id="ae72e-596">Value</span></span>|<span data-ttu-id="ae72e-597">Описание</span><span class="sxs-lookup"><span data-stu-id="ae72e-597">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae72e-598">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae72e-598">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae72e-599">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="ae72e-599">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae72e-600">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae72e-600">S_OK</span></span>  <br/> |<span data-ttu-id="ae72e-601">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="ae72e-601">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetwebpath"></a><span data-ttu-id="ae72e-602">Илсцевент:: Жетвебпас</span><span class="sxs-lookup"><span data-stu-id="ae72e-602">ILSCEvent::GetWebPath</span></span>

<span data-ttu-id="ae72e-603">Это значение заполняется только при LSCEventType_OnFilePathConflict [перечисления лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) события.</span><span class="sxs-lookup"><span data-stu-id="ae72e-603">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a><span data-ttu-id="ae72e-604">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-604">Parameters</span></span>

 <span data-ttu-id="ae72e-605">_пбстрвебпас_</span><span class="sxs-lookup"><span data-stu-id="ae72e-605">_pbstrWebPath_</span></span>
  
<span data-ttu-id="ae72e-606">Указывает веб-путь, связанный с этим событием.</span><span class="sxs-lookup"><span data-stu-id="ae72e-606">Specifies the Web Path associated with this event.</span></span> <span data-ttu-id="ae72e-607">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="ae72e-607">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-608">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-608">Return values</span></span>

<span data-ttu-id="ae72e-609">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="ae72e-609">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent2"></a><span data-ttu-id="ae72e-610">Интерфейс ILSCEvent2</span><span class="sxs-lookup"><span data-stu-id="ae72e-610">Interface ILSCEvent2</span></span>

<span data-ttu-id="ae72e-611">Этот интерфейс содержит дополнительные сведения о событии синхронизации.</span><span class="sxs-lookup"><span data-stu-id="ae72e-611">This interface holds additional information about a synchronizing event.</span></span>
  
<span data-ttu-id="ae72e-612">**Открытые функции элементов**</span><span class="sxs-lookup"><span data-stu-id="ae72e-612">**Public member functions**</span></span>

#### <a name="ilscevent2geterrorchain"></a><span data-ttu-id="ae72e-613">ILSCEvent2:: Жетеррорчаин</span><span class="sxs-lookup"><span data-stu-id="ae72e-613">ILSCEvent2::GetErrorChain</span></span>

<span data-ttu-id="ae72e-614">Получает сведения о цепочке ошибок для события синхронизации.</span><span class="sxs-lookup"><span data-stu-id="ae72e-614">Gets the error chain information about a synchronizing event.</span></span>
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a><span data-ttu-id="ae72e-615">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-615">Parameters</span></span>

 <span data-ttu-id="ae72e-616">_пбстреррорчаин_</span><span class="sxs-lookup"><span data-stu-id="ae72e-616">_pbstrErrorChain_</span></span>
  
<span data-ttu-id="ae72e-617">Строка, в которой хранятся сведения о цепочке ошибок.</span><span class="sxs-lookup"><span data-stu-id="ae72e-617">A string to hold the error chain information.</span></span> <span data-ttu-id="ae72e-618">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="ae72e-618">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-619">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-619">Return values</span></span>

|<span data-ttu-id="ae72e-620">Значение</span><span class="sxs-lookup"><span data-stu-id="ae72e-620">Value</span></span>|<span data-ttu-id="ae72e-621">Описание</span><span class="sxs-lookup"><span data-stu-id="ae72e-621">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae72e-622">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="ae72e-622">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="ae72e-623">Установленная версия Office не поддерживает этот интерфейс</span><span class="sxs-lookup"><span data-stu-id="ae72e-623">The installed version of Office does not support this interface</span></span>  <br/> |
|<span data-ttu-id="ae72e-624">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ae72e-624">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ae72e-625">Одно или несколько значений параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="ae72e-625">One or more of the parameter values are invalid.</span></span>  <br/> |
|<span data-ttu-id="ae72e-626">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="ae72e-626">E_FAIL</span></span>  <br/> |<span data-ttu-id="ae72e-627">Информация о цепочке ошибок недоступна.</span><span class="sxs-lookup"><span data-stu-id="ae72e-627">The error chain information is not available.</span></span>  <br/> |
|<span data-ttu-id="ae72e-628">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae72e-628">S_OK</span></span>  <br/> |<span data-ttu-id="ae72e-629">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="ae72e-629">The call was successful.</span></span>  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a><span data-ttu-id="ae72e-630">Интерфейс Ипартнерактивитикаллбакк</span><span class="sxs-lookup"><span data-stu-id="ae72e-630">Interface IPartnerActivityCallback</span></span>

<span data-ttu-id="ae72e-631">Этот интерфейс предоставляет функцию обратного вызова для COM-объекта Ксисинкклиент.</span><span class="sxs-lookup"><span data-stu-id="ae72e-631">This interface provides a callback function to the CSISyncClient COM object.</span></span>
  
<span data-ttu-id="ae72e-632">**Открытые функции элементов**</span><span class="sxs-lookup"><span data-stu-id="ae72e-632">**Public member functions**</span></span>

#### <a name="ipartneractivitycallbackeventoccurred"></a><span data-ttu-id="ae72e-633">Ипартнерактивитикаллбакк:: Евентоккурред</span><span class="sxs-lookup"><span data-stu-id="ae72e-633">IPartnerActivityCallback::EventOccurred</span></span>

<span data-ttu-id="ae72e-634">Это функция обратного вызова для объекта, данного COM-объекта Ксисинкклиент.</span><span class="sxs-lookup"><span data-stu-id="ae72e-634">This is a callback function on the object given to the CsiSyncClient COM object.</span></span> <span data-ttu-id="ae72e-635">Ожидается, что при возникновении события (см. [перечисление лсцевенттипеоккурред](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) для допустимых типов событий) COM-объект ксисинкклиент вызывает этот метод, засигнализациет получателя.</span><span class="sxs-lookup"><span data-stu-id="ae72e-635">It's expected that when an Event occurs (see [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid event types), the CsiSyncClient COM object will call this method, signalling the consumer.</span></span> 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a><span data-ttu-id="ae72e-636">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae72e-636">Parameters</span></span>

 <span data-ttu-id="ae72e-637">_ивенттипеоккурред_</span><span class="sxs-lookup"><span data-stu-id="ae72e-637">_eEventTypeOccurred_</span></span>
  
<span data-ttu-id="ae72e-638">Тип события для этого события.</span><span class="sxs-lookup"><span data-stu-id="ae72e-638">The event type of this event.</span></span> <span data-ttu-id="ae72e-639">Допустимые значения приведены в разделе [enum лсцевенттипеоккурред](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) .</span><span class="sxs-lookup"><span data-stu-id="ae72e-639">See [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid values.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="ae72e-640">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ae72e-640">Return values</span></span>

<span data-ttu-id="ae72e-641">Всегда возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="ae72e-641">Always returns S_OK.</span></span>
  
## <a name="enumerations"></a><span data-ttu-id="ae72e-642">Перечисления</span><span class="sxs-lookup"><span data-stu-id="ae72e-642">Enumerations</span></span>

<span data-ttu-id="ae72e-643">В Ксисинкклиент используются следующие перечисления.</span><span class="sxs-lookup"><span data-stu-id="ae72e-643">CSISyncClient uses the following enumerations.</span></span>
  
### <a name="enum-lsceventsyncerrortype"></a><span data-ttu-id="ae72e-644">Перечисление Лсцевентсинцеррортипе</span><span class="sxs-lookup"><span data-stu-id="ae72e-644">Enum LSCEventSyncErrorType</span></span>
<span data-ttu-id="ae72e-645"><a name="Enum_LSCEventSyncErrorType"> </a></span><span class="sxs-lookup"><span data-stu-id="ae72e-645"><a name="Enum_LSCEventSyncErrorType"> </a></span></span>

<span data-ttu-id="ae72e-646">Это перечисление указывает категории ошибок, которые могут возникать при синхронизации файла.</span><span class="sxs-lookup"><span data-stu-id="ae72e-646">This enumeration specifies the categories of errors that can occur while synchronizing a file.</span></span>
  
|<span data-ttu-id="ae72e-647">Перечисляем</span><span class="sxs-lookup"><span data-stu-id="ae72e-647">Enumerator</span></span>|<span data-ttu-id="ae72e-648">Описание</span><span class="sxs-lookup"><span data-stu-id="ae72e-648">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae72e-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span><span class="sxs-lookup"><span data-stu-id="ae72e-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span></span>  <br/> |<span data-ttu-id="ae72e-650">Ошибка синхронизации этого события, которая может требовать особой важности.</span><span class="sxs-lookup"><span data-stu-id="ae72e-650">The synchronizing error of this event was unexpected, and may require special consideration.</span></span> <span data-ttu-id="ae72e-651">По умолчанию пользователю может потребоваться последовать.</span><span class="sxs-lookup"><span data-stu-id="ae72e-651">By default, the user may have to intervene.</span></span>  <br/> |
|<span data-ttu-id="ae72e-652">LSCEventSyncErrorType_NoInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="ae72e-652">LSCEventSyncErrorType_NoInterventionRequired</span></span>  <br/> |<span data-ttu-id="ae72e-653">Ошибка синхронизации этого события не требует особой важности.</span><span class="sxs-lookup"><span data-stu-id="ae72e-653">The synchronizing error of this event does not need special consideration.</span></span> <span data-ttu-id="ae72e-654">Office будет автоматически обрабатывать его.</span><span class="sxs-lookup"><span data-stu-id="ae72e-654">Office will handle it automatically.</span></span>  <br/> |
|<span data-ttu-id="ae72e-655">LSCEventSyncErrorType_UserInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="ae72e-655">LSCEventSyncErrorType_UserInterventionRequired</span></span>  <br/> |<span data-ttu-id="ae72e-656">Для ошибки синхронизации этого события необходимо, чтобы пользователь решил эту проблему.</span><span class="sxs-lookup"><span data-stu-id="ae72e-656">The synchronizing error of this event requires a user to resolve it.</span></span> <span data-ttu-id="ae72e-657">Например, для ошибки слияния необходимо, чтобы пользователь открыл документ, а затем слить его.</span><span class="sxs-lookup"><span data-stu-id="ae72e-657">For example, merge conflict error requires a user to open the document and merge it.</span></span>  <br/> |
|<span data-ttu-id="ae72e-658">LSCEventSyncErrorType_WaitingOnClient</span><span class="sxs-lookup"><span data-stu-id="ae72e-658">LSCEventSyncErrorType_WaitingOnClient</span></span>  <br/> |<span data-ttu-id="ae72e-659">Для ошибки синхронизации этого события необходимо, чтобы потребитель натребовался, но не обязательно должен быть особым вопросом.</span><span class="sxs-lookup"><span data-stu-id="ae72e-659">The synchronizing error of this event requires the consumer to intervene, but should not require special consideration by the user.</span></span>  <br/> |
|<span data-ttu-id="ae72e-660">LSCEventSyncErrorType_ClientInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="ae72e-660">LSCEventSyncErrorType_ClientInterventionRequired</span></span>  <br/> |<span data-ttu-id="ae72e-661">Для ошибки синхронизации этого события необходимо, чтобы потребитель был особым случаем.</span><span class="sxs-lookup"><span data-stu-id="ae72e-661">The synchronizing error of this event requires the consumer to intervene as a special case.</span></span>  <br/> |
|<span data-ttu-id="ae72e-662">LSCEventSyncErrorType_Max</span><span class="sxs-lookup"><span data-stu-id="ae72e-662">LSCEventSyncErrorType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtype"></a><span data-ttu-id="ae72e-663">Перечисление Лсцевенттипе</span><span class="sxs-lookup"><span data-stu-id="ae72e-663">Enum LSCEventType</span></span>
<span data-ttu-id="ae72e-664"><a name="Enum_LSCEventType"> </a></span><span class="sxs-lookup"><span data-stu-id="ae72e-664"><a name="Enum_LSCEventType"> </a></span></span>

<span data-ttu-id="ae72e-665">Это перечисление определяет тип событий, которые могут возникать в определенном файле.</span><span class="sxs-lookup"><span data-stu-id="ae72e-665">This enumeration specifies the type of events that can occur for a particular file.</span></span>
  
|<span data-ttu-id="ae72e-666">Перечисляем</span><span class="sxs-lookup"><span data-stu-id="ae72e-666">Enumerator</span></span>|<span data-ttu-id="ae72e-667">Описание</span><span class="sxs-lookup"><span data-stu-id="ae72e-667">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae72e-668">LSCEventType_None</span><span class="sxs-lookup"><span data-stu-id="ae72e-668">LSCEventType_None</span></span>  <br/> ||
|<span data-ttu-id="ae72e-669">LSCEventType_OnLocalChanges</span><span class="sxs-lookup"><span data-stu-id="ae72e-669">LSCEventType_OnLocalChanges</span></span>  <br/> |<span data-ttu-id="ae72e-670">Изменения, внесенные в локальный файл.</span><span class="sxs-lookup"><span data-stu-id="ae72e-670">Changes were made to a local file.</span></span>  <br/> |
|<span data-ttu-id="ae72e-671">LSCEventType_OnOpenedByUser</span><span class="sxs-lookup"><span data-stu-id="ae72e-671">LSCEventType_OnOpenedByUser</span></span>  <br/> |<span data-ttu-id="ae72e-672">Пользователь открыл файл.</span><span class="sxs-lookup"><span data-stu-id="ae72e-672">A user opened a file.</span></span>  <br/> |
|<span data-ttu-id="ae72e-673">LSCEventType_OnServerChangesDownloaded</span><span class="sxs-lookup"><span data-stu-id="ae72e-673">LSCEventType_OnServerChangesDownloaded</span></span>  <br/> |<span data-ttu-id="ae72e-674">Загрузка изменений файлов с сервера завершена.</span><span class="sxs-lookup"><span data-stu-id="ae72e-674">Finished downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="ae72e-675">LSCEventType_OnLocalChangesUploaded</span><span class="sxs-lookup"><span data-stu-id="ae72e-675">LSCEventType_OnLocalChangesUploaded</span></span>  <br/> |<span data-ttu-id="ae72e-676">Отгрузка изменений файлов на сервер завершена.</span><span class="sxs-lookup"><span data-stu-id="ae72e-676">Finished uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="ae72e-677">LSCEventType_OnLocalConflictStateChanged</span><span class="sxs-lookup"><span data-stu-id="ae72e-677">LSCEventType_OnLocalConflictStateChanged</span></span>  <br/> |<span data-ttu-id="ae72e-678">Изменено состояние конфликта слияния файла.</span><span class="sxs-lookup"><span data-stu-id="ae72e-678">The merge conflict state of a file has changed.</span></span>  <br/> |
|<span data-ttu-id="ae72e-679">LSCEventType_OnFileAdded</span><span class="sxs-lookup"><span data-stu-id="ae72e-679">LSCEventType_OnFileAdded</span></span>  <br/> |<span data-ttu-id="ae72e-680">Добавлен файл.</span><span class="sxs-lookup"><span data-stu-id="ae72e-680">A file was added.</span></span>  <br/> |
|<span data-ttu-id="ae72e-681">LSCEventType_OnFileDeleted</span><span class="sxs-lookup"><span data-stu-id="ae72e-681">LSCEventType_OnFileDeleted</span></span>  <br/> |<span data-ttu-id="ae72e-682">Удален файл.</span><span class="sxs-lookup"><span data-stu-id="ae72e-682">A file was deleted.</span></span>  <br/> |
|<span data-ttu-id="ae72e-683">LSCEventType_OnSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="ae72e-683">LSCEventType_OnSyncEnabled</span></span>  <br/> |<span data-ttu-id="ae72e-684">Синхронизация для файлов пользователя включена.</span><span class="sxs-lookup"><span data-stu-id="ae72e-684">Synchronizing was enabled for a user's files.</span></span>  <br/> |
|<span data-ttu-id="ae72e-685">LSCEventType_OnServerChangesDownloadStarted</span><span class="sxs-lookup"><span data-stu-id="ae72e-685">LSCEventType_OnServerChangesDownloadStarted</span></span>  <br/> |<span data-ttu-id="ae72e-686">Началась загрузка изменений файлов с сервера.</span><span class="sxs-lookup"><span data-stu-id="ae72e-686">Started downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="ae72e-687">LSCEventType_OnLocalChangesUploadStarted</span><span class="sxs-lookup"><span data-stu-id="ae72e-687">LSCEventType_OnLocalChangesUploadStarted</span></span>  <br/> |<span data-ttu-id="ae72e-688">Начата отправка изменений файлов на сервер.</span><span class="sxs-lookup"><span data-stu-id="ae72e-688">Started uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="ae72e-689">LSCEventType_OnFilePathConflict</span><span class="sxs-lookup"><span data-stu-id="ae72e-689">LSCEventType_OnFilePathConflict</span></span>  <br/> |<span data-ttu-id="ae72e-690">Это событие создается при вызове [илсклокалсинкклиент:: локалфилечанже ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [Илсклокалсинкклиент:: серверфилечанже ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)или [Илсклокалсинкклиент:: RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) вызывает веб-путь или конфликты локального пути с другим файлом в кэше файлов Office.</span><span class="sxs-lookup"><span data-stu-id="ae72e-690">This event is generated when a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) causes a Web Path or Local Path collision with another file in the Office file cache.</span></span>  <br/> |
|<span data-ttu-id="ae72e-691">LSCEventType_OnFileForked</span><span class="sxs-lookup"><span data-stu-id="ae72e-691">LSCEventType_OnFileForked</span></span>  <br/> ||
|<span data-ttu-id="ae72e-692">LSCEventType_Max</span><span class="sxs-lookup"><span data-stu-id="ae72e-692">LSCEventType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a><span data-ttu-id="ae72e-693">Перечисление Лсцевенттипеоккурред</span><span class="sxs-lookup"><span data-stu-id="ae72e-693">Enum LSCEventTypeOccurred</span></span>
<span data-ttu-id="ae72e-694"><a name="Enum_LSCEventTypeOccurred"> </a></span><span class="sxs-lookup"><span data-stu-id="ae72e-694"><a name="Enum_LSCEventTypeOccurred"> </a></span></span>

<span data-ttu-id="ae72e-695">Это перечисление определяет тип событий, которые могут возникнуть.</span><span class="sxs-lookup"><span data-stu-id="ae72e-695">This enumeration specifies the type of events that can occur.</span></span> <span data-ttu-id="ae72e-696">Потребитель должен вызывать определенные функции Илсклокалсинкклиент на основе типа события.</span><span class="sxs-lookup"><span data-stu-id="ae72e-696">The consumer needs to call specific ILSCLocalSyncClient functions based on the event type.</span></span>
  
|<span data-ttu-id="ae72e-697">Перечисляем</span><span class="sxs-lookup"><span data-stu-id="ae72e-697">Enumerator</span></span>|<span data-ttu-id="ae72e-698">Описание</span><span class="sxs-lookup"><span data-stu-id="ae72e-698">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae72e-699">LSCEventTypeOccurred_GetChanges</span><span class="sxs-lookup"><span data-stu-id="ae72e-699">LSCEventTypeOccurred_GetChanges</span></span>  <br/> |<span data-ttu-id="ae72e-700">Произошла Илсцевент.</span><span class="sxs-lookup"><span data-stu-id="ae72e-700">An ILSCEvent has occurred.</span></span> <span data-ttu-id="ae72e-701">Потребитель должен вызывать [илсклокалсинкклиент::-Changes](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) для получения данных.</span><span class="sxs-lookup"><span data-stu-id="ae72e-701">The consumer should call [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) to retrieve the data.</span></span>  <br/> |
|<span data-ttu-id="ae72e-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="ae72e-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span></span>  <br/> |<span data-ttu-id="ae72e-703">Изменены поддерживаемые расширения файлов.</span><span class="sxs-lookup"><span data-stu-id="ae72e-703">The supported file extensions have changed.</span></span> <span data-ttu-id="ae72e-704">Потребитель должен вызвать [илсклокалсинкклиент:: жетсуппортедфиликстенсионс](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) , чтобы получить новый список поддерживаемых расширений.</span><span class="sxs-lookup"><span data-stu-id="ae72e-704">The consumer should call [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) to retrieve the new list of supported extensions.</span></span>  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a><span data-ttu-id="ae72e-705">Перечисление Лскнетворксинкпермиссионтипе</span><span class="sxs-lookup"><span data-stu-id="ae72e-705">Enum LSCNetworkSyncPermissionType</span></span>
<span data-ttu-id="ae72e-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span><span class="sxs-lookup"><span data-stu-id="ae72e-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span></span>

<span data-ttu-id="ae72e-707">Это перечисление указывает флаги, используемые для эвристики стоимости сети.</span><span class="sxs-lookup"><span data-stu-id="ae72e-707">This enumeration specifies the flags used for a network cost heuristic.</span></span> 

|<span data-ttu-id="ae72e-708">Перечисляем</span><span class="sxs-lookup"><span data-stu-id="ae72e-708">Enumerator</span></span>|<span data-ttu-id="ae72e-709">Описание</span><span class="sxs-lookup"><span data-stu-id="ae72e-709">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae72e-710">LSCNetworkSyncPermissionType_HighCost</span><span class="sxs-lookup"><span data-stu-id="ae72e-710">LSCNetworkSyncPermissionType_HighCost</span></span>  <br/> |<span data-ttu-id="ae72e-711">Значение true, если эвристика затрат для дорогостоящих сетей (например, 3G) переопределена.</span><span class="sxs-lookup"><span data-stu-id="ae72e-711">True if the cost heuristic for expensive networks (such as 3G) is overridden.</span></span>  <br/> |
|<span data-ttu-id="ae72e-712">LSCNetworkSyncPermissionType_HighPowerUsage</span><span class="sxs-lookup"><span data-stu-id="ae72e-712">LSCNetworkSyncPermissionType_HighPowerUsage</span></span>  <br/> |<span data-ttu-id="ae72e-713">Имеет значение true, если переопределяется эвристика затрат для использования питания (например, батарея).</span><span class="sxs-lookup"><span data-stu-id="ae72e-713">True if the cost heuristic for power usage (such as a battery) is overridden.</span></span>  <br/> |
   
### <a name="enum-lscstatusflag"></a><span data-ttu-id="ae72e-714">Перечисление Лскстатусфлаг</span><span class="sxs-lookup"><span data-stu-id="ae72e-714">Enum LSCStatusFlag</span></span>
<span data-ttu-id="ae72e-715"><a name="Enum_LSCStatusFlag"> </a></span><span class="sxs-lookup"><span data-stu-id="ae72e-715"><a name="Enum_LSCStatusFlag"> </a></span></span>

<span data-ttu-id="ae72e-716">Это перечисление используется для представления состояния синхронизации файла.</span><span class="sxs-lookup"><span data-stu-id="ae72e-716">This enumeration is used to represent the synchronize status of a file.</span></span> 
  
|<span data-ttu-id="ae72e-717">Перечисляем</span><span class="sxs-lookup"><span data-stu-id="ae72e-717">Enumerator</span></span>|<span data-ttu-id="ae72e-718">Описание</span><span class="sxs-lookup"><span data-stu-id="ae72e-718">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae72e-719">LCSStatusFlag_None</span><span class="sxs-lookup"><span data-stu-id="ae72e-719">LCSStatusFlag_None</span></span>  <br/> ||
|<span data-ttu-id="ae72e-720">LSCStatusFlag_UploadPending</span><span class="sxs-lookup"><span data-stu-id="ae72e-720">LSCStatusFlag_UploadPending</span></span>  <br/> |<span data-ttu-id="ae72e-721">Значение true, если имеются ожидающие данные для отправки в файл сервера.</span><span class="sxs-lookup"><span data-stu-id="ae72e-721">True if there is pending data to send to the server file.</span></span>  <br/> |
|<span data-ttu-id="ae72e-722">LSCStatusFlag_DownloadPending</span><span class="sxs-lookup"><span data-stu-id="ae72e-722">LSCStatusFlag_DownloadPending</span></span>  <br/> |<span data-ttu-id="ae72e-723">Значение true, если ожидаются данные, которые требуется скачать из файла сервера.</span><span class="sxs-lookup"><span data-stu-id="ae72e-723">True if there is pending data to download from the server file.</span></span>  <br/> |
|<span data-ttu-id="ae72e-724">LSCStatusFlag_LocalFileUnchanged</span><span class="sxs-lookup"><span data-stu-id="ae72e-724">LSCStatusFlag_LocalFileUnchanged</span></span>  <br/> |<span data-ttu-id="ae72e-725">Значение true, если в кэше данных в файле есть последняя копия данных на диске.</span><span class="sxs-lookup"><span data-stu-id="ae72e-725">True if the data Office has on the file in its cache is the most recent copy of the data on disk.</span></span>  <br/> |
   

