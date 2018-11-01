---
title: DBEngine.CreateDatabase Method (DAO)
TOCTitle: CreateDatabase Method
ms:assetid: d5821a4b-483a-b8fa-e929-5f036057d8c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835033(v=office.15)
ms:contentKeyID: 48547966
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052972
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 65a32b2b7e884e2b5957f435df0592549062b7ed
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868020"
---
# <a name="dbenginecreatedatabase-method-dao"></a><span data-ttu-id="a499e-102">DBEngine.CreateDatabase Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="a499e-102">DBEngine.CreateDatabase Method (DAO)</span></span>


<span data-ttu-id="a499e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a499e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a499e-104">Создает новый объект **[базы данных](database-object-dao.md)** , сохраняет базы данных на диск и возвращает объект открыт **базы данных** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="a499e-104">Creates a new **[Database](database-object-dao.md)** object, saves the database to disk, and returns an opened **Database** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="a499e-105">.</span><span class="sxs-lookup"><span data-stu-id="a499e-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="a499e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a499e-106">Syntax</span></span>

<span data-ttu-id="a499e-107">*выражение* . CreateDatabase (***имя***, ***языкового стандарта*** ***параметр***)</span><span class="sxs-lookup"><span data-stu-id="a499e-107">*expression* .CreateDatabase(***Name***, ***Locale***, ***Option***)</span></span>

<span data-ttu-id="a499e-108">*выражение* Переменная, которая представляет собой объект- **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="a499e-108">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="a499e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a499e-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a499e-110">Имя</span><span class="sxs-lookup"><span data-stu-id="a499e-110">Name</span></span></p></th>
<th><p><span data-ttu-id="a499e-111">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="a499e-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="a499e-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a499e-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="a499e-113">Описание</span><span class="sxs-lookup"><span data-stu-id="a499e-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a499e-114">Имя</span><span class="sxs-lookup"><span data-stu-id="a499e-114">Name</span></span></p></td>
<td><p><span data-ttu-id="a499e-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a499e-115">Required</span></span></p></td>
<td><p><span data-ttu-id="a499e-116"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-117">Строка длиной до 255 знаков, — это имя файла базы данных, который вы создаете.</span><span class="sxs-lookup"><span data-stu-id="a499e-117">A String up to 255 characters long that is the name of the database file that you're creating.</span></span> <span data-ttu-id="a499e-118">Это может быть полный путь и имя файла.</span><span class="sxs-lookup"><span data-stu-id="a499e-118">It can be the full path and file name.</span></span> <span data-ttu-id="a499e-119">Если сеть поддерживает его, можно также указать сетевой путь, таких как &quot; \\server1\share1\dir1\db1&quot;.</span><span class="sxs-lookup"><span data-stu-id="a499e-119">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1&quot;.</span></span> <span data-ttu-id="a499e-120">Файлы базы данных Microsoft Access можно создать только с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="a499e-120">You can only create Microsoft Access database files with this method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a499e-121">Locale</span><span class="sxs-lookup"><span data-stu-id="a499e-121">Locale</span></span></p></td>
<td><p><span data-ttu-id="a499e-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a499e-122">Required</span></span></p></td>
<td><p><span data-ttu-id="a499e-123"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-123"><strong>String</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="a499e-124">Строковое выражение, которое определяет порядок сортировки при создании базы данных, как указано в настройки.</span><span class="sxs-lookup"><span data-stu-id="a499e-124">A string expression that specifies a collating order for creating the database, as specified in Settings.</span></span> <span data-ttu-id="a499e-125">Необходимо указать этот аргумент или возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="a499e-125">You must supply this argument or an error occurs.</span></span></p></li>
<li><p><span data-ttu-id="a499e-126">Можно также создать пароль для нового объекта <strong>базы данных</strong> , объединив Строка пароля (начиная с &quot;; pwd =&quot; ) с константой в аргументе <em>языкового стандарта</em> , следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a499e-126">You can also create a password for the new <strong>Database</strong> object by concatenating the password string (starting with &quot;;pwd=&quot; ) with a constant in the <em>locale</em> argument, like this:</span></span></p></li>
<li><p><span data-ttu-id="a499e-127">dbLangSpanish &amp; &quot;; pwd = Новый_пароль&quot;</span><span class="sxs-lookup"><span data-stu-id="a499e-127">dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="a499e-128">Если вы хотите использовать по умолчанию для <em>языкового стандарта</em>, но укажите пароль, просто введите строку пароль для аргумента <em>языкового стандарта</em> :</span><span class="sxs-lookup"><span data-stu-id="a499e-128">If you want to use the default <em>locale</em>, but specify a password, simply enter a password string for the <em>locale</em> argument:</span></span></p></li>
<li><p><span data-ttu-id="a499e-129">&quot;; pwd = Новый_пароль&quot;</span><span class="sxs-lookup"><span data-stu-id="a499e-129">&quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="a499e-130">Используйте надежные пароли, содержащие верхний и строчные буквы, числа и символы.</span><span class="sxs-lookup"><span data-stu-id="a499e-130">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="a499e-131">Ненадежные пароли не смешивайте этих элементов.</span><span class="sxs-lookup"><span data-stu-id="a499e-131">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="a499e-132">Надежный пароль: Y6dh! et5.</span><span class="sxs-lookup"><span data-stu-id="a499e-132">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="a499e-133">Ненадежный пароль: House27.</span><span class="sxs-lookup"><span data-stu-id="a499e-133">Weak password: House27.</span></span> <span data-ttu-id="a499e-134">Используйте надежный пароль, который вы можете запомнить, чтобы записать его не нужно.</span><span class="sxs-lookup"><span data-stu-id="a499e-134">Use a strong password that you can remember so that you don't have to write it down.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a499e-135">Параметр</span><span class="sxs-lookup"><span data-stu-id="a499e-135">Option</span></span></p></td>
<td><p><span data-ttu-id="a499e-136">Необязательный</span><span class="sxs-lookup"><span data-stu-id="a499e-136">Optional</span></span></p></td>
<td><p><span data-ttu-id="a499e-137"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-137"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-138">Константа или сочетание констант, которое указывает один или несколько параметров, как указано в настройки.</span><span class="sxs-lookup"><span data-stu-id="a499e-138">A constant or combination of constants that indicates one or more options, as specified in Settings.</span></span> <span data-ttu-id="a499e-139">Параметры можно использовать суммируются соответствующий констант.</span><span class="sxs-lookup"><span data-stu-id="a499e-139">You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a499e-140">Замечания</span><span class="sxs-lookup"><span data-stu-id="a499e-140">Remarks</span></span>

<span data-ttu-id="a499e-141">Можно использовать один из следующих константы для аргумента языковой стандарт для указания свойства **[CollatingOrder](database-collatingorder-property-dao.md)** текста для сравнения строк.</span><span class="sxs-lookup"><span data-stu-id="a499e-141">You can use one of the following constants for the locale argument to specify the **[CollatingOrder](database-collatingorder-property-dao.md)** property of text for string comparisons.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a499e-142">Constant</span><span class="sxs-lookup"><span data-stu-id="a499e-142">Constant</span></span></p></th>
<th><p><span data-ttu-id="a499e-143">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="a499e-143">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a499e-144"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-144"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-145">Английский, немецкий, французский, португальский, итальянский и современных испанский</span><span class="sxs-lookup"><span data-stu-id="a499e-145">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a499e-146"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-146"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-147">арабский;</span><span class="sxs-lookup"><span data-stu-id="a499e-147">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a499e-148"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-148"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-149">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="a499e-149">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a499e-150"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-150"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-151">Китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="a499e-151">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a499e-152"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-152"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-153">русский;</span><span class="sxs-lookup"><span data-stu-id="a499e-153">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a499e-154"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-154"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-155">чешский;</span><span class="sxs-lookup"><span data-stu-id="a499e-155">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a499e-156"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-156"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-157">голландский;</span><span class="sxs-lookup"><span data-stu-id="a499e-157">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a499e-158"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-158"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-159">греческий;</span><span class="sxs-lookup"><span data-stu-id="a499e-159">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a499e-160"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-160"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-161">иврит;</span><span class="sxs-lookup"><span data-stu-id="a499e-161">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a499e-162"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-162"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-163">венгерский;</span><span class="sxs-lookup"><span data-stu-id="a499e-163">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a499e-164"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-164"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-165">Исландский</span><span class="sxs-lookup"><span data-stu-id="a499e-165">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a499e-166"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-166"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-167">японский;</span><span class="sxs-lookup"><span data-stu-id="a499e-167">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a499e-168"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-168"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-169">корейский;</span><span class="sxs-lookup"><span data-stu-id="a499e-169">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a499e-170"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-170"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-171">Скандинавские языки (ядра Microsoft Jet базы данных версии 1.0 только)</span><span class="sxs-lookup"><span data-stu-id="a499e-171">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a499e-172"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-172"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-173">Датский и норвежский</span><span class="sxs-lookup"><span data-stu-id="a499e-173">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a499e-174"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-174"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-175">польский;</span><span class="sxs-lookup"><span data-stu-id="a499e-175">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a499e-176"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-176"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-177">словенский;</span><span class="sxs-lookup"><span data-stu-id="a499e-177">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a499e-178"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-178"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-179">Испанский (традиционный)</span><span class="sxs-lookup"><span data-stu-id="a499e-179">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a499e-180"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-180"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-181">Финский и шведский</span><span class="sxs-lookup"><span data-stu-id="a499e-181">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a499e-182"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-182"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-183">тайский;</span><span class="sxs-lookup"><span data-stu-id="a499e-183">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a499e-184"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-184"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-185">турецкий;</span><span class="sxs-lookup"><span data-stu-id="a499e-185">Turkish</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a499e-186">Одно или несколько из следующих констант в аргументе параметры можно использовать для указания версии должен иметь формат данных и ли шифрование базы данных.</span><span class="sxs-lookup"><span data-stu-id="a499e-186">You can use one or more of the following constants in the options argument to specify which version the data format should have and whether or not to encrypt the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a499e-187">Константа</span><span class="sxs-lookup"><span data-stu-id="a499e-187">Constant</span></span></p></th>
<th><p><span data-ttu-id="a499e-188">Описание</span><span class="sxs-lookup"><span data-stu-id="a499e-188">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a499e-189"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-189"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-190">Создает зашифрованной базе данных.</span><span class="sxs-lookup"><span data-stu-id="a499e-190">Creates an encrypted database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a499e-191"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-191"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-192">Создает базу данных в формате Microsoft Jet база данных модуля версии 1.0 файла.</span><span class="sxs-lookup"><span data-stu-id="a499e-192">Creates a database that uses the Microsoft Jet database engine version 1.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a499e-193"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-193"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-194">Создает базу данных в формате Microsoft Jet база данных модуля версии 1.1 файла.</span><span class="sxs-lookup"><span data-stu-id="a499e-194">Creates a database that uses the Microsoft Jet database engine version 1.1 file format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a499e-195"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-195"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-196">Создает базу данных в формате Microsoft Jet база данных модуля версии 2.0 файла.</span><span class="sxs-lookup"><span data-stu-id="a499e-196">Creates a database that uses the Microsoft Jet database engine version 2.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a499e-197"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-197"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-198">Создает базу данных, который использует Microsoft Jet engine версии 3.0 формате файла базы данных (совместимый с версией 3.5).</span><span class="sxs-lookup"><span data-stu-id="a499e-198">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a499e-199"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-199"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-200">Создает базу данных в формате Microsoft Jet база данных модуля версии 4.0 файл.</span><span class="sxs-lookup"><span data-stu-id="a499e-200">Creates a database that uses the Microsoft Jet database engine version 4.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a499e-201"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="a499e-201"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="a499e-202">Создает базу данных в формате Microsoft Access базы данных модуля версии 12.0 файла.</span><span class="sxs-lookup"><span data-stu-id="a499e-202">Creates a database that uses the Microsoft Access database engine version 12.0 file format.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a499e-203">Если опустить константу шифрования **CreateDatabase** создает без зашифрованной базе данных.</span><span class="sxs-lookup"><span data-stu-id="a499e-203">If you omit the encryption constant, **CreateDatabase** creates an un-encrypted database.</span></span>

<span data-ttu-id="a499e-204">Используйте метод **CreateDatabase** Создание и открытие новой пустой базы данных и возвращают объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="a499e-204">Use the **CreateDatabase** method to create and open a new, empty database, and return the **Database** object.</span></span> <span data-ttu-id="a499e-205">С помощью дополнительных объектов DAO необходимо выполнить его структуру и содержимое.</span><span class="sxs-lookup"><span data-stu-id="a499e-205">You must complete its structure and content by using additional DAO objects.</span></span> <span data-ttu-id="a499e-206">Если вы хотите создать частичного или полного копию существующей базы данных, можно использовать метод **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** для копирования, можно настроить.</span><span class="sxs-lookup"><span data-stu-id="a499e-206">If you want to make a partial or complete copy of an existing database, you can use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method to make a copy that you can customize.</span></span>

