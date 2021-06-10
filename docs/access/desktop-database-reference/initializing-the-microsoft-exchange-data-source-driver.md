---
title: Инициализация драйвера microsoft Exchange источника данных
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
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a><span data-ttu-id="86cbc-102">Инициализация драйвера microsoft Exchange источника данных</span><span class="sxs-lookup"><span data-stu-id="86cbc-102">Initializing the Microsoft Exchange Data Source driver</span></span>

<span data-ttu-id="86cbc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="86cbc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="86cbc-104">При установке драйвера Microsoft Exchange источника данных программа установки записывает набор значений по умолчанию в реестр microsoft Windows в подкайлах Engines и ISAM Formats.</span><span class="sxs-lookup"><span data-stu-id="86cbc-104">When you install the Microsoft Exchange Data Source driver, the Setup program writes a set of default values to the Microsoft Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="86cbc-105">Не следует изменять эти параметры напрямую; используйте программу установки для приложения, чтобы добавить, удалить или изменить эти параметры.</span><span class="sxs-lookup"><span data-stu-id="86cbc-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="86cbc-106">В следующих разделах описываются параметры инициализации и формата ISAM для драйвера Microsoft Exchange данных.</span><span class="sxs-lookup"><span data-stu-id="86cbc-106">The following sections describe initialization and ISAM Format settings for the Microsoft Exchange Data Source driver.</span></span>

## <a name="microsoft-exchange-data-source-initialization-settings"></a><span data-ttu-id="86cbc-107">Параметры Exchange исходных данных Microsoft</span><span class="sxs-lookup"><span data-stu-id="86cbc-107">Microsoft Exchange data source initialization settings</span></span>

<span data-ttu-id="86cbc-108">Папка **\\ Engines \\ Exchange access Connectivity Engines** включает параметры инициализации драйвера Aceexch.dll, используемых для внешнего доступа к папкам Microsoft Outlook и Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="86cbc-108">The **Access Connectivity Engine\\Engines\\Exchange** folder includes initialization settings for the Aceexch.dll driver, used for external access to Microsoft Outlook and Microsoft Exchange folders.</span></span> <span data-ttu-id="86cbc-109">В этой папке только одна запись:</span><span class="sxs-lookup"><span data-stu-id="86cbc-109">The only entry in this folder is the following:</span></span>

`win32=<path>\ACEEXCH.DLL`

<span data-ttu-id="86cbc-110">Движок базы данных Microsoft Access использует этот параметр, чтобы указать расположение Aceexch.dll.</span><span class="sxs-lookup"><span data-stu-id="86cbc-110">The Microsoft Access database engine uses this setting to indicate the location of Aceexch.dll.</span></span> <span data-ttu-id="86cbc-111">Полный путь определяется во время установки.</span><span class="sxs-lookup"><span data-stu-id="86cbc-111">The full path is determined at the time of installation.</span></span> <span data-ttu-id="86cbc-112">Значения имеют тип REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="86cbc-112">Values are of type REG\_SZ.</span></span>

<span data-ttu-id="86cbc-113">Результаты использования формата Outlook ISAM и использования Exchange клиентского формата ISAM похожи.</span><span class="sxs-lookup"><span data-stu-id="86cbc-113">The results of using the Outlook ISAM format and of using the Exchange client ISAM format are similar.</span></span> <span data-ttu-id="86cbc-114">Единственное отличие состоит в том, что два разных клиента используют разные имена для одинаковых столбцов.</span><span class="sxs-lookup"><span data-stu-id="86cbc-114">The only difference is that the two different clients use different names for the same columns.</span></span> <span data-ttu-id="86cbc-115">Два формата ISAM созданы таким образом, чтобы двигатель базы данных Microsoft Access мог возвращать имена столбцов в определенном стиле, который желает пользователь.</span><span class="sxs-lookup"><span data-stu-id="86cbc-115">The two ISAM formats have been created so that the Microsoft Access database engine can return the column names in the particular style that the user desires.</span></span>

## <a name="microsoft-outlook-client-isam-formats"></a><span data-ttu-id="86cbc-116">Microsoft Outlook клиентских форматов ISAM</span><span class="sxs-lookup"><span data-stu-id="86cbc-116">Microsoft Outlook client ISAM formats</span></span>

<span data-ttu-id="86cbc-117">В **папке IsAM Engine ISAM Outlook \\ \\ 9.0** содержатся следующие записи.</span><span class="sxs-lookup"><span data-stu-id="86cbc-117">The **Access Connectivity Engine\\ISAM Formats\\Outlook 9.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="86cbc-118">Имя входа</span><span class="sxs-lookup"><span data-stu-id="86cbc-118">Entry name</span></span></p></th>
<th><p><span data-ttu-id="86cbc-119">Тип</span><span class="sxs-lookup"><span data-stu-id="86cbc-119">Type</span></span></p></th>
<th><p><span data-ttu-id="86cbc-120">Значение</span><span class="sxs-lookup"><span data-stu-id="86cbc-120">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86cbc-121">Двигатель</span><span class="sxs-lookup"><span data-stu-id="86cbc-121">Engine</span></span></p></td>
<td><p><span data-ttu-id="86cbc-122">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="86cbc-122">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="86cbc-123">Exchange</span><span class="sxs-lookup"><span data-stu-id="86cbc-123">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86cbc-124">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="86cbc-124">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="86cbc-125">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="86cbc-125">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="86cbc-126">Outlook()</span><span class="sxs-lookup"><span data-stu-id="86cbc-126">Outlook()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86cbc-127">CanLink</span><span class="sxs-lookup"><span data-stu-id="86cbc-127">CanLink</span></span></p></td>
<td><p><span data-ttu-id="86cbc-128">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="86cbc-128">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="86cbc-129">01</span><span class="sxs-lookup"><span data-stu-id="86cbc-129">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86cbc-130">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="86cbc-130">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="86cbc-131">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="86cbc-131">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="86cbc-132">00</span><span class="sxs-lookup"><span data-stu-id="86cbc-132">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86cbc-133">IsamType</span><span class="sxs-lookup"><span data-stu-id="86cbc-133">IsamType</span></span></p></td>
<td><p><span data-ttu-id="86cbc-134">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="86cbc-134">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="86cbc-135">3</span><span class="sxs-lookup"><span data-stu-id="86cbc-135">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86cbc-136">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="86cbc-136">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="86cbc-137">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="86cbc-137">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="86cbc-138">00</span><span class="sxs-lookup"><span data-stu-id="86cbc-138">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86cbc-139">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="86cbc-139">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="86cbc-140">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="86cbc-140">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="86cbc-141">00</span><span class="sxs-lookup"><span data-stu-id="86cbc-141">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86cbc-142">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="86cbc-142">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="86cbc-143">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="86cbc-143">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="86cbc-144">01</span><span class="sxs-lookup"><span data-stu-id="86cbc-144">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="86cbc-145">При изменении параметров Windows реестра необходимо выйти и перезапустить двигатель базы данных, чтобы новые параметры вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="86cbc-145">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="microsoft-exchange-client-isam-formats"></a><span data-ttu-id="86cbc-146">Microsoft Exchange клиентских форматов ISAM</span><span class="sxs-lookup"><span data-stu-id="86cbc-146">Microsoft Exchange client ISAM formats</span></span>

<span data-ttu-id="86cbc-147">В **папке IsAM Engine ISAM Exchange \\ \\ 4.0** содержатся следующие записи.</span><span class="sxs-lookup"><span data-stu-id="86cbc-147">The **Access Connectivity Engine\\ISAM Formats\\Exchange 4.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="86cbc-148">Имя входа</span><span class="sxs-lookup"><span data-stu-id="86cbc-148">Entry name</span></span></p></th>
<th><p><span data-ttu-id="86cbc-149">Тип</span><span class="sxs-lookup"><span data-stu-id="86cbc-149">Type</span></span></p></th>
<th><p><span data-ttu-id="86cbc-150">Значение</span><span class="sxs-lookup"><span data-stu-id="86cbc-150">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86cbc-151">Двигатель</span><span class="sxs-lookup"><span data-stu-id="86cbc-151">Engine</span></span></p></td>
<td><p><span data-ttu-id="86cbc-152">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="86cbc-152">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="86cbc-153">Exchange</span><span class="sxs-lookup"><span data-stu-id="86cbc-153">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86cbc-154">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="86cbc-154">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="86cbc-155">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="86cbc-155">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="86cbc-156">Exchange()</span><span class="sxs-lookup"><span data-stu-id="86cbc-156">Exchange()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86cbc-157">CanLink</span><span class="sxs-lookup"><span data-stu-id="86cbc-157">CanLink</span></span></p></td>
<td><p><span data-ttu-id="86cbc-158">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="86cbc-158">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="86cbc-159">01</span><span class="sxs-lookup"><span data-stu-id="86cbc-159">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86cbc-160">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="86cbc-160">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="86cbc-161">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="86cbc-161">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="86cbc-162">00</span><span class="sxs-lookup"><span data-stu-id="86cbc-162">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86cbc-163">IsamType</span><span class="sxs-lookup"><span data-stu-id="86cbc-163">IsamType</span></span></p></td>
<td><p><span data-ttu-id="86cbc-164">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="86cbc-164">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="86cbc-165">3</span><span class="sxs-lookup"><span data-stu-id="86cbc-165">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86cbc-166">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="86cbc-166">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="86cbc-167">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="86cbc-167">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="86cbc-168">00</span><span class="sxs-lookup"><span data-stu-id="86cbc-168">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86cbc-169">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="86cbc-169">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="86cbc-170">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="86cbc-170">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="86cbc-171">00</span><span class="sxs-lookup"><span data-stu-id="86cbc-171">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86cbc-172">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="86cbc-172">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="86cbc-173">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="86cbc-173">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="86cbc-174">01</span><span class="sxs-lookup"><span data-stu-id="86cbc-174">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="86cbc-175">При изменении параметров Windows реестра необходимо выйти и перезапустить двигатель базы данных, чтобы новые параметры вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="86cbc-175">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a><span data-ttu-id="86cbc-176">Настройка файла Schema.ini для Outlook и Exchange данных</span><span class="sxs-lookup"><span data-stu-id="86cbc-176">Customizing the Schema.ini file for Outlook and Exchange data</span></span>

<span data-ttu-id="86cbc-177">Файл Schema.ini используется Outlook и Exchange ISAM таким же образом, как и текстовый ISAM.</span><span class="sxs-lookup"><span data-stu-id="86cbc-177">The Schema.ini file is used by the Outlook and Exchange ISAM in much the same way that it is used by the Text ISAM.</span></span> <span data-ttu-id="86cbc-178">Schema.ini содержит особенности источника данных: форматирование данных и имена столбцов, к которых необходимо получить доступ.</span><span class="sxs-lookup"><span data-stu-id="86cbc-178">Schema.ini contains the specifics of a data source: how the data is formatted, and the names of columns that should be accessed.</span></span>

<span data-ttu-id="86cbc-179">Нет необходимости изменять файл Schema.ini перед чтением, импортом или экспортом для Outlook и Exchange.</span><span class="sxs-lookup"><span data-stu-id="86cbc-179">It is not necessary to modify the Schema.ini file before data can be read, imported, or exported for Outlook and Exchange.</span></span> <span data-ttu-id="86cbc-180">Многие параметры внутри файла Schema.ini для Outlook и Exchange для внутренних тегов, необходимых MAPI.</span><span class="sxs-lookup"><span data-stu-id="86cbc-180">Many of the settings inside the Schema.ini file for Outlook and Exchange are specific to internal tags that MAPI requires.</span></span> <span data-ttu-id="86cbc-181">Не следует пытаться изменить эти значения тегов.</span><span class="sxs-lookup"><span data-stu-id="86cbc-181">You should not attempt to modify those tag values.</span></span>

