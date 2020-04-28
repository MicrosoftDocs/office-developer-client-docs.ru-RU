---
title: Еррорвалуинум (Справочник по базам данных Access на компьютере)
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
# <a name="errorvalueenum"></a><span data-ttu-id="57054-102">ErrorValueEnum</span><span class="sxs-lookup"><span data-stu-id="57054-102">ErrorValueEnum</span></span>

<span data-ttu-id="57054-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="57054-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="57054-104">Задает тип ошибки времени выполнения ADO.</span><span class="sxs-lookup"><span data-stu-id="57054-104">Specifies the type of ADO run-time error.</span></span>

<span data-ttu-id="57054-105">В списке ниже перечислены три формы номера ошибки.</span><span class="sxs-lookup"><span data-stu-id="57054-105">Three forms of the error number are listed:</span></span>

- <span data-ttu-id="57054-106">Положительное десятичное число — два нижних байта полного числа в десятичном формате.</span><span class="sxs-lookup"><span data-stu-id="57054-106">Positive decimal — the low two bytes of the full number in decimal format.</span></span> <span data-ttu-id="57054-107">Этот номер отображается в диалоговом окне "сообщение об ошибке Visual Basic" по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="57054-107">This number is displayed in the default Visual Basic error message dialog box.</span></span> <span data-ttu-id="57054-108">Например, ошибка времени выполнения ' 3707 '.</span><span class="sxs-lookup"><span data-stu-id="57054-108">For example, Run-time error '3707'.</span></span>

- <span data-ttu-id="57054-109">Отрицательное десятичное число — десятичное преобразование полного номера ошибки.</span><span class="sxs-lookup"><span data-stu-id="57054-109">Negative decimal — The decimal translation of the full error number.</span></span>

- <span data-ttu-id="57054-110">Шестнадцатеричное — шестнадцатеричное представление полного номера ошибки.</span><span class="sxs-lookup"><span data-stu-id="57054-110">Hexadecimal — The hexadecimal representation of the full error number.</span></span> <span data-ttu-id="57054-111">Код средства Windows находится в четвертой цифре.</span><span class="sxs-lookup"><span data-stu-id="57054-111">The Windows facility code is in the fourth digit.</span></span> <span data-ttu-id="57054-112">Код устройства для номеров ошибок ADO — *A*. Пример: 0x800***A***0E7B.</span><span class="sxs-lookup"><span data-stu-id="57054-112">The facility code for ADO error numbers is *A*. For example: 0x800***A***0E7B.</span></span>

> [!NOTE]
> <span data-ttu-id="57054-113">Ошибки OLE DB могут передаваться в приложение ADO.</span><span class="sxs-lookup"><span data-stu-id="57054-113">OLE DB errors may be passed to your ADO application.</span></span> <span data-ttu-id="57054-114">Как правило, они могут быть идентифицированы с помощью кода средства Windows *4*.</span><span class="sxs-lookup"><span data-stu-id="57054-114">Typically, these can be identified by a Windows facility code of *4*.</span></span> <span data-ttu-id="57054-115">Например, 0x800_**4**_.... Более подробную информацию об этих номерах можно найти в главе 16 *Справочника программиста OLE DB.*</span><span class="sxs-lookup"><span data-stu-id="57054-115">For example, 0x800_**4**_.... For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="57054-116">Константа</span><span class="sxs-lookup"><span data-stu-id="57054-116">Constant</span></span></p></th>
<th><p><span data-ttu-id="57054-117">Значение</span><span class="sxs-lookup"><span data-stu-id="57054-117">Value</span></span></p></th>
<th><p><span data-ttu-id="57054-118">Описание</span><span class="sxs-lookup"><span data-stu-id="57054-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57054-119"><strong>адеррбаундтокомманд</strong></span><span class="sxs-lookup"><span data-stu-id="57054-119"><strong>adErrBoundToCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-120">3707</span><span class="sxs-lookup"><span data-stu-id="57054-120">3707</span></span><br />
<span data-ttu-id="57054-121">— 2146824581</span><span class="sxs-lookup"><span data-stu-id="57054-121">-2146824581</span></span><br />
<span data-ttu-id="57054-122">0x800A0E7B</span><span class="sxs-lookup"><span data-stu-id="57054-122">0x800A0E7B</span></span></p></td>
<td><p><span data-ttu-id="57054-123">Не удается изменить свойство <strong>ActiveConnection</strong> объекта <strong>Recordset</strong> , который содержит объект <strong>Command</strong> в качестве источника.</span><span class="sxs-lookup"><span data-stu-id="57054-123">Cannot change the <strong>ActiveConnection</strong> property of a <strong>Recordset</strong> object which has a <strong>Command</strong> object as its source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-124"><strong>адеррканноткомплете</strong></span><span class="sxs-lookup"><span data-stu-id="57054-124"><strong>adErrCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-125">3732</span><span class="sxs-lookup"><span data-stu-id="57054-125">3732</span></span><br />
<span data-ttu-id="57054-126">— 2146824556</span><span class="sxs-lookup"><span data-stu-id="57054-126">-2146824556</span></span><br />
<span data-ttu-id="57054-127">0x800A0E94</span><span class="sxs-lookup"><span data-stu-id="57054-127">0x800A0E94</span></span></p></td>
<td><p><span data-ttu-id="57054-128">Серверу не удается завершить операцию.</span><span class="sxs-lookup"><span data-stu-id="57054-128">Server cannot complete the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-129"><strong>адерркантчанжеконнектион</strong></span><span class="sxs-lookup"><span data-stu-id="57054-129"><strong>adErrCantChangeConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-130">3748</span><span class="sxs-lookup"><span data-stu-id="57054-130">3748</span></span><br />
<span data-ttu-id="57054-131">— 2146824540</span><span class="sxs-lookup"><span data-stu-id="57054-131">-2146824540</span></span><br />
<span data-ttu-id="57054-132">0x800A0EA4</span><span class="sxs-lookup"><span data-stu-id="57054-132">0x800A0EA4</span></span></p></td>
<td><p><span data-ttu-id="57054-133">Подключение было отклонено.</span><span class="sxs-lookup"><span data-stu-id="57054-133">Connection was denied.</span></span> <span data-ttu-id="57054-134">Для нового подключения, которое вы запросили, отличаются характеристики, которые уже используются.</span><span class="sxs-lookup"><span data-stu-id="57054-134">New connection you requested has different characteristics than the one already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-135"><strong>адерркантчанжепровидер</strong></span><span class="sxs-lookup"><span data-stu-id="57054-135"><strong>adErrCantChangeProvider</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-136">3220</span><span class="sxs-lookup"><span data-stu-id="57054-136">3220</span></span><br />
<span data-ttu-id="57054-137">— 2146825068</span><span class="sxs-lookup"><span data-stu-id="57054-137">-2146825068</span></span><br />
<span data-ttu-id="57054-138">0X800A0C94</span><span class="sxs-lookup"><span data-stu-id="57054-138">0X800A0C94</span></span></p></td>
<td><p><span data-ttu-id="57054-139">Указанный поставщик отличается от того, который уже используется.</span><span class="sxs-lookup"><span data-stu-id="57054-139">Supplied provider is different from the one already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-140"><strong>адерркантконвертвалуе</strong></span><span class="sxs-lookup"><span data-stu-id="57054-140"><strong>adErrCantConvertvalue</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-141">3724</span><span class="sxs-lookup"><span data-stu-id="57054-141">3724</span></span><br />
<span data-ttu-id="57054-142">— 2146824564</span><span class="sxs-lookup"><span data-stu-id="57054-142">-2146824564</span></span><br />
<span data-ttu-id="57054-143">0x800A0E8C</span><span class="sxs-lookup"><span data-stu-id="57054-143">0x800A0E8C</span></span></p></td>
<td><p><span data-ttu-id="57054-144">Значение данных не может быть преобразовано по причинам, отличным от несоответствия знака или переполнения данных.</span><span class="sxs-lookup"><span data-stu-id="57054-144">Data value cannot be converted for reasons other than sign mismatch or data overflow.</span></span> <span data-ttu-id="57054-145">Например, преобразование приведет к усечению данных.</span><span class="sxs-lookup"><span data-stu-id="57054-145">For example, conversion would have truncated data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-146"><strong>адеррканткреате</strong></span><span class="sxs-lookup"><span data-stu-id="57054-146"><strong>adErrCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-147">3725</span><span class="sxs-lookup"><span data-stu-id="57054-147">3725</span></span><br />
<span data-ttu-id="57054-148">— 2146824563</span><span class="sxs-lookup"><span data-stu-id="57054-148">-2146824563</span></span><br />
<span data-ttu-id="57054-149">0x800A0E8D</span><span class="sxs-lookup"><span data-stu-id="57054-149">0x800A0E8D</span></span></p></td>
<td><p><span data-ttu-id="57054-150">Значение данных не может быть задано или получено, так как тип данных поля неизвестен или у поставщика недостаточно ресурсов для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="57054-150">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-151"><strong>адерркаталогнотсет</strong></span><span class="sxs-lookup"><span data-stu-id="57054-151"><strong>adErrCatalogNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-152">3747</span><span class="sxs-lookup"><span data-stu-id="57054-152">3747</span></span><br />
<span data-ttu-id="57054-153">— 2146824541</span><span class="sxs-lookup"><span data-stu-id="57054-153">-2146824541</span></span><br />
<span data-ttu-id="57054-154">0x800A0EA3</span><span class="sxs-lookup"><span data-stu-id="57054-154">0x800A0EA3</span></span></p></td>
<td><p><span data-ttu-id="57054-155">Для операции требуется допустимый <strong>ParentCatalog</strong>.</span><span class="sxs-lookup"><span data-stu-id="57054-155">Operation requires a valid <strong>ParentCatalog</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-156"><strong>адеррколумннотонсисров</strong></span><span class="sxs-lookup"><span data-stu-id="57054-156"><strong>adErrColumnNotOnThisRow</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-157">3726</span><span class="sxs-lookup"><span data-stu-id="57054-157">3726</span></span><br />
<span data-ttu-id="57054-158">— 2146824562</span><span class="sxs-lookup"><span data-stu-id="57054-158">-2146824562</span></span><br />
<span data-ttu-id="57054-159">0x800A0E8E</span><span class="sxs-lookup"><span data-stu-id="57054-159">0x800A0E8E</span></span></p></td>
<td><p><span data-ttu-id="57054-160">Запись не содержит это поле.</span><span class="sxs-lookup"><span data-stu-id="57054-160">Record does not contain this field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-161"><strong>адеррдатаконверсион</strong></span><span class="sxs-lookup"><span data-stu-id="57054-161"><strong>adErrDataConversion</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-162">3421</span><span class="sxs-lookup"><span data-stu-id="57054-162">3421</span></span><br />
<span data-ttu-id="57054-163">— 2146824867</span><span class="sxs-lookup"><span data-stu-id="57054-163">-2146824867</span></span><br />
<span data-ttu-id="57054-164">0x800A0D5D</span><span class="sxs-lookup"><span data-stu-id="57054-164">0x800A0D5D</span></span></p></td>
<td><p><span data-ttu-id="57054-165">Приложение использует значение неправильного типа для текущей операции.</span><span class="sxs-lookup"><span data-stu-id="57054-165">Application uses a value of the wrong type for the current operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-166"><strong>адеррдатаоверфлов</strong></span><span class="sxs-lookup"><span data-stu-id="57054-166"><strong>adErrDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-167">3721</span><span class="sxs-lookup"><span data-stu-id="57054-167">3721</span></span><br />
<span data-ttu-id="57054-168">— 2146824567</span><span class="sxs-lookup"><span data-stu-id="57054-168">-2146824567</span></span><br />
<span data-ttu-id="57054-169">0x800A0E89</span><span class="sxs-lookup"><span data-stu-id="57054-169">0x800A0E89</span></span></p></td>
<td><p><span data-ttu-id="57054-170">Слишком большое значение данных для представления типом данных поля.</span><span class="sxs-lookup"><span data-stu-id="57054-170">Data value is too large to be represented by the field data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-171"><strong>адеррделресаутофскопе</strong></span><span class="sxs-lookup"><span data-stu-id="57054-171"><strong>adErrDelResOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-172">3738</span><span class="sxs-lookup"><span data-stu-id="57054-172">3738</span></span><br />
<span data-ttu-id="57054-173">— 2146824550</span><span class="sxs-lookup"><span data-stu-id="57054-173">-2146824550</span></span><br />
<span data-ttu-id="57054-174">0x800A0E9A</span><span class="sxs-lookup"><span data-stu-id="57054-174">0x800A0E9A</span></span></p></td>
<td><p><span data-ttu-id="57054-175">URL-адрес удаляемого объекта находится вне области текущей записи.</span><span class="sxs-lookup"><span data-stu-id="57054-175">URL of the object to be deleted is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-176"><strong>адеррденинотсуппортед</strong></span><span class="sxs-lookup"><span data-stu-id="57054-176"><strong>adErrDenyNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-177">3750</span><span class="sxs-lookup"><span data-stu-id="57054-177">3750</span></span><br />
<span data-ttu-id="57054-178">— 2146824538</span><span class="sxs-lookup"><span data-stu-id="57054-178">-2146824538</span></span><br />
<span data-ttu-id="57054-179">0x800A0EA6</span><span class="sxs-lookup"><span data-stu-id="57054-179">0x800A0EA6</span></span></p></td>
<td><p><span data-ttu-id="57054-180">Поставщик не поддерживает ограничения на общий доступ.</span><span class="sxs-lookup"><span data-stu-id="57054-180">Provider does not support sharing restrictions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-181"><strong>адеррденитипенотсуппортед</strong></span><span class="sxs-lookup"><span data-stu-id="57054-181"><strong>adErrDenyTypeNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-182">3751</span><span class="sxs-lookup"><span data-stu-id="57054-182">3751</span></span><br />
<span data-ttu-id="57054-183">— 2146824537</span><span class="sxs-lookup"><span data-stu-id="57054-183">-2146824537</span></span><br />
<span data-ttu-id="57054-184">0x800A0EA7</span><span class="sxs-lookup"><span data-stu-id="57054-184">0x800A0EA7</span></span></p></td>
<td><p><span data-ttu-id="57054-185">Поставщик не поддерживает запрошенный тип ограничения на совместное использование.</span><span class="sxs-lookup"><span data-stu-id="57054-185">Provider does not support the requested kind of sharing restriction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-186"><strong>адеррфеатуренотаваилабле</strong></span><span class="sxs-lookup"><span data-stu-id="57054-186"><strong>adErrFeatureNotAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-187">3251</span><span class="sxs-lookup"><span data-stu-id="57054-187">3251</span></span><br />
<span data-ttu-id="57054-188">— 2146825037</span><span class="sxs-lookup"><span data-stu-id="57054-188">-2146825037</span></span><br />
<span data-ttu-id="57054-189">0x800A0CB3</span><span class="sxs-lookup"><span data-stu-id="57054-189">0x800A0CB3</span></span></p></td>
<td><p><span data-ttu-id="57054-190">Объект или поставщик не могут выполнять запрошенную операцию.</span><span class="sxs-lookup"><span data-stu-id="57054-190">Object or provider is not capable of performing requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-191"><strong>адеррфиелдсупдатефаилед</strong></span><span class="sxs-lookup"><span data-stu-id="57054-191"><strong>adErrFieldsUpdateFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-192">3749</span><span class="sxs-lookup"><span data-stu-id="57054-192">3749</span></span><br />
<span data-ttu-id="57054-193">— 2146824539</span><span class="sxs-lookup"><span data-stu-id="57054-193">-2146824539</span></span><br />
<span data-ttu-id="57054-194">0x800A0EA5</span><span class="sxs-lookup"><span data-stu-id="57054-194">0x800A0EA5</span></span></p></td>
<td><p><span data-ttu-id="57054-195">Не удалось обновить поля.</span><span class="sxs-lookup"><span data-stu-id="57054-195">Fields update failed.</span></span> <span data-ttu-id="57054-196">Для получения дополнительных сведений изучите свойство <strong>Status</strong> отдельных объектов Field.</span><span class="sxs-lookup"><span data-stu-id="57054-196">For further information, examine the <strong>Status</strong> property of individual field objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-197"><strong>адерриллегалоператион</strong></span><span class="sxs-lookup"><span data-stu-id="57054-197"><strong>adErrIllegalOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-198">3219</span><span class="sxs-lookup"><span data-stu-id="57054-198">3219</span></span><br />
<span data-ttu-id="57054-199">— 2146825069</span><span class="sxs-lookup"><span data-stu-id="57054-199">-2146825069</span></span><br />
<span data-ttu-id="57054-200">0x800A0C93</span><span class="sxs-lookup"><span data-stu-id="57054-200">0x800A0C93</span></span></p></td>
<td><p><span data-ttu-id="57054-201">Операция не разрешена в данном контексте.</span><span class="sxs-lookup"><span data-stu-id="57054-201">Operation is not allowed in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-202"><strong>адерринтегритивиолатион</strong></span><span class="sxs-lookup"><span data-stu-id="57054-202"><strong>adErrIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-203">3719</span><span class="sxs-lookup"><span data-stu-id="57054-203">3719</span></span><br />
<span data-ttu-id="57054-204">— 2146824569</span><span class="sxs-lookup"><span data-stu-id="57054-204">-2146824569</span></span><br />
<span data-ttu-id="57054-205">0x800A0E87</span><span class="sxs-lookup"><span data-stu-id="57054-205">0x800A0E87</span></span></p></td>
<td><p><span data-ttu-id="57054-206">Значение данных вступает в противоречие с ограничениями целостности поля.</span><span class="sxs-lookup"><span data-stu-id="57054-206">Data value conflicts with the integrity constraints of the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-207"><strong>адерринтрансактион</strong></span><span class="sxs-lookup"><span data-stu-id="57054-207"><strong>adErrInTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-208">3246</span><span class="sxs-lookup"><span data-stu-id="57054-208">3246</span></span><br />
<span data-ttu-id="57054-209">— 2146825042</span><span class="sxs-lookup"><span data-stu-id="57054-209">-2146825042</span></span><br />
<span data-ttu-id="57054-210">0x800A0CAE</span><span class="sxs-lookup"><span data-stu-id="57054-210">0x800A0CAE</span></span></p></td>
<td><p><span data-ttu-id="57054-211">Объект <strong>Connection</strong> не может быть закрыт явным образом во время транзакции.</span><span class="sxs-lookup"><span data-stu-id="57054-211"><strong>Connection</strong> object cannot be explicitly closed while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-212"><strong>адерринвалидаргумент</strong></span><span class="sxs-lookup"><span data-stu-id="57054-212"><strong>adErrInvalidArgument</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-213">3001</span><span class="sxs-lookup"><span data-stu-id="57054-213">3001</span></span><br />
<span data-ttu-id="57054-214">— 2146825287</span><span class="sxs-lookup"><span data-stu-id="57054-214">-2146825287</span></span><br />
<span data-ttu-id="57054-215">0x800A0BB9</span><span class="sxs-lookup"><span data-stu-id="57054-215">0x800A0BB9</span></span></p></td>
<td><p><span data-ttu-id="57054-216">Аргументы имеют неверный тип, выходят за пределы допустимого диапазона или конфликтуют друг с другом.</span><span class="sxs-lookup"><span data-stu-id="57054-216">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-217"><strong>адерринвалидконнектион</strong></span><span class="sxs-lookup"><span data-stu-id="57054-217"><strong>adErrInvalidConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-218">3709</span><span class="sxs-lookup"><span data-stu-id="57054-218">3709</span></span><br />
<span data-ttu-id="57054-219">— 2146824579</span><span class="sxs-lookup"><span data-stu-id="57054-219">-2146824579</span></span><br />
<span data-ttu-id="57054-220">0x800A0E7D</span><span class="sxs-lookup"><span data-stu-id="57054-220">0x800A0E7D</span></span></p></td>
<td><p><span data-ttu-id="57054-221">Невозможно использовать соединение для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="57054-221">The connection cannot be used to perform this operation.</span></span> <span data-ttu-id="57054-222">Он либо закрывается, либо не является допустимым в данном контексте.</span><span class="sxs-lookup"><span data-stu-id="57054-222">It is either closed or invalid in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-223"><strong>адерринвалидпараминфо</strong></span><span class="sxs-lookup"><span data-stu-id="57054-223"><strong>adErrInvalidParamInfo</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-224">3708</span><span class="sxs-lookup"><span data-stu-id="57054-224">3708</span></span><br />
<span data-ttu-id="57054-225">— 2146824580</span><span class="sxs-lookup"><span data-stu-id="57054-225">-2146824580</span></span><br />
<span data-ttu-id="57054-226">0x800A0E7C</span><span class="sxs-lookup"><span data-stu-id="57054-226">0x800A0E7C</span></span></p></td>
<td><p><span data-ttu-id="57054-227">Объект <strong>Parameter</strong> определен неправильно.</span><span class="sxs-lookup"><span data-stu-id="57054-227"><strong>Parameter</strong> object is improperly defined.</span></span> <span data-ttu-id="57054-228">Предоставлены несогласованные или неполные сведения.</span><span class="sxs-lookup"><span data-stu-id="57054-228">Inconsistent or incomplete information was provided.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-229"><strong>адерринвалидтрансактион</strong></span><span class="sxs-lookup"><span data-stu-id="57054-229"><strong>adErrInvalidTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-230">3714</span><span class="sxs-lookup"><span data-stu-id="57054-230">3714</span></span><br />
<span data-ttu-id="57054-231">— 2146824574</span><span class="sxs-lookup"><span data-stu-id="57054-231">-2146824574</span></span><br />
<span data-ttu-id="57054-232">0x800A0E82</span><span class="sxs-lookup"><span data-stu-id="57054-232">0x800A0E82</span></span></p></td>
<td><p><span data-ttu-id="57054-233">Координация транзакции является недопустимой или не запущена.</span><span class="sxs-lookup"><span data-stu-id="57054-233">Coordinating transaction is invalid or has not started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-234"><strong>адерринвалидурл</strong></span><span class="sxs-lookup"><span data-stu-id="57054-234"><strong>adErrInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-235">3729</span><span class="sxs-lookup"><span data-stu-id="57054-235">3729</span></span><br />
<span data-ttu-id="57054-236">— 2146824559</span><span class="sxs-lookup"><span data-stu-id="57054-236">-2146824559</span></span><br />
<span data-ttu-id="57054-237">0x800A0E91</span><span class="sxs-lookup"><span data-stu-id="57054-237">0x800A0E91</span></span></p></td>
<td><p><span data-ttu-id="57054-238">URL-адрес содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="57054-238">URL contains invalid characters.</span></span> <span data-ttu-id="57054-239">Убедитесь, что URL-адрес введен правильно.</span><span class="sxs-lookup"><span data-stu-id="57054-239">Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-240"><strong>адерритемнотфаунд</strong></span><span class="sxs-lookup"><span data-stu-id="57054-240"><strong>adErrItemNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-241">3265</span><span class="sxs-lookup"><span data-stu-id="57054-241">3265</span></span><br />
<span data-ttu-id="57054-242">— 2146825023</span><span class="sxs-lookup"><span data-stu-id="57054-242">-2146825023</span></span><br />
<span data-ttu-id="57054-243">0x800A0CC1</span><span class="sxs-lookup"><span data-stu-id="57054-243">0x800A0CC1</span></span></p></td>
<td><p><span data-ttu-id="57054-244">Не удается найти элемент в семействе, соответствующем запрошенному имени или порядковому номеру.</span><span class="sxs-lookup"><span data-stu-id="57054-244">Item cannot be found in the collection corresponding to the requested name or ordinal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-245"><strong>адеррнокуррентрекорд</strong></span><span class="sxs-lookup"><span data-stu-id="57054-245"><strong>adErrNoCurrentRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-246">3021</span><span class="sxs-lookup"><span data-stu-id="57054-246">3021</span></span><br />
<span data-ttu-id="57054-247">— 2146825267</span><span class="sxs-lookup"><span data-stu-id="57054-247">-2146825267</span></span><br />
<span data-ttu-id="57054-248">0x800A0BCD</span><span class="sxs-lookup"><span data-stu-id="57054-248">0x800A0BCD</span></span></p></td>
<td><p><span data-ttu-id="57054-249">Либо <strong>BOF</strong> , либо <strong>EOF</strong> имеет значение true, или текущая запись была удалена.</span><span class="sxs-lookup"><span data-stu-id="57054-249">Either <strong>BOF</strong> or <strong>EOF</strong> is True, or the current record has been deleted.</span></span> <span data-ttu-id="57054-250">Для выполнения запрошенной операции требуется текущая запись.</span><span class="sxs-lookup"><span data-stu-id="57054-250">Requested operation requires a current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-251"><strong>адеррнотексекутинг</strong></span><span class="sxs-lookup"><span data-stu-id="57054-251"><strong>adErrNotExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-252">3715</span><span class="sxs-lookup"><span data-stu-id="57054-252">3715</span></span><br />
<span data-ttu-id="57054-253">— 2146824573</span><span class="sxs-lookup"><span data-stu-id="57054-253">-2146824573</span></span><br />
<span data-ttu-id="57054-254">0x800A0E83</span><span class="sxs-lookup"><span data-stu-id="57054-254">0x800A0E83</span></span></p></td>
<td><p><span data-ttu-id="57054-255">Не удается выполнить операцию, пока не выполняется.</span><span class="sxs-lookup"><span data-stu-id="57054-255">Operation cannot be performed while not executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-256"><strong>адеррнотринтрант</strong></span><span class="sxs-lookup"><span data-stu-id="57054-256"><strong>adErrNotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-257">3710</span><span class="sxs-lookup"><span data-stu-id="57054-257">3710</span></span><br />
<span data-ttu-id="57054-258">— 2146824578</span><span class="sxs-lookup"><span data-stu-id="57054-258">-2146824578</span></span><br />
<span data-ttu-id="57054-259">0x800A0E7E</span><span class="sxs-lookup"><span data-stu-id="57054-259">0x800A0E7E</span></span></p></td>
<td><p><span data-ttu-id="57054-260">Не удается выполнить операцию во время обработки события.</span><span class="sxs-lookup"><span data-stu-id="57054-260">Operation cannot be performed while processing event.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-261"><strong>адерробжектклосед</strong></span><span class="sxs-lookup"><span data-stu-id="57054-261"><strong>adErrObjectClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-262">3704</span><span class="sxs-lookup"><span data-stu-id="57054-262">3704</span></span><br />
<span data-ttu-id="57054-263">— 2146824584</span><span class="sxs-lookup"><span data-stu-id="57054-263">-2146824584</span></span><br />
<span data-ttu-id="57054-264">0x800A0E78</span><span class="sxs-lookup"><span data-stu-id="57054-264">0x800A0E78</span></span></p></td>
<td><p><span data-ttu-id="57054-265">Операция не разрешена при закрытии объекта.</span><span class="sxs-lookup"><span data-stu-id="57054-265">Operation is not allowed when the object is closed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-266"><strong>адерробжектинколлектион</strong></span><span class="sxs-lookup"><span data-stu-id="57054-266"><strong>adErrObjectInCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-267">3367</span><span class="sxs-lookup"><span data-stu-id="57054-267">3367</span></span><br />
<span data-ttu-id="57054-268">— 2146824921</span><span class="sxs-lookup"><span data-stu-id="57054-268">-2146824921</span></span><br />
<span data-ttu-id="57054-269">0x800A0D27</span><span class="sxs-lookup"><span data-stu-id="57054-269">0x800A0D27</span></span></p></td>
<td><p><span data-ttu-id="57054-270">Объект уже находится в коллекции.</span><span class="sxs-lookup"><span data-stu-id="57054-270">Object is already in collection.</span></span> <span data-ttu-id="57054-271">Не удается добавить.</span><span class="sxs-lookup"><span data-stu-id="57054-271">Cannot append.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-272"><strong>адерробжектнотсет</strong></span><span class="sxs-lookup"><span data-stu-id="57054-272"><strong>adErrObjectNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-273">3420</span><span class="sxs-lookup"><span data-stu-id="57054-273">3420</span></span><br />
<span data-ttu-id="57054-274">— 2146824868</span><span class="sxs-lookup"><span data-stu-id="57054-274">-2146824868</span></span><br />
<span data-ttu-id="57054-275">0x800A0D5C</span><span class="sxs-lookup"><span data-stu-id="57054-275">0x800A0D5C</span></span></p></td>
<td><p><span data-ttu-id="57054-276">Объект больше не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="57054-276">Object is no longer valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-277"><strong>адерробжектопен</strong></span><span class="sxs-lookup"><span data-stu-id="57054-277"><strong>adErrObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-278">3705</span><span class="sxs-lookup"><span data-stu-id="57054-278">3705</span></span><br />
<span data-ttu-id="57054-279">— 2146824583</span><span class="sxs-lookup"><span data-stu-id="57054-279">-2146824583</span></span><br />
<span data-ttu-id="57054-280">0x800A0E79</span><span class="sxs-lookup"><span data-stu-id="57054-280">0x800A0E79</span></span></p></td>
<td><p><span data-ttu-id="57054-281">Операция не разрешена, если объект открыт.</span><span class="sxs-lookup"><span data-stu-id="57054-281">Operation is not allowed when the object is open.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-282"><strong>адерропенингфиле</strong></span><span class="sxs-lookup"><span data-stu-id="57054-282"><strong>adErrOpeningFile</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-283">3002</span><span class="sxs-lookup"><span data-stu-id="57054-283">3002</span></span><br />
<span data-ttu-id="57054-284">— 2146825286</span><span class="sxs-lookup"><span data-stu-id="57054-284">-2146825286</span></span><br />
<span data-ttu-id="57054-285">0x800A0BBA</span><span class="sxs-lookup"><span data-stu-id="57054-285">0x800A0BBA</span></span></p></td>
<td><p><span data-ttu-id="57054-286">Не удалось открыть файл.</span><span class="sxs-lookup"><span data-stu-id="57054-286">File could not be opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-287"><strong>адерроператионканцеллед</strong></span><span class="sxs-lookup"><span data-stu-id="57054-287"><strong>adErrOperationCancelled</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-288">3712</span><span class="sxs-lookup"><span data-stu-id="57054-288">3712</span></span><br />
<span data-ttu-id="57054-289">— 2146824576</span><span class="sxs-lookup"><span data-stu-id="57054-289">-2146824576</span></span><br />
<span data-ttu-id="57054-290">0x800A0E80</span><span class="sxs-lookup"><span data-stu-id="57054-290">0x800A0E80</span></span></p></td>
<td><p><span data-ttu-id="57054-291">Операция отменена пользователем.</span><span class="sxs-lookup"><span data-stu-id="57054-291">Operation has been cancelled by the user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-292"><strong>адерраутофспаце</strong></span><span class="sxs-lookup"><span data-stu-id="57054-292"><strong>adErrOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-293">3734</span><span class="sxs-lookup"><span data-stu-id="57054-293">3734</span></span><br />
<span data-ttu-id="57054-294">— 2146824554</span><span class="sxs-lookup"><span data-stu-id="57054-294">-2146824554</span></span><br />
<span data-ttu-id="57054-295">0x800A0E96</span><span class="sxs-lookup"><span data-stu-id="57054-295">0x800A0E96</span></span></p></td>
<td><p><span data-ttu-id="57054-296">Не удается выполнить операцию.</span><span class="sxs-lookup"><span data-stu-id="57054-296">Operation cannot be performed.</span></span> <span data-ttu-id="57054-297">Поставщик не может получить достаточно места для хранения.</span><span class="sxs-lookup"><span data-stu-id="57054-297">Provider cannot obtain enough storage space.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-298"><strong>адеррпермиссиондениед</strong></span><span class="sxs-lookup"><span data-stu-id="57054-298"><strong>adErrPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-299">3720</span><span class="sxs-lookup"><span data-stu-id="57054-299">3720</span></span><br />
<span data-ttu-id="57054-300">— 2146824568</span><span class="sxs-lookup"><span data-stu-id="57054-300">-2146824568</span></span><br />
<span data-ttu-id="57054-301">0x800A0E88</span><span class="sxs-lookup"><span data-stu-id="57054-301">0x800A0E88</span></span></p></td>
<td><p><span data-ttu-id="57054-302">Разрешение инсуффицент запрещает запись в поле.</span><span class="sxs-lookup"><span data-stu-id="57054-302">Insufficent permission prevents writing to the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-303"><strong>адеррпровидерфаилед</strong></span><span class="sxs-lookup"><span data-stu-id="57054-303"><strong>adErrProviderFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-304">3000</span><span class="sxs-lookup"><span data-stu-id="57054-304">3000</span></span><br />
<span data-ttu-id="57054-305">— 2146825288</span><span class="sxs-lookup"><span data-stu-id="57054-305">-2146825288</span></span><br />
<span data-ttu-id="57054-306">0x800A0BB8</span><span class="sxs-lookup"><span data-stu-id="57054-306">0x800A0BB8</span></span></p></td>
<td><p><span data-ttu-id="57054-307">Поставщику не удалось выполнить запрошенную операцию.</span><span class="sxs-lookup"><span data-stu-id="57054-307">Provider failed to perform the requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-308"><strong>адеррпровидернотфаунд</strong></span><span class="sxs-lookup"><span data-stu-id="57054-308"><strong>adErrProviderNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-309">3706</span><span class="sxs-lookup"><span data-stu-id="57054-309">3706</span></span><br />
<span data-ttu-id="57054-310">— 2146824582</span><span class="sxs-lookup"><span data-stu-id="57054-310">-2146824582</span></span><br />
<span data-ttu-id="57054-311">0x800A0E7A</span><span class="sxs-lookup"><span data-stu-id="57054-311">0x800A0E7A</span></span></p></td>
<td><p><span data-ttu-id="57054-312">Не удается найти поставщика.</span><span class="sxs-lookup"><span data-stu-id="57054-312">Provider cannot be found.</span></span> <span data-ttu-id="57054-313">Он может быть неправильно установлен.</span><span class="sxs-lookup"><span data-stu-id="57054-313">It may not be properly installed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-314"><strong>адеррреадфиле</strong></span><span class="sxs-lookup"><span data-stu-id="57054-314"><strong>adErrReadFile</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-315">3003</span><span class="sxs-lookup"><span data-stu-id="57054-315">3003</span></span><br />
<span data-ttu-id="57054-316">— 2146825285</span><span class="sxs-lookup"><span data-stu-id="57054-316">-2146825285</span></span><br />
<span data-ttu-id="57054-317">0x800A0BBB</span><span class="sxs-lookup"><span data-stu-id="57054-317">0x800A0BBB</span></span></p></td>
<td><p><span data-ttu-id="57054-318">Не удалось прочитать файл.</span><span class="sxs-lookup"><span data-stu-id="57054-318">File could not be read.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-319"><strong>адеррресаурцеексистс</strong></span><span class="sxs-lookup"><span data-stu-id="57054-319"><strong>adErrResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-320">3731</span><span class="sxs-lookup"><span data-stu-id="57054-320">3731</span></span><br />
<span data-ttu-id="57054-321">— 2146824557</span><span class="sxs-lookup"><span data-stu-id="57054-321">-2146824557</span></span><br />
<span data-ttu-id="57054-322">0x800A0E93</span><span class="sxs-lookup"><span data-stu-id="57054-322">0x800A0E93</span></span></p></td>
<td><p><span data-ttu-id="57054-323">Не удается выполнить операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="57054-323">Copy operation cannot be performed.</span></span> <span data-ttu-id="57054-324">Объект с именем URL-адреса назначения уже существует.</span><span class="sxs-lookup"><span data-stu-id="57054-324">Object named by destination URL already exists.</span></span> <span data-ttu-id="57054-325">Укажите <strong>адкопйоверврите</strong> , чтобы заменить объект.</span><span class="sxs-lookup"><span data-stu-id="57054-325">Specify <strong>adCopyOverwrite</strong> to replace the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-326"><strong>адеррресаурцелоккед</strong></span><span class="sxs-lookup"><span data-stu-id="57054-326"><strong>adErrResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-327">3730</span><span class="sxs-lookup"><span data-stu-id="57054-327">3730</span></span><br />
<span data-ttu-id="57054-328">— 2146824558</span><span class="sxs-lookup"><span data-stu-id="57054-328">-2146824558</span></span><br />
<span data-ttu-id="57054-329">0x800A0E92</span><span class="sxs-lookup"><span data-stu-id="57054-329">0x800A0E92</span></span></p></td>
<td><p><span data-ttu-id="57054-330">Объект, представленный указанным URL-адресом, заблокирован одним или несколькими другими процессами.</span><span class="sxs-lookup"><span data-stu-id="57054-330">Object represented by the specified URL is locked by one or more other processes.</span></span> <span data-ttu-id="57054-331">Дождитесь завершения процесса и повторите операцию.</span><span class="sxs-lookup"><span data-stu-id="57054-331">Wait until the process has finished and attempt the operation again.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-332"><strong>адеррресаурцеаутофскопе</strong></span><span class="sxs-lookup"><span data-stu-id="57054-332"><strong>adErrResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-333">3735</span><span class="sxs-lookup"><span data-stu-id="57054-333">3735</span></span><br />
<span data-ttu-id="57054-334">— 2146824553</span><span class="sxs-lookup"><span data-stu-id="57054-334">-2146824553</span></span><br />
<span data-ttu-id="57054-335">0x800A0E97</span><span class="sxs-lookup"><span data-stu-id="57054-335">0x800A0E97</span></span></p></td>
<td><p><span data-ttu-id="57054-336">Исходный или конечный URL-адрес находится вне области текущей записи.</span><span class="sxs-lookup"><span data-stu-id="57054-336">Source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-337"><strong>адеррсчемавиолатион</strong></span><span class="sxs-lookup"><span data-stu-id="57054-337"><strong>adErrSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-338">3722</span><span class="sxs-lookup"><span data-stu-id="57054-338">3722</span></span><br />
<span data-ttu-id="57054-339">— 2146824566</span><span class="sxs-lookup"><span data-stu-id="57054-339">-2146824566</span></span><br />
<span data-ttu-id="57054-340">0x800A0E8A</span><span class="sxs-lookup"><span data-stu-id="57054-340">0x800A0E8A</span></span></p></td>
<td><p><span data-ttu-id="57054-341">Значение данных вступает в противоречие с типом данных или ограничениями поля.</span><span class="sxs-lookup"><span data-stu-id="57054-341">Data value conflicts with the data type or constraints of the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-342"><strong>адеррсигнмисматч</strong></span><span class="sxs-lookup"><span data-stu-id="57054-342"><strong>adErrSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-343">3723</span><span class="sxs-lookup"><span data-stu-id="57054-343">3723</span></span><br />
<span data-ttu-id="57054-344">— 2146824565</span><span class="sxs-lookup"><span data-stu-id="57054-344">-2146824565</span></span><br />
<span data-ttu-id="57054-345">0x800A0E8B</span><span class="sxs-lookup"><span data-stu-id="57054-345">0x800A0E8B</span></span></p></td>
<td><p><span data-ttu-id="57054-346">Произошел сбой преобразования, так как значение данных было подписано, а тип данных поля, используемый поставщиком, не подписан.</span><span class="sxs-lookup"><span data-stu-id="57054-346">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-347"><strong>адеррстиллконнектинг</strong></span><span class="sxs-lookup"><span data-stu-id="57054-347"><strong>adErrStillConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-348">3713</span><span class="sxs-lookup"><span data-stu-id="57054-348">3713</span></span><br />
<span data-ttu-id="57054-349">— 2146824575</span><span class="sxs-lookup"><span data-stu-id="57054-349">-2146824575</span></span><br />
<span data-ttu-id="57054-350">0x800A0E81</span><span class="sxs-lookup"><span data-stu-id="57054-350">0x800A0E81</span></span></p></td>
<td><p><span data-ttu-id="57054-351">Не удается выполнить операцию при подключении айнчронаусли.</span><span class="sxs-lookup"><span data-stu-id="57054-351">Operation cannot be performed while connecting aynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-352"><strong>адеррстиллексекутинг</strong></span><span class="sxs-lookup"><span data-stu-id="57054-352"><strong>adErrStillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-353">3711</span><span class="sxs-lookup"><span data-stu-id="57054-353">3711</span></span><br />
<span data-ttu-id="57054-354">— 2146824577</span><span class="sxs-lookup"><span data-stu-id="57054-354">-2146824577</span></span><br />
<span data-ttu-id="57054-355">0x800A0E7F</span><span class="sxs-lookup"><span data-stu-id="57054-355">0x800A0E7F</span></span></p></td>
<td><p><span data-ttu-id="57054-356">Не удается выполнить операцию во время асинхронного выполнения.</span><span class="sxs-lookup"><span data-stu-id="57054-356">Operation cannot be performed while executing asynchronously.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-357"><strong>адерртрипермиссиондениед</strong></span><span class="sxs-lookup"><span data-stu-id="57054-357"><strong>adErrTreePermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-358">3728</span><span class="sxs-lookup"><span data-stu-id="57054-358">3728</span></span><br />
<span data-ttu-id="57054-359">— 2146824560</span><span class="sxs-lookup"><span data-stu-id="57054-359">-2146824560</span></span><br />
<span data-ttu-id="57054-360">0x800A0E90</span><span class="sxs-lookup"><span data-stu-id="57054-360">0x800A0E90</span></span></p></td>
<td><p><span data-ttu-id="57054-361">Недостаточно разрешений для доступа к дереву или поддереву.</span><span class="sxs-lookup"><span data-stu-id="57054-361">Permissions are insufficient to access tree or subtree.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-362"><strong>адеррунаваилабле</strong></span><span class="sxs-lookup"><span data-stu-id="57054-362"><strong>adErrUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-363">3736</span><span class="sxs-lookup"><span data-stu-id="57054-363">3736</span></span><br />
<span data-ttu-id="57054-364">— 2146824552</span><span class="sxs-lookup"><span data-stu-id="57054-364">-2146824552</span></span><br />
<span data-ttu-id="57054-365">0x800A0E98</span><span class="sxs-lookup"><span data-stu-id="57054-365">0x800A0E98</span></span></p></td>
<td><p><span data-ttu-id="57054-366">Не удалось завершить операцию, состояние — недоступно.</span><span class="sxs-lookup"><span data-stu-id="57054-366">Operation failed to complete and the status is unavailable.</span></span> <span data-ttu-id="57054-367">Поле может быть недоступно или операция не была предпринята.</span><span class="sxs-lookup"><span data-stu-id="57054-367">The field may be unavailable or the operation was not attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-368"><strong>адеррунсафеоператион</strong></span><span class="sxs-lookup"><span data-stu-id="57054-368"><strong>adErrUnsafeOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-369">3716</span><span class="sxs-lookup"><span data-stu-id="57054-369">3716</span></span><br />
<span data-ttu-id="57054-370">— 2146824572</span><span class="sxs-lookup"><span data-stu-id="57054-370">-2146824572</span></span><br />
<span data-ttu-id="57054-371">0x800A0E84</span><span class="sxs-lookup"><span data-stu-id="57054-371">0x800A0E84</span></span></p></td>
<td><p><span data-ttu-id="57054-372">Параметры безопасности этого компьютера запрещают доступ к источнику данных в другом домене.</span><span class="sxs-lookup"><span data-stu-id="57054-372">Safety settings on this computer prohibit accessing a data source on another domain.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-373"><strong>адеррурлдоеснотексист</strong></span><span class="sxs-lookup"><span data-stu-id="57054-373"><strong>adErrURLDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-374">3727</span><span class="sxs-lookup"><span data-stu-id="57054-374">3727</span></span><br />
<span data-ttu-id="57054-375">— 2146824561</span><span class="sxs-lookup"><span data-stu-id="57054-375">-2146824561</span></span><br />
<span data-ttu-id="57054-376">0x800A0E8F</span><span class="sxs-lookup"><span data-stu-id="57054-376">0x800A0E8F</span></span></p></td>
<td><p><span data-ttu-id="57054-377">Либо исходный URL-адрес, либо родительский URL-адрес назначения не существует.</span><span class="sxs-lookup"><span data-stu-id="57054-377">Either the source URL or the parent of the destination URL does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-378"><strong>адеррурлнамедровдоеснотексист</strong></span><span class="sxs-lookup"><span data-stu-id="57054-378"><strong>adErrURLNamedRowDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-379">3737</span><span class="sxs-lookup"><span data-stu-id="57054-379">3737</span></span><br />
<span data-ttu-id="57054-380">— 2146824551</span><span class="sxs-lookup"><span data-stu-id="57054-380">-2146824551</span></span><br />
<span data-ttu-id="57054-381">0x800A0E99</span><span class="sxs-lookup"><span data-stu-id="57054-381">0x800A0E99</span></span></p></td>
<td><p><span data-ttu-id="57054-382">Запись, указанная с помощью этого URL-адреса, не существует.</span><span class="sxs-lookup"><span data-stu-id="57054-382">Record named by this URL does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-383"><strong>адеррволуменотфаунд</strong></span><span class="sxs-lookup"><span data-stu-id="57054-383"><strong>adErrVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-384">3733</span><span class="sxs-lookup"><span data-stu-id="57054-384">3733</span></span><br />
<span data-ttu-id="57054-385">— 2146824555</span><span class="sxs-lookup"><span data-stu-id="57054-385">-2146824555</span></span><br />
<span data-ttu-id="57054-386">0x800A0E95</span><span class="sxs-lookup"><span data-stu-id="57054-386">0x800A0E95</span></span></p></td>
<td><p><span data-ttu-id="57054-387">Поставщик не может определить устройство хранения данных, указанное с помощью URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="57054-387">Provider cannot locate the storage device indicated by the URL.</span></span> <span data-ttu-id="57054-388">Убедитесь, что URL-адрес введен правильно.</span><span class="sxs-lookup"><span data-stu-id="57054-388">Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-389"><strong>адеррвритефиле</strong></span><span class="sxs-lookup"><span data-stu-id="57054-389"><strong>adErrWriteFile</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-390">3004</span><span class="sxs-lookup"><span data-stu-id="57054-390">3004</span></span><br />
<span data-ttu-id="57054-391">— 2146825284</span><span class="sxs-lookup"><span data-stu-id="57054-391">-2146825284</span></span><br />
<span data-ttu-id="57054-392">0x800A0BBC</span><span class="sxs-lookup"><span data-stu-id="57054-392">0x800A0BBC</span></span></p></td>
<td><p><span data-ttu-id="57054-393">Ошибка записи в файл.</span><span class="sxs-lookup"><span data-stu-id="57054-393">Write to file failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-394"><strong>адврнсекуритидиалог</strong></span><span class="sxs-lookup"><span data-stu-id="57054-394"><strong>adWrnSecurityDialog</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-395">3717</span><span class="sxs-lookup"><span data-stu-id="57054-395">3717</span></span><br />
<span data-ttu-id="57054-396">— 2146824571</span><span class="sxs-lookup"><span data-stu-id="57054-396">-2146824571</span></span><br />
<span data-ttu-id="57054-397">0x800A0E85</span><span class="sxs-lookup"><span data-stu-id="57054-397">0x800A0E85</span></span></p></td>
<td><p><span data-ttu-id="57054-398">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="57054-398">For internal use only.</span></span> <span data-ttu-id="57054-399">Не следует использовать.</span><span class="sxs-lookup"><span data-stu-id="57054-399">Don't use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-400"><strong>адврнсекуритидиалогхеадер</strong></span><span class="sxs-lookup"><span data-stu-id="57054-400"><strong>adWrnSecurityDialogHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="57054-401">3718</span><span class="sxs-lookup"><span data-stu-id="57054-401">3718</span></span><br />
<span data-ttu-id="57054-402">— 2146824570</span><span class="sxs-lookup"><span data-stu-id="57054-402">-2146824570</span></span><br />
<span data-ttu-id="57054-403">0x800A0E86</span><span class="sxs-lookup"><span data-stu-id="57054-403">0x800A0E86</span></span></p></td>
<td><p><span data-ttu-id="57054-404">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="57054-404">For internal use only.</span></span> <span data-ttu-id="57054-405">Не следует использовать.</span><span class="sxs-lookup"><span data-stu-id="57054-405">Don't use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="57054-406">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="57054-406">ADO/WFC equivalent</span></span>

<span data-ttu-id="57054-407">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="57054-407">Package: **com.ms.wfc.data**</span></span>

<span data-ttu-id="57054-408">Определены только следующие подмножества эквивалентов ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="57054-408">Only the following subsets of ADO/WFC equivalents are defined.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="57054-409">Константа</span><span class="sxs-lookup"><span data-stu-id="57054-409">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57054-410">Адоенумс. Еррорвалуе. БАУНДТОКОММАНД</span><span class="sxs-lookup"><span data-stu-id="57054-410">AdoEnums.ErrorValue.BOUNDTOCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-411">Адоенумс. Еррорвалуе. CONVERSION</span><span class="sxs-lookup"><span data-stu-id="57054-411">AdoEnums.ErrorValue.DATACONVERSION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-412">Адоенумс. Еррорвалуе. ФЕАТУРЕНОТАВАИЛАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="57054-412">AdoEnums.ErrorValue.FEATURENOTAVAILABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-413">Адоенумс. Еррорвалуе. ИЛЛЕГАЛОПЕРАТИОН</span><span class="sxs-lookup"><span data-stu-id="57054-413">AdoEnums.ErrorValue.ILLEGALOPERATION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-414">Адоенумс. Еррорвалуе. TRANSACTION</span><span class="sxs-lookup"><span data-stu-id="57054-414">AdoEnums.ErrorValue.INTRANSACTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-415">Адоенумс. Еррорвалуе. INVALIDARGUMENT</span><span class="sxs-lookup"><span data-stu-id="57054-415">AdoEnums.ErrorValue.INVALIDARGUMENT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-416">Адоенумс. Еррорвалуе. ИНВАЛИДКОННЕКТИОН</span><span class="sxs-lookup"><span data-stu-id="57054-416">AdoEnums.ErrorValue.INVALIDCONNECTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-417">Адоенумс. Еррорвалуе. ИНВАЛИДПАРАМИНФО</span><span class="sxs-lookup"><span data-stu-id="57054-417">AdoEnums.ErrorValue.INVALIDPARAMINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-418">Адоенумс. Еррорвалуе. ITEMNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="57054-418">AdoEnums.ErrorValue.ITEMNOTFOUND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-419">Адоенумс. Еррорвалуе. НОКУРРЕНТРЕКОРД</span><span class="sxs-lookup"><span data-stu-id="57054-419">AdoEnums.ErrorValue.NOCURRENTRECORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-420">Адоенумс. Еррорвалуе. НОТЕКСЕКУТИНГ</span><span class="sxs-lookup"><span data-stu-id="57054-420">AdoEnums.ErrorValue.NOTEXECUTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-421">Адоенумс. Еррорвалуе. НОТРИНТРАНТ</span><span class="sxs-lookup"><span data-stu-id="57054-421">AdoEnums.ErrorValue.NOTREENTRANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-422">Адоенумс. Еррорвалуе. ОБЖЕКТКЛОСЕД</span><span class="sxs-lookup"><span data-stu-id="57054-422">AdoEnums.ErrorValue.OBJECTCLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-423">Адоенумс. Еррорвалуе. ОБЖЕКТИНКОЛЛЕКТИОН</span><span class="sxs-lookup"><span data-stu-id="57054-423">AdoEnums.ErrorValue.OBJECTINCOLLECTION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-424">Адоенумс. Еррорвалуе. ОБЖЕКТНОТСЕТ</span><span class="sxs-lookup"><span data-stu-id="57054-424">AdoEnums.ErrorValue.OBJECTNOTSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-425">Адоенумс. Еррорвалуе. ОБЖЕКТОПЕН</span><span class="sxs-lookup"><span data-stu-id="57054-425">AdoEnums.ErrorValue.OBJECTOPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-426">Адоенумс. Еррорвалуе. ОПЕРАТИОНКАНЦЕЛЛЕД</span><span class="sxs-lookup"><span data-stu-id="57054-426">AdoEnums.ErrorValue.OPERATIONCANCELLED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-427">Адоенумс. Еррорвалуе. ПРОВИДЕРНОТФАУНД</span><span class="sxs-lookup"><span data-stu-id="57054-427">AdoEnums.ErrorValue.PROVIDERNOTFOUND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-428">Адоенумс. Еррорвалуе. СТИЛЛКОННЕКТИНГ</span><span class="sxs-lookup"><span data-stu-id="57054-428">AdoEnums.ErrorValue.STILLCONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57054-429">Адоенумс. Еррорвалуе. СТИЛЛЕКСЕКУТИНГ</span><span class="sxs-lookup"><span data-stu-id="57054-429">AdoEnums.ErrorValue.STILLEXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57054-430">Адоенумс. Еррорвалуе. УНСАФЕОПЕРАТИОН</span><span class="sxs-lookup"><span data-stu-id="57054-430">AdoEnums.ErrorValue.UNSAFEOPERATION</span></span></p></td>
</tr>
</tbody>
</table>

