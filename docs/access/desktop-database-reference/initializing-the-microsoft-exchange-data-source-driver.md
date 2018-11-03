---
title: Инициализация драйвера источника данных Microsoft Exchange
TOCTitle: Initializing the Microsoft Exchange Data Source Driver
ms:assetid: cf87a746-f846-1a01-f4ec-20a25e335193
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834677(v=office.15)
ms:contentKeyID: 48547810
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032667
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6e1d61d2f61050118745347441cba1f27c35c41f
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937745"
---
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a><span data-ttu-id="bd1b0-102">Инициализация драйвера источника данных Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="bd1b0-102">Initializing the Microsoft Exchange Data Source Driver</span></span>

<span data-ttu-id="bd1b0-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd1b0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bd1b0-104">При установке драйвера источника данных Microsoft Exchange, программа установки записывает набор значений по умолчанию реестра Microsoft Windows в подразделы обработчики и ISAM Formats.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-104">When you install the Microsoft Exchange Data Source driver, the Setup program writes a set of default values to the Microsoft Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="bd1b0-105">Не изменяйте эти параметры напрямую; для добавления, удаления или изменения этих параметров с помощью программы установки для приложения.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="bd1b0-106">В следующих разделах инициализации и параметров ISAM Format драйвера источника данных Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-106">The following sections describe initialization and ISAM Format settings for the Microsoft Exchange Data Source driver.</span></span>

## <a name="microsoft-exchange-data-source-initialization-settings"></a><span data-ttu-id="bd1b0-107">Параметры инициализации источника данных Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="bd1b0-107">Microsoft Exchange Data Source Initialization Settings</span></span>

<span data-ttu-id="bd1b0-108">**Модуль подключения к Access\\обработчики\\Exchange** папка содержит параметры инициализации для драйвера Aceexch.dll, который используется для внешнего доступа к папкам Microsoft Outlook и Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-108">The **Access Connectivity Engine\\Engines\\Exchange** folder includes initialization settings for the Aceexch.dll driver, used for external access to Microsoft Outlook and Microsoft Exchange folders.</span></span> <span data-ttu-id="bd1b0-109">Единственная запись в этой папке выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bd1b0-109">The only entry in this folder is the following:</span></span>

`win32=<path>\ACEEXCH.DLL`

<span data-ttu-id="bd1b0-110">Ядро базы данных Microsoft Access использует этот параметр для указания расположения Aceexch.dll.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-110">The Microsoft Access database engine uses this setting to indicate the location of Aceexch.dll.</span></span> <span data-ttu-id="bd1b0-111">Полный путь определяется во время установки.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-111">The full path is determined at the time of installation.</span></span> <span data-ttu-id="bd1b0-112">Тип Реестра значений —\_SZ.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-112">Values are of type REG\_SZ.</span></span>

<span data-ttu-id="bd1b0-113">Результаты использования формата Outlook ISAM и использования формата ISAM клиента Exchange похожи.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-113">The results of using the Outlook ISAM format and of using the Exchange client ISAM format are similar.</span></span> <span data-ttu-id="bd1b0-114">Единственное отличие заключается в том, что два разных клиента используют разные имена для одного столбца.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-114">The only difference is that the two different clients use different names for the same columns.</span></span> <span data-ttu-id="bd1b0-115">Два формата ISAM были созданы, чтобы ядро базы данных Microsoft Access может вернуть имена столбцов в виде, который определит пользователь.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-115">The two ISAM formats have been created so that the Microsoft Access database engine can return the column names in the particular style that the user desires.</span></span>

## <a name="microsoft-outlook-client-isam-formats"></a><span data-ttu-id="bd1b0-116">Форматы ISAM клиента Microsoft Outlook</span><span class="sxs-lookup"><span data-stu-id="bd1b0-116">Microsoft Outlook Client ISAM Formats</span></span>

<span data-ttu-id="bd1b0-117">**Модуль подключения к Access\\ISAM Formats\\Outlook 9.0** папка содержит следующие записи.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-117">The **Access Connectivity Engine\\ISAM Formats\\Outlook 9.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bd1b0-118">Имя записи</span><span class="sxs-lookup"><span data-stu-id="bd1b0-118">Entry name</span></span></p></th>
<th><p><span data-ttu-id="bd1b0-119">Тип</span><span class="sxs-lookup"><span data-stu-id="bd1b0-119">Type</span></span></p></th>
<th><p><span data-ttu-id="bd1b0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="bd1b0-120">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd1b0-121">Модуль</span><span class="sxs-lookup"><span data-stu-id="bd1b0-121">Engine</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-122">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bd1b0-122">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-123">Exchange</span><span class="sxs-lookup"><span data-stu-id="bd1b0-123">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd1b0-124">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="bd1b0-124">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-125">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bd1b0-125">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-126">Outlook()</span><span class="sxs-lookup"><span data-stu-id="bd1b0-126">Outlook()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd1b0-127">CanLink</span><span class="sxs-lookup"><span data-stu-id="bd1b0-127">CanLink</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-128">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd1b0-128">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-129">01</span><span class="sxs-lookup"><span data-stu-id="bd1b0-129">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd1b0-130">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="bd1b0-130">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-131">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd1b0-131">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-132">00</span><span class="sxs-lookup"><span data-stu-id="bd1b0-132">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd1b0-133">IsamType</span><span class="sxs-lookup"><span data-stu-id="bd1b0-133">IsamType</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-134">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="bd1b0-134">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-135">3</span><span class="sxs-lookup"><span data-stu-id="bd1b0-135">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd1b0-136">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="bd1b0-136">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-137">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd1b0-137">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-138">00</span><span class="sxs-lookup"><span data-stu-id="bd1b0-138">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd1b0-139">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="bd1b0-139">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-140">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd1b0-140">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-141">00</span><span class="sxs-lookup"><span data-stu-id="bd1b0-141">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd1b0-142">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="bd1b0-142">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-143">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd1b0-143">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-144">01</span><span class="sxs-lookup"><span data-stu-id="bd1b0-144">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="bd1b0-145">При изменении параметров реестра Windows, необходимо выйти из и перезапустить ядро базы данных для новых параметров вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-145">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="microsoft-exchange-client-isam-formats"></a><span data-ttu-id="bd1b0-146">Форматы ISAM клиента Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="bd1b0-146">Microsoft Exchange Client ISAM Formats</span></span>

<span data-ttu-id="bd1b0-147">**Модуль подключения к Access\\ISAM Formats\\Exchange 4.0** папка содержит следующие записи.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-147">The **Access Connectivity Engine\\ISAM Formats\\Exchange 4.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bd1b0-148">Имя записи</span><span class="sxs-lookup"><span data-stu-id="bd1b0-148">Entry name</span></span></p></th>
<th><p><span data-ttu-id="bd1b0-149">Тип</span><span class="sxs-lookup"><span data-stu-id="bd1b0-149">Type</span></span></p></th>
<th><p><span data-ttu-id="bd1b0-150">Значение</span><span class="sxs-lookup"><span data-stu-id="bd1b0-150">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd1b0-151">Модуль</span><span class="sxs-lookup"><span data-stu-id="bd1b0-151">Engine</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-152">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bd1b0-152">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-153">Exchange</span><span class="sxs-lookup"><span data-stu-id="bd1b0-153">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd1b0-154">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="bd1b0-154">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-155">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bd1b0-155">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-156">Exchange()</span><span class="sxs-lookup"><span data-stu-id="bd1b0-156">Exchange()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd1b0-157">CanLink</span><span class="sxs-lookup"><span data-stu-id="bd1b0-157">CanLink</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-158">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd1b0-158">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-159">01</span><span class="sxs-lookup"><span data-stu-id="bd1b0-159">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd1b0-160">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="bd1b0-160">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-161">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd1b0-161">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-162">00</span><span class="sxs-lookup"><span data-stu-id="bd1b0-162">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd1b0-163">IsamType</span><span class="sxs-lookup"><span data-stu-id="bd1b0-163">IsamType</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-164">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="bd1b0-164">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-165">3</span><span class="sxs-lookup"><span data-stu-id="bd1b0-165">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd1b0-166">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="bd1b0-166">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-167">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd1b0-167">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-168">00</span><span class="sxs-lookup"><span data-stu-id="bd1b0-168">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd1b0-169">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="bd1b0-169">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-170">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd1b0-170">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-171">00</span><span class="sxs-lookup"><span data-stu-id="bd1b0-171">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd1b0-172">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="bd1b0-172">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-173">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd1b0-173">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd1b0-174">01</span><span class="sxs-lookup"><span data-stu-id="bd1b0-174">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="bd1b0-175">При изменении параметров реестра Windows, необходимо выйти из и перезапустить ядро базы данных для новых параметров вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-175">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a><span data-ttu-id="bd1b0-176">Настройка файла Schema.ini для Outlook и данных Exchange</span><span class="sxs-lookup"><span data-stu-id="bd1b0-176">Customizing the Schema.ini File for Outlook and Exchange Data</span></span>

<span data-ttu-id="bd1b0-177">Файл Schema.ini используется Outlook и Exchange ISAM точно так же, как он используется в ISAM текста.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-177">The Schema.ini file is used by the Outlook and Exchange ISAM in much the same way that it is used by the Text ISAM.</span></span> <span data-ttu-id="bd1b0-178">Этот файл содержит особенности источника данных: формат данных и имена столбцов, которые должны быть доступны.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-178">Schema.ini contains the specifics of a data source: how the data is formatted, and the names of columns that should be accessed.</span></span>

<span data-ttu-id="bd1b0-179">Измените файл Schema.ini перед данных можно прочитать, импортируемые или экспортируемые для Outlook и Exchange необязательно.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-179">It is not necessary to modify the Schema.ini file before data can be read, imported, or exported for Outlook and Exchange.</span></span> <span data-ttu-id="bd1b0-180">Многие из параметров в файле Schema.ini для Outlook и Exchange специфичны для внутренних тегов, которые требуется MAPI.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-180">Many of the settings inside the Schema.ini file for Outlook and Exchange are specific to internal tags that MAPI requires.</span></span> <span data-ttu-id="bd1b0-181">Не следует пытаться изменить значения этих тегов.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-181">You should not attempt to modify those tag values.</span></span>

