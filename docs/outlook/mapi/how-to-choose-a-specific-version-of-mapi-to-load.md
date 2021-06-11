---
title: Выбор определенной версии MAPI для загрузки
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 85539a7f-74b6-4267-86ea-00da2c900c34
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d353eba55e33b8ab48b3c47d2f31f1b5e0973b58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344522"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a><span data-ttu-id="096e4-103">Выбор определенной версии MAPI для загрузки</span><span class="sxs-lookup"><span data-stu-id="096e4-103">Choose a specific version of MAPI to load</span></span>

<span data-ttu-id="096e4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="096e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="096e4-105">При прямой привязке к реализации MAPI необходимо тщательно выбрать, какую реализацию загрузить.</span><span class="sxs-lookup"><span data-stu-id="096e4-105">When linking explicitly to an implementation of MAPI, you must carefully select which implementation to load.</span></span> 
  
<span data-ttu-id="096e4-106">Существует два способа прямой привязки к реализации MAPI.</span><span class="sxs-lookup"><span data-stu-id="096e4-106">There are two methods to link explicitly to an implementation of MAPI.</span></span> 
  
1. <span data-ttu-id="096e4-107">Вы можете загрузить библиотеку загружки MAPI и указать в реестре настраиваемый DLL для загрузки и отправки звонков MAPI.</span><span class="sxs-lookup"><span data-stu-id="096e4-107">You can load the MAPI stub library, and specify in the registry a custom DLL to load and dispatch MAPI calls to.</span></span>
    
2. <span data-ttu-id="096e4-108">Вы можете реализовать алгоритм поиска клиента MAPI, чтобы найти версию MAPI, используемую клиентом почты по умолчанию, и загрузить его.</span><span class="sxs-lookup"><span data-stu-id="096e4-108">You can implement the MAPI client lookup algorithm to look up the version of MAPI used by the default mail client and load it.</span></span>
    
<span data-ttu-id="096e4-109">Поскольку вы можете изменитьMapi32.dll [реестра stub Параметры,](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) чтобы направить приложение на использование любой реализации MAPI, мы рекомендуем направить приложение на использование реализации MAPI, с помощью которую вы протестировали.</span><span class="sxs-lookup"><span data-stu-id="096e4-109">Because you can change the [Mapi32.dll Stub Registry Settings](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) to direct your application to use any implementation of MAPI, we recommend that you direct your application to use an implementation of MAPI that you have tested with.</span></span> <span data-ttu-id="096e4-110">Ниже описаны оба метода прямой привязки.</span><span class="sxs-lookup"><span data-stu-id="096e4-110">The following describes both methods of linking explicitly.</span></span> 
  
## <a name="reading-from-the-registry"></a><span data-ttu-id="096e4-111">Чтение из реестра</span><span class="sxs-lookup"><span data-stu-id="096e4-111">Reading from the registry</span></span>

### <a name="to-read-mapi-implementation-information-from-the-registry"></a><span data-ttu-id="096e4-112">Чтение сведений о реализации MAPI из реестра</span><span class="sxs-lookup"><span data-stu-id="096e4-112">To read MAPI implementation information from the registry</span></span>

1. <span data-ttu-id="096e4-113">Ключи реестра, которые указывают настраиваемый DLL для почтового клиента, находятся под  `HKLM\Software\Clients\Mail` ключом почтового клиента.</span><span class="sxs-lookup"><span data-stu-id="096e4-113">The registry keys that indicate a custom DLL for a mail client are located under the  `HKLM\Software\Clients\Mail` key of the mail client.</span></span> 
    
   <span data-ttu-id="096e4-114">В следующей таблице описаны следующие клавиши:</span><span class="sxs-lookup"><span data-stu-id="096e4-114">The following table describes these keys:</span></span>
    
   |<span data-ttu-id="096e4-115">**Клавиша**</span><span class="sxs-lookup"><span data-stu-id="096e4-115">**Key**</span></span>|<span data-ttu-id="096e4-116">**Описание**</span><span class="sxs-lookup"><span data-stu-id="096e4-116">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="096e4-117">MSIComponentID</span><span class="sxs-lookup"><span data-stu-id="096e4-117">MSIComponentID</span></span>  <br/> |<span data-ttu-id="096e4-118">Идентификатор категории Windows установки PublishComponent (GUID), который определяет DLL, экспортирует простые вызовы MAPI или MAPI.</span><span class="sxs-lookup"><span data-stu-id="096e4-118">A Windows Installer PublishComponent category ID (GUID) that identifies the DLL that exports simple MAPI or MAPI calls.</span></span> <span data-ttu-id="096e4-119">Если установлено, этот ключ имеет приоритет над **ключом DLLPath** или **DLLPathEx.**</span><span class="sxs-lookup"><span data-stu-id="096e4-119">If set, this key takes precedence over the **DLLPath** or **DLLPathEx** key.</span></span>  <br/> |
   |<span data-ttu-id="096e4-120">MSIApplicationLCID</span><span class="sxs-lookup"><span data-stu-id="096e4-120">MSIApplicationLCID</span></span>  <br/> |<span data-ttu-id="096e4-121">Идентификатор locale (LCID) для приложения.</span><span class="sxs-lookup"><span data-stu-id="096e4-121">Locale identifier (LCID) for your application.</span></span> <span data-ttu-id="096e4-122">Первое строковая величина определяет под ключ от и последующие значения строки определяют значения реестра под этим ключом, которые содержат  `HKLM\Software` сведения о локальном уровне.</span><span class="sxs-lookup"><span data-stu-id="096e4-122">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key that contain locale information.</span></span>  <br/> |
   |<span data-ttu-id="096e4-123">MSIOfficeLCID</span><span class="sxs-lookup"><span data-stu-id="096e4-123">MSIOfficeLCID</span></span>  <br/> |<span data-ttu-id="096e4-124">LCID для Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="096e4-124">LCIDs for Microsoft Office.</span></span> <span data-ttu-id="096e4-125">Первое строковая величина определяет под ключ от строки и последующие значения строки определяют значения реестра  `HKLM\Software` под этим ключом.</span><span class="sxs-lookup"><span data-stu-id="096e4-125">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key.</span></span>  <br/> |
   
   <span data-ttu-id="096e4-126">Получение сведений из этих ключей.</span><span class="sxs-lookup"><span data-stu-id="096e4-126">Obtain the information from these keys.</span></span>
    
2. <span data-ttu-id="096e4-127">Передай значения, полученные на предыдущем шаге, в функцию [FGetComponentPath.](fgetcomponentpath.md)</span><span class="sxs-lookup"><span data-stu-id="096e4-127">Pass the values that you obtained from the previous step to the [FGetComponentPath](fgetcomponentpath.md) function.</span></span> <span data-ttu-id="096e4-128">**FGetComponentPath** — это функция, экспортируемая библиотекой загвоздки MAPI Mapistub.dll.</span><span class="sxs-lookup"><span data-stu-id="096e4-128">**FGetComponentPath** is a function that is exported by the MAPI stub library Mapistub.dll.</span></span> <span data-ttu-id="096e4-129">Возвращает путь настраиваемой версии MAPI.</span><span class="sxs-lookup"><span data-stu-id="096e4-129">It returns the path of the custom version of MAPI.</span></span> 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a><span data-ttu-id="096e4-130">Загрузка реализации MAPI, помеченной как по умолчанию</span><span class="sxs-lookup"><span data-stu-id="096e4-130">To load the implementation of MAPI marked as default</span></span>

1. <span data-ttu-id="096e4-131">Прочитайте  `HKLM\Software\Clients\Mail::(default)` значение реестра.</span><span class="sxs-lookup"><span data-stu-id="096e4-131">Read the  `HKLM\Software\Clients\Mail::(default)` registry value.</span></span> 
    
2. <span data-ttu-id="096e4-132">Сведения о указанных клиентах, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="096e4-132">Look up the information for the indicated client as described earlier.</span></span>
    
> [!NOTE]
> <span data-ttu-id="096e4-133">Обратите внимание, что почтовый клиент по умолчанию может не реализовать расширенный MAPI.</span><span class="sxs-lookup"><span data-stu-id="096e4-133">Note that the default mail client might not implement Extended MAPI.</span></span> 
  
#### <a name="example"></a><span data-ttu-id="096e4-134">Пример</span><span class="sxs-lookup"><span data-stu-id="096e4-134">Example</span></span>

<span data-ttu-id="096e4-135">Чтобы загрузить MAPI в соответствии с Outlook, посмотрите на клавиши реестра и передайте их `HKLM\Software\Clients\Mail\Microsoft Outlook` **в FGetComponentPath.**</span><span class="sxs-lookup"><span data-stu-id="096e4-135">To load MAPI as implemented by Outlook, look up the registry keys under  `HKLM\Software\Clients\Mail\Microsoft Outlook` and pass them to **FGetComponentPath**.</span></span> <span data-ttu-id="096e4-136">**FGetComponentPath** возвращает путь для Outlook реализации MAPI.</span><span class="sxs-lookup"><span data-stu-id="096e4-136">**FGetComponentPath** will return the path for Outlook's implementation of MAPI.</span></span> 
  
<span data-ttu-id="096e4-137">Если ключи **MSIComponentID,** **MSIApplicationLCID** и **MSIOfficeLCID** не заданы, проверьте значение **реестра DLLPathEx.**</span><span class="sxs-lookup"><span data-stu-id="096e4-137">If the keys **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID** are not set, check the **DLLPathEx** registry value.</span></span> <span data-ttu-id="096e4-138">Если задатки, **FGetComponentPath** дает путь реализации MAPI клиентом.</span><span class="sxs-lookup"><span data-stu-id="096e4-138">If the keys are set, **FGetComponentPath** gives the path of the client's implementation of MAPI.</span></span> 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a><span data-ttu-id="096e4-139">Реализация алгоритма поиска клиентов MAPI</span><span class="sxs-lookup"><span data-stu-id="096e4-139">Implementing the MAPI Client Lookup algorithm</span></span>

<span data-ttu-id="096e4-140">В следующей таблице перечислены четыре функции MFCMAPI, которые используются для выполнения настраиваемой реализации MAPI:</span><span class="sxs-lookup"><span data-stu-id="096e4-140">The following table lists the four functions from MFCMAPI that are used to look up the path for a custom implementation of MAPI:</span></span>
  
|<span data-ttu-id="096e4-141">**Function**</span><span class="sxs-lookup"><span data-stu-id="096e4-141">**Function**</span></span>|<span data-ttu-id="096e4-142">**Описание**</span><span class="sxs-lookup"><span data-stu-id="096e4-142">**Description**</span></span>|
|:-----|:-----|
| `GetMAPIPath` <br/> |<span data-ttu-id="096e4-143">Получает путь библиотеки MAPI.</span><span class="sxs-lookup"><span data-stu-id="096e4-143">Gets the MAPI library path.</span></span>  <br/> |
| `GetMailKey` <br/> |<span data-ttu-id="096e4-144">Получает ключ реестра почты MAPI.</span><span class="sxs-lookup"><span data-stu-id="096e4-144">Gets the MAPI mail registry key.</span></span>  <br/> |
| `GetMapiMsiIds` <br/> |<span data-ttu-id="096e4-145">Получает идентификатор Windows установки.</span><span class="sxs-lookup"><span data-stu-id="096e4-145">Gets the Windows Installer identifier.</span></span>  <br/> |
| `GetComponentPath` <br/> |<span data-ttu-id="096e4-146">Получает путь компонента с [помощью FGetComponentPath.](fgetcomponentpath.md)</span><span class="sxs-lookup"><span data-stu-id="096e4-146">Gets the component path using [FGetComponentPath](fgetcomponentpath.md).</span></span>  <br/> |
   
<span data-ttu-id="096e4-147">Так как MFCMAPI загружает по умолчанию реализацию MAPI по умолчанию, если вы хотите использовать другую реализацию MAPI, для этого необходимо явно направить ее.</span><span class="sxs-lookup"><span data-stu-id="096e4-147">Because MFCMAPI loads the default implementation of MAPI by default, if you want to use a different implementation of MAPI, you must explicitly direct it to do so.</span></span> <span data-ttu-id="096e4-148">Это выполняется с помощью **процедуры Session\Load MAPI.**</span><span class="sxs-lookup"><span data-stu-id="096e4-148">This is performed by using the **Session\Load MAPI** routine.</span></span> 
  
### <a name="how-these-functions-work"></a><span data-ttu-id="096e4-149">Как работают эти функции</span><span class="sxs-lookup"><span data-stu-id="096e4-149">How these functions work</span></span>

1. <span data-ttu-id="096e4-150">MFCMAPI  `GetMAPIPath` вызывает, передавая NULL для параметра клиента, для загрузки реализации MAPI по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="096e4-150">MFCMAPI calls  `GetMAPIPath`, passing NULL for the client parameter, to load the default MAPI implementation.</span></span>
    
2.  <span data-ttu-id="096e4-151">`GetMAPIPath` вызовы для чтения  `GetMapiMsiIds` значений **MSIComponentID,** **MSIApplicationLCID** и **MSIOfficeLCID**.</span><span class="sxs-lookup"><span data-stu-id="096e4-151">`GetMAPIPath` calls  `GetMapiMsiIds` to read the values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
3.  <span data-ttu-id="096e4-152">`GetMapiMsiIds` вызовы  `GetMailKey` для открытия ключа реестра для почтового клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="096e4-152">`GetMapiMsiIds` calls  `GetMailKey` to open the registry key for the default mail client.</span></span> 
    
4.  <span data-ttu-id="096e4-153">`GetMapiMsiIds`использует возвращаемую обработку реестра, чтобы найти значения `GetMailKey` **для MSIComponentID,** **MSIApplicationLCID** и **MSIOfficeLCID.**</span><span class="sxs-lookup"><span data-stu-id="096e4-153">`GetMapiMsiIds` uses the registry handle returned by  `GetMailKey` to look up values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
5. <span data-ttu-id="096e4-154">Значения для **MSIComponentID,** **MSIApplicationLCID** и **MSIOfficeLCID** возвращаются в  `GetMAPIPath` .</span><span class="sxs-lookup"><span data-stu-id="096e4-154">The values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**, are returned to  `GetMAPIPath`.</span></span>  <span data-ttu-id="096e4-155">`GetMAPIPath` затем передает их  `GetComponentPath` в .</span><span class="sxs-lookup"><span data-stu-id="096e4-155">`GetMAPIPath` then passes them to  `GetComponentPath`.</span></span>
    
6.  <span data-ttu-id="096e4-156">`GetComponentPath` загружает библиотеку замеси MAPI, Mapi32.dll, из каталога системы.</span><span class="sxs-lookup"><span data-stu-id="096e4-156">`GetComponentPath` loads the MAPI stub library, Mapi32.dll, from the system directory.</span></span> 
    
7.  <span data-ttu-id="096e4-157">`GetComponentPath` затем извлекает адрес функции **FGetComponentPath** из Mapi32.dll, предполагая, что Mapi32.dll **экспортирует FGetComponentPath**.</span><span class="sxs-lookup"><span data-stu-id="096e4-157">`GetComponentPath` then retrieves the address of the **FGetComponentPath** function from Mapi32.dll, assuming that Mapi32.dll exports **FGetComponentPath**.</span></span>
    
8. <span data-ttu-id="096e4-158">Если получение адреса **FGetComponentPath** из Mapi32.dll не удается, извлекает адрес из  `GetComponentPath` Mapistub.dll.</span><span class="sxs-lookup"><span data-stu-id="096e4-158">If getting the address of **FGetComponentPath** from Mapi32.dll fails,  `GetComponentPath` retrieves the address from Mapistub.dll.</span></span> 
    
9.  <span data-ttu-id="096e4-159">`GetComponentPath` затем вызывает **FGetComponentPath,** чтобы получить путь по умолчанию версии MAPI.</span><span class="sxs-lookup"><span data-stu-id="096e4-159">`GetComponentPath` then calls **FGetComponentPath**, obtaining the path of the default version of MAPI.</span></span>
    
10.  <span data-ttu-id="096e4-160">`GetMAPIPath`затем возвращает этот путь вызываемму, который загружает MAPI и явно ссылается на него, как описано в [Link to MAPI Functions.](how-to-link-to-mapi-functions.md)</span><span class="sxs-lookup"><span data-stu-id="096e4-160">`GetMAPIPath` then returns this path to the caller, which then loads MAPI and explicitly links to it as described in [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="096e4-161">Для поддержки локализованных копий MAPI для английских и не-английских локалов считываю значения для `GetMAPIPath` **подкоев MSIApplicationLCID** и **MSIOfficeLCID.**</span><span class="sxs-lookup"><span data-stu-id="096e4-161">To support localized copies of MAPI for English and non-English locales,  `GetMAPIPath` reads the values for the **MSIApplicationLCID** and **MSIOfficeLCID** subkeys.</span></span>  <span data-ttu-id="096e4-162">`GetMAPIPath` затем вызывает **FGetComponentPath,** сначала указывает **MSIApplicationLCID** как **szQualifier,** и снова указывает **MSIOfficeLCID** как **szQualifier**.</span><span class="sxs-lookup"><span data-stu-id="096e4-162">`GetMAPIPath` then calls **FGetComponentPath**, first specifying **MSIApplicationLCID** as **szQualifier**, and again specifying **MSIOfficeLCID** as **szQualifier**.</span></span> <span data-ttu-id="096e4-163">Дополнительные сведения о ключах реестра для почтовых клиентов, которые поддерживают не-английские языки, см. в сообщении [Setting Up the MSI Keys for Your MAPI DLL.](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="096e4-163">For more information about registry keys for mail clients that support non-English languages, see [Setting Up the MSI Keys for Your MAPI DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).</span></span>   
> - <span data-ttu-id="096e4-164">Если MFCMAPI не получает путь для использования MAPI, он загружает библиотеку заглов MAPI из  `GetMAPIPath` каталога системы.</span><span class="sxs-lookup"><span data-stu-id="096e4-164">If MFCMAPI does not receive a path for MAPI using  `GetMAPIPath`, it loads the MAPI stub library from the system directory.</span></span>
> - <span data-ttu-id="096e4-165">Значение **реестра MSMapiApps,** о чем говорится в явном сопоставлении звонков MAPI к [DLLs MAPI,](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) применяется только при том, что используется библиотека STUB MAPI.</span><span class="sxs-lookup"><span data-stu-id="096e4-165">The **MSMapiApps** registry value discussed in [Explicitly Mapping MAPI Calls to MAPI DLLs](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) only applies when the MAPI Stub library is used.</span></span> <span data-ttu-id="096e4-166">Приложения, загружая определенную реализацию MAPI или загружая реализацию по умолчанию, не должны устанавливать ключ **реестра MSMapiApps.**</span><span class="sxs-lookup"><span data-stu-id="096e4-166">Applications that load a specific implementation of MAPI or load the default implementation do not have to set the **MSMapiApps** registry key.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="096e4-167">См. также</span><span class="sxs-lookup"><span data-stu-id="096e4-167">See also</span></span>

- [<span data-ttu-id="096e4-168">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="096e4-168">FGetComponentPath</span></span>](fgetcomponentpath.md)
- [<span data-ttu-id="096e4-169">Общие сведения о программировании MAPI</span><span class="sxs-lookup"><span data-stu-id="096e4-169">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="096e4-170">Ссылки на функции MAPI</span><span class="sxs-lookup"><span data-stu-id="096e4-170">Link to MAPI Functions</span></span>](how-to-link-to-mapi-functions.md)
- [<span data-ttu-id="096e4-171">Mapi32.dll реестра Stub Параметры</span><span class="sxs-lookup"><span data-stu-id="096e4-171">Mapi32.dll Stub Registry Settings</span></span>](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [<span data-ttu-id="096e4-172">Настройка клавиш MSI для DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="096e4-172">Setting Up the MSI Keys for Your MAPI DLL</span></span>](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [<span data-ttu-id="096e4-173">Явное сопоставление вызовов MAPI на DLLs MAPI</span><span class="sxs-lookup"><span data-stu-id="096e4-173">Explicitly Mapping MAPI Calls to MAPI DLLs</span></span>](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

