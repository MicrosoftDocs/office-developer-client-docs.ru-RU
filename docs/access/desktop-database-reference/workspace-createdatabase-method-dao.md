---
title: Workspace.CreateDatabase Method (DAO)
TOCTitle: CreateDatabase Method
ms:assetid: c0ad986e-3b4d-f781-f782-5aa3cdccea7d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822832(v=office.15)
ms:contentKeyID: 48547514
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2ad3d44d67efb240cb97a5b4716e9e00a6951045
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875625"
---
# <a name="workspacecreatedatabase-method-dao"></a><span data-ttu-id="b0ecf-102">Workspace.CreateDatabase Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="b0ecf-102">Workspace.CreateDatabase Method (DAO)</span></span>


<span data-ttu-id="b0ecf-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0ecf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0ecf-104">Создает новый объект **[базы данных](database-object-dao.md)** , сохраняет базы данных на диск и возвращает объект открыт **базы данных** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="b0ecf-104">Creates a new **[Database](database-object-dao.md)** object, saves the database to disk, and returns an opened **Database** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="b0ecf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0ecf-105">Syntax</span></span>

<span data-ttu-id="b0ecf-106">*выражение* . CreateDatabase (***имя***, ***подключение***, ***вариант***)</span><span class="sxs-lookup"><span data-stu-id="b0ecf-106">*expression* .CreateDatabase(***Name***, ***Connect***, ***Option***)</span></span>

<span data-ttu-id="b0ecf-107">*выражение* Переменная, которая представляет собой объект- **рабочей области** .</span><span class="sxs-lookup"><span data-stu-id="b0ecf-107">*expression* A variable that represents a **Workspace** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="b0ecf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0ecf-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0ecf-109">Имя</span><span class="sxs-lookup"><span data-stu-id="b0ecf-109">Name</span></span></p></th>
<th><p><span data-ttu-id="b0ecf-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="b0ecf-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="b0ecf-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b0ecf-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="b0ecf-112">Описание</span><span class="sxs-lookup"><span data-stu-id="b0ecf-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0ecf-113">Имя</span><span class="sxs-lookup"><span data-stu-id="b0ecf-113">Name</span></span></p></td>
<td><p><span data-ttu-id="b0ecf-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b0ecf-114">Required</span></span></p></td>
<td><p><span data-ttu-id="b0ecf-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-116">Строка длиной до 255 знаков, — это имя файла базы данных, который вы создаете.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-116">A String up to 255 characters long that is the name of the database file that you're creating.</span></span> <span data-ttu-id="b0ecf-117">Это может быть полный путь и имя файла.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-117">It can be the full path and file name.</span></span> <span data-ttu-id="b0ecf-118">Если сеть поддерживает его, можно также указать сетевой путь, таких как &quot; \\server1\share1\dir1\db1&quot;.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-118">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1&quot;.</span></span> <span data-ttu-id="b0ecf-119">Файлы базы данных Microsoft Access можно создать только с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-119">You can only create Microsoft Access database files with this method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0ecf-120">Подключение</span><span class="sxs-lookup"><span data-stu-id="b0ecf-120">Connect</span></span></p></td>
<td><p><span data-ttu-id="b0ecf-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b0ecf-121">Required</span></span></p></td>
<td><p><span data-ttu-id="b0ecf-122"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-122"><strong>String</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="b0ecf-123">Строковое выражение, которое определяет порядок сортировки при создании базы данных, как указано в настройки.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-123">A string expression that specifies a collating order for creating the database, as specified in Settings.</span></span> <span data-ttu-id="b0ecf-124">Необходимо указать этот аргумент или возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-124">You must supply this argument or an error occurs.</span></span></p></li>
<li><p><span data-ttu-id="b0ecf-125">Можно также создать пароль для нового объекта <strong>базы данных</strong> , объединив Строка пароля (начиная с &quot;; pwd =&quot;) с константой в аргументе <em>языкового стандарта</em> , следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b0ecf-125">You can also create a password for the new <strong>Database</strong> object by concatenating the password string (starting with &quot;;pwd=&quot;) with a constant in the <em>locale</em> argument, like this:</span></span></p></li>
<li><p><span data-ttu-id="b0ecf-126">dbLangSpanish &amp; &quot;; pwd = Новый_пароль&quot;</span><span class="sxs-lookup"><span data-stu-id="b0ecf-126">dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="b0ecf-127">Если вы хотите использовать по умолчанию для <em>языкового стандарта</em>, но укажите пароль, просто введите строку пароль для аргумента <em>языкового стандарта</em> :</span><span class="sxs-lookup"><span data-stu-id="b0ecf-127">If you want to use the default <em>locale</em>, but specify a password, simply enter a password string for the <em>locale</em> argument:</span></span></p></li>
<li><p><span data-ttu-id="b0ecf-128">&quot;; pwd = Новый_пароль&quot;</span><span class="sxs-lookup"><span data-stu-id="b0ecf-128">&quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="b0ecf-129">Используйте надежные пароли, содержащие верхний и строчные буквы, числа и символы.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-129">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="b0ecf-130">Ненадежные пароли не смешивайте этих элементов.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-130">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="b0ecf-131">Надежный пароль: Y6dh! et5.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-131">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="b0ecf-132">Ненадежный пароль: House27.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-132">Weak password: House27.</span></span> <span data-ttu-id="b0ecf-133">Используйте надежный пароль, который вы можете запомнить, чтобы записать его не нужно.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-133">Use a strong password that you can remember so that you don't have to write it down.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0ecf-134">Параметр</span><span class="sxs-lookup"><span data-stu-id="b0ecf-134">Option</span></span></p></td>
<td><p><span data-ttu-id="b0ecf-135">Необязательный</span><span class="sxs-lookup"><span data-stu-id="b0ecf-135">Optional</span></span></p></td>
<td><p><span data-ttu-id="b0ecf-136"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-136"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-137">Константа или сочетание констант, которое указывает один или несколько параметров, как указано в настройки.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-137">A constant or combination of constants that indicates one or more options, as specified in Settings.</span></span> <span data-ttu-id="b0ecf-138">Параметры можно использовать суммируются соответствующий констант.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-138">You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b0ecf-139">Замечания</span><span class="sxs-lookup"><span data-stu-id="b0ecf-139">Remarks</span></span>

<span data-ttu-id="b0ecf-140">Можно использовать один из следующих константы для аргумента языковой стандарт для указания свойства [CollatingOrder](database-collatingorder-property-dao.md) текста для сравнения строк.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-140">You can use one of the following constants for the locale argument to specify the [CollatingOrder](database-collatingorder-property-dao.md) property of text for string comparisons.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0ecf-141">Constant</span><span class="sxs-lookup"><span data-stu-id="b0ecf-141">Constant</span></span></p></th>
<th><p><span data-ttu-id="b0ecf-142">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="b0ecf-142">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0ecf-143"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-143"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-144">Английский, немецкий, французский, португальский, итальянский и современных испанский</span><span class="sxs-lookup"><span data-stu-id="b0ecf-144">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0ecf-145"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-145"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-146">арабский;</span><span class="sxs-lookup"><span data-stu-id="b0ecf-146">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0ecf-147"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-147"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-148">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="b0ecf-148">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0ecf-149"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-149"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-150">Китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="b0ecf-150">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0ecf-151"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-151"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-152">русский;</span><span class="sxs-lookup"><span data-stu-id="b0ecf-152">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0ecf-153"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-153"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-154">чешский;</span><span class="sxs-lookup"><span data-stu-id="b0ecf-154">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0ecf-155"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-155"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-156">голландский;</span><span class="sxs-lookup"><span data-stu-id="b0ecf-156">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0ecf-157"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-157"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-158">греческий;</span><span class="sxs-lookup"><span data-stu-id="b0ecf-158">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0ecf-159"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-159"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-160">иврит;</span><span class="sxs-lookup"><span data-stu-id="b0ecf-160">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0ecf-161"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-161"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-162">венгерский;</span><span class="sxs-lookup"><span data-stu-id="b0ecf-162">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0ecf-163"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-163"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-164">Исландский</span><span class="sxs-lookup"><span data-stu-id="b0ecf-164">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0ecf-165"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-165"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-166">японский;</span><span class="sxs-lookup"><span data-stu-id="b0ecf-166">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0ecf-167"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-167"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-168">корейский;</span><span class="sxs-lookup"><span data-stu-id="b0ecf-168">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0ecf-169"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-169"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-170">Скандинавские языки (ядра Microsoft Jet базы данных версии 1.0 только)</span><span class="sxs-lookup"><span data-stu-id="b0ecf-170">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0ecf-171"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-171"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-172">Датский и норвежский</span><span class="sxs-lookup"><span data-stu-id="b0ecf-172">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0ecf-173"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-173"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-174">польский;</span><span class="sxs-lookup"><span data-stu-id="b0ecf-174">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0ecf-175"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-175"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-176">словенский;</span><span class="sxs-lookup"><span data-stu-id="b0ecf-176">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0ecf-177"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-177"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-178">Испанский (традиционный)</span><span class="sxs-lookup"><span data-stu-id="b0ecf-178">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0ecf-179"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-179"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-180">Финский и шведский</span><span class="sxs-lookup"><span data-stu-id="b0ecf-180">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0ecf-181"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-181"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-182">тайский;</span><span class="sxs-lookup"><span data-stu-id="b0ecf-182">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0ecf-183"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-183"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-184">турецкий;</span><span class="sxs-lookup"><span data-stu-id="b0ecf-184">Turkish</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b0ecf-185">Одно или несколько из следующих констант в аргументе параметры можно использовать для указания версии должен иметь формат данных и ли шифрование базы данных.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-185">You can use one or more of the following constants in the options argument to specify which version the data format should have and whether or not to encrypt the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0ecf-186">Константа</span><span class="sxs-lookup"><span data-stu-id="b0ecf-186">Constant</span></span></p></th>
<th><p><span data-ttu-id="b0ecf-187">Описание</span><span class="sxs-lookup"><span data-stu-id="b0ecf-187">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0ecf-188"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-188"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-189">Создает зашифрованной базе данных.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-189">Creates an encrypted database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0ecf-190"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-190"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-191">Создает базу данных в формате Microsoft Jet база данных модуля версии 1.0 файла.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-191">Creates a database that uses the Microsoft Jet database engine version 1.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0ecf-192"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-192"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-193">Создает базу данных в формате Microsoft Jet база данных модуля версии 1.1 файла.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-193">Creates a database that uses the Microsoft Jet database engine version 1.1 file format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0ecf-194"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-194"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-195">Создает базу данных в формате Microsoft Jet база данных модуля версии 2.0 файла.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-195">Creates a database that uses the Microsoft Jet database engine version 2.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0ecf-196"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-196"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-197">Создает базу данных, который использует Microsoft Jet engine версии 3.0 формате файла базы данных (совместимый с версией 3.5).</span><span class="sxs-lookup"><span data-stu-id="b0ecf-197">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0ecf-198"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-198"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-199">Создает базу данных в формате Microsoft Jet база данных модуля версии 4.0 файл.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-199">Creates a database that uses the Microsoft Jet database engine version 4.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0ecf-200"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="b0ecf-200"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="b0ecf-201">Создает базу данных в формате Microsoft Access базы данных модуля версии 12.0 файла.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-201">Creates a database that uses the Microsoft Access database engine version 12.0 file format.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b0ecf-202">Если опустить константу шифрования **CreateDatabase** создает без зашифрованной базе данных.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-202">If you omit the encryption constant, **CreateDatabase** creates an un-encrypted database.</span></span>

<span data-ttu-id="b0ecf-203">Используйте метод **CreateDatabase** Создание и открытие новой пустой базы данных и возвращают объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="b0ecf-203">Use the **CreateDatabase** method to create and open a new, empty database, and return the **Database** object.</span></span> <span data-ttu-id="b0ecf-204">С помощью дополнительных объектов DAO необходимо выполнить его структуру и содержимое.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-204">You must complete its structure and content by using additional DAO objects.</span></span> <span data-ttu-id="b0ecf-205">Если вы хотите создать частичного или полного копию существующей базы данных, можно использовать метод **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** для копирования, можно настроить.</span><span class="sxs-lookup"><span data-stu-id="b0ecf-205">If you want to make a partial or complete copy of an existing database, you can use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method to make a copy that you can customize.</span></span>

## <a name="example"></a><span data-ttu-id="b0ecf-206">Пример</span><span class="sxs-lookup"><span data-stu-id="b0ecf-206">Example</span></span>

<span data-ttu-id="b0ecf-207">В этом примере используется **CreateDatabase** для создания нового, зашифрованные объекта **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="b0ecf-207">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

```vb
    Sub CreateDatabaseX() 
     
       Dim wrkDefault As Workspace 
       Dim dbsNew As DATABASE 
       Dim prpLoop As Property 
     
       ' Get default Workspace. 
       Set wrkDefault = DBEngine.Workspaces(0) 
     
       ' Make sure there isn't already a file with the name of  
       ' the new database. 
       If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
     
       ' Create a new encrypted database with the specified  
       ' collating order. 
       Set dbsNew = wrkDefault.CreateDatabase("NewDB.mdb", _ 
          dbLangGeneral, dbEncrypt) 
     
       With dbsNew 
          Debug.Print "Properties of " & .Name 
          ' Enumerate the Properties collection of the new  
          ' Database object. 
          For Each prpLoop In .Properties 
             If prpLoop <> "" Then Debug.Print "  " & _ 
                prpLoop.Name & " = " & prpLoop 
          Next prpLoop 
       End With 
     
       dbsNew.Close 
     
    End Sub
```
