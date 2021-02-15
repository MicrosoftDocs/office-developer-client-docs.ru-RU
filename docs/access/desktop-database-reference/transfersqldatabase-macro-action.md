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

В проекте Access действие **TransferSQLDatabase** можно использовать для передачи базы данных Microsoft SQL Server 7.0 или более поздней в другую базу данных SQL Server 7.0 или более поздней. Дополнительные сведения о передаче базы данных см. в SQL Server документации.

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
<td><p>Имя сервера базы данных SQL Server 7.0 или более поздней копии.</p></td>
</tr>
<tr class="even">
<td><p><strong>База данных</strong></p></td>
<td><p>Имя новой базы данных, которая будет создана на сервере назначения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Использование доверенного подключения</strong></p></td>
<td><p>Сообщает, существует ли надежное подключение к SQL Server. Если за <strong>установлено "Да",</strong>то существует <strong></strong> надежное подключение, а аргументы <strong>входа</strong> и пароля не требуются. Если за <strong>установлено "Нет",</strong>необходимы аргументы <strong>входа</strong> и пароля. <strong></strong> Значение по умолчанию <strong>— Да.</strong> При использовании доверенного подключения система SQL Server с безопасностью операционной системы Windows, обеспечивая единый вход в сеть и базу данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>Вход</strong></p></td>
<td><p>Имя входа на сервер назначения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Password</strong></p></td>
<td><p>Пароль для <strong>аргумента Login.</strong> Этот пароль хранится в проекте Access в виде текста, но скрыт во время операции переноса базы данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>Передача данных копии</strong></p></td>
<td><p>Указывает, следует ли включать данные в операцию передачи базы данных. Если за <strong>установлено "Да",</strong>все данные включаются во все таблицы, а также все структуры данных, расширенные свойства и объекты баз данных. Если за <strong>установлено "Нет",</strong>данные из таблиц не включаются. На конечном сервере создаются только структура таблицы и расширенные свойства, а также все остальные объекты базы данных (кроме схем базы данных). Значение по умолчанию <strong>— Да.</strong></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

Нельзя выполнять другие операции во время переноса базы данных.

Действие **TransferSQLDatabase** по умолчанию копирует данные, определения данных, объекты базы данных и расширенные свойства, такие как значения по умолчанию, текстовые ограничения и значения поиска.

Существуют требования для передачи базы данных:

- Необходимо быть участником роли sysadmin на сервере назначения (на сервере-источнике не требуется специальная роль).

- Текущий SQL к проекту Access и сервер назначения, на который вы переносите базу данных, должен быть SQL Server версии 7.0 или более поздней.

  > [!NOTE]
  > Связанные серверы не переносятся во время операции передачи базы данных.

Чтобы запустить **действие TransferSQLDatabase** в модуле Visual Basic для приложений (VBA), используйте метод **TransferSQLDatabase** объекта **DoCmd.**

