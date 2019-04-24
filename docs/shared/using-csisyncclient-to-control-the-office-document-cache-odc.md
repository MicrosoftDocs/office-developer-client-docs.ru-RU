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
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a><span data-ttu-id="59566-103">Использование Ксисинкклиент для управления кэшем документов Office (ODC)</span><span class="sxs-lookup"><span data-stu-id="59566-103">Using CSISyncClient to control the Office Document Cache (ODC)</span></span>

<span data-ttu-id="59566-104">Узнайте, как использовать Ксисинкклиент для управления кэшем документов Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="59566-104">Learn how to use CSISyncClient to control the Office Document Cache (ODC).</span></span>
  
<span data-ttu-id="59566-105">Ксисинкклиент — это встроенный COM-сервер (Ксисинкклиент. exe), позволяющий Microsoft OneDrive управлять поведением кэша документов Office (ODC).</span><span class="sxs-lookup"><span data-stu-id="59566-105">CSISyncClient is an out-of-proc COM server (CsiSyncClient.exe) that allows Microsoft OneDrive to control the behavior of the Office Document Cache (ODC).</span></span> <span data-ttu-id="59566-106">Например, OneDrive может позвонить на ODC через Ксисинкклиент для отправки и загрузки файлов в конечные точки с включенной поддержкой MS-FSSHTTP.</span><span class="sxs-lookup"><span data-stu-id="59566-106">For example, OneDrive may call upon the ODC via CSISyncClient to upload and download files to and from MS-FSSHTTP enabled endpoints.</span></span> <span data-ttu-id="59566-107">Это позволяет расширенным функциям, поддерживающим обслуживание, в Office, например, совместном редактировании и переходе из автономного режима в оперативный.</span><span class="sxs-lookup"><span data-stu-id="59566-107">This enables advanced service-backed features in Office, such as co-authoring and seamless transitions from offline to online.</span></span>
  
<span data-ttu-id="59566-108">Ксисинкклиент доступен на рабочем столе Office (x86 и x64).</span><span class="sxs-lookup"><span data-stu-id="59566-108">CsiSyncClient is available in Office Desktop (both x86 and x64).</span></span> <span data-ttu-id="59566-109">Примечание. в то время как новые версии Office могут поставляться с Ксисинкклиент, этот процесс будет использоваться только для обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="59566-109">Note: While newer versions of Office may ship with CsiSyncClient, the process will be used for backward compatibility only.</span></span> <span data-ttu-id="59566-110">Интерфейс Ксисинкклиент и методология управления ODC будут изменены в следующих версиях Office.</span><span class="sxs-lookup"><span data-stu-id="59566-110">The CsiSyncClient interface and the methodology of controlling the ODC will change in future versions of Office.</span></span>
  
<span data-ttu-id="59566-111">В настоящее время идентификатор класса имеет значение "ответить только на OneDrive".</span><span class="sxs-lookup"><span data-stu-id="59566-111">The class ID is currently set to respond only to OneDrive.</span></span>
  
<span data-ttu-id="59566-112">COM-объект можно использовать в качестве внепроцессных COM-серверов и работает в Ксисинкклиент. exe.</span><span class="sxs-lookup"><span data-stu-id="59566-112">The COM object is usable as an out-of-proc COM server and runs in CsiSyncClient.exe.</span></span> <span data-ttu-id="59566-113">В связи с ограничениями на доступ (используемая в ODC), она поставляется с типом бита, в котором находится Office, поэтому платформа x64 Office означает, что используется COM-объект на 64-разрядной версии, или x86 — COM-объект x86.</span><span class="sxs-lookup"><span data-stu-id="59566-113">Due to limitations with Access (which the ODC uses), it ships with the bit type that Office comes in, so x64 Office means an x64 COM object, or x86 Office means an x86 COM object.</span></span> <span data-ttu-id="59566-114">Чтобы обойти это ограничение, при указании КЛСКТКС_ЛОКАЛ_СЕРВЕР в составе компонента CoCreateInstance будет размещен COM-объект как внешний COM-сервер, что обеспечивает совместимость с несколькими разрядами.</span><span class="sxs-lookup"><span data-stu-id="59566-114">To get around this limitation, specifying CLSCTX_LOCAL_SERVER as part of the CoCreateInstance will have the COM object be hosted as an out-of-proc COM server, allowing cross-bitness compatibility.</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="59566-115">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="59566-115">Interfaces</span></span>

<span data-ttu-id="59566-116">В Ксисинкклиент используются следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="59566-116">CSISyncClient uses the following interfaces.</span></span>
  
### <a name="interface-ilsclocalsyncclient"></a><span data-ttu-id="59566-117">Интерфейс Илсклокалсинкклиент</span><span class="sxs-lookup"><span data-stu-id="59566-117">Interface ILSCLocalSyncClient</span></span>

<span data-ttu-id="59566-118">Это основной интерфейс, используемый для синхронизации файлов в Office.</span><span class="sxs-lookup"><span data-stu-id="59566-118">This is the primary interface used to synchronize files in Office.</span></span>
  
- <span data-ttu-id="59566-119">ProgID: Office. Локалсинкклиент</span><span class="sxs-lookup"><span data-stu-id="59566-119">ProgID: Office.LocalSyncClient</span></span>
- <span data-ttu-id="59566-120">CLSID: {14286318 – B6CF — 49a1 — 81FC. D74AD94902F9}</span><span class="sxs-lookup"><span data-stu-id="59566-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span></span>
- <span data-ttu-id="59566-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span><span class="sxs-lookup"><span data-stu-id="59566-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span></span>
   
<span data-ttu-id="59566-122">Предоставляемый COM-объект используется в качестве сервера вне процесса.</span><span class="sxs-lookup"><span data-stu-id="59566-122">The COM object that is exposed is used as an out-of-proc server.</span></span> <span data-ttu-id="59566-123">Указание КЛСКТКС_ЛОКАЛ_СЕРВЕР в составе компонента CoCreateInstance обеспечивает возможность совместимости между 64 64 и 32 – 32 процессами.</span><span class="sxs-lookup"><span data-stu-id="59566-123">Specifying CLSCTX_LOCAL_SERVER as part of CoCreateInstance allows compatability between 64bit and 32bit processes.</span></span>
  
<span data-ttu-id="59566-124">После создания объекта COM необходимо вызвать метод [илсклокалсинкклиент:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) First.</span><span class="sxs-lookup"><span data-stu-id="59566-124">Once you've co-created the COM object, you MUST call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) first.</span></span> <span data-ttu-id="59566-125">После [илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) успешно завершена, вы можете вызвать любой API так часто, как вы хотите и в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="59566-125">Once [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has completed successfully, you may call any API as often as you wish and in any order.</span></span> <span data-ttu-id="59566-126">Вы также можете вызвать метод [илсклокалсинкклиент:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) для уже инициализированного объекта, но при этом ничего не происходит.</span><span class="sxs-lookup"><span data-stu-id="59566-126">You may also call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) on an already initialized object, but this does nothing.</span></span> 
  
<span data-ttu-id="59566-127">Исключениями из предыдущего абзаца являются [илсклокалсинкклиент:: ресеткаче](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) и [илсклокалсинкклиент:: Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="59566-127">The exceptions to the previous paragraph are [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) and [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="59566-128">После вызова [илсклокалсинкклиент:: Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) для объекта COM необходимо удалить этот объект и создать новый.</span><span class="sxs-lookup"><span data-stu-id="59566-128">After you call [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) on the COM object, you MUST destroy that object and create a new one.</span></span> <span data-ttu-id="59566-129">[Илсклокалсинкклиент:: ресеткаче](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) удалит ваш подкэш, удалите все связанные сведения о файле в кэше, но оставьте документы на диске.</span><span class="sxs-lookup"><span data-stu-id="59566-129">[ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) will delete your subcache, delete all associated file information in the cache, but leave the documents on disk.</span></span> <span data-ttu-id="59566-130">Кроме того, он оставляет состояние неизменным для связи с кэшем.</span><span class="sxs-lookup"><span data-stu-id="59566-130">It also leaves the state intact for communicating with the cache.</span></span> <span data-ttu-id="59566-131">Это позволяет вызывать [илсклокалсинкклиент:: инициализировать](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) еще раз, чтобы создать новый кэш без необходимости уничтожения и повторного создания com-объекта.</span><span class="sxs-lookup"><span data-stu-id="59566-131">This allows you to call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) again to create a new cache without having to destroy and recreate the COM object.</span></span> 
  
<span data-ttu-id="59566-132">**Открытые функции элементов**</span><span class="sxs-lookup"><span data-stu-id="59566-132">**Public member functions**</span></span>

#### <a name="ilsclocalsyncclientdeletefile"></a><span data-ttu-id="59566-133">Илсклокалсинкклиент::D Елетефиле</span><span class="sxs-lookup"><span data-stu-id="59566-133">ILSCLocalSyncClient::DeleteFile</span></span>

<span data-ttu-id="59566-134">DeleteFile используется для удаления сведений о файле из кэша.</span><span class="sxs-lookup"><span data-stu-id="59566-134">DeleteFile is used to remove the file information from the cache.</span></span> <span data-ttu-id="59566-135">Тем не менее, этот метод оставляет связанный файл на диске и на сервере.</span><span class="sxs-lookup"><span data-stu-id="59566-135">However, this method will leave the associated file on disk and on the server.</span></span>
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="59566-136">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-136">Parameters</span></span>

 <span data-ttu-id="59566-137">_Бстрресаурцеид_</span><span class="sxs-lookup"><span data-stu-id="59566-137">_bstrResourceID_</span></span>
  
<span data-ttu-id="59566-138">Строка, которая определяет значение ResourceID файла.</span><span class="sxs-lookup"><span data-stu-id="59566-138">The string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="59566-139">Это значение не должно быть пустым (не должно превышать 128 символов).</span><span class="sxs-lookup"><span data-stu-id="59566-139">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="59566-140">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-140">Return values</span></span>

|<span data-ttu-id="59566-141">Значение</span><span class="sxs-lookup"><span data-stu-id="59566-141">Value</span></span>|<span data-ttu-id="59566-142">Описание</span><span class="sxs-lookup"><span data-stu-id="59566-142">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="59566-143">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="59566-143">E_FAIL</span></span>  <br/> |<span data-ttu-id="59566-144">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="59566-144">The call failed.</span></span>  <br/> |
|<span data-ttu-id="59566-145">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="59566-145">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="59566-146">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="59566-146">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="59566-147">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="59566-147">E_FAIL</span></span>  <br/> |<span data-ttu-id="59566-148">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="59566-148">The call failed.</span></span>  <br/> |
|<span data-ttu-id="59566-149">Е_ЛСК_ФИЛЕНОТФАУНД</span><span class="sxs-lookup"><span data-stu-id="59566-149">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="59566-150">Данный ResourceID не находится в кэше.</span><span class="sxs-lookup"><span data-stu-id="59566-150">The given ResourceID is not in the cache.</span></span>  <br/> |
|<span data-ttu-id="59566-151">Е_ЛСК_НОТИНИТИАЛИЗЕД</span><span class="sxs-lookup"><span data-stu-id="59566-151">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="59566-152">Инициализация не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="59566-152">Initialize has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="59566-153">Е_ЛСК_ПЕНДИНГЧАНЖЕСИНКАЧЕ</span><span class="sxs-lookup"><span data-stu-id="59566-153">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="59566-154">Файл в настоящее время синхронизируется или открывается, и его невозможно удалить.</span><span class="sxs-lookup"><span data-stu-id="59566-154">The file is currently synchronizing or open and cannot be deleted.</span></span>  <br/> |
|<span data-ttu-id="59566-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="59566-155">S_OK</span></span>  <br/> |<span data-ttu-id="59566-156">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="59566-156">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a><span data-ttu-id="59566-157">Илсклокалсинкклиент:: Changes</span><span class="sxs-lookup"><span data-stu-id="59566-157">ILSCLocalSyncClient::GetChanges</span></span>
<span data-ttu-id="59566-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span><span class="sxs-lookup"><span data-stu-id="59566-158"></span></span>

<span data-ttu-id="59566-159">Метод GetNext возвращает перечислитель объектов Илсцевент, а также возвращает маркер, который передается следующему вызову метода GetNext, предполагая, что потребитель обработал предыдущий набор событий.</span><span class="sxs-lookup"><span data-stu-id="59566-159">GetChanges returns an enumerator of ILSCEvent objects, and also returns a token that is given to the next call to GetChanges, assuming the consumer has processed the previous set of events.</span></span> <span data-ttu-id="59566-160">События, предшествующие указанному _нпревиаусчанжестокен_ , будут удалены и недоступны.</span><span class="sxs-lookup"><span data-stu-id="59566-160">Events before the  _nPreviousChangesToken_ specified will be deleted and unavailable.</span></span> <span data-ttu-id="59566-161">Если события для обработки отсутствуют, _пнкуррентчанжестокен_ должно иметь то же значение, что и _Нпревиаусчанжестокен_, но _ппиевентс_ по-прежнему будет задано.</span><span class="sxs-lookup"><span data-stu-id="59566-161">If there are no events to be processed,  _pnCurrentChangesToken_ should be the same value as  _nPreviousChangesToken_, but  _ppiEvents_ will still be set.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a><span data-ttu-id="59566-162">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-162">Parameters</span></span>

 <span data-ttu-id="59566-163">_Нпревиаусчанжестокен_</span><span class="sxs-lookup"><span data-stu-id="59566-163">_nPreviousChangesToken_</span></span>
  
<span data-ttu-id="59566-164">Определяет, какое событие было последний раз обработано потребителем.</span><span class="sxs-lookup"><span data-stu-id="59566-164">Identifies which event was last processed by the consumer.</span></span> 
  
 <span data-ttu-id="59566-165">_Пнкуррентчанжестокен_</span><span class="sxs-lookup"><span data-stu-id="59566-165">_pnCurrentChangesToken_</span></span>
  
<span data-ttu-id="59566-166">Определяет Последнее событие, переданное потребителю.</span><span class="sxs-lookup"><span data-stu-id="59566-166">Identifies the most recent event being handed to the consumer.</span></span> <span data-ttu-id="59566-167">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="59566-167">Must not be null.</span></span>
  
 <span data-ttu-id="59566-168">_Ппиевентс_</span><span class="sxs-lookup"><span data-stu-id="59566-168">_ppiEvents_</span></span>
  
<span data-ttu-id="59566-169">Перечислитель для событий, которые передаются потребителю.</span><span class="sxs-lookup"><span data-stu-id="59566-169">An enumerator for the events handed to the consumer.</span></span> <span data-ttu-id="59566-170">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="59566-170">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="59566-171">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-171">Return values</span></span>

|<span data-ttu-id="59566-172">Значение</span><span class="sxs-lookup"><span data-stu-id="59566-172">Value</span></span>|<span data-ttu-id="59566-173">Описание</span><span class="sxs-lookup"><span data-stu-id="59566-173">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="59566-174">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="59566-174">E_FAIL</span></span>  <br/> |<span data-ttu-id="59566-175">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="59566-175">The call failed.</span></span>  <br/> |
|<span data-ttu-id="59566-176">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="59566-176">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="59566-177">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="59566-177">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="59566-178">Е_ЛСК_НОТИНИТИАЛИЗЕД</span><span class="sxs-lookup"><span data-stu-id="59566-178">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="59566-179">[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="59566-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="59566-180">S_OK</span><span class="sxs-lookup"><span data-stu-id="59566-180">S_OK</span></span>  <br/> |<span data-ttu-id="59566-181">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="59566-181">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a><span data-ttu-id="59566-182">Илсклокалсинкклиент:: Жетклиентнетворксинкпермиссион</span><span class="sxs-lookup"><span data-stu-id="59566-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span></span>

<span data-ttu-id="59566-183">Жетклиентнетворксинкпермиссион используется, чтобы запросить, переопределяются ли эвристика синхронизации Office для стоимости сети и энергопотребления.</span><span class="sxs-lookup"><span data-stu-id="59566-183">GetClientNetworkSyncPermission is used to query whether Office's synchronizing heuristics for network cost and power usage are overridden.</span></span> <span data-ttu-id="59566-184">При использовании сети 3G или другой сети с высоким уровнем затрат или при работе от батарей и до подключения к сети, Office может блокировать сетевой трафик до тех пор, пока не будет оппортуне время.</span><span class="sxs-lookup"><span data-stu-id="59566-184">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span>
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a><span data-ttu-id="59566-185">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-185">Parameters</span></span>

 <span data-ttu-id="59566-186">_Нсптипе_</span><span class="sxs-lookup"><span data-stu-id="59566-186">_nspType_</span></span>
  
<span data-ttu-id="59566-187">Флаг, определяющий, какой эвристический объект затрат необходимо запросить.</span><span class="sxs-lookup"><span data-stu-id="59566-187">A flag which defines which cost heuristic to query.</span></span> <span data-ttu-id="59566-188">В разделе [enum лскнетворксинкпермиссионтипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="59566-188">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span> 
  
 <span data-ttu-id="59566-189">_Пфсинценаблед_</span><span class="sxs-lookup"><span data-stu-id="59566-189">_pfSyncEnabled_</span></span>
  
<span data-ttu-id="59566-190">Указывает, является ли запрошенный эвристический алгоритм затрат в данный момент перегруженным или нет.</span><span class="sxs-lookup"><span data-stu-id="59566-190">Specifies whether the requested cost heuristic is currently overridden or not.</span></span> <span data-ttu-id="59566-191">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="59566-191">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="59566-192">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-192">Return values</span></span>

|<span data-ttu-id="59566-193">Значение</span><span class="sxs-lookup"><span data-stu-id="59566-193">Value</span></span>|<span data-ttu-id="59566-194">Описание</span><span class="sxs-lookup"><span data-stu-id="59566-194">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="59566-195">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="59566-195">E_FAIL</span></span>  <br/> |<span data-ttu-id="59566-196">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="59566-196">The call failed.</span></span>  <br/> |
|<span data-ttu-id="59566-197">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="59566-197">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="59566-198">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="59566-198">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="59566-199">Е_ЛСК_НОТИНИТИАЛИЗЕД</span><span class="sxs-lookup"><span data-stu-id="59566-199">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="59566-200">[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="59566-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="59566-201">S_OK</span><span class="sxs-lookup"><span data-stu-id="59566-201">S_OK</span></span>  <br/> |<span data-ttu-id="59566-202">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="59566-202">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a><span data-ttu-id="59566-203">Илсклокалсинкклиент:: Жетфилестатус</span><span class="sxs-lookup"><span data-stu-id="59566-203">ILSCLocalSyncClient::GetFileStatus</span></span>

<span data-ttu-id="59566-204">Жетфилестатус используется для сбора сведений о конкретном файле: независимо от того, существует ли он в кэше, если у него есть ожидающая связь с копией на сервере, и если Office 2013 имеет самые актуальные данные из локальной копии.</span><span class="sxs-lookup"><span data-stu-id="59566-204">GetFileStatus is used to gather information for a specific file: whether it exists in the cache, if it has pending communication with the server copy, and if Office 2013 has the most up to date data from the local copy.</span></span> <span data-ttu-id="59566-205">Для определения сведений, к которым необходимо запросить COM-объект Ксисинкклиент, требуется битовый флаг значений [перечисления лскстатусфлаг](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) .</span><span class="sxs-lookup"><span data-stu-id="59566-205">It requires a bitwise flag of [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) values to determine what information the CsiSyncClient COM object is to query for.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a><span data-ttu-id="59566-206">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-206">Parameters</span></span>

 <span data-ttu-id="59566-207">_Бстрресаурцеид_</span><span class="sxs-lookup"><span data-stu-id="59566-207">_bstrResourceID_</span></span>
  
<span data-ttu-id="59566-208">Строка, которая определяет файл на клиенте.</span><span class="sxs-lookup"><span data-stu-id="59566-208">The string which identifies the file on the client.</span></span> <span data-ttu-id="59566-209">Это значение не должно быть пустым, не более 128 символов.</span><span class="sxs-lookup"><span data-stu-id="59566-209">This value must be non-empty, with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="59566-210">_Сфрекуестедстатус_</span><span class="sxs-lookup"><span data-stu-id="59566-210">_sfRequestedStatus_</span></span>
  
<span data-ttu-id="59566-211">Флаг, определяющий возвращаемую информацию.</span><span class="sxs-lookup"><span data-stu-id="59566-211">A flag which defines what information to return.</span></span> <span data-ttu-id="59566-212">В разделе [enum лскстатусфлаг](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="59566-212">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
 <span data-ttu-id="59566-213">_Пбстрфилесистемпас_</span><span class="sxs-lookup"><span data-stu-id="59566-213">_pbstrFileSystemPath_</span></span>
  
<span data-ttu-id="59566-214">Строка, которая определяет расположение файла, определенного _бстрресаурцеид_ в клиенте.</span><span class="sxs-lookup"><span data-stu-id="59566-214">The string which identifies the location of the file identified by  _bstrResourceID_ on the client.</span></span> <span data-ttu-id="59566-215">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="59566-215">Must not be null.</span></span> 
  
 <span data-ttu-id="59566-216">_Пбстретаг_</span><span class="sxs-lookup"><span data-stu-id="59566-216">_pbstrETag_</span></span>
  
<span data-ttu-id="59566-217">Строка, которая будет содержать тег eTag для файла, указанного с помощью _бстрресаурцеид_.</span><span class="sxs-lookup"><span data-stu-id="59566-217">A string which will contain the eTag for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="59566-218">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="59566-218">Must not be null.</span></span> 
  
 <span data-ttu-id="59566-219">_Псффилестатус_</span><span class="sxs-lookup"><span data-stu-id="59566-219">_psfFileStatus_</span></span>
  
<span data-ttu-id="59566-220">Флаг, который будет содержать состояние, запрошенное через _сфрекуестедстатус_ , для файла, определенного _бстрресаурцеид_.</span><span class="sxs-lookup"><span data-stu-id="59566-220">A flag which will contain the status requested via  _sfRequestedStatus_ for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="59566-221">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="59566-221">Must not be null.</span></span> <span data-ttu-id="59566-222">В разделе [enum лскстатусфлаг](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="59566-222">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="59566-223">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-223">Return values</span></span>

|<span data-ttu-id="59566-224">Значение</span><span class="sxs-lookup"><span data-stu-id="59566-224">Value</span></span>|<span data-ttu-id="59566-225">Описание</span><span class="sxs-lookup"><span data-stu-id="59566-225">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="59566-226">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="59566-226">E_FAIL</span></span>  <br/> |<span data-ttu-id="59566-227">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="59566-227">The call failed.</span></span>  <br/> |
|<span data-ttu-id="59566-228">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="59566-228">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="59566-229">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="59566-229">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="59566-230">Е_ЛСК_ФИЛЕНОТФАУНД</span><span class="sxs-lookup"><span data-stu-id="59566-230">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="59566-231">Сведения о файле, указанные в _бстрресаурцеид_ , не существуют в кэше.</span><span class="sxs-lookup"><span data-stu-id="59566-231">The file information specified by  _bstrResourceID_ does not exist in the cache.</span></span>  <br/> |
|<span data-ttu-id="59566-232">Е_ЛСК_ЛОКАЛФИЛЕУНАВАИЛАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="59566-232">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="59566-233">Запрошен Лскстатусфлаг_локалфилеунчанжед или файл, указанный в _бстрресаурцеид_ , заблокирован или отсутствует.</span><span class="sxs-lookup"><span data-stu-id="59566-233">LSCStatusFlag_LocalFileUnchanged was requested or the file specified by  _bstrResourceID_ is locked or missing.</span></span>  <br/> |
|<span data-ttu-id="59566-234">Е_ЛСК_НОТИНИТИАЛИЗЕД</span><span class="sxs-lookup"><span data-stu-id="59566-234">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="59566-235">[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="59566-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="59566-236">S_OK</span><span class="sxs-lookup"><span data-stu-id="59566-236">S_OK</span></span>  <br/> |<span data-ttu-id="59566-237">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="59566-237">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a><span data-ttu-id="59566-238">Илсклокалсинкклиент:: Жетсуппортедфиликстенсионс</span><span class="sxs-lookup"><span data-stu-id="59566-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span></span>
<span data-ttu-id="59566-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span><span class="sxs-lookup"><span data-stu-id="59566-239"></span></span>

<span data-ttu-id="59566-240">Жетсуппортедфиликстенсионс возвращает список расширений файлов с разделением каналов, которые в настоящее время поддерживаются объектом COM Ксисинкклиент.</span><span class="sxs-lookup"><span data-stu-id="59566-240">GetSupportedFileExtensions returns a list of pipe-delimited file extensions which are currently supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="59566-241">Обратите внимание, что этот список может измениться, а потребитель будет уведомлен об изменении с помощью объекта Ипартнерактивитикаллбакк, предоставленного в [илсклокалсинкклиент:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (см евентоккуред).</span><span class="sxs-lookup"><span data-stu-id="59566-241">Note that this list may change, and the consumer will be notified of a change via the IPartnerActivityCallback object provided on [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (See EventOccured).</span></span> 
  
<span data-ttu-id="59566-242">Ниже приведен пример возвращаемой строки: "| docx | DOCM | pptx |"</span><span class="sxs-lookup"><span data-stu-id="59566-242">An example of the string returned is as follows: "|docx|docm|pptx|"</span></span>
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a><span data-ttu-id="59566-243">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-243">Parameters</span></span>

 <span data-ttu-id="59566-244">_Пбстрсуппортедфиликстенсионс_</span><span class="sxs-lookup"><span data-stu-id="59566-244">_pbstrSupportedFileExtensions_</span></span>
  
<span data-ttu-id="59566-245">Строка, для которой задается набор расширений файлов с разделителем каналов, поддерживаемый COM-объектом Ксисинкклиент.</span><span class="sxs-lookup"><span data-stu-id="59566-245">A string to be set with a pipe-delimited set of file extensions supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="59566-246">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="59566-246">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="59566-247">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-247">Return values</span></span>

|<span data-ttu-id="59566-248">Значение</span><span class="sxs-lookup"><span data-stu-id="59566-248">Value</span></span>|<span data-ttu-id="59566-249">Описание</span><span class="sxs-lookup"><span data-stu-id="59566-249">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="59566-250">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="59566-250">E_FAIL</span></span>  <br/> |<span data-ttu-id="59566-251">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="59566-251">The call failed.</span></span>  <br/> |
|<span data-ttu-id="59566-252">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="59566-252">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="59566-253">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="59566-253">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="59566-254">Е_ЛСК_НОТИНИТИАЛИЗЕД</span><span class="sxs-lookup"><span data-stu-id="59566-254">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="59566-255">[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="59566-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="59566-256">S_OK</span><span class="sxs-lookup"><span data-stu-id="59566-256">S_OK</span></span>  <br/> |<span data-ttu-id="59566-257">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="59566-257">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a><span data-ttu-id="59566-258">Илсклокалсинкклиент:: Initialize</span><span class="sxs-lookup"><span data-stu-id="59566-258">ILSCLocalSyncClient::Initialize</span></span>
<span data-ttu-id="59566-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span><span class="sxs-lookup"><span data-stu-id="59566-259"></span></span>

<span data-ttu-id="59566-260">Инициализация должна быть первым вызываемым методом.</span><span class="sxs-lookup"><span data-stu-id="59566-260">Initialize must be the first method called.</span></span> <span data-ttu-id="59566-261">В противном случае все остальные API будут возвращать Е_ЛСК_НОТИНИТИАЛИЗЕД.</span><span class="sxs-lookup"><span data-stu-id="59566-261">Otherwise, all other APIs will return E_LSC_NOTINITIALIZED.</span></span> <span data-ttu-id="59566-262">При вызове метода Initialize для уже инициализированного объекта возвращается значение S_OK и ничего не происходит.</span><span class="sxs-lookup"><span data-stu-id="59566-262">Calling Initialize on an already initialized object returns S_OK and does nothing.</span></span> <span data-ttu-id="59566-263">Если возвращается Е_ЛСК_КАЧЕМИСМАТЧ, вызывающий может вызвать [илсклокалсинкклиент:: ресеткаче](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) , чтобы удалить кэш, связанный с заданным супплиедид.</span><span class="sxs-lookup"><span data-stu-id="59566-263">If E_LSC_CACHEMISMATCH is returned, the caller may call [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) to delete the cache associated with the given SuppliedID.</span></span> <span data-ttu-id="59566-264">Однако в этом случае другие API все равно будут возвращать Е_ЛСК_НОТИНИТИАЛИЗЕД.</span><span class="sxs-lookup"><span data-stu-id="59566-264">However, in this case other APIs will still return E_LSC_NOTINITIALIZED.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a><span data-ttu-id="59566-265">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-265">Parameters</span></span>

 <span data-ttu-id="59566-266">_Бстрсупплиедид_</span><span class="sxs-lookup"><span data-stu-id="59566-266">_bstrSuppliedID_</span></span>
  
<span data-ttu-id="59566-267">Идентифицирует объекта-получателя и используемого кэша.</span><span class="sxs-lookup"><span data-stu-id="59566-267">Identifies the consumer and which cache to use.</span></span> <span data-ttu-id="59566-268">Значение не должно быть пустым (не должно превышать 32 символов).</span><span class="sxs-lookup"><span data-stu-id="59566-268">Must be non-empty with a maximum of 32 characters.</span></span> 
  
 <span data-ttu-id="59566-269">_Бстрпрогид_</span><span class="sxs-lookup"><span data-stu-id="59566-269">_bstrProgID_</span></span>
  
<span data-ttu-id="59566-270">Определяет COM-объект потребителя для двусторонней связи.</span><span class="sxs-lookup"><span data-stu-id="59566-270">Identifies the consumer's COM object for two-way communication.</span></span> <span data-ttu-id="59566-271">Значение не должно быть пустым (не должно превышать 39 символов).</span><span class="sxs-lookup"><span data-stu-id="59566-271">Must be non-empty with a maximum of 39 characters.</span></span> <span data-ttu-id="59566-272">Для получения дополнительных сведений об идентификаторах ProgID см. [ \<\> ](https://docs.microsoft.com/windows/desktop/com/-progid--key)</span><span class="sxs-lookup"><span data-stu-id="59566-272">See [\<ProgID\> Key](https://docs.microsoft.com/windows/desktop/com/-progid--key) for more information about ProgIDs.</span></span> 
  
 <span data-ttu-id="59566-273">_Бстрфилесистемдиректорихинт_</span><span class="sxs-lookup"><span data-stu-id="59566-273">_bstrFileSystemDirectoryHint_</span></span>
  
<span data-ttu-id="59566-274">Определяет корневой каталог, в котором будут храниться локальные файлы.</span><span class="sxs-lookup"><span data-stu-id="59566-274">Identifies the directory root in which local files will be stored.</span></span> <span data-ttu-id="59566-275">Значение не должно быть пустым (не должно превышать 256 символов).</span><span class="sxs-lookup"><span data-stu-id="59566-275">Must be non-empty with a maximum of 256 characters.</span></span> <span data-ttu-id="59566-276">Каталог должен уже существовать.</span><span class="sxs-lookup"><span data-stu-id="59566-276">The directory must already exist.</span></span> 
  
 <span data-ttu-id="59566-277">_Певенткаллбакк_</span><span class="sxs-lookup"><span data-stu-id="59566-277">_pEventCallback_</span></span>
  
<span data-ttu-id="59566-278">Интерфейс обратного вызова, который Ксисинкклиент будет уведомлять об изменениях.</span><span class="sxs-lookup"><span data-stu-id="59566-278">The callback interface which CsiSyncClient will notify on changes.</span></span> <span data-ttu-id="59566-279">См. Ипартнерактивитикаллбакк:: Евентоккурред.</span><span class="sxs-lookup"><span data-stu-id="59566-279">See IPartnerActivityCallback::EventOccurred.</span></span> <span data-ttu-id="59566-280">Это значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="59566-280">This value must not be null.</span></span> 
  
 <span data-ttu-id="59566-281">_Пфкреатедневкаче_</span><span class="sxs-lookup"><span data-stu-id="59566-281">_pfCreatedNewCache_</span></span>
  
<span data-ttu-id="59566-282">Возвращает значение, указывающее, был ли создан новый кэш.</span><span class="sxs-lookup"><span data-stu-id="59566-282">Returns whether a new cache was created.</span></span> <span data-ttu-id="59566-283">Если с Супплиедид не связан ни один кэш, будет создан один из них.</span><span class="sxs-lookup"><span data-stu-id="59566-283">If no cache is associated with the SuppliedID, one will be created.</span></span> <span data-ttu-id="59566-284">Это значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="59566-284">This value must not be null.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="59566-285">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-285">Return values</span></span>

|<span data-ttu-id="59566-286">Значение</span><span class="sxs-lookup"><span data-stu-id="59566-286">Value</span></span>|<span data-ttu-id="59566-287">Описание</span><span class="sxs-lookup"><span data-stu-id="59566-287">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="59566-288">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="59566-288">E_FAIL</span></span>  <br/> |<span data-ttu-id="59566-289">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="59566-289">The call failed.</span></span>  <br/> |
|<span data-ttu-id="59566-290">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="59566-290">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="59566-291">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="59566-291">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="59566-292">Е_ЛСК_КАЧЕМИСМАТЧ</span><span class="sxs-lookup"><span data-stu-id="59566-292">E_LSC_CACHEMISMATCH</span></span>  <br/> |<span data-ttu-id="59566-293">Супплиедид уже имеет связанный с ним кэш, но имеет другой ProgId или Филесистемдиректорихинт, чем предоставленные.</span><span class="sxs-lookup"><span data-stu-id="59566-293">A SuppliedID already has a cache associated with it, but has a different ProgId or FileSystemDirectoryHint than the ones provided.</span></span>  <br/> |
|<span data-ttu-id="59566-294">Е_ЛСК_ДИРЕКТОРИХИНТКОНФЛИКТ</span><span class="sxs-lookup"><span data-stu-id="59566-294">E_LSC_DIRECTORYHINTCONFLICT</span></span>  <br/> |<span data-ttu-id="59566-295">Филесистемдиректорихинт (или вложенная папка) уже существует в другом кэше.</span><span class="sxs-lookup"><span data-stu-id="59566-295">The FileSystemDirectoryHint (or a subfolder) already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="59566-296">Е_ЛАК_ПРОГИДКОНФЛИКТ</span><span class="sxs-lookup"><span data-stu-id="59566-296">E_LAC_PROGIDCONFLICT</span></span>  <br/> |<span data-ttu-id="59566-297">ProgID уже существует в другом кэше.</span><span class="sxs-lookup"><span data-stu-id="59566-297">The ProgID already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="59566-298">S_OK</span><span class="sxs-lookup"><span data-stu-id="59566-298">S_OK</span></span>  <br/> |<span data-ttu-id="59566-299">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="59566-299">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a><span data-ttu-id="59566-300">Илсклокалсинкклиент:: Локалфилечанже</span><span class="sxs-lookup"><span data-stu-id="59566-300">ILSCLocalSyncClient::LocalFileChange</span></span>
<span data-ttu-id="59566-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="59566-301"></span></span>

<span data-ttu-id="59566-302">Локалфилечанже используется, чтобы сообщить COM-объекту Ксисинкклиент попытаться отправить указанный файл.</span><span class="sxs-lookup"><span data-stu-id="59566-302">LocalFileChange is used to tell the CsiSyncClient COM object to attempt to upload the specified file.</span></span> <span data-ttu-id="59566-303">Метод подготовит файл для отправки, включая чтение текущего содержимого файла.</span><span class="sxs-lookup"><span data-stu-id="59566-303">The method will prepare the file for upload, including reading the file's current contents.</span></span> <span data-ttu-id="59566-304">Если отправка уже ожидается, Предыдущая отправка будет отменена и новое содержимое подготовлено к отправке.</span><span class="sxs-lookup"><span data-stu-id="59566-304">If an upload is already pending, the previous upload will be discarded and the new contents prepared for upload.</span></span> <span data-ttu-id="59566-305">Если файл открыт для редактирования в приложении, этот метод возвратит значение S_OK, не подготавливая файл для отправки (при наличии изменений приложение должно выполнить это действие).</span><span class="sxs-lookup"><span data-stu-id="59566-305">If the file is open for editing in an application, this method will return S_OK without preparing the file for upload (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="59566-306">Этот метод позволяет отправлять отправку, если он был помечен как отправленные ранее (см. [илсклокалсинкклиент:: ренамефиле ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span><span class="sxs-lookup"><span data-stu-id="59566-306">This method will allow uploads if it was marked as uploads blocked previously (see [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span></span>
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="59566-307">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-307">Parameters</span></span>

 <span data-ttu-id="59566-308">_Бстрфилесистемпас_</span><span class="sxs-lookup"><span data-stu-id="59566-308">_bstrFileSystemPath_</span></span>
  
<span data-ttu-id="59566-309">Строка, которая определяет файл на клиенте.</span><span class="sxs-lookup"><span data-stu-id="59566-309">A string which identifies the file on the client.</span></span> <span data-ttu-id="59566-310">Это значение должно быть непустым локальным путем длиной не более 256 символов.</span><span class="sxs-lookup"><span data-stu-id="59566-310">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="59566-311">Этот путь должен находиться в дереве каталогов, указанном параметром Филесистемдиректорихинт при вызове [илсклокалсинкклиент:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) .</span><span class="sxs-lookup"><span data-stu-id="59566-311">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was made.</span></span> 
  
 <span data-ttu-id="59566-312">_Бстрресаурцеид_</span><span class="sxs-lookup"><span data-stu-id="59566-312">_bstrResourceID_</span></span>
  
<span data-ttu-id="59566-313">Строка, определяющая значение ResourceID файла.</span><span class="sxs-lookup"><span data-stu-id="59566-313">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="59566-314">Это значение не должно быть пустым (не должно превышать 128 символов).</span><span class="sxs-lookup"><span data-stu-id="59566-314">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="59566-315">_Бстрвебпас_</span><span class="sxs-lookup"><span data-stu-id="59566-315">_bstrWebPath_</span></span>
  
<span data-ttu-id="59566-316">Строка, которая определяет файл на сервере.</span><span class="sxs-lookup"><span data-stu-id="59566-316">A string which identifies the file on the server.</span></span> <span data-ttu-id="59566-317">Это значение должно быть непустым, допустимым URL-АДРЕСом, но не более чем ИНТЕРНЕТ_МАКС_УРЛ_ЛЕНГС, https://support.microsoft.com/kb/208427как определено.</span><span class="sxs-lookup"><span data-stu-id="59566-317">This value must be non-empty, valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="59566-318">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-318">Return values</span></span>

|<span data-ttu-id="59566-319">Значение</span><span class="sxs-lookup"><span data-stu-id="59566-319">Value</span></span>|<span data-ttu-id="59566-320">Описание</span><span class="sxs-lookup"><span data-stu-id="59566-320">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="59566-321">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="59566-321">E_FAIL</span></span>  <br/> |<span data-ttu-id="59566-322">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="59566-322">The call failed.</span></span>  <br/> |
|<span data-ttu-id="59566-323">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="59566-323">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="59566-324">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="59566-324">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="59566-325">Е_ЛСК_КОНФЛИКТИНГФИЛЕ</span><span class="sxs-lookup"><span data-stu-id="59566-325">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="59566-326">Значение ResourceID для файла, указанного в параметре _бстрфилесистемпас_ , отличается от указанного.</span><span class="sxs-lookup"><span data-stu-id="59566-326">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span> <span data-ttu-id="59566-327">При возвращении этой ошибки отправляется событие типа Лсцевенттипе_онфилепасконфликт.</span><span class="sxs-lookup"><span data-stu-id="59566-327">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="59566-328">См. [илсклокалсинкклиент:: Changes ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="59566-328">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="59566-329">Е_ЛСК_ФИЛЕНОТФАУНД</span><span class="sxs-lookup"><span data-stu-id="59566-329">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="59566-330">Файл был удален средней операцией.</span><span class="sxs-lookup"><span data-stu-id="59566-330">The file was deleted mid-operation.</span></span>  <br/> |
|<span data-ttu-id="59566-331">Е_ЛСК_ФИЛЕНОТСУППОРТЕД</span><span class="sxs-lookup"><span data-stu-id="59566-331">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="59566-332">Объект COM Ксисинкклиент не поддерживает заданное расширение файла.</span><span class="sxs-lookup"><span data-stu-id="59566-332">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="59566-333">См. [илсклокалсинкклиент:: жетсуппортедфиликстенсионс ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span><span class="sxs-lookup"><span data-stu-id="59566-333">See [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span></span>  <br/> |
|<span data-ttu-id="59566-334">Е_ЛСК_ФИЛЕУПТОДАТЕ</span><span class="sxs-lookup"><span data-stu-id="59566-334">E_LSC_FILEUPTODATE</span></span>  <br/> |<span data-ttu-id="59566-335">COM-объект не запланировать отправку, так как файл в кэше содержал последние изменения с диска.</span><span class="sxs-lookup"><span data-stu-id="59566-335">The COM object did not schedule an upload because the file in the cache had the most recent changes from the disk.</span></span>  <br/> |
|<span data-ttu-id="59566-336">Е_ЛСК_ЛОКАЛФИЛЕУНАВАИЛАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="59566-336">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="59566-337">Файл, указанный в параметре _бстрфилесистемпас_ , отсутствует или заблокирован.</span><span class="sxs-lookup"><span data-stu-id="59566-337">The file specified by  _bstrFileSystemPath_ is missing or locked.</span></span>  <br/> |
|<span data-ttu-id="59566-338">Е_ЛСК_ЛОКАЛПАСНОТМАППЕД</span><span class="sxs-lookup"><span data-stu-id="59566-338">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="59566-339">Данный Филесистемпас не находится в корневом каталоге, заданном параметром Филесистемдиректорихинт при вызове метода Initialize.</span><span class="sxs-lookup"><span data-stu-id="59566-339">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="59566-340">Е_ЛСК_НОТИНИТИАЛИЗЕД</span><span class="sxs-lookup"><span data-stu-id="59566-340">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="59566-341">[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="59566-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="59566-342">Е_ЛСК_ПАСМИСМАТЧ</span><span class="sxs-lookup"><span data-stu-id="59566-342">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="59566-343">Файл, указанный в параметре _бстрресаурцеид_ , отличается от указанного в параметре филесистемпас.</span><span class="sxs-lookup"><span data-stu-id="59566-343">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="59566-344">Е_ЛСК_ПЕНДИНГЧАНЖЕСИНКАЧЕ</span><span class="sxs-lookup"><span data-stu-id="59566-344">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="59566-345">Указанный файл уже содержит ожидающие изменения в другом кэше и еще не может быть связан с кэшем потребителя.</span><span class="sxs-lookup"><span data-stu-id="59566-345">The file specified already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="59566-346">Е_ЛСК_СЕРВЕРПАСИНДИФФЕРЕНТКАЧЕ</span><span class="sxs-lookup"><span data-stu-id="59566-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="59566-347">Указанный путь находится в другом кэше.</span><span class="sxs-lookup"><span data-stu-id="59566-347">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="59566-348">S_OK</span><span class="sxs-lookup"><span data-stu-id="59566-348">S_OK</span></span>  <br/> |<span data-ttu-id="59566-349">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="59566-349">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a><span data-ttu-id="59566-350">Илсклокалсинкклиент:: Ренамефиле</span><span class="sxs-lookup"><span data-stu-id="59566-350">ILSCLocalSyncClient::RenameFile</span></span>
<span data-ttu-id="59566-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span><span class="sxs-lookup"><span data-stu-id="59566-351"></span></span>

<span data-ttu-id="59566-352">Ренамефиле будет связывать новый URL-адрес и локальный путь для данного ResourceID.</span><span class="sxs-lookup"><span data-stu-id="59566-352">RenameFile will associate a new URL and local path for a given ResourceID.</span></span> <span data-ttu-id="59566-353">Если файл, указанный с помощью ResourceID, еще не существует в кэше, будет выполнена попытка создать его и пометить для скачивания.</span><span class="sxs-lookup"><span data-stu-id="59566-353">If the file specified by the ResourceID doesn't already exist in the cache, an attempt will be made to create it and mark it for download.</span></span>
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a><span data-ttu-id="59566-354">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-354">Parameters</span></span>

 <span data-ttu-id="59566-355">_Бстрресаурцеид_</span><span class="sxs-lookup"><span data-stu-id="59566-355">_bstrResourceID_</span></span>
  
<span data-ttu-id="59566-356">Строка, определяющая значение ResourceID файла.</span><span class="sxs-lookup"><span data-stu-id="59566-356">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="59566-357">Это значение не должно быть пустым (не должно превышать 128 символов).</span><span class="sxs-lookup"><span data-stu-id="59566-357">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="59566-358">_Бстрневфилесистемпас_</span><span class="sxs-lookup"><span data-stu-id="59566-358">_bstrNewFileSystemPath_</span></span>
  
<span data-ttu-id="59566-359">Строка, указывающая новый локальный путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="59566-359">A string which specifies the new local path for the file.</span></span> <span data-ttu-id="59566-360">Это значение должно быть непустым локальным путем длиной не более 256 символов.</span><span class="sxs-lookup"><span data-stu-id="59566-360">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="59566-361">Этот путь должен находиться в дереве каталогов, заданном параметром Филесистемдиректорихинт, при выполнении вызова метода Initialize.</span><span class="sxs-lookup"><span data-stu-id="59566-361">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span> 
  
 <span data-ttu-id="59566-362">_Бстрневвебпас_</span><span class="sxs-lookup"><span data-stu-id="59566-362">_bstrNewWebPath_</span></span>
  
<span data-ttu-id="59566-363">Строка, указывающая новый URL-адрес файла.</span><span class="sxs-lookup"><span data-stu-id="59566-363">A string which specifies the new URL for the file.</span></span> <span data-ttu-id="59566-364">Это значение должно быть непустым допустимым URL-АДРЕСом, но не превышать ИНТЕРНЕТ_МАКС_УРЛ_ЛЕНГС, как https://support.microsoft.com/kb/208427определено.</span><span class="sxs-lookup"><span data-stu-id="59566-364">This value must be non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
 <span data-ttu-id="59566-365">_Фблоккуплоадс_</span><span class="sxs-lookup"><span data-stu-id="59566-365">_fBlockUploads_</span></span>
  
<span data-ttu-id="59566-366">Указывает, разрешена ли в данный момент отправка в новое расположение.</span><span class="sxs-lookup"><span data-stu-id="59566-366">Specifies whether uploads to the new location are allowed currently.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="59566-367">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-367">Return values</span></span>

|<span data-ttu-id="59566-368">Значение</span><span class="sxs-lookup"><span data-stu-id="59566-368">Value</span></span>|<span data-ttu-id="59566-369">Описание</span><span class="sxs-lookup"><span data-stu-id="59566-369">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="59566-370">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="59566-370">E_FAIL</span></span>  <br/> |<span data-ttu-id="59566-371">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="59566-371">The call failed.</span></span>  <br/> |
|<span data-ttu-id="59566-372">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="59566-372">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="59566-373">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="59566-373">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="59566-374">Е_ЛСК_КОНФЛИКТИНГФИЛЕ</span><span class="sxs-lookup"><span data-stu-id="59566-374">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="59566-375">_Бстрневфилесистемпас_ или _бстрневвебпас_ уже существуют в другом файле в любом кэше.</span><span class="sxs-lookup"><span data-stu-id="59566-375">The  _bstrNewFileSystemPath_ or  _bstrNewWebPath_ already exist on another file in any cache.</span></span> <span data-ttu-id="59566-376">При возвращении этой ошибки отправляется событие типа Лсцевенттипе_онфилепасконфликт.</span><span class="sxs-lookup"><span data-stu-id="59566-376">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="59566-377">См. [илсклокалсинкклиент:: Changes ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="59566-377">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="59566-378">Е_ЛСК_ФИЛЕНОТФАУНД</span><span class="sxs-lookup"><span data-stu-id="59566-378">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="59566-379">При выполнении этого метода сведения о файле были удалены из кэша.</span><span class="sxs-lookup"><span data-stu-id="59566-379">The file information was deleted from the cache while this method was running.</span></span>  <br/> |
|<span data-ttu-id="59566-380">Е_ЛСК_ЛОКАЛПАСНОТМАППЕД</span><span class="sxs-lookup"><span data-stu-id="59566-380">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="59566-381">Данный Филесистемпас не находится в корневом каталоге, заданном параметром Филесистемдиректорихинт при вызове метода Initialize.</span><span class="sxs-lookup"><span data-stu-id="59566-381">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="59566-382">Е_ЛСК_НОТИНИТИАЛИЗЕД</span><span class="sxs-lookup"><span data-stu-id="59566-382">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="59566-383">[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="59566-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="59566-384">Е_ЛСК_ПЕНДИНГЧАНЖЕСИНКАЧЕ</span><span class="sxs-lookup"><span data-stu-id="59566-384">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="59566-385">В настоящий момент указанный файл синхронизируется в приложении Office.</span><span class="sxs-lookup"><span data-stu-id="59566-385">The file specified is currently synchronizing in an Office application.</span></span>  <br/> |
|<span data-ttu-id="59566-386">S_OK</span><span class="sxs-lookup"><span data-stu-id="59566-386">S_OK</span></span>  <br/> |<span data-ttu-id="59566-387">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="59566-387">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a><span data-ttu-id="59566-388">Илсклокалсинкклиент:: Ресеткаче</span><span class="sxs-lookup"><span data-stu-id="59566-388">ILSCLocalSyncClient::ResetCache</span></span>
<span data-ttu-id="59566-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span><span class="sxs-lookup"><span data-stu-id="59566-389"></span></span>

<span data-ttu-id="59566-390">Ресеткаче удалит кэш, связанный с Супплиедид, который был предоставлен при инициализации.</span><span class="sxs-lookup"><span data-stu-id="59566-390">ResetCache will delete the cache associated with the SuppliedID that was provided on Initialize.</span></span> <span data-ttu-id="59566-391">Сюда входят все сведения о файле, но файлы будут оставлены как на клиенте, так и на сервере.</span><span class="sxs-lookup"><span data-stu-id="59566-391">This includes all of the file information, but will leave the files on both the client and the server.</span></span> <span data-ttu-id="59566-392">Этот метод также оставляет объект в частично неинициализированном состоянии.</span><span class="sxs-lookup"><span data-stu-id="59566-392">This method also leaves the object in a partially uninitialized state.</span></span> <span data-ttu-id="59566-393">Единственные допустимые вызовы после этого [илсклокалсинкклиент:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) или [илсклокалсинкклиент:: Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="59566-393">The only valid calls after this are [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) or [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="59566-394">Этот метод можно вызвать при сбое инициализации и возврате Е_ЛСК_КАЧЕМИСМАТЧ, а также удалить кэш, связанный с Супплиедид, который был предоставлен при сбое вызова.</span><span class="sxs-lookup"><span data-stu-id="59566-394">This method MAY be called if Initialize fails and returns E_LSC_CACHEMISMATCH, and will delete the cache associated with the SuppliedID that was provided with the failing call.</span></span>
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a><span data-ttu-id="59566-395">Parameters</span><span class="sxs-lookup"><span data-stu-id="59566-395">Parameters</span></span>

<span data-ttu-id="59566-396">Нет</span><span class="sxs-lookup"><span data-stu-id="59566-396">None</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="59566-397">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-397">Return values</span></span>

|<span data-ttu-id="59566-398">Значение</span><span class="sxs-lookup"><span data-stu-id="59566-398">Value</span></span>|<span data-ttu-id="59566-399">Описание</span><span class="sxs-lookup"><span data-stu-id="59566-399">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="59566-400">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="59566-400">E_FAIL</span></span>  <br/> |<span data-ttu-id="59566-401">Вызов завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="59566-401">The call failed.</span></span>  <br/> |
|<span data-ttu-id="59566-402">Е_ЛСК_НОТИНИТИАЛИЗЕД</span><span class="sxs-lookup"><span data-stu-id="59566-402">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="59566-403">[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="59566-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was not successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="59566-404">S_OK</span><span class="sxs-lookup"><span data-stu-id="59566-404">S_OK</span></span>  <br/> |<span data-ttu-id="59566-405">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="59566-405">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a><span data-ttu-id="59566-406">Илсклокалсинкклиент:: Серверфилечанже</span><span class="sxs-lookup"><span data-stu-id="59566-406">ILSCLocalSyncClient::ServerFileChange</span></span>
<span data-ttu-id="59566-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="59566-407"></span></span>

<span data-ttu-id="59566-408">Серверфилечанже указывает COM-объекту Ксисинкклиент пометить указанный файл для загрузки.</span><span class="sxs-lookup"><span data-stu-id="59566-408">ServerFileChange tells the CsiSyncClient COM object to mark the specified file for download.</span></span> <span data-ttu-id="59566-409">Если файл открыт в приложении Office для редактирования, этот метод возвратит значение S_OK, не помечая файл для загрузки (при наличии изменений приложение должно выполнить это действие).</span><span class="sxs-lookup"><span data-stu-id="59566-409">If the file is open in an Office application for edit, this method will return S_OK without marking the file for download (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="59566-410">Этот метод позволит загружать загружаемые файлы, если он был помечен как загруженные ранее (см. Ренамефиле).</span><span class="sxs-lookup"><span data-stu-id="59566-410">This method will allow downloads if it was marked as downloads blocked previously (see RenameFile).</span></span>
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="59566-411">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-411">Parameters</span></span>

|<span data-ttu-id="59566-412">Параметр</span><span class="sxs-lookup"><span data-stu-id="59566-412">Parameter</span></span>|<span data-ttu-id="59566-413">Описание</span><span class="sxs-lookup"><span data-stu-id="59566-413">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="59566-414">Бстрфилесистемпас</span><span class="sxs-lookup"><span data-stu-id="59566-414">bstrFileSystemPath</span></span>  <br/> |<span data-ttu-id="59566-415">Строка, которая определяет файл на клиенте.</span><span class="sxs-lookup"><span data-stu-id="59566-415">A string which identifies the file on the client.</span></span> <span data-ttu-id="59566-416">Это значение должно быть непустым локальным путем длиной не более 256 символов.</span><span class="sxs-lookup"><span data-stu-id="59566-416">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="59566-417">Этот путь должен находиться в дереве каталогов, заданном параметром Филесистемдиректорихинт, при выполнении вызова метода Initialize.</span><span class="sxs-lookup"><span data-stu-id="59566-417">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="59566-418">Бстрресаурцеид</span><span class="sxs-lookup"><span data-stu-id="59566-418">bstrResourceID</span></span>  <br/> |<span data-ttu-id="59566-419">Строка, определяющая значение ResourceID файла.</span><span class="sxs-lookup"><span data-stu-id="59566-419">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="59566-420">Это значение не должно быть пустым (не должно превышать 128 символов).</span><span class="sxs-lookup"><span data-stu-id="59566-420">This value must be non-empty with a maximum of 128 characters.</span></span>  <br/> |
|<span data-ttu-id="59566-421">Бстрвебпас</span><span class="sxs-lookup"><span data-stu-id="59566-421">bstrWebPath</span></span>  <br/> |<span data-ttu-id="59566-422">Строка, которая определяет файл на сервере.</span><span class="sxs-lookup"><span data-stu-id="59566-422">A string which identifies the file on the server.</span></span> <span data-ttu-id="59566-423">Это значение должно быть непустым допустимым URL-АДРЕСом, но не превышать ИНТЕРНЕТ_МАКС_УРЛ_ЛЕНГС, как определено https://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="59566-423">This value must be a non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span>  <br/> |
   
##### <a name="return-values"></a><span data-ttu-id="59566-424">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-424">Return values</span></span>

|<span data-ttu-id="59566-425">Значение</span><span class="sxs-lookup"><span data-stu-id="59566-425">Value</span></span>|<span data-ttu-id="59566-426">Описание</span><span class="sxs-lookup"><span data-stu-id="59566-426">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="59566-427">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="59566-427">E_FAIL</span></span>  <br/> |<span data-ttu-id="59566-428">Не удалось задать состояние подключения кэша.</span><span class="sxs-lookup"><span data-stu-id="59566-428">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="59566-429">Е_ЛСК_КОНФЛИКТИНГФИЛЕ</span><span class="sxs-lookup"><span data-stu-id="59566-429">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="59566-430">Значение ResourceID для файла, указанного в параметре _бстрфилесистемпас_ , отличается от указанного.</span><span class="sxs-lookup"><span data-stu-id="59566-430">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span>  <br/> |
|<span data-ttu-id="59566-431">Е_ЛСК_ФИЛЕНОТСУППОРТЕД</span><span class="sxs-lookup"><span data-stu-id="59566-431">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="59566-432">Объект COM Ксисинкклиент не поддерживает заданное расширение файла.</span><span class="sxs-lookup"><span data-stu-id="59566-432">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="59566-433">Обратитесь к разделу Жетсуппортедфиликстенсионс.</span><span class="sxs-lookup"><span data-stu-id="59566-433">See GetSupportedFileExtensions.</span></span>  <br/> |
|<span data-ttu-id="59566-434">Е_ЛСК_ФИЛЕНОТФАУНД</span><span class="sxs-lookup"><span data-stu-id="59566-434">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="59566-435">Файл был удален в средней операции.</span><span class="sxs-lookup"><span data-stu-id="59566-435">The file was deleted in mid-operation.</span></span>  <br/> |
|<span data-ttu-id="59566-436">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="59566-436">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="59566-437">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="59566-437">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="59566-438">Е_ЛСК_ЛОКАЛПАСНОТМАППЕД</span><span class="sxs-lookup"><span data-stu-id="59566-438">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="59566-439">Данный Филесистемпас не находится в корневом каталоге, заданном параметром Филесистемдиректорихинт при вызове метода Initialize.</span><span class="sxs-lookup"><span data-stu-id="59566-439">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="59566-440">Е_ЛСК_НОИНИТИАЛИЗЕД</span><span class="sxs-lookup"><span data-stu-id="59566-440">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="59566-441">[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="59566-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="59566-442">Е_ЛСК_ПАСМИСМАТЧ</span><span class="sxs-lookup"><span data-stu-id="59566-442">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="59566-443">Файл, указанный в параметре _бстрресаурцеид_ , отличается от указанного в параметре филесистемпас.</span><span class="sxs-lookup"><span data-stu-id="59566-443">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="59566-444">Е_ЛСК_ПЕНДИНГЧАНЖЕСИНКАЧЕ</span><span class="sxs-lookup"><span data-stu-id="59566-444">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="59566-445">Указанный файл уже содержит ожидающие изменения в другом кэше и еще не может быть связан с кэшем потребителя.</span><span class="sxs-lookup"><span data-stu-id="59566-445">The specified file already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="59566-446">Е_ЛСК_СЕРВЕРПАСИНДИФФЕРЕНТКАЧЕ</span><span class="sxs-lookup"><span data-stu-id="59566-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="59566-447">Указанный путь находится в другом кэше.</span><span class="sxs-lookup"><span data-stu-id="59566-447">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="59566-448">S_OK</span><span class="sxs-lookup"><span data-stu-id="59566-448">S_OK</span></span>  <br/> |<span data-ttu-id="59566-449">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="59566-449">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a><span data-ttu-id="59566-450">Илсклокалсинкклиент:: Сетклиентконнективитистате</span><span class="sxs-lookup"><span data-stu-id="59566-450">ILSCLocalSyncClient::SetClientConnectivityState</span></span>
<span data-ttu-id="59566-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="59566-451"></span></span>

<span data-ttu-id="59566-452">ПереВодит кэш в оперативный или автономный режим.</span><span class="sxs-lookup"><span data-stu-id="59566-452">Sets the cache into an online or offline state.</span></span> <span data-ttu-id="59566-453">В автономном режиме Office не будет пытаться установить соединение с сервером для всех файлов в этом кэше, независимо от параметра _фблоккуплоадс_ каждого отдельного файла.</span><span class="sxs-lookup"><span data-stu-id="59566-453">If offline, Office will not attempt to communicate with the server for any files in that cache, regardless of each individual file's  _fBlockUploads_ setting.</span></span> 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a><span data-ttu-id="59566-454">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-454">Parameters</span></span>

 <span data-ttu-id="59566-455">_Фисонлине_</span><span class="sxs-lookup"><span data-stu-id="59566-455">_fIsOnline_</span></span>
  
<span data-ttu-id="59566-456">Логическое значение, определяющее состояние подключения кэша.</span><span class="sxs-lookup"><span data-stu-id="59566-456">A boolean determining the connectivity state of the cache.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="59566-457">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-457">Return values</span></span>

|<span data-ttu-id="59566-458">Значение</span><span class="sxs-lookup"><span data-stu-id="59566-458">Value</span></span>|<span data-ttu-id="59566-459">Описание</span><span class="sxs-lookup"><span data-stu-id="59566-459">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="59566-460">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="59566-460">E_FAIL</span></span>  <br/> |<span data-ttu-id="59566-461">Не удалось задать состояние подключения кэша.</span><span class="sxs-lookup"><span data-stu-id="59566-461">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="59566-462">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="59566-462">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="59566-463">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="59566-463">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="59566-464">Е_ЛСК_НОИНИТИАЛИЗЕД</span><span class="sxs-lookup"><span data-stu-id="59566-464">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="59566-465">[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="59566-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="59566-466">S_OK</span><span class="sxs-lookup"><span data-stu-id="59566-466">S_OK</span></span>  <br/> |<span data-ttu-id="59566-467">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="59566-467">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a><span data-ttu-id="59566-468">Илсклокалсинкклиент:: Сетклиентнетворксинкпермиссион</span><span class="sxs-lookup"><span data-stu-id="59566-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span></span>
<span data-ttu-id="59566-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="59566-469"></span></span>

<span data-ttu-id="59566-470">Сетклиентнетворксинкпермиссион используется для переопределения или Рестореоффице эвристических правил синхронизации для стоимости сети и потребления электроэнергии.</span><span class="sxs-lookup"><span data-stu-id="59566-470">SetClientNetworkSyncPermission is used to either override or restoreOffice's synchronizing heuristics for network cost and power usage.</span></span> <span data-ttu-id="59566-471">При использовании сети 3G или другой сети с высоким уровнем затрат или при работе от батарей и до подключения к сети, Office может блокировать сетевой трафик до тех пор, пока не будет оппортуне время.</span><span class="sxs-lookup"><span data-stu-id="59566-471">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span> <span data-ttu-id="59566-472">Потребитель этого API может использовать его для переопределения эвристики Office и принудительной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="59566-472">The consumer of this API can use it to override Office's heuristics and force synchronizing to occur.</span></span>
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a><span data-ttu-id="59566-473">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-473">Parameters</span></span>

 <span data-ttu-id="59566-474">_Нсптипе_</span><span class="sxs-lookup"><span data-stu-id="59566-474">_nspType_</span></span>
  
<span data-ttu-id="59566-475">Флаг, определяющий, какой эвристикой затрат следует переопределить.</span><span class="sxs-lookup"><span data-stu-id="59566-475">A flag which defines which cost heuristic to override.</span></span> <span data-ttu-id="59566-476">В разделе [enum лскнетворксинкпермиссионтипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="59566-476">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span>
  
 <span data-ttu-id="59566-477">_Фенаблесинк_</span><span class="sxs-lookup"><span data-stu-id="59566-477">_fEnableSync_</span></span>
  
<span data-ttu-id="59566-478">Указывает, следует ли принудительно выполнять синхронизацию, таким образом переопределяя более эвристику затрат или более не переопределять ее.</span><span class="sxs-lookup"><span data-stu-id="59566-478">Specifies whether to force synchronizing on, thus overriding that cost heuristic, or to no longer override it.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="59566-479">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-479">Return values</span></span>

|<span data-ttu-id="59566-480">Значение</span><span class="sxs-lookup"><span data-stu-id="59566-480">Value</span></span>|<span data-ttu-id="59566-481">Описание</span><span class="sxs-lookup"><span data-stu-id="59566-481">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="59566-482">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="59566-482">E_FAIL</span></span>  <br/> |<span data-ttu-id="59566-483">Не удалось переопределить эвристику синхронизации.</span><span class="sxs-lookup"><span data-stu-id="59566-483">Failure to override synchronizing heuristics.</span></span>  <br/> |
|<span data-ttu-id="59566-484">Е_ЛСК_НОИНИТИАЛИЗЕД</span><span class="sxs-lookup"><span data-stu-id="59566-484">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="59566-485">[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="59566-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="59566-486">S_OK</span><span class="sxs-lookup"><span data-stu-id="59566-486">S_OK</span></span>  <br/> |<span data-ttu-id="59566-487">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="59566-487">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a><span data-ttu-id="59566-488">Илсклокалсинкклиент:: Uninitialize</span><span class="sxs-lookup"><span data-stu-id="59566-488">ILSCLocalSyncClient::Uninitialize</span></span>
<span data-ttu-id="59566-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span><span class="sxs-lookup"><span data-stu-id="59566-489"></span></span>

<span data-ttu-id="59566-490">Выгрузка кэша из COM-объекта и выполнение операций закрытия.</span><span class="sxs-lookup"><span data-stu-id="59566-490">Unloads the cache from the COM object and perform closing operations.</span></span> <span data-ttu-id="59566-491">[Илсклокалсинкклиент:: Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) Перед удалением COM-объекта необходимо вызвать метод.</span><span class="sxs-lookup"><span data-stu-id="59566-491">[ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUST be called before destroying the COM object.</span></span> <span data-ttu-id="59566-492">После вызова другие API не могут вызываться, COM-объект должен быть удален, а новый — создан, если вы хотите продолжить операции.</span><span class="sxs-lookup"><span data-stu-id="59566-492">Once called, no other APIs can be called, the COM object MUST be destroyed and a new one created if you wish to continue operations.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a><span data-ttu-id="59566-493">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-493">Parameters</span></span>

<span data-ttu-id="59566-494">Нет.</span><span class="sxs-lookup"><span data-stu-id="59566-494">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="59566-495">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-495">Return values</span></span>

|<span data-ttu-id="59566-496">Значение</span><span class="sxs-lookup"><span data-stu-id="59566-496">Value</span></span>|<span data-ttu-id="59566-497">Описание</span><span class="sxs-lookup"><span data-stu-id="59566-497">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="59566-498">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="59566-498">E_FAIL</span></span>  <br/> |<span data-ttu-id="59566-499">Сбой при неВозможности инициализации.</span><span class="sxs-lookup"><span data-stu-id="59566-499">Failure to uninitialize.</span></span>  <br/> |
|<span data-ttu-id="59566-500">Е_ЛСК_НОИНИТИАЛИЗЕД</span><span class="sxs-lookup"><span data-stu-id="59566-500">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="59566-501">[Илсклокалсинкклиент:: инициализация](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) не была успешно вызвана в прошлое.</span><span class="sxs-lookup"><span data-stu-id="59566-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="59566-502">S_OK</span><span class="sxs-lookup"><span data-stu-id="59566-502">S_OK</span></span>  <br/> |<span data-ttu-id="59566-503">The call succeeded.</span><span class="sxs-lookup"><span data-stu-id="59566-503">The call succeeded.</span></span>  <br/> |
   
### <a name="interface-ienumlscevent"></a><span data-ttu-id="59566-504">Интерфейс Иенумлсцевент</span><span class="sxs-lookup"><span data-stu-id="59566-504">Interface IEnumLSCEvent</span></span>

<span data-ttu-id="59566-505">Этот интерфейс представляет список событий Илсцевент.</span><span class="sxs-lookup"><span data-stu-id="59566-505">This interface represents a list of ILSCEvent events.</span></span>
  
<span data-ttu-id="59566-506">**Открытые функции элементов**</span><span class="sxs-lookup"><span data-stu-id="59566-506">**Public member functions**</span></span>

#### <a name="ienumlsceventfnext"></a><span data-ttu-id="59566-507">Иенумлсцевент:: Фнекст</span><span class="sxs-lookup"><span data-stu-id="59566-507">IEnumLSCEvent::FNext</span></span>

<span data-ttu-id="59566-508">Извлекает следующее событие из списка событий.</span><span class="sxs-lookup"><span data-stu-id="59566-508">Retrieves the next event from the list of events.</span></span>
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a><span data-ttu-id="59566-509">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-509">Parameters</span></span>

 <span data-ttu-id="59566-510">_Ппилсцевент_</span><span class="sxs-lookup"><span data-stu-id="59566-510">_ppiLSCEvent_</span></span>
  
<span data-ttu-id="59566-511">Указатель на интерфейс Илсцевент.</span><span class="sxs-lookup"><span data-stu-id="59566-511">A pointer to an ILSCEvent interface.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="59566-512">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-512">Return values</span></span>

|<span data-ttu-id="59566-513">Значение</span><span class="sxs-lookup"><span data-stu-id="59566-513">Value</span></span>|<span data-ttu-id="59566-514">Описание</span><span class="sxs-lookup"><span data-stu-id="59566-514">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="59566-515">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="59566-515">E_FAIL</span></span>  <br/> |<span data-ttu-id="59566-516">Больше нет событий.</span><span class="sxs-lookup"><span data-stu-id="59566-516">There are no more events.</span></span>  <br/> |
|<span data-ttu-id="59566-517">S_OK</span><span class="sxs-lookup"><span data-stu-id="59566-517">S_OK</span></span>  <br/> |<span data-ttu-id="59566-518">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="59566-518">The call was successful.</span></span>  <br/> |
   
#### <a name="ienumlsceventreset"></a><span data-ttu-id="59566-519">Иенумлсцевент:: Reset</span><span class="sxs-lookup"><span data-stu-id="59566-519">IEnumLSCEvent::Reset</span></span>

<span data-ttu-id="59566-520">Сбрасывает перечислитель к первому событию.</span><span class="sxs-lookup"><span data-stu-id="59566-520">Resets the enumerator to the first event.</span></span>
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a><span data-ttu-id="59566-521">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-521">Parameters</span></span>

<span data-ttu-id="59566-522">Нет.</span><span class="sxs-lookup"><span data-stu-id="59566-522">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="59566-523">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-523">Return values</span></span>

<span data-ttu-id="59566-524">Всегда возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="59566-524">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent"></a><span data-ttu-id="59566-525">Интерфейс Илсцевент</span><span class="sxs-lookup"><span data-stu-id="59566-525">Interface ILSCEvent</span></span>

<span data-ttu-id="59566-526">Этот интерфейс представляет событие синхронизации.</span><span class="sxs-lookup"><span data-stu-id="59566-526">This interface represents a synchronizing event.</span></span> <span data-ttu-id="59566-527">Все сведения о событии можно получить из интерфейса.</span><span class="sxs-lookup"><span data-stu-id="59566-527">All information about the event can be retrieved from the interface.</span></span>
  
<span data-ttu-id="59566-528">**Открытые функции элементов**</span><span class="sxs-lookup"><span data-stu-id="59566-528">**Public member functions**</span></span>

#### <a name="ilsceventgetconflictstatus"></a><span data-ttu-id="59566-529">Илсцевент:: Жетконфликтстатус</span><span class="sxs-lookup"><span data-stu-id="59566-529">ILSCEvent::GetConflictStatus</span></span>

<span data-ttu-id="59566-530">Обратите внимание на то, что это значение заполняется при вызове метода [илсклокалсинкклиент::](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) -Changes, а не при создании события, поэтому отображается только текущее состояние файла, а не его состояние при изменении состояния конфликта.</span><span class="sxs-lookup"><span data-stu-id="59566-530">Note that this value is populated when [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) is called, not when the event was created, so you will only have the current status of the file, not the status of the file when the conflict status changed.</span></span> 
  
<span data-ttu-id="59566-531">Это значение заполняется только в том случае, если переЧисление [лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) для события равно лсцевенттипе_онлокалконфликтстатечанжед.</span><span class="sxs-lookup"><span data-stu-id="59566-531">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnLocalConflictStateChanged.</span></span> 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a><span data-ttu-id="59566-532">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-532">Parameters</span></span>

 <span data-ttu-id="59566-533">_Пфисинконфликт_</span><span class="sxs-lookup"><span data-stu-id="59566-533">_pfIsInConflict_</span></span>
  
<span data-ttu-id="59566-534">Текущее состояние конфликта файла, связанного с событием.</span><span class="sxs-lookup"><span data-stu-id="59566-534">The current conflict status of the file associated with the event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="59566-535">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-535">Return values</span></span>

<span data-ttu-id="59566-536">Всегда возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="59566-536">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeterror"></a><span data-ttu-id="59566-537">Илсцевент:: ошибка</span><span class="sxs-lookup"><span data-stu-id="59566-537">ILSCEvent::GetError</span></span>

<span data-ttu-id="59566-538">Это значение заполняется только в том случае, если переЧисление [лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) для события равно Лсцевенттипе_онсерверчанжесдовнлоадед или лсцевенттипе_онлокалчанжесуплоадед.</span><span class="sxs-lookup"><span data-stu-id="59566-538">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a><span data-ttu-id="59566-539">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-539">Parameters</span></span>

 <span data-ttu-id="59566-540">_Пнеррор_</span><span class="sxs-lookup"><span data-stu-id="59566-540">_pnError_</span></span>
  
<span data-ttu-id="59566-541">Ошибка, связанная с этим событием.</span><span class="sxs-lookup"><span data-stu-id="59566-541">The error associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="59566-542">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-542">Return values</span></span>

<span data-ttu-id="59566-543">Всегда возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="59566-543">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetetag"></a><span data-ttu-id="59566-544">Илсцевент::/ETag</span><span class="sxs-lookup"><span data-stu-id="59566-544">ILSCEvent::GetETag</span></span>

<span data-ttu-id="59566-545">Это значение заполняется только в том случае, если переЧисление [лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) для события равно Лсцевенттипе_онсерверчанжесдовнлоадед или лсцевенттипе_онлокалчанжесуплоадед.</span><span class="sxs-lookup"><span data-stu-id="59566-545">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a><span data-ttu-id="59566-546">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-546">Parameters</span></span>

 <span data-ttu-id="59566-547">_Пбстретаг_</span><span class="sxs-lookup"><span data-stu-id="59566-547">_pbstrETag_</span></span>
  
<span data-ttu-id="59566-548">ETag, связанный с этим событием</span><span class="sxs-lookup"><span data-stu-id="59566-548">The ETag associated with this event</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="59566-549">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-549">Return values</span></span>

<span data-ttu-id="59566-550">Всегда возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="59566-550">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeteventtype"></a><span data-ttu-id="59566-551">Илсцевент:: Жетевенттипе</span><span class="sxs-lookup"><span data-stu-id="59566-551">ILSCEvent::GetEventType</span></span>

<span data-ttu-id="59566-552">Получает тип данного события.</span><span class="sxs-lookup"><span data-stu-id="59566-552">Gets the type for this event.</span></span>
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a><span data-ttu-id="59566-553">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-553">Parameters</span></span>

 <span data-ttu-id="59566-554">_Пневенттипе_</span><span class="sxs-lookup"><span data-stu-id="59566-554">_pnEventType_</span></span>
  
<span data-ttu-id="59566-555">Тип события для этого события.</span><span class="sxs-lookup"><span data-stu-id="59566-555">The event type of this event.</span></span> <span data-ttu-id="59566-556">Допустимые значения приведены в разделе [enum лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) .</span><span class="sxs-lookup"><span data-stu-id="59566-556">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for valid values.</span></span> <span data-ttu-id="59566-557">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="59566-557">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="59566-558">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-558">Return values</span></span>

|<span data-ttu-id="59566-559">Значение</span><span class="sxs-lookup"><span data-stu-id="59566-559">Value</span></span>|<span data-ttu-id="59566-560">Описание</span><span class="sxs-lookup"><span data-stu-id="59566-560">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="59566-561">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="59566-561">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="59566-562">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="59566-562">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="59566-563">S_OK</span><span class="sxs-lookup"><span data-stu-id="59566-563">S_OK</span></span>  <br/> |<span data-ttu-id="59566-564">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="59566-564">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a><span data-ttu-id="59566-565">Илсцевент:: Жетлокалворкингпас</span><span class="sxs-lookup"><span data-stu-id="59566-565">ILSCEvent::GetLocalWorkingPath</span></span>

<span data-ttu-id="59566-566">Получает путь к локальному рабочему пути для этого события.</span><span class="sxs-lookup"><span data-stu-id="59566-566">Gets the local working path for this event.</span></span>
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a><span data-ttu-id="59566-567">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-567">Parameters</span></span>

 <span data-ttu-id="59566-568">_Пбстрлокалворкингпас_</span><span class="sxs-lookup"><span data-stu-id="59566-568">_pbstrLocalWorkingPath_</span></span>
  
<span data-ttu-id="59566-569">Локальный путь к файлу, к которому относится данное событие.</span><span class="sxs-lookup"><span data-stu-id="59566-569">The local path of the file to which this event pertains.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="59566-570">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-570">Return values</span></span>

<span data-ttu-id="59566-571">Всегда возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="59566-571">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceid"></a><span data-ttu-id="59566-572">Илсцевент:: Жетресаурцеид</span><span class="sxs-lookup"><span data-stu-id="59566-572">ILSCEvent::GetResourceID</span></span>

<span data-ttu-id="59566-573">Получает идентификатор ресурса для события.</span><span class="sxs-lookup"><span data-stu-id="59566-573">Gets the resource ID for the event.</span></span>
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="59566-574">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-574">Parameters</span></span>

 <span data-ttu-id="59566-575">_Пбстрресаурцеид_</span><span class="sxs-lookup"><span data-stu-id="59566-575">_pbstrResourceID_</span></span>
  
<span data-ttu-id="59566-576">ResourceID файла, связанного с этим событием.</span><span class="sxs-lookup"><span data-stu-id="59566-576">The ResourceID of the file associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="59566-577">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-577">Return values</span></span>

<span data-ttu-id="59566-578">Всегда возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="59566-578">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceidattempted"></a><span data-ttu-id="59566-579">Илсцевент:: Жетресаурцеидаттемптед</span><span class="sxs-lookup"><span data-stu-id="59566-579">ILSCEvent::GetResourceIDAttempted</span></span>

<span data-ttu-id="59566-580">Это значение заполняется только в том случае, если переЧисление [лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) для события равно лсцевенттипе_онфилепасконфликт.</span><span class="sxs-lookup"><span data-stu-id="59566-580">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> <span data-ttu-id="59566-581">При вызове [илсклокалсинкклиент:: локалфилечанже ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [Илсклокалсинкклиент:: серверфилечанже ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)или [илсклокалсинкклиент:: RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) это приведет к тому, что веб-путь или локальный путь будет конфликтовать с другим файлом в кэше файлов Office. создается событие.</span><span class="sxs-lookup"><span data-stu-id="59566-581">When a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) would cause a Web Path or Local Path collision with another file in the Office file cache, this event is generated.</span></span> 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a><span data-ttu-id="59566-582">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-582">Parameters</span></span>

 <span data-ttu-id="59566-583">_Пбстрресаурцеидаттемптед_</span><span class="sxs-lookup"><span data-stu-id="59566-583">_pbstrResourceIDAttempted_</span></span>
  
<span data-ttu-id="59566-584">Значение ResourceID, которое вызвало создание события.</span><span class="sxs-lookup"><span data-stu-id="59566-584">The ResourceID that caused this event to get generated.</span></span> <span data-ttu-id="59566-585">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="59566-585">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="59566-586">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-586">Return values</span></span>

<span data-ttu-id="59566-587">Всегда возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="59566-587">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetsyncerrortype"></a><span data-ttu-id="59566-588">Илсцевент:: Жетсинцеррортипе</span><span class="sxs-lookup"><span data-stu-id="59566-588">ILSCEvent::GetSyncErrorType</span></span>

<span data-ttu-id="59566-589">Это значение заполняется только в том случае, если переЧисление [лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) для события равно Лсцевенттипе_онсерверчанжесдовнлоадед или лсцевенттипе_онлокалчанжесуплоадед.</span><span class="sxs-lookup"><span data-stu-id="59566-589">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a><span data-ttu-id="59566-590">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-590">Parameters</span></span>

 <span data-ttu-id="59566-591">_Пнсинцеррортипе_</span><span class="sxs-lookup"><span data-stu-id="59566-591">_pnSyncErrorType_</span></span>
  
<span data-ttu-id="59566-592">Тип ошибки, связанный с этим событием.</span><span class="sxs-lookup"><span data-stu-id="59566-592">The error type associated with this event.</span></span> <span data-ttu-id="59566-593">Возможные значения приведены в разделе [enum лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) .</span><span class="sxs-lookup"><span data-stu-id="59566-593">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for potential values.</span></span> <span data-ttu-id="59566-594">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="59566-594">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="59566-595">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-595">Return values</span></span>

|<span data-ttu-id="59566-596">Значение</span><span class="sxs-lookup"><span data-stu-id="59566-596">Value</span></span>|<span data-ttu-id="59566-597">Описание</span><span class="sxs-lookup"><span data-stu-id="59566-597">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="59566-598">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="59566-598">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="59566-599">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="59566-599">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="59566-600">S_OK</span><span class="sxs-lookup"><span data-stu-id="59566-600">S_OK</span></span>  <br/> |<span data-ttu-id="59566-601">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="59566-601">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetwebpath"></a><span data-ttu-id="59566-602">Илсцевент:: Жетвебпас</span><span class="sxs-lookup"><span data-stu-id="59566-602">ILSCEvent::GetWebPath</span></span>

<span data-ttu-id="59566-603">Это значение заполняется только в том случае, если переЧисление [лсцевенттипе](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) для события равно лсцевенттипе_онфилепасконфликт.</span><span class="sxs-lookup"><span data-stu-id="59566-603">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a><span data-ttu-id="59566-604">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-604">Parameters</span></span>

 <span data-ttu-id="59566-605">_Пбстрвебпас_</span><span class="sxs-lookup"><span data-stu-id="59566-605">_pbstrWebPath_</span></span>
  
<span data-ttu-id="59566-606">Указывает веб-путь, связанный с этим событием.</span><span class="sxs-lookup"><span data-stu-id="59566-606">Specifies the Web Path associated with this event.</span></span> <span data-ttu-id="59566-607">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="59566-607">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="59566-608">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-608">Return values</span></span>

<span data-ttu-id="59566-609">Всегда возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="59566-609">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent2"></a><span data-ttu-id="59566-610">Интерфейс ILSCEvent2</span><span class="sxs-lookup"><span data-stu-id="59566-610">Interface ILSCEvent2</span></span>

<span data-ttu-id="59566-611">Этот интерфейс содержит дополнительные сведения о событии синхронизации.</span><span class="sxs-lookup"><span data-stu-id="59566-611">This interface holds additional information about a synchronizing event.</span></span>
  
<span data-ttu-id="59566-612">**Открытые функции элементов**</span><span class="sxs-lookup"><span data-stu-id="59566-612">**Public member functions**</span></span>

#### <a name="ilscevent2geterrorchain"></a><span data-ttu-id="59566-613">ILSCEvent2:: Жетеррорчаин</span><span class="sxs-lookup"><span data-stu-id="59566-613">ILSCEvent2::GetErrorChain</span></span>

<span data-ttu-id="59566-614">Получает сведения о цепочке ошибок для события синхронизации.</span><span class="sxs-lookup"><span data-stu-id="59566-614">Gets the error chain information about a synchronizing event.</span></span>
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a><span data-ttu-id="59566-615">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-615">Parameters</span></span>

 <span data-ttu-id="59566-616">_Пбстреррорчаин_</span><span class="sxs-lookup"><span data-stu-id="59566-616">_pbstrErrorChain_</span></span>
  
<span data-ttu-id="59566-617">Строка, в которой хранятся сведения о цепочке ошибок.</span><span class="sxs-lookup"><span data-stu-id="59566-617">A string to hold the error chain information.</span></span> <span data-ttu-id="59566-618">Значение не должно быть равно null.</span><span class="sxs-lookup"><span data-stu-id="59566-618">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="59566-619">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-619">Return values</span></span>

|<span data-ttu-id="59566-620">Значение</span><span class="sxs-lookup"><span data-stu-id="59566-620">Value</span></span>|<span data-ttu-id="59566-621">Описание</span><span class="sxs-lookup"><span data-stu-id="59566-621">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="59566-622">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="59566-622">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="59566-623">Установленная версия Office не поддерживает этот интерфейс</span><span class="sxs-lookup"><span data-stu-id="59566-623">The installed version of Office does not support this interface</span></span>  <br/> |
|<span data-ttu-id="59566-624">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="59566-624">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="59566-625">Одно или несколько значений параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="59566-625">One or more of the parameter values are invalid.</span></span>  <br/> |
|<span data-ttu-id="59566-626">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="59566-626">E_FAIL</span></span>  <br/> |<span data-ttu-id="59566-627">Информация о цепочке ошибок недоступна.</span><span class="sxs-lookup"><span data-stu-id="59566-627">The error chain information is not available.</span></span>  <br/> |
|<span data-ttu-id="59566-628">S_OK</span><span class="sxs-lookup"><span data-stu-id="59566-628">S_OK</span></span>  <br/> |<span data-ttu-id="59566-629">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="59566-629">The call was successful.</span></span>  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a><span data-ttu-id="59566-630">Интерфейс Ипартнерактивитикаллбакк</span><span class="sxs-lookup"><span data-stu-id="59566-630">Interface IPartnerActivityCallback</span></span>

<span data-ttu-id="59566-631">Этот интерфейс предоставляет функцию обратного вызова для COM-объекта Ксисинкклиент.</span><span class="sxs-lookup"><span data-stu-id="59566-631">This interface provides a callback function to the CSISyncClient COM object.</span></span>
  
<span data-ttu-id="59566-632">**Открытые функции элементов**</span><span class="sxs-lookup"><span data-stu-id="59566-632">**Public member functions**</span></span>

#### <a name="ipartneractivitycallbackeventoccurred"></a><span data-ttu-id="59566-633">Ипартнерактивитикаллбакк:: Евентоккурред</span><span class="sxs-lookup"><span data-stu-id="59566-633">IPartnerActivityCallback::EventOccurred</span></span>

<span data-ttu-id="59566-634">Это функция обратного вызова для объекта, данного COM-объекта Ксисинкклиент.</span><span class="sxs-lookup"><span data-stu-id="59566-634">This is a callback function on the object given to the CsiSyncClient COM object.</span></span> <span data-ttu-id="59566-635">Ожидается, что при возникновении события (см. [ПеречисленИе лсцевенттипеоккурред](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) для допустимых типов событий) COM-объект ксисинкклиент вызывает этот метод, засигнализациет получателя.</span><span class="sxs-lookup"><span data-stu-id="59566-635">It's expected that when an Event occurs (see [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid event types), the CsiSyncClient COM object will call this method, signalling the consumer.</span></span> 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a><span data-ttu-id="59566-636">Параметры</span><span class="sxs-lookup"><span data-stu-id="59566-636">Parameters</span></span>

 <span data-ttu-id="59566-637">_Ивенттипеоккурред_</span><span class="sxs-lookup"><span data-stu-id="59566-637">_eEventTypeOccurred_</span></span>
  
<span data-ttu-id="59566-638">Тип события для этого события.</span><span class="sxs-lookup"><span data-stu-id="59566-638">The event type of this event.</span></span> <span data-ttu-id="59566-639">Допустимые значения приведены в разделе [enum лсцевенттипеоккурред](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) .</span><span class="sxs-lookup"><span data-stu-id="59566-639">See [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid values.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="59566-640">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="59566-640">Return values</span></span>

<span data-ttu-id="59566-641">Всегда возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="59566-641">Always returns S_OK.</span></span>
  
## <a name="enumerations"></a><span data-ttu-id="59566-642">Перечисления</span><span class="sxs-lookup"><span data-stu-id="59566-642">Enumerations</span></span>

<span data-ttu-id="59566-643">В Ксисинкклиент используются следующие перечисления.</span><span class="sxs-lookup"><span data-stu-id="59566-643">CSISyncClient uses the following enumerations.</span></span>
  
### <a name="enum-lsceventsyncerrortype"></a><span data-ttu-id="59566-644">ПереЧисление Лсцевентсинцеррортипе</span><span class="sxs-lookup"><span data-stu-id="59566-644">Enum LSCEventSyncErrorType</span></span>
<span data-ttu-id="59566-645"><a name="Enum_LSCEventSyncErrorType"> </a></span><span class="sxs-lookup"><span data-stu-id="59566-645"></span></span>

<span data-ttu-id="59566-646">Это перечисление указывает категории ошибок, которые могут возникать при синхронизации файла.</span><span class="sxs-lookup"><span data-stu-id="59566-646">This enumeration specifies the categories of errors that can occur while synchronizing a file.</span></span>
  
|<span data-ttu-id="59566-647">Перечисляем</span><span class="sxs-lookup"><span data-stu-id="59566-647">Enumerator</span></span>|<span data-ttu-id="59566-648">Описание</span><span class="sxs-lookup"><span data-stu-id="59566-648">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="59566-649">Лсцевентсинцеррортипе_усеринтервентионрекуиредунекспектед</span><span class="sxs-lookup"><span data-stu-id="59566-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span></span>  <br/> |<span data-ttu-id="59566-650">Ошибка синхронизации этого события, которая может требовать особой важности.</span><span class="sxs-lookup"><span data-stu-id="59566-650">The synchronizing error of this event was unexpected, and may require special consideration.</span></span> <span data-ttu-id="59566-651">По умолчанию пользователю может потребоваться поСледовать.</span><span class="sxs-lookup"><span data-stu-id="59566-651">By default, the user may have to intervene.</span></span>  <br/> |
|<span data-ttu-id="59566-652">Лсцевентсинцеррортипе_ноинтервентионрекуиред</span><span class="sxs-lookup"><span data-stu-id="59566-652">LSCEventSyncErrorType_NoInterventionRequired</span></span>  <br/> |<span data-ttu-id="59566-653">Ошибка синхронизации этого события не требует особой важности.</span><span class="sxs-lookup"><span data-stu-id="59566-653">The synchronizing error of this event does not need special consideration.</span></span> <span data-ttu-id="59566-654">Office будет автоматически обрабатывать его.</span><span class="sxs-lookup"><span data-stu-id="59566-654">Office will handle it automatically.</span></span>  <br/> |
|<span data-ttu-id="59566-655">Лсцевентсинцеррортипе_усеринтервентионрекуиред</span><span class="sxs-lookup"><span data-stu-id="59566-655">LSCEventSyncErrorType_UserInterventionRequired</span></span>  <br/> |<span data-ttu-id="59566-656">Для ошибки синхронизации этого события необходимо, чтобы пользователь решил эту проблему.</span><span class="sxs-lookup"><span data-stu-id="59566-656">The synchronizing error of this event requires a user to resolve it.</span></span> <span data-ttu-id="59566-657">Например, для ошибки слияния необходимо, чтобы пользователь открыл документ, а затем слить его.</span><span class="sxs-lookup"><span data-stu-id="59566-657">For example, merge conflict error requires a user to open the document and merge it.</span></span>  <br/> |
|<span data-ttu-id="59566-658">Лсцевентсинцеррортипе_ваитингонклиент</span><span class="sxs-lookup"><span data-stu-id="59566-658">LSCEventSyncErrorType_WaitingOnClient</span></span>  <br/> |<span data-ttu-id="59566-659">Для ошибки синхронизации этого события необходимо, чтобы потребитель натребовался, но не обязательно должен быть особым вопросом.</span><span class="sxs-lookup"><span data-stu-id="59566-659">The synchronizing error of this event requires the consumer to intervene, but should not require special consideration by the user.</span></span>  <br/> |
|<span data-ttu-id="59566-660">Лсцевентсинцеррортипе_клиентинтервентионрекуиред</span><span class="sxs-lookup"><span data-stu-id="59566-660">LSCEventSyncErrorType_ClientInterventionRequired</span></span>  <br/> |<span data-ttu-id="59566-661">Для ошибки синхронизации этого события необходимо, чтобы потребитель был особым случаем.</span><span class="sxs-lookup"><span data-stu-id="59566-661">The synchronizing error of this event requires the consumer to intervene as a special case.</span></span>  <br/> |
|<span data-ttu-id="59566-662">Лсцевентсинцеррортипе_макс</span><span class="sxs-lookup"><span data-stu-id="59566-662">LSCEventSyncErrorType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtype"></a><span data-ttu-id="59566-663">ПереЧисление Лсцевенттипе</span><span class="sxs-lookup"><span data-stu-id="59566-663">Enum LSCEventType</span></span>
<span data-ttu-id="59566-664"><a name="Enum_LSCEventType"> </a></span><span class="sxs-lookup"><span data-stu-id="59566-664"></span></span>

<span data-ttu-id="59566-665">Это перечисление определяет тип событий, которые могут возникать в определенном файле.</span><span class="sxs-lookup"><span data-stu-id="59566-665">This enumeration specifies the type of events that can occur for a particular file.</span></span>
  
|<span data-ttu-id="59566-666">Перечисляем</span><span class="sxs-lookup"><span data-stu-id="59566-666">Enumerator</span></span>|<span data-ttu-id="59566-667">Описание</span><span class="sxs-lookup"><span data-stu-id="59566-667">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="59566-668">Лсцевенттипе_ноне</span><span class="sxs-lookup"><span data-stu-id="59566-668">LSCEventType_None</span></span>  <br/> ||
|<span data-ttu-id="59566-669">Лсцевенттипе_онлокалчанжес</span><span class="sxs-lookup"><span data-stu-id="59566-669">LSCEventType_OnLocalChanges</span></span>  <br/> |<span data-ttu-id="59566-670">Изменения, внесенные в локальный файл.</span><span class="sxs-lookup"><span data-stu-id="59566-670">Changes were made to a local file.</span></span>  <br/> |
|<span data-ttu-id="59566-671">Лсцевенттипе_онопенедбюсер</span><span class="sxs-lookup"><span data-stu-id="59566-671">LSCEventType_OnOpenedByUser</span></span>  <br/> |<span data-ttu-id="59566-672">Пользователь открыл файл.</span><span class="sxs-lookup"><span data-stu-id="59566-672">A user opened a file.</span></span>  <br/> |
|<span data-ttu-id="59566-673">Лсцевенттипе_онсерверчанжесдовнлоадед</span><span class="sxs-lookup"><span data-stu-id="59566-673">LSCEventType_OnServerChangesDownloaded</span></span>  <br/> |<span data-ttu-id="59566-674">Загрузка изменений файлов с сервера завершена.</span><span class="sxs-lookup"><span data-stu-id="59566-674">Finished downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="59566-675">Лсцевенттипе_онлокалчанжесуплоадед</span><span class="sxs-lookup"><span data-stu-id="59566-675">LSCEventType_OnLocalChangesUploaded</span></span>  <br/> |<span data-ttu-id="59566-676">Отгрузка изменений файлов на сервер завершена.</span><span class="sxs-lookup"><span data-stu-id="59566-676">Finished uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="59566-677">Лсцевенттипе_онлокалконфликтстатечанжед</span><span class="sxs-lookup"><span data-stu-id="59566-677">LSCEventType_OnLocalConflictStateChanged</span></span>  <br/> |<span data-ttu-id="59566-678">Изменено состояние конфликта слияния файла.</span><span class="sxs-lookup"><span data-stu-id="59566-678">The merge conflict state of a file has changed.</span></span>  <br/> |
|<span data-ttu-id="59566-679">Лсцевенттипе_онфилеаддед</span><span class="sxs-lookup"><span data-stu-id="59566-679">LSCEventType_OnFileAdded</span></span>  <br/> |<span data-ttu-id="59566-680">Добавлен файл.</span><span class="sxs-lookup"><span data-stu-id="59566-680">A file was added.</span></span>  <br/> |
|<span data-ttu-id="59566-681">Лсцевенттипе_онфиледелетед</span><span class="sxs-lookup"><span data-stu-id="59566-681">LSCEventType_OnFileDeleted</span></span>  <br/> |<span data-ttu-id="59566-682">Удален файл.</span><span class="sxs-lookup"><span data-stu-id="59566-682">A file was deleted.</span></span>  <br/> |
|<span data-ttu-id="59566-683">Лсцевенттипе_онсинценаблед</span><span class="sxs-lookup"><span data-stu-id="59566-683">LSCEventType_OnSyncEnabled</span></span>  <br/> |<span data-ttu-id="59566-684">Синхронизация для файлов пользователя включена.</span><span class="sxs-lookup"><span data-stu-id="59566-684">Synchronizing was enabled for a user's files.</span></span>  <br/> |
|<span data-ttu-id="59566-685">Лсцевенттипе_онсерверчанжесдовнлоадстартед</span><span class="sxs-lookup"><span data-stu-id="59566-685">LSCEventType_OnServerChangesDownloadStarted</span></span>  <br/> |<span data-ttu-id="59566-686">Началась загрузка изменений файлов с сервера.</span><span class="sxs-lookup"><span data-stu-id="59566-686">Started downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="59566-687">Лсцевенттипе_онлокалчанжесуплоадстартед</span><span class="sxs-lookup"><span data-stu-id="59566-687">LSCEventType_OnLocalChangesUploadStarted</span></span>  <br/> |<span data-ttu-id="59566-688">Начата отправка изменений файлов на сервер.</span><span class="sxs-lookup"><span data-stu-id="59566-688">Started uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="59566-689">Лсцевенттипе_онфилепасконфликт</span><span class="sxs-lookup"><span data-stu-id="59566-689">LSCEventType_OnFilePathConflict</span></span>  <br/> |<span data-ttu-id="59566-690">Это событие создается при вызове [илсклокалсинкклиент:: локалфилечанже ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [Илсклокалсинкклиент:: серверфилечанже ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)или [Илсклокалсинкклиент:: RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) вызывает веб-путь или конфликт локального пути с другим файлом в Кэш файлов Office.</span><span class="sxs-lookup"><span data-stu-id="59566-690">This event is generated when a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) causes a Web Path or Local Path collision with another file in the Office file cache.</span></span>  <br/> |
|<span data-ttu-id="59566-691">Лсцевенттипе_онфилефоркед</span><span class="sxs-lookup"><span data-stu-id="59566-691">LSCEventType_OnFileForked</span></span>  <br/> ||
|<span data-ttu-id="59566-692">Лсцевенттипе_макс</span><span class="sxs-lookup"><span data-stu-id="59566-692">LSCEventType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a><span data-ttu-id="59566-693">ПереЧисление Лсцевенттипеоккурред</span><span class="sxs-lookup"><span data-stu-id="59566-693">Enum LSCEventTypeOccurred</span></span>
<span data-ttu-id="59566-694"><a name="Enum_LSCEventTypeOccurred"> </a></span><span class="sxs-lookup"><span data-stu-id="59566-694"></span></span>

<span data-ttu-id="59566-695">Это перечисление определяет тип событий, которые могут возникнуть.</span><span class="sxs-lookup"><span data-stu-id="59566-695">This enumeration specifies the type of events that can occur.</span></span> <span data-ttu-id="59566-696">Потребитель должен вызывать определенные функции Илсклокалсинкклиент на основе типа события.</span><span class="sxs-lookup"><span data-stu-id="59566-696">The consumer needs to call specific ILSCLocalSyncClient functions based on the event type.</span></span>
  
|<span data-ttu-id="59566-697">Перечисляем</span><span class="sxs-lookup"><span data-stu-id="59566-697">Enumerator</span></span>|<span data-ttu-id="59566-698">Описание</span><span class="sxs-lookup"><span data-stu-id="59566-698">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="59566-699">Лсцевенттипеоккурред_жетчанжес</span><span class="sxs-lookup"><span data-stu-id="59566-699">LSCEventTypeOccurred_GetChanges</span></span>  <br/> |<span data-ttu-id="59566-700">Произошла Илсцевент.</span><span class="sxs-lookup"><span data-stu-id="59566-700">An ILSCEvent has occurred.</span></span> <span data-ttu-id="59566-701">Потребитель должен вызывать [илсклокалсинкклиент::](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) -Changes для получения данных.</span><span class="sxs-lookup"><span data-stu-id="59566-701">The consumer should call [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) to retrieve the data.</span></span>  <br/> |
|<span data-ttu-id="59566-702">Лсцевенттипеоккурред_жетсуппортедфиликстенсионс</span><span class="sxs-lookup"><span data-stu-id="59566-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span></span>  <br/> |<span data-ttu-id="59566-703">Изменены поддерживаемые расширения файлов.</span><span class="sxs-lookup"><span data-stu-id="59566-703">The supported file extensions have changed.</span></span> <span data-ttu-id="59566-704">Потребитель должен вызвать [илсклокалсинкклиент:: жетсуппортедфиликстенсионс](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) , чтобы получить новый список поддерживаемых расширений.</span><span class="sxs-lookup"><span data-stu-id="59566-704">The consumer should call [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) to retrieve the new list of supported extensions.</span></span>  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a><span data-ttu-id="59566-705">ПереЧисление Лскнетворксинкпермиссионтипе</span><span class="sxs-lookup"><span data-stu-id="59566-705">Enum LSCNetworkSyncPermissionType</span></span>
<span data-ttu-id="59566-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span><span class="sxs-lookup"><span data-stu-id="59566-706"></span></span>

<span data-ttu-id="59566-707">Это перечисление указывает флаги, используемые для эвристики стоимости сети.</span><span class="sxs-lookup"><span data-stu-id="59566-707">This enumeration specifies the flags used for a network cost heuristic.</span></span> 

|<span data-ttu-id="59566-708">Перечисляем</span><span class="sxs-lookup"><span data-stu-id="59566-708">Enumerator</span></span>|<span data-ttu-id="59566-709">Описание</span><span class="sxs-lookup"><span data-stu-id="59566-709">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="59566-710">Лскнетворксинкпермиссионтипе_хигхкост</span><span class="sxs-lookup"><span data-stu-id="59566-710">LSCNetworkSyncPermissionType_HighCost</span></span>  <br/> |<span data-ttu-id="59566-711">Значение true, если эвристика затрат для дорогостоящих сетей (например, 3G) переопределена.</span><span class="sxs-lookup"><span data-stu-id="59566-711">True if the cost heuristic for expensive networks (such as 3G) is overridden.</span></span>  <br/> |
|<span data-ttu-id="59566-712">Лскнетворксинкпермиссионтипе_хигхповерусаже</span><span class="sxs-lookup"><span data-stu-id="59566-712">LSCNetworkSyncPermissionType_HighPowerUsage</span></span>  <br/> |<span data-ttu-id="59566-713">Имеет значение true, если переопределяется эвристика затрат для использования питания (например, батарея).</span><span class="sxs-lookup"><span data-stu-id="59566-713">True if the cost heuristic for power usage (such as a battery) is overridden.</span></span>  <br/> |
   
### <a name="enum-lscstatusflag"></a><span data-ttu-id="59566-714">ПереЧисление Лскстатусфлаг</span><span class="sxs-lookup"><span data-stu-id="59566-714">Enum LSCStatusFlag</span></span>
<span data-ttu-id="59566-715"><a name="Enum_LSCStatusFlag"> </a></span><span class="sxs-lookup"><span data-stu-id="59566-715"></span></span>

<span data-ttu-id="59566-716">Это перечисление используется для представления состояния синхронизации файла.</span><span class="sxs-lookup"><span data-stu-id="59566-716">This enumeration is used to represent the synchronize status of a file.</span></span> 
  
|<span data-ttu-id="59566-717">Перечисляем</span><span class="sxs-lookup"><span data-stu-id="59566-717">Enumerator</span></span>|<span data-ttu-id="59566-718">Описание</span><span class="sxs-lookup"><span data-stu-id="59566-718">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="59566-719">Лксстатусфлаг_ноне</span><span class="sxs-lookup"><span data-stu-id="59566-719">LCSStatusFlag_None</span></span>  <br/> ||
|<span data-ttu-id="59566-720">Лскстатусфлаг_уплоадпендинг</span><span class="sxs-lookup"><span data-stu-id="59566-720">LSCStatusFlag_UploadPending</span></span>  <br/> |<span data-ttu-id="59566-721">Значение true, если имеются ожидающие данные для отправки в файл сервера.</span><span class="sxs-lookup"><span data-stu-id="59566-721">True if there is pending data to send to the server file.</span></span>  <br/> |
|<span data-ttu-id="59566-722">Лскстатусфлаг_довнлоадпендинг</span><span class="sxs-lookup"><span data-stu-id="59566-722">LSCStatusFlag_DownloadPending</span></span>  <br/> |<span data-ttu-id="59566-723">Значение true, если ожидаются данные, которые требуется скачать из файла сервера.</span><span class="sxs-lookup"><span data-stu-id="59566-723">True if there is pending data to download from the server file.</span></span>  <br/> |
|<span data-ttu-id="59566-724">Лскстатусфлаг_локалфилеунчанжед</span><span class="sxs-lookup"><span data-stu-id="59566-724">LSCStatusFlag_LocalFileUnchanged</span></span>  <br/> |<span data-ttu-id="59566-725">Значение true, если в кэше данных в файле есть последняя копия данных на диске.</span><span class="sxs-lookup"><span data-stu-id="59566-725">True if the data Office has on the file in its cache is the most recent copy of the data on disk.</span></span>  <br/> |
   

