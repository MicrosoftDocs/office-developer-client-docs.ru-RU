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
# <a name="dbenginecreatedatabase-method-dao"></a>Метод DBEngine.CreateDatabase (DAO)

**Область применения**: Access 2013, Office 2013

Создает новый объект **[Database,](database-object-dao.md)** сохраняет базу данных на диск и возвращает открытый объект **Database** (только рабочие пространства Microsoft Access). .

## <a name="syntax"></a>Синтаксис

*выражения* . CreateDatabase(Имя, ***Локализ***, ***Параметр***)

*expression*: переменная, представляющая объект **DBEngine**.

## <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Строка длиной до 255 символов — это имя создаемого файла базы данных. Это может быть полный путь и имя файла. Если сеть поддерживает ее, можно также указать сетевой путь, например &quot; \\ server1\share1\dir1\db1. &quot; С помощью этого метода можно создавать только файлы базы данных Microsoft Access.</p></td>
</tr>
<tr class="even">
<td><p><em>Locale</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><ul>
<li><p>Строка, указывающий порядок создания базы данных, как указано в Параметры. Необходимо предоставить этот аргумент или возникает ошибка.</p></li>
<li><p>Вы также можете создать пароль для нового объекта <strong>Database,</strong> соединив строку пароля (начиная с ;p wd=) с константой в аргументе &quot; &quot; <em>locale,</em> как это:</p></li>
<li><p>dbLangSpanish &amp; &quot; ;p wd=NewPassword&quot;</p></li>
<li><p>Если вы хотите использовать локализ по <em>умолчанию,</em>но укажите пароль, просто введите строку пароля для <em>аргумента locale:</em></p></li>
<li><p>&quot;;p wd=NewPassword&quot;</p></li>
<li><p>Используйте надежные пароли, содержащие строчные и прописные буквы, цифры и знаки. В ненадежных паролях не используются сочетания таких элементов. Надежный пароль: Y6dh!et5. Слабый пароль: House27. Используйте надежный пароль, который можно запомнить, чтобы не пришлось его записывать.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><em>Option</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа или сочетание констант, которые указывают один или несколько параметров, как указано в Параметры. Вы можете объединить параметры, сложив соответствующие константы.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Для аргумента locale можно использовать одну из следующих констант, чтобы указать свойство **[CollatingOrder](database-collatingorder-property-dao.md)** текста для сравнения строк.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Порядок сортировки</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbLangGeneral</strong></p></td>
<td><p>Английский, немецкий, французский, португальский, итальянский и современный испанский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangArabic</strong></p></td>
<td><p>Арабский</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangChineseSimplified</strong></p></td>
<td><p>Китайский (упрощенное письмо)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangChineseTraditional</strong></p></td>
<td><p>Китайский (традиционное письмо)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangCyrillic</strong></p></td>
<td><p>Русский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangCzech</strong></p></td>
<td><p>Чешский</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangDutch</strong></p></td>
<td><p>Голландский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangGreek</strong></p></td>
<td><p>Греческий</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangHebrew</strong></p></td>
<td><p>Иврит</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangHungarian</strong></p></td>
<td><p>Венгерский</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangIcelandic</strong></p></td>
<td><p>Исландский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangJapanese</strong></p></td>
<td><p>Японский</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangKorean</strong></p></td>
<td><p>Корейский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangNordic</strong></p></td>
<td><p>Скандинавские языки (только ядро СУБД Microsoft Jet версии 1.0)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangNorwDan</strong></p></td>
<td><p>Норвежский и датский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangPolish</strong></p></td>
<td><p>Польский</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangSlovenian</strong></p></td>
<td><p>Словенский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangSpanish</strong></p></td>
<td><p>Традиционный испанский</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangSwedFin</strong></p></td>
<td><p>Шведский и финский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangThai</strong></p></td>
<td><p>Тайский</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangTurkish</strong></p></td>
<td><p>Турецкий</p></td>
</tr>
</tbody>
</table>


В аргументе параметров можно использовать одну или несколько следующих констант, чтобы указать, какая версия должна иметь формат данных и следует ли шифровать базу данных.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbEncrypt</strong></p></td>
<td><p>Создает зашифрованную базу данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion10</strong></p></td>
<td><p>Создает базу данных, использующую формат файла версии 1.0 для двигателя базы данных Microsoft Jet.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion11</strong></p></td>
<td><p>Создает базу данных с использованием формата файловой версии 1.1 базы данных Microsoft Jet.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion20</strong></p></td>
<td><p>Создает базу данных, использующую формат файла версии 2.0 для базы данных Microsoft Jet.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion30</strong></p></td>
<td><p>Создает базу данных, использующую файловый формат 3.0 версии базы данных Microsoft Jet (совместим с версией 3.5).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion40</strong></p></td>
<td><p>Создает базу данных, использующую формат файловой базы данных Microsoft Jet версии 4.0.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion120</strong></p></td>
<td><p>Создает базу данных, использующую формат файла версии 12.0 для базы данных Microsoft Access.</p></td>
</tr>
</tbody>
</table>


Если опустить константу шифрования, **CreateDatabase** создаст нешифроварованную базу данных.

Используйте метод **CreateDatabase** для создания и открытия новой пустой базы данных и возврата объекта **Database.** Необходимо завершить его структуру и контент с помощью дополнительных объектов DAO. Если вы хотите сделать частичную или полную копию существующей базы данных, вы можете использовать метод **[CompactDatabase,](dbengine-compactdatabase-method-dao.md)** чтобы сделать копию, которую можно настроить.

