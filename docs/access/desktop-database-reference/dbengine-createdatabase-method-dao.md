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
# <a name="dbenginecreatedatabase-method-dao"></a>Метод DBEngine. CreateDatabase (DAO)

**Область применения**: Access 2013, Office 2013

Создает новый объект **[Database](database-object-dao.md)** , сохраняет базу данных на диске и возвращает открытый объект **базы данных** (только для рабочих областей Microsoft Access). .

## <a name="syntax"></a>Синтаксис

*Expression* . CreateDatabase (***имя***, ***язык***, ***параметр***)

*Expression (выражение* ) Переменная, представляющая объект **DBEngine** .

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
<th><p>Обязательно/необязательно</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Строка длиной до 255 символов, которая является именем создаваемого файла базы данных. Это может быть полный путь и имя файла. Если ваша сеть поддерживает эту возможность, можно также указать сетевой путь, например &quot; \\server1\share1\dir1\db1&quot;. С помощью этого метода можно создавать только файлы баз данных Microsoft Access.</p></td>
</tr>
<tr class="even">
<td><p><em>Языковой стандарт</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><ul>
<li><p>Строковое выражение, задающее порядок сортировки для создания базы данных, как указано в параметрах. Необходимо указать этот аргумент, иначе возникнет ошибка.</p></li>
<li><p>Кроме того, можно создать пароль для нового объекта <strong>базы данных</strong> , присоединить строку пароля (начиная с &quot;;p WD =&quot; ) с константой в аргументе <em>locale</em> , как показано ниже.</p></li>
<li><p>дблангспаниш &amp; &quot;;p wd = NewPassword&quot;</p></li>
<li><p>Если вы хотите использовать <em>языковой стандарт</em>по умолчанию, но укажите пароль, просто введите строку пароля для аргумента <em>locale</em> :</p></li>
<li><p>&quot;;p WD = NewPassword&quot;</p></li>
<li><p>Используйте надежные пароли, объединяющие прописные и строчные буквы, цифры и символы. В слабых паролях эти элементы не комбинируются. Надежный пароль: Y6dh!et5. Слабый пароль: House27. Используйте надежный пароль, который можно запомнить, чтобы не записывать его.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><em>Вариант</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа или сочетание констант, которые указывают на один или несколько параметров, как указано в параметрах. Вы можете комбинировать параметры, суммируя соответствующие константы.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Можно использовать одну из следующих констант для аргумента locale, чтобы указать свойство **[коллатингордер](database-collatingorder-property-dao.md)** текста для сравнения строк.

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
<td><p><strong>Дблангженерал</strong></p></td>
<td><p>Английский, немецкий, французский, португальский, итальянский и современная Испанская</p></td>
</tr>
<tr class="even">
<td><p><strong>Дблангарабик</strong></p></td>
<td><p>арабский;</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дблангчинесесимплифиед</strong></p></td>
<td><p>китайский (упрощенное письмо)</p></td>
</tr>
<tr class="even">
<td><p><strong>Дблангчинесетрадитионал</strong></p></td>
<td><p>китайский (традиционное письмо)</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дблангцириллик</strong></p></td>
<td><p>русский;</p></td>
</tr>
<tr class="even">
<td><p><strong>Дблангкзеч</strong></p></td>
<td><p>чешский;</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дблангдутч</strong></p></td>
<td><p>голландский;</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбланггрик</strong></p></td>
<td><p>греческий;</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дблангхебрев</strong></p></td>
<td><p>иврит;</p></td>
</tr>
<tr class="even">
<td><p><strong>Дблангхунгариан</strong></p></td>
<td><p>венгерский;</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дблангицеландик</strong></p></td>
<td><p>Исландский</p></td>
</tr>
<tr class="even">
<td><p><strong>Дблангжапанесе</strong></p></td>
<td><p>японский;</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дблангкореан</strong></p></td>
<td><p>корейский;</p></td>
</tr>
<tr class="even">
<td><p><strong>Дблангнордик</strong></p></td>
<td><p>Скандинавские языки (только для ядра базы данных Microsoft Jet версии 1,0)</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дблангнорвдан</strong></p></td>
<td><p>Норвежский и датский</p></td>
</tr>
<tr class="even">
<td><p><strong>Дблангполиш</strong></p></td>
<td><p>польский;</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дблангсловениан</strong></p></td>
<td><p>словенский;</p></td>
</tr>
<tr class="even">
<td><p><strong>Дблангспаниш</strong></p></td>
<td><p>Традиционная испанская</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дблангсведфин</strong></p></td>
<td><p>Шведский и финский</p></td>
</tr>
<tr class="even">
<td><p><strong>Дблангсаи</strong></p></td>
<td><p>тайский;</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дблангтуркиш</strong></p></td>
<td><p>турецкий;</p></td>
</tr>
</tbody>
</table>


Можно использовать одну или несколько из приведенных ниже констант в аргументе Options, чтобы указать, какую версию должен иметь формат данных, а также следует ли шифровать базу данных.

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
<td><p><strong>Дбенкрипт</strong></p></td>
<td><p>Создает зашифрованную базу данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion10</strong></p></td>
<td><p>Создает базу данных, в которой используется формат файлов ядра базы данных Microsoft Jet версии 1,0.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion11</strong></p></td>
<td><p>Создает базу данных, в которой используется формат файлов ядра базы данных Microsoft Jet версии 1,1.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion20</strong></p></td>
<td><p>Создает базу данных, в которой используется формат файлов ядра базы данных Microsoft Jet версии 2,0.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion30</strong></p></td>
<td><p>Создает базу данных, в которой используется формат файлов ядра базы данных Microsoft Jet версии 3,0 (совместимый с версией 3,5).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion40</strong></p></td>
<td><p>Создает базу данных, в которой используется формат файлов ядра базы данных Microsoft Jet версии 4,0.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion120</strong></p></td>
<td><p>Создает базу данных, использующую формат файлов ядра СУБД Microsoft Access версии 12,0.</p></td>
</tr>
</tbody>
</table>


Если опустить константу шифрования, **CreateDatabase** создает незашифрованную базу данных.

Используйте метод **CreateDatabase** , чтобы создать и открыть новую пустую базу данных и возвратить объект **базы данных** . Для выполнения структуры и контента необходимо использовать дополнительные объекты DAO. Если вы хотите создать частичную или полную копию существующей базы данных, можно использовать метод **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** , чтобы создать копию, которую можно настроить.

