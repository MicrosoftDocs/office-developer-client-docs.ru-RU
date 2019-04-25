---
title: Метод DBEngine.CompactDatabase (DAO)
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
localization_priority: Priority
ms.openlocfilehash: b50cb0453df1fa357fbd0b089af2e74fdd4b4c1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294339"
---
# <a name="dbenginecompactdatabase-method-dao"></a><span data-ttu-id="94650-102">Метод DBEngine.CompactDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="94650-102">DBEngine.CompactDatabase Method (DAO)</span></span>

<span data-ttu-id="94650-103">**Область применения**: Access 2013 | Access 2016</span><span class="sxs-lookup"><span data-stu-id="94650-103">**Applies to:** Access 2013 | Access 2016</span></span>

<span data-ttu-id="94650-104">Копирует и сжимает закрытую базу данных, предоставляя возможность изменить ее версию, порядок сортировки и шифрование.</span><span class="sxs-lookup"><span data-stu-id="94650-104">Copies and compacts a closed database, and gives you the option of changing its version, collating order, and encryption.</span></span> <span data-ttu-id="94650-105">(Только для рабочих областей Microsoft Access.)</span><span class="sxs-lookup"><span data-stu-id="94650-105">Creates a new TableDef object (Microsoft Access workspaces only).</span></span>

> [!NOTE]
> <span data-ttu-id="94650-106">Если используются зашифрованные связанные таблицы для действия, обновления и запросов SQL [например, оператор SQL UPDATE (CurrentDb.Execute "UPDATE...")], необходимо указать ключ шифрования.</span><span class="sxs-lookup"><span data-stu-id="94650-106">When using encrypted linked tables for action, update, and SQL queries [such as a SQL UPDATE statement (CurrentDb.Execute "UPDATE...")], you must supply the encryption key.</span></span> <span data-ttu-id="94650-107">Кроме того, в связанных таблицах установлено ограничение в 19 знаков для ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="94650-107">Also, linked tables have a 19-character limit for the encryption key.</span></span> <span data-ttu-id="94650-108">См. раздел **Зашифрованные связанные таблицы** в конце этой статьи.</span><span class="sxs-lookup"><span data-stu-id="94650-108">See the **Encrypted linked tables** section at the end of this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="94650-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94650-109">Syntax</span></span>

<span data-ttu-id="94650-110">*выражение* .CompactDatabase(***SrcName***, ***DstName***, ***DstLocale***, ***Options***, ***password***)</span><span class="sxs-lookup"><span data-stu-id="94650-110">*expression* .CompactDatabase(***SrcName***, ***DstName***, ***DstLocale***, ***Options***, ***password***)</span></span>

<span data-ttu-id="94650-111">*выражение*: выражение, возвращающее объект **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="94650-111">*expression* An expression that returns a **Range** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="94650-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="94650-112">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="94650-113">Имя</span><span class="sxs-lookup"><span data-stu-id="94650-113">Name</span></span></p></th>
<th><p><span data-ttu-id="94650-114">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="94650-114">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="94650-115">Тип данных</span><span class="sxs-lookup"><span data-stu-id="94650-115">Data type</span></span></p></th>
<th><p><span data-ttu-id="94650-116">Описание</span><span class="sxs-lookup"><span data-stu-id="94650-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94650-117"><em>SrcName</em></span><span class="sxs-lookup"><span data-stu-id="94650-117"><em>SrcName</em></span></span></p></td>
<td><p><span data-ttu-id="94650-118">Обязательный</span><span class="sxs-lookup"><span data-stu-id="94650-118">Required</span></span></p></td>
<td><p><span data-ttu-id="94650-119"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="94650-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-120">Определяет существующую закрытую базу данных.</span><span class="sxs-lookup"><span data-stu-id="94650-120">Identifies an existing, closed database.</span></span> <span data-ttu-id="94650-121">Это может быть полный путь и имя файла, например &quot;C:\db1.mdb&quot;.</span><span class="sxs-lookup"><span data-stu-id="94650-121">It can be a full path and file name, such as &quot;C:\db1.mdb&quot;.</span></span> <span data-ttu-id="94650-122">Если имя файла содержит расширение, необходимо его указать.</span><span class="sxs-lookup"><span data-stu-id="94650-122">If the file name has an extension, you must specify it.</span></span> <span data-ttu-id="94650-123">Если в сети поддерживается эта возможность, также можно указать сетевой путь, например &quot;\\server1\share1\dir1\db1.mdb&quot;</span><span class="sxs-lookup"><span data-stu-id="94650-123">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1.mdb&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94650-124"><em>DstName</em></span><span class="sxs-lookup"><span data-stu-id="94650-124"><em>DstName</em></span></span></p></td>
<td><p><span data-ttu-id="94650-125">Обязательный</span><span class="sxs-lookup"><span data-stu-id="94650-125">Required</span></span></p></td>
<td><p><span data-ttu-id="94650-126"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="94650-126"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-127">Имя файла (и путь) сжатой базы данных, которую вы создаете.</span><span class="sxs-lookup"><span data-stu-id="94650-127">the file name (and path) of the compacted database that you're creating.</span></span> <span data-ttu-id="94650-128">Также можно указать сетевой путь.</span><span class="sxs-lookup"><span data-stu-id="94650-128">You can also specify a network path.</span></span> <span data-ttu-id="94650-129">С помощью этого аргумента нельзя указать тот же файл базы данных, что и в аргументе SrcName.</span><span class="sxs-lookup"><span data-stu-id="94650-129">You can't use this argument to specify the same database file as SrcName.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94650-130"><em>DstLocale</em></span><span class="sxs-lookup"><span data-stu-id="94650-130"><em>DstLocale</em></span></span></p></td>
<td><p><span data-ttu-id="94650-131">Необязательный</span><span class="sxs-lookup"><span data-stu-id="94650-131">Optional</span></span></p></td>
<td><p><span data-ttu-id="94650-132"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="94650-132"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-133">Строковое выражение, указывающее порядок сортировки для создания DstName, как указанно в примечаниях.</span><span class="sxs-lookup"><span data-stu-id="94650-133">A string expression that specifies a collating order for creating DstName, as specified in Remarks.</span></span></p>
<ul>
<li><p><span data-ttu-id="94650-134">Если этот аргумент опущен, языковой стандарт DstName совпадает с SrcName.</span><span class="sxs-lookup"><span data-stu-id="94650-134">If you omit this argument, the locale of DstName is the same as SrcName.</span></span></p></li>
<li><p><span data-ttu-id="94650-135">Вы также можете создать пароль для DstName, объединив строку пароля (начиная с &quot;;pwd=&quot;) с константой в аргументе DstLocale следующим образом: dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;.</span><span class="sxs-lookup"><span data-stu-id="94650-135">You can also create a password for DstName by concatenating the password string (starting with &quot;;pwd=&quot;) with a constant in the DstLocale argument, like this: dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;.</span></span></p></li>
<li><p><span data-ttu-id="94650-136">Если вы хотите использовать такой же аргумент DstLocale, как в SrcName (значение по умолчанию), но указать новый пароль, просто введите строку пароля для DstLocale: &quot;;pwd=NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="94650-136">If you want to use the same DstLocale as SrcName (the default value), but specify a new password, simply enter a password string for DstLocale: &quot;;pwd=NewPassword&quot;</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94650-137"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="94650-137"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="94650-138">Необязательно</span><span class="sxs-lookup"><span data-stu-id="94650-138">Optional</span></span></p></td>
<td><p><span data-ttu-id="94650-139"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="94650-139"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-140">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="94650-140">Optional.</span></span> <span data-ttu-id="94650-141">Константа или сочетание констант, определяющих один или несколько параметров, как указано в примечаниях.</span><span class="sxs-lookup"><span data-stu-id="94650-141">A constant or combination of constants that indicates one or more options, as specified in Remarks.</span></span> <span data-ttu-id="94650-142">Вы можете объединить параметры, сложив соответствующие константы.</span><span class="sxs-lookup"><span data-stu-id="94650-142">You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94650-143"><em>password</em></span><span class="sxs-lookup"><span data-stu-id="94650-143"><em>Password</em></span></span></p></td>
<td><p><span data-ttu-id="94650-144">Необязательный</span><span class="sxs-lookup"><span data-stu-id="94650-144">Optional</span></span></p></td>
<td><p><span data-ttu-id="94650-145"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="94650-145"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-146">Строковое выражение, содержащее ключ шифрования, если база данных зашифрована.</span><span class="sxs-lookup"><span data-stu-id="94650-146">A string expression containing an encryption key, if the database is encrypted.</span></span> <span data-ttu-id="94650-147">Перед фактическим паролем должна находиться строка &quot;;pwd=&quot;.</span><span class="sxs-lookup"><span data-stu-id="94650-147">The string &quot;;pwd=&quot; must precede the actual password.</span></span> <span data-ttu-id="94650-148">Если параметр пароля добавлен в DstLocale, этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="94650-148">If you include a password setting in DstLocale, this setting is ignored.</span></span></p><p><span data-ttu-id="94650-149"><strong>ПРИМЕЧАНИЕ</strong>. Это устаревший параметр, который не поддерживается в формате ACCDB.</span><span class="sxs-lookup"><span data-stu-id="94650-149"><strong>NOTE</strong>: This is deprecated parameter and is not supported in .ACCDB format.</span></span> <span data-ttu-id="94650-150">Чтобы зашифровать ACCDB-файл, используйте строку параметра "pwd=".</span><span class="sxs-lookup"><span data-stu-id="94650-150">To encrypt an .ACCDB file, use the "pwd=" option string.</span></span> <span data-ttu-id="94650-151">Используйте надежные пароли, содержащие строчные и прописные буквы, цифры и знаки.</span><span class="sxs-lookup"><span data-stu-id="94650-151">Use strong passwords that combine uppercase and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="94650-152">В ненадежных паролях не используются сочетания таких элементов.</span><span class="sxs-lookup"><span data-stu-id="94650-152">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="94650-153">Надежный пароль: Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="94650-153">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="94650-154">Слабый пароль: House27.</span><span class="sxs-lookup"><span data-stu-id="94650-154">Weak password: House27.</span></span> <span data-ttu-id="94650-155">Используйте надежный пароль, который можно запомнить, чтобы не пришлось его записывать.</span><span class="sxs-lookup"><span data-stu-id="94650-155">Use a strong password that you can remember so that you don't have to write it down.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="94650-156">Примечания</span><span class="sxs-lookup"><span data-stu-id="94650-156">Remarks</span></span>

<span data-ttu-id="94650-157">Можно использовать одну из следующих констант для аргумента DstLocale, чтобы задать свойство **CollatingOrder** для сравнения строк текста.</span><span class="sxs-lookup"><span data-stu-id="94650-157">You can use one of the following constants for the DstLocale argument to specify the **CollatingOrder** property for string comparisons of text.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="94650-158">Константа</span><span class="sxs-lookup"><span data-stu-id="94650-158">Constant</span></span></p></th>
<th><p><span data-ttu-id="94650-159">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="94650-159">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94650-160"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="94650-160"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-161">Английский, немецкий, французский, португальский, итальянский и современный испанский</span><span class="sxs-lookup"><span data-stu-id="94650-161">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94650-162"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="94650-162"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-163">Арабский</span><span class="sxs-lookup"><span data-stu-id="94650-163">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94650-164"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="94650-164"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-165">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="94650-165">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94650-166"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="94650-166"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-167">Китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="94650-167">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94650-168"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="94650-168"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-169">Русский</span><span class="sxs-lookup"><span data-stu-id="94650-169">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94650-170"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="94650-170"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-171">Чешский</span><span class="sxs-lookup"><span data-stu-id="94650-171">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94650-172"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="94650-172"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-173">Голландский</span><span class="sxs-lookup"><span data-stu-id="94650-173">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94650-174"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="94650-174"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-175">Греческий</span><span class="sxs-lookup"><span data-stu-id="94650-175">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94650-176"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="94650-176"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-177">Иврит</span><span class="sxs-lookup"><span data-stu-id="94650-177">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94650-178"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="94650-178"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-179">Венгерский</span><span class="sxs-lookup"><span data-stu-id="94650-179">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94650-180"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="94650-180"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-181">Исландский</span><span class="sxs-lookup"><span data-stu-id="94650-181">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94650-182"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="94650-182"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-183">Японский</span><span class="sxs-lookup"><span data-stu-id="94650-183">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94650-184"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="94650-184"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-185">Корейский</span><span class="sxs-lookup"><span data-stu-id="94650-185">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94650-186"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="94650-186"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-187">Скандинавские языки (только ядро СУБД Microsoft Jet версии 1.0)</span><span class="sxs-lookup"><span data-stu-id="94650-187">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94650-188"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="94650-188"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-189">Норвежский и датский</span><span class="sxs-lookup"><span data-stu-id="94650-189">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94650-190"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="94650-190"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-191">Польский</span><span class="sxs-lookup"><span data-stu-id="94650-191">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94650-192"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="94650-192"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-193">Словенский</span><span class="sxs-lookup"><span data-stu-id="94650-193">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94650-194"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="94650-194"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-195">Традиционный испанский</span><span class="sxs-lookup"><span data-stu-id="94650-195">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94650-196"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="94650-196"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-197">Шведский и финский</span><span class="sxs-lookup"><span data-stu-id="94650-197">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94650-198"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="94650-198"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-199">Тайский</span><span class="sxs-lookup"><span data-stu-id="94650-199">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94650-200"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="94650-200"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-201">Турецкий</span><span class="sxs-lookup"><span data-stu-id="94650-201">Turkish</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="94650-202">Можно использовать одну из следующих констант в аргументе Options, чтобы указать необходимость шифрования или расшифровки базы данных при сжатии.</span><span class="sxs-lookup"><span data-stu-id="94650-202">You can use one of the following constants in the options argument to specify whether to encrypt or to decrypt the database while it's compacted.</span></span>

> [!NOTE]
> <span data-ttu-id="94650-203">Константы dbEncrypt и dbDecrypt являются устаревшими и не поддерживаются в форматах файлов ACCDB.</span><span class="sxs-lookup"><span data-stu-id="94650-203">The constants dbEncrypt and dbDecrypt are deprecated and not supported in .ACCDB file formats.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="94650-204">Константа</span><span class="sxs-lookup"><span data-stu-id="94650-204">Constant</span></span></p></th>
<th><p><span data-ttu-id="94650-205">Описание</span><span class="sxs-lookup"><span data-stu-id="94650-205">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94650-206"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="94650-206"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-207">Шифрование базы данных при сжатии.</span><span class="sxs-lookup"><span data-stu-id="94650-207">Encrypt the database while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94650-208"><strong>dbDecrypt</strong></span><span class="sxs-lookup"><span data-stu-id="94650-208"><strong>dbDecrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-209">Расшифровка базы данных при сжатии.</span><span class="sxs-lookup"><span data-stu-id="94650-209">Decrypt the database while compacting.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="94650-210">Если опустить константу шифрования или указать как **dbDecrypt**, так и **dbEncrypt**, для DstName будет применяться такое же шифрование, как для SrcName.</span><span class="sxs-lookup"><span data-stu-id="94650-210">If you omit an encryption constant or if you include both **dbDecrypt** and **dbEncrypt**, DstName will have the same encryption as SrcName.</span></span>

<span data-ttu-id="94650-211">Можно использовать одну из следующих констант в аргументе Options, чтобы указать версию формата данных сжатой базы данных.</span><span class="sxs-lookup"><span data-stu-id="94650-211">You can use one of the following constants in the options argument to specify the version of the data format for the compacted database.</span></span> <span data-ttu-id="94650-212">Эта константа влияет только на версию формата данных DstName и не влияет на версию объектов, определяемых в Microsoft Access, таких как формы и отчеты.</span><span class="sxs-lookup"><span data-stu-id="94650-212">This constant affects only the version of the data format of DstName and doesn't affect the version of any Microsoft Access-defined objects, such as forms and reports.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="94650-213">Константа</span><span class="sxs-lookup"><span data-stu-id="94650-213">Constant</span></span></p></th>
<th><p><span data-ttu-id="94650-214">Описание</span><span class="sxs-lookup"><span data-stu-id="94650-214">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94650-215"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="94650-215"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-216">Создает базу данных, использующую при сжатии формат файлов ядра СУБД Microsoft Jet версии 1.0.</span><span class="sxs-lookup"><span data-stu-id="94650-216">Creates a database that uses the Microsoft Jet database engine version 1.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94650-217"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="94650-217"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-218">Создает базу данных, использующую при сжатии формат файлов ядра СУБД Microsoft Jet версии 1.1.</span><span class="sxs-lookup"><span data-stu-id="94650-218">Creates a database that uses the Microsoft Jet database engine version 1.1 file format while compacting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94650-219"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="94650-219"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-220">Создает базу данных, использующую при сжатии формат файлов ядра СУБД Microsoft Jet версии 2.0.</span><span class="sxs-lookup"><span data-stu-id="94650-220">Creates a database that uses the Microsoft Jet database engine version 2.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94650-221"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="94650-221"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-222">Создает базу данных, использующую при сжатии формат файлов ядра СУБД Microsoft Jet версии 3.0 (совместимый с версией 3.5).</span><span class="sxs-lookup"><span data-stu-id="94650-222">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5) while compacting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94650-223"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="94650-223"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-224">Создает базу данных, использующую при сжатии формат файлов ядра СУБД Microsoft Jet версии 4.0.</span><span class="sxs-lookup"><span data-stu-id="94650-224">Creates a database that uses the Microsoft Jet database engine version 4.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94650-225"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="94650-225"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="94650-226">Создает базу данных, использующую при сжатии формат файлов ядра СУБД Microsoft Access версии 12.0.</span><span class="sxs-lookup"><span data-stu-id="94650-226">Creates a database that uses the Microsoft Access database engine version 12.0 file format while compacting.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="94650-227">Можно указать константу только одной версии.</span><span class="sxs-lookup"><span data-stu-id="94650-227">You can specify only one version constant.</span></span> <span data-ttu-id="94650-228">Если опустить константу версии, версия DstName будет совпадать с SrcName.</span><span class="sxs-lookup"><span data-stu-id="94650-228">If you omit a version constant, DstName will have the same version as SrcName.</span></span> <span data-ttu-id="94650-229">Можно сжать DstName только до версии, совпадающей с версией SrcName или более поздней.</span><span class="sxs-lookup"><span data-stu-id="94650-229">You can compact DstName only to a version that is the same or later than that of SrcName.</span></span>

<span data-ttu-id="94650-230">Когда вы изменяете данные в базе данных, файл базы данных может фрагментироваться и будет занимать больше места на диске, чем требуется.</span><span class="sxs-lookup"><span data-stu-id="94650-230">As you change data in a database, the database file can become fragmented and use more disk space than is necessary.</span></span> <span data-ttu-id="94650-231">Периодически для сжатия базы данных можно использовать метод **CompactDatabase**, чтобы дефрагментировать файл базы данных.</span><span class="sxs-lookup"><span data-stu-id="94650-231">Periodically, you can use the **CompactDatabase** method to compact your database to defragment the database file.</span></span> <span data-ttu-id="94650-232">Сжатая база данных обычно меньше и часто работает быстрее.</span><span class="sxs-lookup"><span data-stu-id="94650-232">The compacted database is usually smaller and often runs faster.</span></span> <span data-ttu-id="94650-233">Вы также можете изменить порядок сортировки, шифрование или версию формата данных при копировании и сжатии базы данных.</span><span class="sxs-lookup"><span data-stu-id="94650-233">You can also change the collating order, the encryption, or the version of the data format while you copy and compact the database.</span></span>

<span data-ttu-id="94650-234">Необходимо закрыть файл SrcName перед его сжатием.</span><span class="sxs-lookup"><span data-stu-id="94650-234">You must close SrcName before you compact it.</span></span> <span data-ttu-id="94650-235">В многопользовательской среде другие пользователи не могут держать SrcName в открытом состоянии при его сжатии.</span><span class="sxs-lookup"><span data-stu-id="94650-235">In a multiuser environment, other users can't have SrcName open while you're compacting it.</span></span> <span data-ttu-id="94650-236">Если SrcName не закрыт или недоступен для монопольного использования, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="94650-236">If SrcName isn't closed or isn't available for exclusive use, an error occurs.</span></span>

<span data-ttu-id="94650-237">Так как метод **CompactDatabase** создает копию базы данных, необходимо располагать достаточным местом как для исходной базы данных, так и для копии.</span><span class="sxs-lookup"><span data-stu-id="94650-237">Because **CompactDatabase** creates a copy of the database, you must have enough disk space for both the original and the duplicate databases.</span></span> <span data-ttu-id="94650-238">Операция сжатия завершается сбоем, если отсутствует достаточное место на диске.</span><span class="sxs-lookup"><span data-stu-id="94650-238">The compact operation fails if there isn't enough disk space available.</span></span> <span data-ttu-id="94650-239">Дублированную базу данных DstName не обязательно располагать на том же диске, что и SrcName.</span><span class="sxs-lookup"><span data-stu-id="94650-239">The DstName duplicate database doesn't have to be on the same disk as SrcName.</span></span> <span data-ttu-id="94650-240">После успешного сжатия базы данных можно удалить файл SrcName и присвоить сжатому файлу DstName исходное имя файла.</span><span class="sxs-lookup"><span data-stu-id="94650-240">After successfully compacting a database, you can delete the SrcName file and rename the compacted DstName file to the original file name.</span></span>

<span data-ttu-id="94650-241">Метод **CompactDatabase** копирует все данные и параметры разрешений системы безопасности из базы данных, определяемой SrcName, в базу данных, определяемую DstName.</span><span class="sxs-lookup"><span data-stu-id="94650-241">The **CompactDatabase** method copies all the data and the security permission settings from the database specified by SrcName to the database specified by DstName.</span></span>

> [!NOTE]
> <span data-ttu-id="94650-242">Так как метод **CompactDatabase** не преобразует объекты Microsoft Access, не следует использовать **CompactDatabase** для преобразования базы данных, содержащей такие объекты.</span><span class="sxs-lookup"><span data-stu-id="94650-242">Because the **CompactDatabase** method doesn't convert Microsoft Access objects, you shouldn't use **CompactDatabase** to convert a database containing such objects.</span></span>

## <a name="encrypted-linked-tables"></a><span data-ttu-id="94650-243">Зашифрованные связанные таблицы</span><span class="sxs-lookup"><span data-stu-id="94650-243">Encrypted linked tables</span></span>

<span data-ttu-id="94650-244">Зашифрованные пароли зависят от используемого формата файла базы данных.</span><span class="sxs-lookup"><span data-stu-id="94650-244">Encrypted passwords are dependent on the file format of the database that you are using.</span></span> <span data-ttu-id="94650-245">Если вы используете Access 2003 (.mdb) или базу данных более ранней версии, у вас есть один пароль для защиты базы данных и другой пароль для шифрования базы данных.</span><span class="sxs-lookup"><span data-stu-id="94650-245">If you are using an Access 2003 (.mdb) or earlier database, you will have one password to protect the database, and a separate password to encrypt the database.</span></span> <span data-ttu-id="94650-246">В Access 2007 (.accdb) или базах данных более поздних версий (.mdb) зашифровать и защитить базу данных можно только с помощью одного пароля, так как возможность использования двух разных паролей была удалена.</span><span class="sxs-lookup"><span data-stu-id="94650-246">For Access 2007 (.accdb) and later (.mdb) databases, the only option is to encrypt and protect the database with one password, as the option to have two separate passwords has been removed.</span></span>

> [!NOTE]
> <span data-ttu-id="94650-247">Для баз данных Access 2007 (.accdb) пароль является ключом шифрования</span><span class="sxs-lookup"><span data-stu-id="94650-247">For Access 2007 (.accdb) databases, the password is the encryption key</span></span>

<span data-ttu-id="94650-248">Вы можете использовать следующий пример кода VBA для кнопки:</span><span class="sxs-lookup"><span data-stu-id="94650-248">You can use the following example VBA code for a command button:</span></span>

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

<span data-ttu-id="94650-249">В следующем примере кода показано, как использовать CompactDatabase с паролем (ключом шифрования) и затем сослаться на таблицу в этой сжатой базе данных.</span><span class="sxs-lookup"><span data-stu-id="94650-249">The following code sample shows how to use CompactDatabase with a password (encryption key) and then link to a table in that compacted database.</span></span> <span data-ttu-id="94650-250">Обратите внимание, что нужно указать пароль.</span><span class="sxs-lookup"><span data-stu-id="94650-250">Note that a password must be supplied.</span></span>

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
