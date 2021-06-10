---
title: Метод Workspace.CreateDatabase (DAO)
TOCTitle: CreateDatabase Method
ms:assetid: c0ad986e-3b4d-f781-f782-5aa3cdccea7d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822832(v=office.15)
ms:contentKeyID: 48547514
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e6d271676ef91d29dca78ba9ee4b6142e055b36d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305868"
---
# <a name="workspacecreatedatabase-method-dao"></a><span data-ttu-id="12518-102">Метод Workspace.CreateDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="12518-102">Workspace.CreateDatabase method (DAO)</span></span>

<span data-ttu-id="12518-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="12518-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="12518-104">Создает новый объект **[Database,](database-object-dao.md)** сохраняет базу данных на диск и возвращает открытый объект **Database** (только рабочие пространства Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="12518-104">Creates a new **[Database](database-object-dao.md)** object, saves the database to disk, and returns an opened **Database** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="12518-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12518-105">Syntax</span></span>

<span data-ttu-id="12518-106">*выражения* . CreateDatabase(Имя , ***Подключение***, ***Параметр***)</span><span class="sxs-lookup"><span data-stu-id="12518-106">*expression* .CreateDatabase(***Name***, ***Connect***, ***Option***)</span></span>

<span data-ttu-id="12518-107">*expression*: переменная, представляющая объект **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="12518-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="12518-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="12518-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="12518-109">Имя</span><span class="sxs-lookup"><span data-stu-id="12518-109">Name</span></span></p></th>
<th><p><span data-ttu-id="12518-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="12518-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="12518-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="12518-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="12518-112">Описание</span><span class="sxs-lookup"><span data-stu-id="12518-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12518-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="12518-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="12518-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="12518-114">Required</span></span></p></td>
<td><p><span data-ttu-id="12518-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="12518-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-116">Строка длиной до 255 символов — это имя создаемого файла базы данных.</span><span class="sxs-lookup"><span data-stu-id="12518-116">A String up to 255 characters long that is the name of the database file that you're creating.</span></span> <span data-ttu-id="12518-117">Это может быть полный путь и имя файла.</span><span class="sxs-lookup"><span data-stu-id="12518-117">It can be the full path and file name.</span></span> <span data-ttu-id="12518-118">Если сеть поддерживает ее, можно также указать сетевой путь, например &quot; \\ server1\share1\dir1\db1. &quot;</span><span class="sxs-lookup"><span data-stu-id="12518-118">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1&quot;.</span></span> <span data-ttu-id="12518-119">С помощью этого метода можно создавать только файлы базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="12518-119">You can only create Microsoft Access database files with this method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12518-120"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="12518-120"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="12518-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="12518-121">Required</span></span></p></td>
<td><p><span data-ttu-id="12518-122"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="12518-122"><strong>String</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="12518-123">Строка, указывающий порядок создания базы данных, как указано в Параметры.</span><span class="sxs-lookup"><span data-stu-id="12518-123">A string expression that specifies a collating order for creating the database, as specified in Settings.</span></span> <span data-ttu-id="12518-124">Необходимо предоставить этот аргумент или возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="12518-124">You must supply this argument or an error occurs.</span></span></p></li>
<li><p><span data-ttu-id="12518-125">Вы также можете создать пароль для нового объекта <strong>Database,</strong> соединив строку пароля (начиная с ;p wd=) с константой в аргументе &quot; &quot; <em>locale,</em> как это:</span><span class="sxs-lookup"><span data-stu-id="12518-125">You can also create a password for the new <strong>Database</strong> object by concatenating the password string (starting with &quot;;pwd=&quot;) with a constant in the <em>locale</em> argument, like this:</span></span></p></li>
<li><p><span data-ttu-id="12518-126">dbLangSpanish &amp; &quot; ;p wd=NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="12518-126">dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="12518-127">Если вы хотите использовать локализ по <em>умолчанию,</em>но укажите пароль, просто введите строку пароля для <em>аргумента locale:</em></span><span class="sxs-lookup"><span data-stu-id="12518-127">If you want to use the default <em>locale</em>, but specify a password, simply enter a password string for the <em>locale</em> argument:</span></span></p></li>
<li><p><span data-ttu-id="12518-128">&quot;;p wd=NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="12518-128">&quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="12518-129">Используйте надежные пароли, содержащие строчные и прописные буквы, цифры и знаки.</span><span class="sxs-lookup"><span data-stu-id="12518-129">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="12518-130">В ненадежных паролях не используются сочетания таких элементов.</span><span class="sxs-lookup"><span data-stu-id="12518-130">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="12518-131">Надежный пароль: Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="12518-131">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="12518-132">Слабый пароль: House27.</span><span class="sxs-lookup"><span data-stu-id="12518-132">Weak password: House27.</span></span> <span data-ttu-id="12518-133">Используйте надежный пароль, который можно запомнить, чтобы не пришлось его записывать.</span><span class="sxs-lookup"><span data-stu-id="12518-133">Use a strong password that you can remember so that you don't have to write it down.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12518-134"><em>Option</em></span><span class="sxs-lookup"><span data-stu-id="12518-134"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="12518-135">Необязательный</span><span class="sxs-lookup"><span data-stu-id="12518-135">Optional</span></span></p></td>
<td><p><span data-ttu-id="12518-136"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="12518-136"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-137">Константа или сочетание констант, которые указывают один или несколько параметров, как указано в Параметры.</span><span class="sxs-lookup"><span data-stu-id="12518-137">A constant or combination of constants that indicates one or more options, as specified in Settings.</span></span> <span data-ttu-id="12518-138">Вы можете объединить параметры, сложив соответствующие константы.</span><span class="sxs-lookup"><span data-stu-id="12518-138">You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="12518-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="12518-139">Remarks</span></span>

<span data-ttu-id="12518-140">Для аргумента locale можно использовать одну из следующих констант, чтобы указать свойство [CollatingOrder](database-collatingorder-property-dao.md) текста для сравнения строк.</span><span class="sxs-lookup"><span data-stu-id="12518-140">You can use one of the following constants for the locale argument to specify the [CollatingOrder](database-collatingorder-property-dao.md) property of text for string comparisons.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="12518-141">Константа</span><span class="sxs-lookup"><span data-stu-id="12518-141">Constant</span></span></p></th>
<th><p><span data-ttu-id="12518-142">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="12518-142">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12518-143"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="12518-143"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-144">Английский, немецкий, французский, португальский, итальянский и современный испанский</span><span class="sxs-lookup"><span data-stu-id="12518-144">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12518-145"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="12518-145"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-146">Арабский</span><span class="sxs-lookup"><span data-stu-id="12518-146">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12518-147"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="12518-147"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-148">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="12518-148">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12518-149"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="12518-149"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-150">Китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="12518-150">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12518-151"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="12518-151"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-152">Русский</span><span class="sxs-lookup"><span data-stu-id="12518-152">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12518-153"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="12518-153"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-154">Чешский</span><span class="sxs-lookup"><span data-stu-id="12518-154">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12518-155"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="12518-155"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-156">Голландский</span><span class="sxs-lookup"><span data-stu-id="12518-156">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12518-157"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="12518-157"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-158">Греческий</span><span class="sxs-lookup"><span data-stu-id="12518-158">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12518-159"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="12518-159"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-160">Иврит</span><span class="sxs-lookup"><span data-stu-id="12518-160">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12518-161"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="12518-161"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-162">Венгерский</span><span class="sxs-lookup"><span data-stu-id="12518-162">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12518-163"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="12518-163"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-164">Исландский</span><span class="sxs-lookup"><span data-stu-id="12518-164">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12518-165"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="12518-165"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-166">Японский</span><span class="sxs-lookup"><span data-stu-id="12518-166">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12518-167"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="12518-167"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-168">Корейский</span><span class="sxs-lookup"><span data-stu-id="12518-168">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12518-169"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="12518-169"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-170">Скандинавские языки (только ядро СУБД Microsoft Jet версии 1.0)</span><span class="sxs-lookup"><span data-stu-id="12518-170">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12518-171"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="12518-171"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-172">Норвежский и датский</span><span class="sxs-lookup"><span data-stu-id="12518-172">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12518-173"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="12518-173"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-174">Польский</span><span class="sxs-lookup"><span data-stu-id="12518-174">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12518-175"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="12518-175"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-176">Словенский</span><span class="sxs-lookup"><span data-stu-id="12518-176">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12518-177"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="12518-177"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-178">Традиционный испанский</span><span class="sxs-lookup"><span data-stu-id="12518-178">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12518-179"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="12518-179"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-180">Шведский и финский</span><span class="sxs-lookup"><span data-stu-id="12518-180">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12518-181"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="12518-181"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-182">Тайский</span><span class="sxs-lookup"><span data-stu-id="12518-182">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12518-183"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="12518-183"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-184">Турецкий</span><span class="sxs-lookup"><span data-stu-id="12518-184">Turkish</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="12518-185">В аргументе параметров можно использовать одну или несколько следующих констант, чтобы указать, какая версия должна иметь формат данных и следует ли шифровать базу данных.</span><span class="sxs-lookup"><span data-stu-id="12518-185">You can use one or more of the following constants in the options argument to specify which version the data format should have and whether or not to encrypt the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="12518-186">Константа</span><span class="sxs-lookup"><span data-stu-id="12518-186">Constant</span></span></p></th>
<th><p><span data-ttu-id="12518-187">Описание</span><span class="sxs-lookup"><span data-stu-id="12518-187">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12518-188"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="12518-188"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-189">Создает зашифрованную базу данных.</span><span class="sxs-lookup"><span data-stu-id="12518-189">Creates an encrypted database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12518-190"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="12518-190"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-191">Создает базу данных, использующую формат файла версии 1.0 для двигателя базы данных Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="12518-191">Creates a database that uses the Microsoft Jet database engine version 1.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12518-192"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="12518-192"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-193">Создает базу данных с использованием формата файловой версии 1.1 базы данных Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="12518-193">Creates a database that uses the Microsoft Jet database engine version 1.1 file format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12518-194"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="12518-194"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-195">Создает базу данных, использующую формат файла версии 2.0 для базы данных Microsoft Jet.</span><span class="sxs-lookup"><span data-stu-id="12518-195">Creates a database that uses the Microsoft Jet database engine version 2.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12518-196"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="12518-196"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-197">Создает базу данных, использующую файловый формат 3.0 версии базы данных Microsoft Jet (совместим с версией 3.5).</span><span class="sxs-lookup"><span data-stu-id="12518-197">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12518-198"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="12518-198"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-199">Создает базу данных, использующую формат файловой базы данных Microsoft Jet версии 4.0.</span><span class="sxs-lookup"><span data-stu-id="12518-199">Creates a database that uses the Microsoft Jet database engine version 4.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12518-200"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="12518-200"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="12518-201">Создает базу данных, использующую формат файла версии 12.0 для базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="12518-201">Creates a database that uses the Microsoft Access database engine version 12.0 file format.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="12518-202">Если опустить константу шифрования, **CreateDatabase** создаст нешифроварованную базу данных.</span><span class="sxs-lookup"><span data-stu-id="12518-202">If you omit the encryption constant, **CreateDatabase** creates an un-encrypted database.</span></span>

<span data-ttu-id="12518-203">Используйте метод **CreateDatabase** для создания и открытия новой пустой базы данных и возврата объекта **Database.**</span><span class="sxs-lookup"><span data-stu-id="12518-203">Use the **CreateDatabase** method to create and open a new, empty database, and return the **Database** object.</span></span> <span data-ttu-id="12518-204">Необходимо завершить его структуру и контент с помощью дополнительных объектов DAO.</span><span class="sxs-lookup"><span data-stu-id="12518-204">You must complete its structure and content by using additional DAO objects.</span></span> <span data-ttu-id="12518-205">Если вы хотите сделать частичную или полную копию существующей базы данных, вы можете использовать метод **[CompactDatabase,](dbengine-compactdatabase-method-dao.md)** чтобы сделать копию, которую можно настроить.</span><span class="sxs-lookup"><span data-stu-id="12518-205">If you want to make a partial or complete copy of an existing database, you can use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method to make a copy that you can customize.</span></span>

## <a name="example"></a><span data-ttu-id="12518-206">Пример</span><span class="sxs-lookup"><span data-stu-id="12518-206">Example</span></span>

<span data-ttu-id="12518-207">В этом примере используется метод **CreateDatabase** для создания нового зашифрованного объекта **Database**.</span><span class="sxs-lookup"><span data-stu-id="12518-207">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

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
