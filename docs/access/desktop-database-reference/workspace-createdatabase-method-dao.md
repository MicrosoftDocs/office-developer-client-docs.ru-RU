---
title: Метод Workspace.CreateDatabase (DAO)
TOCTitle: CreateDatabase Method
ms:assetid: c0ad986e-3b4d-f781-f782-5aa3cdccea7d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822832(v=office.15)
ms:contentKeyID: 48547514
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5774eb4c9965cad7679d37754fd9a1f431ddaa48
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923415"
---
# <a name="workspacecreatedatabase-method-dao"></a><span data-ttu-id="b89e2-102">Метод Workspace.CreateDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="b89e2-102">Workspace.CreateDatabase method (DAO)</span></span>


<span data-ttu-id="b89e2-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b89e2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b89e2-104">Создает новый объект **[базы данных](database-object-dao.md)** , сохраняет базы данных на диск и возвращает объект открыт **базы данных** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="b89e2-104">Creates a new **[Database](database-object-dao.md)** object, saves the database to disk, and returns an opened **Database** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="b89e2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b89e2-105">Syntax</span></span>

<span data-ttu-id="b89e2-106">*выражение* . CreateDatabase (***имя***, ***подключение***, ***вариант***)</span><span class="sxs-lookup"><span data-stu-id="b89e2-106">*expression* .CreateDatabase(***Name***, ***Connect***, ***Option***)</span></span>

<span data-ttu-id="b89e2-107">*выражение* Переменная, которая представляет собой объект- **рабочей области** .</span><span class="sxs-lookup"><span data-stu-id="b89e2-107">*expression* A variable that represents a **Workspace** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="b89e2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b89e2-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b89e2-109">Имя</span><span class="sxs-lookup"><span data-stu-id="b89e2-109">Name</span></span></p></th>
<th><p><span data-ttu-id="b89e2-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="b89e2-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="b89e2-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b89e2-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="b89e2-112">Описание</span><span class="sxs-lookup"><span data-stu-id="b89e2-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b89e2-113">Имя</span><span class="sxs-lookup"><span data-stu-id="b89e2-113">Name</span></span></p></td>
<td><p><span data-ttu-id="b89e2-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b89e2-114">Required</span></span></p></td>
<td><p><span data-ttu-id="b89e2-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-116">Строка длиной до 255 знаков, — это имя файла базы данных, который вы создаете.</span><span class="sxs-lookup"><span data-stu-id="b89e2-116">A String up to 255 characters long that is the name of the database file that you're creating.</span></span> <span data-ttu-id="b89e2-117">Это может быть полный путь и имя файла.</span><span class="sxs-lookup"><span data-stu-id="b89e2-117">It can be the full path and file name.</span></span> <span data-ttu-id="b89e2-118">Если сеть поддерживает его, можно также указать сетевой путь, таких как &quot; \\server1\share1\dir1\db1&quot;.</span><span class="sxs-lookup"><span data-stu-id="b89e2-118">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1&quot;.</span></span> <span data-ttu-id="b89e2-119">Файлы базы данных Microsoft Access можно создать только с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="b89e2-119">You can only create Microsoft Access database files with this method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b89e2-120">Подключение</span><span class="sxs-lookup"><span data-stu-id="b89e2-120">Connect</span></span></p></td>
<td><p><span data-ttu-id="b89e2-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b89e2-121">Required</span></span></p></td>
<td><p><span data-ttu-id="b89e2-122"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-122"><strong>String</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="b89e2-123">Строковое выражение, которое определяет порядок сортировки при создании базы данных, как указано в настройки.</span><span class="sxs-lookup"><span data-stu-id="b89e2-123">A string expression that specifies a collating order for creating the database, as specified in Settings.</span></span> <span data-ttu-id="b89e2-124">Необходимо указать этот аргумент или возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="b89e2-124">You must supply this argument or an error occurs.</span></span></p></li>
<li><p><span data-ttu-id="b89e2-125">Можно также создать пароль для нового объекта <strong>базы данных</strong> , объединив Строка пароля (начиная с &quot;; pwd =&quot;) с константой в аргументе <em>языкового стандарта</em> , следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b89e2-125">You can also create a password for the new <strong>Database</strong> object by concatenating the password string (starting with &quot;;pwd=&quot;) with a constant in the <em>locale</em> argument, like this:</span></span></p></li>
<li><p><span data-ttu-id="b89e2-126">dbLangSpanish &amp; &quot;; pwd = Новый_пароль&quot;</span><span class="sxs-lookup"><span data-stu-id="b89e2-126">dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="b89e2-127">Если вы хотите использовать по умолчанию для <em>языкового стандарта</em>, но укажите пароль, просто введите строку пароль для аргумента <em>языкового стандарта</em> :</span><span class="sxs-lookup"><span data-stu-id="b89e2-127">If you want to use the default <em>locale</em>, but specify a password, simply enter a password string for the <em>locale</em> argument:</span></span></p></li>
<li><p><span data-ttu-id="b89e2-128">&quot;; pwd = Новый_пароль&quot;</span><span class="sxs-lookup"><span data-stu-id="b89e2-128">&quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="b89e2-129">Используйте надежные пароли, содержащие верхний и строчные буквы, числа и символы.</span><span class="sxs-lookup"><span data-stu-id="b89e2-129">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="b89e2-130">Ненадежные пароли не смешивайте этих элементов.</span><span class="sxs-lookup"><span data-stu-id="b89e2-130">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="b89e2-131">Надежный пароль: Y6dh! et5.</span><span class="sxs-lookup"><span data-stu-id="b89e2-131">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="b89e2-132">Ненадежный пароль: House27.</span><span class="sxs-lookup"><span data-stu-id="b89e2-132">Weak password: House27.</span></span> <span data-ttu-id="b89e2-133">Используйте надежный пароль, который вы можете запомнить, чтобы записать его не нужно.</span><span class="sxs-lookup"><span data-stu-id="b89e2-133">Use a strong password that you can remember so that you don't have to write it down.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b89e2-134">Параметр</span><span class="sxs-lookup"><span data-stu-id="b89e2-134">Option</span></span></p></td>
<td><p><span data-ttu-id="b89e2-135">Необязательный</span><span class="sxs-lookup"><span data-stu-id="b89e2-135">Optional</span></span></p></td>
<td><p><span data-ttu-id="b89e2-136"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-136"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-137">Константа или сочетание констант, которое указывает один или несколько параметров, как указано в настройки.</span><span class="sxs-lookup"><span data-stu-id="b89e2-137">A constant or combination of constants that indicates one or more options, as specified in Settings.</span></span> <span data-ttu-id="b89e2-138">Параметры можно использовать суммируются соответствующий констант.</span><span class="sxs-lookup"><span data-stu-id="b89e2-138">You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b89e2-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="b89e2-139">Remarks</span></span>

<span data-ttu-id="b89e2-140">Можно использовать один из следующих константы для аргумента языковой стандарт для указания свойства [CollatingOrder](database-collatingorder-property-dao.md) текста для сравнения строк.</span><span class="sxs-lookup"><span data-stu-id="b89e2-140">You can use one of the following constants for the locale argument to specify the [CollatingOrder](database-collatingorder-property-dao.md) property of text for string comparisons.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b89e2-141">Constant</span><span class="sxs-lookup"><span data-stu-id="b89e2-141">Constant</span></span></p></th>
<th><p><span data-ttu-id="b89e2-142">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="b89e2-142">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b89e2-143"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-143"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-144">Английский, немецкий, французский, португальский, итальянский и современных испанский</span><span class="sxs-lookup"><span data-stu-id="b89e2-144">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b89e2-145"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-145"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-146">арабский;</span><span class="sxs-lookup"><span data-stu-id="b89e2-146">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b89e2-147"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-147"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-148">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="b89e2-148">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b89e2-149"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-149"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-150">Китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="b89e2-150">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b89e2-151"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-151"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-152">русский;</span><span class="sxs-lookup"><span data-stu-id="b89e2-152">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b89e2-153"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-153"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-154">чешский;</span><span class="sxs-lookup"><span data-stu-id="b89e2-154">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b89e2-155"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-155"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-156">голландский;</span><span class="sxs-lookup"><span data-stu-id="b89e2-156">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b89e2-157"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-157"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-158">греческий;</span><span class="sxs-lookup"><span data-stu-id="b89e2-158">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b89e2-159"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-159"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-160">иврит;</span><span class="sxs-lookup"><span data-stu-id="b89e2-160">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b89e2-161"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-161"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-162">венгерский;</span><span class="sxs-lookup"><span data-stu-id="b89e2-162">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b89e2-163"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-163"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-164">Исландский</span><span class="sxs-lookup"><span data-stu-id="b89e2-164">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b89e2-165"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-165"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-166">японский;</span><span class="sxs-lookup"><span data-stu-id="b89e2-166">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b89e2-167"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-167"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-168">корейский;</span><span class="sxs-lookup"><span data-stu-id="b89e2-168">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b89e2-169"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-169"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-170">Скандинавские языки (ядра Microsoft Jet базы данных версии 1.0 только)</span><span class="sxs-lookup"><span data-stu-id="b89e2-170">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b89e2-171"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-171"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-172">Датский и норвежский</span><span class="sxs-lookup"><span data-stu-id="b89e2-172">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b89e2-173"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-173"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-174">польский;</span><span class="sxs-lookup"><span data-stu-id="b89e2-174">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b89e2-175"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-175"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-176">словенский;</span><span class="sxs-lookup"><span data-stu-id="b89e2-176">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b89e2-177"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-177"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-178">Испанский (традиционный)</span><span class="sxs-lookup"><span data-stu-id="b89e2-178">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b89e2-179"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-179"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-180">Финский и шведский</span><span class="sxs-lookup"><span data-stu-id="b89e2-180">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b89e2-181"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-181"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-182">тайский;</span><span class="sxs-lookup"><span data-stu-id="b89e2-182">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b89e2-183"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-183"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-184">турецкий;</span><span class="sxs-lookup"><span data-stu-id="b89e2-184">Turkish</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b89e2-185">Одно или несколько из следующих констант в аргументе параметры можно использовать для указания версии должен иметь формат данных и ли шифрование базы данных.</span><span class="sxs-lookup"><span data-stu-id="b89e2-185">You can use one or more of the following constants in the options argument to specify which version the data format should have and whether or not to encrypt the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b89e2-186">Константа</span><span class="sxs-lookup"><span data-stu-id="b89e2-186">Constant</span></span></p></th>
<th><p><span data-ttu-id="b89e2-187">Описание</span><span class="sxs-lookup"><span data-stu-id="b89e2-187">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b89e2-188"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-188"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-189">Создает зашифрованной базе данных.</span><span class="sxs-lookup"><span data-stu-id="b89e2-189">Creates an encrypted database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b89e2-190"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-190"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-191">Создает базу данных в формате Microsoft Jet база данных модуля версии 1.0 файла.</span><span class="sxs-lookup"><span data-stu-id="b89e2-191">Creates a database that uses the Microsoft Jet database engine version 1.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b89e2-192"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-192"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-193">Создает базу данных в формате Microsoft Jet база данных модуля версии 1.1 файла.</span><span class="sxs-lookup"><span data-stu-id="b89e2-193">Creates a database that uses the Microsoft Jet database engine version 1.1 file format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b89e2-194"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-194"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-195">Создает базу данных в формате Microsoft Jet база данных модуля версии 2.0 файла.</span><span class="sxs-lookup"><span data-stu-id="b89e2-195">Creates a database that uses the Microsoft Jet database engine version 2.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b89e2-196"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-196"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-197">Создает базу данных, который использует Microsoft Jet engine версии 3.0 формате файла базы данных (совместимый с версией 3.5).</span><span class="sxs-lookup"><span data-stu-id="b89e2-197">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b89e2-198"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-198"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-199">Создает базу данных в формате Microsoft Jet база данных модуля версии 4.0 файл.</span><span class="sxs-lookup"><span data-stu-id="b89e2-199">Creates a database that uses the Microsoft Jet database engine version 4.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b89e2-200"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="b89e2-200"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="b89e2-201">Создает базу данных в формате Microsoft Access базы данных модуля версии 12.0 файла.</span><span class="sxs-lookup"><span data-stu-id="b89e2-201">Creates a database that uses the Microsoft Access database engine version 12.0 file format.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b89e2-202">Если опустить константу шифрования **CreateDatabase** создает без зашифрованной базе данных.</span><span class="sxs-lookup"><span data-stu-id="b89e2-202">If you omit the encryption constant, **CreateDatabase** creates an un-encrypted database.</span></span>

<span data-ttu-id="b89e2-203">Используйте метод **CreateDatabase** Создание и открытие новой пустой базы данных и возвращают объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="b89e2-203">Use the **CreateDatabase** method to create and open a new, empty database, and return the **Database** object.</span></span> <span data-ttu-id="b89e2-204">С помощью дополнительных объектов DAO необходимо выполнить его структуру и содержимое.</span><span class="sxs-lookup"><span data-stu-id="b89e2-204">You must complete its structure and content by using additional DAO objects.</span></span> <span data-ttu-id="b89e2-205">Если вы хотите создать частичного или полного копию существующей базы данных, можно использовать метод **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** для копирования, можно настроить.</span><span class="sxs-lookup"><span data-stu-id="b89e2-205">If you want to make a partial or complete copy of an existing database, you can use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method to make a copy that you can customize.</span></span>

## <a name="example"></a><span data-ttu-id="b89e2-206">Пример</span><span class="sxs-lookup"><span data-stu-id="b89e2-206">Example</span></span>

<span data-ttu-id="b89e2-207">В этом примере используется **CreateDatabase** для создания нового, зашифрованные объекта **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="b89e2-207">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

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
