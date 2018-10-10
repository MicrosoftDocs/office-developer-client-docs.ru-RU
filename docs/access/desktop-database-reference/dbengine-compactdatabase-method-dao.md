---
title: DBEngine.CompactDatabase Method (DAO)
TOCTitle: CompactDatabase Method
ms:assetid: 03f3a156-005a-4b71-81b0-598f326f7d42
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844821(v=office.15)
ms:contentKeyID: 48542997
ms.date: 10/24/2016
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052936
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1be6f910c8ab4aefed483c147ef88e8cecfa3a84
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481018"
---
# <a name="dbenginecompactdatabase-method-dao"></a><span data-ttu-id="95af6-102">DBEngine.CompactDatabase Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="95af6-102">DBEngine.CompactDatabase Method (DAO)</span></span>

<span data-ttu-id="95af6-103">**Применимо к**: Access 2013 | 2016 доступа</span><span class="sxs-lookup"><span data-stu-id="95af6-103">**Applies to**: Access 2013 | Access 2016</span></span>

<span data-ttu-id="95af6-104">Копирует и сжимает закрытой базы данных и позволяет изменить его версию, сортировки порядок и шифрования.</span><span class="sxs-lookup"><span data-stu-id="95af6-104">Copies and compacts a closed database, and gives you the option of changing its version, collating order, and encryption.</span></span> <span data-ttu-id="95af6-105">(Microsoft Access рабочие области только).</span><span class="sxs-lookup"><span data-stu-id="95af6-105">(Microsoft Access workspaces only).</span></span>

> [!NOTE]
> <span data-ttu-id="95af6-106">При использовании зашифрованные связанные таблицы для действия, обновления и запросы SQL [например инструкции SQL UPDATE (CurrentDb.Execute «Обновить...»)], необходимо указать ключ шифрования.</span><span class="sxs-lookup"><span data-stu-id="95af6-106">When using encrypted linked tables for action, update, and SQL queries [such as a SQL UPDATE statement (CurrentDb.Execute "UPDATE...")], you must supply the encryption key.</span></span> <span data-ttu-id="95af6-107">Кроме того связанные таблицы настроено ограничение 19-значный ключ шифрования.</span><span class="sxs-lookup"><span data-stu-id="95af6-107">Also, linked tables have a 19-character limit for the encryption key.</span></span> <span data-ttu-id="95af6-108">В конце этого раздела в разделе **Encrypted связанные таблицы** .</span><span class="sxs-lookup"><span data-stu-id="95af6-108">See the **Encrypted linked tables** section at the end of this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="95af6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95af6-109">Syntax</span></span>

<span data-ttu-id="95af6-110">*выражение* . CompactDatabase (***SrcName***, ***DstName***, ***DstLocale***, ***Параметры***, ***пароль***)</span><span class="sxs-lookup"><span data-stu-id="95af6-110">*expression* .CompactDatabase(***SrcName***, ***DstName***, ***DstLocale***, ***Options***, ***password***)</span></span>

<span data-ttu-id="95af6-111">*выражение* Выражение, возвращающее объект **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="95af6-111">*expression* An expression that returns a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="95af6-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="95af6-112">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95af6-113">Имя</span><span class="sxs-lookup"><span data-stu-id="95af6-113">Name</span></span></p></th>
<th><p><span data-ttu-id="95af6-114">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="95af6-114">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="95af6-115">Тип данных</span><span class="sxs-lookup"><span data-stu-id="95af6-115">Data Type</span></span></p></th>
<th><p><span data-ttu-id="95af6-116">Описание</span><span class="sxs-lookup"><span data-stu-id="95af6-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95af6-117">SrcName</span><span class="sxs-lookup"><span data-stu-id="95af6-117">SrcName</span></span></p></td>
<td><p><span data-ttu-id="95af6-118">Обязательный</span><span class="sxs-lookup"><span data-stu-id="95af6-118">Required</span></span></p></td>
<td><p><span data-ttu-id="95af6-119"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-120">Определяет базу данных существующей, закрытой.</span><span class="sxs-lookup"><span data-stu-id="95af6-120">Identifies an existing, closed database.</span></span> <span data-ttu-id="95af6-121">Это может быть полный путь и имя файла, такие как &quot;C:\db1.mdb&quot;.</span><span class="sxs-lookup"><span data-stu-id="95af6-121">It can be a full path and file name, such as &quot;C:\db1.mdb&quot;.</span></span> <span data-ttu-id="95af6-122">Если расширение имени файла, необходимо указать его.</span><span class="sxs-lookup"><span data-stu-id="95af6-122">If the file name has an extension, you must specify it.</span></span> <span data-ttu-id="95af6-123">Если сеть поддерживает его, можно также указать сетевой путь, таких как &quot; \\server1\share1\dir1\db1.mdb&quot;</span><span class="sxs-lookup"><span data-stu-id="95af6-123">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1.mdb&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95af6-124">DstName</span><span class="sxs-lookup"><span data-stu-id="95af6-124">DstName</span></span></p></td>
<td><p><span data-ttu-id="95af6-125">Обязательный</span><span class="sxs-lookup"><span data-stu-id="95af6-125">Required</span></span></p></td>
<td><p><span data-ttu-id="95af6-126"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-126"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-127">Имя файла (и путь) сжатии базы данных, который вы создаете.</span><span class="sxs-lookup"><span data-stu-id="95af6-127">the file name (and path) of the compacted database that you're creating.</span></span> <span data-ttu-id="95af6-128">Можно также указать сетевой путь.</span><span class="sxs-lookup"><span data-stu-id="95af6-128">You can also specify a network path.</span></span> <span data-ttu-id="95af6-129">Чтобы указать один и тот же файл базы данных в качестве SrcName нельзя использовать этот аргумент.</span><span class="sxs-lookup"><span data-stu-id="95af6-129">You can't use this argument to specify the same database file as SrcName.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95af6-130">DstLocale</span><span class="sxs-lookup"><span data-stu-id="95af6-130">DstLocale</span></span></p></td>
<td><p><span data-ttu-id="95af6-131">Необязательный</span><span class="sxs-lookup"><span data-stu-id="95af6-131">Optional</span></span></p></td>
<td><p><span data-ttu-id="95af6-132"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-132"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-133">Строковое выражение, которое определяет порядок сортировки при создании DstName, как указано в примечания.</span><span class="sxs-lookup"><span data-stu-id="95af6-133">A string expression that specifies a collating order for creating DstName, as specified in Remarks.</span></span></p>
<ul>
<li><p><span data-ttu-id="95af6-134">Если опустить аргумент языковой стандарт DstName совпадает с SrcName.</span><span class="sxs-lookup"><span data-stu-id="95af6-134">If you omit this argument, the locale of DstName is the same as SrcName.</span></span></p></li>
<li><p><span data-ttu-id="95af6-135">Также можно создать пароль для DstName, объединив Строка пароля (начиная с &quot;; pwd =&quot;) с константой в аргументе DstLocale следующим образом: dbLangSpanish &amp; &quot;; pwd = Новый_пароль&quot;.</span><span class="sxs-lookup"><span data-stu-id="95af6-135">You can also create a password for DstName by concatenating the password string (starting with &quot;;pwd=&quot;) with a constant in the DstLocale argument, like this: dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;.</span></span></p></li>
<li><p><span data-ttu-id="95af6-136">Если вы хотите использовать же DstLocale в качестве SrcName (значение по умолчанию), но указать новый пароль, просто введите строку пароль для DstLocale: &quot;; pwd = Новый_пароль&quot;</span><span class="sxs-lookup"><span data-stu-id="95af6-136">If you want to use the same DstLocale as SrcName (the default value), but specify a new password, simply enter a password string for DstLocale: &quot;;pwd=NewPassword&quot;</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95af6-137">Options</span><span class="sxs-lookup"><span data-stu-id="95af6-137">Options</span></span></p></td>
<td><p><span data-ttu-id="95af6-138">Необязательный</span><span class="sxs-lookup"><span data-stu-id="95af6-138">Optional</span></span></p></td>
<td><p><span data-ttu-id="95af6-139"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-139"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-140">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="95af6-140">Optional.</span></span> <span data-ttu-id="95af6-141">Константа или сочетание констант, которое указывает один или несколько параметров, как указано в примечания.</span><span class="sxs-lookup"><span data-stu-id="95af6-141">A constant or combination of constants that indicates one or more options, as specified in Remarks.</span></span> <span data-ttu-id="95af6-142">Параметры можно использовать суммируются соответствующий констант.</span><span class="sxs-lookup"><span data-stu-id="95af6-142">You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95af6-143">password</span><span class="sxs-lookup"><span data-stu-id="95af6-143">password</span></span></p></td>
<td><p><span data-ttu-id="95af6-144">Необязательный</span><span class="sxs-lookup"><span data-stu-id="95af6-144">Optional</span></span></p></td>
<td><p><span data-ttu-id="95af6-145"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-145"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-146">Строковое выражение, содержащий ключ шифрования, если база данных зашифрована.</span><span class="sxs-lookup"><span data-stu-id="95af6-146">A string expression containing an encryption key, if the database is encrypted.</span></span> <span data-ttu-id="95af6-147">Строка &quot;; pwd =&quot; должны предшествовать текущий пароль.</span><span class="sxs-lookup"><span data-stu-id="95af6-147">The string &quot;;pwd=&quot; must precede the actual password.</span></span> <span data-ttu-id="95af6-148">Этот параметр игнорируется, если включить параметр password в DstLocale.</span><span class="sxs-lookup"><span data-stu-id="95af6-148">If you include a password setting in DstLocale, this setting is ignored.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="95af6-149">Это не рекомендуемые для использования параметра, не поддерживается. Формат ACCDB.</span><span class="sxs-lookup"><span data-stu-id="95af6-149">This is deprecated parameter and is not supported in .ACCDB format.</span></span> <span data-ttu-id="95af6-150">Для шифрования. ACCDB-файлу, используйте «pwd =» параметр string.</span><span class="sxs-lookup"><span data-stu-id="95af6-150">To encrypt an .ACCDB file, use the "pwd=" option string.</span></span> <span data-ttu-id="95af6-151">Используйте надежные пароли, содержащие верхний и строчные буквы, числа и символы.</span><span class="sxs-lookup"><span data-stu-id="95af6-151">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="95af6-152">Ненадежные пароли не смешивайте этих элементов.</span><span class="sxs-lookup"><span data-stu-id="95af6-152">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="95af6-153">Надежный пароль: Y6dh! et5.</span><span class="sxs-lookup"><span data-stu-id="95af6-153">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="95af6-154">Ненадежный пароль: House27.</span><span class="sxs-lookup"><span data-stu-id="95af6-154">Weak password: House27.</span></span> <span data-ttu-id="95af6-155">Используйте надежный пароль, который вы можете запомнить, чтобы записать его не нужно.</span><span class="sxs-lookup"><span data-stu-id="95af6-155">Use a strong password that you can remember so that you don't have to write it down.</span></span></P>


</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="95af6-156">Замечания</span><span class="sxs-lookup"><span data-stu-id="95af6-156">Remarks</span></span>

<span data-ttu-id="95af6-157">Допустимы следующие константы для аргумента DstLocale можно использовать для указания свойство **CollatingOrder** для сравнения строк текста.</span><span class="sxs-lookup"><span data-stu-id="95af6-157">You can use one of the following constants for the DstLocale argument to specify the **CollatingOrder** property for string comparisons of text.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95af6-158">Constant</span><span class="sxs-lookup"><span data-stu-id="95af6-158">Constant</span></span></p></th>
<th><p><span data-ttu-id="95af6-159">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="95af6-159">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95af6-160"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-160"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-161">Английский, немецкий, французский, португальский, итальянский и современных испанский</span><span class="sxs-lookup"><span data-stu-id="95af6-161">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95af6-162"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-162"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-163">арабский;</span><span class="sxs-lookup"><span data-stu-id="95af6-163">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95af6-164"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-164"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-165">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="95af6-165">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95af6-166"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-166"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-167">Китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="95af6-167">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95af6-168"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-168"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-169">русский;</span><span class="sxs-lookup"><span data-stu-id="95af6-169">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95af6-170"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-170"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-171">чешский;</span><span class="sxs-lookup"><span data-stu-id="95af6-171">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95af6-172"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-172"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-173">голландский;</span><span class="sxs-lookup"><span data-stu-id="95af6-173">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95af6-174"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-174"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-175">греческий;</span><span class="sxs-lookup"><span data-stu-id="95af6-175">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95af6-176"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-176"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-177">иврит;</span><span class="sxs-lookup"><span data-stu-id="95af6-177">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95af6-178"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-178"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-179">венгерский;</span><span class="sxs-lookup"><span data-stu-id="95af6-179">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95af6-180"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-180"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-181">Исландский</span><span class="sxs-lookup"><span data-stu-id="95af6-181">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95af6-182"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-182"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-183">японский;</span><span class="sxs-lookup"><span data-stu-id="95af6-183">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95af6-184"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-184"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-185">корейский;</span><span class="sxs-lookup"><span data-stu-id="95af6-185">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95af6-186"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-186"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-187">Скандинавские языки (ядра Microsoft Jet базы данных версии 1.0 только)</span><span class="sxs-lookup"><span data-stu-id="95af6-187">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95af6-188"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-188"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-189">Датский и норвежский</span><span class="sxs-lookup"><span data-stu-id="95af6-189">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95af6-190"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-190"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-191">польский;</span><span class="sxs-lookup"><span data-stu-id="95af6-191">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95af6-192"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-192"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-193">словенский;</span><span class="sxs-lookup"><span data-stu-id="95af6-193">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95af6-194"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-194"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-195">Испанский (традиционный)</span><span class="sxs-lookup"><span data-stu-id="95af6-195">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95af6-196"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-196"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-197">Финский и шведский</span><span class="sxs-lookup"><span data-stu-id="95af6-197">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95af6-198"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-198"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-199">тайский;</span><span class="sxs-lookup"><span data-stu-id="95af6-199">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95af6-200"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-200"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-201">турецкий;</span><span class="sxs-lookup"><span data-stu-id="95af6-201">Turkish</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="95af6-202">Одна из следующих констант можно использовать в аргументе параметры для укажите, нужно ли для шифрования и расшифровки базы данных во время его сжатия.</span><span class="sxs-lookup"><span data-stu-id="95af6-202">You can use one of the following constants in the options argument to specify whether to encrypt or to decrypt the database while it's compacted.</span></span>

> [!NOTE]
> <span data-ttu-id="95af6-203">Константы dbEncrypt и dbDecrypt устаревшие и не поддерживается в. Форматы файлов ACCDB.</span><span class="sxs-lookup"><span data-stu-id="95af6-203">The constants dbEncrypt and dbDecrypt are deprecated and not supported in .ACCDB file formats.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95af6-204">Константа</span><span class="sxs-lookup"><span data-stu-id="95af6-204">Constant</span></span></p></th>
<th><p><span data-ttu-id="95af6-205">Описание</span><span class="sxs-lookup"><span data-stu-id="95af6-205">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95af6-206"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-206"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-207">Зашифруйте базу данных и сжатие.</span><span class="sxs-lookup"><span data-stu-id="95af6-207">Encrypt the database while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95af6-208"><strong>dbDecrypt</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-208"><strong>dbDecrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-209">При сжатии расшифровывать базу данных.</span><span class="sxs-lookup"><span data-stu-id="95af6-209">Decrypt the database while compacting.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="95af6-210">Если опустить константой шифрования или включить **dbDecrypt** и **dbEncrypt**, DstName будут иметь такое же шифрование как SrcName.</span><span class="sxs-lookup"><span data-stu-id="95af6-210">If you omit an encryption constant or if you include both **dbDecrypt** and **dbEncrypt**, DstName will have the same encryption as SrcName.</span></span>

<span data-ttu-id="95af6-211">Одна из следующих констант можно использовать в качестве аргумента параметры указывается версия формат данных для сжатии базы данных.</span><span class="sxs-lookup"><span data-stu-id="95af6-211">You can use one of the following constants in the options argument to specify the version of the data format for the compacted database.</span></span> <span data-ttu-id="95af6-212">Это константа влияет на версию формат данных DstName и не влияет на версии объектов любого Microsoft определенные доступа, например форм и отчетов.</span><span class="sxs-lookup"><span data-stu-id="95af6-212">This constant affects only the version of the data format of DstName and doesn't affect the version of any Microsoft Access-defined objects, such as forms and reports.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95af6-213">Константа</span><span class="sxs-lookup"><span data-stu-id="95af6-213">Constant</span></span></p></th>
<th><p><span data-ttu-id="95af6-214">Описание</span><span class="sxs-lookup"><span data-stu-id="95af6-214">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95af6-215"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-215"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-216">Создает базу данных, которая использует формат файла базы данных ядра Microsoft Jet версии 1.0 при сжатии.</span><span class="sxs-lookup"><span data-stu-id="95af6-216">Creates a database that uses the Microsoft Jet database engine version 1.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95af6-217"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-217"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-218">Создает базу данных, которая использует формат файла базы данных ядра Microsoft Jet версии 1.1 при сжатии.</span><span class="sxs-lookup"><span data-stu-id="95af6-218">Creates a database that uses the Microsoft Jet database engine version 1.1 file format while compacting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95af6-219"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-219"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-220">Создает базу данных, который использует формат файла базы данных ядра Microsoft Jet версии 2.0 при сжатии.</span><span class="sxs-lookup"><span data-stu-id="95af6-220">Creates a database that uses the Microsoft Jet database engine version 2.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95af6-221"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-221"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-222">Создает базу данных, которая использует формат файла версии 3.0 ядра базы данных Microsoft Jet (совместимый с версией 3.5) при сжатии.</span><span class="sxs-lookup"><span data-stu-id="95af6-222">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5) while compacting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95af6-223"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-223"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-224">Создает базу данных, которая использует формат файла базы данных ядра Microsoft Jet версии 4.0 при сжатии.</span><span class="sxs-lookup"><span data-stu-id="95af6-224">Creates a database that uses the Microsoft Jet database engine version 4.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95af6-225"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="95af6-225"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="95af6-226">Создает базу данных, которая использует формат файла базы данных модуля Microsoft Access версии 12.0 при сжатии.</span><span class="sxs-lookup"><span data-stu-id="95af6-226">Creates a database that uses the Microsoft Access database engine version 12.0 file format while compacting.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="95af6-227">Можно указать только одна константа версии.</span><span class="sxs-lookup"><span data-stu-id="95af6-227">You can specify only one version constant.</span></span> <span data-ttu-id="95af6-228">Если опустить константа версии DstName будут иметь те же версии как SrcName.</span><span class="sxs-lookup"><span data-stu-id="95af6-228">If you omit a version constant, DstName will have the same version as SrcName.</span></span> <span data-ttu-id="95af6-229">Можно сжать DstName только к версии, такой же или более поздней версии, чем SrcName.</span><span class="sxs-lookup"><span data-stu-id="95af6-229">You can compact DstName only to a version that is the same or later than that of SrcName.</span></span>

<span data-ttu-id="95af6-230">При изменении данных в базе данных, файл базы данных могут стать фрагментированными и используйте больше дискового пространства не требуется.</span><span class="sxs-lookup"><span data-stu-id="95af6-230">As you change data in a database, the database file can become fragmented and use more disk space than is necessary.</span></span> <span data-ttu-id="95af6-231">Периодически можно использовать метод **CompactDatabase** сжатие базы данных для дефрагментации файла базы данных.</span><span class="sxs-lookup"><span data-stu-id="95af6-231">Periodically, you can use the **CompactDatabase** method to compact your database to defragment the database file.</span></span> <span data-ttu-id="95af6-232">Сжатии базы данных обычно меньше и обычно выполняется быстрее.</span><span class="sxs-lookup"><span data-stu-id="95af6-232">The compacted database is usually smaller and often runs faster.</span></span> <span data-ttu-id="95af6-233">Можно также изменить порядок сортировки, шифрование или версии формат данных во время копировать и сжатия базы данных.</span><span class="sxs-lookup"><span data-stu-id="95af6-233">You can also change the collating order, the encryption, or the version of the data format while you copy and compact the database.</span></span>

<span data-ttu-id="95af6-234">Перед его сжатии необходимо закрыть SrcName.</span><span class="sxs-lookup"><span data-stu-id="95af6-234">You must close SrcName before you compact it.</span></span> <span data-ttu-id="95af6-235">В многопользовательской среде другие пользователи не могут иметь SrcName открыть, когда вы сжатие.</span><span class="sxs-lookup"><span data-stu-id="95af6-235">In a multiuser environment, other users can't have SrcName open while you're compacting it.</span></span> <span data-ttu-id="95af6-236">Если SrcName не закрывается или недоступен в монопольном режиме, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="95af6-236">If SrcName isn't closed or isn't available for exclusive use, an error occurs.</span></span>

<span data-ttu-id="95af6-237">Так как **CompactDatabase** создает копии базы данных, необходимо иметь достаточно места для исходной и повторяющихся баз данных.</span><span class="sxs-lookup"><span data-stu-id="95af6-237">Because **CompactDatabase** creates a copy of the database, you must have enough disk space for both the original and the duplicate databases.</span></span> <span data-ttu-id="95af6-238">Compact операция заканчивается с ошибкой, если нет места на диске.</span><span class="sxs-lookup"><span data-stu-id="95af6-238">The compact operation fails if there isn't enough disk space available.</span></span> <span data-ttu-id="95af6-239">База данных повторяющиеся DstName не должен находиться на том же диске SrcName.</span><span class="sxs-lookup"><span data-stu-id="95af6-239">The DstName duplicate database doesn't have to be on the same disk as SrcName.</span></span> <span data-ttu-id="95af6-240">После успешного сжатия базы данных, можно удалить файл SrcName и переименуйте сжатого файла DstName в исходное имя файла.</span><span class="sxs-lookup"><span data-stu-id="95af6-240">After successfully compacting a database, you can delete the SrcName file and rename the compacted DstName file to the original file name.</span></span>

<span data-ttu-id="95af6-241">Метод **CompactDatabase** копирует все данные и параметры разрешений безопасности из базы данных, указанный для базы данных, указанной с DstName SrcName.</span><span class="sxs-lookup"><span data-stu-id="95af6-241">The **CompactDatabase** method copies all the data and the security permission settings from the database specified by SrcName to the database specified by DstName.</span></span>

> [!NOTE]
> <span data-ttu-id="95af6-242">Так как метод **CompactDatabase** не преобразования объектов Microsoft Access, не следует использовать **CompactDatabase** для преобразования база данных, содержащая такие объекты.</span><span class="sxs-lookup"><span data-stu-id="95af6-242">Because the **CompactDatabase** method doesn't convert Microsoft Access objects, you shouldn't use **CompactDatabase** to convert a database containing such objects.</span></span>

## <a name="encrypted-linked-tables"></a><span data-ttu-id="95af6-243">Зашифрованные связанные таблицы</span><span class="sxs-lookup"><span data-stu-id="95af6-243">Encrypted linked tables</span></span>

<span data-ttu-id="95af6-244">Зашифрованные пароли, зависят от формата файла базы данных, которое используется.</span><span class="sxs-lookup"><span data-stu-id="95af6-244">Encrypted passwords are dependent on the file format of the database that you are using.</span></span> <span data-ttu-id="95af6-245">При использовании Access 2003 (.mdb) или более ранних базы данных будут иметь один пароль для защиты базы данных и отдельные пароль для базы данных.</span><span class="sxs-lookup"><span data-stu-id="95af6-245">If you are using an Access 2003 (.mdb) or earlier database, you will have one password to protect the database, and a separate password to encrypt the database.</span></span> <span data-ttu-id="95af6-246">Для Access 2007 (.accdb) и более поздней версии (.mdb) единственно возможный вариант — для шифрования и защиты базы данных с использованием одного пароля как параметр, чтобы два отдельных пароля был удален.</span><span class="sxs-lookup"><span data-stu-id="95af6-246">For Access 2007 (.accdb) and later (.mdb) databases, the only option is to encrypt and protect the database with one password, as the option to have two separate passwords has been removed.</span></span>

> [!NOTE]
> <span data-ttu-id="95af6-247">Для баз данных Access 2007 (.accdb) пароль — это ключ шифрования</span><span class="sxs-lookup"><span data-stu-id="95af6-247">For Access 2007 (.accdb) databases, the password is the encryption key</span></span>

<span data-ttu-id="95af6-248">Можно использовать следующий пример кода VBA для кнопки команды:</span><span class="sxs-lookup"><span data-stu-id="95af6-248">You can use the following example VBA code for a command button:</span></span>

```vb
    Private Sub Command0_Click()
    
    Dim strSourcePath As String
    Dim strDestPath As String
    
    strSourcePath = "<path>\sourceDb.accdb"
    strDestPath = "<path>\destDb.accdb"
    
    DBEngine.CompactDatabase strSourcePath, strDestPath, dbLangGeneral & ";pwd=Access", dbVersion120, ";pwd=Access"
    
    Set CurrentDatabase = CurrentDb
    Set LinkedTableDef = CurrentDatabase.CreateTableDef 
    ("My Linked Table")
    LinkedTableDef.Connect = "MS Access;pwd=Access";database=" & strDestPath
    LinkedTableDef.RefreshLink
    
    
    MsgBox "Finished"
    
    End Sub 
```

<br/>

<span data-ttu-id="95af6-249">В следующем примере кода показано, как использовать CompactDatabase паролем (ключ шифрования) и затем ссылка на таблицу в сжатии базы данных.</span><span class="sxs-lookup"><span data-stu-id="95af6-249">The following code sample shows how to use CompactDatabase with a password (encryption key) and then link to a table in that compacted database.</span></span> <span data-ttu-id="95af6-250">Обратите внимание на то, что необходимо указать пароль.</span><span class="sxs-lookup"><span data-stu-id="95af6-250">Note that a password must be supplied.</span></span>

```vb
    Private Sub CompactAndLink_Click() 
     
    Dim strSourcePath As String
    Dim strDestPath As String
    Dim strSourceTableName As String
    Dim strDestTableName As String
    Dim tdf As TableDef
     
    strSourcePath = "<path>\<database>.accdb"
    strDestPath = "<path>\<database>.accdb"
    strSourceTableName = "<table name in destination database>"
    strDestTableName = "<linked table name>"
     
    ' Compact source database into new destination database with encrypted password
    DBEngine.CompactDatabase strSourcePath, strDestPath, dbLangGeneral & ";pwd=Access", dbVersion120, ";pwd=Access"
     
    ' Link to one of the tables in the destination database
    ' Password must be provided in the Connect property
     
    Set CurrentDatabase = CurrentDb
    Set tdf = CurrentDatabase.CreateTableDef(strDestTableName)
       
        With tdf
            .Connect = ";pwd=Access" & ";DATABASE=" & strDestPath
            .SourceTableName = strSourceTableName
        End With
        
    CurrentDatabase.TableDefs.Append tdf
     
    MsgBox "Database compacted and encrypted password applied. Link to table also completed."
     
    End Sub
```
