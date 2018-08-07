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
ms.openlocfilehash: d0bce7b3a12f259b7ac5f28219c8a92dd2200f07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19808590"
---
# <a name="choose-a-specific-version-of-mapi-to-load"></a><span data-ttu-id="c82ae-103">Выбор определенной версии MAPI для загрузки</span><span class="sxs-lookup"><span data-stu-id="c82ae-103">Choose a specific version of MAPI to load</span></span>

<span data-ttu-id="c82ae-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c82ae-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c82ae-105">При связывании явно реализация интерфейса MAPI, необходимо тщательно выбрать реализация для загрузки.</span><span class="sxs-lookup"><span data-stu-id="c82ae-105">When linking explicitly to an implementation of MAPI, you must carefully select which implementation to load.</span></span> 
  
<span data-ttu-id="c82ae-106">Существует два метода для связывания явно реализация интерфейса MAPI.</span><span class="sxs-lookup"><span data-stu-id="c82ae-106">There are two methods to link explicitly to an implementation of MAPI.</span></span> 
  
1. <span data-ttu-id="c82ae-107">Можно загрузить библиотеку заглушка MAPI и укажите в вызовы пользовательских DLL для загрузки и отправки MAPI реестра.</span><span class="sxs-lookup"><span data-stu-id="c82ae-107">You can load the MAPI stub library, and specify in the registry a custom DLL to load and dispatch MAPI calls to.</span></span>
    
2. <span data-ttu-id="c82ae-108">Можно реализовать алгоритм подстановки клиента MAPI для поиска версия MAPI, используемых почтового клиента по умолчанию и загрузить его.</span><span class="sxs-lookup"><span data-stu-id="c82ae-108">You can implement the MAPI client lookup algorithm to look up the version of MAPI used by the default mail client and load it.</span></span>
    
<span data-ttu-id="c82ae-109">Можно изменить [Параметры реестра Mapi32.dll заглушку](http://msdn.microsoft.com/en-us/library/ms531218%28EXCHG.10%29.aspx) для направления приложения для использования любой реализации интерфейса MAPI, поэтому рекомендуется прямое подключение приложения для использования реализация интерфейса MAPI, проверенного с.</span><span class="sxs-lookup"><span data-stu-id="c82ae-109">Because you can change the [Mapi32.dll Stub Registry Settings](http://msdn.microsoft.com/en-us/library/ms531218%28EXCHG.10%29.aspx) to direct your application to use any implementation of MAPI, we recommend that you direct your application to use an implementation of MAPI that you have tested with.</span></span> <span data-ttu-id="c82ae-110">Ниже описаны оба метода компоновки явным образом.</span><span class="sxs-lookup"><span data-stu-id="c82ae-110">The following describes both methods of linking explicitly.</span></span> 
  
## <a name="reading-from-the-registry"></a><span data-ttu-id="c82ae-111">Чтение из реестра</span><span class="sxs-lookup"><span data-stu-id="c82ae-111">Reading from the registry</span></span>

### <a name="to-read-mapi-implementation-information-from-the-registry"></a><span data-ttu-id="c82ae-112">Чтение из реестра сведения о реализации интерфейса MAPI</span><span class="sxs-lookup"><span data-stu-id="c82ae-112">To read MAPI implementation information from the registry</span></span>

1. <span data-ttu-id="c82ae-113">Разделы реестра, которые указывают пользовательской библиотеки DLL для почтового клиента, находятся в разделе `HKLM\Software\Clients\Mail` ключа почтового клиента.</span><span class="sxs-lookup"><span data-stu-id="c82ae-113">The registry keys that indicate a custom DLL for a mail client are located under the  `HKLM\Software\Clients\Mail` key of the mail client.</span></span> 
    
   <span data-ttu-id="c82ae-114">В следующей таблице описываются эти разделы:</span><span class="sxs-lookup"><span data-stu-id="c82ae-114">The following table describes these keys:</span></span>
    
   |<span data-ttu-id="c82ae-115">**Key**</span><span class="sxs-lookup"><span data-stu-id="c82ae-115">**Key**</span></span>|<span data-ttu-id="c82ae-116">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c82ae-116">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="c82ae-117">MSIComponentID</span><span class="sxs-lookup"><span data-stu-id="c82ae-117">MSIComponentID</span></span>  <br/> |<span data-ttu-id="c82ae-118">Вызывает PublishComponent установщика Windows категории идентификатор (GUID), идентифицирующий библиотеки DLL, которая экспортирует простой MAPI или MAPI.</span><span class="sxs-lookup"><span data-stu-id="c82ae-118">A Windows Installer PublishComponent category ID (GUID) that identifies the DLL that exports simple MAPI or MAPI calls.</span></span> <span data-ttu-id="c82ae-119">Если набор, этот раздел приоритет над **DLLPath** или **DLLPathEx** ключа.</span><span class="sxs-lookup"><span data-stu-id="c82ae-119">If set, this key takes precedence over the **DLLPath** or **DLLPathEx** key.</span></span>  <br/> |
   |<span data-ttu-id="c82ae-120">MSIApplicationLCID</span><span class="sxs-lookup"><span data-stu-id="c82ae-120">MSIApplicationLCID</span></span>  <br/> |<span data-ttu-id="c82ae-121">Код языка (LCID) для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="c82ae-121">Locale identifier (LCID) for your application.</span></span> <span data-ttu-id="c82ae-122">Первая строка значение определяет подраздел из `HKLM\Software` и последующих строковые значения идентификации пример значения реестра, которые содержат сведения о языковом стандарте.</span><span class="sxs-lookup"><span data-stu-id="c82ae-122">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key that contain locale information.</span></span>  <br/> |
   |<span data-ttu-id="c82ae-123">MSIOfficeLCID</span><span class="sxs-lookup"><span data-stu-id="c82ae-123">MSIOfficeLCID</span></span>  <br/> |<span data-ttu-id="c82ae-124">Коды языка для Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="c82ae-124">LCIDs for Microsoft Office.</span></span> <span data-ttu-id="c82ae-125">Первая строка значение определяет подраздел из `HKLM\Software` и последующих строковые значения определение значения реестра под этот ключ.</span><span class="sxs-lookup"><span data-stu-id="c82ae-125">The first string value identifies a sub-key from  `HKLM\Software` and subsequent string values identify registry values underneath this key.</span></span>  <br/> |
   
   <span data-ttu-id="c82ae-126">Получите данные из этих разделов.</span><span class="sxs-lookup"><span data-stu-id="c82ae-126">Obtain the information from these keys.</span></span>
    
2. <span data-ttu-id="c82ae-127">Передайте значения, которые вы получили из предыдущего шага в функцию [FGetComponentPath](fgetcomponentpath.md) .</span><span class="sxs-lookup"><span data-stu-id="c82ae-127">Pass the values that you obtained from the previous step to the [FGetComponentPath](fgetcomponentpath.md) function.</span></span> <span data-ttu-id="c82ae-128">**FGetComponentPath** — это функция, который экспортируется в библиотеке заглушка MAPI Mapistub.dll.</span><span class="sxs-lookup"><span data-stu-id="c82ae-128">**FGetComponentPath** is a function that is exported by the MAPI stub library Mapistub.dll.</span></span> <span data-ttu-id="c82ae-129">Она возвращает путь настраиваемой версии MAPI.</span><span class="sxs-lookup"><span data-stu-id="c82ae-129">It returns the path of the custom version of MAPI.</span></span> 


### <a name="to-load-the-implementation-of-mapi-marked-as-default"></a><span data-ttu-id="c82ae-130">Чтобы загрузить реализации интерфейса MAPI, помеченные как по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c82ae-130">To load the implementation of MAPI marked as default</span></span>

1. <span data-ttu-id="c82ae-131">Чтение `HKLM\Software\Clients\Mail::(default)` значения реестра.</span><span class="sxs-lookup"><span data-stu-id="c82ae-131">Read the  `HKLM\Software\Clients\Mail::(default)` registry value.</span></span> 
    
2. <span data-ttu-id="c82ae-132">Поиск сведений для указанного клиента, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="c82ae-132">Look up the information for the indicated client as described earlier.</span></span>
    
> [!NOTE]
> <span data-ttu-id="c82ae-133">Обратите внимание на то, что почтового клиента по умолчанию не может внедрить расширенного MAPI.</span><span class="sxs-lookup"><span data-stu-id="c82ae-133">Note that the default mail client might not implement Extended MAPI.</span></span> 
  
#### <a name="example"></a><span data-ttu-id="c82ae-134">Пример</span><span class="sxs-lookup"><span data-stu-id="c82ae-134">Example</span></span>

<span data-ttu-id="c82ae-135">Чтобы загрузить MAPI, реализованные в Outlook, поиск разделов реестра в разделе `HKLM\Software\Clients\Mail\Microsoft Outlook` и передавайте их **FGetComponentPath**.</span><span class="sxs-lookup"><span data-stu-id="c82ae-135">To load MAPI as implemented by Outlook, look up the registry keys under  `HKLM\Software\Clients\Mail\Microsoft Outlook` and pass them to **FGetComponentPath**.</span></span> <span data-ttu-id="c82ae-136">**FGetComponentPath** возвращает путь для реализации Outlook MAPI.</span><span class="sxs-lookup"><span data-stu-id="c82ae-136">**FGetComponentPath** will return the path for Outlook's implementation of MAPI.</span></span> 
  
<span data-ttu-id="c82ae-137">Если ключи **MSIComponentID**, **MSIApplicationLCID**и **MSIOfficeLCID** не задано, проверьте значение реестра **DLLPathEx** .</span><span class="sxs-lookup"><span data-stu-id="c82ae-137">If the keys **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID** are not set, check the **DLLPathEx** registry value.</span></span> <span data-ttu-id="c82ae-138">Если заданы ключи, **FGetComponentPath** дает пути реализации клиента MAPI.</span><span class="sxs-lookup"><span data-stu-id="c82ae-138">If the keys are set, **FGetComponentPath** gives the path of the client's implementation of MAPI.</span></span> 
  
## <a name="implementing-the-mapi-client-lookup-algorithm"></a><span data-ttu-id="c82ae-139">Реализация алгоритма поиска клиентов MAPI</span><span class="sxs-lookup"><span data-stu-id="c82ae-139">Implementing the MAPI Client Lookup algorithm</span></span>

<span data-ttu-id="c82ae-140">В следующей таблице приведены четыре функций из mfcmapi (en), которые используются для поиска путь для настраиваемая реализация интерфейса MAPI:</span><span class="sxs-lookup"><span data-stu-id="c82ae-140">The following table lists the four functions from MFCMAPI that are used to look up the path for a custom implementation of MAPI:</span></span>
  
|<span data-ttu-id="c82ae-141">**Функция**</span><span class="sxs-lookup"><span data-stu-id="c82ae-141">**Function**</span></span>|<span data-ttu-id="c82ae-142">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c82ae-142">**Description**</span></span>|
|:-----|:-----|
| `GetMAPIPath` <br/> |<span data-ttu-id="c82ae-143">Возвращает путь к библиотеке MAPI.</span><span class="sxs-lookup"><span data-stu-id="c82ae-143">Gets the MAPI library path.</span></span>  <br/> |
| `GetMailKey` <br/> |<span data-ttu-id="c82ae-144">Получает раздел реестра почты MAPI.</span><span class="sxs-lookup"><span data-stu-id="c82ae-144">Gets the MAPI mail registry key.</span></span>  <br/> |
| `GetMapiMsiIds` <br/> |<span data-ttu-id="c82ae-145">Получает идентификатор установщика Windows.</span><span class="sxs-lookup"><span data-stu-id="c82ae-145">Gets the Windows Installer identifier.</span></span>  <br/> |
| `GetComponentPath` <br/> |<span data-ttu-id="c82ae-146">Возвращает путь к компоненту, с помощью [FGetComponentPath](fgetcomponentpath.md).</span><span class="sxs-lookup"><span data-stu-id="c82ae-146">Gets the component path using [FGetComponentPath](fgetcomponentpath.md).</span></span>  <br/> |
   
<span data-ttu-id="c82ae-147">Так как mfcmapi (en) загружается по умолчанию реализация интерфейса MAPI по умолчанию, если вы хотите использовать другой реализации интерфейса MAPI, необходимо явно прямой соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="c82ae-147">Because MFCMAPI loads the default implementation of MAPI by default, if you want to use a different implementation of MAPI, you must explicitly direct it to do so.</span></span> <span data-ttu-id="c82ae-148">Это выполняется с помощью процедуры **Session\Load MAPI** .</span><span class="sxs-lookup"><span data-stu-id="c82ae-148">This is performed by using the **Session\Load MAPI** routine.</span></span> 
  
### <a name="how-these-functions-work"></a><span data-ttu-id="c82ae-149">Как работают эти функции</span><span class="sxs-lookup"><span data-stu-id="c82ae-149">How these functions work</span></span>

1. <span data-ttu-id="c82ae-150">Mfcmapi (en) вызовы `GetMAPIPath`, передача NULL для параметра клиента для загрузки реализация интерфейса MAPI по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c82ae-150">MFCMAPI calls  `GetMAPIPath`, passing NULL for the client parameter, to load the default MAPI implementation.</span></span>
    
2.  <span data-ttu-id="c82ae-151">`GetMAPIPath`вызовы `GetMapiMsiIds` считывать значения для **MSIComponentID**, **MSIApplicationLCID**и **MSIOfficeLCID**.</span><span class="sxs-lookup"><span data-stu-id="c82ae-151">`GetMAPIPath` calls  `GetMapiMsiIds` to read the values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
3.  <span data-ttu-id="c82ae-152">`GetMapiMsiIds`вызовы `GetMailKey` открыть раздел реестра для почтового клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c82ae-152">`GetMapiMsiIds` calls  `GetMailKey` to open the registry key for the default mail client.</span></span> 
    
4.  <span data-ttu-id="c82ae-153">`GetMapiMsiIds`с помощью реестра дескриптор, возвращенный `GetMailKey` для поиска значений для **MSIComponentID**, **MSIApplicationLCID**и **MSIOfficeLCID**.</span><span class="sxs-lookup"><span data-stu-id="c82ae-153">`GetMapiMsiIds` uses the registry handle returned by  `GetMailKey` to look up values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**.</span></span>
    
5. <span data-ttu-id="c82ae-154">Возвращаемые значения для **MSIComponentID**, **MSIApplicationLCID**и **MSIOfficeLCID**, чтобы `GetMAPIPath`.</span><span class="sxs-lookup"><span data-stu-id="c82ae-154">The values for **MSIComponentID**, **MSIApplicationLCID**, and **MSIOfficeLCID**, are returned to  `GetMAPIPath`.</span></span>  <span data-ttu-id="c82ae-155">`GetMAPIPath`передает их `GetComponentPath`.</span><span class="sxs-lookup"><span data-stu-id="c82ae-155">`GetMAPIPath` then passes them to  `GetComponentPath`.</span></span>
    
6.  <span data-ttu-id="c82ae-156">`GetComponentPath`загружает библиотеку заглушка MAPI, Mapi32.dll, из каталога системы.</span><span class="sxs-lookup"><span data-stu-id="c82ae-156">`GetComponentPath` loads the MAPI stub library, Mapi32.dll, from the system directory.</span></span> 
    
7.  <span data-ttu-id="c82ae-157">`GetComponentPath`затем извлекает адрес функции **FGetComponentPath** из Mapi32.dll, при условии, что Mapi32.dll экспортирует **FGetComponentPath**.</span><span class="sxs-lookup"><span data-stu-id="c82ae-157">`GetComponentPath` then retrieves the address of the **FGetComponentPath** function from Mapi32.dll, assuming that Mapi32.dll exports **FGetComponentPath**.</span></span>
    
8. <span data-ttu-id="c82ae-158">Если получение адреса **FGetComponentPath** из возникает ошибка Mapi32.dll `GetComponentPath` извлекает адрес из Mapistub.dll.</span><span class="sxs-lookup"><span data-stu-id="c82ae-158">If getting the address of **FGetComponentPath** from Mapi32.dll fails,  `GetComponentPath` retrieves the address from Mapistub.dll.</span></span> 
    
9.  <span data-ttu-id="c82ae-159">`GetComponentPath`затем вызывает **FGetComponentPath**, получение путь по умолчанию версии MAPI.</span><span class="sxs-lookup"><span data-stu-id="c82ae-159">`GetComponentPath` then calls **FGetComponentPath**, obtaining the path of the default version of MAPI.</span></span>
    
10.  <span data-ttu-id="c82ae-160">`GetMAPIPath`затем возвращает этот путь к вызывающему, который затем загружает MAPI и явно приведены ссылки на него, как описано в [ссылка на функции MAPI](how-to-link-to-mapi-functions.md).</span><span class="sxs-lookup"><span data-stu-id="c82ae-160">`GetMAPIPath` then returns this path to the caller, which then loads MAPI and explicitly links to it as described in [Link to MAPI Functions](how-to-link-to-mapi-functions.md).</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="c82ae-161">Для поддержки локализованных копий MAPI для английского языка и языковых стандартов неанглийской `GetMAPIPath` считывает значения для **MSIApplicationLCID** и **MSIOfficeLCID** подразделы.</span><span class="sxs-lookup"><span data-stu-id="c82ae-161">To support localized copies of MAPI for English and non-English locales,  `GetMAPIPath` reads the values for the **MSIApplicationLCID** and **MSIOfficeLCID** subkeys.</span></span>  <span data-ttu-id="c82ae-162">`GetMAPIPath`затем вызывает **FGetComponentPath**, сначала указав **MSIApplicationLCID** как **szQualifier**, а еще раз **MSIOfficeLCID** как **szQualifier**.</span><span class="sxs-lookup"><span data-stu-id="c82ae-162">`GetMAPIPath` then calls **FGetComponentPath**, first specifying **MSIApplicationLCID** as **szQualifier**, and again specifying **MSIOfficeLCID** as **szQualifier**.</span></span> <span data-ttu-id="c82ae-163">Дополнительные сведения о разделах реестра для почтовых клиентов, которые поддерживают языками см [параметр копирование MSI для Your MAPI DLL](http://msdn.microsoft.com/en-us/library/ee909494%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c82ae-163">For more information about registry keys for mail clients that support non-English languages, see [Setting Up the MSI Keys for Your MAPI DLL](http://msdn.microsoft.com/en-us/library/ee909494%28VS.85%29.aspx).</span></span>   
> - <span data-ttu-id="c82ae-164">Если mfcmapi (en) не получает путь для использования интерфейса MAPI `GetMAPIPath`, он загружает библиотеку заглушка MAPI из каталога системы.</span><span class="sxs-lookup"><span data-stu-id="c82ae-164">If MFCMAPI does not receive a path for MAPI using  `GetMAPIPath`, it loads the MAPI stub library from the system directory.</span></span>
> - <span data-ttu-id="c82ae-165">Параметр реестра **MSMapiApps** , обсуждаемые в [Явно сопоставление вызовов программного интерфейса MAPI для библиотеки MAPI DLL](http://msdn.microsoft.com/en-us/library/ee909490%28VS.85%29.aspx) применяется только при использовании библиотеки заглушка MAPI.</span><span class="sxs-lookup"><span data-stu-id="c82ae-165">The **MSMapiApps** registry value discussed in [Explicitly Mapping MAPI Calls to MAPI DLLs](http://msdn.microsoft.com/en-us/library/ee909490%28VS.85%29.aspx) only applies when the MAPI Stub library is used.</span></span> <span data-ttu-id="c82ae-166">Приложения, которые загрузить реализации интерфейса MAPI или загрузить реализация по умолчанию не нужно задать раздел реестра **MSMapiApps** .</span><span class="sxs-lookup"><span data-stu-id="c82ae-166">Applications that load a specific implementation of MAPI or load the default implementation do not have to set the **MSMapiApps** registry key.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c82ae-167">См. также</span><span class="sxs-lookup"><span data-stu-id="c82ae-167">See also</span></span>

- [<span data-ttu-id="c82ae-168">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="c82ae-168">FGetComponentPath</span></span>](fgetcomponentpath.md)
- [<span data-ttu-id="c82ae-169">����� �������� � ���������������� MAPI</span><span class="sxs-lookup"><span data-stu-id="c82ae-169">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
- [<span data-ttu-id="c82ae-170">Ссылки на функции MAPI</span><span class="sxs-lookup"><span data-stu-id="c82ae-170">Link to MAPI Functions</span></span>](how-to-link-to-mapi-functions.md)
- [<span data-ttu-id="c82ae-171">Параметры реестра заглушка Mapi32.dll</span><span class="sxs-lookup"><span data-stu-id="c82ae-171">Mapi32.dll Stub Registry Settings</span></span>](http://msdn.microsoft.com/en-us/library/ms531218%28EXCHG.10%29.aspx)
- [<span data-ttu-id="c82ae-172">Настройка разделов MSI для библиотеки DLL MAPI</span><span class="sxs-lookup"><span data-stu-id="c82ae-172">Setting Up the MSI Keys for Your MAPI DLL</span></span>](http://msdn.microsoft.com/en-us/library/ee909494%28VS.85%29.aspx)
- [<span data-ttu-id="c82ae-173">Явным образом сопоставление вызовов программного интерфейса MAPI для библиотеки MAPI DLL</span><span class="sxs-lookup"><span data-stu-id="c82ae-173">Explicitly Mapping MAPI Calls to MAPI DLLs</span></span>](http://msdn.microsoft.com/en-us/library/ee909490%28VS.85%29.aspx)

