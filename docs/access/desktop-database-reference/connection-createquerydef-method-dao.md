---
title: Метод Connection.CreateQueryDef (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 254fe81a-9b45-e8e7-108d-503c1c1c0fcc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191860(v=office.15)
ms:contentKeyID: 48543781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053067
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a03f486d29aa70c7d4901372f81609e378ffae07
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950057"
---
# <a name="connectioncreatequerydef-method-dao"></a>Метод Connection.CreateQueryDef (DAO)

**Применимо к**: Access 2013, Office 2013

Создает новый объект **[QueryDef](querydef-object-dao.md)** .

## <a name="syntax"></a>Синтаксис

*выражение* . CreateQueryDef (***имя***, ***SQLText***)

*выражение* Переменная, которая содержит объект **подключения** .

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
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (<strong>String</strong> подтип), уникальным образом новые <strong>QueryDef</strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>SQLText</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (<strong>String</strong> подтип), которая является инструкцией SQL, определение <strong>QueryDef</strong>. Если опустить аргумент, можно определить <strong>QueryDef</strong> путем установки свойства <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> до или после добавления его в коллекцию.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

QueryDef

## <a name="remarks"></a>Примечания

В рабочей области Microsoft Access Если вы укажите отличное от строку нулевой длины имени при создании **QueryDef**результирующего объекта **QueryDef** автоматически добавляется к коллекции **[QueryDefs](querydefs-collection-dao.md)** .

Если объектом, заданным с именем уже должна быть членом **QueryDefs** коллекции, возникает ошибка времени выполнения. Временные **QueryDef** можно создать с помощью строку нулевой длины для аргумента имени, при выполнении метода **CreateQueryDef** . Это также можно сделать, задав свойство **[Name](connection-name-property-dao.md)** только что созданный **QueryDef** в строку нулевой длины (»»). Временные объекты **QueryDef** полезны, если требуется повторно использовать динамические инструкции SQL, не создавая для создания новых постоянных объектов в коллекции **QueryDefs** . Временные **QueryDef** невозможно добавить в любой коллекции, так как строку нулевой длины не является допустимым именем для постоянного объекта **QueryDef** . Всегда можно задать **имя** и свойства **SQL** объекта **QueryDef** только что созданный и затем добавьте **QueryDef** в коллекцию **QueryDefs** .

Чтобы запустить инструкции SQL в объект **QueryDef** , используйте метод **[Execute](connection-execute-method-dao.md)** или **[OpenRecordset](connection-openrecordset-method-dao.md)** .

С помощью объекта **QueryDef** является предпочтительным для выполнения запросов к серверу с использованием баз данных ODBC.

Для удаления объекта **QueryDef** из коллекции **QueryDefs** в базе данных ядра базы данных Microsoft Access, используйте метод **[Delete](fields-delete-method-dao.md)** в семействе сайтов.

