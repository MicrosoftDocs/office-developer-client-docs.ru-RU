---
title: Инициализация драйвера источника данных Microsoft Exchange
TOCTitle: Initializing the Microsoft Exchange Data Source driver
ms:assetid: cf87a746-f846-1a01-f4ec-20a25e335193
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834677(v=office.15)
ms:contentKeyID: 48547810
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032667
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b3460786785ae7b21184b6d96384ecc59e89d287
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291409"
---
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a><span data-ttu-id="6cd76-102">Инициализация драйвера источника данных Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="6cd76-102">Initializing the Microsoft Exchange Data Source driver</span></span>

<span data-ttu-id="6cd76-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6cd76-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6cd76-104">При установке драйвера источника данных Microsoft Exchange программа установки записывает набор значений по умолчанию в реестр Microsoft Windows в подразделах Engines и ISAM formats.</span><span class="sxs-lookup"><span data-stu-id="6cd76-104">When you install the Microsoft Exchange Data Source driver, the Setup program writes a set of default values to the Microsoft Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="6cd76-105">Эти параметры не следует изменять напрямую; Используйте программу установки приложения, чтобы добавлять, удалять или изменять эти параметры.</span><span class="sxs-lookup"><span data-stu-id="6cd76-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="6cd76-106">В следующих разделах описываются параметры инициализации и ISAM Format для драйвера источника данных Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="6cd76-106">The following sections describe initialization and ISAM Format settings for the Microsoft Exchange Data Source driver.</span></span>

## <a name="microsoft-exchange-data-source-initialization-settings"></a><span data-ttu-id="6cd76-107">Параметры инициализации источника данных Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="6cd76-107">Microsoft Exchange data source initialization settings</span></span>

<span data-ttu-id="6cd76-108">Папка **\\Exchange Engine Engines Engine\\** включает параметры инициализации для драйвера ацеексч. dll, используемого для внешнего доступа к папкам Microsoft Outlook и Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="6cd76-108">The **Access Connectivity Engine\\Engines\\Exchange** folder includes initialization settings for the Aceexch.dll driver, used for external access to Microsoft Outlook and Microsoft Exchange folders.</span></span> <span data-ttu-id="6cd76-109">Единственной записью в этой папке является следующее:</span><span class="sxs-lookup"><span data-stu-id="6cd76-109">The only entry in this folder is the following:</span></span>

`win32=<path>\ACEEXCH.DLL`

<span data-ttu-id="6cd76-110">Этот параметр используется ядром СУБД Microsoft Access для указания расположения Ацеексч. dll.</span><span class="sxs-lookup"><span data-stu-id="6cd76-110">The Microsoft Access database engine uses this setting to indicate the location of Aceexch.dll.</span></span> <span data-ttu-id="6cd76-111">Полный путь определяется во время установки.</span><span class="sxs-lookup"><span data-stu-id="6cd76-111">The full path is determined at the time of installation.</span></span> <span data-ttu-id="6cd76-112">Значения имеют тип REG\_СЗ.</span><span class="sxs-lookup"><span data-stu-id="6cd76-112">Values are of type REG\_SZ.</span></span>

<span data-ttu-id="6cd76-113">Результаты использования формата ISAM Outlook и с использованием формата ISAM клиента Exchange похожи.</span><span class="sxs-lookup"><span data-stu-id="6cd76-113">The results of using the Outlook ISAM format and of using the Exchange client ISAM format are similar.</span></span> <span data-ttu-id="6cd76-114">Единственное отличие состоит в том, что два разных клиента используют разные имена для одних и тех же столбцов.</span><span class="sxs-lookup"><span data-stu-id="6cd76-114">The only difference is that the two different clients use different names for the same columns.</span></span> <span data-ttu-id="6cd76-115">Были созданы два формата ISAM, поэтому ядро СУБД Microsoft Access может возвращать имена столбцов в определенном стиле, который пользователь хочет.</span><span class="sxs-lookup"><span data-stu-id="6cd76-115">The two ISAM formats have been created so that the Microsoft Access database engine can return the column names in the particular style that the user desires.</span></span>

## <a name="microsoft-outlook-client-isam-formats"></a><span data-ttu-id="6cd76-116">ISAM formats клиента Microsoft Outlook</span><span class="sxs-lookup"><span data-stu-id="6cd76-116">Microsoft Outlook client ISAM formats</span></span>

<span data-ttu-id="6cd76-117">**Подсистема\\подключения доступа ISAM\\formats Outlook 9,0** содержит следующие записи.</span><span class="sxs-lookup"><span data-stu-id="6cd76-117">The **Access Connectivity Engine\\ISAM Formats\\Outlook 9.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6cd76-118">Имя записи</span><span class="sxs-lookup"><span data-stu-id="6cd76-118">Entry name</span></span></p></th>
<th><p><span data-ttu-id="6cd76-119">Тип</span><span class="sxs-lookup"><span data-stu-id="6cd76-119">Type</span></span></p></th>
<th><p><span data-ttu-id="6cd76-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6cd76-120">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6cd76-121">Модул</span><span class="sxs-lookup"><span data-stu-id="6cd76-121">Engine</span></span></p></td>
<td><p><span data-ttu-id="6cd76-122">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="6cd76-122">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="6cd76-123">Exchange</span><span class="sxs-lookup"><span data-stu-id="6cd76-123">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cd76-124">Импортфилтер</span><span class="sxs-lookup"><span data-stu-id="6cd76-124">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="6cd76-125">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="6cd76-125">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="6cd76-126">Outlook ()</span><span class="sxs-lookup"><span data-stu-id="6cd76-126">Outlook()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cd76-127">Канлинк</span><span class="sxs-lookup"><span data-stu-id="6cd76-127">CanLink</span></span></p></td>
<td><p><span data-ttu-id="6cd76-128">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="6cd76-128">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="6cd76-129">01</span><span class="sxs-lookup"><span data-stu-id="6cd76-129">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cd76-130">Онетаблеперфиле</span><span class="sxs-lookup"><span data-stu-id="6cd76-130">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="6cd76-131">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="6cd76-131">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="6cd76-132">00</span><span class="sxs-lookup"><span data-stu-id="6cd76-132">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cd76-133">Исамтипе</span><span class="sxs-lookup"><span data-stu-id="6cd76-133">IsamType</span></span></p></td>
<td><p><span data-ttu-id="6cd76-134">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="6cd76-134">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="6cd76-135">4</span><span class="sxs-lookup"><span data-stu-id="6cd76-135">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cd76-136">Индексдиалог</span><span class="sxs-lookup"><span data-stu-id="6cd76-136">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="6cd76-137">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="6cd76-137">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="6cd76-138">00</span><span class="sxs-lookup"><span data-stu-id="6cd76-138">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cd76-139">Креатедбонекспорт</span><span class="sxs-lookup"><span data-stu-id="6cd76-139">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="6cd76-140">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="6cd76-140">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="6cd76-141">00</span><span class="sxs-lookup"><span data-stu-id="6cd76-141">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cd76-142">Суппортслонгнамес</span><span class="sxs-lookup"><span data-stu-id="6cd76-142">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="6cd76-143">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="6cd76-143">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="6cd76-144">01</span><span class="sxs-lookup"><span data-stu-id="6cd76-144">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="6cd76-145">При изменении параметров реестра Windows необходимо выйти и перезапустить ядро СУБД, чтобы новые параметры вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="6cd76-145">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="microsoft-exchange-client-isam-formats"></a><span data-ttu-id="6cd76-146">ISAM formats клиента Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="6cd76-146">Microsoft Exchange client ISAM formats</span></span>

<span data-ttu-id="6cd76-147">**Модуль\\подключения к службе доступа ISAM\\formats Exchange 4,0** папка содержит следующие записи.</span><span class="sxs-lookup"><span data-stu-id="6cd76-147">The **Access Connectivity Engine\\ISAM Formats\\Exchange 4.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6cd76-148">Имя записи</span><span class="sxs-lookup"><span data-stu-id="6cd76-148">Entry name</span></span></p></th>
<th><p><span data-ttu-id="6cd76-149">Тип</span><span class="sxs-lookup"><span data-stu-id="6cd76-149">Type</span></span></p></th>
<th><p><span data-ttu-id="6cd76-150">Значение</span><span class="sxs-lookup"><span data-stu-id="6cd76-150">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6cd76-151">Модул</span><span class="sxs-lookup"><span data-stu-id="6cd76-151">Engine</span></span></p></td>
<td><p><span data-ttu-id="6cd76-152">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="6cd76-152">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="6cd76-153">Exchange</span><span class="sxs-lookup"><span data-stu-id="6cd76-153">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cd76-154">Импортфилтер</span><span class="sxs-lookup"><span data-stu-id="6cd76-154">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="6cd76-155">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="6cd76-155">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="6cd76-156">Exchange ()</span><span class="sxs-lookup"><span data-stu-id="6cd76-156">Exchange()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cd76-157">Канлинк</span><span class="sxs-lookup"><span data-stu-id="6cd76-157">CanLink</span></span></p></td>
<td><p><span data-ttu-id="6cd76-158">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="6cd76-158">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="6cd76-159">01</span><span class="sxs-lookup"><span data-stu-id="6cd76-159">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cd76-160">Онетаблеперфиле</span><span class="sxs-lookup"><span data-stu-id="6cd76-160">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="6cd76-161">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="6cd76-161">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="6cd76-162">00</span><span class="sxs-lookup"><span data-stu-id="6cd76-162">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cd76-163">Исамтипе</span><span class="sxs-lookup"><span data-stu-id="6cd76-163">IsamType</span></span></p></td>
<td><p><span data-ttu-id="6cd76-164">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="6cd76-164">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="6cd76-165">4</span><span class="sxs-lookup"><span data-stu-id="6cd76-165">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cd76-166">Индексдиалог</span><span class="sxs-lookup"><span data-stu-id="6cd76-166">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="6cd76-167">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="6cd76-167">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="6cd76-168">00</span><span class="sxs-lookup"><span data-stu-id="6cd76-168">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cd76-169">Креатедбонекспорт</span><span class="sxs-lookup"><span data-stu-id="6cd76-169">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="6cd76-170">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="6cd76-170">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="6cd76-171">00</span><span class="sxs-lookup"><span data-stu-id="6cd76-171">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cd76-172">Суппортслонгнамес</span><span class="sxs-lookup"><span data-stu-id="6cd76-172">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="6cd76-173">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="6cd76-173">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="6cd76-174">01</span><span class="sxs-lookup"><span data-stu-id="6cd76-174">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="6cd76-175">При изменении параметров реестра Windows необходимо выйти и перезапустить ядро СУБД, чтобы новые параметры вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="6cd76-175">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a><span data-ttu-id="6cd76-176">Настройка файла Schema. ini для данных Outlook и Exchange</span><span class="sxs-lookup"><span data-stu-id="6cd76-176">Customizing the Schema.ini file for Outlook and Exchange data</span></span>

<span data-ttu-id="6cd76-177">Файл Schema. ini используется в Outlook и Exchange ISAM точно так же, как и при использовании текста ISAM.</span><span class="sxs-lookup"><span data-stu-id="6cd76-177">The Schema.ini file is used by the Outlook and Exchange ISAM in much the same way that it is used by the Text ISAM.</span></span> <span data-ttu-id="6cd76-178">Schema. ini содержит особенности источника данных: способ форматирования данных и имена столбцов, к которым нужно получить доступ.</span><span class="sxs-lookup"><span data-stu-id="6cd76-178">Schema.ini contains the specifics of a data source: how the data is formatted, and the names of columns that should be accessed.</span></span>

<span data-ttu-id="6cd76-179">Нет необходимости изменять файл Schema. ini до того, как данные могут быть прочитаны, импортированы или экспортированы для Outlook и Exchange.</span><span class="sxs-lookup"><span data-stu-id="6cd76-179">It is not necessary to modify the Schema.ini file before data can be read, imported, or exported for Outlook and Exchange.</span></span> <span data-ttu-id="6cd76-180">Многие параметры в файле Schema. ini для Outlook и Exchange относятся к внутренним тегам, которые необходимы для MAPI.</span><span class="sxs-lookup"><span data-stu-id="6cd76-180">Many of the settings inside the Schema.ini file for Outlook and Exchange are specific to internal tags that MAPI requires.</span></span> <span data-ttu-id="6cd76-181">Не пытайтесь изменить значения этих тегов.</span><span class="sxs-lookup"><span data-stu-id="6cd76-181">You should not attempt to modify those tag values.</span></span>

