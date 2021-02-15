---
title: Метод DBEngine.CreateDatabase (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 13e41dcd182f720b3611108311db6cd56fb4847e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294367"
---
# <a name="dbenginecreatedatabase-method-dao"></a><span data-ttu-id="9bdbe-102">Метод DBEngine.CreateDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="9bdbe-102">DBEngine.CreateDatabase method (DAO)</span></span>

<span data-ttu-id="9bdbe-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9bdbe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9bdbe-104">Создает новый объект **[базы](database-object-dao.md)** данных, сохраняет базу данных на диск и возвращает открытый объект **базы** данных (только для рабочих пространств Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9bdbe-104">Creates a new **[Database](database-object-dao.md)** object, saves the database to disk, and returns an opened **Database** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="9bdbe-105">.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-105">.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bdbe-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bdbe-106">Syntax</span></span>

<span data-ttu-id="9bdbe-107">*выражение .* CreateDatabase(***Name***, ***Locale***, ***Option***)</span><span class="sxs-lookup"><span data-stu-id="9bdbe-107">*expression* .CreateDatabase(***Name***, ***Locale***, ***Option***)</span></span>

<span data-ttu-id="9bdbe-108">*expression*: переменная, представляющая объект **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="9bdbe-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9bdbe-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9bdbe-110">Имя</span><span class="sxs-lookup"><span data-stu-id="9bdbe-110">Name</span></span></p></th>
<th><p><span data-ttu-id="9bdbe-111">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="9bdbe-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="9bdbe-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9bdbe-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="9bdbe-113">Описание</span><span class="sxs-lookup"><span data-stu-id="9bdbe-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9bdbe-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="9bdbe-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9bdbe-115">Required</span></span></p></td>
<td><p><span data-ttu-id="9bdbe-116"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-117">Строка длиной до 255 символов, которая является именем создаемого файла базы данных.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-117">A String up to 255 characters long that is the name of the database file that you're creating.</span></span> <span data-ttu-id="9bdbe-118">Это может быть полный путь и имя файла.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-118">It can be the full path and file name.</span></span> <span data-ttu-id="9bdbe-119">Если ваша сеть поддерживает его, можно также указать сетевой путь, например &quot; \\ server1\share1\dir1\db1. &quot;</span><span class="sxs-lookup"><span data-stu-id="9bdbe-119">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1&quot;.</span></span> <span data-ttu-id="9bdbe-120">С помощью этого метода можно создавать только файлы базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-120">You can only create Microsoft Access database files with this method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bdbe-121"><em>Locale</em></span><span class="sxs-lookup"><span data-stu-id="9bdbe-121"><em>Locale</em></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-122">Обязательно</span><span class="sxs-lookup"><span data-stu-id="9bdbe-122">Required</span></span></p></td>
<td><p><span data-ttu-id="9bdbe-123"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-123"><strong>String</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="9bdbe-124">Строковая выражение, указывающее порядок настройки параметров для создания базы данных, как указано в параметрах.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-124">A string expression that specifies a collating order for creating the database, as specified in Settings.</span></span> <span data-ttu-id="9bdbe-125">Необходимо предоставить этот аргумент или возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-125">You must supply this argument or an error occurs.</span></span></p></li>
<li><p><span data-ttu-id="9bdbe-126">Вы также можете создать пароль для нового объекта <strong>Database,</strong> совметив строку пароля (начиная с ;p wd= ) с константой в аргументе &quot; &quot; <em>locale,</em> как по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="9bdbe-126">You can also create a password for the new <strong>Database</strong> object by concatenating the password string (starting with &quot;;pwd=&quot; ) with a constant in the <em>locale</em> argument, like this:</span></span></p></li>
<li><p><span data-ttu-id="9bdbe-127">dbLangSpanish &amp; &quot; ;p wd=NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="9bdbe-127">dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="9bdbe-128">Если вы хотите использовать стандарт <em>по</em>умолчанию, но указать пароль, просто введите строку пароля для <em>аргумента locale:</em></span><span class="sxs-lookup"><span data-stu-id="9bdbe-128">If you want to use the default <em>locale</em>, but specify a password, simply enter a password string for the <em>locale</em> argument:</span></span></p></li>
<li><p><span data-ttu-id="9bdbe-129">&quot;;p wd=NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="9bdbe-129">&quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="9bdbe-130">Используйте надежные пароли, содержащие строчные и прописные буквы, цифры и знаки.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-130">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="9bdbe-131">В ненадежных паролях не используются сочетания таких элементов.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-131">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="9bdbe-132">Надежный пароль: Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-132">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="9bdbe-133">Слабый пароль: House27.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-133">Weak password: House27.</span></span> <span data-ttu-id="9bdbe-134">Используйте надежный пароль, который можно запомнить, чтобы не пришлось его записывать.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-134">Use a strong password that you can remember so that you don't have to write it down.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bdbe-135"><em>Option</em></span><span class="sxs-lookup"><span data-stu-id="9bdbe-135"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-136">Необязательный</span><span class="sxs-lookup"><span data-stu-id="9bdbe-136">Optional</span></span></p></td>
<td><p><span data-ttu-id="9bdbe-137"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-137"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-138">Константа или сочетание констант, которое указывает один или несколько параметров, как указано в параметрах.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-138">A constant or combination of constants that indicates one or more options, as specified in Settings.</span></span> <span data-ttu-id="9bdbe-139">Вы можете объединить параметры, сложив соответствующие константы.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-139">You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9bdbe-140">Заметки</span><span class="sxs-lookup"><span data-stu-id="9bdbe-140">Remarks</span></span>

<span data-ttu-id="9bdbe-141">Для аргумента locale можно использовать одну из следующих констант, чтобы указать свойство **[CollatingOrder](database-collatingorder-property-dao.md)** текста для сравнения строк.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-141">You can use one of the following constants for the locale argument to specify the **[CollatingOrder](database-collatingorder-property-dao.md)** property of text for string comparisons.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9bdbe-142">Константа</span><span class="sxs-lookup"><span data-stu-id="9bdbe-142">Constant</span></span></p></th>
<th><p><span data-ttu-id="9bdbe-143">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="9bdbe-143">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9bdbe-144"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-144"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-145">Английский, немецкий, французский, португальский, итальянский и современный испанский</span><span class="sxs-lookup"><span data-stu-id="9bdbe-145">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bdbe-146"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-146"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-147">Арабский</span><span class="sxs-lookup"><span data-stu-id="9bdbe-147">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bdbe-148"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-148"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-149">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="9bdbe-149">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bdbe-150"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-150"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-151">Китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="9bdbe-151">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bdbe-152"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-152"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-153">Русский</span><span class="sxs-lookup"><span data-stu-id="9bdbe-153">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bdbe-154"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-154"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-155">Чешский</span><span class="sxs-lookup"><span data-stu-id="9bdbe-155">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bdbe-156"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-156"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-157">Голландский</span><span class="sxs-lookup"><span data-stu-id="9bdbe-157">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bdbe-158"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-158"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-159">Греческий</span><span class="sxs-lookup"><span data-stu-id="9bdbe-159">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bdbe-160"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-160"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-161">Иврит</span><span class="sxs-lookup"><span data-stu-id="9bdbe-161">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bdbe-162"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-162"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-163">Венгерский</span><span class="sxs-lookup"><span data-stu-id="9bdbe-163">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bdbe-164"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-164"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-165">Исландский</span><span class="sxs-lookup"><span data-stu-id="9bdbe-165">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bdbe-166"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-166"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-167">Японский</span><span class="sxs-lookup"><span data-stu-id="9bdbe-167">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bdbe-168"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-168"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-169">Корейский</span><span class="sxs-lookup"><span data-stu-id="9bdbe-169">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bdbe-170"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-170"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-171">Скандинавские языки (только ядро СУБД Microsoft Jet версии 1.0)</span><span class="sxs-lookup"><span data-stu-id="9bdbe-171">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bdbe-172"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-172"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-173">Норвежский и датский</span><span class="sxs-lookup"><span data-stu-id="9bdbe-173">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bdbe-174"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-174"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-175">Польский</span><span class="sxs-lookup"><span data-stu-id="9bdbe-175">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bdbe-176"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-176"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-177">Словенский</span><span class="sxs-lookup"><span data-stu-id="9bdbe-177">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bdbe-178"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-178"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-179">Традиционный испанский</span><span class="sxs-lookup"><span data-stu-id="9bdbe-179">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bdbe-180"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-180"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-181">Шведский и финский</span><span class="sxs-lookup"><span data-stu-id="9bdbe-181">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bdbe-182"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-182"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-183">Тайский</span><span class="sxs-lookup"><span data-stu-id="9bdbe-183">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bdbe-184"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-184"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-185">Турецкий</span><span class="sxs-lookup"><span data-stu-id="9bdbe-185">Turkish</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9bdbe-186">Вы можете использовать одну или несколько из следующих констант в аргументе options, чтобы указать версию формата данных и нужно ли шифровать базу данных.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-186">You can use one or more of the following constants in the options argument to specify which version the data format should have and whether or not to encrypt the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9bdbe-187">Константа</span><span class="sxs-lookup"><span data-stu-id="9bdbe-187">Constant</span></span></p></th>
<th><p><span data-ttu-id="9bdbe-188">Описание</span><span class="sxs-lookup"><span data-stu-id="9bdbe-188">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9bdbe-189"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-189"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-190">Создает зашифрованную базу данных.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-190">Creates an encrypted database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bdbe-191"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-191"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-192">Создает базу данных, использующую формат файлов яд баз данных Microsoft Jet версии 1.0.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-192">Creates a database that uses the Microsoft Jet database engine version 1.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bdbe-193"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-193"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-194">Создает базу данных, использующую формат файлов ядвижка баз данных Microsoft Jet версии 1.1.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-194">Creates a database that uses the Microsoft Jet database engine version 1.1 file format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bdbe-195"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-195"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-196">Создает базу данных, использующую формат файлов ядвижка баз данных Microsoft Jet версии 2.0.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-196">Creates a database that uses the Microsoft Jet database engine version 2.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bdbe-197"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-197"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-198">Создает базу данных, использующую формат файлов ядвижка базы данных Microsoft Jet версии 3.0 (совместимый с версией 3.5).</span><span class="sxs-lookup"><span data-stu-id="9bdbe-198">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9bdbe-199"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-199"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-200">Создает базу данных, использующую формат файлов ядвижка баз данных Microsoft Jet версии 4.0.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-200">Creates a database that uses the Microsoft Jet database engine version 4.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9bdbe-201"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="9bdbe-201"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="9bdbe-202">Создает базу данных, использующую формат файлов я приложения microsoft Access версии 12.0.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-202">Creates a database that uses the Microsoft Access database engine version 12.0 file format.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9bdbe-203">Если опустить константу шифрования, **CreateDatabase** создаст незашифрованную базу данных.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-203">If you omit the encryption constant, **CreateDatabase** creates an un-encrypted database.</span></span>

<span data-ttu-id="9bdbe-204">Используйте метод **CreateDatabase** для создания и открытия новой пустой базы данных и возврата объекта **Database.**</span><span class="sxs-lookup"><span data-stu-id="9bdbe-204">Use the **CreateDatabase** method to create and open a new, empty database, and return the **Database** object.</span></span> <span data-ttu-id="9bdbe-205">Ее структуру и содержимое необходимо заполнить с помощью дополнительных объектов DAO.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-205">You must complete its structure and content by using additional DAO objects.</span></span> <span data-ttu-id="9bdbe-206">Если вы хотите сделать частичную или полную копию существующей базы данных, можно использовать метод **[CompactDatabase,](dbengine-compactdatabase-method-dao.md)** чтобы сделать копию, которую можно настроить.</span><span class="sxs-lookup"><span data-stu-id="9bdbe-206">If you want to make a partial or complete copy of an existing database, you can use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method to make a copy that you can customize.</span></span>

