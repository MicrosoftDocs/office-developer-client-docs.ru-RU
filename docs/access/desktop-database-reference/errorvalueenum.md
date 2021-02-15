---
title: ErrorValueEnum (справочник по базам данных Access для настольных ПК)
TOCTitle: ErrorValueEnum
ms:assetid: 2af99f32-6004-1225-367c-45d693f447b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249058(v=office.15)
ms:contentKeyID: 48543921
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c2d4207f157d361f3b8aba2ff80f46d06b2f328e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293324"
---
# <a name="errorvalueenum"></a><span data-ttu-id="f2f88-102">ErrorValueEnum</span><span class="sxs-lookup"><span data-stu-id="f2f88-102">ErrorValueEnum</span></span>

<span data-ttu-id="f2f88-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2f88-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f2f88-104">Указывает тип ошибки во время работы ADO.</span><span class="sxs-lookup"><span data-stu-id="f2f88-104">Specifies the type of ADO run-time error.</span></span>

<span data-ttu-id="f2f88-105">Перечислены три формы номера ошибки:</span><span class="sxs-lookup"><span data-stu-id="f2f88-105">Three forms of the error number are listed:</span></span>

- <span data-ttu-id="f2f88-106">Положительное десятичной затравка — низкий двухбайт полного числа в десятичной форме.</span><span class="sxs-lookup"><span data-stu-id="f2f88-106">Positive decimal — the low two bytes of the full number in decimal format.</span></span> <span data-ttu-id="f2f88-107">Этот номер отображается в диалоговом окне Visual Basic сообщения об ошибке по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f2f88-107">This number is displayed in the default Visual Basic error message dialog box.</span></span> <span data-ttu-id="f2f88-108">Например, ошибка времени запуска "3707".</span><span class="sxs-lookup"><span data-stu-id="f2f88-108">For example, Run-time error '3707'.</span></span>

- <span data-ttu-id="f2f88-109">Отрицательный десятичной зачет — десятичной перевод полного номера ошибки.</span><span class="sxs-lookup"><span data-stu-id="f2f88-109">Negative decimal — The decimal translation of the full error number.</span></span>

- <span data-ttu-id="f2f88-110">Hexadecimal — hexadecimal representation of the full error number.</span><span class="sxs-lookup"><span data-stu-id="f2f88-110">Hexadecimal — The hexadecimal representation of the full error number.</span></span> <span data-ttu-id="f2f88-111">Код объекта Windows находится в четвертой цифре.</span><span class="sxs-lookup"><span data-stu-id="f2f88-111">The Windows facility code is in the fourth digit.</span></span> <span data-ttu-id="f2f88-112">The facility code for ADO error numbers is *A*. Например: 0x800 ***A*** 0E7B.</span><span class="sxs-lookup"><span data-stu-id="f2f88-112">The facility code for ADO error numbers is *A*. For example: 0x800 ***A*** 0E7B.</span></span>

> [!NOTE]
> <span data-ttu-id="f2f88-113">Ошибки OLE DB могут передаваться в приложение ADO.</span><span class="sxs-lookup"><span data-stu-id="f2f88-113">OLE DB errors may be passed to your ADO application.</span></span> <span data-ttu-id="f2f88-114">Как правило, их можно определить с помощью кода объекта Windows *4.*</span><span class="sxs-lookup"><span data-stu-id="f2f88-114">Typically, these can be identified by a Windows facility code of *4*.</span></span> <span data-ttu-id="f2f88-115">Например, 0x800_ **4** _.... Дополнительные сведения об этих номерах см. в главе 16 справочника программиста *OLE DB.*</span><span class="sxs-lookup"><span data-stu-id="f2f88-115">For example, 0x800_ **4** _.... For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f2f88-116">Константа</span><span class="sxs-lookup"><span data-stu-id="f2f88-116">Constant</span></span></p></th>
<th><p><span data-ttu-id="f2f88-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f2f88-117">Value</span></span></p></th>
<th><p><span data-ttu-id="f2f88-118">Описание</span><span class="sxs-lookup"><span data-stu-id="f2f88-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-119"><strong>adErrBoundToCommand</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-119"><strong>adErrBoundToCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-120">3707</span><span class="sxs-lookup"><span data-stu-id="f2f88-120">3707</span></span><br />
<span data-ttu-id="f2f88-121">-2146824581</span><span class="sxs-lookup"><span data-stu-id="f2f88-121">-2146824581</span></span><br />
<span data-ttu-id="f2f88-122">0x800A0E7B</span><span class="sxs-lookup"><span data-stu-id="f2f88-122">0x800A0E7B</span></span></p></td>
<td><p><span data-ttu-id="f2f88-123">Не удается изменить <strong>свойство ActiveConnection</strong> объекта <strong>Recordset,</strong> в качестве источника которого имеется объект <strong>Command.</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-123">Cannot change the <strong>ActiveConnection</strong> property of a <strong>Recordset</strong> object which has a <strong>Command</strong> object as its source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-124"><strong>adErrCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-124"><strong>adErrCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-125">3732</span><span class="sxs-lookup"><span data-stu-id="f2f88-125">3732</span></span><br />
<span data-ttu-id="f2f88-126">-2146824556</span><span class="sxs-lookup"><span data-stu-id="f2f88-126">-2146824556</span></span><br />
<span data-ttu-id="f2f88-127">0x800A0E94</span><span class="sxs-lookup"><span data-stu-id="f2f88-127">0x800A0E94</span></span></p></td>
<td><p><span data-ttu-id="f2f88-128">Сервер не может завершить операцию.</span><span class="sxs-lookup"><span data-stu-id="f2f88-128">Server cannot complete the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-129"><strong>adErrCantChangeConnection</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-129"><strong>adErrCantChangeConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-130">3748</span><span class="sxs-lookup"><span data-stu-id="f2f88-130">3748</span></span><br />
<span data-ttu-id="f2f88-131">-2146824540</span><span class="sxs-lookup"><span data-stu-id="f2f88-131">-2146824540</span></span><br />
<span data-ttu-id="f2f88-132">0x800A0EA4</span><span class="sxs-lookup"><span data-stu-id="f2f88-132">0x800A0EA4</span></span></p></td>
<td><p><span data-ttu-id="f2f88-133">Подключение было отклонено.</span><span class="sxs-lookup"><span data-stu-id="f2f88-133">Connection was denied.</span></span> <span data-ttu-id="f2f88-134">Характеристики нового подключения отличаются от уже используемого.</span><span class="sxs-lookup"><span data-stu-id="f2f88-134">New connection you requested has different characteristics than the one already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-135"><strong>adErrCantChangeProvider</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-135"><strong>adErrCantChangeProvider</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-136">3220</span><span class="sxs-lookup"><span data-stu-id="f2f88-136">3220</span></span><br />
<span data-ttu-id="f2f88-137">-2146825068</span><span class="sxs-lookup"><span data-stu-id="f2f88-137">-2146825068</span></span><br />
<span data-ttu-id="f2f88-138">0X800A0C94</span><span class="sxs-lookup"><span data-stu-id="f2f88-138">0X800A0C94</span></span></p></td>
<td><p><span data-ttu-id="f2f88-139">Поставщик отличается от поставщика, который уже используется.</span><span class="sxs-lookup"><span data-stu-id="f2f88-139">Supplied provider is different from the one already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-140"><strong>adErrCantConvertvalue</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-140"><strong>adErrCantConvertvalue</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-141">3724</span><span class="sxs-lookup"><span data-stu-id="f2f88-141">3724</span></span><br />
<span data-ttu-id="f2f88-142">-2146824564</span><span class="sxs-lookup"><span data-stu-id="f2f88-142">-2146824564</span></span><br />
<span data-ttu-id="f2f88-143">0x800A0E8C</span><span class="sxs-lookup"><span data-stu-id="f2f88-143">0x800A0E8C</span></span></p></td>
<td><p><span data-ttu-id="f2f88-144">Значение данных не может быть преобразовано по другим причинам, кроме несоответствия подписей или переполнения данных.</span><span class="sxs-lookup"><span data-stu-id="f2f88-144">Data value cannot be converted for reasons other than sign mismatch or data overflow.</span></span> <span data-ttu-id="f2f88-145">Например, преобразование будет иметь усеченные данные.</span><span class="sxs-lookup"><span data-stu-id="f2f88-145">For example, conversion would have truncated data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-146"><strong>adErrCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-146"><strong>adErrCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-147">3725</span><span class="sxs-lookup"><span data-stu-id="f2f88-147">3725</span></span><br />
<span data-ttu-id="f2f88-148">-2146824563</span><span class="sxs-lookup"><span data-stu-id="f2f88-148">-2146824563</span></span><br />
<span data-ttu-id="f2f88-149">0x800A0E8D</span><span class="sxs-lookup"><span data-stu-id="f2f88-149">0x800A0E8D</span></span></p></td>
<td><p><span data-ttu-id="f2f88-150">Значение данных нельзя установить или извлечь, так как тип данных поля был неизвестным, или у поставщика недостаточно ресурсов для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="f2f88-150">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-151"><strong>adErrCatalogNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-151"><strong>adErrCatalogNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-152">3747</span><span class="sxs-lookup"><span data-stu-id="f2f88-152">3747</span></span><br />
<span data-ttu-id="f2f88-153">-2146824541</span><span class="sxs-lookup"><span data-stu-id="f2f88-153">-2146824541</span></span><br />
<span data-ttu-id="f2f88-154">0x800A0EA3</span><span class="sxs-lookup"><span data-stu-id="f2f88-154">0x800A0EA3</span></span></p></td>
<td><p><span data-ttu-id="f2f88-155">Для операции требуется <strong>допустимый parentCatalog.</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-155">Operation requires a valid <strong>ParentCatalog</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-156"><strong>adErrColumnNotOnThisRow</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-156"><strong>adErrColumnNotOnThisRow</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-157">3726</span><span class="sxs-lookup"><span data-stu-id="f2f88-157">3726</span></span><br />
<span data-ttu-id="f2f88-158">-2146824562</span><span class="sxs-lookup"><span data-stu-id="f2f88-158">-2146824562</span></span><br />
<span data-ttu-id="f2f88-159">0x800A0E8E</span><span class="sxs-lookup"><span data-stu-id="f2f88-159">0x800A0E8E</span></span></p></td>
<td><p><span data-ttu-id="f2f88-160">Запись не содержит это поле.</span><span class="sxs-lookup"><span data-stu-id="f2f88-160">Record does not contain this field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-161"><strong>adErrDataConversion</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-161"><strong>adErrDataConversion</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-162">3421</span><span class="sxs-lookup"><span data-stu-id="f2f88-162">3421</span></span><br />
<span data-ttu-id="f2f88-163">-2146824867</span><span class="sxs-lookup"><span data-stu-id="f2f88-163">-2146824867</span></span><br />
<span data-ttu-id="f2f88-164">0x800A0D5D</span><span class="sxs-lookup"><span data-stu-id="f2f88-164">0x800A0D5D</span></span></p></td>
<td><p><span data-ttu-id="f2f88-165">Приложение использует неправильное значение для текущей операции.</span><span class="sxs-lookup"><span data-stu-id="f2f88-165">Application uses a value of the wrong type for the current operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-166"><strong>adErrDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-166"><strong>adErrDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-167">3721</span><span class="sxs-lookup"><span data-stu-id="f2f88-167">3721</span></span><br />
<span data-ttu-id="f2f88-168">-2146824567</span><span class="sxs-lookup"><span data-stu-id="f2f88-168">-2146824567</span></span><br />
<span data-ttu-id="f2f88-169">0x800A0E89</span><span class="sxs-lookup"><span data-stu-id="f2f88-169">0x800A0E89</span></span></p></td>
<td><p><span data-ttu-id="f2f88-170">Значение данных слишком большое для представления типом данных поля.</span><span class="sxs-lookup"><span data-stu-id="f2f88-170">Data value is too large to be represented by the field data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-171"><strong>adErrDelResOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-171"><strong>adErrDelResOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-172">3738</span><span class="sxs-lookup"><span data-stu-id="f2f88-172">3738</span></span><br />
<span data-ttu-id="f2f88-173">-2146824550</span><span class="sxs-lookup"><span data-stu-id="f2f88-173">-2146824550</span></span><br />
<span data-ttu-id="f2f88-174">0x800A0E9A</span><span class="sxs-lookup"><span data-stu-id="f2f88-174">0x800A0E9A</span></span></p></td>
<td><p><span data-ttu-id="f2f88-175">URL-адрес удаляемого объекта находится вне области текущей записи.</span><span class="sxs-lookup"><span data-stu-id="f2f88-175">URL of the object to be deleted is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-176"><strong>adErrDenyNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-176"><strong>adErrDenyNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-177">3750</span><span class="sxs-lookup"><span data-stu-id="f2f88-177">3750</span></span><br />
<span data-ttu-id="f2f88-178">-2146824538</span><span class="sxs-lookup"><span data-stu-id="f2f88-178">-2146824538</span></span><br />
<span data-ttu-id="f2f88-179">0x800A0EA6</span><span class="sxs-lookup"><span data-stu-id="f2f88-179">0x800A0EA6</span></span></p></td>
<td><p><span data-ttu-id="f2f88-180">Поставщик не поддерживает ограничения общего доступа.</span><span class="sxs-lookup"><span data-stu-id="f2f88-180">Provider does not support sharing restrictions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-181"><strong>adErrDenyTypeNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-181"><strong>adErrDenyTypeNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-182">3751</span><span class="sxs-lookup"><span data-stu-id="f2f88-182">3751</span></span><br />
<span data-ttu-id="f2f88-183">-2146824537</span><span class="sxs-lookup"><span data-stu-id="f2f88-183">-2146824537</span></span><br />
<span data-ttu-id="f2f88-184">0x800A0EA7</span><span class="sxs-lookup"><span data-stu-id="f2f88-184">0x800A0EA7</span></span></p></td>
<td><p><span data-ttu-id="f2f88-185">Поставщик не поддерживает запрашиваемого типа ограничения общего доступа.</span><span class="sxs-lookup"><span data-stu-id="f2f88-185">Provider does not support the requested kind of sharing restriction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-186"><strong>adErrFeatureNotAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-186"><strong>adErrFeatureNotAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-187">3251</span><span class="sxs-lookup"><span data-stu-id="f2f88-187">3251</span></span><br />
<span data-ttu-id="f2f88-188">-2146825037</span><span class="sxs-lookup"><span data-stu-id="f2f88-188">-2146825037</span></span><br />
<span data-ttu-id="f2f88-189">0x800A0CB3</span><span class="sxs-lookup"><span data-stu-id="f2f88-189">0x800A0CB3</span></span></p></td>
<td><p><span data-ttu-id="f2f88-190">Объект или поставщик не могут выполнять запрашиваемую операцию.</span><span class="sxs-lookup"><span data-stu-id="f2f88-190">Object or provider is not capable of performing requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-191"><strong>adErrFieldsUpdateFailed</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-191"><strong>adErrFieldsUpdateFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-192">3749</span><span class="sxs-lookup"><span data-stu-id="f2f88-192">3749</span></span><br />
<span data-ttu-id="f2f88-193">-2146824539</span><span class="sxs-lookup"><span data-stu-id="f2f88-193">-2146824539</span></span><br />
<span data-ttu-id="f2f88-194">0x800A0EA5</span><span class="sxs-lookup"><span data-stu-id="f2f88-194">0x800A0EA5</span></span></p></td>
<td><p><span data-ttu-id="f2f88-195">Сбой обновления полей.</span><span class="sxs-lookup"><span data-stu-id="f2f88-195">Fields update failed.</span></span> <span data-ttu-id="f2f88-196">Для получения дополнительных сведений <strong>изучите свойство Status</strong> отдельных объектов полей.</span><span class="sxs-lookup"><span data-stu-id="f2f88-196">For further information, examine the <strong>Status</strong> property of individual field objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-197"><strong>adErrIllegalOperation</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-197"><strong>adErrIllegalOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-198">3219</span><span class="sxs-lookup"><span data-stu-id="f2f88-198">3219</span></span><br />
<span data-ttu-id="f2f88-199">-2146825069</span><span class="sxs-lookup"><span data-stu-id="f2f88-199">-2146825069</span></span><br />
<span data-ttu-id="f2f88-200">0x800A0C93</span><span class="sxs-lookup"><span data-stu-id="f2f88-200">0x800A0C93</span></span></p></td>
<td><p><span data-ttu-id="f2f88-201">В этом контексте операция не разрешена.</span><span class="sxs-lookup"><span data-stu-id="f2f88-201">Operation is not allowed in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-202"><strong>adErrIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-202"><strong>adErrIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-203">3719</span><span class="sxs-lookup"><span data-stu-id="f2f88-203">3719</span></span><br />
<span data-ttu-id="f2f88-204">-2146824569</span><span class="sxs-lookup"><span data-stu-id="f2f88-204">-2146824569</span></span><br />
<span data-ttu-id="f2f88-205">0x800A0E87</span><span class="sxs-lookup"><span data-stu-id="f2f88-205">0x800A0E87</span></span></p></td>
<td><p><span data-ttu-id="f2f88-206">Значение данных конфликтет с ограничениями целостности поля.</span><span class="sxs-lookup"><span data-stu-id="f2f88-206">Data value conflicts with the integrity constraints of the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-207"><strong>adErrInTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-207"><strong>adErrInTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-208">3246</span><span class="sxs-lookup"><span data-stu-id="f2f88-208">3246</span></span><br />
<span data-ttu-id="f2f88-209">-2146825042</span><span class="sxs-lookup"><span data-stu-id="f2f88-209">-2146825042</span></span><br />
<span data-ttu-id="f2f88-210">0x800A0CAE</span><span class="sxs-lookup"><span data-stu-id="f2f88-210">0x800A0CAE</span></span></p></td>
<td><p><span data-ttu-id="f2f88-211"><strong>Объект подключения</strong> не может быть явно закрыт во время транзакции.</span><span class="sxs-lookup"><span data-stu-id="f2f88-211"><strong>Connection</strong> object cannot be explicitly closed while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-212"><strong>adErrInvalidArgument</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-212"><strong>adErrInvalidArgument</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-213">3001</span><span class="sxs-lookup"><span data-stu-id="f2f88-213">3001</span></span><br />
<span data-ttu-id="f2f88-214">-2146825287</span><span class="sxs-lookup"><span data-stu-id="f2f88-214">-2146825287</span></span><br />
<span data-ttu-id="f2f88-215">0x800A0BB9</span><span class="sxs-lookup"><span data-stu-id="f2f88-215">0x800A0BB9</span></span></p></td>
<td><p><span data-ttu-id="f2f88-216">Аргументы имеют неправильный тип, находятся вне допустимого диапазона или конфликтуют друг с другом.</span><span class="sxs-lookup"><span data-stu-id="f2f88-216">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-217"><strong>adErrInvalidConnection</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-217"><strong>adErrInvalidConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-218">3709</span><span class="sxs-lookup"><span data-stu-id="f2f88-218">3709</span></span><br />
<span data-ttu-id="f2f88-219">-2146824579</span><span class="sxs-lookup"><span data-stu-id="f2f88-219">-2146824579</span></span><br />
<span data-ttu-id="f2f88-220">0x800A0E7D</span><span class="sxs-lookup"><span data-stu-id="f2f88-220">0x800A0E7D</span></span></p></td>
<td><p><span data-ttu-id="f2f88-221">Подключение нельзя использовать для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="f2f88-221">The connection cannot be used to perform this operation.</span></span> <span data-ttu-id="f2f88-222">В этом контексте он либо закрыт, либо недействителен.</span><span class="sxs-lookup"><span data-stu-id="f2f88-222">It is either closed or invalid in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-223"><strong>adErrInvalidParamInfo</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-223"><strong>adErrInvalidParamInfo</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-224">3708</span><span class="sxs-lookup"><span data-stu-id="f2f88-224">3708</span></span><br />
<span data-ttu-id="f2f88-225">-2146824580</span><span class="sxs-lookup"><span data-stu-id="f2f88-225">-2146824580</span></span><br />
<span data-ttu-id="f2f88-226">0x800A0E7C</span><span class="sxs-lookup"><span data-stu-id="f2f88-226">0x800A0E7C</span></span></p></td>
<td><p><span data-ttu-id="f2f88-227"><strong>Объект Parameter</strong> определен неправильно.</span><span class="sxs-lookup"><span data-stu-id="f2f88-227"><strong>Parameter</strong> object is improperly defined.</span></span> <span data-ttu-id="f2f88-228">Предоставлены несогласованные или неполные сведения.</span><span class="sxs-lookup"><span data-stu-id="f2f88-228">Inconsistent or incomplete information was provided.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-229"><strong>adErrInvalidTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-229"><strong>adErrInvalidTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-230">3714</span><span class="sxs-lookup"><span data-stu-id="f2f88-230">3714</span></span><br />
<span data-ttu-id="f2f88-231">-2146824574</span><span class="sxs-lookup"><span data-stu-id="f2f88-231">-2146824574</span></span><br />
<span data-ttu-id="f2f88-232">0x800A0E82</span><span class="sxs-lookup"><span data-stu-id="f2f88-232">0x800A0E82</span></span></p></td>
<td><p><span data-ttu-id="f2f88-233">Координация транзакции недействительна или не запущена.</span><span class="sxs-lookup"><span data-stu-id="f2f88-233">Coordinating transaction is invalid or has not started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-234"><strong>adErrInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-234"><strong>adErrInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-235">3729</span><span class="sxs-lookup"><span data-stu-id="f2f88-235">3729</span></span><br />
<span data-ttu-id="f2f88-236">-2146824559</span><span class="sxs-lookup"><span data-stu-id="f2f88-236">-2146824559</span></span><br />
<span data-ttu-id="f2f88-237">0x800A0E91</span><span class="sxs-lookup"><span data-stu-id="f2f88-237">0x800A0E91</span></span></p></td>
<td><p><span data-ttu-id="f2f88-238">URL-адрес содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="f2f88-238">URL contains invalid characters.</span></span> <span data-ttu-id="f2f88-239">Убедитесь, что URL-адрес введите правильно.</span><span class="sxs-lookup"><span data-stu-id="f2f88-239">Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-240"><strong>adErrItemNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-240"><strong>adErrItemNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-241">3265</span><span class="sxs-lookup"><span data-stu-id="f2f88-241">3265</span></span><br />
<span data-ttu-id="f2f88-242">-2146825023</span><span class="sxs-lookup"><span data-stu-id="f2f88-242">-2146825023</span></span><br />
<span data-ttu-id="f2f88-243">0x800A0CC1</span><span class="sxs-lookup"><span data-stu-id="f2f88-243">0x800A0CC1</span></span></p></td>
<td><p><span data-ttu-id="f2f88-244">Элемент не может быть найден в коллекции, соответствующей запрашиваемой именем или порядку.</span><span class="sxs-lookup"><span data-stu-id="f2f88-244">Item cannot be found in the collection corresponding to the requested name or ordinal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-245"><strong>adErrNoCurrentRecord</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-245"><strong>adErrNoCurrentRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-246">3021</span><span class="sxs-lookup"><span data-stu-id="f2f88-246">3021</span></span><br />
<span data-ttu-id="f2f88-247">-2146825267</span><span class="sxs-lookup"><span data-stu-id="f2f88-247">-2146825267</span></span><br />
<span data-ttu-id="f2f88-248">0x800A0BCD</span><span class="sxs-lookup"><span data-stu-id="f2f88-248">0x800A0BCD</span></span></p></td>
<td><p><span data-ttu-id="f2f88-249">Либо <strong>BOF,</strong> <strong>либо EOF</strong> имеет true, либо текущая запись была удалена.</span><span class="sxs-lookup"><span data-stu-id="f2f88-249">Either <strong>BOF</strong> or <strong>EOF</strong> is True, or the current record has been deleted.</span></span> <span data-ttu-id="f2f88-250">Для запрашиваемой операции требуется текущая запись.</span><span class="sxs-lookup"><span data-stu-id="f2f88-250">Requested operation requires a current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-251"><strong>adErrNotExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-251"><strong>adErrNotExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-252">3715</span><span class="sxs-lookup"><span data-stu-id="f2f88-252">3715</span></span><br />
<span data-ttu-id="f2f88-253">-2146824573</span><span class="sxs-lookup"><span data-stu-id="f2f88-253">-2146824573</span></span><br />
<span data-ttu-id="f2f88-254">0x800A0E83</span><span class="sxs-lookup"><span data-stu-id="f2f88-254">0x800A0E83</span></span></p></td>
<td><p><span data-ttu-id="f2f88-255">Не удается выполнить операцию, пока она не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f2f88-255">Operation cannot be performed while not executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-256"><strong>adErrNotReentrant</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-256"><strong>adErrNotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-257">3710</span><span class="sxs-lookup"><span data-stu-id="f2f88-257">3710</span></span><br />
<span data-ttu-id="f2f88-258">-2146824578</span><span class="sxs-lookup"><span data-stu-id="f2f88-258">-2146824578</span></span><br />
<span data-ttu-id="f2f88-259">0x800A0E7E</span><span class="sxs-lookup"><span data-stu-id="f2f88-259">0x800A0E7E</span></span></p></td>
<td><p><span data-ttu-id="f2f88-260">Операция не может быть выполнена во время обработки события.</span><span class="sxs-lookup"><span data-stu-id="f2f88-260">Operation cannot be performed while processing event.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-261"><strong>adErrObjectClosed</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-261"><strong>adErrObjectClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-262">3704</span><span class="sxs-lookup"><span data-stu-id="f2f88-262">3704</span></span><br />
<span data-ttu-id="f2f88-263">-2146824584</span><span class="sxs-lookup"><span data-stu-id="f2f88-263">-2146824584</span></span><br />
<span data-ttu-id="f2f88-264">0x800A0E78</span><span class="sxs-lookup"><span data-stu-id="f2f88-264">0x800A0E78</span></span></p></td>
<td><p><span data-ttu-id="f2f88-265">Операция не разрешена при закрытии объекта.</span><span class="sxs-lookup"><span data-stu-id="f2f88-265">Operation is not allowed when the object is closed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-266"><strong>adErrObjectInCollection</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-266"><strong>adErrObjectInCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-267">3367</span><span class="sxs-lookup"><span data-stu-id="f2f88-267">3367</span></span><br />
<span data-ttu-id="f2f88-268">-2146824921</span><span class="sxs-lookup"><span data-stu-id="f2f88-268">-2146824921</span></span><br />
<span data-ttu-id="f2f88-269">0x800A0D27</span><span class="sxs-lookup"><span data-stu-id="f2f88-269">0x800A0D27</span></span></p></td>
<td><p><span data-ttu-id="f2f88-270">Объект уже находится в коллекции.</span><span class="sxs-lookup"><span data-stu-id="f2f88-270">Object is already in collection.</span></span> <span data-ttu-id="f2f88-271">Не удается приметься.</span><span class="sxs-lookup"><span data-stu-id="f2f88-271">Cannot append.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-272"><strong>adErrObjectNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-272"><strong>adErrObjectNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-273">3420</span><span class="sxs-lookup"><span data-stu-id="f2f88-273">3420</span></span><br />
<span data-ttu-id="f2f88-274">-2146824868</span><span class="sxs-lookup"><span data-stu-id="f2f88-274">-2146824868</span></span><br />
<span data-ttu-id="f2f88-275">0x800A0D5C</span><span class="sxs-lookup"><span data-stu-id="f2f88-275">0x800A0D5C</span></span></p></td>
<td><p><span data-ttu-id="f2f88-276">Объект больше не действителен.</span><span class="sxs-lookup"><span data-stu-id="f2f88-276">Object is no longer valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-277"><strong>adErrObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-277"><strong>adErrObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-278">3705</span><span class="sxs-lookup"><span data-stu-id="f2f88-278">3705</span></span><br />
<span data-ttu-id="f2f88-279">-2146824583</span><span class="sxs-lookup"><span data-stu-id="f2f88-279">-2146824583</span></span><br />
<span data-ttu-id="f2f88-280">0x800A0E79</span><span class="sxs-lookup"><span data-stu-id="f2f88-280">0x800A0E79</span></span></p></td>
<td><p><span data-ttu-id="f2f88-281">Операция не разрешена, если объект открыт.</span><span class="sxs-lookup"><span data-stu-id="f2f88-281">Operation is not allowed when the object is open.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-282"><strong>adErrOpeningFile</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-282"><strong>adErrOpeningFile</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-283">3002</span><span class="sxs-lookup"><span data-stu-id="f2f88-283">3002</span></span><br />
<span data-ttu-id="f2f88-284">-2146825286</span><span class="sxs-lookup"><span data-stu-id="f2f88-284">-2146825286</span></span><br />
<span data-ttu-id="f2f88-285">0x800A0BBA</span><span class="sxs-lookup"><span data-stu-id="f2f88-285">0x800A0BBA</span></span></p></td>
<td><p><span data-ttu-id="f2f88-286">Не удалось открыть файл.</span><span class="sxs-lookup"><span data-stu-id="f2f88-286">File could not be opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-287"><strong>adErrOperationCancelled</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-287"><strong>adErrOperationCancelled</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-288">3712</span><span class="sxs-lookup"><span data-stu-id="f2f88-288">3712</span></span><br />
<span data-ttu-id="f2f88-289">-2146824576</span><span class="sxs-lookup"><span data-stu-id="f2f88-289">-2146824576</span></span><br />
<span data-ttu-id="f2f88-290">0x800A0E80</span><span class="sxs-lookup"><span data-stu-id="f2f88-290">0x800A0E80</span></span></p></td>
<td><p><span data-ttu-id="f2f88-291">Операция была отменена пользователем.</span><span class="sxs-lookup"><span data-stu-id="f2f88-291">Operation has been cancelled by the user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-292"><strong>adErrOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-292"><strong>adErrOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-293">3734</span><span class="sxs-lookup"><span data-stu-id="f2f88-293">3734</span></span><br />
<span data-ttu-id="f2f88-294">-2146824554</span><span class="sxs-lookup"><span data-stu-id="f2f88-294">-2146824554</span></span><br />
<span data-ttu-id="f2f88-295">0x800A0E96</span><span class="sxs-lookup"><span data-stu-id="f2f88-295">0x800A0E96</span></span></p></td>
<td><p><span data-ttu-id="f2f88-296">Не удается выполнить операцию.</span><span class="sxs-lookup"><span data-stu-id="f2f88-296">Operation cannot be performed.</span></span> <span data-ttu-id="f2f88-297">Поставщик не может получить достаточно места для хранения.</span><span class="sxs-lookup"><span data-stu-id="f2f88-297">Provider cannot obtain enough storage space.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-298"><strong>adErrPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-298"><strong>adErrPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-299">3720</span><span class="sxs-lookup"><span data-stu-id="f2f88-299">3720</span></span><br />
<span data-ttu-id="f2f88-300">-2146824568</span><span class="sxs-lookup"><span data-stu-id="f2f88-300">-2146824568</span></span><br />
<span data-ttu-id="f2f88-301">0x800A0E88</span><span class="sxs-lookup"><span data-stu-id="f2f88-301">0x800A0E88</span></span></p></td>
<td><p><span data-ttu-id="f2f88-302">Ненамеренное разрешение предотвращает запись в поле.</span><span class="sxs-lookup"><span data-stu-id="f2f88-302">Insufficent permission prevents writing to the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-303"><strong>adErrProviderFailed</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-303"><strong>adErrProviderFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-304">3000</span><span class="sxs-lookup"><span data-stu-id="f2f88-304">3000</span></span><br />
<span data-ttu-id="f2f88-305">-2146825288</span><span class="sxs-lookup"><span data-stu-id="f2f88-305">-2146825288</span></span><br />
<span data-ttu-id="f2f88-306">0x800A0BB8</span><span class="sxs-lookup"><span data-stu-id="f2f88-306">0x800A0BB8</span></span></p></td>
<td><p><span data-ttu-id="f2f88-307">Поставщику не удалось выполнить запрашиваемую операцию.</span><span class="sxs-lookup"><span data-stu-id="f2f88-307">Provider failed to perform the requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-308"><strong>adErrProviderNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-308"><strong>adErrProviderNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-309">3706</span><span class="sxs-lookup"><span data-stu-id="f2f88-309">3706</span></span><br />
<span data-ttu-id="f2f88-310">-2146824582</span><span class="sxs-lookup"><span data-stu-id="f2f88-310">-2146824582</span></span><br />
<span data-ttu-id="f2f88-311">0x800A0E7A</span><span class="sxs-lookup"><span data-stu-id="f2f88-311">0x800A0E7A</span></span></p></td>
<td><p><span data-ttu-id="f2f88-312">Не удается найти поставщика.</span><span class="sxs-lookup"><span data-stu-id="f2f88-312">Provider cannot be found.</span></span> <span data-ttu-id="f2f88-313">Он может быть неправильно установлен.</span><span class="sxs-lookup"><span data-stu-id="f2f88-313">It may not be properly installed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-314"><strong>adErrReadFile</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-314"><strong>adErrReadFile</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-315">3003</span><span class="sxs-lookup"><span data-stu-id="f2f88-315">3003</span></span><br />
<span data-ttu-id="f2f88-316">-2146825285</span><span class="sxs-lookup"><span data-stu-id="f2f88-316">-2146825285</span></span><br />
<span data-ttu-id="f2f88-317">0x800A0BBB</span><span class="sxs-lookup"><span data-stu-id="f2f88-317">0x800A0BBB</span></span></p></td>
<td><p><span data-ttu-id="f2f88-318">Не удалось прочитать файл.</span><span class="sxs-lookup"><span data-stu-id="f2f88-318">File could not be read.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-319"><strong>adErrResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-319"><strong>adErrResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-320">3731</span><span class="sxs-lookup"><span data-stu-id="f2f88-320">3731</span></span><br />
<span data-ttu-id="f2f88-321">-2146824557</span><span class="sxs-lookup"><span data-stu-id="f2f88-321">-2146824557</span></span><br />
<span data-ttu-id="f2f88-322">0x800A0E93</span><span class="sxs-lookup"><span data-stu-id="f2f88-322">0x800A0E93</span></span></p></td>
<td><p><span data-ttu-id="f2f88-323">Не удается выполнить операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="f2f88-323">Copy operation cannot be performed.</span></span> <span data-ttu-id="f2f88-324">Объект с именем по url-адресу назначения уже существует.</span><span class="sxs-lookup"><span data-stu-id="f2f88-324">Object named by destination URL already exists.</span></span> <span data-ttu-id="f2f88-325">Укажите <strong>adCopyOverwrite для</strong> замены объекта.</span><span class="sxs-lookup"><span data-stu-id="f2f88-325">Specify <strong>adCopyOverwrite</strong> to replace the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-326"><strong>adErrResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-326"><strong>adErrResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-327">3730</span><span class="sxs-lookup"><span data-stu-id="f2f88-327">3730</span></span><br />
<span data-ttu-id="f2f88-328">-2146824558</span><span class="sxs-lookup"><span data-stu-id="f2f88-328">-2146824558</span></span><br />
<span data-ttu-id="f2f88-329">0x800A0E92</span><span class="sxs-lookup"><span data-stu-id="f2f88-329">0x800A0E92</span></span></p></td>
<td><p><span data-ttu-id="f2f88-330">Объект, представленный указанным URL-адресом, блокируется одним или более другими процессами.</span><span class="sxs-lookup"><span data-stu-id="f2f88-330">Object represented by the specified URL is locked by one or more other processes.</span></span> <span data-ttu-id="f2f88-331">Подождите, пока процесс завершится, и снова попытайтесь повторить операцию.</span><span class="sxs-lookup"><span data-stu-id="f2f88-331">Wait until the process has finished and attempt the operation again.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-332"><strong>adErrResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-332"><strong>adErrResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-333">3735</span><span class="sxs-lookup"><span data-stu-id="f2f88-333">3735</span></span><br />
<span data-ttu-id="f2f88-334">-2146824553</span><span class="sxs-lookup"><span data-stu-id="f2f88-334">-2146824553</span></span><br />
<span data-ttu-id="f2f88-335">0x800A0E97</span><span class="sxs-lookup"><span data-stu-id="f2f88-335">0x800A0E97</span></span></p></td>
<td><p><span data-ttu-id="f2f88-336">Url-адрес источника или назначения находится вне области текущей записи.</span><span class="sxs-lookup"><span data-stu-id="f2f88-336">Source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-337"><strong>adErrSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-337"><strong>adErrSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-338">3722</span><span class="sxs-lookup"><span data-stu-id="f2f88-338">3722</span></span><br />
<span data-ttu-id="f2f88-339">-2146824566</span><span class="sxs-lookup"><span data-stu-id="f2f88-339">-2146824566</span></span><br />
<span data-ttu-id="f2f88-340">0x800A0E8A</span><span class="sxs-lookup"><span data-stu-id="f2f88-340">0x800A0E8A</span></span></p></td>
<td><p><span data-ttu-id="f2f88-341">Значение данных конфликтет с типом данных или ограничениями поля.</span><span class="sxs-lookup"><span data-stu-id="f2f88-341">Data value conflicts with the data type or constraints of the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-342"><strong>adErrSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-342"><strong>adErrSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-343">3723</span><span class="sxs-lookup"><span data-stu-id="f2f88-343">3723</span></span><br />
<span data-ttu-id="f2f88-344">-2146824565</span><span class="sxs-lookup"><span data-stu-id="f2f88-344">-2146824565</span></span><br />
<span data-ttu-id="f2f88-345">0x800A0E8B</span><span class="sxs-lookup"><span data-stu-id="f2f88-345">0x800A0E8B</span></span></p></td>
<td><p><span data-ttu-id="f2f88-346">Сбой преобразования, так как значение данных было подписано, а тип данных поля, используемый поставщиком, не подписан.</span><span class="sxs-lookup"><span data-stu-id="f2f88-346">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-347"><strong>adErrStillConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-347"><strong>adErrStillConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-348">3713</span><span class="sxs-lookup"><span data-stu-id="f2f88-348">3713</span></span><br />
<span data-ttu-id="f2f88-349">-2146824575</span><span class="sxs-lookup"><span data-stu-id="f2f88-349">-2146824575</span></span><br />
<span data-ttu-id="f2f88-350">0x800A0E81</span><span class="sxs-lookup"><span data-stu-id="f2f88-350">0x800A0E81</span></span></p></td>
<td><p><span data-ttu-id="f2f88-351">Операция не может выполняться при асинхронном подключении.</span><span class="sxs-lookup"><span data-stu-id="f2f88-351">Operation cannot be performed while connecting aynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-352"><strong>adErrStillExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-352"><strong>adErrStillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-353">3711</span><span class="sxs-lookup"><span data-stu-id="f2f88-353">3711</span></span><br />
<span data-ttu-id="f2f88-354">-2146824577</span><span class="sxs-lookup"><span data-stu-id="f2f88-354">-2146824577</span></span><br />
<span data-ttu-id="f2f88-355">0x800A0E7F</span><span class="sxs-lookup"><span data-stu-id="f2f88-355">0x800A0E7F</span></span></p></td>
<td><p><span data-ttu-id="f2f88-356">Операция не может выполняться при асинхронном выполнении.</span><span class="sxs-lookup"><span data-stu-id="f2f88-356">Operation cannot be performed while executing asynchronously.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-357"><strong>adErrTreePermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-357"><strong>adErrTreePermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-358">3728</span><span class="sxs-lookup"><span data-stu-id="f2f88-358">3728</span></span><br />
<span data-ttu-id="f2f88-359">-2146824560</span><span class="sxs-lookup"><span data-stu-id="f2f88-359">-2146824560</span></span><br />
<span data-ttu-id="f2f88-360">0x800A0E90</span><span class="sxs-lookup"><span data-stu-id="f2f88-360">0x800A0E90</span></span></p></td>
<td><p><span data-ttu-id="f2f88-361">Недостаточно разрешений для доступа к дереву или подtree.</span><span class="sxs-lookup"><span data-stu-id="f2f88-361">Permissions are insufficient to access tree or subtree.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-362"><strong>adErrUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-362"><strong>adErrUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-363">3736</span><span class="sxs-lookup"><span data-stu-id="f2f88-363">3736</span></span><br />
<span data-ttu-id="f2f88-364">-2146824552</span><span class="sxs-lookup"><span data-stu-id="f2f88-364">-2146824552</span></span><br />
<span data-ttu-id="f2f88-365">0x800A0E98</span><span class="sxs-lookup"><span data-stu-id="f2f88-365">0x800A0E98</span></span></p></td>
<td><p><span data-ttu-id="f2f88-366">Не удалось завершить операцию, и состояние недоступно.</span><span class="sxs-lookup"><span data-stu-id="f2f88-366">Operation failed to complete and the status is unavailable.</span></span> <span data-ttu-id="f2f88-367">Поле может быть недоступно или операция не была предпринята.</span><span class="sxs-lookup"><span data-stu-id="f2f88-367">The field may be unavailable or the operation was not attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-368"><strong>adErrUnsafeOperation</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-368"><strong>adErrUnsafeOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-369">3716</span><span class="sxs-lookup"><span data-stu-id="f2f88-369">3716</span></span><br />
<span data-ttu-id="f2f88-370">-2146824572</span><span class="sxs-lookup"><span data-stu-id="f2f88-370">-2146824572</span></span><br />
<span data-ttu-id="f2f88-371">0x800A0E84</span><span class="sxs-lookup"><span data-stu-id="f2f88-371">0x800A0E84</span></span></p></td>
<td><p><span data-ttu-id="f2f88-372">Параметры безопасности на этом компьютере запрещают доступ к источнику данных в другом домене.</span><span class="sxs-lookup"><span data-stu-id="f2f88-372">Safety settings on this computer prohibit accessing a data source on another domain.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-373"><strong>adErrURLDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-373"><strong>adErrURLDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-374">3727</span><span class="sxs-lookup"><span data-stu-id="f2f88-374">3727</span></span><br />
<span data-ttu-id="f2f88-375">-2146824561</span><span class="sxs-lookup"><span data-stu-id="f2f88-375">-2146824561</span></span><br />
<span data-ttu-id="f2f88-376">0x800A0E8F</span><span class="sxs-lookup"><span data-stu-id="f2f88-376">0x800A0E8F</span></span></p></td>
<td><p><span data-ttu-id="f2f88-377">Исходный URL-адрес или родительский URL-адрес назначения не существуют.</span><span class="sxs-lookup"><span data-stu-id="f2f88-377">Either the source URL or the parent of the destination URL does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-378"><strong>adErrURLNamedRowDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-378"><strong>adErrURLNamedRowDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-379">3737</span><span class="sxs-lookup"><span data-stu-id="f2f88-379">3737</span></span><br />
<span data-ttu-id="f2f88-380">-2146824551</span><span class="sxs-lookup"><span data-stu-id="f2f88-380">-2146824551</span></span><br />
<span data-ttu-id="f2f88-381">0x800A0E99</span><span class="sxs-lookup"><span data-stu-id="f2f88-381">0x800A0E99</span></span></p></td>
<td><p><span data-ttu-id="f2f88-382">Запись с именем по этому URL-адресу не существует.</span><span class="sxs-lookup"><span data-stu-id="f2f88-382">Record named by this URL does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-383"><strong>adErrVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-383"><strong>adErrVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-384">3733</span><span class="sxs-lookup"><span data-stu-id="f2f88-384">3733</span></span><br />
<span data-ttu-id="f2f88-385">-2146824555</span><span class="sxs-lookup"><span data-stu-id="f2f88-385">-2146824555</span></span><br />
<span data-ttu-id="f2f88-386">0x800A0E95</span><span class="sxs-lookup"><span data-stu-id="f2f88-386">0x800A0E95</span></span></p></td>
<td><p><span data-ttu-id="f2f88-387">Поставщик не может найти устройство хранения, обозначенное URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="f2f88-387">Provider cannot locate the storage device indicated by the URL.</span></span> <span data-ttu-id="f2f88-388">Убедитесь, что URL-адрес введите правильно.</span><span class="sxs-lookup"><span data-stu-id="f2f88-388">Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-389"><strong>adErrWriteFile</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-389"><strong>adErrWriteFile</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-390">3004</span><span class="sxs-lookup"><span data-stu-id="f2f88-390">3004</span></span><br />
<span data-ttu-id="f2f88-391">-2146825284</span><span class="sxs-lookup"><span data-stu-id="f2f88-391">-2146825284</span></span><br />
<span data-ttu-id="f2f88-392">0x800A0BBC</span><span class="sxs-lookup"><span data-stu-id="f2f88-392">0x800A0BBC</span></span></p></td>
<td><p><span data-ttu-id="f2f88-393">Сбой записи в файл.</span><span class="sxs-lookup"><span data-stu-id="f2f88-393">Write to file failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-394"><strong>adWrnSecurityDialog</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-394"><strong>adWrnSecurityDialog</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-395">3717</span><span class="sxs-lookup"><span data-stu-id="f2f88-395">3717</span></span><br />
<span data-ttu-id="f2f88-396">-2146824571</span><span class="sxs-lookup"><span data-stu-id="f2f88-396">-2146824571</span></span><br />
<span data-ttu-id="f2f88-397">0x800A0E85</span><span class="sxs-lookup"><span data-stu-id="f2f88-397">0x800A0E85</span></span></p></td>
<td><p><span data-ttu-id="f2f88-398">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="f2f88-398">For internal use only.</span></span> <span data-ttu-id="f2f88-399">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="f2f88-399">Don't use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-400"><strong>adWrnSecurityDialogHeader</strong></span><span class="sxs-lookup"><span data-stu-id="f2f88-400"><strong>adWrnSecurityDialogHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="f2f88-401">3718</span><span class="sxs-lookup"><span data-stu-id="f2f88-401">3718</span></span><br />
<span data-ttu-id="f2f88-402">-2146824570</span><span class="sxs-lookup"><span data-stu-id="f2f88-402">-2146824570</span></span><br />
<span data-ttu-id="f2f88-403">0x800A0E86</span><span class="sxs-lookup"><span data-stu-id="f2f88-403">0x800A0E86</span></span></p></td>
<td><p><span data-ttu-id="f2f88-404">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="f2f88-404">For internal use only.</span></span> <span data-ttu-id="f2f88-405">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="f2f88-405">Don't use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="f2f88-406">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="f2f88-406">ADO/WFC equivalent</span></span>

<span data-ttu-id="f2f88-407">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="f2f88-407">Package: **com.ms.wfc.data**</span></span>

<span data-ttu-id="f2f88-408">Определены только следующие подмесяки эквивалентов ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="f2f88-408">Only the following subsets of ADO/WFC equivalents are defined.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f2f88-409">Константа</span><span class="sxs-lookup"><span data-stu-id="f2f88-409">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-410">AdoEnums.ErrorValue.BOUNDTOCOMMAND</span><span class="sxs-lookup"><span data-stu-id="f2f88-410">AdoEnums.ErrorValue.BOUNDTOCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-411">AdoEnums.ErrorValue.DATACONVERSION</span><span class="sxs-lookup"><span data-stu-id="f2f88-411">AdoEnums.ErrorValue.DATACONVERSION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-412">AdoEnums.ErrorValue.FEATURENOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="f2f88-412">AdoEnums.ErrorValue.FEATURENOTAVAILABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-413">AdoEnums.ErrorValue.ILLEGALOPERATION</span><span class="sxs-lookup"><span data-stu-id="f2f88-413">AdoEnums.ErrorValue.ILLEGALOPERATION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-414">AdoEnums.ErrorValue.INTRANSACTION</span><span class="sxs-lookup"><span data-stu-id="f2f88-414">AdoEnums.ErrorValue.INTRANSACTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-415">AdoEnums.ErrorValue.INVALIDARGUMENT</span><span class="sxs-lookup"><span data-stu-id="f2f88-415">AdoEnums.ErrorValue.INVALIDARGUMENT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-416">AdoEnums.ErrorValue.INVALIDCONNECTION</span><span class="sxs-lookup"><span data-stu-id="f2f88-416">AdoEnums.ErrorValue.INVALIDCONNECTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-417">AdoEnums.ErrorValue.INVALIDPARAMINFO</span><span class="sxs-lookup"><span data-stu-id="f2f88-417">AdoEnums.ErrorValue.INVALIDPARAMINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-418">AdoEnums.ErrorValue.ITEMNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="f2f88-418">AdoEnums.ErrorValue.ITEMNOTFOUND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-419">AdoEnums.ErrorValue.NOCURRENTRECORD</span><span class="sxs-lookup"><span data-stu-id="f2f88-419">AdoEnums.ErrorValue.NOCURRENTRECORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-420">AdoEnums.ErrorValue.NOTEXECUTING</span><span class="sxs-lookup"><span data-stu-id="f2f88-420">AdoEnums.ErrorValue.NOTEXECUTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-421">AdoEnums.ErrorValue.NOTREENTRANT</span><span class="sxs-lookup"><span data-stu-id="f2f88-421">AdoEnums.ErrorValue.NOTREENTRANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-422">AdoEnums.ErrorValue.OBJECTCLOSED</span><span class="sxs-lookup"><span data-stu-id="f2f88-422">AdoEnums.ErrorValue.OBJECTCLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-423">AdoEnums.ErrorValue.OBJECTINCOLLECTION</span><span class="sxs-lookup"><span data-stu-id="f2f88-423">AdoEnums.ErrorValue.OBJECTINCOLLECTION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-424">AdoEnums.ErrorValue.OBJECTNOTSET</span><span class="sxs-lookup"><span data-stu-id="f2f88-424">AdoEnums.ErrorValue.OBJECTNOTSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-425">AdoEnums.ErrorValue.OBJECTOPEN</span><span class="sxs-lookup"><span data-stu-id="f2f88-425">AdoEnums.ErrorValue.OBJECTOPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-426">AdoEnums.ErrorValue.OPERATIONCANCELLED</span><span class="sxs-lookup"><span data-stu-id="f2f88-426">AdoEnums.ErrorValue.OPERATIONCANCELLED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-427">AdoEnums.ErrorValue.PROVIDERNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="f2f88-427">AdoEnums.ErrorValue.PROVIDERNOTFOUND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-428">AdoEnums.ErrorValue.STILLCONNECTING</span><span class="sxs-lookup"><span data-stu-id="f2f88-428">AdoEnums.ErrorValue.STILLCONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2f88-429">AdoEnums.ErrorValue.STILLEXECUTING</span><span class="sxs-lookup"><span data-stu-id="f2f88-429">AdoEnums.ErrorValue.STILLEXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2f88-430">AdoEnums.ErrorValue.UNSAFEOPERATION</span><span class="sxs-lookup"><span data-stu-id="f2f88-430">AdoEnums.ErrorValue.UNSAFEOPERATION</span></span></p></td>
</tr>
</tbody>
</table>

