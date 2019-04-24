---
title: Метод DBEngine. CreateDatabase (DAO)
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
# <a name="dbenginecreatedatabase-method-dao"></a><span data-ttu-id="cfb35-102">Метод DBEngine. CreateDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="cfb35-102">DBEngine.CreateDatabase method (DAO)</span></span>

<span data-ttu-id="cfb35-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cfb35-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cfb35-104">Создает новый объект **[Database](database-object-dao.md)** , сохраняет базу данных на диске и возвращает открытый объект **базы данных** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="cfb35-104">Creates a new **[Database](database-object-dao.md)** object, saves the database to disk, and returns an opened **Database** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="cfb35-105">.</span><span class="sxs-lookup"><span data-stu-id="cfb35-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="cfb35-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cfb35-106">Syntax</span></span>

<span data-ttu-id="cfb35-107">*Expression* . CreateDatabase (***имя***, ***язык***, ***параметр***)</span><span class="sxs-lookup"><span data-stu-id="cfb35-107">*expression* .CreateDatabase(***Name***, ***Locale***, ***Option***)</span></span>

<span data-ttu-id="cfb35-108">*Expression (выражение* ) Переменная, представляющая объект **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="cfb35-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="cfb35-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cfb35-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cfb35-110">Имя</span><span class="sxs-lookup"><span data-stu-id="cfb35-110">Name</span></span></p></th>
<th><p><span data-ttu-id="cfb35-111">Обязательно/необязательно</span><span class="sxs-lookup"><span data-stu-id="cfb35-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="cfb35-112">Тип данных</span><span class="sxs-lookup"><span data-stu-id="cfb35-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="cfb35-113">Описание</span><span class="sxs-lookup"><span data-stu-id="cfb35-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cfb35-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="cfb35-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="cfb35-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="cfb35-115">Required</span></span></p></td>
<td><p><span data-ttu-id="cfb35-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-117">Строка длиной до 255 символов, которая является именем создаваемого файла базы данных.</span><span class="sxs-lookup"><span data-stu-id="cfb35-117">A String up to 255 characters long that is the name of the database file that you're creating.</span></span> <span data-ttu-id="cfb35-118">Это может быть полный путь и имя файла.</span><span class="sxs-lookup"><span data-stu-id="cfb35-118">It can be the full path and file name.</span></span> <span data-ttu-id="cfb35-119">Если ваша сеть поддерживает эту возможность, можно также указать сетевой путь, например &quot; \\server1\share1\dir1\db1&quot;.</span><span class="sxs-lookup"><span data-stu-id="cfb35-119">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1&quot;.</span></span> <span data-ttu-id="cfb35-120">С помощью этого метода можно создавать только файлы баз данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="cfb35-120">You can only create Microsoft Access database files with this method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfb35-121"><em>Языковой стандарт</em></span><span class="sxs-lookup"><span data-stu-id="cfb35-121"><em>Locale</em></span></span></p></td>
<td><p><span data-ttu-id="cfb35-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="cfb35-122">Required</span></span></p></td>
<td><p><span data-ttu-id="cfb35-123"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-123"><strong>String</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="cfb35-124">Строковое выражение, задающее порядок сортировки для создания базы данных, как указано в параметрах.</span><span class="sxs-lookup"><span data-stu-id="cfb35-124">A string expression that specifies a collating order for creating the database, as specified in Settings.</span></span> <span data-ttu-id="cfb35-125">Необходимо указать этот аргумент, иначе возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="cfb35-125">You must supply this argument or an error occurs.</span></span></p></li>
<li><p><span data-ttu-id="cfb35-126">Кроме того, можно создать пароль для нового объекта <strong>базы данных</strong> , присоединить строку пароля (начиная с &quot;;p WD =&quot; ) с константой в аргументе <em>locale</em> , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="cfb35-126">You can also create a password for the new <strong>Database</strong> object by concatenating the password string (starting with &quot;;pwd=&quot; ) with a constant in the <em>locale</em> argument, like this:</span></span></p></li>
<li><p><span data-ttu-id="cfb35-127">дблангспаниш &amp; &quot;;p wd = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="cfb35-127">dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="cfb35-128">Если вы хотите использовать <em>языковой стандарт</em>по умолчанию, но укажите пароль, просто введите строку пароля для аргумента <em>locale</em> :</span><span class="sxs-lookup"><span data-stu-id="cfb35-128">If you want to use the default <em>locale</em>, but specify a password, simply enter a password string for the <em>locale</em> argument:</span></span></p></li>
<li><p><span data-ttu-id="cfb35-129">&quot;;p WD = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="cfb35-129">&quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="cfb35-130">Используйте надежные пароли, объединяющие прописные и строчные буквы, цифры и символы.</span><span class="sxs-lookup"><span data-stu-id="cfb35-130">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="cfb35-131">В слабых паролях эти элементы не комбинируются.</span><span class="sxs-lookup"><span data-stu-id="cfb35-131">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="cfb35-132">Надежный пароль: Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="cfb35-132">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="cfb35-133">Слабый пароль: House27.</span><span class="sxs-lookup"><span data-stu-id="cfb35-133">Weak password: House27.</span></span> <span data-ttu-id="cfb35-134">Используйте надежный пароль, который можно запомнить, чтобы не записывать его.</span><span class="sxs-lookup"><span data-stu-id="cfb35-134">Use a strong password that you can remember so that you don't have to write it down.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfb35-135"><em>Вариант</em></span><span class="sxs-lookup"><span data-stu-id="cfb35-135"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="cfb35-136">Необязательный</span><span class="sxs-lookup"><span data-stu-id="cfb35-136">Optional</span></span></p></td>
<td><p><span data-ttu-id="cfb35-137"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-137"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-138">Константа или сочетание констант, которые указывают на один или несколько параметров, как указано в параметрах.</span><span class="sxs-lookup"><span data-stu-id="cfb35-138">A constant or combination of constants that indicates one or more options, as specified in Settings.</span></span> <span data-ttu-id="cfb35-139">Вы можете комбинировать параметры, суммируя соответствующие константы.</span><span class="sxs-lookup"><span data-stu-id="cfb35-139">You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="cfb35-140">Замечания</span><span class="sxs-lookup"><span data-stu-id="cfb35-140">Remarks</span></span>

<span data-ttu-id="cfb35-141">Можно использовать одну из следующих констант для аргумента locale, чтобы указать свойство **[коллатингордер](database-collatingorder-property-dao.md)** текста для сравнения строк.</span><span class="sxs-lookup"><span data-stu-id="cfb35-141">You can use one of the following constants for the locale argument to specify the **[CollatingOrder](database-collatingorder-property-dao.md)** property of text for string comparisons.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cfb35-142">Константа</span><span class="sxs-lookup"><span data-stu-id="cfb35-142">Constant</span></span></p></th>
<th><p><span data-ttu-id="cfb35-143">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="cfb35-143">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cfb35-144"><strong>Дблангженерал</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-144"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-145">Английский, немецкий, французский, португальский, итальянский и современная Испанская</span><span class="sxs-lookup"><span data-stu-id="cfb35-145">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfb35-146"><strong>Дблангарабик</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-146"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-147">арабский;</span><span class="sxs-lookup"><span data-stu-id="cfb35-147">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfb35-148"><strong>Дблангчинесесимплифиед</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-148"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-149">китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="cfb35-149">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfb35-150"><strong>Дблангчинесетрадитионал</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-150"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-151">китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="cfb35-151">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfb35-152"><strong>Дблангцириллик</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-152"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-153">русский;</span><span class="sxs-lookup"><span data-stu-id="cfb35-153">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfb35-154"><strong>Дблангкзеч</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-154"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-155">чешский;</span><span class="sxs-lookup"><span data-stu-id="cfb35-155">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfb35-156"><strong>Дблангдутч</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-156"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-157">голландский;</span><span class="sxs-lookup"><span data-stu-id="cfb35-157">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfb35-158"><strong>Дбланггрик</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-158"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-159">греческий;</span><span class="sxs-lookup"><span data-stu-id="cfb35-159">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfb35-160"><strong>Дблангхебрев</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-160"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-161">иврит;</span><span class="sxs-lookup"><span data-stu-id="cfb35-161">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfb35-162"><strong>Дблангхунгариан</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-162"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-163">венгерский;</span><span class="sxs-lookup"><span data-stu-id="cfb35-163">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfb35-164"><strong>Дблангицеландик</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-164"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-165">Исландский</span><span class="sxs-lookup"><span data-stu-id="cfb35-165">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfb35-166"><strong>Дблангжапанесе</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-166"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-167">японский;</span><span class="sxs-lookup"><span data-stu-id="cfb35-167">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfb35-168"><strong>Дблангкореан</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-168"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-169">корейский;</span><span class="sxs-lookup"><span data-stu-id="cfb35-169">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfb35-170"><strong>Дблангнордик</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-170"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-171">Скандинавские языки (только для ядра базы данных Microsoft Jet версии 1,0)</span><span class="sxs-lookup"><span data-stu-id="cfb35-171">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfb35-172"><strong>Дблангнорвдан</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-172"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-173">Норвежский и датский</span><span class="sxs-lookup"><span data-stu-id="cfb35-173">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfb35-174"><strong>Дблангполиш</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-174"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-175">польский;</span><span class="sxs-lookup"><span data-stu-id="cfb35-175">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfb35-176"><strong>Дблангсловениан</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-176"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-177">словенский;</span><span class="sxs-lookup"><span data-stu-id="cfb35-177">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfb35-178"><strong>Дблангспаниш</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-178"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-179">Традиционная испанская</span><span class="sxs-lookup"><span data-stu-id="cfb35-179">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfb35-180"><strong>Дблангсведфин</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-180"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-181">Шведский и финский</span><span class="sxs-lookup"><span data-stu-id="cfb35-181">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfb35-182"><strong>Дблангсаи</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-182"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-183">тайский;</span><span class="sxs-lookup"><span data-stu-id="cfb35-183">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfb35-184"><strong>Дблангтуркиш</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-184"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-185">турецкий;</span><span class="sxs-lookup"><span data-stu-id="cfb35-185">Turkish</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cfb35-186">Можно использовать одну или несколько из приведенных ниже констант в аргументе Options, чтобы указать, какую версию должен иметь формат данных, а также следует ли шифровать базу данных.</span><span class="sxs-lookup"><span data-stu-id="cfb35-186">You can use one or more of the following constants in the options argument to specify which version the data format should have and whether or not to encrypt the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cfb35-187">Константа</span><span class="sxs-lookup"><span data-stu-id="cfb35-187">Constant</span></span></p></th>
<th><p><span data-ttu-id="cfb35-188">Описание</span><span class="sxs-lookup"><span data-stu-id="cfb35-188">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cfb35-189"><strong>Дбенкрипт</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-189"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-190">Создает зашифрованную базу данных.</span><span class="sxs-lookup"><span data-stu-id="cfb35-190">Creates an encrypted database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfb35-191"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-191"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-192">Создает базу данных, в которой используется формат файлов ядра базы данных Microsoft Jet версии 1,0.</span><span class="sxs-lookup"><span data-stu-id="cfb35-192">Creates a database that uses the Microsoft Jet database engine version 1.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfb35-193"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-193"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-194">Создает базу данных, в которой используется формат файлов ядра базы данных Microsoft Jet версии 1,1.</span><span class="sxs-lookup"><span data-stu-id="cfb35-194">Creates a database that uses the Microsoft Jet database engine version 1.1 file format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfb35-195"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-195"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-196">Создает базу данных, в которой используется формат файлов ядра базы данных Microsoft Jet версии 2,0.</span><span class="sxs-lookup"><span data-stu-id="cfb35-196">Creates a database that uses the Microsoft Jet database engine version 2.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfb35-197"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-197"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-198">Создает базу данных, в которой используется формат файлов ядра базы данных Microsoft Jet версии 3,0 (совместимый с версией 3,5).</span><span class="sxs-lookup"><span data-stu-id="cfb35-198">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfb35-199"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-199"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-200">Создает базу данных, в которой используется формат файлов ядра базы данных Microsoft Jet версии 4,0.</span><span class="sxs-lookup"><span data-stu-id="cfb35-200">Creates a database that uses the Microsoft Jet database engine version 4.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfb35-201"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="cfb35-201"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="cfb35-202">Создает базу данных, использующую формат файлов ядра СУБД Microsoft Access версии 12,0.</span><span class="sxs-lookup"><span data-stu-id="cfb35-202">Creates a database that uses the Microsoft Access database engine version 12.0 file format.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cfb35-203">Если опустить константу шифрования, **CreateDatabase** создает незашифрованную базу данных.</span><span class="sxs-lookup"><span data-stu-id="cfb35-203">If you omit the encryption constant, **CreateDatabase** creates an un-encrypted database.</span></span>

<span data-ttu-id="cfb35-204">Используйте метод **CreateDatabase** , чтобы создать и открыть новую пустую базу данных и возвратить объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="cfb35-204">Use the **CreateDatabase** method to create and open a new, empty database, and return the **Database** object.</span></span> <span data-ttu-id="cfb35-205">Для выполнения структуры и контента необходимо использовать дополнительные объекты DAO.</span><span class="sxs-lookup"><span data-stu-id="cfb35-205">You must complete its structure and content by using additional DAO objects.</span></span> <span data-ttu-id="cfb35-206">Если вы хотите создать частичную или полную копию существующей базы данных, можно использовать метод **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** , чтобы создать копию, которую можно настроить.</span><span class="sxs-lookup"><span data-stu-id="cfb35-206">If you want to make a partial or complete copy of an existing database, you can use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method to make a copy that you can customize.</span></span>

