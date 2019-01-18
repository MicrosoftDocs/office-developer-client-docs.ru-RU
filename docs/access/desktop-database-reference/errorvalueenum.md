---
title: ErrorValueEnum (Справочник по для настольных баз данных Access)
TOCTitle: ErrorValueEnum
ms:assetid: 2af99f32-6004-1225-367c-45d693f447b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249058(v=office.15)
ms:contentKeyID: 48543921
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c2d4207f157d361f3b8aba2ff80f46d06b2f328e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717666"
---
# <a name="errorvalueenum"></a><span data-ttu-id="9bde6-102">ErrorValueEnum</span><span class="sxs-lookup"><span data-stu-id="9bde6-102">ErrorValueEnum</span></span>

<span data-ttu-id="9bde6-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9bde6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9bde6-104">Указывает тип ADO ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="9bde6-104">Specifies the type of ADO run-time error.</span></span>

<span data-ttu-id="9bde6-105">Перечислены три формы номеру ошибки.</span><span class="sxs-lookup"><span data-stu-id="9bde6-105">Three forms of the error number are listed:</span></span>

- <span data-ttu-id="9bde6-106">Положительное десятичное число — низкий два байта полный номер в десятичном формате.</span><span class="sxs-lookup"><span data-stu-id="9bde6-106">Positive decimal — the low two bytes of the full number in decimal format.</span></span> <span data-ttu-id="9bde6-107">Этот номер отображается в диалоговом окне по умолчанию сообщения об ошибках Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9bde6-107">This number is displayed in the default Visual Basic error message dialog box.</span></span> <span data-ttu-id="9bde6-108">Например ошибка во время выполнения "3707".</span><span class="sxs-lookup"><span data-stu-id="9bde6-108">For example, Run-time error '3707'.</span></span>

- <span data-ttu-id="9bde6-109">Знаков после запятой отрицательные — decimal перевода полного ошибка с номером.</span><span class="sxs-lookup"><span data-stu-id="9bde6-109">Negative decimal — The decimal translation of the full error number.</span></span>

- <span data-ttu-id="9bde6-110">Шестнадцатеричном представлении — Шестнадцатеричное представление полного ошибка с номером.</span><span class="sxs-lookup"><span data-stu-id="9bde6-110">Hexadecimal — The hexadecimal representation of the full error number.</span></span> <span data-ttu-id="9bde6-111">Код устройства Windows — в четвертой из цифр.</span><span class="sxs-lookup"><span data-stu-id="9bde6-111">The Windows facility code is in the fourth digit.</span></span> <span data-ttu-id="9bde6-112">Код средства для номеров ошибка ADO — *A*. Например: 0E7B 0x800***A***.</span><span class="sxs-lookup"><span data-stu-id="9bde6-112">The facility code for ADO error numbers is *A*. For example: 0x800***A***0E7B.</span></span>

> [!NOTE]
> <span data-ttu-id="9bde6-113">OLE DB ошибки могут передаваться в приложение ADO.</span><span class="sxs-lookup"><span data-stu-id="9bde6-113">OLE DB errors may be passed to your ADO application.</span></span> <span data-ttu-id="9bde6-114">Как правило их можно определить по код устройства Windows *4*.</span><span class="sxs-lookup"><span data-stu-id="9bde6-114">Typically, these can be identified by a Windows facility code of *4*.</span></span> <span data-ttu-id="9bde6-115">Например**4**_ 0x800_... Дополнительные сведения об этих номеров см из *Справочник программиста OLE DB.*</span><span class="sxs-lookup"><span data-stu-id="9bde6-115">For example, 0x800_**4**_.... For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9bde6-116">Константа</span><span class="sxs-lookup"><span data-stu-id="9bde6-116">Constant</span></span></p></th>
<th><p><span data-ttu-id="9bde6-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9bde6-117">Value</span></span></p></th>
<th><p><span data-ttu-id="9bde6-118">Описание</span><span class="sxs-lookup"><span data-stu-id="9bde6-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-119"><strong>adErrBoundToCommand</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-119"><strong>adErrBoundToCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-120">3707</span><span class="sxs-lookup"><span data-stu-id="9bde6-120">3707</span></span><br />
<span data-ttu-id="9bde6-121">-2146824581</span><span class="sxs-lookup"><span data-stu-id="9bde6-121">-2146824581</span></span><br />
<span data-ttu-id="9bde6-122">0x800A0E7B</span><span class="sxs-lookup"><span data-stu-id="9bde6-122">0x800A0E7B</span></span></p></td>
<td><p><span data-ttu-id="9bde6-123">Невозможно изменить свойство <strong>ActiveConnection</strong> объекта <strong>набора записей</strong> , который содержит объект <strong>команды</strong> в качестве источника.</span><span class="sxs-lookup"><span data-stu-id="9bde6-123">Cannot change the <strong>ActiveConnection</strong> property of a <strong>Recordset</strong> object which has a <strong>Command</strong> object as its source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-124"><strong>adErrCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-124"><strong>adErrCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-125">3732</span><span class="sxs-lookup"><span data-stu-id="9bde6-125">3732</span></span><br />
<span data-ttu-id="9bde6-126">-2146824556</span><span class="sxs-lookup"><span data-stu-id="9bde6-126">-2146824556</span></span><br />
<span data-ttu-id="9bde6-127">0x800A0E94</span><span class="sxs-lookup"><span data-stu-id="9bde6-127">0x800A0E94</span></span></p></td>
<td><p><span data-ttu-id="9bde6-128">Сервер не может завершить операцию.</span><span class="sxs-lookup"><span data-stu-id="9bde6-128">Server cannot complete the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-129"><strong>adErrCantChangeConnection</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-129"><strong>adErrCantChangeConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-130">3748</span><span class="sxs-lookup"><span data-stu-id="9bde6-130">3748</span></span><br />
<span data-ttu-id="9bde6-131">-2146824540</span><span class="sxs-lookup"><span data-stu-id="9bde6-131">-2146824540</span></span><br />
<span data-ttu-id="9bde6-132">0x800A0EA4</span><span class="sxs-lookup"><span data-stu-id="9bde6-132">0x800A0EA4</span></span></p></td>
<td><p><span data-ttu-id="9bde6-133">Подключение было запрещено.</span><span class="sxs-lookup"><span data-stu-id="9bde6-133">Connection was denied.</span></span> <span data-ttu-id="9bde6-134">Новое подключение запрошенный имеет разные характеристики, чем в уже используется.</span><span class="sxs-lookup"><span data-stu-id="9bde6-134">New connection you requested has different characteristics than the one already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-135"><strong>adErrCantChangeProvider</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-135"><strong>adErrCantChangeProvider</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-136">3220</span><span class="sxs-lookup"><span data-stu-id="9bde6-136">3220</span></span><br />
<span data-ttu-id="9bde6-137">-2146825068</span><span class="sxs-lookup"><span data-stu-id="9bde6-137">-2146825068</span></span><br />
<span data-ttu-id="9bde6-138">0X800A0C94</span><span class="sxs-lookup"><span data-stu-id="9bde6-138">0X800A0C94</span></span></p></td>
<td><p><span data-ttu-id="9bde6-139">Заданный поставщик отличается от одной уже для использования.</span><span class="sxs-lookup"><span data-stu-id="9bde6-139">Supplied provider is different from the one already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-140"><strong>adErrCantConvertvalue</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-140"><strong>adErrCantConvertvalue</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-141">3724</span><span class="sxs-lookup"><span data-stu-id="9bde6-141">3724</span></span><br />
<span data-ttu-id="9bde6-142">-2146824564</span><span class="sxs-lookup"><span data-stu-id="9bde6-142">-2146824564</span></span><br />
<span data-ttu-id="9bde6-143">0x800A0E8C</span><span class="sxs-lookup"><span data-stu-id="9bde6-143">0x800A0E8C</span></span></p></td>
<td><p><span data-ttu-id="9bde6-144">Невозможно преобразовать значение данных по причине, отличной от несоответствия знака или данных переполнения.</span><span class="sxs-lookup"><span data-stu-id="9bde6-144">Data value cannot be converted for reasons other than sign mismatch or data overflow.</span></span> <span data-ttu-id="9bde6-145">Например, для преобразования будет усечено данных.</span><span class="sxs-lookup"><span data-stu-id="9bde6-145">For example, conversion would have truncated data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-146"><strong>adErrCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-146"><strong>adErrCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-147">3725</span><span class="sxs-lookup"><span data-stu-id="9bde6-147">3725</span></span><br />
<span data-ttu-id="9bde6-148">-2146824563</span><span class="sxs-lookup"><span data-stu-id="9bde6-148">-2146824563</span></span><br />
<span data-ttu-id="9bde6-149">0x800A0E8D</span><span class="sxs-lookup"><span data-stu-id="9bde6-149">0x800A0E8D</span></span></p></td>
<td><p><span data-ttu-id="9bde6-150">Значение данных не может быть задана или получена так, как тип данных поля неизвестно или должен недостаточно ресурсов для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="9bde6-150">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-151"><strong>adErrCatalogNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-151"><strong>adErrCatalogNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-152">3747</span><span class="sxs-lookup"><span data-stu-id="9bde6-152">3747</span></span><br />
<span data-ttu-id="9bde6-153">-2146824541</span><span class="sxs-lookup"><span data-stu-id="9bde6-153">-2146824541</span></span><br />
<span data-ttu-id="9bde6-154">0x800A0EA3</span><span class="sxs-lookup"><span data-stu-id="9bde6-154">0x800A0EA3</span></span></p></td>
<td><p><span data-ttu-id="9bde6-155">Операции требуется допустимый <strong>ParentCatalog</strong>.</span><span class="sxs-lookup"><span data-stu-id="9bde6-155">Operation requires a valid <strong>ParentCatalog</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-156"><strong>adErrColumnNotOnThisRow</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-156"><strong>adErrColumnNotOnThisRow</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-157">3726</span><span class="sxs-lookup"><span data-stu-id="9bde6-157">3726</span></span><br />
<span data-ttu-id="9bde6-158">-2146824562</span><span class="sxs-lookup"><span data-stu-id="9bde6-158">-2146824562</span></span><br />
<span data-ttu-id="9bde6-159">0x800A0E8E</span><span class="sxs-lookup"><span data-stu-id="9bde6-159">0x800A0E8E</span></span></p></td>
<td><p><span data-ttu-id="9bde6-160">Запись не содержит это поле.</span><span class="sxs-lookup"><span data-stu-id="9bde6-160">Record does not contain this field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-161"><strong>adErrDataConversion</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-161"><strong>adErrDataConversion</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-162">3421</span><span class="sxs-lookup"><span data-stu-id="9bde6-162">3421</span></span><br />
<span data-ttu-id="9bde6-163">-2146824867</span><span class="sxs-lookup"><span data-stu-id="9bde6-163">-2146824867</span></span><br />
<span data-ttu-id="9bde6-164">0x800A0D5D</span><span class="sxs-lookup"><span data-stu-id="9bde6-164">0x800A0D5D</span></span></p></td>
<td><p><span data-ttu-id="9bde6-165">Приложение использует значение недопустимого типа для текущей операции.</span><span class="sxs-lookup"><span data-stu-id="9bde6-165">Application uses a value of the wrong type for the current operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-166"><strong>adErrDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-166"><strong>adErrDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-167">3721</span><span class="sxs-lookup"><span data-stu-id="9bde6-167">3721</span></span><br />
<span data-ttu-id="9bde6-168">-2146824567</span><span class="sxs-lookup"><span data-stu-id="9bde6-168">-2146824567</span></span><br />
<span data-ttu-id="9bde6-169">0x800A0E89</span><span class="sxs-lookup"><span data-stu-id="9bde6-169">0x800A0E89</span></span></p></td>
<td><p><span data-ttu-id="9bde6-170">Значение данных слишком велик для представления по типу данных поля.</span><span class="sxs-lookup"><span data-stu-id="9bde6-170">Data value is too large to be represented by the field data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-171"><strong>adErrDelResOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-171"><strong>adErrDelResOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-172">3738</span><span class="sxs-lookup"><span data-stu-id="9bde6-172">3738</span></span><br />
<span data-ttu-id="9bde6-173">-2146824550</span><span class="sxs-lookup"><span data-stu-id="9bde6-173">-2146824550</span></span><br />
<span data-ttu-id="9bde6-174">0x800A0E9A</span><span class="sxs-lookup"><span data-stu-id="9bde6-174">0x800A0E9A</span></span></p></td>
<td><p><span data-ttu-id="9bde6-175">URL-адрес объекта к удалению выходит за рамки текущей записи.</span><span class="sxs-lookup"><span data-stu-id="9bde6-175">URL of the object to be deleted is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-176"><strong>adErrDenyNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-176"><strong>adErrDenyNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-177">3750</span><span class="sxs-lookup"><span data-stu-id="9bde6-177">3750</span></span><br />
<span data-ttu-id="9bde6-178">-2146824538</span><span class="sxs-lookup"><span data-stu-id="9bde6-178">-2146824538</span></span><br />
<span data-ttu-id="9bde6-179">0x800A0EA6</span><span class="sxs-lookup"><span data-stu-id="9bde6-179">0x800A0EA6</span></span></p></td>
<td><p><span data-ttu-id="9bde6-180">Поставщик не поддерживает ограничения общего доступа.</span><span class="sxs-lookup"><span data-stu-id="9bde6-180">Provider does not support sharing restrictions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-181"><strong>adErrDenyTypeNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-181"><strong>adErrDenyTypeNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-182">3751</span><span class="sxs-lookup"><span data-stu-id="9bde6-182">3751</span></span><br />
<span data-ttu-id="9bde6-183">-2146824537</span><span class="sxs-lookup"><span data-stu-id="9bde6-183">-2146824537</span></span><br />
<span data-ttu-id="9bde6-184">0x800A0EA7</span><span class="sxs-lookup"><span data-stu-id="9bde6-184">0x800A0EA7</span></span></p></td>
<td><p><span data-ttu-id="9bde6-185">Поставщик не поддерживает запрошенный тип общего доступа к ограничение.</span><span class="sxs-lookup"><span data-stu-id="9bde6-185">Provider does not support the requested kind of sharing restriction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-186"><strong>adErrFeatureNotAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-186"><strong>adErrFeatureNotAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-187">3251</span><span class="sxs-lookup"><span data-stu-id="9bde6-187">3251</span></span><br />
<span data-ttu-id="9bde6-188">-2146825037</span><span class="sxs-lookup"><span data-stu-id="9bde6-188">-2146825037</span></span><br />
<span data-ttu-id="9bde6-189">0x800A0CB3</span><span class="sxs-lookup"><span data-stu-id="9bde6-189">0x800A0CB3</span></span></p></td>
<td><p><span data-ttu-id="9bde6-190">Объект или поставщик не может выполнить запрошенную операцию.</span><span class="sxs-lookup"><span data-stu-id="9bde6-190">Object or provider is not capable of performing requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-191"><strong>adErrFieldsUpdateFailed</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-191"><strong>adErrFieldsUpdateFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-192">3749</span><span class="sxs-lookup"><span data-stu-id="9bde6-192">3749</span></span><br />
<span data-ttu-id="9bde6-193">-2146824539</span><span class="sxs-lookup"><span data-stu-id="9bde6-193">-2146824539</span></span><br />
<span data-ttu-id="9bde6-194">0x800A0EA5</span><span class="sxs-lookup"><span data-stu-id="9bde6-194">0x800A0EA5</span></span></p></td>
<td><p><span data-ttu-id="9bde6-195">Не удалось обновить поля.</span><span class="sxs-lookup"><span data-stu-id="9bde6-195">Fields update failed.</span></span> <span data-ttu-id="9bde6-196">Для получения дополнительных сведений проверьте свойство <strong>Status</strong> объектов отдельного поля.</span><span class="sxs-lookup"><span data-stu-id="9bde6-196">For further information, examine the <strong>Status</strong> property of individual field objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-197"><strong>adErrIllegalOperation</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-197"><strong>adErrIllegalOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-198">3219</span><span class="sxs-lookup"><span data-stu-id="9bde6-198">3219</span></span><br />
<span data-ttu-id="9bde6-199">-2146825069</span><span class="sxs-lookup"><span data-stu-id="9bde6-199">-2146825069</span></span><br />
<span data-ttu-id="9bde6-200">0x800A0C93</span><span class="sxs-lookup"><span data-stu-id="9bde6-200">0x800A0C93</span></span></p></td>
<td><p><span data-ttu-id="9bde6-201">Операция не допускается в данном контексте.</span><span class="sxs-lookup"><span data-stu-id="9bde6-201">Operation is not allowed in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-202"><strong>adErrIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-202"><strong>adErrIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-203">3719</span><span class="sxs-lookup"><span data-stu-id="9bde6-203">3719</span></span><br />
<span data-ttu-id="9bde6-204">-2146824569</span><span class="sxs-lookup"><span data-stu-id="9bde6-204">-2146824569</span></span><br />
<span data-ttu-id="9bde6-205">0x800A0E87</span><span class="sxs-lookup"><span data-stu-id="9bde6-205">0x800A0E87</span></span></p></td>
<td><p><span data-ttu-id="9bde6-206">Данные значения конфликтует с ограничения целостности поля.</span><span class="sxs-lookup"><span data-stu-id="9bde6-206">Data value conflicts with the integrity constraints of the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-207"><strong>adErrInTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-207"><strong>adErrInTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-208">3246</span><span class="sxs-lookup"><span data-stu-id="9bde6-208">3246</span></span><br />
<span data-ttu-id="9bde6-209">-2146825042</span><span class="sxs-lookup"><span data-stu-id="9bde6-209">-2146825042</span></span><br />
<span data-ttu-id="9bde6-210">0x800A0CAE</span><span class="sxs-lookup"><span data-stu-id="9bde6-210">0x800A0CAE</span></span></p></td>
<td><p><span data-ttu-id="9bde6-211">Объект <strong>подключения</strong> не может быть закрыт явным образом в транзакции.</span><span class="sxs-lookup"><span data-stu-id="9bde6-211"><strong>Connection</strong> object cannot be explicitly closed while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-212"><strong>adErrInvalidArgument</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-212"><strong>adErrInvalidArgument</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-213">3001</span><span class="sxs-lookup"><span data-stu-id="9bde6-213">3001</span></span><br />
<span data-ttu-id="9bde6-214">-2146825287</span><span class="sxs-lookup"><span data-stu-id="9bde6-214">-2146825287</span></span><br />
<span data-ttu-id="9bde6-215">0x800A0BB9</span><span class="sxs-lookup"><span data-stu-id="9bde6-215">0x800A0BB9</span></span></p></td>
<td><p><span data-ttu-id="9bde6-216">Аргументы имеют неправильный тип, находятся вне допустимого диапазона или конфликтуют друг с другом.</span><span class="sxs-lookup"><span data-stu-id="9bde6-216">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-217"><strong>adErrInvalidConnection</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-217"><strong>adErrInvalidConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-218">3709</span><span class="sxs-lookup"><span data-stu-id="9bde6-218">3709</span></span><br />
<span data-ttu-id="9bde6-219">-2146824579</span><span class="sxs-lookup"><span data-stu-id="9bde6-219">-2146824579</span></span><br />
<span data-ttu-id="9bde6-220">0x800A0E7D</span><span class="sxs-lookup"><span data-stu-id="9bde6-220">0x800A0E7D</span></span></p></td>
<td><p><span data-ttu-id="9bde6-221">Подключение не может использоваться для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="9bde6-221">The connection cannot be used to perform this operation.</span></span> <span data-ttu-id="9bde6-222">Он является закрытой или недопустимый в данном контексте.</span><span class="sxs-lookup"><span data-stu-id="9bde6-222">It is either closed or invalid in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-223"><strong>adErrInvalidParamInfo</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-223"><strong>adErrInvalidParamInfo</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-224">3708</span><span class="sxs-lookup"><span data-stu-id="9bde6-224">3708</span></span><br />
<span data-ttu-id="9bde6-225">-2146824580</span><span class="sxs-lookup"><span data-stu-id="9bde6-225">-2146824580</span></span><br />
<span data-ttu-id="9bde6-226">0x800A0E7C</span><span class="sxs-lookup"><span data-stu-id="9bde6-226">0x800A0E7C</span></span></p></td>
<td><p><span data-ttu-id="9bde6-227">Объект <strong>параметра</strong> определен неправильно.</span><span class="sxs-lookup"><span data-stu-id="9bde6-227"><strong>Parameter</strong> object is improperly defined.</span></span> <span data-ttu-id="9bde6-228">Несогласованные или неполные сведения отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="9bde6-228">Inconsistent or incomplete information was provided.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-229"><strong>adErrInvalidTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-229"><strong>adErrInvalidTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-230">3714</span><span class="sxs-lookup"><span data-stu-id="9bde6-230">3714</span></span><br />
<span data-ttu-id="9bde6-231">-2146824574</span><span class="sxs-lookup"><span data-stu-id="9bde6-231">-2146824574</span></span><br />
<span data-ttu-id="9bde6-232">0x800A0E82</span><span class="sxs-lookup"><span data-stu-id="9bde6-232">0x800A0E82</span></span></p></td>
<td><p><span data-ttu-id="9bde6-233">Координирование транзакций является недопустимым или не запущен.</span><span class="sxs-lookup"><span data-stu-id="9bde6-233">Coordinating transaction is invalid or has not started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-234"><strong>adErrInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-234"><strong>adErrInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-235">3729</span><span class="sxs-lookup"><span data-stu-id="9bde6-235">3729</span></span><br />
<span data-ttu-id="9bde6-236">-2146824559</span><span class="sxs-lookup"><span data-stu-id="9bde6-236">-2146824559</span></span><br />
<span data-ttu-id="9bde6-237">0x800A0E91</span><span class="sxs-lookup"><span data-stu-id="9bde6-237">0x800A0E91</span></span></p></td>
<td><p><span data-ttu-id="9bde6-238">URL-адрес содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="9bde6-238">URL contains invalid characters.</span></span> <span data-ttu-id="9bde6-239">Убедитесь в том, что URL-адрес введен правильно.</span><span class="sxs-lookup"><span data-stu-id="9bde6-239">Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-240"><strong>adErrItemNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-240"><strong>adErrItemNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-241">3265</span><span class="sxs-lookup"><span data-stu-id="9bde6-241">3265</span></span><br />
<span data-ttu-id="9bde6-242">-2146825023</span><span class="sxs-lookup"><span data-stu-id="9bde6-242">-2146825023</span></span><br />
<span data-ttu-id="9bde6-243">0x800A0CC1</span><span class="sxs-lookup"><span data-stu-id="9bde6-243">0x800A0CC1</span></span></p></td>
<td><p><span data-ttu-id="9bde6-244">Не удается найти элемента в коллекции, соответствующий запрошенные имя или порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="9bde6-244">Item cannot be found in the collection corresponding to the requested name or ordinal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-245"><strong>adErrNoCurrentRecord</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-245"><strong>adErrNoCurrentRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-246">3021</span><span class="sxs-lookup"><span data-stu-id="9bde6-246">3021</span></span><br />
<span data-ttu-id="9bde6-247">-2146825267</span><span class="sxs-lookup"><span data-stu-id="9bde6-247">-2146825267</span></span><br />
<span data-ttu-id="9bde6-248">0x800A0BCD</span><span class="sxs-lookup"><span data-stu-id="9bde6-248">0x800A0BCD</span></span></p></td>
<td><p><span data-ttu-id="9bde6-249"><strong>BOF</strong> или <strong>EOF</strong> имеет значение True или текущей запись была удалена.</span><span class="sxs-lookup"><span data-stu-id="9bde6-249">Either <strong>BOF</strong> or <strong>EOF</strong> is True, or the current record has been deleted.</span></span> <span data-ttu-id="9bde6-250">Запрошенная операция требует текущей записи.</span><span class="sxs-lookup"><span data-stu-id="9bde6-250">Requested operation requires a current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-251"><strong>adErrNotExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-251"><strong>adErrNotExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-252">3715</span><span class="sxs-lookup"><span data-stu-id="9bde6-252">3715</span></span><br />
<span data-ttu-id="9bde6-253">-2146824573</span><span class="sxs-lookup"><span data-stu-id="9bde6-253">-2146824573</span></span><br />
<span data-ttu-id="9bde6-254">0x800A0E83</span><span class="sxs-lookup"><span data-stu-id="9bde6-254">0x800A0E83</span></span></p></td>
<td><p><span data-ttu-id="9bde6-255">Невозможно выполнить операцию во время не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9bde6-255">Operation cannot be performed while not executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-256"><strong>adErrNotReentrant</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-256"><strong>adErrNotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-257">3710</span><span class="sxs-lookup"><span data-stu-id="9bde6-257">3710</span></span><br />
<span data-ttu-id="9bde6-258">-2146824578</span><span class="sxs-lookup"><span data-stu-id="9bde6-258">-2146824578</span></span><br />
<span data-ttu-id="9bde6-259">0x800A0E7E</span><span class="sxs-lookup"><span data-stu-id="9bde6-259">0x800A0E7E</span></span></p></td>
<td><p><span data-ttu-id="9bde6-260">Невозможно выполнить операцию во время обработки событий.</span><span class="sxs-lookup"><span data-stu-id="9bde6-260">Operation cannot be performed while processing event.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-261"><strong>adErrObjectClosed</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-261"><strong>adErrObjectClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-262">3704</span><span class="sxs-lookup"><span data-stu-id="9bde6-262">3704</span></span><br />
<span data-ttu-id="9bde6-263">-2146824584</span><span class="sxs-lookup"><span data-stu-id="9bde6-263">-2146824584</span></span><br />
<span data-ttu-id="9bde6-264">0x800A0E78</span><span class="sxs-lookup"><span data-stu-id="9bde6-264">0x800A0E78</span></span></p></td>
<td><p><span data-ttu-id="9bde6-265">Операция не допускается при закрытии объекта.</span><span class="sxs-lookup"><span data-stu-id="9bde6-265">Operation is not allowed when the object is closed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-266"><strong>adErrObjectInCollection</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-266"><strong>adErrObjectInCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-267">3367</span><span class="sxs-lookup"><span data-stu-id="9bde6-267">3367</span></span><br />
<span data-ttu-id="9bde6-268">-2146824921</span><span class="sxs-lookup"><span data-stu-id="9bde6-268">-2146824921</span></span><br />
<span data-ttu-id="9bde6-269">0x800A0D27</span><span class="sxs-lookup"><span data-stu-id="9bde6-269">0x800A0D27</span></span></p></td>
<td><p><span data-ttu-id="9bde6-270">Объект уже присутствует в коллекции.</span><span class="sxs-lookup"><span data-stu-id="9bde6-270">Object is already in collection.</span></span> <span data-ttu-id="9bde6-271">Не удается добавить.</span><span class="sxs-lookup"><span data-stu-id="9bde6-271">Cannot append.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-272"><strong>adErrObjectNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-272"><strong>adErrObjectNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-273">3420</span><span class="sxs-lookup"><span data-stu-id="9bde6-273">3420</span></span><br />
<span data-ttu-id="9bde6-274">-2146824868</span><span class="sxs-lookup"><span data-stu-id="9bde6-274">-2146824868</span></span><br />
<span data-ttu-id="9bde6-275">0x800A0D5C</span><span class="sxs-lookup"><span data-stu-id="9bde6-275">0x800A0D5C</span></span></p></td>
<td><p><span data-ttu-id="9bde6-276">Объект больше не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="9bde6-276">Object is no longer valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-277"><strong>adErrObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-277"><strong>adErrObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-278">3705</span><span class="sxs-lookup"><span data-stu-id="9bde6-278">3705</span></span><br />
<span data-ttu-id="9bde6-279">-2146824583</span><span class="sxs-lookup"><span data-stu-id="9bde6-279">-2146824583</span></span><br />
<span data-ttu-id="9bde6-280">0x800A0E79</span><span class="sxs-lookup"><span data-stu-id="9bde6-280">0x800A0E79</span></span></p></td>
<td><p><span data-ttu-id="9bde6-281">Операция не разрешена, когда объект открыт.</span><span class="sxs-lookup"><span data-stu-id="9bde6-281">Operation is not allowed when the object is open.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-282"><strong>adErrOpeningFile</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-282"><strong>adErrOpeningFile</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-283">3002</span><span class="sxs-lookup"><span data-stu-id="9bde6-283">3002</span></span><br />
<span data-ttu-id="9bde6-284">-2146825286</span><span class="sxs-lookup"><span data-stu-id="9bde6-284">-2146825286</span></span><br />
<span data-ttu-id="9bde6-285">0x800A0BBA</span><span class="sxs-lookup"><span data-stu-id="9bde6-285">0x800A0BBA</span></span></p></td>
<td><p><span data-ttu-id="9bde6-286">Не удается открыть файл.</span><span class="sxs-lookup"><span data-stu-id="9bde6-286">File could not be opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-287"><strong>adErrOperationCancelled</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-287"><strong>adErrOperationCancelled</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-288">3712</span><span class="sxs-lookup"><span data-stu-id="9bde6-288">3712</span></span><br />
<span data-ttu-id="9bde6-289">-2146824576</span><span class="sxs-lookup"><span data-stu-id="9bde6-289">-2146824576</span></span><br />
<span data-ttu-id="9bde6-290">0x800A0E80</span><span class="sxs-lookup"><span data-stu-id="9bde6-290">0x800A0E80</span></span></p></td>
<td><p><span data-ttu-id="9bde6-291">Операция отменена пользователем.</span><span class="sxs-lookup"><span data-stu-id="9bde6-291">Operation has been cancelled by the user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-292"><strong>adErrOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-292"><strong>adErrOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-293">3734</span><span class="sxs-lookup"><span data-stu-id="9bde6-293">3734</span></span><br />
<span data-ttu-id="9bde6-294">-2146824554</span><span class="sxs-lookup"><span data-stu-id="9bde6-294">-2146824554</span></span><br />
<span data-ttu-id="9bde6-295">0x800A0E96</span><span class="sxs-lookup"><span data-stu-id="9bde6-295">0x800A0E96</span></span></p></td>
<td><p><span data-ttu-id="9bde6-296">Невозможно выполнить операцию.</span><span class="sxs-lookup"><span data-stu-id="9bde6-296">Operation cannot be performed.</span></span> <span data-ttu-id="9bde6-297">Поставщик не удается получить достаточно дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="9bde6-297">Provider cannot obtain enough storage space.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-298"><strong>adErrPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-298"><strong>adErrPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-299">3720</span><span class="sxs-lookup"><span data-stu-id="9bde6-299">3720</span></span><br />
<span data-ttu-id="9bde6-300">-2146824568</span><span class="sxs-lookup"><span data-stu-id="9bde6-300">-2146824568</span></span><br />
<span data-ttu-id="9bde6-301">0x800A0E88</span><span class="sxs-lookup"><span data-stu-id="9bde6-301">0x800A0E88</span></span></p></td>
<td><p><span data-ttu-id="9bde6-302">Недостаточно разрешений не позволяет записи в поле.</span><span class="sxs-lookup"><span data-stu-id="9bde6-302">Insufficent permission prevents writing to the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-303"><strong>adErrProviderFailed</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-303"><strong>adErrProviderFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-304">3000</span><span class="sxs-lookup"><span data-stu-id="9bde6-304">3000</span></span><br />
<span data-ttu-id="9bde6-305">-2146825288</span><span class="sxs-lookup"><span data-stu-id="9bde6-305">-2146825288</span></span><br />
<span data-ttu-id="9bde6-306">0x800A0BB8</span><span class="sxs-lookup"><span data-stu-id="9bde6-306">0x800A0BB8</span></span></p></td>
<td><p><span data-ttu-id="9bde6-307">Не удалось выполнить запрошенную операцию поставщика.</span><span class="sxs-lookup"><span data-stu-id="9bde6-307">Provider failed to perform the requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-308"><strong>adErrProviderNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-308"><strong>adErrProviderNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-309">3706</span><span class="sxs-lookup"><span data-stu-id="9bde6-309">3706</span></span><br />
<span data-ttu-id="9bde6-310">-2146824582</span><span class="sxs-lookup"><span data-stu-id="9bde6-310">-2146824582</span></span><br />
<span data-ttu-id="9bde6-311">0x800A0E7A</span><span class="sxs-lookup"><span data-stu-id="9bde6-311">0x800A0E7A</span></span></p></td>
<td><p><span data-ttu-id="9bde6-312">Не удается найти поставщика.</span><span class="sxs-lookup"><span data-stu-id="9bde6-312">Provider cannot be found.</span></span> <span data-ttu-id="9bde6-313">Она может быть установлено неправильно.</span><span class="sxs-lookup"><span data-stu-id="9bde6-313">It may not be properly installed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-314"><strong>adErrReadFile</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-314"><strong>adErrReadFile</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-315">3003</span><span class="sxs-lookup"><span data-stu-id="9bde6-315">3003</span></span><br />
<span data-ttu-id="9bde6-316">-2146825285</span><span class="sxs-lookup"><span data-stu-id="9bde6-316">-2146825285</span></span><br />
<span data-ttu-id="9bde6-317">0x800A0BBB</span><span class="sxs-lookup"><span data-stu-id="9bde6-317">0x800A0BBB</span></span></p></td>
<td><p><span data-ttu-id="9bde6-318">Не удалось прочитать файл.</span><span class="sxs-lookup"><span data-stu-id="9bde6-318">File could not be read.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-319"><strong>adErrResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-319"><strong>adErrResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-320">3731</span><span class="sxs-lookup"><span data-stu-id="9bde6-320">3731</span></span><br />
<span data-ttu-id="9bde6-321">-2146824557</span><span class="sxs-lookup"><span data-stu-id="9bde6-321">-2146824557</span></span><br />
<span data-ttu-id="9bde6-322">0x800A0E93</span><span class="sxs-lookup"><span data-stu-id="9bde6-322">0x800A0E93</span></span></p></td>
<td><p><span data-ttu-id="9bde6-323">Невозможно выполнить операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="9bde6-323">Copy operation cannot be performed.</span></span> <span data-ttu-id="9bde6-324">Объект с именем, URL-адрес назначения уже существует.</span><span class="sxs-lookup"><span data-stu-id="9bde6-324">Object named by destination URL already exists.</span></span> <span data-ttu-id="9bde6-325">Укажите <strong>adCopyOverwrite</strong> объект.</span><span class="sxs-lookup"><span data-stu-id="9bde6-325">Specify <strong>adCopyOverwrite</strong> to replace the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-326"><strong>adErrResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-326"><strong>adErrResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-327">3730</span><span class="sxs-lookup"><span data-stu-id="9bde6-327">3730</span></span><br />
<span data-ttu-id="9bde6-328">-2146824558</span><span class="sxs-lookup"><span data-stu-id="9bde6-328">-2146824558</span></span><br />
<span data-ttu-id="9bde6-329">0x800A0E92</span><span class="sxs-lookup"><span data-stu-id="9bde6-329">0x800A0E92</span></span></p></td>
<td><p><span data-ttu-id="9bde6-330">Объект, представленный указанным URL-адрес заблокирован один или несколько других процессов.</span><span class="sxs-lookup"><span data-stu-id="9bde6-330">Object represented by the specified URL is locked by one or more other processes.</span></span> <span data-ttu-id="9bde6-331">Дождитесь завершения процесса и повторите попытку выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="9bde6-331">Wait until the process has finished and attempt the operation again.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-332"><strong>adErrResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-332"><strong>adErrResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-333">3735</span><span class="sxs-lookup"><span data-stu-id="9bde6-333">3735</span></span><br />
<span data-ttu-id="9bde6-334">-2146824553</span><span class="sxs-lookup"><span data-stu-id="9bde6-334">-2146824553</span></span><br />
<span data-ttu-id="9bde6-335">0x800A0E97</span><span class="sxs-lookup"><span data-stu-id="9bde6-335">0x800A0E97</span></span></p></td>
<td><p><span data-ttu-id="9bde6-336">URL-адрес источника и назначения выходит за рамки текущей записи.</span><span class="sxs-lookup"><span data-stu-id="9bde6-336">Source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-337"><strong>adErrSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-337"><strong>adErrSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-338">3722</span><span class="sxs-lookup"><span data-stu-id="9bde6-338">3722</span></span><br />
<span data-ttu-id="9bde6-339">-2146824566</span><span class="sxs-lookup"><span data-stu-id="9bde6-339">-2146824566</span></span><br />
<span data-ttu-id="9bde6-340">0x800A0E8A</span><span class="sxs-lookup"><span data-stu-id="9bde6-340">0x800A0E8A</span></span></p></td>
<td><p><span data-ttu-id="9bde6-341">Данные значения конфликтует с типом данных или ограничения поля.</span><span class="sxs-lookup"><span data-stu-id="9bde6-341">Data value conflicts with the data type or constraints of the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-342"><strong>adErrSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-342"><strong>adErrSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-343">3723</span><span class="sxs-lookup"><span data-stu-id="9bde6-343">3723</span></span><br />
<span data-ttu-id="9bde6-344">-2146824565</span><span class="sxs-lookup"><span data-stu-id="9bde6-344">-2146824565</span></span><br />
<span data-ttu-id="9bde6-345">0x800A0E8B</span><span class="sxs-lookup"><span data-stu-id="9bde6-345">0x800A0E8B</span></span></p></td>
<td><p><span data-ttu-id="9bde6-346">Сбой преобразования, так как значение данных имеет знак, а тип данных поля, используемый поставщиком без знака.</span><span class="sxs-lookup"><span data-stu-id="9bde6-346">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-347"><strong>adErrStillConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-347"><strong>adErrStillConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-348">3713</span><span class="sxs-lookup"><span data-stu-id="9bde6-348">3713</span></span><br />
<span data-ttu-id="9bde6-349">-2146824575</span><span class="sxs-lookup"><span data-stu-id="9bde6-349">-2146824575</span></span><br />
<span data-ttu-id="9bde6-350">0x800A0E81</span><span class="sxs-lookup"><span data-stu-id="9bde6-350">0x800A0E81</span></span></p></td>
<td><p><span data-ttu-id="9bde6-351">Не удается выполнить операцию при подключении aynchronously.</span><span class="sxs-lookup"><span data-stu-id="9bde6-351">Operation cannot be performed while connecting aynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-352"><strong>adErrStillExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-352"><strong>adErrStillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-353">3711</span><span class="sxs-lookup"><span data-stu-id="9bde6-353">3711</span></span><br />
<span data-ttu-id="9bde6-354">-2146824577</span><span class="sxs-lookup"><span data-stu-id="9bde6-354">-2146824577</span></span><br />
<span data-ttu-id="9bde6-355">0x800A0E7F</span><span class="sxs-lookup"><span data-stu-id="9bde6-355">0x800A0E7F</span></span></p></td>
<td><p><span data-ttu-id="9bde6-356">Невозможно выполнить операцию во время выполнения асинхронно.</span><span class="sxs-lookup"><span data-stu-id="9bde6-356">Operation cannot be performed while executing asynchronously.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-357"><strong>adErrTreePermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-357"><strong>adErrTreePermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-358">3728</span><span class="sxs-lookup"><span data-stu-id="9bde6-358">3728</span></span><br />
<span data-ttu-id="9bde6-359">-2146824560</span><span class="sxs-lookup"><span data-stu-id="9bde6-359">-2146824560</span></span><br />
<span data-ttu-id="9bde6-360">0x800A0E90</span><span class="sxs-lookup"><span data-stu-id="9bde6-360">0x800A0E90</span></span></p></td>
<td><p><span data-ttu-id="9bde6-361">Недостаточно разрешений для доступа к дерево или поддерево.</span><span class="sxs-lookup"><span data-stu-id="9bde6-361">Permissions are insufficient to access tree or subtree.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-362"><strong>adErrUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-362"><strong>adErrUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-363">3736</span><span class="sxs-lookup"><span data-stu-id="9bde6-363">3736</span></span><br />
<span data-ttu-id="9bde6-364">-2146824552</span><span class="sxs-lookup"><span data-stu-id="9bde6-364">-2146824552</span></span><br />
<span data-ttu-id="9bde6-365">0x800A0E98</span><span class="sxs-lookup"><span data-stu-id="9bde6-365">0x800A0E98</span></span></p></td>
<td><p><span data-ttu-id="9bde6-366">Не удалось завершить операцию и состояние недоступна.</span><span class="sxs-lookup"><span data-stu-id="9bde6-366">Operation failed to complete and the status is unavailable.</span></span> <span data-ttu-id="9bde6-367">Поле может быть недоступна или не попытка выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="9bde6-367">The field may be unavailable or the operation was not attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-368"><strong>adErrUnsafeOperation</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-368"><strong>adErrUnsafeOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-369">3716</span><span class="sxs-lookup"><span data-stu-id="9bde6-369">3716</span></span><br />
<span data-ttu-id="9bde6-370">-2146824572</span><span class="sxs-lookup"><span data-stu-id="9bde6-370">-2146824572</span></span><br />
<span data-ttu-id="9bde6-371">0x800A0E84</span><span class="sxs-lookup"><span data-stu-id="9bde6-371">0x800A0E84</span></span></p></td>
<td><p><span data-ttu-id="9bde6-372">Параметры безопасности на данном компьютере запрещают доступ к источнику данных в другом домене.</span><span class="sxs-lookup"><span data-stu-id="9bde6-372">Safety settings on this computer prohibit accessing a data source on another domain.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-373"><strong>adErrURLDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-373"><strong>adErrURLDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-374">3727</span><span class="sxs-lookup"><span data-stu-id="9bde6-374">3727</span></span><br />
<span data-ttu-id="9bde6-375">-2146824561</span><span class="sxs-lookup"><span data-stu-id="9bde6-375">-2146824561</span></span><br />
<span data-ttu-id="9bde6-376">0x800A0E8F</span><span class="sxs-lookup"><span data-stu-id="9bde6-376">0x800A0E8F</span></span></p></td>
<td><p><span data-ttu-id="9bde6-377">Исходный URL-адрес или родительский URL-адрес конечного не существует.</span><span class="sxs-lookup"><span data-stu-id="9bde6-377">Either the source URL or the parent of the destination URL does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-378"><strong>adErrURLNamedRowDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-378"><strong>adErrURLNamedRowDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-379">3737</span><span class="sxs-lookup"><span data-stu-id="9bde6-379">3737</span></span><br />
<span data-ttu-id="9bde6-380">-2146824551</span><span class="sxs-lookup"><span data-stu-id="9bde6-380">-2146824551</span></span><br />
<span data-ttu-id="9bde6-381">0x800A0E99</span><span class="sxs-lookup"><span data-stu-id="9bde6-381">0x800A0E99</span></span></p></td>
<td><p><span data-ttu-id="9bde6-382">Запись с именем, этот URL-адрес не существует.</span><span class="sxs-lookup"><span data-stu-id="9bde6-382">Record named by this URL does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-383"><strong>adErrVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-383"><strong>adErrVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-384">3733</span><span class="sxs-lookup"><span data-stu-id="9bde6-384">3733</span></span><br />
<span data-ttu-id="9bde6-385">-2146824555</span><span class="sxs-lookup"><span data-stu-id="9bde6-385">-2146824555</span></span><br />
<span data-ttu-id="9bde6-386">0x800A0E95</span><span class="sxs-lookup"><span data-stu-id="9bde6-386">0x800A0E95</span></span></p></td>
<td><p><span data-ttu-id="9bde6-387">Поставщик может найти запоминающее устройство, указанный в параметре URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="9bde6-387">Provider cannot locate the storage device indicated by the URL.</span></span> <span data-ttu-id="9bde6-388">Убедитесь в том, что URL-адрес введен правильно.</span><span class="sxs-lookup"><span data-stu-id="9bde6-388">Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-389"><strong>adErrWriteFile</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-389"><strong>adErrWriteFile</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-390">3004</span><span class="sxs-lookup"><span data-stu-id="9bde6-390">3004</span></span><br />
<span data-ttu-id="9bde6-391">-2146825284</span><span class="sxs-lookup"><span data-stu-id="9bde6-391">-2146825284</span></span><br />
<span data-ttu-id="9bde6-392">0x800A0BBC</span><span class="sxs-lookup"><span data-stu-id="9bde6-392">0x800A0BBC</span></span></p></td>
<td><p><span data-ttu-id="9bde6-393">Запись в файл не удалось.</span><span class="sxs-lookup"><span data-stu-id="9bde6-393">Write to file failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-394"><strong>adWrnSecurityDialog</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-394"><strong>adWrnSecurityDialog</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-395">3717</span><span class="sxs-lookup"><span data-stu-id="9bde6-395">3717</span></span><br />
<span data-ttu-id="9bde6-396">-2146824571</span><span class="sxs-lookup"><span data-stu-id="9bde6-396">-2146824571</span></span><br />
<span data-ttu-id="9bde6-397">0x800A0E85</span><span class="sxs-lookup"><span data-stu-id="9bde6-397">0x800A0E85</span></span></p></td>
<td><p><span data-ttu-id="9bde6-398">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="9bde6-398">For internal use only.</span></span> <span data-ttu-id="9bde6-399">Не следует использовать.</span><span class="sxs-lookup"><span data-stu-id="9bde6-399">Don't use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-400"><strong>adWrnSecurityDialogHeader</strong></span><span class="sxs-lookup"><span data-stu-id="9bde6-400"><strong>adWrnSecurityDialogHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="9bde6-401">3718</span><span class="sxs-lookup"><span data-stu-id="9bde6-401">3718</span></span><br />
<span data-ttu-id="9bde6-402">-2146824570</span><span class="sxs-lookup"><span data-stu-id="9bde6-402">-2146824570</span></span><br />
<span data-ttu-id="9bde6-403">0x800A0E86</span><span class="sxs-lookup"><span data-stu-id="9bde6-403">0x800A0E86</span></span></p></td>
<td><p><span data-ttu-id="9bde6-404">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="9bde6-404">For internal use only.</span></span> <span data-ttu-id="9bde6-405">Не следует использовать.</span><span class="sxs-lookup"><span data-stu-id="9bde6-405">Don't use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="9bde6-406">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="9bde6-406">ADO/WFC equivalent</span></span>

<span data-ttu-id="9bde6-407">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="9bde6-407">Package: **com.ms.wfc.data**</span></span>

<span data-ttu-id="9bde6-408">Определяются следующие подмножества ADO/WFC эквивалентами.</span><span class="sxs-lookup"><span data-stu-id="9bde6-408">Only the following subsets of ADO/WFC equivalents are defined.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9bde6-409">Константа</span><span class="sxs-lookup"><span data-stu-id="9bde6-409">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-410">AdoEnums.ErrorValue.BOUNDTOCOMMAND</span><span class="sxs-lookup"><span data-stu-id="9bde6-410">AdoEnums.ErrorValue.BOUNDTOCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-411">AdoEnums.ErrorValue.DATACONVERSION</span><span class="sxs-lookup"><span data-stu-id="9bde6-411">AdoEnums.ErrorValue.DATACONVERSION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-412">AdoEnums.ErrorValue.FEATURENOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="9bde6-412">AdoEnums.ErrorValue.FEATURENOTAVAILABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-413">AdoEnums.ErrorValue.ILLEGALOPERATION</span><span class="sxs-lookup"><span data-stu-id="9bde6-413">AdoEnums.ErrorValue.ILLEGALOPERATION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-414">AdoEnums.ErrorValue.INTRANSACTION</span><span class="sxs-lookup"><span data-stu-id="9bde6-414">AdoEnums.ErrorValue.INTRANSACTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-415">AdoEnums.ErrorValue.INVALIDARGUMENT</span><span class="sxs-lookup"><span data-stu-id="9bde6-415">AdoEnums.ErrorValue.INVALIDARGUMENT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-416">AdoEnums.ErrorValue.INVALIDCONNECTION</span><span class="sxs-lookup"><span data-stu-id="9bde6-416">AdoEnums.ErrorValue.INVALIDCONNECTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-417">AdoEnums.ErrorValue.INVALIDPARAMINFO</span><span class="sxs-lookup"><span data-stu-id="9bde6-417">AdoEnums.ErrorValue.INVALIDPARAMINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-418">AdoEnums.ErrorValue.ITEMNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="9bde6-418">AdoEnums.ErrorValue.ITEMNOTFOUND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-419">AdoEnums.ErrorValue.NOCURRENTRECORD</span><span class="sxs-lookup"><span data-stu-id="9bde6-419">AdoEnums.ErrorValue.NOCURRENTRECORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-420">AdoEnums.ErrorValue.NOTEXECUTING</span><span class="sxs-lookup"><span data-stu-id="9bde6-420">AdoEnums.ErrorValue.NOTEXECUTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-421">AdoEnums.ErrorValue.NOTREENTRANT</span><span class="sxs-lookup"><span data-stu-id="9bde6-421">AdoEnums.ErrorValue.NOTREENTRANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-422">AdoEnums.ErrorValue.OBJECTCLOSED</span><span class="sxs-lookup"><span data-stu-id="9bde6-422">AdoEnums.ErrorValue.OBJECTCLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-423">AdoEnums.ErrorValue.OBJECTINCOLLECTION</span><span class="sxs-lookup"><span data-stu-id="9bde6-423">AdoEnums.ErrorValue.OBJECTINCOLLECTION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-424">AdoEnums.ErrorValue.OBJECTNOTSET</span><span class="sxs-lookup"><span data-stu-id="9bde6-424">AdoEnums.ErrorValue.OBJECTNOTSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-425">AdoEnums.ErrorValue.OBJECTOPEN</span><span class="sxs-lookup"><span data-stu-id="9bde6-425">AdoEnums.ErrorValue.OBJECTOPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-426">AdoEnums.ErrorValue.OPERATIONCANCELLED</span><span class="sxs-lookup"><span data-stu-id="9bde6-426">AdoEnums.ErrorValue.OPERATIONCANCELLED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-427">AdoEnums.ErrorValue.PROVIDERNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="9bde6-427">AdoEnums.ErrorValue.PROVIDERNOTFOUND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-428">AdoEnums.ErrorValue.STILLCONNECTING</span><span class="sxs-lookup"><span data-stu-id="9bde6-428">AdoEnums.ErrorValue.STILLCONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bde6-429">AdoEnums.ErrorValue.STILLEXECUTING</span><span class="sxs-lookup"><span data-stu-id="9bde6-429">AdoEnums.ErrorValue.STILLEXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bde6-430">AdoEnums.ErrorValue.UNSAFEOPERATION</span><span class="sxs-lookup"><span data-stu-id="9bde6-430">AdoEnums.ErrorValue.UNSAFEOPERATION</span></span></p></td>
</tr>
</tbody>
</table>

