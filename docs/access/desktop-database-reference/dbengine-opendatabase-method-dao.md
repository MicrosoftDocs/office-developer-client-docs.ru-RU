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
ms.openlocfilehash: eb3f6795ba2e64ebd6be1b04d6aa6aecccef781b
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950092"
---
# <a name="dbengineopendatabase-method-dao"></a>Метод DBEngine.OpenDatabase (DAO)

**Применимо к**: Access 2013, Office 2013

Открывает указанной базы данных и возвращает ссылку на объект **[базы данных](database-object-dao.md)** , который представляет его.

## <a name="syntax"></a>Синтаксис

*выражение* . OpenDatabase (***имя***, ***Параметры***, ***только для чтения***, ***подключение***)

*выражение* Переменная, которая представляет собой объект- **DBEngine** .

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
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>имя существующего файла базы данных Microsoft Access или данных источника имя источника данных ODBC (DSN). Просмотрите Дополнительные сведения о настройке это значение свойства <strong><a href="connection-name-property-dao.md">Name</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><em>Варианты</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Задает различные параметры для базы данных, как указано в разделе Примечания.</p></td>
</tr>
<tr class="odd">
<td><p><em>Только для чтения</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Значение true,</strong> Если вы хотите откройте базу данных с доступом только для чтения, или <strong>значение False</strong> (по умолчанию), чтобы открыть базу данных с помощью доступ на чтение и запись.</p></td>
</tr>
<tr class="even">
<td><p><em>Подключение</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Указывает различные сведения о подключении, включая пароли.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

База данных

## <a name="remarks"></a>Примечания

Можно использовать следующие значения для аргумента options.

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
<td><p>Открывает базу данных в монопольном режиме.</p></td>
</tr>
<tr class="even">
<td><p><strong>False</strong></p></td>
<td><p>(По умолчанию) Открывает базу данных в режиме общего доступа.</p></td>
</tr>
</tbody>
</table>


При открытии базы данных, автоматически добавляется в коллекцию **баз данных** .

Некоторые соображения при использовании dbname.

- Если речь идет об базы данных, который уже открыт для доступа к другим пользователем, возникает ошибка.

- Если он не ссылается на существующую базу данных или допустимое имя источника данных ODBC, возникает ошибка.

- Если он является строкой нулевой длины ("») и *подключение* — «ODBC;», отображается диалоговое окно со списком всех зарегистрированных имен источников данных ODBC, которой пользователь может выбрать базу данных.

Чтобы закрыть базу данных и таким образом удаления объекта **базы данных** из коллекции **баз данных** , используйте метод **[Close](connection-close-method-dao.md)** объекта.

> [!NOTE]
> При получении доступа к Microsoft Access базы данных подключен модуль ODBC источника данных, можно увеличить производительность вашего приложения, открыв объекта **базы данных** , подключенных к источнику данных ODBC, а не путем связывания отдельных объектов [TableDef](tabledef-object-dao.md) в определенных в источнике данных ODBC.


