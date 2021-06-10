---
title: Макрокоманда TransferSQLDatabase
TOCTitle: TransferSQLDatabase macro action
ms:assetid: 8cb95e22-f1f0-6c70-7dcb-3a3e9aafdc57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197344(v=office.15)
ms:contentKeyID: 48546244
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm111536
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5ed20555726d0a6f63f0e48fb154cedb411ef8cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306848"
---
# <a name="transfersqldatabase-macro-action"></a>Макрокоманда TransferSQLDatabase

**Область применения**: Access 2013, Office 2013

В проекте Access вы можете использовать действие **TransferSQLDatabase** для передачи базы данных Microsoft SQL Server 7.0 или более поздней базы данных в другую SQL Server 7.0 или более поздней базе данных. Дополнительные сведения о передаче базы данных см. в SQL Server документации.

> [!NOTE]
> Эта макрокоманда доступна только для доверенных баз данных.

## <a name="setting"></a>Параметр

Действие **TransferSQLDatabase** имеет следующие аргументы.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент макрокоманды</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Server</strong></p></td>
<td><p>Имя сервера SQL Server 7.0 или более поздней базы данных, на который вы копируете.</p></td>
</tr>
<tr class="even">
<td><p><strong>База данных</strong></p></td>
<td><p>Имя новой базы данных, которая будет создана на сервере назначения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Использование надежного подключения</strong></p></td>
<td><p>Засвидекторирует, есть ли надежное подключение к SQL Server. Если <strong>установлено да,</strong>то есть доверяемая <strong></strong> связь, и аргументы <strong>входа</strong> и пароля не требуются. Если <strong>установлено нет,</strong>необходимо использовать аргументы <strong>Login</strong> и <strong>Password.</strong> По умолчанию — <strong>Да.</strong> При использовании надежного подключения SQL Server безопасности интегрируется с безопасностью Windows операционной системы для обеспечения единого входа в сеть и базу данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>Вход</strong></p></td>
<td><p>Имя входа на сервер назначения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Password</strong></p></td>
<td><p>Пароль для <strong>аргумента Login.</strong> Этот пароль хранится в виде текста в проекте Access, но скрыт во время операции базы данных передачи.</p></td>
</tr>
<tr class="even">
<td><p><strong>Передача данных копирования</strong></p></td>
<td><p>Указывает, следует ли включать данные в операцию базы данных передачи. При наборе <strong>Да</strong>все данные включаются для всех таблиц, а также для всех структур данных, расширенных свойств и объектов базы данных. При наборе <strong>"Нет"</strong>данные из таблиц не включаются. На сервере назначения создаются только структура таблицы и расширенные свойства, а также все другие объекты базы данных (кроме схем баз данных). По умолчанию — <strong>Да.</strong></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Вы не можете выполнять другие операции во время переноса базы данных.

Действие **TransferSQLDatabase** по умолчанию копирует данные, определения данных, объекты баз данных и расширенные свойства, такие как значения по умолчанию, текстовые ограничения и значения поиска.

Для передачи базы данных существуют требования:

- Вы должны быть членом роли sysadmin на сервере назначения (не требуется специальная роль на исходный сервер).

- Текущий SQL, подключенный к проекту Access и серверу назначения, который вы переносите, должен быть SQL Server версии 7.0 или более поздней версии.

  > [!NOTE]
  > Связанные серверы не передаются во время операции передачи базы данных.

Чтобы выполнить действие **TransferSQLDatabase** в модуле Visual Basic для приложений (VBA), используйте метод **TransferSQLDatabase** объекта **DoCmd.**

