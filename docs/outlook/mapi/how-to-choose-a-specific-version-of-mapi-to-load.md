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
# <a name="choose-a-specific-version-of-mapi-to-load"></a><span data-ttu-id="defa2-103">Выбор определенной версии MAPI для загрузки</span><span class="sxs-lookup"><span data-stu-id="defa2-103">Choose a specific version of MAPI to load</span></span>

<span data-ttu-id="defa2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="defa2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="defa2-105">При явной привязке к реализации MAPI необходимо тщательно выбирать загружаемую реализацию.</span><span class="sxs-lookup"><span data-stu-id="defa2-105">When linking explicitly to an implementation of MAPI, you must carefully select which implementation to load.</span></span> 
  
<span data-ttu-id="defa2-106">Существует два способа явной привязки к реализации MAPI.</span><span class="sxs-lookup"><span data-stu-id="defa2-106">There are two methods to link explicitly to an implementation of MAPI.</span></span> 
  
1. <span data-ttu-id="defa2-107">Вы можете загрузить библиотеку загружок MAPI и указать в реестре настраиваемую библиотеку DLL для загрузки и отправки вызовов MAPI.</span><span class="sxs-lookup"><span data-stu-id="defa2-107">You can load the MAPI stub library, and specify in the registry a custom DLL to load and dispatch MAPI calls to.</span></span>
    
2. <span data-ttu-id="defa2-108">Вы можете реализовать алгоритм поиска клиента MAPI, чтобы найти версию MAPI, используемую почтовым клиентом по умолчанию, и загрузить его.</span><span class="sxs-lookup"><span data-stu-id="defa2-108">You can implement the MAPI client lookup algorithm to look up the version of MAPI used by the default mail client and load it.</span></span>
    
<span data-ttu-id="defa2-109">Так как вы можете [ изменить](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)Mapi32.dll реестра, чтобы приложение было использовать любую реализацию MAPI, рекомендуется направлять приложение на использование проверенной вами реализации MAPI.</span><span class="sxs-lookup"><span data-stu-id="defa2-109">Because you can change the [Mapi32.dll Stub Registry Settings](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) to direct your application to use any implementation of MAPI, we recommend that you direct your application to use an implementation of MAPI that you have tested with.</span></span> <span data-ttu-id="defa2-110">Ниже описаны оба способа явного связывания.</span><span class="sxs-lookup"><span data-stu-id="defa2-110">The following describes both methods of linking explicitly.</span></span> 
  
## <a name="reading-from-the-registry"></a><span data-ttu-id="defa2-111">Чтение из реестра</span><span class="sxs-lookup"><span data-stu-id="defa2-111">Reading from the registry</span></span>

### <a name="to-read-mapi-implementation-information-from-the-registry"></a><span data-ttu-id="defa2-112">Чтение сведений о реализации MAPI из реестра</span><span class="sxs-lookup"><span data-stu-id="defa2-112">To read MAPI implementation information from the registry</span></span>

1. <span data-ttu-id="defa2-113">Ключи реестра, которые указывают настраиваемую DLL для почтового клиента, расположены под  `HKLM\Software\Clients\Mail` ключом почтового клиента.</span><span class="sxs-lookup"><span data-stu-id="defa2-113">The registry keys that indicate a custom DLL for a mail client are located under the  `HKLM\Software\Clients\Mail` key of the mail client.</span></span> 
    
   <span data-ttu-id="defa2-114">В следующей таблице описаны следующие ключи:</span><span class="sxs-lookup"><span data-stu-id="defa2-114">The following table describes these keys:</span></span>
    
   |<span data-ttu-id="defa2-115">**Клавиша**</span><span class="sxs-lookup"><span data-stu-id="defa2-115">**Key**</span></span>|<span data-ttu-id="defa2-116">**Описание**</span><span class="sxs-lookup"><span data-stu-id="defa2-116">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="defa2-117">MSIComponentID</span><span class="sxs-lookup"><span data-stu-id="defa2-117">MSIComponentID</span></span>  <br/> |<span data-ttu-id="defa2-118">Идентификатор категории (GUID) установщика Windows, который определяет DLL,который экспортирует простые вызовы MAPI или MAPI.</span><span class="sxs-lookup"><span data-stu-id="defa2-118">A Windows Installer PublishComponent category ID (GUID) that identifies the DLL that exports simple MAPI or MAPI calls.</span></span> <span data-ttu-id="defa2-119">Если этот ключ задается, он имеет приоритет над **ключом DLLPath** или **DLLPathEx.**</span><span class="sxs-lookup"><span data-stu-id="defa2-119">If set, this key takes precedence over the **DLLPath** or **DLLPathEx** key.</span></span>  <br/> |
   |<span data-ttu-id="defa2-120">MSIApplicationLCID</span><span class="sxs-lookup"><span data-stu-id="defa2-120">MSIApplicationLCID</span></span>  <br/> |<span data-ttu-id="defa2-121">Код локального идентификатора (LCID) для приложения.</span><span class="sxs-lookup"><span data-stu-id="defa2-121">Locale identifier (LCID) for your application.</span></span> <span data-ttu-id="defa2-122">Первое строковая строка определяет под ключ из, а последующие строки определяют значения реестра под этим ключом, содержащие сведения  `HKLM\Software` о региональных значениях.</span><span class="sxs-lookup"><span data-stu-id="defa2-122">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key that contain locale information.</span></span>  <br/> |
   |<span data-ttu-id="defa2-123">MSIOfficeLCID</span><span class="sxs-lookup"><span data-stu-id="defa2-123">MSIOfficeLCID</span></span>  <br/> |<span data-ttu-id="defa2-124">LCID для Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="defa2-124">LCIDs for Microsoft Office.</span></span> <span data-ttu-id="defa2-125">Первое строка определяет под ключ, а последующие строки определяют значения реестра  `HKLM\Software` под этим ключом.</span><span class="sxs-lookup"><span data-stu-id="defa2-125">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key.</span></span>  <br/> |
   
   <span data-ttu-id="defa2-126">Получите информацию из этих ключей.</span><span class="sxs-lookup"><span data-stu-id="defa2-126">Obtain the information from these keys.</span></span>
    
2. <span data-ttu-id="defa2-127">Передав значения, полученные на предыдущем шаге, в функцию [FGetComponentPath.](fgetcomponentpath.md)</span><span class="sxs-lookup"><span data-stu-id="defa2-127">Pass the values that you obtained from the previous step to the [FGetComponentPath](fgetcomponentpath.md) function.</span></span> <span data-ttu-id="defa2-128">**FGetComponentPath** — это функция, экспортируемая библиотекой заг Mapistub.dll.</span><span class="sxs-lookup"><span data-stu-id="defa2-128">**FGetComponentPath** is a function that is exported by the MAPI stub library Mapistub.dll.</span></span> <span data-ttu-id="defa2-129">Он возвращает путь к пользовательской версии MAPI.</span><span class="sxs-lookup"><span data-stu-id="defa2-129">It returns the path of the custom version of MAPI.</span></span> 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a><span data-ttu-id="defa2-130">Загрузка реализации MAPI, отмеченной как стандартная</span><span class="sxs-lookup"><span data-stu-id="defa2-130">To load the implementation of MAPI marked as default</span></span>

1. <span data-ttu-id="defa2-131">Прочитайте  `HKLM\Software\Clients\Mail::(default)` значение реестра.</span><span class="sxs-lookup"><span data-stu-id="defa2-131">Read the  `HKLM\Software\Clients\Mail::(default)` registry value.</span></span> 
    
2. <span data-ttu-id="defa2-132">Найди сведения для указанных клиентов, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="defa2-132">Look up the information for the indicated client as described earlier.</span></span>
    
> [!NOTE]
> <span data-ttu-id="defa2-133">Обратите внимание, что почтовый клиент по умолчанию может не реализовать расширенный MAPI.</span><span class="sxs-lookup"><span data-stu-id="defa2-133">Note that the default mail client might not implement Extended MAPI.</span></span> 
  
#### <a name="example"></a><span data-ttu-id="defa2-134">Пример</span><span class="sxs-lookup"><span data-stu-id="defa2-134">Example</span></span>

<span data-ttu-id="defa2-135">Чтобы загрузить MAPI, реализованные в Outlook, найди под ними ключи реестра и передайте их `HKLM\Software\Clients\Mail\Microsoft Outlook` **в FGetComponentPath.**</span><span class="sxs-lookup"><span data-stu-id="defa2-135">To load MAPI as implemented by Outlook, look up the registry keys under  `HKLM\Software\Clients\Mail\Microsoft Outlook` and pass them to **FGetComponentPath**.</span></span> <span data-ttu-id="defa2-136">**FGetComponentPath** вернет путь для реализации MAPI в Outlook.</span><span class="sxs-lookup"><span data-stu-id="defa2-136">**FGetComponentPath** will return the path for Outlook's implementation of MAPI.</span></span> 
  
<span data-ttu-id="defa2-137">Если ключи **MSIComponentID,** **MSIApplicationLCID** и **MSIOfficeLCID** не заданы, проверьте значение **реестра DLLPathEx.**</span><span class="sxs-lookup"><span data-stu-id="defa2-137">If the keys **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID** are not set, check the **DLLPathEx** registry value.</span></span> <span data-ttu-id="defa2-138">Если ключи за установлены, **FGetComponentPath** предоставляет путь реализации MAPI клиента.</span><span class="sxs-lookup"><span data-stu-id="defa2-138">If the keys are set, **FGetComponentPath** gives the path of the client's implementation of MAPI.</span></span> 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a><span data-ttu-id="defa2-139">Реализация алгоритма поиска клиента MAPI</span><span class="sxs-lookup"><span data-stu-id="defa2-139">Implementing the MAPI Client Lookup algorithm</span></span>

<span data-ttu-id="defa2-140">В следующей таблице перечислены четыре функции из MFCMAPI, которые используются для искомого пути для пользовательской реализации MAPI:</span><span class="sxs-lookup"><span data-stu-id="defa2-140">The following table lists the four functions from MFCMAPI that are used to look up the path for a custom implementation of MAPI:</span></span>
  
|<span data-ttu-id="defa2-141">**Function**</span><span class="sxs-lookup"><span data-stu-id="defa2-141">**Function**</span></span>|<span data-ttu-id="defa2-142">**Описание**</span><span class="sxs-lookup"><span data-stu-id="defa2-142">**Description**</span></span>|
|:-----|:-----|
| `GetMAPIPath` <br/> |<span data-ttu-id="defa2-143">Получает путь к библиотеке MAPI.</span><span class="sxs-lookup"><span data-stu-id="defa2-143">Gets the MAPI library path.</span></span>  <br/> |
| `GetMailKey` <br/> |<span data-ttu-id="defa2-144">Получает ключ реестра почты MAPI.</span><span class="sxs-lookup"><span data-stu-id="defa2-144">Gets the MAPI mail registry key.</span></span>  <br/> |
| `GetMapiMsiIds` <br/> |<span data-ttu-id="defa2-145">Получает идентификатор установщика Windows.</span><span class="sxs-lookup"><span data-stu-id="defa2-145">Gets the Windows Installer identifier.</span></span>  <br/> |
| `GetComponentPath` <br/> |<span data-ttu-id="defa2-146">Получает путь к компоненту с помощью [FGetComponentPath.](fgetcomponentpath.md)</span><span class="sxs-lookup"><span data-stu-id="defa2-146">Gets the component path using [FGetComponentPath](fgetcomponentpath.md).</span></span>  <br/> |
   
<span data-ttu-id="defa2-147">Так как MFCMAPI загружает стандартную реализацию MAPI по умолчанию, если вы хотите использовать другую реализацию MAPI, для этого необходимо явным образом направить ее.</span><span class="sxs-lookup"><span data-stu-id="defa2-147">Because MFCMAPI loads the default implementation of MAPI by default, if you want to use a different implementation of MAPI, you must explicitly direct it to do so.</span></span> <span data-ttu-id="defa2-148">Это выполняется с помощью **процедуры Session\Load MAPI.**</span><span class="sxs-lookup"><span data-stu-id="defa2-148">This is performed by using the **Session\Load MAPI** routine.</span></span> 
  
### <a name="how-these-functions-work"></a><span data-ttu-id="defa2-149">Как работают эти функции</span><span class="sxs-lookup"><span data-stu-id="defa2-149">How these functions work</span></span>

1. <span data-ttu-id="defa2-150">Вызовы MFCMAPI  `GetMAPIPath` с передачей NULL для параметра клиента для загрузки реализации MAPI по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="defa2-150">MFCMAPI calls  `GetMAPIPath`, passing NULL for the client parameter, to load the default MAPI implementation.</span></span>
    
2.  <span data-ttu-id="defa2-151">`GetMAPIPath`вызовы для чтения значений `GetMapiMsiIds` **MSIComponentID,** **MSIApplicationLCID** и **MSIOfficeLCID.**</span><span class="sxs-lookup"><span data-stu-id="defa2-151">`GetMAPIPath` calls  `GetMapiMsiIds` to read the values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
3.  <span data-ttu-id="defa2-152">`GetMapiMsiIds``GetMailKey`вызовы, чтобы открыть ключ реестра для почтового клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="defa2-152">`GetMapiMsiIds` calls  `GetMailKey` to open the registry key for the default mail client.</span></span> 
    
4.  <span data-ttu-id="defa2-153">`GetMapiMsiIds`использует работку реестра, возвращаемую для возвращения значений `GetMailKey` **для MSIComponentID,** **MSIApplicationLCID** и **MSIOfficeLCID.**</span><span class="sxs-lookup"><span data-stu-id="defa2-153">`GetMapiMsiIds` uses the registry handle returned by  `GetMailKey` to look up values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
5. <span data-ttu-id="defa2-154">Значения **MSIComponentID,** **MSIApplicationLCID** и **MSIOfficeLCID** возвращаются в  `GetMAPIPath` .</span><span class="sxs-lookup"><span data-stu-id="defa2-154">The values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**, are returned to  `GetMAPIPath`.</span></span>  <span data-ttu-id="defa2-155">`GetMAPIPath` затем передает их в  `GetComponentPath` .</span><span class="sxs-lookup"><span data-stu-id="defa2-155">`GetMAPIPath` then passes them to  `GetComponentPath`.</span></span>
    
6.  <span data-ttu-id="defa2-156">`GetComponentPath` загружает библиотеку загона MAPI Mapi32.dll из системного каталога.</span><span class="sxs-lookup"><span data-stu-id="defa2-156">`GetComponentPath` loads the MAPI stub library, Mapi32.dll, from the system directory.</span></span> 
    
7.  <span data-ttu-id="defa2-157">`GetComponentPath`затем извлекает адрес функции **FGetComponentPath** из Mapi32.dll при условии, что Mapi32.dll **экспортирует FGetComponentPath.**</span><span class="sxs-lookup"><span data-stu-id="defa2-157">`GetComponentPath` then retrieves the address of the **FGetComponentPath** function from Mapi32.dll, assuming that Mapi32.dll exports **FGetComponentPath**.</span></span>
    
8. <span data-ttu-id="defa2-158">Если получить адрес **FGetComponentPath** из Mapi32.dll не удается, получает адрес из  `GetComponentPath` Mapistub.dll.</span><span class="sxs-lookup"><span data-stu-id="defa2-158">If getting the address of **FGetComponentPath** from Mapi32.dll fails,  `GetComponentPath` retrieves the address from Mapistub.dll.</span></span> 
    
9.  <span data-ttu-id="defa2-159">`GetComponentPath` Затем **вызывается FGetComponentPath,** который получает путь к версии MAPI по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="defa2-159">`GetComponentPath` then calls **FGetComponentPath**, obtaining the path of the default version of MAPI.</span></span>
    
10.  <span data-ttu-id="defa2-160">`GetMAPIPath`затем возвращает этот путь вызываемой, которая затем загружает MAPI и явным образом ссылается на него, как описано в ссылке на [функции MAPI.](how-to-link-to-mapi-functions.md)</span><span class="sxs-lookup"><span data-stu-id="defa2-160">`GetMAPIPath` then returns this path to the caller, which then loads MAPI and explicitly links to it as described in [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="defa2-161">Для поддержки локализованных копий MAPI для английского и неименизованного языка считывайте значения подкайки `GetMAPIPath` **MSIApplicationLCID** и **MSIOfficeLCID.**</span><span class="sxs-lookup"><span data-stu-id="defa2-161">To support localized copies of MAPI for English and non-English locales,  `GetMAPIPath` reads the values for the **MSIApplicationLCID** and **MSIOfficeLCID** subkeys.</span></span>  <span data-ttu-id="defa2-162">`GetMAPIPath`затем вызывает **FGetComponentPath,** сначала укажите **MSIApplicationLCID** как **szQualifier,** а затем снова укажите **MSIOfficeLCID** как **szQualifier.**</span><span class="sxs-lookup"><span data-stu-id="defa2-162">`GetMAPIPath` then calls **FGetComponentPath**, first specifying **MSIApplicationLCID** as **szQualifier**, and again specifying **MSIOfficeLCID** as **szQualifier**.</span></span> <span data-ttu-id="defa2-163">Дополнительные сведения о ключах реестра для почтовых клиентов, которые поддерживают не английский язык, см. в настройке [ключей MSI для вашей DLL MAPI.](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="defa2-163">For more information about registry keys for mail clients that support non-English languages, see [Setting Up the MSI Keys for Your MAPI DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).</span></span>   
> - <span data-ttu-id="defa2-164">Если MFCMAPI не получает путь для использования MAPI, он загружает библиотеку загружки  `GetMAPIPath` MAPI из системного каталога.</span><span class="sxs-lookup"><span data-stu-id="defa2-164">If MFCMAPI does not receive a path for MAPI using  `GetMAPIPath`, it loads the MAPI stub library from the system directory.</span></span>
> - <span data-ttu-id="defa2-165">Значение **реестра MSMapiApps,** обсуждаемые в явном сопоставлении вызовов MAPI с [библиотеками DLL MAPI,](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) применяется только в том случае, если используется библиотека ЗАГТ MAPI.</span><span class="sxs-lookup"><span data-stu-id="defa2-165">The **MSMapiApps** registry value discussed in [Explicitly Mapping MAPI Calls to MAPI DLLs](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) only applies when the MAPI Stub library is used.</span></span> <span data-ttu-id="defa2-166">Приложения, которые загружают определенную реализацию MAPI или загружают реализацию по умолчанию, не должны устанавливать **ключ реестра MSMapiApps.**</span><span class="sxs-lookup"><span data-stu-id="defa2-166">Applications that load a specific implementation of MAPI or load the default implementation do not have to set the **MSMapiApps** registry key.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="defa2-167">См. также</span><span class="sxs-lookup"><span data-stu-id="defa2-167">See also</span></span>

- [<span data-ttu-id="defa2-168">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="defa2-168">FGetComponentPath</span></span>](fgetcomponentpath.md)
- [<span data-ttu-id="defa2-169">Общие сведения о программировании MAPI</span><span class="sxs-lookup"><span data-stu-id="defa2-169">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="defa2-170">Ссылки на функции MAPI</span><span class="sxs-lookup"><span data-stu-id="defa2-170">Link to MAPI Functions</span></span>](how-to-link-to-mapi-functions.md)
- [<span data-ttu-id="defa2-171">Mapi32.dll реестра загной</span><span class="sxs-lookup"><span data-stu-id="defa2-171">Mapi32.dll Stub Registry Settings</span></span>](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [<span data-ttu-id="defa2-172">Настройка ключей MSI для DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="defa2-172">Setting Up the MSI Keys for Your MAPI DLL</span></span>](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [<span data-ttu-id="defa2-173">Явное сопоставление вызовов MAPI с DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="defa2-173">Explicitly Mapping MAPI Calls to MAPI DLLs</span></span>](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

