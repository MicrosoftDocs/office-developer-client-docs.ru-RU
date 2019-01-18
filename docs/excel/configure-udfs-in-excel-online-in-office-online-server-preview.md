---
title: Настройка пользовательских функций в Excel Online в Office Online Server
manager: soliver
ms.date: 03/18/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Используйте пользовательские функции (UDF) в Excel Online в Office Online Server для вызова пользовательских функций.
ms.openlocfilehash: dbba60a62a1a4783b47c3f1fe40a118dd8ed0d6d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722790"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a><span data-ttu-id="d1e32-103">Настройка пользовательских функций в Excel Online в Office Online Server</span><span class="sxs-lookup"><span data-stu-id="d1e32-103">Configure UDFs in Excel Online in Office Online Server</span></span>

<span data-ttu-id="d1e32-104">Используйте пользовательские функции (UDF) в Excel Online в Office Online Server для вызова пользовательских функций.</span><span class="sxs-lookup"><span data-stu-id="d1e32-104">Use user-defined functions (UDFs) in Excel Online in Office Online Server to call custom functions.</span></span> 
  
<span data-ttu-id="d1e32-105">Пользовательские функции (UDF) в Excel Online дают возможность вызова пользовательских функций, написанных в управляемом коде с помощью формулы в ячейках.</span><span class="sxs-lookup"><span data-stu-id="d1e32-105">User-defined functions (UDFs) in Excel Online enable you to call custom functions written in managed code by using formulas in cells.</span></span> <span data-ttu-id="d1e32-106">Вы можете использовать пользовательских функций:</span><span class="sxs-lookup"><span data-stu-id="d1e32-106">You can use UDFs to:</span></span>
  
- <span data-ttu-id="d1e32-107">вызова специальных математических функций;</span><span class="sxs-lookup"><span data-stu-id="d1e32-107">Call custom mathematical functions.</span></span>
    
- <span data-ttu-id="d1e32-108">загрузки на листы данных из специальных источников;</span><span class="sxs-lookup"><span data-stu-id="d1e32-108">Get data from custom data sources into worksheets.</span></span>
    
- <span data-ttu-id="d1e32-109">Вызов веб-служб.</span><span class="sxs-lookup"><span data-stu-id="d1e32-109">Call web services.</span></span>
    
<span data-ttu-id="d1e32-110">Можно установить двоичные файлы пользовательских Функций в одном из двух местоположений:</span><span class="sxs-lookup"><span data-stu-id="d1e32-110">You can install UDF binaries in one of two locations:</span></span>
  
- <span data-ttu-id="d1e32-111">Локальный каталог.</span><span class="sxs-lookup"><span data-stu-id="d1e32-111">A local directory.</span></span> <span data-ttu-id="d1e32-112">Пример:</span><span class="sxs-lookup"><span data-stu-id="d1e32-112">For example:</span></span> 
    
    <span data-ttu-id="d1e32-113">C:\UDFs\MySampleUdf.dll </span><span class="sxs-lookup"><span data-stu-id="d1e32-113">C:\UDFs\MySampleUdf.dll</span></span>
    
- <span data-ttu-id="d1e32-114">В глобальном кэше сборок.</span><span class="sxs-lookup"><span data-stu-id="d1e32-114">The global assembly cache.</span></span> <span data-ttu-id="d1e32-115">Пример:</span><span class="sxs-lookup"><span data-stu-id="d1e32-115">For example:</span></span> 
    
    <span data-ttu-id="d1e32-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span><span class="sxs-lookup"><span data-stu-id="d1e32-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span></span>
    
<span data-ttu-id="d1e32-117">Справочник по месту при создании определения **New-OfficeWebAppsExcelUserDefinedFunction** на сервере Office Online.</span><span class="sxs-lookup"><span data-stu-id="d1e32-117">Reference the location when you create a **New-OfficeWebAppsExcelUserDefinedFunction** definition on the Office Online Server.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d1e32-118">Office Online Server не поддерживает пользовательских функций, расположенных в сетевых папках.</span><span class="sxs-lookup"><span data-stu-id="d1e32-118">Office Online Server does not support UDFs located on network shares.</span></span> 
  
## <a name="enable-udfs-on-office-online-server"></a><span data-ttu-id="d1e32-119">Включение пользовательских функций на сервере Office Online</span><span class="sxs-lookup"><span data-stu-id="d1e32-119">Enable UDFs on Office Online Server</span></span> 

<span data-ttu-id="d1e32-120">Когда администратор создает новую ферму сервера Office Web Apps с помощью командлета [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell, по умолчанию отключены сборки пользовательских Функций.</span><span class="sxs-lookup"><span data-stu-id="d1e32-120">When an adminstrator creates a new Office Web Apps Server farm by using the [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell cmdlet, UDF assemblies are disabled by default.</span></span> <span data-ttu-id="d1e32-121">Значение по умолчанию флаг **ExcelUdfsAllowed** имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="d1e32-121">The default value of the **ExcelUdfsAllowed** flag is false.</span></span> 
  
<span data-ttu-id="d1e32-122">Включение пользовательских функций, выполните следующую команду Windows PowerShell на сервере Office Online, после создания фермы сервера Office Web Apps.</span><span class="sxs-lookup"><span data-stu-id="d1e32-122">To enable UDFs, run the following Windows PowerShell command on the Office Online Server, after the Office Web Apps Server farm has been created.</span></span>
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a><span data-ttu-id="d1e32-123">Создание определений пользовательских Функций на сервере Office Online</span><span class="sxs-lookup"><span data-stu-id="d1e32-123">Create UDF definitions on Office Online Server</span></span>

<span data-ttu-id="d1e32-124">После включения пользовательских функций, необходимо создать определение двоичный файл, содержащий пользовательских функций.</span><span class="sxs-lookup"><span data-stu-id="d1e32-124">After you enable UDFs, you need to create a definition for the binary that contains the UDFs.</span></span> <span data-ttu-id="d1e32-125">Для создания определения для вашей UDF двоичные на сервере Office Online, используйте командлет **New-OfficeWebAppsExcelUserDefinedFunction** .</span><span class="sxs-lookup"><span data-stu-id="d1e32-125">To create a definition for your UDF binary on the Office Online Server, use the **New-OfficeWebAppsExcelUserDefinedFunction** cmdlet.</span></span> <span data-ttu-id="d1e32-126">Этот командлет включает в себя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="d1e32-126">This cmdlet includes the following parameters:</span></span> 
  
- <span data-ttu-id="d1e32-127">**Сборки**</span><span class="sxs-lookup"><span data-stu-id="d1e32-127">**Assembly**</span></span>
    
- <span data-ttu-id="d1e32-128">**Расположение_сборки**</span><span class="sxs-lookup"><span data-stu-id="d1e32-128">**AssemblyLocation**</span></span>
    
- <span data-ttu-id="d1e32-129">**Включение** (присвоено значение False, по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d1e32-129">**Enable** (set to False by default)</span></span> 
    
- <span data-ttu-id="d1e32-130">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d1e32-130">**Description**</span></span>
    
<span data-ttu-id="d1e32-131">В следующем примере показано, как создать определения пользовательских Функций.</span><span class="sxs-lookup"><span data-stu-id="d1e32-131">The following examples show how create the UDF definitions.</span></span>
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
<span data-ttu-id="d1e32-132">После создания новой ссылки UDF, выполните **команду iisreset** на сервере для сбора ссылки сразу же.</span><span class="sxs-lookup"><span data-stu-id="d1e32-132">After you create the new UDF reference, run **iisreset** on the server to pick up the reference immediately.</span></span> 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a><span data-ttu-id="d1e32-133">Дополнительные команды Office Online Server UDF Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d1e32-133">Additional Office Online Server UDF Windows PowerShell commands</span></span>

<span data-ttu-id="d1e32-134">Используйте следующие командлеты Windows PowerShell для работы с помощью пользовательских функций:</span><span class="sxs-lookup"><span data-stu-id="d1e32-134">Use the following Windows PowerShell cmdlets to work with UDFs:</span></span>
  
- <span data-ttu-id="d1e32-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (без обязательных параметров) — возвращает список определений пользовательских Функций, которые настроены на сервере Office Online.</span><span class="sxs-lookup"><span data-stu-id="d1e32-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (no required parameters) - Returns a list of UDF definitions that are configured on the Office Online Server.</span></span> 
    
- <span data-ttu-id="d1e32-136">**Set-OfficeWebAppsExcelUserDefinedFunction** (Параметра identity требуется) - задаются свойства существующего определения пользовательских Функций.</span><span class="sxs-lookup"><span data-stu-id="d1e32-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Sets properties on existing UDF definitions.</span></span> 
    
- <span data-ttu-id="d1e32-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Параметра identity требуется) — удаляет существующие определения пользовательских Функций.</span><span class="sxs-lookup"><span data-stu-id="d1e32-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Removes existing UDF definitions.</span></span> 
    
## <a name="udf-sample"></a><span data-ttu-id="d1e32-138">Пример пользовательских Функций</span><span class="sxs-lookup"><span data-stu-id="d1e32-138">UDF sample</span></span>

<span data-ttu-id="d1e32-139">Следующие файлы содержат пример книги с использованием пользовательской функции и двоичные UDF.</span><span class="sxs-lookup"><span data-stu-id="d1e32-139">The following files provide a sample workbook that uses a UDF and the UDF binary:</span></span>
  
- <span data-ttu-id="d1e32-140">[BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): пример книги, с помощью пользовательской функции</span><span class="sxs-lookup"><span data-stu-id="d1e32-140">[BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): a sample workbook that uses a UDF</span></span>  
- <span data-ttu-id="d1e32-141">[EcsUdfsCommonSet.dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): двоичный пользовательских Функций</span><span class="sxs-lookup"><span data-stu-id="d1e32-141">[EcsUdfsCommonSet.dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): the UDF binary</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d1e32-142">См. также</span><span class="sxs-lookup"><span data-stu-id="d1e32-142">See also</span></span>

- [<span data-ttu-id="d1e32-143">Настройка Excel Online административных параметров</span><span class="sxs-lookup"><span data-stu-id="d1e32-143">Configure Excel Online administrative settings</span></span>](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [<span data-ttu-id="d1e32-144">Office Online Server</span><span class="sxs-lookup"><span data-stu-id="d1e32-144">Office Online Server</span></span>](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

