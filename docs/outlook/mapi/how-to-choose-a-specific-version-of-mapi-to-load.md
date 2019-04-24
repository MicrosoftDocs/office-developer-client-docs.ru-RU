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
# <a name="choose-a-specific-version-of-mapi-to-load"></a><span data-ttu-id="def3b-103">Выбор определенной версии MAPI для загрузки</span><span class="sxs-lookup"><span data-stu-id="def3b-103">Choose a specific version of MAPI to load</span></span>

<span data-ttu-id="def3b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="def3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="def3b-105">При явном связывании с реализацией MAPI необходимо тщательно выбирать реализацию для загрузки.</span><span class="sxs-lookup"><span data-stu-id="def3b-105">When linking explicitly to an implementation of MAPI, you must carefully select which implementation to load.</span></span> 
  
<span data-ttu-id="def3b-106">Существует два метода, которые явно связываются с реализацией MAPI.</span><span class="sxs-lookup"><span data-stu-id="def3b-106">There are two methods to link explicitly to an implementation of MAPI.</span></span> 
  
1. <span data-ttu-id="def3b-107">Вы можете загрузить библиотеку заглушек MAPI и указать в реестре пользовательскую БИБЛИОТЕКУ DLL для загрузки и отправки вызовов MAPI.</span><span class="sxs-lookup"><span data-stu-id="def3b-107">You can load the MAPI stub library, and specify in the registry a custom DLL to load and dispatch MAPI calls to.</span></span>
    
2. <span data-ttu-id="def3b-108">Вы можете реализовать алгоритм поиска клиентов MAPI, чтобы найти версию MAPI, используемую почтовым клиентом по умолчанию, и загрузить ее.</span><span class="sxs-lookup"><span data-stu-id="def3b-108">You can implement the MAPI client lookup algorithm to look up the version of MAPI used by the default mail client and load it.</span></span>
    
<span data-ttu-id="def3b-109">Так как вы можете изменить [параметры реестра для заглушки MAPI32. dll](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) , чтобы приложение могло использовать любую реализацию MAPI, рекомендуется направлять приложение для использования реализации MAPI, с которой вы тестировали.</span><span class="sxs-lookup"><span data-stu-id="def3b-109">Because you can change the [Mapi32.dll Stub Registry Settings](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx) to direct your application to use any implementation of MAPI, we recommend that you direct your application to use an implementation of MAPI that you have tested with.</span></span> <span data-ttu-id="def3b-110">Далее описаны оба метода связывания явным образом.</span><span class="sxs-lookup"><span data-stu-id="def3b-110">The following describes both methods of linking explicitly.</span></span> 
  
## <a name="reading-from-the-registry"></a><span data-ttu-id="def3b-111">Чтение из реестра</span><span class="sxs-lookup"><span data-stu-id="def3b-111">Reading from the registry</span></span>

### <a name="to-read-mapi-implementation-information-from-the-registry"></a><span data-ttu-id="def3b-112">Чтение сведений о реализации MAPI из реестра</span><span class="sxs-lookup"><span data-stu-id="def3b-112">To read MAPI implementation information from the registry</span></span>

1. <span data-ttu-id="def3b-113">Разделы реестра, указывающие на пользовательскую БИБЛИОТЕКУ DLL для почтового клиента, расположены `HKLM\Software\Clients\Mail` в ключе почтового клиента.</span><span class="sxs-lookup"><span data-stu-id="def3b-113">The registry keys that indicate a custom DLL for a mail client are located under the  `HKLM\Software\Clients\Mail` key of the mail client.</span></span> 
    
   <span data-ttu-id="def3b-114">В следующей таблице описываются эти ключи:</span><span class="sxs-lookup"><span data-stu-id="def3b-114">The following table describes these keys:</span></span>
    
   |<span data-ttu-id="def3b-115">**Клавиша**</span><span class="sxs-lookup"><span data-stu-id="def3b-115">**Key**</span></span>|<span data-ttu-id="def3b-116">**Описание**</span><span class="sxs-lookup"><span data-stu-id="def3b-116">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="def3b-117">Мсикомпонентид</span><span class="sxs-lookup"><span data-stu-id="def3b-117">MSIComponentID</span></span>  <br/> |<span data-ttu-id="def3b-118">Идентификатор категории Публишкомпонент установщика Windows (GUID), который определяет БИБЛИОТЕКУ DLL, которая экспортирует простые вызовы MAPI или MAPI.</span><span class="sxs-lookup"><span data-stu-id="def3b-118">A Windows Installer PublishComponent category ID (GUID) that identifies the DLL that exports simple MAPI or MAPI calls.</span></span> <span data-ttu-id="def3b-119">Если этот параметр установлен, этот ключ имеет приоритет над ключом **DLLPath** или **дллпасекс** .</span><span class="sxs-lookup"><span data-stu-id="def3b-119">If set, this key takes precedence over the **DLLPath** or **DLLPathEx** key.</span></span>  <br/> |
   |<span data-ttu-id="def3b-120">МсиаппликатионлЦид</span><span class="sxs-lookup"><span data-stu-id="def3b-120">MSIApplicationLCID</span></span>  <br/> |<span data-ttu-id="def3b-121">Идентификатор языкового стандарта (LCID) для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="def3b-121">Locale identifier (LCID) for your application.</span></span> <span data-ttu-id="def3b-122">Первое строковое значение определяет подключ из `HKLM\Software` , а последующие строковые значения определяют значения реестра под этим ключом, содержащие сведения о языковых стандартах.</span><span class="sxs-lookup"><span data-stu-id="def3b-122">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key that contain locale information.</span></span>  <br/> |
   |<span data-ttu-id="def3b-123">МсиоффицелЦид</span><span class="sxs-lookup"><span data-stu-id="def3b-123">MSIOfficeLCID</span></span>  <br/> |<span data-ttu-id="def3b-124">LCID для Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="def3b-124">LCIDs for Microsoft Office.</span></span> <span data-ttu-id="def3b-125">Первое строковое значение определяет подключ из `HKLM\Software` и последующие строковые значения, определяющие значения реестра под этим ключом.</span><span class="sxs-lookup"><span data-stu-id="def3b-125">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key.</span></span>  <br/> |
   
   <span data-ttu-id="def3b-126">Получите сведения из этих разделов.</span><span class="sxs-lookup"><span data-stu-id="def3b-126">Obtain the information from these keys.</span></span>
    
2. <span data-ttu-id="def3b-127">Передайте значения, полученные на предыдущем шаге, в функцию [фжеткомпонентпас](fgetcomponentpath.md) .</span><span class="sxs-lookup"><span data-stu-id="def3b-127">Pass the values that you obtained from the previous step to the [FGetComponentPath](fgetcomponentpath.md) function.</span></span> <span data-ttu-id="def3b-128">**Фжеткомпонентпас** — это функция, которая экспортируется библиотекой-заглушкой MAPI мапистуб. dll.</span><span class="sxs-lookup"><span data-stu-id="def3b-128">**FGetComponentPath** is a function that is exported by the MAPI stub library Mapistub.dll.</span></span> <span data-ttu-id="def3b-129">Он возвращает путь к настраиваемой версии MAPI.</span><span class="sxs-lookup"><span data-stu-id="def3b-129">It returns the path of the custom version of MAPI.</span></span> 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a><span data-ttu-id="def3b-130">Загрузка реализации MAPI, помеченной как используемая по умолчанию</span><span class="sxs-lookup"><span data-stu-id="def3b-130">To load the implementation of MAPI marked as default</span></span>

1. <span data-ttu-id="def3b-131">Считывание `HKLM\Software\Clients\Mail::(default)` значения реестра.</span><span class="sxs-lookup"><span data-stu-id="def3b-131">Read the  `HKLM\Software\Clients\Mail::(default)` registry value.</span></span> 
    
2. <span data-ttu-id="def3b-132">Найдите сведения об указанном клиенте, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="def3b-132">Look up the information for the indicated client as described earlier.</span></span>
    
> [!NOTE]
> <span data-ttu-id="def3b-133">Обратите внимание, что почтовый клиент по умолчанию не может реализовать расширенный MAPI.</span><span class="sxs-lookup"><span data-stu-id="def3b-133">Note that the default mail client might not implement Extended MAPI.</span></span> 
  
#### <a name="example"></a><span data-ttu-id="def3b-134">Пример</span><span class="sxs-lookup"><span data-stu-id="def3b-134">Example</span></span>

<span data-ttu-id="def3b-135">Чтобы загрузить MAPI как реализованное в Outlook, найдите разделы реестра в разделе `HKLM\Software\Clients\Mail\Microsoft Outlook` и передайте их в **фжеткомпонентпас**.</span><span class="sxs-lookup"><span data-stu-id="def3b-135">To load MAPI as implemented by Outlook, look up the registry keys under  `HKLM\Software\Clients\Mail\Microsoft Outlook` and pass them to **FGetComponentPath**.</span></span> <span data-ttu-id="def3b-136">**Фжеткомпонентпас** вернет путь для реализации MAPI в Outlook.</span><span class="sxs-lookup"><span data-stu-id="def3b-136">**FGetComponentPath** will return the path for Outlook's implementation of MAPI.</span></span> 
  
<span data-ttu-id="def3b-137">Если ключи **мсикомпонентид**, **мсиаппликатионлЦид**и **мсиоффицелЦид** не заданы, проверьте значение реестра **дллпасекс** .</span><span class="sxs-lookup"><span data-stu-id="def3b-137">If the keys **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID** are not set, check the **DLLPathEx** registry value.</span></span> <span data-ttu-id="def3b-138">Если заданы ключи, **фжеткомпонентпас** предоставляет путь к реализации MAPI клиентом.</span><span class="sxs-lookup"><span data-stu-id="def3b-138">If the keys are set, **FGetComponentPath** gives the path of the client's implementation of MAPI.</span></span> 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a><span data-ttu-id="def3b-139">Реализация алгоритма поиска клиентов MAPI</span><span class="sxs-lookup"><span data-stu-id="def3b-139">Implementing the MAPI Client Lookup algorithm</span></span>

<span data-ttu-id="def3b-140">В следующей таблице перечислены четыре функции MFCMAPI, которые используются для поиска пути для пользовательской реализации MAPI:</span><span class="sxs-lookup"><span data-stu-id="def3b-140">The following table lists the four functions from MFCMAPI that are used to look up the path for a custom implementation of MAPI:</span></span>
  
|<span data-ttu-id="def3b-141">**Function**</span><span class="sxs-lookup"><span data-stu-id="def3b-141">**Function**</span></span>|<span data-ttu-id="def3b-142">**Описание**</span><span class="sxs-lookup"><span data-stu-id="def3b-142">**Description**</span></span>|
|:-----|:-----|
| `GetMAPIPath` <br/> |<span data-ttu-id="def3b-143">Получает путь к библиотеке MAPI.</span><span class="sxs-lookup"><span data-stu-id="def3b-143">Gets the MAPI library path.</span></span>  <br/> |
| `GetMailKey` <br/> |<span data-ttu-id="def3b-144">Возвращает раздел почтового ящика MAPI.</span><span class="sxs-lookup"><span data-stu-id="def3b-144">Gets the MAPI mail registry key.</span></span>  <br/> |
| `GetMapiMsiIds` <br/> |<span data-ttu-id="def3b-145">Получает идентификатор установщика Windows.</span><span class="sxs-lookup"><span data-stu-id="def3b-145">Gets the Windows Installer identifier.</span></span>  <br/> |
| `GetComponentPath` <br/> |<span data-ttu-id="def3b-146">Получает путь к компоненту с помощью [фжеткомпонентпас](fgetcomponentpath.md).</span><span class="sxs-lookup"><span data-stu-id="def3b-146">Gets the component path using [FGetComponentPath](fgetcomponentpath.md).</span></span>  <br/> |
   
<span data-ttu-id="def3b-147">Так как MFCMAPI загружает стандартную по умолчанию MAPI по умолчанию, если вы хотите использовать другую реализацию MAPI, необходимо явно направлять ее.</span><span class="sxs-lookup"><span data-stu-id="def3b-147">Because MFCMAPI loads the default implementation of MAPI by default, if you want to use a different implementation of MAPI, you must explicitly direct it to do so.</span></span> <span data-ttu-id="def3b-148">Это выполняется с помощью процедуры **MAPI сессион\лоад** .</span><span class="sxs-lookup"><span data-stu-id="def3b-148">This is performed by using the **Session\Load MAPI** routine.</span></span> 
  
### <a name="how-these-functions-work"></a><span data-ttu-id="def3b-149">Принципы работы этих функций</span><span class="sxs-lookup"><span data-stu-id="def3b-149">How these functions work</span></span>

1. <span data-ttu-id="def3b-150">Вызовы `GetMAPIPath`MFCMAPI, передающие значение NULL для параметра Client, для загрузки реализации MAPI по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="def3b-150">MFCMAPI calls  `GetMAPIPath`, passing NULL for the client parameter, to load the default MAPI implementation.</span></span>
    
2.  <span data-ttu-id="def3b-151">`GetMAPIPath`вызывает `GetMapiMsiIds` чтение значений для **мсикомпонентид**, **мсиаппликатионлЦид**и **мсиоффицелЦид**.</span><span class="sxs-lookup"><span data-stu-id="def3b-151">`GetMAPIPath` calls  `GetMapiMsiIds` to read the values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
3.  <span data-ttu-id="def3b-152">`GetMapiMsiIds`вызывает `GetMailKey` открытие раздела реестра для почтового клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="def3b-152">`GetMapiMsiIds` calls  `GetMailKey` to open the registry key for the default mail client.</span></span> 
    
4.  <span data-ttu-id="def3b-153">`GetMapiMsiIds`использует дескриптор реестра, возвращенный `GetMailKey` для поиска значений для **мсикомпонентид**, **мсиаппликатионлЦид**и **мсиоффицелЦид**.</span><span class="sxs-lookup"><span data-stu-id="def3b-153">`GetMapiMsiIds` uses the registry handle returned by  `GetMailKey` to look up values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
5. <span data-ttu-id="def3b-154">Возвращаются значения для **мсикомпонентид**, **мсиаппликатионлЦид**и **мсиоффицелЦид** `GetMAPIPath`.</span><span class="sxs-lookup"><span data-stu-id="def3b-154">The values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**, are returned to  `GetMAPIPath`.</span></span>  <span data-ttu-id="def3b-155">`GetMAPIPath`затем передает их в `GetComponentPath`.</span><span class="sxs-lookup"><span data-stu-id="def3b-155">`GetMAPIPath` then passes them to  `GetComponentPath`.</span></span>
    
6.  <span data-ttu-id="def3b-156">`GetComponentPath`загружает библиотеку-заглушку MAPI (MAPI32. dll) из системного каталога.</span><span class="sxs-lookup"><span data-stu-id="def3b-156">`GetComponentPath` loads the MAPI stub library, Mapi32.dll, from the system directory.</span></span> 
    
7.  <span data-ttu-id="def3b-157">`GetComponentPath`затем получает адрес функции **фжеткомпонентпас** из MAPI32. dll, предполагая, что MAPI32. DLL экспортирует **фжеткомпонентпас**.</span><span class="sxs-lookup"><span data-stu-id="def3b-157">`GetComponentPath` then retrieves the address of the **FGetComponentPath** function from Mapi32.dll, assuming that Mapi32.dll exports **FGetComponentPath**.</span></span>
    
8. <span data-ttu-id="def3b-158">При сбое получения адреса **фжеткомпонентпас** из MAPI32. dll `GetComponentPath` извлекается адрес из мапистуб. dll.</span><span class="sxs-lookup"><span data-stu-id="def3b-158">If getting the address of **FGetComponentPath** from Mapi32.dll fails,  `GetComponentPath` retrieves the address from Mapistub.dll.</span></span> 
    
9.  <span data-ttu-id="def3b-159">`GetComponentPath`затем вызывает **фжеткомпонентпас**, получая путь к версии MAPI по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="def3b-159">`GetComponentPath` then calls **FGetComponentPath**, obtaining the path of the default version of MAPI.</span></span>
    
10.  <span data-ttu-id="def3b-160">`GetMAPIPath`затем возвращает этот путь к вызывающему абоненту, который затем загружает MAPI и явно ссылается на него, как описано в статье [links to MAPI functions](how-to-link-to-mapi-functions.md).</span><span class="sxs-lookup"><span data-stu-id="def3b-160">`GetMAPIPath` then returns this path to the caller, which then loads MAPI and explicitly links to it as described in [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="def3b-161">Для поддержки локализованных копий MAPI для английских и не английских языковых стандартов `GetMAPIPath` считываются значения подразделов **мсиаппликатионлЦид** и **мсиоффицелЦид** .</span><span class="sxs-lookup"><span data-stu-id="def3b-161">To support localized copies of MAPI for English and non-English locales,  `GetMAPIPath` reads the values for the **MSIApplicationLCID** and **MSIOfficeLCID** subkeys.</span></span>  <span data-ttu-id="def3b-162">`GetMAPIPath`затем вызывает **фжеткомпонентпас**, сначала задавая **мсиаппликатионлЦид** как **Сзкуалифиер**, и повторно указывая **мсиоффицелЦид** как **сзкуалифиер**.</span><span class="sxs-lookup"><span data-stu-id="def3b-162">`GetMAPIPath` then calls **FGetComponentPath**, first specifying **MSIApplicationLCID** as **szQualifier**, and again specifying **MSIOfficeLCID** as **szQualifier**.</span></span> <span data-ttu-id="def3b-163">Дополнительные сведения о разделах реестра для почтовых клиентов, поддерживающих языки, отличные от английского, приведены [в разделе Настройка разделов MSI для библиотеки MAPI](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="def3b-163">For more information about registry keys for mail clients that support non-English languages, see [Setting Up the MSI Keys for Your MAPI DLL](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx).</span></span>   
> - <span data-ttu-id="def3b-164">Если MFCMAPI не получает путь для MAPI using `GetMAPIPath`, он загружает библиотеку заглушки MAPI из системного каталога.</span><span class="sxs-lookup"><span data-stu-id="def3b-164">If MFCMAPI does not receive a path for MAPI using  `GetMAPIPath`, it loads the MAPI stub library from the system directory.</span></span>
> - <span data-ttu-id="def3b-165">Значение реестра **Мсмапиаппс** , описываемое в явном соПоставлении [вызовов MAPI с БИБЛИОТЕКАми DLL MAPI](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) , применяется только при использовании библиотеки-заглушки MAPI.</span><span class="sxs-lookup"><span data-stu-id="def3b-165">The **MSMapiApps** registry value discussed in [Explicitly Mapping MAPI Calls to MAPI DLLs](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx) only applies when the MAPI Stub library is used.</span></span> <span data-ttu-id="def3b-166">Приложения, которые загружают конкретную реализацию MAPI или загружают реализацию по умолчанию, не обязательно устанавливать раздел реестра **мсмапиаппс** .</span><span class="sxs-lookup"><span data-stu-id="def3b-166">Applications that load a specific implementation of MAPI or load the default implementation do not have to set the **MSMapiApps** registry key.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="def3b-167">См. также</span><span class="sxs-lookup"><span data-stu-id="def3b-167">See also</span></span>

- [<span data-ttu-id="def3b-168">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="def3b-168">FGetComponentPath</span></span>](fgetcomponentpath.md)
- [<span data-ttu-id="def3b-169">Общие сведения о программировании MAPI</span><span class="sxs-lookup"><span data-stu-id="def3b-169">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="def3b-170">Ссылки на функции MAPI</span><span class="sxs-lookup"><span data-stu-id="def3b-170">Link to MAPI Functions</span></span>](how-to-link-to-mapi-functions.md)
- [<span data-ttu-id="def3b-171">Параметры реестра для заглушки MAPI32. dll</span><span class="sxs-lookup"><span data-stu-id="def3b-171">Mapi32.dll Stub Registry Settings</span></span>](https://msdn.microsoft.com/library/ms531218%28EXCHG.10%29.aspx)
- [<span data-ttu-id="def3b-172">Настройка ключей MSI для библиотеки MAPI</span><span class="sxs-lookup"><span data-stu-id="def3b-172">Setting Up the MSI Keys for Your MAPI DLL</span></span>](https://msdn.microsoft.com/library/ee909494%28VS.85%29.aspx)
- [<span data-ttu-id="def3b-173">Явное сопоставление вызовов MAPI с библиотеками DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="def3b-173">Explicitly Mapping MAPI Calls to MAPI DLLs</span></span>](https://msdn.microsoft.com/library/ee909490%28VS.85%29.aspx)

