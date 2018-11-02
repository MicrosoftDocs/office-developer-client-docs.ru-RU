---
title: Макрокоманда RunMenuCommand
TOCTitle: RunMenuCommand macro action
ms:assetid: cc4a4f72-0c73-91b7-8cec-6cbcda7e5b1c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834420(v=office.15)
ms:contentKeyID: 48547735
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm6446
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f01fc72a620e5c08a6f98b4b69a8eb8da7b98bbb
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925676"
---
# <a name="runmenucommand-macro-action"></a>Макрокоманда RunMenuCommand


**Применимо к**: Access 2013, Office 2013

Действие **RunMenuCommand** можно использовать для выполнения встроенных команды Microsoft Access.

## <a name="setting"></a>Параметр

Действие **RunMenuCommand** имеет аргумент следующие действия.

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
<td><p><strong>Команда</strong></p></td>
<td><p>Имя команды, которые необходимо выполнить. Поле <strong>команда</strong> отображает доступные встроенными командами в клиенте в алфавитном порядке. Обязательный аргумент.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Действие **RunMenuCommand** можно использовать для выполнения команды Microsoft Access из меню, глобальной строки меню, пользовательского контекстного меню или глобального контекстного меню.

Действие **RunMenuCommand** можно использовать в макросе с условного выражения для выполнения команды в зависимости от определенных условий.


> [!NOTE]
> <P>Перейдите на вкладку <STRONG>файл</STRONG> и затем выбрав <STRONG>последние</STRONG> показывает недавно использованные базы данных. Можно щелкнуть один из этих баз данных, не нажимая <STRONG>Open</STRONG>. Эти элементы базы данных в поле раскрывающегося списка для аргумента <STRONG>команды</STRONG> не отображаются и не доступны с помощью <STRONG>RunMenuCommand</STRONG> действия в макросе.</P>



При преобразовании базы данных Access из предыдущей версии Access некоторые команды могут быть доступны. Команда может была переименована, перемещена в другое меню или больше не может быть доступно в клиенте. Действия **DoMenuItem** для таких команд невозможно привести к **RunMenuCommand** действия. При открытии макрос, будет показан действие **RunMenuCommand** с пустым аргумент **команды** для команды. Измените макрос и введите аргумент допустимой команды или удаление **RunMenuCommand** действия.

Чтобы выполнить действие **RunMenuCommand** в Visual Basic для приложений (VBA) модуль, используйте метод **ВыполнитьКоманду** объекта **приложения** . (Это эквивалентно метод **ВыполнитьКоманду** **объекта** .)

