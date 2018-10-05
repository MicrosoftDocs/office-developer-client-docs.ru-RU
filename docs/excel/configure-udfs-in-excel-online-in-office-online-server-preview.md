---
title: Настройка пользовательских функций в Excel Online в Office Online Server Preview
manager: soliver
ms.date: 03/18/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Используйте пользовательские функции (UDF) в Excel Online в Office Online предварительной версии сервера для вызова пользовательских функций.
ms.openlocfilehash: 2b76b7351a0882762165e37b55c8fbe78f657c34
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384824"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server-preview"></a><span data-ttu-id="db270-103">Настройка пользовательских функций в Excel Online в Office Online Server Preview</span><span class="sxs-lookup"><span data-stu-id="db270-103">Configure UDFs in Excel Online in Office Online Server Preview</span></span>

<span data-ttu-id="db270-104">[Этот раздел предварительной документации и может быть изменен в будущих выпусках.] Используйте пользовательские функции (UDF) в Excel Online в Office Online предварительной версии сервера для вызова пользовательских функций.</span><span class="sxs-lookup"><span data-stu-id="db270-104">[This topic is pre-release documentation and is subject to change in future releases.] Use user-defined functions (UDFs) in Excel Online in Office Online Server Preview to call custom functions.</span></span> 
  
<span data-ttu-id="db270-105">Пользовательские функции (UDF) в Excel Online дают возможность вызова пользовательских функций, написанных в управляемом коде с помощью формулы в ячейках.</span><span class="sxs-lookup"><span data-stu-id="db270-105">User-defined functions (UDFs) in Excel Online enable you to call custom functions written in managed code by using formulas in cells.</span></span> <span data-ttu-id="db270-106">Вы можете использовать пользовательских функций:</span><span class="sxs-lookup"><span data-stu-id="db270-106">You can use UDFs to:</span></span>
  
- <span data-ttu-id="db270-107">Call custom mathematical functions.</span><span class="sxs-lookup"><span data-stu-id="db270-107">Call custom mathematical functions.</span></span>
    
- <span data-ttu-id="db270-108">Get data from custom data sources into worksheets.</span><span class="sxs-lookup"><span data-stu-id="db270-108">Get data from custom data sources into worksheets.</span></span>
    
- <span data-ttu-id="db270-109">Вызов веб-служб.</span><span class="sxs-lookup"><span data-stu-id="db270-109">Call web services.</span></span>
    
<span data-ttu-id="db270-110">Можно установить двоичные файлы пользовательских Функций в одном из двух местоположений:</span><span class="sxs-lookup"><span data-stu-id="db270-110">You can install UDF binaries in one of two locations:</span></span>
  
- <span data-ttu-id="db270-111">Локальный каталог.</span><span class="sxs-lookup"><span data-stu-id="db270-111">A local directory.</span></span> <span data-ttu-id="db270-112">Пример:</span><span class="sxs-lookup"><span data-stu-id="db270-112">For example:</span></span> 
    
    <span data-ttu-id="db270-113">C:\UDFs\MySampleUdf.dll </span><span class="sxs-lookup"><span data-stu-id="db270-113">C:\UDFs\MySampleUdf.dll</span></span>
    
- <span data-ttu-id="db270-114">В глобальном кэше сборок.</span><span class="sxs-lookup"><span data-stu-id="db270-114">The global assembly cache.</span></span> <span data-ttu-id="db270-115">Пример:</span><span class="sxs-lookup"><span data-stu-id="db270-115">For example:</span></span> 
    
    <span data-ttu-id="db270-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span><span class="sxs-lookup"><span data-stu-id="db270-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span></span>
    
<span data-ttu-id="db270-117">Ссылка на расположение при создании определения **New-OfficeWebAppsExcelUserDefinedFunction** в предварительной версии Microsoft Office Online Server.</span><span class="sxs-lookup"><span data-stu-id="db270-117">Reference the location when you create a **New-OfficeWebAppsExcelUserDefinedFunction** definition on the Office Online Server Preview.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="db270-118">Предварительная версия сервера Office Online не поддерживает пользовательских функций, расположенных в сетевых папках.</span><span class="sxs-lookup"><span data-stu-id="db270-118">Office Online Server Preview does not support UDFs located on network shares.</span></span> 
  
## <a name="enable-udfs-on-office-online-server-preview"></a><span data-ttu-id="db270-119">Включение пользовательских функций в предварительной версии Microsoft Office Online Server</span><span class="sxs-lookup"><span data-stu-id="db270-119">Enable UDFs on Office Online Server Preview</span></span>

<span data-ttu-id="db270-120">Когда администратор создает новую ферму сервера Office Web Apps с помощью командлета [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell, по умолчанию отключены сборки пользовательских Функций.</span><span class="sxs-lookup"><span data-stu-id="db270-120">When an adminstrator creates a new Office Web Apps Server farm by using the [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell cmdlet, UDF assemblies are disabled by default.</span></span> <span data-ttu-id="db270-121">Значение по умолчанию флаг **ExcelUdfsAllowed** имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="db270-121">The default value of the **ExcelUdfsAllowed** flag is false.</span></span> 
  
<span data-ttu-id="db270-122">Включение пользовательских функций, выполните следующую команду Windows PowerShell на Office Online Server предварительного просмотра, после создания фермы сервера Office Web Apps.</span><span class="sxs-lookup"><span data-stu-id="db270-122">To enable UDFs, run the following Windows PowerShell command on the Office Online Server Preview, after the Office Web Apps Server farm has been created.</span></span>
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server-preview"></a><span data-ttu-id="db270-123">Создание определений пользовательских Функций на Предварительная версия сервера Office Online</span><span class="sxs-lookup"><span data-stu-id="db270-123">Create UDF definitions on Office Online Server Preview</span></span>

<span data-ttu-id="db270-124">После включения пользовательских функций, необходимо создать определение двоичный файл, содержащий пользовательских функций.</span><span class="sxs-lookup"><span data-stu-id="db270-124">After you enable UDFs, you need to create a definition for the binary that contains the UDFs.</span></span> <span data-ttu-id="db270-125">Для создания определения для вашей UDF двоичные на Office Online Server Preview, используйте командлет **New-OfficeWebAppsExcelUserDefinedFunction** .</span><span class="sxs-lookup"><span data-stu-id="db270-125">To create a definition for your UDF binary on the Office Online Server Preview, use the **New-OfficeWebAppsExcelUserDefinedFunction** cmdlet.</span></span> <span data-ttu-id="db270-126">Этот командлет включает в себя следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="db270-126">This cmdlet includes the following parameters:</span></span> 
  
- <span data-ttu-id="db270-127">**Сборки**</span><span class="sxs-lookup"><span data-stu-id="db270-127">**Assembly**</span></span>
    
- <span data-ttu-id="db270-128">**Расположение_сборки**</span><span class="sxs-lookup"><span data-stu-id="db270-128">**AssemblyLocation**</span></span>
    
- <span data-ttu-id="db270-129">**Включение** (присвоено значение False, по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="db270-129">**Enable** (set to False by default)</span></span> 
    
- <span data-ttu-id="db270-130">**Описание**</span><span class="sxs-lookup"><span data-stu-id="db270-130">**Description**</span></span>
    
<span data-ttu-id="db270-131">В следующем примере показано, как создать определения пользовательских Функций.</span><span class="sxs-lookup"><span data-stu-id="db270-131">The following examples show how create the UDF definitions.</span></span>
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
<span data-ttu-id="db270-132">После создания новой ссылки UDF, выполните **команду iisreset** на сервере для сбора ссылки сразу же.</span><span class="sxs-lookup"><span data-stu-id="db270-132">After you create the new UDF reference, run **iisreset** on the server to pick up the reference immediately.</span></span> 
  
## <a name="additional-office-online-server-preview-udf-windows-powershell-commands"></a><span data-ttu-id="db270-133">Дополнительные команды Office Online Server Preview UDF Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="db270-133">Additional Office Online Server Preview UDF Windows PowerShell commands</span></span>

<span data-ttu-id="db270-134">Используйте следующие командлеты Windows PowerShell для работы с помощью пользовательских функций:</span><span class="sxs-lookup"><span data-stu-id="db270-134">Use the following Windows PowerShell cmdlets to work with UDFs:</span></span>
  
- <span data-ttu-id="db270-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (без обязательных параметров) — возвращает список определений пользовательских Функций, которые будут настроены для предварительной версии Office Online Server.</span><span class="sxs-lookup"><span data-stu-id="db270-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (no required parameters) - Returns a list of UDF definitions that are configured on the Office Online Server Preview.</span></span> 
    
- <span data-ttu-id="db270-136">**Set-OfficeWebAppsExcelUserDefinedFunction** (Параметра identity требуется) - задаются свойства существующего определения пользовательских Функций.</span><span class="sxs-lookup"><span data-stu-id="db270-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Sets properties on existing UDF definitions.</span></span> 
    
- <span data-ttu-id="db270-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Параметра identity требуется) — удаляет существующие определения пользовательских Функций.</span><span class="sxs-lookup"><span data-stu-id="db270-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Removes existing UDF definitions.</span></span> 
    
## <a name="udf-sample"></a><span data-ttu-id="db270-138">Пример пользовательских Функций</span><span class="sxs-lookup"><span data-stu-id="db270-138">UDF sample</span></span>

<span data-ttu-id="db270-139">Следующие файлы содержат пример книги с использованием пользовательской функции и двоичные UDF.</span><span class="sxs-lookup"><span data-stu-id="db270-139">The following files provide a sample workbook that uses a UDF and the UDF binary:</span></span>
  
- <span data-ttu-id="db270-140">[BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx) — пример книги, с помощью пользовательской функции</span><span class="sxs-lookup"><span data-stu-id="db270-140">[BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx) -- a sample workbook that uses a UDF</span></span>  
- <span data-ttu-id="db270-141">[EcsUdfsCommonSet.dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll) --двоичный пользовательских Функций</span><span class="sxs-lookup"><span data-stu-id="db270-141">[EcsUdfsCommonSet.dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll) -- the UDF binary</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="db270-142">См. также</span><span class="sxs-lookup"><span data-stu-id="db270-142">See also</span></span>

- [<span data-ttu-id="db270-143">Настройка Excel Online административных параметров</span><span class="sxs-lookup"><span data-stu-id="db270-143">Configure Excel Online administrative settings</span></span>](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [<span data-ttu-id="db270-144">Office Online Server</span><span class="sxs-lookup"><span data-stu-id="db270-144">Office Online Server</span></span>](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

