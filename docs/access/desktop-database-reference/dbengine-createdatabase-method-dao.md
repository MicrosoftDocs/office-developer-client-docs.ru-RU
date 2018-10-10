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
ms.openlocfilehash: f1f47e403b1b1c61bb766d28be05558f28dba8f1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480781"
---
# <a name="dbenginecreatedatabase-method-dao"></a>DBEngine.CreateDatabase Method (DAO)


**Применимо к**: Access 2013 | Office 2013

Создает новый объект **[базы данных](database-object-dao.md)** , сохраняет базы данных на диск и возвращает объект открыт **базы данных** (только для рабочих областей Microsoft Access). .

## <a name="syntax"></a>Синтаксис

*выражение* . CreateDatabase (***имя***, ***языкового стандарта*** ***параметр***)

*выражение* Переменная, которая представляет собой объект- **DBEngine** .

### <a name="parameters"></a>Параметры

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
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Имя</p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>Строка длиной до 255 знаков, — это имя файла базы данных, который вы создаете. Это может быть полный путь и имя файла. Если сеть поддерживает его, можно также указать сетевой путь, таких как &quot; \\server1\share1\dir1\db1&quot;. Файлы базы данных Microsoft Access можно создать только с помощью этого метода.</p></td>
</tr>
<tr class="even">
<td><p>Locale</p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><ul>
<li><p>Строковое выражение, которое определяет порядок сортировки при создании базы данных, как указано в настройки. Необходимо указать этот аргумент или возникает ошибка.</p></li>
<li><p>Можно также создать пароль для нового объекта <strong>базы данных</strong> , объединив Строка пароля (начиная с &quot;; pwd =&quot; ) с константой в аргументе <em>языкового стандарта</em> , следующим образом:</p></li>
<li><p>dbLangSpanish &amp; &quot;; pwd = Новый_пароль&quot;</p></li>
<li><p>Если вы хотите использовать по умолчанию для <em>языкового стандарта</em>, но укажите пароль, просто введите строку пароль для аргумента <em>языкового стандарта</em> :</p></li>
<li><p>&quot;; pwd = Новый_пароль&quot;</p></li>
<li><p>Используйте надежные пароли, содержащие верхний и строчные буквы, числа и символы. Ненадежные пароли не смешивайте этих элементов. Надежный пароль: Y6dh! et5. Ненадежный пароль: House27. Используйте надежный пароль, который вы можете запомнить, чтобы записать его не нужно.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>Параметр</p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа или сочетание констант, которое указывает один или несколько параметров, как указано в настройки. Параметры можно использовать суммируются соответствующий констант.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Можно использовать один из следующих константы для аргумента языковой стандарт для указания свойства **[CollatingOrder](database-collatingorder-property-dao.md)** текста для сравнения строк.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Порядок сортировки</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbLangGeneral</strong></p></td>
<td><p>Английский, немецкий, французский, португальский, итальянский и современных испанский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangArabic</strong></p></td>
<td><p>арабский;</p></td>
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
<td><p>русский;</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangCzech</strong></p></td>
<td><p>чешский;</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangDutch</strong></p></td>
<td><p>голландский;</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangGreek</strong></p></td>
<td><p>греческий;</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangHebrew</strong></p></td>
<td><p>иврит;</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangHungarian</strong></p></td>
<td><p>венгерский;</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangIcelandic</strong></p></td>
<td><p>Исландский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangJapanese</strong></p></td>
<td><p>японский;</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangKorean</strong></p></td>
<td><p>корейский;</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangNordic</strong></p></td>
<td><p>Скандинавские языки (ядра Microsoft Jet базы данных версии 1.0 только)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangNorwDan</strong></p></td>
<td><p>Датский и норвежский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangPolish</strong></p></td>
<td><p>польский;</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangSlovenian</strong></p></td>
<td><p>словенский;</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangSpanish</strong></p></td>
<td><p>Испанский (традиционный)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangSwedFin</strong></p></td>
<td><p>Финский и шведский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangThai</strong></p></td>
<td><p>тайский;</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangTurkish</strong></p></td>
<td><p>турецкий;</p></td>
</tr>
</tbody>
</table>


Одно или несколько из следующих констант в аргументе параметры можно использовать для указания версии должен иметь формат данных и ли шифрование базы данных.

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
<td><p>Создает зашифрованной базе данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion10</strong></p></td>
<td><p>Создает базу данных в формате Microsoft Jet база данных модуля версии 1.0 файла.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion11</strong></p></td>
<td><p>Создает базу данных в формате Microsoft Jet база данных модуля версии 1.1 файла.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion20</strong></p></td>
<td><p>Создает базу данных в формате Microsoft Jet база данных модуля версии 2.0 файла.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion30</strong></p></td>
<td><p>Создает базу данных, который использует Microsoft Jet engine версии 3.0 формате файла базы данных (совместимый с версией 3.5).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion40</strong></p></td>
<td><p>Создает базу данных в формате Microsoft Jet база данных модуля версии 4.0 файл.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion120</strong></p></td>
<td><p>Создает базу данных в формате Microsoft Access базы данных модуля версии 12.0 файла.</p></td>
</tr>
</tbody>
</table>


Если опустить константу шифрования **CreateDatabase** создает без зашифрованной базе данных.

Используйте метод **CreateDatabase** Создание и открытие новой пустой базы данных и возвращают объект **базы данных** . С помощью дополнительных объектов DAO необходимо выполнить его структуру и содержимое. Если вы хотите создать частичного или полного копию существующей базы данных, можно использовать метод **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** для копирования, можно настроить.

