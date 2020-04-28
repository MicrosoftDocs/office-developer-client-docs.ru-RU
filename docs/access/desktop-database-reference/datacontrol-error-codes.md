---
title: Коды ошибок DataControl
TOCTitle: DataControl error codes
ms:assetid: d81446e2-aae6-b460-08a3-eae9920dc767
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250089(v=office.15)
ms:contentKeyID: 48548027
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 387f37e180d346c09cf3dadbf66f665cb83dbd0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294546"
---
# <a name="datacontrol-error-codes"></a><span data-ttu-id="86e4e-102">Коды ошибок DataControl</span><span class="sxs-lookup"><span data-stu-id="86e4e-102">DataControl error codes</span></span>


<span data-ttu-id="86e4e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="86e4e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="86e4e-104">В следующей таблице перечислены службы [RDS. ](datacontrol-object-rds.md)Коды ошибок объектного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="86e4e-104">The following table lists the [RDS.DataControl](datacontrol-object-rds.md) object error codes.</span></span> <span data-ttu-id="86e4e-105">При положительном десятичном преобразовании двух нижних байтов отображается отрицательный десятичный перевод полного кода ошибки и шестнадцатеричные значения.</span><span class="sxs-lookup"><span data-stu-id="86e4e-105">The positive decimal translation of the low two bytes, the negative decimal translation of the full error code, and the hexadecimal values are shown.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="86e4e-106">Рабочих. Коды ошибок для элементов управления</span><span class="sxs-lookup"><span data-stu-id="86e4e-106">RDS.DataControl error codes</span></span></p></th>
<th><p><span data-ttu-id="86e4e-107">Номер</span><span class="sxs-lookup"><span data-stu-id="86e4e-107">Number</span></span></p></th>
<th><p><span data-ttu-id="86e4e-108">Описание</span><span class="sxs-lookup"><span data-stu-id="86e4e-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86e4e-109"><strong>IDS_AsyncPending</strong></span><span class="sxs-lookup"><span data-stu-id="86e4e-109"><strong>IDS_AsyncPending</strong></span></span></p></td>
<td><p><span data-ttu-id="86e4e-110">4107</span><span class="sxs-lookup"><span data-stu-id="86e4e-110">4107</span></span><br />
<span data-ttu-id="86e4e-111">— 2146824175</span><span class="sxs-lookup"><span data-stu-id="86e4e-111">-2146824175</span></span><br />
<span data-ttu-id="86e4e-112">0x800A1011</span><span class="sxs-lookup"><span data-stu-id="86e4e-112">0x800A1011</span></span></p></td>
<td><p><span data-ttu-id="86e4e-113">Не удается выполнить операцию, пока ожидается асинхронная операция.</span><span class="sxs-lookup"><span data-stu-id="86e4e-113">Operation cannot be performed while async operation is pending.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86e4e-114"><strong>IDS_BadInlineTablegram</strong></span><span class="sxs-lookup"><span data-stu-id="86e4e-114"><strong>IDS_BadInlineTablegram</strong></span></span></p></td>
<td><p><span data-ttu-id="86e4e-115">4105</span><span class="sxs-lookup"><span data-stu-id="86e4e-115">4105</span></span><br />
<span data-ttu-id="86e4e-116">— 2146824183</span><span class="sxs-lookup"><span data-stu-id="86e4e-116">-2146824183</span></span><br />
<span data-ttu-id="86e4e-117">0x800A1009</span><span class="sxs-lookup"><span data-stu-id="86e4e-117">0x800A1009</span></span></p></td>
<td><p><span data-ttu-id="86e4e-118">Неправильное встроенное таблеграм.</span><span class="sxs-lookup"><span data-stu-id="86e4e-118">Bad inline tablegram.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86e4e-119"><strong>IDS_CantConnect</strong></span><span class="sxs-lookup"><span data-stu-id="86e4e-119"><strong>IDS_CantConnect</strong></span></span></p></td>
<td><p><span data-ttu-id="86e4e-120">4099</span><span class="sxs-lookup"><span data-stu-id="86e4e-120">4099</span></span><br />
<span data-ttu-id="86e4e-121">— 2146824189</span><span class="sxs-lookup"><span data-stu-id="86e4e-121">-2146824189</span></span><br />
<span data-ttu-id="86e4e-122">0x800A1003</span><span class="sxs-lookup"><span data-stu-id="86e4e-122">0x800A1003</span></span></p></td>
<td><p><span data-ttu-id="86e4e-123">Не удается подключиться к серверу.</span><span class="sxs-lookup"><span data-stu-id="86e4e-123">Cannot connect to server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86e4e-124"><strong>IDS_CantCreateObject</strong></span><span class="sxs-lookup"><span data-stu-id="86e4e-124"><strong>IDS_CantCreateObject</strong></span></span></p></td>
<td><p><span data-ttu-id="86e4e-125">4100</span><span class="sxs-lookup"><span data-stu-id="86e4e-125">4100</span></span><br />
<span data-ttu-id="86e4e-126">— 2146824188</span><span class="sxs-lookup"><span data-stu-id="86e4e-126">-2146824188</span></span><br />
<span data-ttu-id="86e4e-127">0x800A1004</span><span class="sxs-lookup"><span data-stu-id="86e4e-127">0x800A1004</span></span></p></td>
<td><p><span data-ttu-id="86e4e-128">Не удается создать бизнес-объект.</span><span class="sxs-lookup"><span data-stu-id="86e4e-128">Business object cannot be created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86e4e-129"><strong>IDS_CantFindDataspace</strong></span><span class="sxs-lookup"><span data-stu-id="86e4e-129"><strong>IDS_CantFindDataspace</strong></span></span></p></td>
<td><p><span data-ttu-id="86e4e-130">4102</span><span class="sxs-lookup"><span data-stu-id="86e4e-130">4102</span></span><br />
<span data-ttu-id="86e4e-131">— 2146824186</span><span class="sxs-lookup"><span data-stu-id="86e4e-131">-2146824186</span></span><br />
<span data-ttu-id="86e4e-132">0x800A1006</span><span class="sxs-lookup"><span data-stu-id="86e4e-132">0x800A1006</span></span></p></td>
<td><p><span data-ttu-id="86e4e-133">Недопустимое свойство Space.</span><span class="sxs-lookup"><span data-stu-id="86e4e-133">Dataspace property is not valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86e4e-134"><strong>IDS_CantInvokeMethod</strong></span><span class="sxs-lookup"><span data-stu-id="86e4e-134"><strong>IDS_CantInvokeMethod</strong></span></span></p></td>
<td><p><span data-ttu-id="86e4e-135">4101</span><span class="sxs-lookup"><span data-stu-id="86e4e-135">4101</span></span><br />
<span data-ttu-id="86e4e-136">— 2146824187</span><span class="sxs-lookup"><span data-stu-id="86e4e-136">-2146824187</span></span><br />
<span data-ttu-id="86e4e-137">0x800A1005</span><span class="sxs-lookup"><span data-stu-id="86e4e-137">0x800A1005</span></span></p></td>
<td><p><span data-ttu-id="86e4e-138">Метод не может быть вызван для бизнес-объекта.</span><span class="sxs-lookup"><span data-stu-id="86e4e-138">Method cannot be invoked on business object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86e4e-139"><strong>IDS_CrossDomainWarning</strong></span><span class="sxs-lookup"><span data-stu-id="86e4e-139"><strong>IDS_CrossDomainWarning</strong></span></span></p></td>
<td><p><span data-ttu-id="86e4e-140">4112</span><span class="sxs-lookup"><span data-stu-id="86e4e-140">4112</span></span><br />
<span data-ttu-id="86e4e-141">— 2146824170</span><span class="sxs-lookup"><span data-stu-id="86e4e-141">-2146824170</span></span><br />
<span data-ttu-id="86e4e-142">0x800A1016</span><span class="sxs-lookup"><span data-stu-id="86e4e-142">0x800A1016</span></span></p></td>
<td><p><span data-ttu-id="86e4e-143">Эта страница получает доступ к данным в другом домене.</span><span class="sxs-lookup"><span data-stu-id="86e4e-143">This page accesses data on another domain.</span></span> <span data-ttu-id="86e4e-144">Вы хотите разрешить это действие?</span><span class="sxs-lookup"><span data-stu-id="86e4e-144">Do you want to allow this?</span></span> <span data-ttu-id="86e4e-145">Чтобы избежать появления этого сообщения в Internet Explorer, можно добавить безопасный веб-сайт в зону надежных сайтов на вкладке <strong>Безопасность</strong> диалогового окна <strong>Свойства обозревателя</strong> .</span><span class="sxs-lookup"><span data-stu-id="86e4e-145">To avoid this message in Internet Explorer, you can add a secure website to your Trusted Sites zone on the <strong>Security</strong> tab of the <strong>Internet Options</strong> dialog box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86e4e-146"><strong>IDS_InvalidADCClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="86e4e-146"><strong>IDS_InvalidADCClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="86e4e-147">4106</span><span class="sxs-lookup"><span data-stu-id="86e4e-147">4106</span></span><br />
<span data-ttu-id="86e4e-148">— 2146824176</span><span class="sxs-lookup"><span data-stu-id="86e4e-148">-2146824176</span></span><br />
<span data-ttu-id="86e4e-149">0x800A1010</span><span class="sxs-lookup"><span data-stu-id="86e4e-149">0x800A1010</span></span></p></td>
<td><p><span data-ttu-id="86e4e-150">Недопустимая версия клиента RDS — Клиент новее сервера.</span><span class="sxs-lookup"><span data-stu-id="86e4e-150">Invalid RDS Client Version — Client is newer than server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86e4e-151"><strong>IDS_INVALIDARG</strong></span><span class="sxs-lookup"><span data-stu-id="86e4e-151"><strong>IDS_INVALIDARG</strong></span></span></p></td>
<td><p><span data-ttu-id="86e4e-152">5376</span><span class="sxs-lookup"><span data-stu-id="86e4e-152">5376</span></span><br />
<span data-ttu-id="86e4e-153">— 2147019520</span><span class="sxs-lookup"><span data-stu-id="86e4e-153">-2147019520</span></span><br />
<span data-ttu-id="86e4e-154">0x80071500</span><span class="sxs-lookup"><span data-stu-id="86e4e-154">0x80071500</span></span></p></td>
<td><p><span data-ttu-id="86e4e-155">Один или несколько аргументов являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="86e4e-155">One or more arguments are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86e4e-156"><strong>IDS_InvalidBindings</strong></span><span class="sxs-lookup"><span data-stu-id="86e4e-156"><strong>IDS_InvalidBindings</strong></span></span></p></td>
<td><p><span data-ttu-id="86e4e-157">4097</span><span class="sxs-lookup"><span data-stu-id="86e4e-157">4097</span></span><br />
<span data-ttu-id="86e4e-158">— 2146824191</span><span class="sxs-lookup"><span data-stu-id="86e4e-158">-2146824191</span></span><br />
<span data-ttu-id="86e4e-159">0x800A1001</span><span class="sxs-lookup"><span data-stu-id="86e4e-159">0x800A1001</span></span></p></td>
<td><p><span data-ttu-id="86e4e-160">Ошибка в свойстве Bindings.</span><span class="sxs-lookup"><span data-stu-id="86e4e-160">Error in bindings property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86e4e-161"><strong>IDS_InvalidParam</strong></span><span class="sxs-lookup"><span data-stu-id="86e4e-161"><strong>IDS_InvalidParam</strong></span></span></p></td>
<td><p><span data-ttu-id="86e4e-162">4110</span><span class="sxs-lookup"><span data-stu-id="86e4e-162">4110</span></span><br />
<span data-ttu-id="86e4e-163">— 2146824172</span><span class="sxs-lookup"><span data-stu-id="86e4e-163">-2146824172</span></span><br />
<span data-ttu-id="86e4e-164">0x800A1014</span><span class="sxs-lookup"><span data-stu-id="86e4e-164">0x800A1014</span></span></p></td>
<td><p><span data-ttu-id="86e4e-165">Один или несколько аргументов являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="86e4e-165">One or more arguments are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86e4e-166"><strong>IDS_NOINTERFACE</strong></span><span class="sxs-lookup"><span data-stu-id="86e4e-166"><strong>IDS_NOINTERFACE</strong></span></span></p></td>
<td><p><span data-ttu-id="86e4e-167">5377</span><span class="sxs-lookup"><span data-stu-id="86e4e-167">5377</span></span><br />
<span data-ttu-id="86e4e-168">— 2147019519</span><span class="sxs-lookup"><span data-stu-id="86e4e-168">-2147019519</span></span><br />
<span data-ttu-id="86e4e-169">0x80071501</span><span class="sxs-lookup"><span data-stu-id="86e4e-169">0x80071501</span></span></p></td>
<td><p><span data-ttu-id="86e4e-170">Такой интерфейс не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="86e4e-170">No such interface is supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86e4e-171"><strong>IDS_NotReentrant</strong></span><span class="sxs-lookup"><span data-stu-id="86e4e-171"><strong>IDS_NotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="86e4e-172">4111</span><span class="sxs-lookup"><span data-stu-id="86e4e-172">4111</span></span><br />
<span data-ttu-id="86e4e-173">— 2146824171</span><span class="sxs-lookup"><span data-stu-id="86e4e-173">-2146824171</span></span><br />
<span data-ttu-id="86e4e-174">0x800A1015</span><span class="sxs-lookup"><span data-stu-id="86e4e-174">0x800A1015</span></span></p></td>
<td><p><span data-ttu-id="86e4e-175">Запрос не может быть выполнен, пока обработчик событий еще обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="86e4e-175">Request cannot be executed while the event handler is still processing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86e4e-176"><strong>IDS_ObjectNotSafe</strong></span><span class="sxs-lookup"><span data-stu-id="86e4e-176"><strong>IDS_ObjectNotSafe</strong></span></span></p></td>
<td><p><span data-ttu-id="86e4e-177">4103</span><span class="sxs-lookup"><span data-stu-id="86e4e-177">4103</span></span><br />
<span data-ttu-id="86e4e-178">— 2146824185</span><span class="sxs-lookup"><span data-stu-id="86e4e-178">-2146824185</span></span><br />
<span data-ttu-id="86e4e-179">0x800A1007</span><span class="sxs-lookup"><span data-stu-id="86e4e-179">0x800A1007</span></span></p></td>
<td><p><span data-ttu-id="86e4e-180">Параметры безопасности этого компьютера запрещают создание бизнес-объекта.</span><span class="sxs-lookup"><span data-stu-id="86e4e-180">Safety settings on this computer prohibit creation of business object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86e4e-181"><strong>IDS_RecordsetNotOpen</strong></span><span class="sxs-lookup"><span data-stu-id="86e4e-181"><strong>IDS_RecordsetNotOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="86e4e-182">4109</span><span class="sxs-lookup"><span data-stu-id="86e4e-182">4109</span></span><br />
<span data-ttu-id="86e4e-183">— 2146824173</span><span class="sxs-lookup"><span data-stu-id="86e4e-183">-2146824173</span></span><br />
<span data-ttu-id="86e4e-184">0x800A1013</span><span class="sxs-lookup"><span data-stu-id="86e4e-184">0x800A1013</span></span></p></td>
<td><p><span data-ttu-id="86e4e-185">Объект <strong>Recordset</strong> не открыт.</span><span class="sxs-lookup"><span data-stu-id="86e4e-185"><strong>Recordset</strong> is not open.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86e4e-186"><strong>IDS_ResetInvalidField</strong></span><span class="sxs-lookup"><span data-stu-id="86e4e-186"><strong>IDS_ResetInvalidField</strong></span></span></p></td>
<td><p><span data-ttu-id="86e4e-187">4108</span><span class="sxs-lookup"><span data-stu-id="86e4e-187">4108</span></span><br />
<span data-ttu-id="86e4e-188">— 2146824174</span><span class="sxs-lookup"><span data-stu-id="86e4e-188">-2146824174</span></span><br />
<span data-ttu-id="86e4e-189">0x800A1012</span><span class="sxs-lookup"><span data-stu-id="86e4e-189">0x800A1012</span></span></p></td>
<td><p><span data-ttu-id="86e4e-190">Столбец, указанный в <strong>sortColumn</strong> или <strong>FilterColumn</strong> , не существует.</span><span class="sxs-lookup"><span data-stu-id="86e4e-190">Column specified in <strong>SortColumn</strong> or <strong>FilterColumn</strong> does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86e4e-191"><strong>IDS_RowsetNotUpdateable</strong></span><span class="sxs-lookup"><span data-stu-id="86e4e-191"><strong>IDS_RowsetNotUpdateable</strong></span></span></p></td>
<td><p><span data-ttu-id="86e4e-192">4104</span><span class="sxs-lookup"><span data-stu-id="86e4e-192">4104</span></span><br />
<span data-ttu-id="86e4e-193">— 2146824184</span><span class="sxs-lookup"><span data-stu-id="86e4e-193">-2146824184</span></span><br />
<span data-ttu-id="86e4e-194">0x800A1008</span><span class="sxs-lookup"><span data-stu-id="86e4e-194">0x800A1008</span></span></p></td>
<td><p><span data-ttu-id="86e4e-195">Набор строк не обновляемый.</span><span class="sxs-lookup"><span data-stu-id="86e4e-195">Rowset not updateable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86e4e-196"><strong>IDS_UnexpectedError</strong></span><span class="sxs-lookup"><span data-stu-id="86e4e-196"><strong>IDS_UnexpectedError</strong></span></span></p></td>
<td><p><span data-ttu-id="86e4e-197">4351</span><span class="sxs-lookup"><span data-stu-id="86e4e-197">4351</span></span><br />
<span data-ttu-id="86e4e-198">— 2146823937</span><span class="sxs-lookup"><span data-stu-id="86e4e-198">-2146823937</span></span><br />
<span data-ttu-id="86e4e-199">0x800A10FF</span><span class="sxs-lookup"><span data-stu-id="86e4e-199">0x800A10FF</span></span></p></td>
<td><p><span data-ttu-id="86e4e-200">Непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="86e4e-200">Unexpected error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86e4e-201"><strong>IDS_UpdatesFailed</strong></span><span class="sxs-lookup"><span data-stu-id="86e4e-201"><strong>IDS_UpdatesFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="86e4e-202">4098</span><span class="sxs-lookup"><span data-stu-id="86e4e-202">4098</span></span><br />
<span data-ttu-id="86e4e-203">— 2146824190</span><span class="sxs-lookup"><span data-stu-id="86e4e-203">-2146824190</span></span><br />
<span data-ttu-id="86e4e-204">0x800A1002</span><span class="sxs-lookup"><span data-stu-id="86e4e-204">0x800A1002</span></span></p></td>
<td><p><span data-ttu-id="86e4e-205">Не удается обновить базу данных.</span><span class="sxs-lookup"><span data-stu-id="86e4e-205">Unable to update database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86e4e-206"><strong>IDS_URLMONNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="86e4e-206"><strong>IDS_URLMONNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="86e4e-207">4119</span><span class="sxs-lookup"><span data-stu-id="86e4e-207">4119</span></span><br />
<span data-ttu-id="86e4e-208">— 2146824169</span><span class="sxs-lookup"><span data-stu-id="86e4e-208">-2146824169</span></span><br />
<span data-ttu-id="86e4e-209">0x800A1017</span><span class="sxs-lookup"><span data-stu-id="86e4e-209">0x800A1017</span></span></p></td>
<td><p><span data-ttu-id="86e4e-210">Для свойства <strong>URL-адрес</strong> элемента управления файлом требуется системный файл Urlmon. dll, который не удается найти.</span><span class="sxs-lookup"><span data-stu-id="86e4e-210">DataControl <strong>URL</strong> property requires the system file Urlmon.dll, which cannot be found.</span></span></p></td>
</tr>
</tbody>
</table>

