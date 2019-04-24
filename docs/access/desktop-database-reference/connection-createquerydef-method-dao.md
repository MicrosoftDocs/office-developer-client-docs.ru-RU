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

Создает новый объект **[QueryDef](querydef-object-dao.md)** .

## <a name="syntax"></a>Синтаксис

*Expression* . CreateQueryDef (***имя***, ***склтекст***)

*Expression (выражение* ) Переменная, представляющая объект **Connection** .

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
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (подтип<strong>String</strong> ), уникально названный новому <strong>QueryDef</strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>Склтекст</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Variant</strong> (подтип<strong>String</strong> ), который представляет собой инструкцию SQL, определяющую объект <strong>QueryDef</strong>. Если опустить этот аргумент, можно определить объект <strong>QueryDef</strong> , задав его свойство <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> перед добавлением в коллекцию или после него.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

QueryDef

## <a name="remarks"></a>Замечания

Если при создании объекта **QueryDef**в рабочей области Microsoft Access для имени указана любая строка, отличная от нулевой длины, полученный объект **QueryDef** автоматически добавляется в коллекцию **[QueryDef](querydefs-collection-dao.md)** .

Если объект, указанный по имени, уже является членом коллекции **QueryDef** , возникает ошибка времени выполнения. Вы можете создать временный объект **QueryDef** , используя строку нулевой длины для аргумента name при выполнении метода **CreateQueryDef** . Это также можно сделать, задав для свойства **[Name](connection-name-property-dao.md)** созданного экземпляра **QueryDef** пустую строку (""). Временные объекты **QueryDef** удобно использовать, если вы хотите многократно использовать динамические инструкции SQL без необходимости создавать новые постоянные объекты в коллекции **QueryDef** . Невозможно добавить временный объект **QueryDef** в коллекцию, так как строка нулевой длины не является допустимым именем для постоянного объекта **QueryDef** . Вы всегда можете задать свойства **Name** и **SQL** нового объекта **QueryDef** , а затем добавить объект **QueryDef** в коллекцию **QueryDef** .

Чтобы выполнить инструкцию SQL в объекте **QueryDef** , используйте метод **[EXECUTE](connection-execute-method-dao.md)** или **[OpenRecordset](connection-openrecordset-method-dao.md)** .

Использование объекта **QueryDef** является предпочтительным способом выполнения запросов к серверу SQL с помощью баз данных ODBC.

Чтобы удалить объект **QueryDef** из коллекции **QueryDef** в базе данных ядра СУБД Microsoft Access, используйте метод **[Delete](fields-delete-method-dao.md)** в коллекции.

