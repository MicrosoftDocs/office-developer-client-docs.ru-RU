---
title: DataTypeEnum (Справочник по базам данных Access на компьютере)
TOCTitle: DataTypeEnum
ms:assetid: a8ab7616-552f-ed5f-ed55-95254cfb374a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249780(v=office.15)
ms:contentKeyID: 48546904
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ffba234ed1c5dc56138a665d6dd07038f55da7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294444"
---
# <a name="datatypeenum"></a><span data-ttu-id="bbdae-102">DataTypeEnum</span><span class="sxs-lookup"><span data-stu-id="bbdae-102">DataTypeEnum</span></span>

<span data-ttu-id="bbdae-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bbdae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bbdae-104">Указывает тип данных [поля](field-object-ado.md), [параметра](parameter-object-ado.md)или [Свойства](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="bbdae-104">Specifies the data type of a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md).</span></span> <span data-ttu-id="bbdae-105">Соответствующий индикатор типа OLE DB отображается в круглых скобках в столбце Описание следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="bbdae-105">The corresponding OLE DB type indicator is shown in parentheses in the description column of the following table.</span></span> <span data-ttu-id="bbdae-106">Дополнительные сведения о типах данных OLE DB приведены в главе 13 и приложении A *Справочника программиста OLE DB*.</span><span class="sxs-lookup"><span data-stu-id="bbdae-106">For more information about OLE DB data types, see Chapter 13 and Appendix A of the *OLE DB Programmer's Reference*.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bbdae-107">Константа</span><span class="sxs-lookup"><span data-stu-id="bbdae-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="bbdae-108">Значение</span><span class="sxs-lookup"><span data-stu-id="bbdae-108">Value</span></span></p></th>
<th><p><span data-ttu-id="bbdae-109">Описание</span><span class="sxs-lookup"><span data-stu-id="bbdae-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-110"><strong>Адаррай</span><span class="sxs-lookup"><span data-stu-id="bbdae-110"><strong>AdArray</span></span><br /><span data-ttu-id="bbdae-111">
</strong>(Не применяется к ADOX.)</span><span class="sxs-lookup"><span data-stu-id="bbdae-111">
</strong>(Does not apply to ADOX.)</span></span></p></td>
<td><p><span data-ttu-id="bbdae-112">0x2000</span><span class="sxs-lookup"><span data-stu-id="bbdae-112">0x2000</span></span></p></td>
<td><p><span data-ttu-id="bbdae-113">Значение флага, всегда скомбинированное с другой константой типа данных, которое указывает массив другого типа данных.</span><span class="sxs-lookup"><span data-stu-id="bbdae-113">A flag value, always combined with another data type constant, that indicates an array of that other data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-114"><strong>Адбигинт</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-114"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-115">двадцать</span><span class="sxs-lookup"><span data-stu-id="bbdae-115">20</span></span></p></td>
<td><p><span data-ttu-id="bbdae-116">Указывает 8-разрядное целое число со знаком (DBTYPE_I8).</span><span class="sxs-lookup"><span data-stu-id="bbdae-116">Indicates an eight-byte signed integer (DBTYPE_I8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-117"><strong>Адбинари</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-117"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-118">128</span><span class="sxs-lookup"><span data-stu-id="bbdae-118">128</span></span></p></td>
<td><p><span data-ttu-id="bbdae-119">Указывает двоичное значение (ДБТИПЕ_БИТЕС).</span><span class="sxs-lookup"><span data-stu-id="bbdae-119">Indicates a binary value (DBTYPE_BYTES).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-120"><strong>Адбулеан</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-120"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-121">-11:00</span><span class="sxs-lookup"><span data-stu-id="bbdae-121">11</span></span></p></td>
<td><p><span data-ttu-id="bbdae-122">Указывает логическое значение (ДБТИПЕ_БУЛ).</span><span class="sxs-lookup"><span data-stu-id="bbdae-122">Indicates a boolean value (DBTYPE_BOOL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-123"><strong>Адбстр</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-123"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-124">8,5</span><span class="sxs-lookup"><span data-stu-id="bbdae-124">8</span></span></p></td>
<td><p><span data-ttu-id="bbdae-125">Указывает строку символов (Юникод), заканчивающуюся нулем (ДБТИПЕ_БСТР).</span><span class="sxs-lookup"><span data-stu-id="bbdae-125">Indicates a null-terminated character string (Unicode) (DBTYPE_BSTR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-126"><strong>Адчаптер</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-126"><strong>adChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-127">136</span><span class="sxs-lookup"><span data-stu-id="bbdae-127">136</span></span></p></td>
<td><p><span data-ttu-id="bbdae-128">Указывает значение главы из четырех байт, которое определяет строки в дочернем наборе строк (ДБТИПЕ_ХЧАПТЕР).</span><span class="sxs-lookup"><span data-stu-id="bbdae-128">Indicates a four-byte chapter value that identifies rows in a child rowset (DBTYPE_HCHAPTER).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-129"><strong>Адчар</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-129"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-130">129</span><span class="sxs-lookup"><span data-stu-id="bbdae-130">129</span></span></p></td>
<td><p><span data-ttu-id="bbdae-131">Указывает строковое значение (ДБТИПЕ_СТР).</span><span class="sxs-lookup"><span data-stu-id="bbdae-131">Indicates a string value (DBTYPE_STR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-132"><strong>Адкурренци</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-132"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-133">ICMPv6</span><span class="sxs-lookup"><span data-stu-id="bbdae-133">6</span></span></p></td>
<td><p><span data-ttu-id="bbdae-134">Показывает значение валюты (ДБТИПЕ_ЦИ).</span><span class="sxs-lookup"><span data-stu-id="bbdae-134">Indicates a currency value (DBTYPE_CY).</span></span> <span data-ttu-id="bbdae-135">Currency — это число с фиксированной запятой, сопоставленное с четырьмя цифрами справа от десятичной точки.</span><span class="sxs-lookup"><span data-stu-id="bbdae-135">Currency is a fixed-point number with four digits to the right of the decimal point.</span></span> <span data-ttu-id="bbdae-136">Он хранится в виде целого числа со знаком длиной 8 байт, масштабированное на 10 000.</span><span class="sxs-lookup"><span data-stu-id="bbdae-136">It is stored in an eight-byte signed integer scaled by 10,000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-137"><strong>Аддате</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-137"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-138">см</span><span class="sxs-lookup"><span data-stu-id="bbdae-138">7</span></span></p></td>
<td><p><span data-ttu-id="bbdae-139">Указывает значение даты (ДБТИПЕ_ДАТЕ).</span><span class="sxs-lookup"><span data-stu-id="bbdae-139">Indicates a date value (DBTYPE_DATE).</span></span> <span data-ttu-id="bbdae-140">Дата хранится в виде Double, целой части, которая представляет собой количество дней с 30 декабря 1899 г., и дробная часть, представляющая долю дня.</span><span class="sxs-lookup"><span data-stu-id="bbdae-140">A date is stored as a double, the whole part of which is the number of days since December 30, 1899, and the fractional part of which is the fraction of a day.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-141"><strong>Аддбдате</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-141"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-142">133</span><span class="sxs-lookup"><span data-stu-id="bbdae-142">133</span></span></p></td>
<td><p><span data-ttu-id="bbdae-143">Указывает значение даты (ГГГГММДД) (ДБТИПЕ_ДБДАТЕ).</span><span class="sxs-lookup"><span data-stu-id="bbdae-143">Indicates a date value (yyyymmdd) (DBTYPE_DBDATE).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-144"><strong>Аддбтиме</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-144"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-145">134</span><span class="sxs-lookup"><span data-stu-id="bbdae-145">134</span></span></p></td>
<td><p><span data-ttu-id="bbdae-146">Указывает значение времени (ЧЧММСС) (ДБТИПЕ_ДБТИМЕ).</span><span class="sxs-lookup"><span data-stu-id="bbdae-146">Indicates a time value (hhmmss) (DBTYPE_DBTIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-147"><strong>Аддбтиместамп</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-147"><strong>adDBTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-148">135</span><span class="sxs-lookup"><span data-stu-id="bbdae-148">135</span></span></p></td>
<td><p><span data-ttu-id="bbdae-149">Указывает отметку даты и времени (ГГГГММДДЧЧММСС плюс дробь в биллионсс) (ДБТИПЕ_ДБТИМЕСТАМП).</span><span class="sxs-lookup"><span data-stu-id="bbdae-149">Indicates a date/time stamp (yyyymmddhhmmss plus a fraction in billionths) (DBTYPE_DBTIMESTAMP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-150"><strong>АддеЦимал</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-150"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-151">14</span><span class="sxs-lookup"><span data-stu-id="bbdae-151">14</span></span></p></td>
<td><p><span data-ttu-id="bbdae-152">Указывает точное числовое значение с фиксированной точностью и масштабом (ДБТИПЕ_ДЕЦИМАЛ).</span><span class="sxs-lookup"><span data-stu-id="bbdae-152">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_DECIMAL).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-153"><strong>Аддаубле</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-153"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-154">17:00</span><span class="sxs-lookup"><span data-stu-id="bbdae-154">5</span></span></p></td>
<td><p><span data-ttu-id="bbdae-155">Указывает значение удвоенной точности с плавающей запятой (DBTYPE_R8).</span><span class="sxs-lookup"><span data-stu-id="bbdae-155">Indicates a double-precision floating-point value (DBTYPE_R8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-156"><strong>Адемпти</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-156"><strong>adEmpty</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-157">нуль</span><span class="sxs-lookup"><span data-stu-id="bbdae-157">0</span></span></p></td>
<td><p><span data-ttu-id="bbdae-158">Задает значение No (ДБТИПЕ_ЕМПТИ).</span><span class="sxs-lookup"><span data-stu-id="bbdae-158">Specifies no value (DBTYPE_EMPTY).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-159"><strong>Адеррор</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-159"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-160">десяти</span><span class="sxs-lookup"><span data-stu-id="bbdae-160">10</span></span></p></td>
<td><p><span data-ttu-id="bbdae-161">Указывает 32-разрядный код ошибки (ДБТИПЕ_ЕРРОР).</span><span class="sxs-lookup"><span data-stu-id="bbdae-161">Indicates a 32-bit error code (DBTYPE_ERROR).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-162"><strong>Адфилетиме</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-162"><strong>adFileTime</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-163">64</span><span class="sxs-lookup"><span data-stu-id="bbdae-163">64</span></span></p></td>
<td><p><span data-ttu-id="bbdae-164">Указывает 64-разрядное значение, представляющее количество интервалов 100-наносекундных, начиная с 1 января 1601 (ДБТИПЕ_ФИЛЕТИМЕ).</span><span class="sxs-lookup"><span data-stu-id="bbdae-164">Indicates a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (DBTYPE_FILETIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-165"><strong>Адгуид</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-165"><strong>adGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-166">72</span><span class="sxs-lookup"><span data-stu-id="bbdae-166">72</span></span></p></td>
<td><p><span data-ttu-id="bbdae-167">Указывает глобальный уникальный идентификатор (GUID) (ДБТИПЕ_ГУИД).</span><span class="sxs-lookup"><span data-stu-id="bbdae-167">Indicates a globally unique identifier (GUID) (DBTYPE_GUID).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-168"><strong>Адидиспатч</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-168"><strong>adIDispatch</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-169">10</span><span class="sxs-lookup"><span data-stu-id="bbdae-169">9</span></span></p></td>
<td><p><span data-ttu-id="bbdae-170">Показывает указатель на интерфейс <strong>IDispatch</strong> объекта COM (дбтипе_идиспатч).</span><span class="sxs-lookup"><span data-stu-id="bbdae-170">Indicates a pointer to an <strong>IDispatch</strong> interface on a COM object (DBTYPE_IDISPATCH).</span></span></p><p><span data-ttu-id="bbdae-171"><strong>Примечание</strong>: этот тип данных в настоящее время не поддерживается ADO.</span><span class="sxs-lookup"><span data-stu-id="bbdae-171"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="bbdae-172">Использование может привести к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="bbdae-172">Usage may cause unpredictable results.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-173"><strong>Адинтежер</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-173"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-174">4</span><span class="sxs-lookup"><span data-stu-id="bbdae-174">3</span></span></p></td>
<td><p><span data-ttu-id="bbdae-175">Указывает 4-разрядное целое число со знаком (DBTYPE_I4).</span><span class="sxs-lookup"><span data-stu-id="bbdae-175">Indicates a four-byte signed integer (DBTYPE_I4).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-176"><strong>Адиункновн</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-176"><strong>adIUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-177">13</span><span class="sxs-lookup"><span data-stu-id="bbdae-177">13</span></span></p></td>
<td><p><span data-ttu-id="bbdae-178">Показывает указатель на интерфейс <strong>IUnknown</strong> для объекта COM (дбтипе_иункновн).</span><span class="sxs-lookup"><span data-stu-id="bbdae-178">Indicates a pointer to an <strong>IUnknown</strong> interface on a COM object (DBTYPE_IUNKNOWN).</span></span></p><p><span data-ttu-id="bbdae-179"><strong>Примечание</strong>: этот тип данных в настоящее время не поддерживается ADO.</span><span class="sxs-lookup"><span data-stu-id="bbdae-179"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="bbdae-180">Использование может привести к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="bbdae-180">Usage may cause unpredictable results.</span></span>
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-181"><strong>Адлонгварбинари</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-181"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-182">205</span><span class="sxs-lookup"><span data-stu-id="bbdae-182">205</span></span></p></td>
<td><p><span data-ttu-id="bbdae-183">Указывает длинное двоичное значение.</span><span class="sxs-lookup"><span data-stu-id="bbdae-183">Indicates a long binary value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-184"><strong>Адлонгварчар</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-184"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-185">201</span><span class="sxs-lookup"><span data-stu-id="bbdae-185">201</span></span></p></td>
<td><p><span data-ttu-id="bbdae-186">Указывает длинное строковое значение.</span><span class="sxs-lookup"><span data-stu-id="bbdae-186">Indicates a long string value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-187"><strong>Адлонгварвчар</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-187"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-188">203</span><span class="sxs-lookup"><span data-stu-id="bbdae-188">203</span></span></p></td>
<td><p><span data-ttu-id="bbdae-189">Указывает длинное строковое значение Юникода с завершающим нулем.</span><span class="sxs-lookup"><span data-stu-id="bbdae-189">Indicates a long null-terminated Unicode string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-190"><strong>Аднумерик</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-190"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-191">131</span><span class="sxs-lookup"><span data-stu-id="bbdae-191">131</span></span></p></td>
<td><p><span data-ttu-id="bbdae-192">Указывает точное числовое значение с фиксированной точностью и масштабом (ДБТИПЕ_НУМЕРИК).</span><span class="sxs-lookup"><span data-stu-id="bbdae-192">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_NUMERIC).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-193"><strong>Адпропвариант</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-193"><strong>adPropVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-194">138</span><span class="sxs-lookup"><span data-stu-id="bbdae-194">138</span></span></p></td>
<td><p><span data-ttu-id="bbdae-195">Указывает ПРОПВАРИАНТ автоматизации (ДБТИПЕ_ПРОП_ВАРИАНТ).</span><span class="sxs-lookup"><span data-stu-id="bbdae-195">Indicates an Automation PROPVARIANT (DBTYPE_PROP_VARIANT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-196"><strong>Адсингле</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-196"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-197">SP4</span><span class="sxs-lookup"><span data-stu-id="bbdae-197">4</span></span></p></td>
<td><p><span data-ttu-id="bbdae-198">Показывает значение одиночной точности с плавающей запятой (DBTYPE_R4).</span><span class="sxs-lookup"><span data-stu-id="bbdae-198">Indicates a single-precision floating-point value (DBTYPE_R4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-199"><strong>Адсмаллинт</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-199"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-200">2</span><span class="sxs-lookup"><span data-stu-id="bbdae-200">2</span></span></p></td>
<td><p><span data-ttu-id="bbdae-201">Указывает 2-байтовое целое число со знаком (DBTYPE_I2).</span><span class="sxs-lookup"><span data-stu-id="bbdae-201">Indicates a two-byte signed integer (DBTYPE_I2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-202"><strong>Адтининт</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-202"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-203">столбцов</span><span class="sxs-lookup"><span data-stu-id="bbdae-203">16</span></span></p></td>
<td><p><span data-ttu-id="bbdae-204">Указывает Однобайтовое целое со знаком (DBTYPE_I1).</span><span class="sxs-lookup"><span data-stu-id="bbdae-204">Indicates a one-byte signed integer (DBTYPE_I1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-205"><strong>Адунсигнедбигинт</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-205"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-206">21</span><span class="sxs-lookup"><span data-stu-id="bbdae-206">21</span></span></p></td>
<td><p><span data-ttu-id="bbdae-207">Указывает 8-байтовое целое число без знака (DBTYPE_UI8).</span><span class="sxs-lookup"><span data-stu-id="bbdae-207">Indicates an eight-byte unsigned integer (DBTYPE_UI8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-208"><strong>Адунсигнединт</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-208"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-209">19</span><span class="sxs-lookup"><span data-stu-id="bbdae-209">19</span></span></p></td>
<td><p><span data-ttu-id="bbdae-210">Указывает на значение из четырех байтов без знака (DBTYPE_UI4).</span><span class="sxs-lookup"><span data-stu-id="bbdae-210">Indicates a four-byte unsigned integer (DBTYPE_UI4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-211"><strong>Адунсигнедсмаллинт</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-211"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-212">0,18</span><span class="sxs-lookup"><span data-stu-id="bbdae-212">18</span></span></p></td>
<td><p><span data-ttu-id="bbdae-213">Указывает на 2-байтовое целое число без знака (DBTYPE_UI2).</span><span class="sxs-lookup"><span data-stu-id="bbdae-213">Indicates a two-byte unsigned integer (DBTYPE_UI2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-214"><strong>Адунсигнедтининт</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-214"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-215">17</span><span class="sxs-lookup"><span data-stu-id="bbdae-215">17</span></span></p></td>
<td><p><span data-ttu-id="bbdae-216">Указывает Однобайтовое целое число без знака (DBTYPE_UI1).</span><span class="sxs-lookup"><span data-stu-id="bbdae-216">Indicates a one-byte unsigned integer (DBTYPE_UI1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-217"><strong>Адусердефинед</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-217"><strong>adUserDefined</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-218">132</span><span class="sxs-lookup"><span data-stu-id="bbdae-218">132</span></span></p></td>
<td><p><span data-ttu-id="bbdae-219">Указывает пользовательскую переменную (ДБТИПЕ_УДТ).</span><span class="sxs-lookup"><span data-stu-id="bbdae-219">Indicates a user-defined variable (DBTYPE_UDT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-220"><strong>Адварбинари</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-220"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-221">204</span><span class="sxs-lookup"><span data-stu-id="bbdae-221">204</span></span></p></td>
<td><p><span data-ttu-id="bbdae-222">Указывает двоичное значение (только для объекта<strong>Parameter</strong> ).</span><span class="sxs-lookup"><span data-stu-id="bbdae-222">Indicates a binary value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-223"><strong>Адварчар</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-223"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-224">200</span><span class="sxs-lookup"><span data-stu-id="bbdae-224">200</span></span></p></td>
<td><p><span data-ttu-id="bbdae-225">Указывает строковое значение.</span><span class="sxs-lookup"><span data-stu-id="bbdae-225">Indicates a string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-226"><strong>Адвариант</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-226"><strong>adVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-227">12</span><span class="sxs-lookup"><span data-stu-id="bbdae-227">12</span></span></p></td>
<td><p><span data-ttu-id="bbdae-228">Указывает <strong>вариант</strong> автоматизации (дбтипе_вариант).</span><span class="sxs-lookup"><span data-stu-id="bbdae-228">Indicates an Automation <strong>Variant</strong> (DBTYPE_VARIANT).</span></span></p><p><span data-ttu-id="bbdae-229"><strong>Примечание</strong>: этот тип данных в настоящее время не поддерживается ADO.</span><span class="sxs-lookup"><span data-stu-id="bbdae-229"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="bbdae-230">Использование может привести к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="bbdae-230">Usage may cause unpredictable results.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-231"><strong>Адварнумерик</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-231"><strong>adVarNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-232">139</span><span class="sxs-lookup"><span data-stu-id="bbdae-232">139</span></span></p></td>
<td><p><span data-ttu-id="bbdae-233">Указывает числовое значение (только для объекта<strong>Parameter</strong> ).</span><span class="sxs-lookup"><span data-stu-id="bbdae-233">Indicates a numeric value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-234"><strong>Адварвчар</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-234"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-235">202</span><span class="sxs-lookup"><span data-stu-id="bbdae-235">202</span></span></p></td>
<td><p><span data-ttu-id="bbdae-236">Указывает строку символов Юникода, заканчивающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="bbdae-236">Indicates a null-terminated Unicode character string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-237"><strong>Адвчар</strong></span><span class="sxs-lookup"><span data-stu-id="bbdae-237"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="bbdae-238">130</span><span class="sxs-lookup"><span data-stu-id="bbdae-238">130</span></span></p></td>
<td><p><span data-ttu-id="bbdae-239">Указывает строку символов Юникода, заканчивающуюся нулем (ДБТИПЕ_ВСТР).</span><span class="sxs-lookup"><span data-stu-id="bbdae-239">Indicates a null-terminated Unicode character string (DBTYPE_WSTR).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="bbdae-240">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="bbdae-240">ADO/WFC equivalent</span></span>

<span data-ttu-id="bbdae-241">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="bbdae-241">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bbdae-242">Константа</span><span class="sxs-lookup"><span data-stu-id="bbdae-242">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-243">Адоенумс. DataType. ARRAY</span><span class="sxs-lookup"><span data-stu-id="bbdae-243">AdoEnums.DataType.ARRAY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-244">Адоенумс. DataType. BIGINT</span><span class="sxs-lookup"><span data-stu-id="bbdae-244">AdoEnums.DataType.BIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-245">Адоенумс. DataType. BINARY</span><span class="sxs-lookup"><span data-stu-id="bbdae-245">AdoEnums.DataType.BINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-246">Адоенумс. DataType. BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="bbdae-246">AdoEnums.DataType.BOOLEAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-247">Адоенумс. DataType. BSTR</span><span class="sxs-lookup"><span data-stu-id="bbdae-247">AdoEnums.DataType.BSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-248">Адоенумс. DataType. CHAPTER</span><span class="sxs-lookup"><span data-stu-id="bbdae-248">AdoEnums.DataType.CHAPTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-249">Адоенумс. DataType. CHAR</span><span class="sxs-lookup"><span data-stu-id="bbdae-249">AdoEnums.DataType.CHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-250">Адоенумс. DataType. CURRENCY</span><span class="sxs-lookup"><span data-stu-id="bbdae-250">AdoEnums.DataType.CURRENCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-251">Адоенумс. DataType. DATE</span><span class="sxs-lookup"><span data-stu-id="bbdae-251">AdoEnums.DataType.DATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-252">Адоенумс. DataType. ДБДАТЕ</span><span class="sxs-lookup"><span data-stu-id="bbdae-252">AdoEnums.DataType.DBDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-253">Адоенумс. DataType. ДБТИМЕ</span><span class="sxs-lookup"><span data-stu-id="bbdae-253">AdoEnums.DataType.DBTIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-254">Адоенумс. DataType. ДБТИМЕСТАМП</span><span class="sxs-lookup"><span data-stu-id="bbdae-254">AdoEnums.DataType.DBTIMESTAMP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-255">Адоенумс. DataType. DECIMAL</span><span class="sxs-lookup"><span data-stu-id="bbdae-255">AdoEnums.DataType.DECIMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-256">Адоенумс. DataType. DOUBLE</span><span class="sxs-lookup"><span data-stu-id="bbdae-256">AdoEnums.DataType.DOUBLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-257">Адоенумс. DataType. EMPTY</span><span class="sxs-lookup"><span data-stu-id="bbdae-257">AdoEnums.DataType.EMPTY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-258">Адоенумс. DataType. ERROR</span><span class="sxs-lookup"><span data-stu-id="bbdae-258">AdoEnums.DataType.ERROR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-259">Адоенумс. DataType. FILETIME</span><span class="sxs-lookup"><span data-stu-id="bbdae-259">AdoEnums.DataType.FILETIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-260">Адоенумс. DataType. GUID</span><span class="sxs-lookup"><span data-stu-id="bbdae-260">AdoEnums.DataType.GUID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-261">Адоенумс. DataType. IDISPATCH</span><span class="sxs-lookup"><span data-stu-id="bbdae-261">AdoEnums.DataType.IDISPATCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-262">Адоенумс. DataType. INTEGER</span><span class="sxs-lookup"><span data-stu-id="bbdae-262">AdoEnums.DataType.INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-263">Адоенумс. DataType. IUNKNOWN</span><span class="sxs-lookup"><span data-stu-id="bbdae-263">AdoEnums.DataType.IUNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-264">Адоенумс. DataType. ЛОНГВАРБИНАРИ</span><span class="sxs-lookup"><span data-stu-id="bbdae-264">AdoEnums.DataType.LONGVARBINARY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-265">Адоенумс. DataType. ЛОНГВАРЧАР</span><span class="sxs-lookup"><span data-stu-id="bbdae-265">AdoEnums.DataType.LONGVARCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-266">Адоенумс. DataType. ЛОНГВАРВЧАР</span><span class="sxs-lookup"><span data-stu-id="bbdae-266">AdoEnums.DataType.LONGVARWCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-267">Адоенумс. DataType. NUMERIC</span><span class="sxs-lookup"><span data-stu-id="bbdae-267">AdoEnums.DataType.NUMERIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-268">Адоенумс. DataType. ПРОПВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="bbdae-268">AdoEnums.DataType.PROPVARIANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-269">Адоенумс. DataType. SINGLE</span><span class="sxs-lookup"><span data-stu-id="bbdae-269">AdoEnums.DataType.SINGLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-270">Адоенумс. DataType. SMALLINT</span><span class="sxs-lookup"><span data-stu-id="bbdae-270">AdoEnums.DataType.SMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-271">Адоенумс. DataType. TINYINT</span><span class="sxs-lookup"><span data-stu-id="bbdae-271">AdoEnums.DataType.TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-272">Адоенумс. DataType. УНСИГНЕДБИГИНТ</span><span class="sxs-lookup"><span data-stu-id="bbdae-272">AdoEnums.DataType.UNSIGNEDBIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-273">Адоенумс. DataType. УНСИГНЕДИНТ</span><span class="sxs-lookup"><span data-stu-id="bbdae-273">AdoEnums.DataType.UNSIGNEDINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-274">Адоенумс. DataType. УНСИГНЕДСМАЛЛИНТ</span><span class="sxs-lookup"><span data-stu-id="bbdae-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-275">Адоенумс. DataType. УНСИГНЕДТИНИНТ</span><span class="sxs-lookup"><span data-stu-id="bbdae-275">AdoEnums.DataType.UNSIGNEDTINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-276">Адоенумс. DataType. USERDEFINED типа</span><span class="sxs-lookup"><span data-stu-id="bbdae-276">AdoEnums.DataType.USERDEFINED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-277">Адоенумс. DataType. VARBINARY</span><span class="sxs-lookup"><span data-stu-id="bbdae-277">AdoEnums.DataType.VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-278">Адоенумс. DataType. VARCHAR</span><span class="sxs-lookup"><span data-stu-id="bbdae-278">AdoEnums.DataType.VARCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-279">Адоенумс. DataType. VARIANT</span><span class="sxs-lookup"><span data-stu-id="bbdae-279">AdoEnums.DataType.VARIANT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-280">Адоенумс. DataType. ВАРНУМЕРИК</span><span class="sxs-lookup"><span data-stu-id="bbdae-280">AdoEnums.DataType.VARNUMERIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbdae-281">Адоенумс. DataType. ВАРВЧАР</span><span class="sxs-lookup"><span data-stu-id="bbdae-281">AdoEnums.DataType.VARWCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbdae-282">Адоенумс. DataType. WCHAR</span><span class="sxs-lookup"><span data-stu-id="bbdae-282">AdoEnums.DataType.WCHAR</span></span></p></td>
</tr>
</tbody>
</table>

