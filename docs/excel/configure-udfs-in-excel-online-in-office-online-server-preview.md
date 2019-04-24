---
title: Настройка пользовательских функций в Excel Online в Office Online Server
manager: soliver
ms.date: 03/18/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Используйте пользовательские функции (UDF) в Excel Online в Office Online Server, чтобы вызывать пользовательские функции.
ms.openlocfilehash: dbba60a62a1a4783b47c3f1fe40a118dd8ed0d6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311062"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a><span data-ttu-id="16319-103">Настройка пользовательских функций в Excel Online в Office Online Server</span><span class="sxs-lookup"><span data-stu-id="16319-103">Configure UDFs in Excel Online in Office Online Server</span></span>

<span data-ttu-id="16319-104">Используйте пользовательские функции (UDF) в Excel Online в Office Online Server, чтобы вызывать пользовательские функции.</span><span class="sxs-lookup"><span data-stu-id="16319-104">Use user-defined functions (UDFs) in Excel Online in Office Online Server to call custom functions.</span></span> 
  
<span data-ttu-id="16319-105">Пользовательские функции (UDF) в Excel Online позволяют вызывать пользовательские функции, написанные в управляемом коде, с помощью формул в ячейках.</span><span class="sxs-lookup"><span data-stu-id="16319-105">User-defined functions (UDFs) in Excel Online enable you to call custom functions written in managed code by using formulas in cells.</span></span> <span data-ttu-id="16319-106">Пользовательские функции можно использовать для следующих функций:</span><span class="sxs-lookup"><span data-stu-id="16319-106">You can use UDFs to:</span></span>
  
- <span data-ttu-id="16319-107">Call custom mathematical functions.</span><span class="sxs-lookup"><span data-stu-id="16319-107">Call custom mathematical functions.</span></span>
    
- <span data-ttu-id="16319-108">Get data from custom data sources into worksheets.</span><span class="sxs-lookup"><span data-stu-id="16319-108">Get data from custom data sources into worksheets.</span></span>
    
- <span data-ttu-id="16319-109">Вызов веб-служб.</span><span class="sxs-lookup"><span data-stu-id="16319-109">Call web services.</span></span>
    
<span data-ttu-id="16319-110">Двоичные файлы UDF можно установить в одном из двух расположений:</span><span class="sxs-lookup"><span data-stu-id="16319-110">You can install UDF binaries in one of two locations:</span></span>
  
- <span data-ttu-id="16319-111">Локальный каталог.</span><span class="sxs-lookup"><span data-stu-id="16319-111">A local directory.</span></span> <span data-ttu-id="16319-112">Пример:</span><span class="sxs-lookup"><span data-stu-id="16319-112">For example:</span></span> 
    
    <span data-ttu-id="16319-113">К:\удфс\мисамплеудф.длл</span><span class="sxs-lookup"><span data-stu-id="16319-113">C:\UDFs\MySampleUdf.dll</span></span>
    
- <span data-ttu-id="16319-114">Глобальный кэш сборок.</span><span class="sxs-lookup"><span data-stu-id="16319-114">The global assembly cache.</span></span> <span data-ttu-id="16319-115">Пример:</span><span class="sxs-lookup"><span data-stu-id="16319-115">For example:</span></span> 
    
    <span data-ttu-id="16319-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span><span class="sxs-lookup"><span data-stu-id="16319-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span></span>
    
<span data-ttu-id="16319-117">Ссылайтесь на расположение при создании определения **New-оффицевебаппсексцелусердефинедфунктион** на сервере Office Online Server.</span><span class="sxs-lookup"><span data-stu-id="16319-117">Reference the location when you create a **New-OfficeWebAppsExcelUserDefinedFunction** definition on the Office Online Server.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="16319-118">Office Online Server не поддерживает пользовательские функции, расположенные в сетевых ресурсах.</span><span class="sxs-lookup"><span data-stu-id="16319-118">Office Online Server does not support UDFs located on network shares.</span></span> 
  
## <a name="enable-udfs-on-office-online-server"></a><span data-ttu-id="16319-119">Включение пользовательских функций в Office Online Server</span><span class="sxs-lookup"><span data-stu-id="16319-119">Enable UDFs on Office Online Server</span></span> 

<span data-ttu-id="16319-120">Когда администратор создает новую ферму серверов Office Web Apps с помощью командлета Windows PowerShell [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) , сборки UDF по умолчанию отключены.</span><span class="sxs-lookup"><span data-stu-id="16319-120">When an adminstrator creates a new Office Web Apps Server farm by using the [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell cmdlet, UDF assemblies are disabled by default.</span></span> <span data-ttu-id="16319-121">Значение по умолчанию для флага **ексцелудфсалловед** — false.</span><span class="sxs-lookup"><span data-stu-id="16319-121">The default value of the **ExcelUdfsAllowed** flag is false.</span></span> 
  
<span data-ttu-id="16319-122">Чтобы включить UDF, выполните следующую команду Windows PowerShell на сервере Office Online Server после создания фермы серверов Office Web Apps.</span><span class="sxs-lookup"><span data-stu-id="16319-122">To enable UDFs, run the following Windows PowerShell command on the Office Online Server, after the Office Web Apps Server farm has been created.</span></span>
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a><span data-ttu-id="16319-123">Создание определений UDF в Office Online Server</span><span class="sxs-lookup"><span data-stu-id="16319-123">Create UDF definitions on Office Online Server</span></span>

<span data-ttu-id="16319-124">После включения UDF необходимо создать определение двоичного файла, содержащего пользовательские функции.</span><span class="sxs-lookup"><span data-stu-id="16319-124">After you enable UDFs, you need to create a definition for the binary that contains the UDFs.</span></span> <span data-ttu-id="16319-125">Чтобы создать определение для двоичной функции UDF на сервере Office Online Server, используйте командлет **New-оффицевебаппсексцелусердефинедфунктион** .</span><span class="sxs-lookup"><span data-stu-id="16319-125">To create a definition for your UDF binary on the Office Online Server, use the **New-OfficeWebAppsExcelUserDefinedFunction** cmdlet.</span></span> <span data-ttu-id="16319-126">Этот командлет включает следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="16319-126">This cmdlet includes the following parameters:</span></span> 
  
- <span data-ttu-id="16319-127">**Сборок**</span><span class="sxs-lookup"><span data-stu-id="16319-127">**Assembly**</span></span>
    
- <span data-ttu-id="16319-128">**Ассемблилокатион**</span><span class="sxs-lookup"><span data-stu-id="16319-128">**AssemblyLocation**</span></span>
    
- <span data-ttu-id="16319-129">**Включение** (по умолчанию задано значение false)</span><span class="sxs-lookup"><span data-stu-id="16319-129">**Enable** (set to False by default)</span></span> 
    
- <span data-ttu-id="16319-130">**Описание**</span><span class="sxs-lookup"><span data-stu-id="16319-130">**Description**</span></span>
    
<span data-ttu-id="16319-131">В следующих примерах показано, как создать определения UDF.</span><span class="sxs-lookup"><span data-stu-id="16319-131">The following examples show how create the UDF definitions.</span></span>
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
<span data-ttu-id="16319-132">После создания новой ссылки на UDF запустите **iisreset** на сервере для немедленного получения ссылки.</span><span class="sxs-lookup"><span data-stu-id="16319-132">After you create the new UDF reference, run **iisreset** on the server to pick up the reference immediately.</span></span> 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a><span data-ttu-id="16319-133">Дополнительные команды Windows PowerShell для UDF на сервере Office Online Server</span><span class="sxs-lookup"><span data-stu-id="16319-133">Additional Office Online Server UDF Windows PowerShell commands</span></span>

<span data-ttu-id="16319-134">Используйте следующие командлеты Windows PowerShell для работы с UDF:</span><span class="sxs-lookup"><span data-stu-id="16319-134">Use the following Windows PowerShell cmdlets to work with UDFs:</span></span>
  
- <span data-ttu-id="16319-135">**Get — оффицевебаппсексцелусердефинедфунктион** (нет обязательных параметров) — возвращает список определений UDF, настроенных на сервере Office Online Server.</span><span class="sxs-lookup"><span data-stu-id="16319-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (no required parameters) - Returns a list of UDF definitions that are configured on the Office Online Server.</span></span> 
    
- <span data-ttu-id="16319-136">**Set — оффицевебаппсексцелусердефинедфунктион** (Обязательный параметр Identity) — задает свойства существующих определений UDF.</span><span class="sxs-lookup"><span data-stu-id="16319-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Sets properties on existing UDF definitions.</span></span> 
    
- <span data-ttu-id="16319-137">**Remove — оффицевебаппсексцелусердефинедфунктион** (Обязательный параметр Identity) — удаляет существующие определения UDF.</span><span class="sxs-lookup"><span data-stu-id="16319-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Removes existing UDF definitions.</span></span> 
    
## <a name="udf-sample"></a><span data-ttu-id="16319-138">Пример использования UDF</span><span class="sxs-lookup"><span data-stu-id="16319-138">UDF sample</span></span>

<span data-ttu-id="16319-139">В следующих файлах представлена пример книги, в которой используется UDF и двоичный файл UDF:</span><span class="sxs-lookup"><span data-stu-id="16319-139">The following files provide a sample workbook that uses a UDF and the UDF binary:</span></span>
  
- <span data-ttu-id="16319-140">[Булеандататипе. xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): образец книги, ИСПОЛЬЗУЮЩей UDF</span><span class="sxs-lookup"><span data-stu-id="16319-140">[BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): a sample workbook that uses a UDF</span></span>  
- <span data-ttu-id="16319-141">[Ексудфскоммонсет. dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): двоичный файл UDF</span><span class="sxs-lookup"><span data-stu-id="16319-141">[EcsUdfsCommonSet.dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): the UDF binary</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="16319-142">См. также</span><span class="sxs-lookup"><span data-stu-id="16319-142">See also</span></span>

- [<span data-ttu-id="16319-143">Настройка параметров администрирования Excel Online</span><span class="sxs-lookup"><span data-stu-id="16319-143">Configure Excel Online administrative settings</span></span>](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [<span data-ttu-id="16319-144">Office Online Server</span><span class="sxs-lookup"><span data-stu-id="16319-144">Office Online Server</span></span>](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

