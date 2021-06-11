---
title: Настройка UDF в Excel Online в Office Online Server
manager: lindalu
ms.date: 12/03/2019
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Используйте пользовательские функции (UDF) в Excel Online в Office Online Server для вызова пользовательских функций.
ms.openlocfilehash: e1b005079c03ae3028ba6bf9ee1156c6ae2eae80
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "43102935"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a><span data-ttu-id="92500-103">Настройка UDF в Excel Online в Office Online Server</span><span class="sxs-lookup"><span data-stu-id="92500-103">Configure UDFs in Excel Online in Office Online Server</span></span>

<span data-ttu-id="92500-104">Используйте пользовательские функции (UDF) в Excel Online в Office Online Server для вызова пользовательских функций.</span><span class="sxs-lookup"><span data-stu-id="92500-104">Use user-defined functions (UDFs) in Excel Online in Office Online Server to call custom functions.</span></span> 
  
<span data-ttu-id="92500-105">Пользовательские функции (UDF) в Excel Online позволяют вызывать настраиваемые функции, написанные в управляемом коде с помощью формул в ячейках.</span><span class="sxs-lookup"><span data-stu-id="92500-105">User-defined functions (UDFs) in Excel Online enable you to call custom functions written in managed code by using formulas in cells.</span></span> <span data-ttu-id="92500-106">Вы можете использовать UDFs для:</span><span class="sxs-lookup"><span data-stu-id="92500-106">You can use UDFs to:</span></span>
  
- <span data-ttu-id="92500-107">вызова специальных математических функций;</span><span class="sxs-lookup"><span data-stu-id="92500-107">Call custom mathematical functions.</span></span>
    
- <span data-ttu-id="92500-108">загрузки на листы данных из специальных источников;</span><span class="sxs-lookup"><span data-stu-id="92500-108">Get data from custom data sources into worksheets.</span></span>
    
- <span data-ttu-id="92500-109">Вызов веб-служб.</span><span class="sxs-lookup"><span data-stu-id="92500-109">Call web services.</span></span>
    
<span data-ttu-id="92500-110">Вы можете установить двоики UDF в одном из двух местоположений:</span><span class="sxs-lookup"><span data-stu-id="92500-110">You can install UDF binaries in one of two locations:</span></span>
  
- <span data-ttu-id="92500-111">Локальный каталог.</span><span class="sxs-lookup"><span data-stu-id="92500-111">A local directory.</span></span> <span data-ttu-id="92500-112">Пример.</span><span class="sxs-lookup"><span data-stu-id="92500-112">For example:</span></span> 
    
    <span data-ttu-id="92500-113">C:\UDFs\MySampleUdf.dll</span><span class="sxs-lookup"><span data-stu-id="92500-113">C:\UDFs\MySampleUdf.dll</span></span>
    
- <span data-ttu-id="92500-114">Кэш глобальной сборки.</span><span class="sxs-lookup"><span data-stu-id="92500-114">The global assembly cache.</span></span> <span data-ttu-id="92500-115">Пример.</span><span class="sxs-lookup"><span data-stu-id="92500-115">For example:</span></span> 
    
    <span data-ttu-id="92500-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span><span class="sxs-lookup"><span data-stu-id="92500-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span></span>
    
<span data-ttu-id="92500-117">Ссылка на расположение при создании **определения New-OfficeWebAppsExcelUserDefinedFunction** на Office Online Server.</span><span class="sxs-lookup"><span data-stu-id="92500-117">Reference the location when you create a **New-OfficeWebAppsExcelUserDefinedFunction** definition on the Office Online Server.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="92500-118">Office Online Server не поддерживает UDF, расположенные на сетевых акциях.</span><span class="sxs-lookup"><span data-stu-id="92500-118">Office Online Server does not support UDFs located on network shares.</span></span> 
  
## <a name="enable-udfs-on-office-online-server"></a><span data-ttu-id="92500-119">Включить UDF на Office Online Server</span><span class="sxs-lookup"><span data-stu-id="92500-119">Enable UDFs on Office Online Server</span></span> 

<span data-ttu-id="92500-120">Когда администратор создает новую ферму Office серверов веб-приложений с помощью командулета [New-OfficeWebAppsFarm](https://docs.microsoft.com/powershell/module/officewebapps/new-officewebappsfarm?view=officewebapps-ps) Windows PowerShell, сборки UDF отключены по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="92500-120">When an administrator creates a new Office Web Apps Server farm by using the [New-OfficeWebAppsFarm](https://docs.microsoft.com/powershell/module/officewebapps/new-officewebappsfarm?view=officewebapps-ps) Windows PowerShell cmdlet, UDF assemblies are disabled by default.</span></span> <span data-ttu-id="92500-121">Значение по умолчанию **флага ExcelUdfsAllowed** является ложным.</span><span class="sxs-lookup"><span data-stu-id="92500-121">The default value of the **ExcelUdfsAllowed** flag is false.</span></span> 
  
<span data-ttu-id="92500-122">Чтобы включить UDF, запустите следующую команду Windows PowerShell в Office Online Server после создания фермы Office веб-приложений Server.</span><span class="sxs-lookup"><span data-stu-id="92500-122">To enable UDFs, run the following Windows PowerShell command on the Office Online Server, after the Office Web Apps Server farm has been created.</span></span>
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a><span data-ttu-id="92500-123">Создание определений UDF на Office Online Server</span><span class="sxs-lookup"><span data-stu-id="92500-123">Create UDF definitions on Office Online Server</span></span>

<span data-ttu-id="92500-124">После того как вы включаете UDFs, необходимо создать определение для двоичного, который содержит UDFs.</span><span class="sxs-lookup"><span data-stu-id="92500-124">After you enable UDFs, you need to create a definition for the binary that contains the UDFs.</span></span> <span data-ttu-id="92500-125">Чтобы создать определение для двоичного двоичного файла UDF на Office Online Server, используйте комлет **New-OfficeWebAppsExcelUserDefinedFunction.**</span><span class="sxs-lookup"><span data-stu-id="92500-125">To create a definition for your UDF binary on the Office Online Server, use the **New-OfficeWebAppsExcelUserDefinedFunction** cmdlet.</span></span> <span data-ttu-id="92500-126">В этом комлете содержатся следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="92500-126">This cmdlet includes the following parameters:</span></span> 
  
- <span data-ttu-id="92500-127">**Assembly**</span><span class="sxs-lookup"><span data-stu-id="92500-127">**Assembly**</span></span>
    
- <span data-ttu-id="92500-128">**AssemblyLocation**</span><span class="sxs-lookup"><span data-stu-id="92500-128">**AssemblyLocation**</span></span>
    
- <span data-ttu-id="92500-129">**Включить** (установить значение False по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="92500-129">**Enable** (set to False by default)</span></span> 
    
- <span data-ttu-id="92500-130">**Описание**</span><span class="sxs-lookup"><span data-stu-id="92500-130">**Description**</span></span>
    
<span data-ttu-id="92500-131">В следующих примерах покажите, как создавать определения UDF.</span><span class="sxs-lookup"><span data-stu-id="92500-131">The following examples show how create the UDF definitions.</span></span>
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
<span data-ttu-id="92500-132">После создания новой ссылки UDF запустите **iisreset** на сервере, чтобы немедленно получить ссылку.</span><span class="sxs-lookup"><span data-stu-id="92500-132">After you create the new UDF reference, run **iisreset** on the server to pick up the reference immediately.</span></span> 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a><span data-ttu-id="92500-133">Дополнительные Office Online Server UDF Windows PowerShell команд</span><span class="sxs-lookup"><span data-stu-id="92500-133">Additional Office Online Server UDF Windows PowerShell commands</span></span>

<span data-ttu-id="92500-134">Используйте следующие Windows PowerShell для работы с UDFs:</span><span class="sxs-lookup"><span data-stu-id="92500-134">Use the following Windows PowerShell cmdlets to work with UDFs:</span></span>
  
- <span data-ttu-id="92500-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (без необходимых параметров) — возвращает список определений UDF, настроенных на Office Online Server.</span><span class="sxs-lookup"><span data-stu-id="92500-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (no required parameters) - Returns a list of UDF definitions that are configured on the Office Online Server.</span></span> 
    
- <span data-ttu-id="92500-136">**Set-OfficeWebAppsExcelUserDefinedFunction** (необходимый параметр identity) — задает свойства для существующих определений UDF.</span><span class="sxs-lookup"><span data-stu-id="92500-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Sets properties on existing UDF definitions.</span></span> 
    
- <span data-ttu-id="92500-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (необходимый параметр identity) — удаляет существующие определения UDF.</span><span class="sxs-lookup"><span data-stu-id="92500-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Removes existing UDF definitions.</span></span> 
    
## <a name="udf-sample"></a><span data-ttu-id="92500-138">Пример UDF</span><span class="sxs-lookup"><span data-stu-id="92500-138">UDF sample</span></span>

<span data-ttu-id="92500-139">В следующем примере файла приводится пример книги с использованием двоичного файла UDF и UDF:</span><span class="sxs-lookup"><span data-stu-id="92500-139">The following sample file provide a sample workbook that uses a UDF and the UDF binary:</span></span>
  
- <span data-ttu-id="92500-140">[BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): пример книги, использующей UDF</span><span class="sxs-lookup"><span data-stu-id="92500-140">[BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): a sample workbook that uses a UDF</span></span>  
    
## <a name="see-also"></a><span data-ttu-id="92500-141">См. также</span><span class="sxs-lookup"><span data-stu-id="92500-141">See also</span></span>

- [<span data-ttu-id="92500-142">Настройка параметров администрирования Excel Online</span><span class="sxs-lookup"><span data-stu-id="92500-142">Configure Excel Online administrative settings</span></span>](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [<span data-ttu-id="92500-143">Office Online Server</span><span class="sxs-lookup"><span data-stu-id="92500-143">Office Online Server</span></span>](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

