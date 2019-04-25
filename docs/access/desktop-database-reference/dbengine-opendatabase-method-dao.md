---
title: Метод DBEngine.OpenDatabase (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: 49fca321-5955-3e69-64ea-da191536eadb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193474(v=office.15)
ms:contentKeyID: 48544654
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052979
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 1cd4188931999284a6454064a0906b64cf1f519a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294255"
---
# <a name="dbengineopendatabase-method-dao"></a>Метод DBEngine.OpenDatabase (DAO)

**Область применения**: Access 2013, Office 2013

Открывает указанную базу данных и возвращает ссылку на объект **[Database](database-object-dao.md)**, который ее представляет.

## <a name="syntax"></a>Синтаксис

*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)

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
<td><p>Имя существующего файла базы данных Microsoft Access или имя источника данных (DSN) для источника данных ODBC. См. свойство <strong> <a href="connection-name-property-dao.md">Name</a> </strong> для получения дополнительной информации о настройке данного значения.</p></td>
</tr>
<tr class="even">
<td><p><em>Options</em></p></td>
<td><p>Необязательно</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Определяет различные опции для базы данных, согласно данным в Комментариях.</p></td>
</tr>
<tr class="odd">
<td><p><em>ReadOnly</em></p></td>
<td><p>Необязательно устанавливать.</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Установите значение <strong>True</strong>, если вы хотите открыть базу данных с правами доступа только для чтения, или <strong>False</strong> (установлено по умолчанию), если вы хотите открыть базу данных с правами доступа на чтение и запись.</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>Необязательно заполнять.</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Определяет различные сведения о подключении, включая пароли.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

База данных

## <a name="remarks"></a>Комментарии

Вы можете использовать следующие значения для аргумента Options.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Параметр</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>True</strong></p></td>
<td><p>Открытие базы данных в монопольном режиме.</p></td>
</tr>
<tr class="even">
<td><p><strong>False</strong></p></td>
<td><p>(По умолчанию) Открытие базы данных в режиме совместного доступа.</p></td>
</tr>
</tbody>
</table>


Когда вы открываете базу данных, она автоматически добавляется коллекцию **Databases**.

Несколько советов в отношении применения dbname:

- Если он ссылается на базу данных, которая уже открыта для доступа другому пользователю, возникает ошибка.

- Если он не ссылается на существующую базу данных или допустимое имя источника данных ODBC, возникает ошибка.

- Если он является строкой нулевой длины (""), а для *connect* установлено значение "ODBC;", откроется диалоговое окно со списком всех зарегистрированных имен источник данных ODBC, где пользователь может выбрать базу данных.

Чтобы закрыть базу данных, а значит удалить объект **Database** из коллекции **Databases**, используйте метод **[Close](connection-close-method-dao.md)** для объекта.

> [!NOTE]
> При обращении к источнику данных ODBC, подключенного к ядру СУБД Microsoft Access вы можете повысить производительность вашего приложения, открыв объект **Database**, связанный с источником данных ODBC, не прибегая к связыванию отдельных объектов [TableDef](tabledef-object-dao.md) с определенными таблицами источника данных ODBC.


