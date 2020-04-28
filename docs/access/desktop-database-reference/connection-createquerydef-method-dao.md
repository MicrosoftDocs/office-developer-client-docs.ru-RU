---
title: Метод Connection. CreateQueryDef (DAO)
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
localization_priority: Normal
ms.openlocfilehash: b6600d4508a33a31098d6a2e7c92f5904beb0e95
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295935"
---
# <a name="connectioncreatequerydef-method-dao"></a>Метод Connection. CreateQueryDef (DAO)

**Область применения**: Access 2013, Office 2013

Создает новый объект **[QueryDef](querydef-object-dao.md)**.

## <a name="syntax"></a>Синтаксис

*expression* .CreateQueryDef(***Name***, ***SQLText***)

*выражение*: переменная, представляющая объект **Connection**.

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
<td><p>Необязательно заполнять.</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Объект типа <strong>Variant</strong> (подтип <strong>String</strong>), однозначно определяющий новый объект <strong>QueryDef</strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>SQLText</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Объект <strong>Variant</strong> (подтип <strong>String</strong>), представляющий инструкцию SQL, которая определяет объект <strong>QueryDef</strong>. Если не указать этот аргумент, вы можете определить объект <strong>QueryDef</strong>, задав его свойство <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> до или после его добавления к коллекции.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

QueryDef

## <a name="remarks"></a>Примечания

В рабочей области Microsoft Access, если указать в качестве имени какое-либо значение, кроме строки нулевой длины, при создании объекта **QueryDef**, полученный объект **QueryDef** будет автоматически добавлен к коллекции **[QueryDefs](querydefs-collection-dao.md)**.

Если объект, указанный по имени, уже является элементом коллекции **QueryDefs**, возникает ошибка во время выполнения. Вы можете создать временный объект **QueryDef**, указав в качестве имени строку нулевой длины при выполнении метода **CreateQueryDef**. Это также можно сделать, указав строку нулевой длины ("") в качестве значения свойства **[Name](connection-name-property-dao.md)** нового объекта **QueryDef**. Временные объекты **QueryDef** полезны, если требуется регулярно использовать динамические инструкции SQL, не создавая постоянных объектов в коллекции **QueryDefs**. Временный объект **QueryDef** невозможно добавить к какой-либо коллекции, так как строка нулевой длины не является допустимым именем постоянного объекта **QueryDef**. Вы всегда можете задать свойства **Name** и **SQL** нового объекта **QueryDef**, а затем добавить объект **QueryDef** к коллекции **QueryDefs**.

Чтобы выполнить инструкцию SQL в объекте **QueryDef**, используйте метод **[Execute](connection-execute-method-dao.md)** или **[OpenRecordset](connection-openrecordset-method-dao.md)**.

Использование объекта **QueryDef** является предпочтительным способом выполнения SQL-запросов к серверу с базами данных ODBC.

Чтобы удалить объект **QueryDef** из коллекции **QueryDefs** в базе данных ядра СУБД Microsoft Access, используйте метод **[Delete](fields-delete-method-dao.md)** для этой коллекции.

