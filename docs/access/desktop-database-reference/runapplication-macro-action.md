---
title: Макрокоманда RunApplication
TOCTitle: RunApplication macro action
ms:assetid: 29967e6e-c441-b115-3ee6-2299b8a3bc25
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192038(v=office.15)
ms:contentKeyID: 48543885
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm93359
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: e7bf54934c6be215b2be5f32160d74fc2b4ab346
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306841"
---
# <a name="runapplication-macro-action"></a>Макрокоманда RunApplication

**Область применения**: Access 2013, Office 2013

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Заметка о безопасности" alt="Security note" /><strong>Заметка о безопасности</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Будьте осторожны при запуске исполняемых файлов или кода в макросах и приложениях. Исполняемые файлы или код могут использоваться для выполнения действий, которые могут скомпрометировать безопасность компьютера и данных.</td>
</tr>
</tbody>
</table>

Действие **RunApplication** можно использовать для запуска приложения microsoft Windows или MS-DOS, например Microsoft Excel, Microsoft Word или Microsoft PowerPoint из Microsoft Access. Например, может потребоваться вклеить Excel таблицы в базу данных Access.

> [!NOTE]
> Эта макрокоманда доступна только для доверенных баз данных. 

## <a name="setting"></a>Параметр

Действие **RunApplication** имеет следующий аргумент.

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
<td><p><strong>Командная строка</strong></p></td>
<td><p>Командная строка, используемая для запуска приложения (включая путь и любые другие необходимые параметры, например переключатели, которые запускают приложение в определенном режиме). Введите строку команд в поле <strong>Командная строка</strong> в разделе <strong>Аргументы</strong> действий области Macro Builder. Обязательный аргумент.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Приложение, выбранное с помощью этого действия, загружается и запускается на переднем плане. Макрос, содержащий это действие, продолжает работать после запуска приложения.

Вы можете передавать данные между другим приложением и Access с помощью средства Windows динамического обмена данными (DDE) или буфера обмена данными. Вы можете использовать **действие SendKeys** для отправки нажатия клавиш в другое приложение (хотя DDE является более эффективным методом для передачи данных). Вы также можете обмениваться данными между приложениями с помощью автоматизации.

Приложения на основе MS-DOS работают в окне MS-DOS в Windows среде.

В Windows операционных системах существует несколько способов запуска приложения, включая запуск программы с Windows Explorer, использование  команды Run в меню Пуск и дважды щелкнуть значок программы на Windows Desktop. 

Действие **RunApplication** нельзя выполнить в модуле Visual Basic для приложений (VBA). Вместо этого используйте функцию VBA **Shell.**

