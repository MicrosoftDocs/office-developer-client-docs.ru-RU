---
title: TableDef.Connect Property (DAO)
TOCTitle: Connect Property
ms:assetid: 4fbb324c-a358-8fad-60f2-fb8005cf74d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193791(v=office.15)
ms:contentKeyID: 48544782
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053064
f1_categories:
- Office.Version=v15
ms.openlocfilehash: eaedb53c8cb70746229e3f311ba5925e3b30ddef
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481611"
---
# <a name="tabledefconnect-property-dao"></a>TableDef.Connect Property (DAO)


**Применимо к**: Access 2013 | Office 2013

Задает или возвращает значение, которое предоставляет сведения о связанной таблицы. Для чтения и записи, **String**.

## <a name="syntax"></a>Синтаксис

*выражение* . Подключение

*выражение* Переменная, которая представляет собой объект- **TableDef** .

## <a name="remarks"></a>Замечания

Настройка свойства **подключение** — **строка** состоит из спецификатора типа базы данных и ноль или больше параметров, разделенных точкой с запятой. Свойство **Connect** передает Дополнительные сведения о ODBC и драйверы некоторых ISAM при необходимости.

Для объекта **TableDef** , представляющий связанной таблицы значение свойства **подключение** состоит из одного или двух частях (описатель типа базы данных и путь к базе данных), каждая из которых заканчиваются точкой с запятой.

Путь, как показано в следующей таблице — это полный путь к каталогу, содержащему файлы базы данных и должен предшествовать идентификатор базы данных =. В некоторых случаях (как с помощью Microsoft Excel и Microsoft Access базы данных базами данных, ядро) должен включать имя файла в качестве аргумента базы данных.

Ниже приведены возможные типы и баз данных и их соответствующие спецификаторы базы данных пути для настройки свойства **подключения** .

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Тип базы данных</p></th>
<th><p>Описателя</p></th>
<th><p>Пример</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Базы данных Microsoft Access</p></td>
<td><p>База данных [];</p></td>
<td><p>диск: \path\filename</p></td>
</tr>
<tr class="even">
<td><p>dBASE III</p></td>
<td><p>dBASE III;</p></td>
<td><p>диск: \path</p></td>
</tr>
<tr class="odd">
<td><p>dBASE IV</p></td>
<td><p>dBASE IV;</p></td>
<td><p>диск: \path</p></td>
</tr>
<tr class="even">
<td><p>dBASE 5</p></td>
<td><p>dBASE 5.0;</p></td>
<td><p>диск: \path</p></td>
</tr>
<tr class="odd">
<td><p>Paradox 3.x</p></td>
<td><p>Paradox 3.x;</p></td>
<td><p>диск: \path</p></td>
</tr>
<tr class="even">
<td><p>Paradox 4.x</p></td>
<td><p>Paradox 4.x;</p></td>
<td><p>диск: \path</p></td>
</tr>
<tr class="odd">
<td><p>Paradox 5.x</p></td>
<td><p>Paradox 5.x;</p></td>
<td><p>диск: \path</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Excel 3.0</p></td>
<td><p>Excel 3.0;</p></td>
<td><p>Drive:\path\filename.xls</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel 4.0</p></td>
<td><p>Excel 4.0;</p></td>
<td><p>Drive:\path\filename.xls</p></td>
</tr>
<tr class="even">
<td><p>Microsoft Excel 5.0 или Microsoft Excel 95</p></td>
<td><p>Excel 5.0;</p></td>
<td><p>Drive:\path\filename.xls</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Excel 97</p></td>
<td><p>Excel 8.0;</p></td>
<td><p>Drive:\path\filename.xls</p></td>
</tr>
<tr class="even">
<td><p>Lotus 1-2-3 WKS и WK1</p></td>
<td><p>Lotus WK1;</p></td>
<td><p>Drive:\path\filename.WK1</p></td>
</tr>
<tr class="odd">
<td><p>WK3 Lotus 1-2-3</p></td>
<td><p>Lotus WK3;</p></td>
<td><p>Drive:\path\filename.WK3</p></td>
</tr>
<tr class="even">
<td><p>WK4 Lotus 1-2-3</p></td>
<td><p>Lotus WK4;</p></td>
<td><p>Drive:\path\filename.WK4</p></td>
</tr>
<tr class="odd">
<td><p>Импорт HTML</p></td>
<td><p>Импорт HTML;</p></td>
<td><p>диск: \path\filename</p></td>
</tr>
<tr class="even">
<td><p>Экспорт HTML</p></td>
<td><p>Экспорт HTML;</p></td>
<td><p>диск: \path</p></td>
</tr>
<tr class="odd">
<td><p>Текст</p></td>
<td><p>Текст;</p></td>
<td><p>диск: \path</p></td>
</tr>
<tr class="even">
<td><p>Open Database Connectivity</p></td>
<td><p>ODBC. Базы данных = база данных; UID = пользователя; PWD = пароля; Уведомления о Доставке = источнику данных; [LOGINTIMEOUT = секунды;]</p></td>
<td><p>Отсутствует</p></td>
</tr>
<tr class="odd">
<td><p>Microsoft Exchange</p></td>
<td><p>Exchange 4.0; MAPILEVEL = folderpath; [TABLETYPE = {0 | 1}]; [ПРОФИЛЕЙ = профиля;] [PWD = пароль;] [Базы данных = база данных;]</p></td>
<td><p>диск: \path\filename</p></td>
</tr>
</tbody>
</table>


Если пароль требуется, но не указан в параметре свойства **подключения** , диалоговое окно входа в систему отображается впервые таблицам драйвер ODBC и снова закрыто и повторно открыть подключение.

Для данных в Microsoft Exchange требуется ключ MAPILEVEL должно быть присвоено полностью разрешить пути (например, «почтовый ящик – Pat SmithIAlpha/текущую»). Путь не включает имя папки, которая будет открыта в виде таблицы; Вместо этого следует указать имя этой папки в качестве аргумента имя метода **CreateTable** . Клавиша TABLETYPE должно быть присвоено значение «0» откройте папку (по умолчанию) или «1», чтобы открыть адресную книгу. В настоящее время с помощью ключа ПРОФИЛЯ по умолчанию к профилю.

Для базовых таблиц в базе данных Micorosoft Access значение свойства **подключение** является строкой нулевой длины (»»).


> [!NOTE]
> <UL>
> <LI>
> <P>Необходимо установить свойство <STRONG>подключение</STRONG> , прежде чем задать свойство <STRONG>ReturnsRecords</STRONG> .</P>
> <LI>
> <P>Необходимо иметь разрешения доступа на компьютере, где размещается сервер базы данных, который вы пытаетесь получить доступ к.</P></LI></UL>


